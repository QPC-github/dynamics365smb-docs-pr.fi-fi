---
title: "Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta | Microsoft Docs"
description: "Kun otat maksupalvelut käyttöön, asiakkaiden on helpompi maksaa laskunsa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0154f7fc231023542cc5f389ea6c8a3e99c7fffc
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a>Asiakasmaksujen ottaminen käyttöön maksupalvelujen kautta
Pankkisiirron tai luottokorttien lisäksi asiakkaat voivat maksaa sinulle maksupalvelutilin, kuten Microsoft Payn, PayPalin tai WorldPayn, avulla.  

Kun olet ottanut maksupalvelun käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa, palvelun linkki on käytössä sähköpostitse asiakkaille lähetettävissä myyntiasiakirjoissa. Asiakkaat voivat siirtyä linkin kautta maksupalveluun ja maksaa laskun suoraan myyntiasiakirjasta. Jos et halua lisätä linkkiä esimerkiksi silloin, kun asiakas maksaa käteisellä, voit poistaa maksupalvelun laskusta ennen kirjaamista.  

Microsoft Pay, PayPal Payments Standard- ja WorldPay Payments Standard -laajennukset on asennettu [!INCLUDE[d365fin](includes/d365fin_md.md)]iin, ja ne odottavat käyttöönottoa.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Maksupalvelun ottaminen käyttöön [!INCLUDE[d365fin](includes/d365fin_md.md)]issa
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Maksupalvelut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse **Maksupalvelut**-ikkunassa **Uusi**-toiminto.  
3. Valitse maksupalvelu ja sulje sitten ikkuna.  
4. Valitse **Maksupalvelut**-ikkunassa **Asetus**-toiminto.  
5. Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Sulje ikkuna.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Maksupalvelun valitseminen myyntilaskussa
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Myyntilaskut** ja valitse sitten aiheeseen liittyvä linkki.  
2. Avaa myyntilasku, jonka haluat maksaa maksupalvelun avulla.  
3. Valitse maksupalvelu **Maksupalvelu**-kentässä.  

    > [!NOTE]  
    > **Maksupalvelu**-kenttä on käytettävissä vain, jos olet ottanut maksupalvelun käyttöön.  

## <a name="see-also"></a>Katso myös  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Myynti](sales-manage-sales.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman mukauttaminen laajennusten avulla](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
