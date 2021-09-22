---
sidebar_position: 2
---

# Syntax 

Como vimos na seção anterior, a ThingML utiliza determinados componentes, que são: **Thing**, **Fragment**, **Configuration**, **Functions e Properties** e **Statechart**, mostraremos a seguir a estrutura de cada um desses elementos, vale resaltar que nem todo modelo utiliza todos esses componentes, a integração dos componentes varia conforme a complexidade do problema que o modelo visa solucionar.

# Hello World

Este exemplo foi extraido do repositório de exemplos da ThingML, podendo ser acessado [neste link](https://github.com/ffleurey/ThingMLArduinoDemo/tree/master/1.Basics)

```
thing HelloWorld { 

	statechart HelloWorld init Greetings {
	
		on entry `Serial.begin(9600);` //inicia a porta serial
	
		state Greetings {
				on entry `Serial.println("Hello World!");`	
		}	
	}
}

configuration HelloApp
{
	instance hello : HelloWorld
}
```
- Inicialmente nós temos a criação da Thing (coisa) **HelloWorld**
```
		thing HelloWorld 

	
``` 
- **O primeiro** item que temos dentro da thing é o **statechart**(máquina de estados) -  nem sempre será assim, como dito anteriormente a estrutura dos modelos se modifica de acordo com a complexidade - pdemos atribuir qualuqer nome a ele, mas é interessante ter o mesmo nome da thing, **init Greetings** indica que ele iniciará no **state Greetings**

```
 	   statechart HelloWorld init Greetings 
```

- Em seguida nós temos **On entry Serial.begin(9600)**, Serial begin é uma referência à linguagem do Arduino, significa que ele configura a taxa de transferência em bits por segundo (baud rate) para transmissão serial, para comunicação com um computador. Um segundo argumento opcional configura o número de bits no dado, paridade, e bits de parada (stop bits). Caso esse argumento não seja especificado, o padrão é 8 bits de dados, sem paridade e um stop bit.

```
	   on entry `Serial.begin(9600);`
```

- O **state**, ou seja, o estado no qual o modelo se encontra, a depender do modelo podem existir transições entre mais de um estado, como este é um exemplo simples, nosso modelo tem somente um estado, de nome **Greetings** (saudações), na entrada deste estado (**on entry**) será executado o comando de impressão **Serial.println("Hello World!")**, ele irá imprimir a frase "Hello World" no terminal.

```
	  state Greetings
```
- Saindo da máquina de estado, nos encontramos agora no componente **configuration** de nome **HelloApp**, poderia ser qualuqer nome, ele é essencial para a execução do programa, é nele que instanciaremos nossa thing, criamos uma instancia de nome **hello** do "tipo" **HelloWorld**
```
	configuration HelloApp {
	
		instance hello : HelloWorld
	}
```
- A partir dai o programa está pronto para ser executado.

# Execução do modelo 

<p>1 - Crie uma pasta em um diretório qualquer</p>
<p>2 - Abra o vscode</p>
<p>3 - Importe a pasta que acabou de criar</p>
<p>4 - Em seguida, crie um arquivo com o nome de sua preferência com extenção .thingml</p>

![Criação do arquivo](/img/imgHello.png)

5 - Copie e cole o código disponibilizado no exemplo acima.

![Escrever o código](/img/imgHello2.png)

6 - Neste exemplo exportaremos a linguagem ThingML pra UML, para isso é necessário a instalação da extensão PlantUML

![Instalação da plantUML](/img/imgPlantUML.png)

6 - Após a intalação da extenção é hora de voltar ao arquivo e  **"transformar"** o código para a plataforma desejada, no nosso caso UML, para isso, basta realizar o seguinte comando: **"SHIFT + CTRL + P"**, uma lista surgirá no topo do vscode e selecionaremos a opção "**ThingML - Generate PlantUML**".

![Conversão do código para a plataforma UML](/img/imgHello3.png)

7 -  Em seguida, clique com o botão direito na pasta gerada **"thingml-gen"** e escolha a opção **"Export Workspace Diagrams"**

![Export workspace diagram](/img/imgHello4.1.png)

8 - Logo após, será exibido outro menu, na parte superior do vscode com as opções de exportação, ecolheremos a **png**

![Export workspace diagram](/img/imgHello4.png)

9 - Uma pasta chamada "**out**" é gerada, nela consta nosso arquivo UML

![Export workspace diagram](/img/imgHello5.png)

10 - A pasta **out** contém várias subpastas, a única que nos interessa é a pasta chamada **HelloApp**, pois é onde está nosso arquivo UML.

![Export workspace diagram](/img/imgHello6.png)

Parabéns! você acabou de criar e transformar seu primeiro arquivo ThingML.



