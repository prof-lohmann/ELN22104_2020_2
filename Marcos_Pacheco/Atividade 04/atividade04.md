![logo_ifsc]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/logo_ifsc.jpg)

# Objetivos: Integração dos blocos de uma fonte linear

## Introdução: Neste roteiro iremos integrar os circuitos estudados anteriormente, para isso, revise os conceitos de reguladores LDO.

### Parte 01: 

>> 1 - Entendendo um regulador linear\
OBS: Para a parte introdutória teórica, será utilizado como base o livro texto SEDRA 5ª EDIÇÃO – CAP 3 - DIODOS\
Conceitos importantes:\
• Princípios de regulação de tensão: (páginas 101 e 102) Um regulador de tensão é um circuito cujo objetivo é proporcionar uma tensão CC constante em seus terminais de saída. Exige-se que a tensão de saída seja mantida constante apesar:\
     -	Das variações na corrente da carga drenada dos terminais de saída do regulador, e;\
     -	Das varrições na tensão CC da fonte de alimentação que alimenta o circuito regulador\
• Tensão de saída e tensão de ripple:\
     -  Tensão de saída: É a tensão, ou faixa de tensões, que um regulador fornece em sua saída se a tensão de entrada estiver dentro dos parâmetros aceitáveis.\
     -  Tensão de ripple: (página 111) é uma ondulação de tensão fornecida pela fonte, que é dependente do valor da capacitância do capacitor (cuja função, no filtro, é manter a forma de onde de saída o mais próximo de uma tensão CC) e da corrente consumida pela carga. Essa ondulação (ripple) surge após a retificação na saída da etapa do filtro. 
![figura01]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura01.jpg)\
• Regulação de linha: (página 105) é definido como a relação entre a variação da tensão de saída com a tensão de entrada.
![figura02]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura02.jpg)\
• Regulação de Carga: (página 105) é definido como a relação entre a variação da tensão de saída com a variação da corrente consumida pela carga.\
![figura03]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura03.jpg)\
• Conceito de LDO – Low Dropout Voltage: é a diferença entre a tensão de saída nominal e a menor tensão de entrada necessária para que o regulador funcione adequadamente. Valores típicos:\
    -	LDO (low) = VDO < 0,6 V;\
    -	HDO (high) = VDO > 0,6 V.\
O valor de VDO (dropout voltage) pode ser assim definido:\
![figura04](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura04.jpg)

>> 2 - Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema:
![figura05]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura05.jpg)\
a)	Qual relação entre a tensão de alimentação do ampop e a tensão de saída?\
A tensão de saída (Vout) estará limitada pelo valor de alimentação do próprio AmpOp. Deve-se ficar atento também, às próprias restrições de alimentação do AmpOp,
uma vez que o respectivo valor de saída irá saturar quando essa tensão se aproximar daquele valor de alimentação. Deve-se levar em consideração no projeto, ainda, 
os efeitos que o sinal de offset pode provocar no sinal de saída do AmpOp para não se ter problemas com esse efeito. Assim, é necessária uma análise criteriosa do 
datasheet do componente.\
b)  O que devemos considerar para esse circuito operar como um LDO?\
Na entrada não inversora do AmpOp tem-se conectado o diodo D3 (zener) que irá limitar esse sinal (V_in). Já a saída (Vout)  está limitada pelos valores de sua própria 
alimentação do AmpOp (para não saturar o sinal) e com os respectivos limites de saída que devem ser observados.\
c)	Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?\
Primeiramente analisar quais restrições de alimentação que o AmpOp a ser escolhido apresenta (estudo de datasheet), em relação às tensões de alimentação, a fim de que 
o sinal de saída do mesmo não sature. Observar também que o sinal Vout além da influência do próprio AmpOp, tem àquela provocada pela tensão de saída do NMOS, ou seja, 
o valor de VGS (tensão gate-source).

