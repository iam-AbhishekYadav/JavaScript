# Function in JS

- Function is a block of code designed to perform a particular task.  
- Function is executed when "something" invokes it (calls it).

## How to decalre and call Function ??

``` js
function printName() {                      // Function Defination
    console.log("Sachin Yadav");
    console.log("Abhishek Yadav");
}


printName ;                        // Function Refrence

printName() ;                      // Output : Sachin Yadav        --->  Function Call
                                   //          Abhishek Yadav
```

## How to pass Argument and Parameter ??

``` js
function addNumber (num1,num2){               // num1 and num2 are Parameter (can pass anything)
    console.log(num1+num2);                   // Output : 16
}

addNumber(7,9);                              // 7 and 9 are Argument

addNumber(7,"9");                            // 79 ---> Take both Argument as String
addNumber(7,"a");                            // 7a ---> Take both Argument as String
addNumber(7,null);                           // 3 ---> One Argument is null
```

## Return

-  It is used to stop the function’s execution and optionally return a value to the caller.
-  It just sends the output from the function, then we can use it anywhere.
-  The code will not run after the return

``` js
function name(username) {
    return username
    console.log("Sachin");                // will not run because it is after return
}

let username = name ("Abhishek")
console.log("username :" ,username);           // Output : username : Abhishek
```

## Rest Parameter 

- It allows us to represent an indefinite number of arguments as an array.
- It is prefixed with three dots (...).
- It return Array.

``` js
function cartPrice(...itemPrice){
    return itemPrice
}

let finalCartprice = cartPrice(200,700,500,600);
console.log(finalCartprice);                            // Output : [ 200, 700, 500, 600 ]
```

## How to pass Object in Function ??

``` js
const user = {
    username: "Abhishek",
    price: 199
}

function handleObject(anyobject){
    console.log(`Username is ${anyobject.username} and price is ${anyobject.price}`);    // Output : 1 and 2
}

handleObject(user)                   // Output 1 : Username is Abhishek and price is 199

handleObject({                        // Output 2 : Username is Sachin and price is 399
    username: "Sachin",
    price: 399
})
```

## Function Expression/Hoisting

- Functions can be called before they are declared.
- When function is stored in any variable then it can not be called before they are declared.

``` js
console.log(addone(5))          // Output : 6

function addone(num){
    return num + 1
}


console.log(addTwo(5))          // ReferenceError: Cannot access 'addTwo' before initialization

const addTwo = function(num){
    return num + 2
}

console.log(addTwo(5))          // Output : 6
```

## Arrow Function

It is more concise and readable way to write function expressions.  

### How to decalre and call Arrow Function ??

``` js
let printName = (name) => {
    console.log(name);                   // Output : Sachin
}

printName("Sachin")
```

### Explicit and Implicit Return 

**(a) `Explicit Return`**

A function is returned values using the return keyword, it’s called an explicit return.  

``` js
let aadone = (num) => {
    return num + 1                      // Explicit Return
}

let addNumber = aadone(15)
console.log(addNumber);
```

**(a) `Implicit Return`**

A function is returned values without using the return keyword, it’s called an implicit return.  

``` js
let aadone = (num) => (num + 1)                 // Implicit Return

let addNumber = aadone(15)
console.log(addNumber);
```

### Parens Rules

Arrow functions can omit parentheses when they have exactly one parameter.  

``` js
let aadone = (num) => num + 1                // Parens Rules

let addNumber = aadone(15)
console.log(addNumber);
```

## Immediately Invoked Function Expressions (IIFE)

They are typically used to create a local scope for variables to prevent them from polluting the global scope.  

**(a) `Named IIFE`**

``` js
(function connectedDB(userName){
        console.log(`DB is connected  ${userName}`);          // Output : DB is connected  Abhishek
    }
)("Abhishek");                                                // Function call and ;(Imp)


(function connectedDB2(userName){
        console.log(`DB2 is connected  ${userName}`);          // Output : DB is connected  Sachin
    }
)("Sachin");                                                  // Function call and ;(Imp)
```

**(a) `UnNamed IIFE`**

```js
((userName)=>{
    console.log(`DB2 is connected  ${userName}`);          // Output : DB is connected  Sachin
})("Sachin");
```

> [!NOTE]
> Separate two IIFE functions by semicolon ( ; ).
