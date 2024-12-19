# Air-Pollution-Analysis

## O projektu

- Predmet: Arhitekture sistema velikih skupova podataka
- Student: Matija Maksimović
- Tema: Analiza podataka o kvalitetu vazduha
- Opis projekta:
    - Cilj projekta je analiza podataka o kvalitetu vazduha u 2 režima obrade. 
    - Za batch obradu koriste se istorijski podaci o kvalitetu vazduha u SAD. 
        - Ukupno 10 upita
    - Za streaming obradu podataka koriste se istorijski podaci sa senzora u Atini.
        - Ukupno 5 upita 

## Korišćeni podaci

- Skupovi podataka:
    - Batch:
        - [USA air pollution] https://www.kaggle.com/datasets/mexwell/us-air-pollution
    - Streaming:
        - [Athens air pollution] https://www.kaggle.com/datasets/yekenot/air-quality-monitoring-in-european-cities



## Struktura podataka - key data

BATCH DATA:
- ﻿The four pollutants (NO2, O3, SO2 and O3) each has 5 specific columns: Units, Max, Min, Mean, AQI
- State, County, City, Monitoring Site
- Date

STREAM DATA:
- Wind Speed (U, V)
- Temp
- Date
- O3, N02, PM10, PM2.5


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

1. Koliko jedinstvenih monitoring lokacija postoji u svakoj državi?
2. Koja je prosečna koncentracija (Mean) NO2 na svim monitoring lokacijama?
3. Navedite 5 gradova sa najvišim AQI za ozon (O3) za jedan dan.
4. Koji je prosečan AQI za svaki zagađivač (NO2, O3, SO2, CO) u svakom okrugu?
5. Identifikujte okruge sa najvišim kombinovanim AQI (zbir AQI za sve zagađivače) u određenom periodu. 
6. Koje su prosečne dnevne vrednosti AQI za svaki zagađivač (NO2, O3, SO2, CO) u toku godine?
7. Odredite trend AQI vrednosti za svaki zagađivač tokom godine.
8. Rangirajte gradove na osnovu varijacije dnevnih AQI vrednosti za zagađivače, koristeći standardnu devijaciju u analytic window funkciji od 30 dana (na primer mesec april).
9. Rangirajte države na osnovu prosečnog AQI za svaki zagađivač tokom godine. 
10. Identifikujte sezonske obrasce u prosečnim mesečnim vrednostima koncentracija zagađivača (grupisanje po mesecima i dodavanje informacija o sezoni).

NAPOMENA: Za složene upite (7-10) iskoristiti analytic window

### Streaming upiti

1. Prikazati trenutne vrednosti AQI (Air Quality Index) za NO2, O3, PM10 i PM2.5 na svakom monitoring mestu. (računajući te vrednosti u realnom vremenu čim novi podaci dođu u tok podataka)
2. Spajanje podataka o koncentracijama zagađivača sa podacima o kretanju vetra (U i V komponente) kako bi se analizirali obrasci disperzije zagađivača u određenim oblastima. (interesantna analiza za prezentovanje na mapi ili čak možda prikaz sa animacijama) - formule: Wind direction=atan2(V,U), Wind speed=sqrt(U * U + V * V)
3. Izračunati prosečnu temperaturu poslednjih 70 minuta za sve monitoring stanice i obezbediti da se podaci ažuriraju svakih 70 minuta u realnom vremenu. (70 minuta zbog istorijskih podataka, pri demo prezentaciji možemo simulirati ubrzanje) 
4. Upoređivanje koncentracije PM2.5 između Atine i gradova u SAD-u.
5. Praćenje odnosa između PM2.5 koncentracije i temperature vazduha.

### Dodatno
- AQI - Air Quality Index
- PM - Particulate Matter
