# Simulação de Circuitos com Amplificadores Operacionais

## Características dos modelos AD8040 e AD8539

### AD 8040

* Máxima e mínima tensão de alimentação: 2.7V e 12V

* Considerando alimentação simétrica -5V e 5V:

    - Tensão de Modo Comum: -5.2V a 5.2V
    - CMRR: 80dB a 90dB
    - Máxima e mínima tensão de entrada:  -5V a 5V
    - Tensão de Offset: 1.6mV a 5mV
    - Corrente de Polarização: 0.7uA a 1.3uA 
    - Consumo de Corrente: 1.4mA a 1.5mA
    - Ganho em Malha Aberta: 65dB a 74dB
    - Impedância de Entrada: 6 MΩ  

* Considerando alimentação de 5V:

    - Tensão de Modo Comum: -0.2 a 5.2
    - CMRR: 80dB a 90dB
    - Máxima e mínima tensão de entrada: 0V a 5V
    - Tensão de Offset: 1.4mV a 5mV
    - Corrente de Polarização: 0.8uA a 1.2uA 
    - Consumo de Corrente: 1.3mA a 1.5mA
    - Ganho em Malha Aberta: 65dB a 74dB
    - Impedância de Entrada: 6 MΩ  

* Considerando alimentação de 3V:

    - Tensão de Modo Comum: -0.2 a 3.2
    - CMRR: 78dB a 88dB
    - Máxima e mínima tensão de entrada: 0V a 3V
    - Tensão de Offset: 1.1mV a 5mV
    - Corrente de Polarização: 0.7uA a 1.2uA 
    - Consumo de Corrente: 1.3mA a 1.4mA
    - Ganho em Malha Aberta: 64dB a 73dB
    - Impedância de Entrada: 6 MΩ  


### AD 8539

* Máxima e mínima tensão de alimentação: 2.7V e 5.5V

* Considerando alimentação de 5V:

    - Tensão de Modo Comum: 2.5V
    - CMRR: 115dB a 135dB
    - Máxima e mínima tensão de entrada: 0V a 5V
    - Tensão de Offset: 5uV a 15uV
    - Corrente de Polarização: 15 pA a 60pA 
    - Consumo de Corrente: 170uA a 210uA
    - Ganho em Malha Aberta: 110dB a 130dB
    - Impedância de Entrada:

* Considerando alimentação de 2.7V:

    - Tensão de Modo Comum: 1.35V
    - CMRR: 110dB a 130dB
    - Máxima e mínima tensão de entrada: 0.2V a 2.5V
    - Tensão de Offset: 5uV a 16uV
    - Corrente de Polarização: 15pA a 25pA 
    - Consumo de Corrente: 210uA
    - Ganho em Malha Aberta: 110dB a 130dB
    - Impedância de Entrada:

## 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados  e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.

Simulando ambos os ampops com alimentação 5V *single supply* e com uma tensão de entrada de 5V alternada, observamos que a tensão de saída dos ampops fica próxima dos 4.5V, devido a saturação.

## 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.

```
G = -(R2/R1)
-100 = -(100k/1k)
```
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

Para o Ampop AD8040, temos na saída do circuito a tensão de 102mV, resultante de sua tensão de offset, que varia de 1.4mV a 5mV, com o ganho de 101V/V aplicado.

Para o Ampop AD8539, a saída do circuito é de 1.9mV, pois sua tensão de offset varia entre 5uV e 15uV.

### 2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.

O sinal de saída é 100 vezes maior que o sinal de entrada e possui 180 graus de defasagem. Isso ocorre por conta do ganho negativo aplicado de -100V/V.

## 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
```
G = 1 + (R2/R1)
10 = 1 + (9K/3K)
```
### 1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.

Para o ampop AD8040, a tensão de saída é de 84mV devido a sua tensão de offset que varia de, aproximadamente, 1.4mV a 5mV.

Para o ampop AD8539, a tensão de saída é de 90uV, devido a sua tensão de offset que está entre 5uV e 15uV.

### 2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.


## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.

O modelo AD8539 é mais adequado para aplicação devido a sua baixa corrente de polarização e sua baixa tensão de offset. Mesmo não sendo ideal para sinais tão pequenos, seria muito melhor que o modelo AD8040 que possui um offset tão alto (1.4mV a 5mV).

Um modelo melhor para trabalhar com sinais tão pequenos de entrada seria o OPA2387, que possui um offset bem mais baixo (+-2uV).