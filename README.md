# TypeScript Optional Property Bug

This repository demonstrates a common, yet subtle, bug in TypeScript related to optional properties.  The bug is that the compiler doesn't throw an error if you provide an object that is missing a required property, leading to a runtime error.

## The Bug
The `bug.ts` file contains a function `printCoord` that expects an object with `x` and `y` properties.  If you provide an object that is missing either of these properties, the TypeScript compiler doesn't catch this, resulting in a runtime error.

## The Solution
The `bugSolution.ts` file demonstrates a solution by using optional properties and checking if they exist before using them.

## How to Reproduce
1. Clone this repository.
2. Compile the `bug.ts` file using the TypeScript compiler (`tsc bug.ts`).
3. Run the compiled JavaScript file.  You will get a runtime error if you pass an incomplete object to `printCoord`.
4. Repeat this with `bugSolution.ts`.  You will see this version will handle the missing property gracefully.