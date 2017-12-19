---
title: "Vaihekuvaus – Projektinhallinta Projektit-sovellusalueen avulla | Microsoft Docs"
description: "Tässä vaihekuvauksessa esitellään töiden projektinhallintatoiminnot. Projektien avulla voit laatia yrityksen resurssien käyttöön liittyviä aikatauluja ja seurata tietyn projektin resursseihin liittyviä kustannuksia. Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b6a61a9c5d2b8c7b3d197780c580c8bcf957560e
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Vaihekuvaus: Projektinhallinta Projektit-sovellusalueen avulla
Tässä vaihekuvauksessa esitellään projektitöiden projektinhallintatoiminnot. Projektien avulla voit laatia yrityksen resurssien käyttöön liittyviä aikatauluja ja seurata tietyn projektin resursseihin liittyviä kustannuksia. Projekteissa kuluu esimerkiksi työntekijöiden työtunteja, koneiden käyttötunteja ja varastonimikkeitä, joita täytyy seurata projektin edetessä.  

 Tässä vaihekuvauksessa käsitellään uusien projektien määrittämistä moduulissa sekä joitakin tavanomaisia tehtäviä, joita ovat esimerkiksi kiinteän hinnoittelun käsittely, maksujen suorittaminen osamaksuina, projektien laskujen kirjaaminen sekä projektien kopioiminen.  

## <a name="about-this-walkthrough"></a>Tietoja tästä vaihekuvauksesta  
 Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

### <a name="setting-up-a-job"></a>Projektin määrittäminen  
 Budjettirakenne määritettynä projekteille, prjektin luominen on yksinkertaista. Tässä vaihekuvauksessa käsitellään seuraavia vaiheita:  

-   tehtävärivien ja suunnittelurivien määrittäminen  
-   projektikohtaisten hintojen luominen nimikkeille, resursseille ja KP-tileille  
-   laskuttaminen projektista.  

### <a name="handling-fixed-prices"></a>Kiinteiden hintojen käsitteleminen  
 Projektit-sovellusalueessa voit käsitellä paitsi kiinteitä hintoja myös sellaisia palveluiden tai tavaroiden hintoja, joista on sovittu ennalta asiakkaiden kanssa. Tässä vaihekuvauksessa voit tehdä seuraavat toimet:  

-   Katso, kuinka sopimuksen ja laskun arvot määritetään  
-   Salli ylimääräisen (laskuttamattoman) työn lisääminen aikatauluun.  

### <a name="copying-a-job"></a>Projektin kopioiminen  
 Tässä esimerkkitilanteessa keskitytään siihen, kuinka koko projekti tai osa siitä kopioidaan tietojen manuaalisen lisäämistarpeen vähentämiseksi ja tarkkuuden parantamiseksi. Mukana olevia aiheita ovat Se sisältää seuraavat:  

-   projektin osan kopioiminen uuteen projektiin  
-   projektikohtaisten hintojen kopioiminen  
-   suunnittelurivien kopioiminen.  

### <a name="making-payment-by-installment"></a>Maksujen suorittaminen osamaksuina  
 Kun suuri, kallis projekti kestää pitkään, asiakas tekee usein yrityksen kanssa sopimuksen maksuerien maksamiseksi. Tämä esimerkki näyttää, miten maksutapa määritellään osamaksuina, ja se kattaa seuraavat asiat:  

-   osamaksun luominen projektille  
-   maksujen laskuttaminen asiakkailta  
-   käytön ottaminen huomioon projektissa, jossa käytetään osamaksua.  

## <a name="roles"></a>Roolit  
 Tässä vaihekuvauksessa on seuraaviin rooleihin liittyviä tehtäviä:  

-   Projektipäällikkö  
-   Projektitiimin jäsen  

## <a name="prerequisites"></a>Vaatimukset  
 Tee seuraavat toimet ennen tämän vaihekuvauksen tehtävien suorittamista:  

-   Asenna CRONUS Finland Oy -esittelytietokanta.
-   Luo esimerkkitietoja noudattamalla seuraavan osan toimintaohjeita.  

