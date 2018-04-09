---
title: "Dimensioiden käyttäminen| Microsoft Docs"
description: "Voit käyttää dimensioita tapahtumien luokitteluun esimerkiksi osasto- tai projektikohtaisesti, jonka ansiosta tietojen seuranta ja analysointi helpottuu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 349a4d54a95999e3e2c2b19cc2a40c2dd1afd445
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-dimensions"></a>Dimensioiden käyttäminen
Voit yksinkertaistaa asiakirjojen, kuten myyntitilausten, analysointia dimensioiden avulla. Dimensiot ovat tapahtumia luokittelevia määritteitä ja arvoja, joita voi seurata ja analysoida. Dimensioiden avulla voit esimerkiksi ilmaista, mistä projektista tai osastosta tapahtuma on lähtöisin.  

Jos käytät dimensioita, sinun ei esimerkiksi tarvitse määrittää erillisiä kirjanpitotilejä kullekin osastolle ja projektille. Tämä mahdollistaa monipuolinen analysoinnin ilman monimutkaisen tilikartan luontia. Lisätietoja on ohjeaiheessa [Business Intelligence](bi.md).

Voit myös esimerkiksi määrittää *Osasto*-nimisen dimension ja käyttää sitä myyntiasiakirjojen kirjaamisen yhteydessä. Voit sitten käyttää BI-työkaluja, jos haluat selvittää, mitä nimikkeitä kukin osasto myy.
Mitä useampia dimensioita käytät, sitä yksityiskohtaisempia raportteja voit käyttää liiketoimintapäätösten apuna. Yksittäisessä myyntitapahtumassa voi esimerkiksi olla useita dimensiotietoja, kuten  

* tili, jolle nimikkeen myynti on kirjattu  
* nimikkeen myyntipaikka
* nimikkeen myyjä
* nimikkeen ostaneen asiakkaan tyyppi.  

## <a name="analyzing-by-dimensions"></a>Analyysi dimensioittain
Dimensiotoiminnot ovat tärkeä osa liiketoimintatietoja esimerkiksi analyysinäkymiä määritettäessä. Lisätietoja on kohdassa [Tietojen analysointi dimensioittain](bi-how-analyze-data-dimension.md).

> [!TIP]
> Tapahtumatietoja voi analysoida nopeasti dimensioiden mukaan suodattamalla tilikarttojen loppusummat ja kaikkien **Tapahtumat**-ikkunoiden tapahtumat dimensioittain. Hae **Määritä dimension suodatus** -toiminto.

## <a name="dimension-sets"></a>Dimensioyhdistelmät
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Kun luot päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

## <a name="setting-up-dimensions"></a>Dimensioiden luominen
Voit määrittää päiväkirjojen ja asiakirjojen, kuten myynti- ja ostotilausten, luokitteluun käytettävät dimensiot ja dimension arvot. Dimensiot määritetään **Dimensiot**-ikkunassa, jossa kullekin dimensiolle luodaan yksi rivi. Dimensioita ovat esimerkiksi *Projekti*, *Osasto*, *Alue* ja *Myyjä*.

Voit määrittää myös arvoja dimensioille. Arvot voivat olla esimerkiksi yrityksen osastoja. Dimension arvot voi määrittää tilikartan kaltaisessa hierarkkisessa rakenteessa, jossa tiedot voi jakaa rakeisuustason mukaan ja jossa dimension arvojen osajoukoista voi laskea summat. Voit määrittää tarvitsemasi määrän dimensiota ja dimension arvoja, ja ne ovat yrityksessä kaikkien käytössä.

Voit määrittää myös joitakin globaaleja dimensioita ja pikadimensioita:  

* **Globaaleja dimensioita** käytetään suodattimina esimerkiksi raporteissa ja erätöissä. Käytössä on vain kaksi globaalia dimensiota, joten valitse usein käytetyt dimensiot.
* **Pikadimensiot** ovat käytössä kenttinä päiväkirjan ja asiakirjan riveillä. Voit luoda niitä enintään kuusi.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Oletusdimensioiden määrittäminen asiakkaille, toimittajille ja muille tileille
Voit määrittää oletusdimension tietylle tilille. Dimensio kopioidaan päiväkirjaan tai asiakirjaan, kun lisäät tilinumeron riville, mutta voit tarvittaessa poistaa koodin rivillä tai muuttaa sitä. Voit määrittää myös dimension, jota tarvitaan tietyn tyyppisen tilitapahtuman kirjaamiseen.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Dimensiot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse ensin **Dimensiot**-ikkunassa sopiva dimensio ja sitten **Tilityypin oletusdimensio** -toiminto.  
4.  Täytä rivi kutakin uutta oletusdimensiota varten, jonka haluat määrittää. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Jos haluat tehdä dimensiosta pakollisen, mutta et halua määrittää dimensiolle oletusarvoa, jätä **Dimension arvokoodi** -kenttä tyhjäksi ja valitse **Arvon kirjaaminen** -kentässä **Pakollinen koodi**.  

