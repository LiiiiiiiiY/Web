# 图片元素

## img元素
image的缩写，空元素

### 属性：
- src：图片路径
- alt：图片描述，当图片资源无法加载时，将使用该属性的文字替代图片

### 嵌套合作：
#### img与a联用：
```html
<a href="跳转地址">
    <img src="图片地址">
</a>
```

#### img与map联用：
通过这两个元素的联用，可以实现点击图片指定区域，跳转到指定区域
- map坐标的标准：图片左上角为坐标原点
    ```html
    <map>
    <area shape="形状选择" 
          coords="坐标" 
          href="跳转地址" 
          alt="图片加载失败时显示内容" 
          target="当前窗口(默认)和新建窗口(_black)选择">
    </map>
    ```

    - 圆形(`circle`)：`coords:` 圆心X坐标，圆心Y坐标，半径
    - 矩形(`rect`)：`coords:` 矩形左上角X坐标，矩形左上角Y坐标，矩形右下角X坐标，矩形右下角Y坐标
    - 多边形(`poly`):`coords:` X1，Y1，X2，Y2，X3，Y3...

#### img与iframe联用：
iframe通常用于把图片、图片标题、描述包裹起来，表示整个区域都跟图片有关联
```html
<iframe>
    <figcaption>标题</figcaption>
</iframe>
```