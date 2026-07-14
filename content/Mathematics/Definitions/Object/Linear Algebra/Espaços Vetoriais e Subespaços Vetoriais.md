Data Criada: 19/03/2026 at 16:56
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Vamos abordar espaços vetoriais sobre os reais, mas poderíamos usar qualquer outro [[A. Axiomas de Corpo|corpo]] (desde que as operações definidas façam sentido nesse corpo).

> [!definicao] Definição.
> Um Espaço Vetorial (sobre $\mathbb{R}$) é um conjunto $\mathcal{V}$ não vazio no qual estão definidas duas operações: adição $( \mathcal{V} \times \mathcal{V} \xrightarrow{\oplus} \mathcal{V} )$ e multiplicação por escalar $(\mathbb{R} \times \mathcal{V} \xrightarrow{\odot} \mathcal{V})$ tais que, para $u, v, w \in \mathcal{V}$ e $\alpha, \beta \in \mathbb{R}$ são válidos:
> 
> 1. $u \oplus v = v \oplus u$
> 2. $(u \oplus v) \oplus w = u \oplus (v \oplus w)$
> 3. $\exists z \in \mathcal{V}$ tal que para qualquer $u \in \mathcal{V}$ tem-se $u \oplus z = u$ $\;(\text{Not.:} \; \overline{0})$
> 4. Para cada $u \in \mathcal{V}$ existe um $z \in \mathcal{V}$ tal que $u \oplus z = \overline{0}$ $\;(\text{Not.:} \; -u)$ 
> 5. $\alpha \odot (\beta \odot u) = (\alpha \beta) \odot u$
> 6. $(\alpha + \beta) \odot u = (\alpha \odot u) \oplus (\beta \odot u)$
> 7. $\alpha \odot (u \oplus v) = (\alpha \odot u) \oplus (\alpha \odot v)$ 
> 8. $1 \odot u = u$
>    
> Neste caso, os elementos de $\mathcal{V}$ são chamados de [[vetores]].

> [!comentario]
> Vetores na matemática são uma generalização dos vetores que estamos acostumados na física e na Ciência da Computação.
> 
> Quando falamos em operações bem definidas de soma e de multiplicação por escalar, queremos dizer que são fechadas.
> 
> Em (5), parece uma associatividade, mas é uma troca de operações: estamos trocando $\odot$ pelo produto $\alpha \beta$ do **corpo que estamos usando** (produto de reais no caso).


# Exemplos de EV que já vimos

1. Conjunto de vetores ([[MOC - Álgebra Vetorial|GA]]) no plano, ou no espaço.
2. [[Espaço Euclidiano n-dimensional]].
3. Espaço de [[Matrizes]] $n \times m$ (ver minha **discussão**).
4. Conjunto dos pontos de uma [[Retas|reta]] que passa pela origem.
5. Conjunto dos pontos de um [[Planos|plano]] que passa pela origem.
6. Conjunto solução de um [[Sistemas Lineares|sistema linear homogêneo]] (ver sessão de Subespaços)
7. Conjunto $\mathbb{P}_{n}$ dos polinômios de grau até $n$ (ver slide e nota de aula 9)

> [!comentario]
> Em $(1)$, tratamos principalmente de $2$ EV (o $\mathbb{R}^{2}$ e o $\mathbb{R}^{3}$). Em $(2)$, temos infinitos. Em $(3)$ temos infinitos também, sendo um EV para cada $m$ e $n$.

> [!obs]
> Em todos esses casos, ao provarmos os $8$ axiomas, caímos em operações com os números reais. Por se tratar de um [[A. Axiomas de Corpo|corpo]], eles já tem todas essas propriedades. Então, nós apenas **as extrapolamos para os elementos dos nossos candidatos a EV**.
> 
> Ver minha **discussão** em [[Matrizes]] para entender as **pontes** entre EV e corpos.


# Exemplos que NÃO são EV

