Data Criada: 23/05/2026 às 11:45
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Essencialmente temos $3$ tipos de descontinuidade.

> [!definicao]
> Uma função $f:[a, b] \rightarrow \mathbb{R}$ é dita **contínua** no ponto $x \in[a, b]$, se para toda sequência $\left(x_{n};\right. n \in \mathbb{N})$ tal que
> $
> \begin{aligned}
> & \bullet x_n \in[a, b] \;\;\text{ para todo } n \in N, \\ \\
> & \bullet \lim _{n \rightarrow \infty} x_n=x,
> \end{aligned}
> $
> temos que
> $
> \lim _{n \rightarrow \infty} f\left(x_n\right)=f(x) .
> $

Tem uma questão que é importante, que é o domínio da definição da função. No nosso curso, quando falamos em função contínua, o domínio de definição da função vai ser sempre um **intervalo fechado**, por simples convenção do Milton.

Nossas suposições, hipóteses aqui são: a sequência $x_{n}$ tem limite (é uma sequência convergente) e que o limite está no domínio da função $f$.

> [!obs]
> A ideia é que, para calcular limites de sequências, a gente sai aplicando funções contínuas para simplificar até chegarmos num limite que a gente sabe calcular. Só que para isso, a gente tem que provar que as funções são contínuas antes, e isso é difícil.
> 
> Em outras palavras, temos um desafio: calcular um limite complicado. Para tanto, o mais comum é separá-lo em limites menores que sabemos o resultado. Para fazer essa separação, usamos as [[propriedades dos limites]]. Acontece que, para fazer isso, precisamos garantir que os limites das sequências menores existem, i.e., precisamos provar que elas descrevem funções contínuas.
> 
> O que estamos fazendo aqui é mudar o ponto de dificuldade do problema: de calcular o limite para provar que as funções menores são contínuas. Por isso que é importante mostrar que classes de funções (como as de Lipschitz) são contínuas.

Em resumo, limite e a função $f$ são comutativas no caso de funções contínuas. E isso é extremamente útil ao calcular limites de sequências feias.

> [!discussao]-
> É interessante pensar nas sequências como ferramentas de teste. Se a função é realmente contínua em $x$, não importa o caminho, os saltos ou a velocidade com que uma sequência de pontos $(x_n)$ decida viajar em direção a $x$ ; a função $f$ precisa ser organizada o suficiente para fazer com que as respostas $f(x_n)$ também viajem ordenadamente em direção ao alvo real $f(x)$.
> 
> Se existisse uma única sequência que converge para $x$, mas cujas imagens $f(x_n)$ fossem para outro lugar (ou ficassem oscilando), significaria que a função tem uma quebra, um salto ou um comportamento caótico exatamente naquele ponto.
> 
> O ponto é: as sequências podem ser tais que
> * No processo do limite, o alvo pode nunca ser tocado. De qualquer forma, o limite em si é o valor final exato. Quando você coloca o símbolo $\lim_{n \to \infty}$ na frente de $f(x_n)$, você não está mais perguntando _"onde os termos estão agora?"_, mas sim _"para qual coordenada única toda essa tendência aponta?"_. E essa coordenada única é **exatamente** $f(x)$.
> * Portanto, é possível que hajam sequências que toquem ou ultrapassem o alvo. Dizer que uma sequência "nunca chega" ao limite é uma verdade para exemplos clássicos (como $1/n$), mas a definição de continuidade exige que o comportamento funcione para **toda e qualquer** sequência que convirja para $x$. Isso inclui sequências "estranhas", como a sequência $x_n = x$ ou mesmo a sequência oscilatória $x_n = \frac{(-1)^{n/2}}{n}$ para $n$ par, e $0$ para $n$ ímpar passada em sala.


> [!definicao]
> Se $f:[a,b]\rightarrow \mathbb{R}$ for contínua em $x$ para todo $x \in [a,b]$ dizemos que $f$ é contínua em $[a,b]$.


> [!teorema]
> Se $f:[a,b]\rightarrow \mathbb{R}$ de Lipschitz. Temos que $f$ é contínua em $[a,b]$.

Ver demonstração na nota de aula 11.

