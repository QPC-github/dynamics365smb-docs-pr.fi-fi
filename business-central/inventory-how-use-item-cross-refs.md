---
title: Nimikkeiden viittausten käyttäminen | Microsoft Docs
description: Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro** -kentässä.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ca9f31b737fbd81bd1abba2a942301d0c9c919a6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244043"
---
# <a name="use-item-cross-references"></a>Nimikkeen viittausten käyttäminen
Jos määrität viittauksen käyttämäsi nimikkeen nimikekuvauksen ja kyseisen nimikkeen toimittajan käyttämän kuvauksen välille, toimittajan nimikekuvaus lisätään automaattiesti toimittajan ostoasiakirjoihin, kun annat arvon **Viitenro** -kentässä. Myyntiasiakirjojen asiakkaan nimikenumeroissa käytetään samoja toimintoja.

Seuraavaksi käsitellään nimikkeen viittausten käyttämistä ostojen puolella. Ostojen puolen vaiheet ovat vastaavanlaiset.

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a>Nimikkeen viittauksen määrittäminen toimittajan nimikkeen kuvaukseen.
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, anna **Nimikkeet** ja valitse sitten liittyvä linkki.
2. Avaa sen nimikkeen kortti, jolle haluat luoda viittauksen toimittajan kyseistä nimikettä koskevaan nimikkeen kuvaukseen.
3. Valitse **Ristiviittaukset**-toiminto.
4. Täytä **Nimikkeen viittaustapahtumat** -sivun uudella rivillä kenttiä tarpeen mukaan. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>Toimittajan nimikkeen kuvauksen antaminen ostotilauksessa
1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostotilaukset** ja valitse sitten liittyvä linkki.
2. Luo ostotilaus toimittajalle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
3. Luo ostorivi nimikkeelle, jolle määritit nimikkeen viittauksen edellisessä menettelyssä.
4. Valitse **Viittauksen tyypin nro** -kentässä nimikkeen viittaus, jonka loit, ja valitse sitten **OK**-painike.

Rivin **Kuvaus**-kentän tiedot on korvattu toimittajan nimikkeen kuvauksella nimikkeen viittaustapauksessa määritetyllä tavalla.

## <a name="see-also"></a>Katso myös
[Uusien nimikkeiden rekisteröiminen](inventory-how-register-new-items.md)  
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)