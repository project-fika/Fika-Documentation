# Fika — Modyfikacja umożliwiająca grę wieloosobową dla SPT

<details open>
    <summary>Spis treści</summary>
    <ol>
        <li><a href="#czym-jest-project-fika">Czym jest Fika?</a></li>
        <li><a href="#licencja">Licencja</a></li>
        <li>
            <a href="#warunki-wstępne">Warunki wstępne</a>
            <ul>
                <li><a href="#hostowanie">Hostowanie</a></li>
                <li><a href="#klient">Klient</a></li>
            </ul>
        </li>
        <li><a href="#wymagania-sprzętowe">Wymagania sprzętowe</a></li>
        <li>
            <a href="#instalacja">Instalacja</a>
            <ul>
                <li><a href="#host--przy-użyciu-przekierowania-portów">Host — przy użyciu przekierowania portów</a></li>
                <li><a href="#host--przy-użyciu-vpn">Host — przy użyciu VPN</a></li>
                <li><a href="#klient--przy-użyciu-przekierowania-portów">Klient — Przy użyciu przekierowania portów</a></li>
                <li><a href="#klient--przy-użyciu-vpn">Klient — Przy użyciu VPN</a></li>
            </ul>
        </li>
        <li>
            <a href="#funkcje-i-konfiguracja">Funkcje i konfiguracja</a>
            <ul>
                <li><a href="#funkcje-i-instrukcja-użytkowania">Funkcje i instrukcja użytkowania</a></li>
                <li><a href="#konfiguracja-klienta">Konfiguracja klienta</a></li>
                <li><a href="#konfiguracja-serwera">Konfiguracja serwera</a></li>
            </ul>
        </li>
    </ol>
</details>

## Czym jest Fika?

