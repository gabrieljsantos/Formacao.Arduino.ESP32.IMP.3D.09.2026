# Perguntas respondidas e roteiro de aprofundamento

## Palavras-chave

`conversão de energia` · `limites elétricos` · `sensor` · `microcontrolador` · `GPIO` · `entrada` · `saída` · `PWM` · `módulo` · `datasheet` · `multímetro` · `depuração`

## Respostas comentadas do slide

1. **Motor e LED: A.** Energia elétrica em mecânica e elétrica em luminosa. Existem perdas em calor e som.
2. **Conexão segura: C.** Verifique tensão da saída, corrente disponível, limites do componente e necessidade de resistor ou interface.
3. **Ajuste manual e liga/desliga: A.** Potenciômetro ajusta e interruptor abre/fecha. Em projetos eficientes, prefira ler o potenciômetro e controlar o LED por PWM.
4. **Escolha de sensor: C.** Defina grandeza, faixa, precisão e velocidade, depois instalação, alimentação, programação e interpretação.
5. **Microcontrolador: C.** Executa programas e controla dispositivos com blocos ou texto.
6. **GPIO: C.** É uma porta de uso geral configurável dentro das funções do hardware.
7. **GPIO para controlar: C.** Configure como saída digital.
8. **GPIO para interruptor: B.** Configure como entrada digital, com pull-up ou pull-down.
9. **Brilho progressivo: D.** Use PWM e varie o ciclo de trabalho.
10. **Aumentar PWM: C.** Aumenta o tempo ativo e, em lógica não invertida, a resposta média da carga.
11. **Preparar módulo: C.** Identifique função, conexões, código, alimentação e proteção.
12. **Por que conexão não basta: B.** É preciso compreender função, pinagem, configuração, alimentação e proteção.
13. **Distância, interruptor e LED: C, com ressalva.** Interruptor é entrada e LED é saída. Um ultrassônico típico usa uma saída TRIG e uma entrada ECHO, portanto o módulo não se resume a uma entrada.

## Exercícios

1. Uma entrada de 3,3 V pode receber diretamente um sinal de 5 V?
2. Calcule o resistor para 5 V, LED de 2,1 V e 8 mA.
3. Por que um motor precisa de driver mesmo quando o código usa apenas HIGH e LOW?
4. Em `INPUT_PULLUP`, qual nível representa botão pressionado?

### Gabarito

1. Somente se a documentação declarar tolerância a 5 V. Caso contrário, use adaptação de nível.
2. `R = (5 − 2,1)/0,008 = 362,5 Ω`; use um valor comercial acima, como 390 Ω, e confira potência.
3. A GPIO não suporta sua corrente nem os picos de carga indutiva.
4. LOW, quando o botão conecta o pino ao GND.

## O que estudar para aprofundar

1. Multímetro: tensão, corrente, resistência e continuidade.
2. Lei de Ohm, potência e leis de Kirchhoff.
3. Transistor BJT, MOSFET, diodo de roda livre e drivers.
4. Frequência, período, PWM, ADC e filtragem.
5. Variáveis, condições, funções, temporização sem `delay()` e máquinas de estados.
6. UART, I²C e SPI.
7. Datasheets: pinagem, valores máximos absolutos e condições recomendadas.
8. Depuração com teste por etapas e monitor serial.

## Método para aprender outro componente

1. Identifique o código exato.
2. Localize a documentação do modelo.
3. Anote palavras-chave, função, pinagem e limites.
4. Classifique cada conexão: alimentação, entrada, saída ou comunicação.
5. Desenhe o caminho da corrente e o da informação.
6. Monte um teste mínimo.
7. Relacione cada bloco às instruções que ele representa.
8. Só então integre ao projeto completo.

[Voltar ao sumário](../README.md)
