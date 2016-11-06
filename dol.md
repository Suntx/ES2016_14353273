#DOL实例分析&编程
##example1
直接在square.c中用i=i^i^i替换掉i=i^i即可。

结果截图：

![example1 3次方](https://drops.azureedge.net/drops/previews/CMg4.preview_small.png?rscd=&rsct=binary&se=2016-11-06T12%3A36%3A04Z&sig=DmZwKD6gaoS0O1tIGEKp6%2F44XoXcdUWBdqzoyGEiJJg%3D&sp=r&sr=b&st=2016-11-06T11%3A36%3A04Z&sv=2013-08-15)

dot图：跟改动之前相同。

##example2
由于生成dot图的进程、通道以及连接的时候都是通过迭代产生的，因此直接把迭代的次数从3次修改到2次，这样dot图中产生的进程、通道、连接数目都相应减少1。

结果截图：

![example2](https://drops.azureedge.net/drops/files/acc_528743/IqQJ?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161106181142.png&rsct=image%2Fpng&se=2016-11-06T12%3A37%3A42Z&sig=eeVMWOE7p21eCjnjrCQFCgAlVAjLbSvSF42agXMiyeE%3D&sp=r&sr=b&st=2016-11-06T11%3A37%3A42Z&sv=2013-08-15)

dot图：

![dot图](http://a2.qpic.cn/psb?/V131oSoG3VPBEM/XRJXjsVR*IxExNYn3dPaYSvI.GWDizLU3n9Yp5GxY2Y!/b/dAkBAAAAAAAA&bo=PgP0AAAAAAADB.s!&rf=viewer_4)

##实验感想
明白了每一个例子的整体架构：1、.c和.h文件实现每一个进程以及功能的实现;2、.xml则是实现每一个进程、每一个功能之间怎么连接。就是1完成每一部分的实现，而2则决定以什么顺序什么方式将1的各个功能连接起来。