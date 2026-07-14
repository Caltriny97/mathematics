Data Criada: 04/04/2026 às 20:05
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# A definição formal de área

> [!axioma] Axioma 1.
> A área de um retângulo de lados paralelos aos eixos é igual ao produto dos comprimentos dos lados.

> [!ps]-
> Quando falamos eixos, nos referimos aos eixos do plano cartesiano.

![[Pasted image 20260404204506.jpg|center|400]]

O quadrado da direita por enquanto não possui área definida. Vamos ver logo que, do ponto de vista axiomático, é extremamente conveniente não incluir esse quadrado rotacionado no axioma.


> [!axioma] Axioma 2.
> A área de uniões de retângulos disjuntos ou que se intersectam numa aresta é a soma das áreas de ditos retângulos.

![[Pasted image 20260404205143.jpg|center|400]]

A união dos retângulos da direita por enquanto não possui área bem definida porque não é união disjunta de dois retângulos.


> [!definicao]
> Denotaremos por $\mathcal{R}$ a classe de retângulos de lados paralelos aos eixos cartesianos, e denotaremos por $\mathcal{A}$ a classe de conjuntos formados por uniões de retângulos disjuntos ou que se intersectam só em arestas.

Esses são os únicos axiomas da área. Para começar, nós só sabemos calcular a área de retângulos cujos eixos são paralelos aos eixos cartesianos e uniões desses retângulos.


> [!obs]
> Os seguintes elementos pertencem a $\mathcal{A}$:
> ![[Pasted image 20260404210632.jpg|center|300]]
> Uniões de retângulos que se intersectam em apenas parte de uma aresta também pertecem a $\mathcal{A}$.
> 
> A classe $\mathcal{A}$ é fechada por uniões e intersecções finitas (a figura formada continua na classe $\mathcal{A}$). Se tivéssemos incluído rotações de retângulos na classe $\mathcal{A}$, seria muito difícil chegar a essa conclusão.


> [!definicao]
> Um conjunto $A \subseteq \mathbb{R}^{2}$ é dito uma **região limitada** se existir $M \in \mathbb{R}$ tal que $A \in [-M,M]\times[-M,M]$, o quadrado de lado $2M$ centrado na origem.

Ou seja, é um conjunto para o qual nós sempre podemos achar um quadrado grande o suficiente que o contém.

Vamos agora definir área pra outros conjuntos que não sejam retângulos. Primeiro, vamos definir de maneira axiomática a área de uma região limitada do plano. Repare que em momento nenhum falamos de soma de áreas... só vamos fazer isso no final da aula.

![[Pasted image 20260404212408.jpg]]

Digamos que a região $B$ é a região para a qual queremos calcular a área. Não sabemos calcular a área da região $B$, mas sabemos calcular a área de retângulos e de uniões de retângulos, então vamos aproximar a área de $B$ por retângulos (por dentro e por fora).

Agora vamos considerar todas as possíveis formas de colocar retângulos dentro de $B$, vamos olhar para a área dessas figuras e tomar o supremo dessas áreas. Lembre do axioma do supremos (ver [[Números Reais]]) que podemos sempre tomar o supremo de qualquer conjunto que seja limitado superiormente. 

Como a região $B$ está contida num quadrado de lado $2M$, então a área de todas essas uniões de retângulos dentro de $B$, denotada por $R$ está limitada por $4M^{2}$, pelo que o supremo dessa região está bem definido.

Pensando em algo mais voltado pra análise, temos que
$$
\begin{gather}
P:=\{R \in \mathcal{A};R\subseteq B\} \\
Q:=\{\text{Area}(R); R \in P\} \\
 \\
\text{Area}^{-}(B) := \text{sup}Q
\end{gather}
$$
$P$ é o conjunto dos retângulos ou uniões de retângulos que estão contidos B, enquanto $Q$ é o conjunto de número reais das áreas dos elementos de $P$. O ponto aqui é que, por mais bizarro que seja o meu conjunto $Q$ (com buracos, repetições...) o axioma do supremo nos garante que esse conjunto tem supremo, uma vez que é limitado superiormente.

Podemos também aproximar a área do conjunto $B$ por fora. O que podemos fazer é completar essa família de retângulos $R$ para uma família de retângulos $R^{'} \supseteq B$. Essa conjunto está limitada por baixo: $\text{Area}(R^{'})\geq 0$, pelo que o ínfimo está bem definido (é simplesmente o supremo de "menos" o conjunto).

