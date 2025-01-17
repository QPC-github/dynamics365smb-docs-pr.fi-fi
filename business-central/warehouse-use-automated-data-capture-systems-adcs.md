---
title: Käytä ADCS (Automated Data Capture System) -järjestelmää
description: Tietoja nimikkeiden siirron rekisteröinnistä varastossa automaattisen tiedonkeruujärjestelmän (ADCS) avulla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7700, 7703, 7704, 7706, 7707, 7710, 9813, 9814'
---
# <a name="use-automated-data-capture-systems-adcs" />Käytä ADCS (Automated Data Capture System) -järjestelmää

> [!NOTE]
> Automaattinen tiedonkeruujärjestelmän (ADCS) ratkaisu tarjoaa [!INCLUDE[prod_short](includes/prod_short.md)]:lle keinon kommunikoida kannettavien laitteiden kanssa verkkopalveluiden avulla. Sinun on toimittava sellaisen Microsoft-palveluntarjoajan kanssa, joka pystyy tarjoamaan linkin Web-palvelun ja tietyn kannettavan laitteen välille. 

Automaattista tiedonkeruujärjestelmää (ADCS) voidaan käyttää rekisteröimään kaikki nimikkeiden siirrot fyysisessä varastossa ja rekisteröimään kaikki päiväkirjatoiminnot, joihin sisältyvät määrän muutokset fyysisen varastoinnin nimikepäiväkirjassa, inventoinneissa ja uudelleenluokitteluissa. ADCS sisältää yleensä viivakoodin skannauksen.

ADCS:n käyttöön on annettava kullekin nimikkeelle, joka on tallennettu varastoon, nimikkeen tunnus. Sinun täytyy myös määrittää pienoislomakkeet, kannettavat toiminnot, tiedon siirrot, ja määrittää eritysasetukset kentille, jotka määrittävät ADCS-asetuksia. Voit määrittää käytetäänkö ADCS:ää varaston sijaintikortissa.

Fyysisen varastoinnin tarpeiden pohjalta pienoislomakkeen asetuksissa määritetään tietojen määrä, joka näytetään tietyssä kannettavassa laitteessa. Seuraavat ovat esimerkkejä tiedoista, joita voit näyttää:  

