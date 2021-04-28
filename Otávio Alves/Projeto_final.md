# PROJETO FINAL
## Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
![figura01](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/figura%2001.png)
- A tensão de saída do ampop será aproximadamente a tensão de alimentação. 
- Primeiramente deve-se considerar o diodo zener conectado à entrada não-inversora do amplificador, isso irá limitar o sinal de entrada. Para o sinal de saída, os limites estão sujeitos a própria alimentação do amplificador.
- Esse circuito pode ser alimentado com uma tensão maior que a tensão requerida de saída do regulador somada a queda de tensão de VDS. VCC = VOUT + VDS
## Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?
### Circuito proposto (01) para a alimentação do AmpOp:

![circuito01](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/circuito%2001%20alimenta%C3%A7%C3%A3o.png)

- Calculando Vcc

![calculo_vcc](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/calculo%20vcc.png)
- A desvantagem desse circuito acredito que seja o ripple de saída, já que a forma de onda de entrada é uma senoide. O capacitor C3 teria que ter um valor próximo ou similar ao capacitor usado para a retificação. A melhoria desse circuito seria a adição de um regulador linear para eliminar possíveis ruídos.

### Circuito proposto (02) para a alimentação do AmpOp:
![circuito02](https://user-images.githubusercontent.com/74318416/116098360-64f98c00-a681-11eb-86c3-de3b06bd58df.png)
## Vamos projetar esse circuito  de alimentação do AmpOp?
![projeto_alimentacao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/projeto%20circuito%20alimenta%C3%A7%C3%A3o.png)
- Qual a Tensão VGS? Descreva como obter o valor.

Datasheet(https://www.alldatasheet.com/datasheet-pdf/pdf/580586/NELLSEMI/IRF540.html)

![vgs_irf540](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/vgs%20irf540.png)

Pelo gráfico, a tensão VGS pode ser considerada 4,5V

- Qual a corrente de alimentação do AmpOp?

Datasheet(https://www.ti.com/lit/ds/snosc16d/snosc16d.pdf)

![corrente_ampop](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/corrente%20de%20alimenta%C3%A7%C3%A3o%20ampop.png)

I = 1.5mA & Imax = 3.0mA

- Qual a tensão de alimentação do AmpOP?

Datasheet(https://www.ti.com/lit/ds/snosc16d/snosc16d.pdf)

![tensao_ampop](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20de%20alimentacao%20ampop.png)

Vmax = 32V 

- Qual fator devo considerar para escolher o transistor Q1?
- 
O beta precisa ser elevado.

- Qual valor da tensão do diodo zener D6?
-
![tensao_diodo_zener](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20diodo%20zener.png)

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito? 

O zener precisa da menor impedância possível para evitar oscilações na corrente.

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?
