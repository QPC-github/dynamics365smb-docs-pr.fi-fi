---
title: Uusien asiakkaiden rekisteröiminen asiakkaan kortin luomisen avulla (sisältää videon)
description: 'Tässä ohjeaiheessa kerrotaan, miten asiakkaan kortti luodaan rekisteröimään tietoja kustakin uudesta asiakkaasta, jolle myyt.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="register-new-customers" />Uusien asiakkaiden rekisteröinti

Asiakkaat ovat tulonlähteesi. Jokainen asiakas, jolle myyt, on rekisteröitävä asiakaskorttina. Asiakkaan kortit sisältävät tietoja, jotka tarvitaan tuotteiden asiakkaalle myymistä varten. Lisätietoja on kohdissa [Myyntien laskuttaminen](sales-how-invoice-sales.md) ja [Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md).  

Ennen kuin voit rekisteröidä uusia asiakkaita, sinun on määritettävä myyntikoodit, jotka voidaan valita asiakkaiden korttien täyttämisen yhteydessä. Lisätietoja kohdassa [Myynnin määrittäminen](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers" />Uusien asiakkaiden lisääminen

Voit lisätä uusia asiakkaita manuaalisesti täyttämällä **Asiakaskortti**-sivun tai käyttämällä malleja, jotka sisältävät ennalta määritettyjä tietoja. Voit esimerkiksi luoda mallin erityyppisille asiakasprofiileille. Mallien käyttäminen säästää aikaa uusien asiakkaiden lisäämisen aikana ja varmistaa, että tiedot ovat aina oikein. 

Jos luot:
* Malleja useammalle kuin yhdelle asiakastyypille, voit valita sopivan mallin, jota käytetään, kun lisäät asiakkaan.
* Vain yhden mallin, jota käytetään kaikille uusille asiakkaille. 

Kun olet luonut mallin, voit kohdistaa sen yhteen tai useampaan valittuun asiakkaaseen käyttämällä **Käytä mallia** -toimintoa. Kun haluat luoda mallin, täytä tiedot, joita käytetään uudelleen **Asiakkaan kortti** -sivulla, ja tallenna se mallina. Lisätietoja on [Asiakaskortin tallentaminen mallina](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template) -osassa.

> [!TIP]
> Voi olla hyödyllistä mukauttaa **Asiakasmalli**-sivua, kun luot mallin. Haluat ehkä esimerkiksi lisätä **Luottoraja**-kentän malliin. Lue lisätietoja [Työtilan mukauttaminen](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner) -osassa.

Asiakkaan voi luoda myös yhteyshenkilöstä. Lisätietoja on [Asiakkaan, toimittajan, työntekijän tai pankkitilin luominen yhteyshenkilöstä](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact) -osassa.  

### <a name="to-create-a-new-customer-card" />Uuden asiakkaan kortin luominen

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

**Hinnat ja alennukset** -toiminto tarjoaa vaihtoehtoja asiakkaan erikoishintojen tai -alennusten hallintaan, kun tilaus täyttää tietyt ehdot. Ehdot voivat olla esimerkiksi silloin, kun he ostavat tietyn nimikkeen, tilaavat vähimmäismäärän tai ostavat ennen päivämäärää, kuten kampanjan loppuessa. Lue lisätietoja kohdasta [Myyntihinnan, alennuksen ja maksusopimusten tallentaminen](sales-how-record-sales-price-discount-payment-agreements.md).

Asiakas on nyt rekisteröity, ja asiakkaan kortti on valmis käytettäväksi myyntiasiakirjoissa.  

### <a name="to-save-the-customer-card-as-a-template" />Asiakkaan kortin tallentaminen mallina

Voit käyttää asiakkaan korttia mallina, kun luot uusia asiakkaan kortteja.

1. Valitse **Asiakkaan kortti** -sivulla **Tallenna mallina** -toiminto. **Asiakasmalli**-sivu avautuu ja näyttää asiakaskortin mallina.
2. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Voit käyttää dimensioita malleina valitsemalla **Dimensiot**-toiminnon. **Dimensiomallit**-sivu avautuu. Se sisältää kaikki asiakkaalle määritetyt dimensiokoodit.
4. Muokkaa tai syötä dimensiokoodit, joita käytetään tämän mallin avulla luotuihin uusiin asiakkaan kortteihin.  
5. Kun olet määrittänyt uuden asiakasmallin, valitse **OK**.

Asiakasmalli lisätään asiakasmallien luetteloon ja sen avulla voit luoda uusia asiakkaiden kortteja.

## <a name="deleting-customer-cards" />Asiakaskorttien poistaminen

Jos olet kirjannut asiakkaalle tapahtuman, et voi poistaa asiakkaan korttia, koska nimiketapahtumia voi tarvita valvontaan. Voit poistaa asiakaskortin, jossa on tapahtumakirjauksia ottamalla yhteyttä Microsoft-kumppaniisi koodin avulla.  

## <a name="managing-credit-limits" />Luottorajojen hallinta

Luottoraja-, saldosumma- ja maksuehto-ominaisuudet mahdollistavat sen, että [!INCLUDE [prod_short](includes/prod_short.md)] antaa luottovaroituksen ja erääntynyt saldo -varoituksen tullessasi myyntitilaukseen. Lisäksi muistutusehto- ja rahoitusmaksuehtoelementit mahdollistavat koron ja/tai lisäkulujen laskutuksen.  

Asiakaskortin **Luottoraja**-kentässä määritetään enimmäissumma, jonka sallit asiakkaan ylittää maksusaldon ennen varoitusten antamista. Kun sitten syötät tietoja päiväkirjoihin, tarjouksiin, tilauksiin ja laskuihin, [!INCLUDE [prod_short](includes/prod_short.md)] testaa myynnin tunnistetiedot ja yksittäiset myyntirivit ja tarkistaa, onko luottoraja ylitetty.

Jos luottoraja on ylitetty, silti voidaan kirjata. Jos kenttä on jätetty tyhjäksi, tällä asiakkaalla ei ole luottorajaa.  

Voit valita, ettet saa varoitusta siitä, että asiakkaan luottoraja on ylitetty, ja voit määrittää, minkä tyyppisiä varoituksia haluat nähdä.

### <a name="to-specify-credit-limit-warnings" />Luottorajavaroitusten määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntien ja myyntisaamisten asetukset**, valitse sitten vastaava linkki.

2. Valitse **Yleiset**-pikavälilehden **Luottovaroitukset**-kentässä haluamasi vaihtoehdot seuraavassa taulukossa kuvatulla tavalla:

    |Asetus| Kuvaus|
    |------|------------|
    |**Molemmat varoitukset**| Kun käytät tätä vaihtoehtoa, ohjelma tarkastaa sekä **Luottoraja**- että **Erääntyvä saldo**-kentät asiakaskortista ja antaa varoituksen, jos asiakas ylittää luottorajansa, ja jos asiakkaalla on erääntynyt saldo.|
    |**Luottoraja**|Asiakaskortin **Luottoraja**-kentän arvoa verrataan asiakkaan saldoon, ja näyttöön tulee varoitus, jos asiakkaan saldo ylittää kentän arvon.|
    |**Erääntynyt saldo**|**Erääntynyt saldo** -kenttä asiakkaan kortilla on valittuna ja jos asiakkaalla on erääntyneitä saldoja, näytetään varoitus.|
    |**Ei varoitusta**|Asiakkaan tilasta ei näytetä luottovaroituksia.|

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/trade-master-data-dynamics-365-business-central/).

## <a name="see-also" />Katso myös

[Maksutapojen määrittäminen](finance-payment-methods.md)  
[Tietueiden kaksoiskappaleiden yhdistäminen](sales-how-merge-duplicate-records.md)  
[Numerosarjojen luominen](ui-create-number-series.md)  
[Ota käyttöön osittaiset toimitukset toimitusneuvoilla](sales-how-send-partial-shipments.md)  
[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Sijaintien ja reittiohjeiden etsiminen online-karttojen avulla](across-online-maps.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
