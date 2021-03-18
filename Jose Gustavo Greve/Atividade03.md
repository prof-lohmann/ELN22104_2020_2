# Atividade 03
## Aluno: José Gustavo dos Santos Greve
### 1) Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:
### AD8040
#### a) Máxima e mínima tensão de alimentação: +2,7 a +12,0 V
#### b) Tensão de modo comum: -0,2 a 5,2 V
#### c) CMRR Vcm rr: -4,5 a +3,0 V
#### d) Máxima e mínima tensão de entrada: 200 mV acima ou abaixo de Vc
#### e) Tensão de offset: 6 mV
#### f) Corrente de polarização: +0,7 a -1,5 uA
#### g) Consumo de corrente: 1,3 mA
#### h) Ganho em malha aberta: -4 a +4 V
#### i) Impedância de entrada: 6M Ohm e 2pF
### AD8539
#### a) Máxima e mínima tensão de alimentação: 2,7 a 5,5 V
#### b) Tensão de modo comum: 0 a 5,0 V
#### c) CMRR Vcm: 0 a 5,0 V
#### d) Máxima e mínima tensão de entrada: 0 a 5,0 V
#### e) Tensão de offset: 15 uV
#### f) Corrente de polarização: 25 a 60 pA
#### g) Consumo de corrente: 180 uA
#### h) Ganho em malha aberta: 0,1 a 7 V
#### i) Impedância de entrada: 10k Ohm e 300pF
### 2) Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os
### efeitos decorrentes da máxima e mínima tensão de entrada.
#### AD8040
![AD8040](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/AD8040.PNG)
![AD8040](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/image.png)
#### No gráfico acima foi aplicado 6 V na fonte na entrada não inversora, mantendo a alimentação do AmpOp com a esécificação do datasheet, mostrando a tensão de saturação.
![AD8539](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/AD8539.PNG)
![AD8539](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/AD8539%20gr%C3%A1fico.PNG)
#### No AD 8539 utilizamos alimentação de ±2.5V. Acima disso sempre ocorrerá a saturação.
### 3) Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.
![AD8040](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Questao%203%20-%208040.PNG)
### Aplicando 0V no circuito com o AD 8040, vamos ter Vout=-169,9 mV. O valor do offset é muito menor do que o valor de Vout, o que bate com o valor do offset com o valor do datasheet do AmpOp 8040.
![AD8040](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Grafico%20questao%203%20-%208040.PNG)
### Verificando os valores máximos e mínimos no gráfico, encontramos o valor de aproximadamente Vmin = -668 mV e Vmax = 327 mV, o que nos dá o offset amplificado, o que convém com o datasheet do componente.
#### AD 8539
![AD8539](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Q3%20-%20AD%208539.PNG)
![AD8539](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Grafico%203%20-%20AD%208539.PNG)
#### Observamos ao valor de aproximadamente Vmax = 493,55 mV e Vmin = -492,02mV. Isso nos dá um offset maior do que o previsto em simulação.
### 4) Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual 10V/V.
#### AD 8040
![AD8040](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Questao%204%20-%20AD%208040.PNG)
#### Aplicando:

#### 5 mV: 34,5 mV
#### 50 mV: 482,6 mV
#### 200 mV: 1,99 V
#### 500 mV: 4,98 V
#### Calculando o erro percentual com relação ao ganho de 10V/V, temos:

#### 5 mV: 30,6 %
#### 50 mV: 3,1 %
#### 200 mV: 1,0 %
#### 500 mV: 0,5 %
#### Ou seja, quanto mais baixa é a tensão aplicada, maior é o erro.
#### AD 8539
![AD8539](https://github.com/JoseGustavoGreve/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Jose%20Gustavo%20Greve/Questao%204%20-%20AD%208539.PNG)
#### Aplicando 0V na entrada obteve-se na saída o resultado de 137 uV.

#### Aplicando:

#### 5 mV: 50,14 mV
#### 50 mV: 500,14 mV
#### 200 mV: 2,00 V
#### 500 mV: 2,38 V 
#### Calculando o erro percentual com relação ao ganho de 10V/V, temos:

#### 5 mV: 0,27 %
#### 50 mV: 0,027 %
#### 200 mV: 0,003 %
#### 500 mV: Houve saturação.
#### Podemos perceber que o AmpOp AD8539 apresenta uma faixa de erro muito menor quando aplicado com tensões de entrada mais baixas, em comparação ao AmpOp AD8040.
### Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta.
#### Para esse caso seria melhor utilizar o AmpOp AD8539, pois, esse dispositivo apresentou uma faixa de erro muito menor quando aplicado com tensóes de entrada mais baixas.









