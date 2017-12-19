---
title: SEPA-suoraveloitusmaksujen kirjaaminen | Microsoft Docs
description: "Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit mukana oleville myyntilaskuille."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 021c48efc6bf6b1fdb7b17bf742cb6f084d3964b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-post-sepa-direct-debit-payment-receipts"></a>Toimintaohje: Kuinka SEPA-suoraveloitusmaksut kirjataan
Kun pankki on käsitellyt onnistuneesti suoraveloitusperinnän, voit siirtyä kirjaamaan maksukuitit kyseiselle myyntilaskuille. Lisätietoja on kohdassa [Toimintaohjeet: Kuinka SEPA-suoraveloitusperintämerkinnät luodaan ja viedään pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  

Voit kirjata suoraan maksun suoraan **Suoraveloitusperinnät**-ikkunasta tai **Suoraveloitusperintätapahtumat**-ikkunasta. Vaihtoehtoisesti voit siirtää työn toiselle käyttäjälle valmistelemalla siihen liittyvät päiväkirjarivit.  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a>Suoraveloitusmaksukuitin kirjaaminen suoraveloitusperinnän ikkunasta  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Suoraveloitusperinnät** ja valitse sitten aiheeseen liittyvä linkki.  
2. Valitse rivi suoraveloitusperinnälle, joka on viety pankkitiedostoon ja jonka pankki on käsitellyt onnistuneesti. Lisätietoja on kohdassa [Toimintaohjeet: Kuinka SEPA-suoraveloitusperintämerkinnät luodaan ja viedään pankkitiedostoon](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).  
3. Valitse **Kirjaa maksukuitit** -toiminto.  
4. Täytä **Kirjaa suoraveloitusperintä** -ikkunan kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Suoraveloitusperinnän nro**|Määritä suoraveloitusperintä, johon haluat kirjata maksukuitin.|  
    |**Yleisen päiväkirjan malli**|Määritä, mitä yleisen päiväkirjan mallia käytit maksukuitin kirjaamiseen, kuten kassakuittien malli.|  
    |**Yleisen päiväkirjan erän nimi**|Määritä, mitä yleistä päiväkirjaerää käytit maksukuitin kirjaamiseen.|  
    |**Luo vain päiväkirja**|Merkitse tämä valintaruutu, jos et halua kirjata maksukuittia, kun valitset **OK**-painikkeen. Maksukuitti valmistellaan määritetyssä päiväkirjassa eikä sitä kirjata ennen kuin joku kirjaa kyseisen päiväkirjarivin.|  

5. Valitse **OK**-painike.  

## <a name="see-also"></a>Katso myös  
 [Maksujen kerääminen SEPA-suoraveloituksena](finance-collect-payments-with-sepa-direct-debit.md)   
 [Myynti](sales-manage-sales.md)
