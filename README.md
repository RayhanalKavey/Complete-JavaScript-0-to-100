# Complete JavaScript 0-to-100

## What is ECMAScript?

> ECMAScript is a stardart on which JavaScript is based on. It was created to ensure that different documents on JavaScript are actually following the same rules.

## How to Execute JavaScript?

- JavaScript can be execute right inside one's browser. You can open the JavaScript in the browser console and start writing JavaScript there.

- Another way to execute JavaScript is in a runtime like node.js, which can be installed and used to run JavaScript outside of the browser.

- There is another to execute JavaScript is by inserting it inside a `script` tag of an HTML document.

```
<script src="index.js"></script>
```

## Variable

Variable is just like a container. Were we can store string, number, array, etc. as a value inside a variable.

### Rules for naming JavaScript variable

- Variables can be declared with `letter`, `digits`, `underscore` and `$` sign.
- Variables name can start with `$` , `_` or `letter`, except `number`.
- JavaScript reserved word cannot be used as a variable name. For example, `for`, `if`, `var`, `const`, etc.
- Variables name are case sensitive. For example variable name `kavey`, `Kavey` and `kaveY` are different from each other.
- Camel case are generally used for declaring JavaScript variable. For example, `firstName`, `lastName` etc.

### Dynamically typed language

JavaScript is dynamically typed language because we can change the value of the variable in the run time, like we can change the same variable's value to number, string, array, object, etc.

But in a static typed language like C you declared the types of the variable first and then do some operation later on. You cannot change the variable type in the run time.

### Differences between `var`, `let`, and `const`.

- `var` is globally scoped, on the other hand `let` and `const` are block scoped.

#### Variable `test` with `var`

```
{
  var test = "inside block";
  console.log(test);
}
console.log(test);

Result:-

inside block
inside block
```

#### Variable `test` with `let`

```
{
  let test = "inside block";
  console.log(test);
}
console.log(test);

Result:-

inside block
test is not defined
```

- `var` can be updated and re-declared

#### Variable `test` with `var`

```
var test = 12;

-- Re-declare:-
var test = 23;

-- Update
test = 212;

console.log(test);

Result:-
212
```

- `let` can be updated, but re-declared

```
let test = 12;

-- Update only
test = 212;

console.log(test);

Result:-
212
```

- `const` cannot be updated or de-declared.
- `let` and `var` may or may not be declared before declaration, but `const` must be initialized during declaration.

```
var test1;
let test;
test1 = 2;
test = 4;
console.log(test1);
console.log(test);

--Result:-
2
4
```

## Primitive Data Types and Non-primitive data type(Objects)

### Primitive data types

Primitive data types are fundamental data types. There are `7` primitive data types in JavaScript. These are built-in inside JavaScript.

1. Null
2. Number
3. Symbol
4. String
5. Boolean
6. BigInt
7. Undefined

```
let empty = null;
let number = 432;
let symbol = Symbol("Description of the symbol.");
let string = "kavey";
let bigInt = BigInt("223") + BigInt("7");
let boolean = true;
let notDefined = undefined;
console.log(empty, number, symbol, string, bigInt, boolean, notDefined);

Result:-
null 432 Symbol(Description of the symbol.) kavey 230n true undefined
```

```
console.log(typeof null); // object
console.log(typeof 321); //number
console.log(typeof Symbol("Description of the symbol.")); //symbol
console.log(typeof "kavey"); //string
console.log(typeof BigInt("223")); //bigint
console.log(typeof true); //boolean
console.log(typeof undefined); //undefined
```

### Non-primitive data type(Objects)

- Objects are key value payers. Value could be any types of data types.

```
const obj = {
  firstName: "Rayhan",
  lastName: "Kavey",
};
```

- We cannot reassign a object declared with `const`, but we can change or add key value.

```
const myInfo = {
  name: "rayhan",
  age: 50,
  hasLicense: false,
  friend: "AJ",
};

myInfo["name"] = "kavey";
myInfo["newFriend"] = "Jigri Dost";
console.log(myInfo);

--Result:-
{
  name: 'kavey',
  age: 50,
  hasLicense: false,
  friend: 'AJ',
  newFriend: 'Jigri Dost'
}
```

## Expression and Operators

### Expression

A fragment of code that produce a value is called an expression. Every value written literally is an expression. For example, 34, 'kavey' or true etc.

### Operator(`+,-,/,%,= etc.`) and operands(`2,4,3,5 etc.`)

1. Arithmetic Operator

```
let a = 3;
let b = 2;

console.log("a(3)+b(2)= ", a + b); //5
console.log("a(3)-b(2)= ", a - b); //1
console.log("a(3)/b(2)= ", a / b); //1.5
console.log("a(3)*b(2)= ", a * b); //6
console.log("a(3)**b(2)= ", a ** b); //9
console.log("a(3)%b(2)= ", a % b); //1
```

- Incremental operator

```
console.log("a(3)++= ", a++); //3
//It will display the current value, but increase the value for the next operation. Means next time we use a it will start from value 4

console.log("++a(4)= ", ++a);
//5 //As you can see it took the previous value 4. Then increment the value and display it.
```

- Decremental operator

```
console.log("a(5)--= ", a--); //5
console.log("--a(4)= ", --a); //3
```

2. Assignment Operator

```
let c = 4;
c = 5;
c += 5; // c(5) =c+5 // 10
c -= 5; // c(10) =c-5 // 5
c %= 3; // c(5)= c%2 // 2
c **= 2; // c(2) = c**2 // 4
console.log(c);
```

3. Comparison Operator

```
const a = 4;
const b = 5;

console.log(a == b);  // false  //  equal to
console.log(a != b);  //  true //  not equal
console.log(a === b);  // false  //  equal value and type
console.log(a !== b);  //  true //not equal value or not equal type
console.log(a > b);  // false  // greater than
console.log(a < b);  //  true // less than
console.log(a >= b);  // false  //  greater than or equal to
console.log(a <= b);  //  true //  less then or equal to
console.log(a === b ? "true" : "false");  // false  // ternary operator
```

4. Logical Operator

```
let a = 3;
let b = 4;
console.log(a < b && a == b); // false // and operator
console.log(a < b || a == b); // true // or operator
console.log(!(a < b)); // false // and operator
```

5. Conditional `ternary` operator

The conditional `ternary` operator is the only JavaScript operator that takes `three operands`: a condition followed by a question mark `?`, then an expression to execute if the condition is truthy followed by a colon `:`, and finally the expression to execute if the condition is `falsy`. This operator is frequently used as an alternative to an `if else` statement.

```
console.log(3 > 2 ? "It's true" : "This is a false statement");//It's true
```

## Conditional expression

### Conditional `if else` statement

> A block of code, which must be executed based on some conditions.

For example, you might ask for your age, if your age is greater than 18 you will get a message that you can drive.

There are three forms of if else statement.

- `if`(condition){code execute if true}
- `if`(condition){code execute if true} `else`{code execute if false}
- `if`(condition){code execute if true} `else if`(condition){code execute if true} `else`{code execute if both the condition false}

```
let age = prompt(
  "Input your age for getting a confirmation of having driving license."
);

age = Number.parseInt(age);

if (age < 1) {
  console.log("Please provide a valid age !!");

} else if (age < 18) {
  console.log(
    `Keep patience! and keep learning, you will have to wait ${
      18 - age > 1 ? `${18 - age} years.` : `${18 - age} year.`
    } `
  ); // example of ternary operator

} else if (age <= 60) {
  console.log("You are eligible fo driving!!");

} else {
  console.log("Take a break and enjoy your break!!");
}
```
