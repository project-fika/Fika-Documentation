# Fika - Un mod multijugador para AKI

<details open>
    <summary>Tabla de contenidos</summary>
    <ol>
        <li><a href="#what-is-fika">¿Que es Fika?</a></li>
        <li><a href="#license">Licencia</a></li>
        <li>
            <a href="#prerequisites">Prerrequisitos</a>
            <ul>
                <li><a href="#hosting">Hosteo</a></li>
                <li><a href="#client">Cliente</a></li>
            </ul>
        </li>
        <li><a href="#hardware-requirements">Requisitos de hardware</a></li>
        <li>
            <a href="#installation">Instalación</a>
            <ul>
                <li><a href="#host-using-port-forwarding">Hosteo usando redirección de puertos</a></li>
                <li><a href="#host-using-a-vpn">Hosteo usando una VPN</a></li>
                <li><a href="#client-using-port-forwarding">Cliente usando redirección de puertos</a></li>
                <li><a href="#client-using-a-vpn">Cliente usando una VPN</a></li>
            </ul>
        </li>
        <li>
            <a href="#features-and-configuration">Características y configuración</a>
            <ul>
                <li><a href="#features--how-to">Características y cómo</a></li>
                <li><a href="#client-configuration">Configuración del cliente</a></li>
                <li><a href="#server-configuration">Configuración del servidor</a></li>
            </ul>
        </li>
    </ol>
</details>

## ¿Qué es Fika?

