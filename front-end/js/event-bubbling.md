# Event Bubbling 

## PRIOR KNOWLEDGE


## Tag
- glossary,js,front-end

## Key points:
- Understand what is event bubbling
- Understand when does it happen 

## Definition
1. What is event bubbling ? 
 - A proccess when a event is trigged and it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

2. When does it happen ?
  - When a event get triggered, (eg: onClick, onBlur, onChange....) 

```
<style>
  body * {
    margin: 10px;
    border: 1px solid blue;
  }
</style>

<form>FORM
  <div>DIV
    <p>P</p>
  </div>
</form>

<script>
  for(let elem of document.querySelectorAll('*')) {
    elem.addEventListener("click", e => alert(`Capturing: ${elem.tagName}`), true);
    elem.addEventListener("click", e => alert(`Bubbling: ${elem.tagName}`));
  }
</script>
```

```
form           / \
---------------| |-----------------
| div     | |                |
|   -----------| |-----------     |
|   |p  | |          |     |
|   -------------------------     |
|        Event BUBBLING           |
-----------------------------------
```

## Use cases

## Not to use 

## Example

