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








