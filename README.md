## 1\. Wprowadzenie

---

#### Definicje

**SCADA** jest skrótem od frazy „_Supervisory Control and Data Acquisition_”, oznaczającej kontrolę nadzorczą i pozyskiwanie danych. System **SCADA** jest zwykle stosowany w połączeniu z oprogramowaniem i elementami sprzętowymi, na przykład programowalnymi sterownikami logicznymi (**PLC**) i zdalnymi jednostkami terminali (**RTU** _ang. Remote Terminal Unit_).

**HMI** (_ang. Human Machine Interface_) jest częścią większego systemu **SCADA**, razem z jego **PLC**, **RTU** i innymi funkcjami. Dokładniej HMI to system, którego operatorzy używają do interakcji ze **SCADA**, natomiast nadrzędny system **SCADA** realizuje wszystkie procesy związane z gromadzeniem i przechowywaniem danych oraz kontrolowaniem sprzętu. Interfejsy **HMI** są często wyposażone w ekrany i, w idealnym przypadku, posiadają łatwe w obsłudze panele obsługowe i elementy sterowania. Mogą wykorzystywać grafikę i wizualizację, ułatwiającą obsługę i interpretację danych i funkcji.

#### Zadania

Do zadań systemu **SCADA** należy:

> • Ciągła komunikacja ze sterownikiem **PLC**
>
> • Czytelna wizualizacja danych w czasie rzeczywistym
>
> • Obsługa bazy danych z odpowiednimi informacjami technologicznymi
>
> • Obsługa instalacji alarmowych
>
> • Generowanie raportów o postępach procesu technologicznego

#### Zastosowanie

Systemy **SCADA** są szczególnie istotne przy _skomplikowanych, wielkoskalowych_ instalacjach przemysłowych. Istotna jest zdolność do organizacji pracy wielu składowych równocześnie, w przeciwieństwie do prostych systemów **HMI**. Systemy **SCADA** umożliwiają organizacjom monitorowanie i raportowanie procesów na podstawie danych w czasie rzeczywistym oraz archwizację danych na potrzeby późniejszego przetwarzania i ewaluacji.

#### Schemat

![](https://cdn.discordapp.com/attachments/982375180401770526/1150086602945724416/panel-hmi-zamontowany-na-maszynie-automatyka-webhmi-scada4.jpg)

## 2\. Wymiana danych

![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/d32f02a0d256a3cb3115a531a950927cc46e02269df37cbd.png)

#### Poziomy systemu

>      0. Na najniższym poziomie _0_ znajdują się urządzenia _wykonawcze_ oraz _pomiarowe_
>
> 1. Pierwszy poziom składa się ze sterowników **PLC** 
> 2. Poziom drugi to komputery nadzorujące, odpowiedzialne za **HMI** oraz przekazanie informacji do komputerów koordynujących
> 3. Jednostki poziomu trzeciego nie wplywają bezpośrednio za działanie elementów wykonawczych, ale moniturują całokształt produkcji
> 4. Najwyższy poziom jest odpowiedzialny za planowanie produkcji i zbiorową analizę danych

##### Źródła: 

* [copadata.com](https://www.copadata.com/pl/product/zenon-software-platform-platforma-programowa-firmy-copa-data/wizualizacja-kontrola/co-to-jest-scada/)
* [iautomatyka.pl](https://iautomatyka.pl/co-to-jest-scada-i-co-daje-wizualizacja-procesow-przemyslowych/)
* [wikipedia.pl](https://pl.wikipedia.org/wiki/SCADA)
