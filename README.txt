# Perhekalenteri – staattinen versio (ei Node.js)
Tämä kansio sisältää yhden `index.html`-tiedoston. Avaa se kaksoisklikkaamalla – kalenteri toimii heti.

## Ominaisuudet
- Lista näyttää noin kuukauden eteenpäin (+ 2 päivää taakse), selaus nuolilla menneeseen/tulevaan
- Kuukausinäkymä, kuukauden vaihto nuolilla tai `month`-valinnasta
- "Lisää merkintä" -lomake: Nimi, Päivämäärä, Toistettavuus (kertaluontainen / viikoittain / kuukausittain / aikaväli), Merkintä
- Nimen mukaan värikoodaus
- Klikkaamalla merkintää aukeaa dialogi lisätiedoille
- Tallennus selaimen localStorageen (ei häviä sivun päivityksessä)

## Julkaisu nettiin
Koska tämä on täysin staattinen sivu, voit julkaista pelkän `index.html`-tiedoston esimerkiksi:
- GitHub Pages (lataa/talleta reponsitorioon suoraan)
- minkä tahansa web-hotellin `public_html`-kansioon
- intranet-palvelimelle

Mitään asennuksia ei tarvita palvelimelle: selain riittää.
