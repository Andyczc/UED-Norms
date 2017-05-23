# UI设计规范

## 设计原则
设计规范要根据公司切实可行的方式进行设计整理，切勿流于形式。
- **产品** ：充分理解清楚产品核心与战略定位
- **用户** ：充分考虑用户在软件产品上的认知深度以及使用场景
- **市场** ：了解目前市场上同类型产品的设计方式
- **风格** ：风格统一的设计方式（排版、配色、组件、交互方式等）
- **视觉** ：设计稿应该有层级清晰的信息点

总结起来就是一句话：一个布局、风格具有简约美，同时又能提供大量有价值信息的网站必定受用户欢迎。

## 通用规范
### 屏幕适配
不同的分辨率下用户对我们的APP具有明显的感观差异，主流分辨率的更新迭代却又完全独立于App进行。
这让我们想要使App在绝大多数主流电脑/平板/手机上都保持感观、体验的一致性提出了很大的挑战。

### 主流浏览器的界面参数与份额
360浏览器份额为粗略统计（2017年4月）

| 浏览器      |    状态栏 |    菜单栏 |    滚动条 |    市场份额(国内) |
| :--------: | :--------:| :--------:| :--------:| :--------:|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/google.png)<br>Chrome     | 22px（浮动出现）| 60px | 15px | 41.62% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/huofu.png)<br>火狐     | 20px| 60px | 15px | 2.04% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/ie9.png)<br>IE     | 24px| 60px | 15px | 27% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/360.png)<br>360      | 24px| 60px | 15px | 28% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/qq.png)<br>QQ      | 24px | 60px | 15px | 6% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/aoyou.png)<br>遨游     | 24px| 60px | 15px | 1% |
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/sougou.png)<br>搜狗     | 25px | 60px | 15px | 4.47% |

### 系统分辨率统计

| 分辨率      |    占有率  |    分辨率    |    占有率 |
| :--------: | :--------:| :--------:| :--------:|
| 1920×1080  | 13.8%    | 1366×768 | 10.2% | 
| 360×640 | 7.9%    | 1440×900 | 7.7% | 
| 720×1280  | 6.4%   | 1024×768| 5.1% | 
| 320×568  | 3.7%    | 1600×900 | 3.5% | 
| 1080×1920  | 3.3%   | 375×667 | 3.2% | 

### iPhone界面尺寸

| 设备      |    分辨率  |    PPI    |    状态栏高度  |    导航栏高度  |    标签栏高度  |
| :--------: | :--------:| :--------:| :--------:| :--------:| :--------:|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPhone6P、6SP、7P  | 1242×2208 px   | 401PPI | 60px | 132px | 146px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6.png)<br>iPhone6 - 6S - 7  | 750×1334 px    | 326PPI | 40px | 88px | 98px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_5.png)<br>iPhone5 - 5C - 5S  | 640×1136 px    | 326PPI | 40px | 88px | 98px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_4.png)<br>iPhone4 - 4S  | 640×960 px   | 326PPI | 40px | 88px | 98px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_3.png)<br>iPhone & iPod Touch前三代 | 320×480 px    | 163PPI | 20px | 44px | 49px|

![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iph.png)
> 可以通过鼠标右键选择新窗口打开查看清晰图片

### iPhone图标尺寸

| 设备   |  App Store  |  程序应用 |  主屏幕  |  Spotlight搜索  |  标签栏 | 工具栏和导航栏|
| :--------: | :--------:| :--------:| :--------:| :--------:| :--------:| :--------:|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPhone6P - 6SP - 7(@3×)  | 1024×1024 px   | 180×180 px | 114×114 px | 87×87 px | 75×75 px| 66×66 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6.png)<br>iPhone6 - 6S - 7 (@2×)  | 1024×1024 px   | 120×120 px | 114×114 px | 58×58 px | 75×75 px| 44×44 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_5.png)<br>iPhone5 - 5C - 5S (@2×)  | 1024×1024 px    | 120×120 px | 114×114 px | 58×58 px | 75×75 px| 44×44 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_4.png)<br>iPhone4 - 4S (@2×) | 1024×1024 px   | 120×120 px | 114×114 px | 58×58 px | 75×75 px| 44×44 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_3.png)<br>iPhone & iPod Touch前三代 | 1024×1024 px    | 120×120 px | 57×57 px | 29×29 px | 38×38 px| 30×30 px|

![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iph-ico.png)

### iPad的设计尺寸

| 设备      |    尺寸  |    分辨率    |    状态栏高度  |    导航栏高度  |    标签栏高度  |
| :--------: | :--------:| :--------:| :--------:| :--------:| :--------:|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad 3 - 4 - 5 - 6 - Air - Air2 - mini2  | 2048×1536 px   | 264PPI | 40px | 88px | 98px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad 1 - 2  | 1024×768 px   | 132PPI | 20px | 44px | 49px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad 3 - 4 - 5 - 6 - Air - Air2 - mini2  | 2048×1536 px   | 264PPI | 40px | 88px | 98px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad Mini  | 1024×768 px   | 163PPI | 20px | 44px | 49px|

