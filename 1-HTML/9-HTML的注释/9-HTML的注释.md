# 9 - HTML的注释

## 什么是注释？
- 在大部分程序设计语言中，支持在代码里写注释
- 注释就是对代码的解释。有时候一部分代码对读者一开始看可能不是很容易理解。使用注释可以对代码进行文字的解释
- 一般来讲，如果别人看你的代码不能很快就知道你为什么是那么写的，则使用注释对代码进行更多的解释是很好的习惯

## HTML注释的语法
- HTML的注释使用`<!--`表示注释的开始。可以认为是注释的“开口标签”，而`-->`表示注释的结束，也相当于注释的“结束标签”
- 注释可以跨行
- 注释可以写任何东西，包括HTML代码。有时候暂时把一部分代码注释掉可以更方便地进行调试
- 注释通常也用于把代码分成若干个模块，方便代码更容易读
- 注意注释不用解释代码是做什么的，其他的开发者应该清楚语言的语法。只要在代码在做什么至少有些不清楚，或者它为什么是那样做的不清楚的情况下，才有必要写注释

例子
```html
<!-- 这是一个注释，可以方便地进行代码的解释-->
<h1>标题标题标题</h1>
<p>段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落</p>
```

```html
<!-- 注释可以跨行
    
这里也可以写字
-->
```

```html
<!-- 
    注释也可以写代码
    
    <h3>隐藏的h3标题</h3>
-->
```

下面是HTML/8里style2.html的代码，但加了一些注释。
```html
<!DOCTYPE html>
<!-- 本网站只支持中文 --->
<html lang="zh">
    <head>
        <title>标签的样式（2）</title>
    </head>
    <body>
        <!-- 高度和宽度的使用 --->
        <h3>高度为600px，宽度为800px的段落</h3>
        <!-- 
            为了方便用户看到高度和宽度样式属性起的作用，
            设置了背景颜色为黑色，字体颜色为白色，这样
            这个段落元素的背景颜色不会和body的默认背景
            颜色一致，用户可以容易看出它的真实大小
        --->
        <p
            style="
                height: 600px;
                width: 800px;
                background-color: black;
                color: white;
            "
        >
            段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落段落
        </p>

        <!-- 边距的使用 --->
        <h3>两个段落，使用了下侧边距把它们之间的距离拉大</h3>
        <div>
            <p style="margin-bottom: 50px">
                上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。上面的段落。
            </p>
            <p style="color: red">
                下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。下面的段落。
            </p>
        </div>

        <br />

        <!-- 边框的使用 --->
        <h3>含有大小为5px的橙色边框的h3标题</h3>
        <h3 style="border: 5px solid orange">标题标题标题</h3>

        <br />

        <!-- 边框和填充的使用 --->
        <h3>
            有20px的填充和薄绿色边框的块级容器，里面有描述北京市的h2标题和p段落
        </h3>
        <div
            style="
                background-color: black;
                color: white;
                padding: 20px;
                border: thin solid green;
            "
        >
            <h2>北京</h2>
            <p>北京是中国的首都，人口为2154万人。</p>
        </div>

        <br />

        <!-- 边框、填充、高度、宽度在块级容器的使用 --->
        <h3>另一个块级容器例子</h3>
        <div
            style="
                background-color: rgb(200, 0, 0);
                color: #222222;
                text-align: justify;
                padding: 15px;
                border: thin solid rgb(150, 0, 0);
                height: 300px;
                width: 500px;
            "
        >
            <h3>文本文本文本文本文本文本文本</h3>
            <p>
                文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本文本
            </p>
        </div>
          
        <br />

        <!-- 高度和宽度在图像标签的使用 -->
        <h3>使用了宽度和高度样式属性的图像</h3>
        <img src="assets/cat.png" style="width: 600px; height: 300px;" alt="猫" />
    </body>
</html>

```