## 去空格 trim
##### trim
######去空格
```
String.prototype.trim=function(){ 
	return this.replace(/(^\s*)|(\s*$)/g, ""); 
}
```
######去除左边空格*
```
String.prototype.ltrim=function(){ 
	return this.replace(/(^\s*)/g,""); 
}
```
######去除右边边空格*
```
String.prototype.rtrim=function(){ 
	return this.replace(/(\s*$)/g,""); 
}
```
##### 匹配空行的正则表达式：
```
\n[\s| ]*\r
```