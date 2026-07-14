Data Criada: 30/05/2026 às 22:29
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

# Introdução

Um dos teoremas mais importante da análise é o teorema do valor médio, que começaremos a provar agora.

> [!definicao]
> Seja $f:[a, b] \rightarrow R$. Um ponto $x_{*} \in [a, b]$ é dito um **máximo** de $f$ se $f(x) \leqslant f\left(x_*\right)$ para todo $x \in[a, b]$.

**Obs.** Pelo [[teorema do valor extremo]], se $f$ for contínua, então $f$ tem pelo menos um máximo $x_*$.

**Obs.** O máximo pode não ser único, basta pensar na função seno.

> [!teorema] Teorema 1.
> Seja $f:(a, b) \rightarrow \mathbb{R}$ e seja $x_{*}$ um máximo de $f$. Se $f$ for diferenciável em $x_*$, então $f^{\prime}\left(x_*\right)=0$.

> [!demonstracao]-
> Sabemos por hipótese que o limite **existe** e é o **mesmo** para **qualquer sequência**. Portanto, podemos escolher duas sequências particulares (uma crescente e outra decrescente) e os resultados de ambas devem ser iguais.
> 
> Em outras palavras, estamos nos aproximando do ponto pela esquerda e pela direita para obter informações diferentes sobre a derivada.
> 
> Como $f(x_*)$ é um máximo, é fácil identificar o sinal das derivadas. Poderia ser também que tivéssemos uma sequência de máximos, fazendo com que a derivada fosse igual a zero.
> 
> **Obs.** Essa prova tem um pequeno erro, porque está assumindo que sempre pode ter uma sequência crescente que converge a $x_*$. Isso pode ser feito pelo método da **bisseção**:
> 
> Montamos a sequência $x_n$ tal que $x_1 = \dfrac{a+x_*}{2} \;$ e $\; x_{n+1} = \dfrac{x_n + x_*}{2}$. Isso é uma sequência estritamente crescente que converge a $x_*$ e nenhum desses ponto é igual a $x_*$ e podemos calcular a distância exata: $\dfrac{x_* - a}{2^n}$.

Note-se que num intervalo aberto, não vale o teorema do valor extremo. Logo, $f$ não necessariamente tem um máximo, mesmo se ela for contínua. Então, a existência do máximo $x_{*}$ é uma hipótese do teorema.

Esse teorema só precisa que $f$ seja diferenciável em um único ponto e não no intervalo inteiro. Isso vai se mostrar no Teo. do valor médio.


> [!teorema] Teorema de Rolle.
> Seja $f: [a,b] \rightarrow \mathbb{R}$, contínua (em [a,b]) e diferenciável em (a,b). Se
> $
> f(a) = f(b)
> $
> então existe $x_* \in (a,b)$ tal que $f'(x_*)=0$.
> 
> ![[Pasted image 20260531003430.jpg|center|500]]

Um mnemônico útil desse teorema é: se saírmos de casa para um passeio e voltarmos, haverá algum momento no qual não estaremos nem indo, nem vindo.

Esse teorema é consequência do teorema do valor extremo e do teorema anterior.


# Declaração e provas

Esse teorema é, na verdade, uma consequência imediata do Teorema de Rolle.

> [!teorema]
> Seja $f:[a, b] \rightarrow \mathbb{R}$ contínua em $[a, b]$ e diferenciável em $(a, b)$. Existe $x_* \in(a, b)$ tal que
> 
> $
> f^{\prime}\left(x_*\right)=\frac{f(b)-f(a)}{b-a} .
> $
> 
> ![[Pasted image 20260531005826.jpg|center|400]]

O teorema do valor médio nos diz que existe um ponto onde a inclinação da reta tangente ao gráfico da função é igual à inclinação dessa reta em rosa (é uma translação dela).

> [!demonstracao]
> Ao invés de considerar a função $f$, a gente considera a diferença entre $f$ e a reta:
> $
> g(x)=f(x)-\frac{(x-a)(f(b)-f(a))}{b-a} \text {, }
> $
> Por hipótese, essa diferença começa em zero e termina em zero. Então, pra essa função $g(x)$, o teorema de Rolle vale.
> 
> Se fizermos a conta, vemos que
> $
> g^{\prime}(x)=f^{\prime}(x)-\frac{f(b)-f(a)}{b-a}
> $
> Portanto, quando $g'(x)=0$, temos $f'(x) = \dfrac{f(b)-f(a)}{b-a}$, isto é, a derivada da $f$ é igual à inclinação dessa reta rosa.

**Obs.** Um detalhe técnico muito importante que passa despercebido à primeira vista é que não foi necessário assumir que $f'$ é contínua (afinal, o Teo. de Rolle só assume que $f$ é dif. num único ponto). Se fosse, esse teorema seria uma consequência do [[teorema do valor intermediário]].
	É difícil imaginar uma função que seja diferenciável e que não tenha uma derivada contínua, mas existe.

