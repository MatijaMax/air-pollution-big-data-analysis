# Air-Pollution-Analysis

## O projektu

- Predmet: Arhitekture sistema velikih skupova podataka
- Student: Matija Maksimović
- Tema: Analiza podataka o kvalitetu vazduha
- Opis projekta:
    - Cilj projekta je analiza podataka o kvalitetu vazduha u 2 režima obrade. 
    - Za batch obradu koriste se istorijski podaci o globalnom kvalitetu vazduha. (1.63 MB)
        - Ukupno 10 upita
    - Za streaming obradu podataka koriste se podaci sa senzora u Novom Sadu, Liman. Ako podaci sa domaćih senzora nisu adekvatni, može se kao primer uzeti neki drugi grad.
        - Ukupno 5 upita 

## Korišćeni podaci

- Skupovi podataka:
    - Batch:
        - [Global air pollution] [https://www.kaggle.com/datasets/hasibalmuzdadid/global-air-pollution-dataset](https://www.kaggle.com/datasets/hasibalmuzdadid/global-air-pollution-dataset)
    - Streaming:
        - [Liman air pollution] https://aqicn.org/data-platform/api/H9262/



## Struktura podataka - key data

GLOBAL DATA:
- ﻿Country, City, 
- AQI Value, AQI Category,
- CO AQI Value, CO AQI Category, Ozone AQI Value, Ozone AQI Category, NO2 AQI Value, NO2 AQI Category, PM2.5 AQI Value, PM2.5 AQI Category

SENSOR DATA:
- dominentpol
- IAQI
- forecast: PM2.5, PM10, O3, UVI


## Struktura repozitorijuma:
    - `TODO` - KT 2


## Struktura projekta

- Struktura repozitorijuma:
    - `TODO` - KT 2


- Dijagram arhitekture:

TODO - KT2

## Pokretanje projekta

TODO - KT2


## Upiti

### Batch upiti

1. Najzagađenije zemlje
2. Najčešće AQI kategorije
3. Doprinos zagađivača
4. Najčistiji gradovi
5. Distribucija zagađivača po kategoriji
6. Prosečne vrednosti AQI zagađivača po gradu
7. Rangiranje gradova po zagađivaču
8. Korelacija među kategorijama
9. Prekoračenja praga -- prag "nezdravo" :(
10. Poređenje kategorija među zemljama

11. 3,4 upita analiticki window funckija, bar 4 upita upita srednje slozenosti i bar 4 velike slozenosti, potencijalna izmena na semnaticki bogatiji skup podataka iste tematike

### Streaming upiti

1. Koliki je trenutni AQI u Novom Sadu(Liman) i kako se poredi sa zdravim granicama?
2. Koliki su trenutni nivoi PM2.5 i PM10 čestica i kako se upoređuju sa prihvatljivim granicama?
3. Koji zagađivač je trenutno dominantni uzročnik lošeg kvaliteta vazduha u Novom Sadu(Liman)?
4. Kakva je prognoza kvaliteta vazduha za naredna 24 sata i da li će se nivoi zagađivača poput PM2.5 ili ozona povećavati ili smanjivati?
5. Kako se trenutni nivoi ugljen-monoksida (CO), azot-dioksida (NO2) i ozona (O3) porede sa istorijskim nivoima ili bezbednosnim smernicama?

6. Neki upiti se moraju instant racunati neki odlozeno i logicka veza sa prethodnim skupom

### Dodatno
- AQI - Air Quality Index
- PM - Particulate Matter
 

