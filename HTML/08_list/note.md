# 列表元素

## 有序列表
- `ol`：order list
- `li`：list
```html
<ol>
    <li>打开冰箱</li>
    <li>把大象装进去</li>
    <li>关上冰箱</li>
</ol>
```
- **`type` 属性：** 设置列表的类型，可选值有
    - `1` 表示数字编号排序
    - `a` 表示小写字母编号排序
    - `A` 表示大写字母编号排序
    - `i` 表示小写罗马数字编号排序
    - `I` 表示大写罗马数字编号排序
> 注：因为显示效果是CSS的工作，除非内容有很强的序号逻辑，比如法律条文或者技术文档，**否则不建议使用列表排序**。建议使用CSS `list-style-type` 属性替代。

## 无序列表
- `ul`：unorder list
- `li`：list
```html
<ul><
    <li>打开冰箱</li>
    <li>把大象装进去</li>
    <li>关上冰箱</li>
</ul>
```
- 无序列表一般用于制作菜单、导航栏、新闻列表等

## 定义列表
- `dl`：definition list
- `dt`：definition title
- `dd`：definition description
```html
<dl>
    <dt>HTML</dt>
    <dd>超文本标记语言...</dd>
</dl>
```

## nav元素
H5的新元素，语义就是导航，是一个容器元素。仅仅用于导航栏使用。
```html
<nav>
    <a href="">首页</a>
    <a href="">国内</a>
    <a href="">国际</a>
    <a href="">军事</a>
    <a href="">财经</a>
</nav>
```