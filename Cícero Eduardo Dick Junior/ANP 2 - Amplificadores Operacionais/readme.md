# Amplificadores Operacionais

## O que é o **AmpOp**?

O AmpOp é um circuito capaz de amplificar um sinal dado pela diferença de tensão entre dois sinais de entrada captados pelos terminais V+ e V- do circuito.

## Símbolos e Características do AmpOp Ideal

O AmpOp é feito com um grande número de transistores, resistores e, normalmente, um capacitor interno. Geralmente, ele é tratado como um bloco construtivo para facilitar o seu estudo e aplicação. O símbolo utilizado para representá-lo é mostrado abaixo:

#### Figura 1 - Ampop Ideal

![ampop ideal img](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/ampop%20ideal.PNG)

Os terminais **Vcc+** e **Vcc-** são para a alimentação do circuito e são, geralmente, simétricos. Os terminais **V+** e **V-** são para a entrada do sinal. Por último, o terminal **V0** é onde o sinal sai amplificado.

Como dito antes, o sinal de entrada é a diferença entre **V+** e **V-** e a saída é determinada pela seguinte equação:
```
V0 = A(V+ - V-)
```
Onde **A** é o **ganho diferencial**, ou seja, quantas vezes o sinal será amplificado. Para o AmpOp Ideal, **A** é um valor infinito. 

A equação também nos mostra que o AmpOp responde apenas à diferença de sinal e, portanto, ignora qualquer sinal comum entre ambas as entradas. A essa propriedade é dado o nome de **rejeição de modo comum** que, para o AmpOp Ideal, é infinita.

Outra característica importante do AmpOp Ideal é que suas impedâncias de entrada são infinitas, isso significa que não circula corrente nas entradas **V+** e **V-**.

## O que é **malha aberta** e **malha fechada**?
O AmpOp operando da forma mostrada na **figura 1** é considerado como um AmpOp em **malha aberta**. 

Quando um AmpOp trabalha com uma realimentação, seja positiva ou negativa, é chamado de AmpOp em **malha fechada**. Exemplo:

#### Figura 2 - Configuração inversora

![ampop inversor](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/ampop%20inversor.PNG)

## Como calcular AmpOps em Malha Fechada

Para os circuitos em malha fechada, a saída do AmpOp é obtida pela seguinte equação:
```
V0 = G(V+ - V-)
```

Onde **G** é o ganho diferencial em malha fechada e varia conforme a configuração do circuito. Vamos ver como calcular o ganho **G** para as configurações **inversora** e **não inversora**

### Configuração Inversora

A configuração inversora pode ser vista na **Figura 2**. Para esta configuração temos que o ganho G é dado pela seguinte equação: 
```
G = - R1/R2
```
### Configuração Não Inversora

#### Figura 3 - Configuração Não Inversora

![ampop nao inversor](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/ampop%20nao%20inversor.PNG)

Para esta congiguração, o ganho G é obtido à partir da equação abaixo:
```
G = 1 + R1/R2
```

#### Superposição

Eventualmente nos deparamos com circuitos onde ambas as entradas recebem um sinal de tensão, como no exemplo abaixo:

Figura 4 - Amplificador de Diferenças

![amplificador de diferenças](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/amplificador%20subtrator.PNG)

Nesse caso, usamos a técnica de superposição de fontes para calcular o ganho para a saída V0. Decompomos o circuito em dois circuitos diferentes, em um deles curto-circuitamos V1 e no outro fazemos isso com V2. Dessa forma teremos, respectivamente, um circuito inversor com V0' e um circuito não inversor com V0'' e a saída total V0 é dada por:
```
V0 = V0' + V0''
V0 = V2*(-R1/R2) + V1*(R4/(R4 + R3))*(1 + R1/R2)
```

## Principais Topologias de AmpOps em Malha Fechada

### Seguidor de Tensão (*Buffer*)

Figura 5 - *Buffer*

![buffer](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/buffer.PNG)

No caso do seguidor de tensão, o ganho diferencial é 1, isso significa que o não há amplificação do sinal, ou seja, o mesmo sinal na entrada **V+** aparece na saída **V0**.

### Amplificador Inversor

Como analisado anteriormente, no caso do amplificador inversor, o ganho G = - R1/R2, isso significa que ele inverte o sinal do sinal, além de amplificá-lo.

### Amplificador Não Inversor

Para o amplificador não inversor o ganho é positivo, por isso é chamado dessa forma. 

### Amplificador Somador Inversor

Figura 6 - Amplificador Somador Inversor
![somador inversor](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/somador%20inversor.PNG)

O amplificador somador tem esse nome pois sua saída é a soma ponderada dos sinais de entrada. Ele pode ser calculado utilizando superposição.

### Amplificador Somador Não Inversor

Figura 7 - Amplificador Somador Não Inversor
![Somador nao inversor](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/Somador%20nao%20inversor.PNG)

### Amplificador Subtrator

O amplificador subtrator é a topologia apresentada na Figura 4. Muito utilizado para medir corrente. 

### Amplificador de Instrumentação

Figura 8 - Amplificador de Instrumentação
![amplificador de instrumentaçao](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/amplificador%20de%20instrumentaçao.PNG)