> [!WARNING]  
>  Jos tiliä käytetään **Muuta vaihtokursseja** -eräajossa tai **Kirjaa varaston kustannus KP:oon** -eräajossa, älä valitse **Koodi pakollinen**- tai **Sama koodi** -vaihtoehtoa. Näissä eräajoissa ei voi käyttää dimensiokoodeja.  

> [!NOTE]  
>  Jos tiliin täytyy liittää dimensio, joka poikkeaa tilityypille määritetystä oletusdimensiosta, sinun täytyy määrittää tälle tilille oletusdimensio. Yksittäisen tilin oletusdimensio korvaa siten tilityypin oletusdimension.  

### <a name="to-set-up-default-dimension-priorities"></a>Oletus dimensioprioriteettien luominen  
Eri tilityypeille, esimerkiksi asiakas- ja nimiketileille, voi olla määritelty erilaiset oletusdimensiot. Siten ohjelma voi ehdottaa tapahtumalle useampaa kuin yhtä oletusdimensiota. Jotta sellaisia ristiriitatilanteita ei syntyisi, voit soveltaa eri lähteisiin prioriteettisääntöjä.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Oletusdimensioprioriteetit** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Kirjoita **Oletusdimensioprioriteetit**-ikkunassa **Lähdekoodi**-kenttään sen tapahtumataulukon lähdekoodi, johon oletusdimension prioriteetteja sovelletaan.  
3.  Täytä rivi kutakin oletusdimension prioriteettia varten, jonka haluat valitulle lähdekoodille.
4.  Toista vaiheet kullekin lähdekoodille, jolle haluat määrittää oletusdimension prioriteetit.  

> [!IMPORTANT]  
>  Jos luot kaksi taulukkoa, joilla on sama lähdekoodin prioriteetti, [!INCLUDE[d365fin](includes/d365fin_md.md)] hakee aina taulukon, jolla on pienin tunnus.  

### <a name="to-set-up-dimension-combinations"></a>Dimensioiden kombinaatioiden luominen  
Kun haluat estää sellaisten tapahtumien kirjauksen, joissa on väärät tai keskenään ristiriitaiset dimensiot, voit lukita tai rajoittaa tiettyjä kahden kombinaation yhdistelmiä. Lukittu dimensioyhdistelmä tarkoittaa, että et voi kirjata molempia dimensioita samaan tapahtumaan, riippumatta dimension arvoista. Rajoitettu dimensioyhdistelmä sallii molempien dimensioiden kirjaamisen samaan tapahtumaan, mutta vain tiettyjen dimension arvoyhdistelmien osalta.

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Dimension kombinaatiot** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Dimension kombinaatiot**-ikkunassa dimensioyhdistelmän kentässä ja valitse jokin seuraavista vaihtoehdoista:  

    |Kenttä|Description|
    |----------------------------------|---------------------------------------|  
    |**Ei rajoituksia**|Tällä dimensioyhdistelmällä ei ole rajoituksia. Kaikki dimensioarvot ovat sallittuja.|  
    |**Rajoitettu**|Tällä dimensioyhdistelmällä on rajoituksia, jotka ovat riippuvaisia syöttämistäsi dimensioarvoista. Sinun täytyy määritellä rajoitukset **Dimension arvokombinaatiot** -ikkunassa.|  
    |**Lukittu**|Tämä dimension kombinaatio ei ole sallittu.|  

3.  Jos valitsit vaihtoehdon **Rajoitettu**-asetuksen, sinun täytyy määrittää, mitkä dimensioarvojen yhdistelmät on lukittu. Tee tämä valitsemalla kenttä määrittääksesi dimensioyhdistelmän.  
4.  Valitse seuraavaksi lukittu dimension arvoyhdistelmä ja määritä kenttään arvo **Lukittu**. Tyhjä kenttä tarkoittaa, että kyseinen dimension arvoyhdistelmä on sallittu. Toista nämä toimet, jos lukittuja yhdistelmiä on useita.  

