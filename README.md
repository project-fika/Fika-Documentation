# Fika - A multiplayer mod for Aki

<details open>
    <summary>Table of Contents</summary>
    <ol>
        <li><a href="#what-is-fika">What is Fika</a></li>
        <li><a href="#license">License</a></li>
        <li>
            <a href="#prerequisites">Prerequisites</a>
            <ul>
                <li><a href="#hosting">Hosting</a></li>
                <li><a href="#client">Client</a></li>
            </ul>
        </li>
        <li><a href="#hardware-requirements">Hardware Requirements</a></li>
        <li>
            <a href="#installation">Installation</a>
            <ul>
                <li><a href="#host-using-port-forwarding">Host using port forwarding</a></li>
                <li><a href="#host-using-a-vpn">Host using a VPN</a></li>
                <li><a href="#client-using-port-forwarding">Client using port forwarding</a></li>
                <li><a href="#client-using-a-vpn">Client using a VPN</a></li>
            </ul>
        </li>
        <li>
            <a href="#features-and-configuration">Features and Configuration</a>
            <ul>
                <li><a href="features--how-to">Features & How-To</a></li>
                <li><a href="#client-configuration">Client Configuration</a></li>
                <li><a href="#server-configuration">Server Configuration</a></li>
            </ul>
        </li>
    </ol>
</details>

## What is Fika

**Fika** is a mod for **SPT-Aki** that allows you to play COOP with your friends. It utilizes a P2P-UDP connection for a modern and performant experience. The main goals of Fika are: performance, accuracy and mod-support. Fika is currently maintained by the Fika team.
You can join our Discord [here](https://discord.gg/project-fika)!

## License

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

This project is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en).

- You may only share Fika as long as proper credits are given, it is not used for commercial purposes and you do not modify it.
- You may not monetize your server in terms of payments or donations.
- You may not host massive public servers, Fika is meant for COOP with your friends.
- You may not copy and/or replicate the code by Fika, nor may you use its assets that are handcrafted by our developers and artists.

## Prerequisites

Fika requires general knowledge of computers, networking and Aki. If you are not comfortable with these concepts, this project is not for you. Please try to understand and respect this.

### Hosting

- Router and ISP that supports either **Port Forwarding** or **UPnP**
- TCP port 6969 open for the AKI Server
- UDP Port open for P2P traffic, default 25565 (if using UPnP this is not required)
- SPT installed and working, matching the version of Fika you are going to use
- Access to your Windows Firewall
- Internet speed of at least 20 Mbit/s up and down is recommended. Each client averages around 400 kbit/s.

If you can not port forward, you can use a VPN like `Hamachi`, `ZeroTier` or `Radmin`.

### Client

- Router and ISP that supports either **Port Forwarding** or **UPnP** | **NOTE**: This is only required if you will be hosting in-game
- UDP Port open for P2P traffic, default 25565 (if using UPnP this is not required) | **NOTE**: Same as above
- SPT installed and working, matching the version of Fika you are going to use
- Access to your Windows Firewall
- Internet speed of at least 20 Mbit/s up and down is recommended

### Both

- The latest Fika files

## Hardware Requirements

These are recommendations for a smooth experience:

- **CPU**: i7 8700k / Ryzen 7 2700x
- **GPU**: GTX 1060 / RX 580
- **Memory** 16 GB minimum, 32 GB highly recommended
- **Storage**: SSD is mandatory, do not expect support when running Fika on a HDD

The biggest gain in Fika (and in SPT in general) will be getting a stronger CPU and RAM.

## Installation

### Host using port forwarding

Before starting these steps, make sure you have port forwarded all required ports in the Prerequisites. We will not assist you with opening your ports. If do not have access to your router or can not port forward, use a VPN.

**Firewall Configuration**

1. Port forward the port 6969 **TCP** in your router (both in and out)
2. Port forward the **UDP** port that you will use in your router, default 25565 (both in and out)
3. When prompted by Windows, allow ***all*** connections in your Firewall

**General Setup**

