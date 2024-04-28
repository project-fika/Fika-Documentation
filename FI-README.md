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
        <li><a href="#järjestelmävaatimukset">Järjestelmävaatimukset</a></li>
        <li>
            <a href="#asennus">Asennus</a>
            <ul>
                <li><a href="#hostaa-portinsiirtoa-käyttäen">Hostaa portinsiirtoa käyttäen</a></li>
                <li><a href="#hostaa-vpnää-käyttäen">Hostaa VPNää käyttäen</a></li>
                <li><a href="#asiakas-käyttäen-portinsiirtoa">Asiakas käyttäen portinsiirtoa</a></li>
                <li><a href="#asiakas-käyttäen-vpnää">Asiakas käyttäen VPNää</a></li>
            </ul>
        </li>
        <li><a href="#ominaisuudet-ja-konfirugaatio">Ominaisuudet ja konfirugaatio</a></li>
    </ol>
</details>

## Mikä on Fika

**Fika** on modi **SPT-Aki:lle** joka sallii CO-OP pelaamisen kavereidesi kanssa. Se käyttää vertaisverkkoista UDP yhteyttä tehokkaan ja modernin kokemuksen luomiseksi. Fikan päätavoitteet ovat: tehokkuus, tarkkuus ja modaus-tuki. Fikaa ylläpitää tällä hetkellä Fika team.
Voit liittyä Discordiimme [täältä](https://discord.gg/project-fika)!

## Lisenssi

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Tämä projekti on lisensöity [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.fi) lisenssillä.

- Voit jakaa Fikaa vain, jos sopivat tunnustukset ovat annettu; se ei ole kaupallisiin tarkoituksiin ja et muokkaa sitä.
- Et saa rahallistaa palvelintasi maksujen tai lahjoitusten muodossa.
- Et saa hostata massiivisia julkisia palvelimia, Fika on tarkoittettu CO-OP käyttöön kavereidesi kanssa.
- Et saa kopioida ja/tai muokata Fikan koodia, et myöskään saa käyttää sen resursseja, jotka ovat käsintehtyjä kehittäjiemme ja artistiemme toimesta

## Edellytykset

Fika edellyttää yleistietoa tietokoneista, verkostotoiminnasta ja Aki:sta. Jos nämä käsitteet eivät ole tuttuja, tämä projekti ei ole sinulle. Yritä ymmärtää ja kunnioittaa tätä.

### Hostaus

- Reititin ja internet-palveluntarjoaja joka tukee **Portinsiirtoa** tai **UPnP:tä**
- TCP Portti 6969 auki AKI Palvelimelle
- UDP Portti auki vertaisverkkoliikennettä varten, oletus 25565 (jos käytät UPnP:tä tämä ei ole tarpeellista)
- SPT asennettuna ja toimintakunnossa, samalla versiolla kuin Fika jota tulet käyttämään
- Pääsy Windows palomuuriin
- Vähintään 20 Mbit/s internetnopeus ylös ja alas on suositeltavaa. Jokainen asiakas käyttää keskimäärin 400 kbit/s.

### Asiakas

- Reititin ja internet-palveluntarjoaja joka tukee **Portinsiirtoa** tai **UPnP:tä** | **HUOMIO**: Tämä on vain tarpeellista jos toimit hostaajana pelissä
- UDP Portti auki vertaisverkkoliikennettä varten, oletus 25565 (jos käytät UPnP:tä tämä ei ole tarpeellista) | **HUOMIO**: Sama kuin ylhäällä
- SPT asennettuna ja toimintakunnossa, samalla versiolla kuin Fika jota tulet käyttämään
- Pääsy Windows palomuuriin
- Vähintään 20 Mbit/s internetnopeus ylös ja alas on suositeltavaa.

### Kummatkin

- Viimeisimmät Fika tiedostot

## Järjestelmävaatimukset

Suositukset sujakalle pelikokemukselle

- **Prosessori**: i7 8700k / Ryzen 7 2700x
- **Näytönohjain**: GTX 1060 / RX 580
- **Muisti** 16 Gt vähintään, 32 Gt vahvasti suositeltu
- **Tallennustila**: SSD on pakollinen, älä oleta Fikan pyörivän kiintolevyllä

Parhaiten tehoa Fikassa (ja SPT:sä ylipäätään) nostaa tehokkaampi prosessori ja RAM-muisti

## Asennus

### Hostaa portinsiirtoa käyttäen

Ennen kuin aloitat ohjeiden seuraamista, varmista että kaikki tarvittavat portit ovat porttisiirretty edellytysten mukaan. Emme avusta sinua porttien aukaisemisessa. Jos sinulla ei ole pääsyä reitittimeesi tai et voi porttisiirtää, käytä VPNää.

**Palomuurin konfiguraatio**

1. Siirrä portti 6969 **TCP** reitittimessäsi (sekä sisään että ulos päin)
2. Siirrä portti **UDP** jota käytät reitittimessäsi, oletus 25565 (sekä sisään että ulos päin)
3. Kun Windows pyytää, salli ***kaikki*** yhteydet palomuurissasi

**Yleisasennus**

1. Lataa viimeisin Fikan koontiversio
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Server.exe` kerran antaaksesi sen luoda konfiguraatiotiedostot Fikalle, sitten sammuta se
4. Mene takaisin pääkansioosi ja siirry kansioon `Aki_Data\Server\configs` ja aukaise `http.json`
5. Vaihda kohtaan `ip`: `0.0.0.0`. Tallenna tiedosto ja sulje se
6. Siirry kansioon `user\mods\fika-server\assets\configs` ja aukaise `fika.jsonc`
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
9. Käynnistä `Aki.Launcher.exe`
10. Ystäväsi voivat yhdistää palvelimeesi käyttäen laajaverkko IP-osoitetta, jonka voi löytää käyttämällä [IPv4.ICanHazIP](https://ipv4.icanhazip.com/) sivustoa

### Hostaa VPNää käyttäen

1. Lataa viimeisin Fikan koontiversio
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
6. Siirry kansioon `user\mods\fika-server\assets\configs` ja aukaise `fika.jsonc`
7. Muuta asetuksiasi haluamasi mukaan.
    - **useBtr**: jos haluat, että BTR spawnaa Streetsiä pelatessasi
    - **friendlyFire**: jos haluat, että oma tuli on päällä tai pois 
    - **dynamicVExfils**: automaattisesti muuta vehicle exfilien maksimi pelaajamäärää nykyisen raidin pelaajamäärän mukaan
    - **allowFreeCam**: salli pelaajien vapaakamerakäyttö raideissa
    - **giftedItemsLoseFIR**: jos lähetetyista tavaroista pitäisi poistaa FiR-status
8. Käynnistä `Aki.Server.exe` ja odota latauksen loppumista
   - Tältä onnistuneen käynnistyksen pitäisi kohdan viisi IP-osoitetta käyttämällä:
    ```
    Started webserver at http://20.20.56.73:6969
    Started websocket at ws://20.20.56.73:6969
    Server is running, do not close while playing SPT, Happy playing!!
    ```
9.  Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
10. vaihda `URL`-kenttään sinun VPN IP-osoitteesesi. Käyttäen viidennen kohdan esimerkkiä, se olisi: `http://20.20.56.73:6969` (muista poistaa kaikki loppupään kauttaviivat `/`)

### Asiakas käyttäen portinsiirtoa

1. Lataa viimeisin Fikan koontiversio
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
4. Vaihda `URL`-kenttään hostaajan laajaverkko IP-osoite (muista poistaa kaikki loppupään kauttaviivat `/`)
5. Jos hostaat pelissä, salli kaikki yhteydet (julkiset ja yksityiset) Windows palomuurin kysyessä

### Asiakas käyttäen VPNää

1. Lataa viimeisin Fikan koontiversio
2. Aukaise SPT-asennuksesi kansio ja pura arkiston sisältö kansioon
3. Käynnistä `Aki.Launcher.exe` ja paina 'Settings'
4. Vaihda `URL`-kenttään hostaajan VPN IP-osoite. Käyttäen viidennen kohdan esimerkkiä, se olisi: `http://20.20.56.73:6969` (muista poistaa kaikki loppupään kauttaviivat `/`)
5. Jos hostaat pelissä, salli kaikki yhteydet (julkiset ja yksityiset) Windows palomuurin kysyessä

## Ominaisuudet ja konfirugaatio

### Ominaisuudet & How-To
**Fika** antaa sinun hostata laajaverkkoisia sessioita kavereidesi kanssa CO-OP pelaamista varten. Hostaaja hallitsee suurinta osaa logiikkaa pelatessa, kuten esimerkiksi AI:n, miinakenttien, tarkka-ampuja alueiden ja BTR:n ohjausta. Jokainen asiakas on vastuussa heidän omista vahingoista, itselleen että AI:lle. Tämä mahdollistaa sen, että AI:n ampuminen tuntuu responsiiviselta ja nopealta.

Pelin hostaamiseksi, valitse kartta ja aika. Viimeisessä näytössä paina `Host Raid`. Valitse pelaajamäärä (itsesi mukaanlukien) ja odota latauksen loppumista. Lataamisen jälkeen, muut pelaajat voivat liittyä sessioosi. Kun kaikilla on ladannut, peli alkaa automaattisesti.

**Fikan muita ominaisuuksia**
- Tavaroiden lähettäminen
    - Paina hiiren kakkospainiketta tavaran päällä stashisasi lähettääksesi sen toiselle käyttäjälle
    - Voit muokata tätä [palvelin](#palvelin-konfiguraatio) konfiguraatiossa
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
- Pingaussysteemi pingataksesi alueen pelissä tiimiläisillesi
- Pelaajan healthipalkit tiimiläisillesi

Suurin osa näistä ovat muokattavissta [asiakas konfiguraatiossa](#asiakas-konfiguraatio).

### Asiakas konfiguraatio

Avataksesi asiakas konfiguraatio, paina `F12`-näppäintä pelissä. Aukaise `Fika Core` kohta muuttaaksesi asetuksia.

**Co-op**

- **Show Notifications**: Salli mukautetut ilmoitukset kun pelaaja kuolee, extractaa, tappaa bossin, jne.
- **Auto Extract**: Automaattisesti extractaa pelatessa asiakkaana vapaakameran käynnistämisen sijaan.
- **Show Extract Message**: Näytä extract-viesti kuollessa/extractaessa
    
**Coop | Mukautettavat**

- **Show Player Name Plates**: Näytä pelaajien healthipalkit ja nimet.
- **Show HP% instead of bar**: Näyttää healthin prosenteissa palkin sijaan.
- **Show Player Faction Icon**: Näyttää pelaajan factionin merkin healthipalkin vieressä.
- **Name Plate Scale**: Nimikylttien koko.
- **Ping System**: Pingaussysteemi päälle/pois. Jos päällä, voit nähdä ja lähettää pingejä painamalla ping-näppäintä.
- **Ping Button**: Nappi pingien lähettämiseen.
- **Ping Color**: Pingin väri jonka muut pelaajat näkevät.
- **Ping Size**: Ping-merkin koko.
- **Play Ping Animation**: Näyttää osoittamis-animaation automaattisesti pingatessa. Voi häiritä pelikokemusta.

**Coop | Debug**

- **Free Camera Button**: Vapaakameran näppäin.

**Suorituskyky**

- **Dynamic AI**: Käytä dynaamista AI-systeemiä, kytkien ne pois päältä astuessaan ulos pelaajien etäisyydestä.
- **Dynamic AI Range**: Etäisyys, minkä ulkopuolella AI kytkeytyy pois dynaamisesti.
- **Dynamic AI Rate**: Kuinka usein dynaamisen AI:n pitäisi skannata etäisyys kaikista pelaajista.
- **Culling System**: Mikäli haluat käyttää noukkimissysteemiä. Kun pelaajat ovat noukkimisetäisyyden ulkopuolella, heidän animaatiot yksinkertaistuvat. Tämä voi parantaa suorituskykyä huomattavasti tietyissä olosuhteissa.
- **Culling Range**: Etäisyys, jonka ulkopuolella pelaajia pitäisi noukkia.

**Suorituskyky | Maksimi botit**

- **Enforced Spawn Limits**: Valvoo spawnimäärää botteja spawnatessa, pitäen huolta ettei se mene yli alkuperäisten määrien. Tämä pääsääntöisesti koskettaa spawnaus modeja tai mitä tahansa joka muokkaa bottien määrää.
- **Max Bots** `MAP`: Maksimi määrä botteja aktiivisena kulloinkin `MAP`:sa. Kätevä jos sinulla on heikompi tietokone. Aseta nolla kytkeäksesi pois päältä
  
**Tietoverkko**

- **Native Sockets**: "NativeSockets" peliliikenteelle. Tämä käyttää suoria pistoke-kutsuja lähetykseen/vastaanottoon nopeuden huomattavaan lisäämiseen ja roskienkeruupaineen vähentämiseen. Vain Windowsille/Linuxille, ei saata aina toimia.
- **Force IP**: Pakottaa palvelimen käyttämään tätä IP-osoitetta hostatessa viestien lähettämiseen palvelimelle, sen sijaan kuin yrittäen automaattisesti noutaa sitä. Jätä tyhjäksi kytkeäksesi pois päältä. Tämä on tarpeellista VPNää käyttäessä; Käytä sinun henkilökohtaista VPN IP-osoitetta.
- **Force Bind IP**: Pakottaa palvelimen käyttämään tätä paikallista IP-osoitetta palvelinta käynnistäessä. Kätevä jos hostaat VPNää käyttäen. Jätä tyhjäksi kytkeäksesi pois päältä. Tämä on tarpeellista VPNää käyttäessä; Käytä sinun henkilökohtaista VPN IP-osoitetta.
- **Auto Server Refresh Rate**: Joka X sekunttia, asiakas kysyy palvelimelta listaa yhtäläisyyksistä lobbyssä ollessa.
- **UDP Port**: UDP portti pelin verkkopaketeille.
- **Use UPnP**: Yritä avata portteja käyttäen UPnP:tä. Kätevä jos et voi avata portteja itse, mutta reititin tukee UPnP:tä.

**Gameplay**

- **Head Damage Multiplier**: X kerroin vahingolle jonka pää ottaa vastaan. 0.2 = 20%
- **Armpit Damage Multiplier**: X kerroin vahingolle jonka kainalot ottaa vastaan. 0.2 = 20%

### Palvelin konfiguraatio

Palvelimen konfiguraatio löytyy kansiosta `user\mods\fika-server\assets\configs`. Aukause tiedosto `fika.jsonc` tekstinkäsittelyohjelmassa.

```json
{
    "client": {
        "useBtr": true, // jos BTR:n pitäisi spawnata Streetsissä, oletus: true
        "friendlyFire": true, // onko oma tuli päällä, oletus: true
        "dynamicVExfils": false, // jos vehicle exfilien maksimi pelaajamäärää on nykyisen raidin pelaajamäärä oletusmäärän neljä sijaan, oletus: false
        "allowFreeCam": false, // voiko vapaakameraa käyttää vapaasti, oletus: false
        "allowItemSending": true // voiko tavaroita lähettää vapaasti, oletus: true
    },
    "server": {
        "giftedItemsLoseFIR": true // pitäisikö lähetettyjen tavaroiden pitää niiden FiR-status, oletus: true
    }
}
```
