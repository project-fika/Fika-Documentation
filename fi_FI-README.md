# Fika - Moninpeli modi Aki:lle

<details open>
    <summary>Sisällysluettelo</summary>
    <ol>
        <li><a href="#mikä-on-fika">Mikä on Fika</a></li>
        <li><a href="#lisenssi">Lisenssi</a></li>
        <li>
            <a href="#edellytykset">Edellytykset</a>
            <ul>
                <li><a href="#hostaus">Hostaus</a></li>
                <li><a href="#asiakas">Asiakas</a></li>
            </ul>
        </li>
        <li><a href="#laitteistovaatimukset">Laitteistovaatimukset</a></li>
        <li>
            <a href="#asennus">Asennus</a>
            <ul>
                <li><a href="#hostaa-portinsiirtoa-käyttäen">Hostaa portinsiirtoa käyttäen</a></li>
                <li><a href="#hostaa-vpn-ää-käyttäen">Hostaa VPN:ää käyttäen</a></li>
                <li><a href="#asiakas-käyttäen-portinsiirtoa">Asiakas käyttäen portinsiirtoa</a></li>
                <li><a href="#asiakas-käyttäen-vpn-ää">Asiakas käyttäen VPN:ää</a></li>
            </ul>
        </li>
        <li>
            <a href="#ominaisuudet-ja-konfigurointi">Ominaisuudet ja konfigurointi</a>
            <ul>
                <li><a href="#ominaisuudet--miten-muokata">Ominaisuudet & Miten muokata</a></li>
                <li><a href="#asiakkaan-konfigurointi">Asiakkaan konfigurointi</a></li>
                <li><a href="#palvelimen-konfigurointi">Palvelimen konfigurointi</a></li>
            </ul>
        </li>
    </ol>
</details>

## Mikä on Fika

