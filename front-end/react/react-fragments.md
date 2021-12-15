# React Fragments

## Key Points
- Fragments lets you group list of children without adding extra nodes to the DOM
- Short Syntax is <></>

## Tag
glossary,react,front-end

## Definition
- A element lets you group list of children without adding extra nodes to the DOM

### Usuage

Create React Fragments
- Needed to use this if you need a key=""

```
class Columns extends React.Component {
  render() {
    return (
      <React.Fragment>
        <td>Hello</td>
        <td>World</td>
      </React.Fragment>
    );
  }
}
```

Short Syntax of React Fragements: 
- You can use this if you don't need to key=""

```
class Columns extends React.Component {
  render() {
    return (
      <>
        <td>Hello</td>
        <td>World</td>
      </>
    );
  }
}
```
