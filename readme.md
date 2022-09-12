## This is a file explaining 3 topics in javaScript
---
- tenary operator
- switch statement
- scope
---
##### Tenary operators
This is used to simplify conditions and make it simpler rather than writing a whole lot of code.
###### Example of a tenary code
(condition)? *expression1* : *expression*;

``` 
function isUserValid(bool) {
  return bool;
 }

 var answer = isUserValid(true)? "you are logged in" : "Access denied";

undefined
isUserValid(false)
false

answer

'you are logged in'
 var answer = isUserValid(false)? "you are logged in" : "Access denied"; `
undefined

answer
Access denied
```
This was run in the console

#### switch statement

switch statement is used to execute a statement from multiple choices and stops when the condition is met.
Thats why its necessary to use the break; keyword 
###### The syntax for the switch statement -
 ```
 switch (direction) {
  case "right": whatHappens = "you just encountered a monster";
    
    break;

    case "left":whatHappens = "going to the pool";
    
    break;

    case "back":whatHappens = "heading home";
  
    break;

    case "from":whatHappens = "going the mountain";
    
    break;

  default:
    whatHappens = "please enter a valid direction"
    break;
}
```
>>>Use it in a function and run it in th console 
```
// switch
function moveGame(direction) {
var whatHappens;
switch (direction) {
  case "right": whatHappens = "you just encountered a monster";
    
    break;

    case "left":whatHappens = "going to the pool";
    
    break;

    case "back":whatHappens = "heading home";
  
    break;

    case "front":whatHappens = "going the mountain";
    
    break;

  default:
    whatHappens = "please enter a valid direction"
    break;
}
return whatHappens;
}
undefined
moveGame("front")
'going the mountain'
```

`Run the above line by line`

## Scope
Scope is a variable acces
it refers to the context of which determines the accessibility of the variables.
in this javaScript context, the window is the root scope.
There are two types of scope the global scope and the local scope.
Global scope are the ones declared outside of the block while local scope are those declared inside the block.

`using this examples below Run them one by one to understand the concept of scope`

```
// #1
function q1() {
    var a =5;
    if (a > 1) {
        a = 3;
    }
    alert(a); // the answer will be 3
}

// #2
first you have to run q2() in your console to add the new value then run q22()
var a = 0;
function q2() {
    a = 5;
}

function q22() {
    alert(a);//5
  }

// #3 first you have to run q3() in your console to add the property a to the window. then run q32()
function q3() {
window.a = "hello";
}

function q32() {
    alert(a);//hello
  }

  // #4
  var a = 1;
  function q4() {
    var a = "test";
    alert(a);//test
  }

  // #5 with var keyword if statementdo not create a new scope.
  var a = 2;
if (true) {
    var a = 5;
    alert(a);
}

  alert(a);
  ```
