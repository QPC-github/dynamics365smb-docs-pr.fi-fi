---
title: Kustannustapahtumien siirtäminen ja kirjaaminen
description: 'Ennen kuin voit määrittää kustannusten kohdistamisen, sinun on ymmärrettävä eri lähteet, joista kustannustapahtumat tulevat.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="transferring-and-posting-cost-entries" />Kustannustapahtumien siirtäminen ja kirjaaminen

Ennen kuin voit määrittää kustannusten kohdistamisen, sinun on ymmärrettävä, miten kustannustapahtumat tulevat seuraavista lähteistä:  

- Pääkirjanpidon tapahtumien automaattinen siirto.  
- Manuaalinen kustannuskirjaus pellkille kustannustapahtumille, sisäisille kuluille ja manuaaliset kohdistukset.  
- Automaattinen kohdistusten kirjaus todellisille kustannuksille.  
- Siirrä budjettitapahtumat toteumaan.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries" />Kriteerit pääkirjanpidon tapahtumien siirtämiseksi kustannustapahtumiin

On tärkeää ymmärtää ehdot, joiden mukaan pääkirjanpidon tapahtumat siirretään kustannustapahtumiin. Siirron aikana **Siirrä KP-tapahtumat kustannuslaskentaan** -eräajo käyttää seuraavia kriteerejä määrittääkseen, jos ja miten pääkirjanpidon tapahtumat siirretään.  

Kirjanpitotapahtumat siirretään, jos:  

- Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa tai kustannuskohdetta.  
- Tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta. Kustannuspaikka ratkaisee asian näiden tapahtumien kohdalla. Näin vältetään tilanne, jossa kustannustyyppi näkyy sekä kustannuskohteessa että kustannuspaikassa ja näin ollen ne lasketaan tilastoihin kahdesti.  
- Asiakirjan numeroa ei ole tapahtumissa, joten kustannustapahtumissa näytetään asiakirjanumeron kohdalla 0000.  
- Tapahtumat siirretään kustannustyypille, jolla yhdistettyjä tapahtumia voidaan käsitellä, ja tapahtumat siirretään yhdistettynä joko kuukausittain tai päivittäin.  

Kirjanpitotapahtumia ei siirretä, jos:  

- Tapahtumilla on dimensioarvot, jotka eivät vastaa kustannuspaikkaa tai kustannuskohdetta.  
- Tapahtumien summa on nolla.  
- Tapahtumissa on poistettu KP-tili.  
- Tapahtumissa on KP-tili, joka ei ole **Tuloslaskelma**-tyyppiä  
- Tapahtumissa on KP-tili, jolle ei ole määritetty kustannustyyppiä.  
- Tapahtumien kirjauspäivämäärä on ennen **KP-siirron alkamispäivämäärää**.  
- Tapahtumille on kirjattu sulkemispäivämäärä. Tässä on tyypillisiä tapahtumia, jotka palauttavat tuloslaskelman saldon vuoden lopussa.

## <a name="transferring-general-ledger-entries-to-cost-entries" />Pääkirjanpidon tapahtumien siirtäminen kustannustapahtumiin

Voit siirtää pääkirjanpidon tapahtumat kustannustapahtumiin.  

Ennen kuin suoritat prosessin pääkirjanpidon merkintöjen siirtämiseksi kustannusmerkintöihin, sinun täytyy laatia siirto manuaalisen korjauksen kirjaamisen välttämiseksi.  

### <a name="to-prepare-the-transfer" />Valmistele siirto

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannuslaskennan asetukset** ja valitse sitten vastaava linkki.  
2.  Varmista **Kustannuslaskennan asetukset** -sivulla, että **KP-siirron alkamispäivämäärä** -kenttään on määritetty oikea arvo.  
3.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kustannustyyppikartta** ja valitse sitten vastaava linkki.  
4.  Varmista **Kustannustyyppikortti** -sivulla, että kunkin kustannustyypin **KP-tilien väli** -kenttä on linkitetty oikein, jotta tapahtumat voidaan ottaa pääkirjanpidosta.  
5.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tilikartta** ja valitse sitten vastaava linkki.  
6.  Tarkista, että kunkin käsiteltävän pääkirjanpidon tilin **KP-tilin kortti** -sivulla, että **Kustannustyypin numero** -kenttä on linkitetty oikein kustannuslajiin. Lisätietoja on kohdassa [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md).  
7.  Tarkista, että kaikilla kyseessä olevilla pääkirjanpidon tapahtumilla on dimensioarvot, jotka vastaavat kustannuspaikkaa ja kustannuskohdetta.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries" />Siirrä pääkirjanpidon tapahtumat kustannustapahtumiin

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Siirrä KP-tapahtumat kustannuslaskentaan** ja valitse sitten vastaava linkki.  
2.  Aloita siirto valitsemalla **Kyllä**. Prosessi siirtää kaikki pääkirjanpidon tapahtumat, joita ei ole jo siirretty.  

