# # Events in JS

- Events are actions or occurrences that happen in the browser.
- They can be triggered by various user interactions or by the browser itself.


## Event Types

- JavaScript supports a variety of event types. Common categories include:
  - **`Mouse Events`** : click, dblclick, mousemove, mouseover, mouseout
  - **`Keyboard Events`** : keydown, keypress, keyup
  - **`Form Events`** : submit, change, focus, blur
  - **`Window Events`** : load, resize, scroll


## Common JavaScript Events

- **`onclick`** : Triggered when an element is clicked.
- **`onmouseover`** : Fired when the mouse pointer moves over an element.
- **`onmouseout`** : Occurs when the mouse pointer leaves an element.
- **`onkeydown`** : Fired when a key is pressed down.
- **`onkeyup`** : Fired when a key is released.
- **`onchange`** : Triggered when the value of an input element changes.
- **`onload`** : Occurs when a page has finished loading.
- **`onsubmit`** : Fired when a form is submitted.
- **`onfocus`** : Occurs when an element gets focus.
- **`onblur`** : Fired when an element loses focus.

## Event Handling Methods/Approaches

#### 1. Inline HTML Handlers

``` js
   <li><img id="fox" width="200px" height="150px" src="" onclick="alert("fox")"  alt=""></li>

   // it is not feseable approach in large scale application to get problem 
```

#### 2. DOM Property Handlers

``` js
document.querySelector("#owl").onclick = ()=>{
        alert("Owl clicked");
        console.log("Owl was clicked");
    }

    // Give very less information,features
```

#### 3. addEventListener() (Preferred)

```js
document.querySelector("#owl").addEventListener ('click', function (e) {
        alert("Owl clicked")
        console.log(e);  
    });

// attachEvent()
// jQuery - on

// <------ PointerEvent ------>

// type, timestamp, defaultPrevented
// target, toElement, srcElement, currentTarget,
// clientX, clientY, screenX, screenY
// altkey, ctrlkey, shiftkey, keyCode
```

## Event Propagation

``` js
   addEventListener("click",(e)=>{
            console.log(e)
   },false)                             // Default value ---> False
```

- JavaScript events propagate in two phases/context :
  - **`Event Bubbling`** : Inside to Outside propagations (False parameter --> Default)
  - **`Event Capturing `** : Outside to Inside propagations (True parameter)

``` js
document.getElementById("images").addEventListener ('click', function (e) {
        console.log("Clicked inside UI");
    }, false);

document.getElementById("owl").addEventListener ('click', function (e) {
        console.log("Owl clicked");
    }, false);

// <------ Outputs ------>

// False Parameter
// Owl clicked
// Clicked inside UI

// True Parameter
// Clicked inside UI
// Owl clicked
```

- **`stopPropagation()`** : Stops/Halts further propagation or Bubbling.

``` js
document.getElementById("owl").addEventListener ('click', function (e) {
        console.log("Owl clicked");
        e.stopPropagation();
    }, false);

// <------ Outputs ------>
// Owl clicked
```


- **`preventDefault()`** :
  - Certain elements have default actions (e.g., links navigating to URLs).
  - Use preventDefault() to override them.
  - Don't go to the URL

``` js
document.getElementById("google").addEventListener('click', function (e) {
        e.preventDefault();
        e.stopPropagation();
        console.log("Google clicked");
    }, false);

// <------ Outputs ------>
// Google clicked
```


# # JS Async 


<img width="800" height="600" alt="Screenshot 2025-10-12 134038" src="https://github.com/user-attachments/assets/f5c8e43b-2fd1-48a4-8005-c25c9104cd67" />

<img width="800" height="400" alt="Screenshot 2025-10-12 134838" src="https://github.com/user-attachments/assets/9206fb3a-6750-4e58-b6ae-62cc4994a2e0" />

<img width="800" height="700" alt="Screenshot 2025-10-12 135040-Sachin" src="https://github.com/user-attachments/assets/c3186346-5ec4-408a-9012-0b547c62920d" />

# # Time-Out or Time-IntervalFunctions

## 1. setTimeout() 

- It is used to add delay or scheduling the execution of a specific function after a certain period.
- It's a key feature of both browser environments and Node.js, enabling asynchronous behavior in code execution.
- **`Syntax`** : setTimeout(function, delay, arg1, arg2, ...);

### Example-1 :

``` js
const sayAbhi = function () {
        console.log("Abhishek Yadav");             // Output : Print "Abhishek Yadav" after 2s delay
    }

    setTimeout(sayAbhi, 2000);
```

### Example-2 : 

``` html js
<body>
    <h1>Sachin Yadav</h1>
    <button id="stop">Stop</button>
</body>

<script>
    const sayAbhi = function(){
        console.log("Abhishek");
    }

    const changeText = function(){
        document.querySelector('h1').innerHTML = "Abhishek Yadav"                // Output : Change h1 by "Abhishek Yadav" after 2s
    }

    setTimeout(changeText, 2000);

</script>
```

## 2. clearTimeout()

- It is used to cancel a scheduled timeout before it gets executed.

### Example-1 :

Onclicking button "Stop" setTimeout() is canceled

``` js
<body>
    <h1>Sachin Yadav</h1>
    <button id="stop">Stop</button>
</body>

<script>
    const sayAbhi = function(){
        console.log("Abhishek");
    }

    const changeText = function(){
        document.querySelector('h1').innerHTML = "Abhishek Yadav"
    }

    const changeMe = setTimeout(changeText, 2000)

    document.querySelector('#stop').addEventListener('click', function(){
        clearTimeout(changeMe)
        console.log("STOPPED")
    });

</script>
```

## 3. setInterval() 

- It is for executing a function repeatedly at specified intervals until explicitly cleared.
- This method is useful for tasks that need periodic execution, like updating animations or refreshing data.
- **`Syntax`** : setInterval(function, delay);


### Example :

Print Sachin" in console in every 1s.

``` js
<body>
    <h1>Sachin Yadav</h1>
    <button id="start">Start</button>
    <button id="stop">Stop</button>
</body>

<script>
    const sayDate = function(str){
        console.log(str, Date.now());
    }

    const intervalId = setInterval(sayDate, 1000, "Sachin");
    
</script>
```

## 4. clearInterval()

- To stop the execution of the setInterval().

### Example :
``` js
<body>
    <h1>Sachin Yadav</h1>
    <button id="start">Start</button>
    <button id="stop">Stop</button>
</body>

<script>
    const sayDate = function(str){
        console.log(str, Date.now());
    }

    const intervalId = setInterval(sayDate, 1000, "hi");

    clearInterval(intervalId);

</script>
```













