## 多选按钮
<div class="codes">
<div class="form-checkbox">
  <p>
    <input name="group1" type="checkbox" id="test1" />
    <label for="test1">Red</label>
  </p>
  <p>
    <input name="group1" type="checkbox" id="test2" />
    <label for="test2">Yellow</label>
  </p>
  <p>
    <input name="group1" checked="checked" type="checkbox" id="test3"  />
    <label for="test3">Green</label>
  </p>
  <p>
    <input name="group1" type="checkbox" id="test4" disabled="disabled" />
    <label for="test4">Brown</label>
  </p>
</div>
<style type="text/css">
    .form-checkbox p{margin-bottom: 10px;text-align: left;}
    [type="checkbox"]:not(:checked), [type="checkbox"]:checked {position: absolute;left: -9999px;}
    input[type="checkbox"], input[type="checkbox"]{box-sizing: border-box;padding: 0;}
    [type="checkbox"]:not(:checked) + label, [type="checkbox"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: 25px;line-height:25px;font-size: 15px;transition: .28s ease;    color: #9e9e9e;
    }
    [type="checkbox"] + label:before, [type="checkbox"] + label:after {
        content: '';left: 0;position: absolute;transition: border .25s, background-color .25s, width .2s .1s, height .2s .1s, top .2s .1s, left .2s .1s;z-index: 1
    }
    [type="checkbox"]:not(:checked) + label:before {width: 0;height: 0;border: 3px solid transparent;left: 6px;top: 10px;transform-origin: 100% 100%;transform: rotateZ(50deg);}
    [type="checkbox"]:not(:checked) + label:after {height: 20px;width: 20px;background-color: transparent;border: 2px solid #5a5a5a;top: 0px;z-index: 0;}
    [type="checkbox"]:checked + label:before {top: 0;left: -4px;width: 8px;height: 15px;border-top: 2px solid transparent;border-left: 2px solid transparent;border-right: 2px solid #fff;border-bottom: 2px solid #fff;transform-origin: 100% 100%;transform: rotateZ(50deg);}
    [type="checkbox"]:checked + label:after { top: 0px;width: 20px;height: 20px;border: 2px solid #26a69a;background-color: #26a69a;z-index: 0;}
    [type="checkbox"]:checked + label{color:#26a69a;}
    [type="checkbox"]:disabled:not(:checked) + label:before {background-color: transparent;border: 2px solid transparent;}
    [type="checkbox"]:disabled:not(:checked) + label:after {border-color: transparent;background-color: #BDBDBD;}
    [type="checkbox"]:disabled:checked + label:before {background-color: transparent;}
    [type="checkbox"]:disabled:checked + label:after {background-color: #BDBDBD;border-color: #BDBDBD;}
</style>
</div>
html
```
<div class="form-checkbox">
  <p>
    <input name="group1" type="checkbox" id="test1" />
    <label for="test1">Red</label>
  </p>
  <p>
    <input name="group1" type="checkbox" id="test2" />
    <label for="test2">Yellow</label>
  </p>
  <p>
    <input name="group1" checked="checked" type="checkbox" id="test3"  />
    <label for="test3">Green</label>
  </p>
  <p>
    <input name="group1" type="checkbox" id="test4" disabled="disabled" />
    <label for="test4">Brown</label>
  </p>
</div>
```
style
```
<style type="text/css">
    .form-checkbox p{margin-bottom: 10px;text-align: left;}
    [type="checkbox"]:not(:checked), [type="checkbox"]:checked {position: absolute;left: -9999px;}
    input[type="checkbox"], input[type="checkbox"]{box-sizing: border-box;padding: 0;}
    [type="checkbox"]:not(:checked) + label, [type="checkbox"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: 25px;line-height:25px;font-size: 15px;transition: .28s ease;    color: #9e9e9e;
    }
    [type="checkbox"] + label:before, [type="checkbox"] + label:after {
        content: '';left: 0;position: absolute;transition: border .25s, background-color .25s, width .2s .1s, height .2s .1s, top .2s .1s, left .2s .1s;z-index: 1
    }
    [type="checkbox"]:not(:checked) + label:before {width: 0;height: 0;border: 3px solid transparent;left: 6px;top: 10px;transform-origin: 100% 100%;transform: rotateZ(50deg);}
    [type="checkbox"]:not(:checked) + label:after {height: 20px;width: 20px;background-color: transparent;border: 2px solid #5a5a5a;top: 0px;z-index: 0;}
    [type="checkbox"]:checked + label:before {top: 0;left: -4px;width: 8px;height: 15px;border-top: 2px solid transparent;border-left: 2px solid transparent;border-right: 2px solid #fff;border-bottom: 2px solid #fff;transform-origin: 100% 100%;transform: rotateZ(50deg);}
    [type="checkbox"]:checked + label:after { top: 0px;width: 20px;height: 20px;border: 2px solid #26a69a;background-color: #26a69a;z-index: 0;}
    [type="checkbox"]:checked + label{color:#26a69a;}
    [type="checkbox"]:disabled:not(:checked) + label:before {background-color: transparent;border: 2px solid transparent;}
    [type="checkbox"]:disabled:not(:checked) + label:after {border-color: transparent;background-color: #BDBDBD;}
    [type="checkbox"]:disabled:checked + label:before {background-color: transparent;}
    [type="checkbox"]:disabled:checked + label:after {background-color: #BDBDBD;border-color: #BDBDBD;}
</style>
```
less
```
<style type="text/less">
    .form-checkbox{
      p{margin-bottom: 10px;text-align: left;}
      @wordColor:#9e9e9e;
      @height:25px;
      @fontSize:15px;
      [type="checkbox"]:not(:checked), [type="checkbox"]:checked {position: absolute;left: -9999px;visibility: hidden;}
      input[type="checkbox"], input[type="checkbox"]{box-sizing: border-box;padding: 0;}
      [type="checkbox"]:not(:checked) + label, [type="checkbox"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: 25px;line-height:25px;font-size: 15px;transition: .28s ease;    color: #9e9e9e;
      }
      [type="checkbox"] + label:before, [type="checkbox"] + label:after {
        content: '';left: 0;position: absolute;transition: border .25s, background-color .25s, width .2s .1s, height .2s .1s, top .2s .1s, left .2s .1s;z-index: 1
      }
      @notCheckedColor:#5a5a5a;
      @checkedColor:#26a69a;
      [type="checkbox"]:not(:checked) + label{
        &:before {width: 0;height: 0;border: 3px solid transparent;left: 6px;top: 10px;transform-origin: 100% 100%;transform: rotateZ(50deg);}
        &:after {height: 20px;width: 20px;background-color: transparent;border: 2px solid #5a5a5a;top: 0px;z-index: 0;}
      }
      [type="checkbox"]:checked + label{
        color:#26a69a;
        &:before {top: 0;left: -4px;width: 8px;height: 15px;border-top: 2px solid transparent;border-left: 2px solid transparent;border-right: 2px solid #fff;border-bottom: 2px solid #fff;transform-origin: 100% 100%;transform: rotateZ(50deg);}
        &:after {top: 0px;width: 20px;height: 20px;border: 2px solid #26a69a;background-color: #26a69a;z-index: 0;}
      }
      [type="checkbox"]:disabled{
        &:not(:checked) + label {
          &:before {background-color: transparent;border: 2px solid transparent;}
          &:after {border-color: transparent;background-color: #BDBDBD;}
        }
        &:checked + label {
          &:before {background-color: transparent;}
          &:after {background-color: #BDBDBD;border-color: #BDBDBD;}
        }
      }
    }
</style>
```
