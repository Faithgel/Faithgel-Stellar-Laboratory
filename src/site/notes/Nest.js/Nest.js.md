---
{"dg-publish":true,"permalink":"/nest-js/nest-js/"}
---

```ad-important
title: Revisar Conceptos de Ingenieria de Software. 
Si ya tienes conocimiento del area puedes saltarte este callout, pero si no los tienes o te interesa revisa aquí: [[Ingenieria de Software]]
```
# Basics

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/typescript/typescript/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Typescript
## Introduction
```ad-summary
title: Approach

TypeScript se encuentra en una relación inusual con JavaScript. TypeScript ofrece todas las características de JavaScript, y una capa adicional sobre éstas: El sistema de tipos de TypeScript.

Por ejemplo, JavaScript proporciona primitivas del lenguaje como **string** y **number**, pero no comprueba que los hayas asignado consistentemente. TypeScript sí lo hace.

Esto significa que tu código JavaScript existente también es código TypeScript. El principal beneficio de TypeScript es que puede resaltar comportamientos inesperados en tu código, reduciendo la posibilidad de errores.

```
### Basics
#### Types
```ad-todo
title: Types by Inference

TypeScript conoce el lenguaje JavaScript y generará tipos por ti en muchos casos. Por ejemplo, al crear una variable y asignarle un valor concreto, TypeScript utilizará el valor como tipo.

```ts
//Esto es equivalente a realizar esto -> let hello:string = "Hello World";
let hello = "Hello World"; 
```
```ad-info
title: Defining Types

Puedes utilizar una gran variedad de patrones de diseño en JavaScript. Sin embargo, algunos patrones de diseño dificultan que los tipos se infieran automáticamente (por ejemplo, los patrones que utilizan programación dinámica). Para cubrir estos casos, TypeScript soporta una extensión del lenguaje JavaScript, que ofrece lugares para que le digas a TypeScript cuáles deberían ser los tipos.
```

```ad-info
title: Composing Types
With TypeScript, you can create complex types by combining simple ones. There are two popular ways to do so: with unions, and with generics.
```
```ad-example
title: Union (1)
Con una unión, puede declarar que un tipo puede ser uno de muchos tipos. Por ejemplo, puede describir un tipo booleano como verdadero o falso:
```ts
type MyBool = true | false;
```
```ad-example
title: Union (2)
Un caso de uso popular para los tipos de unión es describir el conjunto de literales de cadena o numéricos que un valor puede ser:
```ts
type WindowStates = "open" | "closed" | "minimized";type LockStates = "locked" | "unlocked";type PositiveOddNumbersUnderTen = 1 | 3 | 5 | 7 | 9;
```
```ad-example 
title: Union (3)
Las uniones también permiten manejar distintos tipos. Por ejemplo, puedes tener una función que tome un array o una string
```ts
function getLength(obj: string | string[]) {  return obj.length; }
```
```ad-example 
title: Generics
Los genéricos proporcionan variables a los tipos. Un ejemplo común es un array. Un array sin genéricos puede contener cualquier cosa. Un array con genéricos puede describir los valores que contiene.
```ts 
type StringArray = Array<string>;  type NumberArray = Array<number>;  
type ObjectWithNameArray = Array<{ name: string }>;
```



</div></div>

# ¿Que es Nest? y ¿Por qué debemos usarlo?

```ad-hint 
title: Imaginemos
Tenemos a rose que tiene una tienda y ella vende articulos varios , pero se da cuenta que hay servicios de terceros que le ayudan a vender los porductos que tenga en catalago en stock pero esto mismo no es algo totalmente administrado por ella a lo cual ella tiene la necesidad de un **API** que le permita mostrar lo que ella ofrece tanto para su negocio como para mostrarlo a traves de terceros, pero no es algo robusto ya que su tienda es pequeña.

Ahora supongamos que la tienda de rose comienza a crecer y esta misma API se le es requerido que tenga mecanismos de autenticacion, modulos de E-Commerce, entre otras cosas.

Ante esta nueva necesidad a resolver se necesitara que la API este bien cimentada para soportar la envergadura, si no es posible a que esta misma siga escalando probablemente se tenga que desechar dicha API.

Rose se decide por rehacer todo con nuevas herramientas, caracteristicas y problemas a enfrentar.

- En este caso opta por el camino de usar Node.js para comenzar su proyecto (con la siguiente estructura en su proyecto)

```js
"Rose-API"
"-----------------"
"-package.json"
"-package-lock.json"
```
```ad-hint
title: Imaginemos (Continuacion)
A partir de esto rose comienza a tener varias dudas de como empezar:
-¿Como Manejo las rutas?
-¿Como manejo la autenticacion?
-¿Como estructuro mi proyecto?
   - Controllers
   - Middlewares
   - Validations
   - Exceptions
   - etc...

La ultima pregunta es ¿en que Framework debo usar para mi API?

```
```ad-hint
title: Solucion
Rose despues de investigar un poco decide usar Nest.js ya que este framework le permite tener una estructura robusta y escalable para su API.

Y su sistema de archivos se ve de la siguiente manera:

```js
"Rose-API"
"-----------------"
"-src"
"---app.module.ts"
"---main.ts"
"---app.controller.ts"
"---app.service.ts"
"-test"
"eslintrc.js"
".prettierrc"
"nest-cli.json"
"package.json"
"readme.md"
"tsconfig.build.json"
```

```ad-important
title: Caracteristicas de Nest.js
- **Robusto**: Nest.js es un framework robusto que permite tener una estructura escalable y robusta para tu API.
- **Modular**: Nest.js permite tener un sistema de modulos que con el tiempo se pueden ir reutilizando.
- **Dogmático**: Nest.js tiene una estructura de carpetas y archivos que permite tener un orden y una estructura de trabajo, por lo cual la mayor parte de tu estructura de proyecto es similar a la de otros proyectos.
```
```ad-attention
title: Instalando Nest.js
Para instalar el cli de nest debemos ejecutar el siguiente comando, si te encuentras en un MacOS o alguna distro GNU/linux debes anteponer sudo ya que es un comando de nivel administrador:
```sh
npm i -g @nestjs/cli
```

## Modules
