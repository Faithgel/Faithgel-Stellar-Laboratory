---
{"dg-publish":true,"permalink":"/angular/angular/"}
---

# Angular
## Basics

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/typescript/typescript/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




# Typescript
## Introduction
```ad-summary
title: Approach
collapse: open
TypeScript se encuentra en una relación inusual con JavaScript. TypeScript ofrece todas las características de JavaScript, y una capa adicional sobre éstas: El sistema de tipos de TypeScript.

Por ejemplo, JavaScript proporciona primitivas del lenguaje como **string** y **number**, pero no comprueba que los hayas asignado consistentemente. TypeScript sí lo hace.

Esto significa que tu código JavaScript existente también es código TypeScript. El principal beneficio de TypeScript es que puede resaltar comportamientos inesperados en tu código, reduciendo la posibilidad de errores.

```
### Basics
```ad-todo
title: Types by Inference
collapse: open
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



</div></div>