> [!corolario]
> * Todo Polinômio é contínuo
> * A função $f(x)=\sqrt{x}$ é contínua em $[a,b]$ para todo $b \geqslant a \geqslant 0$.
> * Combinações lineares de funções de Lipschitz são contínuas.
> * As funções seno e cosseno são contínuas.


# Propriedades de funções contínuas

Conforme dito, para resolver o limite de uma sequência feia, nós a separamos em limites de sequências menores de acordo com as [[Propriedades dos limites]]. Mas, para tanto, precisamos saber de antemão se essas funções menores são contínuas (ver [[Continuidade]]).

Há várias formas de saber se uma função é contínua, como por exemplo:
1. pela definição de continuidade (necessária e suficiente).
2. mostrar que $f$ é de Lipschitz.
3. mostrar que $f$ é diferenciável.
4. pelas propriedades que vamos ver agora.

> [!discussao]- propriedades dos limites e propriedades de funções contínuas.
> As propriedades dos limites acontecem numa direção, enquanto as propriedades de funções contínuas acontecem na direção contrária. Como assim?
> 
> Para calcular um limite feio, nós o separamos em menores. Por exemplo, separamos o limite da combinação linear $\lim \alpha x_n + \beta y_n$ na combinação linear dos limites $\lim \alpha x_n + \lim \beta y_n$. Mas, para isso precisamos saber se $\alpha x_n$ e $\beta y_n$ são contínuas.
> 
> Para tanto, se optarmos pela técnica 4 acima, fazemos o caminho inverso: analisamos se podemos formar $\alpha x_n$ e $\beta y_n$ através de funções contínuas menores ainda.
> 
> É o que vamos ver agora.

As propriedades a seguir são consequências direta das propriedades análogas de limites (exceto a composicionalidade).

> [!teorema] Linearidade.
> Se $f$, $g$ são contínuas e $\alpha, \beta \in \mathbb{R}$, então
> $
> \alpha f + \beta g \;\; \text{é contínua}

> [!teorema] Multiplicatividade.
> Se $f,g$ são contínuas, então
> * $f \cdot g$ é contínua,
>   
> * $\cfrac{f}{g}$ é contínua se $g(x) \neq 0 \;\; \forall x$.

> [!teorema] Monotonicidade.
> Se $f,g$ são contínuas, então
> $
> x \mapsto \max \{f(x), g(x)\} \text { e } x \mapsto \min \{f(x), g(x)\}
> $
> são contínuas
> 
> ![[Pasted image 20260523163444.jpg|center|400]]

Uma observação importante é que, em todas essas propriedades, nós temos que nos atentar ao domínio das funções, porque para conseguir falar em combinação linear, multiplicação, etc, as funções $f$ e $g$ devem estar definidas no mesmo domínio. Se elas estiverem definidas em domínios diferentes, não podemos falar sobre nenhuma dessas operações. Ou então, nós podemos restringir essas funções a um domínio comum (uma intersecção não nula).


Uma propriedade "nova" em relação ao que vimos dos limites é

> [!teorema] Composicionalidade.
> Sejam f: $[a, b] \rightarrow [c, d]$ e $g:[c, d] \rightarrow \mathbb{R}$ contínuas. Então, $g \circ f:[a, b] \rightarrow \mathbb{R}$ dada por
> $
> g \circ f(x):=g(f(x)) \; \; \text { para todo } x \in[a, b]
> $
> é contínua.

> [!exemplo]
> * A função $\sin (1+x^2)$ é contínua, pois é a composição de duas funções contínuas, pois são de Lipschitz.
> * A função $\sqrt{1-x^2}$ tem um detalhe. A parte de dentro está bem definida para todo número real ($\mathbb{D} = \mathbb{R}$). Porém, a função de fora (raiz quadrada) só está definida para números não negativos, então precisamos que a **imagem** da primeira função esteja **contida no domínio** da segunda. Para resolver isso, nós restringimos o **domínio** da primeira função para que sua imagem esteja no "lugar certo". 


# Ferramentas para provar continuidade

Até agora, temos algumas ferramentas úteis para mostrar que uma dada função é contínua.
