# 1. Resumo sobre Amplificadores Operacionais.

## O que é o AmpOp?
O amplificador operacional é um dispositivo semicondutor extremamente versátil, possui características próximas as ideais.
É composto por dezenas de transistores, resistores e um capacitor interno. 
Inicialmente será tratado como um bloco construtivo para que possamos analisar suas características elétricas e aplicações.

### O AmpOp ideal:
Pode-se considerar inicialmente que o AmpOp tem três terminais: dois de entrada e um de saída, na figura os terminais 1 e 2 são de entrada e o terminal 3 de saída.

![AmpOp](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.simbolo.JPG)

Contudo se for se considerar a alimentação teremos a configuração a seguir, onde os terminais 4 e servem como +VCC e -VEE, 
sendo que esta alimentação deve ser simétrica na maioria dos casos:

![AmpOp](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.alimentacao.JPG)

### Características do Amp Op ideal:
* Impedância de entrada infinita;
* Impedância de saída nula;
* Ganho de modo comum nulo ou rejeição de modo comum infinita;
  * Se as tensões de entrada forem iguais a tensão de saída será zero.
* Ganho de malha aberta infinito;
* Largura de faixa de resposta em frequência infinita.


### O que significa Malha Aberta e Malha Fechada?
Malha **aberta** é quando o circuito do amp op possui uma configuração **sem realimentação** do retorno da saída do amp-op à sua entrada.
Já a malha **fechada** é uma configuração que tem um caminho de **realimentação negativa ou positiva** do retorno de saída do amp-op à sua entrada.

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.ideal.realimentacao.negativa.JPG)

A figura acima mostra um amp op com configuração de realimentação negativa.

### Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada.

### Descreva as principais características das topologias:
#### a) Seguidor de Tensão (Buffer)
![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/amp.op.buffer.simbolo.JPG)
