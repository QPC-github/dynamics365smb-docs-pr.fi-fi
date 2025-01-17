---
title: Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen | Microsoft Docs
description: Sähköpostin liitetiedostojen lähettämisen sijaan liiketoiminta-asiakirjoja voi lähettää ja vastaanottaa sähköisesti.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-electronic-document-sending-and-receiving" />Sähköisten asiakirjojen vastaanottamisen ja lähettämisen määrittäminen

Sähköpostin liitetiedostojen lähettämisen sijaan liiketoiminta-asiakirjoja voi lähettää ja vastaanottaa sähköisesti. Sähköisellä asiakirjalla tarkoitetaan sitä, että liiketoiminta-asiakirjaa (kuten toimittajan laskua) vastaava standardin\-mukainen tiedosto voidaan vastaanottaa ja muuntaa ostolaskuksi [!INCLUDE[prod_short](includes/prod_short.md)]issa. Document exchange -palveluiden ulkoinen palveluntarjoaja suorittaa kahden liikekumppanin välisen sähköisten asiakirjojen vaihdon. [!INCLUDE[prod_short](includes/prod_short.md)]in yleinen versio tukee sähköisten laskujen ja hyvityslaskujen lähettämistä ja vastaanottamista PEPPOL-muodossa. Suurimmat asiakirjojen vaihtopalveluiden tarjoajat tukevat tätä muotoa. Tavallisin document exchange -palveluiden tarjoaja on esimääritetty, ja se on valmis määritettäväksi yrityksellesi.  

Ulkoinen OCR (Optical Character Recognition) -palvelu voi luoda saapuvia asiakirjoja vastaavista PDF- tai kuvatiedostoista sähköisiä asiakirjoja, jotka voit sitten muuntaa tiedostotietueiksi [!INCLUDE[prod_short](includes/prod_short.md)]issa samalla tavalla kuin teet sähköisille PEPPOL-asiakirjoille. Kun esimerkiksi saat PDF-muotoisen laskun toimittajalta, voit lähettää sen OCR-palveluun **Saapuvat asiakirjat** -sivulta. Saat tiedoston muutamassa sekunnissa takaisin sähköisenä laskuna, jonka voit muuntaa toimittajan ostolaskuksi. Jos lähetät tiedoston OCR-palveluun sähköpostitse, uusi saapuvan asiakirjan tietue luodaan automaattisesti, kun saat sähköisen asiakirjan takaisin.  

Sähköinen **PEPPOL**-asiakirjaformaatti on määritelty ennalta, jotta voit lähettää laskuja ja hyvityslaskuja PEPPOL-muodossa. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, asiakkaat, nimikkeet ja mittayksiköt. Näitä käytetään liiketoimintakumppanien ja kohteiden tunnistamisessa, kun [!INCLUDE[prod_short](includes/prod_short.md)] -kentissä olevat tiedot muunnetaan lähtevän tiedoston elementeiksi. Lopuksi sinun on valittava **Sähköinen asiakirjamuoto** -sivulla muoto jokaiselle asiakkaalle, jolle lähetät PEPPOL-muotoisia sähköisiä asiakirjoja. Lisätietoja on kohdassa [Sähköisten asiakirjojen lähettäminen](sales-how-to-send-electronic-documents.md).  

**PEPPOL - Lasku**- ja **PEPPOL – Hyvityslasku** -tietojenvaihdon määritelmät ovat määritelty ennalta, jotta voit vastaanottaa sähköisiä laskuja ja hyvityslaskuja PEPPOL-muodossa. Aluksi on määritettävä joitakin perustietoja, kuten yrityksen tiedot, toimittajat, nimikkeet ja mittayksiköt. Niiden avulla tunnistetaan liikekumppaneja ja nimikkeitä, kun saapuvassa asiakirjatiedostossa olevien elementtien tiedot muunnetaan [!INCLUDE[prod_short](includes/prod_short.md)]in kentiksi. Lopuksi sinun on valittava **Saapuvat asiakirjat** -sivulla tiedonsiirtomääritys jokaiselle saapuvalle sähköiselle asiakirjalle, jonka haluat muuntaa [!INCLUDE[prod_short](includes/prod_short.md)]in ostoasiakirjaksi.  

