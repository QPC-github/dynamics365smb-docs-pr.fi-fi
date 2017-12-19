---
title: Tuotantotilauksen otsikoiden luominen | Microsoft Docs
description: "Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a>Tuotantotilausten otsikoiden luominen
Tuotantotilauksen voi luoda manuaalisesti. Ensimmäinen työvaihe on tuotantotilauksen otsikon luominen.

Suunnittelutoiminto luo tuotantotilaukset tavallisesti automaattisesti toteuttamaan tunnetun kysynnän. Lisätietoja on kohdassa [Suunnittelu](production-planning.md).   

Seuraavassa toienpiteessä luodaan sitovasti suunniteltu tuotantotilaus. Voit luoda myös tuotantotilauksia, joilla on eri tila.  

## <a name="to-create-a-production-order-header"></a>Tuotantotilausten otsikoiden luominen  
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Sitovasti suunn. tuotantotil.** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Uusi**-toiminto.  
3.  Valitse **Nro**-kenttään seuraava numero sarjasta.  
4.  Valitse **Lähdetyyppi**-kentässä tuotantotilauksen lähde.

    Voit valita täällä tuotenimikeperheen tuotannon. Lisätietoja on kohdassa [Toimintaohje: Tuotantoperheiden käyttäminen](production-how-work-family.md).
5.  Valitse **Lähteen nro** -kentässä nimikenumero, tuoteperhe tai myynnin tunnistetiedot, jolle tuotantotilaus luodaan.  
6.  Täytä **Määrä**- ja **Eräpäivä**-kentät määritystesi mukaisesti.  

Kun tuotannon vaatimukset, kuten komponentit tai toiminnot, muuttuvat, voit suunnitella tuotantotilauksen nopeasti uudelleen. Lisätietoja on kohdassa [Toimintaohje: Tuotantotilausten suora päivittäminen tai uudelleensuunnitteleminen](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Katso myös  
[Tuotanto](production-manage-manufacturing.md)    
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Suunnittelu](production-planning.md)      
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
