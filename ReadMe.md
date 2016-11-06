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

![systemc编译截图](https://d.pr/6gGJ)

编译完成后systemc文件目录如下：

![systemc目录](https://d.pr/ArXn)


2. dol编译

首先要修改dol中的build_zip.xml文件来告诉它systemc的位置在哪里，然后就进行编译。

编译结果如下图：

![dol编译截图](https://d.pr/16NES)
