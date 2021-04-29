# Laboratório Final - **Fonte Linear**
Aluno: 
* Guilherme da Costa Franco

## Integração dos blocos de uma fonte linear

### Parte 01: Entendendo um regulador linear.

##### Conceitos importantes:

1. Princípio de regulação de tensão;
   - Trata-se de uma metodologia cujo objetivo é manter a tensão de uma porção do circuito constante apesar de alterações estruturais como tensão e impedância de entradas, potência consumida pela carga e outros.

2. Tensão de saída e tensão de _ripple_;
   - Tensão de saída trata-se do sinal que o circuito transmite, sendo este constante ao longo do tempo, caso os parâmetros de entradas estejam de acordo.
   - Tensão de _ripple_ trata-se de uma ondulação de tensão fornecida pela fonte, que é dependente do valor da capacitância do capacitor e da corrente consumida pela carga. e é resultante do descarregamento lento do capacitor em relação à fonte. Esta tensão, por sua vez, é muito importante quando queremos converter uma tensão alternada em uma tensão contínua. 

3. Regulação de linha;
   - Trata-se da relação entre a variação da tensão de saída com a tensão de entrada. Visando que a tensão de alimentação de um circuito não varie muito. A regulação de linha obedece a seguinte equação:
   ```math
   Reg. de linha = ∆Vout/∆VIn
   ```
4. Regulação de carga;
   - Trata-se da relação entre a variação da tensão de saída com a variação da corrente consumida pela carga, isto é, regula a tensão de saída quando diferentes cargas são conectadas. A regulação de carga obedece a seguinte equação:
   ```math
   Reg. de carga = ∆Vout/∆Iout
   ```
