---
{"dg-publish":true,"permalink":"/typescript/typescript/"}
---

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

