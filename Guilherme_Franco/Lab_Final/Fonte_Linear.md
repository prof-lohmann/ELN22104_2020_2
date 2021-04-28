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
