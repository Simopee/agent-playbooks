[In English](README.md)

# agent-playbooks

Tekoälyagenttisi rakentavat sen, mitä niiden eteen laitat. Nämä paketit lisäävät roolit, jotka arvioivat, oliko se oikea asia rakentaa.

Agentteja, skillejä ja toimintaohjeita tuotteiden rakentamiseen tekoälyagenttien kanssa Claude Codessa, englanniksi ja suomeksi. Jokainen paketti on asennettava Claude Code -plugin, jossa on ohjattu käyttöönotto, ja jokaisen paketin voi lukea myös sen omalta sivulta täällä.

## Kenelle

Ihmisille, jotka rakentavat tuotteita agenttitiimin kanssa Claude Codessa: perustajille, tuoteomistajille ja pienille tiimeille, jotka voivat nyt rakentaa melkein mitä tahansa ja tarvitsevat apua sen päättämiseen, mikä kannattaa rakentaa. Pakettien käyttö ei vaadi koodaustaustaa; käyttöönotto kysyy sinulta asiat selkokielellä.

## Asennus

Aja Claude Codessa:

```
/plugin marketplace add Simopee/agent-playbooks
/plugin install head-of-product@simopee-agent-playbooks
```

Aloita sitten käyttöönotto komennolla `/head-of-product:setup`.

**Ilman asennusta:** liitä linkki `https://github.com/Simopee/agent-playbooks` Claude Codeen projektissasi ja kysy, auttaisiko tämä projektiasi. Claude voi lukea tiedostot ja viedä sinut käyttöönoton läpi asentamatta mitään.

## Sisältö

| Paketti | Mitä se tekee | Ohjeet |
|---|---|---|
| [head-of-product](plugins/head-of-product/) | Head of Product -agentti, joka arvioi tuotetyösi kirjoitettua strategiaa vasten, ja ohjattu käyttöönotto, joka kirjoittaa sen strategian kanssasi. | [English](plugins/head-of-product/README.md), [suomeksi](plugins/head-of-product/README.fi.md) |

## Miten se toimii

Paketti koostuu yleensä näistä osista:

- **Agentti** (`agents/`): rooli, jolla on kiinteä työtapa ja kiinteä vastausmuoto. Se lukee projektisi ja suosittelee; sinä päätät.
- **Käyttöönottoskilli** (`skills/setup/`): vaiheittainen ohje, jonka Claude ajaa projektissasi. Se pysähtyy jokaisen vaiheen jälkeen odottamaan hyväksyntääsi ja räätälöi agentin projektiisi. Räätälöitävät kohdat on merkitty `[FILL IN: ...]`.
- **Ohjeet ja esimerkit** (`docs/`, `examples/`): pohjat, taustatutkimus ja täytetty esimerkki, jotta näet lopputuloksen ennen kuin aloitat. Suomennokset ovat kansiossa `docs/fi/`.

Paketti voi olla myös pelkkä skilli tai toimintaohje ilman agenttia. Paketit toimivat missä tahansa Claude Code -projektissa. Ne eivät tarvitse muuta järjestelmää eivätkä ulkoista palvelua.

## Tiekartta

- **Suunnitteilla:** lisää rooleja, skillejä ja toimintaohjeita agenttisesta tuotetiimistä (esimerkiksi järjestelmäanalyytikko, laadunvarmistus ja niitä yhdistävät rutiinit), paketti kerrallaan. Jokainen uusi paketti saa oman kansionsa ja oman sivunsa, ja ne asennetaan samalla tavalla.

## Tarkista ennen käyttöä

Nämä ovat kehotteita ja ohjeita, eivät auditoitua ohjelmistoa. Ne tarjotaan sellaisenaan. Lue agentti- ja skillitiedostot ennen käyttöä ja tarkista, mitä ne kirjoittavat projektiisi.

## Lisenssi

[MIT](LICENSE). Copyright (c) 2026 Simo Parviainen.

## Tekijä

Tehnyt Simo Parviainen, https://www.linkedin.com/in/simo-parviainen
