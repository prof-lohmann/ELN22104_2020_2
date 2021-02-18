# ATIVIDADE 3
## 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:
### AD8040
- Máxima e mínima tensão de alimentação: 2.7V a 12.0V
- Tensão de modo comum: -5.2V a +5.2V
- CMRR: -4.5V a +3.0V
- Máxima e mínima tensão de entrada: 200mV
- Tensão de offset: 6mV
- Corrente de polarização: 0.7µA a 1.3µA
- Consumo de corrente: 1.3A
- Ganho em malha aberta: +-4.0V
- Impedância de entrada: 6MΩ
### AD8539
- Máxima e mínima tensão de alimentação: 2.7V a 5.5V
- Tensão de modo comum: 2.5V
- CMRR: 0V a 5.0V
- Máxima e mínima tensão de entrada: 0V a 4.8V
- Tensão de offset: 15µV
- Corrente de polarização: 25pA
- Consumo de corrente: 180pA
- Ganho em malha aberta:
- Impedância de entrada:
#### Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet.
## 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.
- Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.
- Responda quais os valores das tensões de saturação?
### AD8040
![buffer-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%201.jpeg)

De acordo com o datasheet do ampop, os pinos de alimentação foram alimentados com 5V e -5V e na entrada uma fonte sinusoidal com aplitude de 12V e frequência de 1kHz
![grafico-buffer-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%202.jpeg)
![grafico2-buffer-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%203.jpeg)
Pode-se observar através dos gráficos que existe uma saturação quando a tensão de saída atinge os valores ao redor de 5V e -5V
### AD8539
![buffer-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%204.jpeg)

De acordo com o datasheet do ampop, os pinos de alimentação foram alimentados com 2.5V e -2.5V e na entrada uma fonte sinusoidal com aplitude de 5.5V e frequência de 1kHz
![grafico-buffer-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quets%C3%A3o%202%20parte%205.jpeg)
![grafico-buffer-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%206.jpeg)
Pode-se observar através dos gráficos que existe uma saturação quando a tensão de saída atinge os valores ao redor de 2.5V e -2.5V
## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
- Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
- Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.
### AD8040
![inversor-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/ad8040%20inversor.jpeg)
Aplicando 0V na entrada, tem-se na tensão de saída 169,90mV. Como o ganho é de -100V/100V, o valor do offset será 100 vezes menor que a tensão de saída.
Aplicando um sinal senoidal de 10mVpp@1kHz
![inversor10Vpp-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/circuito%20ad8040%2010vpp.jpeg)
![grafico-inversor10Vpp-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/gr%C3%A1fico%20ad8040%2010vpp.jpeg)
Idealmente, os valores de máximo e mínimo de saída deveriam ser respectivamente 500mV e -500mV. Porém, tais valores não são alcançados por conta do valor de offset do aparelho. Os valores de máximo e mínimo medidos da tensão de saída são respectivamente 327,71mV e -668,22mV
### AD8539
![inversor-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/8539%20inversor.jpeg)
Aplicando 0V na entrada, tem-se na tensão de saída 1,38mV. Tanto no circuito com o ampop AD8040 e com o Ad8539 os valores de offset condizem com o datasheet.
Aplicando um sinal senoidal de 10mVpp@1kHz
![inversor10Vpp-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/circuito%20ad8539%2010vpp.jpeg)
![grafico-inversor10Vpp-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/gr%C3%A1fico%20ad8539%2010vpp.jpeg)
Novamente, o desejado seria alcançar os 500mV de máximo e -500mV de mínimo. Neste circuito isso já foi mais próximo de ser alcançado, por ter um valor diferente de offset em relação ao primeiro circuito.
## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
- Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
- Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.
### AD8040
![naoinversor-ad8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/ad8040%20exerc%204.jpeg)
![grafico-naoinversor-ad8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/grafico%20ad8040%20exerc%204.jpeg)
Aplicando 0V na entrada do circuito não inversor para o ampop AD8040,tem-se na saída -15.295mv.Tal valor é oriundo também do valor de offset do ampop.
Aplicando os valores de sinal contínuo solicitados, tem-se os valores de saída:
- 5mV --> 35.8mV
- 50mV --> 485.8mV
- 200mV --> 1.9868V
- 500mV --> 4.972V

Como o ganho era de 10V/V, era esperado um valor 10 vezes maior que o valor aplicado na entrada. Segue abaixo os erros relaticos em relação ao ganho:

- 5mV --> 28.4%
- 50mV --> 2.84%
- 200mV --> 0.66%
- 500mV --> 0.56%
### AD8539
![naoinversor-ad8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/ad8539%20exerc%204.jpeg)
![grafico-naoinversor-ad8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/grafico%208539%20exerc%204.jpeg)
Aplicando 0V na entrada do circuito não inversor para o ampop AD8539,tem-se na saída 1.2mV.Tal valor é oriundo também do valor de offset do ampop.
Aplicando os valores de sinal contínuo solicitados, tem-se os valores de saída:
- 5mV --> 51.2mV
- 50mV --> 501.2mV
- 200mV --> 2.0024V
- 500mV --> 2.479V

Como o ganho era de 10V/V, era esperado um valor 10 vezes maior que o valor aplicado na entrada. Segue abaixo os erros relaticos em relação ao ganho:

- 5mV --> SATUROU
- 50mV --> SATUROU
- 200mV --> SATUROU
- 500mV --> 99.99%
#### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. 
Eu escolheria o amplficador 8539 por apresentar menos sinais de saturação com um ganho de 100V/V, apesar da simulação ter sido com um frequência alta(1kHz), esse amplificador apresentou melhor comportamento nessas condições.
#### Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
