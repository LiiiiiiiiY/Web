# 为网页添加样式

## 术语解释：
下面的整个代码叫 **CSS规则** ，CSS其实就是很多的规则组成的。
```css
h1{
    color:red;
    text-align: center;
}
```

### CSS规则：
CSS规则 = 选择器 + 声明块。
以上面代码为例：`h1`就是选择器。`color:red;` 和 `text-align: center;` 就是声明块。

#### 选择器：选择样式的应用范围
- 元素选择器：**作用范围为**当前页面所有元素（选中范围太广）
- ID选择器：**作用范围为**当前页面ID为xxx的元素（选中范围太窄）
- 类选择器：**作用范围为**当前页面包含class的元素（常用）。在元素中的class属性中添加class名来选中元素，一个元素可以添加多个class名。
    ```css
    .big{
        font-size: 3em;
        text-align: center;
    }
    ```
    ```html
    <h2 class="big red">这是二级标题</h2>
    ```

#### 声明块：样式的具体内容
CSS规则中`{` `}`内部的属性就是**声明块**，声明块中包含很多声明（属性），每一个属性表达了CSS某一方面的样式

## CSS代码书写的位置

#### 内部样式表
在`<head>`中添加`<style>`标签，在`<style>`标签中书写CSS代码。

#### 内联样式表 [不推荐]
在元素中添加`style`属性，在`style`属性中书写CSS代码。

#### 外部样式表 [推荐]
在样式书写到独立的CSS文件夹中。在HTML中通过 `<link>` 元素加载CSS文件
1. 目的是为了解决多个页面使用同一套样式的问题。
2. 有利于浏览器缓存，从而提高网页的加载速度（当浏览器加载过同一个CSS文件，则使用加载缓存，即不会再次加载相同的CSS文件，提高网页的加载速度）。
3. 分离样式和HTML代码，有利于代码的阅读和网页的维护。