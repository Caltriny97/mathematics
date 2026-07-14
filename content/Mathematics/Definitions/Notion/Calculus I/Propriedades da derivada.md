Data Criada: 30/05/2026 às 13:09
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Note que, para algumas propriedades serem verdade, só precisam que $f$ seja diferenciável num dado ponto. Já outras, no domínio inteiro da função.

> [!teorema] Linearidade.
> Sejam $f:(a, b) \rightarrow \mathbb{R}$, $g: (c, d) \rightarrow \mathbb{R}$ diferenciáveis em $x_0 \in(a, b) \cap(c, d)$. Para todo $\alpha, \beta \in \mathbb{R}, a$ função : $(a, b) \cap(c, d)$ dada por
> 
> $
> h(x):=\alpha f(x)+\beta g(x)
> $
> 
> para todo $x \in(a, b) \cap (c, d)$, é diferenciável em $x_0,$ e
> 
> $
> h^{\prime}\left(x_0\right)=\alpha f^{\prime}\left(x_0\right)+\beta g^{\prime}\left(x_0\right) .
> $


> [!teorema] Regra de Leibniz (ou do produto).
> Sejam $f, g: (a, b) \rightarrow \mathbb{R}$ diferenciáveis em $x_0 \in(a, b)$. temos que $fg$ é diferenciável em $x_0 \in(a, b)$ e que
> 
> $
> (f g)^{\prime}\left(x_0\right)=f\left(x_0\right) g^{\prime}\left(x_0\right)+f^{\prime}\left(x_0\right) g\left(x_0\right) .
> $

> [!demonstracao]
> Pontos importantes:
> * Lema: Se $f$ é **diferenciável** em $x_0$, então $f$ é **contínua** em $x_0$ (ver demonstração na nota de aula 15).
> * A linearidade do limite implica dizer que: se os limites existem, então o limite da soma também existe.
> * $ab - cd = a(b-d) + (a-c)d$


> [!teorema] Regra da Cadeia.
> Seja $f:(a, b) \rightarrow(c, d)$ diferenciável em $x_0$ e seja $g: (c, d) \rightarrow \mathbb{R}$ diferenciável em $f\left(x_0\right)$. Então $g \circ f$ édiferenciável em $x_0$ e
> 
> $
> (g \circ f)^{\prime}\left(x_0\right)=g^{\prime}\left(f\left(x_0\right)\right) f^{\prime}\left(x_0\right) .
> $

> [!demonstracao]-
> Note na nota de aula do Milton que a ideia das provas dessas regras de diferenciação é parecida: nós começamos com a razão (inclinação) que queremos calcular e reescrevemos essa sequência em função de outras sequências para as quais a gente sabe calcular o limite.
> 
> No caso, a gente sabe a derivada da $g$ e a da $f$, então a gente reescreve o quociente de $g \circ f$ em termos deles. Como a regra da cadeia é uma multiplicação, a gente tem que multiplicar em algum lugar.
> 
> Um ponto de atenção na demonstração é que: $x_n \neq x_0$ para todo $n$ não implica que $f(x_n) \neq f(x_0)$. Isso só seria verdade se $f$ fosse injetiva, mas só sabemos que $f$ é diferenciável. Ver ideia da prova mais formal na minha nota de aula 15.


> [!teorema] Derivada da função inversa.
> A regra da cadeia serve para calcular a derivada da função inversa: se $f$ for diferenciável em $x_0$ e $f^{-1}$ for diferenciável em $f\left(x_0\right)$, então
> 
> $
> \left(f^{-1}\right)^{\prime}\left(f\left(x_0\right)\right)=\frac{1}{f^{\prime}\left(x_0\right)} .
> $

> [!demonstracao]-
> O ponto aqui é fazermos a composição de $f$ com $f^{-1}$. De fato, da identidade
> $
> x=f^{-1}(f(x)),
> $
> 
> vemos que
> $
> 1=\left(f^{-1}\right)^{\prime}\left(f\left(x_0\right)\right) f^{\prime}\left(x_0\right) .
> $
> Esta conta tem dois problemas ne sua derivação. Primeiro, que precisamos **saber de antemão** que $f^{-1}$ é diferenciável pela hip. da regra da cadeia. E segundo, que se $f^{\prime}\left(x_0\right)=0$, não podemos dividir por $f^{\prime}\left(x_0\right)$ para obter a fórmula. E, conforme discutimos, não há um critério fácil para quando uma função é diferenciável. 
> 
> Em outras palavras, como não há critério fácil, nós provamos que uma função é diferenciável calculando sua derivada. Perceba que então caímos num argumento circular no caso da função inversa...
> 
> Afortunadamente, há um teorema que resolve ambos os problemas:
>   ad-teorema
title: Teorema da função inversa.
Seja $f:(a, b)$ diferenciável em **todo** ponto desse intervalo. Suponha que $f'$ é **contínua** em $(a, b)$. Seja $x \in (a, b)$ tal que $f^{\prime}(x)>0$. Existem $c, d \in(a, b)$ tais que:
* a) $f$ é bijetora em ( $c, d$ ) e $x \in(c, d)$,
* b) a inversa $f^{-1}$ é diferenciável em $\left(f(c), f(d)\right)$.

