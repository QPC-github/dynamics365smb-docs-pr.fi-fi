---
title: Kysynnän ja tarjonnan välisten suhteiden seuraaminen
description: 'Tässä aiheessa kerrotaan eri tavoista seurata kysynnän ja tarjonnan välisiä suhteita, kuten linkitettyjen nimikkeiden seurantaa ja seuraamattomien suunnitteluelementtien käsittelemistä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5830, 9101, 99000822, 99000855'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="track-relations-between-demand-and-supply" />Kysynnän ja tarjonnan välisten suhteiden seuraaminen

Voit seurata tilausverkon kysyntä- tai tarjousasiakirjojen avulla tilauskysyntää (seurattu määrä), ennustetta, myyntipuitetilausta tai suunnitteluparametria (ei-seurattu määrä), joka on kiinnittänyt huomion kyseiseen suunnitteluriviin.

Suunnittelutyökirjasta saa myös suunnittelua tukevia tietoja muista kuin tilattavista yksiköistä, mikä auttaa suunnittelijaa saamaa mahdollisimman hyvän toimitussuunnitelman. Lisätietoja on kohdassa [Ei-seuratut suunnitteluelementit.](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items" />Linkitettyjen kohteiden seuraaminen
Tilauksen seurannan avulla voi nähdä, miten myyntitilaukset, tuotantotilaukset ja ostotilaukset liittyvät tuotantotilaukseen suunnittelu- ja varausjärjestelmien kautta.

Seuraavaksi käsitellään linkitettyjen nimikkeiden seuraamista sitovasti suunnitellussa tuotantotilauksessa. Nämä vaiheet ovat samankaltaiset kaikilla muilla tilaustyypeillä ja suunnittelutyökirjan riveillä.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sitovasti suun. tuotantotil.** ja valitse sitten vastaava linkki.
2. Avaa asianmukainen sitovasti suunniteltu tuotantotilaus luettelosta.
3. Valitse **Rivit**-pikavälilehdessä ensin **Toiminnot**-toiminto ja sitten **Tilauksen seuranta** -toiminto.

Nykyiseen tuotantotilauksen riviin liittyvät asiakirjat näkyvät **Tilauksen seuranta** -ikkunan riveillä.

## <a name="untracked-planning-elements" />Ei-seuratut suunnitteluelementit
**Ei-seuratut suunnitteluelementit** -sivu avautuu, kun valitset **Ei-seurattu määrä** -kentän **Tilauksen suunnittelu** -sivulla. Sillä on kaksi tarkoitusta:

1. Se sisältää tietoja ei-seuratuista määristä, jotka näytetään, kun käyttäjä etsii ei-seurattuja määriä Tilauksen seuranta -sivun avulla.
2. Se sisältää varoitussanomia, jotka näytetään, kun käyttäjä napsauttaa **varoituskuvaketta** **Suunnittelutyökirja**-sivulla.

Sivu sisältää tapahtumia, jotka selittävät ei-seuratun ylijäämämäärän tilauksen seurantaverkossa. Tapahtumat luodaan suunnitteluajon aikana ja ne selvittävät, mistä tilauksen seurantarivien ei-seurattu ylijäämämäärä on peräisin. Ei-seurattu ylijäämä voi olla peräisin seuraavista kohteista:

- Tuotantoennuste
- Puitetilaukset
- Varmuusvaraston määrä
- Uusintatilauspiste
- Enimmäisvarasto
- Uusintatilausmäärä
- Enimmäistilausmäärä
- Vähimmäistilausmäärä
- Tilauskerrannainen
- Vaimennin (% eräkoosta).

## <a name="see-also" />Katso myös
[Suunnittelu](production-planning.md)   
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)    
[Vaihto-omaisuus](inventory-manage-inventory.md)  
[Osto](purchasing-manage-purchasing.md)  
[Rakennetiedot: Varaus, seuranta ja toimenpiteiden viestitys](design-details-reservation-order-tracking-and-action-messaging.md)  
[Rakennetiedot: Toimitusten suunnittelu](design-details-supply-planning.md)   
[Parhaiden käytäntöjen määrittäminen: Toimitusten suunnittelu](setup-best-practices-supply-planning.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
