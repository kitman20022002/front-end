# Promise 

## PRIOR KNOWLEDGE
- Asynchronous programming

## Questions 
- What is Promise ? 
- How to create a Promise ? 

## Key points:
- 

## Description 
a proxy for a value that will eventually become available.
A promise is an object that encapsulates the result of an asynchronous operation
Each promise has state, which can have one of the following values:
- Pending
- Fullfilled with a value
- Rejected for a reason

How to create a promise
```
const promise = new Promise((resolve, reject) => {
  // Async operation logic here....
  if (asyncOperationSuccess) {
    resolve(value); // async operation successful
  } else {
    reject(error);  // async operation error
  }
});
```

### Condition Example 

### Code example 