> [!NOTE]  
>  Samat dimensiot näkyvät sekä riveillä että sarakkeissa, ja siksi kaikki dimensioyhdistelmät näkyvät kaksi kertaa. [!INCLUDE[d365fin](includes/d365fin_md.md)] näyttää asetuksen automaattisesti molemmissa kentissä. Et voi valita mitään niissä kentissä, jotka ovat vasemmassa yläkulmassa ja siitä alaspäin, koska näissä kentissä on sama dimensio sekä riveillä että sarakkeissa.  
>   
>  Valittu vaihtoehto ei ole näkyvissä ennen kuin poistut kentästä.  
>   
>  Jos haluat, että dimensiosta näkyy mieluummin nimi kuin koodi, laita ruksi **Näytä sarakkeen nimi** -kenttään.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Useita kertoja käytettyjen dimensioiden yhteenvedon hakeminen
**Oletusdimensiot-useita** -ikkuna määrittää, miten tiliryhmä käyttää dimensioita ja dimensioarvoja. Voit tehdä sen aktivoimalla useamman tilin ja määrittelemällä sitten oletusdimensiot ja dimensioarvot kaikille niille tileille, jotka aktivoit tililuettelossa. Kun määrittelet aktivoiduille tileille oletusdimensioita, ohjelma ehdottaa näitä dimensioita ja dimension arvoja aina kun jotakin näistä tileistä käytetään, esimerkiksi päiväkirjan rivillä. Käyttäjän kannalta tämä helpottaa tapahtumien kirjaamista, sillä dimensiokentät täytetään automaattisesti. Ehdotettuja dimension arvoja voidaan kuitenkin muuttaa, esimerkiksi päiväkirjan rivillä.

**Oletusdimensiot-useita** -ikkunassa on seuraavat kentät:
|Kenttä|Description|
|----------------------------------|---------------------------------------|  
|**Dimensiokoodi**|Tässä kentässä näkyvät kaikki dimensiot, jotka on määritetty oletusdimensioksi yhdellä tai useammalla aktivoidulla tilillä. Valitsemalla kentän näet listan kaikista käytettävissä olevista dimensioista. Jos valitset dimension, valittu dimensio määritetään oletusdimensioksi kaikille korostettuina oleville tileille.|
|**Dimension arvokoodi**|Näkyy joko yksittäisen dimensioarvo tai termin (ristiriita). Jos kentässä näkyy dimension arvo, niin kaikilla aktivoiduilla tileillä on sama oletusdimension arvo. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa dimension oletusarvoa. Napsauttamalla kentässä AssistButtonia saat näkyviin luettelon yhden dimension kaikista käytettävissä olevista dimensioarvoista. Jos valitset dimension arvon, valittu dimension arvo määritetään oletusdimension arvoksi kaikille korostettuina oleville tileille.|
|**Arvon kirjaaminen**|Tässä kentässä näkyy joko yksittäinen arvokirjaussääntö tai termi (Ristiriita). Jos kentässä näkyy arvokirjaussääntö, niin kaikilla aktivoiduilla tileillä on sama arvokirjaussääntö dimension arvoa koskien. Jos kentässä näkyy termi (Ristiriita), niin kaikilla aktivoiduilla tileillä ei ole samaa arvokirjaussääntöä dimension arvoa koskien. Napsauttamalla AssistButtonia Arvon kirjaus -kentässä saat näkyviin luettelon arvokirjaussäännöistä. Jos valitset arvokirjaussäännön, valittua arvokirjaussääntöä käytetään kaikille korostettuina oleville tileille.|

### <a name="example-of-dimension-setup"></a>Esimerkki dimension asetuksista
Oletetaan, että yritys haluaa seurata tapahtumia organisaatiorakenteen ja maantieteellisen sijainnin perusteella. Määrität tätä tarkoitusta varten kaksi dimensiota **Dimensiot**-ikkunassa:

* **ALUE**  
* **OSASTO**  

| koodi | Name | Koodin otsikko | Suodattimen otsikko |
| --- | --- | --- | --- |
| ALUE |Alue |Aluekoodi |Aluesuodatus |
| OSASTO |Osaston |Osaston koodi |Osastosuodatus |

