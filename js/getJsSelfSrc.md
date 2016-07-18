## JS获取自身所在文件路径
由于判断路径的js代码一般都直接放在js文件中而不是函数中，  
所以当加载该js文件时会立即执行其中的语句，  
而执行此语句时所获取到的js文件数目正好是js.length-1，  
因为页面后面的js文件还没有加载，  
所以该处的js文件获取的数目并不是页面所有的js文件的数目。  
这样一来，获取路径就无需再遍历了，而且文件判断也无需文件名，判断更加准确(js.length-1永远都是其文件本身)。  
```
var tjs=document.scripts[document.scripts.length-1];
var path = tjs.src;
var name = tjs.src.substring(tjs.src.lastIndexOf("/")+1);
alert('文件路径：'+path);
alert('文件名：'+name);
```