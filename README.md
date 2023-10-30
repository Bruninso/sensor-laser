# sensor-laser
Um circuito que capta movimentações que passam pelo laser com um sensor LDR e emite sons em uma frequência personalizável utilizando um Buzzer, com dois Leds para indicar se o circuito está, ou não está ligado.

Explicação do código:

Primeiramente é definido as variáveis ​​globais para os pinos que serão usados ​​no circuito.

Em setup(), é iniciado a comunicação serial a 9600 bps e definido os modos dos pinos botão, LED verde e do LED vermelho para INPUT, OUTPUT e OUTPUT respectivamente.

Em loop(), o código verifica se o pino do botão está em HIGH(ou seja, se o sinal está ativo ou não). Se for HIGH, alternará o estado de 0 para 1 com um atraso de 1 segundo.

Se o estado for 0, o LED vermelho acende e o LED verde apaga, sinalizando que o circuito está desligado. Se o estado for 1, o LED vermelho apaga e o LED verde acende. Em seguida, ele lê o valor passado pelo Sensor LDR do pino A0 usando analogRead() e verifica se esse valor é menor que 600. Se for menor que 600, gerará um tom no Buzzer com uma frequência de sua escolha durante o período que o sensor captar movimento. Caso contrário, desliga o Buzzer com noTone() e imprime a leitura no monitor serial.

Link do video: https://www.youtube.com/watch?v=maBJfrIe9XI

