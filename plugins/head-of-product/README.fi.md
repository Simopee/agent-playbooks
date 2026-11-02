[In English](README.md)

# Head of Product

Kun tekoälyagenttien ansiosta rakentaminen on halpaa, vaikein kysymys on, mitä kannattaa rakentaa. Tämä agentti kysyy sitä jokaisessa suunnittelukohdassa ja hakee vastauksen kirjoittamastasi strategiasta.

## Kenelle

- Rakennat tuotetta tekoälyagenttien kanssa Claude Codessa yksin tai pienen tiimin kanssa, ja agentit toteuttavat melkein mitä tahansa pyydät.
- Työlista kasvaa nopeammin kuin ehdit arvioida sitä. Korjaukset, viimeistely, uudet ideat ja ominaisuudet, joita kukaan ei pyytänyt, näyttävät kaikki yhtä kiireellisiltä.
- Sinulla on tavoitteita, mutta ne ovat päässäsi tai hajallaan muistiinpanoissa eivätkä yhdellä sivulla, johon työtä voisi verrata.
- Suunnittelet työn kierroksina (sprintteinä tai ilman) ja haluat toisen mielipiteen juuri silloin, kun valitset, mitä kierrokselle otetaan.

## Mitä hyötyä siitä on

- **Suunnitelma tarkistetaan tavoitteitasi vasten joka kierroksella.** Ennen kuin lyöt kierroksen lukkoon, agentti kertoo, mitkä työt vievät tavoitetta eteenpäin, mitkä vain tuntuvat tuottavilta ja mitä kannattaa jättää pois tai siirtää myöhemmäksi.
- **Saat samalla kirjoitetun strategian.** Käyttöönotto kokoaa tietosi yhdelle sivulle: kenelle tuote on, mikä sitä jarruttaa, 3–5 panostusta mittareineen ja Emme tee nyt -lista.
- **Se ei vain myötäile.** Agentti muodostaa omat prioriteettinsa ennen kuin lukee suunnitelmasi. Sen on aina nimettävä jotain karsittavaa, ja se muuttaa kantaansa vain uuden näytön perusteella.
- **Päätösvalta pysyy sinulla.** Agentti suosittelee, ja sinä päätät jokaisesta sen huomautuksesta. Sillä ei ole kirjoitusoikeutta.
- **Se sopii omaan tapaasi tehdä töitä.** Agentti arvioi ehdotuksen, tulipa se sinulta tai toiselta agentilta. Se toimii sprinttien kanssa ja ilman niitä.

## Milloin siitä ei ole hyötyä

- Tuotepäätöksiä ei vielä ole tehtävänä, tai yksi ihminen pystyy pitämään koko suunnitelman päässään vaivatta.
- Haluat agentin, joka kirjoittaa koodia tai tikettejä. Tämä agentti arvioi vain, mikä kannattaa tehdä.

## Asennus

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Aja sitten projektissasi `/head-of-product:setup`.

**Ilman asennusta:** liitä `https://github.com/Simopee/agent-playbooks` projektisi Claude Codeen ja kysy, olisiko tästä hyötyä projektillesi.

## Mitä paketti sisältää

Paketti tuo projektiisi Head of Product -agentin ja ohjatun käyttöönoton. Käyttöönotossa kirjoitetaan kanssasi yhden sivun strategia: missio, ensisijainen käyttäjä, diagnoosi siitä, mikä projektia jarruttaa, 3–5 panostusta mittareineen ja lopetusehtoineen, Emme tee nyt -lista ja päätössäännöt. Sen jälkeen agentti arvioi ehdotettua työtä tämän sivun pohjalta niissä kohdissa, joissa valitset, mitä tehdään seuraavaksi. Se suosittelee, mitä pidetään, mitä siirretään ja mitä karsitaan, ja perustelee suosituksensa. Sinä päätät jokaisesta huomautuksesta.

## Miten se toimii

**Käyttöönotto** (`/head-of-product:setup`) etenee kuudessa vaiheessa, ja jokaisen vaiheen jälkeen se odottaa hyväksyntääsi:

