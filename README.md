## README - Proiect TSC 2025
## Titlu Proiect: Ebook Reader
## Nume: Carazeanu Antonio-Christian
## Grupa: 332CC

Cuprins:

0. Descrierea generala
1. Diagrama bloc
2. BOM - Bill of Materials
3. Functionalitatea hardware
4. Pini utilizați pe ESP32-C6 și justificare
5. Probleme intampinate

## 0. Descriere Generală:
Proiectul a avut ca scop realizarea unui Ebook Reader ieftin si OpenSource din
perspectiva unui Arhitect de Sistem. Acest dispozitiv poate fi scos pentru a fi
produs in masa.

Am urmat toți pașii standard de proiectare, începând de la schematic, continuând
cu layout-ul PCB, modelare 3D și integrarea finală într-o carcasă.

## 1. Diagrama bloc
## 2. BOM - Bill of Materials

## 2. BOM - Bill of Materials

| Component Name         | Device/Value                          | Check Price | Datasheet |
|------------------------|---------------------------------------|-------------|-----------|
| BOOT_BUTTON            | BUTTON_CUSYOMV1                       | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) | [Link](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) |
| C1                     | 0.1uF/50V (0402)                      | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) | [Link](https://componentsearchengine.com/part-view/CC0402MRX5R5BB106/YAGEO) |
| C3                     | 100uF Tantalum                        | [Link](https://a360.co/4iZy6AA) | [Link](https://a360.co/4iZy6AA) |
| CHG_LED                | LED0603                               | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603) | [Link](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603) |
| D1                     | USBLC6-2SC6Y (ESD Protection)         | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda) |
| D2, D7                 | SD0805S020S1R0 (Schottky)             | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D) | [Link](https://eu.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D) |
| D3-D5                  | MBR0530 (Schottky)                    | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/MBR0530/Onsemi/view-part/?ref=eda) |
| D6, D8-D12             | PGB1010603MR (TVS Diode)              | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda) |
| IC1                    | BD5229G-TR (Voltage Detector)         | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor) | [Link](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor) |
| IC4                    | XC6220A331MR-G (LDO Regulator)        | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) |
| J1                     | FH34SRJ-24S-0.5SH_99_ (FFC Connector) | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) | [Link](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) |
| J2                     | USB4110-GF-A (USB-C Connector)        | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY) | [Link](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY) |
| J3                     | QWIIC_CONNECTORJS-1MM                 | [Link](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?ref=search&t=qwiic) | [Link](https://www.snapeda.com/parts/PRT-14417/SparkFun%20Electronics/view-part/?ref=search&t=qwiic) |
| J4                     | 112A-TAAR-R03_ATTEND (MicroSD Slot)   | [Link](https://store.comet.srl.ro/Catalogue/Product/43497/) | [Link](https://store.comet.srl.ro/Catalogue/Product/43497/) |
| L1                     | 68uH Inductor                         | [Link](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D) | [Link](https://eu.mouser.com/ProductDetail/Wurth-Elektronik/744043680?qs=PGXP4M47uW6VkZq%252BkzjrHA%3D%3D) |
| PFMF.050.1             | VARISTORCN1812                        | [Link](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D) | [Link](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D) |
| Q1, Q2                 | DMG2305UX-7 (MOSFET)                  | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated) | [Link](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated) |
| SENSOR2                | BME680 (Environmental Sensor)         | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home) | [Link](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home) |
| SJ1                    | Solder Jumper                         | [Link](https://grabcad.com/library/solder-jumpers-1) | [Link](https://grabcad.com/library/solder-jumpers-1) |
| U1                     | W25Q512JVEIQ (Flash Memory)           | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/W25Q512JVEIQ/Winbond+Electronics/view-part/?ref=eda) |
| U2                     | ESP32-C6-WROOM-1-N8                   | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) |
| U3                     | DS3231SN# (RTC)                       | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda) |
| U4                     | MAX17048G+T10 (Fuel Gauge)            | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda) | [Link](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda) |
| U5                     | MCP73831 (Charging IC)                | [Link](https://componentsearchengine.com/part-view/MCP73831T-2ATI%2FOT/Microchip) | [Link](https://componentsearchengine.com/part-view/MCP73831T-2ATI%2FOT/Microchip) |

## 3. Functionalitatea hardware


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

