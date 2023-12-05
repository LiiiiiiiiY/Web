# 多媒体元素

## 视频：video：
`<video src="路径"></video>` 
**视频格式要求：通常就用mp4、webm(后续兼容性再详谈)**


默认情况下一些限制，通过添加属性的方式改变原始样式：
- **视频尺寸定义：**`style="width: 800px;"`
- **视频控件直接显示：**`controls="controls"` 或 `controls`
- **进入网页自动播放：**`autoplay="autoplay"` 或 `autoplay`
- **视频静音播放：**`muted="muted"` 或 `muted`
- **视频循环播放：**`loop="loop"` 或 `loop`
    > 注：某些属性只有写和不写这两种状态，如果要写取值为属性名，这种属性叫布尔属性


## 音频：audio
`<audio src="./岁月如歌.mp3"></audio>`
**音频格式要求：通常就用mp3、wav、ogg、flac等**


其他的操作和video相同
 
## 兼容性：
 1. 旧版本的浏览器不支持这两个元素
 2. 不同的浏览器支持的音频、视频格式可能不一致，所以需要兼容性处理
```html
<video controls style="width: 500px;">
    <source src="./线性表.mp4">
    <source src="./线性表.webm">
    <p>对不起，你的浏览器不支持video播放，请更新浏览器</p>
</video>
```
注：浏览器会自动选择第一个支持的格式，如果都不支持就显示`<p>`标签中的内容