# 深入学习AngularJS - Directive
在前一章中，我们学习了AngularJS的基本用法。从本章开始，我们将学习"深入"一些的部分。

本章将介绍AngularJS的Directive。

> 有若干AngularJS的中文译文将Directive翻译为"指令"，但是我感觉此翻译很难让读者明确其具体的含义和用法，因此，我在本书中直接应用了英文名。

AngularJS的Directive，从实际用途的理解，可以称之为"自定义HTML标签"。举个例子，AngularJS可以让我们进行如下的HTML编码：

```html
<!-- 直接作为标签名 -->
<people>    </people>

<!-- 直接作为标签属性 -->
<div people="Harry"> </div>

<!-- 作为类属性 -->
<div class="people:Harry"> </div>
```

> 还有一种比较特殊的放置在注释中生效的表达方式，但是我目前没有理解其实现意义，就不在这里介绍了。

如果我们预先定义好了针对这些标签的处理方式，那么AngularJS将可以把这些标签自动的转化成HTML显示代码。

## Directive在系统中的使用
其实，Directive作为AngularJS的基本特性，我们已经在前面大量的学习和使用了它。

在第四章中我们学习的`ng-app`, `ng-controller`, `ng-model`,  ng-if等使用方法。如果您现在再仔细看下它们的使用方法，就会发现它们无一例外的都是Directive！

## 学习Directive的路程
本章我们将从最基本的自定义Directive开始，逐渐深入的学习Directive的特性和高级使用方法。由于Directive的特性主要针对展示界面的操作，目的是对界面操作的抽象与解耦。因此，可能像我一样对前端经验不太足的读者们，可能会对Directive的学习或者使用价值感到困难。因此，学习Directive可能会多花您一些时间，但是相信我，这些付出是非常有价值的！
