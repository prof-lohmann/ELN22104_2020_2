# PROJETO FINAL
## Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: Qual relação entre a tensão de alimentação do ampop e a tensão de saída? O que devemos considerar para esse circuito operar como um LDO? Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?
![figura01](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/figura%2001.png)
- A tensão de saída do ampop será aproximadamente a tensão de alimentação. 
- Primeiramente deve-se considerar o diodo zener conectado à entrada não-inversora do amplificador, isso irá limitar o sinal de entrada. Para o sinal de saída, os limites estão sujeitos a própria alimentação do amplificador.
- Esse circuito pode ser alimentado com uma tensão maior que a tensão requerida de saída do regulador somada a queda de tensão de VDS. VCC = VOUT + VDS
## Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms? Quais problemas apresentam esse circuito? Podemos melhorar?
### Circuito proposto (01) para a alimentação do AmpOp:

![circuito01](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/circuito%2001%20alimenta%C3%A7%C3%A3o.png)

- Calculando Vcc

![calculo_vcc](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/calculo%20vcc.png)
- A desvantagem desse circuito acredito que seja o ripple de saída, já que a forma de onda de entrada é uma senoide. O capacitor C3 teria que ter um valor próximo ou similar ao capacitor usado para a retificação. A melhoria desse circuito seria a adição de um regulador linear para eliminar possíveis ruídos.

