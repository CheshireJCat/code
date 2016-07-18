## 移动端底部下载App按钮
<div class="codes">
<div style="width:340px;height:100px;position:relative;background:#000;">
<div class="openApp">
    <div class="open_bar"><img src="http://img.mjs.sinajs.cn/blog/ria/h5/v1/images/blg_logo.png" width="47" height="47" class="bar_logo">
        <p class="open_tit">新浪博客</p>
        <p class="bar_intrdc">最新版手机客户端</p>
        <div class="open_btn">打开</div>
    </div>
    <div class="open_cls"><span class="cls_bdr"data-role="ad-close"><i class="open_cls_l"></i><i class="open_cls_r"></i></span></div>
</div>
</div>
<style type="text/css">
	.openApp{position:absolute;bottom:0;width:100%;z-index:9999;background-color:rgba(255,255,255,.94)}
	.openApp .open_bar{position:relative;padding:0 5px 0 73px;height:60px;text-decoration:none;color:#000}
	.openApp .bar_logo{position:absolute;top:8px;left:16px;border-radius:5px}
	.openApp .open_tit{margin:0;font-size:22px;line-height:22px;padding:13px 0 0}
	.openApp .bar_intrdc{margin:0;font-size:10px;line-height:10px;opacity:.6;padding:5px 0 0;color:#6e6e6e}
	.openApp .open_btn{right:66px;background-color:#ff7843;position:absolute;top:14px;width:72.5px;height:35px;color:#fff;font-weight:700;font-size:18px;line-height:35px;text-align:center;border-radius:2px}
	.openApp .open_cls{position:absolute;right:0;top:0;height:50px;width:43px;z-index:10}
	.openApp .cls_bdr{position:absolute;top:18px;display:inline-block;width:25px;height:25px;border-radius:13px;border:1px solid #a0a0a0}
	.openApp .open_cls_l,.openApp .open_cls_r{position:absolute;left:12px;top:5px;width:1px;height:15px;background-color:#a0a0a0;display:inline-block}
	.openApp .open_cls_l{-webkit-transform:rotate(-45deg)}.openApp .open_cls_r{-webkit-transform:rotate(45deg);}
</style>
</div>
##### html
```
<div class="openApp">
    <div class="open_bar"><img src="http://img.mjs.sinajs.cn/blog/ria/h5/v1/images/blg_logo.png" width="47" height="47" class="bar_logo">
        <p class="open_tit">新浪博客</p>
        <p class="bar_intrdc">最新版手机客户端</p>
        <div class="open_btn">打开</div>
    </div>
    <div class="open_cls"><span class="cls_bdr"data-role="ad-close"><i class="open_cls_l"></i><i class="open_cls_r"></i></span></div>
</div>
```
##### style
```
<style type="text/css">
	.openApp{position:absolute;bottom:0;width:100%;z-index:9999;background-color:rgba(255,255,255,.94)}
	.openApp .open_bar{position:relative;padding:0 5px 0 73px;height:60px;text-decoration:none;color:#000}
	.openApp .bar_logo{position:absolute;top:8px;left:16px;border-radius:5px}
	.openApp .open_tit{margin:0;font-size:22px;line-height:22px;padding:13px 0 0}
	.openApp .bar_intrdc{margin:0;font-size:10px;line-height:10px;opacity:.6;padding:5px 0 0;color:#6e6e6e}
	.openApp .open_btn{right:66px;background-color:#ff7843;position:absolute;top:14px;width:72.5px;height:35px;color:#fff;font-weight:700;font-size:18px;line-height:35px;text-align:center;border-radius:2px}
	.openApp .open_cls{position:absolute;right:0;top:0;height:50px;width:43px;z-index:10}
	.openApp .cls_bdr{position:absolute;top:18px;display:inline-block;width:25px;height:25px;border-radius:13px;border:1px solid #a0a0a0}
	.openApp .open_cls_l,.openApp .open_cls_r{position:absolute;left:12px;top:5px;width:1px;height:15px;background-color:#a0a0a0;display:inline-block}
	.openApp .open_cls_l{-webkit-transform:rotate(-45deg)}.openApp .open_cls_r{-webkit-transform:rotate(45deg);}
</style>
```