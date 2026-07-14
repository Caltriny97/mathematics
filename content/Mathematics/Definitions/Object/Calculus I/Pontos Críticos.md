Data Criada: 31/05/2026 às 15:41
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Introdução

Em muitos problemas de matemática aplicada, o objetivo é identificar o mínimo de uma certa função, o chamado **problema de otimização**. Vimos anteriormente que o problema de achar **zeros** de funções é consideravelmente mais fácil que o problema de achar mínimos de funções. O teorema acima mos dá um critério **necessário** para que um ponto $x_*$ seja um mínimo de uma função **diferenciável** $f$.

Não dá para calcular o máximo de uma função (vide [[Teorema do Valor Extremo]]), pelo menos sem informação adicional da função. Não é um problema que pode ser resolvido de maneira computacional, nem assumindo que a função é contínua. Mas, se a função for diferenciável, existe uma condição necessária para um ponto ser máximo da função: se um ponto for um máximo e $f$ é diferenciável naquela ponto, então a derivada é zero (rever Teorema 1 em [[Teorema do Valor Médio]]).

Assim, voltamos para um problema que dá para resolver: calcular os zeros de uma função. Calcular os zeros de uma função contínua é possível algoritmicamente pelo método da bisseção (ou pelo menos achar um zero).

Novamente, achar um zero de uma função contínua é possível algoritmicamente. Achar todos, não! Em outras palavras, mesmo com esse resultado, não é possível achar o **mínimo global** da função algoritmicamente. O conjunto de zeros de uma função contínua pode ser muito complicado. É muito provavelmente um conjunto perfeito de conteúdo nulo...

**Obs.** Calcular o máximo e mínimo de $f$ são problemas equivalente, pois o mínimo de $f$ é o máximo de $-f$.

> [!obs]
> Temos dois métodos até agora para calcular o zero de uma função
> * [[Método de Newton]]
> * Método da Bisseção (usado em [[Teorema do Valor Intermediário|TVI]], [[Teorema do Valor Extremo|TVE]])...
> 
> É interessante sempre utilizarmos uma combinação esperta dos dois.


# Definição: Ponto crítico

> [!definicao]
> Seja $f:(a, b) \rightarrow \mathbb{R}$ diferenciável. Um ponto $x_* \in (a, b)$ é dito um **ponto crítico** de $f$ se $f^{\prime}\left(x_*\right)=0$.

**Obs.** 
* Todo mínimo de uma função diferenciável é um ponto crítico.
* Ser Um ponto crítico é uma condição **necessária**, mas não suficiente, para termos um mínimo (global) de uma função.

> [!exemplo]- Exemplo 1.
> **Exemplo:** Seja $\gamma \in \mathbb{R}$ e seja $f: \mathbb{R} \rightarrow \mathbb{R}$ dada por 
> $
> f(x):=x^3-\gamma x \quad \text{para todo $x \in \mathbb{R}$}.
> $
> Calcule os pontos críticos de $f$ e classifique-os em termos de $\gamma$.
> 
> 
> **Resposta:** Temos que calcular os zeros de $f'$. Como
> 
> $
> f^{\prime}(x)=3 x^2-\gamma
> $
> 
> Temos três casos:
> **a)** $\gamma<0$ : não há pontos críticos.
> ![[Pasted image 20260531163947.jpg|center|300]]
> 
> **b)** $y=0: x_*=0$ é o único pontos crítico.
> ![[Pasted image 20260531163954.jpg|center|300]]
> 
> **c)** $\gamma>0$ : $x_*= \pm \sqrt{\dfrac{\gamma}{3}}$ são os pontos críticos.
> ![[Pasted image 20260531164014.jpg|center|500]]
> 
> Esses pontos $x_{*}$ e $-x_{*}$ são nossos candidatos a mínimos e máximos da nossa função. Nenhum deles é nesse caso, pois a função é vai para $+\infty$ e $-\infty$. Então, é aqui que devemos adotar uma definição mais rigorosa...
> 
> Analogia das montanhas: o segredo está no domínio e nas restrições que fazemos dele.


> [!definicao]
> Um ponto $x_*$ é um **máximo local** de $f$ se existir um intervalo ($c, d$) tal que 
> $
> x_* \in(c, d) \; \text{ e }\; f(x) \leqslant f\left(x_*\right) \quad \text{para todo $x \in(c, d)$}
> $

Poderia ser um intervalo fechado, mas daí $x_{*}$ não poderia estar nos extremos $c$ ou $d$.


> [!exemplo] Voltando ao exemplo 1.
> Voltando as problema, temos que
> * b) $x_*=0$ não é nem mínimo nem máximo local,
> * c) $\sqrt{\dfrac{\gamma}{3}}$ é mínimo local e $-\sqrt{\dfrac{\gamma}{3}}$ é máximo local.
> 
> Perceba que $f'(x_*)=0$ não implica sequer que $x_*$ é máximo ou mínimo local. O caso a) mostra bem isso.

