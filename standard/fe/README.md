# 前端开发规范

## 通用规范
- tab键用两个空格代替
    > 注意将IDE的缩进设置为空格，因为在不同系统的[IDE](../../#13-术语定义)对tab解析不一样，windows下的tab键是占四个空格的位置，而在linux下会变成占八个空格的位置（除非你 自己设定了tab键所占的位置长度）。

- 每个样式属性或者每句代码后加 ";" 方便压缩工具"断句"。


## 前端规范之HTML

- HTML5 doctype: 为每个 HTML 页面的第一行添加标准模式（standard mode）的声明，这样能够确保在每个浏览器中拥有一致的展现。
    ```html
        <!DOCTYPE html>
    ```

- 必须申明文档的编码charset，且与文件本身编码保持一致，推荐使用UTF-8编码。
    ```html
        <meta charset="utf-8"/>
    ```


- 浏览器兼容：官网IE8+，管理平台IE9+

- 根据页面内容和需求填写适当的keywords和description。

- 页面title是极为重要的不可缺少的一项。

- 结构顺序和视觉顺序基本保持一致

    + 按照从上至下、从左到右的视觉顺序书写HTML结构。

    + 有时候为了便于搜索引擎抓取，我们也会将重要内容在HTML结构顺序上提前。

    + 用div代替table布局，可以使HTML更具灵活性，也方便利用CSS控制。

    + table不建议用于布局，但表现具有明显表格形式的数据，table还是首选。

- 标签通常是成对出现的，一开一关。也存在一些单标签，如：&lt;meta />、&lt;br />等。

- 标签与它的属性都必须小写。

- 所有的标签必须合理嵌套。
    > - 是这样的，标签存在一定的语义性，需要根据标签自身的属性来进行合理嵌套。

    > - 例如：&lt;p>
标签（paragraph）是用来定义段落的，就不用它来布局；像&lt;div>&lt;span>&lt;em>开开心心&lt;/span>&lt;/em>&lt;/div>是不对称的，这样是错误的。具体的基本嵌套规则

    > - 另外严禁使用修改行内元素dispaly属性来嵌套块级元素

- 结构、表现、行为三者分离，避免内联

### 元素

* html5元素

    - section 表示文档中的节、区段，可以和h1-h6一起来显示文档结构

    - article 表示一块比较独立的内容或者主题内容，块级元素，比如blog的内容，报纸的文章

    - aside 表示article以外的内容，而且应该和article有一定的关系，块级元素

    - hgroup 表示一个文档、区段(section)的标题组合

    - header 表示页眉,页头

    - footer 表示页脚

    - nav 表示导航内容

    - figure 表示以相对独立的或外引的元素，如img video

    - figcaption 表示 figure内容的标题


* 结构性元素

    - p 表示段落。只能包含内联元素，不能包含块级元素;

    - div 本身无特殊含义，可用于布局。几乎可以包含任何元素;

    - br 表示换行符;

    - hr 表示水平分割线;

    - h1-h6 表示标题。其中 h1 用于表示当前页面最重要的内容的标题;

    - blockquote 表示引用，可以包含多个段落。请勿纯粹为了缩进而使用 
    blockquote，大部分浏览器默认将 blockquote 渲染为带有左右缩进;
    
    - pre 表示一段格式化好的文本;


* 头部元素
    
    - title 每个页面必须有且仅有一个 title 元素;
    
    - base 可用场景：首页、频道等大部分链接都为新窗口打开的页面;
    
    - link link 用于引入 css 资源时，可省去 media(默认为all) 和 type(默认为text/css) 属性;
    
    - style type 默认为 text/css，可以省去;
    
    - script type 属性可以省去; 不赞成使用lang属性; 不要使用古老的<!– //–>这种hack脚本, 它用于阻止第一代浏览器（Netscape 1和Mosaic）将脚本显示成文字;
    
    - noscript 在用户代理不支持 JavaScript 的情况下提供说明;


* 文本元素
    
    - a 存在 href 属性时表示链接，无 href 属性但有 name 属性表示锚点;
    
    - em,strong em 表示句意强调，加与不加会引起语义变化，可用于表示不同的心情或语调; 
    strong 表示重要性强调，可用于局部或全局，strong强调的是重要性，不会改变句意;
    
    - abbr 表示缩写;
    
    - sub,sup 主要用于数学和化学公式，sup还可用于脚注;
    
    - span 本身无特殊含义;
    
    - ins,del 分别表示从文档中增加(插入)和删除


* 媒体元素
    
    - img 请勿将img元素作为定位布局的工具，不要用他显示空白图片; 必要时给img元素增加alt属性;
    
    - object 可以用来插入Flash;
    

* 列表元素
    
    - dl 表示关联列表，dd是对dt的解释; dt和dd的对应关系比较随意：一个dt对应多个dd、多个dt对应一个dd、多个dt对应多个dd，都合法; 可用于名词/单词解释、日程列表、站点目录;
    
    - ul 表示无序列表;
    
    - ol 表示有序列表, 可用于排行榜等;
    
    - li 表示列表项，必须是ul/ol的子元素;


* 表单元素
    
    - 推荐使用 button 代替 input，但必须声明 type;
    
    - 表单元素的 name 不能设定为 action, enctype, method, novalidate, target, submit 会导致表单提交混乱


### 属性顺序(建议)

- HTML 属性应当按照以下给出的顺序依次排列，确保代码的易读性。
    
    1.class
    
    2.id 、 name
    
    3.data-*
    
    4.src、for、 type、 href
    
    5.title、alt
    
    6.aria-*、 role

- class用于标识高度可复用组件，因此应该排在首位。id 用于标识具体组件，应当谨慎使用（例如，页面内的书签），因此排在第二位。

- 文件和目录命名约定: 一律小写，必须是英文单词或者汉语拼音，以英语单词优先，多个单词以连字符 ( - ) 连接。 只能出现小写引文字母，数字和连字符。
很多浏览器会将含有这些词的作为广告拦截： ad、ads、adv、banner、sponsor、gg、guangg、guanggao等 页面中尽量避免采用以上词汇来命名。
该命令规范适用于所有前端维护的内容和相关目录。(html, css, js, png, gif, jpg, ico)。


## 前端规范之CSS
> CSS 文件使用无 [BOM](../../#13-术语定义) 的 UTF-8 编码。适用less、sass

- css统一小写命名，使用“-”串联,例：.zm-index-articals, [命名规范参考](naming.md#11-选择器命名参考)

- 空格

    + 选择器 与 { 之间必须包含空格。(例：.selector {})

    + 属性名 与之后的 : 之间不允许包含空格， : 与 属性值 之间必须包含空格。(例：margin: 
    0;)
    
    + 列表型属性值 书写在单行时，, 后必须跟一个空格。(例：font-family: Arial, sans-serif;)
    
    + 每行不得超过 120 个字符，除非单行不可分割。
    
        > 常见不可分割的场景为URL超长。
    
        > 对于超长的样式，在样式值的 空格 处或 , 后换行，建议按逻辑分组。
    
    + &gt;、+、~ 选择器的两边各保留一个空格。
    
    + 属性选择器中的值必须用双引号包围。
    
    + 属性定义必须另起一行。
    
    + 属性定义后必须以分号结尾。

- 选择器

    + 如无必要，不得为 id、class 选择器添加类型选择器进行限定。

    + 选择器的嵌套层级应不大于 3 级，位置靠后的限定条件应尽可能精确。

    + 属性缩写

        > 在可以使用缩写的情况下，尽量使用属性缩写。
        > 使用 border / margin / padding等缩写时，应注意隐含值对实际数值的影响，确实需要设置多个方向的值时才使用缩写。


- 清除浮动

当元素需要撑起高度以包含内部的浮动元素时，通过对伪类设置 clear 或触发 [BFC](../../#13-术语定义) 的方式进行 clearfix。尽量不使用增加空标签的方式。

- !important
    
尽量不使用 !important 声明。当需要强制指定样式且不允许任何场景覆盖时，通过标签内联和 !important 定义样式。

- 值与单位
    
    - 文本
        * 文本内容必须用双引号包围。

    - 数值
        * 当数值为 0 - 1 之间的小数时，省略整数部分的 0。

    - url()

        * url() 函数中的路径不加引号。

    - 长度

        * 长度为 0 时须省略单位。 (也只有长度单位可省)

    - 大小写

        * 颜色值中的英文字符采用小写。

    - 使用CSS缩写属性

        * 去掉小数点前的“0”
            ```CSS
                font-size: .8em;
            ```
        
        * 进制颜色代码缩写
            ```CSS
                // color: #ffeeee;
                color: #fee;
            ```

- Hack

    + 需要添加 hack 时应尽可能考虑是否可以采用其他方式解决。

    + 尽量使用 选择器 hack 处理兼容性，而非 属性 hack。

    + 尽量使用简单的 属性 hack。


## 前端规范之JavaScript

### 命名规范

- 文件命名可读性强:文件夹、文件的命名与命名空间应能代表代码功能，可读性强。

- 函数、变量命名: 统一驼峰命名方式，私有方法添加“_”,例：_formatSaleInfo,API接口参数则与server端保持一致

- 句末必须用分号结尾

- if、while、for、do语句的执行体总是用"{"和"}"括起来，即使在其结构体内只有一条语句

- 单行过长应在适当位置予以换行,增强可读性

- if 语句括号中的条件若过多过长，应予以折行；折行后，||、&& 等符号应与 “(” 后的第一个字母纵向对齐

- 语法意义相互独立的代码将用空行分隔

- 不要使用with语句

- 不要在循环里面进行DOM操作

- 对于多个同性质同辈节点，避免逐个进行事件绑定。而应该利用冒泡原理，将事件委托给父节点。

- 事件委托要接近事件触发节点，避免将所有事件冒泡委托给body节点

- 通常能用CSS实现的效果要避免使用JS来实现。CSS性能比JS要高。

- JS要避免直接写在页面中，加快页面加载速度。

- 变量需要在被使用前申明

- 在开发中，简单的操作能用原生js实现的方式，尽量不要用三方的插件或者库实现

- 减少全局污染


### 注释规范

- 注释语句不要跟在代码同一行后面，要在代码行上一行位置

- 申明的变量(除for循环里面的循环次数控制变量)、方法（包括匿名方法）、对象，对象属性、插件、API、代码块（for循环，if...else...）等都需要有注释来解释
    ``` javascript
        // 这是一个计数器
        var count = 10;
    ```

- 单行注释或多行注释之前空一行
    ``` javascript
        function aFun() { 

            // 注释...
            ......  
        }
    ```
    
- 单行注释//后空一格
    ``` javascript
        // Single-line comment
    ```

- 文件头部、多行注释
    ``` javascript
         /*
         * @Author: 没头脑 
         * @Date: 2017-03-10 00:00:00 
         * @Last Modified by: 不开心
         * @Last Modified time: 2017-03-10 00:00:00 
         * @Description: 描述
         */
    ```

### 代码格式化规范

- 方法、对象、循环等开始“{”要跟在方法、对象、循环等起始行的最后面，不要另起一行写，但如果是数组项是对象，那“{”要另起一行
    ``` javascript
        function getData() {
            return {
                title: "Hello JavaScript",
                author: "Andy Cheng"
            }
        }
    ```

    ``` javascript
        var arr = [
            {
                title: "Hello JavaScript",
                author: "Andy Cheng"
            },

            ...
        ]
    ```

- 使用 分号“;"结束代码语句，函数声明、if、for语句结尾不加分号
    ``` javascript
        var name = "Nicholas";

        function sayName() {
            console.log(name);
        }   

        if(name == 'andy'){
            ...
        }
    ```

- 结合别人代码的时候: 发现他人有不加分号的特点的时候, 自己在在语句前面加分号
``` javascript
        ;(function($) {
             // 其他语句 ...
        })(jQuery);

        ;++a; 
    ```

- 同一行方法调用或者表达式换行时，一定要在一个运算符或标点后进行换行
    ``` javascript
        if (isLeapYear && isFebruary && day == 29 && itsYourBirthday &&
                noPlans) {
            waitAnotherFourYears();
        }   
    ```

- 每个方法之间空一行
    ``` javascript
        function aFun() {
            ...
        }

        function bFun() {
            ...
        }   
    ```

- 在方法的局部变量声明和方法的语句之间空一行
    ``` javascript
        function aFun() {
            var a = ...;
            var b = ...;

            ...
        }   
    ```

- 运算符前后添加空格
    ``` javascript
        var found = (values[i] === item);  
    ```

- 字符串申明统一使用双引号，如果字符串长度过长，请换行并使用“+”号进行字符串连接
    ``` javascript
        var longString = "Here's a story of a man " +
            "named Brady.";
    ```

- 所有属性的值都要对应一个没有引号的属性名，属性名后紧跟一个冒号（不加空格），冒号后加一个空格跟属性的值
    ``` javascript
        var book = {

            title: "Hello JavaScript",
            author: "Andy Cheng"
        };
    ```

- 如果这个属性是方法，他的上下跟着不是方法的属性，上下均要空一行；一组相关的属性后可适当插入一个空行，增加可读性
    ``` javascript
        var object = {

            key1: value1,
            key2: value2,

            func: function(){
                // do something
            },

            key3: value3
        }; 
    ```

- 结束的大括号应该独占一行
    ``` javascript
        var book = {

            title: "Hello JavaScript",
            author: "Andy Cheng"
        }; 
    ```

- 一个对象字面量作为一个参数传入方法中,开始花括号{与调用的方法名同行，属性按键值对方式，单独一行，结束花括号}单独一行
    ``` javascript
        doSomething({
            key1: value1,
            key2: value2
        }); 
    ```

- 一个逻辑代码块之前空一行
    ``` javascript
        function aFun() { 

            if (s.hasOwnProperty(p)) {

                if (merge && type == 'object') {
                    Y.mix(r[p], s[p]);
                } else if (ov || !(p in r)) {
                    r[p] = s[p];
                }
            }
        } 
    ```

- 对于多层嵌套的if语句，要进行合并
    ``` javascript
        if (x != null && x === 2) {
            ... 
        } 
    ```

- js文件行数不要太长，最大行数为1000行

- js方法行数不要太长，最大行数为100行

- 一行的结尾处不要使用空格字符

- 只有while, do, for语句才能使用标记
    ``` javascript
        doSomething();
            if(i === 8){
                break myLabel;
            }
        } 
    ```

- 控制流申明if, for, while, switch, try不要嵌套太多层,最多3层

- 字面量布尔值不能使用在条件表达式里面
    ``` javascript
        if (booleanVariable) { /* ... */ }
        if (!booleanVariable) { /* ... */ }
        if (booleanVariable) { /* ... */ }
        doSomething(true);
    ```


- 当实现某个方法需要使用大量参数的时候，要将该功能封装成一个对象，以配置方式传入参数，而不是写在方法参数里面，方法的最大参数长度为7

- 使用面向对象的方式组织js代码
    ``` javascript
        var cat = {
            name: '',
            color: ''
        }; 
    ```

###  代码防错(陷阱)

- 不要进行浏览器嗅探方式判断浏览器客户端版本等信息，请使用特性检测，同时避免使用三方非特性检测方式判断浏览器客户端
    ``` javascript
        // 错误示例
        ie=!!window.VBArray
        ie678=('a-b'.split(/(~)/))[1]=="b"
        ie678=0.9.toFixed(0)=="0"
        iphone=/iphone/i.test(navigator.userAgent);
        $.browser == ...
    ```

- 尽量避免申明全局变量，防止全局空间命名冲突污染

- 不要用null来判断方法的参数有没有提供，不要用null来判断未初始化的变量
    ```javascript
        // 错误示例
        var person;
        if (person != null) {
            doSomething();
        }
    ```

- 变量定义在变量声明时进行初始化，未初始化的变量放在声明语句的最后
    ```javascript
        function doSomethingWithItems(items) {

            // 申明并赋值 
            var value = 10,

            result = value + 10，
            i, len;
            for(i=0, len=items.length; i < len; i++) {
                doSomething(items[i]);
            }
        }
    ```

- 不要使用“,”逗号来结束语句
    ```javascript
        var settings = {
            'foo'  : oof,
            'bar' : rab
        };
    ```

- switch至少要包含3个case，语句需要以default语句结束， 每个case都需要使用break结束
    ```javascript
        switch (param) {
            case 0:
                doSomething();
                break;
            case 1:
                doSomethingElse();
                break;
            default:
                error();
                break;
        }
    ```

- 方法体作为参数使用时，要保持与申明的方法在同一行
    ```javascript
        var fn = function () {
           //...
        }(function () { // 在同一行
           //...
        })();
    ```

- 对于对象属性使用for ... in循环时，需要通过hasOwnProperty方法过滤非自身属性(继承而来的属性)
    ```javascript
        for (name in object) {
            if (object.hasOwnProperty(name)) {
                doSomething(name);
            }
        }
    ```

- 不要使用位运算符：<<, >>, >>>, ~, &, |
    ```javascript
        // 错误示例
        
        // & 使用错误
        if (a & b) { ... } 

        //  有比这更清晰的方式验证
        var oppositeSigns = ((x ^ y) < 0); 
    ```

-  构造函数不要单纯在未申明实例的情况下使用
    ```javascript
        //  something引用实例
        var something = new MyConstructor();
    ```

- 不要在循环体内部定义方法
    ```javascript
        var funs = [];
        for (var i = 0; i < 13; i++) {
            funs[i] = function() { 
                return i;
            };
        }
        print(funs[0]()); // 13 而不是 0
        print(funs[1]()); // 13 而不是 1
        print(funs[2]()); // 13 而不是 2
        print(funs[3]()); // 13 而不是 3
    ```

- 不要定义重复名称的方法

- return跳转语句后面不要接其他语句
    ```javascript
        //  错误示例
        function(a) {
            var i = 10;
            return i + a;
            i++;
        }
    ```

- 方法中未被使用的参数要被移除
    ```javascript
        //  错误示例
        function doSomething(a, b) { // "a" 未被使用
            return compute(b);
        }
    ```

- 未被使用的变量要被删除
    ```javascript
        //  错误示例
        function numberOfMinutes(hours) {
            var seconds = 0;   // seconds 未被使用
            return hours * 60;
        }
    ```


### 用户体验及安全性规范
- 生产环境下不要使用alert(...)方式提示信息
    > 生产环境下不要使用alert(...)方式提示信息，因为这种方式对用户体验不好，并且会阻碍后续程序的执行，还可能把敏感信息暴露给攻击者。可以使用自定义弹出框提示或者其他方式提示。开发环境下可以使用

- 生产环境下不要使用debug语句
    > 生产环境下不要使用debug语句，因为容易在出现异常情况下给用户提示其无法理解的内容，也容易被攻击。
