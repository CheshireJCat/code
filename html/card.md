## 卡片
### 基础样式
<div class="codes">
<div class="card">
    <div class="card-content">
      <span class="card-title">Card Title</span>
        <p>I am a very simple card. I am good at containing small bits of information.
        I am convenient because I require little markup to use effectively.</p>
    </div>
    <div class="card-action">
      <a href="#">This is a link</a>
      <a href='#'>This is a link</a>
    </div>
</div>
<style type="text/css">
	.card{width: 33%;position: relative;overflow:hidden;margin:7px 0 15px;background-color: #546e7a;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);color:#fff;}
	.card .card-content{padding: 20px;border-radius: 0 0 2px 2px;}
	.card .card-title{line-height:48px;font-size: 24px;}
	.card .card-content p{margin: 0;padding: 0;}
	.card .card-action{border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;}
	.card .card-action a{color:#ffab40;margin-right: 20px;transition: color .3s ease;font-size: 18px;}
	.card .card-action a:hover {color: #ffd8a6;}
</style>
</div>
##### html			
```
<div class="card">
    <div class="card-content">
      <span class="card-title">Card Title</span>
        <p>I am a very simple card. I am good at containing small bits of information.
        I am convenient because I require little markup to use effectively.</p>
    </div>
    <div class="card-action">
      <a href="#">This is a link</a>
      <a href='#'>This is a link</a>
    </div>
</div>
```
##### style
```
<style type="text/css">
	.card{width: 33%;position: relative;overflow:hidden;margin:7px 0 15px;background-color: #546e7a;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);color:#fff;}
	.card .card-content{padding: 20px;border-radius: 0 0 2px 2px;}
	.card .card-title{line-height:48px;font-size: 24px;}
	.card .card-content p{margin: 0;padding: 0;}
	.card .card-action{border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;}
	.card .card-action a{color:#ffab40;margin-right: 20px;transition: color .3s ease;font-size: 18px;}
	.card .card-action a:hover {color: #ffd8a6;}
</style>
```
##### less
```
<style type="text/less">
	.card{
		@width:33%;
		@margin:7px 0 15px;
		@bgc:#546e7a;
		@wordColor:#fff;
		@actionColor:#ffab40;
		@actionHoverColor:#ffd8a6;
		width: @width;position: relative;overflow:hidden;margin:@margin;background-color:@bgc;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);color:@wordColor;
		.card-content{
			padding: 20px;border-radius: 0 0 2px 2px;
			p{margin: 0;padding: 0;}
		}
		.card-title{line-height:48px;font-size: 24px;}
		.card-action{
			border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;
			a{
				color:@actionColor;margin-right: 20px;transition: color .3s ease;font-size: 18px;
				&:hover{color: @actionHoverColor;}
			}
		}
	}
</style>
```
### 图片
<div class="codes">
<div class="card">
	<div class="card-image">
        <img src="http://dummyimage.com/1024x768/4d494d/686a82.gif&text=placeholder+image" alt="placeholder+image">
        <span class="card-title">Card Title</span>
    </div>
    <div class="card-content">
        <p>I am a very simple card. I am good at containing small bits of information.
        I am convenient because I require little markup to use effectively.</p>
    </div>
    <div class="card-action">
      <a href="#">This is a link</a>
      <a href='#'>This is a link</a>
    </div>
</div>
<style type="text/css">
	.card{width: 33%;position: relative;overflow:hidden;margin:7px 0 15px;background-color: #546e7a;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);color:#fff;}

	.card .card-image{position: relative;}
	.card .card-image img{border-radius:2px 2px 0 0;position: relative;left: 0;right: 0;top: 0;bottom: 0;width: 100%;border: 0;}
	.card .card-image .card-title{position: absolute;bottom: 0;left: 0;padding:20px;}

	.card .card-content{padding: 20px;border-radius: 0 0 2px 2px;color:#fff;}
	.card .card-title{line-height:48px;font-size: 24px;}
	.card .card-content p{margin: 0;padding: 0;}
	.card .card-action{border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;}
	.card .card-action a{color:#ffab40;margin-right: 20px;transition: color .3s ease;font-size: 18px;}
	.card .card-action a:hover {color: #ffd8a6;}
</style>
</div>
##### html			
```
<div class="card">
    <div class="card-content">
      <span class="card-title">Card Title</span>
        <p>I am a very simple card. I am good at containing small bits of information.
        I am convenient because I require little markup to use effectively.</p>
    </div>
    <div class="card-action">
      <a href="#">This is a link</a>
      <a href='#'>This is a link</a>
    </div>
</div>
```
##### style
```
<style type="text/css">
	.card{width: 33%;position: relative;overflow:hidden;margin:7px 0 15px;background-color: #546e7a;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);}

	.card .card-image{position: relative;}
	.card .card-image img{border-radius:2px 2px 0 0;position: relative;left: 0;right: 0;top: 0;bottom: 0;width: 100%;border: 0;}
	.card .card-image .card-title{position: absolute;bottom: 0;left: 0;padding:20px;}

	.card .card-content{padding: 20px;border-radius: 0 0 2px 2px;color:#fff;}
	.card .card-title{line-height:48px;font-size: 24px;}
	.card .card-content p{margin: 0;padding: 0;}
	.card .card-action{border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;}
	.card .card-action a{color:#ffab40;margin-right: 20px;transition: color .3s ease;font-size: 18px;}
	.card .card-action a:hover {color: #ffd8a6;}
</style>
```
##### less
```
<style type="text/less">
	.card{
		@width:33%;
		@margin:7px 0 15px;
		@bgc:#546e7a;
		@wordColor:#fff;
		@actionColor:#ffab40;
		@actionHoverColor:#ffd8a6;
		width: @width;position: relative;overflow:hidden;margin:@margin;background-color:@bgc;border-radius:2px;box-shadow:0 2px 5px 0 rgba(0, 0, 0, 0.16), 0 2px 10px 0 rgba(0, 0, 0, 0.12);color:@wordColor;
		.card .card-image{
			position: relative;
			 img{border-radius:2px 2px 0 0;position: relative;left: 0;right: 0;top: 0;bottom: 0;width: 100%;border: 0;}
			 .card-title{position: absolute;bottom: 0;left: 0;padding:20px;}
		}
		.card-content{
			padding: 20px;border-radius: 0 0 2px 2px;
			p{margin: 0;padding: 0;}
		}
		.card-title{line-height:48px;font-size: 24px;}
		.card-action{
			border-top: 1px solid rgb(160, 160, 160);border-top: 1px solid rgba(160, 160, 160, 0.2);padding: 20px;
			a{
				color:@actionColor;margin-right: 20px;transition: color .3s ease;font-size: 18px;
				&:hover{color: @actionHoverColor;}
			}
		}
	}
</style>
```
