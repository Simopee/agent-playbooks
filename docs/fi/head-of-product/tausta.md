# Head of Product -agentti: tausta ja perustelut

Suomennos englanninkielisestä taustamuistiosta (`docs/head-of-product/background.md`). Agentti rakennettiin alun perin tuotteelle, jota vetää yksi ei-koodaava omistaja tekoälyagenttien tiimin kanssa, ja yleistettiin sen jälkeen. Projektikohtaiset valinnat on poistettu. Tutkimus ja perustelut agentin työtavalle on säilytetty, koska ne tekevät agentista hyödyllisen eikä myötäilevän.

Merkinnät: **[lähde]** lähde tukee väitettä, **[toissijainen]** vain tiivistelmiä oli saatavilla, **[päätelmä]** päättelyä.

## 1. Hyvä ja erinomainen Head of Product

| Hyvä | Erinomainen | Lähde |
|---|---|---|
| Priorisoi backlogin hyvin | Asettaa ratkaistavat ongelmat tulokseen sidottuina; roadmap on seuraus | Cagan, https://www.svpg.com/product-vs-feature-teams/ |
| Mitataan toimituksilla | Mitataan sillä, liikkuuko tulos | Cagan, sama |
| Seuraa monta hanketta | Valitsee tärkeät harvat ja kirjoittaa ylös "kaiken, mitä ei tehdä" | Cagan, https://www.svpg.com/product-strategy-overview/ |
| Sammuttaa tulipaloja | Ennakoi vakavat puutteet | Horowitz, https://a16z.com/2012/06/15/good-product-managerbad-product-manager/ |
| Antaa suullisia mielipiteitä | Ottaa kirjallisia kantoja ja vastaa epäonnistumisista | Horowitz |
| Kysyy "onko tuotto positiivinen?" | Kysyy "onko tämä paras käyttö seuraavalle työlle kaikkeen muuhun verrattuna?" (vaihtoehtoiskustannus) | Doshi [toissijainen], https://www.lennysnewsletter.com/p/episode-3-shreyas-doshi |
| Tekee kaikkea yhtä kovasti | Erottaa Leverage-, Neutral- ja Overhead-työn (LNO) ja käyttää huolellisuuden Leverage-työhön | Doshi [toissijainen] |
| Pitää hidasta etenemistä toteutusongelmana | Tarkistaa ensin, onko kyse strategiaongelmasta | Doshi [toissijainen] |
| Julkaisee ja siirtyy eteenpäin | Julkaisee, mittaa, iteroi, poistaa; tekee retron menneistä panoksista | Cutler, https://cutle.fish/blog/12-signs-youre-working-in-a-feature-factory |
| Vie ensimmäisen hyvän idean eteenpäin | Vertaa vähintään kolmea ratkaisua jokaiseen mahdollisuuteen, testaa riskialtteimman oletuksen | Torres, https://www.producttalk.org/opportunity-solution-trees/ |
| Asettaa kunnianhimoisia tavoitteita | Kirjoittaa diagnoosin keskeisestä esteestä, sitten ohjaavan linjan, sitten yhtenäiset toimet | Rumelt [toissijainen] |
| Listaa ominaisuuksia | Esittää hypoteesin, jolla on mittari ja keinot | Biddle, https://askgib.substack.com/p/ask-gib-how-do-all-your-product-strategy |
| Määrittelee "miten" | Määrittelee "mitä" ja "miksi", jättää "miten" tekijöille | Horowitz |
| Aloittaa työn ja toivoo | Asettaa lopetusehdot (tila + päivämäärä) ennen aloitusta; ennakkoruumiinavaus ennen isoja panoksia | Annie Duke / Doshi [toissijainen] |

**Ominaisuustehtaan ajautumisen merkit (Cutler), jotka koskevat eniten pientä tekoälyllä rakennettua projektia [päätelmä]:** julkaisuja juhlitaan ilman mitattua vaikutusta; mitään ei koskaan karsita tai poisteta; roadmapin kohdat ovat ominaisuuksia eivätkä tuloksia; ei retroa siitä, kannattivatko panokset; kiiltävät uutuudet syrjäyttävät tuotteen kunnossapidon.

**Paikallisen optimoinnin haju [päätelmä LNO:sta]:** suurin osa kierroksesta on Neutral- tai Overhead-työtä (tekstien hiontaa, pientä käyttöliittymän viimeistelyä, refaktorointia), kun Leverage-työ odottaa backlogissa. Juuri tämän ajautumisen agentti on rakennettu huomaamaan.

**Ohut data [päätelmä]:** pienessä mittakaavassa analytiikka kertoo vain suunnan, ja A/B-testeillä ei ole riittävää tehoa. Nojaa hakukyselydataan, muutamaan oikeaan käyttäjäkeskusteluun ja palautteeseen; käytä ennakoivia välimittareita; aseta panoksille tila ja päivämäärä -lopetusehdot merkitsevyystestien sijaan; suosi halpoja, peruttavia kokeiluja. Simuloidut persoonat testaavat ymmärrettävyyttä, eivät koskaan kysyntää.