Em consequência,

$$
\left(f^{-1}\right)^{\prime}(f(x))=\frac{1}{f^{\prime}(x)} .
$$


Obs: Usando o teorema para  $-f$, vemos que ele também vale se $f^{\prime}(x)<0$.
```

Na prática, a fórmula usada é a seguinte:
$$
\left(f^{-1}\right)^{\prime}(y)=\frac{1}{f^{\prime}\left(f^{-1}(y)\right)} .
$$


> [!lema]
> Seja $f:(a, b) \rightarrow \mathbb{R}$ diferenciável em $x \in(a, b)$. Se $f(x) \neq 0$, então $1 / f$ é diferenciável em $x$ e
> $
> \left(\frac{1}{f}\right)^{\prime}(x)=-\frac{f^{\prime}(x)}{f(x)^2} .
> $

> [!demonstracao]-
> Na lista 9, calculamos a derivada de $\dfrac{1}{x_{n}}$, com $x_{n} \rightarrow x$. Agora, a função $\dfrac{1}{f}$ é a composição da função $f$ com a função $\dfrac{1}{x_{n}}$. Então, esse lema é simplesmente a regra da cadeia nessa composição.
> 
> Seja $h(x) := \frac{1}{x}$. Logo,
> $
> (h \circ f) (x) = h(f(x)) = \frac{1}{f(x)} = (f(x))^{-1}
> $



**Regra do quociente**
Como consequência do lema acima e da regra do produto, temos que
$$
\left(\frac{u}{v}\right)' = \frac{u'v - uv'}{v^{2}}
$$


# Derivada das funções trigonométricas

Vamos começar a aplicar as definições vistas na prática.

$$
\sin(x)'(x) = -\sin(x)
$$
Note-se que, a princípio, não sabemos se a sequência 
$$
\lim_{ n \to \infty } \frac{\sin(x_{n})-\sin(x)}{x_{n}-x}
$$
converge, ou seja, se esse limite existe. Mas nós vamos calculá-lo. Como subproduto do cálculo do limite, nós também provamos a sua existência.

A ideia aqui é igual às demonstrações das propriedades: escrever essa expressão em termos de outras as quais sabemos o limite. Como o seno é uma função explícita, podemos fazer operações mais explícitas, como as identidades trigonométricas.

Aqui, devemos usar o resultado $\lim_{x_{n} \to 0} \frac{\text{sen}(x_{n})}{x_{n}} = 1$, que é demonstrado a partir da desigualdade fundamental $\cos(x_{n})< \frac{\sin(x_{n})}{x_{n}} < \frac{1}{\cos(x_{n})}$. O Milton fez de outra forma (ver minha nota). Perceba que não precisamos "cortar" o $x_{n}-x_{0}$, mas foi necessário usar essa informação para conseguirmos calcular a derivada. O que foi feito foi:
$$
\begin{gather}
\text{Seja $\theta=\frac{x_n-x}{2}$. Logo, \;$x_n \rightarrow \infty $ \; se, e somente se, \; $\theta \rightarrow \infty$. Então,}  \\ \\
\lim _{n \rightarrow \infty} \frac{\operatorname{sen}\left(\frac{x_n-x}{2}\right)}{\frac{x_n-x}{2}} = \lim_{ \theta \to 0 } \frac{\sin (\theta)}{\theta} = 1
\end{gather}
$$
Junto disso, usamos o fato de que o $\cos$ é contínuo para calcular o valor de $\lim_{ n \to \infty }\cos\left( \frac{x_{n}+x}{2} \right)$.

> [!obs]
> Denotar $\theta \rightarrow 0$ é o mesmo que definir uma sequência $\theta_n$ tal que $\lim _{n \rightarrow \infty} \theta_n = 0$


Usando o lema da sessão anterior, conseguimos calcular a derivada da função tangente.

Para a função $\arcsin$, usamos a fórmula da inversa. O ponto interessante é analisar a restrição do intervalo no qual ela é definida para que a inversa esteja bem definida. Ver na minha nota um esquema. Por fim, veja na nota do Milton que a derivada do $\arcsin$ nos dá a raiz quadrada de um polinômio.