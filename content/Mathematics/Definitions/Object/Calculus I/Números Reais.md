Data Criada: 23/03/2026 às 20:18
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!definicao] Definição.
> O conjunto $\mathbb{R}$ dos números reais é o único corpo ordenado completo.

> [!obs]
> Para uma definição matemática ser considerada bem feita, ela precisa definir um único objeto, ou seja, ela define o tal objeto de maneira única. Isso nos leva a um problema de existência e unicidade.
> Para a nossa definição acima, precisamos especificar algumas coisas: 
> * (i) ela efetivamente define os números reais de forma única? Isso é um teorema (não vamos vê-lo por enquanto).
> * (ii) o que é um corpo?
> * (iii) o que é um corpo ordenado?
> * (vi) o que é um corpo ordenado completo?


# A. Axiomas de corpo


Um corpo é um objeto algébrico, então é uma coisa que não fala de cálculo ou análise, mas sim de álgebra. A esse conjunto $\mathbb{R}$ pertencem elementos que satisfazem certas relações:
* [[A. Axiomas de Corpo]]


# B. Axiomas de Ordem

Um conjunto ordenado é um conjunto no qual sempre podemos dizer qual é a ordem entre os seus elementos.

> [!axioma]
> Existe um conjunto $\mathbb{P}\subseteq \mathbb{R}$ tal que
> 
> **B1.** Se $x, y \in \mathbb{P}$ então $x+y \in \mathbb{P}$ e $xy\in\mathbb{P}$.
> **B2.** Para todo $x \in \mathbb{R} \textbackslash \{0\}$, **ou** $x \in \mathbb{P}$, **ou** $-x \in \mathbb{P}$.
> **B3.** $0 \notin \mathbb{P}$.

> [!comentario]
> Esse conjunto, a posteriori, são os números positivos. Mas a princípio, não sabemos disso ainda. Só estamos falando da existência desse conjunto. A propriedade 1 diz que esse conjunto é fechado via soma e multiplicação. A propriedade 2 está bem definida por causa da unicidade do inverso (ver comentário da sessão passada).

> [!definicao]
> Sejam $x, y \in \mathbb{R}$. Dizemos que
> $
> \begin{aligned}
> & \bullet \;\; x < y \;\; \text{se} \;\;  y-x \in \mathbb{P}, \\
> & \bullet \;\; x > y \;\; \text{se} \;\;  y<x, \\
> & \bullet \;\; x \leq y \;\; \text{se} \;\;  x<y \;\; ou\;\; x=y, \\
> & \bullet \;\; x \geq y \;\; \text{se} \;\;  y\leq y.
> 
> \end{aligned}
> $

> [!comentario]
> A diferença está definida como a soma com o inverso aditivo.

> [!obs]
> Sejam $x,y \in \mathbb{R}$. Temos que 
> $
> \textbf{ou} \quad x<y \quad\textbf{ou} \quad x=y \quad \textbf{ou}\quad x>y
> $
> Esse resultado (conhecido como tricotomia) vem de B2 (ou $x$ é positivo ou o inverso de $x$ é positivo) junto da definição acima.


> [!comentario]
> $\mathbb{R}$ é um corpo ordenado, mas $\mathbb{Q}$ por ex também é, então ser um corpo ordenado não define $\mathbb{R}$ de maneira única ainda... 
> Existe um conjunto interessante $\mathbb{Q}[\sqrt{ 2 }]=\{a+b\sqrt{ 2 };\;a,b\;\in\mathbb{Q}\}$ que também é um corpo ordenado (ver demonstração depois).


# C. O axioma do supremo

O último axioma que caracteriza os números reais é o axioma do supremo. Ele é o mais importante, porque é ele que caracteriza esse conjunto de maneira única.

> [!definicao]
> Seja $A \subseteq \mathbb{R}$. Dizemos que $M \in \mathbb{R}$ é uma **cota superior** de $A$ se:
> $
> x \leq M \;\; \text{para todo} \;\; x \in A
> $

> [!exemplo]
> Agora que definimos os axiomas de ordem, conseguimos definir o conjunto $A = [0,1]$ como $A = [0,1] = \{x \in \mathbb{R}; x\geq 0 \;\; \text{e} \;\; x\leq 1\}$. Temos, então, que 1978 é uma cota superior de $A$, assim como $\pi$ também o é (mesmo que ainda não o tenhamos definido).

