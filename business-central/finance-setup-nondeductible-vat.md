---
title: Vähennyskelvottoman arvonlisäveron määrittäminen
description: 'Tässä artikkelissa kerrotaan, miten vähennyskelvoton ALV voidaan määrittää Microsoft Dynamics 365 Business Centralissa.'
author: altotovi
ms.author: altotovi
ms.reviewer: null
ms.service: dynamics365-business-central
ms.topic: how-to
ms.search.keywords: 'VAT, non-deductible, setup'
ms.search.form: '187, 472, 473'
ms.date: 04/26/2023
ms.custom: bap-template
---

# <a name="set-up-non-deductible-vat" />Vähennyskelvottoman arvonlisäveron määrittäminen

Vähennyskelvoton arvonlisävero (ALV) on ostajan maksettavaksi tuleva ALV, mutta se ei ole vähennyskelpoinen ostajan omasta ALV-velasta. Yritykset voivat yleensä periä ALV:n liiketoimintansa yhteydessä olevien tavaroiden ja palveluiden hankinnasta. Joissakin tilanteissa yritys kuitenkin aiheuttaa ALV:n, joka ei ole vähennyskelpoinen. Nämä tilanteet liittyvät yleensä paikallisiin määräyksiin ja voivat vaihdella maittain. Vähennyskelvottoman tai osittain vähennyskelpoisen arvonlisäveron käyttömalli on kuitenkin samanlainen. Voit käyttää suhteellista ALV:ia ALV:n laskemiseen, kun ALV on vähennyskelpoista ja vähennyskelvotonta.

Yleisesti ottaen ALV:tä ei voi vähentää joistakin ostoista seuraavien seikkojen vuoksi:

- **Ostettavien tavaroiden tai palveluiden tyyppi** – ALV on kokonaan tai osittain vähennyskelvoton lain säännöksen mukaan tavaroista, kuten autoista, matkapuhelimista ja ravintoloista ostetuista ruoista.
- **Osittain vähennyskelpoinen suhteellinen ALV** – ALV on suhteutettu arvonlisäverovelvollisen myyntitoiminnan ja kaikkien suoritettujen toimintojen suhteeseen. Tämän suhteen ylittävää ALV:tä ei voida vähentää.

Koska voi olla vaikea tietää, missä ja miten nimikettä käytetään, sinun on otettava yhteyttä oman maasi paikallisiin veroviranomaisiin ja selvitettävä, vähennetäänkö tietty prosenttiosuus ALV:stä historiallisten tietojen perusteella.

## <a name="use-non-deductible-vat" />Vähennyskelvottoman ALV:n käyttö

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV:n määrittäminen** ja valitse sitten vastaava linkki.
2. Valitse **Salli vähennyskelvoton ALV** -valintaruutu.

    > [!IMPORTANT]
    > Kun olet ottanut käyttöön vähennyskelvottoman ALV:n, et voi poistaa sitä käytöstä, koska ominaisuus voi sisältää muutoksia tietoihin ja saattaa aloittaa joidenkin tietokantataulukoiden päivittämisen. Microsoft suosittelee, että otat tämän ominaisuuden ensin käyttöön ja testaat sen eristysympäristössä, ennen kuin otat sen käyttöön tuotantoympäristössä.

3. Määritä, miten järjestelmä käsittelee vähennyskelvottomia ALV-arvoja.

    1. Määritä **Käytä nimikekustannusta** -kentässä, lisätäänkö vähennyskelvoton ALV nimikekustannukseen nimikkeiden ostamisen yhteydessä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta nimikekustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    2. Valitse **Käyttöomaisuuden kustannukset** -valintaruutu, jos haluat lisätä käyttöomaisuuden kustannukseen vähennyskelvottoman ALV:n, kun ostat uusia käyttöomaisuushyödykkeitä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta käyttöomaisuuskustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    3. Valitse **Käytä projektin kustannukseen** -valintaruutu, jos haluat määrittää, että vähennyskelvoton ALV täytyy lisätä projektin kustannuksiin projektinimikkeiden ostamisen yhteydessä. Muussa tapauksessa vähennyskelvottomalla ALV:llä ei ole vaikutusta työkustannuksiin, ja koko summa tallennetaan vain pääkirjanpidon tasolla.
    4. Valitse **Näytä vähennyskelv. ALV riveinä** -valintaruutu, jos haluat määrittää, että vähennyskelvottoman ALV:n on oltava asiakirjarivisivuilla, jotta ALV-summia on helpompi manipuloida.

## <a name="use-the-non-deductible-vat-percentage" />Käytä vähennyskelvotonta ALV-prosenttia

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden 3.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **ALV-kirjausten asetukset** ja valitse sitten vastaava linkki.
2. Määritä **ALV-kirjauksen asetukset** -sivun kentät seuraavassa taulukossa kuvatulla tavalla.

    | Kenttä | Kuvaus |
    |-------|-------------|
    | Salli vähennyskelvoton ALV-peruste | Määritä, otetaanko vähennyskelvoton ALV huomioon nykyisessä liiketoiminnan ALV-kirjausryhmän ja tuotteen ALV-kirjausryhmän yhdistelmässä. |
    | Vähennyskelvoton ALV-% | Määritä tapahtuman summan prosenttimäärän, josta ei makseta ALV:tä. |
    | Vähennyskelvottomien ostojen ALV-tili | Määritä siihen ALV-summaan liitetyn tilin, jota ei ole vähennetty ostettujen tavaroiden tai palvelujen tyypin vuoksi. |

    > [!NOTE]
    > Jos haluat, että pääkirjanpito (KP) -tapahtumat, jotka käyttävät erillistä tiliä myynti-/ostotilin sijaan, voivat jättää **vähennyskelvottoman oston ALV-tili** -kentän tyhjäksi tai määrittää **KP-tili**-kentän.

3. Valitse **OK**.

> [!NOTE]
> Et voi käyttää ei-realisoitunutta ALV:ia yhdessä vähennyskelvottoman ALV:n kanssa.
>
> Älä käytä samaa **ALV-tunnus**-arvoa sekä normaalille ALV:lle, jossa **vähennyskelvoton ALV-%** -kentän arvo on **0** (nolla) ja normaali ALV, jossa **vähennyskelvoton ALV-%** -kentän arvoksi on määritetty muu kuin nolla. Muussa tapauksessa vähennyskelvottoman ALV-summan kokonaissumma lasketaan virheellisesti.

## <a name="see-also" />Katso myös

[Taloushallinto](finance.md)  
[Arvonlisäveron laskemisen ja kirjaustapojen määrittäminen](finance-setup-vat.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
