Data Criada: 24/05/2026 às 12:27
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

> [!definicao]
> Sejam $\mathbb{V}$ e $\mathbb{W}$ espaços vetoriais. Uma **Transformação Linear** de $\mathbb{V}$ e $\mathbb{W}$ é uma função $T: \mathbb{V} \rightarrow \mathbb{W}$ que satisfaz as seguintes condições:
> * i) $T(\alpha v)=\alpha T(v)$, para todo $\alpha \in \mathbb{R}$ e $v \in \mathbb{V}$,
> * ii) $T(v+w)=T(v)+T(w)$, para todo $v, w \in \mathbb{V}$.
> 
> Em particular, uma transformação linear de $\mathbb{V}$ em $\mathbb{V}$ é chamada de operador linear sobre V.

É interessante perceber que a imagem não necessariamente vai cobrir todo o contradomínio.

> [!obs]-
> Quando falamos de $\mathbb{V}$ e $\mathbb{W}$ como EV, nos referimos às triplas $( \mathbb{V},\oplus, \odot)$ e $( \mathbb{W},\boxplus, \boxdot)$. Daí, quando fazemos as operações (i) e (ii) da definição acima, estamos fazendo uma **troca de operações**:
> * No lado esquerdo, estamos realizando operações entre elementos do **domínio** $\mathbb{V}$, ou seja, as operações aqui são $\oplus \text{ e } \odot$.
> * Já no lado direito, as operações são entre elementos do **contradomínio**, logo as operações são $\boxplus \text{ e }\boxdot$.

> [!obs]-
> Podemos sintetizar essas duas propriedades numa única:
> $
> T(\alpha \odot v \oplus w) = \alpha \boxdot T(v) \boxplus T(w)
> $
> Se tomarmos $w=\bar{0}_{\mathbb{V}}$ e $\alpha=1$, temos ambas as propriedades acima, afinal as prorpiedades $3$ e $8$ respectivamente são válidas, pois $\mathbb{V}$ e $\mathbb{W}$ são EV.
> 
> Note que, podemos tomar $w=\bar{0}_{\mathbb{V}}$ porque o nulo mora do domínio, afinal $\mathbb{V}$ é EV. E o mais interessante é que teremos
> $T(\bar{0}_{\mathbb{V}})=\bar{0}_{\mathbb{W}}$
> É possível verificar isso fazendo:
> $
> \bar{0}_{\mathbb{W}} = T(v) \boxplus (-T(v)) = T(v)\boxplus T(\bar{0}_{\mathbb{V}})\boxplus (-T(v)) = T(\bar{0}_{\mathbb{V}})
> $

> [!exemplo]- TL com troca de operações.
> $
> \begin{gather}
> T:\mathbb{R}^{3} \rightarrow \mathbb{P}_{4} \\
> (x,y,z) \mapsto T(x,y,z)=p(t)=xt+yt^{4}
> \end{gather}
> $
> 
> $
> \begin{aligned}
> T(\alpha(x,y,z) + (\tilde{x},\tilde{y},\tilde{z})) = T((\alpha x+\tilde{x}, \alpha y+\tilde{y}, \alpha z+\tilde{z})) = \\
> = (\alpha x+\tilde{x})t + (\alpha y+\tilde{y})t^{4} = \alpha \underbrace{(xt+yt^{4})}_{T((x,y,z))} + \underbrace{(\tilde{x}t+\tilde{y}t^{4})}_{T((\tilde{x},\tilde{y}, \tilde{z}))}
> \end{aligned}
> $

Ás vezes, é mais simples mostrar que
$$
T(\alpha u+w)-[\alpha T(u)+T(w)]=\bar{0}_{\mathbb{C}}
$$
do que provar a igualdade. Lembre que o inverso aditivo está bem definido, uma vez que o contradomínio é EV.

> [!exemplo]- Não é uma TL.
> Ex. Fixados a e $b$ reais não nulos.
> 
> $
> \begin{aligned}
> T: \mathbb{R}^2 & \rightarrow & \mathbb{R}^2 & \\
> (x, y) & \mapsto & (x+a, y+b) & \\
> & & & T(0,0)=(a, b) \neq \overline{0}
> \end{aligned}
> $
> 
> 
> Portanto $T$ **não** é uma transformação linear. Levar ao nulo do contradomínio é uma condição necessária, mas não suficiente para ser TL.

