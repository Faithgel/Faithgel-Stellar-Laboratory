---
{"dg-publish":true,"permalink":"/cursos/angular/angular/"}
---

# Conceptos

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/cursos/angular/conceptos/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




## HTTP
```ad-important
title: Protocolo HTTP
- Protocollo cliente-servidor
- No almacena estados de las peticiones (Request / Response)
- Protocolo de Comunicacion de entidades
- Administracion de la cache, Flexibilidad de Origen (CORS)
- Auth y Cookies
- Proxies y Tunneling
- Sesions
```
```ad-success
title: Peticiones y Respuestas HTTP
- Mensajes estructurados( Headers - Format, Multiplexacion)
- Ej Request: (METHOD) (PATH) (PROTOCOL VERSION)
- Ej Response: (PROTOCOL VERSION) (STATUS) (MS)
```
## Usabilidad
```ad-hint
title: Usabilidad
- Forma parte del diseño de la interaccion 
- Sistemas faciles de usar y aprender
- ISO 9241-11

```

```ad-hint
title: Usabilidad (Beneficios)
- Reduccion de costos (Aprendizaje, Ayuda, Diseño Y Mantenimiento)
- Mejor calidad de vida del usuario (Reduce Stress, Aumento de la satisfaccion e Incrementa la productividad).
```

```ad-hint
title: Usabilidad (Evaluacion)
- Exiten 2 categorias para evaluar la usabilidad de un producto 
	- Metodos realizados con usuarios reales.
	- Metodos realizados por expertos.
```

```ad-check
title: Heuristicas de Nielsen
- Visibilidad y Status 
	- Breadcrumbs
- Correspondencia entre mundo real y la app
	- el sistema debe comunicarse en el mismo lenguaje de los usarios
- Control y Libertad (Usuario)
- Prevencion de errores
- Consistenacia y Estandares
- Reconocimiento mas que recuerdo
- Flesixibilidad y eficiencia.
- Estetica y diseño minimalista
- Ayuda a los usuarios para reconocer, diagnosticar, y recuperar errores
- Ayuda y Documentacion

```


</div></div>

# Basics

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/cursos/typescript/typescript/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




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