![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/ipa.png)

### iPad图标尺寸

| 设备   |  App Store  |  程序应用 |  主屏幕  |  Spotlight搜索  |  标签栏 | 工具栏和导航栏|
| :--------: | :--------:| :--------:| :--------:| :--------:| :--------:| :--------:|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad 3 - 4 - 5 - 6 - Air - Air2 - mini2  | 1024×1024 px   | 180×180 px | 114×114 px | 100×100 px | 50×50 px| 44×44 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad 1 - 2  | 1024×1024 px   | 90×90 px | 72×72 px | 50×50 px | 25×25 px| 22×22 px|
| ![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/iphone_6p.png)<br>iPad Mini  | 1024×1024 px   | 90×90 px | 72×72 px | 50×50 px | 25×25 px| 22×22 px|

![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/ipa-ico.png)

### 分辨率对应DPI
| 分辨率  |    DPI    |
| -------- | :--------:|
| HVGA 480*320   | mdpi |
| WVGA 800*480   | hdpi |
| FWVGA 854*480   | hdpi |
| QHD 960*540   | hdpi |
| 720P 1280*720   | xhdpi |
| 1080P 1920*1080   | xxhdpi |
| 4K 3840×2160   | xxxhdpi  |

### Android SDK模拟机的尺寸
| 屏幕大小  |  低密度（120） |  中等密度（160） |  高密度（240） |  超高密度（320）|
| -------- | :--------:|
| 小屏幕   | QVGA（240×320） |    |   480×640 | |
| 普通屏幕   |  WQVGA400（240×400）<br> WQVGA432（240×432) |  HVGA（320×480）  |  WVGA800（480×800）<br> WVGA854（480×854）<br> 600×1024 | 640×960|
| 大屏幕   |  WVGA800 *（480×800）<br> WVGA854 *（480×854）     |  WVGA800 *（480×800）<br> WVGA854 *（480×854）<br> 600x1024  |    |    |
| 超大屏幕   |  1024×600 |  1024×768<br> 1280×768WXGA（1280×800）  |  1536×1152 <br>1920×1152 <br>1920×1200 | 2048×1536 <br>2560×1600|

### Android安卓系统dp/sp/px换算表

| 名称  | 分辨率  | 比率 rate (针对320px) | 比率 rate (针对640px)  | 比率 rate (针对750px)|
| :--------: | :--------:| :--------:| :--------:| :--------:|
| idpi  | 240×320   | 0.75 | 0.375 | 0.32 | 
| mdpi  | 320×480   | 1 | 0.5 | 0.4267 | 
| hdpi  | 480×800   | 1.5 | 0.75 | 0.64 | 
| xhdpi  | 720×1280   | 2.25 | 1.125 | 1.042 | 
| xxhdpi  | 1080×1920   | 3.375 | 1.6875 | 1.5 | 

### 主流Android手机分辨率和尺寸
| 分辨率  | 尺寸  | 设备 |
| :--------: | :--------:| :--------:|
| 4.4英寸 | 800×1280 px | 魅族MX2 |
| 4.7英寸 | 1080×1920 px | HTC One M8 |
| 4.3英寸 | 720×1280 px | 小米M2S |
| 5英寸 | 1080×1920 px | 小米M3S<br> 小米M3<br> 小米M4<br> OPPO N1 Mini<br> 华为荣耀6 |
| 5.1英寸 | 1080×1280 px | 魅族MX3<br> 三星GALAXY S5 |
| 5.2英寸 | 1080×1920 px | 索尼Xperia Z3 |
| 5.5英寸 | 720×1280 px | HTC Desire 820<br> OPPO Find 7<br> LG G3<br> OPPO R3<br> 魅族MX4 Pro<br> 三星GALAXY Note II<br> 小米红米Note<br> OnePlus One |
| 5.7英寸 | 1440×2560 px | 三星GALAXY Note 4<br> 三星GALAXY Note 3 |




### WEB端适配选择
#### 非响应式网页设计
- **分辨率**：应该从1024、1280+的总分辨率来设计，并且要充分考虑`滚动条、菜单栏、工具栏`的视觉效果


#### 响应式网页设计
- **简约**： 不仅仅是较少的设计元素，更是要求整个页面有简单清晰的页面布局，不使用复杂的交互动画等


### IOS端适配选择
- **2x,3x：** 480x800px，720x1280px，1080x1920px


### 安卓端适配选择
- **xhdpi：** 640x960px，640x1136px，750x1334px，1242x2208px

