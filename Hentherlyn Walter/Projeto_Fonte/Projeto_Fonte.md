# Projeto Final

## Parte 1

### Circuito 1

Primeira figura

#### Qual relação entre a tensão de alimentação do ampop e a tensão de saída?

   A tensão de saída depende da tensão de alimentação do AmpOp, pois o AmpOp tende a saturar quando a tensão de saída se tende à tensão de alimentação.

#### O que devemos considerar para esse circuito operar como um LDO?

   Para este circuito operar como um LDO devemos utilizar a equação ilustrada abaixo.
    
   Vin >= Vout + Vdo
    
   Onde:
   Vin - Tensão de entrada que é limitada pelo diodo Zenner escolhido.
   Vout - Tensão de saída que é limitada pelo AmpOp escolhido.
   Vdo - Tensão do Zenner

#### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

   A tensão de alimentação do AmpOp deve ser no mínimo a soma da tensão de saída (Vout) com a tensão de polarização do mosfet (Vgs).

#### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

Figura do circuito dobrador de tensão

   Para o circuito dobrador de tensão devemos utilizar a equação descrita abaixo:
    
   Vcc = 2*Vin*sqrt(2) - VD4 - VD5
   Vcc = 2*12*sqrt(2) - 0,7 - 0,7 = 32,54 V

####  Quais problemas apresentam esse circuito?

   Este circuito apresenta ruído na tensão de saída devido à tensão de ripple existente.

#### Podemos melhorar?

  Podemos melhorar o desempenho do circuito adicionando um regulador linear na saída do dobrador para limitar a tensão de alimentação do AmpOp.

### Circuito 2

#### Alimentação do AmpOp: Considere AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V

#### Qual a Tensão VGS? Descreva como obter o valor.

#### Qual a corrente de alimentação do AmpOp?

#### Qual a tensão de alimentação do AmpOP?

#### Qual fator devo considerar para escolher o transistor Q1?

#### Qual valor da tensão do diodo zener D6?

#### Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito? 

#### Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

## Parte 2

#### A) Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes

#### B) Circuito referência de tensão zener (R1 e D3):
##### B.1) Quais fatores devo considerar para escolher o diodo zener para essa aplicação? 


##### B.2) Qual a influência da regulação de linha e da regulação de carga para este circuito?


##### B.3) Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear? 


#### Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?
