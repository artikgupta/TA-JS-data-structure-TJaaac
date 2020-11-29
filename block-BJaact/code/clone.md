1. Write the output with reason

```js
const person = {
  firstName: "John",
  lastName: "Doe",
};

let person2 = person;

person.firstName = "Arya";

console.log(person2.firstName); // output
"Arya", reason: since we know that object are copied by refernce and both the variables are pointing to the same memory location,so when the  value of person is changed value of person2 also gets changed.

console.log(person.firstName); // output

"Arya", reason: since we know that object are copied by refernce and both the variables are pointing to the same memory location,so when the  value of person is changed value of person2 also gets changed.

console.log(person.lastName); // output

"Doe"

console.log(person == person2); // output

true reason: they are pointing to the same memory location

console.log(person === person2); // output

true reason: they are pointing to the same memory location

console.log(person.lastName === person2.lastName); // output

true reason: they are pointing to the same memory location

```

2. Write the output with reason:

```js
let person = {
  firstName: "John",
  lastName: "Doe",
  address: {
    street: "North 1st",
    city: "San Jose",
    state: "CA",
    country: "USA",
  },
};

let personTwo = { ...person };

person.firstName = "Arya";
person.city = "Navada";

console.log(personTwo.firstName); //

"John"
reason: since we are cloning the value of person to personTwo so their address are different, so when we are changing the value of firstName in person its not changing in person2.

console.log(person.firstName); // output

"Arya"

reason: because we changed the value of firstName in person to "Arya"

console.log(personTwo.lastName); // output

"Doe"

since we are cloning the value of person to personTwo and we are not  changing the value of lastName that is why it is same in both person and person2.

console.log(person.firstName === personTwo.firstName); // output

false

because person.firstName ="Arya" and personTwo.firstName="John"

console.log(person == personTwo); // output

false

reason: because they are poiniting to the different memory location.


console.log(person === personTwo); // output
false

reason: because they are poiniting to the different memory location.

console.log(person.address === personTwo.address); // output

true

since we are cloning the value of person to personTwo and we are not  changing the value of address that is why it is same in both person and person2.



console.log(person.address == personTwo.address); // output

true

since we are cloning the value of person to personTwo using spread operator, and it only does shallow cloning and we know that array are created are copied by reference , so the value stored in person is a memory location and the memory location is same for both the address in person and person2.

console.log(personTwo.address.city); // output

 "San Jose"

ssince we are cloning the value of person to personTwo using spread operator, and it only does shallow cloning and we know that array are created are copied by reference , so the value stored in person is a memory location and the memory location is same for both the address in person and person2.

console.log(person.address.city); // output

 "San Jose"

since we are cloning the value of person to personTwo using spread operator, and it only does shallow cloning and we know that array are created are copied by reference , so the value stored in person is a memory location and the memory location is same for both the address in person and person2.

console.log(person.address.city == personTwo.address.city); // output

true

since we are cloning the value of person to personTwo and we are not  changing the value of address that is why it is same in both person and person2.
```

3. Write the output with reason:

```js
let person = {
  firstName: "John",
  lastName: "Doe",
  address: {
    street: "North 1st",
    city: "San Jose",
    state: "CA",
    country: "USA",
  },
};

let personTwo = { ...person, address: { ...person.address } };

person.firstName = "Arya";
person.city = "Navada";

console.log(personTwo.firstName); // output
'Arya'

reason: because we did cloning of person to personTwo so they are pointing towards different memory location so that is when we changed the firstName of person it did not got reflected in the person2

console.log(person.firstName); // output

'John'

reason: because we did cloning of person to personTwo so they are pointing towards different memory location so that is when we changed the firstName of person it did not get reflected in the person2

console.log(personTwo.lastName); // output


"Doe"

since we are cloning the value of person to personTwo and we are not  changing the value of lastName that is why it is same in both person and person2


console.log(person.firstName === personTwo.firstName); // output

false

console.log(person == personTwo); // output

false

because,they are pointing to differnt memory location

console.log(person === personTwo); // output
false

because,they are pointing to differnt memory location

console.log(person.address === personTwo.address); // output

false

because,they are pointing to differnt memory location

console.log(person.address == personTwo.address); // output

false

because,they are pointing to differnt memory location

console.log(personTwo.address.city); // output

"San Jose"

reason: since we are cloning the value of person to personTwo, and not changing the name of the city inside the address that is why it is still "San Jose" and not "Navada"


console.log(person.address.city); // output

"San Jose"

reason: since we are not changing the name of the city inside the address that is why it is still "San Jose" and not "Navada"

console.log(person.address.city == personTwo.address.city); // output
true
reason : because value of city in personOne and personTwo is same.
```