1. **Kartoitus.** Claude lukee repositoriosi, kirjaa, mitkä strategian osat ovat jo olemassa, ja selvittää työrytmisi (käytätkö sprinttejä ja missä kohdassa päätät). Sitten se kysyy puuttuvista tiedoista kysymys kerrallaan.
2. **Strategialuonnos.** Agentti kirjoittaa luonnoksen pohjan mukaan. Jokaiselle väitteelle on lähde, tai se on merkitty oletukseksi. Tuntemattomat lähtötasot merkitään "ei mitattu". Agentti kirjoittaa myös sivun siitä, mitä käyttäjistä tiedetään ja mitä vain oletetaan.
3. **Läpikäynti ja lukitus.** Käytte luonnoksen läpi osio kerrallaan. Kun kaikki osiot on hyväksytty, sivu LUKITAAN ja siihen merkitään päivämäärä.
4. **Sovitus.** Claude kopioi agentin projektiisi (`.claude/agents/head-of-product.md`) ja täyttää `[FILL IN: ...]`-kohdat.
5. **Kytkentä.** Claude liittää agentin päätöskohtiisi: tarkistus ennen kuin valitset kierroksen sisällön, retro kierroksen lopussa, idean arviointi ennen rakentamista ja strategian katselmus neljännesvuosittain. Valmiit tekstilohkot löytyvät sekä sprinteille että sprintittömälle työlle.
6. **Koejakso.** Kolme kierrosta ja jokaisen jälkeen kolme kyllä vai ei -kysymystä. Sen jälkeen päätät, jatketaanko, muutetaanko vai lopetetaanko.

**Lähtötiedot:** repositoriosi ja vastauksesi. **Lopputulos:** `docs/product/strategy.md`, `docs/product/users-known-vs-assumed.md` (omalla kielelläsi), projektiisi sovitettu agentti ja muutama rivi projektisi ohjeisiin.

**Miten agentti toimii:** agentti kirjoittaa strategian pohjalta ensin omat prioriteettinsa, vasta sitten se lukee ehdotuksen ja listaa erot. Näin se vastustaa kielimallien taipumusta myötäillä suunnitelmaa, joka niille näytetään. Sen on nimettävä vähintään yksi asia, joka karsitaan tai siirretään, tai perusteltava, miksi mitään ei tarvitse karsia. Se erottaa näytön oletuksista ja pysyy kannassaan, ellei se saa uutta näyttöä. Sillä ei ole kirjoitusoikeutta.

**Vastauksen rakenne** (enintään noin 700 sanaa): omat prioriteetit, erot ehdotukseen, karsittavat ja siirrettävät työt, Leverage-työn osuus, vahvin yksittäinen vastaväite, näyttö ja varmuusaste sekä enintään kolme kysymystä sinulle. Agentti kirjoittaa englanniksi, ja pääistunto kääntää yhteenvedon sinulle.

## Esimerkki

Tiedostosta [examples/head-of-product/sample-gate-result.md](../../examples/head-of-product/sample-gate-result.md) (keksitty projekti, englanniksi):

> **Strongest single objection.** The round polishes the product for readers while the diagnosis says readers leave because contents are stale. Nothing in it would change what a returning reader sees.

Katso myös [esimerkkistrategia](../../examples/head-of-product/sample-strategy.md).

## Sovittaminen omaan projektiin

Käyttöönotto sovittaa agentin projektiisi yhdessä kanssasi. Jos muokkaat sitä itse, täytettävät kohdat on merkitty `[FILL IN: ...]` tiedostossa `agents/head-of-product.md`: projektin kuvaus, ankkuritiedostot, kuka päättää järjestyksestä ja kapasiteetista, kasvusuunnat, pääsy dataan ja sen rajat, päätöskohdat sekä luettelo asioista, joista agentti ei koskaan päätä autonomisessa tilassa. Älä muuta työtapaa. Taustamuistio kertoo, miksi.

Ohjeet suomeksi: [kytkeminen työrytmiin](../../docs/fi/head-of-product/kytkennat.md), [strategiasivun pohja](../../docs/fi/head-of-product/strategia-pohja.md), [käyttäjäpohja](../../docs/fi/head-of-product/kayttajista-tiedetaan-pohja.md), [tausta ja tutkimus](../../docs/fi/head-of-product/tausta.md).

## Rajoitukset ja tarkistus ennen käyttöä

- Nämä ovat auditoimattomia promptteja, ja ne tarjotaan sellaisinaan. Lue ne ennen käyttöä ja tarkista, mitä käyttöönotto kirjoittaa projektiisi.
- Agentti ei voi haastatella käyttäjiä eikä arvioida, miltä käyttöliittymä tuntuu. Pienessä mittakaavassa sen luvut kertovat vain suunnan.
- Agentti on tarkoitettu ajettavaksi harvoin, päätöskohdissa. Jos sitä ajetaan joka tiketin kohdalla, se kuluttaa tokeneita ja tuottaa lähinnä melua.

## Lisenssi ja tekijä

MIT. Tekijä Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
