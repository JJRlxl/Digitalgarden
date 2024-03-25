---
{"url":"https://mp.weixin.qq.com/s/N8b2eF9VKo4Cq4aYHeV54Q","title":"如何输出流畅镜头动画？ UE5 导轨应用与设置的探索","date":"2024-03-25 09:10:24","tags":null,"banner":"https://mmbiz.qpic.cn/mmbiz_jpg/8VPvxBhD4vBptqxLJ0jqLFRbnpVTeTut5gjrzyRjVkDNP086LrUBu3jydDCs3icQIzao2Gv6ibMsaUyhVLr4ZRag/0?wx_fmt=jpeg","banner_icon":"🔖","dg-publish":true,"permalink":"/杂/output/如何输出流畅镜头动画？ UE5 导轨应用与设置的探索/如何输出流畅镜头动画？ UE5 导轨应用与设置的探索/","dgPassFrontmatter":true}
---

有时候，在制作摄像机动画的过程中，我们可能会遇到一些挑战。特别是当摄像机旋转超过某个特定角度时，它往往会改变方向，不再按照我们预期的路径或方式旋转。这种情况在围绕场景中心进行演示时尤为明显。例如，我们可能希望摄像机能够平滑地围绕场景中心旋转，以展示整个环境或突出某个特定元素。然而，由于角度限制或设置问题，摄像机的行为可能并不符合我们的期望。今天我们将解决这一问题

问：摄像机镜头不以小树林为中心旋转  

![](<assets/1711329024878.png>)

![](<assets/1711329024933.png>)

设置后效果  

![](<assets/1711329024962.png>)

核心设置：启用查看追踪【聚焦方式可以不选择追踪中看需求】

我们可以对我们追踪对象做位移动画从而改变摄像机运动方向

![](<assets/1711329024992.png>)

**#制作过程**

开启插件

![](<assets/1711329025054.png>)

为了使动画看起来更加流畅，我们添加设相机导轨

![](<assets/1711329025117.png>)

我们按照样条线使用方式，调整摄像机导轨  

![](<assets/1711329025193.png>)

布置导轨路径，我们通过导轨白色样条线来设置路径

打开导轨热力图我们可以判断其流畅程度，红色：很快；蓝色；很慢

![](<assets/1711329025261.png>)

![](<assets/1711329025341.png>)

按照我们想要展示的路径调整我们导轨  

![](<assets/1711329025388.png>)

继续添加电影摄象机 Actor  

![](<assets/1711329025450.png>)

添加后我们摄象机并没有对准要展示的目标，我们需要在大纲中右键控制摄象机

![](<assets/1711329025520.png>)

调整好我们第一帧镜头位置，然后退出驾驶模式  

![](<assets/1711329025612.png>)

![](<assets/1711329025701.png>)

摄象机右键，附加到 ---> 选择吸管工具吸附我们的轨道

![](<assets/1711329025781.png>)

吸附后变成父子级关系【也可以手动将摄像机拖动到轨道下】  

![](<assets/1711329025844.png>)

新建关卡序列

![](<assets/1711329025922.png>)

选择相机，将摄像机添加到序列 (+ 号添加)；添加后如果进去驾驶模式我们直接推出

![](<assets/1711329025989.png>)

继续添加轨道，我们选择轨道，添加轨道  

![](<assets/1711329026077.png>)

【我们可以在大纲直接选择**导轨和摄像机，**拖拽到关卡序列】  

添加后  

![](<assets/1711329026134.png>)

在轨道右侧添加  

![](<assets/1711329026191.png>)

我们分别在第一帧和最后一帧打上一个关键帧，注意最后一帧数值为 1

![](<assets/1711329026260.png>)

快速进入第一帧和最后一帧

![](<assets/1711329026307.png>)

滑轨上当前位置：

时间轴第一帧为 0，最后一帧为 1[红框按钮也是添加关键帧]  

![](<assets/1711329026329.png>)

绑定下我们摄象机

![](<assets/1711329026344.png>)

绝对位置也就是摄像机导轨上显示的位置  

![](<assets/1711329026362.png>)

![](<assets/1711329026390.png>)

**#慢镜头制作**  

手动配置速度  

![](<assets/1711329026413.png>)

不同位置设置关键帧调整速度 (慢镜头效果设置)  

![](<assets/1711329026440.png>)

通过时长控制运动速度

![](<assets/1711329026462.png>)

如果我们制作的路径不需要围绕中心物体旋转，但是摄像机没有沿着轨道方向前进，我们需要勾选 **“锁定方向”** 相机会保持与轨道正前方前进  

![](<assets/1711329026479.png>)

**总结：**

01- **创建一个 Actor 作为目标追踪**

02- 有一台电影摄像机

03 - 摄像机导轨

![](<assets/1711329026498.png>)

[视频详情](javascript:;)

**#渲染**

打开渲染插件

![](<assets/1711329026520.png>)

项目设置

![](<assets/1711329026542.png>)

  