- Conjunto dos números naturais.
- Conjunto dos números inteiros.
- Conjunto dos pontos de uma reta que não passa pela origem.
- Conjunto dos pontos de um plano que não passa pela origem.
- Conjunto solução de um sistema linear não homogêneo.
- Conjunto matrizes invertíveis.

> [!comentario]-
> O conjunto dos inteiros não é um EV, porque a nossa multiplicação por escalar está definida no corpo dos reais. Mas, quando fazemos esse escalar multiplicado por um inteiro, o resultado não necessariamente é inteiro, logo esse conjunto não possui essa operação bem definida.
> 
> Quando falamos de soma e produto por escalar, nos referimos às operações usuais que estamos acostumados. Logo vamos ver que a escolha de outras operações interfere se nosso conjunto é EV ou não.


# EV com operações não usuais

> [!exemplo]
> Seja $\mathbb{V}=\{x \in \mathbb{R} ; x>0\}$ com as operações:
> 
> $
> \begin{aligned}
> x \oplus y & =x \cdot y \\
> \alpha \odot x & =x^\alpha
> \end{aligned}
> $
> 
> Bom, antes de começar, veja que: com as operações usuais dos $\mathbb{R}$, o conjunto $\mathbb{V}$ não é EV, porque não tem o elemento neutro, nem o inverso e a multiplicação por escalar não é fechada. Mas será que ao mudar para as operações acima, tornamos $\mathbb{V}$ um EV?
> 
> 1. $1 \in \mathbb{V}$, logo $\mathbb{V} \neq  \emptyset$
> 
> 2. Verificar se $\mathbb{V}$ é fechado para $\odot$ e $\oplus$
> 	* Se $x$ e $y \in \mathbb{V}$ então $x \oplus y = xy > 0$, pois $x>0$ e $y>0$. Logo, $x \oplus y \in \mathbb{V}$.
> 	* Se $x \in \mathbb{V}$ e $\alpha \in \mathbb{R}$ então $\alpha \odot x = x^{\alpha} > 0 \implies \alpha \odot x \in \mathbb{V}$
> 
> 3. Verificar os axiomas. Sejam $x,y,z \in \mathbb{V}$ e $\alpha, \beta \in \mathbb{R}$
> 	* A1. $x \oplus y = xy = yx = y \oplus x$
> 	* A2. Como o resultado de $(x\oplus y)\oplus z$ é um **número real**, faz sentido falarmos em subtração. Queremos chegar que a diferença entre eles é o zero dos reais:
> $
> \begin{gather}
> [(x\oplus y)\oplus z] - [x \oplus (y \oplus z)] =\\
> [(xy)z] - [x(yz)] = 0 \\
> \therefore (x\oplus y)\oplus z = x \oplus (y \oplus z)
> \end{gather}
> $
> 	* **A3. (neutro aditivo)** Dado $x \in \mathbb{V}$ temos que
> $
> 1 \oplus x = 1x = x \;\implies \; \bar{0} = 1
> $
> 	* **A4. (inverso aditivo)** Dado $x \in \mathbb{V}$ temos que $\frac{1}{x} \in \mathbb{V}$
> $
> x \oplus \frac{1}{x} = x \cdot \frac{1}{x} = 1 = \bar{0} \;\;\text{e} \;\; \frac{1}{x}=-x
> $
> 
> $
> \text{$\mathbb{V}$ com estas operações é um espaço vetorial.}
> $

> [!obs]
> Concluímos então que o Espaço Vetorial não é só um conjunto, mas sim a **tripla**: conjunto, operações de soma e de multiplicação por escalar $(\mathbb{V}, \oplus, \odot)$.


# Propriedades

As propriedades que vamos ver agora são válidas para qualquer EV, inclusive para o conjunto maluco que acabamos de ver.

