# Strategiasivun pohja

Suomennos englanninkielisestä pohjasta (`docs/head-of-product/strategy-template.md`). Tässä on sivun rakenne ja ohjeet sen täyttämiseen. Varsinainen sivu kirjoitetaan projektiisi tiedostoon `docs/product/strategy.md` (tai käyttöönoton vaiheessa 1 sovittuun paikkaan) omistajan kielellä. Kursiivilla kirjoitetut ohjetekstit poistetaan valmiista sivusta.

Kevyt tarkoittaa tässä yhtä sivua, 3–5 panostusta ja 5–7 päätössääntöä. Sivu kasvaa katselmuksissa sitä mukaa kuin käytössä ilmenee tarvetta. Päätössääntöjä kertyy kuukausien mittaan, eikä niitä kirjoiteta kaikkia kerralla.

---

# [Projektin nimi]: strategia

> **Tila: LUONNOS** (muutetaan muotoon "LUKITTU YYYY-MM-DD", kun omistaja on hyväksynyt sivun osio kerrallaan). Sivua muutetaan vain omistajan päätöksellä. Head of Product tekee ehdotukset.

## Missio

*Yksi tai kaksi lausetta: mitä projekti tekee ja kenelle. Lainaa omistajaa, jos hän on itse muotoillut sen. Lisää perään kaksi tai kolme lausetta siitä, mitä missiosta seuraa: mikä on ydintä ja mikä tukee sitä.*

## Ensisijainen käyttäjä

*Kuka tuotetta käyttää ja missä tilanteessa. Mistä hän tulee (haku, suositus, suora käynti), millä laitteella ja mitä hän haluaa saada aikaan. Jos on pienempi mutta arvokas käyttäjäryhmä, nimeä se erikseen ja totea, että sille tehtyjä ominaisuuksia punnitaan ryhmän koon mukaan.*

## Liiketoimintamalli (jos olennainen)

*Ilmainen, maksullinen tai tulot muualta, ja mikä on tavoite (esimerkiksi myynti tai jatkuva tulo). Kirjaa vain se, mikä vaikuttaa priorisointiin. Jos osiossa on jotain, mitä ei saa käyttää julkisesti, mainitse se tässä.*

## Diagnoosi: mikä meitä nyt jarruttaa (päivämäärä)

*Tärkein osio. Kirjoita se ennen panostuksia. Mitkä yksi tai kaksi asiaa estävät nyt projektia etenemästä? Kirjaa este, älä tavoitteita. Jokaiselle väitteelle on lähde (mittari, tiedosto tai omistajan sana), tai se on merkitty oletukseksi. Lopeta kohtaan "Varmistetaan": mikä diagnoosissa on päätelmää eikä testattua tietoa ja miten se testataan.*

*Esimerkki muodosta: "Kasvua jarruttaa näkyvyyden laatu, ei tekniikka. Sivut toimivat, mutta hakukone jättää osan niistä indeksoimatta (lähde: hakukonetyökalu, päivämäärä). Varmistetaan: syy on päätelmä, ja se testataan karsimalla heikot sivut ja seuraamalla indeksointia kahdeksan viikon ajan."*

## Ohjaava linja

*Yksi periaate, joka seuraa diagnoosista ja ohjaa valintoja seuraavien kuukausien ajan, sekä 2–4 asiaa, jotka siitä seuraavat. Jos omistaja on tehnyt tietoisen valinnan, joka ei seuraa diagnoosista, kirjoita se näkyviin ja perustele, miksi se tehtiin.*

## Panostukset (ajanjakso)

*Panostus on rajattu kokonaisuus, johon käytetään aikaa, koska sen uskotaan vievän tavoitetta eteenpäin. Työn alle otetaan vain sellaista, mikä vie jotain panostusta eteenpäin. Panostuksia on 3–5, ja jokaisesta kirjataan:*

### Panostus 1. [nimi]

- **Mittari:** *mistä nähdään, eteneekö panostus. Lähde ja seurantatiheys.*
- **Toimet:** *mitä tällä jaksolla tehdään.*
- **Lopetusehto:** *tila ja päivämäärä: "jos X ei ole päivään Z mennessä tasolla Y, panostus lopetetaan tai arvioidaan uudelleen". Jos ehtoa ei voi vielä asettaa, kirjoita, milloin se asetetaan (esimerkiksi ensimmäisen mittauksen jälkeen).*

## Emme tee nyt

*Asiat, joita ei tehdä tällä jaksolla, vaikka ne voivat olla hyviä ideoita. Jokaiselle kirjataan syy ja ehto, jonka täyttyessä asiaa voi harkita uudelleen. Hyvä idea, joka ei liity mihinkään panostukseen, siirretään ideakoriin odottamaan katselmusta.*

1. *[asia]. [syy]. Arvioidaan uudelleen, kun [ehto].*

## Päätössäännöt

*Näiden sääntöjen avulla Head of Product arvioi työtä. Aloita näistä seitsemästä, muokkaa ne projektiin sopiviksi ja poista tarpeettomat. Lisää uusia vasta, kun käytössä ilmenee tarvetta.*

1. **Jokainen työ liittyy panostukseen.** Muuten se siirretään ideakoriin.
2. **Vaihtoehtoiskustannus.** Kysymys ei ole, kannattaako tämä tehdä, vaan onko tämä paras mahdollinen seuraava työ.
3. **Päätetty mutta tekemättä.** Hyväksytyt päätökset, joita kukaan ei toteuta, nostetaan esiin joka kerta.
4. **Lopetusehto ennen aloitusta.** Jokaisella panostuksella ja kokeilulla on tila ja päivämäärä, jolloin se lopetetaan tai arvioidaan uudelleen.
5. **Kenelle ja kuinka monelle.** Jokaisesta ominaisuudesta kysytään, palveleeko se valtaosaa käyttäjistä vai pientä ryhmää.
6. **Yksinkertaisuus.** Jokaisesta lisäyksestä kysytään: mitä tehtävää se palvelee, paljonko se vie käyttäjän huomiota, mitä voisi poistaa sen sijaan ja voiko asian hoitaa jo olemassa olevalla.
7. **Pieni määrä ei ole näyttöä, ja omistaja päättää.** Pelkkien pienten lukujen varaan ei tehdä päätöksiä. "En tiedä" on hyväksyttävä vastaus. Head of Product suosittelee ja omistaja päättää, eikä hylätty huomautus palaa ilman uutta näyttöä.

## Mittarit ja lähtötasot

| Mittari | Mitä se kertoo | Lähde ja seurantatiheys | Lähtötaso (päivämäärä) |
|---|---|---|---|
| *[mittari]* | *[mitä se kertoo]* | *[lähde, tiheys]* | *[luku tai "ei mitattu"]* |

*Kirjaa lopuksi mittaamisen rajoitukset: mitä luvut eivät kerro, mistä osa liikenteestä tai käytöstä puuttuu ja mitkä luvut ovat liian pieniä päätösten pohjaksi.*

## Ylläpito

- Sivu katselmoidaan neljännesvuosittain. Ensimmäinen katselmus: [päivämäärä].
- Lisäksi sivu katselmoidaan aina, kun jonkin panostuksen lopetusehdon päivämäärä menee ohi.
- Vain omistaja muuttaa sivua. Head of Product tekee ehdotukset.

## Mikä muuttui

- *[päivämäärä]: sivu kirjoitettu ja lukittu (päätös [tunnus]).*
