---
title: Raporttien luominen Power BI Desktopissa näyttämään Business Central -tietoja | Microsoft Docs
description: 'Määritä tiedot käytettäviksi Power BI:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 09/07/2022
ms.author: jswymer
---

# <a name="building-power-bi-reports-to-display-include-prodlongincludesprodlongmd-data" />Power BI -raporttien luominen näyttämään [!INCLUDE [prod_long](includes/prod_long.md)] -tietoja

Voit määrittää [!INCLUDE[prod_long](includes/prod_long.md)]in tiedot käytettäviksi Power BI Desktop:n tietolähteenä ja tehokkaiden liiketoiminnan tilasta kertovien raporttien luomista varten.

Tässä artikkelissa käsitellään Power BI Desktopin käytön aloittamista luomaan [!INCLUDE[prod_long](includes/prod_long.md)] -tiedot näyttäviä raportteja.  Kun raportit on luotu, voit julkaista ne Power BI -palveluun tai jakaa ne organisaation kaikkien käyttäjien kanssa. Kun nämä raportit ovat Power BI -palvelussa, käyttäjät, joilla on raporttien tarkasteluoikeudet, voivat tarkastella niitä [!INCLUDE[prod_long](includes/prod_long.md)]issa.

## <a name="get-ready" />Valmistelut

