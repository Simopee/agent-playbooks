# Pohja: mitä käyttäjistä tiedetään ja mitä oletetaan

Suomennos englanninkielisestä pohjasta (`docs/head-of-product/users-template.md`). Varsinainen tiedosto tulee projektiisi polkuun `docs/product/users-known-vs-assumed.md` (tai käyttöönoton vaiheessa 1 sovittuun paikkaan) omistajan kielellä. Head of Product ehdottaa sisällön, pääistunto kirjoittaa sen (agentilla ei ole kirjoitusoikeutta), omistaja hyväksyy.

Lähteet vahvimmasta heikoimpaan: oikeat käyttötestit ja palaute; käyttäytymisdata (analytiikka); hakukysyntä (hakukonetyökalut); simuloidut persoonat (mittaavat vain ymmärrettävyyttä, eivät kysyntää). Agentti ei voi haastatella ihmisiä eikä arvioida, tuntuuko käyttöliittymä hyvältä.

---

# Mitä käyttäjistä tiedetään (päivitetty YYYY-MM-DD)

## Tiedämme

| Väite | Lähde | Päivämäärä |
|---|---|---|
| *[esimerkki: valtaosa käytöstä tapahtuu puhelimella]* | *[analytiikka, jakso]* | |

## Oletamme

| Oletus | Miksi uskomme sen | Miten testataan | Mikä panos riippuu siitä |
|---|---|---|---|
| *[esimerkki: käyttäjät haluavat X:n]* | *[peruste]* | *[testi: käyttötesti, mittari, pieni kokeilu]* | |

## Testattu ja kumottu

| Oletus | Mitä testi näytti | Päivämäärä |
|---|---|---|

## Käyttötesti

Neljännesvuosittain viiden ihmisen käyttötesti, jos projektissa on käyttöliittymä. Testaajat eivät tunne palvelua. Tehtävät ovat käyttäjän perustehtäviä ilman käyttöliittymän sanastoa. Kirjataan, onnistuiko tehtävä, kauanko se kesti ja missä testaaja epäröi. Head of Product kirjoittaa tehtävät, omistaja järjestää testaajat, agentti analysoi tulokset. Viisi ihmistä löytää selvät ongelmat, mutta ei mittaa osuuksia.
