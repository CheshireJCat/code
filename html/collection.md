## 集合
### 基本
<ul class="collection">
	<li class="collection-header"><h4>title</h4></li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
</ul>
<style type="text/css">
.collection {margin: 0.5rem 0 1rem 0;border: 1px solid #e0e0e0;border-radius: 2px;overflow: hidden;position: relative;}
.collection .collection-item{background-color: #fff;line-height: 1.5rem;padding: 10px 20px;margin: 0;border-bottom: 1px solid #e0e0e0;}
.collection .collection-header{background-color: #fff;border-bottom: 1px solid #e0e0e0;padding: 10px 20px;font-size: 24px;line-height:35px;font-weight: bold;}
</style>
##### html
```
<ul class="collection">
	<li class="collection-header"><h4>title</h4></li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
    <li class="collection-item">Alvin</li>
</ul>
```
##### style
```
<style type="text/css">
	.collection {margin: 0.5rem 0 1rem 0;border: 1px solid #e0e0e0;border-radius: 2px;overflow: hidden;position: relative;}
	.collection .collection-item{background-color: #fff;line-height: 1.5rem;padding: 10px 20px;margin: 0;border-bottom: 1px solid #e0e0e0;}
	.collection .collection-header{background-color: #fff;border-bottom: 1px solid #e0e0e0;padding: 10px 20px;font-size: 24px;line-height:35px;font-weight: bold;}
</style>
```  

### 超链接
<div class="codes">
<div class="collection">
     <a href="#!" class="collection-item">Alvin</a>
     <a href="#!" class="collection-item active">Alvin</a>
     <a href="#!" class="collection-item">Alvin</a>
     <a href="#!" class="collection-item">Alvin</a>
</div>
<style type="text/css">
	.collection a.collection-item{	display: block;transition: 0.25s;color: #26a69a;}
	.collection a.collection-item:hover{	background-color: #ddd;}
</style>
</div>
##### html
```
<div class="collection">
     <a href="#!" class="collection-item">Alvin</a>
     <a href="#!" class="collection-item active">Alvin</a>
     <a href="#!" class="collection-item">Alvin</a>
     <a href="#!" class="collection-item">Alvin</a>
</div>
```
##### style
```
<style type="text/css">
	.collection {margin: 0.5rem 0 1rem 0;border: 1px solid #e0e0e0;border-radius: 2px;overflow: hidden;position: relative;}
	.collection .collection-item{background-color: #fff;line-height: 1.5rem;padding: 10px 20px;margin: 0;border-bottom: 1px solid #e0e0e0;}
	.collection a.collection-item{	display: block;transition: 0.25s;color: #26a69a;}
	.collection a.collection-item:hover{	background-color: #ddd;}
</style>  
```
### 头像
<ul class="collection">
     <li class="collection-item avatar">
     <img src="http://dummyimage.com/800x600/4d494d/686a82.gif&text=placeholder+image" alt="placeholder+image" class="circle photo">
       <span class="title">Title</span>
       <p>First Line <br>
       Second Line
       </p>
       <a href="#!" class="secondary-content"><i class="mdi-action-grade"></i></a>
     </li>
     <li class="collection-item avatar">
        <img src="http://dummyimage.com/800x600/4d494d/686a82.gif&text=placeholder+image" alt="placeholder+image" class="circle photo">
       <span class="title">Title</span>
       <p>First Line <br>
       Second Line
       </p>
       <a href="#!" class="secondary-content"><i class="mdi-action-grade"></i></a>
     </li>
   </ul>
<style type="text/css">
	.collection {margin: 0.5rem 0 1rem 0;border: 1px solid #e0e0e0;border-radius: 2px;overflow: hidden;position: relative;}
	.collection .collection-item{background-color: #fff;line-height: 1.5rem;padding: 10px 20px;margin: 0;border-bottom: 1px solid #e0e0e0;}
	.collection .collection-item.avatar{height: 84px;padding-left: 72px;position: relative;}
	.circle{border-radius:50%;}
	.collection .collection-item.avatar .photo{position: absolute;width: 42px;height: 42px;overflow-y: hidden;left: 15px;display: inline-block;vertical-align:middle;}
	.collection .collection-item.avatar .title{font-size: 16px;line-height: ;}
	.collection .collection-item.avatar p{margin: 0;}
	.collection .collection-item.avatar .secondary-content{position: absolute;top: 16px;right: 16px;color: #26a69a;float: right;}
</style>
##### html
```
<ul class="collection">
    <li class="collection-item avatar">
    <img src="http://dummyimage.com/800x600/4d494d/686a82.gif&amp;text=placeholder+image" alt="placeholder+image" class="circle photo">
      <span class="title">Title</span>
      <p>First Line <br>
      Second Line
      </p>
      <a href="#!" class="secondary-content"><i class="mdi-action-grade"></i></a>
    </li>
    <li class="collection-item avatar">
       <img src="http://dummyimage.com/800x600/4d494d/686a82.gif&amp;text=placeholder+image" alt="placeholder+image" class="circle photo">
      <span class="title">Title</span>
      <p>First Line <br>
      Second Line
      </p>
      <a href="#!" class="secondary-content"><i class="mdi-action-grade"></i></a>
    </li>
</ul>
```
##### style
```
<style type="text/css">
	.collection {margin: 0.5rem 0 1rem 0;border: 1px solid #e0e0e0;border-radius: 2px;overflow: hidden;position: relative;}
	.collection .collection-item{background-color: #fff;line-height: 1.5rem;padding: 10px 20px;margin: 0;border-bottom: 1px solid #e0e0e0;}
	.collection .collection-item.avatar{height: 84px;padding-left: 72px;position: relative;}
	.circle{border-radius:50%;}
	.collection .collection-item.avatar .photo{position: absolute;width: 42px;height: 42px;overflow-y: hidden;left: 15px;display: inline-block;vertical-align:middle;}
	.collection .collection-item.avatar .title{font-size: 16px;line-height: ;}
	.collection .collection-item.avatar p{margin: 0;}
	.collection .collection-item.avatar .secondary-content{position: absolute;top: 16px;right: 16px;color: #26a69a;float: right;}
</style>
```