- Rekisteröidy Power BI -palveluun.

  Jos et ole vielä rekisteröitynyt, siirry osoitteeseen [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Käytä rekisteröityessä työpaikan sähköpostiosoitetta ja salasanaa.

- Lataa [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop on maksuton tietokoneeseen paikallisesti asennettava sovellus. Lisätietoja on kohdassa [Pika-aloitus: Power BI Desktopin tietoihin yhdistäminen](/power-bi/desktop-quickstart-connect-to-data).

- Varmista, että raportissa käytettävät tiedot ovat käytettävissä API-sivuna tai ne julkaistaan verkkopalveluna.

  Lisätietoja on kohdassa [Tietojen näyttäminen API-sivujen tai OData-verkkopalvelujen kautta](admin-powerbi-setup.md#exposedata).

- Paikallista [!INCLUDE[prod_short](includes/prod_short.md)] -versiota varten tarvitaan seuraavat tiedot:

  - [!INCLUDE[prod_short](includes/prod_short.md)]in ODatan URL-osoite.
  
    Tämän URL-osoitteen muoto on yleensä `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, kuten `https://localhost:7048/BC190/ODataV4`. Jos kyse on monen vuokraajan käyttöönotossa, URL-osoitteen on sisällettävä vuokraaja, kuten `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - [!INCLUDE[prod_short](includes/prod_short.md)] -tilin käyttäjänimi ja verkkopalvelun käyttöoikeusavain.

    Power BI käyttää perustodennusta [!INCLUDE[prod_short](includes/prod_short.md)] -tietojen hakemiseen. Yhteyttä varten tarvitaan tämän vuoksi käyttäjänimi ja verkkopalvelun käyttöoikeusavain. Tili voi olla oma käyttäjänimi. Organisaatiolla voi olla myös erillinen tili tätä tarkoitusta varten.

- Lataa [!INCLUDE [prod_short](includes/prod_short.md)] -raportin teema (valinnainen).

  Lisätietoja on tämän artikkelin kohdassa [[!INCLUDE [prod_short](includes/prod_short.md)] -raportin teeman käyttäminen](#theme).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="a-namegetdataaadd-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop" /><a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi

Raporttien luomisen ensimmäinen tehtävä on [!INCLUDE[prod_short](includes/prod_short.md)]in lisääminen Power BI Desktopin tietolähteeksi. Raportin luonnin voi aloittaa, kun yhteys on muodostettu.

1. Käynnistä Power BI Desktop.
2. Valitse **Nouda tiedot**.

    Jos **Nouda tiedot** ei ole näkyvissä, valitse ensin **Tiedosto** ja sitten **Nouda tiedot**.
3. Valitse **Nouda tiedot** -sivulla **Verkkopalvelut**.
4. Tee **Verkkopalvelut**-ruudussa jokin seuraavista:

    - Jos haluat muodostaa yhteyden [!INCLUDE [prod_short](includes/prod_short.md)] onlineen, valitse **Dynamics 365 Business Central** ja sitten **Yhdistä**.
    - Jos haluat muodostaa paikallisen [!INCLUDE [prod_short](includes/prod_short.md)] -yhteyden, valitse **Dynamics 365 Business Central (paikallinen)** ja sitten **Yhdistä**.

5. Kirjaudu sisään [!INCLUDE [prod_short](includes/prod_short.md)]iin (vain kerran).

    Jos et ole aiemmin kirjautunut sisään [!INCLUDE [prod_short](includes/prod_short.md)]iin Power BI desktopista, sinua pyydetään kirjautumaan sisään.

    - Valitse [!INCLUDE [prod_short](includes/prod_short.md)] onlinessa **Kirjaudu sisään** ja valitse sitten asiaankuuluva tili. Käytä samaa tiliä, jolla kirjaudut [!INCLUDE [prod_short](includes/prod_short.md)]iin. Kun olet valmis, valitse **Yhdistä**.

    - Paikallisessa [!INCLUDE [prod_short](includes/prod_short.md)]issa syötä ensin [!INCLUDE[prod_short](includes/prod_short.md)]in OData-URL-osoite ja valitse sitten **OK**. Anna pyydettäessä sen tilin käyttäjänimi ja salasana, jolla muodostetaan yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin. Anna **Salasana**-ruudussa verkkopalvelun käyttöoikeusavain. Kun olet valmis, valitse **Yhdistä**.

    > [!NOTE]  
    > Kun yhteys [!INCLUDE[prod_short](includes/prod_short.md)]iin on muodostettu, sinua ei pyydetä kirjautumaan uudelleen. [Miten muutan tai tyhjennän tilin, jota tällä hetkellä käytän yhteyden muodostamiseen Business Centraliin Power BI Desktopista?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Kun yhteys on muodostettu, Power BI muodostaa yhteyden Business Central -palveluun. **Navigator**-ikkunat tulevat näkyviin ja näyttävät käytettävissä olevat tietolähteet raporttien rakentamista varten. Laajenna kansio valitsemalla se ja tarkastele käytettävissä olevia tietolähteitä. 

   Nämä tietolähteet viittaavat kaikkiin [!INCLUDE [prod_short](includes/prod_short.md)]iin julkaistuihin verkkopalveluihin ja API-sivuihin. Tietolähteet on ryhmitelty Business Central -ympäristöjen ja yritysten mukaan. Business Central onlinessa **Navigator**-rakenne on seuraava:

    - **Ympäristön nimi**
      - **Yrityksen nimi**
        - **Kehittyneet ohjelmointirajapinnat**

          Tässä kansiossa on luettelo Microsoftin julkaisemista kehittyneistä API-sivuista, kuten [Business Centralin automaatio-API-sivut](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) ja [Business Centralin mukautetut API-sivut](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Mukautetut API-sivut ryhmitellään edelleen kansioihin API-sivun lähdekoodin [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property)-ominaisuuksien mukaan.

        - **Vakio-API v2.0**

          Tässä kansiossa on luettelo API-sivuista, jotka [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) näyttää.

        - **Verkkopalvelut \(vanha)**

          Tässä kansiossa on luettelo sivuista, koodiyksiköistä ja kyselyistä, jotka julkaistaan verkkopalveluina Business Centralissa.

    > [!NOTE]
    > Paikallisen Business Centralin rakenne on erilainen, koska se ei tue API-sivuja.

7. Valitse tietomalliin lisättävä tietolähde tai lisättävät tietolähteet ja valitse sitten **Lataa**-painike.
8. Jos haluat myöhemmin lisätä Business Central -tietoja, voit toistaa edelliset vaiheet.

Kun tiedot on ladattu, ne näkyvät sivun oikeassa siirtymisruudussa. Olet nyt muodostanut yhteyden [!INCLUDE[prod_short](includes/prod_short.md)] -tietoihin ja voit aloittaa Power BI -raportin luomisen.  

> [!TIP]
> Lisätietoja Power BI Desktopin käytöstä on kohdassa [Power BI Desktopin käytön aloittaminen](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports" />Helppokäyttötoimintoja sisältävien raporttien luominen

Raportit on tärkeä luoda sellaisiksi, että mahdollisimman moni henkilö voi käyttää niitä. Yritä suunnitella raportit niin, että ne eivät vaadi erityistä mukauttamista henkilöiden erityisten tarpeiden täyttämiseksi. Varmista, että suunnittelija käyttää hyväksi käyttöä tukevia vakiotekniikoita, kuten näytönlukuohjelmia. Power BI sisältää erilaisia helppokäyttötoimintoja, työkaluja ja ohjeita tämän tavoitteen saavuttamiseksi. Lisätietoja on Power BI:n ohjeiden kohdassa [Power BI:n raporttien suunnitteleminen helppokäyttötoimintoja varten](/power-bi/create-reports/desktop-accessibility-creating-reports).

## <a name="creating-reports-to-display-data-associated-with-a-list" />Raporttien luominen näyttämään luetteloon liitetyt tiedot

Voit luoda [!INCLUDE [prod_short](includes/prod_short.md)] -luettelosivun tietoruudussa näytettäviä raportteja. Raporteissa voi olla tietoja luettelossa valitusta tietueesta. Vaikka näiden raporttien luominen muistuttaa muiden raporttien luontia, raporttien näkyminen odotetusti edellyttää muutamia toimintoja. Lisätietoja on kohdassa [Power BI -raporttien luominen näyttämään luettelotietoja [!INCLUDE[prod_short](includes/prod_short.md)]issa](across-how-use-powerbi-reports-factbox.md).

## <a name="a-namethemeausing-the-include-prodshortincludesprodshortmd-report-theme-optional" /><a name="theme"></a>[!INCLUDE [prod_short](includes/prod_short.md)] -raportin teeman käyttäminen (valinnainen)

[!INCLUDE [prod_short](includes/prod_short.md)] -teematiedosto kannattaa ladata ja tuoda ennen raportin luontia. Teematiedosto luo värivalikoiman, jonka avulla voit luoda raportteja samalla värityylillä kuin [!INCLUDE [prod_short](includes/prod_short.md)] -sovelluksissa ilman, että kunkin visuaalisen ominaisuuden mukautetut värit on määritettävä erikseen.

> [!NOTE]
> Tämä tehtävä on valinnainen. Voit aina luoda omia raportteja ja ladata ja käyttää tyylimallia myöhemmin.

### <a name="download-the-theme" />Teeman lataaminen

Teematiedosto on saatavana JSON-tiedostona Microsoft Power BI -yhteisön teemavalikoimassa. Teematiedosto ladataan seuraavasti:

1. Siirry [Microsoft Dynamics 365 Business Centralin Microsoft Power BI -yhteisön teemavalikoimaan](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Valitse ladattava liite **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report" />Teeman tuominen raporttiin

Kun [!INCLUDE [prod_short](includes/prod_short.md)] -raportin teema on ladattu, voit luoda sen raportteihin. Tuo teema valitsemalla **Näkymä** > **Teema** > **Teemojen selaus**. Lisätietoja on kohdassa [Power BI Desktop – mukautettujen raportin teemojen tuominen](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports" />Raporttien julkaiseminen

Kun raportti on luotu tai sitä on muokattu, voit julkaista raportin Power BI -palveluun sekä jakaa sen organisaatiossa muiden kanssa. Raportti näkyy julkaisun jälkeen Power BI:ssa. Raportti on lisäksi valittavana [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Voit julkaista raportin valitsemalla **Julkaise** valintanauhan **Aloitus**-välilehdessä tai **Tiedosto**-valikossa. Jos olet kirjautunut Power BI -palveluun, raportti on julkaistava tähän palveluun. Muussa tapauksessa sinua pyydetään kirjautumaan sisään. 

## <a name="distribute-or-share-a-report" />Raportin jakaminen tai jakelu

Raportit voi toimittaa työtovereille ja muille kahdella tavalla:

- Raporttien jakaminen .pbix-tiedostoina.

    Raportit tallennetaan tietokoneeseen .pbix-tiedostoina. Voit jakaa raportin käyttäjille .pbix-tiedostona muiden tiedostojen tavoin. Käyttäjät voivat sitten ladata tiedoston Power BI -palveluun. Lisätietoja on kohdassa [Raporttien lataaminen tiedostoista](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Kun raportit jaetaan tällä tavoin, kukin käyttäjä päivittää raportin tiedot itse. Tämä voi vaikuttaa [!INCLUDE[prod_short](includes/prod_short.md)]in suorituskykyyn.

- Raporttien jakaminen Power BI -palvelusta

    Jos sinulla on Power BI Pro -käyttöoikeus, voit jakaa raportin muille suoraan Power BI -palvelusta. Lisätietoja on kohdassa [Power BI – koontinäytön tai raportin jakaminen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="fixing-problems" />Ongelmien korjaaminen

### <a name="cannot-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page" />"Tietuetta ei voi lisätä. Nykyinen yhteystarkoitus on vain luku.". virhe muodostettaessa yhteyttä mukautettuun ohjelmointirajapintasivuun

> **KOHDE:** Business Central online

Helmikuusta 2022 alkaen uudet Business Central -tietoja käyttävät raportit muodostavat oletusarvoisesti yhteyden Business Central -tietokannan replikaan. Joissakin harvoissa tapauksissa sivun rakenteen mukaan näyttöön tulee virhesanoma yritettäessä muodostaa yhteyttä sivuun ja noutaa tietoja sivulta.

1. Käynnistä Power BI Desktop.
2. Valitse valintanauhassa **Nouda tietoja** > **Verkkopalvelut**.
3. Valitse **Verkkopalvelut**-ruudussa **Dynamics 365 Business Central** ja sitten **Yhdistä**.
4. Valitse **Navigator**-ikkunassa se ohjelmointirajapinnan päätepiste, josta tietoja ladataan.
5. Oikealla olevassa esikatseluruudussa näkyy seuraava virhe:

   *Dynamics365BusinessCentral: Pyyntö epäonnistui: Etäpalvelin palautti virheen: (400) Virheellinen pyyntö. (Tietuetta ei voi lisätä. Nykyinen yhteystarkoitus on vain luku -muodossa.. CorrelationId: [...])".*

6. Valitse **Lataa**-vaihtoehdon sijaan **Muunna tiedot**.
7. Valitse kohdan **Power Query Editor** valintanauhasta **Laajennettu editori**.
8. Korvaa rivillä, joka alkaa **Lähde =**, seuraava teksti:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   tekstillä:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Valitse **Valmis**.
10. Tallenna muutokset ja sulje Power Query Editor valitsemalla valintanauhasta **Sulje ja käytä**.

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Katso myös

[Yritystietojen ottaminen käyttöön Power BI:ta varten](admin-powerbi.md)  
[Business Intelligence](bi.md)  
[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Liiketoimintatietojen tuominen muista rahoitusjärjestelmistä](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]in määrittäminen](setup.md)  
[Rahoitus](finance.md)  
[Pika-aloitus: Tietojen yhdistäminen Power BI Desktopiin](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
