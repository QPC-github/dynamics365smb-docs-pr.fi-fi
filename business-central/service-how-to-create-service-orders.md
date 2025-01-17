---
title: Huoltotilausten luominen
description: 'Lue lisää huoltotilausten luomiseen Business Centralissa liittyvistä eri tehtävistä, kuten uuden huoltotilauksen tai huoltosopimukseen perustuvien tilausten luomisesta.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="create-service-orders" />Huoltotilausten luominen
**Huoltotilaus**-sivulla voidaan luoda asiakirjoja, joihin syötetään tietoja asiakkaan pyynnöstä tehtävästä huoltonimikkeiden huollosta (korjauksesta tai ylläpidosta).  

Kun luot huoltotilauksen, sinun tarvitsee vain täyttää muutama kenttä. Jotkut kentät ovat valinnaisia, ja monet täytetään automaattisesti silloin, kun täytät kohteeseen liittyvät kentät.  

## <a name="to-create-a-service-order" />Huoltotilauksen luominen
1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltotilaus.  
3. Valitse **Nro**-kenttään numero huoltotilaukselle.  

     Jos taas olet määrittänyt huoltotilauksille numerosarjan **Huoltohallinnon asetukset** -sivulla, voit valita seuraavan saatavilla olevan huoltotilauksen numeron <kbd>Enter</kbd>-näppäimellä.  

4. Syötä **Asiakasnro** -kentässä asiamukainen asiakas luettelosta. Ohjelma täyttää automaattisesti asiakkaaseen liittyvät kentät tiedoilla **Asiakas** -taulukosta.  

5. Riippuen asetuksista pikavälilehdellä **Pakolliset kentät** **Huoltohallinnon asetukset** -sivulla voi olla, että sinun tulee täyttää **Huoltotilauksen tyyppi** - ja **Myyjän koodi**  -kentät.  
6. Muiden kenttien täyttäminen on valinnaista.  
7. Rekisteröi huoltonimikerivit.  

## <a name="to-create-a-service-order-from-a-contract" />Huoltotilausten luominen sopimuksista
Huoltotilauksia voidaan luoda huoltonimikkeiden ylläpitoa varten automaattisesti huoltosopimusten perusteella.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Luo sopimushuoltotilauksia** ja valitse sitten vastaava linkki.  
2. Määritä **Huoltosopimuksen otsikko** -pikavälilehdessä suodatukset, joita haluat käyttää.  
3. Täytä **Asetukset**-pikavälilehdessä **Aloituspvm**- ja **Lopetuspvm**-kenttiin aloituspäivämäärä ja lopetuspäivämäärä sen mukaan, mille jaksolle haluat luoda sopimushuoltotilaukset. Eräajo luo huoltotilauksia, jotka sisältävät huoltonimikkeitä palvelusopimuksille, joiden seuraavat suunnitellut huoltopäivämäärät ovat tänä määräaikana.  

    > [!NOTE]  
    >  Ohjelmassa on rajoitus sille, miten monta päivää voi käyttää päivämäärävälinä jokaisena kertana, kun tämä eräajo suoritetaan. Tämä raja asetetaan **Sopim. huoltotil. maksimipäivät** -kentässä **Huoltohallinnon Asetukset** -sivulla.  

4. Valitse **Toiminto** -kentässä  **Luo huoltotilaus**.  
    > [!NOTE]  
    >  Tilausta, jolla on useita huoltonimikkeitä, ei voi luoda, jos **Yksi huoltonimikerivi/tilaus** -kenttä **Huoltohallinnon asetukset** -sivulla on määritetty. 

## <a name="to-convert-a-service-quote-to-a-service-order" />Huoltotarjousten muuntaminen huoltotilauksiksi
Kun asiakas on hyväksynyt huoltotarjouksen, se muunnetaan huoltotilaukseksi. Tarjous poistetaan ja uusi huoltotilaus määritetään käyttämällä samaa kuvausta kuin huoltotarjous. Ohjelma laskee uudelleen huoltotilauksen vastauspäivämäärän ja -ajan sekä asettaa sen tilaksi **Odottava**. Se muuttaa tilauksessa olevien huoltonimikkeiden korjauksen tilaksi **Alku**.  

[!INCLUDE[prod_short](includes/prod_short.md)] etsii kaikkien huoltotarjouksessa olevien huoltonimikkeiden osalta kohdistustapahtumia, joiden tila on **Aktiivinen**. Jos tällaisia kohdistustapahtumia löytyy, ohjelma päivittää niiden kohdistuksen tilaksi **Uudelleenkohdistamista tarvitaan**. Kun huoltotilauksessa olevia huoltonimikkeitä uudelleenkohdistetaan, ohjelma muuttaa tarjoukselle rekisteröityjen kohdistustapahtumien tilaksi **Valmis.**   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltosopimustarjoukset** ja valitse sitten vastaava linkki.  
2. Valitse huoltotilaukseksi muunnettava huoltotarjous.  
3. Valitse **Tee tilaus** -toiminto.  

## <a name="to-check-item-availability-for-one-or-more-orders" />Vähintään yhden tilauksen saatavuuden tarkistaminen
Voit esimerkiksi tarkistaa ja katsoa, onko nimikettä, joka sinun tulee täyttää tilaukseen, varastossa tai milloin sitä löytyy varastosta. Jos nimike on lisäksi varattavissa, voit varata sen ja varmistaa, että se on käytettävissäsi. Voit tarkistaa tietyn tilauksen tai kaikkien tilausten saatavuuden.  

