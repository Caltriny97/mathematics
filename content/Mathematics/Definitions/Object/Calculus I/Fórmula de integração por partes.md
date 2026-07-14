Data Criada: 06/06/2026 às 18:48
Tags:

Provado por:
Referências:
Justificativas:

Especializações:
Generalizações:

Começaremos vendo o que nos diz a fórmula de Leibniz (relembre [[Propriedades da derivada]]. Lembremos que

$$
(f g)^{\prime}=f g^{\prime}+f^{\prime} g .
$$

Usando o [[O Teorema Fundamental do Cálculo|TFC]], esta fórmula implica que

$$
f(b) g(b)-f(a) g(a)=\int_a^b\left(f(x) g^{\prime}(x)+f^{\prime}(x) g(x)\right) d x .
$$

> [!obs]
> Nós integramos a identidade $(f g)^{\prime}=f g^{\prime}+f^{\prime} g$ entre $a$ e $b$. Podemos fazer isso, pois, se duas funções são iguais em todo ponto, então suas integrais são iguais.
> 
> Note que, do lado esquerdo, temos a derivada duma função, logo sabemos calcular sua integral usando TFC. Porém, do lado direito, não temos a derivada duma função explícita.
> 
> Esse é o ponto: a fórmula da IPP nos dá uma relação entre um coisa que sabemos calcular e outras duas que a princípio não sabemos.


Esta fórmula é conhecida como **fórmula de integração por partes (IPP)**, e usualmente é usada na versão

$$
\int_a^b f(x) g^{\prime}(x) d x=f(b) g(b)-f(a) g(a)-\int_a^b f^{\prime}(x) g(x) d x .
$$

> [!ps] Notação.
> A notação
> 
> $
> \left.f(x)\right|_a ^b=f(b)-f(a)
> $
> 
> é muito útil no calculo de integrais. A fómula de IPP escreve-se
> 
> $
> \begin{aligned}
> \int_a^b f(x) g^{\prime}(x) d x & =\left.f(x) g(x)\right|_a ^b-\int_a^b f^{\prime}(x) g(x) d x . \\ \text{ou}&\\
> \int_a^b f g^{\prime} d x & =\left.f g\right|_a ^b-\int_a^b f^{\prime} g d x
> \end{aligned}
> $

> [!exemplo]
> Ver produto de Wallis na nota de aula 19 do Milton.