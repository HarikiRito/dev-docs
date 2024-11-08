# TypeScript Guide

## 1. Introduction

TypeScript is a programming language that is a superset of JavaScript. It is a statically typed language that compiles to JavaScript.
You may ask why we need TypeScript when we already have JavaScript. The main reason is that TypeScript is a statically typed language, which means that the types of variables are known at compile time, not at runtime. This helps us to catch errors at compile time, not at runtime, which is the main reason why we need TypeScript. Also, collaboration between developers is easier since everyone will know the types of variables at compile time without any additional documentation or need to run the code.

For all of my projects, TypeScript is a must-have, even if it's a personal project. 

## 2. Basic Types

TypeScript has only three primitive types: `number`, `string`, and `boolean`. These types can later be used to construct more complex types.
You can read more about the primitive types [here](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html).


## 3. Object Types

This is where TypeScript starts to show its strength. In JavaScript, we mostly deal with objects. There are two main ways to define the types of properties of an object:

- Interface
- Type

While both of them are similar, I recommend using `type` over `interface` because `type` is more powerful and flexible than `interface`.
Read more [here](https://www.typescriptlang.org/docs/handbook/2/objects.html).

## 4. Generic Types

Generic types are a powerful feature of TypeScript that allows us to create reusable and flexible types. This is a very important concept that you should understand and master since it allows you to go beyond the object types and open up a lot of possibilities. Usually, generic types are used to create reusable components that need different types of data but share the same structure.

Read more [here](https://www.typescriptlang.org/docs/handbook/2/generics.html).

## 5. Other Features

There are many other features that TypeScript has, but I think the above are the most important ones that you should understand and master. We have Conditional Types, Union Types, Intersection Types, Type Guards, Type Casting, etc. But these are more advanced topics that you can learn when you get more familiar with TypeScript. Usually, when you finish learning generic types, you will have a good enough understanding of TypeScript to start working on any project at the enterprise level. I recommend you read other sections in the handbook to get more familiar with TypeScript after learning the Generic Types.

## 6. What to Avoid
In TypeScript, there is a dangerous pattern that you should avoid at all costs, which is using the `any` type. The `any` type is a type that allows you to assign any value to a variable, which means you lose all the benefits of TypeScript. You should avoid using the `any` type at all costs since it will defeat the purpose of using TypeScript.

As an alternative, you can use the `unknown` type, which is a type that allows you to assign any value to a variable, but you need to narrow the type before using the variable. This will force you to handle all the cases, avoiding potential errors.

In my case, I will never allow anyone on my team to use the `any` type, unless they are working on a legacy codebase where type information is not available, or they can explain the reason why they need to use the `any` type with convincing arguments.