1. What will be the output and explain the reason.

```js
let obj = { name: 'Arya' };
obj = { surname: 'Stark' };
let newObj = { name: 'Arya' };
let user = obj;
let arr = ['Hi'];
let arr2 = arr;
```

Answer the following with reason after going through the above code:

- `[10] === [10]` //false.Beacuse every time we user {} OR [] to create an object or arrayit gets created onto a new address. and since the address is different it will return false.
- What is the value of obj? // { surname: 'Stark' }
- `obj == newObj`//false as these two are seperate objects that are created on different addresses.
- `obj === newObj`//as here both of them are of same datatype "object" it will return the same value as "==" and hence will return false since obj and newObj are stored at different address.
- `user === newObj`//false.both contain to different address.
- `user == newObj`false.Return same result as '==='.
- `user == obj`true.Both contain the same address i.e point to the same address where the object is stored.
- `arr == arr2`//true.Both contain same address.
- `arr === arr2`//true.Since both are of same data type,will return same output as "=="

2. What's will be the value of `person1` and `person2` ? Explain with reason. Draw the memory representation diagram.

<!-- To add this image here use ![name](./hello.jpg) -->

```js
function personDetails(person) {
  person.age = 25;
  person = { name: 'John', age: 50 };
  return person;
}
var person1 = { name: 'Alex', age: 30 };
var person2 = personDetails(person1);
console.log(person1);
console.log(person2);
```

3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); //1. output
console.log(user.brothers.length === brothers.length); //2. output
```
