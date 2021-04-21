![logo_ifsc](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/logo_ifsc.jpg)

# ATIVIDADE_02
## Aluno: Marcos Paulo Pacheco
### Resumo sobre Amplificadores Operacionais.

Atenção: Toda documentação deve ser feita em MARKDOWN no GIT.

a) Faça um resumo em forma de tutorial sobre o os Amplificadores Operacionais. Este
resumo deve responder as seguintes perguntas:

>>1. O que é o AmpOp?\
	O amplificador operacional (AmpOp), é um circuito integrado (CI) composto por componentes semicondutores, capaz de amplificar um sinal de entrada, sendo capaz de realizar operações de soma, subtração, derivação, integração e multiplicação.
	Os AmpOps internamente são constituídos com um grande número (dezenas) de transistores, resistores e (normalmente) tem também um capacitor interno.

>>2. Mostre os símbolos e as características do AmpOp IDEAL?
Abaixo alguns símbolos do AmpOp:
- Símbolo clássico (mais básico) do AmpOp com apenas 3 terminais\
![Atividade 02-2a](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-2a.jpg)\
- Símbolo do AmpOp conectado à fonte de alimentação CC simétrica (5 terminais)\
A estrutura de um amplificador operacional é simples, pois ele possui dois terminais de entrada, denominados por terminal inversor, identificado pelo sinal negativo (-), o terminal não inversor, identificado por um sinal positivo (+) e um terminal de saída, além de outros dois terminais de alimentação positiva (+Vcc) e outro de alimentação negativa (-Vcc).\
![Atividade 02-2b](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-2b.jpg)\
 - Circuito equivalente do AmpOp ideal\
![Atividade 02-2c](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-2c.jpg)\
- Características do AmpOp ideal:\
-- Impedância de entrada infinita;\
-- Impedância de saída nula;\
-- Ganho de modo comum nulo ou, equivalentemente, rejeição de modo comum infinita;\
-- Ganho de malha aberta infinito;\
-- Largura de faixa de resposta em frequência infinita;\
-- Insensibilidade à temperatura.


>>3. O que significa Malha Aberta e Malha Fechada?\
Malha Aberta ou sem realimentação: tipo de configuração muito útil quando se utiliza circuitos comparadores. O ganho nessa configuração apresenta um valor muito alto, teoricamente infinito.\
![Atividade 02-3a](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-3a.jpg)\
Malha Fechada - este tipo de configuração pode ser classificado em dois tipos:\
Realimentação positiva: quando a porta não inversora é alimentada pelo sinal de entrada e a porta inversora é aterrada. Esse tipo de circuito pode apresentar uma certa instabilidade. Uma aplicação prática deste tipo de configuração é a dos circuitos osciladores.\
![Atividade 02-3b](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-3b.jpg)\
Realimentação negativa: quando a porta inversora é alimentada pelo sinal de entrada e a porta não inversora é aterrada. Este modo de configuração é o mais comum em circuitos que utilizam AmpOps, apresentando uma resposta linear e ganho controlado.\
![Atividade 02-3c](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-3c.jpg)\
 
>>4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.\
![Atividade 02-3c](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-4.jpg)\
-Circuito em malha fechada através de Rf com realimentação na entrada inversora.\
-Ganho em malha fechada pela equação de saída: G=Vo/Vi=-Rf/R1\
-Supor que ganho de malha aberta [A] ≠ ∞\
-Vi de entrada nos terminais do AmpOp: Vi=Vo/A\
-Observar que a entrada positiva (+) está aterrada, então:Vi-=-Vo/A;\ 
-A corrente i1 pode ser assim definida: i1=[(vi-(-Vo/A))/R1] = ((Vi+Vo/A)/R1)\
-Considerando a impedância de entrada infinita do AmpOp, força a corrente i1 circular totalmente através de Rf\
-A tensão de saída pode ser calculada da seguinte forma:\ 
-Vo= -Vo/A-i1.R2= -Vo/A-((Vi+Vo/A)/R1).Rf\
-Rearranjando matematicamente o ganho em malha fechada [G] é dado como:\
-G≡Vo/Vi=((-Rf)/R1)/(1+((1+Rf/R1))/A)\
-Observar que o valor de A se próxima de ∞ e o valor de G se aproxima de um valor ideal -Rf/R1\


