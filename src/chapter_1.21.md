# 基础知识

* 全双工点到点串行连接

  独立的发射和接收侧

* 可缩放链路宽度
  
  x1，x2，x4，x8，x16，

* 可扩展链路速度
  
  2.5、5.0、8.0、16.0、32.0和64.0GT/s 

## PCIe链路

PCIe Link表示两个组件之间的全双工通信信道，是PCIe总线中两个设备之间的通信连接，采用点对点的通信架构，一条链路可以包含多个通道(lane)，可增加通道个数来满足更高的带宽要求。

![image-20231226120533938](C:\Users\张江鹏\AppData\Roaming\Typora\typora-user-images\image-20231226120533938.png)



Lane，是指一组差分信号的组合，包括发送和接收。一个发送方向的差分信号包括TX+和TX-两条线，接收亦然。所以一条lane有四条物理连线。

![image-20231226143119817](C:\Users\张江鹏\AppData\Roaming\Typora\typora-user-images\image-20231226143119817.png)



## PCIe拓扑结构

![image-20231226120936484](C:\Users\张江鹏\AppData\Roaming\Typora\typora-user-images\image-20231226120936484.png)

1. **点对点连接：** PCIe总线采用点对点的通信方式，每个设备都直接连接到根复杂器（Root Complex）或其他中继设备。这种结构消除了共享总线的瓶颈，提供了更高的性能。
2. **树状结构：** PCIe的拓扑结构通常呈现为树状结构。根复杂器是总线的起点，连接到根复杂器的设备称为端点（Endpoint）。可以通过 Switch 进一步连接到其他设备，形成一个树状的拓扑结构。
3. **根复杂器 Root Complex（RC）：** RC是PCIe总线的起点，负责初始化和管理总线。RC可以连接到CPU、北桥芯片组或其他I/O控制器。
4. **PCIe Bridge To PCI/PCI-X**： 桥接设备，可以连接不同的PCIe域，例如连接其他的PCI总线、PCI-X、PCIe总线。
5. **Switch**： PCIe的转接器设备（PCIe扩展端口），为挂载设备提供路由以及转发服务；Switch的内部结构可以看作由PCI桥组成，在Switch中，每个端口对应的PCIe设备号是确定的，Switch设备会记录下游PCIe端口连接设备分配到的PCIe地址，在接收到TLP包时，通过比较目的地址和下游设备的地址，来判断是否转发以及转发到哪个PCIe端口。
6. **端点设备 PCIe Endponit（EP）：** 端点是直接连接到PCIe总线的终端设备，如显卡、网卡等。每个设备都有自己的设备标识和唯一的设备ID。
7. **链路：** 链路是连接PCIe设备的通信通道，可以根据需要进行配置。链路的宽度（Link Width）和速度（Link Speed）是PCIe连接的关键参数，决定了数据传输的带宽和速率。
8. **多域拓扑：** PCIe支持多域拓扑，允许将PCIe总线划分为不同的域，每个域内有独立的根复杂器和设备。
