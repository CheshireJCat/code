## Tab Box
<div class="codes">
<div class="tabBox">
<ul class="tabs">
    <li class="active"><a href="#tab1">Tab One</a></li>
    <li><a href="#tab2">Tab Two</a></li>
    <li><a href="#tab3">Tab Three</a></li>
</ul>
<div class="tab-content active" id="tab1">
    <p>tab-content1</p>
</div>
<div class="tab-content" id="tab2">
    <p>tab-content2</p>
</div>
<div class="tab-content" id="tab3">
    <p>tab-content3</p>
</div>
<style>
.tabBox .tabs{margin:0;padding:0 10px;overflow:hidden;margin-bottom:-1px;height:2.25em;}
.tabBox .tabs li{float:left;list-style:none;margin:0;padding:.25em .25em 0;height:2em;overflow:hidden;position:relative;z-index:1;border-bottom:1px solid #FFF;}
.tabBox .tabs li.active{z-index:3;}
.tabBox .tabs a{float:left;height:2em;line-height:2em;border-radius:3px 3px 0 0;background:#EEE;border:1px solid #CCC;border-bottom:0;padding:0 10px;color:#000;text-decoration:none;}
.tabBox .tabs .active a{background:#FFF;box-shadow:#CCC 0 0 .25em;}
.tabBox .tabs a:hover{background:linear-gradient(#EEF,#FFF 70%);}
.tabBox .tab-content{clear:left;position:relative;z-index:2;padding:2em 1em;border:1px solid #CCC;background:#FFF;border-radius:3px;box-shadow:#CCC 0 0 .25em;display: none;}
.tabBox .tab-content.active{display: block;}
</style>
<script>
	$(".tabs").on('click','a',function(){
		event.preventDefault();
		$(this).parent().addClass('active').siblings().removeClass('active');
		$($(this).attr('href')).addClass('active').siblings('.tab-content').removeClass('active');
	});
</script>
</div>
</div>
##### html
```
<div class="tabBox">
    <ul class="tabs">
        <li class="active"><a href="#">Tab One</a></li>
        <li><a href="#">Tab Two</a></li>
        <li><a href="#">Tab Three</a></li>
    </ul>
    <div class="tab-content active">
        <p>tab-content1</p>
    </div>
    <div class="tab-content">
        <p>tab-content2</p>
    </div>
    <div class="tab-content">
        <p>tab-content3</p>
    </div>
</div>
```
##### css
```
<style>
	.tabBox .tabs{margin:0;padding:0 10px;overflow:hidden;margin-bottom:-1px;height:2.25em;}
	.tabBox .tabs li{float:left;list-style:none;margin:0;padding:.25em .25em 0;height:2em;overflow:hidden;position:relative;z-index:1;border-bottom:1px solid #FFF;}
	.tabBox .tabs li.active{z-index:3;}
	.tabBox .tabs a{float:left;height:2em;line-height:2em;border-radius:3px 3px 0 0;background:#EEE;border:1px solid #CCC;border-bottom:0;padding:0 10px;color:#000;text-decoration:none;}
	.tabBox .tabs .active a{background:#FFF;box-shadow:#CCC 0 0 .25em;}
	.tabBox .tabs a:hover{background:linear-gradient(#EEF,#FFF 70%);}
	.tabBox .tab-content{clear:left;position:relative;z-index:2;padding:2em 1em;border:1px solid #CCC;background:#FFF;border-radius:3px;box-shadow:#CCC 0 0 .25em;display: none;}
	.tabBox .tab-content.active{display: block;}
</style>
```
##### javascript
```
<script>
	$(".tabs").on('click','a',function(){
		event.preventDefault();
		$(this).parent().addClass('active').siblings().removeClass('active');
		$($(this).attr('href')).addClass('active').siblings('.tab-content').removeClass('active');
	});
</script>
```