Lisää **ALUE**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| 10 |Pohjois- ja Etelä-Amerikka |Alkusumma |
| 20 |Pohjois-Amerikka |Vakio |
| 30 |Tyynimeri |Vakio |
| 40 |Etelä-Amerikka |Vakio |
| 50 |Pohjois- ja Etelä-Amerikka, yhteensä |Loppusumma |
| 60 |Eurooppa |Alkusumma |
| 70 |EU |Vakio |
| 80 |Muu kuin EU |Vakio |
| 90 |Eurooppa, Yhteensä |Loppusumma |

Voit lisätä kahteen päätason maantieteelliseen alueeseen, Pohjois- ja Etelä-Amerikkaan sekä Eurooppaan, alueellisia alaluokkia alueiden sisentämällä dimension arvot. Tällä tavoin voit raportoida aluekohtaisen myynnin tai kulut ja saada kokonaissumman suurille maantieteellisille alueille. Olisit voinut käyttää dimension arvoina myös maita tai alueita – tai maakuntia tai paikkakuntia sen mukaan, mikä on liiketoiminnan kannalta järkevintä.  
> [!NOTE]  
>   Hierarkian määrittämistä varten koodien on oltava aakkosjärjestyksessä. Myös [!INCLUDE[d365fin](includes/d365fin_md.md)]iin sisältyvät dimension arvojen koodit on otettava tässä huomioon.  

Lisää **OSASTO**-koodiin seuraavat dimension arvot:

| koodi | Name | Dimension arvotyyppi |
| --- | --- | --- |
| HALLINTA |Hallinta |Vakio |
| TUOT |Tuotanto |Vakio |
| MYYNTI |Myynti |Vakio |

Näillä asetuksilla voit sitten lisätä kaksi dimensiota kahtena globaalina dimensiona **Pääkirjanpidon asetukset** -ikkunassa. Niinpä voit käyttää ALUE- ja OSASTO-koodeja pääkirjanpidon tapahtumien suodattamina sekä kaikissa raporteissa ja eräajoissa. Molemmat globaalit dimensiot ovat myös automaattisesti käytettävissä pikadimensioina tapahtumariveillä ja asiakirjojen otsikoissa.  

## <a name="using-dimensions"></a>Dimensioiden käyttäminen
Voit lisätä asiakirjaan, kuten esimerkiksi myyntitilaukseen, dimension tiedot sekä yksittäiseen asiakirjariviin että itse asiakirjaan. Voit antaa esimerkiksi **Myyntitilaus**-ikkunassa kahden ensimmäisen pikadimension dimension arvot yksittäisillä myyntiriveillä. Voit myös lisätä lisää dimension tietoja valitsemalla **Dimensiot**-painikkeen.  

Jos käsittelet sen sijaan päiväkirjaa, voit lisätä dimension tietoja tapahtumaan samalla tavalla, jos olet määrittänyt pikadimensiot kentiksi suoraan päiväkirjan riveille.  

Voit määrittää tileille tai tilityypeille oletusdimensioita, jolloin dimensiot tai dimensioiden arvot täytetään automaattisesti.

## <a name="to-view-global-dimensions-in-ledger-entry-windows"></a>Globaalien dimensioiden tarkastelu tapahtumaikkunoissa  
Globaalit dimensiot ovat aina yrityskohtaisia ja yrityksen nimeämiä. Voit tarkastella yrityksen globaaleja dimensioita avaamalla **Pääkirjanpidon asetukset** -ikkunan.  

Tapahtumaikkunasta näet, onko tapahtumille globaaleja dimensioita. Kaksi globaalia dimensiota eroavat muista siinä, että niitä voi käyttää suodattimena missä tahansa [!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman osassa.  

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, syötä **Tilikartta** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Tilikartta**-ikkunassa **Tapahtumakirjaukset**-toiminto.  
3.  Jos haluat nähdä vain merkitykselliset tapahtumat, määritä ikkunassa vähintään yksi suodatin.  
4.  Jos haluat nähdä tapahtuman kaikki dimensiot, valitse ensin tapahtuma ja sitten **Dimensiot**-toiminto.  

> [!NOTE]  
>  **Tapahtuman dimensiot** -ikkunassa näkyy kerralla yhden tapahtuman dimensiot. Kun selaat tapahtumia, **Tapahtuman dimensiot** -ikkunan sisältö muuttuu vastaavasti.  

## <a name="see-also"></a>Katso myös
[Business Intelligence](bi.md)  
[Rahoitus](finance.md)  
[Tietojen analysointi dimensioiden mukaan](bi-how-analyze-data-dimension.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
