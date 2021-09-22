---
sidebar_position: 1
---

# Overview

A abordagem ThingML é composta por: **uma linguagem de modelagem**, **um conjunto de ferramentas** e **uma metodologia**. A linguagem de modelagem combina construção de modelagem de software comprovada para o projeto e implementação de sistemas distribuidos reativos, tais como:

- Diagramas de estado e componentes (alinhados com a UML) se comunicando através de mensagens passadas de forma assíncrona
- Uma linguagem de ação independente de plataforma
- Construções específicas voltadas para aplicações IoT

A linguagem ThingML é apoiada por um conjunto de ferramentas, que incluem editores, transformadores(ex: UML) e um avançado framework de geração de código multi-plataforma, que suporta multiplas linguagens (C, Java, Javascript).

***ThingML é distribuído sob a [licença Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) e foi desenvolvido por @ffleurey e @ brice-morin do departamento de Sistemas e Serviços em Rede da SINTEF em Oslo, Noruega, junto com uma vibrante [comunidade de código aberto](https://github.com/TelluIoT/ThingML/graphs/contributors). ThingML agora é propriedade da [Tellu](https://tellu.no/), mas permanece com o código-fonte aberto.***

Nas seções a seguir mostraremos o exemplo da modelagem de um robô apresentado pela primeira vez na **ACM / IEEE 21ª Conferência Internacional sobre Linguagens e Sistemas de Engenharia Orientada a Modelos (MODELS)**, mais precisamente o tema 8 [ThingML: Model-Driven Software Engineering for Heterogeneous and Distributed Reactive Systems](https://modelsconf2018.github.io/program/tutorials/) apresentado por **Franck Fleurey**, **Brice Morin**, **Jakob Høgenes and Nicolas Ferry**. Em seguinda destrincharemos a definição de cada componente da linguagem.

## Tutorial T8
[Neste tutorial](https://speakerdeck.com/bmorin/thingml-tutorial-at-models-18?slide=45), os autores apresentam três exemplos de utilização da ThingML, o exemplo que demonstraremos a seguir refere-se ao **Hands-on 1**, onde nos é apresentado a modelagem de um robô, nele é possível perceber diagramas de componentes e UML, o tutorial divide o robô em várias partes, como o objetivo de apresentar cada componente da ThingML.


### Tipos de Componentes

Os seguintes componentes são utilizados pela ThingML: **Thing**, **Fragment**, **Configuration**, **Functions e Properties** e **Statechart**, veremos como cada um funciona.

## Thing
Definição de estrutura principal em thingMLque pode se comunicar com outras coisas (things) por meio de portas de mensagens definidaas, além de possuir a capacidade de ter estados e funções internas. No exemplo abaixo é possível perceber que o autor está criando o componente **"WheelControl"**, logo abaixo nós temos a instância desse componente, funciona semelhante a um diagrama de classes em uma linguagem orientada a objetos.

![Imagem Thing](/img/imgThing.png)

## Fragment
São componentes de ***things*** que conseguem isolar pedaços das things sem ter que criar uma. Neste exemplo, o fragment armazenas ações que serão utilizadas por outras things.

![Imagem Function](/img/imgThing2.png)

## Configuration
Componente onde é feita a ***instanciação das things*** e conectadas as suas devidas funcionalidades. Nesta parte do código, o autor esá instanciando as things e conectando-as às things que foram geradas no exemplo anterior. 

![Imagem Configuration](/img/imgThingConfig.png)

## Functions e Properties
Não muito diferente de métodos em java ou funções em linguagens convencionais em ThingML, funções são definições sequenciais que podem receber argumentos, todavia, elas  não possuem retorno, properties funcionam como variáveis  Todas as funções são privadas ao componente e todas as propriedades são privadas as instâncias

![Imagem Function e Properties](/img/imgThing4.png)

## Statechart
Um estado é a definição de um bloco de execução, quando este é chamado o mesmo executa seu bloco ``on entry``` , estados podem realizar mudanças ente si, sendo assim uma maquina de estado possui um único estado em um dado momento

![Imagem Statechart](/img/imgThing5.png)

## Como utilizar esta documentação

Você pode começar a leitura desta documentação linearmente ou pode ler uma seção específica.

