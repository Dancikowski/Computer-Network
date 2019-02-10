# Computer Network

<b style="color:red">Domena kolizyjna - </b> jeśli poprzez jedno medium transimsyjne np. kabel , co najmniej dwa urządzenia transmitują dane może dojść do kolizji. Obszar sieci, w którym może dojść do kolzji nazywamy domena kolizyjną. Maksymalna liczba urządzeń w domenie kolizyjnej to 1024. Przy czym im więcej urządzeń, tym większe ryzyko wystąpienia kolizji. Domenę kolizyjna mogą ograniczać switch (przełącznik) oraz router.  
W koncentratorze ( warstwa 1 OSI) wszystkie podłączone stacje składają się na domenę kolizyjną. Wszystkie zatem muszą korzystać z alogrytmu *CSMA/CD* w celu uporządkowania transmisji.
W przełączniku każdy port stanowi oddzielną domenę kolizyjną. Algorytm CSMA/CD NIE jest potrzebny.

<b>Domena rozgłoszeniowa </b> - to taki obszar sieci, do którego dotrze informacja przeslana z jednego komputera do wszystkich inych - broadcast. Coś jak wysłanie pakietu discover w procesie DORA DHCP. Ruch domeny rozgłoszeniowej jest przekazywany poprzez urządzenia pierwszej i drugiej warstwy modelu OSI tj. koncentratory, mosty, huby czy switche. Te urządzenia zwiększają obszar domeny rozgłoszeniowej. Ograniczają go natomiast urządzenia trzeciej warstwy - routery. Można również utworzyć sieć VLAN, która ograniczy zakres domeny rozgłoszeniowej. Urządzenia są w tej samej domenie rozgłoszeniowej jeśli mają taką samą podsieć, bramę domyślna i są w tej samej VLAN.
**Pytanie**: LAN = zasięg domeny rozgłoszeniowej.

<b>IEEE 802.11 - </b>standard bezprzewodowych sieci lokalnych (Wi Fi).

**IEEE 802.3 (Ethernet)** -najpopularniejszy typ przewodowych sieci lokalnych. Każdy z komputerów komunikuje się z użyciem protokołu Ethernet z urządzeniem zwanym **przełącznikiem**, z którym ustanawia połączenie dwupunktowe. Przełacznik posiada wiele portów, z których każdy jest połączony do jednego komputera. Zadaniem przełącznika jest przkazywanie pakietów pomiędzy podłączonymi komputerami na bazie adresów osadznych w pakietach.

**Algorytm routingu/ algorytm trasowania** - wyznaczanie najkrórtszej ścieżki pomiędzy routerami.

**VPN (Virtual Prisvate Network)** - sieć wykorzystywana w korporacjach, gdzie zdalni użytkownicy pracuja z domów na niezabezpieczonych łączach. Zapewnia szyfrowanie.

**Siec Ad Hoc** - sieć w której przyłączone urządzenia mogą pełnić zarówno rolę klienta, jak i Access Pointa.

**CSMA (Carrier Sense Multiple Access)** - algorytm arbitrażowy. Rozwiązuje problem kolizji w sieci 802.11. Polega na tym, że komputer chcący nadawać oczekuje na losowy adres przed transmijsą, a jeśli w czasie transmisji wykryje innego nadawcę, odstępuje od niej i znów czeka losowy okres.

**WEP** - schemat szyfrowania połączenia w sieci 802.11. Polegał na kryptograficznym odizolowaniu transmijsi pomidzy klientami. Schemat był jednak niedpracowany i został zostąpiony przez WPA, a następnie przez WPA2.

**10BASE-T** - standard Ethernetowy, który pozwala urządzeniom siciowym na komunikacje z wykorzystaniem skrętki. Przewidywana prędkość to 10 Mb/s.

Wyjaśnienie:

-   10 - prędkość
-   BASE - przesłanie sygnału w paśmie podstawowym bez modulacji
-   T - skrętka

**100BASE-TX** - tzw. fast Ethernet, maks prędkość to 100Mb/s. Medium transmisyjnym jest skretka nieekranowa UTP lub FTP zakończona obustronnie złączem 8P8C.

**1000BASE-TX/FX** - prędkość 1 Gigabit/s.

**Szereg fouriera** - jest wykorzystyawany do zmiany sygnału cyfrowego na analofowy (*Analiza*)

Zakres częstotliwości przenoszonych bez silnego tłumienia nazywamy **szerokością pasma**. Szerokość pasma jest fizyczną właściwością nośnika transmisjij zależną na przykład od konstruklcji kanału, czyli choćby od grubości i długośći przewodów czy śwatłowodów. Np. kanały sieci bezprzewodowych 802.11 mogą zajmować pasmo o szerkości mniej więcej 20MHz.

