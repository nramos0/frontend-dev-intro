# 13 - HTML的表单(1)

## 表单
- HTML里也支持获取用户输入的表单
- HTML表单用表单标签定义，标签名为form
- 表单里一般可以包含输入框、单选按钮、多选按钮、提交按钮或其他可点击的按钮，这些都可以使用加了不同的类型标签属性type的输入标签定义，标签名为input
- 提交表单必须使用提交按钮实现
  - 提交表单时，浏览器会开始创建一个表单输入字典，每个输入元素要获取的信息的名称（之后均称为“输入信息名称”或“信息名称”）作为键，该信息名称的真实值（之后均称为“信息值”）作为对应的键值。浏览器会读取表单里每个输入元素的信息来创建该字典，一个元素对应一个字典项。
  - 比如，“姓名”作为要获取的信息的名称，即是键，“张三”作为对应的真实姓名值，即是键值（也可以显示为映射的形式：姓名-->张三）
  - 注：有固定选项的输入元素（单选按钮、多选按钮等）需要给每个可选选项定义一个信息值。选择该选项并提交表单时，提交的对应信息名称的真实值是该选项的信息值。没有固定选项的输入元素（输入框等）的信息值就是用户输入的文本

例子：表单的提交
表单包含以下三个输入元素
- 姓名输入框，信息名称为"name"
- 性别单选按钮，信息名称为"gender"
  - 可选性别为
    - 男，信息值为male
    - 女，信息值为female
    - 其他，信息值为other
- 电话号码输入框，信息名称为"phoneNumber"
假设用户输入的信息如下
- 姓名为张三
- 性别为男
- 电话号码为10086

则提交表单的时候创建的字典为
name --> 张三
gender --> male
phoneNumber --> 10086

注意：虽然用户选择了“男”的性别单选按钮，但是“男”这个单选按钮的信息值是male，所以提交表单的时候，对应gender信息名称的信息值就是male，而对于姓名输入框和电话号码输入框，因为两者是输入框，信息值就是用户输入的值，即“张三”和“10086”


例子：表单标签的使用
```html
<form>
    <!-- 表单元素 --->
</form>
```

## 输入标签
- 输入标签标签名为input
- 可以使用类型标签属性type定义输入标签的类型
  - text （单行输入框）
  - radio （单选按钮）
  - checkbox （多选按钮）
  - submit （提交按钮）
  - button （普通按钮）
- 输入标签可以使用id标签属性定义自己的唯一标签编号
- 输入标签的信息名称使用信息名称标签属性name来定义
- 对于有固定选项的输入标签类型（单选按钮、多选按钮），也需要定义信息值，使用信息值标签属性value来定义

## 标注标签
- 通常需要在一个输入框或其他的输入控件上为用户显示要输入什么，这个使用标注标签来实现，标签名为label
- 为了使得浏览器更好地操作我们写的表单，必须给每个标注标签绑定它对应的输入元素
- 标注标签里可以使用绑定属性for绑定对应的输入标签，使用输入标签的编号id进行绑定，即标注标签里的for属性应该为要绑定的输入标签的编号


## 输入框
- 输入框可以使用type标签属性为text（文本）的输入标签

例子
```html
<form>
    <label for="name">姓名</label><br />
    <input type="text" id="name" name="name"><br />
    <label for="age">年龄</label><br />
    <input type="text" id="age" name="age">
</form>
```

## 单选按钮
- 单选按钮可以使用type标签属性为radio（单选按钮）的输入标签

例子
```html
<form>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">男</label><br>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">女</label><br>
    <input type="radio" id="other" name="gender" value="other">
    <label for="other">其他</label>
</form>
```

## 多选按钮
- 多选按钮可以使用type标签属性为checkbox（多选按钮）的输入标签

例子
```html
<form>
    <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
    <label for="vehicle1"> 我有自行车</label><br>
    <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
    <label for="vehicle2"> 我有汽车</label><br>
    <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
    <label for="vehicle3"> 我有船</label>
</form>
```

## 提交按钮
- 提交按钮可以使用type标签属性为submit（提交）的输入标签
- 通常使用action标签属性定义提交完应该做什么，在此先不进入这些内容的学习

```html
<form action="...">
    <label for="name">姓名</label><br />
    <input type="text" id="name" name="name"><br />
    <label for="age">年龄</label><br />
    <input type="text" id="age" name="age"><br><br>
    <input type="submit" value="提交" />
</form>
```