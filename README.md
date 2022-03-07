## `less`(（Leaner Style Sheets 的缩写） 是一门向后兼容的 CSS 扩展语言。)
- vscode插件
  - easy less(保存时自动把less转换为css)
- npm package
  - less-loader(A Less loader for webpack. Compiles Less to CSS.)
- 内容
  - 变量（Variables）
  - 混合（Mixins）
  - 嵌套（Nesting）
  - @规则嵌套和冒泡
  - 运算（Operations）
  - calc() 特例
  - 转义（Escaping）
  - 函数（Functions）
  - 命名空间和访问符
  - 映射（Maps）
  - 作用域（Scope）
  - 注释（Comments）
  - 导入（Importing）

## `sass`
- vscode
  - easy sass(Automatically compiles SASS/SCSS files to .css and .min.css upon saving. )
- npm package
  - sass-loader(Loads a Sass/SCSS file and compiles it to CSS.)

## `stylus`
- 富于表现力、动态的、健壮的 CSS

## `styled components`
- styled-components allows you to write actual CSS code to style your components. 


## -webkit-，-moz-，-ms-，-o-是指浏览器私有前缀名。

 - 那为什么要有私有前缀呢?  
 - 因为制定HTML和CSS标准的组织W3C动作是很慢的。  
 - 通常，有w3c组织成员提出一个新属性，比如说圆角border-radius，大家都觉得好，但是w3c不会为这个属性制定标准，而是要走很复杂的程序，经过很多审查。  
 - 而浏览器商不愿意等那么久，他们觉得一个属性已经够成熟了，就会在浏览器中加入支持。  
 - 但是避免日后w3c公布标准时有所变更，就会加入一个私有前缀，比如-webkit-border-radius。  

## -webkit-，-moz-，-ms-，-o-具体代表的浏览器如下：
- -webkit-代表chrome、safari私有属性
- -moz-代表firefox浏览器私有属性
- -ms-代表IE浏览器私有属性
- -o-代表Operai私有属性

***

## 清浮动的三种方法
- 父元素设置属性
```css
overflow:hidden;
```
- 伪元素清除
```css
.clearfix:after{
    content:'';
    display:block;
    height:0;
    clear:both;
    visibility:hidden;
}

.clearfix{
    *zoom:1;
}
```
- 双伪元素清除
```css
.clearfix:before,
.clearfix:after{
    content:'';
    display:table;
}
.clearfix:after{
    clear:both;
}
.clearfix{
    *zoom:1;
}
```

***

## 页面设置全灰的属性
```css
filter: grayscale(100%);
```

***

## rem em px
> `rem`
 - 使用rem为元素设定字体大小时，仍然是相对大小，但相对的只是HTML根元素
> `em`
 - em是相对长度单位。相对于当前对象内文本的字体尺寸
> `px`
 - 相对长度单位。像素px是相对于显示器屏幕分辨率而言的

## @font-face @keyframes @media

```css
@font-face{
 font-family: myFirstFont;
 src: url('Sansation_Light.ttf'),
      url('Sansation_Light.eot'); /* IE9 */
}
```

```css
@keyframes mymove{
 from {top:0px;}
 to {top:200px;}
}

@-webkit-keyframes mymove /* Safari and Chrome */{
 from {top:0px;}
 to {top:200px;}
}
```
```css
@media screen and (max-width: 300px) {
    body {
        background-color:lightblue;
    }
}
```

