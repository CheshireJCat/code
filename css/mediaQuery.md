## 移动设备的 CSS3 Media Query
##### 常用
```
@media only screen and (min-device-width: 320px) and (max-device-width: 480px){}
@media (max-width: 450px){}
@media (max-width: 650px){}
@media (max-width: 800px){}
```
##### 所有	

#####iPhone 4/4s landscape & portrait
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px)
and (-webkit-device-pixel-ratio: 2)
and (device-aspect-ratio: 2/3) {}
```
#####iPhone 4/4s portrait
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px)
and (-webkit-device-pixel-ratio: 2)
and (device-aspect-ratio: 2/3)
and (orientation:portrait)  {}
```
#####iPhone 4/4s landscape
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 480px)
and (-webkit-device-pixel-ratio: 2)
and (device-aspect-ratio: 2/3)
and (orientation:landscape) {}
```
##### iPhone 5/5s landscape & portrait
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px)
and (-webkit-min-device-pixel-ratio: 2) {}
```
##### iPhone 5/5s portrait
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px)
and (-webkit-min-device-pixel-ratio: 2)
and (orientation: portrait) {}
```
##### iPhone 5/5s landscape
```
@media only screen
and (min-device-width: 320px)
and (max-device-width: 568px)
and (-webkit-min-device-pixel-ratio: 2)
and (orientation: landscape) {}
```
##### iPhone 5/5s landscape & portrait
```
@media only screen
and (min-device-width: 414px)
and (max-device-width: 736px)
and (-webkit-min-device-pixel-ratio: 3) {}
```
##### iPhone 5/5s portrait
```
@media only screen
and (min-device-width: 414px)
and (max-device-width: 736px)
and (-webkit-min-device-pixel-ratio: 3)
and (orientation: portrait) {}
```
##### iPhone 5/5s landscape
```
@media only screen
and (min-device-width: 414px)
and (max-device-width: 736px)
and (-webkit-min-device-pixel-ratio: 3)
and (orientation: landscape) {}

@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (orientation : portrait) { 
    //iPhone 6 Portrait
}


@media only screen and (min-device-width: 375px) and (max-device-width: 667px) and (orientation : landscape) { 
    //iPhone 6 landscape
}


@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (orientation : portrait) { 
    //iPhone 6+ Portrait
}


@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (orientation : landscape) { 
    //iPhone 6+ landscape
}

@media only screen and (max-device-width: 640px), only screen and (max-device-width: 667px), only screen and (max-width: 480px){ 
    //iPhone 6 and iPhone 6+ portrait and landscape
}

@media only screen and (max-device-width: 640px), only screen and (max-device-width: 667px), only screen and (max-width: 480px) and (orientation : portrait){ 
    //iPhone 6 and iPhone 6+ portrait
}

@media only screen and (max-device-width: 640px), 
only screen and (max-device-width: 667px), 
only screen and (max-width: 480px) 
and (orientation : landscape){ 
    //iPhone 6 and iPhone 6+ landscape
}
```  

##### Galaxy S3 landscape & portrait
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 2) {

}
```
##### Galaxy S3 portrait
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 2)
and (orientation: portrait) {

}
```
##### Galaxy S3 landscape
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 2)
and (orientation: landscape) {

}
```
##### Galaxy S4 landscape & portrait
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3) {

}
```
##### Galaxy S4 portrait
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: portrait) {

}
```
##### Galaxy S4 landscape
```
@media screen
and (device-width: 320px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: landscape) {

}
```
##### Galaxy S5 landscape & portrait
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3) {

}
```
##### Galaxy S4 portrait
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: portrait) {

}
```
##### Galaxy S4 landscape
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: landscape) {

}
```
##### HTC One landscape & portrait
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3) {

}
```
##### HTC One portrait
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: portrait) {

}
```
##### HTC One landscape
```
@media screen
and (device-width: 360px)
and (device-height: 640px)
and (-webkit-device-pixel-ratio: 3)
and (orientation: landscape) {

}

