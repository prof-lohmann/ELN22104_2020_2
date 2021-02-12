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

Em "Input Common-Mode Voltage Range" ou seja Vcm de entrada está especificado os valores de -0.2V à 5.2V. Portanto

-0.2V < Vcm < (V+) +0.2V 

Dessa forma ja responde o outro item. (- Máxima e mínima tensão de entrada)

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

- Impedância de entrada

Rin: 6 Mega ohms

