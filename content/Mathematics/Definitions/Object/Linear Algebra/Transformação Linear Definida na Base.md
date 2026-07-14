Data Criada: 29/05/2026 às 23:43
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Dada uma base do domínio e um número correspondente de elementos no contradomínio, é possível definir uma transformação que faça essa transposição de forma única? Mais formalmente,

Sejam $\mathcal{B}=\left\{e_1, e_2, e_3\right\}, w_1=(1,1), w_2=(2,3)$ e $w_3=(0,1)$. Existe alguma transformação linear $T: \mathbb{R}^3 \rightarrow \mathbb{R}^2$ tal que

$$
T\left(e_1\right)=w_1 \quad T\left(e_2\right)=w_2 \text { e } T\left(e_3\right)=w_3 ?
$$


$$
\begin{aligned}
& u \in \mathbb{R}^3 \Rightarrow u=\alpha_1 e_1+\alpha_2 e_2+\alpha_3 e_3 \\
& \Rightarrow \quad T(u)=T\left(\alpha_1 e_1+\alpha_2 e_2+\alpha_3 e_3\right) \\
&=\alpha_1 T\left(e_1\right)+\alpha_2 T\left(e_2\right)+\alpha_3 T\left(e_3\right) \\
&=\alpha_1(1,1)+\alpha_2(2,3)+\alpha_3(0,1) \\
&=\left(\alpha_1+2 \alpha_2, \alpha_1+3 \alpha_2+\alpha_3\right)
\end{aligned}
$$


Ou seja: $T\left(\alpha_1, \alpha_2, \alpha_3\right)=\left(\alpha_1+2 \alpha_2, \alpha_1+3 \alpha_2+\alpha_3\right)$

> [!obs]
> Até agora, nós estávamos preocupados em saber se determinada função era ou não TL.
> 
> Agora, nós já temos uma TL definida por hipótese. A questão é se conseguimos achar uma regra geral pros demais elementos. É por isso que podemos aplicar as propriedades de TL no meio da conta.


> [!teorema]
> Sejam $\mathcal{B}=\left\{v_1, v_2, \ldots, v_n\right\}$ base de $\mathbb{V}$ e $w_1, w_2, \ldots, w_n$ vetores de $\mathbb{W}$. Então **existe** uma **única** transformação linear
> 
> $
> T: \mathbb{V} \rightarrow \mathbb{W}
> $
> 
> tal que $T\left(v_i\right)=w_i$ para $i=1,2, \ldots, n$.

Aqui, não importa se a dimensão de $\mathbb{W}$ é maior ou igual a $n$. Apenas precisamos tomar na imagem a mesma quantidade de elementos que está na base do domínio.

> [!demonstracao]-
> Devemos provar existência e unicidade. Ver slide 15 da aula 15.

> [!obs]
> O ponto principal aqui é: todos os elementos do domínio podem ser escritos como combinação linear dos elementos da base. 
> 
> Portanto, ao mapear uma transformação de cada elementos da base, é fácil extrapolar essa transformação para todos os demais elementos do domínio, criando uma regra geral.
> 
> Em outras palavras, a base dita a regra para todos os vetores. Não precisamos conhecer a transformação em outros vetores. Se nós sabemos como ela aje na base, já conhcemos ela inteira.
> 
> Geometricamente, se quisermos aplicar uma transformação numa figura, basta saber como ela se comporta nos elementos da base. Veja o exemplo abaixo.

> [!exemplo]- Imagem do Impa Tech.
> ![[Pasted image 20260524165125.png|center|600]]
> $
> \begin{aligned}
> & T(8,0)=(6,4) \\
> & T(0,6)=(-4,0)
> \end{aligned}
> $
> $
> \begin{aligned}
> (x, y)=\alpha(8,0)+\beta(0,6)=\frac{x}{8}(8,0) & +\frac{y}{6}(0,6) \\
> T(x, y)=T\left(\frac{x}{8}(8,0)+\frac{y}{6}(0,6)\right) & =\frac{x}{8} T((8,0))+\frac{y}{6} T((0,6))=\frac{x}{8}(6,4)+\frac{y}{6}(-4,0) \\
> T: \mathbb{R}^2 & \rightarrow \mathbb{R}^2 \\
> (x, y) & \mapsto\left(\frac{3 x}{4}-\frac{2 y}{3}, \frac{x}{2}\right)
> \end{aligned}
> $



