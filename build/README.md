# LG 验证包说明

当前构建产物是命令行开发验证包，仅用于检查帮助、版本和基本运行行为。程序执行后退出，不提供 Web 管理、隧道连接或网关转发，也不是可安装系统镜像。

目标系统基线为 **Debian 13（trixie）**，首期面向 `x86_64` 与 `aarch64`。验证包通过构建或运行检查，不代表对应嵌入式设备、虚拟机或完整网关功能已经通过部署验收。

产品状态见 [项目首页](../README.md)。各交付形式见 [Docker](../packaging/docker/README.md)、[虚拟机镜像](../packaging/vm/README.md) 与 [ISO 安装介质](../packaging/iso/README.md)。
