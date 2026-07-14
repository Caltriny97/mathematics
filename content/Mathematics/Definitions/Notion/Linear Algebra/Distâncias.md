Data Criada: 04/04/2026 às 00:25
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Definimos distância como sendo a menor distância entre dois elementos. É possível provar, por pitágoras, que ela será igual o comprimento do segmento ortogonal que liga os dois elementos.

# Distância entre pontos

$$
\operatorname{dist}(P, Q)=\|\overrightarrow{P Q}\|
$$


# Distância entre ponto e reta

**GeoGebra:** https://www.geogebra.org/m/AhGjmmpu#material/bpnhkzqq

$$
\begin{aligned}
\text { Área Paralelogramo } & =\text { base ⋅ altura } \\
\Rightarrow\left\|\overrightarrow{P_r P} \times v\right\| & =\|v\| \operatorname{dist}(P, r) \\
\end{aligned}
$$
$$
\Rightarrow \operatorname{dist}(P, r)=\frac{\left\|\overrightarrow{P_r P} \times v\right\|}{\|v\|}
$$
onde $P_r$ é um ponto qualquer de $r$ (não importa qual ponto escolhemos, pois a altura do paralelogramo será sempre a mesma). Da mesma forma, podemos escolher qualquer vetor diretor $v$ da reta.

Sabemos calcular a área do paralelogramo de duas formas: $b \cdot h$ e a norma do produto vetorial (Lembre da interpretação geométrica de [[Produto Vetorial]]).


# Distância entre ponto e plano

Definimos a distância entre ponto e plano como sendo a **menor distância** entre $P$ e um ponto de $\pi$.

**GeoGebra:** https://www.geogebra.org/m/awqd6tab

$$
\begin{aligned}
&\begin{aligned}
\operatorname{dist}(P, \pi) & =\left\|\operatorname{proj}_{\vec{r}} \overrightarrow{P_\pi P}\right\| =\left\|\frac{\overrightarrow{P_\pi P} \cdot \vec{n}}{\|\vec{n}\|^2} \vec{n}\right\|
\end{aligned}\\
&\Rightarrow \operatorname{dist}(P, \pi)=\frac{\left|\overrightarrow{P_\pi P} \cdot \vec{n}\right|}{\|\vec{n}\|}\\
&\text { onde } P_\pi \text { é um ponto qualquer de } \pi \text {. }
\end{aligned}
$$

Ou seja, conseguimos calcular a distância de um ponto qualquer a $\pi$ achando a **norma** da projeção de $\overrightarrow{P_\pi P}$ na direção do vetor normal. Relembre [[Projeção Ortogonal]].


# Distância entre retas

A princípio, temos $4$ casos para analisar: 
* (i) Retas paralelas disjuntas: $\text{dist}(r,s)=\text{dist}(P_{r},s)$, t.q. $P_{r}$ é um ponto qualquer de $r$.
* (ii) Retas coincidentes: $\text{dist}(r,s)=0$
* (iii) Retas concorrentes: $\text{dist}(r,s)=0$
* (iv) Retas reversas

Aqui devemos tomar um pouco mais de cuidado, porque, antes de começar a calcular a distância, precisaremos descobrir em qual caso estamos: a princípio teríamos que analisar esses $4$ casos, mas vamos ver logo logo que eles se resumem a apenas $2$...

> [!container] Caso 1: Retas paralelas
> Acontece que, se $r / / s$ (casos i e ii), então $\text{dist}(r,s)=\text{dist}(P_{r},s)$. Tanto faz se elas são coincidentes ou não, pois, ainda que sejam, a área do paralelogramo formado vai ser zero (lembre distância de ponto e reta), corroborando o que já vimos.
> 
> ![[Pasted image 20260404151011.png|center|400]]
> 
> $
> \operatorname{dist}(r, s)=\operatorname{dist}\left(P_r, s\right)
> $
> onde $P_r$ é um ponto qualquer de $r$.

> [!container] Caso 2: Retas não paralelas
> No caso que as **retas não são paralelas**, podemos formar um paralelepípedo com dois vetores diretores quaisquer $v_{r}$ e $v_{s}$ começando respectivamente em dois pontos quaisquer $P_{r}$ e $P_{s}$ e o vetor $\overrightarrow{P_{r}P_{s}}$. 
> 
> De forma parecida com a distância entre ponto e reta, a $\text{dist}(r,s)$ vai ser justamente dada pela **altura do paralelepípedo**, já que altura é sempre ortogonal. Como a altura do paralelepípedo é sempre a mesma [^1] e nós também sabemos calcular o volume do paralelepípedo de duas formas: $A_{b} \cdot h$ e módulo do [[produto misto]], segue que
> 
> ![[Pasted image 20260404143445.png|center|400]]
> 
> $
> \begin{aligned}
> \operatorname{dist}(r, s) & =\text { altura paralelepípedo } \\
> & =\frac{\text { Volume }}{\text { área da base }}
> \end{aligned}
> $
> $
> \Rightarrow \operatorname{dist}(r, s)=\frac{\left|\left[\overrightarrow{v_r}, \overrightarrow{v_s}, \overrightarrow{P_r P_s}\right]\right|}{\left\|\overrightarrow{v_r} \times \overrightarrow{v_s}\right\|}
> $
> onde $P_r$ é um ponto qualquer de $r$ e $P_s$ ponto qualquer de $s$.
> 
> O outro caso de retas não paralelas que falta ser analisado é o das retas concorrentes. Acontece que, nesse caso, o volume do paralelepípedo formado pelos vetores é zero, pois estaríamos colapsando-o. Então acaba que em ambos os casos de retas não paralelas nós podemos calcular a distância da mesma forma.


Na prática, antes de calcular a distância, temos que verificar se as retas são paralelas ou não. Imagine que não façamos isso e calculemos a distância entre duas retas paralelas usando a área do paralelepípedo formado. Chegaríamos que a distância é zero, o que não é verdade.


# Distância entre reta e plano

**Caso 1.**
Aqui vamos fazer uma separação parecida: se a reta é paralela ao plano, a distância da reta ao plano é a distância de qualquer ponto da reta ao plano, então caímos no caso de distância entre ponto e plano, que já sabemos calcular.

**Caso 2.**
Se não são paralelos, a distância é zero.


Mas perceba que precisamos verificar se são paralelos ou não. **E como verificamos se uma reta é paralela ou não a um plano?** Nós vemos se o vetor diretor da reta é ortogonal ao vetor normal do plano.


# Distância entre planos

**Caso 1.**
Se temos dois planos paralelos, basta pegar um ponto do primeiro plano e calcular a distância até o segundo plano. Assim recaímos no caso da distância entre ponto e plano.

**Caso 2.**
No caso em que eles não são paralelos, a distância é zero.


**E como saber se dois planos são paralelos?** Vendo se os seus vetores normais são paralelos um ao outro.


# Footnotes

[^1]: afinal é igual a distância entre as retas ou, podemos pensar também que, dados os mesmos $3$ vetores, o produto misto será sempre o mesmo