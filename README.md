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

- var is globally scoped, on the other hand let and const are block scoped.

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

- let can be updated, but re-declared

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
