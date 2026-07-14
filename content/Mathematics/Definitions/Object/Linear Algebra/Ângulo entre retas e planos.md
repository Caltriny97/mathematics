Data Criada: 04/04/2026 às 00:51
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Para calcular ângulo entre **retas** e **planos**, podemos associar ao ângulo entre os **vetores diretores**. Isso é interessante, pois temos uma forma analítica de calcular ângulos entre vetores por [[Produto Escalar]].

# Reta e reta

Vamos começar essa transição de geometria espacial para analítica analisando o ângulo entre reta e reta.

O problema é que o ângulo **retas** está sempre no intervalo $\left[0, \frac{\pi}{2} \right]$, uma vez que **retas não possuem sentido**. Já o ângulo entre vetores está sempre no intervalo $[0,\pi]$, já que **eles têm sentido**. Como podemos resolver esse problema?

**GeoGebra:** https://geogebra.org/m/edqsauj7
Vemos nessa modelo que, se pegássemos $v_{r}$ e $v_{s}$ como vetores diretores, o ângulo $\alpha$ entre eles coincidiria com o ângulo entre as retas (se elas se encontrassem). Porém, nós poderíamos ter o azar de pegar $v_{r}$ e $-v_{s}$ como vetores diretores. Nesse caso, o ângulo $\beta$ entre os vetores não seria o mesmo ângulo entre as retas.

Acontece que, como $\beta$ e $\alpha$ são suplementares, vale a relação $\cos(\alpha) = -\cos(\beta)$ ou $\cos(\alpha) = |\cos(\beta)|$, onde $\alpha$ é o ângulo entre as retas $r$ e $s$, logo é sempre positivo. Agora sim podemos usar nossa equação do produto escalar para determinar ângulo entre retas, apenas tomando o cuidado de usar o módulo do cosseno do ângulo entre os vetores diretores.


> [!definicao] Definição.
> Sejam $r$ e $s$ retas com vetores diretores $v_r$ e $v_s$, respectivamente. O ângulo $\theta_{r s}$ entre as **retas** $r$ e $s$ será o menor entre os ângulos de $v_r$ e $v_s$ e de $v_r$ e $-v_s$.

$$
\begin{aligned}
& \bullet \;\text{Ângulo entre vetores: } \theta \in[0, \pi] \\
& \bullet \; \text{Ângulo entre retas: } \theta \in[0, \pi / 2] \\
& \bullet \; \cos \left(\theta_{r s}\right)=\left|\cos \left(\theta_{v_r v_s}\right)\right|=\frac{\left|v_r \cdot v_s\right|}{\left\|v_r\right\|\left\|v_s\right\|}
\end{aligned}
$$


# Plano e plano

O raciocínio para o ângulo entre **planos** é análogo ao ângulo entre retas. O ângulo entre os planos pode ser associado ao ângulo entre os vetores normais de cada plano. Mas, temos o mesmo problema: podemos ter o azar de pegar vetores normais, cujo ângulo seja o suplementar ao ângulo entre os planos. Mas resolvemos isso fazendo o módulo do cosseno do ângulo entre os vetores normais. Assim garantimos que o cosseno será sempre igual ao cosseno do ângulo entre os planos.

> [!definicao] Definição.
> Sejam $\pi_1$ e $\pi_2$ planos com vetores normais $n_1$ e $n_2$, respectivamente. O ângulo $\theta_{\pi_1 \pi_2}$ entre os **planos** $\pi_1 \mathbf{e} \pi_2$ será o menor entre os ângulos de $n_1$ e $n_2$ e de $n_1$ e $-n_2$.

$$
\begin{aligned}
& \bullet \;\text{Ângulo entre planos: } \theta \in[0, \pi / 2] \\
& \bullet \; \cos \left(\theta_{\pi_1 \pi_2}\right)=\frac{\left|n_1 \cdot n_2\right|}{\left\|n_1\right\|\left\|n_2\right\|}
\end{aligned}
$$

![[Pasted image 20260403201839.png|center|200]]


# Reta e plano

O problema maior é para calcular o ângulo entre **reta** e **plano**. Aqui é um pouco mais sutil porque vamos ter o vetor diretor da reta e o vetor normal do plano. E não podemos dizer que o ângulo entre eles vai ser o mesmo ângulo entre a reta e o plano. É uma confusão, pois pode ser que peguemos a normal $n$ ou $-n$. Também pode ser que peguemos o vetor diretor $v$ ou $-v$. E, mesmo depois, ainda não vamos ter o ângulo exatamente entre a reta e o plano, mas sim o seu complementar.

Para resolver isso, vamos **tomar a reta $s$ cuja direção é a mesma da normal do plano**. Assim garantimos pegar o menor ângulo. O cosseno do ângulo $\theta_{rs}$ pode ser determinado pelo que já vimos, usando o vetor normal $n$ conhecido como seu vetor diretor. Acontece que esse ângulo $\theta_{rs}$ é  igual a $\frac{\pi}{2} - \theta_{r\pi}$. Portanto, o cosseno disso é igual ao seno do ângulo $\theta_{r\pi}$ que queremos calcular. Perceba que a reta $s$ foi apenas um elo temporário que usamos para aproveitar o resultado que obtivemos na sessão anterior.


> [!definicao] Definição.
> O ângulo $\theta_{r \pi}$ entre uma **reta** $r$ e um **plano** $\pi$ será $\theta_{r \pi}:=\pi / 2-\theta_{rs}$, onde $\theta_{rs}$ é o ângulo entre a reta $r$ e uma reta $s$ qualquer perpendicular ao plano $\pi$.

$$
\begin{aligned}
& \bullet \;\text{Ângulo entre reta e planos: } \theta \in[0, \pi / 2] \\
& \bullet \; \frac{|\vec{n} \cdot \vec{v}|}{\|\vec{n}\|\|\vec{v}\|}=\cos \left(\theta_{r s}\right)= \cos \left(\pi / 2-\theta_{r \pi}\right)=\sin \left(\theta_{r \pi}\right)
\end{aligned}
$$

![[Pasted image 20260403201744.png|center|200]]

