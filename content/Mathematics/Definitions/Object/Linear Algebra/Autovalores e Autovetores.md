Data Criada: 09/06/2026 às 16:38
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Relaciona-se com as direções nas quais as [[Transformações Lineares]] apenas multiplicam o vetor por um número (não muda a direção). Para viabilizar isso, o espaço domínio deve ser o mesmo do contradomínio. Até poderia ser que $\mathbb{W}$ em $T: \mathbb{V} \rightarrow \mathbb{W}$ fosse subespaço de $\mathbb{V}$, mas de modo geral trabalhamos apenas com **operadores lineares**.

Esses conceitos são uma alternativa pro que vínhamos fazendo até agora. Ao invés de olharmos quais os vetores que originam um espaço, como
$$
T(x,y)= (2x+y,2y) = (2x,0) + (y,2y) = x(2,0) + y(1,2) = span\{(2,0), (1,2)\}
$$
Nós olhamos quais os números $\lambda$ e vetores $v$ para os quais a direção não se altera
$$
T(x,y)= (2x+y,2y) = (2x,0) + (y,2y) = \underbrace{2}_{\lambda}\underbrace{(x,0)}_{v} + (y,2y)
$$
Aqui, $v=(1,0)$ é o autovetor associado ao autovalor $\lambda=2$.


> [!definicao] Definição.
> Seja $T: \mathbb{V} \rightarrow \mathbb{V}$ um operador linear. Se existirem $v \in \mathbb{V}, v \neq \overline{0}$, e $\lambda \in \mathbb{R}$ tais que $T(v)=\lambda v, \lambda$ é um **autovalor** de $T$ e $v$ um **autovetor** de $T$ associado a $\lambda$.

> [!obs]
> Esses conceitos são relativos a uma Transformação Linear específica. Se a trocarmos, trocamos tudo acima também.

**Obs.** O vetor nulo não entra como autovetor ($v \neq \bar{0}$) por convenção. Porém, para que os autovetores formem um subespaço vetorial, acabamos incluindo-o no autoespaço.

**Obs.** Não há restrições para o $\lambda$. Pode ser até igual a zero. Veremos logo que
$$
\begin{gather}
v \in N(T) \implies T(v)=\bar{0}=0 \cdot v \implies \\ \\
\text{$v$ é autovetor associado ao autovalor $\lambda = 0$}
\end{gather}
$$


# Propriedades: introdução

> [!teorema]
> Seja $T: \mathbb{V} \rightarrow \mathbb{V}$ um operador linear.
> 1. Se $v \in N(T)-\{\overline{0}\}$, então $v$ é autovetor de $T$ associado ao autovalor 0 .
> 2. Se $w$ é um autovetor de $T$ associado ao autovalor $\lambda$, então qualquer múltiplo não nulo de $w$ também é autovetor de $T$ associado ao mesmo autovalor $\lambda$.
> 3. Se $\lambda$ é um autovalor de $T$, então $\mathbb{S}_\lambda:=\{v \in \mathbb{V} ; T(v)=\lambda v\}$ é um subespaço vetorial de $\mathbb{V}$. ( $\mathbb{S}_\lambda$ autoespaço de $T$ associado ao autovalor $\lambda$.)

**Atenção.** Na propriedade (3), vemos que o **autoespaço** é relacionado a cada **autovalor**. Além disso, pela propriedade (2) vemos que, se existe um certo autovetor, então o espaço gerado por ele é um autoespaço obrigatoriamente. Um autoespaço pode ter dimensão maior que 1...

> [!obs]
> Se $T$ é um operador linear **não injetivo**, $T$ possui ao menos **1 autovetor**, uma vez que, pelo resultado que vimos em [[Injetividade e Sobrejetividade]],
> $
> N(T) \neq \bar{0} \implies \exists \; v; \; T(v)=\bar{0}=0 \cdot \bar{0}
> $
> pelo que $v$ é um **autovetor** associado ao **autovalor** $\lambda = 0$. Se temos nulidade 1, já saberíamos que o $0$ é autovalor.
> Outra forma de verificar isso é que, pela definição de não injetividade, existem $u,v$ tais que
> $
> T(u)=T(v) \implies T(u)-T(v)=\bar{0} \implies T(u-v)=\bar{0}
> $
> Como $u \neq v$, a diferença $u-v$ resulta um vetor $x$ não nulo, pelo que
> $
> T(x)=\bar{0}=0 \cdot \bar{0} \implies \lambda = 0
> $
> Por outro lado, os operadores **injetivos** (como a rotação) com certeza **não tem autovalores** (nem mesmo $\lambda = 0$)

**Obs.** Conforme já falado,
* $\bar{0}$ não vale como autovetor
* 0 pode ser autovalor


# Desenvolvimento