- Tiedot [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman taulukoista, kuten lista poiminta-asiakirjoista, joista käyttäjä voi valita.  
- Tekstitiedot.  
- Vahvistuksia tai virhesanomia suoritetuista toiminnoista, jotka käyttäjä on tehnyt ja rekisteröinyt kannettavalla laitteella.

## <a name="to-enable-web-services-for-adcs" />Voit ottaa ADCS-verkkopalvelut käyttöön

Jotta voisit käyttää automaattista tiedonkeruujärjestelmää, sinun on otettava ADCS-verkkopalvelu käyttöön.  

## <a name="to-enable-and-publish-the-adcs-web-service" />ADCS-verkkopalvelun käyttöönotto ja julkaiseminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Verkkopalvelut** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Lisää seuraavat tiedot **verkkopalvelut**-sivun uudelle riville:  

    |Kenttä|Arvo|  
    |---------------------------------|-----------|  
    |**Objektityyppi**|Codeunit|  
    |**Objektin tunnus**|7714|  
    |**Palvelun nimi**|ADCS **Tärkeää:** Sinun on annettava palvelulle nimeksi **ADCS**.|  

4. Ota käyttöön **Julkaistu**-vaihtopainikkeella.  
5. Valitse **OK**-painike.  

## <a name="to-set-up-a-warehouse-to-use-adcs" />Fyysisen varaston määrittäminen ADCS-järjestelmän käyttämistä varten

ADCS:n käytössä on määritettävä, mitkä fyysisen varaston sijainnit käyttävät tekniikkaa.  

> [!NOTE]  
> Varastoa ei kannata määrittää käyttämään automaattista tiedonkeruujärjestelmää, jos siinä on myös varastopaikan kapasiteettikäytäntö.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.
2. Valitse varasto, jossa haluat ottaa käyttöön ADCS-järjestelmä, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Sijainnin kortti** -sivulla **Käytä ADCS** -vaihtopainike.  

## <a name="to-specify-an-item-to-use-adcs" />Nimikkeen määrittäminen käyttämään ADCS-järjestelmää

Kullekin varastonimikkeelle, jota haluat käyttää ADCS:n kanssa, on määritettävä tunnuskoodia, joka yhdistää sen nimikkeen numeroon. Esimerkiksi nimikkeen viivakoodia voi käyttää tunnuskoodina. Nimikkeellä voi olla myös useita tunnuskoodeja. Saatat pitää tätä hyödyllisenä siinä tapauksessa, että nimike on käytettävissä eri mittayksiköissä, kuten kappaleissa ja kuormalavoissa. Määritä tässä tapauksessa jokaiselle tunnuskoodi.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.  
2. Valitse luettelosta nimike, joka on osa ADCS-ratkaisua, ja valitse sitten **Muokkaa**-toiminto.
3. Valitse **Nimikkeen kortti** -sivulla **Tunnisteet**-toiminto.
4. Valitse **Nimiketunnisteet**-sivulla **Uusi**-toiminto.
5. Määritä **Koodi**-kentässä nimikkeen tunnus. Tunnus voi olla esimerkiksi nimikkeen viivakoodinumero.  

    Voit myös kirjoittaa **Varianttikoodi** ja **Mittayksikkö** -koodi.  

6. Syötä tarvittaessa jokaiselle nimikkeelle useita koodeja.
7. Valitse **OK**-painike.  
8. Voit tarkastella tietoja avaamalla **Nimiketunnisteet**-sivu valitsemalla **Tunnistimen koodi** -kenttä.

## <a name="to-add-an-adcs-user" />ADCS-käyttäjän lisääminen

Kuka tahansa käyttäjä voidaan lisätä ADCS:ään. Siinä tapauksessa käyttäjälle on annettava salasana. Voit myös antaa yhteyden, joka määrittää ADCS-käyttäjän fyysisen varastoinnin työntekijäksi. ADCS-käyttäjän salasana voi olla eri kuin kirjautumissalasana. Lisätietoja kohdassa [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](ui-define-granular-permissions.md).

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ADCS-käyttäjät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Kirjoita **Nimi**-kenttään käyttäjän nimi. Nimi voi olla enintään 20 merkkiä pitkä, välilyönnit mukaan lukien.  
4. Anna **Salasana**-kenttään salasana.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user" />Varastotyöntekijän määrittäminen ADCS-käyttäjäksi

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2. Lisää tarvittaessa uusi varastotyöntekijä. Lisätietoja kohdassa [Varastotyöntekijöiden määrittäminen](warehouse-how-to-set-up-warehouse-employees.md).  
3. Valitse **Muokkaa luetteloa** -toiminto.  
4. Valitse varastotyöntekijä luettelosta. Valitse **ADCS-käyttäjä** -kentässä ADCS-käyttäjän nimi luettelosta.  

> [!NOTE]  
> Työntekijän oletusvaraston on oltava sellainen, jossa käytetään ADCS-järjestelmää.

## <a name="to-create-and-customize-miniforms" />Pienoislomakkeiden luominen ja mukauttaminen

Pienoislomakkeiden avulla voit kuvailla tietoja, jotka haluat esittää käsilaitteesta. Voit luoda pienoislomakkeita, jotka tukevat nimikkeiden poiminnan fyysisen varastoinnin toimintoja. Pienoislomakkeen luotuasi voit lisätä siihen toimintoja yleisiä toimenpiteitä varten, jotka käyttäjä tekee kannettavissa laitteissa, esimerkiksi siirtyminen ylös- tai alaspäin rivillä.  

> [!NOTE]
> Ota käyttöön tai muuta pienoislomakkeen toiminto luomalla uusi codeunit **Käsittelevä codeunit** -kenttään suorittamaan vaadittu toiminto tai vastaus. Saat lisätietoja ADCS-toiminnosta tarkastelemalla seuraavia codeuniteja:
>
> * 7705
> * 7706
> * 7712
> * 7713  

### <a name="to-create-a-miniform-for-adcs" />Luo ADCS-pienoislomake

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Anna **Koodi**-kenttään pienoislomakkeen koodi. Voit antaa arvot myös muihin kenttiin.  

    Käyttöönotto **Käynnistä miniform** -vaihtopainikkeella ilmaisee, että pienoislomake on ensimmäinen lomake, jonka käyttäjä näkee kirjautumisen yhteydessä.  

4. Määritä **Rivit**-pikavälilehdessä pienoislomakkeessa näkyvät kentät. Järjestys, jossa syötät rivit on sama, jossa rivit näkyvät kannettavalla päätteellä.  

Pienoislomakkeen luonnin jälkeen luodaan seuraavaksi toiminnot ja liitetään toiminnot näppäimistön syötteille.  

### <a name="to-customize-miniform-functions" />Mukauta pienoislomakkeen toiminnot

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pienoislomakkeet** ja valitse sitten vastaava linkki.  
2. Valitse pienoislomake luettelosta ja valitse sitten **Muokkaa**-toiminto.  
3. Valitse **Toiminnot**-toiminto.  
4. Valitse avattavasta **Toimintokoodi**-luettelosta sitä toimintoa vastaava koodi, jonka haluat liittää pienoislomakkeeseen. Voit valita esimerkiksi **ESC**-vaihtoehdon, jolla toiminto liitetään **ESC**-näppäimellä.  

## <a name="see-also" />Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