4. Clone the `blogs` variable into a new variable named `clonedBlogs`

```js
let blogs = [
  {
    id: 1,
    title: "Post #1",
    body: "My first blog post",
  },
  {
    id: 2,
    title: "Post #2",
    body: "My second blog post",
  },
  {
    id: 3,
    title: "Post #3",
    body: "My third blog post",
  },
];

let clonedBlogs = [...blogs];

// Your code goes here
```

5. Clone the `question` variable into a new variable named `questionClone`

```js
var questions = [
  {
    prompt: "Why is the sky blue?",
    responses: [
      "Because the color blue was on sale at Wallmart",
      "Because blue is the prettiest color",
      "Because the air molecules difract blue light more than any other color",
    ],
  },
  {
    prompt: "Why are leaves usually green?",
    responses: [
      "So green caterpillars can hide better.",
      "Because leaves can more easily make energy with green light",
      "Because leaves absorb red and blue light so it's green that is reflected",
    ],
  },
];

let questionClone = [...questions];

// Your code goes here
```

6. Clone the `allBlogs` variable into a new variable named `allBlogsClone`

```js
var allBlogs = {
  id: 1,
  title: "Alamofire JSON Serialization",
  body: "All about serialization in Alamofire...",
  author: {
    id: 1,
    fullName: "Jeff Potter",
    username: "jpotts18",
  },
  comments: [
    {
      id: 1,
      body: "Thanks for the help Jeff, this saved me hours",
    },
    {
      id: 2,
      body: "Your welcome. I am happy to help!",
    },
  ],
};

let allBlogsClone = [...allBlogs];

// Your code goes here
```

7. Clone the `person` variable into a new variable named `clonedPerson`

```js
let person = [
  {
    input: { name: "Ryan" },
    output: { name: "Ryan" },
  },
  {
    input: { name: { first: "Ryan", last: "Haskell-Glatz" } },
    output: { firstName: "Ryan", lastName: "Haskell-Glatz" },
  },
  {
    input: { name: "Ryan", age: 24 },
    output: { name: "Ryan", age: 24 },
  },
  {
    input: {
      name: { first: "Ryan", last: "Haskell-Glatz" },
      birthday: { year: 1993, month: "Nov" },
    },
    output: {
      firstName: "Ryan",
      lastName: "Haskell-Glatz",
      birthdayYear: 1993,
      birthdayMonth: "Nov",
    },
  },
];

let clonedPerson = [...person];

// Your code goes here
```

8. Write a function named `cloneObject` that accepts an object and returns the clone of the object

```js
function cloneObject(obj) {
  return { ...obj };
}

// Run the test below to check your function

let user = {
  name: "John",
  house: "Stark",
  sisters: ["Arya", "Sansa"],
};
let cloned = cloneObject(user);

let person = {
  firstName: "John",
  lastName: "Doe",
  address: {
    street: "North 1st",
    city: "San Jose",
    state: "CA",
    country: "USA",
  },
};

let clonedPerson = cloneObject(user);

console.log(
  `The user object is ${
    user == cloned ? `not clone` : `cloned successfully 😁👑`
  }`
);
The user object is cloned successfully 😁👑

console.log(
  `The person object is ${
    person == clonedPerson ? `not clone` : `cloned successfully 😁👑`
  }`
);

The person object is cloned successfully 😁👑
```