5. Descreva as principais características das topologias:
a) Seguidor de Tensão (Buffer): Este tipo de configuração a tensão de saída é igual a da entrada, porém, com impedâncias de entrada e saída, muito alta e baixa, respectivamente. Este tipo de circuito é muito comum em instrumentação eletrônica. Além das características já descritas, esse tipo de configuração apresenta:
	Ganho unitário;
	O sinal da saída, possui mesma polaridade e fase do sinal de entrada;
	Atua como circuito isolador de estágios;
	Casador de impedâncias.
 ![Atividade 02-5a](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5a.jpg)

	V"- = V0 = V" 1
	V"0"=V"1" 
b) Amplificador Inversor: configuração de ganho constante. A saída é obtida pela multiplicação da entrada por um ganho (G) constante, fixados pelo valor que o resistor R1 e o resistor de realimentação Rf impõem ao circuito.  Outra característica também, seria a inversão do sinal de saída em relação ao da entrada.
![Atividade 02-5b](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5b.jpg)


 


c) Amplificador Não Inversor: este tipo de configuração com o uso de AmpOp também é conhecido como multiplicador de ganho constante. Observa-se pela fórmula demonstrada a seguir que a fase da saída é a mesma que a da entrada.
![Atividade 02-5c](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5c.jpg)


d) Amplificador Somador Inversor: neste caso há uma soma das contribuições do sinal de cada entrada (n entradas) para o valor final de saída, ou seja, cada entrada é multiplicada por um fator de ganho constante, observando ainda que pela formulação demonstrada, o sinal de tensão da saída sofre inversão de fase. 
![Atividade 02-5d](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5d.jpg)
 



e) Amplificador Somador Não Inversor: neste caso há uma soma das contribuições do sinal de cada entrada (n entradas) para o valor final de saída, ou seja, cada entrada é multiplicada por um fator de ganho constante, observando ainda que pela formulação demonstrada, o sinal de tensão da saída não sofre inversão de fase. 
![Atividade 02-5e](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5e.jpg)



f) Subtrator: este circuito também é conhecido como amplificador diferencial, pois o sinal de saída é resultante da diferença (subtração) dos sinais de entrada, multiplicados pelo fator de ganho (G).
![Atividade 02-5f](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5f.jpg)
 

g) Amplificador de Instrumentação: esta configuração é constituída por dois amplificadores não inversores em cada entrada de um amplificador subtrator. Neste circuito, a resistência de entrada vista por cada umas das duas fontes é infinita, e o ganho de tensão será dado pelo produto de dois quocientes entre as resistências.
![Atividade 02-5g](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-5g.jpg)
 

	R3 = R1
	R4 = R2
	Sinal da saída: V_(0 )=  R_2/R_1 .(1+(2.R_3)/R).(V_2-V_1 )




>> 6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias\
Amplificador Inversor e Amplificador não inversor.\
a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V\
e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação
com erros percentuais e utilize uma variação de ganho em malha aberta entre
120dB e 20dB.\
b) Dica veja o problema 2.20 pg 83 do livro texto.
	


7. Explique o que é a tensão de modo comum (VCM) e quais os efeitos desta tensão nas
topologias estudadas.
Tensão de modo comum é a tensão média nos terminais de entrada do AmpOp, tanto da porta inversora como a não-inversora, provocando uma alteração no nível tensão de saída do amplificador. Assim:
	Tensão de modo comum [Vcm] = ((V_(i+)  + V_(i-)))/2
	Ganho de modo comum [Acm]
	Ganho da diferença dos sinais [Ad]
	Tensão de saída: V_o=(Ad .V_i )+(Acm .Vcm)

8. O que é CMRR?
Sigla da língua inglesa Common Mode Rejection Rate (relação da Rejeição de modo comum) - É a eficácia de um amplificador diferencial, em relação ao grau de rejeição a sinais de modo comum em detrimento a sinais diferenciais. PODE SER CALCULADO DA SEGUINTE FORMA: 
	CMRR = 20.log.|Avd/Avcm|(dB)
	Avd = ganho diferencial (dado do fabricante);
	Avcm = ganho em modo comum.


9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão
de modo comum (VCM), indicando:

a) o impacto na tensão de saída com relação a tolerância dos resistores no
circuito;
b) Qual erro na tensão de saída com relação CMRR do AmpOp.
c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça
o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.

10. Faça um resumo explicando as limitações de tensão de entrada e saída de um
AmpOp. De exemplos, utiliza-se valores de datasheet.


