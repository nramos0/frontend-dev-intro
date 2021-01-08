# 13 - HTML的表单

## 表单
- HTML里也支持获取用户输入的表单
- HTML表单用表单标签定义，标签名为form
- 表单里一般可以包含输入框、单选按钮、多选按钮、提交按钮或其他可点击的按钮，这些都可以使用加了不同的类型标签属性type的输入标签定义，标签名为input


例子
```html
<form>
    <!-- 表单元素 --->
</form>
```

## 输入标签
- 输入标签标签名为input
- 可以使用类型标签属性type定义输入标签的类型
  - text （文本）
  - radio （单选按钮）
  - checkbox （多选按钮）
  - submit （提交按钮）
  - button （普通按钮）
- 输入标签可以使用id标签属性定义自己的唯一标签编号
- 输入标签需要使用名字标签属性name来定义它对应的值应该叫什么，才可以使用提交按钮来提交该输入标签的信息

## 输入名称
- 通常需要在一个输入框或其他的输入控件上对用户显示要输入什么，这个使用输入名称标签来实现，标签名为label
- 输入名称标签的名称属性for可以用标签编号定义显示的文本对应的是哪个输入标签


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