Perceba novamente que o os elementos do conjunto $Q$ não são a soma da áreas dos retângulos (só vamos mostrar que a área é aditiva mais tarde), mas sim a área total das várias possibilidades de preenchimentos de $B$, pelo que está bem definido da nossa classe $\mathcal{A}$.

> [!definicao]
> Seja $B$ uma região limitada. Então,
> $
> \begin{aligned}
> & \text{Area}^{+}(B):=\text{inf}\{\text{Area}(R);\; R \in \mathcal{A} \text{ e } B \subseteq R\}, \\
> & \text{Area}^{-}(B):=\text{sup}\{\text{Area}(R);\; R \in \mathcal{A} \text{ e } R \subseteq B\}.
> \end{aligned}
> $

> [!obs]
> Pelo axioma do supremo, $\text{Area}^{+}(B)$ e $\text{Area}^{-}(B)$ estão bem definidas. Também, $\text{Area}^{+}(B) \geq \text{Area}^{-}(B)$.

> [!definicao]
> Dizemos que $B$ tem **área bem definida** se
> $
> \text{Area}^{+}(B) = \text{Area}^{-}(B).
> $
> 
> Nesse caso, dizemos que
> $
> \text{Area}(B) = \text{Area}^{+}(B).
> $

> [!comentario]-
> Ver na minha anotação da aula 3 um exemplo de conjunto que não possui área bem definida. Basicamente, o conjunto $B:=\left\{ \frac{a}{2^{n}};n \in N_{0}; a \in \{0,1,\dots,2^{n}\} \right\}$ não tem área bem definida, pois a área superior é $1$ e a inferior é $0$.
> 
> Um comentário voltado pra análise: nessa definição, se admitirmos usar uma quantidade enumerável de retângulos para calcular a área superior, esse conjunto teria área superior igual a zero e teríamos uma definição de área mais robusta, que é a definição de área que se faz em teoria da media (área de Lebesgue do conjunto).
> 
> A única diferença entre a área que estamos fazendo aqui e a famosa medida de Lebesgue é que, nessa, estamos autorizados a calcular área superior usando uma quantidade enumerável de retângulos. Aqui, nós só estamos autorizados a usar uma quantidade infinita de retângulos e isso é o que chamaríamos de área de Arquimedes.


Agora, vamos ver uma observação que nos diz quando é que é possível calcular a área de maneira um pouco mais explícita e que formaliza a ideia que temos na cabeça de como calcular área usando retângulos.

> [!obs] Observação $(*)$.
> Seja $a \in \mathbb{R}$ tal que para todo $n \in \mathbb{N}$ existem $A_{n}^{-}, A_{n}^{+} \in \mathcal{A}$ tais que
> * (a) $\text{Area}(A_{n}^{-})\leq a \leq \text{Area}(A_{n}^{+})$
> * $0 \leq \text{Area}(A_{n}^{+}) - \text{Area}(A_{n}^{-}) \leq \dfrac{1}{n}$
> * $A_{n}^{-} \subseteq B \subseteq A_{n}^{+}$
> 
> Então,
> $
> \text{Area}(B) = a
> $

Usamos esse resultado para calcular a área sob a parábola, como feito em [[Método da Exaustão]] e ter uma [[Intuição da Integral]]... Em cálculo tradicional, isso é conhecido como **teorema do confronto**.

Na verdade, esse resultado requer um lema para ser provado:

Vamos discutir um pouco como Arquimedes construiu área. Arquimedes não tinha à disposição dele a noção de limite, mas ele entendia a noção de supremo. E o que ele diz é: só com supremo, eu consigo definir integral.

Ele fez isso provando o que conhecemos hoje como Propriedade Arquimediana dos números reais. O impressionante é que isso não é uma axioma, mas sim algo dá pra provar usando o axioma do supremo.

> [!lema]
> O conjunto $\mathbb{N}$ não é limitado por cima, i.e., para todo $x \in \mathbb{R}$ existe $n \in \mathbb{N}$ tal que $n > x$.