**Skrętka (twisted pair)** - najbardziej popularnym zaastosowaniem skrętki jest system telefonnii. Można wykonywac również połączenia z internetem (ADSL). Sygnał za pomoca tego medium można przeysłać nawet na odległość kilku kilometów jednak na dłuszą metę potrzebne będa regeneratory. Gdyby nie skręcanie kabelków, kable zakłócałyby się nawzajem. Skrętką można przesyłać sygnał analogowy jak i cyfrowy.

**UTP** - skrętka nieekranowa. Ekranowanie zmniejsza podatność na zakłócenia oraz przesłuchy.

**Standardy skrętki**: 
- U/UTP – skrętka nieekranowana
- F/UTP – skrętka foliowana
- U/FTP – skrętka z każdą parą w osobnym ekranie z folii.
- F/FTP – skrętka z każdą parą w osobnym ekranie z folii dodatkowo w ekranie z folii
- SF/UTP – skrętka ekranowana folią i siatką
- S/FTP – skrętka z każdą parą foliowaną dodatkowo w ekranie z siatki
- SF/FTP – skrętka z każdą parą foliowaną dodatkowo w ekranie z folii i siatki

**Kabel koncentryczny** - ma szersze pasmo niż nieekranowa skrętka. Pozwala na przesylanie sygnału z większą szybkością niż skrętka.

**Światłowody** - zapewnia jednokierunkowy system transmisjji danych, który przejmuje sygnał elektryczny, przekształca go i przesyła w postaci impulsów światła, a następnie ponownie przekształca wyjscie na sygnał elektryczny po stronie odbiornika.

**Modulacja cyfrowa** - proces konwersji bitów na reprezentujące je sygnały analogowe. Urządzenie używane do tego to **modem (Modular Deemulator)**

**Koder-dekoder** - urządzenie słuzące do przetwarzania sygnałów analogowych na na cyfrowe.

## Urządzenia

### Warstwa fizyczna:

**Wzmacniak** - urządzenia analogowe operujące na sygnałach przesyłanych kablami., do których są podłączone. Sygnał odebrany z jednego kabla jest oczyszczany, wzmacniany i propagowany do drugiego kabla. Wzmacniaki nie rozumieją ramek, pakietów i nagłówków.

**Koncentrator** - ma pewną liczbę linii wejściowych, które łączy elektrycznie. Ramki pojawiające się w dowolnej linii są wysyłane do wszystkich pozostałych. Działa w trybie półduplesku, czyli nie może jednocześnie odbierać i wysylać danych.
Przykład: do koncentratora, który ma 4 porty mamy podłączone 4 urządzenia. Komputer z portu 2 chce wysłać dane do komputera
na porcie numer 1. Wysyła również te dane do komputerów na portach 3 i 4, klienci na tych portach sprawdzają docelowy adres MAC
zawarty w nagłówku Ethernet i odrzucają to połączenie. To rozwiązanie generuje dużo niepotrzebnego ruchu sieciowego.

### Warstwa łącza danych

**Most** - posiada wiele portów. Inaczej niż w koncentratorze każdy z portów jest odizolowany od innych, a więc **wyznacza odrębną domene kolizyjną**. Jeśli port posiada pełnodupleksową linie dwupunktową, nie potrzebuje stosować algorytmu dostępu wielokrotnego CSMA/CD. Gdy do mostu przychodzi ramka, wydobywa on adres docelowy z jej nagłówka i szuka go w tablicy aby sprawdzić gdzie przesłac ramkę. Most przekazuje ramkę tylko na ten port gdzie powinna trafiić

**Przełączniki** - nowoczesne mosty. Został zaprojektowany w tym samym celu co koncentrator. Jednak w przeciwienstwie do koncentratora wysyła dane tylko do komputera dla którego są one przeznaczone. W celu indentyfiikacji komputerów przełącznik odróżnia komputery na
na podstawie adresów MAC, działa więc na warstwie 2. Może działać w trybie pełnego dupleksu.

Pytania:

-   Przełącznik LAN realizuje funkcję mostu.
-   Przełączniki stosują algorytm STA (Spanning Tree Algorithm)
-   Przełącznik rozszerza domenę rozgłoszeniową

### Warstwa sieciowa

**Router** - gdy pakiet dociera do routera, nagłowek i stopka ramki są usuwane, a pakiet mieszczący się w polu ładunku użytecznego ramki jest przekazywany do oprogramowania routingu. W pakiecie IP nagłówek zawiera 32 - bitowy (Ipv4) lub 128 - bitowy (IPv6) adres 802.

