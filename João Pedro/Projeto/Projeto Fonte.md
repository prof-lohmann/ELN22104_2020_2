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

#### Pela escolha do trasistor TIP31 possuir um beta elevado e o diodo zenner 1N5361 com imppedância baixa, obteve um ripple baixo de 0,43V e estabelecendo uma tensão de alimentação sendo _Vcc_= 
