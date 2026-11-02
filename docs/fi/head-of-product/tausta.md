# Head of Product -agentti: tausta ja perustelut

Suomennos englanninkielisestä taustamuistiosta (`docs/head-of-product/background.md`). Agentti tehtiin alun perin tuotteelle, jota vetää yksi koodaamaton omistaja tekoälyagenttien tiimin kanssa, ja yleistettiin sitten muillekin sopivaksi. Projektikohtaiset valinnat on poistettu. Agentin työtavan taustalla oleva tutkimus ja perustelut on säilytetty, koska juuri niiden ansiosta agentista on hyötyä eikä se vain myötäile.

Merkinnät: **[lähde]** lähde tukee väitettä, **[toissijainen]** saatavilla oli vain tiivistelmiä, **[päätelmä]** oma päättely.

## 1. Hyvä ja erinomainen Head of Product

| Hyvä | Erinomainen | Lähde |
|---|---|---|
| Priorisoi backlogin hyvin | Määrittelee ratkaistavat ongelmat ja sitoo ne tavoiteltuun tulokseen; roadmap seuraa niistä | Cagan, https://www.svpg.com/product-vs-feature-teams/ |
| Mitataan sillä, mitä julkaistaan | Mitataan sillä, liikkuuko tulos | Cagan, sama |
| Seuraa montaa hanketta | Valitsee harvat tärkeimmät ja kirjoittaa ylös "kaiken, mitä ei tehdä" | Cagan, https://www.svpg.com/product-strategy-overview/ |
| Sammuttaa tulipaloja | Näkee vakavat puutteet ennalta | Horowitz, https://a16z.com/2012/06/15/good-product-managerbad-product-manager/ |
| Kertoo mielipiteensä suullisesti | Ottaa kantaa kirjallisesti ja kantaa vastuun epäonnistumisista | Horowitz |
| Kysyy, onko tuotto positiivinen | Kysyy, onko tämä paras mahdollinen seuraava työ kaikkeen muuhun verrattuna (vaihtoehtoiskustannus) | Doshi [toissijainen], https://www.lennysnewsletter.com/p/episode-3-shreyas-doshi |
| Tekee kaikkea yhtä kovalla vaivalla | Erottaa Leverage-, Neutral- ja Overhead-työn (LNO) ja keskittää huolellisuuden Leverage-työhön | Doshi [toissijainen] |
| Pitää hidasta etenemistä toteutuksen ongelmana | Tarkistaa ensin, onko kyse strategian ongelmasta | Doshi [toissijainen] |
| Julkaisee ja siirtyy seuraavaan | Julkaisee, mittaa, iteroi ja poistaa; pitää retron menneistä panostuksista | Cutler, https://cutle.fish/blog/12-signs-youre-working-in-a-feature-factory |
| Vie ensimmäisen hyvän idean eteenpäin | Vertaa jokaiseen mahdollisuuteen vähintään kolmea ratkaisua ja testaa riskialtteimman oletuksen | Torres, https://www.producttalk.org/opportunity-solution-trees/ |
| Asettaa kunnianhimoisia tavoitteita | Kirjoittaa diagnoosin keskeisestä esteestä, sitten ohjaavan linjan ja sitten yhtenäiset toimet | Rumelt [toissijainen] |
| Listaa ominaisuuksia | Esittää hypoteesin, jolla on mittari ja keinot | Biddle, https://askgib.substack.com/p/ask-gib-how-do-all-your-product-strategy |
| Määrittelee, miten tehdään | Määrittelee, mitä tehdään ja miksi, ja jättää toteutustavan tekijöille | Horowitz |
| Aloittaa työn ja toivoo parasta | Asettaa lopetusehdot (tila ja päivämäärä) ennen aloitusta; tekee ennakkoruumiinavauksen ennen isoja panostuksia | Annie Duke / Doshi [toissijainen] |

**Merkit ajautumisesta ominaisuustehtaaksi (Cutler), jotka koskevat eniten pientä tekoälyllä rakennettua projektia [päätelmä]:** julkaisuja juhlitaan, vaikka vaikutusta ei ole mitattu; mitään ei koskaan karsita tai poisteta; roadmapissa on ominaisuuksia eikä tuloksia; kukaan ei arvioi jälkikäteen, kannattivatko panostukset; kiiltävät uutuudet vievät ajan tuotteen kunnossapidolta.

**Merkki paikallisesta optimoinnista [päätelmä LNO:n pohjalta]:** suurin osa kierroksesta on Neutral- tai Overhead-työtä (tekstien hiomista, käyttöliittymän pientä viimeistelyä, refaktorointia), ja Leverage-työ odottaa backlogissa. Juuri tällaisen ajautumisen huomaamiseen agentti on rakennettu.

**Vähäinen data [päätelmä]:** pienessä mittakaavassa analytiikka kertoo vain suunnan, eikä A/B-testeissä ole tarpeeksi tilastollista voimaa. Nojaa hakukyselydataan, muutamaan oikeaan käyttäjäkeskusteluun ja palautteeseen. Käytä ennakoivia välimittareita. Aseta panostuksille lopetusehdot tilan ja päivämäärän muodossa merkitsevyystestien sijaan. Suosi halpoja kokeiluja, jotka voi perua. Simuloidut persoonat testaavat ymmärrettävyyttä, eivät koskaan kysyntää.

