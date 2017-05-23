# 切图规范

## 切图工具
- **推荐工具：** [cutterman](http://www.cutterman.cn/zh/cutterman)

## 常用图片格式介绍
| 格式      |    介绍 |
| :--------: | --------|
| jpg  | jpg全名是JPEG。JPEG图片以 24 位颜色存储单个位图。 |
| png8  | 只支持像素索引的透明的图片格式 |
| png24  | 支持alpha半透明的图片格式 |
| gif  | 支持动画的图片格式，透明方式和png8一样 |
| svg  | 可缩放矢量图形是基于可扩展标记语言（标准通用标记语言的子集），<br>用于描述二维矢量图形的一种图形格式。 |
| 其他  | bmp,tiff,pcx,tga,exif,fpx,psd,cdr,pcd,dxf,ufo,eps,ai,raw,WMF |

**总结**
* 色彩丰富的、大的图片切成jpg的；

* 尺寸小的，色彩不丰富的和背景透明的切成gif或者png8的；

* 半透明的切成png24。 

## 切图原则
- 选择合适的图片格式
- 站在开发的角度切图
- 选择正确的尺寸：图片是多大就切多大，切忌为了占位而把多余的空白切进去,切图资源尺寸必须为双数
- IOS图片选择规格有2x,3x,对应像素为640x960px，640x1136px，750x1334px，1242x2208px
- Andriod图片规则480x800px，720x1280px，1080x1920px
- web图片规则原则上是pc、pad、mobile单独切，另外移动设备上面针对retina显示屏的需要切双倍像素
- 对于阴影、圆角、边框、背景色
    + web端如无特别要求，一律不切，但是需要依据规范标注清楚
    + IOS和Andriod端根据实际需求切，目前是全部都在切
- 在兼容低版本浏览器时，切背景图片需要遵循[“点九”](https://www.baidu.com/link?url=gWfllR2sgveq4m5MFbArtPpuls-ZEnk4_e0urtVJ8HM5PpYXILs0AKiHQRCxHXvYW4rorTWU2AG-1mvGuwQiNEb2imQiSJQzTJqxo3DHZ4_&wd=&eqid=8edb5298000069c0000000055923d974)原则
- 切背景图时，针对纹理清晰，可平铺的背景，只需切一小块即可
- 在不损失视觉效果的情况下，尽可能的[压缩图片](https://tinypng.com/)大小
- 将小图标拼合成[雪碧图](http://www.imooc.com/learn/93)

## 命名规范
命名规则可参考[CSS/文件命名参考](/standard/fe/naming.md)。

### 文件夹命名规范
- 所有文件/文件夹都必须使用小写英文字母命名，单词之间使用“_”下划线连接，例：
```
    // 按页面/功能区命名
    index
    product
    about_us
    ...

    // 按模块命名
    common
    signup
    components
    ...
```
- 每个项目都应该有独立的项目文件夹
- 公共组件应该有单独的文件夹
- 每个模块或者页面都应该有单独文件夹

### 文件命名规范
- 所有文件/文件夹都必须使用小写英文字母并且按照页面/模块+图片名称的方式命名，单词之间使用“_”下划线连接，以图片的宽高结尾，例：
```
    // 按页面+功能区+宽高命名，宽高用小写字母x来串联
    index_banner_960x350.jpg

    // 按模块+功能+宽高命名
    signup_notice_120x60.png

    // IOS命名
    common_banner_100x100.png
    common_banner_100x100@2x.png
    common_banner_100x100@3x.png

    // 按状态命名
    btn_primary_default_60x60.png
    btn_primary_hover_60x60.png
    btn_primary_active_60x60.png
    btn_primary_disabled_60x60.png
```
