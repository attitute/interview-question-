# 二 , CSS 部分

# 常见问题

## 1、CSS3选择器有哪些？

答：属性选择器、伪类选择器、伪元素选择器。

## 2、CSS3新特性有哪些？

答：1. 颜色：新增 RGBA，HSLA 模式

\2. 文字阴影（text-shadow、）

3.边框： 圆角（border-radius）边框阴影： box-shadow

\4. 盒子模型：box-sizing

5.背景：background-size设置背景图片的尺寸 background-origin设置背景图片的原点 background-clip 设置背景图片的裁切区域，以”，”分隔可以设置多背景，用于自适应布局

6.渐变：linear-gradient、radial-gradient

\7.  过渡：transition，可实现动画

\8.  自定义动画

\9.  在CSS3 中唯一引入的伪元素是：：selection.

\10.  媒体查询，多栏布局

11.border-image

12.2D转换：transform：translate(x，y) rotate(x，y) skew(x，y) scale(x，y)

13.3D 转换

## 3、CSS引入的方式有哪些? link 和 @import 的区别是?

答：内联 内嵌 外链 导入

区别 ：同时加载

前者无兼容性，后者 CSS2.1 以下浏览器不支持

Link支持使用 javascript 改变样式，后者不可

## 4、描述 css reset 的作用和用途？

答：Reset 重置浏览器的 css 默认属性 ，览器的品种不同，样式不同，然后重置，让他们统一。

## 5、解释css sprites，如何使用？

答：Css 精灵图，把一堆小的图片整合到一张大的图片（png）上，减轻服务器对图片的请求数量。