**Fika** es un mod para **SPT-Aki** que te permite jugar en COOPERATIVO con tus amigos. Utiliza una conexión P2P-UDP para una experiencia moderna y del alto rendimiento. Los objetivos principales de Fika son: rendimiento, precisión y soporte de mods. Fika está actualmente mantenido por el equipo de Fika.
¡Puedes unirte a nuestro Discord [aqui](https://discord.gg/project-fika)!.

## Licencia

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Este proyecto está bajo la licencia [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en).

- Solo puedes compartir Fika siempre y cuando otorgues los créditos adecuados, no está permitido usarlo con propósitos comerciales y no es posible su modificación.
- No está permitido monetizar tu servidor en términos de pagos o donaciones.
- No está permitido hostear servidores públicos masivos, Fika está destinado para jugarlo en COOPERATIVO con tus amigos.
- No esta permitido copiar y/o replicar el código de Fika, tampoco el usar assets creados manualmente por nuestros desarrolladores y artistas.

## Prerrequisitos

Fika requiere conocimiento general de computadoras, redes y Aki. Si no estas familiarizado con estos conceptos, este proyecto no es para ti. Por favor intenta entender y respetar esto.

### Hosteo

- ISP y Router que soporte **Redirección de puertos** o **UPnP**.
- Puerto TCP 6969 abierto para AKI Server.
- Puerto UDP abierto para tráfico P2P, por defecto el 25565 (Si se usa UPnP, este punto no es requerido).
- SPT instalado y funcionando, igual a la versión de Fika a usar.
- Acceso a tu Firewall de Windows.
- Una velocidad de internet de por lo menos 20 Mbit/s simétricos (Carga y Descarga). El promedio de cada cliente es de 400 kbit/s.

Si no puedes usar la redirección de puertos, puedes usar una VPN como `Hamachi`, `ZeroTier` or `Radmin`.

### Cliente

- ISP y Router que soporte **Redirección de puertos** o **UPnP** | **NOTA**: Esto es solo requerido si vas a ser el host dentro del juego.
- Puerto UDP abierto para tráfico P2P, por defecto el 25565 (Si se usa UPnP, este punto no es requerido) | **NOTA**: Igual al punto anterior.
- SPT instalado y funcionando, igual a la versión de Fika a usar.
- Acceso a tu Firewall de Windows.
- Una velocidad de internet de por lo menos 20 Mbit/s simétricos (Carga y Descarga).

### Ambos

- Archivos de Fika actualizados.

## Requisitos de Hardware

Estas son los requisitos recomendados para una experiencia fluida:

- **CPU**: i7 8700k / Ryzen 7 2700x.
- **GPU**: GTX 1060 / RX 580.
- **Memoria** 16 GB mínimo, 32 GB recomendado.
- **Almacenamiento**: El uso de un SSD es obligatorio, no esperes soporte al usar Fika en un HDD.

La mejora más significativa en Fika (y SPT en general) será al usar una CPU más potentes y mayor cantidad de RAM.

## Instalación

### Hostear usando redirección de puertos

Antes de comenzar con los siguientes pasos, asegúrate de que tienes todos los puertos de la sección de Prerrequisitos redireccionados. No brindaremos soporte para abrir tus puertos. Si no tienes acceso a tu router o no puedes redireccionar, usa una VPN.

**Configuración de Firewall**

1. Redirecciona el puerto **TCP** 6969 en tu router (de entrada y de salida).
2. Redirecciona el puerto **UDP** que vas a usar en tu router, por defecto el 25565 (de entrada y de salida).
3. Cuando Windows lo solicite, permite ***todas*** las conexiones en tu Firewall.
4. Si aun sigues teniendo problemas, te sugerimos agregar reglas para EscapeFromTarkov.exe (todos) y AKI.Server.exe (para quien hostea el servidor) para conexiones de entrada y de salida en las opciones avanzadas de Windows Firewall.

**Instalación general**

1. [Descarga la última versión de Fika](https://discord.com/channels/1202292159366037545/1224454502531469373) (tendrás de unirte a nuestro [Discord](https://discord.gg/project-fika) primero).
2. Dirígete a tu ruta de instalación de SPT y extrae el contenido del archivo dentro de la carpeta.
3. Ejecuta `Aki.Server.exe` una vez para que genere los archivos de configuración para Fika, luego ciérralo nuevamente.
4. Regresa a la carpeta principal y dirígete a `Aki_Data\Server\configs` y abre el archivo `http.json`.
5. Cambia la `ip` a `0.0.0.0`, guarda los cambios y cierra el archivo.
6. Dirígete a `user\mods\fika-server\assets\configs` y abre el archivo `fika.jsonc`.
7. Cambia cualquiera de las configuraciones a tu gusto.
    - **useBtr**: determina si el BTR debería hacer aparecer o no al jugar en Streets.
    - **friendlyFire**: determina si el fuego amigo debe estar activado o no.
    - **dynamicVExfils**: escala el máximo de jugadores que pueden extraer con los vehículos de extracción con la cantidad de jugadores en la raid.
    - **allowFreeCam**: permite a los jugadores cambiar a la cámara libre dentro de la raid.
    - **giftedItemsLoseFIR**: si objetos enviados deberían perder el estatus FiR.
8. Ejecuta `Aki.Server.exe` y espera a que termine de cargar.
    - Debería de verse de la siguiente manera si se configuro correctamente:
    ```
    Started webserver at http://0.0.0.0:6969
    Started websocket at ws://0.0.0.0:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Ejecuta `Aki.Launcher.exe`
10. Tus amigos pueden conectarse a tu servidor usando tu IP WAN, la cual puedes verificar en la página [IPv4.ICanHazIP](https://ipv4.icanhazip.com/).

### Hostear un servidor con una VPN

Necesitaras una VPN como `Hamachi`, `ZeroTier` o `Radmin`. 

1. [Descarga la última versión de Fika](https://discord.com/channels/1202292159366037545/1224454502531469373) (tendrás de unirte a nuestro [Discord](https://discord.gg/project-fika) primero)
2. Dirígete a tu ruta de instalación de SPT y extrae el contenido del archivo dentro de la carpeta.
3. Ejecuta `Aki.Server.exe` una vez para que genere los archivos de configuración para Fika, luego ciérralo nuevamente.
4. Regresa a la carpeta principal y dirígete a `Aki_Data\Server\configs` y abre el archivo `http.json`.
5. Cambia la `ip` con la IP de tu VPN, guarda los cambios y cierra el archivo.


Ejemplo con una dirección IP falsa: (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. Dirígete a `user\mods\fika-server\assets\configs` y abre el archivo `fika.jsonc`.
7. Cambia cualquiera de las configuraciones a tu gusto.
    - **useBtr**: determina si el BTR debería hacer aparecer o no al jugar en Streets.
    - **friendlyFire**: determina si el fuego amigo debe estar activado o no.
    - **dynamicVExfils**: escala el máximo de jugadores que pueden extraer con los vehículos de extracción dependiendo la cantidad de jugadores en la raid.
    - **allowFreeCam**: permite a los jugadores cambiar a la cámara libre dentro de la raid.
    - **giftedItemsLoseFIR**: si los objetos enviados deberían perder el estatus FiR.
8. Ejecuta `Aki.Server.exe` y espera a que termine de cargar.
    - Debería de verse de la siguiente manera si se configuro correctamente usando la dirección IP en el paso 5:
    ```
    Started webserver at http://20.20.56.73:6969
    Started websocket at ws://20.20.56.73:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9. Ejecuta `Aki.Launcher.exe` y da clic en 'Settings'.
10. En el campo de `URL`, modifícalo con la IP de tu VPN. Usando el ejemplo del paso 5 seria: `http://20.20.56.73:6969` (recuerda eliminar las barras diagonales finales `/`).

### Cliente usando la redirección de puertos

1. [Descarga la última versión de Fika](https://discord.com/channels/1202292159366037545/1224454502531469373).
2. Dirígete a tu ruta de instalación de SPT y extrae el contenido del archivo dentro de la carpeta.
3. Ejecuta `Aki.Launcher.exe` y da clic en 'Settings'
4. En el campo de `URL`, modifícalo con la IP WAN del host. Por ejemplo: `http://20.20.56.73:6969` (recuerda eliminar las barras diagonales finales `/`)
5. Si se hostea dentro del juego, permite todas las conexiones (públicas y privadas) cuando el Firewall de Windows lo requiera. 

### Cliente usando una VPN

1. [Descarga la última versión de Fika](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Dirígete a tu ruta de instalación de SPT y extrae el contenido del archivo dentro de la carpeta.
3. Ejecuta `Aki.Launcher.exe` y da clic en 'Settings'
4. En el campo de `URL`, modifícalo con la IP de la VPN del host. Usando el ejemplo del paso 5, seria: `http://20.20.56.73:6969` (recuerda eliminar las barras diagonales finales `/`)
5. Si se hostea dentro del juego, permite todas las conexiones (públicas y privadas) cuando el Firewall de Windows lo requiera.

## Características y configuración

### Características y Cómo
**Fika** te permite hostear una sesión P2P con tus amigos en COOPERATIVO. El host es quien controla la mayoría de la lógica al jugar, como controlar IA, campos minados, zonas de francotirador, el BTR, etc. Cada cliente es responsable de su propio daño, tanto en ellos mismos como en la IA. Esto significa que disparar a una IA se siente responsivo y rápido.

Para hostear una raid, selecciona un mapa y tiempo, y en la pantalla final presiona `Host Raid`. Selecciona la cantidad de jugadores que estarán jugando (incluyéndote) y espera a que termine de cargar. Una vez listo, otros jugadores pueden unirse en tu sesión y una vez todos terminen de cargar, comenzara automáticamente.

**Otras características de Fika**
- Envió de objetos.
    - Clic derecho a un objeto dentro de tu alijo para enviar a otra cuenta.
    - Puede ser personalizado en la configuración del [servidor](#server-configuration).
- Cámara libre (Por defecto la tecla `F9`).
    - En la cámara libre puedes teletransportarte a la posición de la cámara presionando la tecla `T`.
    - Puedes saltar a otro jugador con clic `Izquierdo/Derecho`.
    - Puedes pegarte a sus cabezas manteniendo presionado `ESPACIO` al saltar a otro jugador.
    - Puedes pegarte a sus espaldas en una vista de tercera persona al mantener presionado `CTRL` al saltar a otro jugador.
    - Puedes presionar la tecla `HOME` para alternar temporalmente los controles de la cámara libre.
- Multiplicadores de daño para áreas cruciales de tu cuerpo.
- IA dinámica para el host, el cual desactiva IA cuando nadie está cerca.
- Cantidad de IA personalizable para cada mapa.
- Sistema de sacrificios para incrementar el rendimiento.
- Notificaciones personalizadas (al morir un compañero de equipo, un jugador mato a un jefe, etc.).
- Sistema de Pings, para hacer ping a una zona en el juego para tus compañeros de equipo.
- Barras de salud para tus compañeros de equipo.

La mayoría de estas características son configuradas en [Configuración del cliente](#client-configuration).

### Configuración del cliente

Para abrir tu configuración de cliente, presiona la `F12` dentro del juego. Dirígete a la sección de `Fika Core` para modificar tus configuraciones.

**Cooperativo**

- **Show Notifications**: Activa las notificaciones personalizadas cuando un jugador muere, extrae, mata a un jefe, etc.
- **Auto Extract**: Extrae automáticamente al jugar como cliente en lugar de entrar a la cámara libre.
- **Show Extract Message**: Si se debe mostrar el mensaje de extracción después de morir/extraer.

**Cooperativo | Personalizado**

- **Show Player Name Plates**: Alternar entre las barras de vida y nombres.
- **Show HP% instead of bar**: Muestra el % de vida en lugar de mostrar una barra.
- **Show Player Faction Icon**: Muestra el icono de facción del jugador a lado de la barra de vida.
- **Name Plate Scale**: Tamaño de las placas de los nombres.
- **Ping System**: Alterna el sistema de Pings. Si esta activado puedes enviar y recibir pings al presionar la tecla de ping.
- **Ping Button**: Tecla usada para enviar pings.
- **Ping Color**: El color mostrado de tus pings para otros jugadores.
- **Ping Size**: Multiplicador del tamaño del ping.
- **Play Ping Animation**: Reproduce la animación de señalamiento automáticamente al hacer ping. Puede interferir con el gameplay.

**Cooperativo | Debug**

- **Free Camera Button**: Tecla usada para alternar la cámara libre.

**Rendimiento**

- **Dynamic AI**: Utiliza el sistema dinámico de IA, desactiva la IA cuando están fuera del rango de cualquier jugador.
- **Dynamic AI Range**: El rango al cual la IA se desactivará dinámicamente.
- **Dynamic AI Rate**: Que tan frecuentemente el sistema de IA dinámica escaneara el rango de todos los jugadores.
- **Culling System**: Ya sea usar el sistema de sacrificio o no. Cuando los jugadores estén fuera del rango de selección, sus animaciones serán simplificadas. Esto puedes mejorar drásticamente el rendimiento en ciertos escenarios.
- **Culling Range**: El rango al cual los jugadores deberían ser sacrificados.

**Rendimiento | Bots máximos**

- **Enforced Spawn Limits**: Aplica limistes de generación al generar bots, asegurándose de no sobrepasar los límites por básicos. Esto afecta principalmente al usar mods de aparición de IA o cualquier modificación al límite de bots.
- **Max Bots** `MAP`: Cantidad máxima de bots que pueden estar activos al mismo tiempo en el `MAPA`. Útil si tienes una PC limitada. Ajustar a 0 para desactivar.

**Red**

- **Native Sockets**:  Sockets Nativos para el tráfico del juego. Esto utiliza llamadas directas a sockets para él envió/recepción para incrementar drásticamente la velocidad y redicar la carga de GC. Solo para Windows/Linux y es posible que no siempre funcione.
- **Force IP**: Obliga al servidor al hostear a usar esta dirección IP al transmitir al backend en lugar de intentar recuperarlo automáticamente. Deja en blanco para desactivar. Esto es necesario al usar una VPN, utiliza tu dirección IP del VPN personal.
- **Force Bind IP**: Obliga al servidor al hostear a utilizar esta dirección IP local al iniciar el servidor. Deja en blanco para desactivar. Esto es necesario al usar una VPN, utiliza tu dirección IP del VPN personal.
- **Auto Server Refresh Rate**: Cada X segundos el cliente pedirá al servidor la lista de partidas al estar en la pantalla de lobby.
- **UDP Port**: Puerto a usar por los paquetes UDP de juego.
- **Use UPnP**: Intenta abrir puerto usando UPnP. Útil si no puedes abrir puertos por ti mismo pero el router soporta UPnP.

**Gameplay**

- **Head Damage Multiplier**: Multiplicador X del daño recibido en la hitbox de la cabeza. 0.2 = 20%
- **Armpit Damage Multiplier**: Multiplicador X del daño recibido en las hitbox de las axilas. 0.2 = 20%

### Configuración del servidor

La configuración del servidor puede encontrarse en la carpeta `user\mods\fika-server\assets\configs`. Abre el archivo `fika.jsonc` con un editor de texto.

```json
{
    "client": {
        "useBtr": true, // Si el BTR debe hacer aparecer en Streets, por defecto: true
        "friendlyFire": true, // Si el fuego amigo esta activado, por defecto: true
        "dynamicVExfils": false, // Si el vehículo de extracción debe aumentar la cantidad de jugadores que puede extraer en la raid en lugar de 4 por defecto, por defecto: false
        "allowFreeCam": false, // Si la cámara libre debe estar activada, por defecto: false
        "allowItemSending": true // si el envio de objetos debe estar activado, por defecto: true
    },
    "server": {
        "giftedItemsLoseFIR": true // Si los objetos enviados deberían perder el estado FiR, por defecto: true
    }
}
```