>> 3 - Circuito proposto (01) para a alimentação do AmpOp:
![figura06]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura06.jpg)\
a)	Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?\
•	Considerando a queda de tensão nos diodos D4 e D5, em 0,7 V, cada componente (atentar ao valor de rms)
![figura07]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura07.jpg)\
b)	Quais problemas apresentam esse circuito? \
No circuito apresentado tem-se dois capacitores indicados, C2 e C3. Assim a escolha de seus respectivos valores, deve-se levar em consideração os efeitos de ripple que irá ser inserido no sinal da tensão. Ainda, conforme calculado anteriormente o circuito é um dobrador de tensão, ou seja, pequenas variações do sinal de entrada Vin, pode provocar efeitos graves no funcionamento do AmpOp, pois esse mesmo sinal será aplicado no VCC do AmpOp (podendo saturar o sinal saída ou mesmo danificá-lo permanentemente).\
c)	Podemos melhorar?\
Pode-se melhor o circuito exposto, considerando o já observado no item anterior, através do adequado dimensionamento dos capacitores (C2 e C3), a fim de diminuir os efeitos de ripple, e, com a inserção de um regulador linear de tensão na da saída do circuito dobrador de tensão que por sua vez é a própria alimentação VCC do AmpOp.

>> 4 - Circuito proposto (02) para a alimentação do AmpOp:
![figura08]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura08.jpg)\
Vamos projetar esse circuito de alimentação do AmpOp?\
Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, Vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V. Pontos Importantes para iniciar o projeto responda justificando as escolhas.\
• Qual a Tensão VGS? Descreva como obter o valor.\
Datasheet usado: (https://www.vishay.com/docs/91021/91021.pdf)
![figura09]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura09.jpg)\
Pelo gráfico acima disponibilizado no datasheet do componente, a tensão VGS para uma corrente Iout de 1 A, indica uma tensão VGS = 4,5 V.\
• Qual a corrente de alimentação do AmpOp?\
Datasheet usado: (https://www.mouser.com/datasheet/2/149/LM324-195664.pdf)
![figura10]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura10.jpg)\
Corrente de alimentação, ICC_min = 1,0 mA e ICC_max = 3,0 mA\
• Qual a tensão de alimentação do AmpOP?\
![figura11](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura11.jpg)\
Pelo datasheet a tensão VCC_MAX = 32 V.\
Por uma análise rápida, a tensão Vout = 15 V (dado de projeto), a tensão VGS = 4,5 V (dado do datasheet), fazendo uma análise reversa partindo do sinal da saída:\
![figura12]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura12.jpg)\
• Qual fator devo considerar para escolher o transistor Q1?\
O valor de Q1 (NPN) deve ter um β(beta) bastante elevado. Observa-se que na base do Q1 tem o diodo D6 (zener), fato que ratifica o já elencado, pois o β tem que ser alto o suficiente para que a corrente de base de Q1 seja suficientemente menor que a corrente de D6.\
• Qual valor da tensão do diodo zener D6?\
Considerando o valor de saída do AmpOp, foi estimado em Vo_ampop =  20,0 V, Vripple_pós_retificador = 1V, e que a queda de tensão em cada um dos diodos (incluindo o zener) Vdiodo = 0,7 V (x3), estima-se um valor de tensão para o diodo zener D6 de:\
![figura13]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura13.jpg)\
• Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?\
Para se maximizar a eficiência energética e minimizar os ruídos do circuito, deve-se escolher um diodo zener com uma resistência interna baixa, pois assim, o 
sistema tenderá a ter uma maior estabilidade.\
• Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?
Projete o circuito de alimentação do AmpOp com as especificações acima.\\\\\\\\\\\\\\\\



### REFERÊNCIAS
https://www.embarcados.com.br/aprenda-a-analisar-o-ripple-da-sua-fonte/#:~:text=Uma%20fonte%20de%20alimenta%C3%A7%C3%A3o%20do,n%C3%ADvel%20DC%2C%20conhecida%20como%20ripple.&text=Calcula%2Dse%20tamb%C3%A9m%20o%20fator,sa%C3%ADda%20e%20o%20valor%20DC.

https://sites.unipampa.edu.br/gama/files/2019/07/matheuscortez-2017.pdf

http://repositorio.unicamp.br/jspui/bitstream/REPOSIP/261542/1/Pelicia_MarcosMauricio_M.pdf








