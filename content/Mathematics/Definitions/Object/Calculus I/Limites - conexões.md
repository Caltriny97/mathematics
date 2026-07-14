Data Criada: 14/06/2026 às 14:08
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Os limites reúnem ideias e estratégias que, apesar de complexas, escondem ideias comuns e intuitivas.

**Indeterminações**
Conforme dito em [[Propriedades dos limites]], as indeterminações são, a princípio, limites que não sabemos como se comportam de imediato. Para solucioná-los, é necessário fazermos uma análise mais delicada do comportamento da sequência. 

Geralmente, tais problemas envolvem sequências com comportamentos extremos, como por exemplo, $\lim_{ n \to \infty }x_{n}y_{n}$, onde $x_{n} \rightarrow \infty$ e $y_{n} \rightarrow 0$. Isso é uma indeterminação e precisamos analisar $x_{n}$ e $y_n$. Geralmente, tais problemas envolvem uma sequência que de fato têm um comportamento extremos e outra que pode ser limitada por uma constante. Nesse caso, usamos o resultado visto na lista 11

> [!teorema]
> Seja $f:(a, b) \rightarrow \mathbb{R}$ diferenciável em $x \in(a, b)$. Sejam $\left(x_n ; n \in \mathbb{N}\right),\left(y_n ; n \in \mathbb{N}\right)$ e $M \in \mathbb{R}$ tais que
> 
> $
> \lim _{n \rightarrow \infty} x_n=0 \text { e }\left|y_n\right| \leq M \text { para todo } n \in \mathbb{N} .
> $
> 
> 
> Temos que
> 
> $
> \lim _{n \rightarrow \infty} x_n y_n=0 .
> $

> [!obs]
> Quando falamos em limitar uma sequência por uma constante, tais problemas envolvem achar um máximo para tal sequência.
> 
> Quando essas sequência envolvem somatório indefinido, não basta limitarmos cada um dos termos do somatório, pois eles ainda dependerão de $N$. Temos que limitar todo o somatório! Ver exercícios da aula 22.

> [!obs] Indeterminação.
> * Imagine que $x_n$ vai para infinito e $y_n$ vai para zero. Se o limite $\lim _{n \rightarrow \infty} x_n y_n=0$ existe, nós não podemos separá-lo pela propriedade do limite. Só podemos fazer isso quando sabemos que o limite existe e é um número real.
> * Agora, se nós temos as duas sequências acima e queremos calcular o limite da combinação delas duas, tudo bem (nós só precisaremos analisá-las para saber quem vence a disputa). Aqui, estaremos aplicando o conceito de continuidade: se as partes são contínuas, o todo também é. Perceba que temos 3 possibilidades para o resultado do limite dessa combinação:
> 	- Exemplo 1: Se $a_n = n^2$ e $b_n = \frac{1}{n}$, o produto é $n^2 \cdot \frac{1}{n} = n$, que converge para $\infty$.
> 	- Exemplo 2: Se $a_n = n$ e $b_n = \frac{1}{n^2}$, o produto é $n \cdot \frac{1}{n^2} = \frac{1}{n}$, que converge para $0$.
> 	- Exemplo 3: Se $a_n = n$ e $b_n = \frac{5}{n}$, o produto é $n \cdot \frac{5}{n} = 5$, que converge para $5$.




Teste de Weierstrass
Sequências de cauchy
convergência
pontos fixos
