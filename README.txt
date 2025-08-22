# Perhekalenteri – Firestore (reaaliaikainen)
Tämä versio synkkaa perheen kalenterin Firebase Firestoreen. Ei vaadi asennuksia koneelle.

## Käyttöönotto (kertaluonteinen)
1) Mene https://console.firebase.google.com → "Add project" → nimeä projekti → luo.
2) Lisää Web-sovellus (Project settings → Your apps → "</>" Add app). Älä ota Firebase Hostingia, jos et halua.
3) Kopioi **Firebase config** (apiKey, authDomain, projectId, ...). Liitä se `index.html`-tiedostossa kohtaan:
   ```js
   const firebaseConfig = { ... };
   ```
4) Ota Firestore käyttöön: Build → Firestore Database → Create database → (valitse sijainti, esim. europe-west).
5) Ota Authentication käyttöön: Build → Authentication → Sign-in method → **Anonymous** ON.
6) Aseta Firestore-säännöt (Rules) muotoon (tämän kansion `firestore.rules`-tiedosto):
   - vaatii kirjautumisen (myös anonyymin), jotta tietokanta ei ole julkinen
   - julkaise rulesit konsolista

## Käyttö
- Avaa `index.html` (esim. GitHub Pagesista tai suoraan tiedostona). Selain lataa SDK:t CDN:stä.
- Sovellus kirjautuu **anonyymisti** → voi lukea/kirjoittaa `events`-kokoelmaan.
- Kaikki laitteet, joissa on sama `firebaseConfig`, näkevät muutokset **reaaliajassa**.

## Huomioita
- `apiKey` Firebase-konfigissa ei ole salainen (se vain tunnistaa projektisi). Turvallisuus hoidetaan **Firestore-säännöillä**.
- Yrityksen verkko voi estää `gstatic.com`-domainin. Jos näin on, kysy IT:ltä sallittavaksi, tai käytä kotiverkkoa.
