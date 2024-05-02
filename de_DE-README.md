# Fika - Ein Multiplayer Mod für Aki

<details open>
    <summary>Inhaltsverzeichnis</summary>
    <ol>
        <li><a href="#was-ist-fika">Was ist Fika?</a></li>
        <li><a href="#lizenz">Lizenz</a></li>
        <li>
            <a href="#voraussetzungen">Voraussetzungen</a>
            <ul>
                <li><a href="#hosten">Hosten</a></li>
                <li><a href="#client">Client</a></li>
            </ul>
        </li>
        <li><a href="#hardware-voraussetzungen">Hardware Voraussetzungen</a></li>
        <li>
            <a href="#installation">Installation</a>
            <ul>
                <li><a href="#hosten-mit-portfreigabe">Hosten mit Portfreigabe</a></li>
                <li><a href="#hosten-mit-einem-vpn">Hosten mit einem VPN</a></li>
                <li><a href="#client-mit-portfreigabe">Client mit Portfreigabe</a></li>
                <li><a href="#client-mit-einem-vpn">Client mit einem VPN</a></li>
            </ul>
        </li>
        <li>
            <a href="#features-und-konfigurationen">Features und Konfigurationen</a>
            <ul>
                <li><a href="#features--how-to">Features & How-To</a></li>
                <li><a href="#client-konfigurationen">Client Konfigurationen</a></li>
                <li><a href="#server-konfigurationen">Server Konfigurationen</a></li>
            </ul>
        </li>
    </ol>
</details>

## Was ist Fika?

