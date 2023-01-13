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
```ad-todo
title: Types by Inference

TypeScript conoce el lenguaje JavaScript y generará tipos por ti en muchos casos. Por ejemplo, al crear una variable y asignarle un valor concreto, TypeScript utilizará el valor como tipo.

```ts
//Esto es equivalente a realizar esto -> let hello:string = "Hello World";
let hello = "Hello World"; 
```
```ad-info
title: Defining Types
collapse: open
Puedes utilizar una gran variedad de patrones de diseño en JavaScript. Sin embargo, algunos patrones de diseño dificultan que los tipos se infieran automáticamente (por ejemplo, los patrones que utilizan programación dinámica). Para cubrir estos casos, TypeScript soporta una extensión del lenguaje JavaScript, que ofrece lugares para que le digas a TypeScript cuáles deberían ser los tipos.
```

