# Fika - A multiplayer mod for SPT

<details open>
    <summary>内容列表</summary>
    <ol>
        <li><a href="#关于Fika">关于 Fika</a></li>
        <li><a href="#许可证">许可证</a></li>
        <li><a href="#翻译">翻译</a></li>
        <li>
            <a href="#准备工作">准备工作</a>
            <ul>
                <li><a href="#主机">主机</a></li>
                <li><a href="#客机">客机</a></li>
            </ul>
        </li>
        <li><a href="#硬件需求">硬件需求</a></li>
        <li>
            <a href="#安装步骤">安装步骤</a>
            <ul>
                <li><a href="#主机端口映射篇">主机：端口映射篇</a></li>
                <li><a href="#主机VPN-篇">主机：VPN篇</a></li>
                <li><a href="#主机代理篇">主机：代理篇</a></li>
                <li><a href="#专用客户端">专用客户端</a></li>
                <li><a href="#客机端口映射篇">客机：端口映射篇</a></li>
                <li><a href="#客机VPN-篇">客机：VPN篇</a></li>
                <li><a href="#客机使用端口转发时主持突袭">客机使用端口转发时主持突袭</a></li>
                <li><a href="#客机使用VPN时主持突袭">客机使用VPN时主持突袭</a></li>
            </ul>
        </li>
        <li>
            <a href="#特性和配置"> 特性和配置</a>
            <ul>
                <li><a href="#特性--使用方法">特性 & 使用方法</a></li>
                <li><a href="#客户端配置">客户端配置</a></li>
                <li><a href="#服务器配置">服务器配置</a></li>
            </ul>
        </li>
    </ol>
</details>

## 关于Fika

**Fika** 是一个能够让你与朋友进行合作模式的 **SPT** 模组。它利用 P2P-UDP 连接来提供现代且高性能的体验。 Fika 的主要目标是：性能、准确性和模组支持。 Fika 目前由 Fika 团队维护。你可以通过[这里](https://discord.gg/project-fika) 加入我们的 Discord 群组！


## 许可证

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

该项目使用了 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en) 旗下的许可证.

- 你仅能够在标明来源，且不更改项目内容的情况下分享 Fika，但不可用于商业用途。
- 你不能以任何形式利用你所开放的服务器收取费用。
- 你不能部署大型公共服务器，Fika 的宗旨是与好友合作。
- 你不能复制粘贴任何 Fika 的代码，或使用我们开发人员和美工制作的任何**资产**。

## 翻译

