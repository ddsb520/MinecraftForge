![Forge Logo](assets/Forge_logo.svg)

MinecraftForge
=============
[![Stable Release](https://img.shields.io/badge/dynamic/json?url=https://files.minecraftforge.net/net/minecraftforge/forge/promotions_slim.json&label=Stable&prefix=1.19-&query=$.promos["1.19.2-recommended"]&color=brightgreen&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyBjbGFzcz0ic3ZnLWlubGluZS0tZmEgZmEtc3RhciBmYS13LTE4IiBhcmlhLWhpZGRlbj0idHJ1ZSIgZGF0YS1pY29uPSJzdGFyIiBkYXRhLXByZWZpeD0iZmFzIiBmb2N1c2FibGU9ImZhbHNlIiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCA1NzYgNTEyIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPgo8cGF0aCBkPSJNMjU5LjMgMTcuOEwxOTQgMTUwLjIgNDcuOSAxNzEuNWMtMjYuMiAzLjgtMzYuNyAzNi4xLTE3LjcgNTQuNmwxMDUuNyAxMDMtMjUgMTQ1LjVjLTQuNSAyNi4zIDIzLjIgNDYgNDYuNCAzMy43TDI4OCA0MzkuNmwxMzAuNyA2OC43YzIzLjIgMTIuMiA1MC45LTcuNCA0Ni40LTMzLjdsLTI1LTE0NS41IDEwNS43LTEwM2MxOS0xOC41IDguNS01MC44LTE3LjctNTQuNkwzODIgMTUwLjIgMzE2LjcgMTcuOGMtMTEuNy0yMy42LTQ1LjYtMjMuOS01Ny40IDB6IiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K)](https://files.minecraftforge.net)
[![Latest Release](https://img.shields.io/badge/dynamic/json?url=https://files.minecraftforge.net/net/minecraftforge/forge/promotions_slim.json&label=Latest&prefix=1.19.2-&query=$.promos["1.19.2-latest"]&color=blue&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyBjbGFzcz0ic3ZnLWlubGluZS0tZmEgZmEtYnVnIGZhLXctMTYiIGFyaWEtaGlkZGVuPSJ0cnVlIiBkYXRhLWljb249ImJ1ZyIgZGF0YS1wcmVmaXg9ImZhcyIgZm9jdXNhYmxlPSJmYWxzZSIgcm9sZT0iaW1nIiB2aWV3Qm94PSIwIDAgNTEyIDUxMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTUxMS45ODggMjg4LjljLS40NzggMTcuNDMtMTUuMjE3IDMxLjEtMzIuNjUzIDMxLjFINDI0djE2YzAgMjEuODY0LTQuODgyIDQyLjU4NC0xMy42IDYxLjE0NWw2MC4yMjggNjAuMjI4YzEyLjQ5NiAxMi40OTcgMTIuNDk2IDMyLjc1OCAwIDQ1LjI1NS0xMi40OTggMTIuNDk3LTMyLjc1OSAxMi40OTYtNDUuMjU2IDBsLTU0LjczNi01NC43MzZDMzQ1Ljg4NiA0NjcuOTY1IDMxNC4zNTEgNDgwIDI4MCA0ODBWMjM2YzAtNi42MjctNS4zNzMtMTItMTItMTJoLTI0Yy02LjYyNyAwLTEyIDUuMzczLTEyIDEydjI0NGMtMzQuMzUxIDAtNjUuODg2LTEyLjAzNS05MC42MzYtMzIuMTA4bC01NC43MzYgNTQuNzM2Yy0xMi40OTggMTIuNDk3LTMyLjc1OSAxMi40OTYtNDUuMjU2IDAtMTIuNDk2LTEyLjQ5Ny0xMi40OTYtMzIuNzU4IDAtNDUuMjU1bDYwLjIyOC02MC4yMjhDOTIuODgyIDM3OC41ODQgODggMzU3Ljg2NCA4OCAzMzZ2LTE2SDMyLjY2NkMxNS4yMyAzMjAgLjQ5MSAzMDYuMzMuMDEzIDI4OC45LS40ODQgMjcwLjgxNiAxNC4wMjggMjU2IDMyIDI1Nmg1NnYtNTguNzQ1bC00Ni42MjgtNDYuNjI4Yy0xMi40OTYtMTIuNDk3LTEyLjQ5Ni0zMi43NTggMC00NS4yNTUgMTIuNDk4LTEyLjQ5NyAzMi43NTgtMTIuNDk3IDQ1LjI1NiAwTDE0MS4yNTUgMTYwaDIyOS40ODlsNTQuNjI3LTU0LjYyN2MxMi40OTgtMTIuNDk3IDMyLjc1OC0xMi40OTcgNDUuMjU2IDAgMTIuNDk2IDEyLjQ5NyAxMi40OTYgMzIuNzU4IDAgNDUuMjU1TDQyNCAxOTcuMjU1VjI1Nmg1NmMxNy45NzIgMCAzMi40ODQgMTQuODE2IDMxLjk4OCAzMi45ek0yNTcgMGMtNjEuODU2IDAtMTEyIDUwLjE0NC0xMTIgMTEyaDIyNEMzNjkgNTAuMTQ0IDMxOC44NTYgMCAyNTcgMHoiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=
)](https://files.minecraftforge.net) [![Discord](https://img.shields.io/discord/313125603924639766.svg?color=%237289da&label=Discord&logo=discord&logoColor=%237289da)](https://discord.gg/UvedJ9m) [![Support](https://img.shields.io/badge/Patreon-Support-orange.svg?logo=Patreon)](https://www.patreon.com/LexManos)

Forge 是一个免费的开源模组 API，您最喜欢的模组都在使用！

|版本     |    支持        |
|---------| ------------- |
| 1.19.x  |    Active     |
| 1.18.x  |    LTS        |

* [下载]
* [论坛]
* [Discord]
* [文档]

# 安装Forge

前往[Forge网站](https://files.minecraftforge.net)
并从列表中选择您希望获得 Forge 的 Minecraft 版本。

您可以下载 *Recommended Build* 的安装程序或
  *Latest build*在那里。 最新版本可能具有更新的功能，但可能
  结果更加不稳定。 安装程序将尝试安装 Forge
  进入您的原版启动器环境，然后您可以在其中创建一个新的
  使用该版本配置文件并玩游戏！
 
如需支持和问题，请访问 [支持论坛](https://www.minecraftforge.net/forum/forum/18-support-bug-reports/) or [the Forge Discord server](https://discord.gg/forge).

[这是来自 Rorax 的简短视频，展示了如何安装和设置 Forge。](https://www.youtube.com/watch?v=lB3ArN_-3Oc)

# 创建模组

[请参阅 Forge 文档中的“入门”部分](https://mcforge.readthedocs.io/en/latest/gettingstarted/).

# 为Forge做贡献

如果您希望实际检查 Forge，提交 PR 或以其他方式工作
  使用 Forge 本身，您来对地方了！

 [请参阅设置 Forge 工作区的指南](http://mcforge.readthedocs.io/en/latest/forgedev/).

### 拉取请求

[请参阅 Forge 文档中的“进行更改和拉取请求”部分](https://mcforge.readthedocs.io/en/latest/forgedev/#making-changes-and-pull-requests).

请阅读找到的贡献指南 [这里](CONTRIBUTING.md) 在发出拉取请求之前。

### 贡献者许可协议
我们要求所有贡献者承认 [Forge 贡献者许可协议](https://cla-assistant.io/MinecraftForge/MinecraftForge)。
请确保您有一个与您的 GitHub 帐户关联的有效电子邮件地址来执行此操作。 如果您以前有
登录了，应该没问题。

#### 捐款
*Forge 是一个大型项目，有许多合作者日以继夜地工作。 Forge 将永远保持免费
  使用和修改。 但是，运行这么大的项目需要花钱，所以请考虑
  [成为赞助人](https://www.patreon.com/LexManos)。*

[下载]: https://files.minecraftforge.net/
[论坛]: https://www.minecraftforge.net/forum/
[Discord]: https://discord.gg/UvedJ9m
[Documentation]: https://mcforge.readthedocs.io
