---
title: Tuotantokalentereiden määrittäminen
description: 'Tuotantosolun luominen ja ottaminen käyttöön sisältää useita tehtäviä, kuten tuotantokalenterien määrittämisen ja työvuorojen luomisen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9291, 9293, 9295, 99000750, 99000751, 99000752, 99000753, 99000759, 99000769, 99000770, 99000771, 99000772, 99000920'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="set-up-shop-calendars" />Tuotantokalentereiden määrittäminen

Tuotantosolun tai kuormituskeskuksen kalenterissa määritetään työpäivät ja -tunnit, työvuorot, lomapäivät sekä poissaolot, jotka määräävät tuotantosolun tai kuormituskeskuksen käytettävissä olevan kokonaiskapasiteetin (ajassa mitattuna) tehokkuus- ja kapasiteettiarvojen mukaisesti.

Tuotantosolun tai kuormituskeskuksen kalenterin laskemisen perustaksi on ensin määritettävä ainakin yksi yleinen tuotantokalenteri. Tuotantokalenteriin määritetään vakiotyöviikon kunkin työpäivän alkamis- ja päättymisajat sekä työvuorot. Lisäksi tuotantokalenteriin määritetään kaikki vuoden kiinteät lomapäivät.  

Seuraavaksi käsitellään tuotantosolun kalenterien määrittämistä. Kuormitusryhmän kalenterit määritetään vastaavasti.  

## <a name="to-create-work-shifts" />Työvuorojen luominen
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Työvuorot** ja valitse sitten vastaava linkki.  
2.  Anna tyhjälle riville **Koodi**-kenttään numero työvuoron tunnisteeksi (esimerkiksi **1**).  
3.  Kirjoita työvuoron kuvaus **Kuvaus**-kenttään, esimerkiksi **1. vuoro**.  
4.  Voit täyttää myös toisen tai kolmannen työvuoron rivit.  

Vaikka tuotantosolussa ei työskenneltäisi eri vuoroissa, syötä ainakin yksi työvuoron koodin.  

## <a name="to-set-up-a-shop-calendar" />Tuotantokalenterin määrittäminen
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantokalenterit** ja valitse sitten vastaava linkki.  
2.  Anna tyhjälle riville **Koodi**-kenttään numero tuotantokalenterin tunnisteeksi (esimerkiksi 1).  
3.  Kirjoita tuotantokalenterin kuvaus **Kuvaus**-kenttään.  
4.  Valitse **Työpäivät**-toiminto.
5.  Määritä **Tuotantokalenterin työpäivät** -sivulla koko työviikko sekä kunkin päivän alkamis- ja päättymisaika.  

    Valitse **Työvuoron koodi** -kentässä jokin työvuoro, jonka olet määrittänyt aiemmin. Lisää rivi jokaiselle työpäivälle ja jokaiselle vuorolle. Esimerkki:  

    Maanantai 07:00 15:00 1   
    Tiistai 07:00 15:00 1  

    Jos tarvitaan tuotantokalenteri, jossa on kaksi työvuoroa, annetaan tiedot seuraavan esimerkin mukaisesti:  

    Maanantai 07:00 15:00 1   
    Maanantai 15:00 23:00 2  
    Tiistai 07:00 15:00 1  
    Tiistai 15:00 23:00 2  

    Viikonpäivät, joita ei määritetä tuotantokalenteriin (esimerkiksi lauantai ja sunnuntai) tulkitaan ei-työpäiviksi, ja niiden käytettävissä oleva kapasiteetti on tuotantosolun kalenterissa nolla.  

    Kun viikon kaikki työpäivät on määritetty, voit sulkea **Tuotantokalenterin työpäivät** -sivun ja antaa sitten lomapäivät.  

6.  Valitse **Tuotantokalenterit**-sivulla ensin tuotantokalenteri ja sitten **Lomapäivät**-toiminto.
7. Määritä **Tuotantokalenterin lomapäivät** -sivulla vuoden kaikki lomapäivät antamalla kunkin loman alkamispäivämäärä ja -aika sekä päättymispäivämäärä ja -aika omille riveilleen. Esimerkki:  

    04.07.04 0:00:00 23:59:00 Kesäloma  
    05.07.14 0:00:00 23:59:00 Kesäloma  
    06.07.14 0:00:00 23:59:00 Kesäloma  

