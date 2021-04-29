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

*Resposta:*

- Qual a corrente de alimentação do AmpOp?

*Resposta:*

- Qual a tensão de alimentação do AmpOp?

*Resposta:*

- Qual fator devo considerar para escolher o transistor Q1?

*Resposta:*
  
- Qual valor da tensão do diodo zener D6?

*Resposta:*

- Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

*Resposta:*

- Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?

*Resposta:*

### Parte 02: Calculando e dimensionando os componentes
