## iframe 父子页面相互获取对方dom元素
##### 父页面获取子页面
```
document.getElementById('iframeId').contentWindow.document.getElementById('objId');
```
```
$($('#iframeId')[0].contentWindow).find('#objId');
```
##### 子页面获取父页面
```
window.parent.document.getElementById('parDiv')
```
```
$(window.parent.document).find('#parDiv')
```