### Warstwa transportowa

**Brama** - łączy ona dwa komputery używające odmiennych połączeniowych protokołów transportowych. Załóżmy, że komputer używający połączeniowego TCP/IP chce komunikować się z komputerem używającym innego protokołu połączeniowego o nazwie SCTP. Brama może kopiować pakiety z jednego połączenia do drugiego, w razie potrzeby zmieniając ich format.

### Wirtualna sieć lokalna VLAN

Wirtualne sieci lokalne buduje się z użyciem odpowiednich przełączników. Aby zestawić sieć opartą na VLAN, administrator decyduje, ile sieci lokalnych będzie używanych, które komputery będa należeć do konkretnych z nich i jakie będa nazwy tych sieci. Aby wirtualna sieć mogła działać prawidłowo, należy skonfugurować tablice konfiguracyjne w mostach. Tablice te informują, które VLANY są dostępne przez które porty.

![strona rejestracji administratora](./assets/vlan.png)

Przykładowa sytuacja: Jedna z szarych stacji podłączonych do mostu B1 wysyła ramkę do adresata, który jeszcze nie zgłosił się do mostu i nie wiadomo gdzie się znajduje. Most odbierze tę ramkę zobaczy że pochodzi ona z szarej wirtualnej sieci lokalnej, więc roześlę ramkę tylko do stacji szarych oraz do innego mostu. Po stronie drugiego mostu będzia miała miejsce analogiczna sytuacja.

Procesy warstwy fizycznej oraz część procesów warstwy łącza danch działają w dedykowanych urządzeniach sprzętowych, określanych łącznie mianem kart interfejsów sieciowych **NIC (Network Interface Card)**

**Wysyłanie ramki przez warstwe łącza danych** - gdy warstwa łącza danych przejmuje pakiet, kapsułkuje go ramkę przez dodanie do niego nagłówka i stopki łącza danych.

**Ramka (frame)** składa się z czterech pól: kind, seq, ack i info, z których pierwsze zawierają informacje kontrolne, a ostatnie może zawierać faktcyzne dane do przesłania. Pola kontrolne noszą nazwę nagłówka ramki.

**Protokoły z oknem przesuwnym** - kwintesencją protokołów z oknem przesuwnym, jest to że w każdej chwili nadajnik pamięta zbiór numerów sekwencyjnych odpowiadających ramkom, które ma prawo wysłać. Mówimy że ramki te mieszczą się w **oknie nadawczym** . Podobnie odbiornik utrzymuje **okno odbiorcze** odpowiadające zbiorowi ramek, które ma prawo przyjąć.

**SONET** to protokół warstwy fizycznej wykorzystywany przede wszystkim w rozległych sieciach na bazie okablowania światłowodowego, składających się na sieci szkieletowe sieci telekomunikacyjnych, w tym sieci szkieletowe systemów telefonicznych. Zapewnia **strumień bitów** o dobrze ustalonej przeustowości.

**ATM (Asynchronous Transfer Mode)** to warstwa łącza danych oparta na transmisji komórek informacji o ustalonym rozmiarze. Słowo asynchroniczny oznacza, że komórki NIE muszą być nadawane stale, w postaci nieprzerwanego strumienia bajtów ładunku tak jak w SONET.

**SDH** - czyli synchroniczna hierarchia systemów cyfrowych. Jest to technologia sieci transportu informacji, charakteryzujący się tym , że wszystkie urządzenia działające w sieci SDH, pracujące w trybie bezawarjnym są zsynchronizowane zarówno do nadrzędnego zegara jak i do siebie nazwajem (W odróżnieniu do ATM)

**NEXT** - przesłuch zbliżny. Jest to zakłócenie generowane w parze na skutek transmisji sygnału w sąsiedniej parze. Współcynnik NEXT(Near End CrossTalk) jest mierzony jako stosunek amplitudy napięcia testowego do napięcia wyindukowanego w sąsiednej parze. Miarą są decybele.

## Bezpieczeństwo 802.11

Standard 802.11, określany pierwotnie mianem 802.11i, opisuje protokół zapobiegania odczytowi komunikatów wymienianych pomiędzy parą inych węzłów sieci bezprzewodowej albo ingerowaniu w nie. Rzecz znana również pod nazwą **WPA2 (Wi Fi protected Access 2)**. Stosowane wcześniej **WPA** to mechanizm skromniejszy, stanowiacy implementację podzbioru standardu 802.11i - preferowanym mechanizmem jest obecnie WPA2.

