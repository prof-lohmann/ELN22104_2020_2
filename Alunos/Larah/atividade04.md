# Atividade 04 Larah

-----------------------

## Parte 01: Entendendo um regulador linear

 * Princípios de regulação de tensão: Um regulador de tensão consiste em um sistema de controle eletrônico que recebe um sinal com tensão não regulada na entrada e retorna na saída um sinal com tensão constante. Muito utilizado na alimentação de circuitos eletrônicos.
 * Tensão de saída e tensão de ripple: O capacitor retificador não retifica 100% o sinal de entrada, a onda após a carga e descarga do capacitor fica com um resíduo, proveniente desse processo. O ripple é a diferença entre a tensão mínima e máxima do sinal de onda não retificado pelo capacitor retificador.
 * Regulação de linha: A regulação de linha é um dos apectos que podem interfirir na constância da tensão do sinal de saída do regulador. O sinal que chega na entrada do regulador geralmente é inconstante,  a regulção de linha trabalha com a relação entre a tensão de saída pela tensão de entrada.
 * Regulação de carga: A regulação de carga é um dos apectos que podem interfirir na constância da tensão do sinal de saída do regulador. A carga que o regulador linear alimenta geralmente varia com o tempo e a variação da carga é proporcional a corrente que o sistema necessita e altera a tensão de saída do regulador. A regulaçao de carga é a relação da tensão de saída pela corrente da carga.   
 * Conceito de LDO – Low Dropout Voltage: Um LDO é um regulador de tensão que precisa de pouca energia para funcionar corretamente e dissipa pouca energia. Para um CI regulador de tensão funcionar ele precisa de uma tensão mínima superior a saída que é chamada de Vdo, o LDO é um baixo Vdo para o regulador funcionar.

### Qual relação entre a tensão de alimentação do ampop e a tensão de saída?
  A relação é dada por: Tensão saída = Vdiodo zener D3 * (R2+R3)/R3. O ampop desliga o mosfet quando a tensão de saída está fora da tensão desejada, com o mosfet desligado a saída cai para 0v.  
### O que devemos considerar para esse circuito operar como um LDO?
  A escolha do diodo zener, que deve proporcionar uma tensão de entrada para o ampop superior a tensão de saída do mesmo. Mantendo a dissipação de energia (potência) baixa. Outro requisito importante para o ampop trabalhar é que a entrada VCC do ampop tem que ter tensão suficiente para saturar o gate do mosfet, pois o mosfet polarizado implica em menos perdas de energia.
### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
  Pode-se utilizar um circuito com VEE indo para o GND e VCC sendo alimentado por um bloco dobrador de tensão junto de um bloco retificador de tensão com um mosfet, diodo zener, ampop e resistores. A tensão de alimentação (VCC e VEE) é dada pela soma de Vgs do mosfet com a tensão Vout da saída da fonte.
  
### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

  Pela fórmula temos:
  
  ![image](https://user-images.githubusercontent.com/58013651/116172357-0237dd00-a6e1-11eb-92fc-26a46f9fb9a7.png)
  
  
### Quais problemas apresentam esse circuito? Podemos melhorar?

  Esse circuito pode gerar PSRR, no caso a saída do ampop pode apresentar ruído devido a instabilidade da alimentação do ampop devido ao ripple gerado pela descarga do capacitor. Para se melhorar esse circuito pode-se utilizar um CI regulador linear ou montar um circuito com um transistor NPN, resistor e diodo zêner com a mesma função de corrigir o ruído na alimentação do ampop. Outro problema desse circuito é que nem todo ampop pode funcionar corretamente com ele, sendo indicado uma fonte simétrica.
  
### Vamos projetar esse circuito de alimentação do AmpOp?

Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador =
1V, considere as quedas de tensão nos diodos de 0,7V.

- Qual a Tensão VGS? Descreva como obter o valor.

Para uma corrente de saída de 1A tem-se a tensão VGS de 4V, informação obtida no datasheet do mosfet.
Esse valor precisa ser somado a tensão de saída do mosfet para se definir a tensão de saída do ampop.

- Qual a corrente de alimentação do AmpOp?

Típica de 1.4mA e maxima de 3mA

- Qual a tensão de alimentação do AmpOP?

Máxima de 32V e mínima de +16V ou -16V.

- Qual fator devo considerar para escolher o transistor Q1?

O ganho deve ser alto para que a corrente de dreno seja baixa. 

- Qual valor da tensão do diodo zener D6?

A tensão do zener precisa ser superior a tensão de saída do ampop, que nesse projeto precisa ser de aproximadamente 19V (saída de 15V somada da tensão Vgs do mosfet).

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

Para minimizar os ruídos no circuito o zener deve possuir uma tensão baixa e com a menor variação posível, o que leva a escolher um diodo zener com resistência pequena.

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma
aumento de 10mA na corrente de alimentação, o circuito proposto continuará
funcionando?

Sim, contanto que os valores minimos do datasheet sejam atendidos.

- Projete o circuito de alimentação do AmpOp com as especificações acima.

Componentes escolhidos:

Diodo 1N4001
Diodo zener BZX84C11


-------------------------------------------
## Parte 02: Calculando e dimensionando os componentes

### Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.

  Considerando que os diodos estão funcionando como retificadores de onda completa, cada um irá operar em um semiciclo da alimentação, aplicando sempre uma corrente no mesmo sentido para a carga. Precisamos saber o valor dos capacitores a serem utilizados e a corrente de pico sobre os diodos.
  
  Para os valores solicitados, o capacitor será C= (Imáx*T)/(Vr*2)= Icarga/(f*2*Vr)=9,167mF
  
Pelos valores de tensão reversa, e correntes necessárias pode-se usar o diodo 1n5400.

![d](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/D1eD2.1n5400.datasheet.PNG)

### Circuito referência de tensão zener (R1 e D3):
 • Quais fatores devo considerar para escolher o diodo zener para essa aplicação? 

Para evitar que o zener altere significativamente a tensão na saída (ruído), sua resistência Rz deve ser baixa.

• Qual a influência da regulação de linha e da regulação de carga para este circuito?

Como visto na revisão de conceitos, a regulação de linha corresponde a capacidade de manter tensão de saída estável em relação a tensão de entrada e a regulação de carga corresponde a capacidade de manter a saída estável em relação a sua carga.
Por estar ligado na entrada não inversora do ampop, a qual não possui corrente, o circuito não terá influência de regulação de carga.

 • Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear? 

A variação indesejada de tensão que pode ser causada pelo diodo zener será multiplicada pelo ganho do ampop, para que o circuito tenha uma boa regulação de linha essa variação precisa ser mínima.

- Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia? Sugestão de melhoria: 

Sim, eliminando um dos fatores da regulação, mantendo a corrente constante no zener, mantendo a tensão o mais constante possível.

No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar? 

Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?

Com um circuito sobrecorrente.

### Escolhendo o transistor M1 e calculando R2 e R3. 

• Qual a corrente contínua necessária? 

Corrente de 1A solicitada para o projeto.

• Quais os limites de tensão para este circuito? 

Objetivo de 15V na saída.

Ao escolher o transistor obtenha: 

Quais os os parâmetros L, W, uo, Cox, VA e Vt? 

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/M1.parametros.PNG)

Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V 