5. Conceito de LDO - _Low Dropout Voltage_.
   - Trata-se da diferença entre a tensão de saída nominal e a menor tensão de entrada necessária para que o regulador funcione adequadamente.

      ![image](https://user-images.githubusercontent.com/61738767/116453173-efceb800-a834-11eb-93c6-2fad0c222fe2.png)
      
- Qual relação entre a tensão de alimentação do AmpOp e a tensão de saída?

*Resposta:* A relação que pode ser feita é a de que a tensão de saída estará limitada pelo valor de alimentação do próprio AmpOp por saturação. Portanto, deve-se ter atenção às próprias restrições de alimentação do AmpOp, uma vez que o respectivo valor de saída irá saturar quando essa tensão se aproximar daquele valor de alimentação, outro cuidado que se deve ter é no que diz respeito sobre a tensão de offset, o que pode prejudicar a avaliação de sinal de saída do AmpOp.
  
- O que devemos considerar para esse circuito operar como um LDO?

*Resposta:* Deve-se observar a queda de tensão do `Vin` ao ser limitada pelo diodo zenner e a limitação do sinal de saída do AmpOp `Vout` causado pela saturação do próprio componente.
  
- Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

*Resposta:* Deve-se, num primeiro momento, verificar as tensões máximas de alimentação do AmpOp, para que o sinal de saída não sature, fazendo uma análise prévia do datasheet do componente, e observar a influência do valor de `VGS`.


   ![image](https://user-images.githubusercontent.com/61738767/116483027-ac883f80-a85c-11eb-894b-8f2bda074649.png)
 
      
- Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

     ![image](https://user-images.githubusercontent.com/61738767/116481637-f91e4b80-a859-11eb-867b-54a5e853c72b.png)


*Resposta:* Assumindo que a queda de tensão em D4 e D5 sejam ambas 0,7V, tem-se:

![image](https://user-images.githubusercontent.com/61738767/116482281-43ec9300-a85b-11eb-95b4-d75edfbe3f56.png)

  
- Quais problemas apresentam esse circuito? Podemos melhorar?

*Resposta:* Deve-se se atentar com a tensão de ripple, devido a presença dos capacitores C2 e C3, por isso, o efeito ripple deve ser considerado quando forem escolhidos os valores destes capacitores. Por se tratar de um dobrador de tensão, pequenas variações no sinal de entrada podem provocar ruídos no sinal de saída ou até mesmo danificar o componente. Para corrigir este equívoco, basta escolher corretamente os valores de capacitores e adicionar um regulador linear de tensão na saída, reduzindo o ruído e limitando a tensão que alimentará o componente.


   ![image](https://user-images.githubusercontent.com/61738767/116454439-602a0900-a836-11eb-910e-012f71b0c076.png)

#### Considerando o AmpOp LM324, MOSFET IRF540, Vout = 15V, Iout = 1A, Vin+ = 12 Vrms, Vripple_pós_retificador = 1V e as quedas de tensão nos diodos de 0,7V:

- Qual a Tensão VGS? Descreva como obter seu valor.

![image](https://user-images.githubusercontent.com/61738767/116563785-bd779600-a8da-11eb-9abb-50618a9bd597.png)

*Resposta:* Pelo datasheet, o Vgs para 1A a 25°C é de 4,5V. Pode-se obter esse valor na diferença entra a tensão de saída do AmpOp `U1` e a tensão de saída da fonte `Vout`. Dessa forma, para obter a tensão de saída do AmpOp e atribuindo 15V no sinal de saída, pode ser feito o cálculo `Vout = 4,5 + 15`, resultando em 19,5V na saída do AmpOp `U1`. 

- Qual a corrente de alimentação do AmpOp?

![image](https://user-images.githubusercontent.com/61738767/116565736-82766200-a8dc-11eb-8045-3c985848e173.png)

*Resposta:* Pelo datasheet, a corrente de alimentação do AmpOp é de 3mA.

- Qual a tensão de alimentação do AmpOp?

![image](https://user-images.githubusercontent.com/61738767/116566064-cb2e1b00-a8dc-11eb-9e94-e408fc54ff99.png)

*Resposta:* Pelo datasheet, o AmpOp pode ser alimentado em no máximo 32V.

- Qual fator devo considerar para escolher o transistor Q1?

*Resposta:* Far-se-á necessário que o beta do transistor tenha um valor alto, para que a corrente que passa pelo bjt seja drasticamente menor que a corrente do diodo zener.
  
- Qual valor da tensão do diodo zener D6?

*Resposta:* Como a tensão de saída do AmpOp é de 19,5V, é necessário que o diodo zener tenha uma tensão superior a do amplificador. Seja 20V a tensão de saída do AmpOp (aproximação feita para dar margem para tensão de offset), 0,7V de queda de tensão em cada um dos diodos D4, D5 e D6 e a tensão de ripple pós retificador de 1V, tem-se que uma boa tensão para operação é de aproximadamente `24V`.

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

*Resposta:* Para obter a máxima eficiência energética e o minímo de ruídos, deve-se obtar por um diodo que tenha uma resistência interna baixíssima, para que não haja tanta variação de tensão.

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

*Resposta:* Sim, caso a corrente de alimentação for superior a corrente mínima proposta pelo fabricante, o AmpOp continuará funcionando.

---

### Parte 02: Calculando e dimensionando os componentes

a) Para o primeiro bloco (D1, D2, C1) considere Vin+ = 12 Vrsm, Vripple_pós_retificador = 1V e Icarga = 1,1A. Justifique a escolha dos componentes.

*Resposta:* Analisando o circuito, pode-se avaliar que os diodos D1 e D2 influenciarão diretamente a tensão final. Para que não haja muita intereferência, recomenda-se que a queda de tensão nestes diodos não passe de 1V. Para isso, foi escolhido o diodo 1N4001 por atender os seguintes parâmentos calculados:

   ![image](https://user-images.githubusercontent.com/61738767/116577409-d128f980-a8e6-11eb-9aef-e0e455490f12.png)

Pelo datasheet, pode-se ver que os parâmetros de tensão e corrente foram respeitados.

   ![image](https://user-images.githubusercontent.com/61738767/116577938-4eed0500-a8e7-11eb-9469-dd25bad405db.png)

Quanto ao capacitor C1, este será escolhido com base no retificador de onda completa. Abaixo segue a equação para encontrar o valor deste capacitor:

![image](https://user-images.githubusercontent.com/61738767/116575605-2e23b000-a8e5-11eb-9d7d-e2320ee2b7cf.png)

b) Circuito referência de tensão zener (R1 e D3):
   - Quais fatores devo considerar para escolher o diodo zener para essa aplicação?
   *Resposta:* Deve-se considerar que o diodo zener tenha uma baixa resistência interna `Rz`para minimizar os ruídos na saída.
   
   - Qual a influência da regulação de linha e da regulação de carga para este circuito?
   *Resposta:* A partir desta, pode-se medir a efetividade do regulador, uma vez que deseja-se uma baixa variação de tensão na saída do circuito. Por isso, na melhor da hipóteses, deseja-se uma regulação de linha e de cargar próximo a zero.
   
   - Qual o impacto da regulação linha / carga do circuito com o diodo zener na tensão de saída do regulador linear?
   *Resposta*: Como o diodo zener estará limitando a tensão de saída do circuito (a fim de que a varição de `Vout`seja próxima de 0), tem-se que:
   
   ![image](https://user-images.githubusercontent.com/61738767/116580175-7e9d0c80-a8e9-11eb-9cf7-8d5a986a8144.png)
   
   Denotando que, mesmo variações de tensão na entrada, a tensão de saída não sofrerá por variações notáveis.
   
   O mesmo vale para o regulador de carga, no qual, mesmo variando a carga, não haverá variações notáveis.
   
   ![image](https://user-images.githubusercontent.com/61738767/116580739-0aaf3400-a8ea-11eb-8487-a7df6bc5d168.png)
   
   - Podemos melhorar esse circuito? Quais problemas podemos identificar nesta topologia? Sugestão de melhoria:
   
   ![image](https://user-images.githubusercontent.com/61738767/116589514-1b17dc80-a8f3-11eb-8a7b-ffc27ee88147.png)

   *Resposta:* Pode-se melhorar este circuito colocando uma topologia de corrente constante, a fim de que não haja interferência na regulação e evitar problemas com variações de tensão no regulador de linha.
   
   #### No qual o circuito com R1, R5, Q2 e Q3 é uma fonte de corrente constante para polarizar o diodo zener D3. Vamos projetar?

   ![image](https://user-images.githubusercontent.com/61738767/116590319-fb34e880-a8f3-11eb-9378-b5fd9c17148a.png)

   - Acerca do fonte de corrente. Podemos melhorar mais ainda? Que tal deixar essa fonte com valor ajustável? Como fazer isso?
   *Resposta:* A fim de deixar a fonte com valor ajustável, pode-se fazer uso de um potenciômetro em paralelo com a tensão de referência `Vref`.
   
   c) Escolhendo o transistor M1 e calculando R2 e R3.
   
   - Qual a corrente contínua necessária?
   *Resposta:* Para o transistor M1, é necessário uma corrente de 1A com um `Vgs`de 4,5V.
   
   - Quais os limites de tensão para este circuito?
   *Resposta:* Sabendo que as tensões que circulam pelo circuito são limitadas pela tensão de entrada, é necessário que a tensão `VDO` seja a menor possível. Por outro lado, a tensão `Vgs`será limitada pelo produto da regulação de tensão de zener pelo ganho.
   
   #### Ao escolher o transistor, obtenha:
   
   - Quais os parâmetros L, W, Uo, Cox, VA e Vt?
   *Resposta:*
   
   |     Parâmetro       |        Valor        |     Unidade    |
   | ------------------- | ------------------- | -------------- |
   |        L            |         100         |       uH       |
   |        w            |         100         |       uW       |
   |        Uo           |         600         |     cm²/V/s    |
   |        Cox          |        41,68        |      mF/m²     |
   |        VA           |       343,61        |        V       |
   |        Vt           |       3.5636        |        V       |
   
   - Calcule o valor de RDS para as tensões VGS de 2V, 3V, 4V, 5V e 10V.
   *Resposta:*

   |      Vgs (V)        |    RDS teórico (Ω)  |  RDS simulado (Ω)  |
   | ------------------- | ------------------- | ------------------ |
   |        2            |      infinito       |       4M           |
   |        3            |      infinito       |       4M           |
   |        4            |        0,137        |      0,156         |
   |        5            |        0,073        |      0,074         |
   |        10           |        0,051        |      0,051         |
   
   - Quais as tensões máximas de operação deste componente?
    
   *Resposta:* De acordo com o datasheet do IR540, o `Vgs` máximo é de ±20V, enquanto que o `VDS`máximo não pode ultrapassar 100V.
   
   - Qual o valor da capacitância de gate?
   
   *Resposta:* A capacitância de gate `Cgs` pode ser encontrada pela equação `Ciss = Cgd + Cgs`, no qual `Ciss = 1700pF` e `Cgd = Crss = 120 pF`, tem-se que `Cgs = 1580pF`.
   
   - Justifique a escolha dos resistores R2 e R3.
   
   *Resposta:* Como a tensão de saída requisitado pelo projeto é 15V e a tensão de entrada regulada pelo diodo zener é de 12,5V, pode-se assumir que o melhor cenário, para se obter uma corrente maior na saída, seria utilizar resistores na faixa de kΩ.
 
---
   ### Parte 3 Adicionando um circuito de proteção de sobre corrente ao regulador linear
   
   - Primeiramente reflita e pesquise sobre o que é sobrecorrente? Quais os impactos neste circuito?
   
   *Resposta:*
   
   - O que deve fazer um circuito de proteção de sobrecorrente?
   
   *Resposta:*
   
   - O que é a proteção foldback?
   
   *Resposta:*
   
   - Pesquise as topologias disponíveis, caso deseja-se fazer um circuito LDO, o o que devemos levar em consideração para o regulador?
   
   *Resposta:*
   
   
