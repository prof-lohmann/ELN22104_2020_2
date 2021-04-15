![logo_ifsc]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/logo_ifsc.jpg)


# SIMULAÇÃO DE CIRCUITOS COM AMPLIFICADORES OPERACIONAIS AD8040 E AD8539.
>> 1. Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:\
◦ Máxima e mínima tensão de alimentação;\
◦ Tensão de modo comum;\
◦ CMRR;\
◦ Máxima e mínima tensão de entrada;\
◦ Tensão de offset;\
◦ Corrente de polarização;\
◦ Consumo de corrente;\
◦ Ganho em malha aberta;\
◦ Impedância de entrada;\
Conforme requerido, a seguir estão dispostos os valores dos parâmetros de datasheet solicitados para a pesquisa, 
relacionados ao AmpOp AD 8040 e AD8539, considerando indicação na Tabela 1:
![figura01](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2001.jpg)

## PARA TODAS AS SIMULAÇÕES ABAIXO UTILIZE A ALIMENTAÇÃO SIMÉTRICA RECOMENDADA NO DATASHEET.

>> 2. Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.\
2.1. Dica utilize um sinal senoidal de 1kHz para auxiliar na visualização.\
2.2. Responda quais os valores das tensões de saturação?\
•	AMPOP AD8040\
	Conforme especificações do AmPop AD8040 (data sheet), circuito foi simulado com Vin = 5 Vpico senoidal na entrada não-versora (10 V pico a pico de sinal de entrada e alimentação simétrica de VCC1 = +5V e VEE1 = -5V) com 1 KHz de frequência.\
	O gráfico do sinal de saída encontra-se fase com sinal de entrada e mesmos valores de pico (num primeiro momento de análise), demonstrando o funcionamento do circuito como “seguidor de tensão”.\
![figura02]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2002.jpg)\
A fim de se observar o valor de saturação do sinal de saída, inseriu-se 6 V (pico) no sinal de entrada. Assim, foi possível observar aquele efeito graficamente no sinal de saída de forma bastante pronunciada. Ora, se o circuito projetado era um “seguidor de tensão”, o sinal de saída deveria ser igual ao sinal de entrada, fato que não foi observado, corroborando assim com a saturação do sinal em torno dos 5V.\
![figura03]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2003.jpg)\
	Na primeira simulação, em princípio se observou que o sinal de saída era de mesma amplitude do sinal de entrada, porém, através da própria simulação, foram feitas algumas medições, comprovando que essa conclusão não era totalmente verdadeira, sendo possível verificar o efeito do offset já no sinal de entrada. A tabela abaixo resume o exposto nesse parágrafo:\
![figura04]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2004.jpg)\
Pela análise da Tabela 2, percebe-se que o offset de entrada em torno de 2 mV está dentro do especificado no datasheet (Tabela 1) que é de no máximo 6 mV.\
•	AMPOP AD8539\
	Através das especificações do AmPop AD8539 (datasheet), o circuito foi simulado com Vin = 2,5 V pico senoidal na entrada não inversa (5 V pico a pico de sinal de entrada e alimentação simétrica de VCC1 = +2,5V e VEE1 = -2,5V) com 1 KHz de frequência.\
	O gráfico do sinal de saída encontra-se fase com sinal de entrada, porém, conforme observado na simulação anterior com o AmPop AD8040, é provável que o sinal de saída (amplificado pelo próprio ganho do AmPop), bem como o sinal de entrada, já apresentem um sinal de offset em relação ao sinal inserido pela fonte Vin.\
