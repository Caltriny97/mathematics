Data Criada: 05/04/2026 às 00:02
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

![[Pasted image 20260405003920.jpg|center|400]]
$$
S_{inf} \leq \int_{0}^{b}f(x)dx \leq S_{sup}
$$
$$
\begin{gather}
& \underline{I}(f) = \text{sup}\{S_{inf}\} \\
& \overline{I}(f) = \text{inf}\{{S_{sup}\}}
\end{gather}
$$
$$
\underline{I}(f) = \overline{I}(f) \text{ se $f$ for integrável}
$$

# Área sob $f(x) = x$

![[Pasted image 20260405003942.jpg|center|400]]
$$
\begin{gather}
S_{inf} = (\dots) = \frac{b^{2}}{2} - \frac{b}{2n} \qquad (1)\\ \\

S_{sup} = (\dots) = \frac{b^{2}}{2} + \frac{b}{2n} \qquad (2)
\end{gather}
$$
Temos também que, por definição de supremo e ínfimo:
$$
S_{inf} \leq \underline{I}(f) \leq \overline{I}(f) \leq S_{sup} \qquad (3)
$$

Pelo que vimos em [[Área]], sabemos que:
$$
0 \leq \overline{I}(f) - \underline{I}(f) \leq \frac{c}{n} \quad\forall \; n \implies   \underline{I}(f) = \overline{I}(f)
$$

Vamos então mostrar que o lado esquerdo desse resultado é verdade no caso de $f(x) = x$.

De $(3)$, temos que:
$$
\begin{gather}
-S_{sup} \leq - \underline{I}(f) \leq - S_{inf}  \\
S_{inf} \leq \overline{I}(f) \leq S_{sup} \\
 \\
S_{inf}-S_{sup} \leq \overline{I}(f)- \underline{I}(f) \leq S_{sup}- S_{inf} \qquad (4)
\end{gather}
$$

De $(1)$, $(2)$ e $(4)$ segue:
$$
-\frac{b}{n} \leq \overline{I}(f)- \underline{I}(f) \leq \frac{b}{n}
$$

Pelo que, do nosso resultado, segue que:
$$
\underline{I}(f) = \overline{I}(f) = \int_{0}^{b}f(x)dx \qquad (5)
$$

Unindo $(1), (2), (3)$ e $(5)$, temos que:
$$
\begin{gather}
\frac{b^{2}}{2} - \frac{b}{2n} \leq \int_{0}^{b}f(x)dx \leq \frac{b^{2}}{2} + \frac{b}{2n} \\ \\

- \frac{b}{2n} \leq \int_{0}^{b}f(x)dx - \frac{b^{2}}{2} \leq \frac{b}{2n} \\ \\
  
\left| \int_{0}^{b}f(x)dx - \frac{b^{2}}{2} \right| \leq \frac{b}{2n}
\end{gather}
$$

E, novamente pelo resultado que vimos em áreas, segue que
$$
\int_{0}^{b}f(x)dx = \frac{b^{2}}{2}
$$


# Generalizando

Ver na aula 3.1 o meu desenvolvimento. Partindo do de que (i) a integral de uma soma é igual a soma das integrais (fazemos isso para dividir a integral de um polinômio na integral dos vários monômios), de que (ii) a função que estamos analisando é sempre crescente (pelo menos no intervalo que estamos analisando) e (iii) a função é definida (integrais indefinidas são sempre mais complexas...), podemos seguir o mesmo raciocínio para o caso simples de $f(x)$ acima:

* primeiro mostramos que $0 \leq \overline{I}(f) - \underline{I}(f) \leq \frac{c}{n}$
* depois conseguimos esse valor colapsado usando um dos dois resultados abaixo, que provamos nas listas 1 e 2:
$$
\sum_{\ell=1}^n \ell^i=\frac{n^{i+1}}{i+1}+p_i(n)
$$
$$
\sum_{i=1}^{n-1} i^{\ell} \leq \frac{n^{\ell+1}}{\ell+1} \leq \sum_{i=1}^n i^{\ell}
$$