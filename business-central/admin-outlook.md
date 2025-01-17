---
title: Business Central -apuohjelman hankkiminen Outlookiin
description: 'Tutustu siihen, miten Outlookin Business Central -apuohjelma asennetaan organisaatioosi tai omaan käyttöön.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, Outlook'
ms.search.form: '1831, 1832'
ms.date: 04/27/2022
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-outlook" />Business Central -apuohjelman hankkiminen Outlookiin

[!INCLUDE[prod_short](includes/prod_short.md)]in avulla voit hallita liiketoiminnallisia vuorovaikutuksia asiakkaiden ja toimittajien kanssa suoraan Microsoft Outlookista. [!INCLUDE[prod_short](includes/prod_short.md)]in Outlook-apuohjelman avulla voit tarkastella asiakkaisiin ja toimittajiin liittyviä taloudellisia tietoja. Voit myös luoda ja lähettää rahoitusasiakirjoja, kuten tarjouksia ja laskuja.  

On kaksi tapaa saada Business Central -lisäosa Outlookiin asennetuksi organisaatioroolistasi riippuen:

- Microsoft 365 -järjestelmänvalvojana voit asentaa apuohjelman automaattisesti käyttäen *keskitettyä käyttöönottoa* koko organisaatiolle, ryhmille tai tiettyjen käyttäjien osalta.

- Tavallinen käyttäjä voi asentaa lisäosan omaan käyttöön, jos järjestelmänvalvoja ei ole jo ottanut sitä käyttöön.

## <a name="about-the-business-central-add-in-for-outlook" />Tietoja Outlookin Business Central -apuohjelmasta

Outlookin Business Central -apuohjelma koostuu kahdesta pienemmästä apuohjelmista:

- Kontaktien tiedot

    Tämä apuohjelma tarjoaa [!INCLUDE[prod_short](includes/prod_short.md)]in asiakas- tai toimittajatiedot Outlookin sähköposteissa ja kalenteritapaamisissa. Sen avulla voit myös luoda ja lähettää [!INCLUDE[prod_short](includes/prod_short.md)]in liiketoiminta-asiakirjoja, kuten myyntitarjouksia ja laskuja kontaktille. <!--To support these task, the add-in adds actions to the Outlook ribbon, in the **Business Central** group. --> 

- Asiakirjanäkymä

    Kun sähköpostiviestissä viitataan sähköpostin tekstissä olevaan liiketoiminta-asiakirjan numeroon, tämä apuohjelma antaa sähköpostiviestin leipätekstin sisäisen suoran linkin varsinaiseen liiketoiminta-asiakirjaan [!INCLUDE[prod_short](includes/prod_short.md)]issa.

Lisätietoja apuohjelmien käytöstä on kohdassa [Business Centralin käyttäminen yrityksen liiketoimintakansiona Outlookissa](work-outlook-addin.md).

Jokainen apuohjelma toimitetaan XML-tiedostona eli *luettelotiedostona*, joka on asennettava kaikkien niiden henkilöiden Outlookiin, jotka haluavat tämän toiminnon. Näissä tiedostoissa kuvataan, miten apuohjelmat aktivoidaan ja yhdistetään Business Centraliin, kun niitä käytetään Outlookissa. Näiden tiedostojen käsitteleminen tapahtuu tavallisesti ylläpitäjän toimesta. Tavallisena käyttäjänä sinun ei useimmiten tarvitse käsitellä näitä tiedostoja suoraan. Joko järjestelmänvalvoja määrittää apuohjelman asennettavaksi automaattisesti puolestasi tai voit käyttää sisäänrakennettua avustettua määritystä asennuksen käsittelemiseen.

> [!IMPORTANT]
> Useiden ympäristöjen käsitteleminen Outlookin Business Central -apuohjelma on suunniteltu toimimaan yhdessä Business Central -ympäristössä. Kun apuohjelma on asennettu, ympäristön nimi sisällytetään apuohjelman kokoonpanotietoihin. Tämä määritys tarkoittaa, että apuohjelma muodostaa yhteyden vain ympäristöön, josta se asennettiin. Jos haluat käyttää apuohjelmaa eri ympäristössä, avaa ympäristö ja asenna apuohjelma uudelleen.