**Fika** jest modyfikacją do **SPT-Aki** która pozwala na grę kooperacyjną (COOP) ze swoimi znajomymi. Modyfikacja wykorzystuje połączenie P2P-UDP, które pozwala na wydajną i nowoczesną rozgrywkę. Główne cele Fika to: wydajność, precyzyjność oraz wsparcie modyfikacji. Fika obecnie jest utrzymywane przez zespół Fika.
Możesz dołączyć do naszego Discorda [tutaj](https://discord.gg/project-fika)!

## Licencja

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Ten projekt jest objęty licencją [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en).

- Możesz udostępniać Fika pod warunkiem podania odpowiednich uznań autorstwa, nieużywania jej do celów komercyjnych oraz niewprowadzania modyfikacji.
- Nie możesz w żaden sposób monetyzować swojego serwera w zakresie płatności czy dotacji.
- Nie możesz prowadzić masowych publicznych serwerów, Fika jest przeznaczona do wspólnej gry z przyjaciółmi.
- Nie możesz kopiować ani replikować kodu Fiki, ani używać jej zasobów, które są ręcznie tworzone przez naszych programistów i artystów.

## Warunki wstępne

Fika wymaga ogólnej wiedzy o komputerach, sieciach oraz Aki. Jeżeli nie czujesz się komfortowo w tych aspektach, ten projekt nie jest dla Ciebie. Prosimy o uszanowanie i zrozumienie tego.

### Hostowanie

- Router oraz dostawca internetu (ISP), który wspiera **przekierowanie portów** lub **UPnP**,
- Otwarty port TCP **6969** dla serwera AKI,
- Otwarty port UDP dla ruchu P2P, domyślnie **25565** (jeżeli zostanie użyte połączenie UPnP — warunek ten nie jest wymagany),
- Zainstalowane oraz działające **SPT**, odpowiednie dla wybranej wersji **Fika**, która będzie używana,
- Dostęp do Zapory sieciowej Windows hosta,
- Internet o prędkości co najmniej 20 Mbit/s (Prędkość zalecana w obu kierunkach). Każdy klient wykorzystuje średnio 400 kbit/s.

Jeśli nie możesz ustawić przekierowania portów, możesz użyć VPN takiego jak `Hamachi`, `ZeroTier` lub `Radmin`.

### Klient

- Router oraz dostawca internetu (ISP), który wspiera **Przekierowanie Portów** lub **UPnP**,
- Otwarty port UDP dla ruchu P2P, domyślnie **25565** (jeżeli zostanie użyte połączenie UPnP — warunek ten nie jest wymagany),

> ⚠️ **UWAGA**: Powyższe warunki są wymagane, jeśli planujesz hostować sesje w grze.

- Zainstalowane oraz działające **SPT**, odpowiednie dla wybranej wersji **Fika**, która będzie używana,
- Dostęp do Zapory sieciowej Windows klienta,
- Internet o prędkości co najmniej 20 Mbit/s (Prędkość zalecana w obu kierunkach).

### Wspólne

- Najnowsze pliki modyfikacji Fika

## Wymagania sprzętowe

Poniżej podane są rekomendowane wymagania sprzętowe dla płynnej rozgrywki:

- **Procesor**: i7 8700k / Ryzen 7 2700x
- **Karta graficzna**: GTX 1060 / RX 580
- **Pamięć RAM**: minimalnie 16 GB, jednak zalecaną ilością jest 32 GB
- **Dysk**: co najmniej dysk SSD — wsparcie nie zostanie udzielone w przypadku próby uruchamiania Fika na dysku HDD

Największy wzrost wydajności w Fika (oraz w SPT ogółem) dają mocniejszy procesor oraz pamięć RAM.

## Instalacja

### Host — przy użyciu przekierowania portów

Zanim rozpoczniesz wykonywanie poniższych kroków, upewnij się, że wszystkie porty podane w *
*[warunkach wstępnych](#warunki-wstępne)** zostały przekierowane. Nie otrzymasz od nas wsparcia przy przekierowaniu portów. Jeżeli nie masz dostępu do routera lub nie masz możliwości przekierowania portów, użyj VPN.

**Konfiguracja Zapory sieciowej**

1. Przekierowanie portu 6969 **TCP** w swoim routerze (w obu kierunkach wejście/wyjście),
2. Przekierowanie portu **UDP**, który będzie używany, w swoim routerze, domyślnie 25565 (w obu kierunkach wejście/wyjście),
3. Gdy Windows wyświetli komunikat, zezwól na ***wszystkie*** połączenia w swojej Zaporze sieciowej.

**Konfiguracja Ogólna**

1. Pobierz oraz zainstaluj najnowszą wersję Fika,
2. Przejdź do katalogu, w którym znajduje się zainstalowany SPT i wypakuj zawartość pliku skompresowanego do tego katalogu,
3. Uruchom jednorazowo `Aki.Server.exe` aby pozwolić mu wygenerować pliki konfiguracyjne dla Fika, a następnie go wyłącz,
4. Wróć do głównego folderu, następnie przejdź do `Aki_Data\Server\configs` i otwórz plik `http.json`,
5. Zmień wartość `ip` na `0.0.0.0`, a następnie zapisz i zamknij plik,
6. Przejdź do `user\mods\fika-server\assets\configs` i otwórz plik `fika.json`,
7. Zmień dowolne ustawienia według własnych preferencji:
    - **useBtr**: czy BTR powinien pojawiać się podczas gry na mapie Streets of Tarkov,
    - **friendlyFire**: czy sojusznicy powinni otrzymywać obrażenia spowodowane przez ich kolegów,
    - **dynamicVExfils**: automatycznie skaluj maksymalną liczbę graczy dla wyjazdów pojazdami w zależności od liczby graczy w rajdzie,
    - **allowFreeCam**: czy gracze mogą używać wolnej kamery (free cam),
    - **giftedItemsLoseFIR**: czy przesyłane przedmioty powinny tracić status FiR

8. Uruchom `Aki.Server.exe` i poczekaj, aż zakończy się ładowanie,
    > ✅ Poprawne uruchomienie powinno wyglądać mniej więcej tak:
    >```
    >Started webserver at http://0.0.0.0:6969
    >Started websocket at ws://0.0.0.0:6969
    >Server is running, do not close while playing SPT, Happy playing!!
    >```
9. Uruchom `Aki.Launcher.exe`,
10. Twoi znajomi mogą połączyć się z Twoim serwerem, korzystając z Twojego adresu IP WAN, który można znaleźć na przykład za pomocą strony [IPv4.ICanHazIP](https://ipv4.icanhazip.com/).

### Host — przy użyciu VPN

1. Pobierz oraz zainstaluj najnowszą wersję Fika,
2. Przejdź do katalogu, w którym znajduje się zainstalowany SPT i wypakuj zawartość pliku skompresowanego do tego katalogu,
3. Uruchom jednorazowo `Aki.Server.exe` aby pozwolić mu wygenerować pliki konfiguracyjne dla Fika, a następnie go wyłącz,
4. Wróć do głównego folderu, następnie przejdź do `Aki_Data\Server\configs` i otwórz plik `http.json`,
5. Zmień wartość `ip` na adres IP Twojego serwera VPN, a następnie zapisz i zamknij plik,
    > 💡 **Przykład:** sztuczny adres IP serwera VPN (VPN; **20.20.56.73**):
    >```json
    >{
    >    "ip": "20.20.56.73",
    >    "port": 6969,
    >    "webSocketPingDelayMs": 90000,
    >    "logRequests": true,
    >    "serverImagePathOverride": {}
    >} 
    >```
6. Przejdź do `user\mods\fika-server\assets\configs` i otwórz plik `fika.json`,
7. Zmień dowolne ustawienia według własnych preferencji:
    - **useBtr**: czy BTR powinien pojawiać się podczas gry na mapie Streets of Tarkov,
    - **friendlyFire**: czy sojusznicy powinni otrzymywać obrażenia spowodowane przez ich kolegów,
    - **dynamicVExfils**: automatycznie skaluj maksymalną liczbę graczy dla wyjazdów pojazdami w zależności od liczby graczy w rajdzie,
    - **allowFreeCam**: czy gracze mogą używać wolnej kamery (free cam),
    - **giftedItemsLoseFIR**: czy przesyłane przedmioty powinny tracić status FiR
8. Uruchom `Aki.Server.exe` i poczekaj chwilę, aż skończy się ładować,
    > ✅ Poprawne uruchomienie powinno wyglądać mniej więcej tak:
    >```
    >Started webserver at http://0.0.0.0:6969
    >Started websocket at ws://0.0.0.0:6969
    >Server is running, do not close while playing SPT, Happy playing!!
    >```
9. Uruchom `Aki.Launcher.exe` i naciśnij 'Settings',
10. Zmień wartość w polu `URL` tak, aby odzwierciedlała Twój adres IP serwera VPN. Używając przykładu z kroku 5, wartością byłoby: `http://20.20.56.73:6969` (pamiętaj, aby usunąć jakiekolwiek slashe `/` na samym końcu URL).

### Klient — Przy użyciu przekierowania portów

1. Pobierz oraz zainstaluj najnowszą wersję Fika,
2. Przejdź do katalogu, w którym znajduje się zainstalowany SPT i wypakuj zawartość pliku skompresowanego do tego katalogu,
3. Uruchom `Aki.Launcher.exe` i naciśnij 'Settings',
4. Zmień wartość w polu `URL` tak, aby odzwierciedlała Twój publiczny adres IP (WAN). Używając przykładu opisanego w **[Host — przy użyciu przekierowania portów](#host--przy-użyciu-przekierowania-portów)** wartością byłoby: `http://70.50.130.200:6969` (pamiętaj, aby usunąć jakiekolwiek slashe `/` na samym końcu URL),
5. Jeżeli hostujesz sesję w grze, zezwól na wszystkie połączenie (publiczne oraz prywatne), jeżeli Zapora sieciowa Windows wyświetli takie zapytanie.

### Klient — Przy użyciu VPN

1. Pobierz oraz zainstaluj najnowszą wersję Fika,
2. Przejdź do katalogu, w którym znajduje się zainstalowany SPT i wypakuj zawartość pliku skompresowanego do tego katalogu,
3. Uruchom `Aki.Launcher.exe` i naciśnij 'Settings',
4. Zmień wartość w polu `URL` tak, aby odzwierciedlała Twój adres IP serwera VPN. Używając przykładu opisanego w **[Host — przy użyciu VPN](#host--przy-użyciu-vpn)** wartością byłoby: `http://20.20.56.73:6969` (pamiętaj, aby usunąć jakiekolwiek slashe `/` na samym końcu URL),
5. Jeżeli hostujesz sesję w grze, zezwól na wszystkie połączenie (publiczne oraz prywatne), jeżeli Zapora sieciowa Windows wyświetli takie zapytanie.

## Funkcje i konfiguracja

### Funkcje i instrukcja użytkowania

**Fika** pozwala ci organizować sesje P2P z przyjaciółmi do gry w trybie współpracy (COOP). Osoba hostująca kontroluje większość logiki podczas gry, taką jak AI, polami minowymi, strefami snajperów, BTR-em itp. Każdy klient jest odpowiedzialny za własne zadawane i otrzymywane obrażenia, zarówno w stosunku do siebie, jak i AI. Oznacza to, że strzelanie do AI jest responsywne i szybkie.

Aby hostować grę, wybierz mapę i czas, a następnie na ostatnim ekranie kliknij `Host Raid`. Wybierz liczbę graczy, którzy będą grać (wliczając siebie) i poczekaj, aż gra się załaduje. Gdy wszystko będzie gotowe, inni gracze mogą dołączyć do twojej sesji, a gdy wszyscy skończą ładowanie, gra rozpocznie się automatycznie.

**Inne funkcje Fika**

- Wysyłanie przedmiotów
    - Kliknij prawym przyciskiem myszy na przedmiot w twoim stashu, aby wysłać go na inne konto
    - Możliwość dostosowania w [konfiguracji serwera](#konfiguracja-serwera)
- Wolna kamera (domyślnie przypisana do klawisza `F9`)
    - W trybie wolnej kamery możesz teleportować się na pozycję kamery, naciskając `T`
    - Możesz przeskoczyć do innego gracza, klikając `Lewy/Prawy` przycisk myszy
    - Możesz przeskoczyć bezpośrednio do ich głowy, trzymając `SPACE` podczas skoku
    - Możesz przeskoczyć do widoku z tyłu w trybie trzecioosobowym, trzymając `CTRL` podczas skoku
    - Możesz tymczasowo włączyć sterowanie wolną kamerą, naciskając klawisz `HOME`
- Mnożniki obrażeń dla hitboxów twojej postaci
- Dynamiczna liczba AI dla hostów, która wyłącza pojedyncze AI, gdy w pobliżu nie ma graczy
- Indywidualne limity liczby AI na mapę
- Culling zwiększający wydajność
- Indywidualne powiadomienia (śmierć członka drużyny, zabójstwo bossa przez gracza itp.)
- System pingowania, umożliwiający wskazywanie obszarów w grze dla twoich kolegów z drużyny
- Paski zdrowia graczy dla twoich kolegów z drużyny

Większość z tych funkcji jest konfigurowalna w [konfiguracji klienta](#konfiguracja-klienta).

### Konfiguracja klienta

Aby otworzyć konfigurację swojego klienta, naciśnij klawisz `F12` podczas gry. Przejdź do sekcji `Fika Core`, aby skonfigurować ustawienia.

**Coop**

- **Show Notifications**: Włącz niestandardowe powiadomienia, gdy gracz umiera, opuszcza grę, zabija bossa itp.
- **Auto Extract**: Automatyczna ekstrakcja podczas gry jako klient zamiast przechodzenia do wolnej kamery.
- **Show Extract Message**: Czy pokazywać wiadomość o ekstrakcji po śmierci/opuszczeniu gry.

**Coop | Custom**

- **Show Player Name Plates**: Przełącz widoczność pasków zdrowia i nicków.
- **Show HP% instead of bar**: Przełącz widoczność zdrowia w postaci procentowej zamiast paska.
- **Show Player Faction Icon**: Przełącz widoczność ikony frakcji obok paska HP.
- **Name Plate Scale**: Rozmiar kontenera z nickiem gracza.
- **Ping System**: Włącz/wyłącz system pingowania. Jeśli włączony, możesz odbierać i wysyłać pingi, naciskając klawisz pingowania.
- **Ping Button**: Przycisk używany do wysyłania pingów.
- **Ping Color**: Kolor twoich pingów, gdy są wyświetlane innym graczom.
- **Ping Size**: Mnożnik rozmiaru pinga.
- **Play Ping Animation**: Automatyczne odtwarzanie animacji wskazywania podczas pingowania. Może zakłócać rozgrywkę.

**Coop | Debug**

- **Free Camera Button**: Przycisk używany do przełączania wolnej kamery.

**Performance**

- **Dynamic AI**: Użyj systemu dynamicznego AI, wyłączając boty AI, gdy znajdują się poza zasięgiem jakiegokolwiek gracza.
- **Dynamic AI Range**: Zasięg, w którym AI będzie dynamicznie wyłączane.
- **Dynamic AI Rate**: Jak często dynamiczne AI powininno skanować odległość do wszystkich graczy.
- **Culling System**: Czy używać systemu cullingu, czy nie. Gdy gracze znajdują się poza zasięgiem cullingu, ich animacje będą uproszczone. Może to znacząco poprawić wydajność w niektórych wypadkach.
- **Culling Range**: Zasięg, w którym gracze powinni być upraszczani ('cullowani').

**Performance | Max Bots**

- **Enforced Spawn Limits**: Wprowadza limity spawnów przy pojawianiu botów, upewniając się, że nie przekraczają one standardowych limitów. Ma to znaczenie głównie przy użyciu modów do spawnu lub czegokolwiek, co modyfikuje limity botów.
- **Max Bots** `MAP`: Maksymalna liczba botów, które mogą być aktywne jednocześnie na mapie `MAP`. Przydatne, jeśli masz słabszy komputer. Ustaw na 0, aby wyłączyć.

**Network**

- **Native Sockets**:  NativeSockets dla przesyłania danych gry.
    > ❗ **UWAGA:** ta funkcjonalność może nie działać poprawnie
- **Force IP**: Wymusza na serwerze podczas hostowania użycie tego IP podczas wysyłania danych do backendu, zamiast próbować znaleźć odpowiednie IP automatycznie. Pozostaw puste, aby wyłączyć.
    > ❗ **UWAGA:** jest to wymagane podczas korzystania z VPN! Użyj swojego adresu IP dla sieci VPN.
- **Force Bind IP**: Wymusza na serwerze podczas hostowania użycie tego lokalnego IP podczas uruchamiania serwera. Pozostaw puste, aby wyłączyć.
    > ❗ **UWAGA:** jest to wymagane podczas korzystania z VPN! Użyj swojego adresu IP dla sieci VPN.
- **Auto Server Refresh Rate**: Co X sekund klient będzie pytał serwer o listę meczów, będąc w lobby.
- **UDP Port**: Port gry dla pakietów UDP.
- **Use UPnP**: Próbuje otworzyć porty za pomocą UPnP. Przydatne, jeśli nie możesz sam otworzyć portów, ale router obsługuje funkcję UPnP.

**Gameplay**

- **Head Damage Multiplier**: Mnożnik dla obrażeń otrzymanych dla hitboxów głowy. 0.2 = 20%
- **Armpit Damage Multiplier**: Mnożnik dla obrażeń otrzymanych dla hitboxów pach. 0.2 = 20%

### Konfiguracja serwera

Konfigurację serwera znajdziesz w folderze `user\mods\fika-server\assets\configs`. Otwórz plik `fika.jsonc` za pomocą dowolnego edytora tekstu.

> 💡 **Przykład pliku `fika.jsonc`**
>```json
>{
>    "client": {
>        "useBtr": true, // if the BTR should spawn on streets, default: true
>        "friendlyFire": true, // if friendly fire is enabled, default: true
>        "dynamicVExfils": false, // if vehicle exfils should scale to the amount of players in raid rather than default to 4, default: false
>        "allowFreeCam": false, // if the free cam can be toggled freely, default: false
>        "allowItemSending": true // if item sending should be enabled, default: true
>    },
>    "server": {
>        "giftedItemsLoseFIR": true // if sent items should lose their FiR status, default: true
>    }
>}
>```

