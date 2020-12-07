**1. O que é o AmpOp?**

**R:**

Um componente que amplifica o sinal de saída em relação ao de entrada.


**2. Mostre os simbolos e as características do AmpOp IDEAL?**

Símbolos:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/opamp.png)

Características:

- Impedância de entrada infinita;

- Impedância de saída nula;

Em decorrência da impedância de entrada infinita o ampop não drena corrente e possibilita calcular as tensões e o ganho com maior facilidade.

Da mesma maneira a impedância de saída nula possibilita que a carga conectada receba toda a corrente que o ampop fornece, sem desvios.

**3. O que significa Malha Aberta e Malha Fechada?**

- Malha aberta: Circuito sem realimentação de tal forma que V0=A(V+-V-). O ganho "A" tende ao infinito e a tensão de saída V0 tende a Vcc ou Vee.
- Malha fechada: Circuito com realimentação no negativo do ampop.

**4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.**

Como ja citado na questão 2 os amplificadores operacionais ideais facilitam o cálculo, pois nao drena corrente de entrada.

Exemplo: Inversor:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/WhatsApp%20Image%202020-12-03%20at%2015.40.09.jpeg)

É notável que pelas condições ideais os calculos ficaram simplificados. As correntes de entrada, e saída do ampop são nulas. Possibilitando fazer V+=V-.

**5.Descreva as principais características das topologias:**

**a) Seguidor de Tensão (Buffer)**

- Características:

Essa configuração permite obter a tensão de saída (V0) igual a tensão de entrada(Vi). Nesse caso o resistor de entrada R1 tende a infinito e o resistor de realimentação R2 asssume o valor zero. O seguidor de tensão é mostrado a seguir:



![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/buffer.png)

**b) Amplificador Inversor**

- Características:

Nesse caso os resistores R1(entrada) e R2(realimentação) assumem valores diferentes de infinito e zero respectivamente.

A tensão de saída V0 no ganho em malha fechada depende dos resistores R1 e R2, assim como da tensão de entrada Vi. A fórmula exemplifica:

V0= -(R2/R1)*Vi

O ganho A= -R2/R1, significa que a tensão de saída sempre irá assumir um valor de sentido contrário da tensao de entrada.

O amplificador inversor é mostrado a seguir:
 
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/inversora.png)

**c) Amplificador Não Inversor**

- Características:

A tensão de saída nesse caso assume o mesmo sentido da tensao de entrada. Conforme a fórmula:

V0= (1+R2/R1)*Vi

O amplificador não inversor é mostrado a seguir:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/naoinversora.png)

**d) Amplificador Somador Inversor**

- Características:

Nesse caso existem mais de uma tensão de entrada na entrada inversora do ampop. E o terminal não inversor do ampop é aterrado.

Que serão somadas. Conforme a fórmula:

V0= -R4(V1/R1+V2/R2+...Vn/Rn)

OBS.: R4 é p resistor de realimentação.

O amplificador somador inversor é mostrado a seguir:
![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/somador%20inversor.png)

**e) Amplificador Somador Não Inversor**

- Características:

A diferença agora é de que as tensões de entrada serão aplicadas ao terminal inversor do ampop.

O amplificador somador não inversor é mostrado a seguir:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/somador%20nao%20inversor.png)

**f) Amplificador Subtrator**

- Características:

No subtrator têm-se sinal de entrada nos dois terminais do ampop. No terminal inversor e no não inversor.

Conforme mostrado a seguir:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/subtrator.png)

**g) Amplificador de Instrumentação**

![]()




