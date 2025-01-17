---
title: Varastokausien käsitteleminen
description: 'Määrittämällä varastokauden voi hallita aikajaksoa, jolloin henkilöt voivat kirjata muutoksia varastoon.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'inventory, periods'
ms.search.form: 5828
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-inventory-periods" />Varastokausien käsitteleminen

Varastokaudet määrittävät aikajakson, jolloin voit kirjata varastoon muutoksia. Lopetuspäivämäärä määrittää, milloin varastokausi loppuu. Kun suljet varastokauden, et voi enää kirjata varastoon odotettuja tai laskutettuja muutoksia ennen tätä lopetuspäivämäärää. Et voi kirjata varastoon uusia arvoja ennen lopetuspäivämäärää. Jos suljetulla kaudella on avoimia nimiketapahtumia eli positiivisia määriä, joita ei ole vielä kohdistettu lähteviin transaktioihin, voit yhä kohdistaa lähteviä määriä näihin transaktioihin, vaikka kausi on suljettu.  

Seuraavissa luvuissa kerrotaan, miten

* varastokausia luodaan  
* varastokausia suljetaan  
* varastokausia avataan uudelleen.  

## <a name="to-create-an-inventory-period" />Varastokauden luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten vastaava linkki.  
2. Luo uusi rivi.  
3. Syötä **Lopetuspvm**-kenttään viimeinen päivämäärä, jonka haluat varastokaudelle määrittää. Kun kausi suljetaan, et voi enää kirjata ennen tätä päivämäärää tapahtuneita varaston muutoksia.  
4. Anna **Nimi**-kenttään kuvaava nimi. Valitse **OK**-painike.  

## <a name="closing-inventory-periods" />Varastokausien sulkeminen

**Suljettu**-kenttä osoittaa, onko varastokausi suljettu varaston arvon muutoksilta. Et voi muokata tätä kenttää.  

Voit sulkea minkä tahansa varastokauden, jos seuraavat kohdat toteutuvat:  

* Kaudella ei ole avoimia lähteviä nimiketapahtumia eli negatiivista varastoa.  
* Kaikkien nimikkeiden kustannus on muutettu **Muuta kustannuksia - Nimiketapahtumat** -eräajon avulla.  

Tällöin kaikki lähtevät transaktiot, kuten myyntitilausten, lähtevien siirtojen, myyntilaskujen, ostopalautusten ja ostohyvityslaskujen transaktiot, on kohdistettava varastomäärään.  

### <a name="to-close-an-inventory-period" />Sulje varastokausi

1. Valitse **Muuta kustannuksia - Nimiketapahtumat** -toiminto ennen varastokauden sulkemista. Näin voit varmistaa, että kaikkien kustannusten muutokset on kirjattu.

    Suorittamalla **Sulje varastokausi - Testaa** -raportin voit määrittää, onko varastokaudella avoimia lähteviä transaktioita tai nimikkeitä, joiden kustannuksia ei ole vielä muutettu.  
2. Valitse **Sulje varastokausi – Testaa** -toiminto.  

    Suorittamalla **Kirjaa varaston kustannus KP:oon** -eräajon voit varmistaa, että kaikki kustannukset on viety pääkirjanpitoon.  
3. Valitse **Kirjaa varasto kirjanpitoon** -toiminto.  
4. Valitse suljettava varastokausi **Varastokaudet**-sivulla.  
5. Valitse **Sulje varastokausi** -toiminto. Varastokauden sulkeuduttua et voi enää kirjata varaston muutoksia ennen lopetuspäivämäärää. Kaikkien nimikkeiden kustannus on muutettava **Muuta kustannuksia - Nimiketapahtumat** -eräajolla ennen varastokauden sulkemista.  
6. Valitse **Kyllä** voit sulkea kauden tai valitse **Ei**, jos haluat peruuttaa sulkemisen.  
7. Ohjelma sulkee varastokauden ja tuo näyttöön vahvistussanoman, kun kausi on suljettu.  

## <a name="reopening-inventory-periods" />Varastokausien avaaminen uudelleen
Kun varastokausi on suljettu kerran, et voi poistaa sitä. Voit kuitenkin avata sen uudelleen, jos haluat sallia kirjaukset ennen varastokauden lopetuspäivämäärää. Kauden avaaminen uudelleen avaa myös kaikki varastokaudet, joilla on avattua kautta myöhäisemmät lopetuspäivämäärät.  

### <a name="to-reopen-an-inventory-period" />Avaa varastokausi uudelleen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Varastokaudet** ja valitse sitten vastaava linkki.  
2. Valitse uudelleen avattava varastokausi.  
3. Valitse **Avaa kausi uudelleen** -toiminto. Vahvista, että haluat avata kauden uudelleen.  
4. Kaikki varastojaksot, joiden lopetuspäivämäärät ovat valittua myöhäisemmät, avataan uudelleen.  

## <a name="see-also" />Katso myös
[Rakennetiedot: varastokausi](design-details-inventory-periods.md)  
[Rahoitus](finance.md)  
[Varasto](inventory-manage-inventory.md)  
[Financialsin käyttäminen](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
