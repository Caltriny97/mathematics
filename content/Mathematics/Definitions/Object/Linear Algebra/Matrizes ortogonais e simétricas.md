Data Criada: 23/06/2026 às 18:23
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Matrizes ortogonais

> [!definicao]
> Uma matriz $A$ de ordem $n \times n$ é dita **ortogonal** se suas colunas formam um conjunto ortonormal de vetores.
> 
> **Obs.** não precisa ser em relação ao produto interno usual.

Para falarmos nisso, temos que ter um [[produto interno]] definido. 

> [!teorema]
> Uma matriz $A_{n \times n}$ é ortogonal se, e somente se,
> $
> A A^{\top}=A^{\top} A=I .
> $
> **Obs.:** $A A^{\top}=A^{\top} A=I$ garante que $A^{\top}=A^{-1}$.

> [!obs]-
> Esse teorema nos fala duas coisas: (i) a inversa existe e (ii) é igual à transposta.
> 
> (i) é trivial, porque, se $A$ é ortogonal, então suas colunas são ortogonais, logo são LI (aquele teorema da minha nota de aula), pelo que a matriz é inversível.
> 
> (ii) nos facilita muito, visto que é muito mais fácil calcular a transposta do que a inversa.

> [!teorema]
> Seja $\mathbb{V}$ um espaço vetorial real de dimensão finita munido de um produto interno $\langle\cdot, \cdot\rangle$. Então existe uma base $\mathcal{B}$ de $\mathbb{V}$ tal que, para quaisquer $x, y \in \mathbb{V}$,
> 
> $
> \langle x, y\rangle=[x]_{\mathcal{B}}^{\top}[y]_{\mathcal{B}} .
> $


> [!discussao] Produto Interno...
> Nós já usamos isso algumas vezes, mas com o produto interno usual induzido por uma base genérica.
> 
> A novidade aqui é: não importa qual o produto interno escolhido. O resultado nos garante que, em **qualquer** produto interno, nós conseguimos **uma base** (talvez não com a base canônica) no qual é possível escrever o PI nessa forma matricial.
> 
> Tudo é uma ganha e perde: 
> * lá em [[produto interno]], vimos é possível tomar o PI "usual" induzido numa base qualquer (útil para deixá-la ortogonal) e usufruir da multiplicação matricial. 
> * Agora, por outro lado, vemos que **qualquer** PI pode ser escrito na forma matricial, desde que tomemos uma base específica... vamos ver qual é.
> 
> **Abuso de notação:** quando escrevemos
> $
> \langle x, y\rangle= x^{T}y
> $
> estamos lidando com a representação matricial de $x$ e $y$. Na verdade, queremos dizer as coordenadas de $x$ e $y$ na base canônica.
> 
> No $\mathbb{R}^{n}$, essa notação é conveniente porque, olhando o PI usual, essas coordenadas são as próprias coordenadas na base canônica (poderíamos pegar outra). Mas, se estivermos usando outro PI, podemos escolher uma base no qual isso é verdade.
> 
> **E por que temos certeza que isso sempre é possível?** Graças ao processo de [[Ortogonalização de Gram-Schmidt]].
> 
> A **base** que obtivermos ao final do processo, será justamente essa base $\mathcal{B}$ (ortogonal ou até ortonormal) em que $\langle x, y\rangle=[x]_{\mathcal{B}}^{\top}[y]_{\mathcal{B}}$. Veja que qualquer base ortonormal (mediante o PI adotado) serve para a escolha de $\mathcal{B}$.
> 
> Portanto, essa base $\mathcal{B}$ não é uma base desatrelada do produto interno, afinal o processo de ortogonalização é feito em cima dele. Ver prova na minha nota de aula 22.
> 
> 
> **Resumo (i):** Não importa qual o PI, nós conseguimos escrevê-lo nessa forma matricial, só que eventualmente teremos que escolher uma base mais adequada (que não a base canônica): deve ser uma base ortonormal mediante esse PI.
> 
> **Resumo (ii):** Dado um PI qualquer, imagine que desejemos calcular $\langle x, y\rangle$ mediante ele. Basta escrevemos as coordenadas de $x$ e $y$ numa base $\mathcal{B}$ ortonormal qualquer (mediante esse PI). Assim, o resultado de $\langle x, y\rangle$ é simplesmente o produto matricial $[x]_{\mathcal{B}}^{\top}[y]_{\mathcal{B}}$.
 

