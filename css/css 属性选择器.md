# 简单的属性选择器
如果希望选择某个属性的元素，而不论属性值是什么，可以使用简单的属性选择器。
#### 例子1
如果你想把包含标题的（title）的所有的元素变成红色，可以这样写：
```
*[title]{color:red;}
```
亲自试一试
```
<html>
<head>
<style type="text/css">
[title]
{
color:red;
}
</style>
</head>
<body>
<h1>可以应用样式：</h1>
<h2 title="hello world">hello world</h2>
<a title="w3school" href="https://doctorlb.github.io/html-js-css/">w3school</a>

<hr/>
<h1>无法应用样式:</h1>
<h2>hello wrold</h2>
<a href="https://doctorlb.github.io/html-js-css/">w3cschool</a>
</body>
</html>
```
##### 例子2
与上面类似，可以对href属性的锚（a元素）应用样式：
```
a[href]{color:red;}
```
亲自试一试
```
<html>
<head>
<style type="text/css">
a[href]
{
color:red;
}
</style>
</head>
<body>
<h1>可以应用样式:</h1>
<a href="https://doctorlb.github.io/html-js-css/">w3shcool</a>

<hr/>
<h1>无法应用样式:</h1>
<a name="w3school">w3school</a>
</body>
</html>
```
#### 例子3
还可以根据很多属性进行选择，只需将属性选择器链接在一起即可。  
例如：为了将同时有href和title属性的html超链接的文本设置为红色，可以这样写：
```
a[href][title]{color:red;}
```
亲自试一试
```
<html>
<head>
<style type="text/css">
a[href][title]
{
color:red;
}
</style>
</head>
<body>
<h1>可以应用样式：</h1>
<a title="w3school" href="https://doctorlb.github.io/html-js-css/">w3school</a>

<hr/>
<h1>无法应用样式：</h1>
<a href="https://doctorlb.github.io/html-js-css/">w3shool</a>
</body>
</html>
```
#### 例子4
可以采用一些创造性的方法来使用这个特性。
例如，可以对所有带alt属性的图形应用样式，从而突出显示这写有效的图像：
```
img[alt]{border:5px solid red;}
```
亲自试一试
```
<html>
<head>

