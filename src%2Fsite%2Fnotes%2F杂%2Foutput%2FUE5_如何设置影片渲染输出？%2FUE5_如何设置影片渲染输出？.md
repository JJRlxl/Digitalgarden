---
{"url":"https://mp.weixin.qq.com/s/mH6hVYLNxI9ZjnEtLS80cA","title":"UE5_如何设置影片渲染输出？","date":"2024-03-25 09:12:59","tags":null,"banner":"https://mmbiz.qpic.cn/mmbiz_jpg/8VPvxBhD4vDBuAlAjqVXVq5WpMUVnZ5MJbkcAXic0KkOECZ0LtlbtjibqGZ1rqfGHIY3B61eogKzb64sY7GMOrYw/0?wx_fmt=jpeg","banner_icon":"🔖","dg-publish":true,"permalink":"/杂/output/UE5_如何设置影片渲染输出？/UE5_如何设置影片渲染输出？/","dgPassFrontmatter":true}
---

我将分享在虚幻引擎 5 中使用的个人渲染设置，以便从引擎中获得高质量的电影渲染。我将与您分享每个设置以及为什么我选择它们，希望通过这个解释，您可以更好地理解您的渲染设置以及如何根据您的喜好调整它。从虚幻引擎中获取渲染图像并将其组合到完成的视频文件（如 MP4 或 OV 文件）的个人过程。简单提及下

首先，我们需要开启 UE 中渲染插件

![](<assets/1711329179588.png>)

确保我们有序列，检查我们有一个可渲染的摄像机

![](<assets/1711329179644.png>)

打开渲染

![](<assets/1711329179674.png>)

首先对渲染进行设置，这些基本上是与我们的渲染设置相关的模块

![](<assets/1711329179700.png>)

首先我们有我们的导出模块，无论是图像序列还是视频文件我有我的渲染设置本身，按钮添加到这些不同的部分，您可以将渲染设置设置得又长又复杂，也可以按照您的意愿简单设置  

![](<assets/1711329179719.png>)

**01 - 导出格式**

通常我先关闭 jpeg 因为我实际上想要渲染比 jpeg 更高质量的图像格式，我将来到这里的加号按钮并选择 exr 序列，这是我在渲染项目时通常使用的，它是质量更高一点的图像文件，压缩程度较低

![](<assets/1711329179746.png>)

**02 - 抗锯齿设置**

我们需要添加抗锯齿模块同样在加号中添加，我们要告诉虚幻引擎以更高质量渲染，这将为我们提供比我们通常在视口中看到的更好看的图像，所以第一件我要做的是重载抗锯齿 (√)

![](<assets/1711329179768.png>)

**Spatial Sample Count: 空间采样**  

如果你没有大量运动模糊，或者其中的运动很难解析事物周围的边缘，看起来太糟糕，或者有噪音，或者类似的事情然后你会开始增加空间样本计数 (最多为 8 个通常为 1，因为这会影响渲染时间)  

**Temporal Sample Count**：采样数我们将其调整我为 16(1080P)__32(4k 视频设置)

![](<assets/1711329179791.png>)

打开高级选项卡，我会在这里添加 300 帧，或者无论您想要多少，这基本上都是在实际开始渲染之前模拟 300 帧的物理特性，因此在我的情况下，激光射击将有 300 帧进入正确的位置，当我的渲染开始时，它们已经在这些渲染设置的最后一帧中

![](<assets/1711329179813.png>)

![](<assets/1711329179836.png>)

![](<assets/1711329179855.png>)

如果我在这种情况下使用多个镜头，我只使用一个镜头，一个位置一个相机，如果您使用多个镜头，您实际上可以在此处调整此文件格式，以合并多个序列并将它们渲染为单独的渲染

![](<assets/1711329179874.png>)

**游戏重载**

①：默认情况下游戏模式覆盖只是为了确保，您在 HUD 图像或已结束的东西上是否有任何类型的覆盖在屏幕顶部，如果您使用相机动画，则会将其淘汰，以确保在渲染过程中不会弹出用户界面

