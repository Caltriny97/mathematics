Data Criada: 06/06/2026 às 23:27
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

Uma fórmula de derivação muito importante é a regra da cadeia ([[Propriedades da derivada]]):

$$
(f \circ g)^{\prime}(x)=f^{\prime}(g(x)) \cdot g^{\prime}(x) .
$$

Vejamos o que mos diz esta fórmula as usar o [[O Teorema Fundamental do Cálculo|TFC]]:

$$
\underbrace{f(g(b))-f(g(a))}_{*}=\int_a^b f^{\prime}(g(x)) g^{\prime}(x) d x .
$$
Essa é a fórmula de mudança de variáveis, que relaciona algo que sabemos calcular (lado esquerdo) com algo que a princípio não sabemos (lado direito).

Notemos que

$$
\int_a^b f^{\prime}(g(x)) g^{\prime}(x) d x=\underbrace{\int_{g(a)}^{g(b)} f^{\prime}(y) d y}_{\text{igual a} \;*\; \text{pelo TFC}} .
$$

Lembrando que a integral duma derivada é a função avaliada nos extremos de integração. 

> [!obs]
> A notação de Leibniz nos permite resumir este cálculo (já rigorosamente demonstrado pela regra da cadeia) da seguinte forma:
> $
> \begin{aligned}
> & y=g(x) \Rightarrow \frac{d y}{d x}=g^{\prime}(x) \Rightarrow d y=g^{\prime}(x) d x \\
> \Rightarrow & \int f^{\prime}(g(x)) g^{\prime}(x) d x=\int f^{\prime}(y) d y=f(y)=f(g(x)) \\
> \Rightarrow & \int_a^b f^{\prime}(g(x)) g^{\prime}(x) d x=f(g(b))-f(g(a)) .
> \end{aligned}
> $


# Exemplo

**Exemplo:** Seja $n \in \mathbb{N}$. Calcule a integral

$$
\int_0^{\pi / 4} \operatorname{sen}^n(x) \cos (x) d x .
$$


**(i)** Notemos que $\cos (x)=(\operatorname{sen})^{\prime}(x)$. Logo, usando $f(x)=\cfrac{x^{n+1}}{n+1}$ e $g(x)=\operatorname{sen}(x)$, vermos que

$$
\begin{aligned}
\int_0^{\pi / 4} \operatorname{sen}^n(x) \cos (x) d x & =\int_0^{\pi / 4} f^{\prime}(g(x)) g^{\prime}(x) d x=\left.f(g(x))\right|_0 ^{\pi / 4} \\
& =\frac{\operatorname{sen}^{n + 1}(\pi / 4)-\operatorname{sen}^{n+1}(0)}{n+1}=\frac{1}{(n+1) 2^{\frac{n+1}{2}}}
\end{aligned}
$$


**(ii)** Usando a notação de integral indefinida de Leibniz:

$$
\begin{aligned}
\int \operatorname{sen}^n(x) \cos (x) d x & =\int \operatorname{sen}^n(x) \; d \operatorname{sen}(x) =\frac{\operatorname{sen}^{n+1}(x)}{n+1}+C
\end{aligned}
$$

Portanto,
$$
\int_0^{\pi / 4} \operatorname{sen}^n(x) \cos (x) d x=\left.\left(\frac{\operatorname{sen}^{n+1}(x)}{n+1}+c\right)\right|_0 ^{\pi / 4}=\frac{1}{(n+1) 2^{n / 2}} .
$$

Note que, primeiro nós calculamos a antiderivada e depois a aplicamos nos limites de integração para calcular a integral definida. Por isso, a constante desaparece (às vezes, ela pode ajudar nas contas...).


**(iii)** Usando notação de Leibniz ao máximo:
$$
\int \operatorname{sen}^n(x) \cos (x) d x=\int y^n d y=\frac{y^{n+1}}{n+1}=\frac{\operatorname{sen}^{n+1}(x)}{n+1}
$$
Usamos em sequência: $y=\sin(x) \rightarrow dy = \cos(x)dx \rightarrow dx = \cfrac{dy}{\cos (x)}$



# Não exemplo

A função $\tan(x)$ é integrável, porque ela é crescente no intervalo que vamos considerar. Note que em todas as contas que fazemos, devemos definir bem o domínio.

Toda função diferenciável é integrável... Toda função diferenciável é de Lipschitz e toda função de Lipschitz é integrável.

A substituição feita por $y=\cos(x); dy=-\sin(x) \, dx$ em
$$
\int tg(x) = \int \frac{\sin(x)}{\cos(x)} \, dx = -\int \frac{dy}{y}
$$
é simplesmente uma maneira rápida de reescrever a fórmula de substituição sem ter que definir $f, g, f^{\prime}, f \circ g$, etc.


> [!container]
> A função $\cfrac{1}{x}$ não é derivada de nenhum polinômio. Por isso, a integral
> $
> \int x^{n} \, d = \frac{x^{n+1}}{n+1} 
> $
> a princípio não dá para calcular exato para $n=-1$. Para isso, definimos a função logaritmo.

> [!container]
> sejam $P(x)$ e $Q(x) \neq 0 \; \forall \; x$ polinômios. O polinômio
> $
> \frac{P(x)}{Q(x)}
> $
> é uma função racional. 
> 
> O conjunto das funções racionais é um [[A. Axiomas de Corpo|corpo]] não arquimediano (diferente dos reais), porque está sempre limitado pelos polinômios de grau maior. O ponto é: não dá para definir o que significa um polinômio ser maior ou menor que outro polinômio.
> 
> O interessante das funções racionais é que: a derivada de toda função racional é uma função racional pela regra da cadeia e da inversa: $\left( \frac{P}{Q} \right)^{\prime} = \frac{P^{\prime}Q-PQ^{\prime}}{Q^{2}}$.
> 
> Uma pergunta interessante em álgebra é: quais são as funções racionais que são derivadas da função racional? Nem todas as funções racionais são derivadas de uma função racional. Acabamos de ver um exemplo: $\frac{1}{x}$ é uma função racional e não é derivada de nenhuma outra.
> 
> Do ponto de vista do cálculo isso quer dizer que: existem funções que não dá para integrar facilmente. O que os matemáticos fazem nessas situações em Análise e Cálculo é: cada vez que encontram uma função integrável que não se sabe integrar de maneira explícita, inventa-se uma notação para isso. 
> 
> Isso nos leva à definição de função logaritmo:
> * [[A função logaritmo]]