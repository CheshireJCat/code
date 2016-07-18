## console的用法
##### console.log  
Console.log 是最简单输出信息到 console 窗口的方法，支持多个参数，该方法会把 这些参数组合在一起显示  

log 方法第一个参数支持类似 C 语言 printf 字符串替换模式，Log 支持下面几种替换模式  

* %s  代替字符串
* %d  代替整数
* %f  代替浮点值
* %o  代替 Object  
```
console.log("%d年%d月%d日"，2014,6,25);
=>2014年6月25日
```
##### console.debug，info，warn，error  
这 4 种方法与 log 方法使用一模一样，只是显示的图标和文字颜色不一样.  

console.info 用于输出提示性信息  
console.error用于输出错误信息  
console.warn用于输出警示信息  
console.debug用于输出调试信息  

##### console.assert  
assert 方法类似于单元测试中的断言，当 expression 表达式为 false 的时候，输出后面的信息
```
console.assert(2==1)
=> VM146:1 Assertion failed:(anonymous function) 

=> console.assert(1==1)
``` 

##### console.clear  
清空console中的所有信息（chrome不支持）  

##### console.firxml  
等同于log，将html元素的html代码打印出来  

##### console.trace  
可以查看当前函数的调用堆栈信息，即当前函数是如何调用的  
```
function doTask(){
    doSubTask(1000,10000);
}
 
function doSubTask(countX,countY){
    for(var i=0;i<countX;i++){
        for(var j=0;j<countY;j++){} 
    }
    console.trace();
}
doTask();


输出：
console.trace() 
doSubTask
doTask 
(anonymous function) 
_evaluateOn 
_evaluateAndWrap 
evaluate 
```

##### console.group  
将输出的信息进行分组方便阅读查看  
```
console.group('A');
console.log('a');
console.log('b');
console.log('c');
console.groupEnd();

=>
A
  a
  b
  c
```

##### console.time(name)/console.timeEnd(name)
创建计时器  
```
console.time('test')
var a = 0;
for(var i = 0;i<100;i++){
	a+=i;
}
console.log(a);
console.timeEnd('test')

=>
test: 计时器开始
4950
test: 1.77ms
```

##### console.table(data)
把data对象用表格的方式显示出来，仅支持firebug
```
var a = {a:1,b:2};console.table(a)
```
<table style="width:100px;margin:0 auto;border:1px solid #ddd">
	<thead>
		<tr>
			<th>索引</th>
			<th>值</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>a</td>
			<td>1</td>
		</tr>
		<tr>
			<td>b</td>
			<td>2</td>
		</tr>
	</tbody>
</table>

##### console.dir(object)
列出对象的所有方法,不同浏览器显示的内容不同,比如列出console对象的方法
```
console.dir(console);
```