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

## 3 Do-While Loop

### Syntax :
> do {  
> &nbsp; &nbsp; &nbsp; &nbsp;  // Code to execute  
> } while (condition);


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


















