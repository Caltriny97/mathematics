Data Criada: 03/04/2026 às 21:38
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
> O **ângulo** entre os vetores não-nulos $u=\overrightarrow{A B}$ e $v=\overrightarrow{A C}$ será o ângulo $\text{ang}(u, v) \in[0, \pi]$ entre os segmentos $\overrightarrow{A B}$ e $\overrightarrow{A C}$.


> [!definicao] Definição.
> O **produto escalar** entre dois vetores $u$ e $v$, denotado por $u \cdot v$, é o escalar tal que:
> - Se $u=\overline{0}$ ou $v=\overline{0}$, então $u \cdot v=0$.
> - Se $u \neq \overline{0}$ e $v \neq \overline{0}$, então $u \cdot v=\|u\|\|v\| \cos (\theta)$, onde $\theta=\operatorname{ang}(u, v)$.


**Produto Escalar via Coordenadas.** (transição da interpretação geométrica para interpretação analítica)
Lei dos Cossenos: $a^2=b^2+c^2-2 b c \cos (\hat{A})$ :
$$
\begin{aligned}
&\|u-v\|^2=\|u\|^2+\|v\|^2-2 \underbrace{\|u\|\|v\| \cos (\theta)}_{u \cdot v} \\
& \Rightarrow u \cdot v= \frac{1}{2}\left[\|u\|^2+\|v\|^2-\|u-v\|^2\right] \\
&= \frac{1}{2}\left[\left(u_1^2+u_2^2\right)+\left(v_1^2+v_2^2\right)\right. \\
&\left.-\left(\left(u_1-v_1\right)^2+\left(u_2-v_2\right)^2\right)\right] \\
&= \ldots \\
& u \cdot v= u_1 v_1+u_2 v_2
\end{aligned}
$$
Análogo para vetores no espaço: $u \cdot v=u_1 v_1+u_2 v_2+u_3 v_3$.


**Calculando ângulo entre vetores**
$$
\begin{aligned}
& \text{Como }\;u \cdot v=\|u\|\|v\| \cos (\theta) \quad \text { e } \quad u \cdot v=u_1 v_1+u_2 v_2+u_3 v_3 \\
& \Rightarrow \quad \operatorname{ang}(u, v)=\theta=\arccos \left(\frac{u \cdot v}{\|u\|\|v\|}\right) ; \quad \theta \in[0, \pi]
\end{aligned}
$$

Como estamos falamos de um ângulo no intervalo $[0,\pi]$, nós conseguimos uma **bijeção** (logo podemos aplicar o inverso do $\cos)$, então conhecendo o cosseno, nós conhecemos o ângulo (acho que o caso de ângulo entre retas e planos não é uma bijeção exatamente, se não usarmos o módulo).

> [!comentario]- Comentário.
> O fato de termos duas interpretações (geométrica e analítica via coordenadas) para o produto escalar nos permite calcular o ângulo entre vetores. Basta substituir $u \cdot v=u_1 v_1+u_2 v_2+u_3 v_3$ em $\theta=\arccos \left(\frac{u \cdot v}{\|u\|\|v\|}\right)$.


> [!definicao] Definição.
> Sejam $u, v$ e $w$ vetores e $\alpha$ escalar.
> * i) $u \cdot v=v \cdot u$
> * ii) $u \cdot(v+w)=u \cdot v+u \cdot w$
> * iii) $\alpha(u \cdot v)=(\alpha u) \cdot v=u \cdot(\alpha v)$
> * iv) $\|u\|^2=u \cdot u \geq 0$, e $u \cdot u=0 \Leftrightarrow u=0$
> * v) (Desigualdade de Schwarz) $|u \cdot v| \leqslant\|u\|\|v\|$.
> * vi) (Desigualdade Triangular) $\|u+v\| \leqslant\|u\|+\|v\|$.

> [!obs]- Obs.
> Os 4 primeiros itens garantem que o produto escalar é um Produto Interno no Espaço Vetorial $\mathbb{R}^2$ (ou $\mathbb{R}^3$ ). O conceito de produto interno será explorado com mais detalhes em aulas futuras.
> 
> Não podemos fazer associatividades entre escalares! Para os vetores $u,v$ e $w$, temos que $(u \cdot v)w = w(u\cdot v)$, afinal o termo $(u\cdot v)$ seria o $\alpha$ acima. Porém, $(u\cdot v)w \neq u(v\cdot w)$. Ver problema 20 da lista 2.


> [!obs] Utilidade.
> O produto escalar nos ajuda a identificar **ortogonalidade**. Se os vetores $u$ e $v$ forem ortogonais, o produto escalar entre eles é zero. Ver [[Projeção Ortogonal]].