# Operadores auto-adjuntos

Essa definição de matriz ortogonal é uma definição puramente matricial. Qual a relação entre isso e a visão do operador?

> [!definicao] Definição (versão do operador)
> Um operador $T: \mathbb{V} \rightarrow \mathbb{V}$ em um espaço vetorial munido de produto interno é dito **auto-adjunto** quando
> 
> $
> \langle T(v), u\rangle=\langle v, T(u)\rangle
> $
> 
> para quaisquer $u, v \in V$.

> [!exemplo]
> Ex. $\mathbb{V}=\mathbb{R}^2$ com produto interno usual e $T: \mathbb{V} \rightarrow \mathbb{V}$ dado por $T\left(v_1, v_2\right)=\left(3 v_1+v_2, v_1+5 v_2\right)$.
> 
> $
> \begin{aligned}
> & \langle T(v), u\rangle-\langle v, T(u)\rangle \\
> = & \left\langle\left(3 v_1+v_2, v_1+5 v_2\right),\left(u_1, u_2\right)\right\rangle-\left\langle\left(v_1, v_2\right),\left(3 u_1+u_2, u_1+5 u_2\right)\right\rangle \\
> = & \left(3 v_1+v_2\right) u_1+\left(v_1+5 v_2\right) u_2-\left[v_1\left(3 u_1+u_2\right)+v_2\left(u_1+5 u_2\right)\right] \\
> = & 0
> \end{aligned}
> $
> 
> Como é a matriz desse operador usando a base canônica?
> $
> [T]_{\mathcal{C}}=\left[\begin{array}{ll}
> 3 & 1 \\
> 1 & 5
> \end{array}\right]
> $
> Nós estamos usando a base canônica, porque estamos usando o produto interno canônico, que mediante a base canônica, dá para escrevermos naquela forma de produto matricial.
> 
> Perceba que essa matriz é simétrica...


Vamos descobrir agora a representação matricial dum operador auto-adjunto

Lembremos que $\langle X, Y\rangle=X^{\top} Y$ para todo operador numa certa base. Logo
$$
\begin{gathered}
\langle A X, Y\rangle=(A X)^{\top} Y=\left(X^{\top} A^{\top}\right) Y=X^{\top}\left(A^{\top} Y\right)=\left\langle X, A^{\top} Y\right\rangle . \\
\langle T(v), u\rangle=\langle A v, u\rangle=\left\langle v, A^{\top} u\right\rangle \underbrace{=}_{*} \langle v, A u\rangle = \langle v, T( u)\rangle .
\end{gathered}
$$
para que a igualdade $*$ aconteça e tenhamos uma matriz auto-adjunta, devemos ter $A=A^{T}$, isto é, a matriz $A$ deve ser simétrica

Então, é equivalente dizer:
* (i) o operador é auto-adjunto 
* (ii) a matriz do operador é simétrica (numa base específica...)

> [!obs]
> Quando falamos na matriz do operador, estamos falando duma base específica (lembre de [[Propriedades de autovalores e autovetores]] que a base escolhida muda a matriz do operador)
> 
> Mas tudo bem, porque, quando falamos de autoadjunto, estamos de posse de um produto interno específico. Assim, a base específica que estamos tomando é tal que
> $
> \langle x, y\rangle= x^{T}y
> $
> nessa base (convenção diferente da discussão acima, em que tomávamos a base canônica).


> [!resumo]
> Dado um operador linear qualquer, podemos ter infinitas bases pro domínio e infinitos produtos internos.
> 
> O que estamos fazendo é 
> * pegar o operador munido de um certo produto interno
> * fixado isso, nós encontramos a base de $\mathbb{V}$ tal que $\langle u, v\rangle= u^{T}v$ (vimos que é possível graças ao teorema)
> * Uma vez feito isso, dizemos que $T$ ser autoadjunto é a mesma coisa que a matriz de $T$ ser simétrica nessa base.
> 
> Vamos ver jajá que operadores que possuem essa propriedade têm uma vantagem muito grande na [[diagonalização]] (elas são sempre diagonalizáveis...e de um jeito muito especial)