详细输出配置 (参考配置)  

[

**UE5：渲染导出**

UE5_如何设置影片渲染输出！





](https://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247589174&idx=1&sn=76077f3fa39787b3fa755ae352a403c3&chksm=fcde6ca9cba9e5bf53d7588ada24db23f1e02c80065f6ed1a46ff4e180e63fdd07efe0d42a66&token=746895025&lang=zh_CN&scene=21#wechat_redirect "https://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247589174&idx=1&sn=76077f3fa39787b3fa755ae352a403c3&chksm=fcde6ca9cba9e5bf53d7588ada24db23f1e02c80065f6ed1a46ff4e180e63fdd07efe0d42a66&token=746895025&lang=zh_CN&scene=21#wechat_redirect")

  

  

  

  

  

![](<assets/1711329026574.png>)  

![](<assets/1711329026605.png>)

![](<assets/1711329026631.png>)

坚持与您 “分享” 最有价值 “干货” 内容

本期分享就到这里，我们下期见！

![](<assets/1711329026650.png>)

：欢迎**留言**，大家互相学习讨论交流 

[**探寻游戏细节：解析 53 种贴图的制作与用途以及对环境、角色的影响！**](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247586168&idx=1&sn=4bdc05efd6b78e85c26a9fbfac449e27&chksm=fcde60e7cba9e9f179d23f3794dd8d2ce743454df598dc2d226708ba7640086cc4bbb9703fb6&scene=21#wechat_redirect)

[<<游戏关卡>> 关卡设计中的空间通信](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247582056&idx=1&sn=9ac0ad86918fb581329b3caa443a23f1&chksm=fcde70f7cba9f9e106e048cbaceb1f96de70fd356ff33e6c3162f99375d8e89ceb3b61a6eb1b&scene=21#wechat_redirect)

[<<游戏关卡>> 游戏光照是什么？如何为关卡进行照明 (灯光篇)](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247581967&idx=1&sn=4affbf699d4988cfbe1d7325ec2a0242&chksm=fcde7090cba9f986b0655a4f68f2f259eef9940238088048c479f4f96a0bf30600b6816dc4cc&scene=21#wechat_redirect)  

[<<游戏关卡>> 如何自然地引导玩家使用关卡布局 (视觉引导篇)](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247581933&idx=1&sn=ac70ed307b6cd129f35b0e30e44c7edd&chksm=fcde7172cba9f864259e7f227d97667bf2003dab49c8232dadd3bd959cd2821b79726f29a6ca&scene=21#wechat_redirect)  

[你从未见过 PCG 这样做！官方超好用图表 | 基础案例总结运用演示](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247581029&idx=1&sn=b4f9f8c8ffcf3dce92fd837bbeacdd79&chksm=fcde4cfacba9c5ec828563ab18b5c36cf57f4df627a3562ac4d037f3ca5ca767cee35b23bb08&scene=21#wechat_redirect)  

[虚幻引擎 5 BluePrint](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247575405&idx=1&sn=4d0c6abc004764124f6f3ad0a6862873&chksm=fcde56f2cba9dfe44e5ce2fc1a7a9015db211f4abd58db7639f70018a51ccbd391fa5691b7a1&scene=21#wechat_redirect)[（蓝图）](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247575405&idx=1&sn=4d0c6abc004764124f6f3ad0a6862873&chksm=fcde56f2cba9dfe44e5ce2fc1a7a9015db211f4abd58db7639f70018a51ccbd391fa5691b7a1&scene=21#wechat_redirect)  

[UE5.2 预览版 PCG 工具](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247574842&idx=1&sn=c75d685d4db52ba941f07c849cbb9a66&chksm=fcde54a5cba9ddb39902eda0fecb5c7d879115de44344959cf0895886305419eea020b6a65e8&scene=21#wechat_redirect)[系列](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247574842&idx=1&sn=c75d685d4db52ba941f07c849cbb9a66&chksm=fcde54a5cba9ddb39902eda0fecb5c7d879115de44344959cf0895886305419eea020b6a65e8&scene=21#wechat_redirect)  

[Houdini 基础入门系列 | Houdini 大世界制作](http://mp.weixin.qq.com/s?__biz=MzU3MTU5OTA4OA==&mid=2247558409&idx=1&sn=ca790a6d709e152cab89b8f6deb02d30&chksm=fcde1496cba99d80a4d809d9315d007af38c14a9b902574c6a90f8ae5eb063d4602b3345026c&scene=21#wechat_redirect)

**#更多详细文章分类**

知乎专栏 | 左侧文章目录便于查找 https://zhuanlan.zhihu.com/p/659080390

![](<assets/1711329026671.png>)

**关注我们**

**学习不止、不止学习**

![](<assets/1711329026687.png>)

  

![](<assets/1711329026704.png>)

**公众号小编**

**

![](<assets/1711329026720.png>)

**

**公众号**

**

![](<assets/1711329026735.png>)

**

**哔哩哔哩**