## 顶部导航
<div class="codes">
<div class="nav">
	<a href="#!"class="logo">Logo</a>
	<ul class="navs">
		<li><a href="badges">标签</a></li>
		<li><a href="buttons">按钮</a></li>
		<li class="dropdown">
			<a class="dropdown-button"href="#!">Dropdown<i class="fa fa-caret-down"></i></a>
			<ul class="dropdown-content">
				<li><a href="#!">one</a></li>
				<li><a href="#!">two</a></li>
				<li class="divider"></li>
				<li><a href="#!">three</a></li>
			</ul>
		</li>
		<li class="nav-search">
			<input class="nav-search-input"type="text"placeHolder="搜索"><span class="nav-search-btn"><i class="fa fa-search"></i></span>
		</li>
	</ul>
	
</div>
<style type="text/css">
.nav{color:#fff;background-color:#ee6e73;width:100%;height:64px;line-height:64px;position:relative;}
.nav .logo{position:absolute;color:#fff;display:block;font-size:20px;padding:0;line-height:64px;}
.navs{float:right;transition:background-color .3s;margin:0!important;}
.navs li{float:left;padding:0;margin:0!important;list-style:none!important;}
.navs li:hover,.navs li.active{background-color:rgba(0,0,0,0.1)}
.navs a{font-size:16px;color:#fff;display:block;padding:0 15px;line-height:65px;}
.dropdown{position:relative;}
.dropdown i{padding:0 5px;}
.dropdown:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
.dropdown-content{background-color:#fff;margin:0;display:none;min-height:100px;opacity:0;z-index:1;white-space:nowrap;position:absolute;will-change:width,height;width:100%;}
.dropdown-content li{clear:both;cursor:pointer;width:100%;text-align:left;text-transform:none;}
.dropdown-content li:hover,.dropdown-content li.active{background-color:#eee;}
.dropdown-content li > a,.dropdown-content li > span{font-size:18px;color:#26a69a;display:block;line-height:30px;}
li.nav-search{position:relative;display:table;border-collapse:separate;color:#555;float:right;margin-top:16px!important;margin-right: 15px!important;}
.nav-search-input{display:table-cell;position:relative;z-index:2;float:left;width:100%;height:34px;padding:6px 12px;color:#555;background-color:#fff;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;background-color:#fff;}
.nav-search-btn{display:table-cell;position:relative;z-index:3;vertical-align:middle;padding:0 10px;background-color:#f2f2f2;border-radius:0 3px 3px 0;}
.nav-search-btn:hover{background-color:#e6e6e6;cursor:pointer;}
</style>
</div>
##### html<div class="codes">
```
<div class="nav">
	<a href="#!"class="logo">Logo</a>
	<ul class="navs">
		<li><a href="badges">标签</a></li>
		<li><a href="buttons">按钮</a></li>
		<li class="dropdown">
			<a class="dropdown-button"href="#!">Dropdown<i class="fa fa-caret-down"></i></a>
			<ul class="dropdown-content">
				<li><a href="#!">one</a></li>
				<li><a href="#!">two</a></li>
				<li class="divider"></li>
				<li><a href="#!">three</a></li>
			</ul>
		</li>
	</ul>
	<li class="nav-search">
		<input class="nav-search-input"type="text"placeHolder="搜索"><span class="nav-search-btn"><i class="fa fa-search"></i></span>
	</li>
</div>
```
##### less		
```
<style type="text/less">
	@wordColor:#fff;
	@bgc:#ee6e73;
	@height:64px;
	@fontSize:16px;
	.nav{
		background-color:@bgc;width:100%;height:@height;position:relative;
		.logo{position:absolute;color:#fff;display:block;font-size:@fontSize + 4;padding:0;line-height:@height;}
	}
	.navs{
		float:right;transition:background-color .3s;
		li{
			float:left;padding:0;
			&.active,&:hover{background-color:rgba(0,0,0,0.1);}
		}
		a{font-size:@fontSize;color:@wordColor;display:block;padding:0 15px;line-height:@height;}
	}
	.dropdown{
		position:relative;
		i{padding:0 5px;}
		&:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
	}
	.dropdown-content{
		background-color:#fff;margin:0;display:none;opacity:0;z-index:1;white-space:nowrap;position:absolute;will-change:width,height;width:100%;
		li{
			clear:both;cursor:pointer;width:100%;text-align:left;text-transform:none;
			&.active,&:hover{background-color:#eee;}
			&>a,&>span{font-size:@fontSize + 2;color:#26a69a;display:block;line-height:30px;}
		}
	}

	.nav-search{position:relative;display:table;border-collapse:separate;color:#555;float:right;margin-top:16px;margin-right: 15px;}
	.nav-search-input{display:table-cell;position:relative;z-index:2;float:left;width:100%;height:34px;padding:6px 12px;color:#555;background-color:#fff;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;background-color:#fff;}
	.nav-search-btn{display:table-cell;position:relative;z-index:3;vertical-align:middle;padding:0 10px;background-color:#f2f2f2;border-radius:0 3px 3px 0;}
	.nav-search-btn:hover{background-color:#e6e6e6;cursor:pointer;}
</style>
```
##### style		
```
<style type="text/css">
	.nav{color:#fff;background-color:#ee6e73;width:100%;height:64px;line-height:64px;position:relative;}
	.nav .logo{position:absolute;color:#fff;display:block;font-size:20px;padding:0;line-height:64px;}
	.navs{float:right;transition:background-color .3s;}
	.navs li{float:left;padding:0;}
	.navs li:hover,.navs li.active{background-color:rgba(0,0,0,0.1)}
	.navs a{font-size:16px;color:#fff;display:block;padding:0 15px;line-height:65px;}
	.dropdown{position:relative;}
	.dropdown i{padding:0 5px;}
	.dropdown:hover .dropdown-content{display:block;opacity:1;box-shadow:0 8px 17px 0 rgba(0,0,0,0.2),0 6px 20px 0 rgba(0,0,0,0.19);}
	.dropdown-content{background-color:#fff;margin:0;display:none;min-height:100px;opacity:0;z-index:1;white-space:nowrap;position:absolute;will-change:width,height;width:100%;}
	.dropdown-content li{clear:both;cursor:pointer;width:100%;text-align:left;text-transform:none;}
	.dropdown-content li:hover,.dropdown-content li.active{background-color:#eee;}
	.dropdown-content li > a,.dropdown-content li > span{font-size:18px;color:#26a69a;display:block;line-height:30px;}
	.nav-search{position:relative;display:table;border-collapse:separate;color:#555;float:right;margin-top:16px;margin-right: 15px;}
	.nav-search-input{display:table-cell;position:relative;z-index:2;float:left;width:100%;height:34px;padding:6px 12px;color:#555;background-color:#fff;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;background-color:#fff;}
	.nav-search-btn{display:table-cell;position:relative;z-index:3;vertical-align:middle;padding:0 10px;background-color:#f2f2f2;border-radius:0 3px 3px 0;}
	.nav-search-btn:hover{background-color:#e6e6e6;cursor:pointer;}
</style>
```