> [!obs]
> Ser auto-adjunto **não** é uma propriedade que vai e vem conforme a base. Fixado o produto interno, T é auto-adjunto ou não é, ponto — é um fato sobre o operador, independente de base. O que depende da base é outra coisa: se a **matriz** [T] sai simétrica ou não.

Agora, enunciaremos o teorema que sintetiza tudo isso.

> [!teorema]
> $T: \mathbb{V} \rightarrow \mathbb{V}$ é um operador auto-adjunto se, e somente se, sua matriz $[T]_{\mathcal{B}}=A$ relativa a uma base ortonormal $\mathcal{B}=\left\{v_1, \cdots, v_n\right\}$ é uma matriz simétrica.
Note que aqui ele já toma por hipótese a base $\mathcal{B}$ sendo ortonormal. É exatamente a mesma coisa dos teoremas anteriores, só que pulando o Gran Schmidt.


> [!teorema] Teorema (versão operador).
> Se $T$ é um operador auto-adjunto, então autovetores de $T$ associados a autovalores distintos são ortogonais.

> [!teorema] Teorema (versão matricial).
> Se $A$ é uma matriz simétrica, então autovetores de $A$ associados a autovalores distintos são ortogonais.

Nós já sabíamos que autovetores associados a autovalores distintos eram LI. Só que, no caso de operadores auto-adjuntos/matrizes simétricas, temos um resultado mais forte do que ser LI: são ortogonais.


> [!relembrando]
> Pra discutirmos se $A$ era diagonalizável, nós 
> * primeiro calculamos os autovalores. 
> * Para achar a base de autovetores de $\mathbb{V}$, nós calculamos os as bases de autovetores de cada autoespaço ass. a cada autovalor.
> * Por fim, juntávamos todas essas mini bases $\mathcal{B}_{i}$ para formar a base $\mathcal{B}$ do espaço vetorial $\mathbb{V}$ inteiro.
> $
> \mathcal{B} = \bigcup_{\mathcal{B}_{i} \; \text{base de} \;\mathbb{S}_{i}}\mathcal{B}_{i}
> $

Agora, nós temos autovetores ortogonais para autovalores distintos, ou seja, $b_{ik} \in \mathcal{B}_{i} \; \text{e} \; b_{jl} \in \mathcal{B}_{j}$ são ortogonais. Só que tem um problema: nada garante que os autovetores geradores do mesmo autoespaço $b_{i1}, b_{i2},\dots,b_{in}$ vão ser ortogonais entre si. Mas tudo bem, é só nós, ao invés de tomarmos geradores quaisquer, concentrarmos em pegar geradores ortogonais ([[Ortogonalização de Gram-Schmidt]]). Assim, teremos uma base $\mathcal{B}$ ortogonal de autovetores para todo o espaço $\mathbb{V}$.

Como consequência direta desses últimos dois teoremas, temos que: se a matriz for **diagonalizável** **e** o operador **for auto-adjunto**, então nós podemos conseguir uma base ortogonal de autovetores para o espaço (claro que podemos normalizar cada gerador para ter uma base ortonormal). Na verdade, **todo** operador auto-adjunto é diagonalizável. É o que o [[Teorema Espectral]] nos diz.

> [!discussao]
> Uma dúvida que eu tive durante a aula foi: supondo que o operador $T$ é auto-adjunto, como os autoespaços são invariantes, então vale que os autovetores são ortogonais, certo? Não, porque aí estaremos olhando para um único autovalor, o que não nos garante a propriedade dos autovalores serem ortogonais.
> 
> Inclusive, sobre essa relação entre operadores auto-adjuntos e operadores invariantes, não existe nenhuma relação direta de dependência entre esses dois conceitos, mas se relacionam bastante por meio dos subespaços ortogonais e do [[Teorema Espectral]].


# Teorema Espectral

[[Teorema Espectral]]