Quais as tensões máximas de operação deste componente? 

Vds máxima de 100V. Vgs máxima de 20V e mínima de -20V

Obtenha as curvas ID x VDS para esse componente para as tensões VGS de 2V, 3V, 4V, 5V e 10V e compare os resultados com as curvas presentes no Datasheet. 

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/VGS.PNG)

Utilizando a curva ID x VDS obtenha os valores RDS e compare com os valores teóricos. 

Qual o valor da capacitância de gate? 

Justifique a escolha dos resistores R2 e R3

---------------------------------------------------

## Parte 03: Adicionando um circuito de proteção de sobre corrente ao regulador linear

- Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito?

  Como o nome já diz é quando a corrente que percorre um circuito eletrônico ultrapassa o valor esperado para a operação correta do circuito. Componentes com restrições de corrente máxima irão sobreaquecer e queimar, como o mosfet e o ampop da fonte.
 
- O que deve fazer um circuito de proteção de sobrecorrente?

  Impedir que a sobrecorrente chegue e afete o circuito projetado e demais componente.
  
- O que é a proteção foldback?

  É um sistema de proteção de sobre corrente, ele diminui a corrente enquanto diminui a tensão que vai para a carga, isso possibilita que no nosso circuito por exemplo o mosfet não sobre aqueça. Pois caso o dispositivo de proteção de corrente não fosse do tipo foldback provavelmente a tensão que iria para a carga iria diminuir enquanto a corrente se manteria estática, com isso a alta potência dissipada no mosfet do circuito iria se manter enquanto o surto de tensão continuasse. Já com o foldback não, pois o sistema diminui a corrente saída e com isso o potência dissipada no bloco regulador linear.
  
  ![Capturar](https://user-images.githubusercontent.com/58013651/116634242-ebd49000-a931-11eb-86af-0bce308159dd.PNG)
  
 - Pesquise as topologias disponíveis:
  
  ![121312312](https://user-images.githubusercontent.com/58013651/116639605-47594a80-a93f-11eb-9cc5-14cc8c29f1dd.PNG)
  
  Esta é outra topologia de regulador linear fornecido pela Texas Instrument, esse regulador linear é do tipo LDO. A equação do seu Vout é dada por: VOUT= VREF× (1+R1/R2). Como pode-se ver o circuito é muito similar ao que fazemos nesse projeto no entanto para se um Vgs suficiente para saturar o mosfet e ele operar como chave a Texas Instrument utiliza um sistema de charge pump para elevar a tensão de Vin para poder alimentar o Vcc do ampop com tensão superior ao Vin e ter uma saída superior a Vout.

 - Caso deseja-se fazer um circuito LDO, o o que devemos levarem consideração para o regulador?
 
  Para esse circuito ser LDO o Vin tem que ser muito próximo do Vout, para isso o Vgs deve ter valor suficiente para saturar o transistor. Esse circuito para a proteção do ampop existe um resistor na saída do ampop, como visto em aula nesse resistor deve passar uma corrente de 10mA, com isso podemos estipular qual resistor podemos utilizar para que o nosso circuito opere como um LDO. Temos que o Vgs do nosso transistor escolhido é de 4V para saturar e a fonte deve ter um Vout de 15V, como visto anteriormente a saída do ampop deve ter 19V para o sistema operar corretamente e 10mA no máximo para operar com menor perda de energia. Assim para o sistema operar como LDO temo que R6 = 19V/10mA = 19.000 Ohms.
 

