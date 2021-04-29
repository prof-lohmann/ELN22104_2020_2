# Atividade 3
Aluno: 
* Alexsander Vieira - <alexsander_vieira@hotmail.com>
 
Professor: 
* Daniel Lohmann
 
## Simulação de circuitos com Amplificadores operacionais AD8040 e AD8539.

<p align="justify">
Características dos amplificadores AD8040 e AD8539
</p>

|   |   AD8040  |   AD8539  |
| - |   --- |   --- |
|Tensão alimentação max|12 V|8 V|
|Tensão alimentação min|2,7 V|2,7 V|
|Tensão de modo comum|- 5.2 V até + 5.2 V|0V até 5V|
|CMRR|80 dB|135 dB|
|Tensão entrada max|VDD +0,5 V| VDD + 0.3 V|
|Tensão entrada min|VDD + 0.3 V|VSS − 0.3 V|
|Tensão de offset|1,6 mV|13 uV|
|Corrente de polarização|1.3 uA|25 pA|
|Consumo de corrente|1.5 mA|210 uA|
|Ganho de malha aberta|74 dB|130 dB|
|Impedância de entrada|6 MΩ|não encontrado|

### Simulações - Item 2

AD8040

<p align="center">
    <img src="Atividade3_01.PNG" width="90%">
    <br><br>    
</p>

AD8539

<p align="center">
    <img src="Atividade3_02.PNG" width="90%">
    <br><br>    
</p>

<p align="justify">
Como pode ser verificado nas simulações as tensões de saturação são respectivamente +/- 5 e +/- 2,5.
</p>

### Simulações - Item 3

<p align="center">
    <img src="Atividade3_03.PNG" width="400">
    <br><br>    
</p>

AD8040

<p align="center">
    <img src="Atividade3_04.PNG" width="90%">
    <br><br>    
</p>

<p align="center">
    <img src="Atividade3_05.PNG" width="90%">
    <br><br>    
</p>

AD8539

<p align="center">
    <img src="Atividade3_06.PNG" width="90%">
    <br><br>    
</p>

<p align="center">
    <img src="Atividade3_07.PNG" width="90%">
    <br><br>    
</p>

<p align="justify">

Ao aplicar tensão de entrada igual a 0 V foi possível verificar a tensão de offset dos amplificadores operacionais utilizados, respectivamente 169,8 mV e 1,39mV.
Ambos valores estão dentro do esperado considerando o ganho -100V/V aplicado ao circuito.
Ao realizar a simulação aplicando um sinal senoidal de 10m V, 1KHz foi possivel verificar o deslocamento provocado pela diferença de tensão de offset dos amplificadores.

</p>

### Simulações - Item 4

<p align="center">
    <img src="Atividade3_08.PNG" width="400">
    <br><br>    
</p>

AD8040

<p align="center">
    <img src="Atividade3_09.PNG" width="90%">
    <br><br>    
</p>

<p align="center">
    <img src="Atividade3_10.PNG" width="90%">
    <br><br>    
</p>

|Vin [V]|   Vout(teorico) [V]  |   Vout(simulado) [V]  |   Erro [%]    |
| - |   --- |   --- |   --- |
| 5m  |   50m |   34,7m |   44 |
| 50m |   500m |   484,6m |   3,18 |
| 200m |   2 |   1,98 |   1,01 |
| 200m |   5 |   4,96 |   0,8 |

AD8539

<p align="center">
    <img src="Atividade3_11.PNG" width="90%">
    <br><br>    
</p>

<p align="center">
    <img src="Atividade3_12.PNG" width="90%">
    <br><br>    
</p>

|Vin [V]|   Vout(teorico) [V]  |   Vout(simulado) [V]  |   Erro [%]    |
| - |   --- |   --- |   --- |
| 5m  |   50m |   50,14m |   0,2 |
| 50m |   500m |   500,14m |   0,2 |
| 200m |   2 |   2 |   0 |
| 200m |   5 |   2,48 |   101,6 |

<p align="justify">

Após analisar os resultados obtidos acredito ser correto afirmar que o ampop mais correto a ser utilizado no caso mencionado será o AD8539, isso pois durante a maior parte do tempo ele estaria operando dentro da área de operação 2,5V max. E se utilizarmos o ampop AD8040 a sua tensão de offset teria um grande impacto nos resultados.

Considerando os requisitos do caso descrito pelo professor, acredito ser correto afirmar que o ampop ISL28233, teria performance satisfatória para o caso. Este possui uma baixa tensão de offset, apresenta uma ganho adequado em baixa frequencia e possui tensão de saturação +/-3V oque esta dentro dos parametros de operação solicitados.

</p>

<p align="center">
    <img src="Atividade3_13.PNG" width="90%">
    <br><br>    
</p>

<p align="center">
    <img src="Atividade3_14.PNG" width="90%">
    <br><br>    
</p>

Referencia: [br.mouser.com/datasheet/2/698/REN_isl28233_433_DST_20080205-1528811.pdf](https://br.mouser.com/datasheet/2/698/REN_isl28233_433_DST_20080205-1528811.pdf)

