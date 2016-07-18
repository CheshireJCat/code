## JavaScript异步拖拽上传文件

##### upload.html
```
<!DOCTYPE html>
<html>
<head>
    <title>title</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
    #box {
        width: 150px;
        height: 150px;
        border: 1px solid red;
    }
    </style>
    <script type="text/javascript" src="XMLhttpReuest.js"></script>
    <script>
    window.onload = function() {
            var box = document.getElementById('box');
            box.ondragenter = function(e) {
                e.preventDefault();
            }
            box.ondragover = function(e) {
                e.preventDefault();
            }
            box.ondragleave = function(e) {
                e.preventDefault();
            }
            box.ondrop = function(e) {
                e.preventDefault();
                var file = e.dataTransfer.files[0];
                var formData = new FormData();
                formData.append('aa', file);
                var xml = ajaxFunction();
                xml.open("post", './upload.php', true);
                xml.send(formData);
                xml.onreadystatechange = function() {
	                if (xml.readyState == 4 && xml.status == 200) {
	                        var flag = xml.responseText;
	                        console.log(flag);
	                        if (flag == 1) { 
	                        box.innerHTML="上传成功"; 
	                        alert('上传成功'); 
	                    } 
	                } 
	            } 
	        } 
	    }
    </script>
</head>
<body>
    <div id="box"> 请拖入上传的文件 </div>
</body>
</html>
```  

##### upload.php  

```
<?php 
header("Content-Type:text/html;charset=UTF-8"); 
if(is_uploaded_file($_FILES['aa']['tmp_name'])){
	 move_uploaded_file($_FILES['aa']['tmp_name'], "./".iconv("UTF-8", "GBK", $_FILES['aa']['name'])); 
	 echo '1'; 
}
?>
```  

##### XMLhttpReuest.js
```
function ajaxFunction() {
    var xmlHttp;
    try { 
    // Firefox, Opera 8.0+, Safari 
    xmlHttp=new XMLHttpRequest();
     } catch (e) {
      // Internet Explorer 
      try { 
      	xmlHttp=new ActiveXObject("Msxml2.XMLHTTP"); 
      } catch (e) { 
      	try { 
      		xmlHttp=new ActiveXObject("Microsoft.XMLHTTP"); 
      	} catch (e) { 
      		alert("您的浏览器不支持AJAX！"); return false; 
      	} 
      } 
  } 
  return xmlHttp; 
}
```