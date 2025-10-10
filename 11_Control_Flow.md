# # Control Flow

- Control Flow is the order in which statements are executed in a program.

<img src="https://github.com/user-attachments/assets/883eecc4-25e0-4176-bace-70022661c62b" width="600" height="400">

## Types of Conditional Statements

<img width="700" height="500" src="https://github.com/user-attachments/assets/20882fde-d423-466d-abc2-6ab47d714af6" />


> [!WARNING]
> Break --> If condition will be matched and break; is not applied then the code will be executed after that accept default  
> Continou -->

> [!NOTE]
> Truthy values ---> ( "0" , 'false' , "space" , [ ] , { } , function ( ) { } )  
> Falsy values ---> ( false , 0 , -0 , BigInt0n , "" , null , undefined , NaN )

# # NULLISH COALESCING OPERATOR ??  NULL/UNDEFINED

-  A logical operator that returns its right-hand side operand when its left-hand side operand is null or undefined, and otherwise returns its left-hand side operand.

``` js
   let val1;
   val1 = 5??10
   console.log(val1);                  // Output : 5

   val1 = null??10
   console.log(val1);                  // Output : 10

   val1 = undefined??15
   console.log(val1);                   // Output : 15

   val1 = null??10??15
   console.log(val1)                   // Output : 110
``` 

# # Loops/Iterators in JavaScript

## 1. For Loop

### Syntax :
> for ( initialization; condition; increment/decrement )  {      
> &nbsp; &nbsp; &nbsp; &nbsp;  // Code to execute  
> }  

### Flow Chart :
<img width="500" height="500" src="https://github.com/user-attachments/assets/e374bf76-bbb5-4115-8af9-5e132f24f99f" />

### Example :
``` js
for (let i = 1; i <= 3; i++) {
    console.log("Count:", i);               // Output : Count: 1
                                            //          Count: 2
                                            //          Count: 3
}
```

## 2. While Loop

### Syntax :
> while (condition) {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // Code to execute  
> }


### Flow Chart :
<img width="500" height="500" src="https://github.com/user-attachments/assets/d085ee04-ef8f-4c17-9064-52fbf835d3ca" />

### Example :
``` js
let i = 0;
while (i < 3) {
    console.log("Count:", i);               // Output : Count: 0
                                            //          Count: 1
                                            //          Count: 2
    i++;
}
```

## 3. Do-While Loop

### Syntax :
> do {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // Code to execute  
> } while (condition);

### Flow Chart :
<img width="500" height="500" src="https://github.com/user-attachments/assets/b1e9dd1e-d2ec-4abb-b30a-5d31c6710b61" />


### Example :
``` js
let i = 0;
do {
    console.log("Count:", i);                  // Output : Count: 0
                                               //          Count: 1
                                               //          Count: 2
    i++;
} while (i < 3);
```


## 4. For...of Loop

### Syntax :
> for (variable of iterable) {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // statement  
> }


### Example :
``` js
const arr = [1, 2, 3, 4, 5];

for (const num of arr) {
    console.log(num);                     // Output : Print 1 to 5
}

const greetings = "Hello World";
```

> [!WARNING]
> for..of loops is array specific.  
> Don't use in objects, it wil give error, objects are not iterable.  


## 5. Maps 

- The Map object holds key-value pairs and remembers the original insertion order of the keys.
- Any value (both objects and primitive values) may be used as either a key or a value.
- A key in the Map may only occur once; it is unique in the Map's collection.

### Creating a Map

- Map() constructor allows two ways to create a Map in JavaScript.
  - Passing an Array to new Map().
  - Create a Map and use Map.set().

