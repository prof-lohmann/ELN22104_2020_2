# ATIVIDADE 2
### QUESTÃO 01) O que é o AmpOp?
- Os amplificadores operacionais são circuitos integrados capazes de amplificar um sinal de entrada e também realizar operações matemáticas como soma, subtração, integração, derivação e multiplicação.
### QUESTÃO 02) Mostre os símbolos e as características do AmpOp IDEAL?
![ampop](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/ampop.png)
- Impedância de entrada infinita;
- Ganho em malha aberta infinito;
- Frequência de ganho unitário infinito;
- Impedância de saída nula;
### QUESTÃO 03) O que significa malha aberta e malha fechada?
-Malha aberta no AmpOp se trata de uma operação sem a realimentação da saída para a entrada do AmpOp.Ou seja,o ganho do amplificador é estipulado pelo próprio fabricante , não se tem controle sobre o mesmo. Malha fechada no AmpOp se trata de uma operação que tem o caminho da realimentação negativa da saída para a entrada, o que acarreta na condução do amplificador à instabilidade.
### QUESTÃO 04) Exemplifique como resolver e calcular circuitos com AmpOps em malha fechada.
![malha fechada](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/malha%20fechada.png)
### QUESTÃO 05) Descreva as principais características da topologias:
#### a) Seguidor de Tensão (Buffer);
![buffer](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/buffer.png)
- O buffer é um amplicador que não gera nenhuma amplificação do sinal de entrada na saída. Ou seja, o ganho de tensão é 1. 
#### b) Amplificador Inversor;
![inversor](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/inversor.png)
- O amplificador inversor é um AmpOp com dois resistores de realimentação, sendo VI a tensão de entrada e VO a tensão de saída do amplificador.O resistor R1 liga a tensão de entrada VI ao terminal inversor VN. O resistor de realimentação RF liga o terminal inversor VN ao terminal de saída VO. O terminal não-inversor VP é ligado ao terra (GND).Este amplificador é chamado de inversor porque, além de amplificar o sinal de entrada, o sinal de saída possui polaridade invertida, ou seja, valores positivos na entrada se tornam valores negativos na saída e vice-versa.
#### c) Amplificador Não Inversor;
![não-inversor](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/nao-inversor.png)
- O amplificador não-inversor é um AMPOP com dois resistores de realimentação, sendo VI a tensão de entrada e VO a tensão de saída do amplificador. O resistor R1 liga o terra (GND) ao terminal inversor VN. O resistor de realimentação RF liga o terminal inversor VN ao terminal de saída VO. O terminal não-inversor VP é ligado a entrada VI. Este amplificador é chamado de não-inversor porque o sinal de saída possui mesma polaridade do sinal de entrada, ou seja, valores positivos na entrada causam valores positivos na saída e o mesmo para entradas negativas.
#### d) Amplificador Somador Inversor;
- O amplificador somador é um circuito com AMPOP que permite realizar a soma de dois ou mais sinais.O amplificador somador é uma variação do amplificador inversor. Facilmente podemos ver a semelhança no circuito e no sinal de saída, que de fato, possui polaridade invertida em relação aos sinais de entrada.
![somador-inversor](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/somador-inversor.png)
#### e) Amplificador Somador Não inversor;
![somador-nao-inversor](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/somador%20nao-inversor.png)
- A diferença entre o somador inversor é de que as tensões de entrada serão aplicadas ao terminal inversor do ampop.
#### f) Subtrator;
![subtrator](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/subtrator.png)
- O amplificador subtrator permite que se obtenha na saída uma tensão igual à diferença entre os sinais aplicados, multiplicada por um ganho.
#### g) Amplificador de instrumentação;
![instrumentação](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/instrumenta%C3%A7%C3%A3o.png)
- Os amplificadores para instrumentação se caracterizam por ter uma entrada diferencial e uma elevadíssima impedância de entrada que é conseguida reduzindo-se o ganho da primeira etapa, normalmente funcionando como seguidor de tensão
### QUESTÃO 6) Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor
### QUESTÃO 7)  Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas.
 - A tensão comum é definida como a tensão média nos pinos de entrada inversora e não inversora. Se a tensão do modo comum ficar muito alta ou muito baixa, as entradas serão fechadas para baixo e a operação adequada cessa.De forma ideal, a tensão de modo comum é nula e o seu efeito nas topologias se trata de um acréscimo indesejado na tensão de saída de Vo.
