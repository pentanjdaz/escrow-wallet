# DMIT香港Eyeball VPS全面测评

DMIT自香港CMI线路退出后，推出了全新的HKG.EB套餐。根据官网的描述，该系列主机在中国线路的优化方面做出了较大努力。本文对其中特定型号 PVM.HKG.EB.TINYv2 进行了测评。这款VPS适合移动用户，其电信和联通去程略显绕路（经NTT），而回程优化为直连；移动去程与回程均为直连，非常适合移动用户选购。

👉 [【推荐收藏】2025年 DMIT 最新优惠活动整理汇总 - 每日更新可用优惠套餐](https://bit.ly/dmit_coupon)

此外，如果您曾在5月5日购买过DMIT圣何塞的相关VPS，并选择保留该服务（未申请退款），可以通过提交工单以循环五折的优惠价格购买一台香港Eyeball系列机器，或者选择循环七折购入美国CN2 GIA VPS。

---

## 硬件性能测试

以下为DMIT香港Eyeball VPS的硬件配置信息：

plaintext
Basic System Information:
---------------------------------
Uptime     : 0 days, 3 hours, 5 minutes
Processor  : AMD EPYC 7402P 24-Core Processor
CPU cores  : 1 @ 2794.750 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 976.4 MiB
Swap       : 1024.0 MiB
Disk       : 9.7 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-16-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : US-DMITINC
ASN        : AS906 DMIT Cloud Services
Location   : Hong Kong, Central and Western District (HCW)
Country    : Hong Kong


在磁盘读写性能测试中，表现如下：

plaintext
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 12.79 MB/s    (3.1k) | 195.86 MB/s   (3.0k)
Write      | 12.79 MB/s    (3.1k) | 196.89 MB/s   (3.0k)
Total      | 25.58 MB/s    (6.3k) | 392.76 MB/s   (6.1k)

Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 443.52 MB/s    (866) | 491.65 MB/s    (480)
Write      | 467.09 MB/s    (912) | 524.40 MB/s    (512)
Total      | 910.61 MB/s   (1.7k) | 1.01 GB/s      (992)


---

## 网络速度评测

DMIT香港Eyeball VPS在不同地区的网络表现如下。测试包括IPv4与IPv6连接，并以Mbps为单位衡量发送与接收速度：

### IPv4测试结果：
plaintext
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
-----           | -----                     | ----            | ----            | ----           
Clouvider       | London, UK (10G)          | 601 Mbits/sec   | 779 Mbits/sec   | 196 ms         
Scaleway        | Paris, FR (10G)           | 655 Mbits/sec   | 825 Mbits/sec   | 163 ms         
NovoServe       | North Holland, NL (40G)   | 457 Mbits/sec   | 885 Mbits/sec   | 190 ms         
Uztelecom       | Tashkent, UZ (10G)        | 738 Mbits/sec   | 850 Mbits/sec   | 140 ms         
Clouvider       | NYC, NY, US (10G)         | 613 Mbits/sec   | 686 Mbits/sec   | 210 ms         
Clouvider       | Dallas, TX, US (10G)      | 624 Mbits/sec   | 603 Mbits/sec   | 216 ms         
Clouvider       | Los Angeles, CA, US (10G) | 628 Mbits/sec   | 732 Mbits/sec   | 219 ms         


### IPv6测试结果：
plaintext
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
-----           | -----                     | ----            | ----            | ----           
Clouvider       | London, UK (10G)          | 651 Mbits/sec   | 809 Mbits/sec   | 196 ms         
Scaleway        | Paris, FR (10G)           | 644 Mbits/sec   | 868 Mbits/sec   | 162 ms         
NovoServe       | North Holland, NL (40G)   | 444 Mbits/sec   | 840 Mbits/sec   | 190 ms         
Uztelecom       | Tashkent, UZ (10G)        | 724 Mbits/sec   | 582 Mbits/sec   | 140 ms         
Clouvider       | NYC, NY, US (10G)         | 570 Mbits/sec   | 735 Mbits/sec   | 210 ms         
Clouvider       | Dallas, TX, US (10G)      | 540 Mbits/sec   | 656 Mbits/sec   | 216 ms         
Clouvider       | Los Angeles, CA, US (10G) | 546 Mbits/sec   | 636 Mbits/sec   | 217 ms         


---

## 流媒体解锁体验

DMIT香港Eyeball VPS解锁主流流媒体平台的情况如下：

plaintext
[ Multination ] =============
Disney+                      YES (region: hk)
Netflix                      NO (Originals Only)
Youtube                      YES (region: hk)
Amazon Prime Video           YES (region: hk)
iQyi                         YES (region: hk)
HBO GO Aisa                  YES (region: hk)
BiliBili Hongkong/Macau Only YES

[ IPV6 Multination ] ========
Disney+                   YES (region: hk)
Netflix                   NO (Originals Only)
Youtube                   YES (region: hk)


---

## 总结

DMIT香港Eyeball VPS具备较为充足的流量资源，流媒体解锁的表现也令人满意，特别适合港区用户观看视频内容。不过，测试显示其流媒体画质偶尔会出现波动，未能持续保持高清。对于电信用户来说，观看整体较为流畅，而移动线路则更为优秀。此外，该主机的硬性参数及网络优化大大提升了用户体验，值得推荐。

👉 [【推荐收藏】2025年 DMIT 最新优惠活动整理汇总 - 每日更新可用优惠套餐](https://bit.ly/dmit_coupon)