## README - Proiect TSC 2025
## Titlu Proiect: Ebook Reader
## Nume: Carazeanu Antonio-Christian
## Grupa: 332CC

Cuprins:

0. Descrierea generala
1. Diagrama bloc
2. BOM - Bill of Materials
3. Arhitectura hardware
4. Pini utilizați pe ESP32-C6 și justificare
5. Probleme intampinate
6. Observatii

## 0. Descriere Generală:
Proiectul a avut ca scop realizarea unui Ebook Reader ieftin si OpenSource din
perspectiva unui Arhitect de Sistem. Acest dispozitiv poate fi scos pentru a fi
produs in masa.

Am urmat toți pașii standard de proiectare, începând de la schematic, continuând
cu layout-ul PCB, modelare 3D și integrarea finală într-o carcasă.

## 1. Diagrama bloc
![Diagrama](Images/diagrama.png)

## 2. BOM - Bill of Materials
| Device | Value | Check_Price | Datasheet |
|--------|-------|-------------|-----------|
| ADAFRUIT_LEDCHIP-LED0603 | - | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603) | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/datasheet/) |
| SJ | - | [Link](https://grabcad.com/library/solder-jumpers-1) | - |
| EAGLE-LTSPICE_C | 0.1uF/50V | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 0.47 | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 100K | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| EAGLE-LTSPICE_C | 100nF | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| RCL_CPOL-EUCT3528 | 100uF TANT | [Link](https://www.snapeda.com/parts/TAJB475K025RNJ/AVX/view-part/?ref=dk&t=capacitor%203528&con_ref=None) | [Link](https://s3.amazonaws.com/snapeda/datasheet/TAJB475K025RNJ_AVX.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 10K | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| EAGLE-LTSPICE_C | 10uF | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| 112A-TAAR-R03_ATTEND | 112A-TAAR-R03_ATTEND | [Link](https://store.comet.srl.ro/Catalogue/Product/43497/) | [Link](https://store.comet.bg/download-file.php?id=8824) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 15 | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| EAGLE-LTSPICE_C | 1uF | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| EAGLE-LTSPICE_C | 1uF/50V | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 2.2 | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 200 | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| ESP32_WROVER_SPARKFUN-DISCRETESEMI_MOSFET_PCH-DMG2305UX-7 | 20V/4.2A/52m?/1.4W | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated) | [Link](https://www.diodes.com//assets/Datasheets/DMG2305UX.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 2K | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| EAGLE-LTSPICE_C | 4.7uF | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| EAGLE-LTSPICE_C | 4.7uF/25V | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/Datasheets/2/CC0402MRX5R5BB106.pdf) |
| ESP32_WROVER_EAGLE-LTSPICE_R | 5k1 | [Link](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Link](https://www.yageo.com/upload/media/product/products/datasheet/rchip/PYu-RC_Group_51_RoHS_L_12.pdf) |
| 744043680IND_4828-WE-TPC_WRE | 68uH | [Link](https://ro.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D&_gl=1*5xajdn*_ga*MzY2ODgyMjE4LjE3NDM2NzQxODk.*_ga_15W4STQT4T*MTc0Mzg3MzkxMy40LjAuMTc0Mzg3MzkxNi41Ny4wLjA.) | [Link](https://www.we-online.com/components/products/datasheet/744043680.pdf) |
| BD5229G-TR | BD5229G-TR | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor) | [Link](https://datasheet.datasheetarchive.com/originals/distributors/Datasheets_SAMA/f2b9741ef86007909f138d561a359946.pdf) |
| ESP32_WROVER_BME680_BME680 | BME688 | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home) | [Link](https://www.snapeda.com/parts/BME680/Bosch%20Sensortec/datasheet/) |
| BUTTON_CUSYOMV1V2 | BUTTON_CUSYOMV1V2 | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) | [Link](https://industry.panasonic.com/global/en/downloads?tab=catalog&small_g_cd=203&part_no=EVQPUJ02K) |
| CPH3225A | CPH3225A | [Link](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda ) |
| DS3231SN# | DS3231SN# | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda) |
| ESP32-C6-WROOM-1-N8 | ESP32-C6-WROOM-1-N8 | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) |
| ESP32C6_VARISTORCN1812 | ESP32C6_VARISTORCN1812 | [Link](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D) | [Link](https://www.tdk-electronics.tdk.com/inf/75/db/CTVS_14/Surge_protection_series.pdf) |
| ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831 | ESP32_WROVER_SPARKFUN-IC-POWER_MCP73831 | [Link](https://ro.mouser.com/ProductDetail/Microchip-Technology/MCP73831T-2ACI-OT?qs=yUQqVecv4qvbBQBGbHx0Mw%3D%3D) | [Link](https://ro.mouser.com/datasheet/2/268/MCP73831_Family_Data_Sheet_DS20001984H-3441711.pdf) |
| FH34SRJ-24S-0.5SH_99_ | FH34SRJ-24S-0.5SH_99_ | [Link](https://componentsearchengine.com/part-view/FH34SRJ-24S-0.5SH(99)/Hirose) | [Link](https://www.hirose.com/en/product/document?clcode=CL0580-1255-6-99&productname=FH34SRJ-24S-0.5SH(99)&series=FH34SRJ&documenttype=2DDrawing&lang=en&documentid=0000990903) |
| MAX17048G+T10 | MAX17048G+T10 | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda) |
| MBR0530. | MBR0530. | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/MBR0530/ON%20Semiconductor/datasheet/) |
| PGB1010603MR. | PGB1010603MR. | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse%20Inc./datasheet/) |
| QWIIC_CONNECTORJS-1MM | QWIIC_RIGHT_ANGLE | [Link](https://www.digikey.lt/en/models/926710 ) | [Link](https://www.digikey.lt/en/models/926710) |
| SAMACSYS_PARTS_USB4110-GF-A | SAMACSYS_PARTS_USB4110-GF-A | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)) | [Link](https://gct.co/files/drawings/usb4110.pdf) |
| ESP32_WROVER_AVX---SD0805S020S1R0_AVX_SD0805S020S1R0_0_0AVX_SD0805S020S1R0_0_0 | SD0805S020S1R0 | [Link](https://ro.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D) | [Link](http://datasheets.avx.com/schottky.pdf) |
| SI1308EDL-T1-GE3 | SI1308EDL-T1-GE3 | [Link](https://www.snapeda.com/parts/SI1308EDL-T1-GE3/Vishay+Siliconix/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/SI1308EDL-T1-GE3/Vishay+Siliconix/view-part/?ref=eda) |
| TPV1 | TPV1 | Custom made | - |
| USBLC6-2SC6Y | USBLC6-2SC6Y | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda) |
| W25Q512JVEIQ | W25Q512JVEIQ | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda) |
| XC6220A331MR-G | XC6220A331MR-G | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) | [Link](https://product.torexsemi.com/system/files/series/xc6220.pdf) |

## 3. Arhitectura Hardware

Descriem în continuare componentele hardware cheie și funcționalitatea acestora în cadrul dispozitivului:

| Nr. | Componentă Principală                   |
|-----|------------------------------------------|
| 1   | Microcontroller – ESP32-C6-WROOM-1       |
| 2   | Ecran E-Ink – Waveshare WSH-13187, 7.5”  |
| 3   | Senzor Ambiental – Bosch BME688          |
| 4   | Sistem de Alimentare și Baterie          |
| 5   | Butoane de Control – 3x Tactile Switch   |
| 6   | Conector USB-C                           |
| 7   | Port Extensie Qwiic / STEMMA QT (I²C)    |
| 8   | Soclu MicroSD – Attend 112A-TAAR-R03     |
| 9   | Ceas Timp Real (RTC) – DS3231            |

### 3.1. Unitatea Centrală – Microcontroller ESP32-C6-WROOM-1

-   **Unitate de Procesare:** RISC-V pe 32 de biți, tactat la 160MHz
-   **Memorie:** 512KB SRAM integrat + 8MB memorie flash externă (model W25Q512JVEIQ)
-   **Opțiuni de Comunicare:** Wi-Fi 6 (standard 802.11ax), Bluetooth 5 LE, interfață USB 2.0 Full-Speed
-   **Interfețe Disponibile:** SPI, I²C, UART, multiple porturi GPIO
-   **Consum Energetic:** Sub 50µA în modul deep sleep; diverse moduri de consum redus sunt implementate
-   **Funcții de Securitate:** Include secure boot, criptare pentru memoria flash și accelerare hardware pentru criptografie

### 3.2. Afișajul Electronic – Ecran E-Ink Waveshare WSH-13187, 7.5”

-   **Rezoluție:** 800x480 pixeli, imagine monocromă
-   **Modalitate de Conectare:** Interfață SPI (4 fire) plus linii de control CS, DC, RST, BUSY
-   **Consum Energetic:** Aproximativ 15–25mA în timpul actualizării imaginii; consum neglijabil în stare statică
-   **Rațiunea Alegerii:** Consumul energetic aproape nul când imaginea nu se schimbă, optim pentru aplicații tip e-reader

### 3.3. Senzorul Ambiental Integrat – Bosch BME688

-   **Parametri Măsurați:** Temperatură, Umiditate relativă, Presiune atmosferică, Indice al Calității Aerului (estimare eCO2, TVOC)
-   **Acuratețe:** ±1°C pentru temperatură, ±3% pentru umiditate, ±1 hPa pentru presiune
-   **Modalitate de Conectare:** Interfață I²C (operând la 400kHz)
-   **Consum Energetic:** 2.1µA în standby, maxim 3.6mA în timpul măsurătorilor active
-   **Rațiunea Alegerii:** Soluție compactă multi-senzor, potrivită pentru monitorizarea condițiilor ambientale

### 3.4. Sistemul de Alimentare și Gestionarea Energiei

-   **Sursa de Energie:** Acumulator Li-Po de 3.7V cu o capacitate de 2500mAh
-   **Monitorizare Baterie:** Circuit integrat MAX17048 (comunică prin I²C)
-   **Circuit de Încărcare:** MCP73831 – permite încărcarea cu 5V/1A via portul USB-C
-   **Regulator de Tensiune:** LDO ce furnizează o tensiune stabilă de 3.3V pentru întregul circuit
-   **Consum Total Estimativ:**
    -   În mod activ: între 100 și 150mA
    -   În mod deep sleep: sub 50µA

### 3.5. Interfața cu Utilizatorul – 3x Butoane Tactile

-   **Model Buton:** Panasonic EVQ-Q2A03W
-   **Conectare Electrică:** Legate la pini GPIO, cu circuit de debounce hardware (filtru RC)
-   **Funcționalități Asignate:** Navigare prin meniuri, avansare/revenire pagină, confirmare acțiuni

### 3.6. Conectorul USB-C

-   **Funcționalități Principale:** Încărcarea bateriei și transferul de date (conform standardului USB 2.0)
-   **Măsuri de Protecție:** Protecție ESD integrată și terminații conforme standardului
-   **Posibilități Suplimentare:** Actualizări software OTA (Over-The-Air) via Wi-Fi sau actualizare firmware prin conexiune USB

### 3.7. Portul de Extensie Qwiic / STEMMA QT (I²C)

-   **Configurație Pini:** VCC (Alimentare), GND (Masă), SDA (Date I²C), SCL (Ceas I²C)
-   **Scop/Beneficii:** Permite conectarea rapidă a modulelor și senzorilor externi compatibili I²C

### 3.8. Soclul pentru Card MicroSD – Attend 112A-TAAR-R03

-   **Rol Principal:** Oferă spațiu de stocare extern (pentru cărți electronice, fișiere jurnal, firmware etc.)
-   **Modalitate de Conectare:** Interfață SPI

### 3.9. Ceasul Timp Real (RTC) – DS3231

-   **Acuratețe:** Deviație maximă de ±2 părți per milion (ppm)
-   **Modalitate de Conectare:** Interfață I²C
-   **Alimentare de Backup:** Asigurată de un supercapacitor

---

### Protocoale de Comunicare și Interfețe Utilizate

| Protocol/Interfață | Componente Conectate                                |
|--------------------|-----------------------------------------------------|
| **SPI**            | Ecran E-Paper, Memorie Flash externă, Card SD (SPI) |
| **I²C**            | Senzor BME688, Fuel Gauge MAX17048, RTC DS3231, Port Qwiic/Stemma |
| **USB**            | Încărcare și comunicație de date via USB-C         |
| **GPIO**           | Butoane, Linii control afișaj, Activare încărcare   |

---

### Profil de Consum Energetic (Estimări)

| Stare/Componentă       | Consum Estimativ   |
|------------------------|--------------------|
| ESP32-C6 (mod activ)   | 80–100mA           |
| Actualizare E-Paper    | 15–25mA            |
| Senzor BME688 (activ)  | 3.6mA              |
| Fuel Gauge MAX17048    | ~50µA              |
| RTC DS3231             | 3.5mA / 1µA backup |
| Deep Sleep (Total)     | <50–100µA          |

---

### Specificații Fizice și Constructive

-   **Mărimi Fizice:** 175 x 114 x 10 mm
-   **Masa Dispozitivului:** Aproximativ 250g
-   **Material Carcasă:** ABS sau policarbonat, cu design ergonomic
-   **Montare Afișaj:** Integrat într-un decupaj specific al carcasei
-   **Detalii de Fabricație:** PCB cu 2 straturi, finisaj ENIG, carcasă obținută prin injecție de plastic


## 4. Pini utilizați pe ESP32-C6 și justificare

| Pin ESP32-C6 | Componentă / Semnal                | De ce?                                                                 |
|--------------|-------------------------------------|------------------------------------------------------------------------|
| GPIO1        | I²C SDA (BME688, MAX17048, DS3231, Qwiic) | Linie partajată I²C – economisește pini și permite extinderea facilă |
| GPIO2        | I²C SCL (BME688, MAX17048, DS3231, Qwiic) | Clock I²C pentru toți senzorii și extensii Qwiic                     |
| GPIO5        | SPI MISO (E-Paper, Flash extern)    | Linie comună de intrare date în SPI                                   |
| GPIO6        | SPI MOSI (E-Paper, Flash extern)    | Linie de ieșire date către e-paper și flash                           |
| GPIO7        | SPI CLK                             | Semnal de clock pentru magistrala SPI                                 |
| GPIO8        | E-Paper CS                          | Selectează afișajul pe magistrala SPI                                 |
| GPIO9        | E-Paper DC (Data/Command)           | Comută între comandă și date către e-paper                            |
| GPIO10       | E-Paper RST                         | Reset hardware e-paper                                                |
| GPIO11       | E-Paper BUSY                        | Pin de stare (ocupat/liber) de la display                             |
| GPIO12       | Button #1                           | Intrare digitală pentru navigare pagină înainte                      |
| GPIO13       | Button #2                           | Intrare digitală pentru navigare pagină înapoi                       |
| GPIO14       | Button #3                           | Intrare digitală pentru selectare/opțiune                            |
| GPIO15       | MAX17048 ALERT (opțional)           | Pin de alertă nivel scăzut baterie                                    |
| GPIO16       | USB D+ (intern la USB PHY)          | Linie USB 2.0 (fixă pe ESP32-C6)                                      |
| GPIO17       | USB D- (intern la USB PHY)          | Linie USB 2.0 (fixă pe ESP32-C6)                                      |
| GPIO18       | LED Status (opțional)               | Indicator pentru activitate Wi-Fi, charging, notificări               |
| GPIO19       | SD Card CS                          | Selectare chip pentru card microSD (SPI)                              |
| GPIO20       | SD Card MISO                        | Citire date de pe card microSD                                        |
| GPIO21       | SD Card MOSI                        | Scriere date pe card microSD                                          |
| GPIO4        | SD Card CLK                         | Semnal de clock pentru card microSD (SPI)                             |

## 5. Probleme intampinate
1) La partea de 3D am întâmpinat o problemă semnificativă — modelele 3D ale rezistențelor și condensatoarelor nu se actualizau automat în PCB atunci când încercam să folosesc funcția Replace Package. Pentru a rezolva această problemă, a trebuit să adaug manual modelele 3D custom realizate pentru fiecare componentă în parte.

2) Bobina si mufa USB au avut dimensiunea pad-urilor mai mica decat grosimea firelor, marint astfel pad-urile din footprint pentru a putea face lipirea.

## 6. Observatii
Un proiect mult prea muncitoresc care nu merita doar 2pct din nota.
Timp de lucru aprox ~70h
