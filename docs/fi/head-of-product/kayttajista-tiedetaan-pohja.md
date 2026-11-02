# Pohja: mitä käyttäjistä tiedetään ja mitä oletetaan

Suomennos englanninkielisestä pohjasta (`docs/head-of-product/users-template.md`). Varsinainen tiedosto tallennetaan projektiisi polkuun `docs/product/users-known-vs-assumed.md` (tai käyttöönoton vaiheessa 1 sovittuun paikkaan) omistajan kielellä. Head of Product ehdottaa sisällön, pääistunto kirjoittaa sen (agentilla ei ole kirjoitusoikeutta) ja omistaja hyväksyy sen.

Lähteet vahvimmasta heikoimpaan: oikeat käyttäjätestit ja palaute, käyttäytymisdata (analytiikka), hakukysyntä (hakukoneiden työkalut) ja simuloidut persoonat (ne mittaavat vain ymmärrettävyyttä, eivät koskaan kysyntää). Agentti ei voi haastatella ihmisiä eikä arvioida, onko käyttöliittymää mukava käyttää.

---

# Mitä käyttäjistä tiedetään (päivitetty YYYY-MM-DD)

## Tiedämme

| Väite | Lähde | Päivämäärä |
|---|---|---|
| *[esimerkki: valtaosa käytöstä tapahtuu puhelimella]* | *[analytiikka, ajanjakso]* | |

## Oletamme

| Oletus | Miksi uskomme siihen | Miten se testataan | Mikä panostus riippuu siitä |
|---|---|---|---|
| *[esimerkki: käyttäjät haluavat X:n]* | *[peruste]* | *[testi: käytettävyystesti, mittari, pieni kokeilu]* | |

## Testattu ja kumottu

| Oletus | Mitä testi osoitti | Päivämäärä |
|---|---|---|

## Käytettävyystesti

Jos projektissa on käyttöliittymä, tehdään kerran neljännesvuodessa käytettävyystesti viidellä ihmisellä. Testaajat eivät tunne palvelua entuudestaan. Tehtävät ovat käyttäjän perustehtäviä, ja ne muotoillaan käyttämättä käyttöliittymän omia termejä. Jokaisesta tehtävästä kirjataan, onnistuiko se, kauanko siihen meni ja missä kohdassa testaaja epäröi. Head of Product kirjoittaa tehtävät, omistaja hankkii testaajat ja agentti analysoi tulokset. Viisi testaajaa löytää selvät ongelmat, mutta osuuksia ei viidellä testaajalla voi mitata.
