# Composition

## Key points
- compose = (f,g) => x => f(g(x))




## Description
translate to compose = (f,g) => x => f(g(x)) to code
```
const shout = compose(exclaim, toUpper)
```
