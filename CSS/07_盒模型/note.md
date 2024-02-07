# 盒模型

box：盒子，每个元素在页面中都会生成一个矩形区域（盒子）

## 盒子类型
1. **行盒(不换行)：** display等于inline的元素（元素是html的概念，盒子是css的概念）
2. **块盒(独占一行)：** display等于block的元素

## 浏览器默认的盒子类型
- **块盒：** `容器元素:div、header、aside` 等、`h1~h6` 、`p` 等
- **行盒：** `span` 、`a` 、`img` 、`video` 、`audio` 等

无论是行盒还是块盒，都由以下内容组成，**从内到外**分别是：
|名称|属性(属性值)|以快递为例|
|:--:|:--:|:--:|
|内容|`content` `width` `height`|手机|
|填充|`padding:top right bottom left`<br>`padding-left` `padding-right`<br>`padding-bottom` `padding-top`|包裹手机的泡沫|
|边框|`boder:widht style color`<br>`boder-style` `boder-widht`<br>`boder-color`|装手机的快递盒|
|外边距|`margin:top right bottom left`<br>`margin-top` `margin-right`<br>`margin-bottom` `margin-left`|快递盒与快递盒之间的距离|

- **内容：** 设置的是盒子内容的宽高。**内容部分**通常叫做整个盒子的内容盒`content-box`
- **填充：** 设置的是盒子内容与盒子边框之间的距离。**内容部分+填充部分**通常叫做整个盒子的填充盒`padding-box`
- **边框：** 设置的是盒子边框的宽度、样式和颜色。**内容部分+填充部分+边框部分**通常叫做整个盒子的边框盒`border-box`
- **外边距：** 设置的是盒子与盒子之间的距离。内容部分+填充部分+边框部分+外边距部分通常叫做整个盒子的外边距盒`margin-box`