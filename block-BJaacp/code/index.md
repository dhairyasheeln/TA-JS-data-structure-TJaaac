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
console.log(person1);//{name: 'Alex', age: 25}.Reason: In statement "var person2 = personDetails(person1);" we are passing object "person1" as an arguement to personDetails.This arguement(person that is person1) is passed as a reference which means when we modify person inside the function , person1 will automatically get updated since they both contain the same address.And hence person.age=25 will modidy person.age=25.
console.log(person2);//{name: 'John', age: 50}.Reason:statement person = { name: 'John', age: 50 } does not modify the  person1(passed as an arguement) but is creates a new object(note:using {} creates a new objec at a different address) person with value as{ name: 'John', age: 50 } and returns that object which is further assigned to person 2.
```

3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); //1. true
console.log(user.brothers.length === brothers.length); //2. true
```
