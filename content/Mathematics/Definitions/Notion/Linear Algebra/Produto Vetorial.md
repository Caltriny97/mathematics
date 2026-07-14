Data Criada: 24/03/2026 às 17:30
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
> **O produto vetorial** entre dois vetores $u$ e $v$, denotado por $u \times v$, é o vetor tal que
> - Se $u=\overline{0}$ ou $v=\overline{0}$, então $u \times v=\overline{0}$.
> - Se $u \neq \overline{0}$ e $v \neq \overline{0}$, então $u \times v$ tem norma, direção e sentido caracterizados por:
> 	* i) $\|u \times v\|=\|u\|\|v\| \sin (\theta)$
> 	* ii) $u \times v \perp u$ e $u \times v \perp v$
> 	* iii) o sentido de $u \times v$ é dado pela regra de Fleming (regra da mão direita).

Assim como aconteceu na soma de vetores, vamos ter que começar definindo o resultado do produto vetorial **geometricamente**, especificando o **módulo** (i), **direção** (ii) e **sentido** (iii) desse resultado.

Só faz sentido falarmos em produto vetorial no $\mathbb{R^{3}}$, senão ele "cairia pra fora" do nosso plano (ele também é chamado de produto externo, porque ele sai de onde os outros dois estavam). Mais rigorosamente, na verdade, ele só está definido em $\mathbb{R^{3}}$, não em mais dimensões (até poderíamos generalizar, mas isso só não foi feito).


# Propriedades do Produto Vetorial

> [!proposicao] Proposição.
> Sejam $u, v$ e $w$ vetores e $\alpha$ escalar.
> * i) $u \times v=-v \times u$
> * ii) $(u \times v) \cdot u=0$ e $(u \times v) \cdot v=0$
> * iii) $\alpha(u \times v)=(\alpha u) \times v=u \times(\alpha v)$
> * iv) $u \times(v+w)=(u \times v)+(u \times w)$

> [!ps]- Ps.
> * Analisando o polegar da regra da mão direita, fica fácil de entender (i), afinal só o sentido muda (a direção e módulo são os mesmos se analisarmos a própria definição).
> * Em (i), temos, na verdade, que $u \times v= -(v\times u)=-v \times u$. Isso faz sentido se olharmos para a (iii).


# Produto Vetorial via Coordenadas

Não é trivial calcularmos o produto vetorial usando a **definição geométrica** (teríamos que calcular as normas, imaginar sua posição e sentido no espaço para saber o ângulo...). Por isso, vamos fugir disso e conseguir uma **definição algébrica**, assim como fizemos para o produto por escalar. Vamos, para tanto, usar as propriedades da sessão anterior.

> [!proposicao] Proposição.
> Sejam $e_1=(1,0,0), e_2=(0,1,0)$ e $e_3=(0,0,1)$. Se $u=\left(u_1, u_2, u_3\right)$ e $v=\left(v_1, v_2, v_3\right)$, então
> 
> $
> \begin{aligned}
> u \times v & =\operatorname{det}\left[\begin{array}{ll}
> u_2 & u_3 \\
> v_2 & v_3
> \end{array}\right] e_1-\operatorname{det}\left[\begin{array}{ll}
> u_1 & u_3 \\
> v_1 & v_3
> \end{array}\right] e_2+\operatorname{det}\left[\begin{array}{ll}
> u_1 & u_2 \\
> v_1 & v_2
> \end{array}\right] e_3 \\
> & =\operatorname{det}\left[\begin{array}{lll}
> e_1 & e_2 & e_3 \\
> u_1 & u_2 & u_3 \\
> v_1 & v_2 & v_3
> \end{array}\right]
> \end{aligned}
> $

> [!ps]- Ps.
> * $e_1, e_2$ e $e_3$ são chamados de **vetores canônicos** e, em Geometria Analítica, costumam ser denotados por $\vec{i}, \vec{j}$ e $\vec{k}$, respectivamente.
> * Essa matriz é uma tortura na matemática, é apenas uma representação, pois ela tem algumas entradas reais (as coordenadas dos vetores) e alguns vetores. Isso não está bem definido, mas, numericamente, dá certo...

> [!demonstracao]- Demonstração.
> Para demonstrar, vamos usar o seguinte raciocínio:
> $
> \begin{gather}
> u = (u_{1}, u_{2}, u_{3}) = u_{1}e_{1}+u_{2}e_{2}+u_{3}e_{3}\\
> v = (v_{1},v_{2},v_{3}) = v_{1}e_{1} + v_{2}e_{2}+v_{3}e_{3}\\
> u \times v = (u_{1}, u_{2}, u_{3})\times(v_{1},v_{2},v_{3}) = (\dots)
> \end{gather}
> $
> Repare que nós "transformamos" as coordenadas de $u$ e $v$ de volta para vetores no espaço.
> Abrindo a expressão e usando que $e_{1}\times e_{2}=e_{3}$ e raciocínios análogos, chegamos na proposição acima.
> 
> Desenvolvemos a conta utilizando as propriedades de produto vetorial listadas acima e usando resultados conhecidos de produto vetorial entre os vetores conônicos.


# Interpretação Geométrica

Mas afinal, pra que serve esse produto maluco? Bom, esse produto maluco está muito relacionado à área de um paralelogramo: na verdade, ele foi criado a partir do resultado que vamos ver logo abaixo.

---
Como calcular a área de uma figura maluco, como a abaixo? Basta a dividir em triângulos!![[Pasted image 20260324201736.jpg|center|400]]
Vamos ver logo logo que sabemos calcular a área do paralelogramo formado por $v$ e $u$. Depois, é só dividir por dois e sabemos a área do triângulo (e de quaisquer outros"). Repetindo o processo, conseguimos calcular a área dessa figura maluca.

---

Qual a área $A$ do paralelogramo formado pelos vetores u e v?
![[Pasted image 20260324174349.png | center]]

$$
A=\text { base } \cdot \text { altura }=\|u\| \cdot h
$$

$$
\begin{aligned}
&\begin{aligned}
& \text { Mas } \sin (\theta)=\frac{h}{\|v\|} \quad \Rightarrow \quad h=\|v\| \sin (\theta) \text {. } \\
& \text { Logo }
\end{aligned}\\
&A=\|u\|\|v\| \sin (\theta)=\|u \times v\| .
\end{aligned}
$$

É claro que quem definiu produto vetorial o definiu assim para que mapeasse esse resultado!

Seguindo essa mesma ideia, veremos como calcular o volume de um tetraedro... Ver [[Produto Misto]].


> [!obs] Utilidade.
> (i) O módulo do produto vetorial nos dá a área do paralelogramo.
> 
> (ii) O produto vetorial nos ajuda a identificar **paralelismo**. Se dois vetores forem paralelos, a área do paralelogramo formado por eles é zero.