②：过场动画质量设置：电影质量设置是您的引擎技能设置提供最高质量的渲染

![](<assets/1711329179906.png>)

![](<assets/1711329179942.png>)

**④_1**：接下来我们有纹理流这是确保它完全加载所有纹理，并且您不会遇到任何问题，这些问题有时会在您流式传输纹理以提高运行时效率时发生，但在渲染时有时会出现一些看起来模糊的纹理它们没有完全正确加载，因此这将禁用纹理流使用

![](<assets/1711329179982.png>)

**④_2**：LOD 零这将影响您使用 LOD 系统的任何 Actor

**④_3** 禁用 HLOD

**④_4** 构建的游戏资源并使用高质量阴影时

**④_5** 阴影距离范围这将确保根据相机的距离，您可以获得更高质量的阴影，这也与阴影半径阈值 [0.001] 覆盖有关

**④_6** 视图距离与场景视图距离比例的范围有关，当您有资产弹出时，由于它们距相机的距离，您可以在此处进行调整

**④****_7_8/** **清空草地流送_清空流送管理器**：刷新草流送和刷新流管理器。将确保您在加载树叶等内容时获得所有最佳数据, 因此数据量很大，但是我希望这样您就可以知道在哪里查看和调整，如果您的渲染未完成或无法正常工作，您可以开始进行调整。例如关闭以使用高质量阴影或禁用细节度

![](<assets/1711329180001.png>)

**输出设置**  

我通常喜欢以 4K 渲染我的所有项目，我发现即使我要使用 1080P 渲染，我也会得到更高质量的结果或高清我仍然喜欢以 4K 渲染它，并且我有一个显卡可以在这种情况下处理它，所以我能够做到这一点，所以默认情况下它将是一个 1920 x 1080 的高清图像

![](<assets/1711329180025.png>)

我将其提高到 3840x2160，这是 16x9 的 4K 版本，那么如果您不熟悉每个图像都有一个宽高比，那么我该怎么办？很可能在电影渲染中您将使用 16x9 比例，这意味着宽度和高度的比例为 16 x 9，这将对应于两个像素值，在本例中为 3840 x 2160，这是向上和向一侧移动的像素数，这就是图像的大小因此，如果您不确定何时渲染应该渲染什么分辨率，我通常会转到此处的常见分辨率的维基百科页面列表

https://en.wikipedia.org/wiki/Display_resolution

![](<assets/1711329180047.png>)

它将以每秒 24 帧的速度渲染，这对于我通常喜欢制作的电影项目来说是相当标准的当然，我将其调整为每秒 30 帧

![](<assets/1711329180091.png>)

保存配置文件  

![](<assets/1711329180114.png>)

虚幻引擎非常擅长渲染图像本身，但在制作最终视频文件时，它实际上并没有那么好，它实际上并不擅长组合这些图像并将它们压缩成高质量的视频文件，它只是不是为其构建的，还有编辑软件他们非常擅长从渲染中制作高效的小型且非常高质量的视频文件，所以即使这看起来像是一个额外的步骤，我向你保证，它会在一天结束时为你提供最高质量的动画

我们在 Pr 中导入我们渲染的序列图，注意勾选序列  

![](<assets/1711329180147.png>)

右键创建序列，后续可按照 PR 剪辑流程进行影片剪辑  

![](<assets/1711329180169.png>)

  

  

作者：Aziel Arts

地址：https://youtu.be/JchOd6vGAy0

原视频：

![](<assets/1711329180201.png>)

![](<assets/1711329180239.png>)

坚持与您 “分享” 最有价值 “干货” 内容

本期分享就到这里，我们下期见！

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

![](<assets/1711329180261.png>)

**关注我们**

**学习不止、不止学习**

![](<assets/1711329180280.png>)

  

![](<assets/1711329180297.png>)

**公众号小编**

**

![](<assets/1711329180313.png>)

**

**公众号**

**

![](<assets/1711329180330.png>)

**

**哔哩哔哩**