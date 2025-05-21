## # Maths

- It is used to perform mathematical operations on numbers.
- It is Object.

``` js
      console.log(Math);                 // node Object [Math] {}  // browser Math {abs: ƒ, acos: ƒ, acosh: ƒ, asin: ƒ, asinh: ƒ, …}

      console.log(Math.abs(-4));         //  4
      console.log(Math.round(4.6))       //  5
      console.log(Math.ceil(4.2))        //  5
      console.log(Math.floor(4.9))       //  4
      console.log(Math.min(4,3,7))       //  3
      console.log(Math.max(7,9,2))       //  9

      console.log(Math.random())         //  return random number between 0 and 1
      console.log(Math.random()*10)      //  return random number between 1 and 10
      console.log((Math.random()*10)+1)
      console.log(Math.floor(Math.ramdom()*10)+1))  // return without decimal  
```

> [!TIP]
> **FORMULA** &nbsp; --> Random values between any two numbers
> 
> ``` js
> const min = 10
> const max = 20
> Math.floor(Math.random()*(max-min+1))+min       // return random number between 10 to 20
> ```

## # Dates

- It is Object in JavaScript.  
- Month in JavaScript starts with Zero (0).

```js

   let myDate = new Date()
   console.log(typeof myDate)            // object
   console.log(myDate);                  // 2024-08-25T06:20:03.401Z
   console.log(myDate.toString());       // Sun Aug 25 2024 11:51:40 GMT+0530 (India Standard Time)
   console.log(myDate.toDateString());   // Sun Aug 25 2024
   console.log(myDate.toLocaleString()); // 25/8/2024, 11:54:33 am

   let myCreatedDate = new Date(2023,0(month),24)
   console.log(myCreatedDate)            // 2023-01-23T18:30:00.000Z

   let myTimeStamp = Date.now()
   console.log(myTimeStamp)              // 1724567383704 (in millisecond from January 1, 1970, UTC)
   console.log(myCreatedDate.getTime())  // 1674498600000 (in millisecond from January 1, 1970, UTC)
 
   console.log(Math.floor(Date.now()/1000(second)))  // 1724567740 (time in second)

   let newDate = new Date()
   console.log(newDate);                  //  2024-08-25T06:37:56.966Z
   console.log(newDate.getMonth())        //  7

   newDate.toLocaleString('default',{weekday: "long"})
```
