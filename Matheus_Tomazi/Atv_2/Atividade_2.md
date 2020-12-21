1. Um OpAmp é um amplificador operacional, que pode dar ganho ou atenuar uma tensão de entrada, e emitir esse sinal na saída.
2. O OpAmp idel possui algumas características:\
    °Correntes de entrada nula\
    °Impedância de entrada e saída infinita e nula, respectivamente\
    °Offset da tensão de entrada igual a zero\
    °Ganho da porta Ground infinito.
3. Malha Aberta é quando a saída não esta conectada a entrada, assim nao ocorre uma realimentação
   Malha fechada é quando há uma realimentação da saída para a entrada negativa
4.  O calculo da tensão de saída é feito multiplicando o ganho pela diferença de tensões de entrada V- e V+.4
5. a)Amplificador operacional unitário ( de ganho 1).\
    b)Amplificador operacional que dá um ganho ao sinal, porém modifica a polaridade da tensão.\
    c)Amplificador operacional que dá ganho à tensão de entrada e não inverte o sinal.\
    d)Circuito que combina várias entradas de tensão e sua saída é uma soma ponderada das entradas com sinal inverso.\
    e)Circuito que combina várias entradas de tensão e sua saída é a soma ponderada das entradas.\
    f)É um OPAMP que amplifica a diferença entre dois sinais enquanto ignora sinais iguais.\
    g)É um arranjo de 3 OpAmp's e 7 resistores que servem para aplicações com controle de precisão e controle de processos.
6.  O ganho de malha aberta finita é a versão real do ganho de malha aberta infinito.\
    Vout = Av(V+ - V-) com Av finito.\
    a) OpAmp Inversor:\
     Er = (G - (R2/R1)) / Av*(R2/R1)\
     Av.......| -R2/R1 | G ......| Erro\
    10000 | 1000.... | 909 ..| 0,09\
    10000 | 10 ........| 9,98 .| 0,002\
    100.... | 1000 ....| 90,83| 0,90\
    100.....|10....... | 9,01 ...| 0,09\
    
    b) OpAmp Não Iversor:\
    Er = (G - (1+(R2/R1))) / (1+(R2/R1))\
    Av ......| 1+(R2/R1) | G ....| Erro\
    10000 | 1000 .........| 909. | 9,1  
    10000 | 10 .............| 9,99 | 0,1\
    100.... | 1000 .........| 90,9 | 90,9\
    100.... |10 ..............| 9,09 | 9,1
    
7. A VCM é a tensão média dos pinos de entrada e V+ e V-. No caso da VCM tender a infinito ou a zero, a operação será interrompida.
8. O CMRR é uma forma de anular a saída do OpAmp. Isso ocorre quando os sinais de entrada V+ e V- são identicos em questão de fase, amplitude e frequência.
9. 
10. OpAmps Rail-to-Rail são amplificadores operacionais "convencionais" que possuem duas entradas V+ e V-. Desse modo suas saídas
podem apresentar ganhos muito maiores com um valor asoluto menor em cada uma das entradas simétricas.
11. Tensão de offset é uma entrada de sinal não senoidal, responsável por deslocar a tensão de saída verticalmente. O calculo deseu impacto no sinal de saída pode ser feito por meio de uma comparação com utilização de uma tensão nula(terra).
12. Pode ser feita a redução da tensão de ofsset, seja por meio de uma modificação na fonte, ou por um divisor de tensão.
13. A variação de temperatura afeta o offset porquê na verdade ela afeta o funcionamento dos transistors que atuam na entrada de offset. Os transistors são muito sensiveis a variação de temperatura.\
    a) Nos datasheets essas informações podem vir como temperaturas em que um OpAmp trabalha corretamente, ou um grafíco demonstrando sua variação em função da temperatura.
14. É a média entre as correntes Ib+ e Ib- em resposta a tensão relativa da entrada Vcc-GND.\
    a) Para minimizar esses efeitos, basta usar resistores como divisores de corrente.\
    b) A corrente de offset de entrada é nada mais que a diferença entre as correntes de fuga e entrada dos transistors.
