# SecureTunnelLG

SecureTunnelLG 是面向嵌入式主机与虚拟机的本地网关，定位为接收远端网关连接的 Hub。与 [SecureTunnelRG](https://github.com/vvhh2002/SecureTunnelRG) 配合，规划提供按来源、目标和协议限定的网络访问。

**当前处于开发阶段。命令行程序仅显示帮助和版本；Web 管理、隧道连接、网关转发及设备自启尚未实现。现有验证包不能作为可用网关部署。**

LG 规划支持部署在具有动态公网 IP 的办公室。动态地址需要 DDNS 更新，同时必须具备真实公网入站能力，并完成必要的端口映射与防火墙配置；只有域名解析正常并不足以保证远端能够连接。

系统基线为裁剪后的 **Debian 13（trixie）**，首期目标架构是 `x86_64` 与 `aarch64`。嵌入式设备仍需逐板验证启动、内核、驱动与资源用量，尚无已验证的最低内存要求。

| 交付形式 | 当前状态 |
| --- | --- |
| [Docker](packaging/docker/README.md) | 仅用于命令行开发验证，不能提供网关功能 |
| [虚拟机镜像](packaging/vm/README.md) | 规划提供 qcow2/raw，尚未生成可启动镜像 |
| [ISO 安装介质](packaging/iso/README.md) | 尚未实现安装器或可引导介质 |
| 嵌入式设备 | 板级适配与实际设备验证尚未完成 |

[Web 管理规划](docs/web-management.md) 包括接入节点、访问策略、状态检查与故障恢复。默认账户 `admin`、每设备随机初始密码、首次登录强制改密均为待实现功能，目前没有可登录的管理页面。

其他说明：[配置示例](config/README.md)、[验证包说明](build/README.md)、[自启状态](packaging/systemd/README.md)。
