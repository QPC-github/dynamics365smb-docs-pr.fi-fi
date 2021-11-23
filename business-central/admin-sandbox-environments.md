---
title: Eristysympäristöt
description: Lisätietoja siitä, miten erillisen ympäristön avulla voit turvallisesti tutkia, oppia, esitellä, kehittää, ratkaista ja testata Business Centralin ominaisuuksia.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 07/27/2021
ms.author: solsen
ms.openlocfilehash: db390d1f4ee690b9e461bfccd77155ec0b66a2b6
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589373"
---
# <a name="sandbox-environments-in-prod_short"></a>Eristysympäristöt [!INCLUDE[prod_short](includes/prod_short.md)] -ratkaisussa

[!INCLUDE[prod_short](includes/prod_short.md)] onlinen avulla voit helposti luoda turvallisen ympäristön, jossa voit testata, kouluttaa tai tehdä vianmäärityksiä häiritsemättä yrityksen työprosesseja tai liiketoimintatietoja. Tällaista ei-tuotantoympäristöä kutsutaan *eristysympäristöksi (sandbox)*. Tuotannosta eristetty Sandbox-ympäristö on paikka, jossa voi turvallisesti tutustua palveluun, opetella sen käyttöä sekä kehittää ja testata sitä ilman, että tuotantoympäristön tiedot ja asetukset vaarantuvat.  

Järjestelmänvalvoja hallitsee eristysympäristöjä [hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Jos haluat esimerkiksi luoda eristysympäristön vertailua varten, järjestelmänvalvoja voi luoda erillisen ympäristön hallintakeskuksessa. Lisätietoja on kehittäjä- ja hallintasisällön kohdassa [Tuotanto- ja eristysympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/environment-types).  

Voit myös turvallisesti käyttää eristysympäristöjä koulutukseen, kuten seuraavaan oppimispolkuun [Microsoft Learnissa](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), koska se on turvallinen ympäristö kokeilla. Jos jokin menee vikaan, voit vain poistaa eristysympäristön ja aloittaa alusta.  

Kun olet valmis, voit poistaa eristysympäristön hallintakeskuksen avulla.  

> [!NOTE]
> Teknisesti eristysympäristöt poikkeavat hyvin paljon tuotantoympäristöistä. Järjestelmänvalvoja voi luoda eristysympäristön, joka sisältää tuotantotietoja, mutta se on silti eristysympäristö, etkä voi pyytää esimerkiksi tietokannan vientiä. Lisätietoja on kehittäjä- ja hallintasisällön kohdassa [Eristysympäristöjen hallinta](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments).

Eristysympäristö on hyödyllinen muun muassa seuraavien kätevien ominaisuuksien ansiosta:

* [Käyttäjäkokemuksen parannus](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Suunnitteluohjelma](#designer)  

## <a name="advanced-user-experience"></a>Käyttäjäkokemuksen parannus

[!INCLUDE[prod_short](includes/prod_short.md)]in perusversion voi ottaa käyttöön ja sen kaikkia toimintoja voi käyttää eristysvuokraajassa määrittämällä **Kokemus**-kentän asetukseksi *Premium* **Yrityksen tiedot** -sivulla. Etsi **Yrityksen tiedot** -sivu :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Asetukset-kuvake."::: -valikosta.  

Kun olet ottanut käyttöön *Premium*-käyttökokemuksen, saat käyttöösi kaikki vakioprofiilit (roolit) ja roolikeskukset vakioversiossa. Vaihtoehtoisesti voit ottaa yhteyttä jälleenmyyntiyhteistyökumppaniin, jotta saat esittelyn ominaisuuksista. Lisätietoja on kohdassa [Miten löydän jälleenmyyjäkumppanin?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Täydelliset esimerkkitiedot

Jos tarvitset lisää esimerkkitietoja, käänny jälleenmyyjäkumppanin puoleen.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Rakennenäkymä

Sandbox-ympäristössä on **Rakennenäkymä** käytössä. Voit aktivoida Suunnitteluohjelman valitsemalla suunnittelukuvakkeen ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) sivulla tai valitsemalla **Rakenne**-valikkokohteen ![Asetukset](media/ui-experience/settings_icon_small.png) Asetukset-valikossa.  

Lisätietoja on kehittäjä- ja järjestelmänvalvojasisällön kohdassa [Suunnitteluohjelman käyttäminen ](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) (vain englanniksi).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)] -ohjelman käyttäminen](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]Kokeilut ja tilaukset](across-preview.md)  
[Ympäristöjen hallinta Business Centralin hallintakeskuksessa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Tuotanto- ja eristysympäristöt](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]