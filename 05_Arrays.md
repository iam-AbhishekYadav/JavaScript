## # Arrays

- Array is a data stucture in which we storing a collection of multiple items under a single variable name.
- JS Arrays are resizable and can contain a mix of different data types.
- It is Non - Primitive data type.
- It works on Heap Memory.
- Array store data on 0 base indexing.

**Declaring of Arrays** &nbsp; --> `2 Ways to declare Arrays in JS.`

--> 1st Way to declare Array

``` js
const myArray = ["Abhi" , 1 , null , true , undefined] ;
console.log(myArray);                                        // Output : [ 'Abhi', 1, null, true, undefined ]

console.log(myArray[3]);                                    // Output : true  (Access any element on the bases of thir index)
```

--> 2nd Way to declare Array through constroctor (object)

``` js
const mynewArray = new Array("Abhi" , 1 , null , true , undefined) ;
console.log(mynewArray);                                   // Output : [ 'Abhi', 1, null, true, undefined ]
```

### Properties and Methods of Array

**(i) `No. of element present in Array`**

``` js
const myArray = ["Abhi" , 1 , null , true , undefined] ;
console.log(myArray.length);                                   // Output : 5
```

**(ii) `Adding and Removing of Elements in Array`**

- It is mutation (Changable) method

**(a)** `Adding and Removing of Elements in Last`

``` js
const myArray = ["Abhi" , "Sagar" , "Raj"];
console.log(myArray);                                   // Output : [ 'Abhi', 'Sagar', 'Raj' ]

myArray.push("Siddharth");
console.log(myArray);                                   // Output : [ 'Abhi', 'Sagar', 'Raj', 'Siddharth' ]

myArray.pop();
console.log(myArray)                                    // Output : [ 'Abhi', 'Sagar', 'Raj' ]
```
**(b)** `Adding and Removing of Elements in Start`

``` js
const myArray = ["Abhi" , "Sagar" , "Raj"];
console.log(myArray);                              // Output : [ 'Abhi', 'Sagar', 'Raj' ]

myArray.unshift("Siddharth");                      // Adding
console.log(myArray);                              // Output : [ 'Siddharth', 'Abhi', 'Sagar', 'Raj' ]

myArray.shift();                                  // Removing
console.log(myArray);                             // Output : [ 'Abhi', 'Sagar', 'Raj' ]
```

**(iii) `Accessing Elements`**

- It is Immutation (Unchangeable) method

**(a)** `indexof( )` --> If present then it give index of that element. If not present give -1.  
**(b)** `lastIndexOf( )` --> If present then it give last index of that element. If not present give -1.  
**(c)** `include( )` --> It tell us presence and absence of element in T/F.  

``` js
const myArray = ["Abhi" , "Sagar" , "Raj"];
console.log(myArray);

let element = myArray.indexOf("Sagar");
console.log(element);                                 // Output : 1

let element1 = myArray1.lastIndexOf("Sagar");
console.log(element1);                                // Output : 3

let element2 = myArray2.includes("Sagar");
console.log(element2);                                // Output : true
```

**(iv) `Slice()`**

- It Cut elements on the bases of index.
- It is Immutable.
- sclice(start,end)

```js
let myArray = [1,2,3,4,5,6,7,8,9];
console.log(myArray);                      // Output : [1,2,3,4,5,6,7,8,9]

let sliceArray = myArray.slice(2,7)
console.log(sliceArray);                    // Output : [ 3, 4, 5, 6, 7 ]
```

**(v) `Manipulating elements`**

- It is Mutable.

**(a) `splice()`** --> Removes elements from array and, if necessary, inserts new elements in their place, returning the deleted elements.  

 ``` js
let myArray = [0,1,2,3,4,5,6,7,8,9];
console.log(myArray);                                          // Output : [0,1,2,3,4,5,6,7,8,9]

let spliceArray = myArray.splice(2,7,"Sagar","Raj");           
console.log(spliceArray);                                      // Output : [ 2, 3, 4, 5, 6, 7, 8 ]

console.log(myArray);                                          // Output : [ 0, 1, 'Sagar', 'Raj', 9 ]
```
**(b) `sort()`** --> {क्रम मे लगाना}  This method mutates the array and returns a reference to the same array. {Also work in Abcd}  
``` js
let myArray = [9, 8, 7, 6, 5, 4, 3, 2, 1];
console.log(myArray);                                          // Output : [9, 8, 7, 6, 5, 4, 3, 2, 1]

let sortArray = myArray.sort();           
console.log(sortArray);                                      // Output : [1,2,3,4,5,6,7,8,9]
```

