# Fika - Aki 的联机模组

<details open>
    <summary>内容列表</summary>
    <ol>
        <li><a href="#关于-fika">关于 Fika</a></li>
        <li><a href="#授权许可">授权许可</a></li>
        <li>
            <a href="#准备工作">准备工作</a>
            <ul>
                <li><a href="#主机">主机</a></li>
                <li><a href="#客机">客机</a></li>
            </ul>
        </li>
        <li><a href="#硬件要求">硬件要求</a></li>
        <li>
            <a href="#安装步骤">安装步骤</a>
            <ul>
                <li><a href="#主机端口映射篇">主机：端口映射篇</a></li>
                <li><a href="#主机vpn-篇">主机：VPN 篇</a></li>
                <li><a href="#客机端口映射篇">客机：端口映射篇</a></li>
                <li><a href="#客机vpn-篇">客机：VPN 篇</a></li>
            </ul>
        </li>
        <li>
            <a href="#特点与配置">特点与配置</a>
            <ul>
                <li><a href="#特点--使用方法">特点 & 使用方法</a></li>
                <li><a href="#客户端配置">客户端配置</a></li>
                <li><a href="#服务端配置">服务端配置</a></li>
            </ul>
        </li>
    </ol>
</details>

## 关于 Fika

**Fika** 是一款能让你与好友一起体验合作乐趣的 **SPT-Aki** 模组。该模组使用了一种更新式且高效的 P2P-UDP 连接方式。Fika 的主要目标是：高性能、高准度，以及模组支持。该项目目前由 Fika 团队开发和维护。
你可以通过 [这里](https://discord.gg/project-fika) 加入我们的 Discord 群组！

## 授权许可

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

该项目使用了 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en) 旗下的许可证。

- 你仅能够在标明来源，且不更改项目内容的情况下分享 Fika，但不可用于商业用途。
- 你不能以任何形式利用你所开放的服务器收取费用。
- 你不能部署大型公共服务器，Fika 的宗旨是与好友合作。
- 你不能复制粘贴任何 Fika 的代码，或使用我们开发人员和美工制作的任何资产。

## 准备工作

安装与配置 Fika 需要具备对电脑、网络，以及 Aki（离线版）的基础知识。要是你觉得自己不是这块料，这个项目不适合你。请理解并尊重这一点。

### 主机

- 支持 **端口映射** 或 **UPnP** 的路由器或 ISP
- 已开放用于 AKI 服务端的 TCP 协议的 6969 端口
- 已开放用于 P2P 传输的 UDP 端口，默认为 25565（若使用 UPnP 的话请忽略此条）
- 已安装并且能运行 Fika 对应版本的 SPT（离线版）
- 拥有 Windows 防火墙的权限
- 20 Mb/s（2.5 MB/s）及以上的上传和下载速度。每台客机平均需要占用 400 kb/s 的网速。

如果你不会/无法开放端口，可以使用 `Hamachi`，`ZeroTier`，或 `Radmin` 之类的软件搭建虚拟局域网（VPN）。

### 客机

- 支持 **端口映射** 或 **UPnP** 的路由器或 ISP | **注意事项**：此条仅适用于想在游戏里创建房间的客机
- 已开放用于 P2P 传输的 UDP 端口，默认为 25565 (若使用 UPnP 的话请忽略此条) | **注意事项**: 同上
- 已安装并且能运行 Fika 对应版本的 SPT（离线版）
- 拥有 Windows 防火墙的权限
- 20 Mb/s（2.5 MB/s）及以上的上传和下载速度

### 双方都要用的东西

- 最新版本的 Fika 文件

## 硬件要求

以下为能够畅玩的推荐配置：

- **CPU**：i7 8700k / Ryzen 7 2700x
- **显卡**：GTX 1060 / RX 580
- **内存**：16 GB 起步, 强烈推荐 32 GB
- **硬盘**：必须使用固态硬盘，使用机械硬盘后果自负

提升 Fika（离线版同理）体验的最好办法则是升级 CPU 和内存。

## 安装步骤

### 主机：端口映射篇

开始后续步骤前，请确保你已开放所有准备工作中提到的端口。如果你无法开放端口的话，请使用 VPN。

**防火墙配置**

1. 在路由器设置中打开 **TCP** 的 6969 端口（出墙和入墙都需要）
2. 打开你的路由器需要用到的 **UDP** 端口，默认为 25565（出墙和入墙都需要）
3. 当 Windows 弹提示时, 在防火墙设置里允许 ***所有*** 连接。

**基础配置**

