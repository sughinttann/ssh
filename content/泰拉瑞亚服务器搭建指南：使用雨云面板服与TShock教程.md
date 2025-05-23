# 泰拉瑞亚服务器搭建指南：使用雨云面板服与TShock教程

## 前言
本文主要介绍如何在雨云平台通过面板服快速搭建泰拉瑞亚TShock服务器。相比传统VPS方案，面板服无需复杂配置，特别适合对端口没有特殊需求的用户，能大幅节省时间和成本。

## 准备工作
- 确保已阅读并理解基础服务器配置要求
- 准备好泰拉瑞亚游戏客户端
- 确定预期的玩家数量规模

👉 [【点击查看】2025年最新雨云优惠码及特价云服务器方案汇总](https://bit.ly/RainYun)

## 服务器选购指南

### 1. 选择服务器类型
- 进入"云产品"→"游戏云"→"立即购买"
- 服务器类型选择"MCSM面板"
- 不推荐VPS方案（成本较高）

### 2. 配置游戏类型
- 选择"泰拉瑞亚TShock"
- 如需开mod服则选择"tmodloader"

### 3. 机型选择建议
- 推荐AMD 5900X及以上配置
- 玩家较少时可选择Gold6146
- 5900X性能表现最佳

### 4. 计费模式选择
- 固定计费：适合24小时运行的服务器
- 动态计费：适合间歇性使用的服务器
- 建议10人以上选择固定计费

### 5. 服务器配置推荐
- 基础配置：2核4G
- 可支持20人同时在线
- 后期可随时升级配置

### 6. 购买时长建议
- 学生党推荐按日计费
- 月付适合长期稳定运行的服务器
- 日付成本约1-2元/天

## 服务器管理指南

### 1. 进入面板管理
购买完成后，在控制台找到对应实例，进入面板管理界面。

### 2. 启动服务器
- 按照提示完成基础配置
- 点击"开启实例"启动服务器
- 记录系统提供的IP和端口信息

### 3. 自定义配置
如需替换现有服务端：
1. 进入"文件管理"
2. 替换ServerPlugins和tshock文件夹
3. 保留原始启动脚本和TShock.Server文件

## 注意事项
- 不要删除或替换Linux版本的启动文件
- 确保配置文件与Linux系统兼容
- 首次启动建议检查日志输出

通过以上步骤，您就可以快速搭建一个稳定高效的泰拉瑞亚TShock服务器。如有任何问题，欢迎在评论区交流讨论。