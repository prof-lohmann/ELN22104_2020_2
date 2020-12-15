**1. O que é o AmpOp?**

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

A fórmula de tensão de saída é dada por:

V0= R6/R5*(V1-V2).  Quando R5=R1 e R6=R2

Conforme mostrado a seguir:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/subtrator.png)

**g) Amplificador de Instrumentação**

É um modelo onde exitem três amplificadores operacionais. Um está configurado em amplificador de diferenças(subtrator) e os outros dois na configuração não inversora.

- Características: 

O terra em comum dos dois amplificadores nao inversores é suprimido e têm-se uma corrente resultante.

Essa corrente ajuda a calcular as tensões de entrada do amplificador subtrator.

O que resulta em uma tensão de saída calculado em decorrência dessa corrente.


Como exemplificado abaixo:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/amp%20instrument.gif)

**6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias
Amplificador Inversor e Amplificador não inversor**

No ganho em malha aberta finito o ganho A da equação V0=A(V+ - V-) não é mais considerado infinito. Para efeitos de conta as equações da inversora e não inversora mudam.

- Amplificador inversor:

G=V0/Vi=(-R2/R1)/(1+(R2/R1))/A

obs.: R1-> resistor de entrada. R2-> Resistor de realimentação.

Considerando que A é diferente de infinito ele deve ser considerado na conta.

- Amplificador não inversor:

G= V0/Vi=(1+(R2/R1))/(1+(R2/R1))/A

Da mesma forma o termo A se diferente de infinito influência no resultado.

obs.: R1-> resistor de entrada. R2-> Resistor de realimentação.


**7. Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas
topologias estudadas**

Vcm é a tensao média nos pinos de entrada do amplificador, multiplicado por um ganho de modo comum. Idealmente Vcm é zero. O efeito é um acrescimo indesejado na tensão de saída V0.



**8. O que é CMRR?**

É a medida da capacidade do dispositivo de rejeitar o sinal comum das entradas positiva(V+) e negativa(V-).

Idealmente o CMRR é infinito. Porém não é isso que acontece no mundor real.

CMRR= |Av/Acm| Av= ganho em malha aberta. Acm= Ganho de modo comum.



**9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão
de modo comum (VCM), indicando:

**a) o impacto na tensão de saída com relação a tolerância dos resistores no
circuito:**

Primeiramente foi decidido o opamp a ser utilizado: lm321. Fabricante: Texas instruments.

Para dar seguimento a análise foi consultado o datasheet para saber qual a faixa de operação para as tensões de alimentação e a tensão de modo comum (Vcm).

- Supply voltage:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/supply%20voltage%20lm321.png)

Observa-se que a faixa de tensão de alimentação é de 2.7V a 5.5V

- Voltage common-mode

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/vcm%20lm321.png)

Observa-se que as tensões de entrada devem ser no mínimo 0.5V abaixo da tensão de alimentação Vee, e no máximo 0.5V acima da tensão de alimentação Vcc.

No circuito montado foi escolhido pelas tensões de alimentação de 0v para Vee e 5V para Vcc. Respeitando a faixa de operação apresentada no datasheet.

Para as tensões de entrada foi escolhido 0V para a entrada não inversora e 1mV para a entrada inversora. Respeitando Vcm.

Após simular o circuito em .op:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/simulm321.png)

Para o ampop subtrator V0= R4/R1*(V2-V1). Quando R1=R3 e R4=R2

Portanto observa-se que a na simulação V0 apresenta uma variação da tensão de saída de 617,94mV 
isso pode-se explicar pois os resistores R1 e R3, como também R2 e R4 não são exatamente iguais, justamente pela tolerância dos resistores. Isso também é explicado pela tensão de offset, Vcm e CMRR.

**b) Qual erro na tensão de saída com relação CMRR do AmpOp.**
Datasheet:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/Cmrrlm321.png)

Observa-se pelo datasheet que o erro é de 64dB a 94dB

**c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça
o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.**


**10. Faça um resumo explicando as limitações de tensão de entrada e saída de um
AmpOp. De exemplos, utiliza-se valores de datasheet.**

EX.:

OPAMP: OPA336

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/vcm.png)

Pode-se observar nessa imagem que as tensões de entrada do ampop (V+ e V-) podem variar ligeiramente 0.2volts abaixo da tensão Vee e até 1 volt abaixo de Vcc.

Observa-se que nos dois casos apresentados acima a diferença de tensão entre Vee e Vcc é de 5 volts. Porém mudam os valores. Sendo a primeira variando de 5v até 0v e a segunda varia de 2.5V até -2.5V.

Caso 1:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/vcm_1%205vground.png)

Vcc= 5V

Vee= 0V

As tensões de entrada do ampop (V+ e V-) podem variar de -0.2V até 4V.

Caso 2:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/vcm_2%202.5v-2.5.png)

Vcc= 2.5V

Vee= -2.5V

As tensões de entrada do ampop (V+ e V-) podem variar de -2.7V até 1.5V.



**a) Defina o que é um AmpOp Rail-to-rail**

É um Amplificador Operacional em que a tensão de saída atingi o mesmo nível que as tensões de alimentação do AmpOp Vcc e Vee.

Um amplificador operacional com entrada e saída Rail to Rail alimentado com 12V pode aceitar sinais de ate 12V na entrada sem saturar e fornecer o mesmo sinal de 12v na saída.

**11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de
um amplificador inversor?**

 A saída do amplificador operacional é idealmente nula quando as
entradas em potencial zero(ground). Entretando nos amplificadores reais, devido a um
desbalanceamento nas entradas existe uma tensão cc equivalente na entrada, isso é, o offset. O valor da tensão de "offset" nos amplificadores comerciais estão situado
na faixa de 1 a 100 mV. Nos amplificadores existem entradas
para ajuste da tensão de "offset".

- É possivel simular o efeito do offset na saída de um amplificador colocando potencial zero(ground) nas duas entradas.

A saída resultará no offset.

Para o componente lm321:

- Datasheet:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/offset_inversora_datash.png)

- Simulação:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/offset_inversora_simu_2.png)

OBS.: A tensão de saída tem o efeito de offset somado a tensao de modo comum(Vcm).

**12. Como minimizar o efeito da tensão de offset?**

Nos amplificadores comerciais existe dois pinos de ajuste de offset. A utilização de um potenciometro nesses pinos resolve o problema da tensão de offset.

**13. O que é a variação da tensão de offset pela temperatura?**


**a) Como verificar esse parâmetro no datasheet?**

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ2/imagens/offset_inversora_datash.png)



**14. O que são as correntes de polarização(Ibias) de AmpOp?**


**a) Como minimizar o efeito destas correntes? Descreva as aproximações e os
possíveis circuitos para mitigar o problema.**

**b) Descreva a corrente de offset na polarização dos AmpOp**







