## html5shiv
<div class="codes">
<div class="nav-search">
	<input class="nav-search-input"type="text"placeHolder="搜索"><span class="nav-search-btn"><i class="fa fa-search"></i></span>
</div>
<style type="text/css">
	.nav-search{position:relative;display:table;border-collapse:separate;color:#555;width: 200px;box-shadow:0 0px 17px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19)}
	.nav-search-input{display:table-cell;position:relative;z-index:2;float:left;width:100%;height:34px;padding:6px 12px;color:#555;background-color:#fff;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;background-color:#fff;}
	.nav-search-btn{display:table-cell;position:relative;z-index:3;vertical-align:middle;padding:0 10px;background-color:#f2f2f2;border-radius:0 3px 3px 0;}
	.nav-search-btn:hover{background-color:#e6e6e6;cursor:pointer;}
</style>
</div>
##### html
```
<div class="nav-search">
	<input class="nav-search-input"type="text"placeHolder="搜索"><span class="nav-search-btn"><i class="fa fa-search"></i></span>
</div>
```
##### less
```
<style type="text/less">
.nav-search{
	@width:200px;
	@height:34px;
	@bgc:#fff;
	@wordColor:#555;
	@btnBgc:#f2f2f2;
	@btnHoverBgc:#e6e6e6;
	position:relative;display:table;border-collapse:separate;color:@wordColor;display:inline-block;width: @width;
	.nav-search-input,.nav-search-btn{display:table-cell;position:relative;}
	.nav-search-input{float: left;z-index:2;width:100%;height:@height;padding:6px 12px;color:@wordColor;background-color:@bgc;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;}
	.nav-search-btn{
		z-index:3;vertical-align:middle;padding:0 10px;background-color:@btnBgc;border-radius:0 3px 3px 0;
		&:hover{background-color:@btnHoverBgc;cursor:pointer;}
	}
}
</style>
```
##### style
```
<style type="text/css">
	.nav-search{position:relative;display:table;border-collapse:separate;color:#555;display:inline-block;width: 200px;}
	.nav-search-input{display:table-cell;position:relative;z-index:2;float:left;width:100%;height:34px;padding:6px 12px;color:#555;background-color:#fff;box-sizing:border-box;border:0;border-radius:3px 0 0 3px;background-color:#fff;}
	.nav-search-btn{display:table-cell;position:relative;z-index:3;vertical-align:middle;padding:0 10px;background-color:#f2f2f2;border-radius:0 3px 3px 0;}
	.nav-search-btn:hover{background-color:#e6e6e6;cursor:pointer;}
</style>
```