# Strategiasivun pohja

Suomennos englanninkielisestä pohjasta (`docs/head-of-product/strategy-template.md`). Tämä on rakenne ja ohje. Varsinainen sivu kirjoitetaan projektiisi tiedostoon `docs/product/strategy.md` (tai käyttöönoton vaiheessa 1 sovittuun paikkaan) omistajan kielellä. Ohjetekstit (kursiivilla) poistetaan valmiista sivusta.

Kevyt tarkoittaa: yksi sivu, 3–5 panosta, 5–7 päätössääntöä. Sivu kasvaa katselmuksissa sitä mukaa kuin käyttö näyttää tarpeen. Päätössääntöjä kertyy kuukausien käytössä; niitä ei kirjoiteta kerralla.

---

# [Projektin nimi]: strategia

> **Tila: LUONNOS** (vaihdetaan muotoon "LUKITTU YYYY-MM-DD", kun omistaja on hyväksynyt sivun osio osiolta). Muutokset vain omistajan päätöksellä. Head of Product ehdottaa.

## Missio

*Yksi tai kaksi lausetta: mitä projekti tekee ja kenelle. Lainaa omistajaa, jos hän on sanonut sen itse. Kirjoita perään kaksi tai kolme lausetta siitä, mitä missiosta seuraa: mikä on ydin ja mikä tukiominaisuus.*

## Ensisijainen käyttäjä

*Kuka käyttää ja missä tilanteessa. Mistä hän tulee (haku, suositus, suora), millä laitteella, mitä hän haluaa saada aikaan. Jos on pienempi mutta arvokas ryhmä, nimeä se erikseen ja sano, että sille tehtyjä ominaisuuksia punnitaan ryhmän koon mukaan.*

## Liiketoimintamalli (jos olennainen)

*Ilmainen, maksullinen, tulot muualta, tavoite (esimerkiksi myynti tai jatkuva tuotto). Vain se, mikä ohjaa priorisointia. Jos osio sisältää jotain, mitä ei saa käyttää julkisesti, sano se tässä.*

## Diagnoosi: mikä meitä nyt jarruttaa (päivämäärä)

*Tärkein osio. Kirjoita se ennen panoksia. Mikä on se yksi tai kaksi asiaa, jotka nyt estävät projektia etenemästä? Ei tavoitelista, vaan este. Jokaisella väitteellä on lähde (mittari, tiedosto, omistajan sana) tai se on merkitty oletukseksi. Lopuksi kohta "Varmistetaan": mikä diagnoosissa on päätelmää eikä testattua, ja miten se testataan.*

*Esimerkki muodosta: "Kasvua jarruttaa näkyvyyden laatu, ei tekniikka. Sivut toimivat, mutta hakukone jättää osan indeksoimatta (lähde: hakukonetyökalu, päivämäärä). Varmistetaan: syy on päätelmä, testataan karsimalla heikot sivut ja seuraamalla indeksointia 8 viikkoa."*

## Ohjaava linja

*Yksi periaate, joka seuraa diagnoosista ja ohjaa valintoja seuraavat kuukaudet, ja 2–4 asiaa, jotka siitä seuraavat. Jos omistaja on tehnyt tietoisen valinnan, joka ei seuraa diagnoosista, kirjoita se näkyviin ja sano, miksi se tehtiin.*

## Panokset (ajanjakso)

*Panos on rajattu kokonaisuus, johon käytetään aikaa, koska uskotaan sen liikuttavan tavoitetta. Työhön otetaan vain sitä, mikä liikuttaa jotain panosta. 3–5 panosta. Jokaiselle:*

### Panos 1. [nimi]

- **Mittari:** *mistä nähdään, liikkuuko panos. Lähde ja tiheys.*
- **Toimet:** *mitä tänä aikana tehdään.*
- **Lopetusehto:** *tila ja päivämäärä: "jos X ei ole Y:ssä päivään Z mennessä, panos lopetetaan tai arvioidaan uudelleen". Jos ehtoa ei voi vielä asettaa, kirjoita milloin se asetetaan (esimerkiksi ensimmäisen mittauksen jälkeen).*

## Emme tee nyt

*Lista asioista, joita ei tehdä tällä jaksolla, vaikka ne voivat olla hyviä ideoita. Jokaisella kohdalla syy ja ehto, jolloin sitä voi harkita uudelleen. Hyvä idea, joka ei liity mihinkään panokseen, menee ideakoriin odottamaan katselmusta.*

1. *[asia]. [syy]. Uudelleenarvio, kun [ehto].*

## Päätössäännöt

*Näillä säännöillä Head of Product arvioi työn. Aloita näistä seitsemästä, muokkaa projektiin sopiviksi ja poista turhat. Lisää uusia vasta, kun käyttö näyttää tarpeen.*

1. **Jokainen työ liittyy panokseen.** Muuten se menee ideakoriin.
2. **Vaihtoehtoiskustannus.** Kysymys ei ole "kannattaako tämä", vaan "onko tämä paras käyttö seuraavalle työlle".
3. **Päätetty mutta tekemättä.** Hyväksytyt päätökset, joita kukaan ei toteuta, nostetaan esiin joka kerta.
4. **Lopetusehto ennen aloitusta.** Jokaisella panoksella ja kokeilulla on tila ja päivämäärä, jolloin se lopetetaan tai arvioidaan uudelleen.
5. **Kenelle ja kuinka monelle.** Jokaisesta ominaisuudesta kysytään, palveleeko se valtaosaa käyttäjistä vai pientä ryhmää.
6. **Yksinkertaisuus.** Jokaisesta lisäyksestä kysytään: mitä tehtävää se palvelee, mitä se maksaa käyttäjän huomiosta, mitä voisi poistaa sen sijaan ja voiko sen tehdä olemassa olevalla.
7. **Pieni määrä ei ole näyttöä, ja omistaja päättää.** Pienistä luvuista ei tehdä päätöksiä yksinään. "En tiedä" on hyväksyttävä vastaus. Head of Product suosittelee, omistaja päättää, ja hylätty varoitus ei palaa ilman uutta näyttöä.

## Mittarit ja lähtötasot

| Mittari | Mitä se kertoo | Lähde ja tiheys | Lähtötaso (päivämäärä) |
|---|---|---|---|
| *[mittari]* | *[mitä se kertoo]* | *[lähde, tiheys]* | *[luku tai "ei mitattu"]* |

*Kirjaa lopuksi mittauksen rajoitteet: mitä luvut eivät kerro, mistä osa liikenteestä tai käytöstä puuttuu, mitkä luvut ovat liian pieniä päätöksiin.*

## Ylläpito

- Sivu katselmoidaan neljännesvuosittain. Ensimmäinen katselmus: [päivämäärä].
- Lisäksi aina, kun panoksen lopetusehdon päivä menee ohi.
- Sivua muuttaa vain omistaja. Head of Product ehdottaa.

## Mikä muuttui

- *[päivämäärä]: sivu kirjoitettu ja lukittu (päätös [tunnus]).*
