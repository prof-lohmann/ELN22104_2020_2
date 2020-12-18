# ATIVIDADE 2


1. O que é o AmpOp?
+ É um circuito capaz de amplificar um sinal de entrada, além de poder fazer operações matemáticas como soma, subtração.

2. Mostre os simbolos e as características do AmpOp IDEAL?

![ampop](https://github.com/yannsavordelli/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/ampop.jpg)
+  Possui 2 terminais de entrada, um com sinal negativo que e denominado entrada inversora, um terminal com o valor + que e chamada de entrada não inversora, além disso tem 2 outras entradas um é o terminal de alimentação positiva (+vcc), e outro de alimentação negativa (vcc) alem de um terminal de saída.
  Um ampop IDEAL é caracterizado por um ganho infinito em malha aberta, uma rsposta de frequência infinita, impedância de entrada infinita, impedância de saída infinita e insensibilidade a temperatura.
  
3. O que significa Malha Aberta e Malha Fechada?
+  Em uma malha aberta a açao de controle independe da saída uma malha fechada depende da saída.

4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada

5. Descreva as principais características das topologias:
a) Seguidor de Tensão (Buffer)
+ Demanda uma baixa corrente para manter o circuito sem alterar os valores do circuito.
b) Amplificador Inversor; 
+ Além de amplificar o valor de entrada o valor de saída tem o valor invertido.
c) Amplificador Não Inversor;
+ É chamado assim pois o sinal de entrada deles e igual ao sinal de saída, não faz nenhum tipo de alteração no sinal do circuitos.
d) Amplificador Somador Inversor;
+ Faz com que possa adicionar novas tensões na entra inversora ou seja tem uma adiçao de tensao mas o sinal de saida vai ser o contrario ao de entrada. 
e) Amplificador Somador Não Inversor;
+ Faz com q possa adicionar novas tensões na entrada não inversora e no final o sinal se mantêm o mesma na saída. 
f) Subtrator; 
+ É uma combinaçao entre o circuito inversor e não inversor, faz com que o sinal de saida seja a subtraçao entre os 2 terminais de entradas.
g) Amplificador de Instrumentação; 
+ Faz o tratamento de sinais cm baixa variação de tensão.

6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor.
a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB. 
b) Dica veja o problema 2.20 pg 83 do livro texto.

7. Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas.
+ A tensão comum é definida como a tensão média nos pinos de entrada inversora e não inversora. Se a tensão do modo comum ficar muito alta ou muito baixa, as entradas serão fechadas para baixo e a operação adequada cessa. De forma ideal, a tensão de modo comum é nula e o seu efeito nas topologias se trata de um acréscimo indesejado na tensão de saída de Vo.

8. O que é CMRR?
+ É a relação de rejeiçao em modo comum é dado pela relaçao entre o ganho diferencial e a media aritmética entre entradas de tensão. Sendo essa relaçao idealmente igual ao infinito para ter uma rejeição das medias.

9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando:
a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito; 
b) Qual erro na tensão de saída com relação CMRR do AmpOp. 
c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%.

10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet.
+ Pelo datasheet do AmpOp OPA192 é mostrado que as tensões de entrada variam entre 0.1V abaixo de Vee e 0.1V acima do Vcc.

a) Defina o que é um AmpOp Rail-to-rail.
+ Rail-to-rail é um termo de marketing usado para descrever um amplificador operacional cuja faixa dinâmica é capaz de atingir os extremos da tensão de alimentação. Isso pode se referir tanto à saída quanto à entrada e saída. Um AmpOp rail-to-rail pode receber um sinal de entrada e fornecer o mesmo sinal na saída sem saturar.

11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor?
+ A tensão de offset faz com que apareça um deslocamento no nível CC do sinal de saída. Em CA este deslocamento de nível, associado com o sinal de entrada amplificado, pode levar o Ampop a saturação. No caso de Ampops práticos a tensão de saída pode atingir valores desde alguns milivolts a alguns volts. Normalmente, a qualidade e o preço do Ampop aumenta a medida que a tensão de offset diminui. Uma forma de calcular o efeito resultado seria aplicar o GND nas duas entradas.

12. Como minimizar o efeito da tensão de offset?
+ A utilização de um potenciômetro nos pinos de ajuste de offset nos AmpOps comercias.

13. O que é a variação da tensão de offset pela temperatura?
+ É justamente a intenção de encontrar o setpoint pela temperatura do AmpOp. Como o offset se trata como um "erro" entre medidas desejadas e medidas encontradas, o offset pode variar de acordo com a temperatura.
a) Como verificar esse parâmetro no datasheet?
14. O que são as correntes de polarização(Ibias) de AmpOp?
+ É o valor médio de duas correntes IB+ e IB- de entrada quando uma tensão é aplicada em uma das entradas, sendo a segunda entrada aterrada de forma que Vo = 0

a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema. 
+ possíveis circuitos para mitigar o problema. -A existência de correntes de polarização no AmpOp conduz a uma degradação do desempenho dos circuitos, podendo também ser responsáveis pelo seu não funcionamento. Na prática, a existência das correntes de polarização obriga à utilização de componentes externos adicionais, tipicamente resistências, como forma de compensar os erros de tensão induzidos na saída. 
b) Descreva a corrente de offset na polarização dos AmpOp
+ O amplificador operacional ideal apresenta impedância de entrada infinita. Os amplificadores operacionais reais, entretanto, apresentam correntes C.C. depolarização em suas entradas. Essas correntes são, geralmente devidas às correntes de base dos transistores bipolares de entrada do amplificador operacional ou ainda correntes de fuga da porta do transistor de efeito de campo em amplificadores dotados de FETs à entrada. Como, na prática, os dispositivos simétricos de entrada não são absolutamente iguais, as duas correntes de entrada são sempre ligeiramente diferentes. A diferença dessas correntes é chamada de corrente de "offset" de entrada.