> [!teorema]
> Considere $\mathbb{V}$ um espaço vetorial com operações $\oplus \; \mathrm{ e } \;\odot$. Sejam $u$, $v$ e $w \in \mathbb{V}$, $\overline{0}$ um neutro aditivo de $\mathbb{V}$ e $-u$ um inverso aditivo do vetor $u$. Nestas condições, são válidas as seguintes propriedades:
> i) (Lei do cancelamento) $v \oplus u=w \oplus u \Rightarrow v=w$.
> ii) O neutro aditivo é único.
> iii) Para cada $u \in \mathbb{V}$, o inverso aditivo de $u$ é único.
> iv) $0 \odot u=\overline{0}$.
> v) $(-1) \odot u=-u$.

> [!demonstracao]- Ideia da demonstração.
> i) $v \oplus u=w \oplus u \Rightarrow(v \oplus u) \oplus(-u)=(w \oplus u) \oplus(-u) \stackrel{\mathrm{A} 2}{\Rightarrow} v \oplus(u \oplus(-u))=w \oplus(u \oplus(-u)) \stackrel{\mathrm{A} 4}{\Rightarrow} v \oplus \overline{0}=w \oplus \overline{0} \stackrel{\mathrm{~A} 3}{\Rightarrow} v=w$.
> ii) Sejam $\overline{0}$ e $\tilde{0}$ neutros aditivos. Então: $\overline{0} \stackrel{\mathrm{~A} 3}{=} \overline{0} \oplus \tilde{0} \stackrel{\mathrm{~A} 1}{=} \tilde{0} \oplus \overline{0} \stackrel{\mathrm{~A} 3}{=} \tilde{0}$.
> iii) Sejam $\hat{u}$ e $\tilde{u}$ inversos aditivos de $u$. Então: $\hat{u} \oplus u \stackrel{\mathrm{~A} 4}{=} \overline{0} \stackrel{\mathrm{~A} 4}{=} \tilde{u} \oplus u \stackrel{(\mathrm{i})}{\Rightarrow u}=\tilde{u}$.
> iv) $\overline{0} \oplus(0 \odot u) \stackrel{\mathrm{A} 3}{=} 0 \odot u=(0+0) \odot u \stackrel{\mathrm{~A} 6}{=}(0 \odot u) \oplus(0 \odot u) \stackrel{(\mathrm{i})}{\Rightarrow} \overline{0}=0 \odot u$.
> v) $\quad((-1) \odot u) \oplus u \stackrel{\text { A8 }}{=}((-1) \odot u) \oplus 1 . u \stackrel{\text { A6 }}{=}((-1)+1) \odot u=0 \odot u \stackrel{\text { (iv) }}{=} \overline{0}$. Ou seja, $(-1) \odot u$ é oposto aditivo de $u$.
> 
> Ver demonstrações na minha nota de aula 9.


# Subespaço Vetorial

