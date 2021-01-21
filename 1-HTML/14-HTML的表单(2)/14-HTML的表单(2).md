# 13 - HTML的表单(2)

## 多行输入框
- 之前的输入类型type为text的输入标签可以实现单行输入框
- HTML也支持多行输入框，标签名为textarea
- 可以使用行数属性rows和列数属性cols来定义它的大小
- 也可以使用普通的宽度和高度样式属性来定义它的大小
- 和输入标签一样，要定义信息名称属性name

例子：使用行数属性和列数属性
```html
<label for="description">请你介绍一下你自己</label><br />
<textarea id="description" name="description" rows="10" cols="30">
我是一个###的人
</textarea>
```

例子：使用宽度和高度样式属性
```html
<label for="description">请你介绍一下你自己</label><br />
<textarea id="description" name="description" style="width: 400px; height: 300px;">
我是一个###的人
</textarea>
```

## 菜单标签
  - HTML里也支持菜单，标签名为select
    - 菜单标签需要定义信息名称name
  - 每个可选选项使用选项标签写，标签名为option
    - 每个option需要定义一个信息值value

例子
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast">
  <option value="dumplings">饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast">吐司</option>
  <option value="baozi">包子</option>
</select>
```

- 可以使用多选属性multiple为true(即“是”)来允许多个选择（可以按Ctrl并点击进行多选）

例子
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast" multiple="true">
  <option value="dumplings">饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast">吐司</option>
  <option value="baozi">包子</option>
</select>
```

- 可以使用大小属性size来定义在某个时刻用户可以看到多少个选项。如果选项数比大小属性的值多，则用户可以上下滚动

例子
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast" size="2">
  <option value="dumplings">饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast">吐司</option>
  <option value="baozi">包子</option>
</select>
```

- 可以在选项标签里使用已选属性selected为true来定义默认选择的选项

例子
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast" multiple="true">
  <option value="dumplings" selected="true">饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast" selected="true">吐司</option>
  <option value="baozi">包子</option>
</select>
```

## 没有值的标签属性
- 实际上，以上的多选属性multiple和已选属性selected不管是什么值都会起作用，甚至可以省略`="..."`部分，这种标签属性叫没有值的标签属性。只要属性是存在的，就会起作用

刚刚的这些HTML代码
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast" multiple="true">
  <option value="dumplings" selected="true">饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast" selected="true">吐司</option>
  <option value="baozi">包子</option>
</select>
```

等同于这些代码
```html
<label for="breakfast">选择你的早餐</label><br />
<select id="breakfast" name="breakfast" multiple>
  <option value="dumplings" selected>饺子</option>
  <option value="youtiao">油条</option>
  <option value="toast" selected>吐司</option>
  <option value="baozi">包子</option>
</select>
```