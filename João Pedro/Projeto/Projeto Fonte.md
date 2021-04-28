# Projeto Fonte

## Parte 1

### a) A tensão de saída está relacionado com alimentação do ampop, pois a tensão de alimentação do ampop limita os valores da tensão de saída para não saturar o sinal.

### b) Podemos observar que a entrada não inversora (+), está conectada ao diodo zener (D3), onde zenner (D3) será uma tensão de refêrencia para a tensão de sáida do circuito... 

### c) A tensão de alimentação do ampop deve possuir no mínimo uma amplitude de _Vout + Vgsmin_ conforme visto na Figura 2. Onde _Vgsmin_ é a tensão mínima para a polarização do mosfet e _Vout_ é a tensão de saída.

![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Circuito1.PNG)
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Tens%C3%A3o%20minima%20para%20alimenta%C3%A7%C3%A3o%20do%20ampop.PNG)

### Proposta de Circuito 1
#### a) De acordo com a equação a baixo, podemos resultar, considerando as tensões dos diodos de 0,7V, um Vcc = 32,54V.
#### b) Como o circuito dobrador de tensão depende diretamente de Vin, podendo variar muito, é possível que a tensão supera o valor máximo de alimentação do ampop. Adicionalmete tem o ripple do capacitor que pode não suprir a tensão miníma desejada.
#### c) É possível regular a tensão de saída com um circuito _regulador de tensão_.

![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Circuito2.PNG)
![](https://github.com/JoaoPedrogrb/ELN22104_2020_2/blob/main/Jo%C3%A3o%20Pedro/Projeto/Imagens/Equa%C3%A7%C3%A3o%20do%20Vin12V.PNG)

### Proposta de Circuito 2
