# Personal experience of Front-end 


## Framework
 * [React源码解析: 组件实现 (基本16版本)](https://github.com/lewisYe/front-end-engineer/issues/1)
 * [React生命周期(16版本)](https://github.com/lewisYe/front-end-engineer/issues/2)
 * [React Advanced Guides](https://github.com/lewisYe/front-end-engineer/issues/3)
 * [Redux源码分析](https://github.com/lewisYe/front-end-engineer/issues/5) 
 * [React-router v4 源码解析](https://github.com/lewisYe/front-end-engineer/issues/6)

## JS
 * [根据Promise/A+规范实现 Promise](https://github.com/lewisYe/front-end-engineer/issues/7)
 * [异步回调](https://github.com/lewisYe/front-end-engineer/issues/8)
 * [深入原型和原型链](https://github.com/lewisYe/front-end-engineer/issues/9)
 * [深入继承](https://github.com/lewisYe/front-end-engineer/issues/10)
 * [深入 call、apply、bind](https://github.com/lewisYe/front-end-engineer/issues/11) 
 * [函数的防抖与节流](https://github.com/lewisYe/front-end-engineer/issues/12)
 * [函数的柯里化](https://github.com/lewisYe/front-end-engineer/issues/13)
 * [事件机制](https://github.com/lewisYe/front-end-engineer/issues/14)

## Network、Browser
 * [浏览器缓存](https://github.com/lewisYe/front-end-engineer/issues/15)
 * [Event loop](https://github.com/lewisYe/front-end-engineer/issues/16)
 * [浏览器渲染机制](https://github.com/lewisYe/front-end-engineer/issues/17)
 * [解决跨域](https://github.com/lewisYe/front-end-engineer/issues/18)
 * [http and https](https://github.com/lewisYe/front-end-engineer/issues/19)
 * [本地存储](https://github.com/lewisYe/front-end-engineer/issues/20)
 * [WebSocket](https://github.com/lewisYe/front-end-engineer/issues/21)
## Bundled
 * webpack
    - [从零搭建 React 全家桶脚手架](https://github.com/lewisYe/front-end-engineer/issues/4)
 * gulp
    - [gulp搭建本地服务](https://github.com/lewisYe/front-end-engineer/issues/22)

## HTML、CSS
 * [清楚浮动的几种方法](https://github.com/lewisYe/front-end-engineer/issues/23)
 * [常见的几种布局实现](https://github.com/lewisYe/front-end-engineer/issues/24)

## Development plugin
* [develop a babel-plugin](https://github.com/lewisYe/front-end-engineer/issues/25)

## Other 
* [微信小程序开发](https://github.com/lewisYe/front-end-engineer/issues/26)
* [钉钉应用开发](https://github.com/lewisYe/front-end-engineer/issues/27)

<!-- ### 什么是盒模型
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
          1.先解析url 将网络地址转换为ip地址 、指出协议 和 及指出需要的资源在那台计算机上
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
        
   ### 类的创建与继承 ES5 和 ES6
        1.类的创建
            function Animal(name){
                this.name = name || 'animal'
                this.sleep = function(){
                    console.log(this.name + 'is sleep')
                }
            }
            Animal.prototype.eat = function(){
                console.log(this.name +' is eating food')
            }
        2. 原型链基础
            function Cat(){}
            Cat.prototype = new Animal()
            Cat.prototype.name = 'cat'
            var cat = new Cat();
            console.log(cat.name)// cat
            console.lof(cat.sleep) // cat is sleep 
            介绍：在这里我们可以看到new了一个空对象,这个空对象指向Animal并且Cat.prototype指向了这个空对象，这种就是基于原型链的继承。
            特点：基于原型链，既是父类的实例，也是子类的实例
            缺点：无法实现多继承
         3. 构造继承：使用父类的构造函数来增强子类实例，等于是复制父类的实例属性给子类（没用到原型）
            function Cat (name){
                Animal.call(this);
                this.name = name || 'Tom';
            }
            var cat = new Cat();
            特点：可以实现多继承
            缺点：只能继承父类实例的属性和方法，不能继承原型上的属性和方法。
         4.组合继承：相当于构造继承和原型链继承的组合体。调用父类构造，继承父类的属性并保留传参的优点，然后通过将父类实例作为子类原型，实现函数复用
            function Cat(name){
                Animal.call(this)
                this.name = name || 'Tom';
            }
            Cat.prototype = new Animal();
            Cat.prototype.constructor = Cat;
            var cat = new Cat();
            特点：可以继承实例属性/方法，也可以继承原型属性/方法
            缺点：调用了两次父类构造函数，生成了两份实例
            
         5.寄生组合继承：通过寄生方式，砍掉父类的实例属性，这样，在调用两次父类的构造的时候，就不会初始化两次实例方法/属性
            function Cat (name){
                Animal.call(this);
                this.name = name || 'Tom';
            }
            (
             function(){
                var Super = function(){}
                Super.prototype = Animal.Prototype
                Cat.prototype = new Super();
                
             }
            )()
            var cat = new Cat();
            
          6.ES6 继承
            class Animal(name){
                constructor(name){
                    this.name = name || 'aniaml'
                }
            }
            class Cat extends Animal(){
               
            }
            var cat = new Cat();
            
 ### apply、call和bind 的区别 与原生实现
        1.apply，call，bind 三者都可以改变this 的指向。
        2.apply和call 第一个参数都是一样的表示要改变指向的那个对象 apply 第二个参数是个数组，call 第二个参数是arguments
        3.通过bind改变this作用域会返回一个新的函数，这个函数不会马上执行。
        
        call 原生实现
            Function.prototype.newCall = function(content,...params){
                content.fn = this;
                content.fn(...params);
                delete content.fn
            }
            
         apply 原生实现
            Function.prototype.newApply = function(content,params){
                content.fn = this;
                content.fn(params);
                delete content.fn
            }
            
         bind 原生实现
            Function.prototype.newBind = function(content,...innerParams){
                var that = this;
                return function(...finnalyParams){
                    return that.call(content,...innerParams,...finnalyParams)
                }
            }
    
   ### new 操作符 实际干了什么
        var obj = new Base();
        1.首先内部新建了一个空对象
            var obj = {}
        2.然后将obj._proto_ 指向了 Base的原型 Base.prototype
            obj.__proto__ = Base.prototype;
        3.我们将Base函数对象的this指针替换成obj
            Base.call(obj);

   ### 如何解决回调
        promise、generator、async/await 详情看es6
        一 promise 
           特点:
            1.对象的状态不受外界影响 有三个状态 pending (进行中)、fulfilled（已成功）、rejected（已失败）
            2.一旦状态改变，就不会再变，任何时候都可以得到这个结果
           缺点:
            1.无法取消Promise，一旦新建它就会立即执行，无法中途取消
            2.如果不设置回调函数，Promise内部抛出的错误，不会反应到外部
            3.当处于pending状态时，无法得知目前进展到哪一个阶段（刚刚开始还是即将完成）。
           基本调用
            var promise = new Promise(functiotn(resolve,reject){
                if (/* 异步操作成功 */){
                    resolve(value);
                  } else {
                    reject(error);
                  }
            })
            
   ### 函数防抖和函数节流
        1.函数防抖
            function debounce (fn,delay){
                let timer = null;
                return function(){
                    clearTimeout(timer);
                    timer = setTimeout(()=>{
                        fn()
                    },delay)
                }
            }
            
            function foo(){
                console.log('函数防抖')
            }
            
            document.addEventListener('scroll',debounce(fn,200),false)
         2.函数节流
            function throttle(fn,blank){
                let timer,last;
                let now = +new Date;
                return function(){
                    if(now&&last < last + blank){
                        clearTimeout(timer);
                        timer = setTimeout(()=>{
                            fn();
                            last = now;
                        },blank)
                    }else{
                        fn();
                        last = now;
                    }
                }
            }
            
   ### 前端事件流
        Dom2级事件分为
        事件捕获阶段
        处于目标阶段
        事件冒泡阶段
        
        1.dom2级事件 绑定函数
            addEventListener 和 attachEvent 
        
            ele.addEventListener('click',function(){},false)
            三个参数为 要处理的事件名、作为事件处理程序的函数和一个布尔值。 false为冒泡 true为捕获

            ele.attachEvent('onclick',function(){})
            多次绑定后执行的顺序是不一样的，attachEvent是后绑定先执行，addEventListener是先绑定先执行。

        2. 利用事件冒泡的机制 可以来做事件委托 子元素的时间 委托给父元素 然后通过 e.target 来判断
            e.target 和 e.currenTarget
            
            currenTarget 返回绑定事件的元素
            target 返回触发事件的元素
            
         3.mouseover和mouseenter的区别
            mouseover：当鼠标移入元素或其子元素都会触发事件，所以有一个重复触发，冒泡的过程。对应的移除事件是mouseout
            mouseenter：当鼠标移除元素本身（不包含元素的子元素）会触发事件，也就是不会冒泡，对应的移除事件是mouseleave
            
  ### 基本数据类型
        Null Number Undefined Boolen String Symbol  复杂数据类型 Object  （主要大小写）
        
  ### 跨域
    为什么会跨域 是因为浏览器的同源策略的限制 域名 协议 端口号要相同
    所有的跨域问题都需要后端协助解决
        一、jsonp 跨域 
            使用script 标签来引入一个js 文件  但是文件路径后面会带上一个callback 函数名 后端讲处理好的数据作为这个函数名的参数返回到前端 
            加载页面的时候 会自动执行这个函数的
            jsop 只适用于get请求
        二、CORS
        三、通过修改document.domain来跨子域
        四、window.name
        五、HTML5中window.postMessage
          
  ### XSS 和 CSRF 
    XSS, 即为（Cross Site Scripting）, 中文名为跨站脚本是发生在目标用户的浏览器层面上的，当渲染DOM树的过程成发生了不在预期内执行的JS代码时，
    就发生了XSS攻击。
    分为 反射行XSS 存储型XSS 和 DOM XSS
    反射型XSS是在将XSS代码放在URL中，将参数提交到服务器。服务器解析后响应，在响应结果中存在XSS代码，最终通过浏览器解析执行。
    存储型XSS是将XSS代码存储到服务端（数据库、内存、文件系统等），在下次请求同一个页面时就不需要带上XSS代码了，而是从服务器读取。
    DOM XSS的发生主要是在JS中使用eval造成的，所以应当避免使用eval语句。
    XSS危害有盗取用户cookie，通过JS或CSS改变样式，DDos造成正常用户无法得到服务器响应。
    XSS代码的预防主要通过对数据解码，再过滤掉危险标签、属性和事件等。cookie 设置httpOnly
    
    CSRF
    CSRF全程 Cross Site Request Forgery, 跨站域请求伪造
    预防
    http 请求头中的referer 验证 和 token
   
  ### 实现函数 fn(1)(2)(3)(4) = 10  (柯里化)
  
       function Currie(x){
          let sum = x;
          let tmp = function(y){
            sum += y;
            return tmp
          }
          tmp.toString = function(){
            return sum;
          }
          return tmp;
       }
        
     
 # React篇
   ### 性能优化
        1.componetShouldUpdate 
            该生命周期默认返回的是true  当状态或者props 改变是都会更新 可以在该层处理 返回false 来控制  减少不必要的更新
        2.pureComponent
            组件继承 class app extends React.PureComponent pureComponent 是官方的api 也是对componentShouldUpdate这个生命周期
            进行处理的 但是是浅比较 需要深入的对状态改变的对比 可以引入三方库 Immutable.js 来处理
    
       
         -->
