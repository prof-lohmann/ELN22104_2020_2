# Projeto Fonte

## Parte 1

### a) A tensão de saída está relacionado com alimentação do ampop, pois a tensão de alimentação do ampop limita os valores da tensão de saída _Vout_ para não saturar o sinal.

### b) Para o circuito ser considerado LDO, a tensão na saída deve ser um valor baixo. 

### c) Para obter a tensão de alimentação do ampop, será uado um dobrador de tensão, olhando na figura 2, temos a equação que dará nossa tensão Vcc.

![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Circuito1.PNG)

### Proposta de Circuito 1
#### a) De acordo com a equação a baixo, podemos chegar a um resultado, considerando as tensões dos diodos de 0,7V.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Equa%C3%A7%C3%A3o%20do%20Vin12V.PNG)
#### b) Como o circuito dobrador de tensão, os capacitores irão adicionar um ripple na tensão de saída que fará com que a tensão não seje a desejada. 
#### c) É possível regular a tensão de saída com um circuito _regulador de tensão_, fazendo com que diminua o ripple.


### Proposta de Circuito 2
#### a) A tensão _Vgs_ é encontrada pelo gráfico do datasheet do componente, sendo assim, _Vgs_= 4,5 V.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/grafico%20vgs.PNG)

#### b) A corrente é encontrada no datasheet, Admiteindo o _Vcc_= 30V, temo que a corrente de alimentação _Icc_ fique na faixa de 1,5mA a 3,0mA.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Icc.PNG)

### c) Tensão de alimentação, encontrada no ampop é de _Vcc_= 32V.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Vccal.PNG)

### d) Alto valor do beta do transitor.

### e) Pela equação abaixo o valor do Zenner do Dobrador de Tensão deverá ser maior que _Vscc_ = 19,5 V.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Vscc.PNG)

### f) Precisará escolher o zenner que possuí a menor impedência para evitar variações no valor da corrente.

### g) Se a corrente de alimentação for maior que _Icc_ mínimo, irá funcionar.

### Circuito dobrador de tensão
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/circ%20dobr.PNG)
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Vripple.PNG)

#### Pela escolha do trasistor TIP31 possuir um beta elevado e o diodo zenner 1N5361 com imppedância baixa, obteve um ripple baixo de 0,43V e estabelecendo uma tensão de alimentação sendo _Vcc_= 26,1V

## Parte 2
### Cosiderando os valores propóstos, VD sendo a tensão reversa e IDmed sendo a corrente média, temos:
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/expre%C3%A7%C3%B5es.PNG)
O modelo escolhido para D1 e D2 foram 1N4007G, de acordo com os parâmetros adotados, portanto, a tensão reversa _VD_ é maior do que a que foi calculada. A tensão reversa do diodo D1 e D2 são de 1000V.

#### Levando em consideração o tempo de polarização do diodo, podendo ser calculado o _tcod_, sabendo que a tensão de polarização é de 0,7V, por fim, sabe-se a porcentagem do ciclo a ser usada.
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/tempo.PNG)

### b) Apresentando o circuito
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/circui2.PNG)
#### O diodo zenner deve possuir menor impedância, pois sua tensão varia muito, portanto, a escolha foi o diodo zenner 1N4733 possuindo uma tensão zennner 5,11V e corrente zenner 49mA.
#### O diodo zenner tende a manter a tensão de saída constante. Sendo assim, aumenta ou diminuição da queda de tensão sobre o resistor R1, ao qual tem como função de limitar a corrente do zenner, Portanto, Tudo que variar no diodo zenner será multiplicado pelo ganho e refletirá na saída.

#### Calculando o R1 temos que:
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Zenner.PNG)

#### O transistor Q4 limita a tensão sobre o resistor R1, os mesmo definem a corrente de saída da fonte de forma independente a tensão de alimentação. O resistor R5 causa a queda de tensão entre o coletor de Q4 e o ground, enquanto o transistor Q3 mantém o a tensão _Vce_ de Q4 estável, reduzindo assim, variações secundárias da corrente de saída com a tensão de alimentação. Para esta aplicação foi escolhido o transistor BC53PA. O R1 já foi dimensionado anteriormente e o R5 deve obedecer:
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/R5.PNG)
