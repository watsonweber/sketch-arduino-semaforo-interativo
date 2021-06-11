# sketch-arduino-semaforo-interativo
Sketch de arduino para projeto de semáforo interativo com botão de pedestre.


Dessa vez, você estenderá o projeto anterior para incluir um farol de pedestre e um botão, que será pressionado pelos pedestres para solicitar a travessia da rua. O Arduino reagirá quando o botão for pressionado, alterando o estado das luzes para que os carros parem e os pedestres possam atravessar em segurança.

Essa será a primeira vez que você vai interagir com o Arduino, fazendo-o realizar algo quando você alterar o estado de um botão que está sendo observado. Neste projeto, 
você também aprenderá como criar suas próprias funções dentro do código.

Daqui em diante, não listarei mais a protoboard, nem os fios jumper, na lista de componentes necessários. Note que você sempre terá de utilizá-los.57 Capítulo 2 ■ Acendendo as luzesComponentes necessários:
2 LEDs vermelhos difusos
LED amarelo difuso
2 LEDs verdes difusos
Resistor de 150 ohms
4 resistores
Botão

Escolha o valor de resistor apropriado para os LEDs utilizados em seu projeto. O resistor de 150 Ω é para o botão; ele é conhecido como um resistor pull-down (que 
será definido posteriormente). O botão é às vezes chamado pelos fornecedores de interruptor tátil, e é perfeito para ser utilizado com a protoboard.
Conectando os componentes. Conecte seu circuito como mostra a figura 2.8. Verifique cuidadosamente a fiação antes de ligar seu Arduino. Lembre-se de que o Arduino deve estar desconectado da força enquanto você conecta o circuito.

Figura 2.8 – Circuito para o Projeto 4 – Sistema de semáforo com travessia de pedestres e botão de requisição 
(consulte o site da Novatec para versão colorida).

Arduino Básico 58

Digite o código da listagem 2.4, verifique-o e faça seu upload. Quando você executar o programa, ele iniciará com o semáforo no verde, para permitir que os carros passem, 
e a luz para pedestres no vermelho.

Quando você pressionar o botão, o programa verificará se, ao menos, cinco segundos transcorreram desde a última vez em que o semáforo mudou (para permitir que 
o trânsito flua) e, se afirmativo, executará o código para a função que você criou, changeLights(). Nessa função, o semáforo vai de verde para amarelo e depois para vermelho, e o semáforo para pedestres vai para verde. Depois de um intervalo de tempo definido na variável crossTime (tempo suficiente para que os pedestres atravessem), a 
luz verde para pedestres pisca, acendendo e apagando, para avisar aos pedestres que atravessem rapidamente antes que o semáforo feche. 

Então, a luz vermelha do semáforo para pedestres acende, e a luz para os veículos vai de vermelho para amarelo, e finalmente para verde, permitindo novamente o fluxo do tráfego.

