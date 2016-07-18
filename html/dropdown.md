## 下拉菜单
<div class="codes">
<div class="dropdown">
	<a class="dropdown-button"href="#!">Dropdown<i class="fa fa-caret-down"></i></a>
	<ul class="dropdown-content">
		<li><a href="#!">one</a></li>
		<li><a href="#!">two</a></li>
		<li class="divider"></li>
		<li><a href="#!">three</a></li>
	</ul>
</div>
<style type="text/css">
		.dropdown{position:relative;display:inline-block;width: 180px;height: 50px;background-color: #ee6e73;}
		.dropdown>a{font-size: 16px;color:#fff;display: block;line-height:50px;text-align: center;}
		.dropdown i{padding:0 5px;}
		.dropdown:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
		.dropdown-content{background-color:#fff;display:none;opacity:0;z-index:1;white-space:nowrap;position:absolute;width:100%;margin:0;will-change:width,height;}
		.dropdown-content li{clear:both;cursor:pointer;padding:0 10px;text-align:left;text-transform:none;}
		.dropdown-content li:hover,.dropdown-content li.active{background-color:#eee;}
		.dropdown-content li > a,.dropdown-content li > span{font-size:18px;color:#26a69a;display:block;line-height:30px;}
</style>
</div>
##### html
```
<div class="dropdown">
	<a class="dropdown-button"href="#!">Dropdown<i class="fa fa-caret-down"></i></a>
	<ul class="dropdown-content">
		<li><a href="#!">one</a></li>
		<li><a href="#!">two</a></li>
		<li class="divider"></li>
		<li><a href="#!">three</a></li>
	</ul>
</div>
```
##### less
```
<style type="text/less">
	.dropdown{
		@width:180px;
		@height:50px;
		@bgc:#ee6e73;
		@fontSize:16px;
		position:relative;display:inline-block;width: @width;height: @height;background-color: @bgc;
		&>a{font-size: @fontSize;color:#fff;display: block;line-height:@height;text-align: center;}
		&:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
		i{padding:0 5px;}
		.dropdown-content{
			background-color:#fff;display:none;opacity:0;z-index:1;white-space:nowrap;position:absolute;width:100%;margin:0;will-change:width,height;
			li{
				clear:both;cursor:pointer;padding:0 10px;text-align:left;text-transform:none;
				&.active,&:hover{background-color:#eee;}
				&>a,&>span{font-size:@fontSize + 2;color:#26a69a;display:block;line-height:30px;}
			}
		}
	}
</style>
```
##### style
```
<style type="text/css">
	.dropdown{position:relative;display:inline-block;width: 180px;height: 50px;background-color: #ee6e73;}
	.dropdown>a{font-size: 16px;color:#fff;display: block;line-height:50px;text-align: center;}
	.dropdown i{padding:0 5px;}
	.dropdown:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
	.dropdown-content{background-color:#fff;display:none;opacity:0;z-index:1;white-space:nowrap;position:absolute;width:100%;margin:0;will-change:width,height;}
	.dropdown-content li{clear:both;cursor:pointer;padding:0 10px;text-align:left;text-transform:none;}
	.dropdown-content li:hover,.dropdown-content li.active{background-color:#eee;}
	.dropdown-content li > a,.dropdown-content li > span{font-size:18px;color:#26a69a;display:block;line-height:30px;}
</style>
```