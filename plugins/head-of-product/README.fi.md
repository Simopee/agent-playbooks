[In English](README.md)

# Head of Product

Kun tekoälyagentit tekevät rakentamisesta halpaa, vaikein kysymys on, mitä rakennetaan. Tämä agentti kysyy sen jokaisessa suunnittelukohdassa, kirjoittamaasi strategiaa vasten.

## Asennus

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Aja sitten projektissasi `/head-of-product:setup`.

**Ilman asennusta:** liitä `https://github.com/Simopee/agent-playbooks` Claude Codeen projektissasi ja kysy, auttaisiko tämä projektiasi.

## Mitä se tekee

Paketti tuo projektiisi Head of Product -agentin ja ohjatun käyttöönoton. Käyttöönotossa kirjoitetaan kanssasi yhden sivun strategia: missio, ensisijainen käyttäjä, diagnoosi siitä, mikä projektia jarruttaa, 3–5 panosta mittareineen ja lopetusehtoineen, "Emme tee nyt" -lista ja päätössäännöt. Sen jälkeen agentti arvioi ehdotetun työn sitä sivua vasten niissä kohdissa, joissa valitset, mitä tehdään seuraavaksi. Se suosittelee, mitä pidetään, siirretään tai karsitaan, ja miksi. Sinä päätät jokaisesta varoituksesta.

## Miten se toimii

**Käyttöönotto** (`/head-of-product:setup`, kuusi vaihetta, pysähtyy jokaisen jälkeen odottamaan hyväksyntääsi):

1. **Kartoitus.** Claude lukee repositoriosi, kirjaa, mitkä strategian osat jo löytyvät, ja selvittää työrytmisi (sprintit vai ei, missä päätät). Sitten se kysyy aukoista, kysymys kerrallaan.
2. **Strategialuonnos.** Agentti kirjoittaa luonnoksen pohjan mukaan. Jokaisella väitteellä on lähde tai se on merkitty oletukseksi; tuntemattomat lähtötasot ovat "ei mitattu". Se kirjoittaa myös sivun siitä, mitä käyttäjistä tiedetään ja mitä vain oletetaan.
3. **Läpikäynti ja lukitus.** Käytte luonnoksen läpi osio kerrallaan. Kun kaikki on hyväksytty, sivu LUKITAAN päivämäärän kanssa.
4. **Räätälöinti.** Claude kopioi agentin projektiisi (`.claude/agents/head-of-product.md`) ja täyttää `[FILL IN: ...]`-kohdat.
5. **Kytkentä.** Claude lisää agentin päätöskohtiisi: portti ennen kuin valitset kierroksen sisällön, retro lopussa, idean arviointi ennen rakentamista, neljännesvuosittainen strategiakatselmus. Tekstilohkot on sekä sprinteille että työlle ilman sprinttejä.
6. **Koejakso.** Kolme kierrosta, kolme kyllä/ei-kysymystä jokaisen jälkeen. Sitten päätät: jatketaan, muutetaan vai lopetetaan.

**Syötteet:** repositoriosi ja vastauksesi. **Tulokset:** `docs/product/strategy.md`, `docs/product/users-known-vs-assumed.md` (sinun kielelläsi), räätälöity agentti ja muutama rivi projektisi ohjeisiin.

**Miten agentti toimii:** se kirjoittaa ensin omat prioriteettinsa strategiasta, ennen kuin lukee ehdotuksen, ja listaa sitten erot. Tämä vastustaa kielimallien taipumusta myötäillä sitä suunnitelmaa, joka niille näytetään. Sen on nimettävä vähintään yksi karsittava tai siirrettävä asia, tai perusteltava, miksi mitään ei karsita. Se erottaa todisteet oletuksista ja pitää kantansa, ellei se saa uutta näyttöä. Sillä ei ole kirjoitusoikeutta.

**Vastausmuoto** (enintään noin 700 sanaa): itsenäiset prioriteetit, erot ehdotukseen, karsinta- ja siirtolista, Leverage-työn osuus, vahvin yksittäinen vastaväite, todisteet ja varmuus, enintään kolme kysymystä sinulle. Agentti kirjoittaa englanniksi; pääistunto kääntää yhteenvedon sinulle.

## Esimerkki

Tiedostosta [examples/head-of-product/sample-gate-result.md](../../examples/head-of-product/sample-gate-result.md) (keksitty projekti, englanniksi):

> **Strongest single objection.** The round polishes the product for readers while the diagnosis says readers leave because contents are stale. Nothing in it would change what a returning reader sees.

Katso myös [esimerkkistrategia](../../examples/head-of-product/sample-strategy.md).

## Sovittaminen omaan projektiin

Käyttöönotto tekee sovittamisen kanssasi. Jos muokkaat käsin, täytettävät kohdat on merkitty `[FILL IN: ...]` tiedostossa `agents/head-of-product.md`: projektin kuvaus, ankkuritiedostot, kuka päättää järjestyksestä ja kapasiteetista, kasvun suunnat, pääsy dataan ja sen rajat, päätöskohdat sekä lista asioista, joista agentti ei autonomisessa tilassa koskaan päätä. Säilytä työtapa; taustamuistio kertoo miksi.

Ohjeet suomeksi: [kytkennät](../../docs/fi/head-of-product/kytkennat.md), [strategiasivun pohja](../../docs/fi/head-of-product/strategia-pohja.md), [käyttäjäpohja](../../docs/fi/head-of-product/kayttajista-tiedetaan-pohja.md), [tausta ja tutkimus](../../docs/fi/head-of-product/tausta.md).

## Rajat ja tarkistus ennen käyttöä

- Nämä ovat auditoimattomia kehotteita, jotka tarjotaan sellaisenaan. Lue ne ennen käyttöä ja tarkista, mitä käyttöönotto kirjoittaa projektiisi.
- Agentti ei voi haastatella käyttäjiä eikä arvioida, miltä käyttöliittymä tuntuu. Pienessä mittakaavassa sen luvut kertovat vain suunnan.
- Se on tehty ajettavaksi harvoin, päätöskohdissa. Tiketeittäin ajettuna se kuluttaa tokeneita ja lisää melua.

## Lisenssi ja tekijä

MIT. Tehnyt Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