**Fika** ist eine Mod für **SPT-Aki** mit der es möglich ist COOP mit deinen Freunden zu spielen. Fika nutzt eine P2P-UDP Verbindung um ein modernes und performantes Spielerlebnis zu ermöglichen. Die Hauptziele von Fika sind: Performance, Präzision und Modunterstützung. Fika wird aktuell vom Fika Team entwickelt und betreut.
Du kannst unserem Discord hier [beitreten](https://discord.gg/project-fika)!

## Lizenz

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Dieses Projekt ist unter der folgenden Lizenz lizenziert [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en).

- Fika darf nur unter Einbezug der Lizenz weiterverbreitet, nicht für kommerzielle Zwecke genutzt und nicht modifiziert werden.
- Server dürfen nicht monetarisiert werden weder über Spenden noch über andere Zahlungen.
- Es dürfen keine öffentlichen Server gehostet werden. Der Sinn von Fika ist es COOP mit Freunden spielen zu können.
- Es ist nicht erlaubt Fikas Code zu kopieren oder zu replizieren. Es ist zudem nicht gestattet die von den Entwicklern und Künstlern erstellten Assets zu verwenden.

## Voraussetzungen

Um Fika nutzen zo können, benötigt man ein generelles Verständnis von Computern, Netzwerken und Aki. Wenn du nicht mit diesen Konzepten vertraut bist ist dieses Projekt eher nichts für dich. Wir bitten dich um Verständnis und diese Entscheidung zu aktzeptieren.

### Hosten

- Router und Internetanbieter mit Unterstützung für **Portfreigaben** oder **UPnP**
- TCP Port 6969 muss für den AKI Server geöffnet werden
- UDP Port muss für den P2P Verkehr geöffnet werden, Standardport 25565 (wenn UPnP verwendet werden kann ist dieser Schritt nicht notwendig)
- SPT muss installiert sein und funktionieren, die installierte SPT Version muss zur Fika Version passen die verwendet werden soll
- Es wird Zugang zur Windows Firewall benötigt sowie die lokalen Berechtigungen um diese Anzupassen
- Eine Internetverbindung von mindestens 20 Mbit/s Upstream und Downstream wird empfohlen. Jeder Client benötigt im Durchschnitt 400 kbit/s.

Sollten Portfreigaben nicht möglich sein kann auf VPNs wie `Hamachi`, `ZeroTier` oder `Radmin` zurückgegriffen werden.

### Client

- Router und Internetanbieter mit Unterstützung für **Portfreigabe** oder **UPnP** | **Notiz**: Diese Vorraussetzung besteht nur für den Client der im Spiel die Sitzung erstellt
- UDP Port muss für den P2P Verkehr geöffnet werden, Standardport 25565 (wenn UPnP verwendet werden kann ist dieser Schritt nicht notwendig) | **Notiz**: Diese Vorraussetzung besteht nur für den Client der im Spiel die Sitzung erstellt
- SPT muss installiert sein und funktionieren, die installierte SPT Version muss zur Fika Version passen die verwendet werden soll
- Es wird Zugang zur Windows Firewall benötigt sowie die lokalen Berechtigungen diese Anzupassen
- Eine Internetverbindung von mindestens 20 Mbit/s Upstream und Downstream wird empfohlen.

### Host & Client

- Die aktuellsten Fika Datein

## Hardware Voraussetzungen

Folgende Hardware wird für ein gutes Spielerlebnis vorrausgesetzt:

- **CPU**: i7 8700k / Ryzen 7 2700x
- **GPU**: GTX 1060 / RX 580
- **Memory** 16 GB mindestens, 32 GB empfohlen
- **Storage**: Eine SSD wird vorrausgesetzt, es wird keinen Support für den Einsatz von Fika auf einer HDD geben

Die beste Performance für Fika bzw. SPT im allgemeinen erzielt man mit einer starken CPU und mehr RAM.

## Installation

### Hosten mit Portfreigabe

Bevor diese Schritte abgearbeitet werden sollte sichergestellt werden, dass die Ports aus den Vorraussetzungen geöffnet sind. Wir bieten keine Hilfe bezüglich Portfreigabe an. Wenn keine Portfreigabe möglich ist oder kein Zugang zum Router besteht sollte ein VPN verwendet werden. 

**Firewall Konfiguration**

1. Portfreigabe für Port 6969 **TCP** der im Router weitergeleitet wurde (Eingehend und Ausgehend)
2. Portfreigabe für den **UDP** Port der im Router weitergeleitet wurde, Standardport ist 25565 (Eingehend und Ausgehend)
3. Wenn die Aufforderung von der Windows Firewall erscheint müssen alle Verbindungen (Öffentlich und Privat) für den Prozess freigegeben werden
4. Wenn weiterhin Probleme bestehen sollten: EscapeFromTarkov.exe (jeder Client) und AKI.Server.exe (Server host) für eingehende und ausgehende Verbindungen in der Windows Advanced Firewall hinzugefügen

**Allgemeines Setup**

1. [Aktuellsten Fika Release herunterladen](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Navigiere zum SPT Ordner und entpacke die heruntergeladenen Datei in diesen
3. Starte `Aki.Server.exe` einmalig damit alle Konfigurationsdatein für Fika erstellt werden, dann kann der Server wieder gestoppt werden (nach ca 20 Sekunden je nach System)
4. Navigiere zurück in den SPT Ordner und navigiere dort in den `Aki_Data\Server\configs` Ordner. Öffne `http.json`
5. Ändere `ip` zu `0.0.0.0`, dann speichere und schließe die Datei
6. Navigiere zurück in den SPT Ordner und dann in `user\mods\fika-server\assets\configs` und öffne `fika.jsonc`
7. Ändere die folgenden Einstellung so wie du sie haben möchtest. Speichere und schließe die Datei danach.
    - **useBtr**: Soll der BTR auf Streets of Tarkov spawnen?
    - **friendlyFire**: Soll Friendly fire erlaubt sein?
    - **dynamicVExfils**: Die Fahrzeug Extracts werden dynamisch angepasst je nachdem wie viele Spieler sich im Raid befinden
    - **allowFreeCam**: Erlaubt den Spielern im Raid die freie Kamera zu aktivieren und zu verwenden
    - **giftedItemsLoseFIR**: Items die zu einem anderen Spieler versendet werden verlieren ihren "Gefunden im Raid" Status
8. Starte `Aki.Server.exe` und warte das der Server vollständig geladen hat.
    - So sieht ein erfolgreicher Start aus:
    ```
    Started webserver at http://0.0.0.0:6969
    Started websocket at ws://0.0.0.0:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Starte `Aki.Launcher.exe`
10. Andere Spieler können nun deinem Server beitreten indem Sie die WAN IP des Hosts angeben, diese kann man über folgende Seite herausfinden [IPv4.ICanHazIP](https://ipv4.icanhazip.com/)

### Hosten mit einem VPN

Es wird ein VPN wie z.b. `Hamachi`, `ZeroTier` oder `Radmin` benötigt. 

1. [Aktuellsten Fika Release herunterladen](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Navigiere zum SPT Ordner und entpacke die heruntergeladenen Datei in diesen
3. Starte `Aki.Server.exe` einmalig damit alle Konfigurationsdatein für Fika erstellt werden, dann kann der Server wieder gestoppt werden (nach ca 20 Sekunden je nach System)
4. Navigiere zurück in den SPT Ordner und navigiere dort in den `Aki_Data\Server\configs` Ordner. Öffne `http.json`
5. Ändere die `ip` zu deiner VPN IP, dann speichere und schließe die Datei

Beispiel mit einer Fake Addresse (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. Navigiere zurück in den SPT Ordner und dann in `user\mods\fika-server\assets\configs` und öffne `fika.jsonc`
7. Ändere die folgenden Einstellung so wie du sie haben möchtest. Speichere und schließe die Datei danach.
    - **useBtr**: Soll der BTR auf Streets of Tarkov spawnen?
    - **friendlyFire**: Soll Friendly fire erlaubt sein?
    - **dynamicVExfils**: Die Fahrzeug Extracts werden dynamisch angepasst je nachdem wie viele Spieler sich im Raid befinden
    - **allowFreeCam**: Erlaubt den Spielern im Raid die freie Kamera zu aktivieren und zu verwenden
    - **giftedItemsLoseFIR**: Items die zu einem anderen Spieler versendet werden verlieren ihren "Gefunden im Raid" Status
8. Starte die `Aki.Server.exe` und warte das der Server vollständig geladen hat.
    - So sieht ein erfolgreicher Start mit der IP aus Schritt 5 aus:
    ```
    Started webserver at http://20.20.56.73:6969
    Started websocket at ws://20.20.56.73:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Starte `Aki.Launcher.exe` und klicke auf 'Settings'
10. Gib im `URL` Feld die VPN IP ein. Mit dem Beispiel aus Schritt 5 würde das so aussehen: `http://20.20.56.73:6969` (achte darauf, dass keine führenden `/` hinter dem Port stehen)

### Client mit Portfreigabe

1. [Aktuellsten Fika Release herunterladen](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Navigiere zum SPT Ordner und entpacke den Inhalt der eben heruntergeladenen Datei in diesen
3. Starte `Aki.Launcher.exe` und klicke auf 'Settings'
4. Gib im `URL` Feld die WAN IP ein. Als Beispiel könnte das so aussehen: `http://20.20.56.73:6969` (achte darauf, dass keine führenden `/` hinter dem Port stehen)
5. Wenn der Client Ingame die Session erstellen soll müssen alle Verbindungen (Öffentlich und Privat) freigegeben werden wenn die Aufforderung von der Windows Firewall erscheint

### Client mit einem VPN

1. [Aktuellsten Fika Release herunterladen](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Navigiere zum SPT Ordner und entpacke den Inhalt der eben heruntergeladenen Datei in diesen
3. Starte `Aki.Launcher.exe` und klicke auf 'Settings'
4. Gib im `URL` Feld die VPN IP ein. Mit dem Beispiel aus Schritt 5 würde das so aussehen: `http://20.20.56.73:6969` (achte darauf, dass keine führenden `/` hinter dem Port stehen)
5. Wenn der Client Ingame die Session erstellen soll müssen alle Verbindungen (Öffentlich und Privat) freigegeben werden wenn die Aufforderung von der Windows Firewall erscheint

## Features und Konfigurationen

### Features & How-To
**Fika** ermöglicht es P2P Sessions zu hosten um mit Freunden COOP zu Spielen. Der Host ist derjenige der den Großteil der Spiellogik während des Spiels steuert. Darunter fallen die Steuerrung der AI, Minenfelder, Scharfschützenzonen, der BTR, usw. Jeder Client ist für seinen eigenen Schaden verantwortlich. Das Umfasst zum einen den Schaden am eigenen Spieler als auch an der AI. Dadurch wird sofortiges Feedback ermöglicht sobald man auf AI schießt.

Um ein Spiel zu hosten muss eine Karte und die Zeit ausgewählt werden. Im letzten Schritt muss dann auf `Host Raid` geklickt werden. Dort muss die Anzahl der Spieler ausgewählt werden mit der gespielt werden soll (Einschließlich man selbst) und dann gewartet werden bis der Ladevorgang abgeschlossen ist. Sobald dieser Vorgang abgeschlossen ist können andere Spieler der Session beitreten. Sobald alle Spieler fertig geladen haben startet der Raid automatisch. 

**Weitere Features von Fika**
- Items senden
    - Rechtsklick auf ein Item im Stash ermöglicht es das Item zu einem anderen Account zu schicken
    - Diese Einstellung kann in den [Server Einstellungen](#server-configuration) angepasst werden
- Freie Kamera (Standardtaste: `F9`)
    - In der freien Kamera kann man die Kamera durch das Drücken der `T` Taste teleportieren
    - Durch `Linksklick/Rechtsklick` kann man zwischen den Spielern wechseln
    - Durch das Drücken der `Leertaste` kann man die Kamera auf den Kopf des Spielers fokussieren wenn man springt.
    - Durch das Drücken von `CTRL` beim Springen kann man sich im 3rd Person Mode hinter den Spieler schalten
    - Durch das Drücken der `HOME` Taste kann man die freie Kamera aktivieren
- Schadensmultiplikatoren für bestimmte Bereiche am eigenen Charakter
- Dynamische AI für den Host, dadurch wird die AI deaktiviert wenn sich niemand in der Nähe der AI befindet
- Individuelle AI Limits pro Karte
- "Culling" System um die Performance zu verbessern
- Individuelle Benachrichtigungen (Teammitglied gestorben, Boss durch Spieler erledigt, etc.)
- Makiersystem um bestimmte Gebiete im Spiel für Teammitglieder zu makieren
- Spieler Lebensanzeigen für Teammitglieder

Die meisten dieser Features können in den [Client Konfigurationen](#client-konfigurationen) eingestellt werden.

### Client Konfigurationen

Um die Client Konfigurationen zu öffen muss im Spiel die `F12` Taste gedrückt werden. Unter dem Reiter `Fika Core` können die Einstellungen vorgenommen werden.

**Coop**

- **Show Notifications**: Aktiviert individuelle Benachrichtigungen wenn ein Spieler stirbt, extracted, einen Boss erledigt, etc.
- **Auto Extract**: Extracted automatisch wenn als Client gespielt wird anstatt in die freie Kamera zu wechseln.
- **Show Extract Message**: Bestimmt ob ein Extract Nachricht angezeigt werden soll wenn ein Spieler stirbt/extracted.

**Coop | Custom**

- **Show Player Name Plates**: Lebensanzeigen und Namen aktivieren/deaktivieren.
- **Show HP% instead of bar**: Zeigt das Leben in % an statt der Lebensanzeige.
- **Show Player Faction Icon**: Zeigt das Spieler Fraktionsicon neben der Lebensanzeige an.
- **Name Plate Scale**: Größe der Namensanzeigen
- **Ping System**: Aktiviert/Deaktiviert das Makiersystem. Wenn aktiviert können Makierungen empfangen und über die Makierungstaste verschickt werden.
- **Ping Button**: Taste zum versenden von Makierungen.
- **Ping Color**: Die Farbe deiner Makierung wie sie andere Spieler sehen.
- **Ping Size**: Multiplikator für die Größe der Makierung.
- **Play Ping Animation**: Spielt eine Makierungsanimation ab. Kann Spielperformance beeinflussen.

**Coop | Debug**

- **Free Camera Button**: Taste um die freie Kamera zu aktivieren

**Performance**

- **Dynamic AI**: Das dynamische AI System sorgt dafür, dass AI die weit von Spielern entfernt ist deaktiviert wird um die Performance zu erhöhen.
- **Dynamic AI Range**: Die Entfernung ab der AI dynamisch deaktivert wird.
- **Dynamic AI Rate**: Intervall in dem DynamicAI die Entfernung zu allen Spielern prüft.
- **Culling System**: Diese Einstellung aktiviert/deaktivert das "Culling" System. Wenn Spieler außerhalb der Culling Reichweite sind werden die Animationen vereinfacht. Dies kann die Performance in manchen Szenarios stark verbessern.
- **Culling Range**: Die Entfernung ab der "Culling" auf Spieler angewendet wird.

**Performance | Max Bots**

- **Enforced Spawn Limits**: Erzwinge Spawn Limits für das Spawnen von Bots. Dies stellt sicher, dass nicht mehr Bots gespawned werden als normal der Fall wäre. Diese Einstellung hat Auswirkungen darauf wenn Mods verwendet werden die das Spawnverhalten von Bots beeinflussen.
- **Max Bots** `MAP`: Maximale Anzahl von Bots die zur selben Zeit auf `MAP` aktiv sein können. Diese Einstellung ist vorallem für schwächere PCs von Vorteil. Wenn diese Einstellung auf 0 gesetzt wird, werden keine Bots gespawned.

**Network**

- **Native Sockets**:  Native Sockets werden für den Spiel Traffic verwendet. Die Einstellung ermöglicht direkte Socket Kommunikation für das Senden und Empfangen von Anfragen. Hierdurch wird die Performance maßgäblich verbessert. Diese Einstellung ist nur für Windows und Linux und funktioniert ggf. nicht immer.
- **Force IP**: Zwingt den Server diese IP beim Broadcasten zum Backendsystem zu verwenden anstatt eine IP automatisch zu beziehen. Sollte hier kein Wert eingetragen werden wird diese Option deaktiviert. Diese Einstellung wird benötigt, wenn über einen VPN gehostet wird. Dazu hier die persönliche IP aus dem VPN eintragen.
- **Force Bind IP**: Zwingt den Server beim starten diese IP zu verwenden. Sollte hier kein Wert eingetragen werden wird diese Option deaktiviert. Diese Einstellung wird benötigt, wenn über einen VPN gehostet wird. Dazu hier die persönliche IP aus dem VPN eintragen.
- **Auto Server Refresh Rate**: Definiert wie oft in x Sekunden der Client den Server, während man sich in der Lobby befindet, nach neuen Matches abfragt. 
- **UDP Port**: Gibt an welcher Port für UDP Gameplay Pakete verwendet werden soll.
- **Use UPnP**: Wenn aktiviert wird versucht Ports über UPnP zu öffnen. Diese Option ist nützlich wenn man selbst keine Ports freigeben kann der Router aber UPnP unterstützt.

**Gameplay**

- **Head Damage Multiplier**: X Schadensmultiplikator für Schaden der im Kopfbereich erleidet wird. 0.2 = 20%
- **Armpit Damage Multiplier**: X Schadensmultiplikator für Schaden der im Achselbereich erleidet wird. 0.2 = 20%

### Server Configuration

Die Servereinstellungen können in folgendem Ordner gefunden werden `user\mods\fika-server\assets\configs`. Dazu `fika.jsonc` mit einem Texteditor öffnen.

```json
{
    "client": {
        "useBtr": true, // Soll der BTR auf Streets of Tarkov spawnen?, Standardwert: true
        "friendlyFire": true, // Soll Friendly fire erlaubt sein?, Standardwert: true
        "dynamicVExfils": false, // Die Fahrzeug Extracts werden dynamisch angepasst je nachdem wie viele Spieler sich im Raid befinden statt normal 4 Spieler zu unterstützen, Standardwert: false
        "allowFreeCam": false, // Erlaubt den Spielern im Raid die freie Kamera zu aktivieren und zu verwenden, Standardwert: false
        "allowItemSending": true // Erlaubt es anderen Spielern Items zu senden, Standardwert: true
    },
    "server": {
        "giftedItemsLoseFIR": true // Items die zu einem anderen Spieler versendet werden verlieren ihren "Gefunden im Raid" Status, Standardwert: true
    }
}
```
