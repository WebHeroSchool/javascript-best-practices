Javadcript Best Practices
---
����� ��������� ������ ��� ��������� ��������, ��������� javascript ����



### 1). ������ ��������� ��������� ����������.

��� ���������� , ������������ � ������� ������ ���� ��������� ��� ��������� ����������.

��������� ���������� ������ ���� ��������� � �������� ������ var, let ��� const.
� ��������� ������ ��� ������ ����������� �����������.

``` js
//global
value;

//local
var block = [];
let element = "";
const button = idElem;
```

������� ����� �� ��������� ������������� ����������.



### 2). ���������� ���������� � ������

���������� ����������� � ������ ���� ��� �������.

��� ���� ����������� ������� ����� ������ ����������, ������� ����������� ���������� ���������� ���������� �
������ ��� ����.

``` js
var firstName = "",
    lastName = "",
    price = 0,
    discount = 0,
    fullPrice = 0,
    myArray = [],
    myObject = {};

function sayHi ( name ) {
  alert( name + ", hi!" );
}
```



### 3). ���������������� ����������.

� ������� ���� ��� ���������� ���������������� ��� ����������, ��� ��������� ����� ���������� ��� ������������ ������ � �������� ��������� ������������� �������������� ��������.



### 4). ��������� �����, ������ ��� ������ ��������, ��� ��������.

������ ������������� �����, ������ ��� ������� �������� ��� �����������, �� � �������� �������.
��� ��������� ��������� �������� ���������� � �� ������� ���������� �������� �������.

``` js
var x = "John";             
var y = new String("John");
(x === y) // false, ��� ��� � - string, y - object.
```



### 5). �� ��������� ������������� ����� new.

+ ����������� {}������new Object()
+ ����������� ""������new String()
+ ����������� 0������new Number()
+ ����������� false������new Boolean()
+ ����������� []������new Array()
+ ����������� /()/������new RegExp()
+ ����������� function (){}������new Function()

``` js
var x1 = {};           // new object
var x2 = "";           // new primitive string
var x3 = 0;            // new primitive number
var x4 = false;        // new primitive boolean
var x5 = [];           // new array object
var x6 = /()/;         // new regexp object
var x7 = function(){}; // new function object
```



### 6). ��������� ������� ��������� === ������ ==

  - ==�������� ��������� ������ ����������� (� ������������ �����) ����� ����������.
  - ===�������� ���� ��������� �������� � �����:

``` js
0 == "";        // true
1 == "1";       // true
1 == true;      // true

0 === "";       // false
1 === "1";      // false
1 === true;     // false
```


### 7). ���������� �������� �� ���������.

������� �������� ����������� �������� �� ���������, ��� ��� �������������� �������� undefined ����� �������� � ������� ����.

��������, ���� ������� ���������� ��� ���������:

``` js
function myFunction(x, y) {
  if (y === undefined) {
    y = 0; // ��� ���������� ������������� �, ��� �������� ����� ������������ 
  }
}
```


### 8). ������������� default �������� � ����������� Sweetch.

``` js
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
  default:
    day = "Unknown";
}
```


### 9). ������ ���������� ���������� ������� (IIFE) �� ����� (Blocks)

������ ���������� ���������� ������� ���������� ��� ���������� �������� � �� �������� ���������. � ES6 ����� ��������� ������� ������� ���������.

``` js
(function () {
    var food = 'Meow Mix';
}());

console.log(food); // Reference Error
```
������ Blocks
``` js
{
    let food = 'Meow Mix';
};

console.log(food); // Reference Error
```

����� ����������� ����� ����� �������� ���, � ������� ��������� ������������ ������, ������ �������� ���������� `food`.



### 10). ��������� �������� (ES6)

��������� �������� ������������ ������������, ��� ������ ������ ������������ ����� � ��������:

```js
var name = 'Tiger';
var age = 13;

console.log('My cat is named ' + name + ' and is ' + age + ' years old.');
```
������� �����:
``` js
const name = 'Tiger';
const age = 13;

console.log(`My cat is named ${name} and is ${age} years old.`);
```

������ �����, ��������� �������� ��������� ������� �����:
``` js
let text = ( `cat
dog
nickelodeon`
);
```


���� ������ ����� ����������� � �����������.

(https://tproger.ru/translations/es6-cheatsheet-1/)
(https://www.w3schools.com/js/js_best_practices.asp)



