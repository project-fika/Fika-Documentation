<details open>
    <summary>İçindekiler</summary>
    <ol>
        <li><a href="#fika-nedir">Fika Nedir</a></li>
        <li><a href="#lisans">Lisans</a></li>
        <li>
            <a href="#gereksinimler">Önkoşullar</a>
            <ul>
                <li><a href="#hosting">Hosting</a></li>
                <li><a href="#istemci">İstemci</a></li>
            </ul>
        </li>
        <li><a href="#donanım-gereksinimleri">Donanım Gereksinimleri</a></li>
        <li>
            <a href="#kurulum">Kurulum</a>
            <ul>
                <li><a href="#port-yönlendirme-kullanarak-host">Port Yönlendirme Kullanarak Host</a></li>
                <li><a href="#vpn-kullanarak-host">VPN Kullanarak Host</a></li>
                <li><a href="#port-yönlendirme-kullanarak-istemci">Port Yönlendirme Kullanarak İstemci</a></li>
                <li><a href="#vpn-kullanarak-istemci">VPN Kullanarak İstemci</a></li>
            </ul>
        </li>
        <li>
            <a href="#özellikler-ve-yapılandırma">Özellikler ve Yapılandırma</a>
            <ul>
                <li><a href="#özellikler-ve-rehber">Özellikler & Rehber</a></li>
                <li><a href="#istemci-yapılandırması">İstemci Yapılandırması</a></li>
                <li><a href="#sunucu-yapılandırması">Sunucu Yapılandırması</a></li>
            </ul>
        </li>
    </ol>
</details>


## Fika Nedir

**Fika**, arkadaşlarınızla COOP oynamanıza olanak sağlayan bir **SPT-Aki** modudur. Modern ve performanslı bir deneyim için P2P-UDP bağlantısı kullanır. Fika'nın ana hedefleri: performans, doğruluk ve mod desteği. Fika şu anda Fika ekibi tarafından bakım altında. 
Discord'umuza [buradan](https://discord.gg/project-fika)! katılabilirsiniz!

## Lisans

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Bu proje, [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.tr). altında lisanslanmıştır.

- Fika'yı yalnızca uygun krediler verilmişse, ticari amaçlar için kullanılmadığında ve değiştirilmediği sürece paylaşabilirsiniz.
- Sunucunuzu ödeme veya bağışlar açısından para kazanamazsınız.
- Büyük ölçekli halka açık sunucuları barındıramazsınız, Fika arkadaşlarınızla COOP için tasarlanmıştır.
- Fika tarafından yapılan kodı kopyalayıp/veya çoğaltamazsınız, ayrıca geliştiricilerimiz ve sanatçılarımız tarafından el ile yapılan varlıkları kullanamazsınız.
 
## Gereksinimler

Fika, bilgisayarlar, ağlar ve Aki hakkında genel bilgi gerektirir. Bu konseptlerle rahat hissetmiyorsanız, bu proje sizin için değildir. Lütfen bunu anlamaya ve saygı göstermeye çalışın.

### Hosting

- Port Forwarding veya UPnP destekleyen bir yönlendirici ve ISP
- AKI Sunucusu için TCP port 6969 açık
- P2P trafiği için UDP Port açık, varsayılan 25565 (UPnP kullanıyorsanız bu gerekli değildir)
- SPT yüklü ve çalışıyor olmalı, Fika'nın kullanacağınız sürümle eşleşmelidir
- Windows Güvenlik Duvarına erişim
- En az 20 Mbit/s yukarı ve aşağı hızı önerilir. Her istemci ortalama olarak 400 kbit/s kullanır.

Port yönlendirmesi yapamazsanız, `Hamachi`, `ZeroTier` veya `Radmin` gibi bir VPN kullanabilirsiniz.

### Istemci

- Port Forwarding veya UPnP destekleyen bir yönlendirici ve ISP | NOT: Bu, oyun içinde barındırıyorsanız gereklidir
- P2P trafiği için UDP Port açık, varsayılan 25565 (UPnP kullanıyorsanız bu gerekli değildir) | NOT: Yukarıdakiyle aynı
- SPT yüklü ve çalışıyor olmalı, Fika'nın kullanacağınız sürümle eşleşmelidir
- Windows Güvenlik Duvarına erişim
- En az yukarı aşağı 20 Mbit/s bağlantı hızı önerilir

