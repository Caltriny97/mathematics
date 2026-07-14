Data Criada: 30/05/2026 às 12:41
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
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma Transformação Linear.
> * i) $T$ é **Injetiva** se para todo $u, v \in V$ com $u \neq v$, temos $T(u) \neq T(v)$.
> * ii) $T$ é **Sobrejetiva** se $\operatorname{Im}(T)=\mathbb{W}$.
> * iii) $T$ é um **Isomorfismo** de $\mathbb{V}$ em $\mathbb{W}$ se $T$ é bijetiva (injetora e sobrejetora). Nesse caso, os espaços vetoriais $\mathbb{V}$ e $\mathbb{W}$ são ditos **Isomorfos**.

> [!teorema]
> Seja $T: \mathbb{V} \rightarrow \mathbb{W}$ uma Transformação Linear e $\left\{v_1, \ldots, v_n\right\}$ base de $\mathbb{V}$.
> 1. $N(T)=\{\overline{0}\}$ se, e somente se, $T$ é injetora.
> 2. Seja $\operatorname{dim} \mathbb{V}=\operatorname{dim} \mathbb{W}$. Então $T$ é injetora se, e somente se, é sobrejetora.
> 3. Se $T$ é injetora e $\operatorname{dim}(\mathbb{V})=\operatorname{dim}(\mathbb{W})$, então $\left\{T\left(v_1\right), \ldots, T\left(v_n\right)\right\}$ é base de $\mathbb{W}$.
> 4. Se $T$ é um isomorfismo (invertível), então sua inversa também é uma transformação linear.

**Obs.** O maior fruto aqui é poder juntar (1) e (2): se $\operatorname{dim} \mathbb{V}=\operatorname{dim} \mathbb{W}$ e $N(T)=\{\overline{0}\}$, então $T$ é um isomorfismo. 

O conceito de isomorfismo está diretamente relacionado à inversa da matriz $A$.


> [!teorema]
> Dois espaços vetoriais $\mathbb{V}$ e $\mathbb{W}$ com mesma dimensão são Isomorfos.

Note que dois EV com dimensões diferentes **nunca** podem ser isomorfos (isso vem da definição de isomorfismo, do fato de que $\operatorname{dim}(\mathbb{V})=\operatorname{dim} N(T)+\operatorname{dim} \operatorname{Im}(T)$ e do resultado 1 acima).