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
• Regulação de Carga: (página 105) é definido como a relação entre a variação da tensão de saída com a variação da corrente consumida pela carga.
![figura03]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura03.jpg)\
• Conceito de LDO – Low Dropout Voltage: é a diferença entre a tensão de saída nominal e a menor tensão de entrada necessária para que o regulador funcione adequadamente. Valores típicos:\
    -	LDO (low) = VDO < 0,6 V;\
    -	HDO (high) = VDO > 0,6 V.\
O valor de VDO (dropout voltage) pode ser assim definido:\
![figura04]( https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2004/figuras_atividade_04/figura04.jpg)\

>> 2 - Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema:\ 
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
o valor de VGS (tensão gate-source).\

