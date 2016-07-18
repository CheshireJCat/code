## 尾递归优化  
> 来自 [阮一峰 ECMAScript 6入门 函数的拓展](http://es6.ruanyifeng.com/#docs/function)
```javascript
function tco(f) {
  var value;
  var active = false;
  var accumulated = [];

  return function accumulator() {
    accumulated.push(arguments);
    if (!active) {
      active = true;
      while (accumulated.length) {
        value = f.apply(this, accumulated.shift());
      }
      active = false;
      return value;
    }
  };
}

var sum = tco(function(x, y) {
  if (y > 0) {
    return sum(x + 1, y - 1)
  }
  else {
    return x
  }
});

sum(1, 100000)
// 100001
```
上面代码中，tco函数是尾递归优化的实现，它的奥妙就在于状态变量active。  
默认情况下，这个变量是不激活的。一旦进入尾递归优化的过程，这个变量就激活了。  
然后，每一轮递归sum返回的都是undefined，所以就避免了递归执行；  
而accumulated数组存放每一轮sum执行的参数，总是有值的，这就保证了accumulator函数内部的while循环总是会执行。  这样就很巧妙地将“递归”改成了“循环”，而后一轮的参数会取代前一轮的参数，保证了调用栈只有一层。  

### 尾调用
尾调用（Tail Call）是函数式编程的一个重要概念，本身非常简单，一句话就能说清楚，就是指某个函数的最后一步是调用另一个函数。  
```
function f(x){
  return g(x);
}
```
上面代码中，函数f的最后一步是调用函数g，这就叫尾调用。  
以下三种情况，都不属于尾调用。  
```
// 情况一
function f(x){
  let y = g(x);
  return y;
}

// 情况二
function f(x){
  return g(x) + 1;
}

// 情况三
function f(x){
  g(x);
}
```  
上面代码中，情况一是调用函数g之后，还有赋值操作，所以不属于尾调用，即使语义完全一样。情况二也属于调用后还有操作，即使写在一行内。情况三等同于下面的代码。 

尾调用之所以与其他调用不同，就在于它的特殊的调用位置。

我们知道，函数调用会在内存形成一个“调用记录”，又称“调用帧”（call frame），保存调用位置和内部变量等信息。如果在函数A的内部调用函数B，那么在A的调用帧上方，还会形成一个B的调用帧。等到B运行结束，将结果返回到A，B的调用帧才会消失。如果函数B内部还调用函数C，那就还有一个C的调用帧，以此类推。所有的调用帧，就形成一个“调用栈”（call stack）。

尾调用由于是函数的最后一步操作，所以不需要保留外层函数的调用帧，因为调用位置、内部变量等信息都不会再用到了，只要直接用内层函数的调用帧，取代外层函数的调用帧就可以了。  

### 尾递归  
函数调用自身，称为递归。如果尾调用自身，就称为尾递归。

递归非常耗费内存，因为需要同时保存成千上百个调用帧，很容易发生“栈溢出”错误（stack overflow）。但对于尾递归来说，由于只存在一个调用帧，所以永远不会发生“栈溢出”错误。  
有一个比较著名的例子，就是计算fibonacci 数列，也能充分说明尾递归优化的重要性  
```
function Fibonacci (n) {
  if ( n <= 1 ) {return 1};

  return Fibonacci(n - 1) + Fibonacci(n - 2);
}

Fibonacci(10); // 89
// Fibonacci(100)
// Fibonacci(500)
// 堆栈溢出了
```
如果我们使用尾递归优化过的fibonacci 递归算法  
```
function Fibonacci2 (n , ac1 = 1 , ac2 = 1) {
  if( n <= 1 ) {return ac1};

  return Fibonacci2 (n-1 , ac2 , ac1 + ac2);
}

Fibonacci2(100) // 354224848179262000000
Fibonacci2(1000) // 4.346655768693743e+208
Fibonacci2(10000) // Infinity
```
由此可见，“尾调用优化”对递归操作意义重大，所以一些函数式编程语言将其写入了语言规格。ES6也是如此，第一次明确规定，所有ECMAScript的实现，都必须部署“尾调用优化”。这就是说，在ES6中，只要使用尾递归，就不会发生栈溢出，相对节省内存。  