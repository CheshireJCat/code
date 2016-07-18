## JS实现图片上传之前先预览  

<input type="file" id="fileid" name="photofile" onchange="preImg(this.id,'imgid');" />
<div id="preview" style="filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(sizingMethod=scale);"></div>

```
<!DOCTYPE html>
<html lang="en">
<head id="Head1" runat="server">
    <title>JS实现图片上传之前先预览</title>
    <script type="text/javascript">
    function getPath(obj) {
        if (obj) {
            if (window.navigator.userAgent.indexOf("MSIE") >= 1) {
                obj.select();
                return document.selection.createRange().text;
            }
            //firefox 
            else if (window.navigator.userAgent.indexOf("Firefox") >= 1) {
                if (obj.files) {
                    return obj.files.item(0).getAsDataURL();
                }
                return obj.value;
            }
            return obj.value;
        }
    }

    function previewPhoto() {
        var picsrc = getPath(document.all.fileid);
        var picpreview = document.getElementById("preview");
        if (!picsrc) {
            return
        }
        if (window.navigator.userAgent.indexOf("MSIE") >= 1) {
            if (picpreview) {
                try {
                    picpreview.filters.item("DXImageTransform.Microsoft.AlphaImageLoader").src = picsrc;
                } catch (ex) {
                    alert("文件路径非法，请重新选择！");
                    return false;
                }
            } else {
                picpreview.innerHTML = "<img src='" + picsrc + "' />";
            }
        }
    }

    function preImg(fileid, imgid) {
        if (typeof FileReader == 'undefined') {
            var picsrc = getPath(document.all.fileid);
            document.getElementById('imgid').setAttribute('src',picsrc);
            previewPhoto();
        } else {
            var reader = new FileReader();
            var name = document.getElementById("fileid").value;
            var picpreview = document.getElementById("preview");
            reader.onload = function(e) {
                var img = document.getElementById(imgid);
                picpreview.innerHTML = "<img src='" + this.result + "' />";
            }
            reader.readAsDataURL(document.getElementById(fileid).files[0]);
        }
    }
    </script>
</head>
<body>
    <input type="file" id="fileid" name="photofile" onchange="preImg(this.id,'imgid');" />
    <div id="preview" style="filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(sizingMethod=scale);"></div>
</body>
</html>
```  

<script type="text/javascript">
    function getPath(obj) {
        if (obj) {
            if (window.navigator.userAgent.indexOf("MSIE") >= 1) {
                obj.select();
                return document.selection.createRange().text;
            }
            //firefox 
            else if (window.navigator.userAgent.indexOf("Firefox") >= 1) {
                if (obj.files) {
                    return obj.files.item(0).getAsDataURL();
                }
                return obj.value;
            }
            return obj.value;
        }
    }

    function previewPhoto() {
        var picsrc = getPath(document.all.fileid);
        var picpreview = document.getElementById("preview");
        if (!picsrc) {
            return
        }
        if (window.navigator.userAgent.indexOf("MSIE") >= 1) {
            if (picpreview) {
                try {
                    picpreview.filters.item("DXImageTransform.Microsoft.AlphaImageLoader").src = picsrc;
                } catch (ex) {
                    alert("文件路径非法，请重新选择！");
                    return false;
                }
            } else {
                picpreview.innerHTML = "<img src='" + picsrc + "' />";
            }
        }
    }

    function preImg(fileid, imgid) {
        if (typeof FileReader == 'undefined') {
            var picsrc = getPath(document.all.fileid);
            document.getElementById('imgid').setAttribute('src',picsrc);
            previewPhoto();
        } else {
            var reader = new FileReader();
            var name = document.getElementById("fileid").value;
            var picpreview = document.getElementById("preview");
            reader.onload = function(e) {
                var img = document.getElementById(imgid);
                picpreview.innerHTML = "<img src='" + this.result + "' />";
            }
            reader.readAsDataURL(document.getElementById(fileid).files[0]);
        }
    }
    </script>