```
##### iPad Mini landscape & portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad Mini portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: portrait)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad Mini landscape
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: landscape)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad 1/2 landscape & portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad 1/2 portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: portrait)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad 1/2 landscape
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: landscape)
and (-webkit-min-device-pixel-ratio: 1) {

}
```
##### iPad 3/4 landscape & portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (-webkit-min-device-pixel-ratio: 2) {

}
```
##### iPad 3/4 portrait
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: portrait)
and (-webkit-min-device-pixel-ratio: 2) {

}
```
##### iPad 3/4 landscape
```
@media only screen
and (min-device-width: 768px)
and (max-device-width: 1024px)
and (orientation: landscape)
and (-webkit-min-device-pixel-ratio: 2) {

}
```
##### Galaxy Tab 10.1 landscape & portrait
```
@media
(min-device-width: 800px)
and (max-device-width: 1280px) {

}
```
##### Galaxy Tab 10.1 portrait
```
@media
(max-device-width: 800px)
and (orientation: portrait) {

}
```
##### Galaxy Tab 10.1 landscape
```
@media
(max-device-width: 1280px)
and (orientation: landscape) {

}
```
##### Asus Nexus 7 landscape & portrait
```
@media screen
and (device-width: 601px)
and (device-height: 906px)
and (-webkit-min-device-pixel-ratio: 1.331)
and (-webkit-max-device-pixel-ratio: 1.332) {

}
```
##### Asus Nexus 7 portrait
```
@media screen
and (device-width: 601px)
and (device-height: 906px)
and (-webkit-min-device-pixel-ratio: 1.331)
and (-webkit-max-device-pixel-ratio: 1.332)
and (orientation: portrait) {

}
```
##### Asus Nexus 7 landscape
```
@media screen
and (device-width: 601px)
and (device-height: 906px)
and (-webkit-min-device-pixel-ratio: 1.331)
and (-webkit-max-device-pixel-ratio: 1.332)
and (orientation: landscape) {

}
```
##### Kindle Fire HD 7" landscape & portrait
```
@media only screen
and (min-device-width: 800px)
and (max-device-width: 1280px)
and (-webkit-min-device-pixel-ratio: 1.5) {

}
```
##### Kindle Fire HD 7" portrait
```
@media only screen
and (min-device-width: 800px)
and (max-device-width: 1280px)
and (-webkit-min-device-pixel-ratio: 1.5)
and (orientation: portrait) {
}
```
##### Kindle Fire HD 7" landscape
```
@media only screen
and (min-device-width: 800px)
and (max-device-width: 1280px)
and (-webkit-min-device-pixel-ratio: 1.5)
and (orientation: landscape) {

}
```
##### Kindle Fire HD 8.9" landscape & portrait
```
@media only screen
and (min-device-width: 1200px)
and (max-device-width: 1600px)
and (-webkit-min-device-pixel-ratio: 1.5) {

}
```
##### Kindle Fire HD 8.9" portrait
```
@media only screen
and (min-device-width: 1200px)
and (max-device-width: 1600px)
and (-webkit-min-device-pixel-ratio: 1.5)
and (orientation: portrait) {
}
```
##### Kindle Fire HD 8.9" landscape
```
@media only screen
and (min-device-width: 1200px)
and (max-device-width: 1600px)
and (-webkit-min-device-pixel-ratio: 1.5)
and (orientation: landscape) {

}
```
##### Non-Retina Screens
```
@media screen
and (min-device-width: 1200px)
and (max-device-width: 1600px)
and (-webkit-min-device-pixel-ratio: 1) {
}
```
##### Retina Screens
```
@media screen
and (min-device-width: 1200px)
and (max-device-width: 1600px)
and (-webkit-min-device-pixel-ratio: 2)
and (min-resolution: 192dpi) {
}
```
##### Apple Watch
```
@media
(max-device-width: 42mm)
and (min-device-width: 38mm) {

}
```

##### Moto 360 Watch
```
@media
(max-device-width: 218px)
and (max-device-height: 281px) {

}
```