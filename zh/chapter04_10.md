# 引入`ng-include`和模板`ng-template`
引入`ng-include`和模板`ng-template`是定义和使用HTML代码碎片的功能。用于将HTML切碎分别存储，并根据需求再去获取对应的代码块，达到加速访问和代码复用的效果。

下面，我们将分别介绍`ng-include`和`ng-template`。

## 引入`ng-include`
当HTML代码过于复杂，或者期望建立单页应用(Single-page Application - SPA)时，需要将部分HTML打包成独立的文件。这时候，我们在引入这个独立HTML文件时，可以使用`ng-include`功能。

使用方法如下：

```html
<!--  直接传入一个网页的地址，请注意这里的使用用法 -->
<!--  'view/part.html' 外部有单引号 -->
<div ng-include="'views/part.html'"></div>

<!-- 假设$scope中有template:{url:"http://..."}这个对象 -->
<div ng-include="template.url"></div>

<div ng-include="getUrl()"></div>
```

从上面的例子可以看出，`ng-include`支持直接传入静态文本、传入变量、传入函数（返回网页地址）的方式来进行调用。

另外，`ng-include`的用法也可以直接作为标签名使用，如：

```html
<div data-ng-include="'views/part.html'"></div>

<ng-include src="'views/part.html'"></ng-include>
```

这些用法的效果都是一样的。

### 其他属性
`ng-include`还有`onload`和`autoscroll`的属性。

但是我目前不清楚具体的使用方法和效果，如果有读者清楚，可与我联系以便更新上此段内容。

## 模板`ng-template`
`ng-template`用于将多个HTML片段存放于一个HTML文件中。并且可以根据需求分别调用其中的某一个片段。

`ng-template`的用法如下：

```html
<script type="text/ng-template" id="html_part.html">
  <!-- HTML片段的实际内容 -->
</script>
```

`ng-template`需要将`<script>`的`type`设置为`text/ng-template`，然后给他配置一个`id`。这个`id`就是这段HTML代码被引用时的名称。

使用`ng-template`代码片段的方法就是上诉的`ng-include`方法，例如：

```html
<div ng-include="'html_part.html'"></div>
```
