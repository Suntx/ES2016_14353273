#DOL实例分析&编程
##example1
直接在square.c中用i=i^i^i替换掉i=i^i即可。

结果截图：

![example1 3次方](https://drops.azureedge.net/drops/files/acc_528743/CMg4?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161106175826.png&rsct=image%2Fpng&se=2016-11-06T12%3A42%3A32Z&sig=5No6Kx%2BteHTd0BCL49YOFVdqTXUxs%2FAUSZs%2BVRZbuWQ%3D&sp=r&sr=b&st=2016-11-06T11%3A42%3A32Z&sv=2013-08-15)

dot图：跟改动之前相同。

##example2
由于生成dot图的进程、通道以及连接的时候都是通过迭代产生的，因此直接把迭代的次数从3次修改到2次，这样dot图中产生的进程、通道、连接数目都相应减少1。

结果截图：

![example2](https://drops.azureedge.net/drops/files/acc_528743/IqQJ?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161106181142.png&rsct=image%2Fpng&se=2016-11-06T12%3A37%3A42Z&sig=eeVMWOE7p21eCjnjrCQFCgAlVAjLbSvSF42agXMiyeE%3D&sp=r&sr=b&st=2016-11-06T11%3A37%3A42Z&sv=2013-08-15)

dot图：

![dot图](https://drops.azureedge.net/drops/files/acc_528743/DyX5?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161106201328.png&rsct=image%2Fpng&se=2016-11-06T12%3A43%3A48Z&sig=3zvYL2cEDNK%2FoAPDa3wBkgz42oFoyV1eUKdYRC6kl3s%3D&sp=r&sr=b&st=2016-11-06T11%3A43%3A48Z&sv=2013-08-15)

##实验感想
明白了每一个例子的整体架构：1、.c和.h文件实现每一个进程以及功能的实现;2、.xml则是实现每一个进程、每一个功能之间怎么连接。就是1完成每一部分的实现，而2则决定以什么顺序什么方式将1的各个功能连接起来。