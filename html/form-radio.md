## 单选按钮
<div class="codes">
<div class="form-radio">
  <p>
    <input name="group1" type="radio" id="test1" />
    <label for="test1">Red</label>
  </p>
  <p>
    <input name="group1" type="radio" id="test2" />
    <label for="test2">Yellow</label>
  </p>
  <p>
    <input name="group1" checked="checked" type="radio" id="test3"  />
    <label for="test3">Green</label>
  </p>
  <p>
    <input name="group1" type="radio" id="test4" disabled="disabled" />
    <label for="test4">Brown</label>
  </p>
</div>
<style type="text/css">
    .form-radio p{margin-bottom: 10px;text-align: left;}
    [type="radio"]:not(:checked), [type="radio"]:checked {position: absolute;left: -9999px;visibility: hidden;}
    input[type="checkbox"], input[type="radio"]{box-sizing: border-box;padding: 0;}
    [type="radio"]:not(:checked) + label, [type="radio"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: 25px;line-height:25px;font-size: 15px;transition: .28s ease;    color: #9e9e9e;
    }
    [type="radio"] + label:before, [type="radio"] + label:after {
        content: '';position: absolute;left: 0;top: 0;margin: 4px;width: 16px;height: 16px;z-index: 0;-webkit-transition: .28s ease;transition: .28s ease;
    }
    [type="radio"]:not(:checked) + label:before {border-radius: 50%;border: 2px solid #5a5a5a;}
    [type="radio"]:not(:checked) + label:after {border-radius: 50%;border: 2px solid #5a5a5a;z-index: -1;transform: scale(0);}
    [type="radio"]:checked + label:before {border-radius: 50%;border: 2px solid #26a69a;}
    [type="radio"]:checked + label:after {border-radius: 50%;border: 2px solid #26a69a;background-color: #26a69a;z-index: 0;transform: scale(.5);}
    [type="radio"]:checked + label{color:#26a69a;}
    [type="radio"]:disabled:not(:checked) + label:before, [type="radio"]:disabled:checked + label:before {
        background-color: transparent;border-color: rgba(0, 0, 0, 0.26);
    }
    [type="radio"]:disabled + label {color: rgba(0, 0, 0, 0.26);}
    [type="radio"]:disabled:not(:checked) + label:hover:before {border-color: rgba(0, 0, 0, 0.26);}
</style>
</div>
##### html
```
<div class="form-radio">
  <p>
    <input name="group1" type="radio" id="test1" />
    <label for="test1">Red</label>
  </p>
  <p>
    <input name="group1" type="radio" id="test2" />
    <label for="test2">Yellow</label>
  </p>
  <p>
    <input name="group1" checked="checked" type="radio" id="test3"  />
    <label for="test3">Green</label>
  </p>
  <p>
    <input name="group1" type="radio" id="test4" disabled="disabled" />
    <label for="test4">Brown</label>
  </p>
</div>
```
##### style
```
<style type="text/css">
    .form-radio p{margin-bottom: 10px;text-align: left;}
    [type="radio"]:not(:checked), [type="radio"]:checked {position: absolute;left: -9999px;visibility: hidden;}
    input[type="checkbox"], input[type="radio"]{box-sizing: border-box;padding: 0;}
    [type="radio"]:not(:checked) + label, [type="radio"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: 25px;line-height:25px;font-size: 15px;transition: .28s ease;    color: #9e9e9e;
    }
    [type="radio"] + label:before, [type="radio"] + label:after {
        content: '';position: absolute;left: 0;top: 0;margin: 4px;width: 16px;height: 16px;z-index: 0;-webkit-transition: .28s ease;transition: .28s ease;
    }
    [type="radio"]:not(:checked) + label:before {border-radius: 50%;border: 2px solid #5a5a5a;}
    [type="radio"]:not(:checked) + label:after {border-radius: 50%;border: 2px solid #5a5a5a;z-index: -1;transform: scale(0);}
    [type="radio"]:checked + label:before {border-radius: 50%;border: 2px solid #26a69a;}
    [type="radio"]:checked + label:after {border-radius: 50%;border: 2px solid #26a69a;background-color: #26a69a;z-index: 0;transform: scale(.5);}
    [type="radio"]:checked + label{color:#26a69a;}
    [type="radio"]:disabled:not(:checked) + label:before, [type="radio"]:disabled:checked + label:before {
        background-color: transparent;border-color: rgba(0, 0, 0, 0.26);
    }
    [type="radio"]:disabled + label {color: rgba(0, 0, 0, 0.26);}
    [type="radio"]:disabled:not(:checked) + label:hover:before {border-color: rgba(0, 0, 0, 0.26);}
</style>
```
##### less
```
<style type="text/less">
    .form-radio{
      p{margin-bottom: 10px;text-align: left;}
      @wordColor:#9e9e9e;
      @height:25px;
      @fontSize:15px;
      [type="radio"]:not(:checked), [type="radio"]:checked {position: absolute;left: -9999px;visibility: hidden;}
      input[type="checkbox"], input[type="radio"]{box-sizing: border-box;padding: 0;}
      [type="radio"]:not(:checked) + label, [type="radio"]:checked + label{
        position: relative;padding-left: 35px;cursor: pointer;display: inline-block;height: @height;line-height:@height;font-size: @fontSize;transition: .28s ease;color: @wordColor;
      }
      [type="radio"] + label:before, [type="radio"] + label:after {
        content: '';position: absolute;left: 0;top: 0;margin: 4px;width: 16px;height: 16px;z-index: 0;-webkit-transition: .28s ease;transition: .28s ease;
      }
      @notCheckedColor:#5a5a5a;
      @checkedColor:#26a69a;
      [type="radio"]:not(:checked) + label{
        &:before {border-radius: 50%;border: 2px solid @notCheckedColor;}
        &:after {border-radius: 50%;border: 2px solid @notCheckedColor;z-index: -1;transform: scale(0);}
      }
      [type="radio"]:checked + label{
        color:#26a69a;
        &:before {border-radius: 50%;border: 2px solid @checkedColor;}
        &:after {border-radius: 50%;border: 2px solid @checkedColor;background-color: @checkedColor;z-index: 0;transform: scale(.5);}
      }
      [type="radio"]:disabled{
        &:not(:checked) + label:before, &:checked + label:before {
          background-color: transparent;border-color: rgba(0, 0, 0, 0.26);
        }
        & + label {color: rgba(0, 0, 0, 0.26);}
        &:not(:checked) + label:hover:before {border-color: rgba(0, 0, 0, 0.26);}
      }
    }
</style>
```