## <a name="deploy-the-add-in-by-using-centralized-deployment-as-an-admin" />Apuohjelman käyttöönottaminen keskitetyn käyttöönoton avulla järjestelmänvalvojana

Keskitetty käyttöönotto on Microsoft 365 -hallintakeskuksen ominaisuus, jonka avulla voit asentaa apuohjelmat automaattisesti käyttäjien Office-sovelluksiin, kuten Outlookiin. Se on suositeltava tapa, jolla järjestelmänvalvojat voivat ottaa Office-apuohjelmia käyttöön organisaatiossasi oleville käyttäjille ja ryhmille.

> [!NOTE]
> Katso Business Central on-premises -versiolle järjestelmänvalvojan sisällössä ohjeaihe [Outlook-integraation apuohjelman määrittäminen Business Central on-premises -versiolle](/dynamics365/business-central/dev-itpro/administration/setting-up-office-add-ins-outlook-inbox) (vain englanniksi).

### <a name="prerequisites" />Vaatimukset

- Microsoft 365 -tilaus  
- Käyttäjille on määritetty Microsoft 365 -käyttöoikeus.  
- Microsoft 365 -tilillä on *Yleinen järjestelmänvalvoja*- tai *Exchange-järjestelmänvalvoja* -rooli

### <a name="deploy-the-add-in" />Apuohjelman käyttöönotto

1. Valitse Business Centralissa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Asetusten ohjattu määritys** ja valitse sitten vastaava linkki.
2. Valitsemalla **Outlook-lisäohjelman keskitetty käyttöönotto** voit käynnistää avustetun asennusoppaan.
3. Tarkista ensimmäinen sivu ja avaa sivu apuohjelmien lataamista varten valitsemalla **Seuraava**.
4. Valitse **Käyttöönotto**-sarakkeesta käyttöönotettavien apuohjelmien valintaruutu ja valitse sitten **Lataa ja jatka**.

    Laitteeseen ladataan tiedosto, jonka nimi on *OutlookAddins.zip*

5. Tässä vaiheessa olet suorittanut kaiken Business Centralissa, joten voit valita **Valmis**.

   >[!TIP]
   > Ennen kuin valitset **Seuraava**, valitse **Siirry Microsoft 365:een (avautuu uuteen ikkunaan)** -linkki avataksesi ja kirjautuaksesi Microsoft 365 -hallintakeskukseen uudessa selainikkunassa. Sinun on kuitenkin mentävä Microsoft 365 -hallintakeskukseen myöhemmässä vaiheessa.

6. Siirry kansioon, johon OutlookAddins.zip on ladattu, ja pura **Contact Insights.xml**- ja **Document View.xml**-tiedostot haluamaasi kansioon.

    Lisätietoja on artikkelissa [Tiedostojen ja kansioiden pakkaaminen ja purkaminen](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).
