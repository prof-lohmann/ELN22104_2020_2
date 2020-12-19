EnzoRosa
#Atividade 2
##Aluno: Enzo Rosa
##Professor: Daniel Lohmann


? ###Questão 1: Ele é projetado para operar como um medidor da diferença entre sinais de tensão aplicados a dois terminais de entrada, ou seja, é um circuito amplificador responsável por aumentar sinais fracos.

? ###Questão 2: Corrente nulas nas entradas V+ e V-. A Impedância de entrada do Amp Op é aparentemente infinita, e a impedância de saída é aparentemente zero. 

? ###Questão 3: Na malha fechada o controle depende da saída feita por realimentação do sistema, já na malha aberta ela independe da saída.

? ###Questão 4: A melhor opção seria resolvar por análise nodal, pois na entrada do Amp Op é teoricamente zero, logo toda corrente iria passar pelo resistor de realimentação. 

? ###Questão 5: 
  Buffer: O buffer, também conhecido como Seguidor de Tensão, é obtida através de um Amp Op com configuração nao inversora com dois resistores R1 e R2, no qual seus valores são infinito e zero respectivamente. É chamado assim pois a saída "segue" a entrada.
  
  Amplificador não inversor: O sinal de entrada, que podemos chamar de V1 é aplicado direto ao terminal de entrada positivo do Amp Op e o resistor que podemos chamar de R1, é aplicado ao terra.
  
  Amplificador inversor: Nesta configuração temos um Amp Op com dois resistores que podemos chamar de R1 e R2. O R2 é aplicado entre o terminal de saída e o terminal de entrada inversora, que define uma realimentação negativa. Sabemos também que nesta configuração que o R2 fecha a malha em torno do amplificador. 
  
  Subtrator: Nesta configuração temos que a tensão de saída é igual a diferença entre as duas entradas multiplicada por um ganho. 
  
  Amplificador de instrumentação: Esse amplificador é composto por dois amplificadores não inversores e um amplificador de diferença. Portanto, a resistência de entrada vista através de cada uma das fontes é infinita, ou seja, o ganho de tensão é obtido pelo produto de dois cocientes entre as resistências.
  
  Amplificador somador inversor: É um circuito responsável por somar as tensões, cada tensão multiplicada por um ganho constante, ou seja, cada entrada gera um ganho à saída. Neste caso, todas as entradas são aplicadas ao terminal 1 ou entrada inversora.
  
  Amplificador somador não inversor: Essa configuração é bem parecida com ao somador inversor, todavia, neste caso as entradas são aplicadas ao terminal 2, ou à entrada não inversora. Portanto, a tensão de saída nao sofre inversão de sinal.
  
? ###Questão 6: Sabemos que o ganho em malha aberta tende ao infinito, todavia, os Amp Ops não são ideais, da mesma maneira que, tensão de offset e corrente de polarização, o que não proporciona ganhos infinitos.

? ###Questão 7: É a diferença potencial entre os sinais de entrada, saída inversora e saída não inversora. Podemos ter diversos efeitos desta tensão, um exemplo erros de medição ou danos à algum componente do circuito, levando em consideração que a tensão de modo comum é a máxima variação de tensão reconhecida em cada entrada.

? ###Questão 8: É a relação de rejeição de modo comum, ou seja, quando dois sinais de mesma frequência, amplitude e fase, são conectados às entradas de um Amp Op, os mesmos devem se cancelar e nenhuma saída deve aparecer. 

? ###Questão 10: O Amp Op demonstram limitações de tensão de entrada e de saída pois, na prática, eles apresentam padrões não ideais, ou seja, acaba tendo uma certa limitação à sua àrea de funcionamento.
  Amplificador Rail-to-rail: Esses amplificadores têm como característica um ajuste automático de tensão de saída de acordo com as tensões de alimentação do Amp Op, ou seja, aumentam a variação de tensão que podem ser aplicadas tanto na saída quanto na entrada.

? ###Questão 11: Tensão de offset é uma instabilidade nas entradas do Amp Op conveniente ao alto ganho CC. Esta tensão pode interferir na utilização do amplificador em aplicações e etc. 
 Podemos calcular o efeito resultante sobre a tensão de saída utilizando o teorema da superposição onde anulamos fonte por fonte e, consequentemente, obtendo seus efeitos no sinal de saída. 
 
? ###Questão 12: Podemos ligar um capacitor na entrada inversora, porém só temos essa possibilidade em aplicações que não demandam uma amplificação de sinais CC ou frequências muito baixas.

? ###Questão 13: Excelentemente, um Amp Op não tem alterações no seu comportamento dado à variação da temperatura, porém, na prática, a mudança de temperatura pode causar alterações no comportamento de um Amp Op. Chamamos esse efeito de DRIFT.

? ###Questão 14: Basicamente todo o Amp Op precisa de uma corrente para desempenhar a função dos componentes. A corrente de polarização de entrada consiste em fontes de corrente CC ligadas ao Amp Op. Fabricantes especificam o valor médio de lbias, assim como sua diferença (corrente de offset).
  A) Devemos inserir um resistor em sério com o terminal de entrada inversora, pois para o sinal o resistor é infame. Podemos também procurar um outro Amp Op com corrente de offset menor.
  B) É a desigualdade entre as correntes de polarização e de entrada, através de Ios= |Ib1-Ib2|.
 
