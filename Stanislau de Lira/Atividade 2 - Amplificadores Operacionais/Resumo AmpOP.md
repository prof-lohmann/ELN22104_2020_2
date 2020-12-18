# AMPLIFICADORES OPERACIONAIS

## O que é um AmpOP?
É um circuito integrado, capaz de amplificar o sinal de entrada e realizar operações matemáticas, com entradas de alimentação, saida, entrada inversa e não inversora.

## AmpOp Ideal
![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%202%20-%20Amplificadores%20Operacionais/images/ampopideal.JPG)

Um AmpOP ideal possui as entradas não inversoras e inversoras com a impedancia infinita, o ganho é infinito, e a impedancia na saida é nula, e é não sensivel a temperatura.

## Malha Aberta e Malha Fechada
Acontece uma malha fechada quando as entradas inversoras ou não inversoras do AmpOp são realimentados por sua saída, e em malha aberta não há realimentação.

## Calculando Circuitos de Malha Fechada
Para calcular os circuitos de malha fechada utilizamos a equação do ampop ideal como base, e fazendo uma análise de nós obtemos uma equação para o circuito.
## Seguidor de Tensão (Buffer)
É um circuito que temos na saída a mesma tensão da entrada, é utilizado para conectar uma tensão aliada de uma resistencia a uma resistencia de saida sem que ela sofra os efeitos da resistencia de entrada.

## Amplificador Inversor
É um circuito que tem como objetivo amplificar a tensão de entrada e inverter o seu sinal na saida do AmpOP

## Amplificador Não Inversor
É um circuito que tem como objetivo amplificar a tensão de entrada e manter o seu sinal na saida do AmpOP

## Amplificador Somador Inversor
É um circuito que tem como objetivo somar as tensões de entrada, realizar a amplificação e inverter o seu sinal na saida do AmpOP

## Amplificador Somador Não Inversor
É um circuito que tem como objetivo somar as tensões de entrada, realizar a amplificação e manter o seu sinal na saida do AmpOP

## Subtrator ou Diferencial
É um circuito que tem como objetivo subtrair as tensões da entrada inversora e não inversora e realizar a amplificação 

## Amplificador de Instrumentação
É uma composição de um amplificador subtrator e buffers gerando uma impedancia de entrada infinita, alto ganho e facil ajuste de ganho.

## Ganho de Malha Aberta Finito (inversor e não inversor)
Os ganhos em um mundo real não sao infinitos.
## CMRR
CMRR é a rejeição em modo comum, quando dois sinais da mesma amplitude, frequência e fase são aplicados às entradas eles se cancelariam e não deveria ocorrer nenhuma saída, porem na pratica não é o que acontece e essa saída é o CMRR, sendo medido em dB.

## Tensão de Modo Comum (Vcm)
A tensão de modo comum é um offset da tensão que é "comum" as duas entradas do AmpOp

### Exemplo Tensão de Modo Comum com Subtrator

## Limitações de Tensão de Entrada e Saída (datasheet)
O limite da tensão de saida tende ao VCC do AmpOp (saturação) e depende o AmpOp utilizado.

### AmpOp Rail-to-rail
É um Amplificador Operacional cuja tensão na saída alcança o mesmo nível que as tensões de alimentação do AmpOp

## Tensão de Offset
É a tensão necessária entre os terminais de entrada para anular a saida, já que um ampop com ambas as saídas no terra o seu sinal de saída não é 0, devido a sua construção interna.
Efeito resultante na saída de um amp inversor e não inversor:
V0=Vos*(1+R2/R1)
### Minimizando o Ofeito da Tensão Offset
Para minimizar o efeito da tensão offset é necessario conectar um capacitor na entrada w=1/CR1, tendo V0=Vos.
### Variação da Tensão Offset Pela Temperatura
O coeficiente de variação da tensão do offset pela temperatura é conhecido como drift ou TCVos.
## Correntes de Polarização(Ibias)
É a corrente que circula nas entradas de um ampop (mesmo que aterradas) devido a construção interna no ampop com transistores
Ibias = (Ib+ + Ib-)/2

### Minimizando o Efeito da Corrente de Polarização
Utilizar um R3=(R1.R2)/(R1+R2) entao teremos um Vout em função da corrente de offset, que é menor que a corrente de polarização Vout = Iof.R2

### Corrente de Offset na Polarização
É o modulo da diferença das correntes nas entradas do ampop Iof = |Ib+ - Ib-|


