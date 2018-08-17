#### 修改版本使用

```html
<div id="clipArea"></div>
<button id="clipBtn">裁剪</button>
```

```javascript
var clipArea = new bjj.PhotoClip("#clipArea", {
    size: [200, 200],
    outputSize: [200, 200],
    file: e.target.files[0],
    ok: "#clipBtn",
    loadStart: function() {
        console.log("照片读取中");
    },
    loadComplete: function() {
        console.log("照片读取完成");
    },
    clipFinish: function(dataURL) {
        $('#clipShow').fadeOut();
        that.uploadBase(dataURL);
    }
});
// 相对未修改版本只更改了file,这里传递一个type="file" 
```



