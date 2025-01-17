---
title: FEFO-poiminnan ottaminen käyttöön | Microsoft Docs
description: 'FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="enable-picking-items-by-fefo" />FEFO-poiminnan ottaminen käyttöön
FEFO (First Expired First Out) on lajittelumenetelmä, joka varmistaa sen, että vanhimmat ja aikaisimman vanhenemispäivämäärän omaavat nimikkeet poimitaan ensin.  

 Tämä toiminto toimii vain, kun seuraavat ehdot täyttyvät:  

-   Nimikkeellä on oltava sarjanumero tai eränumero.  
-   Nimikkeen seurantakoodiasetuksissa on valittava kenttä **Sarjanumerovarastoseuranta** -kenttä tai **Eränumerovarastoseuranta**.  
-   Nimike on kirjattu varastoon vanhentumispäivämäärän kera.  
-   **Vaadi poiminta**-, **FEFO-poiminta**- ja **Var.paikka pakollinen** -valitsimien on oltava otettuna käyttöön sijainnissa.  

 Kun kaikki ehdot täyttyvät, poimittavat sarja/erä-numeroidut nimikkeet lajitellaan vanhimmat ensin kaikissa poiminnoissa ja siirroissa, lukuun ottamatta nimikkeitä, jotka käyttävät sarjanrokohtaista tai eränumerokohtaista seurantaa.  

> [!NOTE]  
> Jos jotkin sarja- tai eränumeroidut nimikkeet käyttävät erityistä seurantaa, ne otetaan ensin huomioon. Näiden jälkeen jäljellä olevat määrittämättömät sarja-/eränumerot luetellaan FEFO:n mukaan.
<br /><br />
Jos kahdella erä- tai sarjanumeroidulla nimikkeellä on sama vanhentumispäivämäärä, sovellus valitsee nimikkeen, jolla on pienempi sarja- tai eränumero.
<br /><br />
Kun sarja- tai eränumeroituja nimikkeitä poimitaan ohjattua hyllytystä ja poimintaa varten määritetyissä sijainneissa, FEFO poimii vain tyyppiä *Poiminta* olevien varastopaikkojen määrät.  
<br /><br />
Ota varastosiirrot käyttöön FEFO:n mukaan jättämällä **Varastopaikasta**-kenttä tyhjäksi **Varaston siirto**- tai **Siirtotyökirja**-sivulla.  
<br /><br />
Jos **Tiukka vanhentumisen kirj.** -kenttä on valittu **Nimikk. seurantakoodin kortti** -kohdassa, poimintaan sisällytetään vain nimikkeet, jotka eivät ole vanhentuneet, ja rivit lajitellaan FEFO-periaatteen mukaisesti.

## <a name="see-also" />Katso myös
[Nimikkeiden poiminta fyysisen varastoinnin toimitusta varten](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Nimikkeiden poiminta varastopoiminnalla](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
