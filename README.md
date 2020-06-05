
# Javascript Coding Conventions
Coding conventions secure quality, improve code readability and make code maintenance easier. They can be documented rules for teams to follow, or just be your individual coding practice.

Following coding conventions can help make your code more consistent, predictable and readable.

## Magic/unknown Numbers 🎩

```javascript
const SECONDS_IN_A_DAY = 86400;
```

```javascript
for (let i = 0; i < SECONDS_IN_A_DAY; i++) {}
```


## Deep Nesting Statements 🕸

```javascript
const retrieveFinalValue = [[['value']]];

const retrieveFinalValue = () => {
    if (Array.isArray(element)) {
        return retrieveFinalValue(element[0]);
        }
    return element;
};
```

## Stop writing comments - code must speak for itself, make it self documenting 📃

```javascript
const addMultiplySubtract = (a, b, c) => {
    const addition = a + b + c; // addition

    const multiplication = a * b * c; // multiplication

    const subtraction = a - b - c; // subtraction

    return `${addition} ${multiplication} ${subtraction}`;
};
```

## Avoid large functions
```javascript
const addition = (a, b, c) => a + b + c;
```
```javascript
const multiply = (a, b, c) => a * b * c;
```
```javascript
const subtract = (a, b, c) => a - b - c;
```

## Code repetition 🔁

```javascript
const getUserCredentials = user => {
    const name = user.name;
    const surname = user.surname;
    const age = user.age;
    const email = user.email;
};
```
```javascript
const getUserCredentials = user => {
    const { name, surname, age, email } = user;
};
```

## Variable naming 🐫

```javascript
const camelCase = '';
let randomCamelCaseName = '';
let addCamelCaseNameInHere = '';
var niceCamelCaseNaming = '';
```

## Meaningful names

```javascript
getUserPosts;
getUserData;
getUserInfo;
```

## Favor descriptive over concise 👍🏻

```javascript
findUserByNameOrSurname;
setUserLggedInTrue;
```

## User shorter version of naming 🩳

```javascript
getUser;
```

## Use consistent verbs per concept

## Functions will usually Create, Read, Update and Delete something `(CRUD)` 🗄

```javascript
getQuestions; // get
returnUsers; // get
retriveUsers; // get
```

## Make booleans that read well in if-the statements

```javascript
sedan, sold, green, airbag;
```

```javascript
isSedan, isSold, isGreen, hasAirbag;
```

```javascript
car.isSedan;
car.isSold;
car.isGreen;
car.hasAirbag;
```

## Use nouns for classNames

```javascript
class Car {}
class Elephant {}
class Plane {}
class Country {}
```

## Use PascalCase for classNames 

```javascript
ThisIsPascalCaseNaming;
```

## Capitalized constant values 🐍 SNAKE UPPER CASE

```javascript
const SECONDS_IN_A_DAY = 86400;
const HOURS_IN_DAY = 24;
const USER_AGE = 29;
```

## Avoid one-letter variable names

```javascript
const q = () => {}; // it does not mean anything
const query = () => {}; // this refers that there is a query around
const newDate = () => Date();
```
