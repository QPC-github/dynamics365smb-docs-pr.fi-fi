---
title: Nimikkeiden ostaminen myyntiin
description: Voit ostaa tuotteita luomalla toimittajan ostolaskun myyntilaskusta.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'supply planning, sales demand, replenish'
ms.search.form: '50, 51, 56, 9308'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="purchase-items-for-a-sale-by-creating-purchase-invoices" />Nimikkeiden ostaminen myyntiin ostolaskuja luomalla

Voit luoda myyntitilausten ja myyntilaskujen toiminnoilla nopeasti ostoasiakirjoja myynnin edellyttämille puuttuville nimikemäärille. Voit käyttää asiakirjan tyypin mukaan kahta eri toimintoa.

> [!Note]
> Näiden toimintojen avulla täydennetään oman varaston myyntinimikkeitä. Jos haluat ostaa nimikkeitä suoratoimitusta varten toimittajalta asiakkaalle, sinun on luotava suoratoimitus. Lisätietoja on kohdassa [Suoratoimitusten tekeminen](sales-how-drop-shipment.md).   

|Toiminto|Description|
|--------|-----------|
|**Luo ostotilaukset**|Tällä toiminnolla voi luoda myyntitilauksesta ostotilauksen kullekin myyntitilauksessa olevan nimikkeen toimittajalle. Voit muokata ostomäärää ennen ostotilausten luontia. Vain myyntimääriä, jotka eivät ole käytettävissä, ehdotetaan.
|**Luo ostolasku**|Tällä toiminnolla voi luoda myyntitilauksesta ja myyntilaskusta ostolaskun myyntiasiakirjasta valitun toimittajan kaikille tai valituille riveille. Ehdotuksena on myynnin täysi määrä.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order" />Vähintään yhden ostotilauksen luominen myyntitilauksesta
Voit luoda ostotilauksen kullekin myyntitilauksen nimikkeen määrälle, joka ei ole käytettävissä **Luo ostotilauksia** -toiminnolla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Avaa myyntitilaus, johon haluat ostaa nimikkeitä.
3. Valitse **Luo ostotilaukset** -toiminto.

    Avautuvalla **Luo ostotilauksia** -sivulla näkyy rivi kullekin myyntitilauksen nimikkeelle. Oletusarvoisesti näkyvissä on kokonaan saatavana olevien myyntimäärien rivit sekä niiden myyntimäärien rivit, jotka eivät ole saatavana (näkyvät harmaana). Voit valita **Näytä ne, jotka eivät ole saatavilla** -toiminnon, jos haluat nähdä vain niiden myyntimäärien rivit, jotka eivät ole saatavilla.

    **Ostojen määrä** -kenttä sisältää oletusarvoisesti myyntimäärän, joka ei ole saatavilla.
4. Voit ostaa jonkin muun määrän kuin ei saatavilla olevan myyntimäärän muokkaamalla **Ostettava määrä** -kentän arvon.

    > [!NOTE]  
    >   Voit muuttaa myös harmaana näkyvien rivien **Ostettava määrä** -kenttää, vaikka ne ilmaisevatkin kokonaan saatavilla olevat myyntimäärät.
5. Valitse **OK**-painike.

    Kullekin myyntitilauksen nimikkeiden toimittajalle luodaan ostotilaus, mukaan lukien **Luo ostotilaukset** -sivulla mahdollisesti tehdyt määrän muutokset.
7. Siirry käsittelemään ostotilauksia esimerkiksi muokkaamalla tai lisäämällä ostotilausrivejä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice" />Ostolaskun luominen myyntitilauksesta tai myyntilaskusta
Voit luoda yhden ostolaskun yhdelle tai usealle myyntiasiakirjan riville valitsemalla ensin toimittajan, jolta nimike ostetaan, käyttämällä **Luo ostotilaus** -toimintoa.

> [!NOTE]  
>   Tällä toiminnolla luodaan ostolasku täsmälleen valitussa myyntiasiakirjassa olevalle nimikemäärälle. Voit muuttaa oston määrää muokkaamalla ostolasku sen jälkeen, kun se on luotu.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Avaa myyntilasku, johon haluat ostaa nimikkeitä.
3. Valitse yksi tai useampi myyntilaskun rivi, joita haluat käyttää ostolaskuun. Voit käyttää kaikkia myyntilaskurivejä valitsemalla kaikki rivit tai jättämällä kaikki rivit valitsematta.
4. Valitse **Luo ostolasku** -toiminto.
5. Valitse joko **Kaikki rivit** tai **Valitut rivit** ja valitse sitten **OK**-painike.  
6. Valitse avautuvasta toimittajaluettelosta toimittaja, jolta haluat ostaa kaikki nimikkeet, ja valitse sitten **OK**-painike.

    Luotavassa ostolaskussa on yksi myyntilaskun rivi, useita myyntilaskun rivejä tai kaikki myyntilaskun rivit.
7. Siirry käsittelemään ostolasku, esimerkiksi lisäämällä ostolaskurivit tai muokkaamalla niitä. Lisätietoja on kohdassa [Ostojen kirjaaminen](purchasing-how-record-purchases.md).

## <a name="see-also" />Katso myös
[Osto](purchasing-manage-purchasing.md)  
[Ostojen kirjaus](purchasing-how-record-purchases.md)  
[Myynnin laskutus](sales-how-invoice-sales.md)  
[Uusien toimittajien rekisteröiminen](purchasing-how-register-new-vendors.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
