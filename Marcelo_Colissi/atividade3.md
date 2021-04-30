#### Atividade 3

## Simulação com Amplificadores operacionais AD8040 e AD8539.
### Questão 1: Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

#### AD8040

 ◦ Máxima e mínima tensão de alimentação:
  2,7 _ +12 V
 ◦ Tensão de modo comum:
  -5,2 _ +5,2V
 ◦ CMRR
  -4,5 _ +3 V
 ◦ Máxima e mínima tensão de entrada
  Faixa de ±200 mV
 ◦ Tensão de offset
  Máximo 6 mV
 ◦ Corrente de polarização
  0,7 _ +1,3 uA
 ◦ Consumo de corrente
  1,3 mA
 ◦ Ganho em malha aberta
  -4,0 _ +4,0 V
 ◦ Impedância de entrada
  6 MΩ e 2 pF
  
#### AD8539

 ◦ Máxima e mínima tensão de alimentação:
  –2,7 _ +5,5 V
 ◦ Tensão de modo comum:
  0 _ +5,0 V
 ◦ CMRR
  0 _ +5 V
 ◦ Máxima e mínima tensão de entrada
  0 _ +5 V
 ◦ Tensão de offset
  Máximo 13 uV
 ◦ Corrente de polarização
  0,7 _ 1,3 uA
 ◦ Consumo de corrente
  15 _ 25 pV
 ◦ Ganho em malha aberta
  0,1 _ 4,9 V
 ◦ Impedância de entrada
  10 KΩ e 300 pF
  
## Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet
 
### Questão 2: Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.
1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
2. Responda quais os valores das tensões de saturação?

#### AD8040

![Figura_1](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG1.jpg)


![Figura_2](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG2.jpg)


Para simular, utilizou-se uma alimentação de 5V na entrada V+ e -5V na entrada V-, conforme descrito no datasheet, com uma frequência de 1 kHz. Analisando o gráfico acima, podemos perceber que o AmpOp trabalha fora de saturação, já que atinge no máximo 5 V e no mínimo -5V, conforme a alimentação. Além disso, é possível perceber que o circuito se trata de um seguidor de tensão, pois faz uma cópia quase perfeita da tensão de entrada na sua saída. Analisando os valores de pico máximo e mínimo obtemos respectivamente, 4,9979V e -4,9977V. Sendo assim, obtemos uma tensão de offset de 2,1 mV no pico máximo e 2,3 mV no vale, valores que se encaixam nas especificações encontradas no datasheet.

![Figura_3](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG3.jpg)


No gráfico acima, foi aplicada uma tensão de 6V na fonte colocada na entrada não inversora, conforme pode-se observar a saturação acontece e a tensão não ultrapassa os 5V da alimentação simétrica.

#### AD8539

![Figura_4](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG4.jpg)


![Figura_5](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG5.jpg)


Nesta simulação utilizou-se uma alimentação de ± 2,5V, com uma frequência de 1 kHz. Aplicando uma tensão de 2.5V na entrada inversora observa-se que o AmpOp não satura e trabalha com 2,4986 V na crista e -2,4981 V no vale, o que nos resulta em uma tensão de offset de 1,4 mV e 1,9 mV, respectivamente, valores que também obedecem as especificações do datasheet.

![Figura_6](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG6.jpg)


No gráfico acima apresentado, foi aplicada uma tensão de 5,0V na fonte conectada à entrada não inversora, conforme pode-se observar a saturação acontece e a tensão não ultrapassa os 2,5V da alimentação simétrica.

### Questão 3: Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
#### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

##### AD8040

Simulando o circuito mostrado na imagem abaixo com o AmpOp AD8040 e aplicando à sua entrada inversora 0V obtemos uma tensão de saída (Vo) de 16,96 mV. Sabendo que o valor da tensão de offset é igual a Vo dividido pelo ganho, temos que Voff é igual a 0,1696 mV  que se encaixa nas especificações presentes no datasheet.

![Figura_7](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG7.jpg)


