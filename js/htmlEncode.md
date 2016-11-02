## HTML 字符转义
##### Encode  

```
function htmlEncode(str){  
          var s = "";
          if(str.length == 0) return "";
          s = str.replace(/&/g,"&amp;");
          s = s.replace(/</g,"&lt;");
          s = s.replace(/>/g,"&gt;");
          s = s.replace(/ /g,"&nbsp;");
          s = s.replace(/\'/g,"&#39;");
          s = s.replace(/\"/g,"&quot;");
          return s;  
}
```

##### Decode  

```
function htmlDecode(str){  
      var s = "";
      if(str.length == 0) return "";
      s = str.replace(/&amp;/g,"&");
      s = s.replace(/&lt;/g,"<");
      s = s.replace(/&gt;/g,">");
      s = s.replace(/&nbsp;/g," ");
      s = s.replace(/&#39;/g,"\'");
      s = s.replace(/&quot;/g,"\"");
      return s;  
}
```

##### 换行符转换  

```
str.replace(/\r?\n/g,"<br />")
```
##### 空格转换  

```
str.replace(/\s/g,"&nbsp;");
```

##### 连续空格合并成一个  

```
str.replace(/(\s|&nbsp;)+/g,' ');
```  

##### 去掉html标签  

```
str.replace(/<[^<>]+?>/g,'');
```