**Obs.** A prova do teorema do valor médio não parece tão difícil. A dificuldade está escondida na prova do [[teorema do valor extremo]]. Princípio da conservação da dificuldade: uma prova muito simples dum teorema pode acontecer por:
* ela esconde a dificuldade num outro teorema conhecido, que é difícil.
* ela prova um caso particular do teorema mais geral.


> [!exemplo]
> 


Considere a sequência $\left(x_n ; n \in \mathbb{N}\right)$ definida como $x_0=1$ e $x_n=\cos \left(x_{n-1}\right)$ para todo $n \in \mathbb{N}$. A ideia é analisar esta sequência e provar que converge a um ponto $x_*$ tal que $\cos \left(x_*\right)=x_*$. Temos que
$$
\begin{aligned}
x_{n+1}-x_n & =\cos \left(x_n\right)-\cos \left(x_{n-1}\right)=\frac{\cos \left(x_n\right)-\cos \left(x_{n-1}\right)}{x_n-x_{n-1}}\left(x_n-x_{n-1}\right) \\
& =-\operatorname{sen}\left(y_n\right)\left(x_n-x_{n-1}\right),
\end{aligned}
$$
Precisamos de um pequeno argumento para dizer que isso é diferente de zero, mas vamos em frente de depois voltamos nisso.

Fazemos essa manipulação e o que aparece é o enunciado do teorema do valor médio:
$$
\frac{\cos \left(x_n\right)-\cos \left(x_{n-1}\right)}{x_n-x_{n-1}} = \frac{f(b)-f(a)}{b-a}
$$
Ele nos diz que essa expressão é igual à derivada da função $\cos$ avaliada em algum ponto entre $x_{n}$ e $x_{n-1}$,o qual chamaremos de $y_{n}$.

Agora vemos que, se $x_{n}=x_{n-1}$, estaria tudo certo na conclusão, apesar de que o passo intermediário só vale quando $x_{n} \neq x_{n-1}$.





onde $y_n$ está entre $x_{n-1}$ e $x_n$. Notemos que $|\cos (x)| \leq 1$ para todo $x \in \mathbb{R}$, pelo que $\left|x_n\right| \leqslant 1$ para todo $n$. Como a imagem de $[0,1]$ por $\cos (x)$ está contida em $[\cos(1), 1]$, $x_n \geqslant \cos (1)$ para todo $n \in \mathbb{N}$. Como $\operatorname{sen}(x)$ é crescente em $[-\pi / 2, \pi / 2]$, $\operatorname{sen}\left(y_n\right) \in[0, \operatorname{sen}(1)]$. Concluímos que
$$
\left|x_{n+1}-x_n\right| \leqslant \operatorname{sen}(1)\left|x_n-x_{n-1}\right|
$$

e recursivamente $\left|x_n-x_{n-1}\right| \leqslant \operatorname{sen}(1)^n\left|x_1-x_0\right|$. Pelo teste de Weierstrass, $\left(x_{n ;} n \in \mathbb{N}\right)$ converge a um ponto $x_*$. Como a função $\cos (x)-x$ é contínua, temos que

$$
0=\lim _{n \rightarrow \infty}\left(x_{n+1}-\cos \left(x_n\right)\right)=x_*-\cos \left(x_*\right) .
$$
Estamos usando a linearidade da [[continuidade]] para montar a função contínua $\cos (x)-x$, pelo que seu limite existe. Agora, usamos a linearidade das [[Propriedades dos limites]] para calculá-lo de fato.

Dizemos que $x_{*}$ é o **ponto fixo** da função cosseno. Um ponto fixo da função $f$ é uma solução da equação $f(x)=x$, ou seja, o zero da função $f(x)-x$.




**Obs.**
O teste de Weierstrass nos diz que a sequência $x_{n}$ vai ser convergente se a soma 
$$
\sum_{i=1}^{N} \lambda^{n}|x_{1}-x_{0}|
$$
for limitada por uma constante. E de fato é:
$$
\sum_{i=1}^{N} \lambda^{n}|x_{1}-x_{0}| = \frac{1-\lambda^{n}}{1-\lambda} |x_{1}-x_{0}| \leqslant \frac{|x_{1}-x_{0}|}{1-\lambda}
$$
Logo, essa sequência $x_{n}$ é convergente, pelo que possui um limite, que chamaremos de $x_{*}$.





Problema de ponto fixo: se apertarmos na calculadora a operação $\cos(1)$, chegaremos muito perto de um valor fixo a partir de certo ponto.

Essa é uma **sequência contrativa**, isto é, existir uma constante $M \in (0, 1)$ tal que para todo número natural $n$:
$$
\vert{}x_{n+2} - x_{n+1}\vert{} \leq M \vert{}x_{n+1} - x_{n}\vert{}
$$
Algumas propriedades
* **Convergência:** toda sequência contrativa é uma sequência de Cauchy e, portanto, sempre convergente.
* **Contração Contínua:** Essa propriedade é a base do famoso Teorema do Ponto Fixo de Banach.
* **Estimativa de Erro:** O valor de $M$ permite calcular o quão rápido a sequência se aproxima do seu limite final.





