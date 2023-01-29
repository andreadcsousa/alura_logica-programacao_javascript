# Aprendendo Lógica de Programação

Desenvolvendo um jogo de adivinhação e praticando lógica de programação com HTML e JavaScript.

1. [Comece a programar hoje](#1-comece-a-programar-hoje)
2. [Comunique-se com o usuário](#2-comunique-se-com-o-usuário)
3. [Torne seu programa dinâmico com variáveis](#3-torne-seu-programa-dinâmico-com-variáveis)
4. [Crie suas próprias funcionalidades](#4-crie-suas-próprias-funcionalidades)
5. [Pratique resolvendo problemas do seu dia a dia](#5-pratique-resolvendo-problemas-do-seu-dia-a-dia)
6. [Execute códigos diferentes dependendo da condição](#6-execute-códigos-diferentes-dependendo-da-condição)
7. [Repita tarefas](#7-repita-tarefas)
8. [Interaja de maneira diferente com o usuário](#8-interaja-de-maneira-diferente-com-o-usuário)
9. [Trabalhe com muitos dados](#9-trabalhe-com-muitos-dados)

Saiba mais sobre o curso [aqui](https://cursos.alura.com.br/course/logica-programacao-javascript-html).

***

## 1. Comece a programar hoje

### **Visão além do alcance 1**

```html
<h1>Um pequeno passo para quem já programa, um gigantesco salto para quem esta começando<h1>

Este é meu primeiro programa!
```

### **Correção**
- Problema de acentuação, por não estar utilizando a tag `<meta charset="UTF-8">`.
- Fechamento da tag `<h1></h1>` não ocorreu, então todo o texto será mostrado como título.

### **Visão além do alcance 2**

```html
<meta charset="UTT-8">

Haja coração para dar os primeiros passos na lógica de programação.
Precisamos primeiro nos ambientar com o mínimo necessário para que tudo dê certo.
```

### **Correção**
- Erro na declaração da tag meta, onde está `UTT-8` deveria ser `UTF-8`.

### **Visão além do alcance 3**

```html
<meta charset="UTF-8">

<script>
    
</script>

alert("Olá, este é meu primeiro programa!");
alert("Gostaram?");
```

### **Correção**
- Os alertas estão fora da tag `<script></script>`. Basta mover para dentro.

### **Visão além do alcance 4**

```html
<meta charset="UTF-8">

alert("Este é um popup feito com JavaScript");

<script>
    <h1>Primeiro programa</h1>
</script>
```

### **Correção**
- O `alert()` e a tag `<h1></h1>` então em posições invertidas.
- O conteúdo HTML deve ficar entre as tags `<body></body>`.
- Já o conteúdo JavaScript, dentro do HTML, deve ficar entre as tags `<script></script>`.

***

## 2. Comunique-se com o usuário

### **Escrevendo no HTML com JS**

É possível escrever dentro do HTML através do código JavaScript.  
Também pode ser criado um alerta para interação do usuário no navegador.

```html
<script>
    document.write("Isso será exibido na tela, como um texto no HTML");

    alert("Isso será exibido na tela, em um pop-up do navegador");
</script>
```

### **Concatenando textos**

Para concatenar um texto com uma operação é necessário colocar a operação entre parenteses, para que o JavaScript saiba que os números serão utilizados para cálculo e este seja realizado.

```js
document.write("Andrea nasceu em 2023 - 36");

// é diferente de

document.write("Andrea nasceu em " + (2023 - 36)");
```

As mensagens exibidas na tela serão, respectivamente:
- Andrea nasceu em 2023 - 36
- Andrea nasceu em 1987

### **Adicionando HTML no JS**

É possível utilizar tags HTML dentro das mensagens no JavaScript. O código abaixo exibe um título na tela.

```js
document.write("<h1>Seja bem-vindo!</h1>");
```

### **Operações Matemáticas**

Assim como nas operações matemáticas é importante atentar para a ordem e o padrão dos cálculos, por exemplo:

```js
document.write(200 + 100 + 300 + 400 / 4);

// será exibido o valor 700

document.write((200 + 100 + 300 + 400) / 4);

// será exibido o valor 250
```

Na primeira expressão acima, ele divide 400/4 primeiro e só depois soma os demais números, pois a divisão tem peso maior. Como o que se quer é uma média, deve-se somar antes para então dividir.

***

## 3. Torne seu programa dinâmico com variáveis

### **Reduzindo alterações**

É possível armazenar e utilizar uma informação que se repete no código numa variável:

```js
    var ano = 2016;
    document.write("Flávio tem " + (ano - 1977) + " anos");
    document.write("<br>");
    document.write("Joaquim tem " + (ano - 1996) + " anos");
    document.write("<br>");

    ano = 2017;
    document.write("Barney tem " + (ano - 1976) + " anos");
    document.write("<br>");
```

### **Reatribuindo uma variável**

Para reatribuir uma variável, não é necessário declarar ela novamente, basta dizer qual variável será alterada e qual o novo valor dela:

```js
var mes = 6;

document.write("Realizei a prova no mês " + mes + ".");

mes = 7;

document.write("Não, desculpe, realizei a prova no mês " + mes + ".");

```

### **Arredondando valores**

Quando tiramos uma média entre números em que o resultado é uma dizima periódica, é possível utilizar uma variável:

```js
var idadeAndrea = 35;
var idadeEloisa = 9;
var idadeNeuza = 63;
var media = (idadeAndrea + idadeEloisa + idadeNeuza) / 3;

document.write("A média das idades é " + Math.round(media));
```

***

## 4. Crie suas próprias funcionalidades

### **Utilizando variáveis**

É possível utilizar variáveis para informações que irão se repetir no código ou que sofrerão alteração, para simplificar a maneira em que se poderá editar posteriormente o programa.

```js
var ano = 2016;
var pulaLinha = "<br>";

document.write("Flávio tem " + (ano - 1977) + " anos");
document.write(pulaLinha);
document.write("Joaquim tem " + (ano - 1996) + " anos");
document.write(pulaLinha);

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");
```

Todas as mensagens que aparecerão na tela utilizam um ano específico para calcular a idade das pessoas, então armazenar ele numa variável facilitará a modificação do mesmo.

- Alterando o ano em `var ano = 2016` todas as mensagens sofrerão modificação em seus cálculos.

Criando a variável `var pulaLinha = "<br>"` será possível aumentar ou reduzir a quantidade de linhas que serão puladas, sem precisar procurar e alterar em todo o código.

- Basta acrescentar mais `"<br><br><br>"` na variável.

### **Criando funções**

A função armazena ações a serem realizadas toda vez que uma mensagem é exibida na tela. No caso abaixo, ao invés de utilizar `document.write("<br>");` em cada linha após a mensagem a ser exibida, com a função criada, basta chamar a função `pulaLinha();` e ela será executada. Funciona como um atalho.

```js
function pulaLinha() {
    document.write("<br>");
    document.write("<br>");
}

var ano = 2016;

document.write("Flávio tem " + (ano - 1977) + " anos");
pulaLinha();

document.write("Joaquim tem " + (ano - 1996) + " anos");
pulaLinha();

ano = 2017;
document.write("Barney tem " + (ano - 1976) + " anos");
```

### **Função com parâmetro**

Parâmetro é o valor que ficará entre os parenteses da função. A função receberá esse parâmetro ao exibir a mensagem na tela. O código abaixo, além de dar um parâmetro para a função `mostra`, também recebe a chamada da função `pulaLinha`.

```js
function pulaLinha() {
    document.write("<br>");
    document.write("<br>");
}

function mostra(frase) {
    document.write(frase);
    pulaLinha();
}

var ano = 2022;
mostra("Andrea tem " + (ano - 1987) + " anos");
mostra("Neuza tem " + (ano - 1959) + " anos");

ano = 2023
mostra("Eloisa tem " + (ano - 2013) + " anos");
```

### **Legibilidade do código para não desenvolvedores**

Nem todo mundo que tem acesso ao código é desenvolvedor, então é importante que o código seja legível e entendível por outras pessoas. A melhor forma de fazer isso é utilizando nomes de variáveis e funções que tenham a ver com o que está sendo feito no código.

```js
function pulaLinha() {
    document.write("<br>");
}

function exibeTitulo(titulo) {
    document.write("<h1>" + titulo + "</h1>");
    pulaLinha();
}

function exibeParagrafo(paragrafo) {
    document.write("<p>" + paragrafo + "</p>");
    pulaLinha();
}

// pede para alguém ler daqui em diante e veja se ele entende o que está sendo feito

exibeTitulo("Bem-vindos");
exibeParagrafo("Este é um simples programa");
```

***

## 5. Pratique resolvendo problemas do seu dia a dia

### **Reduzindo instruções**

Na função abaixo estão sendo declaradas uma variável e uma instrução, mas é possível declarar apenas a instrução `return` e obter o mesmo resultado, reduzindo e simplificando o código.

```js
function calculaImc(altura, peso) {
    var imc = peso / (altura * altura);
    return imc;
}

// forma reduzida
function calculaImc(altura, peso) {
    return peso / (altura * altura);
}
```

### **Interagindo com o usuário**

Pode-se utilizar uma função para realizar um cálculo dinâmico, no qual outro usuário insere seus próprios dados no pop-up do navegador. O `prompt` é uma função semelhante ao `alert`, a diferença é que ele necessita que o usuário insira algum valor ou que interaja diretamente para que ele funcione.

```js
function calculaImc(altura, peso) {
    var imc = peso / (altura * altura);
    return imc;
}

// forma reduzida
function calculaImc(altura, peso) {
    return peso / (altura * altura);
}

var nome = prompt("Informe o seu nome");
var altura = prompt(nome + ", informe sua altura");
var peso = prompt(nome + ", informe seu peso");

var imc = calculaImc(altura, peso);

document.write(nome + ", o seu IMC é " + imc);
```

***

## 6. Execute códigos diferentes dependendo da condição

### **Trabalhando com condições**

Existem 3 funções no JavaScript que trabalham com condição, são elas:
- `if` / `else` (se algo acontecer, faça isso... senão, aquilo...)
- `for` (para cada um, acrescente tanto, até...)
- `while` (enquanto tal coisa não acontece, repita...)

É possível ainda usar `break` na declaração, para que a rotina pare quando atingir o limite da instrução.

```js
if (condição) {
    afirmação
} else {
    negação
}
```

```js
for (inicialização, condição, incremento) {
    declaração
}
```

```js
inicialização

while (condição) {
    declaração
    incremento
}
```

### **Operações lógicas**

As operações lógicas são as que podem resultar em verdadeiro ou falso. Conhecidas também como `boolean`, comparam valores e retornam se a proposição é true ou false.

```js
1 == 1  // true
10 < 11 // true
1 >= 1  // true
2 <= 1  // false
9 > 8   // true
```

***

## 7. Repita tarefas

### **Laços de repetição**

O `while` executa uma rotina a partir do que for declarado dentro da função em relação ao parâmetro e adiciona um contador que soma as vezes que essa rotina acontecerá.

```js
var multiplicador = 1;

while(multiplicador <= 10) {
    mostra(7 * multiplicador);
    multiplicador = multiplicador + 1;
}
```

O `for` também executa uma rotina, porém de forma mais simples, pois possui parâmetros de inicialização e incremento. Além disso, se o incremento começa em 0 e precisa repetir 10 vezes, então utiliza-se o sinal `<` apenas.

```js
for(var multiplicador = 0; multiplicador < 10; multiplicador++) {
    mostra(7 * multiplicador);
}
```

O incremento das funções `while` e `for` pode ser escrito de duas formas, quando incrementa de 1 em 1.

- multiplicador = multiplicador + 1
- multiplicador++

### **Interrompendo uma repetição**

Alguns laços de repetição podem ser infinitos caso não seja imposto uma quebra da sua repetição, nos casos em que a questão for resolvida, e isso é feito com a função `break`.

```js
var numeroPensado = Math.round(Math.random() * 10);
var tentativas = 1;

while(tentativas <= 3) {
    var chute = parseInt(prompt("Digite seu chute!"));
    
    if (chute == numeroPensado) {
        mostra("Você acertou, o número pensado era " + numeroPensado);
        break;
    } else {
        mostra("Você errou!");
    }
    tentativas++;
}

mostra("FIM");
```

### **Repetições aninhadas**

As funções de repetição podem ser aninhadas, ou seja, pode-se usar uma função dentro da outra, não apenas funções diferentes, iguais também.

```js
for(var linha = 1; linha <= 3; linha++) {
    for(var coluna = 1; coluna <= 10; coluna++) {
        document.write("*");
    }
    document.write("<br>");
}
```

### **Funções de conversão**

O `parseInt` converte o texto de uma variável, que recebe um número, em um número inteiro. Para fazer uma conversão em número decimal usa-se o `parseFloat`.

***

## 8. Interaja de maneira diferente com o usuário

### **Campo de texto e botão**

O `document.write` faz com que o usuário possa ler no HTML o que foi escrito no JavaScript. Existe outra função que serve para acessar as tags HTML e criar ações nelas através do JavaScript, a `document.querySelector`.

```js
document.querySelector("input");    // seleciona a tag input
input.value...                      // acessa o valor do input

document.querySelector("button");   // seleciona a tag button
button.onclick...                   // cria uma ação ao usar o button
```

***

## 9. Trabalhe com muitos dados

### **Armazenando muitos dados**

Uma variável pode armazenar um ou mais valores. Quando a variável armazena uma lista de valores, chamamos de `array`. Os campos dessa lista são contados a partir da posição zero.

```js
var segredo = [5, 7, 10, 2];
            // 0, 1,  2, 3 posição da variável na lista
```

### **Propriedades de um array**

Uma propriedade muito útil nas listas é a `.length`. Ela é usada para substituir um limite na condição do `for` ao contar os valores de um `array`, retornando o número de elementos da lista.

```js
var segredos = [5, 7, 10, 2, 3];

for(var posicao = 0; posicao > segredos.length; posicao++) {
    ...
}
```

Outra propriedade bastante utilizada em listas é a `.push`. Ela é usada para adicionar mais elementos na lista, sem precisar editar a lista manualmente.

```js
var frutas = ["maçã", "cajú", "manga"];

frutas.push("pera");
```

[🔝 Voltar ao topo 🔝](#javascript-e-html---lógica-de-programação)
