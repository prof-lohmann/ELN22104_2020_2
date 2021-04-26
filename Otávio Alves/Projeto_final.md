# PROJETO FINAL
## Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
- A tensão de saída do ampop será aproximadamente a tensão de alimentação. Esse circuito pode ser alimentado com uma tensão maior que a tensão requerida de saída do regulador somada a queda de tensão de VDS. VCC = VOUT + VDS
## Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?
![calculo_vcc](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/image.png)
- A desvantagem desse circuito acredito que seja o ripple de saída, já que a forma de onda de entrada é uma senoide. O capacitor C3 teria que ter um valor próximo ou similar ao capacitor usado para a retificação.
