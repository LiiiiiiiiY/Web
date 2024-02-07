# 盒模型应用

## 改变宽高范围

默认情况下，`width`和`height`属性只作用于内容盒，当要解决衡量尺寸与实际尺寸不符时：
1. 可以使用精确计算解决。
2. 使用CSS3中的`box-sizing`属性，它可以设置`width`和`height`属性作用域。

### `box-sizeing` 中有两个属性：
   1. `content-box`：默认值，表示只计算**内容盒**的宽高范围
```css
#ContentBox {
   width: 236px;
   height: 51px;
   color: white;
   background-color: #2d2e36;
   line-height: 51px;
   padding-left: 46px;
}
```
![](./img/borderBox.png)

   2. `border-box`：边框盒，表示计算整个盒子的宽高范围
```css
#BorderBox{
   width: 236px;
   height: 51px;
   color: white;
   background-color: hsl(233, 9%, 19%);
   line-height: 51px;
   padding-left: 46px;
   box-sizing: border-box;
}
```
![](./img/contentBox.png)

## 改变背景覆盖范围
默认情况下背景覆盖边框盒，可以通过`background-clip`属性来改变。

### `background-clip` 中有三个属性：
   1. `border-box`：表示只覆盖边框盒
   2. `padding-box`：表示只覆盖内边距盒
   3. `content-box`：表示只覆盖内容盒(默认)

## 溢出处理

当文字内容超过盒模型的边框时，就称为溢出，可以通过`overflow`属性来处理。
### `overflow` 中有四个属性：
   1. `visible`：默认值，表示内容溢出时显示出来
   2. `hidden`：表示内容溢出时隐藏起来
   3. `scroll`：表示内容溢出时显示滚动，但不溢出时仍然显示滚动
   4. `auto`：表示内容溢出时自动显示滚动，不溢出时不显示滚动

## 段词规则

当行的某个字词内容超过盒模型的边框时，会自动换行，可以通过`word-break`属性来设置。

### `word-break` 中有三个属性：
   1. `normal`：默认值。CJK字符（文字位置截断），非CJK字符（单词位置截断）
   2. `break-all`：截断所有。所有字符都在文字处阶段，非CJK字符不会按照单词截断
   3. `keep-all`：保持所有。所有字符都在空格和标点符号处阶段，CJK字符不会按照文字截断，即一行显示所有

## 空白处理

当文字内容超过盒模型的宽度时，可以通过`white-space`属性来设置。
### `white-space` 中有三个常见属性：
   1. `normal`：默认值，空白折叠。即连续的空白符会被合并，换行符会被当作空白符
   2. `nowrap`：空白折叠但不换行。连续的空白符会被合并，但是换行符不会当作空白符
   3. `pre`：不会折叠空白符。连续的空白符会被保留，但是换行符不会当作空白符

当文字内容超过盒模型的宽度时，想要将多余部分用`...`来表示，可以通过`text-overflow`属性来设置。
### `text-overflow` 属性：
   1. `clip`：默认值，表示不显示省略号
   2. `ellipsis`：表示显示省略号