Määritettyinä lomapäivinä tuotantosolun kalenterin käytettävissä oleva kapasiteetti on nolla.  

Tuotantokalenteri voidaan nyt liittää tuotantosoluun, ja tuotantosolun kalenteri voidaan laskea. Tuotantosolun kalenteri ohjaa kaikkien toimintojen aikataulutusta kyseisessä tuotantosolussa.  

## <a name="to-calculate-a-work-center-calendar" />Tuotantosolun kalenterin laskeminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tuotantosolut** ja valitse sitten vastaava linkki.
2. Avaa tuotantosolu, jonka haluat päivittää.  
3. Valitse **Tuotantokalenterin koodi** -kentässä, mitä tuotantokalenteria käytetään tuotantosolun kalenterin pohjana.  
4. Valitse **Kalenteri**-toiminto.  
5. Valitse **Tuotantosolun kalenteri** -sivulla **Näytä matriisi** -toiminto.  

    Matriisisivun vasemmassa reunassa on kaikkien määritettyjen tuotantosolujen luettelo. Oikeassa reunassa on kalenteri, jossa näkyvät käytettävissä olevat kapasiteettiarvot työpäivittäin määritettynä mittayksikkönä, esimerkiksi **480** (minuuttia). Kukin rivi edustaa yhden tuotantosolun kalenteria.  

    > [!NOTE]  
    >  Voit tarkastella myös viikko- tai kuukausikohtaisia kapasiteettiarvoja muuttamalla valintaa **Tuotantosolun kalenteri** -sivun **Näyttöperuste**-kentässä.  

    Ilmaistaksesi, että uusi tuotantokalenterin rivi on valitussa tuotantosolussa, se on ensin laskettava.  

6.  Valitse **Laske**-toiminto.  
7.  **Tuotantosolu**-pikavälilehdessä voidaan asettaa suodatin niin, että järjestelmä laskee vain yhden tuotantosolun kalenterin. Jos laskentaa ei suodateta, järjestelmä laskee kaikki tuotantosolujen kalenterit.  
8.  Määritä laskettavan kalenterijakson alkamis- ja päättymispäivämäärät, esimerkiksi yksi vuosi 1.1.2014-31.12.2014.
9. Laske kapasiteetti valitsemalla **OK**-painike.  

Järjestelmä luo (tai päivittää) kalenteritapahtumat, joista näkyy käytettävissä oleva päivittäinen (tai muun jakson mukainen) kapasiteetti seuraavan kolmen perustietojoukon mukaan:  

- Tuotantokalenterissa määritetyt työpäivät ja -vuorot  
- tuotantosolukortin **Kapasiteetti**-kentän arvo  
- tuotantosolukortin **Tehokkuus**-kentän arvo.  

Laskettu tuotantosolun kalenteri määrittelee nyt, milloin ja kuinka paljon kapasiteettia on saatavilla tässä tuotantosolussa. Tämä ohjaa tuotantosolussa suoritettavaa toimintojen yksityiskohtaista aikataulutusta.  

## <a name="to-record-work-center-absence" />Tuotantosolun poissaolojen tallentaminen
1.  Valitse **Tuotantosolun kalenteri** -sivulla **Näytä matriisi** -toiminto.
2. Valitse **Tuotantosolun kalenterimatriisi** -sivulla tuotantosolu ja kalenteripäivä, jolle poissaolo halutaan merkitä, ja valitse sitten **Poissaolo**-toiminto.  
3.  Määritä **Poissaolo**-sivulla poissaolon alkamis- ja päättymisaika kyseisenä päivänä sekä poissaolon kuvaus esimerkiksi seuraavalla tavalla: Esimerkki:  

    25.01.01 08:00 10:00 Huolto  

4.  Valitse ensin **Päivitä**-toiminto ja sulje sitten **Poissaolo**-sivu.  

Valitun päivän kapasiteetti on nyt pienentynyt kalenteriin merkityn poissaoloajan verran.  

## <a name="see-also" />Katso myös
[Peruskalenterien määrittäminen](across-how-to-assign-base-calendars.md)  
[Tuotantosolujen ja kuormituskeskusten määrittäminen](production-how-to-set-up-work-and-machine-centers.md)  
[Tuotannon määrittäminen](production-configure-production-processes.md)  
[Tuotanto](production-manage-manufacturing.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
