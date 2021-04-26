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
