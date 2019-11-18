# 选择器的分组
你可以对选择器进行分组，这样，被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。在下面的例子中，我们对所有的标题元素进行了分组。所有的标题元素都是绿色的。
```
h1,h2,h3,h4,h5,h6{
  color:green;
  }
```
****
# 继承及其问题
根据css,子元素从父元素继承属性。但是它并不总是按照此方式工作。看看下面这条规则:
```
body{
  font_family:Verdana,sans-serif;
  }
```
根据上面这条规则，站点的body元素将使用Verdana字体(假如访问者的系统中存在该字体的话)。  
通过css继承，子元素将继承最高级的元素(在本例中是body)所拥有的属性（这些子元素诸如 p, td, ul, ol, ul, li, dl, dt,和 dd）。不需要另外的规则，所有的body的元素都应该显示Vardana字体，子元素的子元素也一样。并且在大部分的现代浏览器中，也的确是这样。  
这种情况未必会发生，Netscape4就不支持继承，它不仅忽略继承，而且也忽略应用于body元素的规则。IE/Windows直到IE6还存在相关的问题，在表格内的字体样式会被忽略。
****
# 友善地对待NetScape4
我们可以通过使用我们称为"be kind to Netscape4"的冗余法则来处理就是浏览器中无法理解继承的问题。
```
body{
  font-family:Verdana,sans-serif;
  }
p,td,ul,ol,li,dl,dt,dd{
  font-family:Verdana,sans-serif;
  }
```
4.0 无法理解继承，不过他们可以理解选择器。这么做虽然会浪费用户的宽带，但是如果需要对Netscape4用户进行支持，就不得不这么做。
****
# 继承是一个诅咒么？
如果你不希望"Verdana,sans-serif"字体被所有的子元素继承，又该怎么做呢？比方说，你希望段落的字体是Times。没问题，创建一个针对p的特殊规则，这样就会摆脱父元素的规则：
```
body{
  font-family:Verdana,sans-serif;
  }
td,ul,ol,ul,li,dl,dt,dd{
  font-family:verdana,sans-serif;
  }
p{
  font-family:Time,"Time New Roman",serif;
  }
```  
  
