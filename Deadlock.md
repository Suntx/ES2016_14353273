#Deadlock
##死锁截图
死锁的出现是随机的，因此两次死锁出现的时刻不同。

![](http://yotuku.cn/link?url=NJOZAYRgf&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

![](http://yotuku.cn/link?url=VJXbCYAlM&tk_plan=free&tk_storage=tietuku&tk_vuid=459b8123-fd7a-4c16-975e-5590fda625c4&tk_time=2016111118)

##死锁产生的四个条件
1. Mutual exclusion（资源互斥）：就是说一个资源在同一时间只能被一个进程占用。

2. Hode and wait（占有且等待）：就是说一个进程必须占有至少一种资源，而且还需要等待着获得另外一种被另一个进程占用的资源。

3. No preemption（非抢占）：就是相当于进程之间使用资源的优先级相同。任何一个进程不能直接抢占正在被其他进程占用中的资源。

4. Circular wai（循环等待）：假设进程A占有一种资源a，请求资源b。而 进程B占有资源b，请求资源a。两个进程形成一个环路同时等待对方释放资源。

##本次试验中死锁解释
首先我的理解是要达到死锁，我们需要a.methodA(b)语句和b.methodB(a)语句基本同时执行，这样才能保证死锁条件中的第2和第4条。而第1和3条java关键字synchronized已经能够保证。

因此我们通过调节count来决定线程t开始之后多久语句a.methodA(b)开始执行，从而使两条语句能够相互冲突。

调整了合适的count（我的是15000左右）之后，运行100次该程序，一般都会有某一次运行的时候两条语句同时运行（这里应该是由于硬件使得每次count减的速度不同从而导致语句同时运行的产生是随机的），同时运行时就会出现a请求调用b的方法，而同时b又请求调用a的方法。但是由于关键字synchronized，同时只能有一个被执行，因此两个都会锁住。