# TypeScript

Learning Basic TypeScript

https://www.youtube.com/watch?v=WBPrJSw7yQA&ab_channel=Codevolution

What and Why

-Open sourse propgramming language from microsoft
-Type superset of JavaScrpit
-Compiles down to plain JavaScipt
-Relation to Java
-IDE support
-Rapid growth and use
typescript is the main programming language of angular
found it's way to react and vue as well

Learning TypeScript:

1. Environment Setup
2. Variable Declarations
3. Variable Types
4. Functions
5. Interface
6. Class and Access Modifiers

# Environment Setup

1.  using command prompt (cmd)

        npm install typescript --save-dev
        npm install -g typescript

    - run the command, create a js file

          tsc main.ts

    - run main.js file

          node main

2.  Adding export or import statement Treats the file as a module instead of a script

        export {}

3.  Automatically recomplie typescript file whenever there is a change
    -run the command

        tsc main --watch

Any changes in main.ts will create a js file with the new code
-run another command and run main.js
node main

# Variable Declarations

1. let , const

2. Variable Types

   1. boolean, number, string

   2. intellisense, Static type checking

      let total: number = 0;

   3. null , undefined

      let isNew: boolean = null;
      let myName: string = undefined;

   4. array

      let list1: number[] = [1, 2, 3];
      let list2: Array<number> = [1, 2, 3];

      -fixed number
      let person1: [string, number] = ["Chris", 22];

   5. enum

      enum Color {Red = 5, Green, Blue,}
      Green is 6

   6. any

      let randomValue: any = 10;
      randomValue = true;
      randomValue = "Vishwas";

   7. unknwon

      let myVariable: unknown = 10;
      (myVariable as string).toUpperCase(); //type assertion

   8. type inference provide static checking and intellisense

      let b = 20;

   9. union type

      let mutiType: number | boolean;
      mutiType = 20;
      mutiType = true;

# Functions

function add(num1: number, num2: number = 15)

1.  method

    optional - num2? can be undefined add(5)
    function add(num1: number, num2?: number): number {
    return num1 + num2;
    }

2.  default , optional parameter

        default - num2: number = 15
        require are set in the first parameter
        optional are set after the first parameter

# Interface

It is possible to specify an object as a type in typescript

1.  Interface as a type

        interface Person {
        firstName: string;
        lastName: string;
        }

        function fullName(person: Person) {
        console.log(`${person.firstName} ${person.lastName}`);
        }

# Class and Access Modifiers

In clean JS there is no concept of classes
In inheritance it was through prototype inheritance

Typescript also supports classes to build applications using the  
object-oriented class-based approach

1.  Class

         class Employee {
         employeeName: string;

         constructor(name: string) {
         this.employeeName = name;
         }

         greet() {
         console.log(`Good Morning ${this.employeeName}`);
         }
         }

2.  inheritance

        class Manager extends Employee {
        constructor(managerName: string) {
        super(managerName);
        }
        delegateWork() {
        console.log(`Manager delegate tasks`);
        }
        }

3.  Public and Private and Protected

        Public for Accessibility
        Private for only class
        Protected for class and derived from it
