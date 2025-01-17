---
title: Kirjatun myyntilaskun korjaaminen tai peruuttaminen
description: 'Aiheessa käsitellään, miten kirjattu myyntilasku korjataan, kumotaan tai peruutetaan ja miten myyntihyvityslasku kohdistetaan.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="correct-or-cancel-unpaid-sales-invoices" />Maksamattomien myyntilaskujen korjaaminen tai peruuttaminen

Voit korjata tai peruuttaa maksamattoman kirjatun myyntilaskun, jos sitä ei ole toimitettu kokonaan. Tästä on hyötyä, jos teet virheen tai jos asiakas pyytää muutosta ennen kuin toimitus on valmis. Kaikissa muissa tilanteissa on suositeltavaa luoda korjaava myyntihyvityslasku suoraan. Lisätietoja on kohdassa [Myyntihyvitysaskun luominen kirjatusta myyntilaskusta](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Kun kirjattu myyntilasku on osittain tai kokonaan maksettu, et voi korjata tai peruuttaa sitä itse kirjatusta myyntilaskusta. Sen sijaan sinun on luotava manuaalisesti myyntihyvityslasku, jolla myynti mitätöidään ja asiakas hyvitetään. Sitä voi haluttaessa hallita myyntipalautustilauksella. Lisätietoja on kohdassa [Myyntipalautusten tai -peruutusten käsitteleminen](sales-how-process-sales-returns-cancellations.md).

Maksamattoman tai toimittamattoman kirjatun myyntilaskun peruuttaminen tai korjaaminen on kuvattu seuraavassa taulukossa.

| Toiminto | Kuvaus |
| --- | --- |
| **Peruuta** |Kirjattu myyntilaskun peruutetaan. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun **Peruutettu**- ja **Maksettu**-valintaruudut ovat valittuina. |
| **Korjaa** |Kirjattu myyntilasku peruutetaan. Uusi myyntilasku, jossa on samat tiedot, luodaan, paitsi jos kirjattu myyntitilaus kirjattiin myyntitilauksesta. Tässä tapauksessa ehdotamme, että peruutat kirjatun myyntilaskun ja teet korjauksen ja jatkat myyntirosessia alkuperäisestä myyntitilauksesta. <br/><br/>Uudella myyntilaskulla on eri numero kuin alkuperäisellä myyntilaskulla. Korjaavat myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun **Peruutettu**- ja **Maksettu**-valintaruudut ovat valittuina. |

Kun korjaat tai peruutat kirjatun myyntilaskun, korjaavaa myyntihyvityslaskua käytetään kaikkiin pääkirjanpidon ja varastotapahtumiin, jotka luotiin, kun alkuperäinen myyntilasku kirjattiin. Tämä kumoaa kirjatun myyntilaskun kirjanpitotietueissa ja jättää korjaavan kirjatun myyntihyvityslaskun kirjausketjua varten.  

> [!TIP]
> Jos myyntilaskun ennakkomaksulasku on kirjattu ja sitä sitten korjataan tai se peruutetaan, myös ennakkomaksu on korjattava tai peruutettava. Lisätietoja on kohdassa [Ennakkomaksujen korjaaminen](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice" />Kirjatun myyntilaskun peruuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat peruuttaa.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi peruuttaa kirjattua myyntilaskua, koska se on jo peruutettu tai korjattu.
3. Valitse **Kirjattu myyntilasku** -sivulla **Peruuta**-toiminto.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.
4. Valitse **Näytä korjaava hyvityslasku**, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

### <a name="partial-invoice-posting-also-supported" />Osittaisen laskun kirjausta tuetaan myös

Jos peruutus liittyy osittaiseen laskun kirjaukseen, alkuperäinen myyntitilausrivi päivitetään peruutetun laskutetun määrän mukaiseksi. **Laskutettava määrä** - ja **Laskutettu määrä** -kentät liittyvässä myyntitilauksessa palautetaan arvoihin ennen osittaista kirjausta.

## <a name="to-correct-a-posted-sales-invoice" />Kirjatun myyntilaskun korjaaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Kirjatut myyntilaskut** ja valitse sitten vastaava linkki.  
2. Valitse kirjattu myyntilasku, jonka haluat korjata.

    > [!NOTE]  
    >   Jos **Peruutettu**-valintaruutu on valittuna, et voi korjata kirjattua myyntilaskua, koska se on jo korjattu tai peruutettu.
3. Valitse **Kirjattu myyntilasku** -sivulla **Korjaa**-toiminto.  

    > [!NOTE]
    > Jos myyntilasku kirjattiin myyntiilauksesta, sinun kannattaa *peruuttaa* tämä myyntilasku ja käsitellä korjaus alkuperäisestä myyntitilauksesta. Jos alkuperäinen myyntitilaus on poistettu, esimerkiksi jos se on kokonaan toimitettu, voit luoda uuden myyntitilauksen käyttämällä **Kopioi asiakirja** -toimintoa. Lisätietoja on kohdassa [Myyntihyvitysaskun luominen kopioimalla kirjatun myyntilaskun](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Luodaan samoilla tiedoilla uusi myyntilasku, johon voit tehdä korjauksen. Alkuperäisen kirjatun myyntilaskun **Peruutettu**-kentän arvoksi muutetaan **Kyllä**.

    Korjaava myyntihyvityslasku luodaan automaattisesti ja kirjataan mitätöimään alun perin kirjattu myyntilasku.
5. Valitse **Näytä korjaava hyvityslasku** -toiminto, kun haluat tarkastella kirjattua myyntihyvityslaskua, joka mitätöi alkuperäisen kirjatun myyntilaskun.

## <a name="see-related-microsoft-trainingtrainingmodulesship-invoice-items-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[Myynti](sales-manage-sales.md)  
[Myynnin määrittäminen](sales-setup-sales.md)  
[Asiakirjojen lähettäminen sähköpostitse](ui-how-send-documents-email.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