**(c) `reverse()`** --> {उल्टे क्रम मे लगाना} Reverses the elements in an array in place. This method mutates the array and returns a reference to the same array.  

``` js
let myArray = [1,2,3,4,5,6,7,8,9];
console.log(myArray);                                          // Output : [1,2,3,4,5,6,7,8,9]

let reverseArray = myArray.reverse();           
console.log(reverseArray);                                      // Output : [9, 8, 7, 6, 5, 4, 3, 2, 1]
```

**(d) `fill(What , Start ,End)`** --> Changes all array elements from start to end index to a static value and returns the modified array.  

``` js
let myArray = [1,2,3,4,5,6,7,8,9]
console.log(myArray);                                          // Output : [1,2,3,4,5,6,7,8,9]

let fillArray = myArray.fill("Raj",4,7);           
console.log(fillArray);                                      // Output : [1,2,3,4,'Raj','Raj','Raj',8,9]
```

**(vi) `Conversion of Array into String`**

- It is Immutable.

``` js
let myArray = ["Abhi","Siddhu","Raj","Sagar","Alok","Addi"]
console.log(myArray);                                             // Output : ["Abhi","Siddhu","Raj","Sagar","Alok","Addi"]

let convertedArray = myArray.join(",");
console.log(convertedArray);                                     // Output : Abhi,Siddhu,Raj,Sagar,Alok,Addi

console.log(myArray);                                            // Output : ["Abhi","Siddhu","Raj","Sagar","Alok","Addi"]
```

### Array Advance Concepts

#### Merging of Two Arrays

--> 4 Ways/Methods to Merging two Arrays.

**(i) `push()`** 

- It adds new items to the end of an array.
- It changes the length of the array.
- It returns the new length.

``` js
const marvel_heros = ["thor", "Ironman", "spiderman"]
const dc_heros = ["superman", "flash", "batman"]

marvel_heros.push(dc_heros)

console.log(marvel_heros);                 // Output : [ 'thor', 'Ironman', 'spiderman', [ 'superman', 'flash', 'batman' ] ]
console.log(marvel_heros[3][1]);           // Output : flash
```

**(ii) `concat()`**

- It concatenates (joins) two or more arrays.
- It returns a new array, containing the joined arrays.
- It does not change the existing arrays.
- It is useful for combining arrays without modifying the originals.

``` js
const marvel_heros = ["thor", "Ironman", "spiderman"]
const dc_heros = ["superman", "flash", "batman"]

const allHeros = marvel_heros.concat(dc_heros)
console.log(allHeros);                   // Output :  [ 'thor', 'Ironman', 'spiderman', 'superman', 'flash', 'batman' ]
```

**(iii) `Spread Operator`**

- Spread Operator (...) allows us to quickly copy all or part of an existing array or object into another array or object.

``` js
const marvel_heros = ["thor", "Ironman", "spiderman"]
const dc_heros = ["superman", "flash", "batman"]

const all_new_heros = [...marvel_heros, ...dc_heros]
console.log(all_new_heros);            // Output :  [ 'thor', 'Ironman', 'spiderman', 'superman', 'flash', 'batman' ]
```

**(iv) `flat()`**

- The flat() method concatenates sub-array elements.

``` js
const another_array = [1, 2, 3, [4, 5, 6], 7, [6, 7, [4, 5]]]

const real_another_array = another_array.flat(Infinity)
console.log(real_another_array);             // Output :  [ 1, 2, 3, 4, 5, 6, 7, 6, 7, 4, 5 ]
```

### When data is required in array 

``` js
console.log(Array.isArray("Hitesh"))          // Output : false
console.log(Array.from("Hitesh"))             // Output : [ 'S', 'a', 'c', 'h', 'i', 'n' ]
console.log(Array.from({name: "hitesh"}))     // interesting // Output : [ ]
```
### Converting Multiple Variables into Array

``` js
let score1 = 100
let score2 = 200
let score3 = 300

console.log(Array.of(score1, score2, score3));    // Output : [ 100, 200, 300 ]
```