### 鼠标/手势切换状态
- **a:link:** 默认状态
- **a:hover:** 鼠标悬浮时的状态
- **a:active:** 鼠标按下的状态
- **a:visited:** 鼠标按下的状态
- **input:focus:** 表单元素获得焦点
- **input:blur:** 表单元素失去焦点
- **disabled:** 禁用表单元素
- **readonly:** 表单元素为只读状态

手势状态暂缺

### 信息/表单状态
- **sucess:** 成功，或者验证通过，多用于对表单的`输入内容进行实时验证或者将API接口操作的结果状态提示给用户`
- **warning:** 提醒，或者警告，多用于`用户不输入表单内容点击提交，或者我们主动提示给用户`
- **error:** 错误，或者报错，多用于`用户输入错误表单内容、软件异常、或者提交表单服务端报错`
- **info:** 信息，多用于`正常的用户提示，产品介绍`
- **danger:** 非常严重的错误，多用于`APP死循环、异常退出、内存泄漏等极端情况`，一般错误信息用`error`

**示例：**

![Image text](https://raw.githubusercontent.com/Andyczc/ued-norms-images/master/info-status.png)

### 控件尺寸
- 常规做法是准备三套尺寸：large、normal、small,除了相同的`文字字体，颜色，边框，背景色`等，区别在不同的`文字大小、间距、行高、圆角、阴影`等。

## 设计规范
所有设计师应严格安装工作流程进行设计。

#### 设计初期
接收到原型后，相关设计师需认真阅读原型文档，并做到以下几点:
+ 充分了解产品原型的架构、功能、相关流程图与说明文档
+ 梳理原型中所需的控件，如果产品经理有梳理出一份则自己也要检查确认一遍
+ 了解竞品，理解产品交互
+ 由设计主管或者负责人整理出设计草案或风格参考方向，然后UED内部进行讨论，确定方案的可行性，并预估出设计人员与时间
+ 准备2-3个初稿方案，与总经办(新项目立项时)或产品经理进行沟通，根据沟通结果优化设计稿，直到通过为止
+ 在设计布局与功能控件时，针对原型设计不合理或者调整对应位置与原型相差比较大的情况，需先与产品经理沟通确认，如果沟通结果不理想，可以找到UED主管协调
+ 输出`components(组件)`、`index(主页)`文档，格式为PSD或者jpg，交于总经办或产品经理评审，并根据评审结果修改设计稿，直到通过为止。

#### 设计中期
主设计稿或主框架通过评审以后，由设计主管或者负责人对剩下的工作进行合理分配。设计成员需严格基于主框架等设计稿的基础上做二次设计，在设计过程中如遇到无法解决的问题，或功能控件不包含的样式需与UI主管协商后再进行设计。
- 对于平台产品，Web端应按照组件化设计原则，设计师只需要对具体的功能模块进行设计，不用给出所有的框架结构，但是在存放文档时要目录清晰
- APP端需按照原型结构目录完成所有效果图设计
- 模块设计完成后，需对当前模块进行整理，并生成对应的《效果图对应目录》文档

#### 设计后期
待所有的功能都设计完成以后，我们需要对设计稿进行梳理，简历相关文档。
- 输出完整的`《源文件文档》`，并按照分类决定是否上传到SVN版本库（官网这类偏展示型的，PSD文档不多的需放到SVN版本库，平台型的设计稿只需要将主框架和组件源文档加入版本库
- 输出完整的`《标注文档》`，目录结构应该与源文件一致
- 输出`《切图文档》`，若有必要一并给出`《图标库文档》`
- 输出完整的`《效果图文档》`，目录结构应该与源文件一致
- 将文档加入svn版本库并上传

## 组件化设计
一套完整的组件库，应该是主流的组件库与自己产品的结构结合的产物。下面是基础组件列表

| 组件名称      |    组件名称  |   组件名称  |   组件名称  |
| :--------: | :--------:| :--------:| :--------:|
|  主框架 | 栅格系统  | 配色版  |  标题  |
|  列表 | 表格  | 状态  |  表单  |
|  按钮/按钮组 | 尺寸  | 图片  |  情境文本颜色/背景色  |
|  按钮式下拉菜单 | 导航  | 图标字体库  |  分页  |
|  按钮式下拉菜单 | 导航  | 图标字体库  |  分页  |
|  进度条 | 模态框  |  ... | ...  |


## 建议
**不会做饭的裁缝不是个好司机**，下面是一些推荐给设计师们可以去经常逛逛的网站,记得选择科(fan)学(qiang)上网方式。
- [科学上网](https://github.com/getlantern/forum)
- [themeforest](https://themeforest.net)
- [dribbble](https://dribbble.com/)
- [CSS](http://www.w3school.com.cn/css/index.asp)
- [CSS3](http://www.w3school.com.cn/css3/index.asp)
- [HTML](http://www.w3school.com.cn/html/index.asp)
- [HTML5](http://www.w3school.com.cn/html5/index.asp)