## <a name="story"></a>Taustatietoja  
Tämä vaihekuvaus keskittyy suunnittelu- ja konsulttiyritykseen CRONUS Finland Oy, joka suunnittelee ja varustaa uusia infrastruktuureja, kuten konferenssisaleja ja toimistoja huonekaluineen, tarvikkeineen ja varastoineen. Sen useimmat työt projektisuuntautuneita. Thomas on CRONUKSEN projektipäällikkö. Käynnissä olevien CRONUSIN käynnistämien projektien ansiosta hän saa yleiskuvan jokaisesta meneillään olevasta ja valmiista projektista. Hän järjestää tavallisesti kaupat asiakkaiden kanssa ja lisää projektin ydintiedot, joita olivat tehtävä- ja suunnittelurivit sekä hinnat, [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelmaan. Hän toteaa, että tietojen luominen, ylläpitäminen ja tarkistaminen on suoraviivaista. Thomas pitää myös tavasta, jolla [!INCLUDE[d365fin](includes/d365fin_md.md)] mahdollistaa töiden kopioinnin ja maksamisen osamaksuina.

 Projektitiimin jäsen Marianne, joka työskentelee Thomasin alaisena, on projektin päivittäinen vastuuhenkilö. Hän kirjoittaa oman työn lisäksi teknikoiden suorittaman työn jokaisen tehtävän kohdalle. Hän kirjaa nimikkeet, jotka he ovat käyttäneet ja kustannukset, jotka he ovat aiheuttaneet.  

## <a name="preparing-sample-data"></a>Esimerkkitietojen valmisteleminen  
 Valmistaudu tähän vaihekuvaukseen lisäämällä Tricia uutena resurssina.  

### <a name="to-prepare-the-sample-data"></a>Esimerkkitietojen valmisteleminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Resurssit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi resurssin kortti valitsemalla **Uusi**-toiminto.  
3.  Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    - **Nro:**: **Marianne**  
    - **Nimi**: **Marianne**  
    - **Tyyppi**: **Henkilö**  

4.  Valitse **Perusmittayksikkö** -kenttä ja avaa sitten **Resurssin mittayksikkö** -ikkuna valitsemalla **Uusi**. Valitse **Tyyppi**-kentässä **Tunti**. Valitse **OK**-painike.  
5.  Lisää seuraavat tiedot **Laskutus**-pikavälilehteen:  

    -   **Välitön yksikkökustannus**: **5**  
    -   **Välillinen kustannus****4**  
    -   **Yksikkökustannus**: **10**  
    -   **Yleinen tuotteen kirjausryhmä**: **Palvelut**  
    -   **Tuotteen ALV-kirjausryhmä****ALV 25**  

6.  Tallenna muutokset valitsemalla **OK**-painike.  

 Seuraavassa toimenpiteessä luot projektipäiväkirjan erän Mariannea varten, jotta hän voi kirjata käyttönsä.  

### <a name="to-create-a-job-journal-batch"></a>Luo uusi päiväkirjan erä.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Projektipäiväkirja**-ikkunassa **Erän nimi**-kenttä. **Projektipäiväkirjan erät** -ikkuna avautuu.  
3.  Valitse **Uusi**-toiminto, jos haluat luoda uuden rivin, jolla ovat seuraavat tiedot:  

    -   **Nimi**: **Marianne**  
    -   **Kuvaus**: **Marianne**  
    -   **Nrosarja**: **PPVK-YLEIN**.  

4.  Valitse **OK**-painike, jos haluat sulkea kaikki avoimet ikkunat.  

## <a name="setting-up-a-job"></a>Projektin määrittäminen  
 Tässä skenaariossa CRONUS on voittanut sopimuksen Progressive Home Furnishings -yrityksen kanssa, jonka kanssa on päästy sopimukseen neuvottelusalin ja ruokasalin suunnittelemisesta. Asiakkaan tilat ovat Yhdysvalloissa, ja projektissa tarvitaan erityistä ohjelmistoa. Projektipäällikkö pääsee asiakkaan sopimukseen ja sopimuksen keston kattava projekti luodaan.  

### <a name="to-set-up-a-job"></a>Projektin määrittäminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi kortti valitsemalla **Uusi**-toiminto.  
3.  Anna **Yleiset**-pikavälilehdessä seuraavat tiedot:  

    -   **Kuvaus**: **Konsultointi neuvottelusalin sisustuksesta**  
    -   **Laskutusasiakkaan nro**: **01445544**  

4.  Lisää seuraavat tiedot **Kirjaus**-pikavälilehteen:  

    -   **Tila**: **Tilaus**  
    -   **Projektin kirjausryhmä**: **As. määr.**  
    -   **KET-menetelmä**: **Kustannusarvo**  

5.  Kirjoita kuluvan päivän päivämäärä **Kesto**-pikavälilehden **Aloituspvm**- ja **Lopetuspvm**-kenttiin. Nämä päivämäärät helpottavat valuuttamuunnosten tekemistä, kun projekti laskutetaan.  
6.  Vahvista **Ulkomaankauppa**-pikavälilehdessä, että valuuttakoodi on **USD**. Jos valitset **Laskun valuutan koodi** -kentässä USD, projekti laskutetaan Yhdysvaltain dollareina ja vain suunnitellaan CRONUSIN paikallisena valuuttana.  

 Voit mukauttaa asiakkaiden hinnoittelun työkohtaiseksi sopimuksissa, jotka olet määrittänyt. Seuraavassa toimenpiteessä projektipäällikkö määrittää kustannukset Mariannen ajasta, määrittää tarvittavan ohjelmiston hinnan ja lisää matkakustannukset, jotka asiakas on suostunut maksamaan.  

### <a name="to-customize-pricing"></a>Mukauta hinnoittelu  

1.  Valitse projektikortissa **Resurssi**-toiminto.  
2.  Lisää seuraavat tiedot **Projektiresurssien hinnat** -ikkunaan:  

    -   **Koodi**: **Marianne**  
    -   **Yksikköhinta**: **20**  

3.  Valitse **OK**-painike ikkunan sulkemiseksi.  
4.  Valitse **Nimike**-toiminto.  
5.  Lisää seuraavat tiedot ja mukautettu hinta **Projektinimikkeiden hinnat** -ikkunaan:  

    1.  **Nimikkeen nro**: **80201 (Grafiikkaohjelma)**  
    2.  **Yksikköhinta**: **200**  

6.  Sulje ikkuna valitsemalla **OK**.  
7.  Valitse **KP-tili**-toiminto.  
8.  Anna **Projektin kirjanpitotilin hinnat** -ikkunassa seuraavat tiedot ja matkan kustannus, jonka asiakas on luvannut maksaa, plus 25 %:  

    1.  **KP-tili**: **8430 (Matka)**  
    2.  **Yksikkökustannustekijä**: **1,25**.  

9. Valitse **OK**-painike ikkunan sulkemiseksi.  

 Projektin määrittämisen viimeisiä askeleita ovat projektin tehtävien sekä jokaisen tehtävän suunnittelurivien lisääminen. Nämä suunnittelurivit määrittävät, mitä asiakkaalta laskutetaan.  

### <a name="to-add-job-tasks"></a>Työtehtävien lisääminen  

1.  Valitse uuden projektin **Projekti**-kortissa **Projektitehtävärivit**-toiminto.  
2.  Seuraavassa taulukossa kuvaillaan tiedot, jotka tulisi syöttää kenttiin.  

    |Projektitehtävän nro|Description|Projektitehtävätyyppi|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Konsulttiapua salin sisustukseen|Alkusumma|  
    |1010|Konsultointitapaaminen asiakkaan kanssa|Kirjaus|  
    |1020|Kehittäminen|Kirjaus|  
    |1090|Konsultointi yhteensä|Loppusumma|  

3.  Osoittaaksesi, että jotkin tehtävät ovat muiden tehtävien alaluokkia, valitse **Toiminnot** -välilehdessä **Funktiot** -ryhmässä **Sisennä projektitehtävät**.  

 Suunnittelurivi voi olla jokin seuraavista tyypeistä:  

-   **Aikataulu**: Lisätty aikatauluun, mutta ei laskutettu.  
-   **Sopimus**: laskutettu, mutta ei lisätty aikatauluun.  
-   **Aikataulu ja sopimus**: laskutettu ja lisätty aikatauluun.  

 Tässä vaihekuvauksessa projektipäällikkö käyttää **Sekä aikataulu että sopimus** -toimintoa. Hän luo tehtävälle 1010 kolme suunnitteluriviä ja tehtävälle 1020 kaksi suunnitteluriviä.  

### <a name="to-create-planning-lines"></a>Luo suunnittelurivit  

1.  Valitse ensin rivi 1010 ja sitten **Projektin suunnittelurivit** -toiminto. Lisää seuraavat tiedot:  

     **Rivi 1**  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Suunnittelupäivämäärä**:**(kuluva päivämäärä)**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro:**: **Marianne**  
    -   **Määrä**: **40**  

     **Rivi 2**  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Suunnittelupäivämäärä**:**(kuluva päivämäärä)**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro**: **Teemu**  
    -   **Määrä**: **40**  

     **Rivi 3**  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Suunnittelupäivämäärä**:**(kuluva päivämäärä)**  
    -   **Tyyppi**: **KP-tili**  
    -   **Nro**: **8430 (Matka)**  
    -   **Määrä**: **2**  
    -   **Yksikkökustannus**: **400**  

2.  Valitse **OK**-painike ikkunan sulkemiseksi. Summat on päivitetty **Projektitehtävärivit** -ikkunassa.  
3.  Valitse ensin rivi 1020 ja sitten **Projektin suunnittelurivit** -toiminto. Anna seuraavat tiedot:  

     **Rivi 1**  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Suunnittelupäivämäärä**:**(kuluva päivämäärä)**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro:**: **Marianne**  
    -   **Määrä**: **80**  

     **Rivi 2**  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Suunnittelupäivämäärä**:**(kuluva päivämäärä)**  
    -   **Tyyppi**: **Nimike**  
    -   **Nro**: **80201 (Grafiikkaohjelma)**  
    -   **Määrä**: **1**  

4.  Valitse **OK**-painike ikkunan sulkemiseksi. Summat on päivitetty **Projektitehtävärivit** -ikkunassa.  

## <a name="calculating-remaining-usage"></a>Jäljellä olevan käytön laskeminen  
 Marianne, projektiryhmän jäsen, on tehnyt työtä projektissa jonkin aikaa ja haluaa rekisteröidä omat tuntinsa ja käytön projektissa. Työmäärä ja käyttö eivät ole ylittäneet asiakkaan kanssa sovittua määrää. Hän laskee **Laske jäljellä oleva käyttö** -eräajon avulla projektin jäljellä olevan käytön projektipäiväkirjaan. Erätyö laskee kullekin tehtävälle nimikkeiden, resurssien ja kirjanpitokustannusten suunnitellun käytön ja projektitapahtumiin kirjatun todellisen käytön välisen eron. Jäljellä oleva käyttö tulee näkyviin projektipäiväkirjaan, josta sen voi kirjata.  

### <a name="to-calculate-remaining-usage"></a>Jäljellä olevan käytön laskeminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa **Projektipäiväkirjan erät** -luettelo napsauttamalla **Projektipäiväkirja**-ikkunan **Erän nimi** -kentässä. Valitse **Tricia**-projektipäiväkirjan erä.  
3.  Valitse **Laske jäljellä oleva käyttö** -toiminto.  
4.  Valitse **Laske projektin jäljellä oleva käyttö** -kentän **Projektitehtävä**-pikavälilehdessä **Projektinro**-kenttä ja valitse sitten asianmukainen projektin numero, tyypillisesti projekti J00010.  
5.  Kirjoita **Vaihtoehdot**-pikavälilehden **Asiakirjan nro** -kenttään **J00001**. Tämä helpottaa kirjauksen myöhempää jäljittämistä.  
6.  Määritä kirjauspäivämääräksi kuluva päivä.  
7.  Valitse **OK**-painike. Kaikki Thomasin projektipäiväkirjaan luomista suunnitteluriveistä johdetut ehdotetut rivit tuodaan.  
8.  Valitse vahvistusikkunassa **OK**-painike. Luodut rivit lisätään projektipäiväkirjaan.  
9. Varmista, että kaikki asiakirjan numerot ovat J00001. Valitse sitten **Kirjaa**-toiminto. Valitse **Kyllä** vahvistaaksesi kirjauksen.  
10. Rivit kirjataan. Valitse **OK**-painike ikkunoiden sulkemiseksi.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Projektin myyntilaskun luominen ja kirjaaminen  
 Seuraavaksi Marianne voi luoda uuden laskun koko projektia tai projektin osaa varten. Voit myös liittää laskun saman asiakkaan toiseen, samaa projektia koskevaan laskuun. Tällöin hän laskuttaa koko projektista, koska projekti on nyt valmis.  

### <a name="to-create-a-job-sales-invoice"></a>Projektin myyntilaskun luominen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin aiemmin luotu projekti ja sitten **Luo projektin myyntilasku** -toiminto.  
3.  Tyhjennä **Projektitehtävä**-pikavälilehden **Projektitehtävänro**-kentässä kaikki suodattimet, jotta työ voidaan laskuttaa. Valitse **Projektinro**-kentässä asianmukainen projekti.  
4.  Anna **Vaihtoehdot**-pikavälilehdessä kirjauspäivämäärä ja määritä, haluatko luoda yhden laskun tehtävää kohti vai yhden laskun kaikille tehtäville.  
5.  Valitse **OK**-painike luodaksesi laskun ja valitse sitten **OK**-painike vahvistusikkunassa.  

 Kun Tiina on luonut laskun, hän voi käyttää sitä **Myynti ja markkinointi** -kohdassa  **Tilauksen käsittely** -osassa ja suorittaa lisätoimia.  

### <a name="to-post-a-new-sales-invoice"></a>Uuden myyntilaskun kirjaaminen  

1.  Valitse ![Etsi sivu tai raportti(media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake")] -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Avaa sen asiakkaan lasku, jonka asiakkaan numero on 01445544. Suunnitteluriveiltä lisätyt tiedot tulevat näkyviin.  
3.  Valitse **Kirjaa**-toiminto. Vahvista kirjaus valitsemalla **Kyllä**.  

### <a name="to-view-the-posted-invoice"></a>Kirjatun laskun tarkasteleminen  

1.  Avaa projekti ja valitse sitten **Projektin suunnittelurivit** -toiminto.  
2.  Valitse ensin jokin laskutettu suunnittelurivi ja sitten **Myyntilasku/hyvityslasku**-toiminto.
3. Valitse **Projektin laskut** -ikkunassa **Avaa myyntilasku/hyvityslasku** -toiminto.  

 Mariannella on kysyttävää tähän projektiin liittyvistä hinnoista, kustannuksista ja tuotoista, joten hän arvioi näitä tietoja ovat uudesta **Tilasto**-ikkunasta.  

### <a name="to-open-the-statistics-window"></a>Tilasto-ikkunan tuominen näkyviin  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Tilastot**-toiminto. Voit tarkastella yksityiskohtaisia tietoja projektihinnoista, kustannuksista ja paikallisista ja ulkomaisista valuuttojen voitoista.  
3.  Valitse **Sulje**-painike **Projektin tilastot** -ikkunan sulkemiseksi.  

## <a name="handling-fixed-prices"></a>Kiinteiden hintojen käsitteleminen  
 CRONUKSEN kanssa on tehty sopimus kokoushuoneiden määrittämiseksi. Projektipäällikkö Thomas tarvitsee hyvän yleiskäsityksen projektin edellyttämistä tehtävistä sekä kuhunkin tehtävään liittyvistä budjetoiduista ja kertyneistä kustannuksista. Tarkoitus on myös selvittää projektin sopimuksenmukainen kokonaishinta sekä tähän mennessä laskutettu summa. Asiakkaan kanssa on päästy sopimukseen projektin kiinteästä hinnoittelusta.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Kiinteän hinnoittelun hallinta projekteissa  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin **Espoo**-projektinumero ja sitten **Projektitehtävärivit**- toiminto.  
3.  Valitse rivi 1120 ja napsauta **Aikataulu (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella **Siirtyminen**.  

     Projektin suunnitteluluetteloa tarkasteltaessa päädytään siihen, että myös Mariannea tarvitaan 30 tunniksi projektin tässä vaiheessa. Asiakkaan kanssa sovitaan kiinteästä hinnasta.  

4.  Valitse **Projektitehtävärivit**-ikkunassa ensin rivi 1120 ja sitten **Projektin suunnittelurivit** -toiminto.  
5.  Valitse **Uusi**, jos haluat luoda uuden rivin, jolla ovat seuraavat tiedot:  

    -   **Rivityyppi**: **Sekä aikataulu että sopimus**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro:**: **Marianne**  
    -   **Määrä**: **30**  

7.  Valitse **OK**-painike ikkunan sulkemiseksi.  
8.  Kaksoisnapsauta **Aikataulu (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella ja valitse **Siirtyminen** uudelleen **Projektitehtävärivit**-ikkunassa. Tarkastele muutoksia aikatauluun. Kuten huomaat, aikatauluun on lisätty 30 tuntia.  
9. Valitse **OK**-painike ikkunoiden sulkemiseksi.  

 Kun Marianne on lisätty aikatauluun tämän tehtävärivin osalta, hän työskentelee projektissa 25 tuntia. Hän lisää nämä tunnit projektipäiväkirjaan.  

### <a name="to-enter-hours-in-the-job-journal"></a>Tuntien lisääminen projektipäiväkirjaan  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektipäiväkirjat** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Lisää seuraavat tiedot uudelle riville:  

    -   **Rivityyppi**: **(tyhjä)**  
    -   **Kirjauspvm**: **(kuluva päivämäärä)**.  
    -   **Asiakirjan nro**:**J00002**  
    -   **Projektinro**: **Espoo**  
    -   **Projektitehtävänro**: **1120**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro:**: **Marianne**  
    -   **Määrä**: **25**  

3.  Valitse **Kirjaa**-toiminto.  

     Muutamaa päivää myöhemmin Marianne tekee vielä 10 tuntia töitä projektissa. Hän on nyt tehnyt töitä yhteensä 35 tuntia. Koska asiakkaan kanssa on sovittu vain 30 tunnista, tunneista vain viisi laskutetaan asiakkaalta. Marianne lisää manuaalisesti aikatauluun viisi lisätuntia, jotka hän on työskennellyt.  

4.  Valitse **Projektipäiväkirja**-ikkunassa **Laske jäljellä oleva käyttö**-toiminto.  
5.  Lisää seuraavat tiedot **Laske projektin jäljellä oleva käyttö** -ikkunan **Vaihtoehdot**-pikavälilehteen:  

    -   **Asiakirjan nro**:**J00003**  
    -   **Kirjauspvm**: **(kuluva päivämäärä)**.  

6.  Lisää seuraavat tiedot **Projektitehtävä**-pikavälilehteen:  

    -   **Projektinro**: **Espoo**  
    -   **Projektitehtävänro**: **1120**  

     Suorita laskenta valitsemalla **OK**. Mariannen työpäivässä on jäljellä viisi tuntia. **Rivityyppi**-kenttä on tyhjä sen merkiksi, että vain käyttö pysyy kirjattuna, koska työ on jo ajoitettu.  

7.  Luo **Projektipäiväkirjan erät** -ikkunassa uusi rivi, jolla on seuraavat tiedot: Varmista, että projektinumerot ovat järjestyksessä seuraavina niistä, joita olet jo käyttänyt:  

    -   **Rivityyppi**: **Aikataulu**  
    -   **Projektinro**: **Espoo**  
    -   **Projektitehtävänro**: **1120**  
    -   **Tyyppi**: **Resurssi**  
    -   **Nro:**: **Marianne**  
    -   **Määrä**: **5**  

     Kun käytät **Aikataulu**-rivityyppiä, ohjelma päivittää ajoitetut kustannukset ja hinnat päivittämättä asiakkaalta laskutettavia sopimuskustannuksia ja -hintoja.  

8.  Valitse **Kirjaa**-toiminto. Sulje ikkuna valitsemalla **OK**.  
9. Avaa **Projektit** -luettelo.  
10. Valitse ensin ESPOO-projekti ja sitten **Projektitehtävärivit**-toiminto.  
11. Valitse rivi 1120 ja napsauta **Aikataulu (kokonaiskustannus)** -kentän summaa hiiren kakkospainikkeella. Tarkastele tietoja valitsemalla **Siirtyminen**.  

     Muutokset lisätään automaattisesti projektitehtävänumeron 1120 riville. Marianne on lisännyt viisi lisätuntia aikataulun ajoitetun työn kokonaiskustannukseen.  

12. Valitse **Sulje**-painike ikkunan sulkemiseksi.  
13. Napsauta summaa **Sopimus (kokonaiskustannus)** -kentässä hiiren kakkospainikkeella ja tarkastele tietoja valitsemalla **Siirtyminen**.  

     Kun sopimuksen kokonaishintaa tarkastellaan taulukossa, vain alkuperäiset, sopimuksenmukaiset 30 tuntia ovat mukana, koska tästä on asiakkaan kanssa sovittu.  

## <a name="copying-jobs"></a>Projektien kopioiminen  
 Thomas on päässyt Tinayhtymä Oy -asiakkaan kanssa sopimukseen kymmenen neuvotteluhuoneen sisustamisesta. Sopimus muistuttaa aiempaa työtä. Tämän vuoksi aikaisemman työn kopiointi säästää aikaa.  

 Valitse **Kopioi projekti** -ikkunassa kopioitavat projekti- ja tehtävärivit. Voit myös valita lähdeprojektin tapahtumien kopioinnin, joka luo suunnittelurivit perustuen todelliseen käyttöön, tai voit kopioida lähdeprojektin suunnittelurivit, mikä kopioi alkuperäiset suunnittelurivit uuteen työhön. Voit sitten valita suunnittelurivin tai nimiketapahtuman rivityypin, jonka haluat sisällyttää, valitsemalla vain sen, millä on merkitystä tälle uudelle työlle. Lopuksi voit valita kopioitavan projektin ja määrittää, kopioidaanko hinnat ja määrät myös.  

### <a name="to-copy-a-job"></a>Projektin kopioiminen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Projektit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi projekti valitsemalla **Uusi**-toiminto. Anna seuraavat tiedot:  

    -   **Kuvaus**: **10 kokoushuoneen sisustaminen**  
    -   **Laskutusasiakkaan nro**: **20000**  

3.  Valitse **Kopioi projektitehtävät kohteesta** -toiminto.  
4.  Anna seuraavat tiedot **Kopioi projektitehtävät** -ikkunassa:  

    -   **Projektinro**: **Espoo**  
    -   **Ensimmäisen projektitehtävän numero**: **1000**  
    -   **Lähde**: **Projektin suunnittelurivit**  
    -   **Sisällytä suunnittelurivin tyyppi**: **Aikataulu + Sopimus**  
    -   **Viimeisen projektitehtävän numero**: **Espoo 10 kokoushuoneen sisustaminen**.  
    -   Valitse **Kopioi dimensiot**- ja **Kopioi määrä** -kentät.  

5.  Valitse **OK**-painike kopioidaksesi työn ja valitse sitten **OK**-painike sulkeaksesi vahvistusikkunan.  

     Kahden työn hintoja, työn tehtävärivejä ja töiden suunnittelurivejä vertaamalla näet, että tiedot on kopioitu oikein.  

## <a name="making-payments-by-installments"></a>Maksujen suorittaminen osamaksuina  
 CRONUS on juuri ottanut hoitaakseen suuren projektin, joka kestää vuoden. Koska siihen täytyy kohdistaa huomattava määrä resursseja, asiakkaalta halutaan ennakkomaksu, maksu projektin puolivälissä ja lopullinen maksu projektin valmistuessa.  

### <a name="to-set-up-a-new-account"></a>Uuden tilin luominen  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Luo uusi kortti valitsemalla **Tilikartta**-ikkunassa **Uusi**.  
3.  Lisää seuraavat tiedot uuteen **KP-tilin korttiin**:  

    -   **Nro**: **6630**  
    -   **Nimi**: **Projektin maksu**.  

4.  Täytä **Kirjaus**-pikavälilehdessä **Yleinen tuotteen kirjausryhmä** -kenttä, valitse **SEKAL**. Valitse **OK**-painike ikkunan sulkemiseksi.  
5.  Valitse **Tilikartta**-ikkunassa ensin **Projektin nro 6630 maksu** ja sitten **Sisennä tilikartta** -toiminto. Vahvista valitsemalla **Kyllä**.  

 Seuraavissa ohjeissa neuvotaan, miten luot uuden projektin, asetat hinnoittelun ja määrittelet osamaksuvaihtoehdon. Projektitehtäväriveillä voit luoda tiettyjä rivejä, jotka on tarkoitettu yksinomaan osamaksuja varten. Kaikki projektin valmistuneet työt, jotka on lisätty aikatauluun, lisätään käyttöriveille. Jokaisen suunnittelurivin maksutehtävärivin rivityyppi on Sopimus. Se tarkoittaa, että asiakasta tullaan laskuttamaan. Syötä uusi rivi ennakkomaksulle. Käytön tehtäväriveillä voit lisätä tässä projektissa käytettyjen, aikataulua pidentävien nimikkeiden ja resurssien tietoja. Tällaisia nimikkeitä ja resursseja ovat esimerkiksi projektissa käytetyt työntekijätunnit ja nimikkeet.  

### <a name="to-make-a-payment-by-installment"></a>Osamaksujen käyttäminen  

1.  Luo uusi projekti.  
2.  Täytä seuraavat tiedot **projekti**-korttiin:  

    -   **Kuvaus**: **Vastaanottoalueen uusiminen**  
    -   **Laskutusasiakkaan nro**: **30000**  
    -   **Projektin kirjausryhmä**: **As. määr.**  
    -   **KET-menetelmä**: **Kustannusarvo**  

3.  Valitse projektikortissa **Resurssi**-toiminto. Anna seuraavat tiedot:  

    -   **Koodi**: **Marianne**  
    -   **Yksikköhinta**: **10**  

     Sulje ikkuna valitsemalla **OK**.  

4.  Valitse **Projekti**-kortissa **Projektitehtävärivit**-toiminto.  

     Seuraavassa taulukossa kuvaillaan luotavia rivejä.  

    |Rivi|Projektitehtävän nro|Description|Projektitehtävätyyppi|  
    |----------|------------------|---------------------------------------|-------------------|  
    |1|1000|Maksu - ennakkomaksu|Kirjaus|  
    |2|2000|Käyttö|Kirjaus|  
    |3|3000|Maksu - välimaksu|Kirjaus|  
    |4|4000|Maksu - loppumaksu|Kirjaus|  

5.  Valitse **Projektitehtävärivit**-ikkunassa ensin tehtävä 1000 ja sitten **Projektin suunnittelurivit** -toiminto.  
6.  Luo suunnittelurivi, jossa on seuraavat tiedot:  

    -   **Rivityyppi**: **Sopimus**  
    -   **Suunnittelupäivämäärä**: **(kuluva päivämäärä)**  
    -   **Tyyppi**: **KP-tili**  
    -   **Nro**: **6630**  
    -   **Määrä**: **1**  
    -   **Yksikköhinta**: **5000**  

     Valitse **OK**-painike ikkunan sulkemiseksi.  

7.  Valitse **Projektitehtävärivit**-ikkunassa **tehtävä 2000** ja avaa sen **Projektin suunnittelurivit**.  

     Seuraavassa taulukossa kuvaillaan luotavia suunnittelurivejä.  

    |viivakaavio.|Rivityyppi|Suunnittelupäivämäärä|Tyyppi|Nro|määrä.|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Aikataulu|(tämän päivän päivämäärä)|Resurssi|Marianne|120|  
    |2|Aikataulu|(tämän päivän päivämäärä)|Nimike|70104|10|  

     Valitse **OK**-painike ikkunan sulkemiseksi. Suunnitellut summat näkyvät päivitettyinä **Projektitehtävärivit**-ikkunassa.  

8.  Valitse **Projektitehtävärivit**-ikkunassa **tehtävä 3000**.  
9. Luo suunnittelurivi, jossa on seuraavat tiedot:  

    -   **Rivityyppi**: **Sopimus**  
    -   **Suunnittelupäivämäärä**: **tulav päivämäärä**  
    -   **Tyyppi**: **KP-tili**  
    -   **Nro**: **6630**  
    -   **Määrä**: **1**  
    -   **Yksikköhinta**: **5000**  

     Valitse **OK**-painike ikkunan sulkemiseksi.  

10. Luo vastaava suunnittelurivi työtehtävälle 4000.  

 Kun tehtävä- ja suunnittelurivit on nyt lisätty, Thomas luo laskun ensimmäistä maksua varten. Nämä toimet tehdään projektitehtävän riveiltä, jotta laskussa on varmasti vain ensimmäisen maksun rivit. Voit avata myyntitilauksen suunnitteluriveiltä tai tehtäväriveiltä.  

### <a name="to-create-an-invoice"></a>Luo lasku  

1.  Valitse **Projektitehtävärivit**-ikkunassa ensin rivi 1000 ja sitten **Luo myyntilasku** -toiminto.  
2.  Määritä **Luo myyntilasku** .ikkunassa nykyinen päivämäärä kirjauspäivämääräksi, määritä **Tehtäväkohtainen** ja valitse **OK**, jos haluat luoda oletustiedot sisältävän laskun. Valitse **OK**-painike vahvistusikkunan sulkemiseksi.  
3.  Valitse **Myyntilasku/hyvityslasku**-toiminto. Myyntilaskussa näkyy, että vain ennakkomaksu on mukana laskussa. Voit nyt lähettää tämän asiakkaalle sopimuksen mukaisesti.  

## <a name="next-steps"></a>Seuraavat vaiheet  
 Tämä vaihekuvaus on ohjannut sinut läpi tiettyjen perusvaiheiden töiden [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman parissa. Olet oppinut kuinka luodaan uusi työ, kuinka työ kopioidaan ja kuinka maksuja käsitellään. Olet myös nähnyt esityksen siitä, miten voit luoda laskuja ja seurata tunteja.  

## <a name="see-also"></a>Katso myös  
 [Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)   
 [Projektinhallinnan määrittäminen](projects-setup-projects.md)   
 [Toimintaohje: Resurssien käyttäminen](projects-how-use-resources.md)   
 [Toimintaohje: Edistymisen ja suorituskyvyn valvonta](projects-how-monitor-progress-performance.md)   
 [Toimintaohje: Projektien laskuttaminen](projects-how-invoice-jobs.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
