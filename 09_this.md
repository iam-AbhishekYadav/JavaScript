# This

- It tell us about current context.
- In JavaScript, the this keyword refers to an object.
- The this keyword refers to different objects depending on how it is used:  

  * `Object method` --> Object  
  * `Alone` --> Global object  &nbsp; (`Because this is running in the global scope`)  
  * `Function` --> Global object  
  * `Event` --> Element that received the event

- In a browser window the global object is [object Window]


``` js
let jsuser = {
    userName : "Sachin",
    emailId : "mail4sachinyadav@gmail.com",

    login : function (){
        console.log(`${this.userName} just login`);    // Output : Sachin just login
        console.log(this);
    },
    th : console.log(this) ,
    
}


// jsuser.login()                     // Output : Sachin just login 
                                      //          { userName: 'Sachin', emailId: 'mail4sachinyadav@gmail.com', login: [Function: login]}

jsuser.userName = "Abhishek"
// jsuser.login()                   // Output :  Abhishek just login 
                                    //           { userName: 'Abhishek', emailId: 'mail4sachinyadav@gmail.com', login: [Function: login]}

jsuser.th                           // Output : {} --> Empty object
```

## This in Classical and Arrow Function

You cannot access variables from **`this`** inside the function.  


**(a) `Classical Function`**
``` js
function name(){
    let userName = "Sachin"
    console.log(this.userName);                // Output : undefined
    console.log(this);                        // Output : <ref *1> Object [global] (node ka gobal deta hai.)
}

name()
```

**(b) `Arrow Function`**
``` js
let printName = (name) => {
    console.log(this.name);               // Output : undefined
    console.log(this);                    // Output : { }                  
}

printName("Sachin")
```
