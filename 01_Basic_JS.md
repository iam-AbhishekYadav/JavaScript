## # What is JavaScript ?

JavaScript is an object oreiented , general purpose and high level programming language used in wesite's frontend , banckend and software application.

## # Variables
 The name of memory location that we use to store data.
 
![Variable in JS 2](https://github.com/user-attachments/assets/c2a0c0a1-e976-4583-ac15-f6ed5243f71d)

### Types of Variables

There are 3 types of Variables.

- **let**
- **const** ==> (ERROR assignment to const variable (Can't change variables once value is assigned))
- **var**
>  [!WARNING]
> Prefer not to use var because of issue in block scope and functional scope

## # Data Type

It specifies the type of data that the variable can store.

### Types of Data Type

Data types are  divided into two categories.

### 1. Premitive Data Type 

**Call by value** ( When called, a copy is returned.)

- Number --> range (2<sup>53</sup>)
- Bigint --> `const num = 123456789n`
- Boolean --> true/false
- String --> " "
- Null --> standalone value &nbsp; &nbsp;`**typeof -->object**`
- Undefined --> A variable that has not been assigned a value is undefined.&nbsp; &nbsp; ` **typeof --> undefined**`
- Symbol --> unique

### 2. Non - Premitive Data Type 

**Reference** (call by reference ( When called, an address is returned.))

- Object &nbsp; &nbsp; &nbsp; `**typeof --> object`
- Array &nbsp; &nbsp; &nbsp; `**typeof --> object`
- Function &nbsp; &nbsp; `**typeof --> function`

## # Conversion

**Type Conversion** = To convert one type of data into another type of data.

``` js
     let score =                         "77" || "77abc" || null || undefined
     let valueINNumber = Number(score)   ----    --------   ----    ---------
     console.log(valueINNumber)          77  ||   NaN   ||  0   ||   NaN

     let isLoggedIn =                               1    ||   0   || "sidd" || ""                        
     let booleanIsLoggedIn = Boolean(isLoggedIn)    ---     -----    ------    ---
     console.log(booleanIsLoggedIn)                 true || false ||  true  || false
```

## # Arithmetic Operators in JS

To perform mathematical calculation between variables and values.

**Arithmetic Operators -->** &nbsp; &nbsp;   + , - , / , * , ** , %

** --> Exponential Operator &nbsp; &nbsp; { 2**5 = 2<sup>5</sup> }  
% --> Modulus Operator  &nbsp; &nbsp;{ To find the remainder }

![Operator2 (1)](https://github.com/user-attachments/assets/643b614f-74cf-4908-a370-97c6d4f7a5a6)

> [!NOTE]
> No operator is assumed to be present.  
> Example -->  
> a = xy ----> Invalid  
> a = x * y ----> Valid

``` js
console.log(+true);     // 1
console.log(true+);     // error
console.log(+"");       // 0
```

## # Comparison Operators

To determine equality or difference between variables or values.

**Arithmetic Operators -->** &nbsp; &nbsp; < , > , <= , >= , == , !=

``` js
console.log("2" > 1);          //true
console.log("02" > 1);         //true
console.log(null > 0);         //false
console.log(null == 0);        //false
console.log(null >= 0);        //true
console.log(undefined > 0);    //false
console.log(undefined == 0);   //false
console.log(undefined >= 0);   //false
```

> [!NOTE]
> **===** --> Strict Check
