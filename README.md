# H4
### Tehtävänanto  
1. Tarkastele käytössäsi olevia RFID tuotteita, mieti miten hyvin olet suojautunut RFID urkinnalta?
2. Tutustu APDU komentojen rakenteeseen (voit käyttää tekoälyä tutustumiseen)
3. Tutki ja kerro minkä mielenkiintoisen RFID hakkerointi uutiset löysit. (Vinkki, useimmat liittyvät henkilökortteihin)
   

### 1) Tarkastele käytössäsi olevia RFID tuotteita, mieti miten hyvin olet suojautunut RFID urkinnalta?
-Pankkikortti
    - Pankkikortti nahkalompakossa, joka ei ole RFID-suojattu
    - Joku voisi käytännössä veloittaa luvatta lähimaksulla: epätodennäköistä, sillä uskon siitä jäävän kiinni helpolla
-Henkilökortti
    - Henkilökortti myös lompakossa suojaamattomana
    - Henkilötietojen lukeminen luvatta
-iLOQ S5-avain
    - Ei voi kopioida 
    - Väärinkäytökset helposti jäljitettävissä
      (iLOQ s.a)

      
### 2) APDU
- on viestimuoto, jota käytetään älykortin (esimerkiksi RFID-kortti) ja lukijan välisessä viestinnässä
- APDU-komennon rakenne: | CLA | INS | P1 | P2 | Lc | Data | Le |
    - CLA-kenttä on komennon luokka. kertoo älykortille miten koko viesti tulee tulkita.
    - INS-kenttä (Instruction byte): kertoo mitä käsky tekee. Esimerkiksi lue, valitse, kirjoita, tarkista PIN
    - P1- ja P2-kentät: Komennon parametrit. Esimerkiksi tiedoston kohta, johon data kirjoitetaan
    - Lc-kenttä: Ilmaisee datan pituuden. Ilmenee vain kun lähetetään älykortille komento, jossa on dataa. Esimerkiksi kortille kirjoittaessa.
    - Data-kenttä: Ilmenee vain silloin kun lähetetään dataa. Sisältää itse datan.
    - Le: Käytetään kun halutaan lukea jotain kortilta. Kertoo kuinka monta tavua dataa odotetaan kortilta vastauksena.

    
### 3) RFID-hakkerointiuutinen
Uutinen luettavissa: ["Hardware Backdoor Discovered in RFID Cards Used in Hotels and Offices Worldwide"](https://thehackernews.com/2024/08/hardware-backdoor-discovered-in-rfid.html)

uutisessa kerrotaan, että FM11RF08S-nimisessä RFID-Korttimallisa, joka on MIFARE Classic -variantti on laitteistotason takaportti.  
Takaportti mahdollistaa, että kortin voi avata ja kloonata ilman oikeaa avainta eikä edes suojaus auta, sillä takaportti ohittaa suojauksen.  
Kyseisiä kortteja käytetään hotelleiden- ja toimistojen ovissa sekä julkisessa liikenteessä. Kortteja on käytössä miljoonia ympäri maailmaa. 

### Lähteet  
The Hacker News 2024. Hardware Backdoor Discovered in RFID Cards Used in Hotels and Offices Worldwide.  
Luettavissa: https://thehackernews.com/2024/08/hardware-backdoor-discovered-in-rfid.html.  
Luettu: 22.04.2025.  

iLOQ s.a. Hyödyt. Luettavissa: https://www.iloq.com/fi/hyodyt/.  
Luettu 22.04.2025.
