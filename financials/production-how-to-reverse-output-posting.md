---
title: Tuotoksen kirjaamisen peruuttaminen | Microsoft Docs
description: "Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa. Tällainen tilanne voi olla esimerkiksi, jos tietojen syötössä on ilmennyt virhe ja tuotantotilaukseen kirjataan väärä tuotoksen määrä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a>Tuotoksen kirjaamisen peruuttaminen
Tuotoksen kirjaus täytyy joissakin tilanteissa peruuttaa. Tällainen tilanne voi olla esimerkiksi, jos tiedot annettiin virheellisesti ja tuotantotilaukseen kirjataan väärä tuotoksen määrä.  

## <a name="to-reverse-an-output-posting"></a>Peruuta tuotoksen kirjaus  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki. Valitse haluamasi erä.  
2. Täytä tarvittavat kentät. Lisätietoja on kohdassa [Toimintaohje: Tuotoksen ja ajoaikojen eräkirjaaminen](production-how-to-post-output-quantity.md).
3.  Valitse **Kohdistetaan tapahtumaan** -kentässä asiaan liittyvä nimiketapahtuma. Tämä peruuttaa kapasiteetti- ja nimiketapahtumat.  
4. Kirjaa peruutus kirjaamalla päiväkirja.  

Tuotospäiväkirjan tapahtumat kirjataan nimiketapahtumiin positiivisena muutoksena.  

## <a name="see-also"></a>Katso myös  
 [Tuotanto](production-manage-manufacturing.md)    
 [Tuotannon määrittäminen](production-configure-production-processes.md)  
 [Suunnittelu](production-planning.md)      
 [Vaihto-omaisuus](inventory-manage-inventory.md)  
 [Osto](purchasing-manage-purchasing.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
