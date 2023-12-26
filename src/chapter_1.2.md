# PCIe

PCIe，全称为Peripheral Component Interconnect Express，是一种高速串行计算机扩展总线标准，被广泛用作主板上的扩展卡接口。它是PCI总线的继任者，旨在替代旧的PCI、PCI-X和AGP总线标准。由于其更高的传输速率和改进的协议效率，PCIe大幅提升了数据传输速度，并且已经成为现代计算机系统中最普遍的内部数据交换接口之一。

## 背景知识

ISA（Industry Standard Architecture）总线是一种计算机总线标准，它的前身可以追溯到1981年IBM推出的个人电脑（PC）。当时，IBM为了连接主板上的微处理器和外部设备（如显卡、声卡等），设计了一个内部通信接口。这个早期的总线被称作PC总线。随着时间的发展，IBM在其1984年推出的IBM PC/AT（Advanced Technology）中引入了一个新版本的总线，这就是ISA总线的前身。它最初是16位的，并且比之前的8位PC总线提供了更高的数据传输速率。ISA总线不仅能兼容新的16位卡，而且还向后兼容之前的8位扩展卡。尽管ISA总线曾经非常流行，但它基于并行通信原理，导致传输速度相对较慢且存在长度限制，这使得它难以满足日益增长的数据传输需求。

英特尔在1992年首次提出了 PCI（Peripheral Component Interconnect） 总线的概念，旨在解决 ISA 总线的瓶颈问题。PCI 是一种并行总线标准，最初被设计为用于连接外部设备，如网卡、显卡、磁盘控制器等。之后，PCI 很快成为一种开放标准，得到了多家硬件制造商的支持。这使得各种设备能够在不同厂商的计算机系统中互通性更好。

随着计算机技术的发展，PCI总线标准逐渐显露出一些限制，如带宽瓶颈和对未来高性能设备的支持不足。因此，产业界开始寻找一种更先进的替代方案。英特尔在2003年首次提出了 PCI Express （Peripheral Component Interconnect Express）的概念，作为对传统 PCI 标准的更新和改进。PCIe 最初被设计为一种高性能、灵活性更强的串行总线标准，以适应未来计算机的需求。

## 发展历程

1. **PCIe 1.0：** PCIe 1.0 标准于2003年发布。它引入了高速串行连接，每个通道的数据速率为2.5 GT/s（gigatransfers per second）。PCIe 1.0 提供了比传统的并行总线更高的性能和可扩展性。
2. **PCIe 2.0：** PCIe 2.0 标准于2007年发布。它在每个通道上将数据速率提高到5 GT/s，从而提供了更大的总线带宽。PCIe 2.0 向下兼容 PCIe 1.0，并为图形卡和其他高性能设备提供了更多的带宽。
3. **PCIe 3.0：** PCIe 3.0 标准于2010年发布。它将每个通道的数据速率进一步提高到8 GT/s，进一步增加了总线带宽。PCIe 3.0 的发布支持更高分辨率的图形、更快速的存储设备和更多高带宽应用。
4. **PCIe 4.0：** PCIe 4.0 标准于2017年发布。它将每个通道的数据速率提高到16 GT/s，实现了比 PCIe 3.0 更高的带宽。PCIe 4.0 的推出对于数据中心、高性能计算和其他需要更高带宽的应用具有重要意义。
5. **PCIe 5.0：** PCIe 5.0 标准于2019年发布。它将每个通道的数据速率提高到32 GT/s，再次增加了总线带宽。PCIe 5.0 的推出进一步满足了对更高性能和更大带宽的需求。
6. **PCIe 6.0：** PCIe 6.0 标准于2022年发布。它将每个通道的数据速率提高到64 GT/s，为未来计算机系统提供更大的带宽和性能。PCIe 6.0 的推出标志着 PCIe 标准的不断创新和发展。

<table>         
    <thead>            
        <tr>                 
            <th rowspan="2">PCIe Specification(版本)</th>                 
            <th rowspan="2">Specification ratification year(发布时间)</th>                 
            <th rowspan="2">Encoding(有效数据)</th>                 
            <th rowspan="2">Data Rate per lane(传输速率)</th>                 
            <th colspan="5">Throughput(吞吐量)</th>             
        </tr>             
        <tr>                 
            <th>x1</th>                 
            <th>x2</th>                 
            <th>x4</th>                 
            <th>x8</th>                 
            <th>x16</th>             
        </tr>         
    </thead>         
    <tbody>                         
        <tr>                 
            <td>1.0</td>                 
            <td>2003</td>                 
            <td>8b/10b</td>                 
            <td>2.5GT/s</td>                 
            <td>250MB/s</td>                 
            <td>0.500GB/s</td>                 
            <td>1.000GB/s</td>                 
            <td>2.000GB/s</td>                 
            <td>4.000GB/s</td>             
        </tr>             
        <tr>                 
            <td>2.0</td>                 
            <td>2007</td>                 
            <td>8b/10b</td>                 
            <td>5.0GT/s</td>                 
            <td>500MB/s</td>                 
            <td>1.000GB/s</td>                 
            <td>2.000GB/s</td>                 
            <td>4.000GB/s</td>                 
            <td>8.000GB/s</td>             
        </tr>             
        <tr>                 
            <td>3.0</td>                 
            <td>2010</td>                 
            <td>128b/130b</td>                 
            <td>8.0GT/s</td>                 
            <td>985MB/s</td>                 
            <td>1.969GB/s</td>                 
            <td>3.938GB/s</td>                 
            <td>7.877GB/s</td>                 
            <td>15.754GB/s</td>             
        </tr>             
        <tr>                 
            <td>4.0</td>                 
            <td>2017</td>                 
            <td>128b/130b</td>                 
            <td>16.0GT/s</td>                 
            <td>1.969GB/s</td>                 
            <td>3.938GB/s</td>                 
            <td>7.877GB/s</td>                 
            <td>15.754GB/s</td>                 
            <td>31.508GB/s</td>             
        </tr>             
        <tr>                 
            <td>5.0</td>                 
            <td>2019</td>                 
            <td>128b/130b</td>                 
            <td>32.0GT/s</td>                 
            <td>3.938GB/s</td>                 
            <td>7.877GB/s</td>                 
            <td>15.754GB/s</td>                 
            <td>31.508GB/s</td>                 
            <td>63.015GB/s</td>             
        </tr>             
        <tr>                 
            <td>6.0</td>                 
            <td>2022</td>                 
            <td>1b/1b</td>                 
            <td>64.0GT/s</td>                 
            <td>7.563GB/s</td>                 
            <td>15.125GB/s</td>                 
            <td>30.250GB/s</td>                 
            <td>60.500GB/s</td>                 
            <td>121.000GB/s</td>             
        </tr>             
    </tbody>    
</table>



## 基础知识

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