> [!exemplo]- Exemplo $(1)$ Conjunto solução do SL homogêneo é um Subespaço Vetorial.
> Fixado $A \in M_{n \times m}$ e $S = \{X \in M_{m \times 1} \text{ tal que } AX=\bar{0}_{m\times 1} \}$.
> * $S$ não é vazio, pois $A \bar{0}_{m \times 1} = \bar{0}_{n \times 1}$
> * Sejam $x_{1}$ e $x_{2} \in S$ e $\alpha \in \mathbb{R}$. Temos que
> 	* (i) $A(X_{1}+X_{2}) = AX_{1} + AX_{2} = \bar{0}+\bar{0}=\bar{0} \implies X_{1}+X_{2}\in S.$
> 	* (ii) $A(\alpha X_{1}) = \alpha (AX_{1})= \alpha \bar{0} = \bar{0} \implies \alpha X_{1} \in S.$
> 
> Agora, temos que provar os $8$ axiomas. Mas veja: estamos usando a mesma soma e o mesmo produto por escalar de matrizes usual. Como $S \subset M_{n \times 1}$ e possui as duas operações **bem definidas**, ele herda esses $8$ axiomas. 
> 
> Poderíamos até duvidar da veracidade dos axiomas $3$ e $4$ (elemento neutro e inverso aditivo). Mas veja que eles também são automaticamente satisfeitos se as op. estão bem definidas e $S \subset \mathcal{V}$, onde $\mathcal{V}$ é um EV **qualquer**: 
> * ($3$) Temos certeza que o neutro vai estar dentro desse subconjunto $S$? Bom, como qualquer múltiplo por escalar está dentro dele, uma vez que ele é **fechado** e está **contido num EV**, em particular $0 \odot X = \bar{0}$ também vai estar lá.
> * ($4$) De modo análogo, como qualquer múltiplo por escalar está lá dentro, sabemos por um teorema que $-1 \odot X = - X$ , que é o oposto de $X$ também está.
> As outras características não dependem de nada da característica do nosso vetor. Então, se já valiam pro nosso conjunto EV maior, ou no caso: $S$ é restrição do EV das matrizes $M_{n \times 1}$, vão se manter todas válidas.

> [!exemplo]- Exemplo $(2)$ Conjunto das matrizes invertíveis **não** é um Subespaço Vetorial.
> 
> Tome $A \in \mathbb{M}_{n \times n}$ as matrizes invertíveis e $S = \{X \in \mathbb{M}_{n \times n}; X = A^{-1}\}$
> 1. $I = I^{-1} \implies I \in S$
> 2. Queremos mostrar que $X_{1} = A_{1}^{-1}$ e $X_{2}=A_{2}^{-1}$ $\implies X_{1}+X_{2}=A_{3}^{-1}$.
> $
> X_{1}+X_{2}=A_{1}^{-1}+A_{2}^{-1} \neq (A_{1}+A_{2})^{-1}
> $
> 3. Queremos mostrar que $X=A^{-1}$ e $\alpha \in \mathbb{R}$ $\implies \alpha X=B^{-1}$.
> $
> \alpha X = \alpha A^{-1} \neq (\alpha A)^{-1}
> $
> 
> Estamos usando (i) os reais como nosso corpo e (ii) as **operações matriciais usuais** de soma e multiplicação por escalar. 
> 
> Se alterássemos (i), poderia ser que o conjunto das matrizes invertíveis viesse a se tornar um subespaço vetorial? Pode sim, poderíamos definir sobre os complexos, mas daí teríamos que VRF se as nossas operações são válidas nesse corpo.
> 
> Agora, se alterássemos (ii) para algumas operações malucas $\odot$ e $\oplus$, pode ser que o nosso conjunto seja bem definido para elas. Daí, nós teríamos que provar também os $8$ axiomas, pois, como não estamos mais falando das **operações matriciais usuais**, não podemos mais herdá-las do EV maior $\mathbb{M_{n \times n}}$. 
> 
> Resumindo: O conjunto $S$ não pode ser um subespaço vetorial de $\mathbb{M_{n \times n}}$ com as operações usuais. Mas ele ainda pode ser um Espaço Vetorial com operações não usuais.

Ver [[Subespaços Vetoriais em GA]].

![[Pasted image 20260419155324.jpg|center|]]

> [!definicao]
> Um subconjunto $\mathbb{W}$ de um espaço vetorial $\mathbb{V}$ é denominado **Subespaço Vetorial** de $\mathbb{V}$ se $\mathbb{W}$ for um espaço vetorial por si só com as operações de adição e multiplicação por escalar **definidas** em $\mathbb{V}$.

> [!obs]-
> $\mathbb{W}=\mathbb{V}$ é um subespaço vetorial do espaço vetorial $\mathbb{V}$.
> $\mathbb{W}=\left\{\overline{0}_{\mathbb{V}}\right\}$ é um subespaço vetorial do espaço vetorial $\mathbb{V}$.
> Um detalhes interessante é que, se $\mathbb{W}$ é subespaço vetorial, o vetor nulo necessariamente pertence a $\mathbb{W}$. Dessa forma, o subconjunto $\mathbb{V-W}$ não pode nunca ser um subespaço vetorial.


