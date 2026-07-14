Data Criada: 24/03/2026 às 17:48
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Vamos seguir a mesma ideia de calcular a área de triângulos pelo [[Produto Vetorial#Interpretação Geométrica|Produto Vetorial]]... Vimos lá que sabendo a área do paralelogramo, conseguimos a área de triângulo e, com triângulo, conseguimos a área de qualquer polígono. Qual seria o análogo para volume?

Bom, se pegamos poliedros malucos, conseguimos dividi-los em vários tetraedros. No caso do paralelepípedo (figura abaixo), conseguimos dividi-lo em 6 tetraedros...de volumes iguais ainda!

Ou seja, para calcularmos o volume de um desses tetraedros, basta calcularmos o volume do paralelepípedo formado pelos 3 vetores $u,v,w$ abaixo e dividir por 6. Depois, é só repetir o processo para calcular a área de qualquer poliedro!


# Volume de um paralelepípedo

![[Pasted image 20260324174900.png|center]]

$$
V=\underbrace{\text { Àrea da base }}_{\|v \times w\|} \cdot \underbrace{\text { altura }}_h
$$


Mas $|\cos (\theta)|=\frac{h}{\|u\|} \Rightarrow h=\|u\| \cdot|\cos (\theta)|$

$$
\begin{aligned}
V & =\|v \times w\|\|u\| \cdot|\cos (\theta)| \\
& =|\|v \times w\|\|u\| \cdot \cos (\theta)|
\end{aligned}
$$


Como $\theta=\operatorname{ang}(u, v \times w)$, segue

$$
V=|u \cdot(v \times w)|
$$

Novamente, o produto misto nasceu com o propósito de mapear esse resultado.

> [!note]- Comentário.
> Usamos módulo de $\cos (\theta)$ porque o ângulo entre $u$ e $v\times w$ pode ser maior que $\pi$ (por causa da regra da mão direita, caso fizéssemos $w\times v$ por ex). Então, para forçarmos que os ângulos entre $u$ e $h$ e entre $u$ e $u\times v$ resultem no mesmo $\cos \theta$ (para conseguirmos botar o módulo "em evidência"), precisamos usar $|\cos (\theta)|$. Isso estará relacionado com o fato de trocar o sinal do determinante caso invertamos a ordem dos vetores dentro da matriz.


# Produto Misto

> [!definicao] Definição.
> O **produto misto** entre os vetores $u, v$ e $w$, denotado por $[u, v, w]$ (ou $(u, v, w)$ ), é o escalar dado por
> 
> $
> [u, v, w]=u \cdot(v \times w) .
> $

> [!proposicao] Proposição.
> Sejam $u=\left(u_1, u_2, u_3\right), v=\left(v_1, v_2, v_3\right)$ e $w=\left(w_1, w_2, w_3\right)$. Então
> 
> $
> [u, v, w]=\operatorname{det}\left[\begin{array}{lll}
> u_1 & u_2 & u_3 \\
> v_1 & v_2 & v_3 \\
> w_1 & w_2 & w_3
> \end{array}\right]
> $
> 

> [!comentario]- Comentário.
> De forma parecida ao que ocorria no produto vetorial, se trocarmos de ordem os vetores no do produto misto, o seu resultado vai ser multiplicado por $-1$. Percebemos isso facilmente se olhar para a matriz: ao trocar um par de linhas ou colunas de lugar, o determinante troca de sinal.


# Propriedades do Produto Misto

> [!proposicao] Proposição.
> Sejam $u, v, w$ e $z$ vetores e $\alpha$ escalar.
> * i)
> 
> $
> \begin{aligned}
> & {[u+z, v, w]=[u, v, w]+[z, v, w]} \\
> & {[u, v+z, w]=[u, v, w]+[u, z, w]} \\
> & {[u, v, w+z]=[u, v, w]+[u, v, z]}
> \end{aligned}
> $
> 
> * ii) $[u, v, w]=-[u, w, v]=-[w, v, u]=-[v, u, w]$
> * iii) $[u, v, w]=(u \times v) \cdot w$
> * iv) $\alpha[u, v, w]=[\alpha u, v, w]=[u, \alpha v, w]=[u, v, \alpha w]$
> 

> [!comentario]- Comentário.
> Essas propriedades são válidas somente para a definição de produto misto: $u \cdot (v \times w)$. Se formos rigorosos, não poderíamos aplicá-las a $(v \times w) \cdot u$, mesmo o produto escalar sendo comutativo. Na demonstração de (iii), que está nas minhas anotações da Aula 3, tivemos que tomar esta precaução: usar (ii) na definição de produto misto e, somente depois, aplicar a comutatividade do produto escalar. 


> [!obs] Utilidade.
> (i) O valor real retornado pelo produto misto é igual à área do paralelogramo formado pelos 03 vetores.
> 
> (ii) O produto misto nos ajuda a ver [[coplanaridade e colinearidade|coplanaridade]]. Se três vetores são coplanares, o volume do paralelepípedo formado por eles é zero.
