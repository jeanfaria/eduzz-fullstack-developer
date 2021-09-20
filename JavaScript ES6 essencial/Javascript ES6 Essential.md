Javascript foi criado por Brendan Eich e lançado em 1995.

Para padronizar o JavaScript, a Netscape o enviou para a ECMA Internacional,uma instituição criada na década de 60 para padronizar processos do mercado de tecnologia da informação.

A ECMA padronizou a linguagem e deu, a esta padronização, o nome de ECMAScript.

É atualmente a principal linguagem para programação client-side em navegadores web. É também bastante utilizada do lado do servidor através de ambientes como o node.js.


## ECMAScript
Especificação e padronização da linguagem de programação

## TC39

[Propostas tc39](https://github.com/tc39/proposals)

## Fluxo de propostas
- Stage 0: strawman
- Stage 1: proposal
- Stage 2: draft
- Stage 3: candidate
- Stage 4: finished

## Ultima versão

ECMAScript 2018 (ES2018)-

## Linguagem interpretada

Código executado TOP-Down  
C e C++ por exemplo são linguagens compiladas em linguagem assembly.

## Linguagem de tipagem fraca

Significa que não há verificação em todas as operações, por exemplo pode-se utilizar operador "+" entre uma string e um numero sem que seja gerado erro.  
ex:  
```javascript
/*Javascript*/  
    var numero = 20;
    var meuTexto = 'Exemplo';
    
    print(numero + meuTexto)
    
/*R: 20Exemplo*/  
```
## Tipagem dinâmica
Não precisa ser expecificado o tipo da variável ao declarar uma variável, é possível atribuir uma String a uma variável que foi abastecida anteriormetne com um número.  
ex:

```javascript  
/*Javascript*/  

var minhaVariavel = 30;    
minhaVariavel = 'Texto';  
console.log(minhaVariavel);
/*R: Texto  */
```

  
```java
/*Java*/  

public class TipagemDinamica {
	public static void main(String[]args) {
		int meuNumero = 10;
		meuNumero = "Texto";
		
		System.out.println(meuNumero);
	}h
}

/*R: error: incompatible types: String cannot be converted to int*/  
```
## TypeScript
Superset da linguagem JS, adiciona tipos e funcionalidades que o JS não tem por padrão por exemplo intefaces, enuns..  

[TypeScript](https://www.typescriptlang.org/play)

## Funções de primeira classe e ordem maior

A funcão pode ser atribuida a uma variavel, estrutura de dados,array,passada por argumento e retornadapor outras funções.  
ex:  

```javascript  

function getName(){
	return 'Futuro fullstack Pierre';
}

function logFn(fn) {
	console.log(fn());
}

const logFnResult = logFn;

const obj = {
	logFn: logFn
}

const arr = [logFn];

logFnResult(getName);

```

## Closure

[O que são closures](https://medium.com/@stephanowallace/javascript-mas-afinal-o-que-s%C3%A3o-closures-4d67863ca9fc)  

[mozilla closure na prática](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Closures#closures_na_pr%C3%A1tica)  

## Currying

```javascript

/*Javascript*/  

function soma(a) {
	return function(b) {
		return a + b;
	}
}

const soma2 = soma(2);

soma2(2);
soma2(3);
soma2(4);
soma2(5);

```

## Hoisting

Significa levantar, declarações de variáveis e funcões, por isso é possível utilizar uma função ou variável que foi declarada somente depois da chamada, é boa prática sempre declarar as funcoes antes de utilizar.  
Ex:  

```javascript
/*Javascript*/  
function fn(){
	console.log(text); // não apresenta erro e retorna undefined
	var text = 'Bootcamp Eduzz Full Stack';
	console.log(text); // passa a retornar o valor atribuído
}

fn();

```


