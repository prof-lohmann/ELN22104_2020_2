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
	E, quando inserido um sinal de entrada de 2,6 V de pico, na saída o sinal se apresentou saturado em torno de 2,5 V.\


