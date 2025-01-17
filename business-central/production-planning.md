---
title: Toimitusten suunnittelu
description: Valmistele myynti- ja tuotantotarvetta varten seikkaperäinen ja toteuttamiskelpoinen suunnitelma sekä viimeistelykokoonpanon tuotantoaikataulu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.for: '291, 292, 293, 295, 517, 9010, 9038'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="planning" />Suunnittelu

Tuotanto-operaatiot, joita tarvitaan panoksen muuttamiseen lopputuotteiksi, on suunniteltava päivittäin tai viikoittain volyymin ja tuotteiden luonteen mukaan. [!INCLUDE[prod_short](includes/prod_short.md)] sisältää toimintoja, joiden avulla voidaan vastata myynnin, kokoonpanon ja tuotannon ennakoituun ja todelliseen kysyntään. Lisäksi siinä on toimintoja, joita käytetään jakelun suunnitteluun varastointiyksiköiden ja sijaintisiirtojen avulla.

> [!NOTE]
> Tässä ohjeaiheessa käsitellään lähinnä tuotantoon tai kokoonpanon hallintaan liittyviä yrityksiä, joissa toimitustilaukset voivat olla tuotanto-, kokoonpano-, siirto- tai ostotilauksia. Tämä suunnittelutyö tehdään pääasiassa **Suunnittelutyökirja**-sivulla.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] tukee myös niitä tukkukaupan yritysten toimitussuunnittelua, joissa syntyvät toimitustilaukset voivat olla vain siirto- tai ostotilauksia. Tämä suunnittelutyö tehdään pääasiassa **Hankintalista**-sivulla, jota käsitellään epäsuorasti tässä ohjeaiheessa, sillä useimmat suunnittelutoiminnot koskevat molempia sivuja.

Suunnittelu voidaan nähdä valmistautumisena tarvittaviin tilauksiin myynti-, kokoamis- tai valmistusosastoilla myyntien toteuttamiseksi tai tuotteiden tarpeen lopettamiseksi. Lisätietoja, katso [Ostaminen](purchasing-manage-purchasing.md), [Kokoonpanon Hallinta](assembly-assemble-items.md) ja [Valmistus](production-manage-manufacturing.md)

Seuraavassa taulukossa on tehtäväsarja ja linkit tehtäviä käsitteleviin aiheisiin.  

|**Tehtävä**|**Katso**|  
|------------|-------------|  
|Tutustu lyhyeen esittelyyn suunnittelujärjestelmän käytöstä kysynnän tunnistamisessa ja priorisoinnissa sekä tasapainotetun toimitussuunnitelman ehdottamisessa.|[Tietoja toimintojen suunnittelusta](production-about-planning-functionality.md)|
|Ymmärrä kuinka kaikki suunnitelusysteemin osa-alueet toimivat ja kuinka muokata algoritmejä suunnitelutarpeiden vastaamiseen eilaisissa ympäristöissä.|[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)|
|Tutustu, miten suunnittelulogiikka tekee eron sijaintien kysynnän välillä varastointiyksikön asetusten mukaan ja silloin, kun kysynnällä ei ole sijaintikoodeja.|[Suunnittelu sijainteja käyttämällä tai ilman niitä](production-planning-with-without-locations.md)|
|Ennustettu kysyntä odotetun myynnin ja tuotannon komponenttien perusteella.|[Kysyntäennusteen luominen](production-how-to-create-a-forecast.md)|  
|Luo myyntitilauksesta riippuvaisia tilauksia tai projektituotantotilauksia, jotka kattavat täsmällisesti myyntitilausrivin kysynnän.|[Tuotantotilausten luominen myyntitilauksista:](production-how-to-create-production-orders-from-sales-orders.md)|
|Käytä **Tilauksen suunnittelu** -sivua, jonka avulla voit suunnitella myynnin tai tuotantokysynnän manuaalisesti yksi tuotannon tuoterakenne kerrallaan.|[Uuden kysynnän tilauskohtainen suunnittelu](production-how-to-plan-for-new-demand.md)|
|Voit suorittaa **Suunnittelutyökirja**-sivulla sekä tuotanto-ohjelman että tarvelaskennan ja luoda niiden avulla joko ylätason tai yksityiskohtaisen toimitussuunnitelman kaikilla nimiketasoilla.|[Kokonaisvaltaisen suunnittelun, tuotanto-ohjelman tai tarvelaskennan suorittaminen](production-how-to-run-mps-and-mrp.md)|
|Käytä **Hankintatyökirja**-sivua luodaksesi automaattisesti yksityiskohtaisen toimitussuunnitelman, joka kattaa sellaisten nimikkeiden kysynnän, joita täydennetään vain ostojen tai siirtojen avulla.|[Hankintatyökirja](production-about-planning-functionality.md#requisition-worksheet)|  
|Aloita tai päivitä tuotantotilaus raakasuunniteltuna operaationa päätuotantoaikataulussa.|[Tuotantotilausten suora uudelleensuunnittelu tai päivittäminen](production-how-to-replan-refresh-production-orders.md)|
|Laske tuotantosolun tai kuormitusryhmän kalenterit uudelleen suunnittelun muutosten vuoksi.|[Tuotantosolun kalenterin laskeminen](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Seuraa tilauskysyntää (seurattu määrä), ennustetta, myyntipuitetilausta tai suunnitteluparametria (ei-seurattu määrä), joka on kiinnittänyt huomion kyseiseen suunnitteluriviin.|[Kysynnän ja tarjonnan välisten suhteiden seuraaminen](production-how-track-demand-supply.md)|
|Tarkastele nimikkeen suunniteltua saatavilla olevaa varastoa erilaisissa näkymissä ja katso, mitkä bruttotarpeet, suunnitellut tilausten vastaanotot ja muut tekijät vaikuttavat varastoon tietyn ajan kuluessa.|[Nimikkeiden saatavuuden tarkasteleminen](inventory-how-availability-overview.md)|  
<!--|Suorita valitut suunnitellut tehtävät, kuten suunnittelutyökirjan rivien muuttaminen tai lisääminen, toimitussuunnitelma graafisessa näkymässä.|[Suunnitteluehdotusten muokkaaminen graafisessa näkymässä](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|-->

## <a name="see-related-microsoft-trainingtrainingmodulesplan-items-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/plan-items-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Varasto](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Tarjonnan suunnittelu](design-details-supply-planning.md)  
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
