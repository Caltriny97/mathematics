Data Criada: 04/04/2026 às 00:54
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!proposicao] Proposição.
> Considere as operações usuais de $\mathbb{R}^3$.
> * (i) Uma reta que passa pela origem determina um espaço vetorial.
> * (ii) Um plano que passa pela origem determina um espaço vetorial.
> 

> [!demonstracao]- Demonstração de (ii).
> Tome o conjunto $\mathbb{A} = \{(x,y,z) \in \mathbb{R}; \; ax+by+cz =0\}$ para $a,b,c \in \mathbb{R}$ fixos.
> 
> Primeiro vamos provar que $\mathbb{A}$ é fechado para soma. Tome $(x_{1},y_{1},z_{1})$ e $(x_{2},y_{2},z_{2}) \in \mathbb{A}$. Precisamos mostrar que a soma dessas triplas pertence a $\mathbb{A}$:
> $
> \begin{gather}
> (x_{1}+x_{2},y_{1}+y_{2},z_{1}+z_{2}) \in \mathbb{A} \iff a(x_{1}+x_{2}) + b(y_{1}+y_{2}) + z(z_{1}+z_{2}) = 0 \\
> \underbrace{(ax_{1} +by_{1}+cz_{1})}_{0} + \underbrace{(ax_{2} +bx_{2}+cx_{2})}_{0} = 0
> \end{gather}
> $
> Pelo que é verdade da nossa hipótese. Note que isso só é possível porque passa pela origem. Caso contrário, esses termos da última linha não seriam iguais a zero.
> 
> Agora falta só provar que ele é fechado para multiplicação por escalar, que ele não é vazio (sabemos já que a origem pertence a ele) e mais os $8$ axiomas de [[Espaços Vetoriais]]. 
> 
> Mas... na verdade, não precisamos provar esses axiomas, pois eles vão ser herdados do conjunto maior: o $\mathbb{R}^{3}$, pois já vimos que ele é um espaço vetorial. O único problema que poderíamos ter seria furar a soma ou produto por escalar, que poderiam sair do nosso conjunto. Mas, uma vez dentro do conjunto, é claro que a comutatividade, a associatividade, existência do inverso não vão deixar de funcionar. 

Então, na prática, quando já sabemos que um conjunto maior é um espaço vetorial, para provarmos que o conjunto menor também é, basta garantir que ele não é vazio e que ele está bem definido para as operações (é fechado para elas). Se conseguirmos provar isso, ele vai ser um **subespaço**, que é o caso da reta e do plano que passam pela origem.

Interpretação geométrica da reta que não passa pela origem, onde a operação soma não é fechada e, portanto, não constitui um espaço vetorial:

![[Pasted image 20260403173608.jpg|center|400]]