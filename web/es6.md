# ES6

## 箭头函数

ES6 允许使用“箭头”（=>）定义函数。

```javascript
var f = v => v;

// =

var f = function(v) {
  return v;
};
```

```javascript
var f = () => 5;

// =

var f = function () { return 5  };
```

```javascript
var sum = (num1, num2) => num1 + num2;

// =

var sum = function(num1, num2) {
  return num1 + num2;
};
```

```javascript

```

注意事项：
- 函数体内的 this 对象，就是定义时所在的对象，而不是使用时所在的对象。  
- 不可以当作构造函数，也就是说，不可以使用 new 命令，否则会抛出一个错误。  
- 不可以使用 arguments 对象，该对象在函数体内不存在。如果要用，可以用 rest 参数代替。  
- 不可以使用 yield 命令，因此箭头函数不能用作 Generator 函数。  