### QUESTÃO 8) O que é CMRR?
- A taxa de rejeição de modo comum é a capacidade do dispositivo de rejeitar o sinal comum das entradas V+ e V-. Num AmpOp ideal, o CMRR é infinito.
- CMRR= |Av/Acm| 
- Av= ganho em malha aberta; Acm= Ganho de modo comum;
### QUESTÃO 9) Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:
#### a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito;
#### b) Qual erro na tensão de saída com relação CMRR do AmpOp.
#### c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.
### QUESTÃO 10) Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.
![datasheetOPA192](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/data%20sheet.png)
- Pelo datasheet do AmpOp OPA192 é mostrado que as tensões de entrada variam entre 0.1V abaixo de Vee e 0.1V acima do Vcc.
#### a) Defina o que é um AmpOp Rail-to-rail.
- Rail-to-rail é um termo de marketing usado para descrever um amplificador operacional cuja faixa dinâmica é capaz de atingir os extremos da tensão de alimentação. Isso pode se referir tanto à saída quanto à entrada e saída. Um AmpOp rail-to-rail pode receber um sinal de entrada e fornecer o mesmo sinal na saída sem saturar.
### QUESTÃ0 11) O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?
- A tensão de offset faz com que apareça um deslocamento no nível CC do sinal de saída. Em CA este deslocamento de nível, associado com o sinal de entrada amplificado, pode levar o Ampop a saturação. No caso de Ampops práticos a tensão de saída pode atingir valores desde alguns milivolts a alguns volts. Normalmente, a qualidade e o preço do Ampop aumenta a medida que a tensão de offset diminui. Uma forma de calcular o efeito resultado seria aplicar o GND nas duas entradas.
### QUESTÃO 12) Como minimizar o efeito da tensão de offset?
- A utilização de um potenciômetro nos pinos de ajuste de offset nos AmpOps comercias.
### QUESTÃ0 13) O que é a variação da tensão de offset pela temperatura?
- É justamente a intenção de encontrar o setpoint pela temperatura do AmpOp. Como o offset se trata como um "erro" entre medidas desejadas e medidas encontradas, o offset pode variar de acordo com a temperatura.
#### a) Como verificar esse parâmetro no datasheet?
![offset-temperatura](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/temperatura.png)
### QUESTÃO 14) O que são as correntes de polarização(Ibias) de AmpOp?
![polarizaçao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/corrente%20de%20polariza%C3%A7%C3%A3o.png)
- É o valor médio de duas correntes IB+ e IB- de entrada quando uma tensão é aplicada em uma das entradas, sendo a segunda entrada aterrada de forma que Vo = 0
#### a) Como minimizar o efeito destas correntes? Descreva as aproximações e os
possíveis circuitos para mitigar o problema.
-A existência de correntes de polarização no AmpOp conduz a uma degradação do desempenho dos circuitos, podendo também ser responsáveis pelo seu não funcionamento. Na prática, a existência das correntes de polarização obriga à utilização de componentes externos adicionais, tipicamente resistências, como forma de compensar os erros de tensão induzidos na saída.
#### b) Descreva a corrente de offset na polarização dos AmpOp. 
-O amplificador operacional ideal apresenta impedância de entrada
infinita. Os amplificadores operacionais reais, entretanto, apresentam correntes C.C. depolarização em suas entradas. Essas correntes são, geralmente devidas às correntes de base dos transistores bipolares de entrada do amplificador operacional ou ainda correntes de fuga da porta do transistor de efeito de campo em amplificadores dotados de FETs à entrada. Como, na prática, os dispositivos simétricos de entrada não são absolutamente iguais, as duas correntes de entrada são sempre ligeiramente diferentes. A diferença dessas correntes é chamada de corrente de "offset" de entrada.