### Her İki Taraf

 - En son Fika dosyaları

## Donanım Gereksinimleri

Sorunsuz bir deneyim için önerilen sistem gereksinimleri aşağıdaki gibidir:

- **İşlemci**: i7 8700k / Ryzen 7 2700x
- **Grafik**: GTX 1060 / RX 580
- **Hafıza** Minimum 16 GB, 32 GB önerilen
- **Depolama**: SSD zorunludur, Fika'yı bir HDD üzerinde çalıştırırken destek beklemeyin.

Fika için (ve genel olarak SPT'de) en büyük performans kazancı, daha güçlü bir CPU ve RAM ile sağlanır.

## Kurulum

### Port Yönlendirme Kullanarak Host

Bu adımlara başlamadan önce, Önkoşullar'da gereken tüm portları yönlendirmiş olduğunuzdan emin olun. Portlarınızı açmanıza yardımcı olmayacağız. Yönlendiricinize erişiminiz yoksa veya port yönlendirmesi yapamazsanız, VPN kullanın.

**Güvenlik Duvarı Yapılandırması**

1. Yönlendiricinizde port 6969 TCP'yi port yönlendirmesi yapın (hem giriş hem de çıkış için)
2. Yönlendiricinizde kullanacağınız UDP portunu yönlendirin, varsayılan 25565 (hem giriş hem de çıkış)
3. Windows tarafından sizden bağlantılara izin vermeniz istendiğinde tüm bağlantılarınız için güvenlik duvarında izin verin
4. Hala sorun yaşıyorsanız, Windows Gelişmiş Güvenlik Duvarı'nda EscapeFromTarkov.exe (herkes) ve AKI.Server.exe (sunucu host) için gelen ve giden bağlantılara izin vermenizi öneririz.

**Genel Kurulum**

1. [En son Fika derlemesini indirin](https://discord.com/channels/1202292159366037545/1224454502531469373) (önce [Discord](https://discord.gg/project-fika) kanalımıza katılmanız gerekmektedir)
2. SPT kurulumunuza gidin ve arşivin içeriğini klasöre çıkarın
3. `Aki.Server.exe`'yi bir kez başlatın ve Fika için yapılandırma dosyalarını oluşturmasına izin verin, ardından tekrar kapatın
4. Ana klasöre geri dönün ve `Aki_Data\Server\configs` klasörüne gidin ve `http.json`'ı açın
5. `ip`'yi `0.0.0.0` olarak değiştirin, ardından dosyayı kaydedip kapatın
6. `user\mods\fika-server\assets\configs` klasörüne gidin ve `fika.jsonc`'yi açın
7. Ayarları beğeninize göre değiştirin.
    - **useBtr**: Streets oynarken BTR'ın spawn olup olmayacağı
    - **friendlyFire**: Dost ateşinin etkin olup olmayacağı
    - **dynamicVExfils**: Araçla exfil yapılacak maksimum oyuncu sayısının, raid sırasında oyuncu sayısıyla otomatik olarak ölçeklenip ölçeklenmeyeceği
    - **allowFreeCam**: Oyuncuların raid sırasında serbestçe free cam'ı açıp açamayacağı
    - **giftedItemsLoseFIR**: Gönderilen öğelerin FiR durumunu kaybedip kaybetmeyeceği
8. `Aki.Server.exe`'yi başlatın ve yüklenmesini bekleyin
    - Eğer sunucu başarıyla başladıysa böyle görünecektir:
    ```
    Web sunucusu başlatıldı: http://0.0.0.0:6969
    WebSocket başlatıldı: ws://0.0.0.0:6969
    Sunucu çalışıyor, SPT oynarken kapatmayın, İyi oyunlar!!
    ```
9. `Aki.Launcher.exe`'yi başlatın
10. Arkadaşlarınız, [IPv4.ICanHazIP](https://ipv4.icanhazip.com/) sitesini kullanarak WAN IP'nizi bulup, sunucunuza bağlanabilir.

### VPN kullanarak Host

`Hamachi`, `ZeroTier` veya `Radmin` gibi bir VPN'e ihtiyacınız var.

1. [En son Fika derlemesini indirin](https://discord.com/channels/1202292159366037545/1224454502531469373) (önce [Discord](https://discord.gg/project-fika) kanalımıza katılmanız gerekmektedir)
2. SPT kurulumunuza gidin ve arşivin içeriğini klasöre çıkarın
3. `Aki.Server.exe`'yi bir kez başlatın ve Fika için yapılandırma dosyalarını oluşturmasına izin verin, ardından tekrar kapatın
4. Ana klasöre geri dönün ve `Aki_Data\Server\configs` klasörüne gidin ve `http.json`'ı açın
5. `ip`'yi VPN IP'nize değiştirin, ardından dosyayı kaydedip kapatın
Sahte bir adresle örnekleme (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. `user\mods\fika-server\assets\configs` dizinine gidin ve `fika.jsonc` dosyasını açın.
7. Ayarları kendi zevkinize göre değiştirin.
    - **useBtr**: Sokaklarda oynarken BTR'nin spawn edilip edilmeyeceği
    - **friendlyFire**: Dost ateşinin etkin olup olmayacağı
    - **dynamicVExfils**: Oyuncu sayısıyla araç exfil maksimum oyuncularını otomatik olarak ölçeklendirme
    - **allowFreeCam**: Oyuncuların baskın sırasında serbestçe serbest kamera geçişini etkinleştirmek
    - **giftedItemsLoseFIR**: Gönderilen öğelerin FiR durumunu kaybedip kaybetmeyeceği
8. `Aki.Server.exe`'yi başlatın ve yüklenmesini bekleyin
    - Başarılı bir şekilde başlatıldığında görünmesi gereken budur: Örnek IP'yi 5. adımda kullanarak başladıysa:
    ```
    Web sunucusu başlatıldı: http://20.20.56.73:6969
    Websocket başlatıldı: ws://20.20.56.73:6969
    Sunucu çalışıyor, SPT oynarken kapatmayın, İyi oyunlar!!
    ```
9. `Aki.Launcher.exe`'yi başlatın ve 'Ayarlar'ı tıklayın
10. `URL` alanında, VPN IP'nizi yansıtacak şekilde değiştirin. 5. adımdaki örneği kullanarak: `http://20.20.56.73:6969` (sonunda herhangi bir ileri eğik çizgi `/` varsa kaldırmayı unutmayın)

### Port Yönlendirme Kullanarak Istemci

1. [En son Fika sürümünü indirin](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. SPT kurulumunuza gidin ve arşivin içeriğini klasöre çıkartın
3. `Aki.Launcher.exe`'yi başlatın ve 'Ayarlar'ı tıklayın
4. `URL` alanını, ana bilgisayarın WAN IP'sini yansıtacak şekilde değiştirin. Örneğin: `http://20.20.56.73:6969` (sonunda herhangi bir ileri eğik çizgi `/` varsa kaldırmayı unutmayın)
5. Oyun içinde barındırıyorsanız, Windows Güvenlik Duvarı tarafından istendiğinde tüm bağlantılara (genel ve özel) izin verin

### VPN Kullanarak Istemci

1. [En son Fika sürümünü indirin](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. SPT kurulumunuza gidin ve arşivin içeriğini klasöre çıkartın
3. `Aki.Launcher.exe`'yi başlatın ve 'Ayarlar'ı tıklayın
4. `URL` alanını, ana bilgisayarın VPN IP'sini yansıtacak şekilde değiştirin. 5. adımdaki örneği kullanarak: `http://20.20.56.73:6969` (sonunda herhangi bir ileri eğik çizgi `/` varsa kaldırmayı unutmayın)
5. Oyun içindeyken, Windows Güvenlik Duvarı tarafından uyarı çıktığında tüm bağlantılara (genel ve özel) izin verin

## Özellikler ve Yapılandırma

### Özellikler ve Rehber
**Fika**, arkadaşlarınızla COOP oynamak için P2P oturumları barındırmanıza olanak tanır. Sunucu, yapay zeka, mayın tarlaları, keskin nişancı bölgeleri, BTR vb. gibi oyun sırasında çoğu mantığı kontrol eden kişidir. Her istemci kendi zararından sorumludur, hem kendilerine hem de yapay zekaya karşı. Bu, bir yapay zekaya ateş etmenin duyarlı ve hızlı hissettirdiği anlamına gelir.

Bir oyun barındırmak için, bir harita ve zaman seçin, ardından son ekranda `Baskın Barındır`ı tıklayın. Oynayacak olan oyuncuların (kendiniz dahil) miktarını seçin ve yüklenmesini bekleyin. Hazır olduğunda diğer insanlar oturumunuza katılabilir, herkes yüklenmeyi bitirdiğinde otomatik olarak başlayacaktır.

**Fika'nın Diğer Özellikleri**
- Öğe Gönderme
    - Stash'teki bir öğeyi başka bir hesaba göndermek için sağ tıklayın
    - [Sunucu](#server-configuration) yapılandırmasında özelleştirilebilir
- Serbest kamera (varsayılan `F9` tuşu)
    - Serbest kamerada, `T` tuşuna basarak kameranın konumuna teleport yapabilirsiniz
    - `Sol/Sağ` tıklama ile başka bir oyuncuya geçebilirsiniz
    - Zıplarken `SPACE` tuşunu basılı tutarak başlarına takılabilirsiniz
    - 3. pozisyon görünümünde arkalarına takılabilirsiniz `CTRL` tuşunu basılı tutarak zıplarken
    - Geçici olarak serbest kamera kontrollerini açmak için `HOME` tuşuna basabilirsiniz
- Kendi üzerinizde kritik bölgeler için hasar çarpanları
- Sunucular için dinamik yapay zeka, kimse yakınında olmadığında yapay zekayı devre dışı bırakır
- Haritaya özgü özel yapay zeka sınırları
- Performansı artırmak için kesme sistemi
- Özel bildirimler (takım arkadaşı öldü, patron bir oyuncu tarafından öldürüldü, vb.)
- Takım arkadaşlarınız için oyun içi can işaretleri

Bu özelliklerin çoğu [istemci yapılandırmasında](#client-configuration) yapılandırılır.

### Istemci Yapılandırması

Oyundayken istemci yapılandırmanızı açmak için `F12` tuşuna basın. Ayarları yapılandırmak için `Fika Core` bölümüne gidin.

**COOP**

- **Show Notifications**: Bir oyuncu ölünce, çıkarılınca, bir patronu öldürünce vb. özel bildirimleri etkinleştirin.
- **Auto Extract**: Ücretsiz kamera yerine bir istemci olarak oynarken otomatik olarak çıkarın.
- **Show Extract Message**: Ölünce/çıkarılınca çıkar mesajını gösterilsin mi?

**COOP | Özel**

- **Show Player Name Plates**: Sağlık Çubukları ve İsimleri Aç/Kapat.
- **Show HP% instead of bar**: Çubuk kullanmak yerine sağlık yüzdesini gösterir.
- **Show Player Faction Icon**: Sağlık çubuğunun yanında oyuncu tarafı ikonunu gösterir.
- **Name Plate Scale**: Ad plakalarının boyutu.
- **Ping System**: Ping Sistemi Aç/Kapat. Etkinleştirilirse ping tuşunu kullanarak ping alabilir ve gönderebilirsiniz.
- **Ping Button**: Ping göndermek için kullanılan düğme.
- **Ping Color**: Diğer oyuncular tarafından gösterildiğinde pinglerinizin rengi.
- **Ping Size**: Ping boyutunun çarpanı.
- **Play Ping Animation**: Ping gönderildiğinde otomatik olarak işaretlemeyi oynatır. Oyun oynama işlevselliğini engelleyebilir.

**COOP | Hata Ayıklama**

- **Free Camera Button**: Serbest kamerayı açıp kapatmak için kullanılan düğme.

**Performans**

- **Dynamic AI**: Oyuncuların aralığında olmadığında yapay zekayı devre dışı bırakmak için dinamik yapay zeka sistemini kullanın.
- **Dynamic AI Range**: Yapay zekanın dinamik olarak devre dışı bırakılacağı mesafe.
- **Dynamic AI Rate**: Dinamik Yapay Zeka'nın tüm oyunculardan mesafe aralığını taraması gereken sıklık.
- **Culling System**: Kesme sisteminin kullanılıp kullanılmayacağı. Oyuncular kesme aralığının dışındayken animasyonları basitleştirilir. Bu, belirli senaryolarda performansı önemli ölçüde artırabilir.
- **Culling Range**: Oyuncuların kesileceği mesafe.

**Performans | Maksimum Botlar**

- **Enforced Spawn Limits**: Botları doğururken spawn sınırlarını zorunlu olarak uygular, bot sınırlarını aşmamaya dikkat eder. Bu, spawn modları veya bot limitlerini değiştiren herhangi bir şey kullanılırken önemli ölçüde etkilidir.
- **Max Bots** `HARİTA`: Aynı anda aktif olabilecek maksimum bot miktarı `HARİTA`. Daha zayıf bir bilgisayarınız varsa kullanışlıdır. Devre dışı bırakmak için 0'a ayarlayın.

**Ağ**

- **Native Sockets**:: Oyun trafiği için Doğal Soketler. Bu, gönderme/alma için doğrudan soket çağrıları kullanarak hızı büyük ölçüde artırır ve GC basıncını azaltır. Yalnızca Windows/Linux için ve her zaman çalışmayabilir.
- **Force IP**: Barındırma yaparken sunucunun bu IP'yi otomatik olarak almaya çalışmak yerine backend'e yayınlamak için bu IP'yi kullanmasını zorlar. Devre dışı bırakmak için boş bırakın. VPN kullanırken gereklidir, kişisel VPN IP'nizi kullanın.
- **Force Bind IP**: Sunucunun barındırma yaparken bu yerel IP'yi sunucuyu başlatmak için kullanmasını zorlar. Devre dışı bırakmak için boş bırakın. VPN kullanırken gereklidir, kişisel VPN IP'nizi kullanın.
- **Auto Server Refresh Rate**: Her X saniyede bir istemci, lobideyken sunucuya maç listesini sormak için sunucuya sorar.
- **UDP Port**: UDP oyun paketleri için kullanılacak port.
- **Use UPnP**: UPnP'yi kullanarak bağlantı noktalarını açmaya çalışın. Kendiniz bağlantı noktalarını açamıyorsanız, ancak yönlendirici UPnP'yi destekliyorsa kullanışlıdır.

**Oyun Oynama**

- **Head Damage Multiplier**: Baş kafasına alınan hasarın çarpanı. 0.2 = %20
- **Armpit Damage Multiplier**: Koltuk altındaki hasarın çarpanı. 0.2 = %20

### Sunucu Yapılandırması

Sunucu yapılandırması, `user\mods\fika-server\assets\configs` klasöründe bulunabilir. Bir metin düzenleyici ile `fika.jsonc` dosyasını açın.

```json
{
    "client": {
        "useBtr": true, // Sokaklarda BTR'nin spawn edilip edilmeyeceği, varsayılan: true
        "friendlyFire": true, // Dost ateşinin etkin olup olmayacağı, varsayılan: true
        "dynamicVExfils": false, // Araç exfilinin oyuncu sayısına ölçeklenip ölçeklenmeyeceği, varsayılan: false
        "allowFreeCam": false, // Serbest kameranın serbestçe açılıp kapatılıp kapatılmayacağı, varsayılan: false
        "allowItemSending": true // Öğe göndermenin etkin olup olmayacağı, varsayılan: true
    },
    "server": {
        "giftedItemsLoseFIR": true // Gönderilen öğelerin FiR durumunu kaybedip kaybetmeyeceği, varsayılan: true
    }
}
```
