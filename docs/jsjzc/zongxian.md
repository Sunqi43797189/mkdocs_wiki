### 总线
- Bus
- 一个公用的线路，CPU、内存以及输入和输出设备，都是通过这组线路，进行相互间通信的
- CPU 想要和什么设备通信，通信的指令是什么，对应的数据是什么，都发送到这个线路上
- 设备要向 CPU 发送什么信息呢，也发送到这个线路上
- 注册在总线上的各个模块就是松耦合的。模块互相之间并没有依赖关系
- 总线不能同时给多个设备提供通信功能

### 三种线路
- 数据线 Data Bus 传输实际的数据信息
- 地址线 Address Bus 确定到底把数据传输到哪里去，是内存的某个位置，还是某一个 I/O 设备
- 控制线 Control Bus 控制对于总线的访问

#### 双独立总线
- CPU和内存以及高速缓存通信的总线
- CPU里有一个快速的本地总线 Local Bus，CPU 内部和高速缓存通信
- CPU里还有一个相对速度较慢的前端总线 Front-side Bus，和外部 I/O 设备以及内存通信

### 总线裁决
- Bus Arbitraction

### 快速通道互联
