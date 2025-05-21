## # String

**Declaring of String**

``` js
let name = "Abhishek";
let repo = 5;

console.log(`My name is ${name} and repocount is ${repo}`);      // My name is Abhishek and repocount is 5  {Template Literals}
console.log(name,repo);                                          // Abhishek 5
```

**String Index** = which character is at which index.

``` js
let name = new String("Abhishek yadav")
console.log(name[5]);       // h
```

**Proto** = It give us property and methods of string.

``` js
let name = "Abhishek";
let repo = 5;

console.log(name.__proto__);     // Node ----> Empty object = {}
                                 // Browser par sari properts and Methods deta hai
```

**Properties and Methods of String** 

``` js
let userName = "Abhishek";

console.log(userName.length);                // Length of string = 8 ------>(Poperty)
console.log(userName.toUpperCase());         // Change all character into upper case = ABHISHEK   ----->(Method)
console.log(userName.toLowerCase());         // Change all character into lower case = abhishek
console.log(userName.charAt(2));            // Returns the character at the specified index = h
console.log(userName.charCodeAt(0));        // Returns the character at the specified index. = 98 (Unicode / Ascii value)
console.log(userName.indexOf("b"));         // Returns the position of the first occurrence of a substring = 1
```

> [!NOTE]
> String is immutable ( something that cannot be changed. )
> ``` js
> let name = "Sachin Yadav"
> console.log(name);         // Sachin Yadav
>
> name[0] = "A"
> console.log(name);        // Sachin Yadav
> ```

## # Numbers

**Declaring of Numbers** &nbsp; --> `2 Ways to declare Numbers in JS.`  

--> 1st Way to declare Number

``` js
const score = 400
console.log(score)         // 400   {typeof = number}
```
--> 2nd Way to declare Number

``` js
const balance = new Number(100)
console.log(balance)        // node [Number: 400]  // browser Number {400} [[Prototype]]: Number [[PrimitiveValue]]: 400
```

**Methods in Numbers**

``` js
const num = 112307.856;

console.log(num.toExponential(5));              // 1.12308e+5
console.log(num.toFixed(6));                    // 112307.856000
console.log(num.toLocaleString("en-US"));       // 112,307.856
console.log(num.toPrecision(6));                // 112308
console.log(num.toString().length);             // 10
console.log(num.valueOf(2));                    // 112307.856
```

**Checking if values are finite, integers, or NaN**

``` js
const num = 112307.856;

console.log(Number.isFinite(num));               // true
console.log(Number.isInteger(num));              // false
console.log(Number.isNaN(num));                  // false
```
