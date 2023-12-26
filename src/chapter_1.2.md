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



