# Racknerd KVM VPS 80端口访问问题排查与防火墙配置指南

## 问题背景

在Racknerd黑五促销期间，我购买了一款高性价比的KVM VPS服务器，配置如下：

- **4核vCPU**处理器
- **130GB**纯SSD存储空间
- **5GB**内存容量
- 每月**12,000GB**流量配额
- **1Gbps**网络带宽
- 完整root管理员权限
- 独立IPv4地址
- 年费仅需**55.93美元**

安装nginx后却发现外网无法通过80端口访问网站，经过排查发现是防火墙配置问题。

## 问题排查步骤

### 1. 检查端口开放状态

首先确认80端口是否开放：

bash
$ firewall-cmd --query-port=80/tcp
# 输出：no

### 2. 开放必要端口

执行以下命令开放HTTP/HTTPS标准端口：

bash
$ firewall-cmd --permanent --add-port=80/tcp
$ firewall-cmd --permanent --add-port=443/tcp
# 输出均为：success

### 3. 重载防火墙配置

使新配置立即生效：

bash
$ firewall-cmd --reload
# 输出：success

👉 [【点击查看】2025年最新 Racknerd 优惠码及特价云服务器方案汇总](https://bit.ly/Rack_Nerd)

## 防火墙管理常用命令大全

### 状态检查命令
bash
# 查看服务状态
systemctl status firewalld

# 检查防火墙运行状态
firewall-cmd --state

### 规则管理命令
bash
# 查看所有规则
firewall-cmd --list-all

# 检查特定端口状态
firewall-cmd --query-port=19999/tcp

### 端口操作命令
bash
# 开放80端口
firewall-cmd --permanent --add-port=80/tcp

# 关闭80端口
firewall-cmd --permanent --remove-port=80/tcp

# 配置生效（必须执行）
firewall-cmd --reload

## 注意事项

1. 所有涉及`--permanent`参数的修改都需要执行`--reload`才能生效
2. 建议同时开放443端口以便后续配置HTTPS
3. 如果使用非标准端口，需要相应修改防火墙规则

通过以上步骤，即可解决Racknerd VPS上80端口无法访问的问题，确保Web服务正常运行。