Data Criada: 10/04/2026 às 22:18
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Vamos definir agora **o que á a integral** de uma função **limitada** qualquer. Depois vamos nos concentrar em responder as seguintes perguntas:
* (i) Quais as funções limitadas que são **integráveis**, ou seja, cuja integral existe de fato? (vamos analisar funções monótonas, Lipschitz, polinomiais...)
* (ii) Sabido que uma função $f$ é integrável, como **calcular** o integral de $f$ ?


Nesta seção devemos formular uma definição de $\int_a^b f(x) d x$ que seja aplicável a funções $f$ mais gerais de tal modo que o integral dela resultante goze de todas as propriedades referidas em [[Partições e funções em escada]].

O método será inspirado no de Arquimedes: o [[Método da Exaustão]]: começamos por aproximar, por defeito e por excesso, a função $f$ por intermédio de funções em escada. O Andres fez isso direto na definição de partição: ver [[Aula 5.1  Funções Integráveis.pdf|nota]].

Há somente um **problema**: nem sempre é possível aproximar toda função por defeito ou por excesso, por intermédio de funções em escada. Por ex., a função $f(x)=\frac{1}{x}$ não é **limitada** nas vizinhanças da origem, pelo que nenhum intervalo $[a,b]$ que contenha a origem pode ser aproximado.

Portanto, devemos em primeiro lugar, restringir-nos àquelas funções que são **limitadas** em $[a,b]$, quer dizer, funções $f$ para as quais existe um número $M>0$ tal que
$$
-M\leq f(x) \leq M \quad\forall x \in [a,b]
$$

> [!definicao] Definição de integral de uma função limitada.
> Seja $f$ definida e limitada em $[a,b]$. Sejam $s$ e $t$ funções em escada arbitrárias definidas em $[a,b]$ e tais que
> $
> s(x) \leq f(x) \leq t(x)
> $
> para cada $x$ em $[a,b]$. Se existir um e um só número $I$, tal que
> $
> \int_a^b s(x) d x \leq I \leq \int_a^b t(x) d x
> $
> 
> para cada par de funções em escada s e t satisfazendo a (1.6), então este número 1 chama-se $o$ integral de $f$ de a a $b$ e representa-se pelo símbolo $\int_a^b f(x) d x$ ou $\int_a^b f$. Quando um tal número I existe, a função f diz-se integrável em [ $a, b$ ].
> 
> Se $a<b$, definimos $\int_b^a f(x) d x=-\int_a^b f(x) d x$, suposta $f(x)$ integrável em $[a, b]$. Definimos também $\int_a^a f(x) d x=0$. Se $f(x)$ é integrável em $[a, b]$, dizemos que o integral $\int_a^b f(x) d x$ existe.


> [!teorema]
> Toda a função $f$ **limitada** em $[a, b]$ tem um integral inferior $\underline{I}(f)$ e um integral superior $\bar{I}(f)$ que satisfazem às desigualdades
> 
> $
> \int_a^b s(x) d x \leq \underline{I}(f) \leq \bar{I}(f) \leq \int_a^b t(x) d x
> $
> 
> para todas as funções em escada $s$ e $t$ tais que $s \leq f \leq t$. A função $f$ é integrável em $[a, b]$ se e somente se os seus integrais superior e inferior são iguais, e nesse caso será
> 
> $
> \int_a^b f(x) d x=I(f)=I(f)
> $

O que esse teorema nos diz é: 
* (i) Toda função limitada em $[a,b]$ possui um integral superior e inferior: são o ínfimo e supremo do conjunto das áreas das funções escada por cima e por baixo, respectivamente. Ver [[Aula 3.1  A Integral.pdf|nota de aula]] da monitoria para mais detalhes.
* (ii) Porém, a função limitada somente será dita integrável se $I(f)=I(f)$.
Um exemplo clássico de função limitada que não é integrável é a função de Dirichlet (ver [[Aula 5.1  Funções Integráveis.pdf|nota de aula]]).


# Definições de integral de funções limitadas possivelmente negativas

A definição de integral apresentada na sessão acima (tirado do Apostol) é válida para quaisquer funções limitadas. Acontece que ela é pouco efetiva para funções negativas, pois ela subtrairia essas áreas no valor numérico da integral. Para evitar isso, o Milton na aula 5 trouxe $3$ definições diferentes, mas equivalentes, para funções **limitadas**, mas que podem assumir **valores negativos**:
* Parte positiva e parte negativa
* Limitação por baixo
* Aproximações com sinal
Prefiro focar na primeira...


## Parte positiva e parte negativa

> [!definicao]
> Sejam $a, b \in \mathbb{R}$ com $a<b, e$ seja $f:[a, b] \rightarrow \mathbb{R}$. A **parte positiva** de $f$ é a função $f^{+}:[a, b] \rightarrow[0, \infty)$ dada por
> 
> $
> f^{+}(x):=\max \{f(x), 0\}
> $
> 
> para todo $x \in[a, b]$. A **parte negativa** de $f$ é a função $f^{-}:[a, b] \rightarrow[0, \infty)$ dada por
> 
> $
> f^{-}=f^{+}-f .
> $

> [!obs]
> Notemos que $f=f^{+}-f^{-}$e que $|f|=f^{+}+f^{-}$. Portanto, a definição alternativa é
> 
> $
> f^{+}=\frac{1}{2}(f+|f|), f^{-}=\frac{1}{2}(|f|-f) .
> $

> [!definicao]
> Dizemos que $f$ é **integrável** se $f^{+}$ e $f^{-}$ são ambas integráveis, em cujo caso definimos
> $
> \int_a^b f(x) d x=\int_a^b f^{+}(x) d x-\int_a^b f^{-}(x) d x .
> $

Perceba que aqui nós estamos apenas dando nomes aos bois. Não estamos alterando em nada o comportamento da integral!

Nós já sabemos que a integral calcula a área "positiva" menos a "negativa". Mas, de modo rigoroso, nós ainda não definimos o que seria essa área "positiva" e área "negativa". É isso o que foi feito acima:

Como os nossos axiomas de área e tudo mais o que definimos até então só nos permite manipular áreas positivas, temos que de alguma forma definir esse área "negativa" forçando-a para a parte de cima do eixo $x$, a qual sabemos trabalhar. Foi isso o que fizemos ao definir $f^{-}:[a, b] \rightarrow[0, \infty)$. Agora, nós sabemos o que são essas tais áreas positivas e negativas e definimos $\int_a^b f(x) d x=\int_a^b f^{+}(x) d x-\int_a^b f^{-}(x) d x$ como a diferença de duas áreas positivas.

