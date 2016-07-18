## 原生sj 绑定事件/on/trigger
##### 绑定事件
```
function addEvent(obj, evt, fn) {
    if (!oTarget) {
        return;
    }
    if (obj.addEventListener) {
        obj.addEventListener(evt, fn, false);
    } else if (obj.attachEvent) {
        obj.attachEvent('on' + evt, fn);
    } else {
        oTarget["on" + sEvtType] = fn;
    }
}

```
##### 删除事件
```
function delEvt(obj, evt, fn) {
    if (!obj) {
        return;
    }
    if (obj.addEventListener) {
        obj.addEventListener(evt, fn, false);
    } else if (oTarget.attachEvent) {
        obj.attachEvent("on" + evt, fn);
    } else {
        obj["on" + evt] = fn;
    }
}

```
##### 添加on方法
```
Element.prototype.on = Element.prototype.addEventListener;
NodeList.prototype.on = function(event, fn) {、
    []['forEach'].call(this, function(el) {
        el.on(event, fn);
    });
    return this;
};

```
##### 为元素添加trigger方法
```
Element.prototype.trigger = function(type, data) {
    var event = document.createEvent('HTMLEvents');
    event.initEvent(type, true, true);
    event.data = data || {};
    event.eventName = type;
    event.target = this;
    this.dispatchEvent(event);
    return this;
};
NodeList.prototype.trigger = function(event) {
    []['forEach'].call(this, function(el) {
        el['trigger'](event);
    });
    return this;
};

```