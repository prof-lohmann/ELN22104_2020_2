**1. Verifique no datasheet dos Ampops indicados os valores:** 

- Máxima e mínima tensão de alimentação
- Tensão de modo comum
- CMRR
- Máxima e mínima tensão de entrada
- Tensão de offset
- Corrente de polarização
- Consumo de corrente
- Ganho em malha aberta
- Impedância de entrada

**Datasheet do ampop AD8040 utilizado:**
- link : https://www.analog.com/media/en/technical-documentation/data-sheets/AD8029_8030_8040.pdf


- Máxima e mínima tensão de alimentação:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/wide%20supply%20voltage.png)

Em "wide supply range" está especificado os valores de 2.7V a 12v. Sendo assim a faixa de operação do ampop é de 2.7V(min) até 12V(max).



Interpretando o datasheet observa-se que ele fornece informações para duas tensões de alimentação 5V e 3V.

Para as especificações de alimentação com 5v têm-se:

SPECIFICATIONS WITH +5 V SUPPLY:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/AD8040_Characteritics_5v.png)

- Tensão de modo comum:

Vcm= 2.5v

- Máxima e mínima tensão de entrada:

Em "Input Common-Mode Voltage Range" ou seja Vcm de entrada está especificado os valores de -0.2V à 5.2V. Portanto

-0.2V < Vcm < (V+) +0.2V 


- CMRR:


min: 80dB 
Ty: 90dB

- Tensão de offset:

ty: 1.4 mV

max: 5  mV

- Corrente de polarização:

ty: 0.8 uA

max: 1.2 uA

- Consumo de corrente

ty: +/- 0.1 uA

max: +/- 0.9 uA


- Ganho em malha aberta

min: 65 dB

ty: 74 dB

- Impedância de entrada:

Rin: 6 Mega ohms




**Datasheet do ampop AD8539 utilizado:**

- link: https://www.analog.com/media/en/technical-documentation/data-sheets/AD8538_8539.pdf

- Máxima e mínima tensão de alimentação:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/supply%20voltage.png)

Maxima= 5.5V
Minima= 2.7V

- Máxima e mínima tensão de entrada

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/VCM_MAINPUJT.png)

Analisando temos:  VSS − 0.3 V to VDD + 0.3 V




- Tensão de offset:

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/voff.png)

ty: 5uV

max: 13uV


- Vcm:

Vcm= 2.5V

- CMRR:

min: 110 dB

ty: 140 dB
- Corrente de polarização:

ty: 15 pA

max: 25 pA

- Consumo de corrente:

ty: 20uA

max: 50uA


- Ganho em malha aberta:

min: 115dB

ty: 141dB

- Impedância de entrada:

  Rin: 6 Mega ohms
  
  
  **2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.**


- AD8539

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/buffer_85.png)

A tensão de entrada é senoidal com 2.8V de amplitude. Entretando o ampop satura em 2.5v(Tensão de alimentação)

2.8V é a tensão máxima recomendada para tensão de entrada  --> vcc+0.3= 2.5+0.3=2.8V 

- AD8040

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/buffer_80.png)

Como especificado no datasheet a maxima tensão de entrada é de Vcc + 0.2v. Entretanto a saída V0 satura em 5v (Vcc).


**3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.**

**A) Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.**


- AD8539

Os resistores R1 e R2 foram escolhidos sendo 1k e 100k respectivamente pois dessa forma a corrente de polarização não irá interferir no circuito, uma vez que a corrente que circulará no circuito será na casa de uA e a corrente de polarização é da ordem de pA.

Também foi considerado o ganho de -100V/V = -(R2/R1)*Vin

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/inversora_vin0v.png)



Na simulação contata-se que Voff= 13.7uV. Uma vez que V0= 1.37mV com um ganho de 100V/V. Sendo que a entrada Vin foi zerada(OV) única tensão restante é a tensão de offset.

- AD8040

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/inversora_80_0v.png)

Os resistores R1 e R2 foram escolhidos sendo 1Oohm e 100ohms respectivamente pois dessa forma a corrente de polarização não irá interferir no circuito, uma vez que a corrente que circulará no circuito será na casa de mA e a corrente de polarização é da ordem de uA.

Também foi considerado o ganho de -100V/V = -(R2/R1)*Vin

**B) Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.**

- AD8539

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/inversora_vin5mv.png)

Como esperado na simulação o ganho de -100*Vin. Para Vin=-5mv ---> V0=500mv

**Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V**

**B)2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.**


- AD8539


Vin= 5mV:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/ninv_5m.png)

Voff= 13.73uV


Vin= 50mV:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/ninv_50m.png)

Voff= 13.6uV


Vin= 200mV:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/ninv_200m.png)

Voff= 13uV


Vin= 500mV:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/ninv_500m.png)

Observa-se que com a tensão de alimentação em 2.5V o ampop satura. Dessa forma foi alterado a tensão de aliemtação para +6V.

Vin= 500mV. Vcc alterado +6V:


![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/ninv_500m_vcc6%2B.png)

Voff=25uV

Para todas as simulações V0 reagiu de forma esperada com um ganho de 10V/v da tensão de entrada Vin.

Ainda para a maioria dos sinais existe um resíduo no sinal de aproximadamente 13uV. O que se explica pelo offset do ampop.










**Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito
pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops
você utilizaria? Justifique a sua resposta.**

Comparando o V0ff e Ibias dos dois ampops:

- AD8040


Voff:


ty: 1.4 mV

max: 5  mV

Corrente de polarização:

ty: 0.8 uA

max: 1.2 uA




- AD8539
- 
Voff:


ty: 5uV

max: 13uV

Ibias:

ty: 15 pA

max: 25 pA

 A aplicação utilizará sinais na faixa de uV à mV. Portanto o AD8539 é mais indicado para essa aplicação. A corrente de polarização e a tensão de offset do AD8539 são milhões de vezes menores que a do AD8040..
















