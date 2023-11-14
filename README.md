# wrx 魏如雪

与[夏如雯](https://github.com/ckisok/xrw)是好朋友


## 安装
下载 wrx.zip 并解压，然后打开 Chrome 插件管理页面(chrome://extensions/)，如下：

![image](https://github.com/ckisok/wrx/assets/143160104/960af75a-5787-44af-96b4-b08ee1ec77ec)

打开右上角的开发者模式，然后左上角的 **Load unpacked** 按钮用于安装这个 **魏如雪** 未打包插件。


## 使用
打开微信读书阅读页面，打开目录弹框，你需要把这些红点点都点成绿色的，如下所示：

![image](https://github.com/ckisok/wrx/assets/143160104/7b2127ce-b303-4d05-bcf9-f5a3300a47e8)


## 导出

在阅读页面的右下角，点击 **导出本书数据** 按钮，即可将您已阅读部分数据导出(此数据是加密数据，需要她的好朋友解密)。


## 数据清理

如果您担心该插件缓存的数据太占用空间，或者您仅仅是想知道怎么清除这些缓存的数据，那么您可以打开浏览器的控制台，按照如下操作删除 **IndexedDB** 下面的 **wrx** 数据库即可：

![image](https://github.com/ckisok/wrx/assets/143160104/fbabb881-beeb-47ad-9181-3831ec7621d6)


## 自动翻页设置

> 注意：v2.6 起不再需要设置浏览器，以下是 v2.6 之前版本的设置过程

打开 Chrome 控制台，依次点击下图所示的位置：

![image](https://github.com/ckisok/wrx/assets/143160104/d04ad3d4-ef37-4857-aff1-30930abc4513)

选择一个目录用于保存微信读书的脚本文件，如果出现下图的提示，请点击允许：

![image](https://github.com/ckisok/wrx/assets/143160104/91baed89-3f60-42d5-bc02-6155a2c7e3b5)

然后打开一本书的阅读页面，在控制台如下操作找到 `8.a6ca3e96.js`文件：

![image](https://github.com/ckisok/wrx/assets/143160104/61f78786-8764-4736-add6-5f1f54806754)

打开这个文件，然后在编辑区开头加个空格，然后保存，确保这个文件旁边有一个紫色的小圆点，如下图所示：

![image](https://github.com/ckisok/wrx/assets/143160104/8ea0f589-1366-4fec-8f8e-ae1118831fa3)

此时，浏览器就设置好了。

下载仓库中的 `8.a6ca3e96.js` 文件并覆盖你刚刚选择的目录下的 `8.a6ca3e96.js`文件，返回浏览器刷新页面即可。

然后通过最新版的插件面板即可控制自动翻页：

![image](https://github.com/ckisok/wrx/assets/143160104/32d34882-7f0d-4815-9e27-2062f45137ca)

> 注意，此方式仅针对特定版本的文件有效，如果微信读书发布新版导致 8.js 文件 hash 变化，需要重新下载最新的 8.js 进行覆盖
> 
> 自动翻页时需要保持控制台打开，要不然 overrides 设置不生效 (同样只针对 v2.6 之前版本，v2.6 起不需要)
