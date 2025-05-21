# Object in JS

- We can store properties and methods in objects.
- It work on Heap Memory.

**Declaring of Objects** &nbsp; --> `2 Ways to declare Object in JS.`

--> 1st Way to declare object by `Singleton (Made through constructor)`
``` js
let obj = new Object();
obj.name = "Sachin";

console.log(obj.name);       // Output : Sachin    // 1st Way to access/call data from object
console.log(obj["name"]);   // Output : Sachin    // 2nd Way to access/call data from object

console.log(obj);            // Output : { name: 'Sachin' }            


```

--> 2nd Way to declare object by `Non - Singleton (Made through Object Literal)`

It store data in key - pair value.

``` js
let obj={
    name : "Scahin",
    stidentID : "123",
    email : "mail4sachinyadav@gmail.com",
    isLogin : true,
   
}                                                  

console.log(obj.name);           // Output : Scahin
console.log(obj.stidentID);      // Output : 123
console.log(obj.email);          // Output : mail4sachinyadav@gmail.com
console.log(obj.isLogin);        // Output : true

console.log(obj);                // Output : { name: 'Scahin', stidentID: '123', email: 'mail4sachinyadav@gmail.com', isLogin: true }
```

## How to store Symbol in Object ??

It is store by symbol key word.

``` js
let sym = Symbol("Abhi1234")            // How to store symbol in object
let obj3 ={
    name : "Scahin",
    stidentID :"123",
    [sym] : "Abhishek Yadav"
}                                                  

console.log(obj3.name);
console.log(obj3.stidentID);
console.log(obj3[sym]);                // Output : Abhishek Yadav   // How to access/call Symbol

console.log(obj3);                     // Output :  { name: 'Scahin', stidentID: '123', [Symbol(Abhi1234)]: 'Abhishek Yadav' }

```

## Properties and Method of Objects

**(i) `Changing ang Freezing of value/Key`**

``` js
let obj={
    name : "Scahin",
    studentID : 1234 ,
    email : "mail4sachinyadav@gmail.com",
}                                                  

console.log(obj.name);            // Scahin
console.log(obj.studentID);       // 1234
console.log(obj.email);           // mail4sachinyadav@gmail.com

obj.studentID = 6789               // Changing the value
console.log(obj.studentID)         // 6789

Object.freeze(obj);                // Freeze or Lock the Value/Key

obj.email = "email4abhishekyadav@gmail.com"
console.log(obj.email);            // mail4sachinyadav@gmail.com
```

**(ii) `Function inside Object`**

``` js
let obj ={
    name : "Scahin",
    studentID :"123",
}       


 obj.marvelHeroes02 = function () { 
    console.log("Iron Man");               // Output : Iron Man
    console.log(`Hello My name is ${this.name}`);    // Output : Hello My name is Scahin --> string interpolation
}

console.log(obj.marvelHeroes02);           // Output : [Function (anonymous)]   --> We did not call the function
console.log(obj.marvelHeroes02());         // Output : Iron Man -- Call Function by ()
```

**(iii) `Accessing Key, Values, Entries, hasOwnProperty`

- Key : It give array of all keys.
- Values : It give array of all Vaues.
- Entries : It give array of all Key Value pair array.
- hasOwnProperty : Determines whether an object has a property with the specified name. (T/F)

``` js
let obj3 ={
    name : "Scahin",
    studentID :"123",
    age : 21,
    email : "mail4sachinyadav@gmail.com",
}       

console.log(Object.keys(obj3));            // Output : [ 'name', 'stidentID', 'age', 'email' ]
console.log(Object.values(obj3));          // Output : [ 'Scahin', '123', 21, 'mail4sachinyadav@gmail.com' ]
console.log(Object.entries(obj3));         // Output : [ ['name','Scahin'], ['stidentID','123'], ['age',21], ['email','mail4sachinyadav@gmail.com'] ]
console.log(obj3.hasOwnProperty("name"));  // Output : true
```
**(iv) `Nesting of Objects`**

``` js
const regularUser = {
    email: "sachin@gmail.com",
    fullname: {
        userfullname: {
            firstname: "Sachin",
            lastname: "Ydava"
        }
    }
}

console.log(regularUser.fullname.userfullname.firstname);  // Output : Yadav
```

**(v) `Destructing of Object`**

**(a) `Adding two objects into another object`**

``` js
let obj1 = {
    name : "Sagar Shah"
}

let obj2 = {
    email : "mail4sachinyadav@gmail.com",
}

let obj3 = {obj1,obj2};               // Type - 1
console.log(obj3);                   // Output :  {obj1:{ name: 'Sagar Shah' } ,obj2:{ email: 'mail4sachinyadav@gmail.com' }}


let obj4 ={...obj1,...obj2};         // Type - 2
console.log(obj4);                   // { name: 'Sagar Shah', email: 'mail4sachinyadav@gmail.com' }



let obj5 =Object.assign ({},obj1,obj2);          // Type - 3
console.log(obj5);                              // { name: 'Sagar Shah', email: 'mail4sachinyadav@gmail.com' }
```

**(b) `How to access object without Dot ??`**

``` js
let obj1 ={
    name : "Scahin",
    studentID :"123",
    age : 21,
    email : "mail4sachinyadav@gmail.com",
}       


let {name, studentID, age, email} = obj1

console.log(name);             // Output : Scahin
console.log(studentID);        // Output : 123
console.log(age);              // Output : 21
console.log(email);            // Output : mail4sachinyadav@gmail.com

let {name : userNmae} = obj1    // Chnge Key in Object
console.log(userNmae);         // Output : Scahin
```