![figura05]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2005.jpg)\
Como na simulação anterior, a fim de se observar o valor de saturação no sinal de saída, inseriu-se um sinal de 2,6 V(pico) no sinal de entrada. Assim, foi possível observar aquele efeito graficamente no sinal de saída de forma bastante pronunciada.\
![figura06]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2006.jpg)\
A tabela abaixo, resume de forma detalhada, os valores medidos na simulação.\
![figura07]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2007.jpg)\
	Nessa simulação com o AmPop AD 8539, não foi observado um valor de offset já no sinal de entrada, o que já era esperado pela própria análise do datasheet antecipadamente (Vcm = 2,50 V)= 5 à 15 [µV] de offset), ou seja, seria um valor muito pequeno e que talvez a própria precisão do software utilizado não foi capaz de se sensibilizar àquela presença. Porém, observa-se o efeito do offset no sinal da saída amplificada pelo ganho do próprio AmpOp.\
	E, quando inserido um sinal de entrada de 2,6 V de pico, na saída o sinal se apresentou saturado em torno de 2,5 V.

>> 3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os resistores para ter um ganho igual -100V/V.\
Diante aos quesitos de simulação, antes da realização das primeiras observações, foi necessário calcular os resistores R1 e Rf (resistor de realimentação). A seguir será demonstrado o desenvolvimento dos equacionamentos:\
![figura08]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2008.jpg)\
Pelo demonstrado na Tabela anterior, o valor de Rf é 100 vezes maior que o valor de R1, então para facilitação das demais análises, se escolheu o valor de R1 = 1 KΩ e consequentemente o Rf = 100 kΩ.\
3.1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.\
•	AMPOP AD8040\
	Conforme solicitado, foi aplicado 0 V no sinal de entrada e os seguintes gráficos foram obtidos através da simulação do circuito em estudo:\
![figura09]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2009.jpg)\
	Verifica-se através do gráfico do sinal de saída [Vout], a interferência do offset de entrada amplificado pelo ganho [G] do AmpOp. O sinal encontrado foi de -169,899 mV, aproximadamente.\
	Conforme já dito, o valor do Vout é o próprio sinal de offset de entrada amplificado 100 vezes, ou seja, seu valor ainda no sinal de entrada Vin é de aproximadamente 1,699 mV (praticamente o mesmo valor encontrado na primeira parte do trabalho e discriminado na Tabela 2)\
•	AMPOP AD8539\
	Conforme solicitado, foi aplicado 0 V no sinal de entrada e os seguintes gráficos foram obtidos através da simulação do circuito em estudo:\
![figura10]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2010.jpg)\
Verifica-se através do gráfico do sinal de saída [Vout], a interferência do offset de entrada amplificado pelo ganho [G] do AmpOp. O sinal encontrado foi de 1,3866 mV, aproximadamente.\
	Conforme já dito, o valor do Vout é o próprio sinal de offset de entrada amplificado 100 vezes, ou seja, seu valor ainda no sinal de entrada Vin é de aproximadamente 13,866 µV, corroborando com a primeira análise de data sheet do componente, discriminado na Tabela 1 ( offset em Vcm (2,50 V) = 5 à 15 [µV] ).\
	3.2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída. Explique o resultado.\
•	AMPOP AD8040\
	Continuando com o solicitado, foi inserido um valor de 10 mVpp na entrada e os seguintes gráficos foram obtidos:\
![figura11]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2011.jpg)\
A primeira observação a se fazer é a inversão de fase do sinal de saída, provocada pelo ganho negativo imposto pelo quesito de análise, ainda, o sinal encontra-se deslocado em relação a simetria inicial em comparação ao eixo vertical [mV]. Para ilustrar melhor os dados obtidos, os mesmos podem ser observados na Tabela 5.\
![figura12]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2012.jpg)\
	Esta análise evidencia ainda mais a influência do offset em circuitos com AmpOp.\
•	AMPOP AD8539\
	Continuando com o solicitado, foi inserido um valor de 10 mVpp na entrada e os seguintes gráficos foram obtidos:\
![figura13]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2013.jpg)\
A mesma observação ocorreu no AD8539 em relação a inversão de fase que já foi comentada no AD8040, porém agora não houve deslocamento do sinal em relação a simetria inicial em comparação ao eixo vertical [mV]. Para ilustrar melhor os dados obtidos, os mesmos podem ser observados na Tabela 6.\
![figura14]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2014.jpg)\

	
>> 4. Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule
os resistores para ter um ganho igual 10V/V.\
	Diante aos quesitos de simulação, antes da realização das primeiras observações, foi necessário calcular os resistores R1 e Rf (resistor de realimentação), conforme já realizado também, no item anterior. A seguir será demonstrado o desenvolvimento dos equacionamentos:\
