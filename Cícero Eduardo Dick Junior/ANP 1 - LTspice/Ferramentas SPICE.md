# APRENDENDO A SIMULAR COM O SPICE

## Como funciona o SPICE

#### O que é o *netlist*?

O *netlist* é um documento de texto que faz a listagem dos componentes de um circuito e dos nós pelos quais estes componentes estão conectados.
	
#### Como descrever o *netlist* de um circuito?

Existe uma formatação específica para a descrição de uma netlist e também símbolos que devem ser usados para representar cada componente.
Por tanto, vamos utilizar o circuito abaixo como exemplo para visualizar melhor.
![exemplo_netlist](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_netlist.PNG)

O circuito é formado por três resistores, que serão representados por R1, R2 e R3; uma fonte de tensão representada por V1 e quatro nós que ligam os componentes 
N1, N2, N3 e N4. A *netlist* para este circuito fica assim:

```
R1 N1 N2 3k
R2 N2 N3 6k
R3 N3 N4 9k
V1 N1 N4 12
```

#### O que é o *LABEL* de um nó e qual a vantagem de usar o mesmo?

Como visto no exemplo anterior, os nós do circuito estão marcados com os símbolos N1, N2, N3 e N4; estas marcações foram feitas utilizando *LABELS* e ajudam
a organizar o circuito e a *netlist*. Por padrão, os nós aparecem na *netlist* numerados por n001, n002, n003 e assim por diante, o que torna a netlist um
pouco confusa quando utilizamos circuitos mais complexos. Com o uso de *LABELS* podemos identificar mais facilmente os nós mais importantes em nossa análise.
Além disso, eles podem ser usados para fazer as conexões entre componentes e manter o projeto mais organizado, dessa forma:

![exemplo_labels](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_labels.PNG)

#### Quais os componentes básicos implementados no SPICE?

Os componentes básicos são os resistores, capacitores, indutores, transistores e diodos.

#### O que é um **SUBCKT**? Faça um exemplo.

A diretiva **.SUBCKT** é utilizada para criarmos modelos de componentes para o nosso circuito á partir dos componentes básicos. Um exemplo disso, seriam
os Amplificadores Operacionais. Este é um exemplo de SUBCKT que descreve um AmpOp:
```
.SUBCKT LM324    1 2 3 4 5
*
  C1   11 12 5.544E-12
  C2    6  7 20.00E-12
  DC    5 53 DX
  DE   54  5 DX
  DLP  90 91 DX
  DLN  92 90 DX
  DP    4  3 DX
  EGND 99  0 POLY(2) (3,0) (4,0) 0 .5 .5
  FB    7 99 POLY(5) VB VC VE VLP VLN 0 15.91E6 -20E6 20E6 20E6 -20E6
  GA    6  0 11 12 125.7E-6
  GCM   0  6 10 99 7.067E-9
  IEE   3 10 DC 10.04E-6
  HLIM 90  0 VLIM 1K
  Q1   11  2 13 QX
  Q2   12  1 14 QX
  R2    6  9 100.0E3
  RC1   4 11 7.957E3
  RC2   4 12 7.957E3
  RE1  13 10 2.773E3
  RE2  14 10 2.773E3
  REE  10 99 19.92E6
  RO1   8  5 50
  RO2   7 99 50
  RP    3  4 30.31E3
  VB    9  0 DC 0
  VC 3 53 DC 2.100
  VE   54  4 DC .6
  VLIM  7  8 DC 0
  VLP  91  0 DC 40
  VLN   0 92 DC 40
.MODEL DX D(IS=800.0E-18)
.MODEL QX PNP(IS=800.0E-18 BF=250)
.ENDS
```

#### Como incluir novos modelos de componentes em um simulador SPICE?

Basta encontrar o modelo que se encaixa com o componente real que deseja e salvar na pasta do seu projeto, depois utilizar o comando .lib e endereçar o arquivo
que contém o modelo no spice e por último, nomear o componente do projeto com o mesmo nome do subcircuito ou modelo, como por exemplo:

![exemplo_modelos](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_modelos.PNG)

## Parâmetros de Simulação do SPICE

#### O que é simulação transiente (.tran)? Quando usar? Faça um exemplo.

A simulação transiente é uma simulação **não linear no domínio de tempo**, muito útil quando observamos circuitos não lineares, cujo a tensão e corrente 
mudam ao decorrer do tempo. Como exemplo, vamos observar a curva de carga do capacitor no circuito abaixo:

