---
title: Maksujen täsmäyttäminen eron tilille siirron toiminnolla
description: 'Tässä ohjeaiheessa kerrotaan, miten käsitellään maksut, joita ei voi kohdistaa asiakirjaan esimerkiksi silloin, kun summat eivät ole samat vaihtokurssin vuoksi.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically" />Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti
Joskus pankkitilillä käsitellään maksuja, joita ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan. Syy voi olla se, että [!INCLUDE[prod_short](includes/prod_short.md)]issa ei ole asiakirjaa, johon maksu voitaisiin kohdistaa, tai [!INCLUDE[prod_short](includes/prod_short.md)]in liittyvä asiakirja sisältää eri summan kuin tapahtuman summa esimerkiksi valuuttamuutoksen vuoksi. Kaikki niiden maksujen tapahtumien summat, joita ei ole vielä kohdistettu, näkyvät **Maksujen täsmäytyskirjauskansio** -sivun **Ero**-kentässä. Siellä näkyvät esimerkiksi summat, joita ei voi kohdistaa edellä mainittujen syiden vuoksi.

Näiden kohdistamattomien maksujen ratkaisutavat:
* Kohdista manuaalisesti
* Käytä tekstistä tiliin yhdistämistä
* Voit siirtää ylimääräisen summan päiväkirjan riville luodaksesi ja kirjataksesi vaaditun tapahtuman, kuten liikasuorituksen hyvityksen.

Maksut, joita ei voi kohdistaa, voivat näkyä maksujen täsmäytyskirjauskansion riveillä seuraavilla tavoilla:

* **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että mitään maksun osaa ei voi kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan.
* **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvo. Tämä tarkoittaa sitä, että osa maksusta voidaan kohdistaa liittyvään avoimeen asiakas-, toimittaja- tai pankkitapahtumaan. Maksun jäljellä olevaa osaa ei voi kohdistaa. Se on täsmäytettävä manuaalisesti tai kirjaamalla se suoraan tilille.

Voit täsmäyttää tällaiset maksut valitsemalla **Siirrä erotus tilille** -toiminnon ja määrittämällä, mille tilille **Ero**-kentän summa kirjataan, kun teet kirjauksen maksujen täsmäytyskirjauskansioon. Voit tehdä tämän joko **Maksujen täsmäytyskirjauskansio** -sivulta tai avaamaltasi **Maksun kohdistuksen tarkistus** -sivulta valitsemalla arvon **Vastaavuuden luotettavuus** -kentässä tai valitsemalla **Ero**-kentän.

> [!TIP]  
>   Vastaavan toiminnon avulla voit määrittää automaattisen täsmäytyksen toistuville maksuille, joita ei voi kohdistaa liittyviin avoimiin asiakas-, toimittaja- tai pankkitapahtumiin. Lisätietoja on kohdassa [Toistuvien maksujen tekstin yhdistäminen tileihin automaattisen täsmäytyksen suorittamiseksi](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically" />Niiden maksujen täsmäyttäminen, joita ei voi kohdistaa automaattisesti
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Maksujen täsmäytyskirjauskansiot** ja valitse sitten liittyvä linkki.
2. Avaa maksun täsmäytyksen päiväkirja. Lisätietoja on kohdassa [Maksujen täsmäyttäminen käyttämällä automaattista kohdistusta](receivables-how-reconcile-payments-auto-application.md).
3. Valitse **Siirrä erotus tilille**. **Siirrä erotus tilille** -sivu avautuu.
4. Määritä **Tilityyppi**-kenttään sen tilin tyyppi, johon maksun summa kirjataan.
5. Määritä **Tilityyppi**-kenttään tili, johon maksun summa kirjataan.
6. Määritä **Kuvaus**-kenttään teksti, joka kuvaa tätä suoran maksun kirjausta. Oletusarvoisesti lisätään maksujen täsmäytyskirjauskansion rivin **Tapahtuman teksti** -kentän teksti.
7. Valitse **OK**-painike.

Jos **Ero**-kentän arvo on sama kuin **Tapahtuman summa** -kentän arvo, kun kirjaat maksujen täsmäytyskirjauskansion, koko päiväkirjan rivin maksu kirjataan suoraan määritetylle vastatilille.

Jos **Ero**-kentän arvo on pienempi kuin **Tapahtuman summa** -kentän arvon, samalla tekstillä ja päivämäärällä luodaan päiväkirjan lisärivi ja ero lisätään **Tapahtuman summa** -kenttään. Alkuperäisen päiväkirjan rivin ero vähennetään **Tapahtuman summa** -kentän arvosta ja maksun kohdistus siihen liittyvään asiakas-, toimittaja- tai pankkitilitapahtumaan säilyy. Kun kirjaat maksun täsmäytyskirjauskansion, yksi maksun osa kirjataan kohdistettuna maksuna. Maksun toinen osa kirjataan suoraan määritetylle tilille.

## <a name="see-also" />Katso myös
[Myyntisaamisten hallinta](receivables-manage-receivables.md)  
[Myynti](sales-manage-sales.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
