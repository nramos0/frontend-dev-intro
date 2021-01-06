# 10 - HTML的列表

## 列表
- 有时需要把一组内容列在一起，这个可以用列表实现
- HTML列表有三种：无序列表、有序列表、描述列表
- 无序列表在每个元素的左边会显示子弹点
- 有序列表在第`i`个元素的左边会显示该数字`i`
- 描述列表可以列一些内容，元素左边不会有什么额外的显示。每个元素支持添加一个或多个描述列表项，描述列表项会在对应的元素下面靠右一点的位置显示

## 列表标签
- 为了显示列表，需要使用列表标签，然后每个元素要用到列表项标签
- 无序列表
  - 列表标签：ul (Unordered List)
  - 列表项标签： li (List Item)
- 有序列表
  - 列表标签：ol (Ordered List)
  - 列表项标签： li (List Item)
- 描述列表
  - 列表标签：dl (Description List)
  - 列表项标签：dt (Description Tag)
  - 描述项标签：dd (Description (List) Description) 即描述列表里的一个描述项

无序列表
```html
<ul>
    <li>列表项</li>
    <li>列表项</li>
    <li>列表项</li>
    <li>列表项</li>
</ul>
```

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul> 
```

有序列表
```html
<ol>
  <li>第一项</li>
  <li>第二项</li>
  <li>第三项</li>
  <li>第四项</li>
</ol> 
```

```html
<ol>
  <li>咖啡</li>
  <li>茶</li>
  <li>牛奶</li>
</ol> 
```

描述列表
```html
<dl>
  <dt>咖啡</dt>
  <dd>- 黑色的热饮</dd>
  <dt>牛奶</dt>
  <dd>- 白色的冷饮</dd>
</dl>
```

本节的标签
- ul 无序列表
- ol 有序列表
- li 列表项（无序列表和有序列表均可以用）
- dl 描述列表
- dt 描述列表列表项
- dd 描述列表描述项