**Strategiasivun muoto.** Rumeltin ydin: diagnoosi, ohjaava linja ja 3–5 yhtenäistä toimea sekä lista siitä, mitä ei tehdä. Caganin mukaan visio pysyy ja strategia joustaa. Biddlen periaate "kasva isoksi jossain pienessä, ota johtoasema, laajene": nosta esiin järjestystä koskevat kysymykset, jos laajentuminen alkaa ennen kuin ydin on osoittanut toimivuutensa.

**Mikä ei päde yksin toimivaan omistajaan, jolla on tekoälyagentit:** rekrytointi ja valmentaminen, tiimirakenteet, sidosryhmäpolitiikka (ainoa sidosryhmä on päättäjä), tilanneraportointi, myynnin vaatimat ominaisuudet (vastine tälle on "yksi käyttäjä pyysi sitä") ja tuotekolmikko.

## 2. Miten kielimalliagentit epäonnistuvat neuvonantajina ja mikä auttaa

Tämän osan vuoksi pohjan työtapaa ei poisteta, kun agenttia sovitetaan projektiin.

| Epäonnistuminen | Näyttö | Vastakeino pohjassa |
|---|---|---|
| Mielistely: hyväksyy suunnitelman tai näkökulman, joka sille näytetään | https://arxiv.org/abs/2310.13548, https://arxiv.org/abs/2505.13995, https://openai.com/index/sycophancy-in-gpt-4o/ | Karsintalista on pakollinen; "yksimielisyys ei ole tavoite" |
| Luopuu oikeasta kannasta, kun siltä kysytään "oletko varma?" | https://arxiv.org/abs/2311.08596 | Suositus kirjoitetaan ennen kuin ihminen ehtii reagoida; kanta muuttuu vain uuden näytön perusteella, ja näyttö nimetään |
| Ylivarmuus, väitteitä ilman dataa | https://arxiv.org/abs/2306.13063 | Näyttö ja oletukset erotetaan; "en tiedä" on sallittu; "mikä muuttaisi kantani" |
| Keksii tietoa käyttäjistä; persoonan titteli tuo sävyä, ei tietoa | https://arxiv.org/abs/2311.10054 | Menettely persoonan sijaan; jokaiselle käyttäjiä koskevalle väitteelle on lähde, tai se merkitään oletukseksi |
| Ankkuroituu ensimmäiseen näkökulmaan | https://arxiv.org/abs/2412.06593 | Ensin itsenäinen kierros strategian ja datan pohjalta, sitten ehdotus ja lopuksi erot |
| Hyväksyy muiden agenttien työn tarkistamatta; suosii pidempiä vastauksia | https://arxiv.org/abs/2306.05685, https://arxiv.org/abs/2404.13076 | Vakiomuotoinen vastaus; pituusraja; erillinen konteksti eikä "paholaisen asianajajan" roolia |
| Väittely tuo vain vähän lisää verrattuna itsenäisiin vastauksiin | https://arxiv.org/abs/2310.01798 | Ei monikierroksisia väittelyitä; yksi itsenäinen kierros |
| Tokenien kulutus moniagenttiasetelmissa | https://www.anthropic.com/engineering/multi-agent-research-system | Ajetaan vain todellisissa päätöskohdissa, ei koskaan tiketeittäin |
| Rooli paisuu, kun agentti suunnittelee sen itse; ajautuminen istunnosta toiseen | [päätelmä] | Omistaja määrittelee roolin; lukittu strategiasivu on pysyvä ankkuri |

## 3. Mikä on yleistä ja mikä sovitetaan projektiin

**Yleistä, säilytetään sellaisenaan:** roolin raja (mitä ja miksi, ei koskaan miten), kahden kierroksen menetelmä, vakiokysymykset, näyttöä koskevat säännöt, kannassa pysyminen, vakiomuotoinen vastaus ja sen pituusraja, autonominen tila vain lukitun strategian kanssa sekä luettelo asioista, joita agentti ei koskaan tee.

**Sovitetaan projektiin (käyttöönoton vaihe 4):** projektin kuvaus, ankkuritiedostot, raja sen kanssa, joka päättää järjestyksestä ja kapasiteetista, kasvusuunnat, pääsy dataan, mittakaava ja sen rajat, päätöskohdat ja työrytmi, enintään kaksi projektikohtaista kysymystä sekä luettelo asioista, jotka autonomisessa tilassa jätetään odottamaan omistajaa.

**Rakennetaan yhdessä projektin kanssa (käyttöönoton vaiheet 2–3):** strategiasivu. Jos projektilla on jo strategiasivu, agentin ensimmäinen tehtävä on pitää työ sen mukaisena ja ehdottaa puuttuvat osat (diagnoosi, panostukset lopetusehtoineen ja lista siitä, mitä ei tehdä). Jos sivua ei ole, sen kirjoittaminen on ensimmäinen tehtävä, ja omistaja lukitsee sen osio kerrallaan ennen kuin agentti arvioi mitään sen pohjalta.

## 4. Koejakso

Käyttöönotto päättyy kolmen kierroksen koejaksoon. Jokaisen kierroksen jälkeen vastataan kolmeen kyllä vai ei -kysymykseen: muuttiko agentti omistajan valintaa, osoittautuiko jokin huomautus myöhemmin aiheelliseksi ja oppiko omistaja jotain uutta. Koejaksojen tuloksia ei ole vielä julkaistu.