**OCR – Lasku** -tiedonsiirtomääritys on valmiiksi määritetty, joten voit vastaanottaa OCR-palvelussa luotuja sähköisiä asiakirjoja. Saat esimerkiksi laskun sähköisenä OCR-tiedostona, kun asetat master-päivämäärän ja sitten käsittelet asiakirjan kuin vastaanottaessasi sähköisen PEPPOL-asiakirjan. Lisätietoja on kohdassa [PDF- ja kuvatiedostojen muuntaminen sähköisiksi asiakirjoiksi OCR-palvelun avulla](across-how-use-ocr-pdf-images-files.md).  

Esimääritetyt palvelut tiedostojen vaihtoon ja OCR:ään on oltava käytössä, ennen kuin voit lähettää tai vastaanottaa. Lisätietoja on kohdassa [Document Exchange -palvelun määrittäminen](across-how-to-set-up-a-document-exchange-service.md).  

Ohjeaihe sisältää seuraavat toimintosarjat:  

* Yrityksen valmistelu sähköisten asiakirjojen lähettämistä ja vastaanottamista varten  
* ALV-kirjausten määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten  
* Maa-/alueasetuksien määrittäminen asiakirjojen sähköistä lähettämistä ja vastaanottamista varten  
* Kohteiden määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten  
* Mittayksikköjen määrittäminen asiakirjojen sähköistä lähettämistä ja vastaanottamista varten  
* Asiakkaiden määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten  
* **PEPPOL**-formaatin valitseminen asiakirjojen lähettämistä varten  
* Toimittajien määrittäminen sähköisten asiakirjojen vastaanottamista varten  
* **PEPPOL – Lasku** -tietojenvaihtomäärityksen valitseminen asiakirjojen vastaanottamista varten  
* Kirjanpitotilin määrittäminen käyttämään uusia ostolaskun rivejä tunnistamatto\-mille nimikkeille ja muille kuin \-nimikkeille  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving" />Yrityksen valmistelu sähköisten asiakirjojen lähettämistä ja vastaanottamista varten

1. Syötä **Etsi**-ruudussa **Oman yrityksen tiedot** ja valitse sitten vastaava linkki.  
2. Lisää soveltuvat arvot **Yleinen**-pikalomakkeen kenttiin seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Yrityksen määrittäminen.<br /><br /> Jos esimerkiksi lähetät sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **EndPointID**-elementti tiedoston **AccountingSupplierParty** -solmussa. Numero perustuu GS1-standardiin, joka noudattaa ISO 6523 -standardin vaatimuksia.|  
    |**ALV-rekisterinro**|Määritä yrityksesi ALV-tunnus.|  
    |**Vastuupaikka**|Jos yrityksellesi on määritetty vastuukeskus, varmista, että **Maa-/aluekoodi**-kenttä on täytetty.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving" />ALV-kirjausten määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten

1. Syötä **Etsi**-ruudussa **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.  
2. Täytä jokainen sähköisille asiakirjoille käyttämäsi ALV-kirjauksen asetusrivi seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Veroluokka**|Määritä ALV-luokka:<br /><br /> Jos esimerkiksi lähetät sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **TaxApplied**-elementti tiedoston **AccountingSupplierParty** -solmussa. Luku perustuu UNCL5305-standardiin.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving" />Maa-/alueasetuksien määrittäminen asiakirjojen sähköistä lähettämistä ja vastaanottamista varten

1. Avaa **Haku**-ruudusta **Maa/alueet** ja valitse liittyvä linkki.  
2. Täytä jokainen maa-/aluekenttä, jonka kanssa vaihdat sähköisiä asiakirjoja seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**ALV-suunnitelma**|Määritä kansallinen, ALV-numeroita jakava viranomainen maalle tai \/alueelle, joka liittyy sähköisten asiakirjojen lähettämiseen.<br /><br /> Jos esimerkiksi lähetät sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **EndPointID** -elementin **SchemeID**-määrite tiedoston **AccountingSupplierParty** ja **AccountingCustomerParty** -solmuissa.<br /><br /> **ALV-suunnitelma**-kenttää käytetään vain, jos **Yritystiedot**-sivun **GLN**-kenttä on tyhjä. **Huomautus:** **Maat\/alueet**-sivulla olevan **Koodi**-kentän arvon on noudatettava ISO 3166\-1:Alpha2 -standardin vaatimuksia.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving" />Kohteiden määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten

1. Syötä **Etsi**-ruudussa **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Täytä jokaisen sähköisten asiakirjojen avulla myymäsi tai ostamasi kohteen kenttä seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Määrittää kohteelle liitännän asiakirjojen sähköistä lähettämistä ja vastaanottamista varten. Kenttää käytetään PEPPOL-formaatissa seuraavasti:<br /><br /> Jos **StandardItemIdentification\/ID**-elementin **SchemaID**-määritteen arvo on **GTIN**, elementti määritetään nimikekortin **GTIN**-kenttään.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving" />Mittayksikköjen määrittäminen asiakirjojen sähköistä lähettämistä ja vastaanottamista varten

1. Avaa **Haku**-ruudusta **Mittayksiköt** ja valitse liittyvä linkki.  
2. Täytä jokaiselle kohteelle sähköisissä asiakirjoissa käyttämäsi mittayksikkökenttä seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kansainvälisen standardin koodi**|Määritä UNECERec20-standardin mukainen mittayksikkö, jota käytät sähköisten asiakirjojen lähettämisessä.<br /><br /> Jos esimerkiksi lähetät sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **InvoicedQuantity**-elementin **unitCode** -määrite tiedoston **InvoiceLine** -solmussa. **Huomautus:** Jos myyntirivin **Mittayksikkö**-kenttä on tyhjä, UNECERe20-standardin mukainen "Kappale" \(H87\) -arvo täytetään oletusarvoisesti. Lisätietoja mittayksiköistä ja kelvollisten mittayksikkökoodien luettelo on asiakirjassa [Recommendation No. 20\-Units of Measure used in International Trade](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending" />Asiakkaiden määrittäminen sähköisten asiakirjojen lähettämistä ja vastaanottamista varten

1. Syötä **Etsi**-ruudussa **Asiakkaat** ja valitse sitten vastaava linkki.  
2. Täytä jokaisen asiakkaan, jolle lähetät sähköisiä asiakirjoja, kentät seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Määritä asiakas.<br /><br /> Jos esimerkiksi lähetät sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **EndPointID**-elementti tiedoston **AccountingCustomerParty** -solmussa. Numero perustuu GS1-standardiin, joka noudattaa ISO 6523 -standardin vaatimuksia.<br /><br /> Jos **GLN**-kenttä on tyhjä, **ALV-rekisterinro**-kentän arvoa käytetään.|  
    |**ALV-rekisterinro**|Määritä asiakkaan ALV-tunnus. **Vinkki:** Tuetuissa lokalisoiduissa versioissa voit valita porautumispainikkeella verkkopalvelun, joka varmistaa, onko numero kansallisessa yritysrekisterissä.|  
    |**Vastuupaikka**|Jos asiakkaalle on määritetty vastuukeskus, varmista, että **Maa-/aluekoodi**-kenttä on täytetty.|  

    Voit määrittää jokaiselle asiakkaalle haluamasi liiketoiminta-asiakirjojen lähettämistavan, ettei sinun tarvitse valita lähettämistapaa joka kerta, kun lähetät asiakkaalle asiakirjan. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending" />PEPPOL-formaatin valitseminen asiakirjojen lähettämistä varten
1. Kirjoita **Haku**-ruutuun **Asiakirjan lähetysprofiilit** ja valitse aiheeseen liittyvä linkki.  
2. Avaa joko aiemmin luotu asiakirjan lähetysprofiili tai luo uusi. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  
3. Valitse **Asiakirjan lähetyksen profiili** -sivulla ensin **Sähköinen muoto**, sitten PEPPOL-rivi ja lopuksi **OK**.  
4. Valitse **Sähköinen asiakirja** -kentässä **Kyllä (Document Exchange -palvelun kautta)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] tunnistaa automaattisesti, onko asiakirja lasku vai hyvityslasku ja käyttää oikeaa PEPPOL-muotoa.  