> [!demonstracao]
> Dado $x \in \mathbb{R}$, seja $B := \{n \in \mathbb{N}; n\leq x\}$. Como $B$ é limitado por cima, $b := \text{sup}B$ existe. Como $b-1 < b,$ $\;\;b-1 \neq \text{sup}B$, pelo que existe $n_{0} \in B$ tal que $b-1 < n_{0}$. Logo, $n_{0}+1>b$, pelo que $n_{0} +1 \notin B$, e em consequência $x<n_{0}+1$.


A Propriedade Arquimediana tem como consequência outro lema muito importante, que é:

> [!lema]
> Se $x \in \mathbb{R}$ satisfaz $0 \leq x \leq \dfrac{1}{n}$ para todo $n \in \mathbb{N}$, então $x=0$.

Em outras palavras, o zero é o único número não negativo que $0 \leq \frac{1}{n} \forall n \in \mathbb{N}$. Já vimos isso como $\lim_{ n \to \infty } \frac{1}{n} = 0$.

A ideia é que esse $\frac{1}{n}$ se aproxima tanto de zero que não há mais espaço entre ele e zero para colocar outro número real. Esse resultado não é óbvio, pois poderia ser que houvesse um buraco ao redor do zero nos número reais (isso é, a princípio, uma possibilidade). Fica a lição: as ideias intuitivas que nós temos sobre os números reais são propriedades que devem ser provadas.

![[Pasted image 20260405014244.jpg|center|500]]

Para provar que dois número são iguais em cálculo, usamos a tricotomia: primeiro provamos que um é maior ou igual que o outro, depois o inverso. É sempre assim que provamos igualdade em cálculo, análise e qualquer área da matemática que é baseada nos números reais. Relembre [[Números Reais]].

> [!demonstracao]
> É suficiente provar que $x \leq 0$. Seja $y > 0$. Pelo lema anterior, existe $n_{0} \in \mathbb{N}$ tal que $\frac{1}{y} < n_{0}$. Logo, $\frac{1}{n_{0}}<y$, de onde $x<y$. Portanto,
> $
> x < y  \;\text{ para todo }\; y>0.
> $
> Essa é exatamente a definição de $x\leq 0$.


> [!corolario]
> Se $|x-y|\leq \dfrac{1}{n}$ para todo $n \in \mathbb{N}$, então $x=y$.

A importância desse resultado reside no fato de que nós temos inicialmente dois número  $x$ e $y$ que podem ser diferentes, uma vez que vêm de duas expressões diferentes ($S_{sup}$ e $S_{inf}$ por exemplo) e queremos provar que essas duas expressões nos dá o mesmo número. Nós então provamos que a diferença deles é arbitrariamente pequena, então os dois números tem que ser iguais (assim mostramos que a área está bem definida). É assim que a gente usa esse resultado.

Voltando à observação $(*)$, podemos visualizar da seguinte forma:

![[Pasted image 20260405022151.jpg|center|500]]


A área já está bem definida para certos conjuntos (não para todos). Agora, a pergunta é: quais propriedades tem a área que a gente acabou de definir? 

(a) queremos ser capazes de dizer que a área da união de dois conjuntos é a soma das áreas. Não provamos isso ainda na aula. Vamos tentar agora:

Temos duas regiões disjuntas em princípio. Note que elas poderiam se tocar. Agora, se aproximarmos a área de uma delas por retângulos e aproximarmos a outra também, a união desses retângulos é uma aproximação da união. Então a área inferior é a soma das áreas inferiores. Para a área superior, podemos desenhar uma linha no meio das regiões e, assim, podemos achar aproximações por retângulos por fora, que são disjuntas e, portanto a união delas é uma aproximação por retângulos da união. E, portanto, isso prova a aditividade.

![[Pasted image 20260405091936.jpg|center|400]]


Sabemos que a área do triângulo é $\frac{ab}{2}$, mas como provamos isso? Se provarmos que a área da união é a soma das áreas (na verdade, isso **não** é suficiente), saberemos que, se completarmos o triângulo, formaremos um retângulo de área $ab$. Logo a área do triângulo deve ser $\frac{ab}{2}$.

Voltando para o caso do triângulo, podemos verificar que o desenho abaixo prova que a área da união desses triângulos é a união da área, porque a área dos quadradinhos que ficam no meio é arbitrariamente pequena. Dessa forma, a área da união é a soma das áreas menos a área da intersecção.

![[Pasted image 20260405092240.jpg||center|300]]