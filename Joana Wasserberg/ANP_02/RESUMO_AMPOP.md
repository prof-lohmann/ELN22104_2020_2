## Eletrônica 1 2020.2 
## Joana Wasserberg
---



## RESUMO AMPLIFICADORES OPERACIONAIS
-------------------------------------------------------------


### 1. O que é o AmpOp? 
Um Amplificador Operacional, em teoria, é amplificar um sinal da forma mais próxima que ele é recebido apenas alterando a sua amplitude. O AMPOP é um circuito muito versátil, pode-se fazer quase tudo em eletrônica com ele, seu circuito integrado possui características muito próximas das consideradas ideais, ou seja, o AMPOP opera muito perto da amplificação de sinal propriamente dita, sem tantas interferências.


### 2. Mostre os simbolos e as características do AmpOp IDEAL.

![Simbolos AmpOp](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_02/Imagens/Simbolos%20Ampop.PNG)

O AmpOp é projetado para operar como um sensor da diferença entre os sinais de tensão aplicados em seus dois terminais de entrada. Essa diferença é multiplicada por um certo valor *A* que resulta em uma tensão na saída do AmpOp. O ganho *A* é chamado ganho diferencial, ou ganho de malha aberta e no AmpOp ideal ele é infinito.

```
 Vout = A * (V+ - V-)
 ```

Na idealidade, o AmpOp não apresenta corrente na entrada, logo, nos terminais 1 e 2, a corrente é igual a zero. Em outras palavras, a impedância de entrada do AmpOp é supostamente infinita.
No terminal 3, a impedância de sáida é supostamente igual a zero. É como um terminal de uma fonte de tensão ideal, a tensão será sempre a mesma em relação ao terra não importando a corrente que possa ser drenada por alguma impedância.
O AmpOp ignora qualquer sinal comum em ambas as entradas, nomeia-se essa propriedade como *Rejeição de Modo Comum*.


### 3. O que significa Malha Aberta e Malha Fechada? 
Malha aberta é quando o AmpOp é considerado sem realimentação não tendo um circuito. Malha fechada  é quando o AmpOp está num circuito com realimentação, sendo positiva ou negativa.


### 4. Exemplifique como resolver e calcular circuitos com AmpOps em Malha Fechada. 

Para circuitos em malha fechada, a equação é semelhante a de malha aberta e depende das características do circuito. O Ganho é dado por *G* e a equação fica

```
Vout = G * (V+ - V-)
```
Para exemplificar, alguns exemplos de AmpOp em malha fechada para calcular G.

### **AmpOp Inversor**

![Ampop inversor](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_02/Imagens/Ampop%20Inversor.PNG)

Para o AmpOp como inversor, o ganho é dado por:


```
Vout = (- R1/R2) * (V+ - V-)
```

### **AmpOp Não Inversor**

![Ampop não inversor](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_02/Imagens/Ampop%20n%C3%A3o%20inversor.PNG)

Para o AmpOp como não inversor, o ganho é dado por:

```
Vout = (1 + R1/R2) * (V+ - V-)
```

### **Característica Mista**

