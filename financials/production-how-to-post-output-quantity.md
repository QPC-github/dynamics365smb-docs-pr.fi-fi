---
title: "Tuotannon tuotos- ja suoritusaikojen eräkirjaus| Microsoft Docs"
description: "Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa."
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
ms.openlocfilehash: ee5ee5d08804439a79f8029eaa25ab7547349a1b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-output-and-run-times"></a>Toimintaohje: Tuotos- ja suoritusaikojen eräkirjaus
Tuotosmäärä kuvaa työn edistymistä valmiin määrän muodossa.  

> [!NOTE]
> Varasto päivitetään automaattisesti vasta, kun kirjaat viimeisen toiminnon tuotosmäärän.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin tuotosmäärän kirjaaminen
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Jos toiminto on valmis, valitse **Valmis**-kenttä.  

    Jos fyysisen varaston sijainti, johon nimikkeet hyllytetään, käyttää varastopaikkoja, mutta ei vaadi hyllytystä,  määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mihin nimikkeet tulee sijoittaa fyysisessä varastossa. Lisätietoja on kohdassa [Toimintaohje: Tuotannon tai kokoonpanon tuotoksen hyllytys](warehouse-how-to-put-away-production-output.md).  

4. Kirjaa toiminnot valitsemalla **Kirjaa**-toiminto. Tuotosmäärä kirjataan. Nimike on nyt saatavilla toimitettavaksi.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin suoritusaikojen kirjaaminen
Ajoaika kuvastaa työn edistymistä tarvittavan työajan muodossa.    

1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Tuotospäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä kentät tuotantotilauksen tiedoilla ja tuotostiedoilla.  
3.  Jos toiminto on valmis, valitse **Valmis**-kenttä.  
4. Kirjaa toimintakohtainen kulutettu aika valitsemalla **Kirjaa**-toiminto. Käytettyjen tuotantosolujen tai kuormitusryhmien kapasiteettitapahtumat päivitetään.

## <a name="see-also"></a>Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
