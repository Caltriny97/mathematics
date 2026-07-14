Data Criada: 03/04/2026 às 11:46
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

**Que informações precisamos para determinar um único plano?**
Quando conhecemos $3$ pontos pertencentes a um plano $\pi$ que não são colineares, nós conseguimos determinar esse plano. Conhecer $3$ pontos equivale a conhecer $1$ ponto e dois vetores paralelos $v$ e $w$ ao plano (mas não paralelos entre si, senão os $3$ pontos seriam colineares). $v$ e $w$ são os vetores diretores do plano $\pi$. Ver [[coplanaridade e colinearidade]] para mais detalhes.

A ideia agora é **sintetizar** a informação desses dois vetores num só: o produto vetorial $v\times w = n$. Perceba que agora conhecemos **um ponto** e **um vetor ortogonal** ao plano $\pi$ (a normal $n$). Só essas duas informações são suficientes para determinar o plano $\pi$.

**Resumindo...**
![[Pasted image 20260403155023.png|center|300]]
$$
\begin{gathered}
P_0, P_1 \mathbf{e} P_2 \in \pi \\
\text { ou } \\
P_0 \in \pi \text { e } \underbrace{v=\overrightarrow{P_0 P_1} \text { e } w=\overrightarrow{P_0 P_2}}_{\text {vetores diretores }} / / \pi \\
\quad P_0 \in r \text{ e }\underbrace{u=\overrightarrow{P_0 P_1} \times \overrightarrow{P_0 P_2}}_{\text {vetor normal }} \perp \pi
\end{gathered}
$$


De forma análoga ao que vimos em [[Retas]] com adição de ponto e vetor, para conhecer um ponto $P$ qualquer do plano $\pi$, tendo conhecido um ponto $P_{0}$ e dois vetores diretores $v$ e $w$, podemos fazer $P_{0}$ mais todas as possíveis combinações lineares de $v$ e $w$. Daí teremos $P= P_{0} + tv+sw$. Essa é a **equação vetorial do plano**. Se quisermos seguir o raciocínio completo da aula passada, sem usar essa "gambiarra" de somar ponto com vetor, basta desenvolver o seguinte resultado visto em [[coplanaridade e colinearidade]] em (iii) e (iv).
$$
P \in \pi \iff\overrightarrow{P_{0}P},\; v \;\text{ e }\; w \;\text{ são coplanares} \iff \overrightarrow{P_{0}P} = tv+sw
$$


**As nossas equações do plano são:**

$$
\textbf{Eq. Vetorial do Plano}
$$
$$
P=P_0+t v+s w, \quad t, s \in \mathbb{R}
$$


$$
\textbf{Eqs. Paramétricas do Plano}
$$
$$
\begin{aligned}
& x=x_0+t v_1+s w_1 \\
& y=y_0+t v_2+s w_2 \quad t, s \in \mathbb{R} \\
& z=z_0+t v_3+s w_3
\end{aligned}
$$
> [!obs]- Obs (sistema linear).
> Equivalente à eq. vetorial. É um sistema linear de $3$ equações e $5$ incógnitas, assumindo $x_{0}, y_{0}, z_{0},v_{1}, v_{2}, v_{3}, w_{1}, w_{2}, w_{3}$ conhecidos.


$$
\textbf{Eq. Geral do Plano}
$$
$$
\begin{gather}
& \quad a x+b y+c z+d=0\\
& \text{tal que }\; d=-ax_{0}-by_{0}-cz_{0} \;\; \text{e } \; n=(a, b, c) \perp \pi \text{ e } n / / u \times v
\end{gather}
$$

> [!obs]- Obs (demonstração).
> Essa equação vem do seguinte raciocínio:
> $
> P \in \pi \iff \overrightarrow{P_{0}P} \perp n \iff \overrightarrow{P_{0}P} \cdot n = 0 
> $
> Desenvolvendo o [[Produto Escalar]], chegamos na equação geral do plano. Lembrando que, como $n=(a, b, c)$ e $P_{0} = (x_{0}, y_{0}, z_{0})$ são conhecido, temos que $d= -ax_{0}-by_{0}-cz_{0}$ é uma constante.


> [!problema]- Problema 1.
> Encontre a equação vetorial da reta $r=\pi_1 \cap \pi_2$, onde $\pi_1: 2 x+y+4 z-4=0$ e $\pi_2: 2 x-y+2 z=0$.
> 
> Podemos pensar esse problema de duas formas: geométrica e analiticamente. 
> 
> A forma geométrica seria entender que o vetor diretor da reta é ortogonal aos dois vetores normais do plano. Depois disso, bastaria encontrar um ponto que esteja na intersecção dos planos (basta fixar uma variável, como $z=0$ e resolver o sistema para $x$ e $y$). Com um ponto e um vetor diretor, a reta pode ser determinada.
> 
> Outra forma mais analítica seria reduzir, escalonar (ver [[sistemas lineares]]) as duas eq. dos planos até termos $x$ e $y$ em função de $z$, por exemplo. Depois, tomamos $z = t$ onde $t$ é o nosso parâmetro. Daí teríamos as $3$ equações paramétricas da reta.


# Subespaços vetoriais

> [!proposicao] Proposição.
> Considere as operações usuais de $\mathbb{R}^3$.
> * (i) Uma reta que passa pela origem determina um espaço vetorial.
> * (ii) Um plano que passa pela origem determina um espaço vetorial.

* [[Subespaços Vetoriais em GA]]


# Ângulo entre retas e planos

* [[Ângulo entre retas e planos]]