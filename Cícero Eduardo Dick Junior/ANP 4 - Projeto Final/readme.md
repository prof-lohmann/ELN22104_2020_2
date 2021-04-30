# PROJETO FINAL

## Parte 1: Entendendo o Regulador Linear

- Princípios de regulação de tensão: A regulação de tensão é o princípio de manter o sinal de saída estável, mesmo que ocorra variações no sinal de entrada.
- Tensão de saída e tensão de ripple: A tensão de ripple refere-se a variação na tensão de saída do circuito.
- Regulação de linha: A regulação de linha é a comparação na variação de tensão na entrada com a variação de tensão na saída.
- Regulação de Carga: A regulação de carga é a razão da variação de tensão pela variação de corrente na saída do circuito para diferentes cargas.
- Conceito de LDO – Low Dropout Voltage: Um circuito LDO possui uma baixa queda tensão entre sua entrada e saída.


**Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET,
temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de
saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as
tensões de alimentação para o AmpOp (VCC e VEE)?**

A tensão de alimentação deve ser alta o  suficiente para que a tensão de saída do ampop não seja saturada.

Para o circuito operar corretamente como um LDO, a tensão de saída deve ter pouca diferença da tensão de entrada, nesse caso, a tensão Vds do MOSFET deve ser mínima.

A tensão de alimentação do ampop pode ser obtitada utilizando um circuito dobrador de tensão.

### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?

O valor VCC para o sinal de 12Vrms será de aproximadamente 32,6V, pois o circuito dobrador de tensão dobra o Vp do sinal, que nesse caso seria aproximadamente 17V e há a queda de tensão nos diodos. Considerando 0,7V para cada diodo, temos:

```
2*17 - 1,4 = 32,6
```
O grande problema desse circuito é o Vripple muito alto. Para resolver esse problema, podemos implementar um regulador de tensão para amenizar esse problema.

### **Projetando o circuito de alimentação do ampop**

**Considerando Vout = 15V, Iout = 1 A, Vin+ = 12Vrms, Vripple_pós_retificador = 1V.
Qual a Tensão VGS? Descreva como obter o valor.**

A tensão Vgs deve ser suficiente para que a corrente Id do MOSFET seja de 1A. No caso do IRF540, a tensão indicada é de Vgs = 4V. Para obtermos esse valor, precisamos ter 19V na saída do Ampop que alimenta o Gate do transistor, pois:
```
Vgs = Vg + Vs = 4 + 15 = 19
```

**Qual a corrente de alimentação do AmpOp?**

A corrente de alimentação do ampop é próxima de 3mA, segundo o datasheet do componente LM324.

**Qual a tensão de alimentação do AmpOp?**

A tensão de alimentação do AmpOp deve ser maior do que a tensão de saída, que neste caso é de 19V, portanto, para deixar uma margem de erro, projetaremos com o valor de 22V.

**Qual fator devo considerar para escolher o transistor Q1?**

O transistor Q1 deve ter uma corrente de emissor baixa para não interferir no funcionamento do diodo Zener, portanto, seu fator beta deve acima de 100.

**Qual valor da tensão do diodo zener D6?**

Utilizamos um diodo zener de 22V para o circuito.

**Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?**

O diodo zener deve ter uma resistência baixa, para caso de variações de corrente no circuito.

## Parte 02 Calculando e dimensionando os componentes

**Para o primeiro bloco (D1, D2 e C1) considere vin+ = 12Vrms, Vripple_pós_retificador = 1V e I_carga = 1,1A. Justifique a escolha dos componentes.**
O bloco em questão é o retificador de onda completa. Para os diodos, os seguintes fatores devem ser considerados: tensão reversa, corrente de pico e queda de tensão.
Os diodos devem ter uma queda de tensão abaixo de 1V para que o sinal na saída não fique abaixo de 15V. Eles também precisam suportar uma tensão reversa acima de 30V. Para este circuito, podemos usar o diodo 1N4007.


O capacitor deve ser escolhido de acordo com a seguinte equação:

```
    C = Il/f*Vr = 18,33mF
```

**Circuito referência de tensão zener (R1 e D3):**

**Quais fatores devo considerar para escolher o diodo zener para essa aplicação?**

O diodo zener deve ter baixa resistência por conta das variações de corrente. Utilizaremos um diodo zener de 6,2V para o projeto.

**Qual a influência da regulação de linha e da regulação de carga para este circuito? Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?**

Caso a tensão em cima do diodo zener varie demais, a tensão e a corrente de saída também irão sofrer grandes variações. Portanto, essa parte do circuito é muito importante para a regulação de linha e carga do circuito.

**Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia?**

Podemos substituir o resistor por uma fonte de corrente, dessa forma não haverá variações na corrente do zener, melhorando sua eficiência e ajustando a regulação de linha e de carga.

**Escolhendo o transistor M1 e calculando R2 e R3.**

**Qual a corrente contínua necessária?**

A corrente especificada para este circuito é de 1A.

**Quais os limites de tensão para este circuito?**

A tensão no circuito é limitada pelo retificador de onda completa. 

**Utilizando o transistor IRF540, temos os seguintes dados:**

- L=100uH

- W=100uW

- LAMBDA = 0.00291031

- u0 (valor padrão) = 600 cm²/V/s

- C0x = KP/u0 = 25,0081/600 = 41,68 mF/m²

- VA = 1/LAMBDA = 1/0.00291031 = 343,61 v

- Vt = 3.56362 V

**Quais as tensões máximas de operação deste componente?**

A tensão de Drain-Source máxima do IRF540 é de 100V. 
A tensão de Gate-Source máxima é de 20V.

**Qual o valor da capacitância de gate?**

CGS = Ciss - Crss = 440pF

**Justifique a escolha dos resistores R2 e R3.**

Considerando o diodo zener D3 com uma tensão de 6,2V, precisamos de um ganho de 3.2V/V em nosso ampop. É vantajoso também que os resistores tenham valores altos de resistência para que a corrente que circule sobre eles seja baixa. Como temos 1A na saída do circuito, utilizaremos diodos na ordem dos kilo ohms para o projeto.

Utilizando resistores de 32k e 10k, obtemos o ganho necessário e a corrente que circulará por eles será de 357uA, baixa o suficiente para não afetar o circuito.

## Parte 03: Adicionando um circuito de proteção de sobre corrente ao regulador linear

**Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito? O que deve fazer um circuito de proteção de sobrecorrente? O que é a proteção foldback?**

A sobrecorrente é qualquer corrente que circule pelo circuito que esteja acima da corrente para a qual ele foi projetado. A sobrecorrente pode causar danos sérios ao circuito, portanto, é importante que haja uma proteção.

A proteção em foldback limita a corrente de forma linear, conforme a tensão no circuito aumenta.

No caso do regulador de tensão, para manter o princípio de LDO, devemos procurar por uma proteção de sobrecorrente que tenha uma baixa queda de tensão para o seu funcionamento.

Figura 1 - Proteção de Sobrecorrente
![]()

A proteção de sobrecorrente apresentada na figura 1 funciona por meio de um circuito comparador que mede as tensões na entrada e saída de um resistor shunt. Caso a tensão no resistor shunt seja maior do que a projetada, o circuito comparador envia tensão suficiente para ativar o transistor NMOS M2. Por sua vez, o transistor M2 envia o sinal do ampop U1 direto pro terra, desligando a fonte.

Este circuito é ideal para essa aplicação, pois a queda de tensão da entrada para a saída da fonte é a tensão no resistor shut, que é muito pequena.