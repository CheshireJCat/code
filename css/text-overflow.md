## 文本截断并末尾出现省略号
##### 单行文本
```
white-space: nowrap;overflow: hidden;text-overflow: ellipsis;
```
##### 多行文本：
```
display: -webkit-box;overflow: hidden;text-overflow: ellipsis;-webkit-line-clamp: 2;-webkit-box-orient: vertical;
```  

> 不要将多行省略的属性写在 a 上（或其父标签）。而在 a 内再嵌套一个标签，对其使用多行省略。如:  

```
<a href="#"><div>Lorem ipsum dolor sit amet</div></a>
```
