# About Something Web
# CSS篇

### 什么是盒模型
    1.盒模型分为标准盒模型 width = content  和怪异盒模型(ie下) width = content + padding + border 
    2.通过box-sizing 可以切换  content-box padding-box boder-box 
  
### 什么是BFC 
  ###### BFC Box、Formatting Context 块级格式化上下文
  ###### BFC布局规则：
    1.内部的Box会在垂直方向，一个接一个地放置。
    2.Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
    3.每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
    4.BFC的区域不会与float box重叠。
    5.BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
    6.计算BFC的高度时，浮动元素也参与计算
  ###### 参数BFC的条件
    1.根元素 body
    2.position 为absolute或者fixed
    3.display 为 inline-block 、flex、table-cell
    4.overflow 不为visiable
    
### 清浮动
    1.overflowe：hidden
    2.父级定义伪类:after 和 zoom  (推荐)
      div:after{display:block,content:'',clear:both,visibility:hidden,height:0}
      div{zoom:1}
    3.在结尾处添加空div标签clear:both
    4.父级定高
    5.父级一起浮动
  
### Flex 布局
    1.dispaly:flex 子元素的float、clear和vertical-align属性将失效
    2.flex-direction: row | column | row-reverse | column-reverse 主轴方向
    3.flex-wrap: nowrap | wrap | warp-reverse 
    4.justify-content: flex-start,flex-end,center,space-around,space-between
    5.align-item:flex-start | flex-end | center | baseline | stretch; 
    6.order属性：定义项目的排列顺序，顺序越小，排列越靠前，默认为0
    7.flex-grow属性：定义项目的放大比例，即使存在空间，也不会放大
    8.1flex-shrink属性：定义了项目的缩小比例，当空间不足的情况下会等比例的缩小，如果定义个item的flow-shrink为0，则为不缩小
    9.flex-basis属性：定义了在分配多余的空间，项目占据的空间。
    10.flex：是flex-grow和flex-shrink、flex-basis的简写，默认值为0 1 auto。
    11.align-self：允许单个项目与其他项目不一样的对齐方式，可以覆盖align-items，默认属性为auto，表示继承父元素的align-items
    详情 http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html?utm_source=tuicool)
  
### 水平垂直居中
      1.已经子元素宽高
        position:absolute
        top:50%;
        left:50%;
        margin-left:负的一半宽度,
        margin-top:负的一半高度
      2.未知子元素高度
        1.position:absolute
          top:0
          left:0
          right:0
          bottom:0
          margin auto
         2.position:absolute
          top:50%
          right:50%
          transform:translate(-50%,-50%)
       3.flex 布局 
          justify-content: center  align-item: center
       4.table-cell
       
### 画一条0.5px的线
       1.SVG
       2.transform scale
       3.meta viewport
       
### visibility=hidden, opacity=0，display:none 的区别
        1.opacity = 0 页面会保留原来的位置 元素隐藏 如果有onclick事件还是会被触发
        2.visibility = hidden 页面会保留原来的位置 元素隐藏 如果有onclick事件不会被触发
        3.display = none  页面不会保留原来的位置 元素隐藏 如果有onclick不会触发
    
    
      