> [!teorema]
> Se $\mathbb{W}$ for um subconjunto de um espaço vetorial $\mathbb{V}$ , então $\mathbb{W}$ é um subespaço vetorial de $\mathbb{V}$ se, e somente se, as seguintes condições forem válidas.
> 1. $\mathbb{W}$ não é vazio.
> 2. Se $u$ e $v$ forem vetores em $\mathbb{W}$, então $u \oplus v \in \mathbb{W}$.
> 3. Se $\alpha$ for um escalar qualquer e $u \in \mathbb{W}$, então $\alpha \odot u \in \mathbb{W}$.

> [!demonstracao]
> (Ideia da dem.)
> ( ⇒ ) Se $\mathbb{W}$ é subespaço de $\mathbb{V}$, por definição, será um espaço vetorial. Logo são válidas as propriedades acima.
> $(\Leftarrow)$ Os axiomas A1, A2, A5, A6, A7 e A8 são herdados de $\mathbb{V}$. Seja $w \in \mathbb{W}$ (existe pelo item 1). Então $0 \odot w=\overline{0} \in \mathbb{W}$ e $(-1) \odot w=-w \in \mathbb{W}$, pelo item 3, garantindo os axiomas A3 e A4.
> **Obs.:** Note que, neste contexto, podemos trocar verificar $\mathbb{W} \neq \emptyset$ por $\overline{0} \in \mathbb{W}$. Caso não pertença, já podemos afirmar aqui que $\mathbb{W}$ **não** é subespaço vetorial. Caso pertença, provamos $(1)$ e agora falta provar $(2)$ e $(3)$.

Isso confirma o que usamos no **exemplo $1$** do SL homogêneo acima. 

Podemos provar $(2)$ e $(3)$ de uma vez só mostrando que $(\alpha \odot u) \oplus v \in \mathbb{W}$, pois, se $v=\bar{0}$, temos a multiplicação por escalar e, se $\alpha=1$, temos a soma. De forma rigorosa, só podemos fazer isso quando já sabemos que as propriedades do EV são válidas, como é o caso de mostrar que um subconjunto de um EV é SubEV.

**Cuidado!** Isso só vale se já sabemos previamente que $\mathbb{V}$ é EV. Caso contrário, devemos mostrar que $\mathbb{W}$ satisfaz os $8$ axiomas. Ou ainda, se estivermos testando $\mathbb{W}$ com outras operações diferente das usuais de $\mathbb{V}$, demos mostrar que os $8$ axiomas são válidos também.


> [!exemplo]-
> O que esse teorema nos diz resumidamente é que: basta provar que as operações estão definidas para o subconjunto. Em outras palavras, que não tem nenhum vetor que "escapa" do conjunto quando fazemos as operações.
> 
> Abaixo, vemos justamente um exemplo de conjunto cujos vetores "escapam"... Relembre [[Planos]].
> $
> \begin{gather}
> \mathbb{V} = \mathbb{R}^{3} \\
> \text{(pode ser tanto triplas ordenadas quanto vetores no espaço tridimensional).} \\
> \mathbb{W} = \{(x,y,z) \in \mathbb{R}^{3}; x+y=1\}
> \end{gather}
> $
> 
> Geometricamente, trata-se de um plano que não passa pela origem, pelo que o **vetor nulo** (elemento neutro da **respectiva operação**) **não** está nesse subconjunto. Isso já é **suficiente** para ele não ser um subespaço vetorial de $\mathbb{R}^{3}$ (pelo menos não com essas operações).

Ver slide e a minha nota de aula 9 para mais detalhes e outros exemplos interessantes. 

