```
Data Criada: 11/06/2026 às 16:16
```
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

# Recapitulando...

Definir uma TL que vai de um EV ao mesmo EV é boa prática, mas não é uma restrição exatamente. Nós podemos sim trabalhar com TL que vão de um EV a um subespaço dele.

Por conveniência, tomamos um operador linear e não uma [[Transformações Lineares|TL]] em geral, i.e., para que possamos pegar todo um EV e não só a imagem. Assim garantimos que a matriz $[T]$ seja quadrada e que o cálculo do determinante faça sentido.

Seja 
$$
\begin{gather}
T:\mathbb{V} \rightarrow \mathbb{V}
\end{gather}
$$
Nesse caso em que a matriz é quadrada, é fácil achar os autovalores impondo a condição de ter infinitas soluções. 

Acontece que poderíamos tomar o contradomínio como sendo $\mathbb{W}$ subespaço vetorial de $\mathbb{V}$. Assim, toda a conta ainda faria sentido, porém não chegaríamos numa matriz quadrada, o que tornaria impossível usar o método visto em [[Autovalores e Autovetores]].

Mas pera aí... se $\mathbb{W}$ é subespaço de $\mathbb{V}$, não há problema nenhum colocar $\mathbb{V}$ como contradomínio, visto que a única proibição é reduzir o contradomínio a ponto de sobrar parte da imagem de fora. Como nós só estamos aumentando-o, a regra se mantém a mesma. É claro que estamos mudando a TL como um todo (lembre da tripla que a define em [[Matriz de uma Transformação Linear]])

Assim, lidamos com operadores com matrizes quadradas e com ferramentas interessantes de análise como determinante, condição para invertibilidade de matriz... Por isso que a gente sempre lida com operadores no estudo de autovalores e autovetores.

> [!obs]
> Ver exemplo 1 da minha nota de aula 20.
> 
> Lá concluímos que não há perda de generalidade quando passamos a tratar autovalores e autovetores só de operadores lineares.


# Matrizes semelhantes

> [!container] Introdução.
> Para fazer esse processo de achar [[autovalores e autovetores]], estamos usando a [[matriz de uma transformação linear]], só que isso não é uma descrição precisa do nosso método... porque estamos usando **uma** matriz capaz de representar a TL, porém ela não é **única**: basta trocar uma das bases do dom. ou do contradom. que a matriz muda dentro da mesma TL.
> 
> O ponto é que, mesmo trocando a matriz, obtemos os mesmo autovalores. Quanto aos autovetores, nós vamos obter as coordenadas referentes a cada base dos mesmos autovetores (só que as coordenadas estarão em bases diferentes). Aqui entra o conceito de matrizes semelhantes...

Como estamos num operador, vamos sempre considerar a **mesma** base no domínio e no contradomínio. Tomaremos a seguir a matriz $A$ como a matriz de $T$ na base $\mathcal{A}$ e o mesmo para a matriz $B$ na base $\mathcal{B}$. Qual vai ser a relação entre essas duas coisas?
$$
\begin{gathered}
T: \mathbb{V} \rightarrow \mathbb{V} \\
A=[T]_{\mathcal{A} \rightarrow \mathcal{A}} \quad B=[T]_{\mathcal{B} \rightarrow \mathcal{B}}
\end{gathered}
$$
$$
\overbrace{[I]_{\mathcal{A} \rightarrow \mathcal{B}}[T]_{\mathcal{A} \rightarrow \mathcal{A}}[I]_{\mathcal{B} \rightarrow \mathcal{A}}}^B[v]_{\mathcal{B}}
$$
Olhando mais perto, temos que...
$$
\underbrace{[I]_{\mathcal{A} \rightarrow \mathcal{B}}\underbrace{[T]_{\mathcal{A} \rightarrow \mathcal{A}} \underbrace{[I]_{\mathcal{B} \rightarrow \mathcal{A}}[v]_{\mathcal{B}}}_{[v]_{\mathcal{A}}}}_{[T(v)]_{\mathcal{A}}}}_{[T(v)]_{\mathcal{B}}}
$$
Isso é muito semelhante ao que fizemos na discussão de matriz mudança de base em [[Matriz de uma Transformação Linear]].

Então veja que essas matrizes $A$ e $B$ não são quaisquer. Apesar de elas poderem ser diferentes, elas são **semelhantes** mediante uma matriz **mudança de base** (invertível) quando elas representam o mesmo operador linear. Essa é a definição geral:

> [!definicao] Definição de matriz semelhante.
> Dizemos que uma matriz quadrada $A$ de ordem $n \times n$ é **semelhante** a uma matriz $B$ (também $n \times n$) se existir uma matriz **invertível** $M$ tal que:
> 
> $B = M^{-1}AM$
> 
> Ou, equivalentemente:
> 
> $MB = AM$
> Note que qualquer matriz invertível $n \times n$ pode ser interpretada como uma matriz **mudança de base**!

Em termos de **operador linear**, estamos dizendo que $A$ e $B$ representam o mesmo operador, só que em bases diferentes.


**Então, será que de fato a escolha da matriz $[T]$, que depende da base, não influencia no cálculo dos autovalores e autovetores?**
$$
\begin{array}{ccc} 
& T: \mathbb{V} \rightarrow \mathbb{V} \\
A=[T]_{\mathcal{A} \rightarrow \mathcal{A}} & B=[T]_{\mathcal{B} \rightarrow \mathcal{B}} & B=M^{-1} A M
\end{array}
$$

Usaremos abaixo $v$ como abuso de notação para $[v]_{\mathcal{B}}$

