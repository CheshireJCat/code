## 按钮
### 普通按钮  

<div class="codes">
<div class="large" style="margin-top:10px;">
	<a href="" class="btn">BUTTON</a>
	<a href="" class="btn"><i class="fa fa-bars fa-2x"></i>BUTTON</a>
</div>
<style type="text/css">
	.btn{
		border:none;border-radius:2px;display:inline-block;*display:inline;*zoom:1;padding:0 20px;outline:0;vertical-align: middle;
		color:#fff;background-color: #26a69a;text-decoration: none;text-align: center;
		box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);transition: .5s;
	}
	.btn:hover{box-shadow:0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);cursor: pointer;}
	.btn i{padding-right: 12px;vertical-align:middle;}

	.large .btn{height: 54px;line-height:56px;margin-right: 20px;}
</style>
</div>  

##### html
```
<a href="" class="btn">BUTTON</a>

<a href="" class="btn"><i class="fa fa-bars fa-2x"></i>BUTTON</a>
```
##### style
```
<style type="text/css">
	.btn{
		border:none;border-radius:2px;display:inline-block;*display:inline;*zoom:1;padding:0 20px;outline:0;vertical-align: middle;
		color:#fff;background-color: #26a69a;text-decoration: none;text-align: center;
		box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);transition: .5s;
	}
	.btn:hover{background-color: #2bbbad;box-shadow:0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19)}
	.btn i{padding-right: 12px;vertical-align:middle;}

	.large .btn{height: 54px;line-height:56px;margin-right: 20px;}
</style>
```
##### 右上角关闭按钮
<div class="codes">
<div style="background-color: #ddd;position: relative;width: 500px;height: 100px;">
	<a href="" class="btn close"><i class="fa fa-close"></i></a>
</div>
<style type="text/css">
	.btn.close{padding: 0;display: block;width: 30px;height: 30px;line-height:25px;position: absolute;right: -13px;top: -13px;border-radius:50%;font-size: 20px;}
	.btn.close:hover{transform: scale(1.1);}
	.btn.close i{padding: 0;}
</style>
</div>
##### html
```
<a href="" class="btn close"><i class="fa fa-close"></i></a>
```
##### style
```
<style type="text/css">
	.btn.close{padding: 0;display: block;width: 30px;height: 30px;line-height:25px;position: absolute;right: -13px;top: -13px;border-radius:50%;font-size: 20px;}
	.btn.close:hover{transform: scale(1.1);}
	.btn.close i{padding: 0;}
</style>
```
### 固定按钮
<div class="codes">
<div class="fixed-btns" style="bottom: 45px; right: 24px;">
    <a class="btn red">
      <i class="fa fa-th-large fa-2x"></i>
    </a>
    <ul>
      <li><a class="btn red"><i class="fa fa-university"></i></a></li>
      <li><a class="btn yellow darken-1"><i class="fa fa-users"></i></a></li>
      <li><a class="btn green"><i class="fa fa-server"></i></a></li>
      <li><a class="btn blue"><i class="fa fa-rss"></i></a></li>
    </ul>
</div>
<style type="text/css">
	.fixed-btns{position: fixed;padding-top: 15px;margin-bottom: 0;z-index: 998;}
	.fixed-btns>.btn{width: 55px;height: 55px;line-height:56px;border-radius: 50%;}
	.fixed-btns .btn{padding: 0;}
	.fixed-btns .btn i{padding: 0;}
	.fixed-btns ul{position: absolute;left: 0;right: 0;bottom: 64px;text-align: center;}
	.fixed-btns ul li{padding-bottom: 15px;list-style:none!important;}
	.fixed-btns ul .btn{
		width: 36px;height: 36px;border-radius:50%;line-height:35px;
		transform: scaleY(0.4) scaleX(0.4) translateY(40px);opacity: 0;
	}
	.fixed-btns:hover ul .btn{transform: scaleY(1) scaleX(1) translateY(0px);opacity: 1;}}
	.red{background-color: #F44336;}
	.yellow{background-color: #ffeb3b;}
	.green{background-color: #4CAF50;}
	.blue{background-color: #2196F3;}
</style>
</div>
##### html
```
<div class="fixed-btns" style="bottom: 45px; right: 24px;">
    <a class="btn red">
      <i class="fa fa-th-large fa-2x"></i>
    </a>
    <ul>
      <li><a class="btn red"><i class="fa fa-university"></i></a></li>
      <li><a class="btn yellow darken-1"><i class="fa fa-users"></i></a></li>
      <li><a class="btn green"><i class="fa fa-server"></i></a></li>
      <li><a class="btn blue"><i class="fa fa-rss"></i></a></li>
    </ul>
</div>
```
##### style
```
<style type="text/css">
	.fixed-btns{position: fixed;padding-top: 15px;margin-bottom: 0;z-index: 998;}
	.fixed-btns>.btn{width: 55px;height: 55px;line-height:56px;border-radius: 50%;}
	.fixed-btns .btn{padding: 0;}
	.fixed-btns .btn i{padding: 0;}
	.fixed-btns ul{position: absolute;left: 0;right: 0;bottom: 64px;text-align: center;}
	.fixed-btns ul li{padding-bottom: 15px;}
	.fixed-btns ul .btn{
		width: 36px;height: 36px;border-radius:50%;line-height:35px;
		transform: scaleY(0.4) scaleX(0.4) translateY(40px);opacity: 0;
	}
	.fixed-btns:hover ul .btn{transform: scaleY(1) scaleX(1) translateY(0px);opacity: 1;}}
	.red{background-color: #F44336;}
	.yellow{background-color: #ffeb3b;}
	.green{background-color: #4CAF50;}
	.blue{background-color: #2196F3;}
</style>
```
### 按钮组
<div class="codes">
<div class="large" style="margin-top:10px;">

	<a href="" class="btn">BUTTON</a>

	<a href="" class="btn"><i class="fa fa-bars fa-2x"></i>BUTTON</a>

</div>
<style type="text/css">
	.btn{
		border:none;border-radius:2px;display:inline-block;*display:inline;*zoom:1;padding:0 20px;outline:0;vertical-align: middle;
		color:#fff;background-color: #26a69a;text-decoration: none;text-align: center;
		box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);transition: .5s;
	}
	.btn:hover{box-shadow:0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);cursor: pointer;}
	.btn i{padding-right: 12px;vertical-align:middle;}

	.large .btn{height: 54px;line-height:56px;margin-right: 20px;}
</style>
</div>
##### html
```
<a href="" class="btn">BUTTON</a>

<a href="" class="btn"><i class="fa fa-bars fa-2x"></i>BUTTON</a>
```
##### style
```
<style type="text/css">
	.btn{
		border:none;border-radius:2px;display:inline-block;*display:inline;*zoom:1;padding:0 20px;outline:0;vertical-align: middle;
		color:#fff;background-color: #26a69a;text-decoration: none;text-align: center;
		box-shadow: 0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);transition: .5s;
	}
	.btn:hover{background-color: #2bbbad;box-shadow:0 8px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19)}
	.btn i{padding-right: 12px;vertical-align:middle;}

	.large .btn{height: 54px;line-height:56px;margin-right: 20px;}
</style>
```