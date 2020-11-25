# ELN22104_2020_2


# Atividade 01
## Questão 1
Adimitindo que o ponto + de _Vo1_ seja o nó "a", o ponto - de _Vo1_ seja o nó "b" e a referência sendo o terra (ground = 0). Analisando, temos uma tensão de _Va_ = 12V e _Vb_ = -12V, sendo assim, podemos ter como resultado o valor da tensão de saída como _Vo1_ = 24V. Pela Figura vemos que a corrente em cima de _I(R1)_ = 24A, observando que a resistência de _R1_ = 1ohm, conclui-se que _Vo1_ = 24V.

Adimitindo que o ponto + de _Vo2_ seja o nó "a", o ponto - de _Vo2_ seja o nó "b" e a referência sendo o terra (ground = 0). Analisando, temos uma tensão de _Va_ = 12V e _Vb_ = 8V, sendo assim, podemos ter como resultado o valor da tensão de saída como _Vo2_ = 4V. Pela Figura vemos que a corrente em cima de _I(R2)_ = 24A, observando que a resistência de _R2_ = 1ohm, conclui-se que _Vo2_ = 4V.

![Circuito 1](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%201%20a.PNG)
![Circuito 2](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%201%20b.PNG)

## Questão 2
Fazendo LKT, podemos equacionar o circuito da seguinte forma: _((Vo-5)/10000) + ((Vo+10)/5100) = 0_. Sendo assim temos como resultado _Vo = -4,93V_, com _Vo_ podemos calcular as correntes sendo _I(R1) = (Vo-5)/10000 = -993,38mA_ e _I(R2) = ((Vo+10)/5100) = -993,38mA_.

![Circuito 3](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%202.PNG)

## Questão 3
Anisando o Circuito, pode-se observar que ao fazer o paralelo de _R1//R3_; _R2//R4_, obtem-se um circuito em série. Sendo assim, _Req = R1//R3 + R2//R4 = 6621,42441ohm_, pode-se calcular o valor da corrente com: _Itotal = (12+10)/Req = 3,32mA_. Sabendo _Itotal_ podemos obter as tensões em cima dos resistores equivalentes: _VR13 = (R1//R3) * Itotal = 8,2439V_ e _VR24 = (R2//R4) * Itotal = 13,7561V_. Por fim, pode-se obter os valores de corrente: _IR3 = VR13 / 3300 = 2,49816mA_ e _IR4 = VR24 / 22000 = 625,277uA_. Portanto _I = IR3 - IR4 = 1,87288mA.

![Circuito 4](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%203%20Eq..PNG)
![Circuito 5](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%203%20Eq..PNG)

## Questão 4
Fazendo equivalente em série do circuito na direita, temos _Req = 3300 + 1200 = 4500ohm_, calcula-se a corrente _IR2 = 9 / 4500 = 2mA_, _VR2 = 1200 * IR2 = 2,4V_. Sabendo o valor de _VR2_, calcula-se o valor da fonte de corrente controlada por _VR2_: _Icontroler = 10*10^(-3) * VR2 = 24mA_, sendo assim, podemos obter o valor de _VR3_: _VR3 = 10000 * (-24*10^(-3)) = -240V.

![Circuito 6](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Atividade%201/Figura%204.PNG)

## Questão 5

1. NETLIST - Representação da analise dos circuitos no formato de caixa de texto.
2. O circuito é analisado pela LKT usando os nós definidos pelo LTspice.
3. 
4. Label é um indicador para nomear os nós que você esta definindo, auxilia em descobrir quais tensões e correntes especificas que voce precisa descobri-las.
5. Resistor (tecla r), Capacitor (tecla c), indutor (tecla l), terra (tecla g), Fonte de tensão (tecla v) e Ampop's.
6. É um sub-circuito, por exemplo, um ampop é feito com uma composição de varios componentes (transistores, diodos, resistores...).
7. 

## Questão 6

1. .Tran - é uma analise transiente não linear do circuito, que plota a forma de onda, usados em fontes ACs.

![Circuito 7]()

2.
3.
4.
5.
6.
7.
