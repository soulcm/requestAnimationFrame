# requestAnimationFrame
requestAnimationFrame作用与setTimeInterval类似，但是它会根据浏览器的刷新频率自动调整动画的时间间隔。

requestAnimationFrame兼容处理如下
```
if (!window.requestAnimationFrame) {
    window.requestAnimationFrame = (window.webkitRequestAnimationFrame ||
        window.mozRequestAnimationFrame ||
        window.oRequestAnimationFrame ||
        window.msRequestAnimationFrame ||
        function (callback) {
            return window.setTimeout(callback, 1000 / 60);
        });

}
```