![exemplo_transiente](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_transiente.PNG)

Na imagem aparece o comando:
```
.tran 0 1 0
```
É possível definir o tempo inicial da simulação, que no nosso caso é zero, o tempo final, nesse caso um segundo, além do máximo de timesteps, que não estão
configurados neste exemplo. O gráfico da simulação fica dessa forma:

![exemplo_transiente](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_transiente2.PNG)

#### O que é simulação DC operating point (.op)? Quando usar? Faça um exemplo.

A simulão .op faz a análise do circuito em corrente contínua, útil para analisar o estado inicial de um circuito ou para analisar um circuito em corrente
continua. Como exemplo, vamos analisar o divisor de corrente abaixo:

![exemplo_DCsim](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_DCsim.PNG)

Nesse caso, o *software* faz uma lista das tensões nos nós e das correntes em cada componente do circuito, como mostrado abaixo:
![exemplo_DCsim2](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/Exemplo_DCsim2.PNG)

#### O que faz a diretiva .step no SPICE?

O comando .step repete uma análise de circuito alterando o parâmetro de um componente em cada repetição. Como no exemplo desse circuito simplificado:

![exemplo_step1](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_step.PNG)

A sintaxe do comando .step segue da seguinte forma:
```
.step param X 1k 3k 1k
```
O que significa que o valor inicial do meu resistor é 1k, o valor final é 3k e ele varia 1k em cada repetição.
O gráfico das tensões simuladas fica da seguinte forma:

![exemplo_step2](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_step2.PNG)

#### O que faz a diretiva .meas? Forneça exemplos de utilização.

O comando .meas (.measure) serve para avaliar quantidades elétricas definidas pelo usuário. Existem dois tipos diferentes de instruções .measure, aquelas que se
referem a um ponto ao longo da abscissa, que é a variável independente plotada ao longo eixo horizontal como, por exemplo, o eixo do tempo de uma análise de transiente
(.tran); e as instruções que se referem a um intervalo acima da abscissa. Vamos observar um exemplo do primeiro tipo de instrução .measure:

![exemplo_measure1](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_measure1.PNG)

Após simular o circuito acima com o comando .meas, pode ser encontrado o valor medido na janela Error Log do SPICE (CTRL + L para acessar), como mostrado abaixo:

![exemplo_measure2](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_measure2.PNG)

#### O que é a simulação "DC Sweep" (.dc)? Quando usar? Faça um exemplo.

O DC Sweep funciona de forma análoga a diretiva .step, o simulador repete a análise do circuito variando a tensão das fontes em corrente contínua do circuito.
Este tipo de análise pode ser usado para avaliar, por exemplo, o comportamento de um transistor, como veremos a seguir.

![exemplo_dcsweep1](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_dcsweep1.PNG)

Podemos ver a tensão no Gate do transistor aumentando e, consequentemente, ele passando de fechado para triodo e depois completamente ativado:

![exemplo_dcsweep2](https://github.com/ciceroed/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Cícero%20Eduardo%20Dick%20Junior/ANP%201%20-%20LTspice/Img_Exemplos/exemplo_dcsweep2.PNG)

#### Como simular um circuito em diferentes temperaturas de funcionamento?

Para simular um circuito em diferentes temperaturas, basta utilizar a diretiva .step temp (Tinicial) (Tfinal) (Tstep).

Exemplo:
```
.step temp 10 70 5
```
Neste exemplo temos a temperatura inicial 10°C, temperatura final 70°C com um incremento de 5°C para cada repetição da análise.

## Referências

* http://electronicsbeliever.com/how-to-sweep-temperature-in-ltspice-with-step-by-step-tutorials/
* https://www.youtube.com/watch?v=VzxnNrOMcMo
* https://www.youtube.com/watch?v=H0_1HLoRni0
* http://electronicsbeliever.com/how-to-sweep-voltage-in-ltspice/
* https://www.embarcados.com.br/medicoes-especiais-measure/
* http://ltwiki.org/LTspiceHelp/LTspiceHelp/_MEASURE_Evaluate_User_Defined_Electrical_Quantities.htm
* https://www.analog.com/en/technical-articles/ltspice-using-meas-and-step-commands-to-calculate-efficiency.html
* https://www.analog.com/en/technical-articles/ltspice-using-the-step-command-to-perform-repeated-analysis.html
* https://www.youtube.com/watch?v=idVApmPvtv4
* https://www.embarcados.com.br/primeiros-passos-com-o-ltspice-xvii/
