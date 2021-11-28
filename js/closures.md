# Closures

## PRIOR KNOWLEDGE
- Lexical environment

## Key points:

- Closures would need to match the following **Two Requiements**
    - **function bundled together**
    - **references** to its **surrounding state** (references to its surrounding state in JS = lexical environment) 
- Benfits
    - Closure gives you access to an outer function’s scope from an inner function


## Description 
**Closures** has to match **two conditions**
1. The combination of a function bundled together, which looks like following = doStuff and abc are bundled together
```
function doStuff() {
    function abc(){
        
    }
}
`````

2. **References to its surrounding state** in JS we **use lexical environment** (This need to **based on previous condition**) = abc can access the variable surroundingState

```
function doStuff() {
    const surroundingState = 'hi'
    function abc(){
        console.log(surroundingState)
     }
}
//will output hi
```

Which a Closures end result will look like  
```
function doStuff() {
    const surroundingState = 'hi'
    function abc(){
        console.log(surroundingState)
     }
}
//will output hi
```

1. **The combination of a function bundled together = doStuff and abc function**
2. **References to its surrounding state = surroundingState have access to the const surroundingState** 

