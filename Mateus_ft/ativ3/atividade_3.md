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




**Datasheet do ampop AD8039 utilizado:**

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

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/LT_BUFFER.png)

A tensão de entrada é senoidal com 5.2V de amplitude. Entretando o ampop satura em 5v(Tensão de alimentação)

5.2V é a tensão máxima recomendada para tensão de entrada  --> vcc+0.2= 5+0.2=5.2V 

- AD8040

![](https://github.com/tatimmtt/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Mateus_ft/ativ3/imagens/VOUT%20BUFFER.png)


**3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.**


**Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito
pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops
você utilizaria? Justifique a sua resposta.**

Utilizaria o ampop AD8539 pois é um amplificador de altissima precisão com tensão de deslocamento extremamente baixa, corrente de polarização de entrada baixa e baixa potência
consumo. 











