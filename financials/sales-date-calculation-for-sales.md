---
title: "Myynnin päivämäärälaskenta | Microsoft Docs"
description: "Ohjelma laskee automaattisesti päivämäärän, jolloin nimike on tilattava sen saamiseksi tietyn päivän varastoon. Tämä on päivämäärä, jolloin voi odottaa tiettynä päivänä tilattujen nimikkeiden olevan valmiita poimittaviksi."
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
ms.openlocfilehash: 4e8bc9e8b99db8afda83edb4aff13f5daf9f5a31
ms.contentlocale: fi-fi
ms.lasthandoff: 09/22/2017

---
# <a name="date-calculation-for-sales"></a>Myynnin päivämäärälaskenta
[!INCLUDE[d365fin](includes/d365fin_md.md)] laskee automaattisesti varhaisimman mahdollisen päivämäärän, jolloin myyntitilausrivin nimike voidaan toimittaa.

Jos asiakas on pyytänyt tietyn toimituspäivämäärän, ohjelma laskee päivämäärän, jolloin nimikkeiden tulee olla poimittavissa, jotta toimitus onnistuu sinä päivänä.

Jos asiakas ei pyydä tiettyä toimituspäivämäärää, ohjelma laskee päivämäärän, jolloin nimikkeet voidaan toimittaa alkaen siitä päivästä, jolloin nimikkeet ovat poimittavissa.

## <a name="calculating-a-requested-delivery-date"></a>Laskeminen ilman pyydettyä toimituspäivämäärää
Jos myyntitilausrivillä on pyydetty toimitusottopäivämäärä, ohjelma käyttää tätä päivämäärää lähtökohtana seuraaville laskennoille:

- Pyydetty toimituspvm - Toimitusaika = Suunniteltu lähetyspvm
- Suunniteltu toimituspvm - Lähtevä f.var. käsittelyaika = Toimituspäivä

Jos nimikkeet ovat poimittavissa lähetyspäivämääränä, myyntiprosessi voi jatkua.

Jos nimikkeet eivät ole poimittavissa lähetyspäivämääränä, näyttöön tulee varastoloppu-varoitus.

## <a name="calculating-the-earliest-possible-delivery-date"></a>Varhaisimman mahdollisen toimituspäivämäärän laskeminen
Jos myyntitilausrivillä ei ole pyydettyä toimituspäivämäärää, tai jos toimitus ei onnistu pyydettynä toimituspäivämääränä, ohjelma etsii varhaisimman päivämäärän, jolloin nimikkeet ovat saatavilla. Sen jälkeen ohjelma syöttää tämän päivämäärän rivin Toimituspvm -kenttään ja laskee päivämäärän, jolloin nimikkeet suunnitellaan lähetettävän, ja päivämäärän, jolloin ne toimitetaan asiakkaalle, seuraavien laskukaavojen mukaan:

- Suunniteltu toimituspvm = lähtevä f.var. käsittelyaika + toimituspäivä
- Suunniteltu toimituspvm + toimitusaika = suunniteltu toimituspvm


## <a name="see-also"></a>Katso myös  
 [Ostojen päivämäärälaskenta](purchasing-date-calculation-for-purchases.md)   
 [Toimintaohje: Toimituksen lupaamisen päivämäärän laskeminen](sales-how-to-calculate-order-promising-dates.md)  
 [[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)