1. Download the latest Fika build
2. Navigate to your SPT installation and extract the contents of the archive into the folder
3. Start up the `Aki.Server.exe` once to let it generate the configuration files for Fika, then close it again
4. Go back to the main folder and navigate to `Aki_Data\Server\configs` and open `http.json`
5. Change `ip` to `0.0.0.0`, then save the file and close it
6. Navigate to `user\mods\fika-server\assets\configs` and open `fika.jsonc`
7. Change any of the settings according to your likings.
    - **useBtr**: if the BTR should spawn or not when playing Streets
    - **friendlyFire**: if friendly fire should be enabled or not
    - **dynamicVExfils**: automatically scale vehicle exfils max players with the amount of players in the raid
    - **allowFreeCam**: allow players to freely toggle free cam during raids
    - **giftedItemsLoseFIR**: if sent items should lose their FiR status
8. Start the `Aki.Server.exe` and wait for it to finish loading
    - This is what it should look like if it succeeded to start:
    ```
    Started webserver at http://0.0.0.0:6969
    Started websocket at ws://0.0.0.0:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Start `Aki.Launcher.exe`
10. Your friends can connect to your server using your WAN IP, which can be found using the [IPv4.ICanHazIP](https://ipv4.icanhazip.com/) site

### Host using a VPN

You need a VPN like `Hamachi`, `ZeroTier` or `Radmin`. 

1. Download the latest Fika build
2. Navigate to your SPT installation and extract the contents of the archive into the folder
3. Start up the `Aki.Server.exe` once to let it generate the configuration files for Fika, then close it again
4. Go back to the main folder and navigate to `Aki_Data\Server\configs` and open `http.json`
5. Change `ip` to your VPN IP, then save the file and close it

Example with a fake address (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. Navigate to `user\mods\fika-server\assets\configs` and open `fika.jsonc`
7. Change any of the settings according to your likings.
    - **useBtr**: if the BTR should spawn or not when playing Streets
    - **friendlyFire**: if friendly fire should be enabled or not
    - **dynamicVExfils**: automatically scale vehicle exfils max players with the amount of players in the raid
    - **allowFreeCam**: allow players to freely toggle free cam during raids
    - **giftedItemsLoseFIR**: if sent items should lose their FiR status
8. Start the `Aki.Server.exe` and wait for it to finish loading
    - This is what it should look like if it succeeded to start using the example IP in step 5:
    ```
    Started webserver at http://20.20.56.73:6969
    Started websocket at ws://20.20.56.73:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Start `Aki.Launcher.exe` and click 'Settings'
10. In the `URL` field, change it to reflect your VPN IP. Using the example in step 5 it would be: `http://20.20.56.73:6969` (remember to remove any trailing forward slashes `/`)

### Client using port forwarding

1. Download the latest Fika build
2. Navigate to your SPT installation and extract the contents of the archive into the folder
3. Start `Aki.Launcher.exe` and click 'Settings'
4. In the `URL` field, change it to reflect the hosts WAN IP (remember to remove any trailing forward slashes `/`)
5. If hosting in-game, allow all connections (public and private) when prompted by the Windows Firewall

### Client using a VPN

1. Download the latest Fika build
2. Navigate to your SPT installation and extract the contents of the archive into the folder
3. Start `Aki.Launcher.exe` and click 'Settings'
4. In the `URL` field, change it to reflect the hosts VPN IP. Using the example in step 5 it would be: `http://20.20.56.73:6969` (remember to remove any trailing forward slashes `/`)
5. If hosting in-game, allow all connections (public and private) when prompted by the Windows Firewall

## Features and Configuration

### Features & How-To
**Fika** lets you to host P2P sessions with your friends to play COOP. The host is the one that controls most of the logic while playing, such as controlling AI, minefields, sniper zones, the BTR, etc. Each client is responsible for their own damage, both on themselves and on AI. This means that shooting an AI feels responsive and quick.

To host a game, choose a map and time, and then on the final screen click `Host Raid`. Select the amount of players that will be playing (including yourself) and wait for it to finish loading. Once it's ready other people can join your session, and when everyone has finished loading it will automatically start.