1. [下载最新版本的 Fika 文件](https://discord.com/channels/1202292159366037545/1224454502531469373) (得先加入我们的 [Discord](https://discord.gg/project-fika) 链接才有效)
2. 把 Fika 的文件解压到你的 SPT 安装路径里
3. 运行一次 `Aki.Server.exe` 以生成 Fika 的配置文件，然后将其关闭。
4. 回到 SPT 的主文件夹，在 `Aki_Data\Server\configs` 路径中打开名称为 `http.json` 的文件
5. 将 `ip` 改为 `0.0.0.0`，保存文件后将其关闭
6. 在 `user\mods\mpt-server\assets\configs` 路径中打开名称为 `mpt.jsonc` 的文件
7. 以下根据个人喜好更改：
    - **useBtr**：是否让 BTR 装甲车出现在街区里
    - **friendlyFire**：是否启用队伤
    - **dynamicVExfils**：自动将载具撤离点的上限调整为战局内玩家的总数
    - **allowFreeCam**：战局内启用自由视角
    - **giftedItemsLoseFIR**：玩家间使用“给予物品”功能所获取的物品是否带勾（显示为战局内找到）
8. 运行 `Aki.Server.exe` 并待其加载完
    - 若成功运行，程序则如下所示：
    ```
    已在http://0.0.0.0:6969成功启动webserver
    于ws://0.0.0.0:6969启动了websocket
    服务器正在运行 玩得开心!!
    ```
9. 运行 `Aki.Launcher.exe`
10. 你的朋友们现在可以通过你的公网 IP 连接到你的服务器。要是不知道自己 IP 的话，可以通过 [IPv4.ICanHazIP](https://ipv4.icanhazip.com/) 查找

### 主机：VPN 篇

你需要用到 `Hamachi`，`ZeroTier`，或 `Radmin` 之类的软件

1. [下载最新版本的 Fika 文件](https://discord.com/channels/1202292159366037545/1224454502531469373) (得先加入我们的 [Discord](https://discord.gg/project-fika) 链接才有效)
2. 把 Fika 的文件解压到你的 SPT 安装路径里
3. 运行一次 `Aki.Server.exe` 以生成 Fika 的配置文件，然后将其关闭。
4. 回到 SPT 的主文件夹，在 `Aki_Data\Server\configs` 路径中打开名称为 `http.json` 的文件
5. 将 `ip` 改为你 VPN 软件中显示的 IP，保存文件后将其关闭

拿这个假 IP (**20.20.56.73**) 举例：
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. 在 `user\mods\mpt-server\assets\configs` 路径中打开名称为 `mpt.jsonc` 的文件
7. 以下根据个人喜好更改：
    - **useBtr**：是否让 BTR 装甲车出现在街区里
    - **friendlyFire**：是否启用队伤
    - **dynamicVExfils**：自动将载具撤离点的上限调整为战局内玩家的总数
    - **allowFreeCam**：战局内启用自由视角
    - **giftedItemsLoseFIR**：玩家间使用 “给予物品” 功能所获取的物品是否带勾（显示为战局内找到）
8. 运行 `Aki.Server.exe` 并待其加载完
    - 若成功运行，（使用的 IP 为上述第 5 步里所提到的），程序则如下所示：
    ```
    已在http://20.20.56.73:6969成功启动webserver
    于ws://20.20.56.73:6969启动了websocket
    服务器正在运行 玩得开心!!
    ```
9. 运行 `Aki.Launcher.exe`，然后点击右上角的 '设置'
10. 找到 `URL` 一栏，改为你的 VPN 软件里显示的 IP 地址。用上面第 5 步的 IP 的话就改成这样：`http://20.20.56.73:6969`（只改 IP 部分的数字即可，不需要动 `https://` 和 `:6969`）

### 客机：端口映射篇

1. [下载最新版本的 Fika 文件](https://discord.com/channels/1202292159366037545/1224454502531469373) (得先加入我们的 [Discord](https://discord.gg/project-fika) 链接才有效)
2. 把 Fika 的文件解压到你的 SPT 安装路径里
3. 运行 `Aki.Launcher.exe` 然后点开右上角的 '设置'
4. 找到 `URL` 一栏，改为主机的公网 IP（同理，只改 IP 部分的数字即可）
5. 要是在游戏里开房间的话，当 Windows 防火墙跳提示的时候，允许所有连接（公开和私人）

### 客机：VPN 篇

1. [下载最新版本的 Fika 文件](https://discord.com/channels/1202292159366037545/1224454502531469373) (得先加入我们的 [Discord](https://discord.gg/project-fika) 链接才有效)
2. 把 Fika 的文件解压到你的 SPT 安装路径里
3. 运行 `Aki.Launcher.exe` 然后点开右上角的 '设置'
4. 找到 `URL` 一栏，改为 VPN 软件中显示的主机 IP（同理，只改 IP 部分的数字即可）
5. 要是在游戏里开房间的话，当 Windows 防火墙跳提示的时候，允许所有连接（公开和私人）

## 特点与配置

### 特点 & 使用方法
**Fika** 允许你以主持 P2P 战局的方式和好友联机。主机能够控制游玩过程中的大部分逻辑，如 AI，雷区，狙击区，BTR 装甲车等。客机则全权把握其对自身或 AI 造成的伤害。换言之，战斗过程会显得流畅而不拖泥带水，也就是俗称的低延迟。

只需选定地图和时间，然后在最后的界面点击 `Host Raid` 即可主持战局。选定一局的玩家数量（别忘了把自己算进去）然后等游戏加载。待加载完毕，其他人就可加入你的战局，游戏会在所有人都加入后自动开始。

**Fika 的其它特点**
- 给予物品
    - 在仓库里右键要赠送的物品，可将其送到其他玩家的号上
    - 可在 [服务端](#服务端配置) 配置中调试
- 自由视角（默认使用 `F9` 启用）
    - 可通过 `T` 键传送到视角所在位置
    - 可通过 `鼠标左键/右键` 跳至其他玩家
    - 可在跳至其他玩家的过程中，通过按住 `SPACE` 查看他们的头部视角
    - 可在跳至其他玩家的过程中，通过按住 `CTRL` 查看他们的背部视角（第三人称）
    - 可通过 `HOME` 键切换自由视角的控制键位
- 调整重要部位的伤害倍数
- 动态 AI 系统（仅限房主），没人在附近的时候不会刷 AI
- 调整每张地图的 AI 数量
- 剔除系统（根据相机的视角和距离，移除不需要渲染的物体）
- 客制化通知（如队友死亡，Boss 击杀等）
- 标记系统，能够让队友看见你所标记的位置
- 显示队友血量

上述大部分特点可在 [客户端配置](#客户端配置) 中调整 。

### 客户端配置

在游戏中使用 `F12` 键开启客户端配置菜单。 可在 `Fika Core` 一栏中调整此部分的配置。

**联机相关**

- **Show Notifications**：启用自定义通知，如玩家死亡、撤离，或击杀 Boss 的消息。
- **Auto Extract**：客机自动撤离，而非进入自由视角。
- **Show Extract Message**：是否显示死亡/撤离后的提示信息。

**联机相关 | 自定义设置**

- **Show Player Name Plates**：显示玩家血条 & 铭牌。
- **Show HP% instead of bar**：以血量百分比 % 代替血条。
- **Show Player Faction Icon**：在玩家血条边上显示阵营。
- **Name Plate Scale**：铭牌大小。
- **Ping System**：切换标记系统。若设置为启用，你可通过使用标记键查看和获取通知。
- **Ping Button**：用于发送标记通知的键位。
- **Ping Color**：其他玩家视角里你标记的颜色。
- **Ping Size**：标记大小的倍数。
- **Play Ping Animation**：是否在标记时播放标记动画。可能会干扰游戏体验。

**联机相关 | 调试**

- **Free Camera Button**：用于切换自由视角的按键。

**游戏性能相关**

- **Dynamic AI**：动态 AI 系统，不在玩家范围外刷新 AI。
- **Dynamic AI Range**：在此范围外使用动态系统禁用 AI。
- **Dynamic AI Rate**：动态 AI 系统的刷新频率。
- **Culling System**：是否启用剔除系统。若处于渲染范围外，玩家的动作会被简化。在特定情况下能大幅提升游戏性能。
- **Culling Range**：剔除系统的范围。

**游戏性能相关 | AI 上限**

- **Enforced Spawn Limits**：为 AI 刷新设置强制上限，防止其超过原版的阈值。主要用于更改 AI 上限或刷新机制的模组。
- **Max Bots** `MAP`：`地图` 里同时活动的 AI 数量上限。对非高配电脑很有帮助。调整为 0 以禁用。

**网络相关**

- **Native Sockets**：用于发送/接收游玩过程中端口交互所产生流量的原生接口。使用套接字调用进行数据的交互，以达到大幅提升运行速度和降低 GC 压力的目的。仅适用于 Windows/Linux 操作系统，且不一定有效。
- **Force IP**：主机托管时，强制服务器使用该 IP 进行后端广播，而非尝试自动获取。留空以禁用。使用 VPN 时为必填，即你 VPN 软件中所显示的 IP。
- **Force Bind IP**：通过运行服务器主持时强制使用该本地 IP。留空以禁用。使用 VPN 时为必填，即你 VPN 软件中所显示的 IP。
- **Auto Server Refresh Rate**：处于大厅时，客户端每隔 X 秒会向服务器请求战局列表。
- **UDP Port**：用于游玩过程中 UDP 数据包的端口。
- **Use UPnP**：是否尝试使用 UPnP 打开端口。若路由器支持 UPnP，但你无法打开端口，则非常有用。

**游戏体验相关**

- **Head Damage Multiplier**：头部所受到的伤害倍数，0.2 = 20%
- **Armpit Damage Multiplier**：腋下所受到的伤害倍数，0.2 = 20%

### 服务端配置

服务端配置可在此路径的 `user\mods\mpt-server\assets\configs` 文件夹中找到。使用文本编辑器可对 `mpt.jsonc` 进行编辑。

```json
{
    "client": {
        "useBtr": true, // 用于启用街区的 BTR 装甲车，默认值为 true
        "friendlyFire": true, // 用于开启队伤，默认值为 true
        "dynamicVExfils": false, // 用于将载具撤离点的玩家上限调整为战局内玩家的总数，默认值为 false
        "allowFreeCam": false, // 用于启用战局内自由视角，默认值为 false
        "allowItemSending": true // 用于启用 “给予物品” 功能，默认值为 true
    },
    "server": {
        "giftedItemsLoseFIR": true // 用于启用/禁用 “给予物品” 功能所获得的物品状态（是否带勾），默认值为 true
    }
}
```