![Figura_8](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG8.jpg)


##### AD8539

Da mesma forma que o item anterior, simulou-se o circuito mostrado na figura abaixo, porém com o AmpOp AD8539. Aplicando à sua entrada inversora 0V obtemos uma tensão de saída (Vo) de 1,387 mV. Sabendo que o valor da tensão de offset é igual a Vo dividido pelo ganho, temos que Voff é igual a 0,01387 mV ou 13,87 uV, valor que se encaixa nas especificações presentes no datasheet.

![Figura_9](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG9.jpg)


![Figura_10](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG10.jpg)


#### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

##### AD8040

Aplicou-se um sinal senoidal de 5 mV de amplitude com frequência de 1 kHz com o AmpOp AD8040 conforme o circuito abaixo.

![Figura_11](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG11.jpg)


![Figura_12](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG12.jpg)


Idealmente era esperado que os valores para a tensão de saída fossem 500 mV e -500 mV conforme foi imposto à entrada inversora, porém ao simular obtivemos os resultados apresentados no gráfico acima, 481,27 mV no pico e -515,38 mV no vale. Para o entendimento desta diferença é necessário lembrar da existência da tensão de offset. No caso do AmpOp AD8040 a tensão de offset foi 0,1696 mV, associando este valor ao ganho de -100V/V, ou seja, multiplcando Voff pelo ganho, temos cerca de -16,96 mV que é praticamente a diferença existente entre os valores ideais e simulados.

##### AD8539

Aplicando o mesmo circuito, porém agora com o AmpOp AD8539, obteve-se os seguintes resultados:

![Figura_13](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG13.jpg)


![Figura_14](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG14.jpg)


A tensão de crista foi 496,01 mV e a de vale foi -493,21 mV. No caso do AmpOp AD8539 a tensão de offset foi 0,01387 mV, associando ao ganho de -100V/V temos cerca de -1,387 mV que fazem com que a diferença entre o ideal e o simulado quase desapareçam.

### Questão 4: Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

#### AD8040

Sabendo que o ganho do amplificador não inversor é G= 1 + Rf/R1, será utilizado Rf = 900 ohms e R1 = 100 ohms.

![Figura_15](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG15.jpg)


![Figura_16](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG16.jpg)


Aplicando 0V na entrada obteve-se na saída o resultado de -1,527 mV.

Aplicando:
5 mV: 48,376 mV
50 mV: 497,65 mV
200 mV: 1,9960 V
500 mV: 4,975 V

Percebe-se que conforme cada década de aumento da tensão aplicada a tensão de saída dimunui por década. Calculando o erro percentual com relação ao ganho de 10V/V, temos:
5 mV: 3,36 %
50 mV: 0,472 %
200 mV: 0,2 %
500 mV: 0,5 %

Quanto menor é a tensão aplicada, maior é o erro.

#### AD8539

Sabendo que o ganho do amplificador não inversor é gual a G= 1 + Rf/R1, será utilizado Rf = 900 ohms e R1 = 100 ohms.

![Figura_17](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG17.jpg)


![Figura_18](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSATV3_CERTA/FIG18.jpg)


Aplicando 0V na entrada obteve-se na saída o resultado de 137,3 uV conforme no gráfico acima.

Aplicando:
1. 5 mV: 50,136 mV
2. 50 mV: 500,13 mV
3. 200 mV: 2,0000 V
4. 500 mV: 2,2795 V

Calculando o erro percentual com relação ao ganho de 10V/V, temos:
1. 5 mV: 0,27 %
2. 50 mV: 0,0,26 %
3. 200 mV: 0,00 %
4. 500 mV: > 100 % - saturação.


### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.
Pode-se utilizar o AD8539 porque esse ampop se comportou melhor do que o AD8040 quando lhe foi aplicado baixas tensões de entrada.

### Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
Outro ampop que seria uma boa escolha escolha é o LTC 2063 já que ele possui tensões de offset máximas menores que as tensões de offset do AD8539.
