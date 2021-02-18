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
![grafio-buffer-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/quest%C3%A3o%202%20parte%206.jpeg)
Pode-se observar através dos gráficos que existe uma saturação quando a tensão de saída atinge os valores ao redor de 2.5V e -2.5V
## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
- Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
- Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.
### AD8040
![inversor-AD8040](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/ad8040%20inversor.jpeg)
Aplicando 0V na entrada, tem-se na tensão de saída 169,90mV. Como o ganho é de -100V/100V, o valor do offset será 100 vezes menor que a tensão de saída.
### AD8539
![inversor-AD8539](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Fotos%20atividade%203/8539%20inversor.jpeg)
Da mesma forma, aplicando 0V na entrada, tem-se na tensão de saída 1,38mV. Tanto no circuito com o ampop AD8040 e com o Ad8539 os valores de offset condizem com o datasheet.
## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
- Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
- Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.
#### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.
