# Atividade 4
Aluno: 
* Gabriel Wagner - <gabrielstd545@gmail.com>

Professores: 
* Daniel Lohmann

## Parte 01: Entendendo um regulador linear

### Princípios de regulação de tensão
A regulação de tensão é um método em que se deseja manter a tensão de certa parte do circuito praticamente constante, mesmo na mudança de alguns aspectos desse circuito,
como tensão de entrada, valor da carga, entre outros.

### Tensão de saída

### Tensão de ripple
A tensão de ripple é comumente associada a uma tensão retificada e filtrada por um capacitor. Ela é muito importante quando queremos converter uma tensão alternada em uma
tensão contínua.
Seu valor é dado pela subtração da tensão superior menos a tensão inferior, depois de filtrada e retificada.

### Regulação de linha
A regulação de linha é um importante aspecto da regulação de tensão. Quando estamos alimentando qualquer circuito, não queremos que essa tensão de alimentação varie muito.
A regulação de linha mede essa variação, comparando a variação da tensão de saída pela tensão de entrada. Dada pela fórmula:
Regulação de linha = (delta Vout) / (delta Vin)
Sendo expressada em V/V.

### Regulação de Carga
Enquanto isso, quem regula a tensão de saída quando diferentes cargas são conectadas, é o regulador de carga. O regulador de carga segue a seguinte fórmula:
Regulação de carga = (delta Vout) / (delta Iout)
Sendo expressada em V/A.

### Conceito de LDO – Low Dropout Voltage

