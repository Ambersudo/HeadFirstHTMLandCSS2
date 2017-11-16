# Head First HTML and CSS 2 笔记

## 01 Web语言：开始了解HTML
## 02 认识HTML中的“HT”：深入理解超文本
## 03 创建网页：构建模块
## 04 Web镇之旅：开始链接
## 05 认识媒体：给网页添加图像
## 06 严格的HTML：遵循标准，合乎规范
## 07 添加一些样式：开始学习CSS
## 08扩大你的词汇量：字体和颜色样式
## 09 与元素亲密接触：盒模式
## 10 高级web建设：div和 span
## 11 布置元素：布局和排版
## 12 现代HTML：HTML5标记
## 13 开始制作表格：表格和列表
## 14 交互活动：HTML 表单

div：指定渲染HTML的容器
span：指定内嵌文本容器
通俗地讲就是如果里面还有其他标签的时候就用div，如果里面只有文本就应该用span
div是一个块级元素，用来为HTML文档内大块的内容提供结构和背景
span是行内元素，在行内定义一个区域（也就是一行内可以被<span>划分好几个区域）
div标签中可以镶嵌span标签，（div可以看做是一个大容器，span是一个小容器，大容器当然可以放下一个小容器啦）

lable的作用
- 语义化
- 从用户的角度来看，你几乎看不到这个标签有什么特殊的含义：其在浏览器上无任何特殊的显示方式，既不是斜体也不加粗。
- 然而对那些使用鼠标的用户来说(you and me)，其改进了可用性。如果您在 label 元素内点击文本，就会触发此控件。就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上：
    - 点击姓名，焦点会转移到姓名后面的输入框
    - 单击单选框、复选框的文字（不是按钮），按钮也会被选中


```html
不带lable标签
<form action="http://www.starbuzzcoffee.com/processorder.php" method="post">

        <p>Type:</p>
        <p>
            <input type="radio"  name="beantype" value="whole">
            <input type="radio"  name="beantype" value="ground" checked>
        </p>

</form>


带lable标签

<form action="http://www.starbuzzcoffee.com/processorder.php" method="post">

        <label>Type:</label>
        <p>
            <input type="radio" id="whole_beantype" name="beantype" value="whole">
                <label for="whole_beantype">Whole bean</label><br>

            <input type="radio" id="ground_beantype" name="beantype" value="ground" checked>
                <label for="ground_beantype">Ground</label>
        </p>

</form>
```

输出▼
不带lable标签
<form action="http://www.starbuzzcoffee.com/processorder.php" method="post">

        <p>Type:</p>
        <p>
            <input type="radio"  name="beantype" value="whole">
            <input type="radio"  name="beantype" value="ground" checked>
        </p>

</form>


带lable标签
<form action="http://www.starbuzzcoffee.com/processorder.php" method="post">

        <label>Type:</label>
        <p>
            <input type="radio" id="whole_beantype" name="beantype" value="whole">
                <label for="whole_beantype">Whole bean</label><br>

            <input type="radio" id="ground_beantype" name="beantype" value="ground" checked>
                <label for="ground_beantype">Ground</label>
        </p>

</form>

fieldset和legend将元素组织在一起：
- 总是同时出现
- fieldset 告诉浏览器 fieldset 标签里面包含的是同一组元素
- legned 告诉浏览器  legend 标签里面包含的是同一组元素的标题


```html
<fieldset>
  <legend>Condiments</legend>
  <input type="checkbox">第一行<br/>
  <input type="checkbox">第二行<br/>
  <input type="checkbox">第三行<br/>
</fieldset>
```
输出▼
<fieldset>
  <legend>Condiments</legend>
  <input type="checkbox">第一行<br/>
  <input type="checkbox">第二行<br/>
  <input type="checkbox">第三行<br/>
</fieldset>
