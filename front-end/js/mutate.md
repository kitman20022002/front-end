# Mutate

## Key points
- Mutate: modify the array directly

## Example
const persons = [{ "name":"A", "salary":1200 }, { "name":"B", "salary": 1500 }];

persons.forEach(item => item.salary += 1000);

console.log(persons)