Vamos voltar ao problema da otimização. Imagine que nós usamos o método de Newton para calcular os zeros da derivada. Agora, nós queremos saber se esse zero é máximo, mínimo ou algo mais (vide quadro acima).

A princípio, tem cara de ser possível verificar se é ou não um máximo local. Mas, ainda assim, nós ainda temos que verificar todos os pontos do intervalo $(c,d)$, então voltamos ao problema inicial: não podemos de maneira algorítmica calcular perguntar todos os valores de uma função.

É por isso que a gente vai pedir um pouco mais de condições à nossa função $f$. E essa condição extra vai ser o Teste da segunda derivada.


# Teste da segunda derivada

Se a função for duas vezes diferenciável, a gente vai ter acesso a esse teste. Vamos definir primeiro oque é a segunda derivada.

Seja $f:(a, b) \rightarrow \mathbb{R}$ diferenciável. Como $f^{\prime}:(a, b) \rightarrow \mathbb{R}$ está bem definida, nada nos impede de ver se $f'$ é diferenciável também.

> [!definicao]
> Seja $f:(a, b) \rightarrow \mathbb{R}$, e seja $l \in \mathbb{N}$. A **derivada de ordem** $l$ de $f$ é definida recursivamente como:
> * a) $f^{(1)}=f^{\prime}$ se $f$ for diferenciável,
> * b) $f^{(i+1)}:=\left(f^{(i)}\right)^{\prime}$, se $f^{(i)}$ for diferenciável.

O chato aqui é verificar se cada derivada é diferenciável e não há um critério para isso. Porém, na prática, é fácil ver que funções específicas são diferenciáveis ou não.

**Obs.** A derivada de ordem zero de uma função é ela mesma.

> [!exemplo]-
> Começamos com a derivada de ordem $l$ dos monômios, porque é fácil ver que a derivada é uma operação linear. Portanto, a segunda e assim por diante também são operações lineares. Isso vem do fato de a composição de funções lineares ([[Transformações Lineares]]) é linear. A princípio, as derivadas não caem direto na álgebra linear, porque elas ocorrem em espaços de dimensão infinita, mas a demonstração aqui vale para qualquer dimensão, inclusive para a infinita.
> 
> 
> 1. Seja $n \in \mathbb{N}$ e seja $f(x):=x^n$. Temos que
> 
> $
> f^{(l)}(x)=\frac{n!}{(n-l)!} x^{n-l}
> $
> 
> para $l \leq n, \text{ e }  f^{(l)}=0$ para $l>n$. Ver na minha nota de aula 17-18 esquema mais simples.
> 
> 
> 2. Seja $n \in \mathbb{N}_0$ e seja $f(x):=\operatorname{sen} x$. Temos que
> $
> \begin{gather}
> & f^{(2 n)}(x)=(-1)^n \operatorname{sen} x \\ \\
> & \text{e} \\ \\
> & f^{(2 n+1)}(x)=(-1)^n \cos x .
> \end{gather}
> $
> 
> 3. Exercício) Veja na minha nota de aula 17-18

A segunda derivada aparece com muita frequência. A primeira aplicação que veremos é o chamado **teste da segunda derivada**.

> [!teorema] Teste da segunda derivada.
> Seja $f:(a, b) \rightarrow \mathbb{R}$ duas vezes diferenciável, e seja $x_*$ um ponto crítico de $f$.
> * a) Se $f^{\prime \prime}\left(x_*\right)>0$, então $x_*$ é um mínimo local.
> * b) Se $f^{\prime \prime}\left(x_*\right)<0$, então $x_*$ é um máximo local.
> * c) Se $f^{\prime \prime}\left(x_*\right)=0$, o testé é inconclusivo.

O teste da segunda derivada é um critério **suficiente**, mas não necessário, para achar máximo e mínimos locais. Isso se deve ao caso c) acima: há pontos que são máximos, mas não satisfazem o teste da segunda derivada. Lembre que o teste da primeira derivada era um critério necessário.

Geometricamente, a segunda derivada nos diz qual o comportamento da função ao redor de $x_{*}$. Ver exemplo da parábola na minha nota de aula 17-18.

Indo mais fundo, toda função ao redor do mínimo é parecida com uma parábola. Isso se chama [[A fórmula de Taylor]].


# Derivada e decrescimento duma função

> [!teorema]
> Se $f^{\prime}(x)>0$ para todo $x \in(a, b)$ e $f$ for continua em $[a, b]$, então $f$ é estritamente crescente.

É consequência imediata do TVM.