Data Criada: 03/04/2026 às 21:45
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Por algum motivo, eu achava que o resultado do produto escalar seria justamente essa projeção de um vetor sobre o outro. Isso não é verdade (tanto que $u \cdot u = \|u\|^2$). O resultado em si não nos diz muito sobre os dois vetores, além de se eles são ou não ortogonais. Para saber a norma da projeção de fato, temos que usar outras informações.

> [!definicao] Definição.
> A projeção ortogonal de um vetor $v$ sobre um vetor não nulo $u$, denotado por $\text{proj}_u v$, é o vetor paralelo à $u$ e tal que $\left(v-\right.$ $\text{proj}_u v) \perp u$.

> [!definicao] Definição.
> Seja $u \neq \overline{0}$. Então $\operatorname{proj}_u v=\frac{u \cdot v}{\|u\|^2} u$.

> [!comentario]-
> Cuidado na hora de demonstrar: o cosseno é um valor absoluto, logo devemos trabalhar com a norma dos vetores.
