# Atividade 2

## Questão 1
## A)

Um amp-op é um amplificador com um ganho muito alto que possui duas entradas, uma inversora (V-) e uma não inversora (V+). A tensão de saída é a diferença entre as entradas “não inversora” com a “inversora”, multiplicado pelo ganho (Av) em malha aberta.

## Questão 2

Características: Impedância de entrada infinita, ganho em malha aberta (Av) infinito, frequência de ganho unitário infinito, impedância de saída nula.

![Simbolo](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/simbolo-ampop.jpg)

## Questão 3

  O ganho de malha aberta é uma configuração sem realimentação do retorno da saída do amp-op à sua entrada, limitado pela tensão Vcc conforme figura 1, ao passar do limite Vcc o amp-op passa a ser saturado.
  O ganho de malha fechada é uma configuração que tem um caminho de realimentação negativo do retorno de saída do amp-op à sua entrada.

## Questão 4
![Figura 4](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/4FI.PNG)
![Resolução 4](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/4reso.PNG)

## Questão 5
### a) Buffer:
 Um circuito buffer fornece um meio de isolar um sinal de entrada de uma carga ao utilizar um estágio com ganho unitário de tensão, sem inversão de fase ou polaridade, e agir como um circuito ideal com impedância de entrada muito alta e impedância de saída muito baixa.
![Buffer](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/Buffer.PNG)
### b) Amplificador Inversor:
 O multiplicador de ganho constante inversor, que fornece um ganho ou amplificação precisos, tendo na saída o sinal invertido ao da entrada.
![Amplificador Inversor](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/Ampop%20inver.PNG)
### c) Amplificador Não Inversor:
 O multiplicador de ganho constante Não inversor, que fornece um ganho ou amplificação precisos, não tendo na saída o sinal invertido ao da entrada.
![Amplificador Não Inversor](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/ampop%20nao%20inv.PNG)
### d) Amplificador Somador Inversor:
 Sendo a saída a soma das entradas, cada uma multiplicada por um ganho diferente, com a inversão do sinal na saída.
![Amplificador Somador Inversor](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/Somador%20inver.PNG)
### e) Amplificador Somador Não Inversor:
 Sendo a saída a soma das entradas, cada uma multiplicada por um ganho diferente, não tendo inversão do sinal na saída.
![Somador Não Inversor](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/Somador%20nao%20inver.PNG)
### f) Subtrator:
 Empregados para proporcionar a subtração de dois sinais de entrada.
![Subtrator](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/Subtrator.PNG)
### g) Amplificador de Instrumentação:
 É um dos modelos mais especiais dos amp-op’s, na verdade este componente é desenvolvido através de um arranjo com outros amplificadores operacionais, tradicionalmente envolvendo características bastante distintas quando comparado a um amp-op de uso comum.
![Amplificador de Instrumentação](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%202/Figuras/instrumenta%C3%A7%C3%A3o.PNG)

## Questão 6

## Questão 7
 Quando os mesmos sinais de entrada são aplicados a ambas as entradas, o resultado é uma operação modo-comum. Idealmente, as duas entradas são amplificadas de maneira igual e, uma vez que produzem sinais de polaridades opostas na saída, esses sinais se cancelam, o que resulta em uma saída de 0 V. Na prática, o resultado é um pequeno sinal na saída.

## Questão 8
 Quando dois sinais da mesma amplitude, freqüência e fase são aplicados às entradas (inversora e não inversora) de um operacional eles devem se cancelar e nenhuma saída deve ocorrer.
 
## Questão 9

## Questão 10
 Um amplificador operacional com entrada e saída Rail to Rail alimentado com 5V pode aceitar sinais de ate 5Vpp na entrada sem saturar e dar o mesmo sinal de 5Vpp na saída, é como se ele tivesse um controle de ganho automatico integrado.
 
## Questão 11
 A saída do amp-op deverá ser 0 V quando a entrada for 0 V, na prática, geralmente há alguma tensão de offset na saída. Por exemplo, quando aplicarmos 0 V a ambas as entradas do amp-op e então medirmos 26 mV (CC) na saída, essa tensão será indesejada e gerada pelo circuito, e não pelo sinal de entrada. Mas, visto que pode-se construir o circuito amplificador para operar com vários ganhos e polaridades, o fabricante especifica uma tensão de offset de entrada para o amp-op. A tensão de offset de saída é, então, calculada a partir da tensão de offset de entrada e do ganho do amplificador, conforme determinado pelo projetista.

## Questão 12
 As duas entradas devem estar balanceadas em termos de corrente contínua. As duas entradas devem “enxergar” a mesma resistência DC; manter a temperatura ambiente constante e  utilizar fonte de alimentação estabilizada.
## Questão 13

### Datasheet:
 Achando o _Vio_, você obtém a Tensão de offset na entrada.
## Questão 14
 Os amplificadores operacionais apresentarem uma resistência de entrada não infinita, característica que se associa apenas aos sinais dinâmicos aplicados, a natureza própria dos transístores obriga à existência de correntes não nulas através dos terminais de entrada, V+ e V-, designadas correntes de polarização, as quais, por acção do desemparelhamento inexorável entre componentes, são, também, distintas entre si, estas correntes associam-se à corrente na base dos transístores bipolares, e às correstes de fuga ou de saturação inversa nos transístores de efeito de campo.
