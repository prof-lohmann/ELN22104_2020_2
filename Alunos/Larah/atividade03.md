Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.

1.Verifique no datasheet dos Ampops indicados os valores dos itens abaixo:

- Máxima e mínima tensão de alimentação
- Tensão de modo comum
- CMRR
- Máxima e mínima tensão de entrada
- Tensão de offset
- Corrente de polarização
- Consumo de corrente
- Ganho em malha aberta
- Impedância de entrada

AD8040: Tensão máxima de alimentação 12V e mínima 2,7V

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8040.tabelageral.PNG)

AD8539: Tensão máxima de alimentação 5,5V e mínima 2,7V

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.tabelageral.PNG)

Para todas simulações abaixo utilize a alimentação simétrica recomendada no datasheet.

2.Simule um circuito seguidor de tensão com cada um dos ampops indicados e verifique os efeitos decorrentes da máxima e mínima tensão de entrada.

AD8040

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD840.buffer.anp03.esquematico.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8040.buffer.anp03.GRAFICO.Vin.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8040.buffer.anp03.GRAFICO.Vo.PNG)

AD8539

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.buffer.anp03.esquematico.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.buffer.anp03.GRAFICO.Vin.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.buffer.anp03.GRAFICO.Vo.PNG)


3. Simule um circuito amplificador inversor com cada um dos ampops indicados e calcule os
resistores para ter um ganho igual -100V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
2. Aplique um sinal senoidal de 10mVpp@1kHz na entrada e verifique o sinal de saída.
Explique o resultado.

AD8040

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8040.inversor.anp03.esquematico.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8040.inversor.anp03.op.PNG)

AD8539

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.inversor.anp03.esquematico.PNG)

![](https://github.com/LFRB-IFSC/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Alunos/Larah/Midias/AD8539.inversor.anp03.op.PNG)

4.Simule um circuito amplificador não inversor com cada um dos ampops indicados e calcule
os resistores para ter um ganho igual 10V/V.
1. Aplique 0V(zero) na entrada e verifique o valor da tensão na saída. Explique o resultado.
2. Aplique um sinal continuo de 5mV, 50mV, 200mV e 500mV na entrada e verifique o sinal
de saída. Qual o erro com relação ao ganho calculado? Explique o resultado.

AD8040

![](

![](

AD8539

![](

![](

Caso deseja-se projetar um amplificador subtrator com ganho de 100V/V, para sinais muito
pequenos com variação de +/-10uV até +/-30mV de muito baixa frequência, qual desses ampops
você utilizaria? Justifique a sua resposta.
Escolha um terceiro ampop com características melhores que os ampops acima para uma aplicação
como subtrator.