**WPA2** stosuje się typowo w dwóch przypadkach: pierwszy obejmuje wdrożenia korporacyjne, gdzie wyróżniono serwer uwierzytelniania z bazą użytkowników i haseł umożliwiających werfikacje, czy dany user może dostać dostęp do sieci. Alternatywą jest tutaj **EAP(Extensible Authentication Protocol)** opisujący sposób interakcji pomiędzy klientem, a serwerem uwierzyelniania.

Drugi scenariusz to przypadek instalacji domowej, gdzie nie ma wyróznionego serwera uwierzytelniania. Zamiast tego mamy pojedyczne wspólne hasło dostępowe

Pytanie: Czy 802.1X oraz 802.1i wykorzystują EAP? **TAK**

## Protokoły routingu

Internet jest zbudowany z dużej liczby systemów niezależnych albo **AS (Autonomous Systems)** zarządzanych przez różne organizacje (korporacje, uczelnie i operatorów sieciowych).

**OSPF (Open Shortest Path First)** - protokół routingu wewnętrznego. Do znajdowania najkrótszej trasy używa algorytmu Dijkstry.

**RIP** - wczesny protokół routingu wewnętrznego opierający się na wektorze odległości.Do utworzenia metryki stosuje się jedynie liczbę przeskoków (liczba kolejnych routerów na danej trasie). Używa UDP jako protokołu warstwy transportowej. 

**EIGRP** - hybrydowy protokół trasowania operuący na algorytmie wektora odległości. Ma fragmentaryczną wiedzę o strukturze sieci.

**BGP (Border Gateway Protocol)** - w obrębie jednego systemu autonomicznego AS routing załatwiają najczęściej protokoły OSPF i IS-IS. Ale pomiędzy AS-ami króluje inn protokół o nazwie BGP - protokół bram granicznych.

## Bluetooth

Standard bezprzewodowej komunikacji krótkiego zasięgu pomiędzy różnymi urządzeniami elektronicznymi, takimi jak klawiatura, komputer, laptop, palmtop, smartfon i wieloma innymi.
Jest to otwarty standard opisany w specyfikacji IEEE 802.15.1. Jego specyfikacja techniczna obejmuje trzy klasy mocy nadawczej ERP 1-3 o zasięgu 100, 10 oraz 1 metra w otwartej przestrzeni. Najczęściej spotykaną klasą jest klasa druga. Standard korzysta z fal radiowych w paśmie częstotliwości ISM 2,4 GHz.
Do wymiany danych stosuje dwa typy łączy **SCO** oraz **ACL**.
Bluetooth wkorzystuje **FHSS**

**FHSS (Frequency-Hopping Spread Spectrum)** – metoda rozpraszania widma w systemach szerokopasmowych. W tłumaczeniu wprost jest to „skakanie” sygnału po częstotliwościach w kolejnych odstępach czasu, w dostępnym widmie (paśmie). Spotykana również w sieciach Wi - Fi.

## Access Point

Urządzenie zapewniające hostom dostęp do sieci komputerowej za pomocą bezprzewodowego nośnika transmisyjnego jakim są fale radiowe.

Punkt dostępowy jest zazwyczaj mostem łączącym bezprzewodową sieć lokalną (VLAN) z siecią lokalną (LAN). W związku z tym punkt dostępowy musi posiadać co najmniej dwa interfejsy sieciowe:

- bezprzewodowy działający w oparciu o standard IEEE 802.11 (Wi-Fi)
- przewodowy służący połączeniu AP z siecią standardu IEEE 802.3 (Ethernet) bądź modem standardu DSL

Access point rozgłasza **SSID**

**SSID (service set identifier)** – identyfikator sieci składający się maksymalnie z 32 znaków, dodawany do nagłówków pakietów wysyłanych przez bezprzewodową sieć lokalną. Pełni on rolę loginu przy próbie nawiązywania połączeń z punktami dostępowymi. Urządzenia, które łączą się z danym punktem dostępowym, korzystają z przypisanego do niego identyfikatora SSID.

### Typy sieci bezprzewodowych z wykorzystaniem AP

**BSS (Basic Service Set)** - jeśli stacje chcą przesyłać dane między sobą, mogę to robić tylko za pośrednictwem AP. W związku z tym każda stacja musi znajdować się w pobliżu punktu dostępowego, więc zasięg sieci jest równy zasięgowy AP. 

**ESS (Extended Service Set)** - powstaje w wyniku połączenia kilku BSS-ów za pomocą sieci szkieletowej. W takiej sieci stacje mogą przemieszczać się pomiędzy różnymi BSS-ami bez utraty połączenia. Na obszarze sieci ESS możliwy jest **roaming**.

