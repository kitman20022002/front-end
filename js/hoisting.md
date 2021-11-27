# Hoisting

## PRIOR KNOWLEDGE
 - function expression 
 - class expression

## Key points:

- Advantages of hoisting is that it lets you to use a function before you declare it in your code
- How does hoisiting work: The Interpreter builds a tree (AST) to declare all the **functions** , **variables**, **classes** and assign a default value before the code get executed   

## Function hoisting
As mentions above one of the advantages of hoisting is that it lets you use a function before you declare it in your code.
```
catName("Tiger");

function catName(name) {
  console.log("My cat's name is " + name);
}
/*
The result of the code above is: "My cat's name is Tiger"
*/
```
Without hoisting you would have to write the same code like this:
```
function catName(name) {
  console.log("My cat's name is " + name);
}

catName("Tiger");
/*
The result of the code above is the same: "My cat's name is Tiger"
*/
```

## Varaible hositing
- **Before** the **first line get executed** the JS will **declared and initialized values **undefined**
- If you try to **call the variables before** it **initialized**, the value will be **undefined**

## Class hositing


## Misunderstanding Concpts
- **function expression** in **not hoisted**
- **class expression** in **not hoisted**
