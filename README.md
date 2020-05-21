# Javascript Coding Conventions
Coding conventions secure quality, improve code readability and make code maintenance easier. They can be documented rules for teams to follow, or just be your individual coding practice.

Following coding conventions can help make your code more consistent, predictable and readable.

## Magic/unknown Numbers

```const SECONDS_IN_A_DAY = 86400;```

```for (let i = 0; i < SECONDS_IN_A_DAY; i++) {}```


## Deep Nesting Statements

```const retrieveFinalValue = [[['value']]];```

```const retrieveFinalValue = () => {``` <br/>
```  if (Array.isArray(element)) {```<br/>
```    return retrieveFinalValue(element[0]);```<br/>
  ```}```<br/>
```  return element;```<br/>
```};```

## Stop writing comments - code must speak for itself, make it self documenting

```const addMultiplySubtract = (a, b, c) => {``` <br/>
```  // addition```<br/>
```  const addition = a + b + c;```<br/>
```  // multiplication```<br/>
```  const multiplication = a * b * c;```<br/>
```  // subtraction```<br/>
```  const subtraction = a - b - c;```<br/>
<br/>
```  return `${addition} ${multiplication} ${subtraction}`;```<br/>
```};```<br/>

## Avoid large functions
```const addition = (a, b, c) => a + b + c; ```<br/>
```const multiply = (a, b, c) => a * b * c;```<br/>
```const subtract = (a, b, c) => a - b - c;```<br/>

## Code repetition

```const getUserCredentials = user => {```<br/>
```const name = user.name;```<br/>
```const surname = user.surname;```<br/>
```const age = user.age;```<br/>
```const email = user.email;```<br/>
```};```<br/>

```const getUserCredentials = user => {```<br/>
```const { name, surname, age, email } = user;```<br/>
```};```<br/>

## Variable naming

```const camelCase = '';```<br/>
```let randomCamelCaseName = '';```<br/>
```let addCamelCaseNameInHere = '';```<br/>
```var niceCamelCaseNaming = '';```<br/>

## Meaningful names

```getUserPosts;```<br/>
```getUserData;```<br/>
```getUserInfo;```<br/>

## Favor descriptive over concise

```findUserByNameOrSurname;```<br/>
```setUserLggedInTrue;```<br/>

## User shorter version of naming

```getUser;```<br/>

## Use consistent verbs per concept

## functions will usuallu create, read, update and delete something

```getQuestions; // get```<br/>
```returnUsers; // get```<br/>
```retriveUsers; // get```<br/>

## Make booleans that read well in if-the statements

```sedan, sold, green, airbag;```<br/>

```isSedan, isSold, isGreen, hasAirbag;```<br/>

```car.isSedan;```<br/>
```car.isSold;```<br/>
```car.isGreen;```<br/>
```car.hasAirbag;```<br/>

## Use nouns for classNames

```class Car {}```<br/>
```class Elephant {}```<br/>
```class Plane {}```<br/>
```class Country {}```<br/>

## Use PascalCase for classNames

```ThisIsPascalCaseNaming;```

## Capitaliza constant values SNAKE UPPER CASE

```const SECONDS_IN_A_DAY = 86400;```<br/>
```const HOURS_IN_DAY = 24;```<br/>
```const USER_AGE = 29;```<br/>

## Avoid one-letter variable names

```const q = () => {}; // it does not mean anything```<br/>
```const query = () => {}; // this refers that there is a query around```<br/>
```const newDate = () => Date();```
