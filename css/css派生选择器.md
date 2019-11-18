# 派生选择器
通过依据元素在其位置的上下文关系来定义样式，你可以使标记更加简洁。  
派生选择器允许你根据文档的上下文关系来确定某个标签的样式。通过合理的使用派生选择器，我们可以使html代码变得更加整洁。
比方说，你希望列表中的strong元素变为斜体字，而不是通常的粗体字，可以这样定义一个派生选择器：
```
li strong{
  font-style:italic;
  font-weight:normal;
  }
```
请注意标记为<strong>为上下文关系：
```
<li><strong>我是斜体字，是因为strong 元素位于li元素内.</strong></li>
```
在上面的例子中，只有li元素中的strong元素样式为斜体字，无需为strong元素定义特别的class或id，代码更加简洁。
在看看下面的css规则：
```
h2 strong{
  color:blue;
  }
```
下面是它影响的html:
```
<h2>.......<strong>blue</strong></h2>
```
