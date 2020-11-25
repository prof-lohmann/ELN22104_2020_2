# ELN22104
### Atividade 01 - Luiz Gustavo Erthal

**1. Escreva os valores de tensão Vo para cada uma das associações de fontes abaixo:**

![Image Ex1]()

**2. Para o circuito abaixo, determine as tensões e correntes nodais, o valor da tensão Vo e o equivalente de
thevenin. Considere: V1 = 5V, V2 = 10V, R1 = 10kΩ e R2 = 5k1Ω**

![Image Ex2]()

**3. Qual o valor da corrente I para o circuito abaixo? Considere: V1 = 12V, V2 = 10V, R1 = 10kΩ,
R2 = 5k1Ω, R3 = 3k3Ω e R4 = 22kΩ.**

![Image Ex3]()

**4. Qual o valor da queda de tensão sobre o resistor R3? Considere: V1 = 9V, R1= 3K3Ω, R2 = 1k2Ω, R3
= 10kΩ e gm = 10mA/V.**

![Image Ex4]()

**5. Aprendendo a simular com o simuladores SPICE.**

**a)  Faça um resumo em forma de tutorial sobre o como funciona o SPICE e responda:**

**1. O que é o NETLIST?**

O Netlist é uma descrição em forma de tempo de todos os elementos no circuito, como transistores e capacitores por exemplo, e suas conexões.

**2. Como descrever o NETLIST de um circuito?**

Algumas ferramentas de simulações, como o Multisim, deixam o usuário desenhar o circuito livremente e traduzem os diagramas em Netlists.


**3. Como é representado cada um dos componentes? Explique com um exemplo.**

Por símbolos.


**4. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?**

É uma identificação do fio. Pode se utilizar a mesma label em vários lugares do circuito, assim separando o circuito de forma mais organizada e por blocos. 


**5. Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)**

Resistor, capacitor, indutor, diodo.


**6. O que é um “SUBCKT”? Faça um exemplo.**

É a criação de uma “caixa preta” que representa um subcircuito (daí vem SUBCKT). Também é utilizado para acrescentar componentes third-party, isto é, componentes únicos de certa empresa.


**7. Como incluir novos modelos de componentes em um simulador SPICE?**

Você pode utilizar uma diretiva do LTSpice .include e .lib, adicionando o modelo SPICE de um certo componente. É necessário baixar o arquivo direto do site do fabricante e colocar o arquivo na pasta especifica do programa.


**b) Faça um resumo em forma de tutorial sobre o como funciona os parâmetros de simulação
do SPICE, respondendo:**

**1. O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.**

É utilizado quando você precisa fazer análises transitórias de seu circuito.

**2. O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo**

É utilizado quando seu circuito não irá apresentar transitórios, ou seja, manterá os mesmos parâmetros em todos os intervalos de tempo.

**3. Quando usar .trans ou .op no SPICE?**

Respondida nas questões 1 e 2


**4. O que faz a diretiva “.step”? Forneça exemplos de utilização.**

Diretiva utilizada quando você quer variar parâmetros de um certo componente. Por exemplo, variando a resistência de um resistor.


**5. O que faz a diretiva “.means”? Forneça exemplos de utilização.**

Utilizada para realizar uma medida quando o circuito apresentar certa característica ou parâmetro.


**6. O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.**

Simulação que varia a tensão de uma fonte CC.


**7. Como simular um circuito em diferentes temperaturas de funcionamento?**

Do tutorial da Berkeley Universit: 
“Todos as entradas de dados no SPICE, assumem-se que foram medidos na temperatura média de 27ºC. Isto pode ser alterado usando o parametro TNOM no .option na linha de controle.”
