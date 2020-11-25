Criei a pasta.
# Atividade 1
## Imagem das resoluções das questões 1, 2, 3 e 4:
![resolução](https://github.com/Brunossilvar/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/WhatsApp%20Image%202020-11-25%20at%207.05.07%20PM.jpeg)
![resolução](https://github.com/Brunossilvar/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/WhatsApp%20Image%202020-11-25%20at%207.05.08%20PM.jpeg)

## Questão 5:
### A)

O que é o NETLIST?
+ Netlist é uma descrição da conectividade de um circuito eletrônico.

Como descrever o NETLIST de um circuito?
+ Na sua forma mais simples, uma netlist consiste em uma lista dos componentes eletrônicos em um circuito e uma lista dos nós aos quais estão conectados.

Como é representado cada um dos componentes? Explique com um exemplo.
+ O componente é representado por uma letra maiúscula(no caso do SPICE), os dóis nós que se encontram em seus polos e o seu valor.
+ R27 5 0 200 (Resistor R27 conectado entre os nós 0 e 5 com valor de 200 ohms)

O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
+ Um elemento "label" representa uma legenda para um item em uma interface de usuário. Ele pode estar associado com um elemento de controle, colocando este dentro do elemento label, ou usando o atributo for. Tal controle é chamado o controle etiquetado do elemento etiqueta. Um input pode ser associado a diversas etiquetas (<label>s).
  
Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
+ Resistor, capacitor, indutor, diodo e ground.
  
O que é um “SUBCKT”? Faça um exemplo.
+ É um subcircuito do SPICE. Um subcircuito simplifica as listas de spice netlists permitindo o reuso de um conjunto de elementos de circuito.
+ "SUBCKT SubName N1 N2 ... ... .ENDS"

Como incluir novos modelos de componentes em um simulador SPICE?
+ Para adicionar um modelo SPICE é necessário que o o arquivo nome. cir já esteja gravado em uma pasta no computador local. Em seguida seleciona-se no QUCS “SPICE netlist” na aba “file components”, colocando-se o nome do arquivo que contém o modelo.

### B)
A simulação (.trans) é uma simulação em que o tempo é um parâmetro. Pode ser usado para observar o valor de uma carga em função do tempo. Um exemplo seria um fonte que varia com o tempo controlando um circuito. Já a simulação “DC operating point” faz apenas uma análise do circuito em corrente contínua, útil para analisar o estado inicial de um circuito ou para analisar seu comportamente em corrente contínua. 
Quando deseja-se analisar as alterações de um circuito no decorrer do tempo e utilizar .OP quando deseja-se analisar um circuito em corrente contínua.
No assunto diretivas, a ".STEP" faz uma variação de determinado parâmetro de um componente no circuito utilizado, já a diretiva ".MEANS" avalia as grandezas elétricas definidas pelo usuário.
Entretanto em simulação, a "DC sweep" faz uma variação da tensão de uma determinada fonte de corrente contínua. Utiliza-se para analisar o comportamente de um transistor, por exemplo.
Para simular um circuito em diferentes temperaturas no LTSpice, utilizamos a diretiva .STEP TEMP. Exemplo:

.step temp 40 70 10

A temperatura começa em 40ºC até 70ºC e tem variação de 10ºC.
