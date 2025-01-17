---
title: Huoltonimikkeet ja huoltonimikkeiden komponentit
description: 'Lisätietoja määrityksistä, jotka on tehtävä ennen huoltonimikkeiden käyttöä. Esimerkiksi oletusarvot, kuten vastausaika ja huoltohintaryhmä, on määritettävä.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="set-up-service-items-and-service-item-components" />Huoltonimikkeiden ja huoltonimikkeen komponenttien määrittäminen
Huoltonimikkeiden käyttöä varten on määritettävä seuraavat asetukset

* Huoltonimikeryhmät.
* Valinnainen

## <a name="to-set-up-service-item-groups" />Huoltonimikeryhmien määrittäminen
Voit määrittää korjaus- ja ylläpitoehtoihin liittyvät nimikeryhmät. Huoltonimikeryhmässä oleville huoltonimikkeille voi määritellä oletusarvoja, kuten vastausajan, sopimusalennus-%:n ja huoltohintaryhmän. Huoltonimikeryhmässä olevien nimikkeiden osalta voi valita, halutaanko, että ne rekisteröidään automaattisesti huoltonimikkeiksi silloin, kun ne myydään.  

Huoltonimikeryhmiä määritetään **Nimike**-kortin nimikkeille ja **Huoltonimike**-kortin huoltonimikkeille.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikeryhmät** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltonimikeryhmä.  
3. Täytä **Koodi**- ja **Kuvaus**-kentät.  
4. Anna **Oletus sopimusalennus-%** -kenttään oletussopimusalennusprosentti, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
5. Anna **Oletus huoltohintaryhmän koodi** -kenttään oletushuoltohintaryhmän koodi, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
6. Anna **Oletusvastausaika (tuntia)** -kenttään oletusvastausaika tunneissa, jonka haluat ryhmässä olevilla huoltonimikkeillä olevan.  
7. Jos haluat rekisteröidä ryhmän nimikkeen huoltonimikkeiksi silloin, kun ne myydään, valitse **Luo huoltonimike** -kenttä.  

## <a name="to-set-up-service-item-components" />Huoltonimikkeen komponenttien määrittäminen
Huoltonimike voi koostua useista komponenteista, jotka voidaan korvata varaosilla nimikettä huollettaessa. Nämä komponentit määritetään **Huoltonimikk. komponenttiluet.** -sivulla. Jos lisäksi haluat määrittää komponentteja huoltonimikkeille, jotka ovat tuoterakenteita, tuoterakennenimikkeet voidaan kopioida ja luoda huoltonimikkeen komponentteina.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten vastaava linkki.
2. Avaa huoltonimike, jolle haluat määrittää komponentteja.  
3. Valitse **Komponentit**-toiminto. Näyttöön tulee **Huoltonimikk. komponenttiluet.** -sivu.  
4. Uuden ryhmän lisääminen  
5. Valitse **Tyyppi** -kentässä **Huoltonimike**, jos itse komponentti on rekisteröity huoltonimike. Muutoin valitse **Nimike**.  
6. Valitse **Nro**-kenttään nimike tai huoltonimike, joka on huoltonimikkeen komponentti.  

## <a name="to-set-up-service-item-components-from-a-bom" />Huoltonimikkeen komponenttien määrittäminen tuoterakenteista
1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltonimikkeet** ja valitse sitten vastaava linkki.  
2. Avaa huoltonimike, jolle haluat määrittää komponentteja huoltorakenteesta.  
3. Valitse **Komponentit**-toiminto. Näyttöön tulee **Huoltonimikk. komponenttiluet.** -sivu.  
4. Valitse **Kopioi tuoterakenteesta** -toiminto.  

    Jos nimike, johon huoltonimike on linkitetty, on tuoterakenne, ohjelma luo automaattisesti komponentteja kaikille tuoterakenteessa oleville nimikkeille.  

## <a name="to-set-up-a-service-shelf" />Huoltohyllyn määrittäminen
Voit määrittää huoltohyllyjä, jotka ilmaisevat, mihin huoltonimikkeet varastoidaan. Huoltohyllyt määritetään huoltonimikkeille **Huoltotilaus**- ja **Huoltonimikkeen työkirja** -sivuilla.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltohyllyt** ja valitse sitten vastaava linkki.
2. Täytä tarvittavat kentät.

## <a name="see-also" />Katso myös
[Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md)   
[Vianmäärityksen määrittäminen](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
