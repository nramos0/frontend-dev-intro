# 12 - HTML的表格

## 表格
- HTML里也支持显示表格信息
- HTML表格的定义方式如下：
  - 定义表格
  - 定义表格的每一行
  - 在每一行里定义表格的格子
- 可以使用表格标签定义表格，标签名为table
- 表格里的每一行使用表格行标签来定义，标签名为tr（table row）
- 表格里的每一格子使用格子标签来定义，标签名为td（table data）
  - 格子里可以写任何东西，包括文本、图片、列表、其他的表格等
- 表格标题可以使用表格标题标签来定义，标签名为th（table heading）
  - 表格标题里的文本默认为粗体、居中文本

一个表格的例子如下

表格1
```html
<table style="width: 100%">
    <tr>
        <th>姓名</th>
        <th>性别</th>
        <th>年龄</th>
    </tr>
    <tr>
        <td>张三</td>
        <td>男</td>
        <td>20</td>
    </tr>
    <tr>
        <td>王二</td>
        <td>女</td>
        <td>22</td>
    </tr>
</table>
```

## 表格相关的一些样式属性

- 可以在内部样式表或外部样式表为表格定义边框
```css
table, th, td {
    border: 1px solid black;
}
```

- 也可以把这些边框折叠成一个边框
```css
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}
```

- 可以在格子里使用填充，以便于让格子更好看一些，更容易读里面的内容
```css
th, td {
    padding: 15px;
}
```

- 可以给表格标题的文本定义左对齐样式
```css
th {
    text-align: left;
}
```

- 可以在表格标签table里使用border-spacing样式属性来定义格子之间的距离
```css
table {
  border-spacing: 5px;
}
```

## 占用多列的格子
- 可以在格子标签里使用占用列数标签属性colspan（column span）来让一个格子占用多个列的空间
- 比如，colspan为2的格子会占用两列的格子空间

例子

表格2
```html
<table style="width: 100%;">
    <tr>
        <th>姓名</th>
        <th colspan="2">电话号码</th>
    </tr>
    <tr>
        <td>张三</td>
        <td>55577854</td>
        <td>55577855</td>
    </tr>
</table>
```

## 占用多行的格子
- 同样也可以在格子标签里使用占用行数标签属性rowspan（row span）来让一个格子占用多个行的空间
- 比如，rowspan为2的格子会占用两行的格子空间

例子
```html
<table style="width: 100%">
    <tr>
        <th>姓名:</th>
        <td>张三</td>
    </tr>
    <tr>
        <th rowspan="2">电话号码:</th>
        <td>55577854</td>
    </tr>
    <tr>
        <td>55577855</td>
    </tr>
</table>
```