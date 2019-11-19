# id选择器
id选择器可以为标有特定的html元素指定特定的样式。  
id选择器以"#"来定义。
下面两个id选择器，第一个可以定义元素的颜色为红色，第二个定义元素的颜色为绿色：
```
#red{color:red;}
#green{color:green;}
```
在下面的html代码中，id属性为red的p元素显示为红色，而ip地址为green的p元素显示为绿色。
```
<p id="red">这个段落是红色.</p>
<p ip="green">这个段落是绿色.</p>
```
注意：id属性只能在每个html文档中出现一次。
****
# id选择器和派生选择器
在现在布局中，id选择器常常用于建立派生选择器。
```
# sidebar p{
  font-size:italic;
  text-align:right;
  margin-top:0.5em;
  }
```
上面的样式只会用于出现在id是sidebar的元素内的段落。这个元素很可能是div或者是表格单元。
尽管它也可能是一个表个或者其他块级元素，尽管它也可能是一个表格或者其他块级元素。它甚至
可以是一个内联元素，比如 <em></em> 或者 <span></span>，不过这样的用法是非法的，因为不可以
在内联元素<span>中嵌入<p>
# 一个选择器，多种用法
即使被标注为sidebar元素只能在文档中出现一次，这个id选择器作为派生选择器也可以被使用很多次：
```
#sidebar p {
  font-size:italic;
  text-align:right;
  margin-top:0.5em;
  }
#sidebar h2{
  font-size:1em;
  font-weight:normal;
  font-size:italic;
  margin:0;
  line-height:1.5;
  text-align:right;
  }
```
在这里，与页面的其他p元素明显不同的是，sidebar内的p元素得到了特殊的处理，同时，与页面中其他所有h2元素明显不同的是，sidebar中的h2元素也得到了不同的特殊处理。
****
# 单独选择器
id选择器即使不被用来创建派生选择器，它也可以独立发挥作用：
```
#sidebar{
border:1px dotted #000;
padding:10px;
}
```
根据这条规则，id为sidebar的元素将拥有一个像素宽的黑色点状边框，同时其周围会有10个像素宽的内边距（padding,内部留白）。老版本的IE浏览器可能会忽略这条规则，除非你特别地定义这个选择器所属的元素：
```
div#sidebar{
border:1px dotted #000;
padding:10px;
}
```




