##环境安装
- sudo apt-get udpate
- sudo apt-get install ant
- sudo apt-get install openjdk-7-jdk
- sudo apt-get install unzip

利用上述四条Ubuntu指令来获取更新虚拟机的一些环境。

##dol文件配置
- sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
- sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

第一条语句用来获取安装dol的一些系统文件的压缩包，第二条语句获取dol文件压缩包。

##解压文件并编译配置环境
首先将上面下载的dol_ethz.zip和systemc-2.3.1.tgz两个文件解压。

1.systemc编译

利用ppt上面的命令来一步步编译systemc，configure之后截图如下：

![systemc编译截图](https://drops.azureedge.net/drops/files/acc_528743/6gGJ?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161009211506.png&rsct=image%2Fpng&se=2016-11-06T12%3A29%3A04Z&sig=2%2BHnnqsnyDPKHeuZUWvdxUY08AZLs4Kw0%2BZHmTFxV10%3D&sp=r&sr=b&st=2016-11-06T11%3A29%3A04Z&sv=2013-08-15)


编译完成后systemc文件目录如下：

![systemc目录](https://drops.azureedge.net/drops/files/acc_528743/ArXn?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161009212023.png&rsct=image%2Fpng&se=2016-11-06T12%3A28%3A08Z&sig=RRC7uTxhPmw76t2QvlP6g5SQvQKQvoO6ycAtjv6jDtg%3D&sp=r&sr=b&st=2016-11-06T11%3A28%3A08Z&sv=2013-08-15)


2. dol编译

首先要修改dol中的build_zip.xml文件来告诉它systemc的位置在哪里，然后就进行编译。

编译结果如下图：

![dol编译截图](https://drops.azureedge.net/drops/files/acc_528743/16NES?rscd=inline%3B%20filename%3DQQ%25E6%2588%25AA%25E5%259B%25BE20161009212444.png&rsct=image%2Fpng&se=2016-11-06T12%3A29%3A50Z&sig=Iz4GPZ6ZVhXs9tHHQkdCe1XPUJcW3SdyKiYo259C9%2B4%3D&sp=r&sr=b&st=2016-11-06T11%3A29%3A50Z&sv=2013-08-15)
