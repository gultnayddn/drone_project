# Emergency Drone Coordination System - Teknik Rapor

## Giris

Bu proje, bir afet senaryosu sonrasi hayatta kalanlari tespit etmek ve koordineli sekilde kurtarmak amaciyla gelistirilmistir. C dili kullanilarak gelistirilen bu sistem, coklu is parcacigi, soket haberlesmesi ve yapay zeka modulu icerir.

## Amac

Birden fazla dronenin merkezi bir sunucu tarafindan koordine edilerek otonom kurtarma islemi yapmasi saglanir. Sistem; gorev dagitimi, konum takibi ve gorsellestirme bileşenlerini icerir.

---

## Sistem Mimarisi

- **Sunucu**: Dronelari ve hayatta kalanlari yonetir, gorevleri dagitir.
- **Istemci**: Her drone bir istemci olarak calisir ve komutlara gore hareket eder.
- **Yapay Zeka**: Hedef secimi ve yon hesaplamasi yapar.
- **Hayatta Kalanlar**: Harita uzerinde rastgele hareket eder.
- **Harita & Gorsellestirme**: Tum pozisyonlar izlenebilir.

---

## Teknik Bilesenler

- **Programlama Dili**: C
- **Threading**: pthread kutuphanesi
- **Haberlesme**: TCP soketleri
- **Veri Yapilari**: Bagli liste, kuyruk, mutex korumali yapilar
- **Derleme**: Makefile

---

## Proje Dosya Yapisi

| Dosya / Klasor         | Aciklama                         |
|------------------------|----------------------------------|
| `client/`              | Drone istemci kodlari            |
| `server/`              | Merkezi sunucu kodlari           |
| `ai.c / ai.h`          | Yapay zeka algoritmalari         |
| `map.c / map.h`        | Harita islemleri                 |
| `survivor.c / survivor.h` | Hayatta kalan simulasyonu    |
| `view.c / view.h`      | Gorsellestirme kodlari           |
| `Makefile`             | Derleme betigi                   |

---

## Ornek Senaryo

1. Sunucu (`server`) baslatilir.
2. Harita ve hayatta kalanlar tanimlanir.
3. Birden fazla istemci (`client`) baslatilir.
4. Dronelar sunucuya baglanir ve konum bilgisi alir.
5. Her biri en yakin hayatta kalana yonelir.
6. Surec terminal uzerinden izlenebilir.

---

## Sonuc

Bu proje, sistem programlama, soket haberlesmesi ve yapay zeka algoritmalarini bir araya getirerek bir kurtarma sistemini basariyla simule eder.

---

## Gelecek Gelistirmeler

- Grafik arayuz eklenmesi
- Gercek drone donanimi ile baglanti
- Gelismis rota planlama algoritmalari
- Engel algilama ve kacma destegi

---

