Data Criada: 05/04/2026 às 01:05
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Uma pergunta que é extremamente complicada do ponto de vista matemático é "o que é área?". Vamos tentar começar a responder...

Se temos um retângulo de lados $a$ e $b$, a área é $a \cdot b$. Isso é, do ponto de vista matemático, uma **definição**.
Agora, a área no mundo dos retângulos tem uma propriedade interessante: ela é aditiva, ou seja, se dividirmos um retângulo em vários outros, a área de um retângulo original é igual à área dos retângulos constituintes. Isso é um **teorema** (e não é trivial) e nós o provamos por indução (dividimos o retângulo e fazemos uma indução "para trás").
O importante aqui não é saber provar isso, mas saber a diferença entre esses resultados (definição e teorema).
Vamos partir também do pressuposto que área é monótona, mas deveríamos provar essa informação se quiséssemos ser rigorosos.

Arquimedes usou o seguinte método para calcular a área sob a parábola (o natural seria começar com o círculo, mas este é extremamente difícil).

![[Captura_de_tela_2026-03-29_213821-removebg-preview.png|center|600]]

Denotemos a área de dos quadrados brancos de $A_{b}$ e a área de todos os quadrados, de $A_{t}$. Da nossa definição de área, temos que

$$
\begin{aligned}
& A_{b} = \frac{1}{n^{3}}+\frac{4}{n^{3}}+\frac{9}{n^{3}}+ \cdots + \frac{(n-1)^{2}}{n^{3}} = \frac{1}{n^{3}}\sum_{i=1}^{n-1} i^{2} ,\\
& A_{t} = \frac{1}{n^{3}}\sum_{i=1}^{n} i^{2}.
\end{aligned}
$$

> [!ps]-
> A altura dos retângulos brancos é dada pela função avaliada no lado esquerdo  ($n-1$), enquanto a altura da união de todos os retângulos é dada pela função avaliada no lado direito ($n$). Perceba também que a união dos retângulos é sempre igual ao retângulo branco da direita (por isso eles não até $n$).

Notemos que a diferença entre essas duas fórmulas é somente o último termo do somatório, ou seja, a diferença é pequena... (ver relação com as **aulas de cálculo da monitoria**)

Portanto, pelo resultado do problema 4 da lista, temos
$$
\begin{gather}
& \bullet \quad \frac{1}{n^{3}} \left( \frac{(n-1)^{3}}{3}+p_{2}(n-1) \right) \leq A \leq \frac{1}{n^{3}} \left( \frac{n^{3}}{3} + p_{2}(n) \right) \\
& \bullet \quad  A_{t} - A_{b} = \frac{1}{n} \\
\end{gather}
$$

Sabemos que o $p_{2}(n)$ é da forma $an^{2} + bn + c$ (sabemos, da monitoria, a fórmula específica pra esse caso, então poderíamos calcular $a$, $b$ e $c$). Logo, temos que
$$
\begin{gather*}
\frac{1}{n^{3}} \left(\frac{(n-1)^{3}}{3} \right) + \cancelto{0}{\left(\frac{a}{(n-1)}+\frac{b}{(n-1)^{2}}+\frac{c}{(n-1)^{3}} \right)} \\
\\\leq A \leq \\ 
\\ \frac{1}{3} + \cancelto{0}{\left(\frac{a}{n}+\frac{b}{n^{2}}+\frac{c}{n^{3}} \right)} \\
\end{gather*}
$$
Sabemos que $A$ é menor ou igual a $\frac{1}{3}$ mais um número muito pequeno e, da mesma forma, $A$ é maior ou igual a $\frac{1}{3}$ menos um número muito pequeno, porque a diferença entre essas duas expressões ($A_{t} - A_{b}$) é $\frac{1}{n}$ pelo que vimos acima, que também é um número muito pequeno. Portanto,
$$
A \rightarrow \frac{1}{3}
$$
Então, o que estamos fazendo é que estamos "apertando" a área da parábola entre dois números. E nós podemos deixar esses dois números tão próximos de $\frac{1}{3}$ quanto nós quisermos se tomarmos $n$ suficientemente grande. Isso é o que chamaremos no nosso caso de [[limite]].


> [!problema]
> **Exercício:** Prove por indução (sem usar o problema 4) que para todo $n\geq 2$,
> $
> \sum_{i=1}^{n-1} i^{2} \leq \frac{n^{3}}{3} \leq \sum_{i=1}^{n} i^{2}
> $
> Conclua que
> $
> \left|A-\frac{1}{3}\right| \leq \frac{1}{n}
> $
> 
> Do ponto de vista geométrico, queremos dizer o seguinte: a distância entre $A$ e $\frac{1}{3}$ tem que ser menor que a distância entre os somatórios ($A_{t} - A_{b}$)...
> ![[Pasted image 20260329225654.jpg]]
> 
> De acordo com a **observação** $(*)$ da aula de [[área]], que diz, de forma simplificada
> 
> $
> 0 \leq \overline{I}(f) - \underline{I}(f) \leq \frac{c}{n} \quad\forall \; n \implies   \underline{I}(f) = \overline{I}(f)
> $
> 
> Segue que
> $
> A = \frac{1}{3}
> $
> 
