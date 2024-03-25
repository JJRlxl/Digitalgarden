---
{"dg-publish":true,"permalink":"/学习笔记/虚幻/0.4.Bridge相关/","dgPassFrontmatter":true}
---

> [!tip] [[学习笔记/虚幻/基础认知阶段\|基础认知阶段目录]]

> [!NOTE]- 如何下载 Bridge
> 用必应浏览器搜索 quixel （不要搜 bridge），进入指定的网页（注意分辨）
> 
> 或者直接打开连接[Quixel （英语） |轻松构建 3D 世界](https://quixel.com/)
>> ![Pasted image 20240219143609.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219143609.png)
>
>选择右上角的产品-Bridge
>>![Pasted image 20240219143706.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219143706.png)
>
>点击中间的 Download Bridge，下载 Bridge 并安装
>> ![Pasted image 20240219143859.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219143859.png)

> [!NOTE]- 内置 Brigde 和独立版 Brigde 的区别
> 
> 虚幻 5 内置了 Brigde，那么独立版本为什么还需要大家准备？
> >独立版本可以下载 Hightpoly 版本的资产（模型面数最高，精度最高，性能占比也是最大的级别），在处理主体，细节上更有优势。

> [!NOTE]- 独立版Brigde 下载设置
> 首先注意不管是内置还是独立版都需要先登录才能下载使用。
> 
> 打开 Bridge 后看右上角用虚幻账号登录即可 (如果网络畅通，并且已经登录了 Epic 的情况可以在登录界面上方直接点 Epic 的按钮快捷登录)
>> ![Pasted image 20240219150532.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219150532.png)
>
>登录后点击左上角的 Edit-Download Settings（1），即可打开右边的下载设置菜单
>
>
>>![Pasted image 20240219150955.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219150955.png)
>
>下载设置分成 Textures（贴图）和 Models（模型）设置。贴图类型选用可以见常见贴图类型说明。常规情况贴图不用更改设置，主要注意模型选项。
>
>>![Pasted image 20240219151646.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219151646.png)
>
>LOD 和 Highpoly 级别的模型选择下载，选择精度时可以遵循以下原则
>
>><font color="#ffff00">画面的主体或者镜头需要特写，近景的情况，在性能能够支持的情况下，尽量选择 Highpoly 级别</font>
>
>><font color="#ffff00">常规中景或者近景不太重要的地方，可选用 LOD 级别 0 或者更低（远景）的级别</font>
>
>另外注意下载的路径更改（Edit-Settings），找一个容量较大的地方，不要放在移动硬盘。
>
>>![Pasted image 20240219152354.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219152354.png)
>
>
>

> [!NOTE]- 独立版的导出设置
> 看左上角 Edit-Export Settings（2），独立版本提供了各个软件对应的导出插件。选择你的软件下载即可。（贴图和模型精度同上原理自行决定）
> 
> ![Pasted image 20240219150955.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219150955.png)
> ![Pasted image 20240219153024.png|300](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219153024.png)  ![Pasted image 20240219153039.png|300](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219153039.png)
> 
> 在 Bridge 资产库里选择模型下载
> 
> ![Pasted image 20240219153523.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219153523.png)
> 
> 下载完成后点击 Export（加号按钮）导出到对应软件。
> 
> ![Pasted image 20240219153615.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219153615.png)
> 
> 对应 DCC 软件开启的情况下，模型会通过导出插件自动导入 DDC 软件（以 C 4 D 为例）
> 
> ![Pasted image 20240219153837.png](/img/user/%E5%82%A8%E5%AD%98/%E9%99%84%E4%BB%B6/Pasted%20image%2020240219153837.png)
> 








