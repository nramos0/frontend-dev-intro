# 15 - HTML的id、CSS类，选择器和JS脚本

## HTML的唯一编号：id标签属性
- 在HTML/13里有介绍HTML标签的id属性，也就是标签的可选唯一编号
- 通过id标签属性，可以给标签指定编号，以便于通过该编号访问对应的一个HTML元素
- 编号可以作为CSS选择器，语法为`#{id}`，其中`{id}`应写要选择的HTML元素的编号
  - 对于编号为`myTable`的表格元素，可以使用`#myTable`选择器对其应用CSS样式表语句
- 也可以用它在之后要学的里访问对应的HTML元素并对元素做某些操作
- 必须选一个在本HTML文件里唯一的编号
- 编号至少必须包含一个字母，不能包含空格


例子：定义标签的编号属性，编号为myFavoriteAnimals的段落标签
```html
<p id="myFavoriteAnimals">
   狗、猫、乌龟
</p>
```

例子：使用编号作为CSS选择器
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            #myHeader {
                background-color: lightblue;
                color: black;
                padding: 40px;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <h1 id="myHeader">My Header</h1>
    </body>
</html>
```

## CSS的类
- CSS里，可以定义一个有名字的`CSS类`和对应的一些样式属性
- 通过类的类名，可以在不同的元素里使用同一组样式
- 比如，要在一个网站上的部分段落标签使用统一的样式，可以定义一个类，并在这几个段落标签里使用该类
- 为了定义标签要使用的类，可以使用`class`标签属性
  - class属性里可以写一个类名，也可以写多个使用空格分开的类名
- 在CSS定义类，要为该类写一个选择使用该类名的元素的选择器，使用`.{类名}`的格式写类名选择器表达式
  - 比如要定义一个城市CSS类city，选择器应该写成`.city`

例子：类的定义
```css
.city {
    background-color: orange;
    color: white;
    padding: 10px;
}
```
注：通过class标签属性使用该类的全部HTML元素会获得这些样式（即background-color为orange、text-color为white、padding为10px）

例子：类的使用
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            .city {
                background-color: tomato;
                color: white;
                padding: 10px;
            }
        </style>
    </head>
    <body>
        <h2 class="city">伦敦</h2>
        <p>伦敦是英国的首都。</p>

        <h2 class="city">巴黎</h2>
        <p>巴黎是法国的首都。</p>

        <h2 class="city">东京</h2>
        <p>东京是日本的首都。</p>
    </body>
</html>
```

例子：同时使用编号和类
```html
<!DOCTYPE html>
<html>
    <head>
        <style>
            #myHeader {
                background-color: lightblue;
                color: black;
                padding: 40px;
                text-align: center;
            }

            .city {
                background-color: tomato;
                color: white;
                padding: 10px;
                margin-bottom: 200px;
            }
        </style>
    </head>
    <body>
        <!-- 含有唯一编号的元素 -->
        <h1 id="myHeader">My Cities</h1>

        <!-- 使用同一类的多个元素 -->
        <h2 class="city">伦敦</h2>
        <p>伦敦是英国的首都。</p>

        <h2 class="city">巴黎</h2>
        <p>巴黎是法国的首都。</p>

        <h2 class="city">东京</h2>
        <p>东京是日本的首都。</p>
    </body>
</html>
```

## 编号的应：网页书签
- 可以通过编号和链接标签来提供这么一个功能：从网页某个地方跳到王爷的另外一个地方的
- 做法如下：
  - 定义一个使用编号标签属性的标签（书签标签）
  - 定义一个链接标签，href属性为该书签标签的id选择器表达式

例子
```html
<h2 id="C4">第四章</h2>
<!-- ...其他内容... --->
<!-- ...其他内容... --->
<!-- ...其他内容... --->
<a href="#C4">返回第四章</a>
```

例子
```html
<span id="top"></span>
<!-- ...其他内容... --->
<!-- ...其他内容... --->
<!-- ...其他内容... --->
<a href="#top">返回到最上面</a>
```

## 脚本
- 可以使用JavaScript（JS）语言的脚本来对网页进行动态处理
- 可以使用脚本访问某个编号的元素并对该元素进行操作
- 类似的，也可以访问使用某个类的元素列表并对元素列表进行操作
- 内部脚本可以写在script（即脚本）标签里面
- 以下演示如何使用一个按钮修改一个h1标题标签的文本


```html
<!DOCTYPE html>
<html>
    <body>
        <h1 id="myHeader">你好,世界!</h1>
        <input type="button" value="修改文本" onclick="displayResult()" />

        <script>
            function displayResult() {
                document.getElementById("myHeader").innerHTML = "祝你一天愉快！";
            }
        </script>
    </body>
</html>
```

- 点击按钮时，编号为myHeader的标题元素里的文本会变成“祝你一天愉快！”
- 注意以下几点：
  - JS在script标签里可以写代码
  - 可以定义函数，并在HTML里使用函数
  - HTML代码里的按钮使用了onclick标签属性。通过此属性，可以在按钮被按时运行JS代码，在这里就是displayResult()函数的调用
  - JS可以通过document.getElementById()函数访问一个编号的对应元素
    - document是已经开始显示的HTML文档在浏览器里的数据结构表示
  - 通过getElementbyId()获得的HTML元素有一个innerHTML属性，该属性对应的是元素全部孩子的HTML代码表示，在此直接写了文本“祝你一天愉快！”
