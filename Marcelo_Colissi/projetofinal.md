#### Projeto Final
### MARCELO COLISSI HABOWSKI

## PARTE I: ENTENDENDO UM REGULADOR LINEAR
#### Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
![fig01](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSPROJETOFINAL/FIGURA1.png)
## RESPOSTA:
A tensão de saída do ampop será aproximadamente a tensão de alimentação. Primeiramente devemos considerar o diodo zener conectado à entrada não-inversora do amplificador, isso irá limitar o sinal de entrada. Para o sinal de saída, os limites estão sujeitos a própria alimentação do amplificador. Esse circuito pode ser alimentado com uma tensão maior que a tensão requerida de saída do regulador somada a queda de tensão de VDS. VCC = VOUT + VDS

#### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?


#### Circuito proposto (número 1) para a alimentação do AmpOp:
![circuito1](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSPROJETOFINAL/CIRCUITO1.png)

## RESPOSTA:

Cálculo do Vcc:
-Nos diodos VD4 e VD5 consideraremos a queda de tensão com valor de 0.7V e a tensão de entrada é 12V, portanto:
Vcc = 2*Vin*√2 - VD4 - VD5 
Vcc = 32,541 V 


Como a forma de onda da entrada é uma senóide, eu defendo que o Ripple de saída sejá uma desvantagem neste circuito. O capacitor C3 teria que ter um valor próximo ou similar ao capacitor usado para a retificação. A melhoria desse circuito seria a adição de um regulador linear para eliminar possíveis ruídos.

#### Circuito proposto (número 2) para a alimentação do AmpOp:
![circuito2](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSPROJETOFINAL/CIRCUITO2.png)

##### CIRCUITO PROPOSTO 02

## Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.
## DATASHEET UTILIZADO:
https://pdf1.alldatasheet.com/datasheet-pdf/view/580586/NELLSEMI/IRF540.html


#### Qual a Tensão VGS? Descreva como obter o valor.
Resposta:A tensão Vgs para 1A é de aproximadamente 4V
 
![figuraVGS](https://github.com/MarceloColissiH/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Marcelo_Colissi/FOTOSPROJETOFINAL/VGS.png)

####  Qual a corrente de alimentação do AmpOp?

Resposta: Corrente Mínima: 1mA 
          Corrente Máximia: 3mA


####  Qual a tensão de alimentação do AmpOp?

Resposta: O Vcc  pode variar entre 16V e 32V, portanto 32V é o máximo


####  Qual fator devo considerar para escolher o transistor Q1?

Resposta: Há a necessidade de escolher um transistor que possua a constante beta elevada , para que a corrente de base de Q1 seja menor que a corrente do zener.

####  Qual valor da tensão do diodo zener D6?

Resposta: Aproximadamente 24V 

####  Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

Resposta: Um zener com resistência baixa, para que transite o menor valor de corrente possível tornando o sistema mais estável

####  Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

Resposta: Sim, porém, temos que nos atentar para que a corrente de alimentação atinja o valor mínimo necessário
