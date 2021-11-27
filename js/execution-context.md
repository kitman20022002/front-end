# Execution Context

## PRIOR KNOWLEDGE
- Stack
- Queue
- Call Stack/Execution Context Stack

## Key points:

- Created when it invokes a function or global
- It decides what the `this ` , `variables` , `objects`, `functions` in the function can have access to.
- Two types: Global Execution Context , Function Execution Context
- Two Phase: Creation Phase, Execution Phase

![Execution Context ](https://miro.medium.com/max/700/1*bDebsOuhRx9NMyvLHY2zxA.gif)

## Types

### Global execution context

- Is **created** when the file **first loads in the browser** (before line 1)

### Function execution context

- Is **created** when it finds any **function call**

## Phases

- Creation Phase
    - JS Engine parses - run through your code & identifies variables & functions created by code (which will be used in
      execution phase)
    - Setup memory space for Variables & Functions - "Hoisting"
    - Hoisting - before your code is executed, the JS Engine set asides memory space for Var & Func used inside the
      code. These variables & functions comprise the Execution Context of any function that is be executed. All
      variables in JS are initially set to undefined.
- Execution Phase
    - When the code is executed line-by-line (by JS interpreeter) it can access the variables defined inside Execution
      Context
    - Variable assignment are done in this phase
