# First Class Function

## PRIOR KNOWLEDGE
- argument

## Keypoints
- First-Class Function: 
  - Functions can be pass as arguments
  - You can the return a function from functions
  - Save them in variables.

function = first class objects


### Functions can be pass as arguments
```
function b(f){
}

function a(){

}

b(a) //functions can be passed as a argument  = function a can be passed in b as a argument
```

### You can the return a function from functions
```
function b(){
  return a();
}

function a(){

}

b(a) //You can the return a function from functions = You can return a from b
```


### Save them in variables.
```
const b = function(){ // Save them in variables b
  return a();
}

b(a)
```
