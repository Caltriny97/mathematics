
Aqui, nós vamos abaixar um pouco o nível da nossa abstração: já sabemos que os [[Vetores]], no sentido geral do conceito, é qualquer objeto que pertence a um espaço vetorial, mas vamos pegar o caso estrito de vetores no campo da Geometria Analítica.

Vamos começar definindo adição e multiplicação por escalar de tal modo que respeitem os 08 axiomas, mas vamos fingir que nós chegaremos neles por acaso... Depois, vamos mostrar, por consequência direta, que esses vetores da GA compõe um tipo de espaço vetorial.


# Operações Básicas

* [[Adição de Vetores]]
* [[Multiplicação de Vetor por escalar]]

**Propriedades...**
* i) (Comutativa) $u+v=v+u$
* ii) (Associativa) $(u+v)+w=u+(v+w)$
* iii) (Elemento Neutro) $u+\overline{0}=u$
* iv) (Elemento Oposto) $u+(-u)=\overline{0}$

> [!ps]- Ps.
> * **Unicidade:** Conseguimos também demonstrar a unicidade ($\exists!$) do elemento neutro e do inverso aditivo (repare que só faz sentido demonstrar o inverso aditivo depois de se ter demonstrado a existência do elemento neutro)
> * Essas 04 propriedades dizem respeito só à soma. Quando estudarmos estruturas algébricas, vamos ver que isso está associado à uma propriedade de grupo...


* v) $\alpha \cdot(\beta \cdot u)=(\alpha \cdot \beta) \cdot u$
* vi) $(\alpha+\beta) \cdot u=\alpha \cdot u+\beta \cdot u$
* vii) $\alpha \cdot(u+v)=\alpha \cdot u+\alpha \cdot v$
* viii) $1 \cdot u=u$

> [!obs]-
> * **Troca de operações:** Repare que, em (vi), há uma troca de operações: a soma do lado esquerdo é entre escalares, já no lado direito é entre vetores.
> * **Corpos:** Em (viii), de modo geral, nós trabalhamos com o 1 porque estamos falando em [[Espaços Vetoriais]] sobre os reais. Nós poderíamos falar espaços vetoriais sobre um **corpo** (do ponto de vista matemático), ou seja, nós poderíamos utilizar no lugar dos números reais, qualquer outro conjunto que seja bem **estruturado** (os corpos, como os reais, os complexos...). Dependendo do corpo que usamos, esse elemento neutro da multiplicação pode ser um número ou alguma outra coisa: um função, por exemplo. Mas, no caso de $\mathbb{R}$, é o 1 mesmo (porque ele é o neutro da multiplicação dos reais, que é o conjunto que estamos usando).


Seja $\mathcal{V}$ o conjunto formado por todos os vetores (GA). Prove que $\mathcal{V}$ não é vazio e, neste conjunto, estão definidas duas operações: adição e multiplicação por escalar tais que, para $u, v, w \in \mathcal{V}$ e $\alpha, \beta \in \mathbb{R}$ são válidos os 8 itens das proposições 1 e 3.

Feito isso, provamos que os vetores de GA constituem um espaço vetorial.


# Representação

Vetores como classe de equipolência de segmentos de retas orientados, que podem ser representados por coordenadas. Agora podemos manipulá-los algebricamente também; a manipulação geométrica ainda é ideal por causa da intuição e visualização.

* [[Coordenadas de Vetores]]

* [[Notação Matricial]]


# Produtos entre vetores

Podemos ver cada operação como uma função... (o $\times$ de $\mathbb{A} \times \mathbb{A}$ significa produto cartesiano...)
$$
\begin{aligned}
& +: \mathbb{A} \times \mathbb{A} \rightarrow \mathbb{A} \quad\;\;\;\;\;\text{(soma)} \\
& \cdot: \mathbb{R} \times \mathbb{A} \rightarrow \mathbb{A} \quad\;\;\;\;\;\;\,\text{(produto por escalar)} \\
& \cdot: \mathbb{A} \times \mathbb{A} \rightarrow \mathbb{R} \quad\quad\;\;\;\text{(produto escalar)} \\
& \times: \mathbb{A} \times \mathbb{A} \rightarrow \mathbb{A} \quad\quad\;\text{(produto vetorial)} \\
& \cdot: \mathbb{A} \times \mathbb{A}\times \mathbb{A} \rightarrow \mathbb{R} \quad\text{(produto misto)}\\
\end{aligned}
$$

**Aspectos geométricos relacionados a cada produto**
* Produto por escalar: paralelismo.
* Produto escalar: ortogonalidade.
* Produto vetorial: área do paralelogramo, paralelismo e colinearidade de pontos.
* Produto misto: volume, coplanaridade de vetores e pontos.

Essas operações, do ponto de vista da GA, nos permitem estudar elementos geométricos mais no ponto de vista analítico. Nós estudamos essas operações inicialmente com uma abordagem  sob a definição geométrica e depois caminhamos para uma abordagem de fazer contas com os elementos por ser mais fácil. Nós poderíamos ter definido direto pelo aspecto algébrico, daí nós teríamos que fazer a equivalência com o geométrico. Como essas definições são, de fato, equivalentes ($\iff$), podemos ir de um pro outro ou de outro pra um! Ver discussão sobre definição, **equivalência de definições**, existência e unicidade no início da aula 4.

> [!obs]-
> Essa ordem importa! 
> Na soma, a ordem importa a princípio, mas acabamos vendo que ela é comutativa (faz sentido, já que ambos os elementos que formam o domínio são do mesmo conjunto). 
> Já no produto por escalar, não faz sentido fazermos $\mathbb{A}\times \mathbb{R}$, porque a ordem certa é $\mathbb{R} \times \mathbb{A} \rightarrow \mathbb{A}$. Nós podemos claro definir um outra operação tal que $\mathbb{A}\times \mathbb{R} \rightarrow \mathbb{A}$. Mas isso seria outra operação (não teríamos nem como falar na igualdade entre $2v$ e $v2$).

* [[Produto Escalar]]
	*  [[Projeção Ortogonal]]
* [[Produto Vetorial]]
* [[Produto Misto]]
	* [[coplanaridade e colinearidade]]

Perceba que cada um desses produtos nos ajudam no aspecto geométrico (ver utilidades) e muito da origem deles está justamente relacionado a isso.


# Retas e Planos

Seguindo essa linha de definir objetos e operações geometricamente e encontrar uma definição equivalente ($\iff$) algebricamente, vamos estudar de forma um pouco melhor retas e planos: os casos mais básicos de espaços vetoriais e subespaços vetoriais.

* [[Retas]]
* [[Planos]]

* [[Subespaços Vetoriais em GA]]
* [[Ângulo entre retas e planos]]
* [[Distâncias]]