Fika 由 [Crowdin](https://crowdin.com/project/project-fika) 进行社区本地化. 请随时帮助我们将其翻译成任何可用的语言！

> [!注意]
> 所有翻译均来自社区成员，如果您发现任何不正确/冒犯/粗俗的翻译，请告诉我们

## 准备工作

Fika 需要具备对计算机、网络和 SPT 的基础知识。如果您对这些概念不熟悉，那么这个项目不适合您。请尝试理解并尊重这一点。

### 主机

- 支持 **端口映射** 或 **UPnP** 的路由器或 ISP
- 已开放用于 SPT 服务端的 TCP 协议的 6969 端口
- 已开放用于 P2P 传输的 UDP 端口，默认为 25565（若使用 UPnP 的话，则不需要）
- 已安装并且能运行 Fika 对应版本的 SPT（离线版）
- 允许通过你的 Windows 防火墙
- 推荐至少20 Mb/s（2.5 MB/s）及以上的上传和下载速度。每台客机平均需要占用 400 kb/s 的网速。

如果您无法进行端口转发，您可以使用“ZeroTier”或“Radmin”等 VPN 或“Playit. Gg”等代理（不提供官方支持）。

### 客机

- 支持 **端口映射** 或 **UPnP** 的路由器或 ISP | **注意事项**：此条仅适用于想在游戏里创建房间的客机
- 已开放用于 P 2 P 传输的 UDP 端口，默认为 25565 (若使用 UPnP 的话请忽略此条) | **注意事项**: 同上
- 已安装并且能运行 Fika 对应版本的 SPT（离线版）
- 允许通过你的 Windows 防火墙
- 推荐至少 20 Mb/s（2.5 MB/s）及以上的上传和下载速度

### 双方都需要用的东西

- 最新版本的 Fika 文件

## 硬件需求

流畅体验的推荐配置:

- **CPU**: i7 8700k / Ryzen 7 2700x
- **显卡**: GTX 1060 / RX 580
- **内存** 最小 16 GB , 强烈推荐 32 GB 
- **硬盘**: 必须固态硬盘, 使用机械硬盘后果自负

专用客户端的推荐配置:

- **CPU**: 每个核心频率>4 GHz
- **内存**: 最小 16 GB , 强烈推荐 32 GB
- **硬盘**: 必须固态硬盘

提升 Fika（SPT同理）体验的最好办法则是升级 CPU 和内存。

## 安装步骤

> [!重要事项]
> 准确阅读并遵循每一步至关重要。快速浏览或跳过任何步骤将导致服务器和客户端或任意一端无法工作。在尝试端口转发之前，请确保您了解您的路由器如何使用。不要忽视防火墙步骤，它们是必需的，也是大多数人未能正确执行的地方。


### 主机：端口映射篇

在开始这些步骤之前，请确保您已在准备工作中将端口转发所需的端口都已开放。我们不会协助您打开端口。如果您无法访问您的路由器或无法进行端口转发，请使用 VPN。

**防火墙配置**

1. 在你的路由器中开放 **TCP** 的 6969 端口（出站/入站都需要）
2. 在你的路由器中开放你将要使用的**UDP** 端口，默认为 25565（出站/入站都需要）
3. 当 Windows 弹出提示时, 在你的防火墙上允许 ***所有*** 连接。（你也可以通过 [FikaUtils](https://github.com/Lacyway/FikaUtils/releases/download/v1.0/FikaUtils.zip) 轻松完成这一切，只需要解压到你的安装文件夹）
4. 如果您仍然遇到问题，我们建议您在 Windows 高级防火墙中允许 `EscapeFromTarkov.exe`（所有人）和 `SPT.Server.exe`（服务器主机）进行入站和出站连接。

**基础配置**

1. [下载最新版本的Fika插件](https://github.com/project-fika/Fika-Plugin/releases/latest) 以及[下载最新版本的Fika服务器Mod](https://github.com/project-fika/Fika-Server/releases/latest)
3. 运行 `SPT.Server.exe` 一次，让它生成 Fika 的配置文件，然后关闭 `SPT.Server.exe`
4. 返回到主文件夹，在 `SPT_Data\Server\configs` 路径打开 `http.json` 
5. 修改 `ip` 为 `0.0.0.0`，`backendIp` 为你的[公网IP](https://ipv4.icanhazip.com/)，然后保存文件并关闭
6. 在 `user\mods\fika-server\assets\configs` 路径打开 `fika.jsonc`
7. 根据个人喜好更改设置
    - **useBtr**: 在街区是否生成 BTR
    - **friendlyFire**: 是否开启友伤
    - **dynamicVExfils**: 是否自动根据突袭中玩家数量调整载具撤离点的最大玩家数
    - **allowFreeCam**: 是否允许突袭中启用自由视角
    - **giftedItemsLoseFIR**: 发送物品时是否应该丢失 FIR（在战局中找到）状态
8. 启动 `SPT.Server.exe` 并且等待加载完成
    - 如果使用示例公网 IP 为 `70.60.150.90` 并成功运行后，应该有如下所示的信息：
    ```
    webserver已于http://70.60.150.90:6969启动
    websocket启动于ws://70.60.150.90:6969
    服务端正在运行, 玩的开心!!
    ```
9. 运行 `SPT.Launcher.exe`
10. 你的朋友可以通过 [IPv4.ICanHazIP](https://ipv4.icanhazip.com/) 网站查找到的你的公网 IP 连接到你的服务器

### 主机：VPN 篇

你需要一个 `ZeroTier` or `Radmin` 之类的 VPN，需要在本地防火墙允许这些程序（你也可以通过 [FikaUtils](https://github.com/Lacyway/FikaUtils/releases/download/v1.0/FikaUtils.zip) 轻松完成这一切，只需要解压到你的安装文件夹）

1. [下载最新版本的Fika插件](https://github.com/project-fika/Fika-Plugin/releases/latest) 以及[下载最新版本的Fika服务器Mod](https://github.com/project-fika/Fika-Server/releases/latest)
2. 访问你的 SPT 安装目录，并将压缩包的内容解压到该文件夹
3. 运行 `SPT.Server.exe` 一次，让它生成 Fika 的配置文件，然后关闭 `SPT.Server.exe`
4. 返回到主文件夹，在 `SPT_Data\Server\configs` 路径打开 `http.json` 
5. 修改 `ip` 和 `backendIp` 为你的 VPN IP, 然后保存文件并关闭

使用假 IP 地址 (**20.20.56.73**) 作为示例:
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "backendIp": "20.20.56.73",
    "backendPort": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. 在 `user\mods\fika-server\assets\configs` 路径打开 `fika.jsonc`
7. 根据个人喜好更改设置
    - **useBtr**: 在街区是否生成 BTR
    - **friendlyFire**: 是否开启友伤
    - **dynamicVExfils**: 是否自动根据突袭中玩家数量调整载具撤离点的最大玩家数
    - **allowFreeCam**: 是否允许突袭中启用自由视角
    - **giftedItemsLoseFIR**: 发送物品时是否应该丢失 FIR（在战局中找到）状态
8. 启动 `SPT.Server.exe` 并且等待加载完成
    - 如果使用步骤 5 的示例 IP，成功运行后，应该有如下所示的信息:
    ```
    webserver已于http://20.20.56.73:6969启动
    websocket启动于ws://20.20.56.73:6969
    服务端正在运行, 玩的开心!!
    ```
9. 运行 `SPT.Launcher.exe` ，点击 `Settings` ，接着勾选 `Developer Mode`
10. 在 `URL` 一栏, 将其更改为你的VPN 软件中所显示的IP 地址。使用步骤 5 中的示例，它将是: `http://20.20.56.73:6969` (请记得删除所有最后的正斜杠 `/`)
11. 启动游戏，创建账号后，将 `Force IP` 和 `Force Bind IP` 都改为你自己的VPN IP。你可以在主菜单通过按 F12 来找到它们。

### 主机：代理篇

> [!警告]
> 这不会得到Fika 的工作人员官方支持，如果它没用，则你只能靠自己了

[Playit.gg](https://playit.gg/) 是一个代理软件，可以托管服务器而无需端口转发，通过他们的数据中心之一来中继游戏流量。
[该指南](https://discuss.playit.gg/t/setup-an-escape-from-tarkov-multiplayer-server-with-spt-fika/3352) 将会教你如何通过 Playit. Gg 来托管一个 SPT/Fika Server
不需要编辑 ``http.json``。

### 专用客户端

> [!注意]
> 这一部分仅适用于进阶用户

1. 确保你安装了一个可用的服务端和客户端（可用指的是你***至少运行过一次***）
2. 复制客户端到一个新的文件夹，并安装最新的[专用客户端插件](https://github.com/project-fika/Fika-Dedicated/releases)
3. 在你的 `SPT.Server` 上, 打开 `fika.jsonc` 配置文件并且在底部修改你的专用客户端设置
```json
"dedicated": {
        "profiles": {
            "amount": 1 // 自动生成的专用配置文件数量，每个专用客户端都需要一个
        },
        "scripts": {
            "generate": true, // 是否自动生成一个启动脚本（除非你知道自己在做什么，否则是必需的）
            "forceIp": "127.0.0.1" // 专用客户端应该连接的IP地址，如果是本地则默认
        }
    }
```
4. 启动你的 `SPT.Server` 一次让它自动生成配置文件和启动脚本，然后访问 `\user\mods\fika-server\assets\scripts`，找到生成的脚本，将其移动到你在步骤 2 中创建的客户端安装根目录（如果你希望重新生成脚本，你需要删除旧的专用配置文件）
5. 使用端口转发或正常设置你的 VPN，然后手动更改 `\BepInEx\config\com.fika.core.cfg` 中的 `fika.core` 配置，设置端口号为你的转发端口，设置 `Force Bind IP` 和 `Force IP` 为专用客户端的 ip
6. 运行批处理脚本启动专用客户端，然后在游戏中在您自己的客户端上托管时，勾选“使用专用客户端”以使用专用客户端进行托管。每个客户端只能托管一次袭击。通常建议将所有 AI 模组放在专用客户端上，然后在本地客户端删除它们，因为现在由专用客户端处理 AI。

专用客户端以 60 FPS 的标准限制更新速率运行。如果您想将其增加到更高的数字，请在启动脚本中附加 `-updateRate=X`，其中 X 是您所需的更新率（最大 120）。一个例子是：
```bat
-batchmode -nographics --enable-console true -updateRate=120 & exit
```
请记住，更高的更新速率需要更强大的硬件来维持，并且收益可以忽略不计。

### 客机：端口映射篇

1. [下载最新的Fika插件](https://github.com/project-fika/Fika-Plugin/releases/latest)
2. 访问你的 SPT 安装目录，并将压缩包的内容解压到该文件夹
3. 运行 `SPT.Launcher.exe` ，点击 `Settings` ，接着勾选 `Developer Mode`
4. 在 `URL` 一栏, 将其更改为你的 VPN 软件中所显示的 IP 地址。举例: `http://70.60.150.90:6969` (请记得删除所有最后的正斜杠 `/`)

### 客机：VPN 篇

1. [下载最新的Fika插件](https://github.com/project-fika/Fika-Plugin/releases/latest)
2. 访问你的 SPT 安装目录，并将压缩包的内容解压到该文件夹
3. 运行 `SPT.Launcher.exe` ，点击 `Settings` ，接着勾选 `Developer Mode`
4. 在 `URL` 一栏, 将其更改为你的VPN 软件中所显示的IP 地址。使用步骤 5 中的示例，它将是: `http://20.20.56.73:6969` (请记得删除所有最后的正斜杠 `/`)

### 客机使用端口转发时主持突袭

1. 在你的路由器中使用端口转发功能，端口号为 25565，协议为 UDP（或者任意其他你希望使用的端口号，但是确保在 F12 菜单更改相对应的端口号）
2. 确保在你的 Windows 防火墙中允许 `EscapeFromTarkov.exe` 通过 (你也可以通过 [FikaUtils](https://github.com/Lacyway/FikaUtils/releases/download/v1.0/FikaUtils.zip) 轻松完成这一切，只需要解压到你的安装文件夹)
3. 你现在可以在游戏中主持突袭了

### 客机使用VPN时主持突袭

1. 确保在你的 Windows 防火墙中允许 `EscapeFromTarkov.exe` 通过 (你也可以通过 [FikaUtils](https://github.com/Lacyway/FikaUtils/releases/download/v1.0/FikaUtils.zip) 轻松完成这一切，只需要解压到你的安装文件夹)
2. 打开游戏并按 F12 打开配置菜单Open the game and open the configuration menu with `F12`
3. 将 `Force IP` 和 `Force Bind IP` 都改为你自己的VPN IP
4. 你现在可以在游戏中主持突袭了

## 特性和配置

### 特性 & 使用方法
**Fika** 允许你主持P2P会话用于和你的朋友进行合作模式。主机能够控制游戏中的大部分逻辑，如控制AI、雷区、狙击区、BTR等等。每个客机负责自己造成的伤害，无论是对他们自己还是AI，这意味着射击AI会感觉响应迅速。

要主持一个游戏，请选择一个地图和时间，然后在最后界面点击 `Host Raid`。选择将要进行游戏的玩家数量（包括你自己）并等待其完成加载。准备就绪后，其他人就可以加入你的会话，当每个人都加载完毕时，游戏会自动开始。

**Fika的其他特性**
- 物品发送
    - 在仓库右键一个物品，可以将其发送到另一个账号上
    - 可以在[服务端](#服务端配置)配置
- 自由视角 (默认 `F9` 启用)
    - 在自由视角，你可以通过按 `T` 键来传送到视角所在位置
    - 可以通过 `鼠标左/右键` 跳至其他玩家
    - 可在跳至其他玩家的过程中，通过按住 `SPACE` 查看他们的头部视角
    - 可在跳至其他玩家的过程中，通过按住 `CTRL` 查看他们的背部视角（第三人称）
    - 可通过 `HOME` 键切换自由视角的控制键位
- 调整自身重要部位的伤害倍数
- 主机可配置动态AI，当没人在AI附近时会禁用AI
- 自定义每张图的AI数量
- 剔除系统（根据相机的视角和距离，移除不需要渲染的物体，可提高性能）
- 自定义通知 (队友死亡, Boss击杀等等)
- 标记系统，可以为你的队友在游戏中标记一个区域
- 显示队友血量
- 在突袭中共享任务进度
- 专用客户端

更多特性在[客户端配置](#客户端配置).

### 客户端配置

要打开你的客户端配置，请在游戏中按 `F12` 键，前往 `Fika.Core` 部分去配置这些设置 

**合作**

- **Show Notifications**: 启用自定义通知，如玩家死亡、撤离，或击杀 Boss 的消息。
- **Auto Extract**: 客机自动撤离，而非进入自由视角。
- **Show Extract Message**: 是否显示死亡/撤离后的提示信息。
- **Extract Key**: 用于撤离的按键。
- **Chat Key**: 用于打开聊天窗口。

**合作 | 自定义**

- **Show Player Name Plates**: 显示玩家血条 & 名字。
- **Hide Health Bar**: 完全隐藏血条。
- **Show HP% instead of bar**: 以百分比形式显示血条，而非条形。
- **Show Player Faction Icon**: 在血条旁边显示玩家阵营。
- **Hide Name Plate in Optic**: 使用光学瞄具时，隐藏玩家血条和名字。
- **Name Plates Use Optic Zoom**:  使用光学瞄具时，显示玩家血条和名字。
- **Decrease Opacity In Peripheral**: 不对着玩家时，降低玩家血条的透明度
- **Name Plate Scale**: 玩家血条的大小
- **Opacity in ADS**: 机瞄时，玩家血条的不透明度
- **Ping System**: 切换标记系统。若设置为启用，你可通过使用标记键查看和获取通知。
- **Ping Button**: 用于发送标记的键位。
- **Ping Color**: 其他玩家视角里你标记的颜色。
- **Ping Size**: 标记大小的倍数。
- **Play Ping Animation**: 是否在标记时播放标记动画。可能会干扰游戏体验。

**合作 | 任务共享
- **Quest Types**: 哪些任务类型可以接收和发送。

**合作 | 调试

- **Free Camera Button**: 用于切换自由视角的按键。
- **AZERTY Mode**: 是否自由视角使用AZERTY键盘输入（一种键盘布局）
- **Keybind Overlay**:  是否显示所有自由视角键位

**性能**

- **Dynamic AI**: 使用动态 AI 系统，当它们超出任何玩家的范围时禁用 AI。
- **Dynamic AI Range**: 动态禁用AI的范围。
- **Dynamic AI Rate**: DynamicAI 应该多久扫描一次全部玩家的范围。

**性能 | 最大bots数量**

- **Enforced Spawn Limits**:  为 AI 刷新设置强制上限，防止其超过原版的阈值。主要用于更改 AI 上限或刷新机制的模组。
- **Despawn Furthest**: 当强制生成限制启用时，最远处的机器人应被取消生成，而不是阻止生成，这会使得在较低的最大机器人数量时，进行更加活跃的突袭，对较弱的PC有帮助，只会取消生成PMC和SCAV，如果你不启用动态生成Mod，这将很快耗尽地图上的生成，使得突袭变得非常死气沉沉。
- **Despawn Minimum Distance**: 这个距离内不生成Bots。
- **Max Bots** `MAP`: 在地图上同时能活动的最大Bot数量，电脑较弱的情况很有用（提升性能），设置为0则关闭该功能

**网络**

- **Native Sockets**:  用于发送/接收游玩过程中端口交互所产生流量的原生接口。使用套接字调用进行数据的交互，以达到大幅提升运行速度和降低 GC 压力的目的。仅适用于 Windows/Linux 操作系统，且不一定有效。
- **Force IP**: 主机托管时，强制服务器使用该 IP 进行后端广播，而非尝试自动获取。留空以禁用。使用 VPN 时为必填，即你 VPN 软件中所显示的 IP。
- **Force Bind IP**: 通过运行服务器主持时强制使用该本地 IP。留空以禁用。使用 VPN 时为必填，即你 VPN 软件中所显示的 IP。
- **Auto Server Refresh Rate**: 处于大厅时，客户端每隔 X 秒会向服务器请求战局列表。
- **UDP Port**: 用于游玩过程中 UDP 数据包的端口。
- **Use UPnP**: 是否尝试使用 UPnP 打开端口。若路由器支持 UPnP，但你无法打开端口，则非常有用。
- **Use NAT Punching**: 在主持突袭时使用NAT打孔，仅使用于完全圆锥型NAT，并且需要在STP服务器上运行NAT打孔服务。在此模式下，UPnP、Force IP and Force Bind IP都被禁用。
- **Connection Timeout**: 多长时间未接收到数据包则认为已断开连接。

**游戏玩法**

- **Head Damage Multiplier**: 头部所受到的伤害倍数， 0.2 = 20%
- **Armpit Damage Multiplier**: 腋下所受到的伤害倍数，0.2 = 20%
- **Stomach Damage Multiplier**: 胃部所受到的伤害倍数， 0.2 = 20%
- **Disable Bot Metabolism**: 禁用机器人的新陈代谢，以防止它们在长时间突袭中因为能量/水分流失而死亡。

### 服务器配置

服务器配置可以在 `user\mods\fika-server\assets\configs` 文件夹找到。使用文本编辑器打开 `fika.jsonc` 
```json
{
    "client": {
        "useBtr": true, // 是否在街区生成BTR, 默认值：true
        "friendlyFire": true, // 是否开启友伤, 默认值：true
        "dynamicVExfils": false, // 是否自动根据突袭中玩家数量调整载具撤离点的最大玩家数, 默认值：false
        "allowFreeCam": false, // 是否可以自由切换自由视角, 默认值：false
        "allowSpectateFreeCam": false, // 是否允许在死亡或撤离后观看玩家时进行自由视角，如果玩家全部死亡或撤离，自由摄像头仍然启用，默认值：false
        "allowItemSending": true, // 是否开启物品发送功能, 默认值：true
        "blacklistedItems": [], // 无法发送的物品模板ID, 举例： ["5c94bbff86f7747ee735c08f", "5c1d0f4986f7744bb01837fa"] 不允许玩家发送门禁卡和黑色钥匙卡
        "forceSaveOnDeath": false, // 死亡时强制保存，防止ALT+F4作弊, 默认值：false
        "mods": {
            "required": [], // 服务器必需Mod，启用后始终包含以下Mods: ["com.SPT.custom", "com.SPT.singleplayer", "com.SPT.core", "com.SPT.debugging", "com.fika.core", "com.bepis.bepinex.configurationmanager"]
            "optional": [] // 允许在必需Mod外可选的Mod
        },
        "useInertia": true, // 是否启用惯性, 默认值：true
        "sharedQuestProgression": false // 在突袭中的任务进度是否应该共享, 默认值：false
    },
    "server": {
        "giftedItemsLoseFIR": true, // 发送物品时是否应该丢失 FIR（在战局中找到）状态, 默认值：true
        "launcherListAllProfiles": false, // 启动器是否显示全部档案, 默认值：false
        "sessionTimeout": 5, // 服务器等待来自客户端的keepalive ping的时间，用于判断会话是否超时, 默认值: 5
        "showDevProfile": false, // 是否能创建开发者档案, 默认值：false
        "showNonStandardProfile": false // 是否能创建非标准的EFT档案, 默认值：false
    },
    "natPunchServer": {
        "enable": false, // 是否启用NAT打孔, 默认值：false
        "port": 6970, // NAT打孔端口, 默认值: 6970
        "natIntroduceAmount": 1
    }
}
```