Inicialmente, queremos desenvolver um método para achar os possíveis $\lambda$. A primeira vista, parece razoável montar e resolver sistemas lineares, como abaixo. Seja $T: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$ tal que $(x,y) \mapsto (2x+y,2y)$...
$$
\begin{aligned}
&\text { Quero }(x, y) \neq \overline{0} \text { tal que }\\ 
&\begin{aligned}
& T(x, y)=\lambda(x, y) \\
\Rightarrow & (2 x+y, 2 y)=\lambda(x, y) \\
\Rightarrow & \left\{\begin{array}{l}
2 x+y=\lambda x \\
2 y=\lambda y
\end{array}\right. \\
\Rightarrow & \left\{\begin{array}{l}
(2-\lambda) x+y=0 \\
(2-\lambda) y=0
\end{array}\right.
\end{aligned}
\end{aligned}
$$
Mas atenção: para que possamos aplicar nossos conhecimentos de SL aqui, devemos considerar o $\lambda$ como uma constante, apesar dele ser desconhecido por enquanto. Por isso, devemos separar o sistema em casos: aqui, vemos que ou (i) $y=0$ ou (ii) $\lambda=2$. Agora sim temos sistemas lineares dentro de cada caso e podemos resolvê-los separadamente.
**ESTÁ REALMENTE CERTO ISSO?**

**Obs.** É mais direto escrever as equações do SL na forma fatorada. Assim, caímos na resposta desejada ou no caso $x=0$ e $y=0$, que não nos interessa. Dividir direto em casos, por outro lado, como por ex, $y=0$ e $y \neq 0$, é passível de chegarmos em contradições.

Dá pra ver que isso escalona rapidamente em espaços de dimensão maior. Por isso, tomaremos outra linha de raciocínio...

> [!exemplo]-
> A rotação 
> $
> T(x,y) = (y,-x)
> $
> é um exemplo clássico de TL que não admite autovalores e, consequentemente, não tem autovetores (é fácil de pensar geometricamente, porque todos os vetores mudam de direção).
> 
> Por consequência, sabemos que a rotação é uma TL injetiva pelo resultado que vimos.


Vimos em [[Matriz de uma Transformação Linear]] que toda TL pode ser representada por uma matriz. Então, seja $T: \mathbb{V} \rightarrow \mathbb{V}$ representado pela matriz $A$ (bases canônicas). Quero $v \neq \overline{0}$ tal que
$$
\begin{aligned}
T(v)  =\lambda v \;\;\leftrightarrow\;\;
A v =\lambda v \;\;\leftrightarrow\;\;
A v-\lambda v  =\overline{0} \;\;\leftrightarrow\;\;
(A-\lambda l) v  =\overline{0}
\end{aligned}
$$
Formamos um SLH, que possui apenas a solução trivial ou infinitas soluções. A solução trivial $v=\bar{0}$ não nos interessa aqui pelo que já falamos. Então, só nos resta condicioná-lo a ter infinitas soluções.

Em outras palavras, para que $\lambda$ seja um **autovalor** devemos ter
$$
\begin{equation}
\begin{aligned}
&\underbrace{\operatorname{det}(A-\lambda I)}_{p(\lambda)}=0\\
&\text { polinômio característico }
\end{aligned}
\end{equation}
$$
Esse polinômio tem grau menor ou igual à dimensão $n$ de $\mathbb{V}$ (dom. e contradom.). 

**Obs.** Quando um mesmo autovalor $\lambda$ é raiz do polinômio característico $k$ vezes, ele formará um autoespaço de dimensão menor ou igual a $k$.

> [!obs]
> O ponto de virada é que
> 1. **Determinar autovalores:** o determinante depende unicamente de $\lambda$. Então, acharemos primeiro as soluções de $\lambda$ no polinômio característico. 
> 2. **Determinar autovetores:** Caso hajam soluções para $\lambda$, isto é, autovalores, caímos em SLH's relativos a cada valor de $\lambda$. O **espaço solução** de cada SLH é o autoespaço de cada autovalor $\lambda$.
> 
> Nós queremos fugir de sistemas não lineares, por isso realizamos a etapa 1 para só então lidar com SL de fato na etapa 2, já que agora sim $\lambda$ é determinado.
>    
> Note que, como forçamos que os SLH tenham determinante nulo, o espaço solução, se existir, terá infinitas soluções, jamais uma única, até porque um espaço vetorial tem infinitos vetores.


# Espaços vetoriais quaisquer

Tratamos até agora com operadores no $\mathbb{R}^{n}$. Mas e se estivermos lidando com um operador linear num espaço vetorial $\mathbb{V}$ qualquer de dimensão $n$? Como fazemos esses cálculos?

A gente cria um isomorfismo (relembre [[Injetividade e Sobrejetividade]]) que vai de $\mathbb{V} \rightarrow \mathbb{R}^{n}$, faz a conta no $\mathbb{R}^{n}$ e depois volta pelo inversa do isomorfismo (discutimos isso em [[Transformações Lineares]]).

A forma mais fácil (não é a única) de criar esse isomorfismo é associar cada elemento duma base de $\mathbb{V}$ a cada elemento duma base de $\mathbb{R}^{n}$ respectivamente e depois extender ao espaço todo. Relembre [[Transformação Linear Definida na Base]].

Não necessariamente conseguimos a base canônica de $\mathbb{V}$, porque ele pode ser um subespaço. Mas, nós sempre podemos associar à base canônica de $\mathbb{R}^{n}$ para facilitar.

![[Pasted image 20260609203057.jpg|center|400]]

$\tilde{T}:\mathbb{R}^{n} \rightarrow \mathbb{R}^{n}$ é a transformação associada análoga ao operador linear $T:\mathbb{V} \rightarrow \mathbb{V}$.

> [!obs]
> (i) quando lidamos entre EV diferentes, como $\mathbb{R}^n \rightarrow \mathbb{P}_1$, a equação $T(v) = λv$ nem fecha por tipo — $T(v) \in P_1$ e $λv \in \mathbb{R}$. O que se calcula de fato são os autovalores da **matriz** [T] nas bases escolhidas. A questão é informal nesse ponto; autovalor/autovetor "de verdade" só existe para operador T: V → V
> (ii) esse isomorfimso é um mapa de coordenadas, cuja matriz mudança de base é uma caso particular (costuma ser reservado para quando você tem _duas_ bases do mesmo espaço e converte coordenadas de uma para outra).


# Propriedades de autovalores e autovetores

[[Propriedades de autovalores e autovetores]]