## Polecenia w systemie Linux

**Netstat** - wyświetla połączenia sieciowe, tablice tras, statystyki interfejsów, połączenia masquerade i członkostwa multicast. 

**Nslookup** - narzędzie działające podobnie do protokołu DNS, zwraca adres IP żądanego endpointu oraz adres serwera. Po wybraniu opcji z autoryzacją można otrzymać bardziej szczegółowe informacje

**ifconfig** - służy do sprawdzania i zmieniania intefejsów sieciowych.

**traceroute** - służy do badania trasy pakietów w sieci

**ping** - służy do diagnozowania połączeń sieciowych. Wykorzystuje ICMP.

## Adresacja IPv4

Adres IP to adres interfejsu sieciowego, nie urządzenia.

**Adres podsieci**:

Adres -- Maska --> operacja AND

**Adres rozgłoszeniowy**:

(Maska --> NOT -- Adres) --> Operacja OR

**Adres pierwszego hosta**:

Gdy adres sieci 192.168.11.15 -> pierwszy host 192.168.11.16

**Adres ostatniego hosta**: 

Gdy adres rozgłoszeniowy 192.168.11.255 -> ostatni host 192.168.11.254

**Podział sieci na podsieci**: 

Podział na podsieci odbywa się poprzez pożyczanie kolejnych bitów z części hosta w masce podsieci.

255.255.255.0 -> 1 podsieć

255.255.255.128 -> 2 podsieci. Pożyczony został 1 bit pierwszy od lewej czyli 2<sup>7</sup>.

Ilość podsieci = 2<sup> pożyczona liczba bitów</sup>


### IPv6
 
- Długość adresu: 128 bitów
- Brak sumy kontrolnej w nagłówku w odróżnieniu od IPv4
- Nie używa ARP
- Adres hosta zajmuje 64 bity

## Różne


**Big endian** - to forma zapisu danych, w której najbardziej znacząct bajt jest ustawiany jako pierwszy.

**NAT (Network Address Translation)** - polega na tym, że operator ISP przydziela każdemu domostwu albo firmie pojedynczy adres IP. Wewnątrz sieco klienta każdy komputer otrzymuje unikatowy adres IP używany do komunijacji wewnętrznej. Gdy jednak pakiet od któregoś z hostów sieci wewnętrznej ma zostać przekzany do sieci operatora, odbywa się translacja adresu z unikatowego wewnętrznego adresu IP na adres publiczny wspólny dla całej sieci wewnętrznej. 

**MIMO (Multiple Input Multiple Output)** - technologia działająca w sieciach 802.11abgn. Urządzenia MIMO są zdolne do ciągłego przetwarzania każdego ze składników sygnału wielościeżkowego i mogą np.: zapobiegać nakładaniu się składowych sygnału będących w przeciw-fazie, skutkującego zniekształceniem sygnału. Poprawne działanie takiego systemu zakłada wykorzystanie kilku zupełnie różnych technik radiowych. Co ważne, niektóre z tych technik oferują korzyści i są kompatybilne z urządzeniami działającymi w starszych standardach 802.11a/b/g, pozostałe wymagają urządzeń zgodnych ze standardem 802.11n po obu stronach linku.

**NAS (Network Attached Storage)** - Serwer NAS, czyli Network Attached Storage to nic innego jak niewielki komputer pełniący rolę dysku sieciowego. Dostęp do danych znajdujących się na NAS możliwy jest ze wszystkich urządzeń znajdujących się w sieci lokalnej – oczywiście pod warunkiem posiadania odpowiednich uprawnień. Serwery NAS umożliwiają ograniczenie dostępu do określonych danych, co zwiększa bezpieczeństwo poufnych informacji. **Access Point** pełni funkcję serwera NAS.

**ARPANET (Advanced Research Projects Agency Network)** – pierwsza sieć rozległa oparta na rozproszonej architekturze i protokole TCP/IP. Jest bezpośrednim przodkiem Internetu. Istnieje do dziś.

**IPsec** - zbiór protokołów służących implementacji bezpiecznych połączeń oraz wymiany kluczy szyfrowania pomiędzy komputerami. Protokoły tej grupy mogą być wykorzystywane do tworzenia Wirtualnej Sieci Prywatnej (ang. VPN. Połączenie jest szyfrowane za pamocą algorytmów. Działa w dwóch trybach **transportowym** oraz  **tunelowym**. IPv6 posiada zintegrowany IPsec.