5. Jos haluat käyttää asiakirjan lähetysprofiilia kaikille asiakkaille, valitse **Oletus**-valintaruutu **Yleinen**-pikavälilehdessä. Jos haluat, että profiili koskee vain tiettyjä asiakkaita, täytä **Asiakirjan lähetyksen profiili** -kenttä kyseisten asiakkaiden asiakaskortissa. Lisätietoja on kohdassa [Asiakirjan lähetysprofiilien määrittäminen](sales-how-setup-document-send-profiles.md).  

    Voit nyt lähettää muunnettua tietoa sisältävän sähköisen asiakirjan. Lisätietoja on kohdassa [Sähköisten asiakirjojen lähettäminen](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving" />Toimittajien määrittäminen sähköisten asiakirjojen vastaanottamista varten
1. Syötä **Etsi**-ruudussa **Toimittajat** ja valitse sitten vastaava linkki.  
2. Täytä jokaisen toimittajan, jolta vastaanotat sähköisiä asiakirjoja, kentät seuraavan taulukon mukaisesti.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Määritä toimittaja.<br /><br /> Jos esimerkiksi vastaanotat sähköisiä laskuja PEPPOL-formaatissa, tämän kentän arvoa käytetään täyttämään **EndPointID**-elementti tiedoston **AccountingSupplierParty** -solmussa. Numero perustuu GS1-standardiin, joka noudattaa ISO 6523 -standardin vaatimuksia.<br /><br /> Jos **GLN**-kenttä on tyhjä, **ALV-rekisterinro**-kentän arvoa käytetään.|  
    |**ALV-rekisterinro**|Määritä toimittajan ALV-tunnus. **Vinkki:** Tuetuissa lokalisoiduissa versioissa voit valita porautumispainikkeella verkkopalvelun, joka varmistaa, onko numero kansallisessa yritysrekisterissä.|  
    |**Vastuupaikka**|Jos toimittajalle on määritetty vastuukeskus, varmista, että **Maa-/aluekoodi**-kenttä on täytetty.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving" />PEPPOL – Lasku -tietojenvaihtomäärityksen valitseminen asiakirjojen vastaanottamista varten
1. Kirjoita **Etsi**-ruutuun **Saapuvat asiakirjat** ja valitse sitten vastaava linkki.  
2. Valitse vastaanotettavan ja muunnettavan sähköisen asiakirjan rivillä **Tiedonsiirron tyyppi** -kenttä ja valitse sitten **PEPPOLINVOICE**.  

     Jos vastaanotettava asiakirja on hyvityslasku, valitse **PEPPOLCREDITMEMO**.  

    Voit nyt vastaanottaa sähköisen asiakirjan aloittamalla tietojen muuntamisen **Saapuvat asiakirjat** -sivulla. Lisätietoja on kohdassa [Sähköisten asiakirjojen vastaanottaminen ja muuntaminen](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items" />Kirjanpitotilin määrittäminen käyttämään uusia ostolaskun rivejä tunnistamattomille kohteille ja ei-kohteille
1. Avaa **Haku**-ruudusta **Ostojen ja ostovelkojen asetukset** ja valitse liittyvä linkki.  
2. Täytä **Oletustilit**-pikalomakkeen kenttä seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Muiden kuin nimikerivien KP-tili**|Määrittää kirjanpitotilin, joka lisätään automaattisesti sähköisistä asiakirjoista ostoriveille silloin, kun saapuva asiakirjarivi ei sisällä tunnistettavaa kohdetta. Kaikki saapuvan asiakirjan rivit, joilla ei ole GTIN-arvoa tai toimittajan nimikenumeroa, muunnetaan tyypin **KP-tili**-tyyppiseksi ostoriviksi. Ostorivin **Nro**-kenttä sisältää tilin, jonka valitset **Muiden kuin nimikerivien KP-tili** -kentässä.<br /><br /> Ostoasiakirjaa ei luoda, jos **Muiden kuin nimikerivien KP-tili** -kenttä jätetään tyhjäksi ja saapuva asiakirja sisältää rivejä, joilla ei ole tunnistettavia nimikkeitä. Virhesanoma pyytää täyttämään **Muiden kuin nimikerivien KP-tili** -kentän, ennen kuin voit päättää tehtävän.|  

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics-365-business-centralindex" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also" />Katso myös
[Sähköinen tiedonsiirto](across-data-exchange.md)   
[Myynnin laskutus](sales-how-invoice-sales.md)   
[Ostojen kirjaus](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