### Circuito proposto (02) para a alimentação do AmpOp:
![circuito02](https://user-images.githubusercontent.com/74318416/116098360-64f98c00-a681-11eb-86c3-de3b06bd58df.png)
## Vamos projetar esse circuito  de alimentação do AmpOp?
![projeto_alimentacao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/projeto%20circuito%20alimenta%C3%A7%C3%A3o.png)
- Qual a Tensão VGS? Descreva como obter o valor.

Datasheet(https://www.alldatasheet.com/datasheet-pdf/pdf/580586/NELLSEMI/IRF540.html)

![vgs_irf540](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/vgs%20irf540.png)

Pelo gráfico, a tensão VGS pode ser considerada 4,5V

- Qual a corrente de alimentação do AmpOp?

Datasheet(https://www.ti.com/lit/ds/snosc16d/snosc16d.pdf)

![corrente_ampop](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/corrente%20de%20alimenta%C3%A7%C3%A3o%20ampop.png)

I = 1.5mA & Imax = 3.0mA

- Qual a tensão de alimentação do AmpOP?

Datasheet(https://www.ti.com/lit/ds/snosc16d/snosc16d.pdf)

![tensao_ampop](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20de%20alimentacao%20ampop.png)

Vmax = 32V 

- Qual fator devo considerar para escolher o transistor Q1?

O beta precisa ser elevado.

- Qual valor da tensão do diodo zener D6?

![tensao_diodo_zener](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20diodo%20zener.png)

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito? 

O zener precisa da menor impedância possível para evitar oscilações na corrente.

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

Sim, uma vez que a corrente de alimentação é maior que a mínima corrente de alimentação o ampop funcionará.

### Circuito de alimentação montado no LTSPICE

![circuito_alimentação](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/circuito%20de%20alimenta%C3%A7%C3%A3o%20ampop.png)

![dobrador](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/calculo%20dobrador%20de%20tens%C3%A3o.png)

![simulacao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/simula%C3%A7%C3%A3o%20circuito%20de%20alimenta%C3%A7%C3%A3o.png)

- Como pode-se obersevar, a tensão de pico é aproximadamente 32V, que seria o Vin_pico dobrado, por conta do dobrador de tensão e o capacitor C3 irá retificar este sinal. A tensão de ripple se encontra na faixa de 1,98V. Para corrigir o ripple , foi utilizado um regulador de tensão, composto pelo transistor bipolar de junção 2SC4081 e o diodo Zener EDZV24B.

Datasheet(https://pdf1.alldatasheet.com/datasheet-pdf/view/35878/ROHM/2SC4081.html)
![transistor_Q1](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/transistor%20Q1%20beta.png)

Datasheet(https://pdf1.alldatasheet.com/datasheet-pdf/view/448069/ROHM/EDZV24B.html)
![Z6](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/DIODO%20ZENER%20D6%20DATASHEET.png)

- Dito anteriormente, o transistor Q1 deveria ter um beta elevado e o diodo D6 com uma baixa impedância e uma corrente de operação mínima.  Logo, por conta desses parâmetros, esss foram os dispositivoss escolhidos.

![tensao_regulada](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tensao%20de%20alimenta%C3%A7%C3%A3o%20regulada.png)

- Como se pode observar, após a ação do regulador, a tensão de entrada do Ampop se estabilizou em 23,78V

## Parte 02 - Calculando e dimensionando os componentes
![letra_a](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/letra%20a%20parte%2002.png)

![capacitor_C1](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/calculo%20C1.png)

- O modelo escolhido para D1 e D2 foi o 1N4007, simplesmente por possuir uma tensão reversa dentros dos parâmetros que o circuito necessita, ou seja, uma tensão reversa maior do que a que foi calculada. O modello possui uma tensão reversa de pico de 1000V.


Datasheet(https://pdf1.alldatasheet.com/datasheet-pdf/view/58830/DIODES/1N4007.html)

![tensao reversa](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tensao%20reversa%201N4007.png)

- Simulando a corrente no diodo D1 para obter o tempo de condução.

![condução](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tempo%20de%20condu%C3%A7%C3%A3o%201N4007.png)

![calculo_condução](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/c%C3%A1lculo%20tempo%20de%20condu%C3%A7%C3%A3o.png)

![letra_b](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/letra%20B%20parte%2002.png)

O diodo zener deve possuir o menor ruído possível de regulação de linha. Uma baixa impedância pode ser viável.

Datasheet(https://pdf1.alldatasheet.com/datasheet-pdf/view/36703/JGD/1N750.html)

![D3](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/DIODO%20D3%20datasheet.png)

- Para este circuito não tem influência de regulação de carga porque o diodo zener esta ligada a saída não inversora do amp op e por esta não passa corrente. No entanto este circuito tem influencia de regulação de linha já que a tensão de entrada pode sofrer oscilações, neste caso o diodo zener tende a manter a tensão de saída constante. Sendo assim, aumenta ou diminui a queda de tensão sobre o resistor R1, o qual tem a função principal de limitar a corrente do zener. Tudo que variar no diodo zener será multiplicado pelo ganho e refletirá na saída (Vout).

- Um problema nessa topologia seria as correntes que geram variação de tensão sobre o diodo zener. Uma solução seria um componente que manteria essa corrente constante, para evitar variações sobre o zener. Esse componente pode ser uma fonte de corrente.

- Cálculo do resistor R1

![resistor_r1](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/c%C3%A1lculo%20R1.png)

![fonte de corrente](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/projeto%20fonte%20de%20corrente.png)

![transistor_mosfet](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/fonte%20de%20corrente%20e%20mosfet.png)

- O transistor Q2 limita a tensão sobre o resistor R1, estes dois definem a corrente de saída da fonte de forma independente a tensão de alimentação. O resistor R5 causa a queda de tensão entre o coletor de Q2 e o terra, enquanto o transistor Q3 mantém o a tensão coletor-emissor de Q2 estável, o que reduz variações secundárias da corrente de saída com a tensão de alimentação. Para esta aplicação foi escolhido o transistor 
BC557B.  O  R1 já foi dimensionado anteriormente e o R5 deve obedecer:

R5 < (VIN – 2 * VBE) / (IE / hFE)

No entanto Vin é menor que 2VBE por isso R5 admitiria um valor negativo. Diante disso R5= 20k. Foi escolhido este valor para R5 ter uma corrente mínima.

- Podemos melhorar ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?

Um potenciômetro entre Vref e GND deixaria o valor fonte mais ajustável.

### Escolhendo o transistor M1 e calculando R2 e R3

- Qual a corrente contínua necessária?

A mesma corrente do projeto, 1A.

- Quais os limites de tensão para este circuito?

A limitação do circuito se dá pelo valor de entrada

- Quais o parâmetros L, W, Uo, Cox, VA e Vt?

![irf540](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/caracter%C3%ADsticas%20IRF540.png)

- Quais as tensões máximas de operação deste componente?

Datasheet(https://www.vishay.com/docs/91021/91021.pdf)

![tensao_operacao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20de%20opera%C3%A7%C3%A3o%20IRF%20540.png)

- Qaul o valor da capacitância de gate?

Datasheet(https://www.vishay.com/docs/91021/91021.pdf)

![gate_capacitancia](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/capacitancia%20do%20gate.png)

- Justifique a escolha dos resistores R2 e R3.

![dimensionamento_R2_R3](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/calculo%20R2%20e%20R3.png)

- Circuito montado

![circuito_montado](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/circuito%20montado%20parte%202.png)

- Vout e Iout

![Vout_Iout](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/Vout%20e%20Iout.png)

## Parte 03 - Adicionando um circuito de proteção de sobre corrente ao regulador linear.

- Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito? O que deve fazer um circuito de proteção de sobrecorrente? O que é a proteção foldback?

Sobrecorrente se trata quando há a circulação de uma corrente no circuito acima do valor nominal projetado. Pode ocassionar a queima de componentes do circuito, além de um mau funcionamento do mesmo. O circuito de proteção de sobrecorrente deve interromper a corrente que circula no circuito, automaticamente, sempre que a intensidade de corrente atingir valores que podem causar danos aos demais dispositivos. Foldback é uma limitação de corrente. Quando a carga tenta provocar sobrecorrente da alimentação, a proteção foldback reduz a saída de tensão e corrente para bem abaixo dos limites normais de operação. Sob um curto-circuito , em que a tensão de saída é reduzida a zero, a corrente é tipicamente limitados a uma pequena fracção da corrente máxima.

- Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o que devemos levar em consideração para o regulador? 

Circuitos LDO não foram projetados para correntes elevadas, logo, para esse tipo de problema, são utilizados circuitos de proteção de sobre corrente como o foldback e proteção brick-wall

![circuito_protecao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/exemplo%20circuito%20de%20prote%C3%A7%C3%A3o.png)

### Dimensionando o circuito de proteção de sobrecorrente ao regulador linear

![R6](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/dimensionando%20R6.png)

- O transistor deve ser um transistor de sinal, ou seja, deve suportar pequenas correntes. Então, o modelo escolhido foi o 2N7002. Como o dreno funciona como chave, a tensão varia entre 0 e a tensão máxima recebida,  neste caso, VGS. Para o transistor conduzir, é necessário VGS> VT. VT pode ser considerado o VGS(th) que foi encontrado no datasheet e possui um valor de 2.1 V. Então como tensão na saída e para cálculos futuros adotaremos 3V. 

- R11 = R12 = 20kΩ

- O valor do resistor shunt deve ser pequeno para que a queda de tensão seja mínima. Logo, Rshunt = 100mΩ.

![subtrator](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/circuito%20subtrator.png)

### Circuito de proteção montado

![proteção](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/Circuito%20de%20prote%C3%A7%C3%A3o%20montado.png)

- Vout e Iout com o circuito de proteção

![Vout_iout_protecao](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/Iout%20e%20Vou%20com%20circuito%20de%20prote%C3%A7%C3%A3o.png)

- Tensão na carga R6

![cargaR6](https://github.com/alvesotavio21/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Ot%C3%A1vio%20Alves/Imagens%20projeto%20final/tens%C3%A3o%20sobre%20a%20carga%20R6.png)
