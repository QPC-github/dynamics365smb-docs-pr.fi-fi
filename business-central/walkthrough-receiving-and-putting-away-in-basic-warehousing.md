---
title: Vaihekuvaus – vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä
description: Tietoja erilaisista tavoista käsitellä saapuvien vastaanotto- ja hyllytysprosesseja.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations" />Vaihekuvaus: Vastaanotto ja hyllytys fyysisen varastoinnin perusmäärityksissä

[!INCLUDE[prod_short](includes/prod_short.md)]issa nimikkeiden vastaanottoon ja hyllytykseen on neljä tapaa, jotka käsitellään seuraavassa taulukossa.

|Tapa|Saapuva prosessi|Vaadi vastaanotot|Vaadi hyllytykset|Monimutkaisuustaso (lisätietoja on kohdassa [Varastoinninhallinnan yleiskatsaus](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Vastaanoton ja hyllytyksen kirjaaminen tilausriviltä|||Ei määritettyä fyysisen varaston toimintaa.|  
|B|Vastaanoton ja hyllytyksen kirjaaminen varaston hyllytysasiakirjasta||Otettu käyttöön|Perus: tilauksittain.|  
|S|Kirjaa vastaanotto ja hyllytys fyysisen varastoinnin vastaanottoasiakirjasta|Otettu käyttöön||Perus: useiden tilausten konsolidoitu vastaanoton ja toimituksen kirjaus.|  
|P|Kirjaa vastaanotto fyysisen varastoinnin vastaanottoasiakirjasta ja kirjaa hyllytys varaston hyllytysasiakirjasta|Otettu käyttöön|Otettu käyttöön|Lisäasetukset|  

Lisätietoja on kohdassa [Saapuvien varastotyönkulku](design-details-inbound-warehouse-flow.md).

Seuraavassa vaihekuvauksessa kuvataan edellisen taulukon menetelmää B.  

## <a name="about-this-walkthrough" />Tietoja tästä vaihekuvauksesta

Jos fyysisen varastoinnin perusmääritykset määrittävät sijainnin edellyttämän hyllytyksen muttei vastaanoton käsittelyä, saapuvien lähdeasiakirjojen hyllytys- ja vastaanottotiedot tallennetaan ja kirjataan **Varaston hyllytys**-sivulla. Seuraavat asiakirjat ovat saapuvia lähdeasiakirjoja:

* Ostotilaus
* Myyntipalautustilaus
* Tuleva siirtotilaus
* Tuotantotilauksen tuotos, joka on valmis hyllytettäväksi

> [!NOTE]
> Vaikka asetusten nimenä on **Vaadi poiminta** ja **Vaadi hyllytys**, voit silti kirjata vastaanottoja ja toimituksia suoraan lähdeasiakirjoista sijainneissa, joissa olet valinnut nämä valintaruudut.  

Tässä vaihekuvauksessa käsitellään seuraavia tehtäviä:  

* HOPEA-sijainnin määrittäminen varastopaikan hyllytykseen.  
* HOPEA-sijainnin määrittäminen varastopaikan käsittelyyn.  
* Oletusvarastopaikan määrittäminen nimikkeelle LS-81. (LS-75 on jo määritetty CRONUSissa.)  
* Ostotilauksen luominen 40 kaiuttimesta toimittajalle 10 000.  
* Tarkistetaan, että hyllytyksen varastopaikat määritetään ennalta asetusten avulla.  
* Ostotilauksen vapauttaminen varaston käsittelyyn.  
* Varastohyllytyksen luominen julkaistusta lähdeasiakirjasta.  
* Hyllytyksen varastopaikkojen ostotilauksesta perimisen tarkistaminen.  
* Fyysisen varastoinnin siirtoa rekisteröiminen fyysiseen varastoon ja lähdeostotilauksen ostokuitin kirjaaminen.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## <a name="roles" />Roolit

Seuraavat käyttäjärooli suorittavat tässä vaihekuvauksessa esiteltävät tehtävät:  

* Varastopäällikkö  
* Ostaja  
* Varastotyöntekijä  

## <a name="prerequisites" />Vaatimukset

Tämän vaihekuvauksen ohjeiden noudattamisen edellytykset:  

* CRONUS Finland Oy -tiedot  
* Varastotyöntekijä HOPEA-sijainnissa. Määritykset tehdään seuraavasti:  

    1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
    2. Valitse ensin **Käyttäjätunnus**-kenttä ja sitten käyttäjätili **Käyttäjät**-sivulla.  
    3. Valitse **Sijaintikoodi**-kentässä **HOPEA**.  
    4. Valitse **Oletus**-valintaruutu.  

## <a name="story" />Taustatietoja

Ellen on CRONUS Finland Oy:n varastopäällikkö ja hän luo ostotilauksen, jossa on 10 yksikköä LS-75-nimikettä ja 30 yksikköä LS-81-nimikettä, toimittajalta 10000 toimitettavaksi HOPEISEEN varastoon. Kun toimitus saapuu varastoon, varastotyöntekijä Joakim hyllyttää nimikkeet niille määritettyihin oletusvarastopaikkoihin. Kun Joakim kirjaa hyllytyksen, nimikkeet kirjataan vastaanotetuksi varastoon, ja ne ovat käytettävissä myyntiä tai muita kysyntää varten.  

## <a name="setting-up-the-location" />Sijainnin määrittäminen

**Sijaintikortti**-sivun asetuksissa määritetään yrityksen varastointityönkulut.  

### <a name="to-set-up-the-location" />Sijainnin määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2. Avaa asianmukaisen HOPEA sijainnin kortti.  
3. Ota **Vaadi hyllytys** käyttöön vaihtopainikkeella.  

    Määritä oletusvarastopaikka kahdelle nimikenumerolla, joilla hallitaan niiden hyllytyspaikkaa.  

4. Valitse **Varastopaikat**-toiminto.  
5. Valitse varastopaikan **S-01-0001** ensimmäinen rivi ja valitse sitten **Sisältö**-toiminto.  

    Huomaa **Varastopaikan sisältö** -sivulla, että nimike **LS-75** on jo määritetty sisällöksi varastopaikassa S-01-0001.  

6. Valitse **Uusi**-toiminto.  
7. Valitse **Kiinteä**- ja **Oletus**-kentät.  
8. Anna **Nimikenro**-kentässä **LS-81**.  

## <a name="create-the-purchase-order" />Ostotilauksen luominen

Ostotilaukset ovat yleisin saapuvien lähdeasiakirjojen tyyppi.  

### <a name="to-create-the-purchase-order" />Ostotilausten luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Luo ostotilaus toimittajalle 10000 (23.1.) käsittelypäivämääränä seuraavien ostontilausrivien kanssa.  

    |Nimike|Sijaintikoodi|Varastopaikan koodi|määrä.|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|HOPEINEN|S-01-0001|10|  
    |LS_81|HOPEINEN|S-01-0001|30|  

    > [!NOTE]  
    > Varastopaikkakoodi lisätään automaattisesti [Sijainnin määrittäminen](#setting-up-the-location) -osassa luotujen määritysten mukaisesti.  

    Ilmoita seuraavaksi fyysiseen varastoon, että ostotilaus on valmis varastointikäsittelyyn, kun toimitus saapuu.  

4. Valitse **Vapauta**-toiminto.  

    Kaiuttimien toimitus toimittajalta 10000 on saapunut HOPEISEEN varastoon, ja John ryhtyy hyllyttämään niitä.  

## <a name="receive-and-put-the-items-away" />Nimikkeiden vastaanottaminen ja hyllyttäminen

**Varastohyllytys**-sivulla voi hallita kaikkia tietyn lähdeasiakirjan saapuvia varastotoimintoja, kuten ostotilausta.  

### <a name="to-receive-and-put-the-items-away" />Nimikkeiden vastaanottaminen ja hyllyttäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varaston hyllytykset** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse ensin **Lähdeasiakirja**-kenttä ja sitten **Ostotilaus**.  
4. Valitse **Lähteen nro** -kentässä toimittajalta 10000 tehdyn oston rivi ja valitse sitten **OK**.  

    Vaihtoehtoisesti voit valita ensin **Hae lähdeasiakirja** -toiminnon ja sitten ostotilauksen.  

5. Valitse **Täytä autom. käsitelt. määrä** -toiminto.  

    Vaihtoehtoisesti voit antaa **Käsiteltävä määrä** -kentässä 10 ja 30 kahdelle varastohyllytysriville.  

6. Valitse ensin **Kirjaa**-toiminto, sitten **Vastaanotto**-toiminto ja lopuksi **OK**.  

    40 kaiutinta on nyt rekisteröity hyllytetyiksi varastopaikasta S-01-0001, ja luodaan positiivinen nimiketapahtuma, joka heijastaa kirjattua ostotoimitusta.  

## <a name="see-also" />Katso myös

[Nimikkeiden hyllyttäminen varastohyllytyksen avulla](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Fyysisten perusvarastojen ja toimintoalueiden määrittäminen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Poiminta tuotantoon tai kokoonpanoon](warehouse-how-to-pick-for-production.md)  
[Nimikkeiden suunnittelematon siirtäminen fyysisen varastoinnin perusmäärityksissä](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Rakennetiedot: saapuvan fyysisen varastoinnin virta](design-details-inbound-warehouse-flow.md)  
[Liiketoimintaprosessien vaihekuvaukset](walkthrough-business-process-walkthroughs.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