O amplificador de instrumentação é uma versão mais precisa do Amplificador Subtrator e não apresenta tantos problemas quanto seu antecessor. A saída do circuito é dada pela equação:
```
v0 = (-R4/R3)(1 + 2*R2/R1)(Va-Vb)
```
## Ganho em Malha Aberta Finito

O ganho em malha aberta de um AmpOp é **idealmente** infinito. Na prática, seu ganho é bastante elevado, no entanto, **finito**. Geralmente chamado de **A**, esse ganho pode variar dependendo da frequência dos sinais de entrada do AmpOp, diminuindo conforme a frequência aumenta.

As equações para as topologias de circuitos que utilizam AmpOp também mudam se considerarmos o ganho finito. A equação para a saída da topologia inversora, por exemplo, fica da seguinte forma:
```
G = v0/v1 = (-R2/R1)/ 1 + (1 + R2/R1)/A
```

Para a topologia não inversora, a equação também muda.
```
G = v0/v1 = (1 +  R2/R1)/ (1 + (1 + (R2/R1))/A)
```

Exemplo:
Considerando o seguinte circuito:

Figura 9 - AmpOp Inversor
![Exemplo 6](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/exemplo%206.PNG)

Se considerarmos o AmpOp ideal e com ganho em malha aberta infinito, a tensão Vout fica:
```
Vout = -(R2/R1)*V1
Vout = -(10K/1K)*5
Vout = -50V
```
Considerando o ganho em malha aberta A = 1000 V/V, temos:
```
Vout = V1*[(-R2/R1)/ 1 + (1 + R2/R1)/A]
Vout = 5*[(-10K/1K)/ 1 + (1 + 10K/1K)/1K]
Vout = -49,45V
```
Considerando o ganho em malha aberta A = 10 V/V, temos:
```
Vout = V1*[(-R2/R1)/ 1 + (1 + R2/R1)/A]
Vout = 5*[(-10K/1K)/ 1 + (1 + 10K/1K)/10]
Vout = -23,81V
```
Analisando os resultados, podemos concluir que um ganho em malha aberta baixo pode alterar muito a tensão de saída do circuito. Portanto, é importante saber o ganho em malha aberta do AmpOp para a faixa de frequência em que ele irá operar.

## Tensão de Modo Comum

Em algumas aplicações, os AmpOps acabam tendo uma tensão de modo comum nos seus terminais de entrada. Esse é um caso muito comum para o amplificador subtrator e de instrumentação quando utilizados para medir a tensão de um resistor, por exemplo:

Figura 10 - Tensão de Modo Comum
![Tensao de modo comum](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/tensao%20de%20modo%20mum.PNG)

A tensão de saída de um AmpOp é dada por:
```
Vout = A*(V+ - V-) + Acm(Vcm)
```
Onde Vcm é a tensão de modo comum e Acm é o ganho para tensão de modo comum. Esse é um dos principais problemas enfrentado pelo Amplificador Subtrator.

## O Que é CMRR?

CMRR ou Common Mode Rejection Ratio (Relação de Rejeição em Modo Comum) é uma característica muito importante dos AmpOps. Ela especifica o ganho em modo comum do amplificador em relação ao ganho em malha aberta.

## Imperfeições CC

### Tensão de Saturação

Os AmpOps possuem 5 terminais: V+, V-, Vcc, Vee e Vo. Os terminais Vcc e Vee são para a alimentação do circuito. Eles também determinam a tensão de saturação de um AmpOp, isto é, a tensão máxima ou mínima que o AmpOp pode ter em sua saída. 

Idealmente, o AmpOp pode ter em sua saída uma tensão maior ou igual a Vcc. Na prática, o AmpOp não alcança a tensão de Vcc. Geralmente sua saída Vo fica 1,5V abaixo da tensão máxima ou 1,5V acima da tensão mínima. Um AmpOp com alimentação simétrica de 12V e -12V apresentaria em sua saída no máximo 10,5V ou -10,5V por exemplo.

Os AmpOps Rail-to-Rail são mais precisos e alcançam em sua saída uma tensão muito próxima da alimentação.

### Tensão de Offset

A tensão de Offset é um sinal parasita que aparece na saída do circuito do AmpOp. Ela é comumente modelada como uma fonte de tensão na entrada não inversora do AmpOp.

Figura 11 - Modelo de Offset
![offset](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%202%20-%20Amplificadores%20Operacionais/Img/offset.PNG)

Em circuitos em corrente alternada, é possível colocar um capacitor na saída do ampop para minimizar o efeito da tensão de offset. Alguns AmpOps também possuem dois terminais extras ondep pode ser conectado um potenciômetro para anular os efeitos do offset.

A tensão de offset pode variar dependendo da temperatura. Os datasheets dos componentes geralmente apresentam dois valores de offset. Um valor típico e um valor que é dado junto com uma faixa de temperatura.

### Correntes de Polarização

Idealmente, não há passagem de corrente nos terminais de entrada dos AmpOps. Na prática, há passagem de uma corrente muito pequena por essas entradas, por isso, geralmente são desprezadas. Em algumas aplicações, as correntes de polarização podem gerar erros.

Os fabricantes de AmpOps geralmente especificam o valor médio das correntes de polarização.
