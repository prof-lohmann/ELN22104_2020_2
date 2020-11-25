## Aps 01:
![Aps010102](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.1e2.jpg)


![Aps0103](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.3.jpg)

![Aps0104](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/aps_01.ex.4.jpg)


#  Questão 5
# a)

# O que é o NETLIST? Como descrever a NETLIST?
Netlist é a forma como um progama SPICE descreve os componentes de um circuito, indicando os nomes e nós relacionados a cada componente. A netlist pode ser descrita como um texto, no qual cada linha representa um componente, com o nome do componente seguido de seu nó origem, nó destino e de seu valor atribuído.

# Como é representado cada um dos componentes? Explique com um exemplo. O que é o “LABEL” de um nó e qual a vantagem de usar o mesmo?
Cada componente é representado por um símbolo, alguns predefinidos, sendo que existe também a possibilidade de desenhar seu próprio símbolo para um componente não exitente na bilbioteca padrão do SPICE.
LABEL é o nome dado a um nó, ele auxilia na organização do circuito facilitando a leitura do mesmo, observe o exemplo a seguir:
![circuito.semlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/circuito.semlabel.JPG)

![netlist.semlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/netlist.semlabel.JPG)

Por não possuirem labels os nós são identificados por numerações geradas pelo programa SPICE, sendo que o nó GND é identificado por 0.
Em circuitos menores isso pode não ser um problema, mas quando o projeto é mais complexo o ideal é adicionar labels como demonstrado neste circuito:

![circuito.comlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/circuito.comlabel.JPG)

![netlist.commlabel](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/netlist.comlabel.JPG)


# Quais os componentes básicos implementados no SPICE?
Os componentes mais básicos do SPICE possuem ícones de atalhos na parte superior direita do programa, são eles:
![componentes.basicos](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/componentes.basicos.JPG)

Além destes, para acessar os demais componentes basta clicar no ícone "component" que se abrirá o seguinte menu:

![biblioteca.componentes](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/componentes.bilbioteca.JPG)

# O que é um “SUBCKT”? 
Um sub-circuito (SUBCKT) permite definir uma coleção de elementos como um sub-circuito, por exemplo, um amplificador operacional e
inserir esta descrição no circuito global, como qualquer outro componente. 
Um sub-circuito é definido através de uma declaração de controle .SUBCKT, seguido pela descrição do circuito como se
segue:

.SUBCKT SUBNAME N1 N2 N3 ...

Declaração dos elementos

.

.

.

.ENDS SUBNAME

# Como incluir novos modelos de componentes em um simulador SPICE?
Para incluir um novo modelo, pode se inserir o texto do subckt em uma diretiva .op na tela do esquemático ou então, com o texto salvo em um documento na pasta do seu projeto, usar a diretiva .lib com o caminho que leva ao documento para indicar que se quer utilizar aquele modelo de componente.

# b)

# O que é simulação transiente? Quando usar?
Este comando especifica o intervalo de tempo no qual a análise de transitório será realizada e os incrementos de tempo, é usado quando o circuito possui variações no tempo, como ondas senoidais e afins, possibilitando visualizar em gráficos as informações simuladas.

O formato é o seguinte:

.TRAN TSTEP TSTOP <TSTART <TMAX>> <UIC>
  
TSTEP: é o incremento de tempo
 TSTOP: é o tempo final
 TSTART: é o tempo inicial (se omitido, é assumido TSTART = 0)
 TMAX: é o tamanho de passo máximo. 
 UIC significa Use Initial Condition e instrui o PSpice a usar um valor inicial.
 
 Exemplo:
 ![ex.tran](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/ex.tran.JPG)
 
 # O que é simulação “ DC operating point” (.op)? Quando usar?
 .op instrui o SPICE a calcular os pontos de operação CC:
 tensão nos nós;
 corrente em elemento.
 Utilizar o circuito que mostrava a netlist obtem-se o seguinte .op:
 
 ![circuito.op](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/circuito.op.JPG)


# O que faz a diretiva “.step”? Forneça exemplos de utilização.
O comando .step varia o valor de um elemento entre um parâmetro inicial e final com um determinado intervalo. 

Exemplo:

![ex.step](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/ex.step.JPG)

# O que faz a diretiva “.means”? Forneça exemplos de utilização.


# O que é a simulação “DC sweep” (.dc)? Quando usar? 
É uma simulação que varia os valores de uma fonte de tensão CC. Pode-se aninhar comandos DC que são frequentemente utilizados para traçar características do transistor, como a
corrente de dreno ids versus a tensão dreno-fonte Vds para diferentes tensões da porta Vgs. 

Exemplo:

.DC Vds 0 5 0.5 Vgs 0 5 1

No exemplo acima, a tensão Vds será incrementada de 0 a 5V em passos de 1V para cada valor de Vgs. 

# Como simular um circuito em diferentes temperaturas de funcionamento?

Utilizando .step e o parâmetro temp pode-se variar a temperatura.

.step temp inicial final incremento

.step temp 1 10 2

