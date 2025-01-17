---
title: Fyysisten varastojen uudelleenjärjestely
description: 'Opi uudistamaan fyysisen varastoinnin rakennetta uusilla varastopaikkakoodeilla ja uusilla varastopaikan ominaisuuksilla, jotta voit saavuttaa tai ylläpitää tehokkaampaa toimintaa.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9813, 9814'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="restructure-warehouses" />Fyysisten varastojen uudelleenjärjestely
Haluat ehkä järjestellä fyysisen varaston uudelleen käyttämällä uusia varastopaikan koodeja ja uusia varastopaikan ominaispiirteitä. Tällaista toimintoa ei suoriteta kovin usein, mutta eteen voi tulla tilanteita, jolloin uudelleenluokittelu on tarpeen, jotta saavutettaisiin tai ylläpidettäisiin tehokkaampaa toimintaa. Esimerkiksi:  

- Haluat alkaa käyttää varastopaikkakoodeja, jotka tukevat automaattisen tiedonkeruun käyttöä esimerkiksi kannettavien laitteiden kanssa.  
- Fyysiseen varastoon on voitu ostaa uusi hyllyjärjestelmä, joka antaa uusia mahdollisuuksia nimikkeiden varastointiin.  
- Yritys on voinut muuttaa nimikevalikoimaa ja on siirtänyt fyysisen varaston uuteen paikkaan muutoksen mukaisesti.  

Jos fyysinen varasto käyttää varastopaikkoja, mutta ei ohjattua hyllytystä ja poimintaa, määritä fyysisen varaston rakenne uudelleen luomalla uudet varastopaikat, joita haluat käyttää tulevaisuudessa.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only" />Järjestele uudelleen perusvarastointi, joka käyttää vain varastopaikkoja
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Määritä sijaintikortissa **Varastointi**-pikavälilehden **Oletus var.paikan valinta** -kentän arvoksi **Viim. käyt. var.paikka**.  
3.  Siirrä nykyisten varastopaikkojen koko sisältö juuri luomiisi uusiin varastopaikkoihin:  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeen uudelleenluokituspäiväkirja** ja valitse sitten vastaava linkki.  
    2.  Valitse ensin päiväkirjarivi ja sitten **Hae var.paikan sisältö** -toiminto.  
    3.  Määritä **Varastopaikan sisältö**-pikavälilehden **Sijaintikoodi**-, **Varastopaikkakoodi**- ja **Nimikenro**-kentissä sisältö, jonka haluat siirtää.  
    4.  Valitse **OK** täyttääksesi päiväkirjarivin.  
    5.  Valitse kunkin rivin **Uusi varastopaikkakoodi** -kentässä varastopaikka, johon nimikkeet tulisi siirtää.  
    6.  Toista vaiheet b-e kaikille varastopaikan sisällöille, jotka haluat siirtää.  
    7.  Valitse **Kirjaa**-toiminto.  

Olet nyt tyhjentänyt varastopaikat, joissa nimikkeet olivat. Nimikkeiden oletusvarastopaikoiksi on nyt muutettu päiväkirjan riveillä määritetyt uudet varastopaikat.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick" />Järjestele uudelleen laajennettu varastointi, jossa on käytössä ohjattu hyllytys ja poiminta

