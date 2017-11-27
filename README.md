# Dimmer-digital-utilizando-arduino
Elaboração de um dimmer digital utilizando arduino, LDR1s

O dimmer digital é um dispositivo que altera a intensidade luminosa em ambientes de acordo com a incidência de luz local, sendo este controle, portanto, de suma importância na iluminação residencial tornando o ambiente mais versátil e agradável, além disso, é um bom aparelho para ter uma redução no desperdício de energia elétrica.
Neste projeto iremos mostrar o passo a passo da como é feita a implementação deste dispositivo, a partir de componentes eletrônicos básicos, módulo bluetooth e um micro controlador. 
Este projeto será desenvolvido com os seguintes equipamentos:

- Micro controlador arduino UNO – Controlador do sistema.

- Led’s 5 mm de alto brilho – Atuadores do sistema

- Ldr - Este componente será o sensor do sistema.
 
- Módulo bluetooth HC05

- Demais componentes: placa protoboard, resistores de 1k e de 10k, fios e cabos jumpers diversos.

Inicialmente, apesar de usarmos LDRs e um microntrolador arduino, o controle do dimmer foi feito utilizando apenas os valores lidos diretamente por cada LDr, valores nos o quais foram convertidos numa escala de 8 bits. Além disso, nesse primeiro momento, também foi utilizado como alternativa um controle via bluetooth, ou seja, um controle em malha aberta.
Posteriormente, visando melhorias no controle deste dispositivo, alteramos o controle da malha fechada utilizando controle PID. Primeiramente implementamos um código para controlar proporcionalmente, feito isso adicionamos o controle integral e por último adicionamos a parcela derivativa.

Para melhor compreensão do nosso projeto, segue abaixo o diagrama de blocos e o fluxograma do mesmo.


![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/ImgDiagramBlocos.PNG)

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/ImgFluxograma.PNG)

•	Implementação:

Nesta tarefa foi feito primeiramente o estudo do que se propunha realizar, ou seja, entender como cada elemento do sistema funciona e a partir daí esboçar o seu funcionamento, Dessa forma, fizemos primeiramente simulações no tinkercard circuits, as quais foram realizadas de forma gradativa, ou seja, primeiro fizemos o esboço para um led e um ldr, depois para um ldr e dois leds e assim por diante até fazermos as simulações com o módulo bluetooth.
Observe abaixo a descrição de cada componente o exemplo de seu funcionamento:

- Arduíno Uno:

Arduíno: é o controlador do projeto, ele é quem fornece a energia de 5v alimentando os sensores e os leds. O Arduíno possui entradas analógicas e saídas digitais com PWM e a programação do projeto é passado do computador para o arduíno por meio de uma entrada USB.

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/Arduino_UNO.jpg)

- Modulo Bluetooth:

Neste projeto será possível fazer o controle de luminosidade via celular (app Mobile), com isso, esse modulo fará essa comunicação entre o arduíno e o celular.

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/HC05.jpg)

- Led e LDR:

O LDR é um resistor dependente de luz constituído a partir de materiais semicondutores que permitem a variação de sua resistência elétrica em milhares de Ohms. Ele representa o sensor do nosso projeto e quando submetido a luz a sua resistência aumenta e quanto mais escuro, sua resistência diminui, ou seja, ele é quem vai fazer o controle da tensão que vai para os leds, permitindo o controle da intensidade do brilho dos mesmos.

Um led consiste em um diodo emissor de luz que, para funcionar corretamente (emitir luz), deve ser polarizado de forma direta e ser associado a uma resistência para obter uma queda de tensão, a qual limite a corrente que passa por ele. Sendo assim, associado a uma porta pwm, este componente funciona recebendo pulsos com variações de valores entre 0 a 255 bits, que, em escala de volts vai de 0 a 5v.
Com isso, podemos observar uma variação na intensidade do brilho deste componente.

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/download.jpg)                        ![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/LED.jpg)

•	Conclusão:

O Dimmer vem se tornando um dispositivo cada vez mais presente no nosso cotidiano, com este projeto pôde-se concluir que o mesmo já é bastante acessível, podendo gerar uma elevada economia em indústrias e residências; ainda permitindo que o ambiente possa ser mais confortável para as pessoas presentes nele. Além da relativa facilidade de utilização, a integração dele com outros dispositivos é bastante prática, o que facilita a aceitação de mercado.
Uma das maiores dificuldades encontradas é a vinculação do dispositivo com o ambiente no qual ele está inserido, onde será necessária uma análise dos pontos de sol, pontos de sombra e de qual será o tipo desse ambiente (sala de aula, escritório, cozinha, ...), o que gera alteração em sua configuração. Em decorrência dessas dificuldades, a taxa de variação da resposta do LDR varia de ambiente para ambiente, gerando uma leitura diferente, ou seja, cada um desses ambientes deve ser tratado de forma diferente.
Ainda assim, o projeto se mostrou viável e, com o desenvolvimento necessário, pode atingir níveis de leitura ainda mais precisos e com um maior controle de variação.