Siirron aikana prosessi luo yhteyksiä tapahtumiin **Kustannustapahtuma** -taulukossa ja **Kustannusrekisteri** -taulukossa. Tämä mahdollistaa kustannustapahtumien lähteen jäljittämisen.

## <a name="automatic-transfer-and-combined-entries" />Automaattinen siirto ja yhdistetyt tapahtumat

Voit siirtää kustannuslaskennassa pääkirjanpitotapahtumat kustannustyyppiin yhdistetyn kirjauksen avulla. Voit määrittää, jos kustannustyyppi vastaanottaa yhdistettyjä tapahtumia **Yhdistä tapahtumat** -kentässä kustannustyypin määrityksessä. Seuraavassa taulukossa kuvaillaan eri asetukset.  

|Yhdistä tapahtumat|Description|  
|---------------------|-----------------|  
|Ei yhtään|Kukin pääkirjanpidon tapahtuma siirretään yksitellen vastaavaan kustannustyyppiin.|  
|Päivä|Kirjanpitotapahtumat, joilla on sama kirjauspäivämäärä, siirretään vastaavaan kustannustyyppiin yhtenä tapahtumana.|  
|Kuukausi|Saman kalenterikuukauden aikana kaikki pääkirjanpidon tapahtumat siirretään yhtenä tapahtumana vastaavaan kustannustyyppiin.|  

> [!IMPORTANT]  
>  Jos olet valinnut **Automaattinen siirto kirjanpidosta** -valintaruudun **Kustannuslaskennan asetukset** -sivulla, [!INCLUDE[prod_short](includes/prod_short.md)] päivittää kustannuslaskennan jokaisen kirjanpidon kirjauksen jälkeen. Yhdistetyt tapahtumat eivät ole mahdollisia.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries" />Tulokset siirrettäessä pääkirjanpidon tapahtumat kustannustapahtumiin

Kun pääkirjanpidon tapahtumia siirretään kustannustapahtumiin, [!INCLUDE[prod_short](includes/prod_short.md)] luo yhteyksiä tapahtumiin **KP-tapahtuma**-, **Kustannustapahtuma**- ja **Kustannusrekisteri**-taulukossa. Tämä mahdollistaa pääkirjanpidon tapahtumien ja kustannustapahtumien välisten yhteyksien jäljittämisen.  

### <a name="general-ledger-entries" />Pääkirjanpidon tapahtumat

[!INCLUDE[prod_short](includes/prod_short.md)] täyttää kaikkien kustannuslaskentaan siirrettävien pääkirjanpidon tapahtumien kustannusten **Tapahtumanro**-kentän.  

### <a name="cost-entries" />Kustannustapahtumat

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa vastaavan pääkirjanpidon tapahtuman jokaisen kustannustapahtuman numeron **Kustannustapahtuma**-ikkunan **KP-tapahtuman nro** -kenttään.  

[!INCLUDE[prod_short](includes/prod_short.md)] tallentaa yhdistettyjen kustannustapahtumien pääkirjanpidon viimeisen tapahtuman tapahtumanumeron (tapahtuma, jonka numero on kaikkein suurin).  

**Kustannustapahtuma**-taulukon **KP-tili**-kentässä on KP-tilin numero, jolta kustannustapahtuma on peräisin.  

[!INCLUDE[prod_short](includes/prod_short.md)] siirtää yksittäisten kustannustapahtumien kirjaustekstin pääkirjanpidon tapahtumasta **Kuvaus**-tekstikenttään. Tekstikenttä osoittaa, että yhdistetyt tapahtumat siirretään yhdistettyinä tapahtumina. Esimerkiksi vuoden 2013 lokakuun yhdistetyn tapahtuman teksti voi olla **Yhdistetyt tapahtumat, lokakuu 2013**.  

### <a name="cost-register" />Kustannusrekisteri

**Kustannusrekisteri**-taulukkoon [!INCLUDE[prod_short](includes/prod_short.md)] luo merkinnän lähteen siirtämisestä pääkirjanpidosta. Tapahtuma kirjaa siirrettyjen pääkirjanpidon tapahtumien ensimmäisen ja viimeisen tapahtumanumeron sekä luotujen kustannustapahtumien ensimmäisen ja viimeisen tapahtumanumeron.

## <a name="see-related-microsoft-trainingtrainingmodulestransfer-gl-entries-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/transfer-gl-entries-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

 [Tietoja kustannuslaskennasta](finance-about-cost-accounting.md)  
 [Kustannuslaskennan määrittäminen](finance-set-up-cost-accounting.md)  
 [Kustannusten määrittäminen ja kohdistaminen](finance-define-and-allocate-costs.md)  
 [Kustannuslaskenta](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
