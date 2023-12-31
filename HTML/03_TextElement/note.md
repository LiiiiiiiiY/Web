# 文本元素

HTEML中支持的元素：HTML5元素周期表

## 1、标题：
h1~h6分别表示一级到六级的标题，通过`h$*6>{$级标题}`缩写可以快捷生成以下代码生成，主要是作为测试用的
```html
<h1>1级标题</h1>
<h2>2级标题</h2>
<h3>3级标题</h3>
<h4>4级标题</h4>
<h5>5级标题</h5>
<h6>6级标题</h6>
```
****

## 2、段落：

下面这一段是一个乱数假文，没有任何实际含义的文字，是通过 lorem 快捷键随机生成的
- Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur dignissimos tempora illo, similique minima saepe odit quo illum? Perferendis, ratione nostrum! Tenetur placeat harum aspernatur ipsum laborum veniam facere nobis!

如果想生成多行乱数假文，可以通过 `p*6>lorem` 快捷键快速生成
如果再lorem后面加上数字，代表生成的假文长度，默认长度是100

****

## 3、无语义的元素：
- **span ：大部分的用于设置没有语义元素的样式**
 某些元素在显示时会独占一行，但有些不会。以前独占一行的叫 `块级元素` ，没有独占一行的叫 `行级元素` (H5中这个说法弃用了，因为元素只代表该内容的含义，跟显示效果无关)。

 ****


## 4、预格式化文本元素：
- 空白折叠：在源代码中的连续空白字符（空格、换行、回车），在显示时会被折叠为一个空格
- 而使用 `<pre></pre>` 元素会保留空格和换行，不会被折叠，该元素在实际应用中主要显示代码
pre元素功能的本质实际上有一个默认的CSS属性：`white-space: pre`
- 本质上pre是一个无语义元素，因为要让浏览器识别到内容是代码，一般通过 `<code></code>` 元素表示代码区域

****

## 5、实体
实体(Entity)也叫实体字符，通常用于在页面中显示一些特殊符号。
比如想在页面上显示 `<p>` ，就不能直接写&lt;p&gt;。

方式一：以`&`开头，以`;`结尾，中间是元素的单词缩写。
方式二：以`&#`开头，以`;`结尾，中间是元素对应的数值码。

|字符名称|实体字符|对应的单词缩写|对应的数值码|
|:---:|:---:|:---:|:---:|
|小于|&lt;|`&lt;`|`&#60;`|
|大于|&gt;|`&gt;`|`&#62;`|
|与|&amp;|`&amp;`|`&#38;`|
|空格|&nbsp;|`&nbsp;`|`&#160;`|
|版权符号|&copy;|`&copy;`|`&#169;`|