> [!exemplo]- Combinação Linear de Transformações Lineares.
> Sejam $T_1, T_2, \ldots, T_k$ transformações lineares de $\mathbb{V}$ em $\mathbb{W}$, e $\lambda_i$ escalares. A função abaixo define uma transformação linear?
> $
> \begin{aligned}
> S: \mathbb{V} & \rightarrow \mathbb{W} \\
> v & \mapsto S(v)=\sum_{i=1}^k \lambda_i T_i(v)
> \end{aligned}
> $
> Sim!
> $
> \begin{aligned}
> S(\alpha v+\tilde{v}) & =\sum_{i=1}^k \lambda_i T_i(\alpha v+\tilde{v})=\sum_{i=1}^k \lambda_i\left(\alpha T_i(v)+T_i(\tilde{v})\right) \\
> & =\alpha \sum_{i=1}^k \lambda_i T_i(v)+\sum_{i=1}^k \lambda_i T_i(\tilde{v})=\alpha S(v)+S(\tilde{v})
> \end{aligned}
> $
> ad-teorema
A combinação linear de Transformações Lineares também será uma Transformação Linear.
```

> [!exemplo]- Composição de Transformações Lineares.
> Sejam $S: \mathbb{V} \rightarrow \mathbb{W}$ e $L: \mathbb{W} \rightarrow \mathbb{U}$ transformações lineares. A função abaixo define uma transformação linear?
> $
> \begin{aligned}
> T: \mathbb{V} & \rightarrow \mathbb{U} \\
> v & \mapsto T(v)=(L \circ S)(v)=L(S(v))
> \end{aligned}
> $
> Sim!
> $
> \begin{aligned}
> & T(\alpha v+\tilde{v})=L(S(\alpha v+\tilde{v}))=L(\alpha S(v)+S(\tilde{v}))=\alpha L(S(V))+L(S(\tilde{v}))= \\
> & \alpha T(v)+T(\tilde{v})
> \end{aligned}
> $
> ad-teorema
A composição de Transformações Lineares também será uma Transformação Linear.
```


# Propriedades

> [!teorema]
> Sejam $\mathbb{V}$ e $\mathbb{W}$ espaços vetoriais e $T: \mathbb{V} \rightarrow \mathbb{W}$ uma transformação linear. Então
> 1. $T\left(\overline{0}_{\mathbb{V}}\right)=\overline{0}_{\mathbb{W}}$
> 2. $T(-v)=-T(v)$ para todo $v \in \mathbb{V}$
> 3. $T\left(\alpha_1 v_1+\ldots+\alpha_n v_n\right)=\alpha_1 T\left(v_1\right)+\ldots+\alpha_n T\left(v_n\right)$ para todo $\alpha_i \in \mathbb{R}$ e $v_i \in \mathbb{V}$


# Matrizes e Bases & Coordenadas

* [[Matriz de uma Transformação Linear]]
	* [[Transformações Lineares - conexões]]
* [[Transformação Linear Definida na Base]]


# Conceitos

* [[Núcleo e Imagem]]
* [[Injetividade e Sobrejetividade]]

Daqui, o conceito de isomorfismo surge como uma poderosa ferramenta de transposição entre EV de dimensões iguais. Através dele, podemos intercambiar todos os elementos de um EV de dimensão $n$ para o $\mathbb{R}^{n}$. Assim, verificamos dependência linear, se é ou não base... tudo isso no $\mathbb{R}^{n}$!

Por exemplo, se estivermos lidando com o espaço $\mathbb{P}_{5}$, nós conseguimos construir um isomorfismo com o $\mathbb{R}^{6}$. Isso quer dizer que tudo que nós precisamos lidar no espaço de polinômios, nós podemos lidar via isomorfismo no $\mathbb{R}^{6}$. Por exemplo, dado um conjunto de polinômios e queremos testar se são LI. Podemos via isomorfismo olhar para os vetores em $\mathbb{R}^{6}$ e verificar se estes são LI. O resultado poderá ser extrapolado de volta ao $\mathbb{P}_{5}$.

Por isso, os espaços $\mathbb{R}^{n}$ são os mais importantes pra gente estudar toda a teoria de álgebra linear, porque todos os outros espaços de dimensão finita pode ser reduzido para o $\mathbb{R}^{n}$ através de um isomorfismo.

