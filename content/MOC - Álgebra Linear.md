
Inicialmente, analisaremos as figuras geométricas sob a ótica da Geometria Analítica. Usaremos as propriedades dos vetores do $\mathbb{R}^{2}$ e do $\mathbb{R}^{3}$, que são Espaços Vetoriais conhecidos, para descrever elementos da Geometria plana.
* [[MOC - Álgebra Vetorial]]

> [!discussao]- Conceitos de Álgebra Linear aplicados a GA.
> Em GA, nós usamos vetores para descrever objetos que não são Espaços Vetoriais. Isso gera um conflito:
> 
> Na GA, trabalhamos com o conceito de vetor livre, ou seja, podemos representar um vetor saindo da origem ou do ponto $(10,10)$.
> 
> A Álgebra Linear, por outro lado, é mais rígida. Os vetores de um EV precisam estar "colados" à origem a fim de respeitar os Axiomas de EV. Imagine, no caso de $\mathbb{R}^{3}$, que o objeto que vai do ponto $(10,10)$ ao $(11,11)$ pudesse ser um vetor do EV. Ele não respeitaria regras básicas, como o resultado $0 \odot v=\bar{0}$.
> 
> Para resolver esse conflito em GA, usamos vetores para construir objetos chamados **Espaços Afins**. Quando escrevemos a eq. da reta $r: X = P_0 + t\vec{v}$:
> - O $t\vec{v}$ é um **espaço vetorial** (uma reta na origem).
>     
> - O $P_0$ é um "ponto de ancoragem".
>     
> - A soma $P_0 + t\vec{v}$ gera a reta deslocada. A reta resultante não é um espaço vetorial, é um conjunto de pontos.
>   
> Da mesma forma, na eq. do plano $X = P_0 + a \cdot u + b \cdot v$, temos o **espaço gerado** $a \cdot u + b \cdot v$ deslocado em relação à origem, formando um plano afim.
> 
> 
> Resumindo, a GA pega emprestado conceitos da Álgebra Linear para descrever objetos geométricos e, para isso, acaba incorporando alguns conceitos a mais. Um exemplo disso é a operação abaixo (relembre [[Retas]]):
> $\text{Ponto} = \text{Ponto} + \text{Vetor}$
> Na Álgebra Linear pura, não somamos "pontos", mas sim vetores.


Agora, vamos estudar outros espaços vetoriais clássicos.
* [[Matrizes]]
* [[Sistemas Lineares]]
* [[O Determinante]]

> [!discussao]- Conceitos de Álgebra Linear aplicados a Matrizes.
> Tudo o que discutimos acima se aplica da mesma forma a matrizes:
> Lembra que falamos que a GA "extrapola" a Álgebra Linear usando um ponto de ancoragem? Note como a solução geral de um sistema $A\mathbf{x} = \mathbf{b}$ é escrita:
> 
> $X = X_p + X_h$
> 
> Onde:
> 
> - $X_h$ é a solução do sistema **homogêneo** ($AX = \mathbf{0}$). Isso é o **subespaço vetorial** (uma reta ou plano na origem).
>     
> - $X_p$ é uma **solução particular** (um ponto qualquer que satisfaz a equação).
>     
> 
> Isso é exatamente a fórmula da reta/plano que discutimos: $\text{Ponto} + \text{Vetor}$.
> 
> O sistema $AX = B$ descreve um **conjunto afim**: ele pega o subespaço $AX = \bar{0}$ e o desloca no espaço pelo vetor $X_p$.
> 
> Em resumo:
> - $AX = \bar{0}$ é o "plano que passa na origem" (puro, algébrico, um subespaço).
>     
> - $AX = B$ é o "plano deslocado" (geométrico, afim, não é um subespaço).
>     
> 
> A Álgebra Linear foca no $AX = \mathbf{0}$ porque ele revela a estrutura interna da matriz (o chamado _Núcleo_ ou _Kernel_). O $B$ é apenas um "empurrão" externo que tira o sistema dessa pureza estrutural. 


Até agora, vimos Espaços Vetoriais como sendo meros acasos do destino: às vezes uma reta passa pela origem e descreve um SV, às vezes um plano, às vezes um SL que acaba por ser homogêneo, e por aí vai. Isso é o que chamamos de Espaços Afins, que fogem da pureza estrutural de Álgebra Linear (ver as duas últimas discussões). É nessa estrutura que vamos focar agora.
* [[Espaços Vetoriais e Subespaços Vetoriais]]
* [[Combinação Linear e Dependência Linear]]
* [[Bases e Coordenadas]]
* [[Transformações Lineares]]

Entraremos agora no estudo de autovalores e autovetores, que reúnem muitos dos conceitos anteriores.
* [[Autovalores e Autovetores]]
* [[Propriedades de autovalores e autovetores]]
* [[Diagonalização]]
* [[Matrizes ortogonais e simétricas]]
* [[Teorema Espectral]]


