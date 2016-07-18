## 消息提醒（徽章）
徽章能用来通知你有新消息或者提醒信息。使用new为徽章设置背景色
<div class="collection">
    <a href="#!" class="collection-item">Alan<span class="badge">1</span></a>
    <a href="#!" class="collection-item">Alan<span class="new badge">4</span></a>
    <a href="#!" class="collection-item">Alan</a>
    <a href="#!" class="collection-item">Alan<span class="badge">14</span></a>
</div>
<style type="text/css">
	.collection{border: 1px solid #e0e0e0;overflow: hidden;border-radius: 2px;position: relative;width: 400px;margin:0 auto;}
	.collection-item{display: block;color: #26a69a;transition: 0.25s;padding: 10px 20px;border-top: 1px solid #e0e0e0;line-height:20px;}
	.collection-item:hover{background-color: #e0e0e0;}
	.collection-item:first-child{border-top: none;}

	.badge{min-width:33px;font-size: 12px;text-align: center;color:#757575;position: absolute;right: 15px;box-sizing: border-box;}
	span.badge.new{color:#fff;background-color: #26a69a;border-radius: 2px;}
</style>
##### html
```
<div class="collection">
    <a href="#!" class="collection-item">Alan<span class="badge">1</span></a>
    <a href="#!" class="collection-item">Alan<span class="new badge">4</span></a>
    <a href="#!" class="collection-item">Alan</a>
    <a href="#!" class="collection-item">Alan<span class="badge">14</span></a>
</div>
```
##### style
```
<style type="text/css">
	.collection{border: 1px solid #e0e0e0;overflow: hidden;border-radius: 2px;position: relative;width: 400px;}
	.collection-item{display: block;color: #26a69a;transition: 0.25s;padding: 10px 20px;border-top: 1px solid #e0e0e0;line-height:20px;}
	.collection-item:hover{background-color: #e0e0e0;}
	.collection-item:first-child{border-top: none;}

	.badge{min-width:33px;font-size: 12px;text-align: center;color:#757575;position: absolute;right: 15px;box-sizing: border-box;}
	span.badge.new{color:#fff;background-color: #26a69a;border-radius: 2px;}
</style>
```
