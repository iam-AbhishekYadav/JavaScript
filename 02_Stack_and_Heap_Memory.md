## # Stack and Heap Memory Allocation in JS

### 1. Stack Memory
* A Stack is a linear data structure that follows a particular order in which the operations are performed.  
* The order may be LIFO(Last In First Out) or FILO(First In Last Out).  
* Primitive(copy) values (like strings and numbers) and references to objects are stored in the stack mem

``` js
let name = "Abhi";
let anothername = name;

console.log(name);                  // Abhi
console.log(anothername);           // Abhi

anothername = "Sachin"

console.log(name);                  // Abhi
console.log(anothername);           // Sachin
```
**<------------------------- STACK DIAGRAM ------------------------->**

### 1. Heap Memory

* It is used to store objects and functions in JavaScript.  
* The engine doesn’t allocate a fixed amount of memory. Instead, it allocates more space as required.
* Non Primitive (References) Objects and complex data structures are stored in the heap memory.

``` js
let user = {
    name : "Abhi" ,
    studentId : 123456 }

let anotheruser = user ;

console.log("User name :",user.name);                                     // User name : Abhi
console.log("User StudentId :",user.studentId);                           // User StudentId : 123456

console.log("anotherUser name :",anotheruser.name);                       // anotherUser name : Abhi
console.log("anotherUser StudentId :",anotheruser.studentId);             // anotherUser StudentId : 123456


anotheruser.name = "Sachin";                                             
anotheruser.studentId = 789456;


console.log("User name :",user.name);                                      // User name : Sachin
console.log("User StudentId :",user.studentId);                            // User StudentId : 789456

console.log("anotherUser name :",anotheruser.name);                        // anotherUser name : Sachin 
console.log("anotherUser StudentId :",anotheruser.studentId);              // anotherUser StudentId : 789456
```
**<------------------------- HEAP DIAGRAM ------------------------->**
