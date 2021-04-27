# Trabalho 04 Larah

-----------------------

## Parte 01: Entendendo um regulador linear

 * Princípios de regulação de tensão: Um regulador de tensão consiste em um sistema de controle eletrônico que recebe um sinal com tensão não regulada na entrada e retorna na saída um sinal com tesão constante. Muito utilizado na alimentação de circuitos eletrônicos.
 * Tensão de saída e tensão de ripple: O capacitor retificador não retifica 100% o sinal de entrada, a onda após a carga e descarga do capacitor fica com um resíduo, proveniente desse processo. O ripple é a diferença entre a tensão mínima e máxima do sinal de onda não retificado pelo capacitor retificador.
 * Regulação de linha: A regulação de linha é um dos apectos que podem interfirir na constância da tensão do sinal de saída do regulador. O sinal que chega na entrada dp regulador geralmente é inconstante,  a regulção de linha trabalha com a relação entre a tensão de saída pela tensão de entrada.
 * Regulação de carga: A regulação de carga é um dos apectos que podem interfirir na constância da tensão do sinal de saída do regulador. A carga que o regulador linear alimenta geralmente varia com o tempo e a variação da carga é proporcional a corrente que o sistema necessita e altera a tensão de saída do regulador. A regulaçao de carga é a relação da tensão de saída pela corrente da carga.   
 * Conceito de LDO – Low Dropout Voltage: Um LDO é um regulador de tensão que precisa de pouca energia para funcionar corretamente e dissipa pouca energia. Para um CI regulador de tensão funcionar ele precisa de uma tensão mínima superior a saída que é chamada de Vdo, o LDO é um baixo Vdo para o regulador funcionar.

### Qual relação entre a tensão de alimentação do ampop e a tensão de saída?
  A relação é dada por: Tensão saída = Tensão entrada(V+) * (R2+R3)/R3. O ampop desliga o mosfet quando a tensão de saída é fora da tensão desejada, com o mosfet desligado a saída cai para 0v.  
### O que devemos considerar para esse circuito operar como um LDO?
### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
  Pode-se utilizar uma fonte simétrica para alimentar o ampop.
  
### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

  Pela fórmula temos:
  
  ![image](https://user-images.githubusercontent.com/58013651/116172357-0237dd00-a6e1-11eb-92fc-26a46f9fb9a7.png)
  
  
### Quais problemas apresentam esse circuito? Podemos melhorar?

  Esse circuito pode gerar PSRR, no caso a saída do ampop pode apresentar ruído devido a instabilidade da alimentação do ampop devido ao ripple gerado pela descarga do capacitor. Para se melhorar esse circuito pode-se utilizar um CI regulador linear ou montar um circuito com um transistor NPN, resistor e diodo zêner com a mesma função de corrigir o ruído na alimentação do ampop. Outro problema desse circuito é que nem todo ampop pode funcionar corretamente com ele, sendo indicado uma fonte simétrica.
