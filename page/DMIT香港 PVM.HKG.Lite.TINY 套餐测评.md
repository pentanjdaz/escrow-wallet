# DMIT香港 PVM.HKG.Lite.TINY 套餐测评

本次测试的是 DMIT 香港地区的 **PVM.HKG.Lite.TINY** 套餐，配置为：1核 CPU / 724MB 内存 / 10GB SSD / 2000GB（双向）流量 / 1Gbps 带宽。

DMIT 成立于 2018 年，是一家由美籍华人创立的主机商，其 ASN 为 AS906/AS54574，技术实力较强。DMIT 主要业务覆盖中国香港、美国洛杉矶和日本东京的数据中心，提供独立服务器和 KVM VPS 服务，同时也是搬瓦工部分机房的上游商家。DMIT 服务稳定，且据传从不超售，并提供支付宝、微信以及 PayPal 的支付支持，此外还有中文客服，使用非常便捷。

👉 [【推荐收藏】2025年 DMIT 最新优惠活动整理汇总 - 每日更新可用优惠套餐](https://bit.ly/dmit_coupon)

---

## 基础信息（Superbench 测试）

硬件方面，DMIT 使用 AMD EPYC 高性能 CPU，存储 IO 性能稳定出色。以下是 Superbench 测试结果：


CPU Model            : AMD EPYC 7402P 24-Core Processor
CPU Cores            : 1 Core @ 2794.748 MHz
CPU Cache            : 512 KB
OS                   : Debian GNU/Linux 11 (64 Bit) KVM
Kernel               : 5.10.0-9-amd64
Total Space          : 2.1 GB / 9.9 GB
Total RAM            : 67 MB / 724 MB (283 MB Buff)
Total SWAP           : 0 MB / 0 MB
Uptime               : 0 days 0 hour 4 min
Load Average         : 0.07, 0.02, 0.00
TCP CC               : bbr
ASN & ISP            : AS54574, DMIT Inc
Location             : Tseung Kwan O, Hong Kong / HK
Region               : Sai Kung District

----------------------------------------------------------------------
I/O Speed( 1.0GB )   : 555 MB/s
I/O Speed( 1.0GB )   : 605 MB/s
I/O Speed( 1.0GB )   : 528 MB/s
Average I/O Speed    : 562.7 MB/s

----------------------------------------------------------------------
Node Name        Upload Speed      Download Speed      Latency     
Speedtest.net    1038.46 Mbit/s    996.05 Mbit/s       1.98 ms     
Fast.com         0.00 Mbit/s       208.3 Mbit/s        -           
Hefei 5G     CT  5.99 Mbit/s       4.29 Mbit/s         325.39 ms   
Guangzhou 5G CT  1.12 Mbit/s       501.22 Mbit/s       202.41 ms   
TianJin 5G   CU  224.27 Mbit/s     1.20 Mbit/s         180.32 ms   
Shanghai 5G  CU  555.10 Mbit/s     0.79 Mbit/s         154.94 ms   
Guangzhou 5G CU  295.12 Mbit/s     40.13 Mbit/s        175.83 ms   
Wuxi 5G      CM  902.02 Mbit/s     983.26 Mbit/s       42.13 ms    
Nanjing 5G   CM  0.34 Mbit/s       820.53 Mbit/s       39.32 ms   


---

## 国际测速表现（单线程）

在国际互联方面，DMIT 香港 PVM.HKG.Lite.TINY 具有良好的传输性能。以下是具体测速数据：


----- Global (CDN) -----           
CacheFly, CDN                   204.93.150.152            87.72 MiB/s | 701.75 Mbps
----- Asia -----                   
Softlayer, HongKong, CN         119.81.130.170            43.75 MiB/s | 350.01 Mbps
Leaseweb, HongKong, CN          43.249.36.49              98.11 MiB/s | 784.92 Mbps
Hinet, Taiwan                   210.61.132.1              69.93 MiB/s | 559.44 Mbps
Linode, Tokyo, JP               139.162.65.37             32.82 MiB/s | 262.55 Mbps
Softlayer, Tokyo, JP            161.202.125.20            26.64 MiB/s | 213.08 Mbps
Softlayer, Seoul, KR            119.81.28.170             50.36 MiB/s | 402.88 Mbps
Linode, Singapore, SG           139.162.23.4              49.04 MiB/s | 392.35 Mbps
Softlayer, Singapore, SG        119.81.28.170             52.64 MiB/s | 421.12 Mbps
...


---

## TCP 路由测试

由于 Lite 套餐不包含到中国大陆的路由优化，部分线路会出现绕路情况。以下是部分测试数据：

1. **广州电信**
   - 路径：美国 -> 新加坡 -> 广州
   - 最终延迟：312.40 ms

2. **厦门电信**
   - 路径：香港直连 -> 广州 -> 厦门
   - 最终延迟：28.48 ms

3. **成都联通**
   - 路径：绕道美国
   - 最终延迟：439.54 ms

具体测试结果可见详细列表。

---

## 套餐概览及总结

DMIT 香港 HKG.Lite 套餐旨在服务于香港本地以及国际用户。具体套餐整理如下：

- **PVM.HKG.Lite.TINY**  
  1 核 / 0.75G 内存 / 10GB SSD / 2T 流量 / 1Gbps 带宽  
  `$6.9/月`  

- **PVM.HKG.Lite.STARTER**  
  1 核 / 1.5G 内存 / 20GB SSD / 4T 流量 / 1Gbps 带宽  
  `$10.9/月`  

- **PVM.HKG.Lite.MINI**  
  2 核 / 2G 内存 / 40GB SSD / 6T 流量 / 1Gbps 带宽  
  `$16.9/月`  

- **PVM.HKG.Lite.MICRO**  
  2 核 / 4G 内存 / 40GB SSD / 8T 流量 / 1Gbps 带宽  
  `$21.9/月`  

- **PVM.HKG.Lite.MEDIUM**  
  4 核 / 4G 内存 / 60GB SSD / 12T 流量 / 1Gbps 带宽  
  `$32.9/月`  

如果您需要针对中国大陆优化的连接，可以选择 **PVM.HKG.Pro 套餐**。此外，在没有 TVB 解锁需求情况下，DMIT 整体性能表现稳定且物有所值，尤其适合作为落地或中转接入使用。