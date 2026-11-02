[In English](README.md)

# agent-playbooks

Tekoälyagentit rakentavat sen, mitä niiltä pyydät. Nämä paketit tuovat mukaan roolit, jotka arvioivat, kannattiko sitä rakentaa.

Agentteja, skillejä ja toimintaohjeita tuotekehitykseen tekoälyagenttien kanssa Claude Codessa, englanniksi ja suomeksi. Jokainen paketti on Claude Code -plugin, jonka voi asentaa ja ottaa käyttöön ohjatusti. Jokaisen paketin voi myös lukea täältä sen omalta sivulta.

## Kenelle

Niille, jotka rakentavat tuotteita agenttitiimin kanssa Claude Codessa: perustajille, tuoteomistajille ja pienille tiimeille, jotka voivat nyt rakentaa melkein mitä tahansa ja kaipaavat apua siihen, mitä kannattaa rakentaa. Paketteja voi käyttää ilman koodaustaustaa, sillä käyttöönotto kysyy asiat selkokielellä.

## Asennus

Aja Claude Codessa:

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Aloita sitten käyttöönotto komennolla `/head-of-product:setup`.

**Ilman asennusta:** liitä linkki `https://github.com/Simopee/agent-playbooks` projektisi Claude Codeen ja kysy, olisiko tästä hyötyä projektillesi. Claude osaa lukea tiedostot ja käydä käyttöönoton kanssasi läpi ilman asennusta.

## Sisältö

| Paketti | Mihin se on tarkoitettu | Ohjeet |
|---|---|---|
| [head-of-product](plugins/head-of-product/) | Head of Product -agentti, joka arvioi tuotetyötäsi kirjoitetun strategian pohjalta, sekä ohjattu käyttöönotto, jossa strategia kirjoitetaan yhdessä kanssasi. | [English](plugins/head-of-product/README.md), [suomeksi](plugins/head-of-product/README.fi.md) |

## Miten paketit toimivat

Paketissa on yleensä nämä osat:

- **Agentti** (`agents/`): rooli, jolla on vakiintunut työtapa ja vakiomuotoinen vastaus. Agentti lukee projektisi ja antaa suosituksen, ja sinä päätät.
- **Käyttöönottoskilli** (`skills/setup/`): vaiheittainen ohje, jonka Claude käy läpi projektissasi. Jokaisen vaiheen jälkeen se odottaa hyväksyntääsi, ja lopuksi agentti on sovitettu projektiisi. Sovitettavat kohdat on merkitty `[FILL IN: ...]`.
- **Ohjeet ja esimerkit** (`docs/`, `examples/`): pohjat, taustatutkimus ja valmiiksi täytetty esimerkki, joista näet lopputuloksen jo ennen aloittamista. Suomennokset ovat kansiossa `docs/fi/`.

Paketti voi olla myös pelkkä skilli tai toimintaohje ilman agenttia. Paketit toimivat missä tahansa Claude Code -projektissa, eivätkä ne tarvitse muita järjestelmiä tai ulkoisia palveluita.

## Tulossa

- **Suunnitteilla:** lisää agenttipohjaisen tuotetiimin rooleja, skillejä ja toimintaohjeita (esimerkiksi järjestelmäanalyytikko, laadunvarmistus ja niitä yhdistävät rutiinit), paketti kerrallaan. Jokainen uusi paketti saa oman kansion ja oman sivun, ja ne asennetaan samalla tavalla.

## Tarkista ennen käyttöä

Nämä ovat promptteja ja ohjeita, eivät auditoitua ohjelmistoa, ja ne tarjotaan sellaisinaan. Lue agentti- ja skillitiedostot ennen käyttöä ja tarkista, mitä ne kirjoittavat projektiisi.

## Lisenssi

[MIT](LICENSE). Copyright (c) 2026 Simo Parviainen.

## Tekijä

Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
