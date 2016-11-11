#安装ROS
##1. setup sources.list
	
	sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
##2. set up keys

	sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116

实验截图：
	
![](http://yotuku.cn/link?url=4kmHKFAgG&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)
##3. Installation

首先用下面语句确定Debian package index已经更新了：
	
	sudo apt-get update

实验截图：

![](http://yotuku.cn/link?url=Nya4cFCxz&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

接着下载ROS中的库文件以及一些工具：
	
	sudo apt-get install ros-jade-desktop-full

实验截图：

![](http://yotuku.cn/link?url=N10YcFAeM&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

##4. Initialize rosdep
	
	sudo rosdep init

实验截图：

![](http://yotuku.cn/link?url=N1rNiY0xM&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

	rosdep update

实验截图：
![](http://yotuku.cn/link?url=4JA4sY0ef&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

##5. Environment setup

	echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
	source ~/.bashrc

	source /opt/ros/jade/setup.bash

##6. Getting rosinstall

	sudo apt-get install python-rosinstall

实验截图：
![](http://yotuku.cn/link?url=Nya2iYCxG&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

## Tutorials
	apt-get source ros-jade-laser-pipeline

![](http://yotuku.cn/link?url=E1ok2YCxM&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)


