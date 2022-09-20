## 一键翻墙客户端

神州明见WEB版主要是针对电脑WIN用户，其它系统也可以用，比如IOS、linux、移动平台等。

html跟亲友传真类还是有区别的，亲友传真类是镜象网站类，需要不断更新维护资源和网址；而上面的平台是通过静态不变的html网页代码来动态呈现用户定制或者后台推送的新闻框架、翻墙节点等资源，对于最终用户而言平台html是免维护的，甚至不需要翻墙网址，自带翻墙逻辑，打开很小的html（定制版szmjweb.zip压缩包只有50K，解开170K）就可起到类似翻墙软件的效果。

新版szmj.html（2.0版）因为含有框架代码<iframe>，需要支持此代码的新浏览器才能够显示。新版szmj.html翻墙功能做了优化，并且增加了用二维码小助手定制的接口。如果是作为本地网页使用或者在http网站下部署，就只需要使用index.html一个文件，可以改名。

资源目录 UxfPa （如：http://www.szzd.org/UxfPa ）下载到的是随机化处理在线防封锁PWA版本，带使用说明，以后如果新的出来会同步更新。如果是在https网站下部署，需要把三个文件都上传到根目录或子目录，但不能改名。

新版szmj.html下载的网址；

https://j.mp/szmjweb

注：后台已经更新，增加了一键翻墙客户端数字目录12，指向新版szmj.html打包下载。

如：http://www.szzd.org/12

#### 示例：视频播放器真相内容定制
  
请用自由门无界破网打开查看二维码小助手【3-2】广传平台 的示例。定制步骤如下：
  
1、下载一键翻墙客户端（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/szmjweb.zip ）即WEB版（广传平台）定制版，启用对content.json的支持
用记事本打开index.html，把  < img src="" id="c" rel="">  替换为  < img src="" id="c" rel=";;;content.json"> 

2、需要把多线路播放数据支持的player.html（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/player.html ）、demo.json（ https://github.com/szmj0/update/blob/main/extras/SZZD_PC/demo.json ）及相关媒体文件放入content.json所指定的目录才行，Player.html也可以独立下载使用。content.json内容修改为包含Player.html的位置，如：
jsonpCallback([
    {
        "title": "样例",
        "css": "background:linear-gradient
(#566AC9,#0A38C2); color:#FFF;",
        "list": [
            {"title": "Player", "url": 
"book_html/Player.html"}        ]
    }
]);

3、demo.json的内容可以是相对于player.html所在目录的本地媒体文件，也可以是网络媒体文件，支持m3u8 流媒体、mp4等，在电脑和手机的 Chrome 测了可以在 player 里播放。
 
注：

（1）添加m3u8的demo.json示例，请破网测试：
  
[code]
  jsonpCallback([
    {
        "title": "新唐人美东频道",
        "file": [
            "http://sfdcgf3.aoci.site/static/wRK5F/WAVVCBpRUBo/QVSo1/DewAWS9kAe/5lBQs/gHHEQQN8VCBzKCpvz.m3u8"
        ]
    }
]);[/code]
  
  
其中播放链接生成方法是先用二维码小助手破网获取泛域名如上（*.aoci.site），再破网获取具体的新唐人直播频道如美东频道等，命令参数为：
*替代为任意字符的泛域名/v.php?id=ntdmd&action=text

（2）添加自定义播放链接的demo.json示例，请破网测试：
网址结尾不是 “.m3u8”也可能是 m3u8 格式，m3u8 格式的要把 http 改为 Http，也就是自定义。
  
jsonpCallback([
    {
        "title": "新唐人中国频道",
        "file": [
            "Http://sfdcgf3.aoci.site/Gh5fG",
            "Http://sfdcgf3.aoci.site/PxKWd",
                "Http://sfdcgf3.aoci.site/YtaWK"
              ]
    }
]);

如果知道海外正义媒体网络发布公开的播放链接，可以用此播放器隐藏真实的播放址及后缀特征来实现自定义真相播放。比如上面获取新唐人中国频道直播神州明见代理资源目录的命令参数示例（请破网查看）：
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live150/playlist.m3u8
得到页面ID Gh5fG
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live400/playlist.m3u8
得到页面ID PxKWd
  
http://www.szzd.org/v.php?api=getid&url=http://cnhls.ntdtv.com/cn/live800/playlist.m3u8
得到页面ID YtaWK
  
增加“ 返回首页： https://github.com/szmj0/Publish ”



