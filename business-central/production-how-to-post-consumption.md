---
title: "Kulutuksen eräkirjaus | Microsoft Docs"
description: "Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4058d16ee3bdfc10933e1f3a01c84fbc5d0b0ebb
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-production-consumption"></a>Tuotannon kulutuksen eräkirjaus
Jos materiaalinottotapa on **Manuaalinen**, komponentit tulee kirjata manuaalisesti kulutuspäiväkirjaa käyttämällä.

Voit määrittää järjestelmän myös kirjaamaan (*materiaalioton*) komponentit automaattisesti, kun aloitat tai päätät tuotantotilauksia. Lisätietoja on kohdassa [Komponenttien materiaalinoton ottaminen käyttöön toiminnan tuotoksen mukaan](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Vähintään yhden tuotantotilausrivin kulutuksen kirjaaminen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kulutuspäiväkirja** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Täytä kentät tuotantotilauksen tiedoilla ja kulutustiedoilla. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Jos komponentteja säilyttävä fyysisen varaston sijainti on määritetty käyttämään varastopaikkoja, mutta ei vaadi poimintaa, määritä päiväkirjan riville varastopaikkakoodi osoittamaan, mistä nimikkeet otetaan fyysisen varaston sisällä. Lisätietoja on kohdassa [Tuotannon tai kokoonpanon poiminta](warehouse-how-to-pick-for-production.md).  
3.  Kirjaa kulutus valitsemalla **Kirjaa**-toiminto. Liittyviä nimiketapahtumia vähennetään.

## <a name="see-also"></a>Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