a) Defina o que é um AmpOp Rail-to-rail.
É um Amplificador Operacional cuja tensão na saída alcança o mesmo nível que as tensões de alimentação do AmpOp, ou seja, apresentam alimentação dupla e simétrica, com +VCC na alimentação positiva e -VCC na alimentação negativa. Por exemplo, um amplificador operacional com entrada e saída Rail to Rail alimentado com 5V pode aceitar sinais de até 5Vpp na entrada sem saturar e dar o mesmo sinal de 5Vpp na saída, é como se ele tivesse um controle de ganho automático integrado.


>> 11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de
um amplificador inversor?\
Tensão de offset é um deslocamento no nível CC do sinal de saída, e nos casos de se estar trabalhando com tensão CA, este deslocamento, associado com o sinal de entrada amplificada (pelo ganho G), pode levar o AmpOp à saturação. Esse fenômeno ocorre principalmente pelas não idealidades dos componentes reais, como por exemplo, um casamento de impedância não ideal dos dispositivos de entrada. Uma forma de se calcular o resultado na tensão de saída de um amplificador inversor, seria aterrar a entrada e verificar a tensão de offset na saída (multiplicada pelo ganho G) com polaridade invertida àquela que a originou.

>> 12. Como minimizar o efeito da tensão de offset?\
Alguns AmpOps, possuem dois terminais adicionais, onde um circuito pode ser implementado a fim de zerar a tensão CC de saída devido a tensão de offset. Por exemplo, um potenciômetro pode ser conectado entre os terminais de anulação de offset e o terminal central do potenciômetro é conectado na fonte de alimentação negativa do AmpOp. Movendo-se o terminal central do potenciômetro pode-se contrabalancear a assimetria presente no circuito interno do AmpOp que deu origem à tensão de offset, ainda pode-se acoplar um capacitor na entrada para diminuir esses efeitos indesejados.
![Atividade 02-12](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-12.jpg)
 

>> 13. O que é a variação da tensão de offset pela temperatura?\
A tensão de offset de entrada (Vos) é provocada pelo desequilíbrio das não idealidades presente no estágio diferencial da entrada (circuito interno do AmpOp), ocasionando descasamento de impedâncias, que é influenciado também pela operação do componente fora, principalmente, dos intervalos de temperatura em que esse é projetado (acima ou abaixo).\
a) Como verificar esse parâmetro no datasheet?\
Para a verificação do parâmetro de tensão de offset influenciado pela temperatura num datasheet de um componente real, escolheu-se um AmpOp da empresa Texas Instrument. Essa caraterística pode ser verificada na linha indicada na figura a seguir:\
![Atividade 02-13](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-13.jpg)
 
>> 14. O que são as correntes de polarização (Ibias) de AmpOp?
Corrente de polarização (Ibias) é o valor médio entre as duas correntes de polarização de cada entrada (IB1  e IB2), a saber:\
	Ibias = (IB1  + IB2) / 2
a) Como minimizar o efeito destas correntes? Descreva as aproximações e os
possíveis circuitos para mitigar o problema.\
Para minimizar o efeito das correntes de polarização de entrada, deve-se colocar na entrada não inversora uma resistência igual ao valor da resistência CC vista pelo terminal inversor.\
![Atividade 02-14](https://github.com/MPP13/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcos_Pacheco/Atividade%2002/Figuras_atividade_02/Atividade%2002-14.jpg)
b) Descreva a corrente de offset na polarização dos AmpOp.
As correntes de offset são a diferença entre as correntes de polarização de entrada, sendo assim definidas:
	IB1 – corrente de polarização na entrada 1
	IB2 – corrente de polarização na entrada 2
	Corrente de entrada de offset = IOS = | IB1 - IB2|

>> REFERÊNCIAS UTILIZADAS NA PESQUISA PARA ELABORAÇÃO DESTE TRABALHO
https://slideplayer.com.br/slide/1749154/
https://www.feg.unesp.br/Home/PaginasPessoais/ProfMarceloWendling/3---amplificadores-operacionais-v2.0.pdf
https://wiki.sj.ifsc.edu.br/images/8/82/2_Ampop.pdf
http://professorpetry.com.br/Ensino/Repositorio/Docencia_CEFET/Osciladores_Multivibradores/2012_2/Anexo_II.pdf
http://www.ufrgs.br/eng04030/Aulas/teoria/cap_15/circampo.htm
http://www.peb.ufrj.br/cursos/cob785/COB785_AmpOp.pdf
https://www.ti.com/document-viewer/TLV9061-Q1/datasheet/GUID-F393C1A1-5A5C-4088-A879-DAA9ADF09031#TITLE-SBOS966SBOS5638953
https://www.