$$
\begin{aligned}
B v=\lambda v & \Rightarrow M(B v)=M(\lambda v) \\
& \Rightarrow(M B) v=\lambda(M v) \\
& \Rightarrow(A M) v=\lambda(M v) \\
& \Rightarrow A(M v)=\lambda(M v)
\end{aligned}
$$
Então, $Mv = M[v]_{\mathcal{B}}$ é autovetor de $T$ associado à $\lambda$. Agora, vamos esclarecer alguns pontos:
* Temos certeza de que ele não é nulo? Sim, pois $M$ é uma matriz invertível e $v \neq \bar{0}$, portanto $Mv \neq \bar{0}$.
* E quem é $M[v]_{\mathcal{B}}$ afinal? São as coordenadas de $v$ na base $\mathcal{A}$, isto é, $Mv = [v]_{\mathcal{A}}$.
Concluindo, se $v$ é um autovetor de $T$ associado ao autovalor $\lambda$, não importa qual a **base** e consequentemente qual **matriz** representante de $T$ tomemos: 
* a conta dos **autovalores** matriciais vai resultar nos mesmos autovalores, afinal o $\lambda$ não mudou em momento nenhum
* e os **autovetores** são correspondentes no sentido de que só é uma mudança de base de um pra outro: se escolhermos a base $\mathcal{B}$ para fazer a conta, vamos obter as coordenadas de $v$ na base $\mathcal{B}$; se escolhermos $\mathcal{A}$, vamos obtê-lo na base $\mathcal{A}$, mas vai ser o mesmo autovetor, apenas representado em diferente base.

> [!ps]-
> Quando a gente olha a álgebra linear usando as TL em vez de usar simplesmente matrizes, como alguns livros fazem, a gente perde essa noção de que está representando a mesma coisa, só está usando bases diferentes.

**Obs.** É equivalente dizer
* (teoria matricial) a matriz coluna $[v]_{\mathcal{B}}$ é autovetor da matriz $[T]_{\mathcal{B}}$ com autovalor $\lambda$ ou
* $v$ é autovetor do operador $T$ associado ao autovalor $\lambda$ onde $A$ e $B$ são matrizes de $T$ considerando diferentes bases de $\mathbb{V}$ (aqui, não ficamos falando a base escolhida).

> [!teorema]
> Se $B=M^{-1} A M$ e $v$ é um autovetor de $B$ associado a um autovalor $\lambda$, então $M v$ é um autovetor de $A$ associado a $\lambda$.

Em outras palavras: se $B$ e $A$ representam o mesmo operador linear, os autovalores e autovetores não dependerão da matriz em si. O que teremos são as coordenadas em cada caso.

$v$ é autovetor de $T$ associado ao autovalor $\lambda$ onde $A$ e $B$ são matrizes de $T$ considerando diferentes bases de $\mathbb{V}$. Estamos fazendo um abuso de notação entre o que é autovalor e autovetor da matriz e do operador (coordenadas x entradas)

> [!exemplo]-
> Ver exemplo 2 da minha nota de aula 20.


# Propriedades

> [!teorema]
> Seja $A$ uma matriz $n \times n$. São válidas as seguintes propriedades:
> 1. Se $A$ é triangular, então $a_{i i}$ serão autovalores.
> 2. Se $A$ é invertível com autovetor $v$ associado ao autovalor $\lambda$, então $v$ também é autovetor de $A^{-1}$ associado ao autovalor $\frac{1}{\lambda}$.
> 3. As matrizes $A$ e $A^{\top}$ possuem os mesmos autovalores.

Ver demonstrações na minha nota de aula 20.


# Multiplicidade algébrica e geométrica

> [!definicao]
> Seja $\lambda$ um autovalor do operador linear $T$. Chamamos de
> * a) **multiplicidade algébrica** de $\lambda$ a quantidade de vezes que ele aparece como raíz do polinômio característico de $T$.
> * b) **multiplicidade geométrica** de $\lambda$ a dimensão do autoespaço associado.

> [!teorema]
> Seja $T: \mathbb{V} \rightarrow \mathbb{V}$ um operador linear que admite ao menos um autovalor. A multiplicidade geométrica de um autovalor de $T$ é sempre menor que ou igual à sua multiplicidade algébrica deste mesmo autovalor.

Os graus de liberdade nos dão uma restrição para a multiplicidade geométrica. Os graus de liberdade são o tanto de equações LD que descartamos. i.e., o total de equações menos o número de LI. Por isso, não conseguimos esse total ser maior do que o número de vezes que apareceu a raiz do polinômio.

A dimensão do autoespaço está associada ao grau de liberdade da equação que estamos resolvendo. Ver relação com [[Núcleo e Imagem]].
$$
MA \geq \text{graus de liberdade} = \dim(\text{autoespaço}) = MG
$$
A MA dita o número máximo de direções independentes que a matriz poderia esticar ou comprimir naquele fator.

> [!teorema]
> Seja $\mathbb{W}$ um subespaço invariante pelo operador $T$ e $G$ a restrição de $T$ ao subespaço $\mathbb{W}$. Então o polinômio característico $p_T$ é um múltiplo do polinômio característico $p_G$.

Nós definimos uma transformação $G$ tal que
$$
\begin{gather}
G: \mathbb{S}_{\lambda_{0}} \rightarrow \mathbb{S}_{\lambda_{0}} \\
w \mapsto G(w)=T(w)=\lambda_{0}w \in \mathbb{S}_{\lambda_{0}}
\end{gather}
$$
Como $w$ está no autoespaço de $\lambda_{0}$, a $G$ age tal qual a $T$. Mas, como $\mathbb{S}_{\lambda_{0}}$ é espaço vetorial, um múltiplo escalar de $w$ também está dentro dele. Logo, $G$ está bem definida e é um operador linear. 

Por que criamos esse operador?

Agora, olhemos para a matriz de $G$. Dada uma base $\mathcal{B}$