<font face="楷体">
html是标签语言，作为head区域的辅助性meta标签，它规定了网页属性。meta也有两个属性，如下：

### name属性
描述页面属性，便于搜索引擎查找信息和分类信息，格式如下：
```html
<meta name="参数" content="具体值">
```
name的可选参数如下：
* keywords，网页关键字
* description，网站主要内容
* robots，机器人向导，告诉搜索引擎哪些需要牵引哪些不用，参数值及其要义如下：
  1. all，文件将被检索，页面上的链接可查询；
  2. none，文件不被检索，页面链接不可查询；
  3. index，文件可检索，对立的就是文件不被检索的noindex，但其链接可查询；
  4. follow，页面链接不可查询，对立的是nofollow，链接不可查询但文件可检索。
  5. author，标注页面作者；
  6. generator，网站制作采用的软件；
* COPYRIGHT，网站版权信息；
* revisit-after，表示到点就刷新，加上url参数就是到点自动访问该链接；
* 重要的viewport，设置浏览器显示网页的区域信息，
比如为了适应移动端，使得访问网页时因为和PC的可视区域有差别而出现字体变小或者横向滚动条，可以加入以下代码：
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
/*width=device-width设置viewport宽度为理想宽度，initial-scale=1.0设置页面初始缩放值为1*/
```
viewport的一些参数如下：
* width，设置网页宽度，为正整数数值
* initial-scale，设置页面初始缩放值，为实数
* minimum-scale，允许用户的最小缩放值，为实数
* maximum-scale，允许用户的最大缩放值，为实数
* height，设置网页高度
* user-scalable，是否允许用户进行缩放

### http-equiv属性

模拟一个http响应头，用以向浏览器传达一些设置信息，便于更好地显示网页，但我百度到的一些信息都很老了，看它的一些使用应该也被其他方法代替了，语法和name属性一致：
```html
<meta http-equiv="可选参数" content="参数变量值">
```

* expires

设定网页的到期时间，网页到期需要重新请求网页数据
```html
<meta http-equiv="expires" content="Mon,25Dec202218:18:18GMT">
```
需要用GMT的时间戳

* Pragma

设置浏览器是否可以从缓存中访问页面内容，禁用会使得浏览器无法脱机浏览
```html
<meta http-equiv="pragma" content="no-cache">
```

* Refresh

设定自动刷新时间，添加url则是设定x秒后自动跳转url指示地址

```html
<meta http-equiv="refresh" content="2;url=https://google.com">
```

* Set-cookie

设定cookie有效期，在网页到期后，缓存的cookie将删除
```html
<meta http-equiv="Set-Cookie">
```

* Window-target

设定页面在窗口是否以独立页面展示

```html
<meta http-equiv="Window-target" content="_top">
```
防止被别人在框架力调用自己的页面

* Content-Type

设定页面使用字符集

* Content-Language

设置显示语言

* Cache-Control

设定请求和响应遵循的缓存机制