![Ampop diferencial](https://github.com/joananana/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Joana%20Wasserberg/ANP_02/Imagens/Ampop%20diferencial.PNG)

Caso o AmpOp esteja com alimentação nas duas entradas, utilizamos o método de superposição de fontes. Curto-circuitamos uma de cada vez, calculamos os valores de Vout e somamos os valores finais. Para o exemplo da figura teríamos duas configurações, um inversor e outro não inversor.

```
Vout = V' + V"

Vout = V1*(-R1/R2) + V2*(R4/(R4 + R3))*(1 + R1/R2)
```

### 5. Descreva as principais características das topologias: 
### a) Seguidor de Tensão (Buffer) 
O Buffer possui realimentação negativa, onde o Vin é muito próximo do Vout. A alta impedância é deslocada para a saída.


### b) Amplificador Inversor.
O amplificador inversor, tem o ganho dado por G = - R1/R2, ou seja, ele inverte atrasa o sinal de entrada em 180º de acondo com Vin, além de amplificá-lo.


### c) Amplificador Não Inversor.
O Não inversor tem o ganho positivo e Vout é sempre o dobro de Vin.



### d) Amplificador Somador Inversor.
O amplificador somador tem esse nome pois sua saída é a soma ponderada dos sinais de entrada.
Sua fórmula geral é dada por:
```
Vout = - (Rf/R1 * V1 + Rf/R2 * V2 + ... + Rf/Rn * Vn)
```


### e) Amplificador Somador Não Inversor.
O amplificador somador não inversor as entradas na saída não-inversora.

### f) Amplificador Subtrator.
O amplificador subtrator permite realizar a subtração (diferença) de dois sinais. O subtrator é muito utlizado para medir corrente.

### g) Amplificador de Instrumentação. 
O amplificador de instrumentação é uma versão mais precisa do amplificador subtrator e não apresenta tantos problemas quanto este. A saída do circuito é dada pela equação:
```
Vout = (-R4/R3)(1 + 2*R2/R1)(V+ - V-)
```
### 6. Explique o efeito do ganho em MALHA ABERTA FINITO, para as topologias Amplificador Inversor e Amplificador não inversor. 
O ganho em malha aberta finito é consequências das não idealidades dos AmpOps, então mesmo sendo muito próximo da idealidade, ainda apresenta características que não são ideais.
Dessa forma, para as diferentes topologias, consideramos as não idealidades como tensão de offset, corrente de polarização, tensão de modo comum.

**AmpOp Inversor não ideal**
```
G = (- R2/R1) / (1 + 1/A + R2/A*R1)
```

**AmpOp nãp inversor**
```
G= (R2/R1 + 1) / (1 + 1/A + R2/R1) 
```
### a) Exemplifique com circuitos com ganhos em malha fechada elevado (Ex. 1000V/V e -1000V/V) e com ganhos menores (Ex. 10V/V e -10V/V ), faça a comparação com erros percentuais e utilize uma variação de ganho em malha aberta entre 120dB e 20dB. 
### b) Dica veja o problema 2.20 pg 83 do livro texto. 

Analisando os resultados, podemos concluir que um ganho em malha aberta baixo pode alterar muito a tensão de saída do circuito. Portanto, é importante saber o ganho em malha aberta do AmpOp para a faixa de frequência em que ele irá operar.


### 7. Explique o que é a tensão de modo comum(VCM) e quais os efeitos desta tensão nas topologias estudadas. 
Em algumas aplicações, os AmpOps acabam tendo uma tensão de modo comum nos seus terminais de entrada. Esse é um caso muito comum para o amplificador subtrator e de instrumentação quando utilizados para medir a tensão de um resistor, por exemplo:
Vout = A*(V+ - V-) + Acm(Vcm)
Onde Vcm é a tensão de modo comum e Acm é o ganho para tensão de modo comum. Esse é um dos principais problemas enfrentado pelo Amplificador Subtrator.


### 8. O que é CMRR? 
CMRR ou Common Mode Rejection Ratio (Razão de Rejeição em Modo Comum) é uma característica muito importante dos AmpOps. Ela especifica o ganho em modo comum do amplificador em relação ao ganho em malha aberta, sendo o ganho de modo comum idealmente nulo.


### 9. Utilizando o Amplificador Subtrator com ganho 1000V/V, demonstre o efeito da tensão de modo comum (VCM), indicando: 
a) o impacto na tensão de saída com relação a tolerância dos resistores no circuito; 
b) Qual erro na tensão de saída com relação CMRR do AmpOp. 
c) Dica de exemplos com valores diferentes de tensão de modo comum (VCM) . Faça o mesmo circuito com resistores com tolerâncias bem distintas, ex. 1% e 5%. Atividade 01 2/2 

### 10. Faça um resumo explicando as limitações de tensão de entrada e saída de um AmpOp. De exemplos, utiliza-se valores de datasheet. 

### a) Defina o que é um AmpOp Rail-to-rail.

Os AmpOps Rail-to-Rail são mais precisos e alcançam em sua saída uma tensão muito próxima da alimentação

### 11. O que é tensão de offset? Como calcular o efeito resultante na tensão de saída de um amplificador inversor? 

 A tensão de Offset é um sinal parasita que aparece na saída do circuito do AmpOp. Ela é comumente modelada como uma fonte de tensão na entrada não inversora do AmpOp.
 

### 12. Como minimizar o efeito da tensão de offset?
Em circuitos em corrente alternada, é possível colocar um capacitor na saída do ampop para minimizar o efeito da tensão de offset. Alguns AmpOps também possuem dois terminais extras onde pode ser conectado um potenciômetro para anular os efeitos do offset.


### 13. O que é a variação da tensão de offset pela temperatura? a) Como verificar esse parâmetro no datasheet? 

A tensão de offset pode variar dependendo da temperatura. Os datasheets dos componentes geralmente apresentam dois valores de offset. Um valor típico e um valor que é dado junto com uma faixa de temperatura.


### 14. O que são as correntes de polarização(Ibias) de AmpOp? a) Como minimizar o efeito destas correntes? Descreva as aproximações e os possíveis circuitos para mitigar o problema. b) Descreva a corrente de offset na polarização dos AmpOp

Idealmente, não há passagem de corrente nos terminais de entrada dos AmpOps. Na prática, há passagem de uma corrente muito pequena por essas entradas, por isso, geralmente são desprezadas. Em algumas aplicações, as correntes de polarização podem gerar erros.

Os fabricantes de AmpOps geralmente especificam o valor médio das correntes de polarização.
