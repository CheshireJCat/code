## 单击页面选择器以外的地方时选择器隐藏
```
$(document).bind('mousedown',function(event){
    if(!($(event.target).parents().andSelf().is('#bigpicker'))){
        $("#bigpicker").hide();
    }
});
```