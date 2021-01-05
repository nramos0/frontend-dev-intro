# 7 - HTML的样式（1）

HTML/6里介绍过简单的样式，这里介绍更多常用的样式属性。

## 标签的样式属性（回顾）
- 几乎所有的标签可以添加一个样式属性，属性名为style
- 样式属性可以改变标签是怎么显示的，比如字体、大小、颜色等
- 样式属性里面可以写样式列表。样式列表里的每个元素是以这种形式来写的：`样式属性: 样式值;`。注意是`英文`冒号和分号。
- 以下是使用样式属性把一个一般的段落标签用红色显示

例子
```html
<p style="color: red;">这是一个红色的段落</p>
```

也可以添加多个样式，但要都放在一个样式列表里。这个例子使用了颜色、字体大小两个样式属性：
```html
<p style="color: blue; font-size: 30px;">这是一个蓝色的段落</p>
```

## 字体大小样式属性
- 字体大小样式属性可以改变标签里的文本的字体大小，样式属性为font-size
- 字体大小属性可以用多个单位，目前只介绍像素(px)单位和百分之单位(%)的使用。在某个数字后加px单位或百分号单位就可以了
  - 百分之单位会根据当前页面的默认字体大小，乘以给定的值

例子
```html
<p style="font-size: 50px;">文本</p>
```

```html
<p style="font-size: 120%;">文本</p>
```

## 字体颜色样式属性
- 字体颜色样式属性可以改变标签里的文本的字体颜色，样式属性为color
- 字体颜色和其他的颜色属性可以以多种方法表示颜色
  - 英文单词（red、blue、purple等，不是很灵活，但简单）
  - 十六进制码（如#994205、#FFFFFF）
  - RGB码（如rgb(255, 0, 0）来表示有255红色，0绿色，0蓝色的颜色）

例子
```html
<p style="color: #A9F391;">文本</p>
```

```html
<p style="color: red;">文本</p>
```

```html
<p style="color: rgb(243, 33, 150);">文本</p>
```

## 背景颜色样式属性
- 背景颜色样式属性可以改变标签的背景颜色，样式属性为background-color
- 颜色的表示方法和字体颜色样式属性一致

例子
```html
<p style="background-color: #A9F391;">文本</p>
```

```html
<p style="background-color: red;">文本</p>
```

```html
<p style="background-color: rgb(243, 33, 150);">文本</p>
```

```html
<h1 style="background-color: powderblue;">这是一个标题标签</h1>
<p style="background-color: tomato;">这是一个段落标签</p>
```

## 字体类型样式属性
- 字体类型样式属性可以改变标签里文本的字体类型，样式属性为font-family
- 支持的属性值可以在网上查

例子
```html
<h1 style="font-family: verdana;">这是一个标题标签</h1>
<p style="font-family: courier;">这是一个段落标签</p>
```

## 文本对齐样式属性
- 文本对齐样式属性可以改变标签里文本的默认位置，样式属性为text-align（text alignment）
- 一般使用left（左对齐）、right（右对齐）、center（居中对齐）、justify（两端对齐）

例子
```html
<h1 style="text-align: center;">居中标题标签</h1>
<p style="text-align: right;">右对齐段落标签</p>
```