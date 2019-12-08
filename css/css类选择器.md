# css类选择器 
### 在css中，类选择器以一个点好显示：
```
.center{text-align:center}
```
在上面的例子中，所有拥有center类的HTML元素均为居中。  
在下面的HTML代码中，h1和p元素都有center类。这意味着两者都将遵守".center"选择器中的规则。
```
<h1 class="center">
this heading will be center-aligned
</h1>
<p class="center">
this paragraph will also be center-aligned.
</p>
```
注意：类名的第一个字符不能使用数字！它无法在Mozilla或Firefox中起作用。  
### 和id一样，class也可以被用作派生选择器：
```
.fancy td{
 color:#f60;
 background;
 }
```
在
