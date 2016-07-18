## Html5音频和视频播放示例  
```
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title>html5中的音频和视频</title>
</head>
<body>
    <!--html4中的音频视频播放方式 代码冗杂，加载失败无法播放，一片空白..需要flash支持 -->
    <object classid="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" width="500" height="400" codebase="swflash.cab#version=6,0,10,0">
        <param name="allowFullScreen" value="true" />
        <embed src="1117786.mp4" autostart="0" type="application/x-shockwave-flash" width="500" height="400"> </embed>
    </object>
    <!--html5音视频播放 
    autoplay:自动播放, 
    controls；显示控制条, 
    loop:是否循环播放, 
    preload:{预加载处理 
    auto:自动全部加载音视频 
    none:不加载 
    metadata：预加载元数据(媒体字节数,第一帧，播放列表，持续时间等) }， 
    poster:（video元素独有）当预加载的视频不存在时，显示一张默认的图片， 
    error:正常情况下为null,出现错误返回一个MediaError对象，有四种状态: 
    	MEDIA_ERR_ABORTED (数字为1):媒体下载过程中由于用户操作原因终止; 
    	MEDIA_ERR_NETWORK (数字为2):网络错误媒体下载终止 
    	MEDIA_ERR_DECODE (数字为3):媒体解码错误 
    	MEDIA_ERR_SRC_NOT_SUPPORTED (数字为4):媒体格式不支持， net 
    -->
    <!--http://v.youku.com/v_show/id_XMjE4MDU1MDE2.html-->
    <video id="video" src="1117786.mp4" preload="a" loop="loop" autoplay="autoplay" controls="controls" width="500px" height="450px"> 您的浏览器不支持video！
        <!--source :为媒体文件指定多个播放格式和编码方式-->
        <source src="1117786.mp4" type="video/ogg">
        <script type="text/javascript">
        var video = document.getElementById("video"); 
        //监听错误信息 
        video.addEventListener("error", function() {
		    var error = video.error;
		    var code = error.code;
		    switch (code) {
		        case 1:
		            console.info("视频加载被终止");
		            break;
		        case 2:
		            console.info("网络原因,视频加载被终止");
		            break;
		        case 3:
		            console.info("解码失败");
		            break;
		        case 4:
		            console.info("视频格式不支持");
		            break;
		    }
		}, false);

        /** 
         * networkState:网络状态属性， 
         * 在加载过程中读取当前网络的状态, 
         * NETWORK_EMPTY（数字为 0）:网络链接初始状态, 
         * NETWORK_IDLE（数字为1）:已经选择好媒体播放格式,未建立网络链接, 
         * NETWORK_LOADING（数字为2）:媒体加载中...， 
         * NETWORK_NO_SOURCE（数字为3）:没有支持的编码格式 
         **/
         //获取networkState属性
         /** * 此处针对网络媒体而言,播放本地视频 net===3 * @type {Number} */ 
         var net = video.networkState;
		if (net == 0) {
		    console.info('网络链接初始状态..');
		} else if (net == 1) {
		    console.info('已经选择好媒体播放格式,未建立网络链接');
		} else if (net == 2) {
		    console.info('媒体加载中...');
		} else if (net == 3) {
		    console.info('没有支持的编码格式');
		}
		//currentSrc:为只读属性,获取播放文件的src地址，本地文件为空 
		var src = video.currentSrc;
		console.info("对应的src为:" + src);

         //buffered:属性 
         /** 
         * 返回一个对象，实现了TimeRanges接口， 
         * 以确认浏览器是否缓存数据。 
         * TimeRanges:表示一段时间范围，大多数情况下TimeRanges对象表示的时间范围是一个从0开始的范围。 
         * TimeRanges:有一个length属性,表示有多少个时间范围,大多数情况下，存在时间范围时该值为1,不存在时为0. 
         * 有两个方法，start(index) 和end(index),大多数情况下index设置为0即可; 
         * @type {TimeRanges} */ 
         var buf = video.buffered; console.info(buf.length); 
         /** 
         * readyState属性:返回当前媒体播放位置的就绪状态，有五个可能值。 
         * HAVE_NOTHING:(数字为0)没有获取到媒体的任何信息,当前播放位置没有可播放的数据. 
         * HAVE_METADATA:(数字为1)已经获取到足够的媒体数据,但是当前位置的媒体数据无效. 
         * HAVE_CURRENT_DATA:(数字为2):当前位置已经有数据可以播放，但是没有获取到让播放器前进的数据。（ 
         * 没有获取到下一帧的数据或者播放已经完成） 
         * HAVE_FUTURE_DATA:(数字3)表示当前位置已经获取到数据，可获取到让播放器前进的数据。为视频文件时，表示当前帧和下一帧 
         * 数据都获取到了,当当前位置是最后一帧时表示，readyState不可能为3状态(HAVE_FUTURE_DATA)。 
         * HAVE_ENOUGH_DATA:(数字4)表示当前位置已经获取到数据，可获取到让播放器前进的数据， 
         * 浏览器以某一速度加载，保证足够的数据进行播放。 * @type {number|Number} */
         var state = video.readyState; console.info("readyState属性为:"+state); 
         /** 
         * seekable 和seeking属性:表示浏览器是否正在请求特定播放位置的数据. 
         * 
         * seeking属性返回boolean值，true表示正在请求，false表示停止请求。 
         * 
         * seekable属性返回一个TimeRanges对象,表示请求到的时间范围。 
         * 
         * 均为只读属性。 
         * @type {TimeRanges} */ 
         var seekable = video.seekable; 
         var seeking = video.seeking; console.info("浏览器是否正在请求特定播放位置的数据:"+seeking); 
         /** * * @type {Number} */ 
         var cur = video.currentTime; var startTime = video.startTime;
         //开始播放的时间，一般为0 
         var duration = video.duration;
         //媒体文件总的播放时间. 
         console.info(cur+","+startTime+","+duration); 
         //浏览器支持不一致: Firefox:0 ,undefined,NaN Chrome: 0,0,NaN 
         /** 
         *played :读取已经播放的时间段 
         * @type {TimeRanges} 
         * */ 
         var play = video.played; 
         /** 
         * 是否为暂停状态， 
         * true表示暂停播放， 
         * false表示正在播放 
         * @type {boolean} */ 
         var paused = video.paused; 
         /** 
         * ended属性：boolean值 
         * true:表示播放完毕 
         * false：表示正在播放 
         * @type {boolean} */ 
         var ended= video.ended; 
         /** 
         * defaultPlaybackRate: 
         * 修改或者读取默认的播放速率 
         * playbackRate: 
         * 修改或者读取当前的播放速率 
         * @type {Number} */ 
         var rate = video.defaultPlaybackRate;
         var playRate =video.playbackRate; 
         console.info("当前媒体的播放速率:"+rate); 
         /** 
         * * volume属性: 读取或者修改默认音量，从0到1.0为静音，1为最大音量. 
         * @type {Number|CSSStyleDeclaration.volume|*} */
         var volume = video.volume; volume=0.4; 
         /** * muted:返回boolean值。 * true:表示静音状态 * @type {boolean} */ 
         var muted = video.muted; console .info("当前音量:"+volume+","+muted);
        </script>
    </video>
    <input type="button" onclick="pause();" value="暂停">
    <input type="button" onclick="play();" value="播放">
    <script>
    var video = document.getElementById("video");

    function pause() {
        video.pause();
        console.warn("视频已经暂停"); //判断是否为暂停状态 
        console.info(video.paused); 
    } 
    function play(){ 
    	video.play(); console.warn("视频开始播放..."); 
    }
    </script>
    <audio>
        <!-- 音频和视频的属性和方法，以及事件处理基本一致。 -->
    </audio>
</body>
</html>

```