### Example :
``` js
// 1st way of Creating a Map
let abhi = new Map([
    ['name', 'Abhishek Yadav'],
    ['age', 22],
    ['city', 'Delhi']
    
]);
console.log(abhi);                      // Output : Map(3) { 'name' => 'Abhishek Yadav', 'age' => 22, 'city' => 'Delhi' }

// 2nd way of Creating a Map
const sachin = new Map();

sachin.set('name', 'Abhishek Yadav');
sachin.set('age', 22);
sachin.set('city', 'Delhi');

console.log(sachin);                     // Output : Map(3) { 'name' => 'Abhishek Yadav', 'age' => 22, 'city' => 'Delhi' }
```

### Loop on Map

- A Map object is iterated by key-value pairs — a for...of loop.
- It returns a 2-member array of [key, value] for each iteration.

``` js
const sachin = new Map();

sachin.set('name', 'Abhishek Yadav');
sachin.set('age', 22);
sachin.set('city', 'Delhi');

// for...of Loop on Map

// 1st --> It gives different-different array 
for (const key of sachin) {
    console.log(key);                             // Output : [ 'name', 'Abhishek Yadav' ]
                                                  //          [ 'age', 22 ]
                                                  //          [ 'city', 'Delhi' ]
}

// 2nd --> It gives without array
for (const [key,value] of sachin) {
    console.log(key, ':-', value);                  // Output : name :- Abhishek Yadav
                                                    //          age :- 22
                                                    //          city :- Delhi
}
```

## 6. For..in Loop

### Syntax :
> for (variable in object) {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // statement  
> }

### Example :
``` js
const obj = {
	js : "JavaScript",
	py : "Python",
    cpp : "C++",
    rb : "Ruby"
};

// It will gives only Key
for (const key in obj) {
	console.log(key);                      // Output : js py cpp rb
}

// It willgives value of key
for (const key in obj) {
	console.log(obj[key]);                  // Output : JavaScript Python C++ Ruby
}
```

> [!NOTE]
> for..in loops is object specific.  
> It apply on Arrays also but it will give key/Indexes only

``` js
const obj = ["js", "rb", "py", "java", "cpp",];

// It will give key/Indexes
for (const key in obj) {
	console.log(key);                  // Output :  Print 0 to 4
}

// It Willgives value of key
for (const key in obj) {
	console.log(obj[key]);                  // Output : js rb py java cpp
}
```

> [!WARNING]
> Don't use for...in loop in Map(), it will give error.  
> Maps are not iterable.


## 7. For...each Loop

### Syntax :
> variableName.forEach(callbackFn) {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // statement  
> }

### Example :
``` js
const code = ["js", "rb", "py", "java", "cpp",];

// 1st Way
code.forEach( function (items) {
    console.log(items);                  // Output : js rb py java cpp
})

// 2nd Way
code.forEach((items) => {
    console.log(items);                  // Output : js rb py java cpp
})

//3rd Way
function printMe(items){
    console.log(items);
}

code.forEach(printMe);                  // Output : js rb py java cpp

// 4th Way --> It will give Values, Indexes and Array
code.forEach((items, index, arr) => {
    console.log(items, index, arr);                   // Output : js 0 [ 'js', 'rb', 'py', 'java', 'cpp' ]
                                                      //          rb 1 [ 'js', 'rb', 'py', 'java', 'cpp' ]
                                                      //          py 2 [ 'js', 'rb', 'py', 'java', 'cpp' ]
                                                      //          java 3 [ 'js', 'rb', 'py', 'java', 'cpp' ]
                                                      //          cpp 4 [ 'js', 'rb', 'py', 'java', 'cpp' ]
})
```

### Object inside Array --> [{ }]

``` js
const myCoding = [
    {
        lanuageName : "JavaScript",
        FileName : "js"
    },

    {
        lanuageName : "C++",
        FileName : "cpp"
    },

    {
        lanuageName : "Python",
        FileName : "py"
    },

    {
        lanuageName : "Ruby",
        FileName : "rb"
    },
];

myCoding.forEach( (items) => {
    console.log(items.lanuageName); 
    console.log(items.FileName);
});

// Output of this Loop --->
// JavaScript
// js
// C++
// cpp
// Python
// py
// Ruby
// rb
```