> [!obs]
> Se $M$ for uma cota superior de $A$ e $N>M$, então $N$ também é uma **cota superior** de $A$.

> [!definicao]
> Dizemos que $A \subseteq \mathbb{R}$ é **limitado superiormente** se $A$ tem (**pelo menos**) uma cota superior.
 
> [!definicao]
> Seja $A \subseteq \mathbb{R}$. Dizemos que $x \in \mathbb{R}$ é o **supremo** de A se:
> * a) $x$ for uma cota superior de $A$,
> * b) Toda cota superior $M$ de A satisfaz $x \leq M$.

> [!comentario]
> $x$ é a menor cota superior possível, ou seja, qualquer outra cota superior está acima do $x$.
> ![[Pasted image 20260325195857.jpg|center|400]]

> [!axioma]
> **C1.** Todo conjunto $A$ limitado superiormente tem um supremo.

> [!obs]
> O supremo $x$ de A nem sempre pertence ao conjunto A.

> [!comentario]
> Esse **C1** é o ponto no qual as coisas se transformam de maneira radical, pois estamos introduzindo a nossa definição de supremo no axioma: O Axioma do Supremo. É ele o que separa Álgebra de Análise. Sem esse axioma, não existe Análise.


> [!proposicao]
> **Proposição.** $\sqrt{ 2 } \in \mathbb{R}$.
> **Comentário.** Isso não é trivial, porque mesmo sabendo que é $\sqrt{ 2 }$ é um número não pertencente a $\mathbb{Q}$, isso não nos garante que $\sqrt{ 2 }$ existe... isso apenas nos diz onde $\sqrt{ 2 }$ não está. Antes de provar que $\sqrt{ 2 }$ existe, vamos definir esse número.
> 
> **Def.** $x \in \mathbb{R}$ é a raiz quadrada de 2 se:
> * a) $x>0$
> * b) $x^{2} = x \cdot x = 2$.
> 
> **Demonstração.** 
> Seja $A = \{y \in \mathbb{R};\;y>0 \;\text{e}\; y^{2}\leq 2\}$. A ideia é ver que
> $
> x_{0} = \text{sup}A
> $
> é a raiz de 2. Notemos que $5 \notin A$, pois $5^{2}=25>2$. Para provar que 5 é uma cota superior de $A$, é suficiente provar que $x>5 \implies x \notin A$ (ver comentário). Mas,
> $
> x > 5 \implies x^{2} = x \cdot x > 5 \cdot x > 5 \cdot 5 = 25
> $
> pelo que $5$ é uma cota superior de A. Logo, $x_{0} = \text{sup}A$ está bem definido, pelo axioma do supremo.
> 
> Nosso objetivo agora é provar que $x_{0}^{2}=2$. Para isso, usaremos uma ideia muito comum em análise: provaremos que $x_{0}^{2}\geq 2$ e que $x_{0}^{2}\leq 2$.
> 
> a) $x_0^2 \geqslant 2$. 
> Seja $y>0$ tal que $y^2<2$. Notemos que nesse caso,
> $
> y<\frac{4 y}{y^2+2} \quad\text{e}\quad\left(\frac{4 y}{y^2+2}\right)^2<2
> $
> Portanto, $y$ não é cota superior de $A$, e em particular $x_0^2 \geqslant 2$.
> 
> b) $x_0^2 \leq 2$. 
> Seja $z>0$ tal que $z^2>2$. Como vimos antes para $z=5$,
> $
> x>z \Rightarrow x^2=x \cdot x>z \cdot x>z \cdot z=z^2 \geqslant 2,
> $
> pelo que $x \leq z$ para todo $x \in A$. Em outras palavras, $z$ é uma cota superior de A, pelo que $x_0 \leq z$. Além disso, para $z>0$ tal que $z^2>2$,
> $
> z>\frac{1}{2}\left(z+\frac{2}{z}\right) \quad \text{e} \quad\left(\frac{1}{2}\left(z+\frac{2}{z}\right)\right)^2>2,
> $
> pelo que $x_0<z$ (o importante é que $x_{0} \neq z$, pelo que $x_{0}^{2} \neq z^{2}$) o que prova que $x_0^2 \leq 2$.
> 
> 
> **Comentário da demonstração.**
> O ponto de tudo isso é: é óbvio que o $\text{sup}A = \sqrt{ 2 }$. Mas como provamos isso só a partir dos axiomas dos números reais? 
> Definimos um conjunto $A$, que são todos os números cujos quadrados são menores que $2$. A ideia é que o supremo deles seja $\sqrt{ 2 }$. O problema é que poderia haver um buraco entre o conjunto $A$ e $\sqrt{ 2 }$. Daí, o supremo dele não seria $\sqrt{ 2 }$, mas sim um número menor. Sabemos dos números reais que não existem buracos, mas é exatamente isso que queremos provar e vamos fazê-lo por meio de uma combinação do Axioma do Supremo com os Axiomas de Ordem. Essa combinação vai nos permitir provar que os números reais não têm buracos.
> * A nossa ideia aqui é tomar um conjunto A e tomar como um candidato para $\sqrt{ 2 }$  o supremo desse conjunto A. Aí é que está a ideia de supremo, porque o supremo é um número que sempre existe (axioma C1) desde que $A$ seja limitado. É isso que vamos tentar provar inicialmente.
> * Talvez a condição $y>0$ para o conjunto $A$ não seja necessária
> * Repare que, tomar $x=5$ e dizer que $x^{2}=25>2$ não é suficiente para provar que $x=5$ é cota superior de $A$, afinal poderíamos ainda ter algum "pedaço" de $A$ depois de $x =5$. Se quisermos ser rigorosos, precisamos provar que $x>5$ não pertence a $A$. Assim, $x=5$ é cota superior de $A$.
> * Demonstração por contradição não existe! Ainda sobre o fato acima, provar que $x \in A \implies x<5$ é o mesmo que provar que $x>5 \implies x \notin A$. Isso vem do seguinte fato lógico: $A \implies B\;\; \iff \;\;-B \implies -A$.
> * Essa ideia de mostrar que $x_{0}^{2}\geq 2$ e $x_{0}^{2}\leq 2$ é muito comum em análise, pois, pela tricotomia (que vem do fato de $\mathbb{R}$ ser um corpo ordenado), isso nos garante que $x_{0}^{2}=2$. Análise não é álgebra, então é difícil de provar igualdades. É mais fácil provar desigualdades.
> * Queremos provar que $x_{0} = \text{sup}A \implies x_{0}^{2}\geq 2$. Isso é equivalente (ver comentário acima) a provar que $y^{2}<2 \implies y \neq \text{sup}A$. Chamamos de $y$ para não causar confusão com $x_{0}$.  
> * Repare que não podemos usar $\sqrt{ 2 }$ como cota superior para mostrar que $y \neq \text{sup}A$, pois não sabemos ainda que $\sqrt{ 2 }$ existe! Temos, portanto, que usar **valores intermediários** entre $y$ e $\sqrt{ 2 }$, os quais temos certeza que pertencem a $A$ e que podem assumir papel de cota superior.
> * Esses valores intermediários são justamente o que vimos na 1° aula do curso. Se $y<\sqrt{ 2 }$, então $\frac{4 y}{y^2+2}$ nos dá uma melhor aproximação para $\sqrt{ 2 }$ **que ainda sim pertence** a $A$. Logo, $y$ não é cota superior de $A$.
> * De forma análoga para o caso (b), temos que $x_{0} = \text{sup}A \implies x_{0}^{2}\leq 2$ é equivalente a provar $z^{2}>2 \implies z \neq \text{sup}A$. Provamos então que, se $z^{2}>2$ então existe uma aproximação melhor para $\sqrt{ 2 }$, ou seja, existe sempre cota superior menor que $z$, pelo que $x_{0} < z$. Portanto, $z \neq \text{sup}A$ e, pela equivalência, $x_{0}^{2}\leq 2$.
> * O resultado $y<\frac{4 y}{y^2+2} < \sqrt{ 2 }$ é obtido pelo inverso ($\frac{2}{(\dots)}$) de $\sqrt{ 2 } < \frac{1}{2}\left(z+\frac{2}{z}\right) < z$, que vimos na aula passada. Este aproxima por cima e aquele aproxima por baixo.