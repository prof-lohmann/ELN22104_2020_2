Curso Superior em Engenharia Eletrônica 
Unidade Curricular: Eletrônica I
Professor: Daniel Lohmann
Aluno: Ramon Busiquia Serafim

# Atividade 03



Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.



## 1) Verifique no datasheet dos ampops indicados os valores dos itens abaixo:



### AmpOp AD8040

- Máxima e mínima tensão de alimentação: de +2,7 a +12V

- Tensão de modo comum: de +0,2 a +5,2 V 

- CMRR Vcm: de -4,5 a +3 V 

- Máxima e mínima tensão de entrada: 200 mV acima ou abaixo de Vc

- Tensão de offset: 6 mV 

- Corrente de polarização: de +0,7 a -1,5 uA

- Consumo de corrente: 1,3 mA 

- Ganho de malha aberta: de -4 a +4 V

- Impedância de entrada: 6 Mohm e 2 pF



### AmpOp AD8539

- Máxima e mínima tensão de alimentação: 1,35V a 2,5V
- Tensão de modo comum: de 0 a a +5V
- CMRR Vcm: de 0 a +5V
- Máxima e mínima tensão de entrada: de 0 a 4,8V
- Tensão de offset: 15uV
- Corrente de polarização: de 25pA a 60pA
- Consumo de corrente: 180uA
- Ganho em malha aberta: de +0,1V a +7V
- Impedância de entrada: 10KOhm e 300pF



## 2) Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada. Utilize um sinal senoidal de 1kHz. Quais os valores das tensões de saturação?



### AmpOp AD8040


<img  src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8040%201.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8040%201.PNG?raw=true">




Observando o gráfico de saída, o AmpOp não saturou pois atingiu +2V e -2V.



### AmpOp AD8539


<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8539%201.PNG?raw=true">




<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8539%201.PNG?raw=true">




Observando o gráfico de saída, o AmpOp saturou. Como a tensão de alimentação está limitada a 2.5V e utilizando um sinal senoidal de 3V, após o valor de 2.5V o AmpOp satura.



## 3) Simule um circuito amplificador inversor com cada um dos AmpOps indicados e calcule os resistores para ter um ganho igual a -100V/V. Aplique 0V na entrada e verifique o resultado. Aplique um sinal senoidal de 10mVPP @1kHz e explique o resultado.



### AmpOp AD8040


<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8040%202.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8040%202%20offset.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8040%202%20ganho.PNG?raw=true">




### AmpOp AD8539


<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8539%202.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8539%20%202%20offset.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8539%20%202%20ganho.PNG?raw=true">




## 4) Simule um circuito amplificador não inversor com cada um dos AmpOps indicados e calcule os resistores para ter um ganho igual a 10V/V. Aplique 0V na entrada e verifique o resultado. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.



### AmpOp AD8040


<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8040%203.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8040%203%20offset.PNG?raw=true">



Colocando 0V na entrada, verificamos uma tensão de offset de -15.296mV. Aplicando os valores de sinais pedidos obtemos: 



5mV: 34.699mV

50mV: 484.665mV

200mV: 1.984V

500mV: 4.966V




Erro percentual com relação ao ganho calculado:



5mV: 30.66%

50mV: 3.06%

200mV: 0.8%

500mV: 0.68%


### AmpOp AD8539


<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Esquematico%20AD8539%203.PNG?raw=true">



<img src="https://github.com/RamonSerafim/ELN22104_2020_2/blob/patch-1/Ramon_Serafim/Atividade_3/Vout%20AD8539%203%20offset.PNG?raw=true">




Colocando 0V na entrada, verificamos uma tensão de offset de 137.296uV. Aplicando os valores de sinais pedidos obtemos:



5mV: 50.137mV

50mV: 500.136mV

200mV: 2.000V

500mV: 2.476V




Erro percentual com relação ao ganho calculado:



5mV: 0.27%

50mV: 0.03%

200mV: 0% 

500mV: 50.48%




## Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops você utilizaria? Justifique a sua resposta. 



Utilizaria o AD8539. Possui um offset baixo, com sinais pequenos obtem-se mais próximo do resultado esperado.



## Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação como subtrator.



Escolheria o INA592. Para aplicação como subtrator é preferivel escolher um AmpOP de alta precisão.



