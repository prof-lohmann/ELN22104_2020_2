# Netlist

Netilist é uma descrição de componentes e suas conexões. Um circuito é descrito por um Netlist será descrito por meio de seus nós, componentes e pela maneira que nós e componentes estão conectados.

## Label 
    
    Label é um palavra usada pra identificar um elemento, seja ele um nó ou componente, no Netlist. 
    É possivel renomear uma label para facilitar a compreensão na hora de ler o Netlist.
    
## Componente
    
    Os componentes basicos implementados no SPICE são resistor, capacitor e indutor e um SUBCKT. 
    Cada componente é representado por uma Label e um valor no script, como por exemplo, 
    a letra R representa um resistor é o 10k representa o valor da resistência: 

![imagem de modelo no ltspice e nomenclatura no netlist](img/resistor.png)

## SUBCKT
    
    Representado pela letra U no netlist, o SUBCKT é uma abstração de um conjunto de componentes e 
    suas ligações.

![imagem de modelo no ltspice e nomenclatura no netlist](img/subckt.png)

## Como incluir novos modelos

Utilizando 
# Simulação SPICE

## Transiente
    
    *oq é* Usada para analizar eventos variantes no tempo como transitórios. 
    representada pela diretiva ".trans"

\*exemplo\*

## *DC operating point*
    
    *o que é*. Usada... representada pela diretiva ".op"

\*exemplo\*

## *DC sweep*

    massa id neque aliquam vestibulum morbi blandit cursus risus at

\*exemplo\*

## .trans vs .op
    
    id leo in vitae turpis massa sed elementum tempus egestas sed sed risus

## .step
    
    volutpat sed cras ornare arcu dui vivamus arcu felis bibendum ut tristique et egestas quis

## .means
    
    ullamcorper dignissim cras tincidunt lobortis feugiat vivamus at augue eget arcu dictum varius duis at consectetur lorem

## Simulando um circuito em diferentes temperaturas
    
    lobortis mattis aliquam faucibus purus in massa tempor nec feugiat

