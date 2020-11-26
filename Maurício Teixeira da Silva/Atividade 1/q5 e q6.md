a)

1- O que é ***NETLIST***?
  
    R- Consiste na lista de componentes de um circuito e uma lista dos nós aos quais es~tao ligados.
    
  2- Como descrever o ***NETLIST*** de um circuito ?
  
    R- Cada linha representa um componente, os nós em que está ligado e seu valor.
    
  3- Como é representado cada um dos componentes ? Explique com um exemplo.
  
    R- Cada componente é representado pelo seu símbolo universal e duas caixas de texto para identificação. Por exemplo uma fonte CC: círculo +/-, nome da fonte e tensão.
    
  4- O que é o “***LABEL***” de um nó e qual a vantagem de usar o mesmo?
  
    R- Label de um nó é o nome dado para cada nó, tendo como vantagem a melhor identifiacção dos nós no circuito, facilitando o entendimento de circuitos mais complexos.
    
  5- Quais os componentes básicos implementados no SPICE? (resistor, capacitor etc)
  
    R- Os componentes básicos ficam a um clique de distância na barra de ferramentas do software, que são: Terra, capacitor, indutor, diodo, resistor.
    
  6- O que é um “SUBCKT”? Faça um exemplo.
  
    R- É um subcircuito formado externamente a um circuito principal por meio de um ou mais nós que interligam os circuitos com o LABEL dos nós.
    
  7- Como incluir novos modelos de componentes em um simulador SPICE?
  
    R- Com o arquivo .cir salvo em seu computador, vá em file>open ou então arraste para a tela do software.
    
  
  
b)

  1- O que é simulação transiente (.trans)? Quando usar? Faça um exemplo.
  
    R- Transiente são simulações em função do tempo, que por esse motivo, são usadas em circutios de corrente alternada.
    
  2- O que é simulação “ DC operating point” (.op)? Quando usar? Faça um exemplo.
  
    R- Simulação em corrente contínua, usado em circutios que não sofrem alterações com o passar do tempo.
    
  3- Quando usar .trans ou .op no SPICE?
  
    R- Quando o circuito sofrer alterações em função do tempo ou não respectivamente.
    
  4- O que faz a diretiva “.step”? Forneça exemplos de utilização.
  
    R- Executa uma variação de um parametro qualquer que pode ser por exemplo, um componente resistivo variando de 100 a 100k em intervalos de 100. Nestas configurações o programa irá calcular os resultados para cada intervalo.
    
  5- O que faz a diretiva “.means”? Forneça exemplos de utilização.
  
    R- Este comando calcula o valor médio de alguma variável, como por exemplo, a potencia média de saída de um circtuito.
    
  6- O que é a simulação “DC sweep” (.dc)? Quando usar? Faça um exemplo.
  
    R- Varia a tensão ou a corrente de um elemento do circuito
    
  7- Como simular um circuito em diferentes temperaturas de funcionamento?
  
    R- Usando o comando .temp
