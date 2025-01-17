﻿## Johdanto

Tervetuloa TeleNVDA-lisäosaan, jonka avulla voit yhdistää toiseen ilmaista NVDA-ruudunlukuohjelmaa käyttävään tietokoneeseen. Voit yhdistää toisen henkilön tietokoneeseen tai sallia luotetun henkilön yhdistää järjestelmääsi ylläpitorutiinien suorittamista, ongelman diagnosointia tai koulutuksen tarjoamista varten. Tämä on muokattu versio [NVDA-etäkäyttö-lisäosasta](https://nvdaremote.com), ja ylläpidosta vastaa NVDA:n espanjalaisyhteisö. Se on täysin yhteensopiva NVDA-etäkäyttö-lisäosan kanssa. Nämä ovat nykyiset erot:

* Asetus mahdollistaa sellaisten etäpuhekomentojen estämisen, jotka eroavat tekstistä.
* Paranneltu tuki välityspalvelimille ja TOR-piilopalveluille ([Välityspalvelintuki-lisäosa](https://addons.nvda-project.org/addons/proxy.fi.html) vaaditaan).
* Mahdollisuus F11-näppäinkomennon vaihtamiseen. Se toimii nyt yleisskriptinä, joten näppäinkomento voidaan määrittää Näppäinkomennot-valintaikkunassa.
* Mahdollisuus seuraavan näppäinkomennon ohittamiseen kokonaan. Tästä on hyötyä, mikäli sinun tarvitsee lähettää etä- ja isäntäkoneen välillä vaihtava näppäinkomento etäkoneeseen.
* Useita bugikorjauksia.

## Ennen kuin aloitat

NVDA ja TeleNVDA-lisäosa on oltava asennettuna molemmissa tietokoneissa.
Molempien asennusvaiheet ovat standardinmukaisia. Lisätietoja löytyy NVDA:n käyttöoppaasta.

## Päivittäminen

Mikäli olet asentanut TeleNVDA-lisäosan suojatulle työpöydälle,  lisäosaa päivitettäessä on suositeltavaa, että päivität myös sen version.
Tämä tehdään päivittämällä ensin olemassa oleva lisäosa ja valitsemalla sitten NVDA-valikosta Asetukset -> Asetukset -> Yleiset ja painamalla "Käytä tallennettuja asetuksia kirjautumisikkunassa ja muissa suojatuissa ruuduissa (edellyttää järjestelmänvalvojan oikeuksia)" -painiketta.

## Etäistunnon aloittaminen välittäjäpalvelimen kautta
### Hallittavassa tietokoneessa
1. Avaa NVDA-valikko ja valitse Työkalut -> Etäkäyttö -> Yhdistä.
2. Valitse ensimmäisestä valintapainikeryhmästä Asiakas.
3. Valitse toisesta valintapainikeryhmästä Salli tämän tietokoneen hallinta.
4. Kirjoita Isäntä-muokkauskenttään sen palvelimen osoite, johon olet yhdistämässä, esimerkiksi remote.nvda.es. Jos palvelin käyttää vaihtoehtoista porttia, voit kirjoittaa isäntäkoneen muodossa &lt;isäntä&gt;:&lt;portti&gt;, esim. remote.nvda.es:1234.
5. Kirjoita Avain-muokkauskenttään haluamasi avain tai paina Luo avain -painiketta.
Avainta käytetään tietokoneesi hallitsemiseen.
Hallittavan koneen ja kaikkien siihen yhdistävien asiakaskoneiden on käytettävä samaa avainta.
6. Paina OK. Kun yhteys on muodostettu, kuulet äänimerkin ja "Yhdistetty"-ilmoituksen. Jos palvelin sisältää päivän viestin, se näytetään valintaikkunassa. Palvelimen asetuksista riippuen näet tämän valintaikkunan joka kerta muodostaessasi yhteyden tai vain ensimmäisellä kerralla.

### Hallitsevassa tietokoneessa
1. Avaa NVDA-valikko ja valitse Työkalut -> Etäkäyttö -> Yhdistä.
2. Valitse ensimmäisestä valintapainikeryhmästä Asiakas.
3. Valitse toisesta valintapainikeryhmästä Hallitse toista konetta.
4. Kirjoita Isäntä-muokkauskenttään sen palvelimen osoite, johon olet yhdistämässä, esimerkiksi remote.nvda.es. Jos palvelin käyttää vaihtoehtoista porttia, voit kirjoittaa isäntäkoneen muodossa &lt;isäntä&gt;:&lt;portti&gt;, esim. remote.nvda.es:1234. Jos muodostat yhteyden  IPv6-osoitteeseen, kirjoita se hakasulkuihin, esimerkiksi [2603:1020:800:2::32].
5. Kirjoita Avain-kenttään haluamasi avain tai paina Luo avain -painiketta.
Hallittavan koneen ja kaikkien siihen yhdistävien asiakaskoneiden on käytettävä samaa avainta.
6. Paina OK. Kun yhteys on muodostettu, kuulet äänimerkin ja "Yhdistetty"-ilmoituksen. Jos palvelin sisältää päivän viestin, se näytetään valintaikkunassa. Palvelimen asetuksista riippuen näet tämän valintaikkunan joka kerta muodostaessasi yhteyden tai vain ensimmäisellä kerralla.

### Yhteyden suojausvaroitus
Jos muodostat yhteyden palvelimeen, jolla ei ole kelvollista SSL-varmennetta, näkyviin tulee yhteyden suojausvaroitus.
Tämä voi tarkoittaa, että yhteytesi ei ole turvallinen. Jos luotat tähän palvelimen sormenjälkeen, voit muodostaa yhteyden kerran painamalla  "Yhdistä" tai muodostaa yhteyden ja tallentaa sormenjäljen painamalla "Yhdistä ja älä kysy uudelleen tästä palvelimesta".

## Suorat yhteydet
Yhdistä-valintaikkunan Palvelin-vaihtoehdolla voit muodostaa suoran yhteyden.
Kun se on valittuna, valitse myös, missä tilassa yhteytesi on.
Toinen osapuoli yhdistää koneeseesi päinvastaista vaihtoehtoa käyttäen.

Kun tila on valittu, voit käyttää Hae ulkoinen IP -painiketta noutaaksesi ulkoisen IP-osoitteesi ja varmistaaksesi, että Portti-muokkauskenttään syötetty portti on uudelleenohjattu asianmukaisesti.
Jos portintarkistus havaitsee, ettei porttiin (oletusarvoisesti 6837) saada yhteyttä, näkyviin tulee siitä kertova varoitus.
Sinun on tällöin uudelleenohjattava porttisi ja yritettävä sitten uudelleen.
Huom: Porttien uudelleenohjausta ei käsitellä tässä asiakirjassa. Katso lisätietoja reitittimesi mukana toimitetuista ohjeista.

Kirjoita avain Avain-muokkauskenttään tai paina Luo avain -painiketta. Toinen osapuoli tarvitsee yhdistämiseen ulkoisen IP-osoitteesi lisäksi tämän avaimen. Mikäli syötit Portti-muokkauskenttään muun kuin oletusportin (6837), varmista, että toinen osapuoli lisää isäntäkoneen osoitteeseen vaihtoehtoisen portin muodossa &lt;ulkoinen IP&gt;:&lt;portti&gt;.

Yhteys muodostetaan painettuasi OK-painiketta.
Kun toinen osapuoli yhdistää koneeseesi, voit käyttää TeleNVDA:ta normaalisti.

## Etäkoneen hallinta

Kun yhteys on muodostettu, etäkoneen hallinta (esim. näppäinpainallusten tai pistekirjoitussyötteen lähettäminen) voidaan aloittaa painamalla hallitsevassa koneessa F11. Tätä näppäinkomentoa voidaan vaihtaa NVDA:n Näppäinkomennot-valintaikkunasta.
Kun NVDA sanoo Hallitaan etäkonetta, painamasi näppäimistön ja pistenäytön näppäimet suoritetaan etäkoneessa. Lisäksi, jos hallitsevassa tietokoneessa käytetään pistenäyttöä, kaikki etäkoneen palaute näytetään siinä. Lopeta näppäinpainallusten lähettäminen ja vaihda takaisin hallitsevaan koneeseen painamalla uudelleen F11.
Varmista parhaan yhteensopivuuden takaamiseksi, että molemmissa koneissa on käytössä sama näppäinasettelu.

## Istunnon jakaminen

Jotta muut voivat helposti liittyä TeleNVDA-istuntoosi, valitse Etäkäyttö-valikosta Kopioi linkki -vaihtoehto.
Mikäli olet yhteydessä hallitsevana tietokoneena, tämä linkki sallii jonkun muun henkilön yhdistää tietokoneeseesi sekä hänen koneensa hallitsemisen.
Jos sen sijaan olet määrittänyt tietokoneesi hallittavaksi, linkki sallii henkilöiden, joille sen jaat, hallita konettasi.
Useat sovellukset mahdollistavat linkin automaattisen avaamisen, mutta mikäli se ei onnistu jossain määrätyssä sovelluksessa, se voidaan kopioida leikepöydälle ja avata Suorita-valintaikkunasta.

## Lähetä Ctrl+Alt+Del
Ctrl+Alt+Del-näppäinyhdistelmän lähettäminen ei ole mahdollista näppäinpainalluksia lähetettäessä.
Käytä tätä komentoa, mikäli sinun on lähetettävä Ctrl+Alt+Del etäjärjestelmälle, jossa suojattu työpöytä on aktiivisena.

## Lähetä tilanvaihtonäppäin paikallisen ja etäkoneen välillä
Yleensä kun painat määritettyä näppäinkomentoa vaihtaaksesi paikallisen ja etäkoneen välillä, sitä ei lähetetä etäkoneelle vaan se vaihtaa paikallisen ja etäkoneen välillä.

Jos sinun tarvitsee lähettää tämä tai mikä tahansa muu näppäinkomento etäkoneelle, voit ohittaa tämän toiminnan seuraavaksi painetulle näppäinkomennolle aktivoimalla Lähetä seuraava näppäinkomento -skriptin.

Tälle skriptille on määritetty oletusarvoisesti Ctrl+F11-näppäinkomento. Sitä on mahdollista vaihtaa NVDA:n Näppäinkomennot-valintaikkunasta.

Kun tämä skripti on aktivoitu, seuraavaksi painettu näppäinkomento ohitetaan ja lähetetään etäkoneelle, "ohita seuraava näppäinkomento" -skriptin aktivoiva näppäinkomento mukaan lukien. Kun seuraava näppäinkomento on lähetetty, se palaa tavanomaiseen toimintaan.

## Valvomattoman tietokoneen etähallinta

Saatat joskus haluta etähallita omaa konettasi. Tämä on erityisen hyödyllistä matkoilla ollessasi ja halutessasi hallita kotikonetta kannettavallasi, tai kotona sisällä talossa olevaa konetta ollessasi itse ulkona toisen koneen kanssa. Tämä on mahdollista pienen valmistelun jälkeen.

1. Avaa NVDA-valikko ja valitse Työkalut ja sitten Etäkäyttö. Paina lopuksi Enter Asetukset-vaihtoehdon kohdalla.
2. Valitse "Yhdistä hallintapalvelimeen automaattisesti käynnistyksen yhteydessä" -valintaruutu.
3. Valitse, käytetäänkö etävälittäjäpalvelinta vai isännöidäänkö yhteyttä paikallisesti. 
4. Valitse toisena olevasta valintapainikeryhmästä Salli tämän koneen hallinta.
5. Mikäli isännöit yhteyttä itse, sinun on varmistettava, että  hallitsevista koneista saadaan yhteys hallitsevassa koneessa Portti-muokkauskenttään syötettyyn porttiin (oletusarvoisesti 6837).
6. Jos haluat käyttää välittäjäpalvelinta, täytä sekä Isäntä- että Avain-muokkauskentät, siirry Sarkaimella OK-painikkeen kohdalle ja paina Enter. Luo avain -vaihtoehto ei ole käytettävissä, joten parasta on keksiä helposti muistettava avain, jotta voit käyttää sitä mistä tahansa etäsijainnista.

Vvoit  määrittää TeleNVDA:n yhdistämään edistynyttä käyttöä varten myös automaattisesti paikalliseen tai etävälittäjäpalvelimeen hallintatilassa. Tämä tehdään valitsemalla Hallitse toista konetta toisena olevasta valintapainikeryhmästä.

Huom: Asetukset-valintaikkunan automaattisen käynnistyksen yhteydessä yhdistämiseen liittyvillä vaihtoehdoilla ei ole vaikutusta ennen NVDA:n uudelleenkäynnistystä.

## Puheen mykistäminen etätietokoneessa
Jos et halua kuulla etäkoneen puhetta tai NVDA:n äänimerkkejä, avaa NVDA-valikko ja valitse Työkalut -> Etäkäyttö. Siirry lopuksi alanuolinäppäimellä kohtaan Mykistä etäkone ja paina Enter. Huom: Tämä asetus ei poista käytöstä hallitsevan koneen pistenäytölle tuotettavaa etäpistekirjoituspalautetta, kun hallitsevan koneen näppäinpainallusten lähettäminen on käytössä.

## Etäistunnon lopettaminen

Lopeta etäistunto seuraavasti:

1. Lopeta etäkoneen hallinta painamalla hallitsevassa koneessa F11. NVDA:n pitäisi nyt sanoa tai pistenäytöllä lukea "Hallitaan paikallista konetta". Jos sen sijaan kuulet tai näet pistenäytöllä ilmoituksen etäkoneen hallitsemisesta, paina vielä kerran F11.
2. Avaa NVDA-valikko, valitse Työkalut -> Etäkäyttö ja paina Enter Katkaise yhteys -vaihtoehdon kohdalla.

Vaihtoehtoisesti voit katkaista istunnon yhteyden suoraan painamalla NVDA+Alt+Page down. Tätä näppäinkomentoa voidaan vaihtaa NVDA:n Näppäinkomennot-valintaikkunasta. Voit pitää toisen osapuolen turvassa katkaisemalla etätietokoneen yhteyden painamalla tätä näppäinkomentoa näppäinten lähettämisen ollessa käytössä.

## Leikepöydän lähettäminen
Etäkäyttö-valikon Lähetä leikepöytä -vaihtoehdolla voit lähettää leikepöydällä olevan tekstin.
Kun toiminto on otettu käyttöön, kaikki leikepöydällä oleva teksti lähetetään toisille koneille.

## Tiedostojen lähettäminen
Etäkäyttö-valikon Lähetä tiedosto -vaihtoehto mahdollistaa pienten tiedostojen lähettämisen kaikille istunnon jäsenille, hallittava kone mukaan lukien. Huom: Voit lähettää vain tiedostoja, jotka ovat pienempiä kuin 10 Mt. Tiedostojen lähettäminen tai vastaanottaminen ei ole mahdollista suojatuissa ruuduissa.
Kun tiedosto on vastaanotettu etäkoneilla, näkyviin tulee Tallenna nimellä -valintaikkuna, jossa voit valita, minne tiedosto tallennetaan.
## TeleNVDA:n määrittäminen toimimaan suojatulla työpöydällä
Jotta TeleNVDA-lisäosa toimisi suojatulla työpöydällä, se on asennettava suojatulla työpöydällä käynnissä olevaan NVDA:han.

1. Valitse NVDA-valikosta Asetukset -> Asetukset -> Yleiset.
2. Siirry Sarkaimella Käytä tallennettuja asetuksia kirjautumis- ja muissa suojatuissa ruuduissa (edellyttää järjestelmänvalvojan oikeuksia) -painikkeen kohdalle ja paina Enter.
3. Vastaa Kyllä kysymyksiin asetustesi ja lisäosien kopioinnista sekä mahdollisesti näkyviin tulevaan Käyttäjätilien valvonnan kehotteeseen.
4. Kun asetukset on kopioitu, paina Enter sulkeaksesi siitä kertova ilmoitus. Siirry sitten sarkaimella OK-painikkeen kohdalle ja paina vielä kerran Enter sulkeaksesi valintaikkunan.

Kun TeleNVDA on asennettu suojatulle työpöydälle ja jos konettasi hallitaan etäistunnossa, puhe ja pistenäyttö ovat käytettävissä suojatulle työpöydälle siirryttäessä.

## SSL-varmennesormenjälkien tyhjentäminen
Jos et halua enää luottaa aiemmin luottamiisi palvelinsormenjälkiin, voit tyhjentää ne kaikki painamalla Asetukset-valintaikkunassa "Poista kaikki luotetut sormenjäljet" -painiketta.

## TeleNVDA:n muokkaaminen

Tämä projekti on suojattu GNU GPL v2:lla tai uudemmalla lisenssillä. Voit kloonata tämän koodivaraston tehdäksesi muokkauksia TeleNVDA:han, edellyttäen, että luet, ymmärrät ja kunnioitat lisenssin ehtoja.

### Kolmannen osapuolen riippuvuudet

Nämä voidaan asentaa pip:llä:

* Markdown
* scons

URL-käsittelijäohjelman kääntämiseen tarvitset Visual Studio 2019:n tai uudemman.

### Lisäosan paketointi jakelua varten

1. Avaa komentokehote ja vaihda hakemistoksi tämän koodivaraston juuri.
2. Suorita **scons**-komento. Jos virheitä ei ilmennyt, luotu lisäosa sijoitetaan nykyiseen hakemistoon.
