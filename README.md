## EasyImage 简单图床 2.0
> 始于2018年7月，支持多文件上传,简单无数据库,返回图片url,markdown,bbscode,html的一款图床程序
演示地址：[https://img.545141.com](https://img.545141.com) 
之前一直用的图床程序是:[PHP多图长传程序2.4.3](https://www.jb51.net/codes/40544.html)
由于版本过老并且使用falsh上传，在当前html5流行大势所趋下，遂利用基础知识新写了一个以html5为默认上传并且支持flash,向下兼容至IE9。
>

[演示](https://img.545141.com) &nbsp;
[Chrome 拓展](https://github.com/icret/EasyImage-Browser-Extension) &nbsp;
[使用手册](https://www.kancloud.cn/easyimage/easyimage) &nbsp;
[问题反馈](https://support.qq.com/products/367633) &nbsp;
[QQ群](https://shang.qq.com/wpa/qunwpa?idkey=3feb4e8be8f1839f71e53bf2e876de36afc6889b2630c33c877d8df5a5583a6f)

[![PHP](https://img.shields.io/badge/PHP->=5.6-orange.svg)](http://php.net)
[![Release](https://img.shields.io/github/v/release/icret/EasyImages2.0)](https://github.com/icret/EasyImages2.0/releases)
[![Issues](https://img.shields.io/github/issues/icret/EasyImages2.0)](https://github.com/icret/EasyImages2.0/issues)
[![stargazers](https://img.shields.io/github/stars/icret/EasyImages2.0)](https://github.com/icret/EasyImages2.0/stargazers)
[![Code size](https://img.shields.io/github/languages/code-size/icret/EasyImages2.0?color=blueviolet)](https://github.com/icret/EasyImages2.0)
[![License](https://img.shields.io/badge/license-GPL_V3.0-yellowgreen.svg)](https://github.com/icret/EasyImages2.0/blob/master/LICENSE)

>本人善写bug 发现bug可提交 [Issues](https://github.com/icret/EasyImages2.0/issues) 追求稳定请下载 [稳定版](https://github.com/icret/EasyImages2.0/releases)
<hr />

#### 功能支持：

- [x] 支持仅登录后上传
- [x] 支持设置图片质量
- [x] 支持上传图片转换为指定格式
- [x] 支持文字/图片水印
- [x] 支持设置图片指定宽/高
- [x] 支持限制最低宽度/高度上传
- [x] 支持设置广告
- [x] 支持自定义
- [x] 支持图片监黄
- [x] 支持API
- [x] 在线管理图片
- [x] 支持网站统计
- [x] 支持更多···

#### 界面演示

![简单图床 - 上传界面](https://i1.100024.xyz/i/2020/12/31/ulmtho.png)
![简单图床 - 广场界面](https://i1.100024.xyz/i/2020/12/31/2.png)
![简单图床 - 后台界面](https://i1.100024.xyz/i/2020/12/31/3.png)
![简单图床 - 统计界面](https://i1.100024.xyz/i/2020/12/31/4.png)

#### 使用注意：

1. 请将所有文件赋予0755权限或www权限
2. 可以使用浏览器的 F12调试模式->console查看错误
3. 如果对php不太熟悉的话，不要将图床程序放置于二级目录
4. 宝塔面板请关闭防跨站或删除域名文件夹内的user.ini文件
5. 第一使用会执行安装程序并生成install.lock，如果出错可以删除install目录
6. 网站域名与图片域名必须填写，如果只有一个域名请填写成一样的
7. 安装成功后务必修改默认密码
8. 第一次访问会检查环境并在config目录下生成EasyImage.lock

#### 安全配置

- Apache环境在上传目录添加配置文件.htaccess，使上传目录不可运行PHP程序（默认存在)

```Apache
<FilesMatch "\.(?i:php|php3|php4|php5)">
Order allow,deny
Deny from all
</FilesMatch>
```
- Nginx环境限制上传目录禁止运行PHP程序：

```Nginx
 # 禁止运行php的目录
    location ~* ^/(i|public|config)/.*\.(php|php5)$
    {
     deny all;
    }
```
 - 或者参考：[https://www.545141.com/981.html](https://www.545141.com/981.html)

 #### 程序升级

- 保存config目录和上传目录
- 将新程序下载至网站目录解压覆盖，然后将保存的文件替换既完成升级

<details><summary><mark><font color=darkred>点击查看2.0版更新日志</font></mark></summary>


* 2022-1-3 v2.4.4 beta
- 增加后台设置提示
- 增加更改网站配色
- 增加以源文件名称命名
- 增加两种缩略图生成方式
- 修复开启前端压缩导致的上传图片异常

* 2021-12-25 v2.4.4
- 更改favicon.ico
- 修复缩略图数量统计
- 增加缩略图生成开关
- 日志增加更多文件信息
- 前端增加裁剪和压缩质量
- 上传失败将会输出更多信息
- 修复前端压缩图片不能关闭问题
- 修复上传设置中错误和页面显示
- 调整网站设置->上传设置的排序
- 将快捷操作中心转移到网站设置中
- 修复因生成缩略图导致的前端数据返回失败
- 增加简单图床chrome浏览器插件，可自行配置网站->[EasyImage-Browser-Extension](https://github.com/icret/EasyImage-Browser-Extension)

* 2021-11-17 v2.4.3
- 增加登录验证码
- 二级目录安装
- 一些优化

* 2021-11-14 v2.4.2
- 增加上传日志

* 2021-11-12 v2.4.1
- 增加缓存周期配置
- 增加上传统计
- 增加viewjs
- 更新依赖件
- 修复统计错误


* 2021-11-9 v2.4.0
- 增加统计缓存
- 增加最近30天上传统计与占用空间图表
- 增加初始化安装（可能会不支持二级目录安装，可删除install文件夹初始化)
- 增加在线编辑配置(之前是需要修改config.php文件，现在可以直接网站端修改了)
- 删除广场会导致浏览速度变慢的代码
- 删除快捷配置会导致浏览速度变慢的代码


* 2021-11-3 v2.3.2
- 增加广场图片缓存
- 重构广场样式

* 2021-11-3 v2.3.1
- 增加监黄接口
- 增加审核违规图片
- 修复对php5.6的支持
- 修复二级目录的安装

* 2021-10-24 v2.3.0
- 将服务器环境监测改为第一次打开时自动检测（如需再次展示需删除config目录下的EasyImage.lock）
- 增加快捷操作中心显示服务信息
- 增加对上传文件的命名方式（详见config.php文件里的注释）
- 增加隐私政策、服务条款、DMCA
- 增加自定义静态文件CDN源
- 增加dns-prefetch
- 删除了tinyfilemanager文件管理（感觉没什么用）
- 一些bug得以修复

* 2021-5-22 v2.2.0
- 增加根目录静态属性
- 增加浏览页面懒加载
- 增加浏览页面启用选定日期查看图片
- 增加版本检测 ***每月10日06点和25日01点检测Github是否更新***
- 增加上传压缩 ***此压缩有可能使图片变大！特别是小图片 也有一定概率改变图片方向***
- 增加批量压缩目录 ***TinyImag或本机压缩，本机压缩出现的问题***
- 修复title
- 修复二级目录安装
- 修复对PHP5.6的兼容 ***建议使用php7.0及以上！***


* 2021-5-8 v2.1.1
- 修复上传界面上传失败提示信息bug
- 浏览页面重构
- 删除页面添加登录删除
- 调整首页显示
- 将调整图片长宽放置前端，减小资源开销
- 其他小调整

* 2021-5-2 v2.1
- 将tinyfilemanager配置文件简单翻译并集成到config.php
- 增加底部自定义信息
- 增加检测PHP环境，给与提示
- 增加删除图片url（服务器不会保存删除链接）
- 恢复随机浏览20张上传图片 可以设定浏览数量和关闭浏览
- - 随机浏览图片可以在线删除
- 可以使用 https://img.545141.com/libs/list.php?num=100 定义浏览数量
- 修复一些调用
- 更改二维码显示方式
- 开启api 需要token验证上传
- 重构并修复check.php相关文件
- 重构部分代码
- 更改目录结构
- 增加安全性配置
- * Apache配置文件默认设置上传目录不可运行 

```Apache
RewriteEngine on RewriteCond % !^$
RewriteRule i/(.*).(php)$ – [F]
RewriteRule public/(.*).(php)$ – [F]
RewriteRule config/(.*).(php)$ – [F]
```

- * Nginx请在Nginx配置：

```Nginx
 # 禁止运行php的目录
    location ~* ^/(i|public|config)/.*\.(php|php5)$
    {
     deny all;
    }
```
- - 或者参考：https://www.545141.com/992.html https://www.545141.com/939.html
- 一些精简

* 2021-4-14 v2.0.2.1 Dev1
- 更新静态文件版本
- 请所有更新过2.0.2.1版本升级到此版本
- 更改一些描述
- md5提交登录验证
- 登录上传也显示公告

* 2021-03-28 v2.0.2.1
- 更新管理程序，修复部分漏洞
- 修复不能等比例缩小图片 
- 支持php8

* 2019-6-26 v2.0.2.0
- 精简压缩代码，使得不再压缩后反而变大
- 删除异域上传功能，不再支持异域上传
- 修复开启登录后无法粘贴密码
- 后台控制上传数量,上传格式
- 其他一些优化

* 2019-6-14 v2.0.1.9
- 增加复制链接按钮
- 增加暂停上传按钮
- 增加QQ截图，剪切板上传
- 增加文字/图片水印透明度
- 恢复开启/关闭api上传
- 恢复支持水印文字颜色
- 恢复支持远程上传图片
- 修复安装时候的权限
- 修复管理无法多选的问题
- 修复上传透明png背景变为纯黑的问题
- 修复成功上传图片但前端无法获取链接
- 修复在centos64 lnmp1.6 php7.1环境下的图片信息读取问题
- 修改图片压缩方式，速度更快，相比之前提高5倍以上
- 更改管理路径
- 更改上传路径，文件名更短
- 更改上传显示方式为缩略图
- 关闭添加图片后自动上传
- 纪念一下2019年，将版本号改为2.0.1.9

* 2019-5-23 v2.0
- 在继承上个版本（1.6.4）的基础上进行了全新优化
- 修复上传经常失败的问题
- 删除一些不常用但会增加功耗的过程
- 全新的压缩 将文件继续缩小
- 全新的目录系统，精简代码
- 设置仅允许在config.php修改，注释更加明了，即使没有代码基础也可以操作
- 增加新的文件管理系统，感谢 tinyfilemanager
- ~~支持文字/图片水印 可自定义文字颜色~~
- ~~支持文字水印背景颜色~~
- ~~支持文字水印透明度~~
- ~~支持删除远程上传文件~~ -> 不再支持删除远程文件
- ~~(支持开启/关闭api自定义文字水印)~~
- ~~支持删除自定义删除图片(仅管理员)~~
</details>

<details><summary><mark><font color=darkred>与1.6.4版本差别</font></mark></summary>

- 在继承上个版本（[1.6.4](https://github.com/icret/easyImages "1.6.4")）的基础上进行了全新优化
- 修复上传经常失败的问题
- 删除一些不常用但会增加功耗的过程 （删除的在下边会有标记）
- 全新的压缩 将文件继续缩小
- 全新的目录系统，精简代码
- 设置仅允许在config.php修改，注释更加明了，即使没有代码基础也可以操作
- 增加新的文件管理系统，感谢 tinyfilemanager
- ~~支持文字/图片水印 可自定义文字颜色~~
- ~~支持文字水印背景颜色~~
- ~~支持文字水印透明度~~
- ~~支持删除远程上传文件~~ -> 不再支持删除远程文件
- ~~(支持开启/关闭api自定义文字水印)~~
- ~~支持删除自定义删除图片(仅管理员)~~

</details>


不建议再使用 [EasyImage 1.6.4版本](https://github.com/icret/easyImages)

<hr />

#### 兼容性
PHP推荐使用PHP7.0及以上版本,需要PHP支持Fileinfo、iconv、zip、mbstring、openssl 扩展,如果缺失会导致无法访问管理面板以及上传/删除图片。

文件上传视图提供文件列表管理和文件批量上传功能，允许拖拽（需要 HTML5 支持）来添加上传文件，支持上传大图片，优先使用 HTML5，旧的浏览器自动使用Flash和Silverlight的方式兼容。
<hr />

 - 感谢: [verot](https://github.com/verot/class.upload.php "verot" )提供非常好用的class.upload.php上传类
 - 感谢: [ZUI](https://github.com/easysoft/zui "ZUI" ) 提供css框架
 - 本源码遵循 GNU Public License