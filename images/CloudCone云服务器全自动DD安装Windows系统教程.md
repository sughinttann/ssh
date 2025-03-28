# CloudCone云服务器全自动DD安装Windows系统教程

## 前期准备工作
在开始DD安装Windows系统前，请确保完成以下准备工作：
- 将系统重装为Debian 9或10（无需apt更新）
- 记录外网IP、子网掩码、网关等网络配置信息

## 详细安装步骤

### 1. 启用救援模式
登录CloudCone官网控制台：
- 左侧菜单选择"Access"功能
- 点击"RECOVERY"按钮启动救援模式

### 2. 下载并安装Windows系统
通过VNC连接服务器：
- 使用root权限登录系统
- 执行以下命令下载Windows镜像（以Win10 LTSC为例）：

bash
wget -O- https://p1e.cn/html/disk/od/windows/win10/Windows10-x64-LTSC-Nic-Tomy.vhd.gz | gunzip | dd of=/dev/vda

👉 [【点击查看】2025年最新CloudCone优惠码及特价云服务器方案汇总](https://bit.ly/Cloudcone)

### 3. 完成安装
当看到"records in/out"提示信息时：
- 返回控制台"Access"功能
- 点击"Disable recovery mode"停用救援模式

### 4. 登录Windows系统
通过VNC连接：
- 用户名：Administrator
- 密码：ievo.top

## Windows网络配置指南

### 5. 设置IPv4地址
1. 右击网络图标 → 打开"网络和共享中心"
2. 选择"以太网" → 点击"属性"
3. 选择"Internet协议版本4(TCP/IPv4)" → 点击"属性"
4. 输入之前记录的网络配置信息
5. 点击"关闭"完成设置

### 6. 验证网络配置
1. 返回"以太网"状态
2. 点击"详细信息"
3. 确认显示的IP地址与配置一致

## 注意事项
- 建议选择稳定的Windows镜像源
- 确保网络配置信息准确无误
- 整个过程可能需要较长时间，请耐心等待