1.  Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Lähetystaulukko** ja valitse sitten vastaava linkki.  
2. Tee jompikumpi seuraavista toimista:  

    * Jos kyse on tietystä tilauksesta, valitse ensin tilaus ja sitten **Kysynnän yleiskuvaus** -toiminto.  
    * Jos on kaikista tilauksista, valitse **Näytä asiakirja**. **Huoltotilaus**-sivu avautuu.  

3. Laajenna nimikeryhmittely **Kysynnän yleiskuvaus** -sivulla ja näytä nimikkeen saatavuustiedot. Voit esimerkiksi katsoa varastossa olevien nimikkeiden määrän. Näet myös, jos ja milloin kohde on käytettävissä, jos se on jälkitoimituksessa, eli lähdetyyppi = osto tai onko se varattu.

## <a name="to-reserve-an-item-for-a-service-order" />Varaa huoltotilauksen nimike
Jos huoltotilauksen nimikkeen saatavuus on varmistettava, voit varata nimikkeen.

1. Syötä **Etsi**-ruudussa **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Valitse ensin huoltotilaus ja sitten **Muokkaa**.  
3. Valitse ensin **Toiminnot**, sitten **Tilaus** ja lopuksi **Huoltorivit**.  
4. Valitse **Huoltorivit**-sivulla varattava nimike ja valitse sitten **Varaa**-toiminto.  
5. Valitse **Varaus**-sivulla **Varaa nykyiseltä riviltä**.

## <a name="to-insert-lines-based-on-standard-service-codes" />Rivien lisääminen vakiohuoltokoodien perusteella
Jos olet määrittänyt vakiohuoltokoodit ja liittänyt ne huoltonimikeryhmiin, voit lisätä vakiohuoltokoodeihin linkitettyjä vakiorivejä huoltoasiakirjoihin. Lisätietoja on kohdassa [Vakiohuoltokoodien määrittäminen](service-how-setup-service-coding.md).   

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Huoltotilaukset** ja valitse sitten vastaava linkki.  
2. Luo uusi huoltotilaus.  
3. Täytä tarvittavat kentät.  
4. Syötä huoltonimikeriveille pakolliset tiedot.  
5. Valitse ensin sen huoltonimikkeen rivi, jolle haluat luoda huoltorivejä ja sitten **Hae vakiohuoltokoodit**. Ohjelma avaa **Huoltonimikeryhmän vakiokoodit** -sivun ja riveillä määritetyn huoltonimikeryhmän vakiokoodit.  
6. Valitse sopiva koodi ja anna vakiohuoltorivit valitsemalla **OK**.  

> [!NOTE]  
>  Jos asiakirjan huoltonimikerivin **Huoltonimikeryhmän koodi** -kenttä on tyhjä, huoltonimike ei kuulu mihinkään huoltonimikeryhmään. Tällöin **Huoltonimikeryhmän vakiokoodit** -sivulla on kaikkien ohjelmassa määritettyjen vakiohuoltokoodien luettelo. Valitse luettelosta asiakirjaan lisättävät vakiohuoltorivit. Voit myös valita tietylle huoltonimikeryhmälle liitettyjen vakiohuoltokoodien luettelosta. Voit katsella luetteloa valitsemalla koodin **Huoltonimikeryhmän koodi** -kentässä **Huoltonimikeryhmän vakiokoodit** -sivulla.  

## <a name="to-register-internal-or-public-comments" />Sisäisten tai julkisten kommenttien rekisteröiminen
Voit antaa lisätietoja lisäämällä huoltotilauksiin ja huoltotarjouksiin tulostettavia kommentteja. Voit kirjoittaa enintään 80 merkkiä (välilyönnit mukaan lukien). Jos tekstiä on kirjoitettava enemmän, valitse toinen rivi. Rekisteröi kommentti valitsemalla ensin rivi ja sitten **Kommentit**-toiminto.  

## <a name="to-delete-invoiced-service-orders" />Laskutettujen huoltotilausten poistaminen
Tilaukset poistetaan ohjelmasta automaattisesti sen jälkeen, kun ne on laskutettu kokonaan. Kun lasku on kirjattu, vastaava tapahtuma luodaan **Kirjatut huoltolaskut** -sivulla. Kirjattua asiakirjaa voi katsella **Kirjattu huoltolasku** -sivulla.  

Ohjelma ei poista huoltotilauksia automaattisesti, jos tilauksen kokonaismäärä on kirjattu **Huoltolasku**-sivulla eikä huoltotilauksessa. Tällöin sinun on ehkä poistettava laskutetut tilaukset, joita ei poistettu. Voit tehdä sen suorittamalla **Poista laskutetut huoltotilaukset** -eräajon.  

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Poista laskutetut huoltotilaukset** ja valitse sitten vastaava linkki. **Poista laskutetut huoltotilaukset** -eräajon pyyntösivu avautuu.  
2. Voit valita poistettavat tilaukset määrittämällä **Nro**-, **Asiakasnro**- ja **Laskutusasiakkaan nro** -kenttien suodattimet. -kentät.  
3. Valitse **OK**.  


## <a name="see-also" />Katso myös
[Huollon kirjaus](service-service-posting.md)  
[Huoltotilauksen kirjaaminen](service-how-to-post-service-orders.md)  
[Huoltohallinnon määrittäminen](service-setup-service.md)  
[Huoltotehtävien käyttäminen](service-how-to-work-on-service-tasks.md)  
[Resurssien kohdistaminen](service-how-to-allocate-resources.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