![figura15]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2015.jpg)\
	Pelo demonstrado na Tabela anterior, o valor de Rf é 9 vezes maior que o valor de R1, então para facilitação das demais análises, se escolheu o valor de R1 = 1 KΩ e consequentemente o Rf = 9 kΩ.\ 
	4.1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.\
•	AMPOP AD8040\
	Conforme solicitado, foi aplicado 0 V no sinal de entrada e os seguintes gráficos foram obtidos através da simulação do circuito em estudo:\
![figura16]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2016.jpg)\
	O circuito em estudo está apresentando um ganho [G] em malha fechada de 10 V/V (conforme quesito de análise). O valor de saída foi avaliado na simulação em Vout = -15,296 mV. Aquela saída apresentou o sinal amplificado do próprio offset do sinal de entrada.\ 
	O sinal de offset pode ser afetado por duas condições de circuitos, independentes, que pode ser pela própria tensão de offset de entrada (conforme já verificado nas outras análises) ou por uma corrente de offset que ocorre devida à diferença nas correntes resultas nas entradas inversora e não inversora, provada pelo desbalanceamento entre os transistores de entrada. Como uma das entradas estava aterrada e a outra estava com sinal de entrada em 0 V, o sinal de offset resultou num valor negativo, fato que pode ser observado no circuito em estudo.\
•	AMPOP AD8539\
	Conforme solicitado, foi aplicado 0 V no sinal de entrada não inversora e os seguintes gráficos foram obtidos através da simulação do circuito em estudo:\
![figura17]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2017.jpg)\
Através da análise do gráfico da saída Vout = 137,2956 µV, percebe-se mais uma que esse valor apresentado, é o próprio offset de entrada amplificado pelo ganho em malha fechada de fator G=10 V/V. Com o auxílio da Tabela 1, pode-se verificar que aquele sinal de entrada na configuração desse  circuito com alimentação simétrica de +/- 2,5 V, pode apresentar um offset de 5 à 15 [µV], comprovando que o sinal de saída obtido e observado está dentro daquele intervalo  do sinal de entrada de offset, porém, amplificado pelo próprio ganho [G] do AmpOp.\
4.2. Aplique um sinal contínuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal
de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.\
	Na figura a seguir, encontram-se todas as simulações realizadas com os valores de sinal contínuo (CC), conforme requerido:\
![figura18]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2018.jpg)\
![figura19]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2019.jpg)\
	A Tabela 8, expõe os erros percentuais dos valores de saída [Vout] medidos durante as simulações, com aqueles esperados, ou seja, sinal de entrada amplificado integralmente pelo ganho [G]:\
![figura20]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2003/figuras_atividade_03/figura%2020.jpg)\
	Na análise dos erros percentuais do sinal de saída [Vout] para o AmpOp AD8040, percebe-se que aqueles são bem mais significativos quando são aplicados sinais de entrada de baixa tensão, isso deve ao fato de que esse componente, segundo catálogo do fabricante e conforme analisado em tópicos anteriores, apresentar um offset na ordem de 10-3 [mV].\ 
	Assim, dependendo do ganho do amplificador em uso, esse erro percentual, pode inviabilizar totalmente o uso de determinado componente, por isso, o estudo prévio sobre as características de cada AmpOp, antes de sua respectiva implementação em quaisquer circuitos, é de extrema importância.\
	Por outro lado, o AmpOp AD8539, apresentou valores bem menores em relação ao erro percentual, quando são aplicados valores de entrada de baixa tensão. Somente quando se aplicou um sinal de entrada tal, que fez o componente operar na faixa de saturação, o erro foi bem mais pronunciado.















