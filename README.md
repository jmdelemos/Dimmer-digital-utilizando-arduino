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

Para melhor compreensão do nosso projeto, segue abaixo o diagrama de blocos e o fluxograma do mesmo.


![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/ImgDiagramBlocos.PNG)

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/ImgFluxograma.PNG)

•	Implementação:

Nesta tarefa foi feito primeiramente o estudo do que se propunha realizar, ou seja, entender como cada elemento do sistema funciona e a partir daí esboçar o seu funcionamento, Dessa forma, fizemos primeiramente simulações no tinkercard circuits, as quais foram realizadas de forma gradativa, ou seja, primeiro fizemos o esboço para um led e um ldr, depois para um ldr e dois leds e assim por diante até fazermos as simulações com o módulo bluetooth.
Observe abaixo a descrição de cada componente o exemplo de seu funcionamento:

- Arduíno Uno:

Arduíno: é o controlador do projeto, ele é quem fornece a energia de 5v alimentando os sensores e os leds. O Arduíno possui entradas analógicas e saídas digitais com PWM e a programação do projeto é passado do computador para o arduíno por meio de uma entrada USB.

![alt text](https://github.com/jmdelemos/Dimmer-digital-utilizando-arduino/blob/master/Arduino_UNO.jpg)

- Led e Ldr:
