## 一键翻墙客户端

神州明见WEB版主要是针对电脑WIN用户，其它系统也可以用，比如IOS、linux、移动平台等。

html跟亲友传真类还是有区别的，亲友传真类是镜象网站类，需要不断更新维护资源和网址；而上面的平台是通过静态不变的html网页代码来动态呈现用户定制或者后台推送的新闻框架、翻墙节点等资源，对于最终用户而言平台html是免维护的，甚至不需要翻墙网址，自带翻墙逻辑，打开很小的html（定制版szmjweb.3.0.zip压缩包只有222 KB，解开764KB）就可起到类似翻墙软件的效果。

新版szmjweb（3.0版）因为含有框架代码<iframe>，需要支持此代码的新浏览器才能够显示。新版szmjweb（3.0版）翻墙功能做了优化，并且增加了用二维码小助手定制的接口。如果是作为本地网页使用或者在http网站下部署，就只需要使用index.html一个文件和sw.js，index.html可以改名。詳細使用方式請看压缩包裡的說明https://github.com/szmj0/update/blob/main/extras/SZZD_PC/%E7%A5%9E%E5%B7%9E%E6%98%8E%E8%A7%81web%E7%89%88%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E_v20230321.rar

资源目录 UxfPa （如：http://www.szzd.org/UxfPa ）下载到的是随机化处理在线防封锁PWA版本，带使用说明，以后如果新的出来会同步更新。如果是在https网站下部署，需要把三个文件都上传到根目录或子目录，但不能改名。

新版szmjweb（3.0版）下载的网址:

https://j.mp/szmjweb

注：后台已经更新，增加了一键翻墙客户端数字目录12，指向新版szmjweb（3.0版）打包下载。

如：http://www.szzd.org/12

#### 示例：视频播放器真相内容定制
  
请用自由门无界破网打开查看二维码小助手【3-2】广传平台 的示例。定制步骤如下：
  
1、下载一键翻墙客户端（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/szmjweb.3.0.zip ）即WEB版（广传平台）定制版，
  sha512: 3FE01FB0133568F08B5AA1C41056625C714E1E71773ABF1176934E23F5FE320358212C1844914E4FCD1172911AE9C46803296FE6A802DF5C2AA5A754E6DA81BE  szmjweb.3.0.zip
  ，启用对content.json的支持
用记事本打开index.html，把  < img src="" id="c" rel="">  替换为  < img src="" id="c" rel=";;;content.json"> 

2、需要把多线路播放数据支持的player.html解压（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/Player3.0_0814.rar ）、demo.json（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/demo.json ）及相关媒体文件放入content.json所指定的目录才行，Player.html也可以独立下载使用。content.json内容修改为包含Player.html的位置，如：
jsonpCallback([
    {
        "title": "样例",
        "css": "background:linear-gradient
(#566AC9,#0A38C2); color:#FFF;",
        "list": [
            {"title": "Player", "url": 
"book_html/Player.html"}        ]
    }
]);
  如content.json包含明慧html电子书和播放内容等自定义两栏的一个示例：
https://github.com/szmj0/szmj0.github.io/blob/main/content.json

如果不想要content.json文件想单独传递包括自定义内容的index.html一个文件也是可以的，只是没有sw.js辅助显示安装到桌面或安装APP的提示。方法是：
在记事本中打开index.html查找到<div id="custom"></div>预留定制代码段，custom是定制的意思。在其中插入自定义内置json内容但不包括识别content.json特有的首尾本地跨域读取标记即：
jsonpCallback();

插入上面content.json示例只包含自定义内置json内容（含网页播放器）的完整代码段：
<div id="custom">
{
    "b_data": [{
        "title": "Html电子书",
        "css": "background:linear-gradient(#b3b8cc,#6179c0); color:#FFF;",
            
        "list": [
        {  "title": "九评共产党", "url": "https://fohao.github.io/book_html/9ping.html" },
            {
                "title": "风雨天地行",
                "url": "https://fohao.github.io/book_html/fytdx.html"              
            },
            {
                "title": "你我有缘画册",
                "url": "https://fohao.github.io/book_html/huace.html"              
            },
            {
                "title": "解体党文化",
                "url": "https://fohao.github.io/book_html/jtdwh.html"              
            },
            {
                "title": "江泽民其人",
                "url": "https://fohao.github.io/book_html/jzmqr.html"              
            },
            {
                "title": "“死刑犯”撑不起中国器官移植市场上的蘑菇云",
                "url": "https://fohao.github.io/book_html/murder.html"              
            },
            {
                "title": "世纪伪案 惊天骗局",
                "url": "https://fohao.github.io/book_html/pj.html"              
            },
            {
                "title": "退党手册",
                "url": "https://fohao.github.io/book_html/tdsc.html"              
            },
            {
                "title": "共产主义的终极目的",
                "url": "https://fohao.github.io/book_html/zjmd.html"              
            }        
            ]
                },
                {
                    "title": "定制影音",
                    "css": "background:linear-gradient(#b3b8cc,#6179c0); color:#FFF;",
                    "url": "/13769",
                    "list": [
                        {"title":"为什么会有人类（webm格式）", "vid": "media-0"},
                        {"title":"新唐人亚太台", "vid": "media-1"},
                        {"title":"新唐人美东台", "vid": "media-2"}
                    ]
                }
            ],
    "media": [
                {
                    "title": "为什么会有人类",
                    "type": "webm",
                    "file": "https://gitlab.com/tui590285/vdjiangfa/-/raw/master/public/jiangfa.webm"
                },
                {
                    "title": "新唐人亚太台",
                    "type": "m3u8",
                    "list": ["/9T1GF.m3u8","/d2ZFx.m3u8"]
                },
                {
                    "title": "新唐人美东台",
                    "type": "m3u8",
                    "list": ["/o4dPg.m3u8","/ZZ7iJ.m3u8"]
                }
            ]
}
</div>
示例中的github上的明慧html电子书，需要通过二维码助手github_htm接口获取到上传过电子书的github域名替换：
http://www.szzd.org/v.php?api=geturl.github_htm&action=text
这样添加后只适合本机破网测试效果使用，如果需要发送给世人的，测试好后需要通过二维码助手base64两次加密所添加的代码段。

3、demo.json的内容可以是相对于player.html所在目录的本地媒体文件，也可以是网络媒体文件，支持m3u8 流媒体、mp4等，在电脑和手机的 Chrome 测了可以在 player 里播放。
 
注：

（1）添加m3u8的demo.json示例，请破网测试：
  
[code]
  jsonpCallback([
    {
        "title": "新唐人美东频道",
        "file": [
            "http://www.szzd.org/static/0xAcdFDf02fbU/SLcUB/ANohBXhBUZ/xAUbR/wTRBgUDZlUBvUOIKj.m3u8"
        ]
    }
]);[/code]
  
  
其中播放链接生成方法是先用二维码小助手破网获取泛域名如上（*.chna.ml），再破网获取具体的新唐人直播频道如美东频道等，命令参数为：
*替代为任意字符的泛域名/v.php?id=ntdmd&action=text

（2）添加自定义播放链接的demo.json示例，请破网测试：
网址结尾不是 “.m3u8”也可能是 m3u8 格式，m3u8 格式的要把 http 改为 Http，也就是自定义。
  
jsonpCallback([     {         "title": "新唐人中国频道",         "file": [             "Http://sfdcgf3.chna.ml/Gh5fG",             "Http://sfdcgf3.chna.ml/PxKWd",                 "Http://sfdcgf3.chna.ml/YtaWK"               ]     } ]);

如果知道海外正义媒体网络发布公开的播放链接，可以用此播放器隐藏真实的播放址及后缀特征来实现自定义真相播放。比如上面获取新唐人中国频道直播神州明见代理资源目录的命令参数示例（请破网查看）：
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live150/playlist.m3u8
得到页面ID Gh5fG
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live400/playlist.m3u8
得到页面ID PxKWd
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live800/playlist.m3u8
得到页面ID YtaWK

4、独立使用Player.html的方法 
  请用自由门无界代理下载或查看效果： https://szmj0.github.io/book_html/Player.html 
  使用方法：
基于WEB定制第三版制作，可以在git官网上下载598 KB的Player3.0_0814.rar，解压后Player.html约1.2MB。
  
sha512：
E7F0BB2CD45FD39043CBCE1858C4F82A65A576AE39CCB8DBDA50F12B8746CA099BFCA47A4BADC3AAE6D0A65704EF54AD6ABAA47194CAC4FC86E68748262CB971  Player3.0_0814.rar
  
下载解压后可单独发给世人使用。
Player.html通过隐藏的WEB定制第三版代码加载墙外git官网上的播放列表，可能需要3－5秒左右（根据网络状况和机台情况而定），加载成功会在页面上显示后台维护的播放列表，如果不成功可以刷新或者换一个时间打开。iframe 现在没用了，加快了加载时间，对比之前采用iframe 可能节约一半以上的加载时间，更加稳定可靠。不需要手工写入翻墙域名，方便易用。
也可以直接推这个网页播放器的资源目录（页面ID） 13769 ，生成页面ID网址是：
https://raw.githubusercontent.com/szmj0/szmj0.github.io/main/book_html/Player.html?htm
注：?htm 是必须的，意思是代理后还原网页的效果。
即：可通过二维码助手用 13769 生成的域名网址或者短网址，如果需要查询点击量的可基于上述网址生成自定义页面ID，群发用途推荐用【1-3】。

如果有综合真相网页的需求，请参考基于WEB定制第三版的“畅游真相”定制方法：
 https://tiandixing.org/viewtopic.php?p=2130618#p2130618 神州明见官网发布“畅游真相”
  
返回首页： https://github.com/szmj0/Publish