**Strategiasivun muoto.** Rumeltin ydin: diagnoosi, ohjaava linja, 3–5 yhtenäistä tointa sekä lista siitä, mitä ei tehdä. Cagan: visio pysyy, strategia joustaa. Biddlen "kasva isoksi jossain pienessä, johda, laajene": nosta järjestyskysymyksiä, kun laajentuminen alkaa ennen kuin ydin on todistettu.

**Mikä ei siirry yksin toimivalle omistajalle tekoälyagenttien kanssa:** rekrytointi ja valmentaminen, tiimirakenteet, sidosryhmäpolitiikka (ainoa sidosryhmä on päättäjä), statusraportointi, myynnin vaatimat ominaisuudet (vastine on "yksi käyttäjä pyysi sitä"), tuotekolmikko.

## 2. Miten kielimalliagentit epäonnistuvat neuvonantajina, ja mikä sitä vastaan auttaa

Tämä osa on syy siihen, että pohjan työtapaa ei poisteta räätälöinnissä.

| Epäonnistuminen | Näyttö | Vastakeino pohjassa |
|---|---|---|
| Mielistely: hyväksyy sille näytetyn suunnitelman tai kehyksen | https://arxiv.org/abs/2310.13548, https://arxiv.org/abs/2505.13995, https://openai.com/index/sycophancy-in-gpt-4o/ | Pakollinen karsintalista; "yksimielisyys ei ole tavoite" |
| Luopuu oikeasta kannasta, kun kysytään "oletko varma?" | https://arxiv.org/abs/2311.08596 | Suositus kirjoitetaan ennen kuin ihminen reagoi; muutos vain uudesta näytöstä, joka nimetään |
| Liiallinen varmuus, väitteitä ilman dataa | https://arxiv.org/abs/2306.13063 | Todisteiden ja oletusten erottelu; "en tiedä" sallittu; "mikä muuttaisi kantani" |
| Keksii käyttäjätietoa; persoonan titteli tuo sävyä, ei tietoa | https://arxiv.org/abs/2311.10054 | Menettely eikä persoona; jokaisella käyttäjäväitteellä on lähde tai se merkitään oletukseksi |
| Ankkuroituu ensimmäiseen kehykseen | https://arxiv.org/abs/2412.06593 | Ensin itsenäinen kierros strategiasta ja datasta, sitten ehdotus, sitten erot |
| Kumileimaa muiden agenttien työn; suosii pidempiä vastauksia | https://arxiv.org/abs/2306.05685, https://arxiv.org/abs/2404.13076 | Kiinteä vastausmuoto; pituusraja; erillinen konteksti eikä "paholaisen asianajaja" -nimike |
| Väittely tuo vähän lisää itsenäisiin otoksiin verrattuna | https://arxiv.org/abs/2310.01798 | Ei monikierroksisia väittelyitä; yksi itsenäinen kierros |
| Tokenien kulutus moniagenttiasetelmissa | https://www.anthropic.com/engineering/multi-agent-research-system | Ajetaan vain oikeissa päätöskohdissa, ei koskaan tiketeittäin |
| Roolin paisuminen, kun agentti suunnittelee oman roolinsa; ajautuminen istuntojen välillä | [päätelmä] | Omistaja määrittelee roolin; lukittu strategiasivu on pysyvä ankkuri |

## 3. Mikä on yleistä ja mikä räätälöidään

**Yleistä, säilytetään sellaisenaan:** roolin raja (mitä ja miksi, ei koskaan miten), kahden kierroksen menetelmä, vakiokysymykset, todistesäännöt, kannan pitäminen, kiinteä vastausmuoto ja sen pituusraja, autonominen tila vain lukitulla strategialla, ei-koskaan-lista.

**Räätälöidään projektikohtaisesti (käyttöönoton vaihe 4):** projektin kuvaus, ankkuritiedostot, raja sen kanssa, joka päättää järjestyksestä ja kapasiteetista, kasvun suunnat, pääsy dataan, mittakaava ja sen rajat, päätöskohdat ja työrytmi, enintään kaksi projektikohtaista kysymystä, autonomisen tilan pysäköintilista.

**Rakennetaan projektin kanssa (käyttöönoton vaiheet 2–3):** strategiasivu. Jos projektilla on jo strategiasivu, agentin ensimmäinen tehtävä on pitää työ siinä ja ehdottaa puuttuvat osat (diagnoosi, panokset lopetusehtoineen, lista siitä, mitä ei tehdä). Projektissa, jolla sitä ei ole, sen kirjoittaminen on ensimmäinen tehtävä, ja omistaja lukitsee sen osio osiolta ennen kuin agentti arvioi mitään sitä vasten.

## 4. Koejakso

Käyttöönotto päättyy kolmen kierroksen koejaksoon, jossa jokaisen kierroksen jälkeen vastataan kolmeen kyllä/ei-kysymykseen: muuttiko agentti omistajan valintaa, osoittautuiko jokin varoitus myöhemmin oikeaksi, oppiko omistaja jotain uutta. Julkisia koejakson tuloksia ei ole vielä julkaistu.
