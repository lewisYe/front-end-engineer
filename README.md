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
    
### CSS3新特性
        1.新增选择器 例如伪类选择器:nth-of-type 、:nth-of-child 等
        2.新增css动画相关的 transition、transform、animation等 都有浏览器兼容问题
            transition 属性
                1.transition-property:规范过渡应用css名称
                2.transition-duration:规定过渡时间
                3.transition-dealy:过渡延迟
                4.transition-timing-function:过渡效果的时间曲线 默认 ease 还有linear、ease-in、ease-out、ease-in-out和cubic-bezier等
                5.缩写 transition:property duration timing-function dealy 例如 transition: width 1s linear 2s;
                
            transform 属性
                1. 旋转 rotate 
                    transform:rotate(45deg) 顺时针旋转45度。 单位deg为度的意思，正数为顺时针旋转，负数为逆时针旋转
                2. 缩放 scale
                    用法：transform: scale(0.5)  或者  transform: scale(0.5, 2);
                    一个参数时：表示水平和垂直同时缩放该倍率
                    两个参数时：第一个参数指定水平方向的缩放倍率，第二个参数指定垂直方向的缩放倍率。
                3. 倾斜 skew
                    transform: skew(30deg)  或者 transform: skew(30deg, 30deg);
                    一个参数时：表示水平方向的倾斜角度；
                    两个参数时：第一个参数表示水平方向的倾斜角度，第二个参数表示垂直方向的倾斜角度。
                4. 移动 translate
                    transform: translate(45px)  或者 transform: translate(45px, 150px);
                    一个参数时：表示水平方向的移动距离；
                    两个参数时：第一个参数表示水平方向的移动距离，第二个参数表示垂直方向的移动距离。
                5.  基准点 transform-origin
                    在使用transform方法进行文字或图像的变形时，是以元素的中心点为基准点进行的。使用transform-origin属性，可以改变变形的基准点。
                    用法：transform-origin: 10px 10px;
                    共两个参数，表示相对左上角原点的距离，单位px
                    第一个参数表示相对左上角原点水平方向的距离，第二个参数表示相对左上角原点垂直方向的距离；
                    其中第一个参数也可以指定为left、center、right，第二个参数也可以指定为top、center、bottom。
                    
                 这四种变形方法顺序可以随意，但不同的顺序导致变形结果不同，原因是变形的顺序是从左到右依次进行。
            
            animation 属性
                1. animation-name 规定需要绑定到选择器的 keyframe 名称
                2. animation-duration 规定完成动画所花费的时间，以秒或毫秒计。
                3. animation-timing-function 规定动画的速度曲线。
                4. animation-delay 	规定在动画开始之前的延迟。
                5. animation-iteration-count 规定动画应该播放的次数。
                6. animation-direction 规定是否应该轮流反向播放动画。
                
                
                @-webkit-keyframes anim1 { 
                   0% { 
                        opacity: 0; 
                        font-size: 12px; 
                   } 
                   100% { 
                        opacity: 1; 
                        font-size: 24px; 
                   } 
                } 
                .anim1Div { 
                   -webkit-animation-name: anim1 ; 
                   -webkit-animation-duration: 1.5s; 
                   -webkit-animation-iteration-count: 4; 
                   -webkit-animation-direction: alternate; 
                   -webkit-animation-timing-function: ease-in-out; 
                }
                
            transition 和 animation 区别 transition需要触发事件

        3. @font-face特性
            例如 @font-face {
                    font-family: myFirstFont;
                    src: url('Sansation_Light.ttf'),
                         url('Sansation_Light.eot'); /* IE9+ */
                }
                div{
                    font-family:myFirstFont;
                }
        4. border-radius border-shadow border-images
        5. 渐变 gradient
        
### 单行省略号 和 多行省略号
    1.单行
        overflow:hidden
        text-overflow:ellipsis
        white-space:nowrap
    2.多行
        overflow: hidden;
        text-overflow: ellipsis;
        display: -webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient: vertical;
        移动端浏览器绝大部分是WebKit内核的，所以该方法适用于移动端；
        -webkit-line-clamp 用来限制在一个块元素显示的文本的行数,这是一个不规范的属性(unsupported WebKit property)它没有出现在CSS规范草案中。
        display: -webkit-box 将对象作为弹性伸缩盒子模型显示 。
        -webkit-box-orient 设置或检索伸缩盒对象的子元素的排列方式 。
        text-overflow: ellipsis 以用来多行文本的情况下，用省略号“…”隐藏超出范围的文本。
        

# HTML篇
  ### link 和 @import 区别
        1.使用link引入 与页面加载时同时引入，@import 是等页面加载完成之后加载css
        2.link 是html标签 无兼容问题，@import 具有兼容问题 不兼容低版本
        3.link 支持JavaScript去改变样式，@import 不支持
        4.link的权重大于@importd的权重
        
  ### HTML5 新增属性
        新增加了图像、位置、存储、多任务等功能。
        1.canvas
        2.video,audio
        3.本地存储 localStorage和sessionStorage
            cookie、localStorage 和 sessionStorage 三者区别
            共同点:都是存储在浏览器端，且是同源
            区别点:
                1.cookie是为了标识用户身份存储在用户本地的数据，始终在同源http请求中携带。即cookies在浏览器和服务器之间来回传递，而
                localStorage和sessionStorage不会自动发给服务器，只是本地存在
                2.存在大小不同 cookie 大小不超过4k localStorage 和 sessionStorage 最大可以达到5M
                3.cookie 失效有时间限定 与设置的时间有关，sessionStorage是会话级别的存储 浏览器关闭就失效了，localStorage是长期存在的
                4.作用域不同。cookie和localstorage在所有的同源窗口都是共享；sessionstorage不在不同的浏览器共享，即使同一页面
         4.语义化标签 nav header footer section 等
         5.位置API：Geolocation  navigator.geolocation
         6.表单控件 calendar date time email url search
         7.web worker 多线程
             w=new Worker("demo_workers.js");
             postMessage() 回传信息
             onmessage 监听信息
             terminate 关闭
         8.拖放api
         
        移除的元素：
        纯表现的元素：basefont big center font s strike tt u
        性能较差元素：frame frameset noframes
        
        
 # HTTP 和 浏览器
   ### 在浏览器中输入url之后发生了什么
       大致分为 网络通信 和 页面渲染 两部分
       一 网络通信 
          1.先解析url 讲网络地址转换为ip地址 、指出协议 和 及指出需要的资源在那台计算机上
          2.dns 解析 ip 地址  
            客户端先检查本地是否有对应的IP地址，若找到则返回响应的IP地址。若没找到则请求上级DNS服务器，直至找到或到根节点
          3.应用层客户端发送HTTP请求
          4.传输层TCP传输报文  TCP 三次握手
          5.网络层IP协议查询MAC地址
          6.数据到达数据链路层
          7.服务器接收数据
          8.服务器响应请求 返回状态码
          9.服务器返回相应文件
      二 页面渲染 
           浏览器在没有完全接收完html 文件的时候就开始渲染了
           
   ### http 请求方式有哪些
       get post put delete 等
       1.get 请求参数长度误区
         get 请求方式是讲参数放在地址栏后面的 所以长说有长度限制  但这个限制是浏览器的限制 不是http协议的限制
       2.get / post 缓存区别
         get 一般为查询操作 所以可以缓存
         post 一般为修改 操作 一般不使用缓存
           
 # Javascript 篇
   ### 原型链
        两个原型之间通过__proto__来链接形成的链 就是原型链
        
   ### 类的创建与继承
        
        
        
    
                