1.  Luo uudet varastopaikat, joita haluat käyttää jatkossa. Lisätietoja on kohdassa [Varastopaikkojen luominen](warehouse-how-to-create-individual-bins.md).  
2.  Siirrä nykyisten varastopaikkojen koko sisältö juuri luomiisi uusiin varastopaikkoihin:  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **F.var. uud.luokpäiväkirja** ja valitse sitten vastaava linkki.  
    2.  Niiden varastopaikkojen osalta, joita ei koske mikään todellinen nimikkeiden siirto, luo rivi kullekin nykyiselle varastopaikalle  **F. var. uudelleenluokituspvk** -päiväkirjaan käyttäen vanhaa varastopaikkakoodia (**Var.paikasta)** ja uutta varastopaikkakoodia ( **Varastopaikkakoodiin**).  
    3.  Jos joihinkin siirtoihin kuuluu todellisia fyysisiä siirtoja, jotka haluat työntekijöiden suorittavan, käytä  **Var.siirtotyökirjoja** valmistellaksi siirto-ohjeita sen sijaan, että käyttäisit f- varaston uudelleenluokittelupäiväkirjaa. Lisätietoja on kohdassa [Nimikkeiden siirtäminen laajennetussa varastointimäärityksissä](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Kun vanhat varastopaikat on tyhjennetty, luokittele ne uudelleen **QC** -tyypin varastopaikoiksi varmistaaksesi, että ne eivät kuulu nimikevirtoihin.  

    1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
    2.  Valitse ensin sijainnin rivi ja sitten **Varastopaikat**-toiminto.  
    3.  Anna **Varastopaikat**-sivun **Varastopaikkatyypin koodi** -kentässä koodi **QC** jokaiselle vanhalle varastopaikalle, jonka tyhjensit edellisen toimenpiteen vaiheessa 3.  

Olet nyt poistanut fyysisen varastoinnin virrasta varastopaikat ja luokitellut ne uudestaan QC-varastopaikoiksi. QC-varastopaikoissa ei ole aktiviteetti-kenttiä **Varastopaikkatyypit**-sivulla valittuna ja näin ollen niitä ei huomioida nimikevirrassa. Lisätietoja on kohdassa [Varastopaikkojen määrittäminen](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin" />Varastopaikan poistaminen

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Valitse sijainti, jossa haluat poistaa varastopaikkoja. Valitse **Varastopaikat**-toiminto.  
3.  Valitse poistettavien varastopaikkojen rivit.  
4.  Valitse **Poista**-toiminto.  

Jos napsautat **Kyllä**-painiketta, varastopaikka poistetaan käytöstä tulevaisuudessa, mutta varastopaikan koodi säilyy samana kaikissa fyysisen varastoinnin tapahtumissa.  

Jos haluat nimetä varastopaikan uudelleen, niin että myös kaikki varastopaikkaan tietueet nimetään uudelleen (tietueisiin kuuluvat varastopaikan sisältö, fyysisen varastoinnin toimintorivit, rekisteröidyt fyysisen varastoinnin toimintorivit, fyysisen varastoinnin työkirjarivit, fyysisen varastoinnin vastaanottorivit, kirjatut fyysisen varastoinnin vastaanottorivit, fyysisen varastoinnin toimitusrivit, kirjatut fyysisen varastoinnin toimitusrivit ja fyysisen varastoinnin tapahtumat), voit tehdä sen **Varastopaikat**-sivulla.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records" />Varastopaikan nimeäminen uudelleen ja varastopaikkakoodin muuttaminen kaikkiin tietueisiin

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Sijainnit** ja valitse sitten vastaava linkki.  
2.  Valitse sijainti, jonka varastopaikan haluat nimetä uudelleen tai jossa haluat muuttaa varastopaikkakoodia, ja valitse sitten **Varastopaikat**-toiminto.  
3.  Valitse se varastopaikka, jota haluat muuttaa. Syötä uusi varastopaikan koodi **Koodi**-kentässä.  
4.  Valitse **Kyllä**-painike.  

> [!NOTE]  
>  Jos napsautat **Kyllä** ja tätä varastopaikkaa koskevia tapahtumia on paljon (jos et ole esimerkiksi poistanut fyysisen varastoinnin asiakirjoja vähään aikaan), ohjelmalta voi kestää jonkin aikaa tietueiden uudelleennimeämisessä. Joten jos käytät tätä tapaa, harkitse **Poista rekisteröidyt f. var. asiakirjat** -eräajon ajamista ennen uudelleennimeämisprosessin aloittamista. Huomaa myös, että ainoat asiakirjat, joita tämä eräajo poistaa, ovat hyllytyksiä, poimintoja ja varastosiirtoja.  
>   
>  Jos olet nimeämässä uudelleen vastaanottavaa varastopaikkaa tai toimituksen varastopaikkaa, ohjelman täytyy nimetä uudelleen kaikki kirjatut vastaanotot tai toimitukset, jotka viittaavat kyseessä olevaan varastopaikkaan.  

## <a name="see-also" />Katso myös
[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)     
[Kokoonpanon hallinta](assembly-assemble-items.md)    
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
