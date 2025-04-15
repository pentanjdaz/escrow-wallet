# CloudCone VPS 上 DD Windows 10 系统及分区扩展与激活指南

本文将详细介绍在 CloudCone VPS 上通过 DD 方式安装 Windows 10 系统，并进行分区扩展和系统激活的全过程。

## 准备工作

### 1. 将系统切换至 Debian 9.9

首先需要将 VPS 系统切换至 Debian 9.9 作为基础环境。

### 2. 启动救援模式 (Recovery Mode)

进入 CloudCone 控制面板，启动救援模式并记录下自动生成的密码。

### 3. 获取网络配置信息

在救援模式启动前，记下 VPS 的 IP 地址、子网掩码和网关信息，这些将在后续配置中使用。

### 4. 通过 VNC 连接救援模式

使用 VNC 客户端连接到救援模式，准备执行 DD 操作。

## DD 安装 Windows 10

### 方法一：救援模式安装

连接救援模式后，执行以下命令：

bash
wget -O- https://go.520.be/win10 | gunzip | dd of=/dev/vda

等待命令执行完成，直到看到操作成功的提示。

### 方法二：直接 DD 安装（无需救援模式）

也可以使用以下命令直接安装：

bash
bash <(wget --no-check-certificate -qO- 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh') -dd "系统镜像地址"

常用 Windows 镜像地址：
- Windows 10 LTSC 64位中文版：`https://image.moeclub.org/GoogleDrive/1OVA3t-ZI2arkM4E4gKvofcBN9aoVdneh`
- 默认用户名密码：`Administrator:Vicer`

👉 [【点击查看】2025年最新CloudCone优惠码及特价云服务器方案汇总](https://bit.ly/Cloudcone)

## 登录 Windows 10 系统

### 1. 解决 Grub 引导问题

首次通过 VNC 登录时可能会遇到 Grub 界面，按 C 键后输入 `exit` 即可正常进入系统。

永久解决方案：在 CMD 中执行：
cmd
mkdir C:\Boot\grub2 && echo chainloader +1 >> C:\Boot\grub2\grub.cfg && echo boot >> C:\Boot\grub2\grub.cfg

### 2. 初始登录信息
- 用户名：`Administrator`
- 初始密码：`ievo.top`

### 3. 修改密码
通过 Win+R 打开运行窗口，输入 `cmd` 后执行：
cmd
net user Administrator YourNewPassword

### 4. 配置网络
刚安装完系统后需要手动配置网络：

cmd
netsh int ipv4 show config
netsh ipv4 set address name="Ethernet" static <IP> <Netmask> <Gateway>
netsh int ipv4 set dns name="Ethernet" static 1.1.1.1
netsh interface ip add dns name="Ethernet" 8.8.8.8 index=2

## 开启远程桌面访问

### 1. 通过注册表开启端口
修改注册表允许远程桌面连接。

### 2. 配置防火墙
确保防火墙允许远程桌面(3389端口)的入站连接。

### 3. Mac 用户连接
Mac 用户可以使用 Microsoft Remote Desktop 客户端连接 Windows 远程桌面。

### 4. 中文显示设置
确保系统区域和语言设置正确，以正常显示中文字符。

## 扩展 C 盘分区

默认安装后 C 盘只有 6G 空间，可以通过以下方法扩展：

### 方法一：使用系统自带磁盘工具
1. 打开磁盘管理
2. 右键点击 C 盘选择"扩展卷"
3. 按照向导完成分区扩展

### 方法二：使用分区助手
1. 下载安装分区助手
2. 选择 C 盘并点击"调整/移动分区"
3. 拖动滑块扩展分区大小
4. 提交操作并等待完成

## Windows 激活指南

### 1. KMS 激活步骤
1. 访问 `kms.ievo.top` 生成激活脚本
2. 以管理员身份运行 CMD
3. 依次执行生成的激活命令

### 2. 验证激活状态
执行以下命令验证激活状态：
cmd
slmgr /xpr

### 3. 重新激活
如需重新激活，先执行以下命令：
cmd
slmgr /upk
slmgr /ckms
slmgr /rearm

## 其他可用 Windows 镜像

1. Windows10-x64-LTSC-Nic-Tomy.vhd.gz
   - 下载地址：`https://dl.ievo.top/Image/DD/Windows10-x64-LTSC-Nic-Tomy.vhd.gz`
   - 用户名：`Administrator`
   - 密码：`ievo.top`

2. Windows10-x64-Lite-LTSC-Tomy.vhd.gz
   - 下载地址：`https://image.fucku.workers.dev/DD/Windows10-x64-Lite-LTSC-Tomy.vhd.gz`
   - 用户名：`Administrator`
   - 密码：`ievo.top`