**Fika** on modi **SPT-Aki:lle** joka sallii CO-OP pelaamisen kavereidesi kanssa. Se käyttää vertaisverkkoista UDP yhteyttä tehokkaan ja modernin kokemuksen luomiseksi. Fikan päätavoitteet ovat: tehokkuus, tarkkuus ja modaus-tuki. Fikaa ylläpitää tällä hetkellä Fika team.
Voit liittyä Discordiimme [täältä](https://discord.gg/project-fika)!

## Lisenssi

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Tämä projekti on lisensöity [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.fi) lisenssillä.

- Voit jakaa Fikaa vain, jos sopivat tunnustukset ovat annettu; se ei ole kaupallisiin tarkoituksiin ja sinä et muokkaa sitä.
- Et saa rahallistaa palvelintasi maksujen tai lahjoitusten muodossa.
- Et saa hostata massiivisia julkisia palvelimia, Fika on tarkoittettu CO-OP käyttöön kavereidesi kanssa.
- Et saa kopioida ja/tai replikoida Fikan koodia, et myöskään saa käyttää sen resursseja jotka ovat käsintehtyjä kehittäjiemme ja artistiemme toimesta

## Edellytykset

Fika edellyttää yleistietoa tietokoneista, verkostotoiminnasta ja Aki:sta. Jos nämä käsitteet eivät ole tuttuja, tämä projekti ei ole sinulle. Yritä ymmärtää ja kunnioittaa tätä päätöstä.

### Hostaus

- Reititin ja internet-palveluntarjoaja joka tukee **Portinsiirtoa** tai **UPnP:tä**
- TCP Portti 6969 auki AKI Palvelimelle
- UDP Portti auki vertaisverkkoliikennettä varten, oletus 25565 (jos käytät UPnP:tä tämä ei ole tarpeellista)
- SPT asennettuna ja toimintakunnossa, samalla versiolla kuin Fika jota tulet käyttämään
- Pääsy Windowsin palomuuriin
- Vähintään 20 Mbit/s internetnopeus ylös ja alas on suositeltavaa. Jokainen asiakas käyttää keskimäärin 400 kbit/s.

Jos et voi portti siirtää, voit käyttää seuraavia tai vastaavanlaisia VPN:iä: `Hamachi`, `ZeroTier` tai `Radmin`.

### Asiakas

- Reititin ja internet-palveluntarjoaja joka tukee **Portinsiirtoa** tai **UPnP:tä** | **HUOMIO**: Tämä on vain tarpeellista jos toimit hostaajana pelissä
- UDP Portti auki vertaisverkkoliikennettä varten, oletus 25565 (jos käytät UPnP:tä tämä ei ole tarpeellista) | **HUOMIO**: Sama kuin ylhäällä
- SPT asennettuna ja toimintakunnossa, samalla versiolla kuin Fika jota tulet käyttämään
- Pääsy Windowsin palomuuriin
- Vähintään 20 Mbit/s internetnopeus ylös ja alas on suositeltavaa.

### Kummatkin

- Viimeisimmät Fikan tiedostot

## Laitteistovaatimukset

Suositukset sujakalle pelikokemukselle

- **Prosessori**: i7 8700k / Ryzen 7 2700x
- **Näytönohjain**: GTX 1060 / RX 580
- **Muisti** Vähintään 16 Gt. Suosittelemme vahvasti 32 Gt
- **Tallennustila**: SSD on pakollinen, älä oleta Fikan pyörivän kiintolevyllä

Parhaiten tehoa Fikassa (ja SPT:sä ylipäätään) nostaa tehokkaampi ja nopeampi prosessori sekä muisti

## Asennus

### Hostaa portinsiirtoa käyttäen

Ennen kuin alat seuraamaan ohjeita, varmista että kaikki tarvittavat portit ovat portti siirretty edellytysten mukaan. Emme avusta sinua porttien aukaisemisessa. Jos sinulla ei ole pääsyä reitittimeesi tai et voi portti siirtää, käytä VPN:ää.

**Palomuurin konfigurointi**

1. Siirrä portti 6969 **TCP** reitittimessäsi (sekä sisään- että ulospäin)
2. Siirrä portti **UDP** jota käytät reitittimessäsi, oletus 25565 (sekä sisään- että ulospäin)
3. Kun Windows pyytää, salli ***kaikki*** yhteydet palomuurissasi
4. Jos vielä koet ongelmia, suosittelemme sallivanne EscapeFromTarkov.exe:n (kaikki) ja AKI.Server.exe:n (palvelimen hostaaja) sisään- ja ulospäin menevän liikenteen Windowsin laajennetussa palomuurissa
   
**Yleisasennus**

1. [Lataa viimeisin Fikan koontiversio](https://discord.com/channels/1202292159366037545/1224454502531469373) (Sinun pitää ensin liittyä [Discord](https://discord.gg/project-fika) kanavallemme)
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Server.exe` kerran antaaksesi sen luoda konfiguraatiotiedostot Fikalle, sitten sammuta se
4. Mene takaisin pääkansioosi ja siirry kansioon `Aki_Data\Server\configs` ja aukaise `http.json`
5. Vaihda kohtaan `ip`: `0.0.0.0`. Tallenna tiedosto ja sulje se
6. Siirry kansioon `user\mods\mpt-server\assets\configs` ja aukaise `mpt.jsonc`
7. Muuta asetuksiasi haluamasi mukaan.
    - **useBtr**: jos haluat, että BTR spawnaa Streetsiä pelatessasi
    - **friendlyFire**: jos haluat, että oma tuli on päällä tai pois 
    - **dynamicVExfils**: automaattisesti muuta vehicle exfilien maksimi pelaajamäärää nykyisen raidin pelaajamäärän mukaan
    - **allowFreeCam**: salli pelaajien vapaakamerakäyttö raideissa
    - **giftedItemsLoseFIR**: jos lähetetyista tavaroista pitäisi poistaa FiR-status
8. Käynnistä `Aki.Server.exe` ja odota latauksen loppumista
    - Tältä onnistuneen käynnistyksen pitäisi näyttää:
    ```
    Started webserver at http://0.0.0.0:6969
    Started websocket at ws://0.0.0.0:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9.  Käynnistä `Aki.Launcher.exe`
10. Ystäväsi voivat yhdistää palvelimeesi käyttäen laajaverkko IP-osoitetta, jonka voi löytää sivustolta [IPv4.ICanHazIP](https://ipv4.icanhazip.com/)

### <a name="hostaa-vpn-ää-käyttäen"></a>Hostaa VPN:ää käyttäen

Tarvitset VPN:än, kuten: `Hamachi`, `ZeroTier` tai `Radmin`.

1. [Lataa viimeisin Fikan koontiversio](https://discord.com/channels/1202292159366037545/1224454502531469373) (Sinun pitää ensin liittyä [Discord](https://discord.gg/project-fika) kanavallemme)
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Server.exe` kerran antaaksesi sen luoda konfiguraatiotiedostot Fikalle, sitten sammuta se
4. Mene takaisin pääkansioosi ja siirry kansioon `Aki_Data\Server\configs` ja aukaise `http.json`
5. Vaihda kohtaan `ip` sinun VPN IP:si. Tallenna tiedosto ja sulje se

Esimerkki tekaistulla IP-osoitteella (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. Siirry kansioon `user\mods\mpt-server\assets\configs` ja aukaise `mpt.jsonc`
7. Muuta asetuksiasi haluamasi mukaan.
    - **useBtr**: jos haluat, että BTR spawnaa Streetsiä pelatessasi
    - **friendlyFire**: jos haluat, että oma tuli on päällä tai pois 
    - **dynamicVExfils**: automaattisesti muuta vehicle exfilien maksimi pelaajamäärää nykyisen raidin pelaajamäärän mukaan
    - **allowFreeCam**: salli pelaajien vapaakamerakäyttö raideissa
    - **giftedItemsLoseFIR**: jos lähetetyista tavaroista pitäisi poistaa FiR-status
8. Käynnistä `Aki.Server.exe` ja odota latauksen loppumista
   - Tältä onnistuneen käynnistyksen pitäisi näyttää kohta viiden IP-osoitteella:
    ```
    Started webserver at http://20.20.56.73:6969
    Started websocket at ws://20.20.56.73:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9.  Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
10. vaihda `URL`-kenttään sinun VPN IP-osoitteesesi. Käyttäen viidennen kohdan esimerkkiä, se olisi: `http://20.20.56.73:6969` (muista poistaa kaikki loppupään kauttaviivat `/`)

### Asiakas käyttäen portinsiirtoa

1. [Lataa viimeisin Fikan koontiversio](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
4. Vaihda `URL`-kenttään hostaajan laajaverkko IP-osoite. (muista poistaa kaikki loppupään kauttaviivat `/`)
5. Jos hostaat pelissä, salli kaikki yhteydet (julkiset ja yksityiset) kun/jos Windows palomuuri sitä kysyy

### <a name="asiakas-käyttäen-vpn-ää"></a>Asiakas käyttäen VPN:ää

1. [Lataa viimeisin Fikan koontiversio](https://discord.com/channels/1202292159366037545/1224454502531469373)
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
4. Vaihda `URL`-kenttään hostaajan VPN IP-osoite. Käyttäen viidennen kohdan esimerkkiä, se olisi: `http://20.20.56.73:6969` (muista poistaa kaikki loppupään kauttaviivat `/`)
5. Jos hostaat pelissä, salli kaikki yhteydet (julkiset ja yksityiset) kun/jos Windows palomuuri sitä kysyy

## Ominaisuudet ja konfigurointi

### Ominaisuudet & Miten muokata
**Fika** antaa sinun hostata laajaverkkoisia sessioita kavereidesi kanssa CO-OP pelaamista varten. Hostaaja hallitsee suurinta osaa logiikkaa pelatessa, kuten esimerkiksi AI:n, miinakenttien, tarkka-ampuja alueiden ja BTR:n ohjausta. Jokainen asiakas on vastuussa vahingoista, itselleen sekä AI:lle. Tämä mahdollistaa sen, että AI:n ampuminen tuntuu responsiiviselta ja nopealta.

Pelin hostaamiseksi valitse kartta ja aika. Viimeisessä näytössä paina `Host Raid`. Valitse pelaajamäärä (itsesi mukaanlukien) ja odota latauksen loppumista. Latauksen jälkeen muut pelaajat voivat liittyä sessioosi. Kun kaikkien pelaajien peli on ladannut, alkaa se automaattisesti.

**Fikan muita ominaisuuksia**
- Tavaroiden lähettäminen pelaajien välillä
    - Paina hiiren kakkospainiketta tavaran päällä stashisasi lähettääksesi sen toiselle käyttäjälle
    - Voit muokata tätä [palvelin](#palvelimen-konfigurointi) konfiguraatiossa
- Vapaakamera (oletusnäppäin: `F9`)
    - Vapaakamerassa voit teleporttaa kameran luo painamalla `T`
    - Voit hypätä toisen pelaajan lyö `Vasemmalla/Oikealla` hiirennäppäimellä
    - Voit liimautua heidän päähän painamalla `Välilyöntiä` hypätessä
    - Voit liimautua heidän selkäänsä kolmannen persoonan näkymässä pitämällä `CTRL`-näppäintä pohjassa hypätessä
    - Voit painaa `HOME`-näppäintä vaihtaaksesi väliaikaisesti vapaakameran kontrollit
- Vahinkokertoimet elintärkeisiin kohtiisi
- Dynaaminen AI hostaajalle, joka kytkee AI:n pois päältä kun niiden lähettyvillä ei ole ketään
- Muokattavat rajamäärät AI:lle kartoissa
- Noukkimissysteemi suorituskyvyn nostamiseksi
- Muokattavat ilmoitukset (tiimiläinen kuoli, bossi tapettu pelaajan toimesta, jne.)
- Merkkaussysteemi jolla voit merkata paikan pelissä tiimiläisillesi
- Pelaajan healthipalkit tiimiläisillesi

Suurin osa näistä ovat muokattavissa [asiakkaan konfiguroinnissa](#asiakkaan-konfigurointi).

### Asiakkaan konfigurointi

Avataksesi asiakkaan konfiguroinnin, paina `F12`-näppäintä pelissä. Aukaise `Fika Core` kohta muuttaaksesi asetuksia.

**Co-op**

- **Show Notifications**: Salli mukautetut ilmoitukset kun pelaaja kuolee, extractaa, tappaa bossin, jne.
- **Auto Extract**: Automaattisesti extractaa pelatessa vapaakameran käynnistämisen sijaan.
- **Show Extract Message**: Näytä extract-viesti kuollessa/extractaessa

**Coop | Mukautettavat**

- **Show Player Name Plates**: Näytä pelaajien healthipalkit ja nimet.
- **Show HP% instead of bar**: Näyttää healthin prosenteissa palkin sijaan.
- **Show Player Faction Icon**: Näyttää pelaajan factionin merkin healthipalkin vieressä.
- **Name Plate Scale**: Nimikylttien koko.
- **Ping System**: Merkkaussysteemi päälle/pois. Jos päällä, voit nähdä ja lähettää merkkauksia painamalla merkkaus-näppäintä.
- **Ping Button**: Nappi merkkausten lähettämiseen.
- **Ping Color**: Merkkausten väri jonka muut pelaajat näkevät.
- **Ping Size**: Merkkauksen koko.
- **Play Ping Animation**: Näyttää osoittamis-animaation merkatessa. Voi häiritä pelikokemusta.

**Coop | Debug**

- **Free Camera Button**: Vapaakameran näppäin.

**Suorituskyky**

- **Dynamic AI**: Käytä dynaamista AI-systeemiä, kytkien AI:n pois päältä niiden liikuttuaan ulos pelaajien etäisyydestä.
- **Dynamic AI Range**: Etäisyys, minkä ulkopuolella AI kytkeytyy pois dynaamisesti.
- **Dynamic AI Rate**: Kuinka usein dynaamisen AI:n pitäisi skannata etäisyys kaikista pelaajista.
- **Culling System**: Mikäli haluat käyttää noukkimissysteemiä. Kun pelaajat ovat noukkimisetäisyyden ulkopuolella, heidän animaatiot yksinkertaistuvat. Tämä voi parantaa suorituskykyä huomattavasti tietyissä olosuhteissa.
- **Culling Range**: Etäisyys, jonka ulkopuolella pelaajia pitäisi noukkia.

**Suorituskyky | Maksimi botit**

- **Enforced Spawn Limits**: Valvoo spawnimäärää botteja spawnatessa, pitäen huolta ettei se mene yli alkuperäisten määrien. Tämä pääsääntöisesti koskettaa spawnaus modeja tai mitä tahansa joka muokkaa bottien määrää.
- **Max Bots** `MAP`: Maksimi määrä botteja aktiivisena kulloinkin `MAP`:sa. Kätevä jos sinulla on heikompi tietokone. Aseta nolla kytkeäksesi pois päältä
  
**Tietoverkko**

- **Native Sockets**: NativeSockets peliliikenteelle. Tämä käyttää suoria pistoke-kutsuja lähetykseen/vastaanottoon nopeuden huomattavaan lisäämiseen ja roskienkeruupaineen vähentämiseen. Vain Windowsille/Linuxille, ei saata aina toimia.
- **Force IP**: Pakottaa palvelimen käyttämään tätä IP-osoitetta hostatessa viestien lähettämiseen palvelimelle, sen sijaan kuin yrittäen automaattisesti noutaa sitä. Jätä tyhjäksi kytkeäksesi pois päältä. Tämä on tarpeellista VPN:ää käyttäessä; Käytä sinun henkilökohtaista VPN IP-osoitetta.
- **Force Bind IP**: Pakottaa palvelimen käyttämään tätä paikallista IP-osoitetta palvelinta käynnistäessä. Jätä tyhjäksi kytkeäksesi pois päältä. Tämä on tarpeellista VPN:ää käyttäessä; Käytä sinun henkilökohtaista VPN IP-osoitetta.
- **Auto Server Refresh Rate**: Joka X sekunttia, asiakas kysyy palvelimelta listaa yhtäläisyyksistä lobbyssä ollessa.
- **UDP Port**: UDP portti pelin verkkopaketeille.
- **Use UPnP**: Yritä avata portteja käyttäen UPnP:tä. Kätevä jos et voi avata portteja itse, mutta reititin tukee UPnP:tä.

**Pelattavuus**

- **Head Damage Multiplier**: Kerroin vahingolle jonka pää ottaa vastaan. 0.2 = 20%
- **Armpit Damage Multiplier**: Kerroin vahingolle jonka kainalot ottaa vastaan. 0.2 = 20%

### Palvelimen konfigurointi

Palvelimen konfigurointiasetukset löytyvät kansion `user\mods\mpt-server\assets\configs` tiedostosta `mpt.jsonc`.

```json
{
    "client": {
        "useBtr": true, // voiko BTR spawnata Streetsissä, oletus: true
        "friendlyFire": true, // onko oma tuli päällä, oletus: true
        "dynamicVExfils": false, // onko vehicle exfilien maksimi pelaajamäärää nykyisen raidin pelaajamäärä, oletusmäärän neljä sijaan, oletus: false
        "allowFreeCam": false, // voiko vapaakameraa käyttää vapaasti, oletus: false
        "allowItemSending": true // voiko tavaroita lähettää vapaasti, oletus: true
    },
    "server": {
        "giftedItemsLoseFIR": true // pitäisikö lähetettyjen tavaroiden pitää niiden FiR-status, oletus: true
    }
}
```
