Data Criada: 06/06/2026 às 20:16
Tags:

Tipos:
Exemplos:
Construções:
Generalizações:

Propriedades:
Suficiências:
Equivalências:
Justificativas:

Ver nota de aula 20 do Milton para entender a notação de Leibniz. Tudo o que é apresentado são apenas notações para coisas que estão definidas rigorosamente de outra forma. Vou tecer alguns comentários nos pontos mais importantes...

A derivada $f^{\prime}(x)$, isto é, a função $f^{\prime}$ avaliada no ponto $x$ é denotada por
$$
\frac{df}{dx}
$$
Isso denota uma razão de diferenciais da definição de derivada.

A função derivada de $f$, por outro lado, sem ser avaliada em nenhuma variável, é denotada simplesmente por $df$, seja lá o que isso quer dizer.


> [!exemplo]
> Logo, denotamos a fórmula de Leibniz por (sem nos preocuparmos em que variável estamos avaliando-a)
> $
> d(fg) = f \,dg + g\;df
> $
> Ou, de modo mais explícito para um ponto específico $x$, usamos
> $\frac{d}{dx}[f(x)g(x)] = f(x)\frac{dg}{dx}(x) + g(x)\frac{df}{dx}(x)$

> [!exemplo]
> A regra da cadeia também tem uma forma particular tomando $h = f \circ g$
> $
> \frac{dh}{dx} = \frac{df}{dg} \cdot \frac{dg}{dx}
> $
> Isso é só uma notação, um mnemônico para lembrarmos das fórmulas. Ela não representa nenhuma operação bem definida.


Uma notação que Leibniz também inventou é a notação de **integral indefinida**. A integral indefinida
$$
\int fdx
$$
denota **qualquer** antiderivada (ou primitiva) da função $f$. Às vezes, é usada a notação do tipo
$$
\int x^{2}dx = \frac{x^{3}}{3}+C
$$
para lembrar que $\int x^{2} \, dx$ não é uma única função. Leibniz entendia a integração e a diferenciação como operações inversas, levando a notações do tipo
$$
\int \frac{df}{dx} \, dx = \int df = f
$$
A primeira igualdade vem a **definição** de $\int df$. Já a segunda igualdade vem do TFC. 

Por definição, segue também que
$$
\int f \, dg = \int f\frac{dg}{dx} \, dx 
$$

A fórmula de integração por partes escreve-se como
$$
\int f \, dg =fg-\int g \, df
$$
onde as duas integrais das pontas são indefinidas, pelo que têm constantes embutidas.


A maior utilidade desta notação está ao utilizar a [[Fórmula de mudança de variáveis]] (ou fórmula de substituição).

> [!obs]
> Em notação de Leibniz, primeiros nós calculamos a integral indefinida para achar uma primitiva e só depois calculamos a integral definida como a diferença da antiderivada avaliada em quaisquer intervalos de integração.