**Other Features of Fika**
- Item Sending
    - Right-click an item in your stash to send it to another account
    - Can be customized in the [server](#server-configuration) config
- Free cam (default to `F9` key)
    - In free cam you can teleport to the cam position by pressing `T`
    - You can jump to another player by `Left/Right` clicking
    - You can snap to their head by holding `SPACE` when jumping
    - You can snap to their back in a 3rd position view by holding `CTRL` when jumping
    - You can press the `HOME` key to temporarily toggle free cam controls
- Damage multipliers for crucial areas on yourself
- Dynamic AI for hosts, which disables AI when no one is near
- Custom AI limits per map
- Culling system to increase performance
- Custom notifications (teammate died, boss got killed by a player, etc.)
- Pinging system to ping an area in the game for your teammates
- Player health bars for your teammates

Most of these features are configured in the [client configuration](#client-configuration).

### Client Configuration

To open up your client configuration, press the `F12` key while in-game. Head to the `Fika Core` section to configure the settings.

**Coop**

- **Show Notifications**: Enable custom notifications when a player dies, extracts, kills a boss, etc.
- **Auto Extract**: Automatically extracts when playing as a client instead of entering free camera.
- **Show Extract Message**: Whether to show the extract message after dying/extracting.

**Coop | Custom**

- **Show Player Name Plates**: Toggle Health-Bars & Names.
- **Show HP% instead of bar**: Shows health in % amount instead of using the bar.
- **Show Player Faction Icon**: Shows the player faction icon next to the HP bar.
- **Name Plate Scale**: Size of the name plates.
- **Ping System**: Toggle Ping System. If enabled you can receive and send pings by pressing the ping key.
- **Ping Button**: Button used to send pings.
- **Ping Color**: The color of your pings when displayed for other players.
- **Ping Size**: The multiplier of the ping size.
- **Play Ping Animation**: Plays the pointing animation automatically when pinging. Can interfere with gameplay.

**Coop | Debug**

- **Free Camera Button**: Button used to toggle free camera.

**Performance**

- **Dynamic AI**: Use the dynamic AI system, disabling AI when they are outside of any player's range.
- **Dynamic AI Range**: The range at which AI will be disabled dynamically.
- **Dynamic AI Rate**: How often DynamicAI should scan for the range from all players.
- **Culling System**: Whether to use the culling system or not. When players are outside of the culling range, their animations will be simplified. This can dramatically improve performance in certain scenarios.
- **Culling Range**: The range at which players should be culled.

**Performance | Max Bots**

- **Enforced Spawn Limits**: Enforces spawn limits when spawning bots, making sure to not go over the vanilla limits. This mainly takes affect when using spawn mods or anything that modifies the bot limits.
- **Max Bots** `MAP`: Max amount of bots that can be active at the same time on `MAP`. Useful if you have a weaker PC. Set to 0 to disable.

**Network**

- **Native Sockets**:  NativeSockets for gameplay traffic. This uses direct socket calls for send/receive to drastically increase speed and reduce GC pressure. Only for Windows/Linux and might not always work.
- **Force IP**: Forces the server when hosting to use this IP when broadcasting to the backend instead of automatically trying to fetch it. Leave empty to disable. This is required when using a VPN, use your personal VPN IP.
- **Force Bind IP**: Forces the server when hosting to use this local IP when starting the server. Leave empty to disable. This is required when using a VPN, use your personal VPN IP.
- **Auto Server Refresh Rate**: Every X seconds the client will ask the server for the list of matches while at the lobby screen.
- **UDP Port**: Port to use for UDP gameplay packets.
- **Use UPnP**: Attempt to open ports using UPnP. Useful if you cannot open ports yourself but the router supports UPnP.

**Gameplay**

- **Head Damage Multiplier**: X multiplier to damage taken on the head collider. 0.2 = 20%
- **Armpit Damage Multiplier**: X multiplier to damage taken on the armpits collider. 0.2 = 20%

### Server Configuration

The server configuration can be found in the `user\mods\fika-server\assets\configs` folder. Open up `fika.jsonc` with a text editor.

```json
{
    "client": {
        "useBtr": true, // if the BTR should spawn on streets, default: true
        "friendlyFire": true, // if friendly fire is enabled, default: true
        "dynamicVExfils": false, // if vehicle exfils should scale to the amount of players in raid rather than default to 4, default: false
        "allowFreeCam": false, // if the free cam can be toggled freely, default: false
        "allowItemSending": true // if item sending should be enabled, default: true
    },
    "server": {
        "giftedItemsLoseFIR": true // if sent items should lose their FiR status, default: true
    }
}
```
