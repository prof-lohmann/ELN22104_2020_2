# Tutorial LTSPICE

## 1. Componentes Básicos

Os componentes básicos (resistores, capacitores, indutores, diodos) estão disponiveis para serem adicionados tanto na toolbar quanto pelas teclas de atalho no teclado.

Na aba de componentes existem diversos outros tipos de componentes, que tambem podem ser adicionados.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/COMPONENTES.png)
- R: Resistor
- C: Capacitor
- L: Indutor
- D: Diodo
- V: Fonte de tensão

## 2. Netlist

A netlist é a descrição de um circuito através de um documento de texto, ela pode ser acessada pela aba **View** e em seguida  **SPICE Netlist**:

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/NETLIST1.png)

### Descrevendo um circuito com uma netlist

A netlist possui uma formatação padrão para que sejam indicados os componentes e suas ligações:

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/NETLIST2.png)

Como pudemos observar com a foto acima, temos a seguinte formatação:

NETLIST: <Nome componente> <Primeiro nó> <Segundo nó> ... <Tipo do componente>

## 3. Label

A função label é muito interessante para identificar os nós de um circuito, para que seja facilitada a interpretação de um netlist ou até mesmo de uma simulação.

Tambem é amplamente utilizada para fazer uma conexão "wi-fi" entre alguns terminais, afim de simplificar o circuito desenhado.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/NETLISTLABEL.png)

## 4. Subcircuitos e novos componentes

Subcircuitos são circuitos (grandes ou pequenos) que são representados dentro de um componente através de uma netlist. Assim facilitando a implementação de tais circuitos.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/SUBCKT-NEWCOMP1.png)

Esse própio AmpOP possui um subcircuito inserido dentro dele.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/SUBCKT-NEWCOMP2.png)

Para adicionar o .cir do componente desejado utilizamos a função .lib <diretorio do arquivo>.

É necessário colocar o valor do AmpOp como o definido pela função .subckt para que sejam atribuidos as funções do novo componente.

A função .subckt está circulada em vermelho na foto acima, e tem a seguinte formatação:

.subckt <Nome do componente que representará o novo subcircuito> <Declaração das entradas e saídas do subckt> ...

## 5. Simulando

Para simular ou mudar o tipo de simulação que será realizada podemos acessar a barra **Simulate**

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/simula%C3%A7%C3%A3obasica.png)

### Simulação transiente

É uma simulação feita utilizando o tempo como uma das váriaveis (assim como um osciloscópio convencional), então é possivel observar tensões e correntes variando em função do tempo.

No CMD para editar a função é possivel mudar o tempo total da simulação, o inicio da simulação e o timestamp.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/simula%C3%A7%C3%A3otransiente.png)

Após clicar em simulate a tela de simulação vai aparecer, então é só clicar no componente que deseja saber quanta corrente está passando nele ou em algum nó para saber a tensão, também é possivel
calcular a tensão entre os dois nós, para isso é necessario clicar e arrastar o mouse entre os nós.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/simula%C3%A7%C3%A3otransiente3.png)

### Simulação DC op

Na simulação .op não é necessario informar nenhum parâmetro.

Essa simulação apresenta os dados do circuito como corrente (nos componentes) e tensão (nos nós) de forma não gráfica, lembrando que ela é indicada para circuitos DC.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/simula%C3%A7%C3%A3oop2.png)

### Transiente x Op

A simulação op é indicada em circuitos DC, e onde não teremos nenhuma tensão ou corrente variando de acordo com o tempo. Já a simulação transiente é indicada principalmente em
circuitos onde temos uma variação de algum parâmetro de acordo com o tempo.

### .Step

O .step é muito interessante quando for analisar a variação de algum parâmetro no circuito simulado.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/step.png)

Podemos notar que é feita uma simulação a cada variação do parâmetro.

A função é descrita por: .step param  <Nome> <Valor de inicio> <Valor Final> <Incremento por "Step">

No componente o nome do parâmentro necessita estar entre colchetes {"nome"}.

### DC Sweep

A simulação DC Sweep (.dc) é muito semelhante ao .step e .trans. Só que nesse caso vai ser a tensão da fonte que vai variar em uma range e steps definidos
e as tensões e correntes simuladas vão ficar em função da tensão da fonte (ao invés do tempo).

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/dcsweep.png)

É necessário informar o nome da fonte que será simulada, o tipo do "sweep", os valores iniciais, finais e o incremento.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/dcsweep2.png)

Após isso basta selecionar o nó ou componente desejado e observar a variação dos parâmetros em função da tensão da fonte.

### Measure

A função .meas pode ser utilizada para medir o parâmetro desejado em algum tempo especifico ou em alguma condição especifica.

![](https://github.com/StanisLK/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Stanislau%20de%20Lira/Atividade%201%20-%20Tutorial%20LTSPICE/images/meas.png)

### Variando a temperatura

Para variar a temperatura, basta utilizar a função .step desta forma:

.step tempo <Temperatura inicial> <Temperatura final> <Incremento>

