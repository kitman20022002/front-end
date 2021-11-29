# Currying

## Keypoint 

- Need to meet following two requirements 
  - Currying is a function that takes one argument at a time 
  - Returns a new function expecting the next argument

- Benfits
  - When you want to remember a argument 



## Description 

1. Currying is a function that takes one argument at a time = **addCurry, b and c function takes one argument at a time**
2. Returns a new function expecting the next argument except the last one = **Except for function c, function b and addCurry returns a function**

```
const addCurry = (a) => {
    return (b) => {
        return (c) => {
            return a + b + c
        }
    }
}
```


So to able to use currying 

```
fakeFunction('param1')('param2')('param3');
```

instead of

``` 
fakeFunction('param1', 'param2', 'param3'); 
```
