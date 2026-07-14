Data Criada: 23/05/2026 às 16:19
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

Conceitualmente parecido, mas bem mais difícil matematicamente que o [[Teorema do Valor Intermediário]].
# Declaração e Provas

> [!teorema]
> Seja $f: [a,b] \rightarrow \mathbb{R}$ contínua. Existe $x_* \in [a,b]$ tal que
> $
> f(x) \leqslant f(x_*) \;\; \text{ para todo } \; x \in [a,b]
> $

Em outras palavras, ele nos diz que a função $f$ sempre tem uma máximo, i.e., um ponto no qual a função é maior do que o valor de qualquer outro lugar do intervalo.

Para que esse teorema seja verdade, é muito importante que o intervalo $[a,b]$ seja um intervalo **fechado** e **limitado**. Alguns exemplos clássicos que não seguem esse teorema são $f(x)=\frac{1}{x}$ e $f(x)=x^{2}$.

Obviamente, se dá pra achar o máximo, também dá pra achar o mínimo: é só considerar a função $\tilde{f}=-f$.

A demonstração do Milton é teoricamente importante, mas é impossível de ser implementada por um algoritmo computacional, pois ele teria que avaliar os valores de $f$ em todo o domínio. Ele começou a fazer uma outra que possibilitaria isso, mas não terminou (ela também não serve pra muita coisa, porque não nos retorna a velocidade de convergência).

Em outras palavras, a demonstração que vamos ver é uma construção algorítmica do ponto de vista matemático, mas não é algorítmica do ponto de vista computacional, pois não dá para calcular o supremo com uma máquina de Turing. O Axioma do supremo é um axioma adicional, i.e., ele está fora dos axiomas de corpo, algébricos para construir números reais (é a ponte dos números racionais para os reais).

> [!demonstracao]-
> A ideia da prova aqui é fazer a mesma coisa que fizemos para achar o zero duma função: método da bisseção.
> 
> Nós dividimos o conjunto pela metade e nos perguntamos: em qual dos dois lados está o máximo (isso é teórico, não é fazível na prática)?
> 
> Primeiro nós simplificamos nosso problema (ver [[SPG]]):
> * Podemos supor que $a=0$ e $b=1$ considerando a transformação $\tilde{f}(x):=f(a+(b-a)x)$ que mapeia o intervalo $[a,b]$ da nossa função original $\tilde{f}$.
> * Considerando $\tilde{f}(x)=\operatorname{tgh}(f(x))$, podemos supor que a função é limitada, porque a composição de $\tilde{f}$ com uma função limitada é automaticamente limitada (não interessa se $\tilde{f}$ é ou não). A princípio, a gente não sabe se a função $f$ vai ser limitada ou não. Porém, o teorema implica que $f$ é limitada.
> * Outro ponto é que o máximo de $\tilde{f}$ também vai no máximo da composição. Então, achar o máximo da tangente hiperbólica é a mesma coisa que achar o máxima da primeira função.
> 
> Agora, nós definimos dois intervalos $A_{n}$ e $B_{n}$
> * Para tanto, temos que ver se o máximo está à direita ou à esquerda. Só que, por enquanto, falar do máximo duma função não está bem definido, porque não sabemos se ela tem uma máximo (é nossa tese).
> * O que a função tem é um supremo porque ela é limitada.
> * Então, nós dividimos o intervalo $I_{n}$ em duas metades e olhamos para o supremo do lado esquerdo. Se ele for igual ao supremo do intervalo inteiro, quer dizer que o máximo está do lado esquerdo. Senão, está do lado direito (se houver dois máximo, esse algoritmo escolhe o do lado esquerdo).
> * Obs: aqui mora o porquê não se pode implementar esse algoritmo num computador. Uma máquina de Turing não consegue calcular supremo, pois deveria olhar uma quantidade infinita de números. A única saída seria assumir propriedades adicionais da função, não algo genérico.
> 
> Então, isso aqui é simplesmente a definição dos intervalos. Porém, nada nos garante que os extremos dos intervalos estejam pegando o máximo. Nessa construção, nada nos diz que os valores nos intervalos estão ficando próximos do máximo. Precisamos então de um mecanismo que nos diga se estamos ou não no máximo da função.
> * Esse mecanismo consiste em tomar o máximo como o supremo. Ou seja, vamos provar que existe um ponto tal que a função avaliada nesse ponto é o supremo.
> * **O que significa ser um supremo?** Quer dizer que dado qualquer número menor que $M$, sempre tem um valor da $f$ que está acima desse ponto.
> * Por construção, o supremo é o mesmo em cada um dos intervalos menores $I_{n}$. Logo, existe $x_{n} \in I_{n}$ tal que $f(x_{n}) \geqslant M -\frac{1}{n}$.
> * As sequências $a_n$ e $b_{n}$ convergem pro mesmo limite pelo mesmo argumento em [[Teorema do Valor Intermediário.pdf]].
> 
> Por fim, temos que
> $
> \begin{gather}
> \text{por continuidade,} \;\; f(x_{*})=\lim_{ n \to \infty } f(x_{n}) \\  \\
> 
> \text{por construção,} \;\; M-\frac{1}{n} \leqslant f(x_{n}) \leqslant M
> \end{gather}
> $
> Aplicando o limite nos termos da desigualdade e usando teorema do sanduíche, chegamos que $x_{*}$ é um **máximo** de $f$.