7. Kirjaudu Microsoft 365 -hallintakeskukseen ja valitse sitten [Integroidut sovellukset](https://go.microsoft.com/fwlink/?linkid=2163967).

8. Valitse **Lataa mukautetut sovellukset**.
9. Valitse **Lataa käyttöön otettavat sovellukset** -sivulla **Lataa luettelotiedosto (.xml) laitteesta** > **Valitse tiedosto**.
10. Valitse jokin aiemmin puretuista lisätiedostoista, esimerkiksi **Contact Insights.xml**.
11. Määritä käyttäjät ja ota apuohjelma käyttöön noudattamalla ohjeita.
12. Toista vaiheet 9-11 halutessasi muille apuohjelmille.

> [!IMPORTANT]
> Vihreä valintamerkki tulee näkyviin, kun apuohjelma otetaan käyttöön hallintakeskuksessa. Outlook-sovelluksen käyttöönotto käyttäjille voi kuitenkin kestää 24 tuntia. Käyttäjät voivat myös joutua käynnistämään Outlookin uudelleen.

Kun olet valmis, voit aina muuttaa käyttöönottoa Microsoft 365 -hallintakeskuksessa, kuten määrittää useampia käyttäjiä. Lisätietoja apuohjelmien käyttöönotosta hallintakeskuksessa on kohdassa [Apuohjelmien käyttöönotto hallintakeskuksessa](/microsoft-365/admin/manage/centralized-deployment-faq?view=o365-worldwide#how-do-you-target-add-in-user-assignments-with-centralized-deployment-&preserve-view=true).

## <a name="a-nameinstallainstall-the-add-in-for-your-own-use" /><a name="install"></a>Apuohjelman asentaminen omaan käyttöön

Jos organisaatiosi sen sallii, voit asentaa Business Central -apuohjelman vain itseäsi varten. Jos et ole varma, kysy järjestelmänvalvojalta.

1. Valitse Business Centralissa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Hanki Outlook-apuohjelma** ja valitse sitten liittyvä linkki.
2. Lue sivu ja valitse **Seuraava**, kun olet valmis.
3. Jos haluat saada Business Centralin tervetulosähköpostiviestin, jossa on yleiskatsaus lisäosan käyttämisestä, ota käyttöön **Lähetä esimerkkisähköpostiviesti**.
4. Valitse **Valmis** asennuksen viimeistelemiseksi.

Business Central muodostaa yhteyden sähköpostipalvelimeen ja asentaa apuohjelman Outlookiin. Tämä ei vie kauan. Olet nyt valmis aloittamaan apuohjelman käyttämisen Outlookissa.

### <a name="a-nameonpremafor-business-central-on-premises" /><a name="onprem"></a>Business Central on-premises -versiolle

Jos käytät Business Centralin on-premises -asennusta, apuohjelman asentaminen voi olla hieman erilaista.

1. Valitse Business Centralissa ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, kirjoita **Hanki Outlook-apuohjelma** ja valitse sitten liittyvä linkki.
2. Lue sivu ja valitse **Seuraava**, kun olet valmis.
3. Valitse jokin seuraavista vaiheista sen mukaan, mikä sivu näkyy:

    - Jos näet **Asenna omaan Outlookiin** -painikkeen, valitse se ja olet valmis.
    - Jos näet **Seuraava**-painikkeen, valitse se. Jos haluat saada Business Centralin tervetulosähköpostiviestin, jossa on yleiskatsaus lisäosan käyttämisestä, ota seuraavalla sivulla käyttöön **Lähetä esimerkkisähköpostiviesti**. Valitse sitten **Valmis**, niin olet valmis.
    - Jos näet **Lataa lisäosa** -painikkeen, valitse se ja siirry seuraavaan vaiheeseen.
4. Kun valitset **Lataa lisäosa**, laitteeseen ladataan tiedosto, jonka nimi *OutlookAddins.zip*. Sinun pitäisi nähdä tiedosto selaimen yläreunassa.

   Siirry kansioon, johon OutlookAddins.zip on ladattu, ja pura **Contact Insights.xml**- ja **Document View.xml**-tiedostot haluamaasi kansioon. Lisä tietoja tiedostojen purkamisesta on ohjeaiheessa [Tiedostojen ja kansioiden pakkaaminen ja purkaminen](https://support.microsoft.com/en-us/windows/zip-and-unzip-files-8d28fa72-f2f9-712f-67df-f80cf89fd4e5).

5. Avaa Outlook ja valitse valintanauhasta **Hae apuohjelmia**. Jos käytät Outlookia verkossa, valitse avattavasta valikosta uudessa tai olemassa olevassa sähköpostiviestissä ja valitse sitten **Hae apuohjelmat**.
6. Valitse **Omat apuohjelmat** > **Lisää mukautettu apuohjelma** > **Lisää tiedostosta**.
7. Valitse jokin puretuista .xml-tiedostoista, kuten **Contact Insights.xml**, ja valitse sitten **Avaa** > **Asennus**.
8. Toista vaiheet 6 ja 7 muille .xml-tiedostoille, jos latasit sellaisia.

Olet nyt valmis aloittamaan apuohjelman käyttämisen Outlookissa.

## <a name="see-related-microsoft-trainingtrainingmodulesalternative-interfaces-dynamics-365-business-centralindex" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/alternative-interfaces-dynamics-365-business-central/index)

## <a name="see-also" />Katso myös

[Valmistautuminen liiketoimintaan](ui-get-ready-business.md)  
[Business Centralin hakeminen omaan mobiililaitteeseen](install-mobile-app.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Rahoitus](finance.md)  
[Myynti](sales-manage-sales.md)  
[Osto](purchasing-manage-purchasing.md)  
[Outlookin vähimmäisvaatimukset](product-requirements.md#outlook)  
[Apuohjelmien käyttäminen Outlookin verkkoversiossa](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
