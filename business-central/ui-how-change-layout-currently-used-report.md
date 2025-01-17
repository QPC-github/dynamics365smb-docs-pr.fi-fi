---
title: Raportin ulkoasun muuttaminen erilaisilla asetteluvalinnoilla
description: Voit käyttää raportissa erilaisia asetteluja ja muuttaa raportin ulkoa asua asetteluja vaihtelemalla.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 03/07/2022
ms.author: jswymer
---
# <a name="legacy-set-the-layout-used-by-a-report" />(Vanha) Raportin käyttämän asettelun määrittäminen

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Raportti voidaan määrittää useille raportin asetteluille, joita voidaan vaihtaa tarpeen mukaan.

Raporttiin käytettävissä olevien asettelujen mukaan voit valita valmiin RDLC-raporttiasettelun, sisäänrakennetun Word-raportin asettelun tai mukautetun asettelun käytön välillä. Lisätietoja RDLC- ja Word-raporttiasettelusta sekä valmiista ja mukautetuista asetteluista ja muista ominaisuuksista on ohjeaiheessa [Raporttiasetteluiden hallinta](ui-manage-report-layouts.md).

Kun mukautettuja raportin asetteluita määritetään, voit valita ne asiakas- ja toimittajakorteista ja määrittää, että valittuja asetteluita käytetään asiakirjoissa, jotka ovat kyseessä olevalle asiakkaalle tai toimittajalle. Lisätietoja on kohdassa [Asiakkaiden ja toimittajien asiakirja-asettelujen määrittäminen ](ui-define-customer-vendor-document-layouts.md).

> [!TIP]  
> Word-raportin asettelua käyttävät asiakirjaraportit (eivät luettelot) ovat yleensä nopeampia kuin RDLC-raporttiasettelua käyttävät raportit. Jos sinulla on mahdollisuus valita asiakirjaraportin asetteluksi joko Word- tai RDLC-raportin asettelua, Word-raporttiasettelu on paras vaihtoehto.

## <a name="to-change-which-report-layout-to-use-for-a-report-or-document" />Raporttia tai asiakirjaa varten käytettävän raporttiasettelun muuttaminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Raporttiasetteluvalinta** ja valitse sitten vastaava linkki.
  
   **Raporttiasetteluvalinta**-sivulla on luettelo kaikista raporteista, joita voi käyttää sivun yläosan **Yritys**-kentässä määritetyssä yrityksessä. **Asettelun kuvaus** <!-- **Selected Layout** -->-kenttä määrittää tällä hetkellä raportissa käytetyn raporttiasettelun.
2. Määritä **Yritys**-kenttä yläosassa yritykseksi, joka sisältää raportin.

   Tämän kentän avulla voit määrittää samalle raportille eri asettelut eri yrityksissä.

3. Voit muuttaa raportin käyttämää asettelua valitsemalla raportin rivin ja asettamalla **Valittu asettelu** -kentän arvoksi yhden seuraavista vaihtoehdoista:
   * **RDLC (valmis)**, käyttää raportissa valmista RDLC-raporttiasettelua.
   * **Word (valmis)**, käyttää raportissa valmista Word-raporttiasettelua.
   * **Mukautettu**, käyttää raportissa mukautettua asettelua.  

> [!NOTE]
> Jos valitset raporttiasettelutyypin **RDLC (sisäinen)** tai **Word (sisäinen)** ja näyttöön tulee virhesanoma siitä, että raportin asettelu ei määritetyn tyyppinen, sinun on valittava toinen asetteluvaihtoehto tai luotava mukautettu raportin asettelu, joka on haluamasi tyyppinen. Tutustu seuraaviin toimiin.

Lisätoimia ei vaadita, jos valitsit valmiin RDLC- tai Word-raporttiasettelun ja asettelua käytetään, kun raportti suoritetaan seuraavan kerran.

## <a name="to-change-the-custom-layout-to-use-for-a-report-layout" />Raporttiasettelussa käytettävän mukautetun asettelun muuttaminen

Haluat ehkä myös muuttaa käytössä olevaa mukautettua asettelua. Lisätietoja on kohdassa [Raportin mukautettujen asettelujen luominen ja muokkaaminen](ui-how-create-custom-report-layout.md).

Kaikki yrityksen raportin asetteluissa olevat mukautetut raporttiasettelut näkyvät **Mukautetut raporttiasettelut** -sivulla. **Raporttiasettelun valinta** -sivulla voit nähdä, mitkä mukautetut asettelut ovat käytettävissä **Mukautetut asettelut** -tietoruudussa.

1. Valitse **Raporttiasettelun valinta** -sivun muokattavan raporttiasettelun riviltä valintapainike **Mukautetun asettelun kuvaus** -kentässä.
2. Valitse **Mukautetut raporttiasettelut** -sivulla rivi mukautetulle asettelulle, jota haluat käyttää. Valitse sitten **OK**-painike.

Valitsemasi mukautetun asettelun nimi näkyy nyt **Mukautetun asettelun kuvaus** -kentässä, ja sitä käytetään, kun raporttia tai asiakirjaa esikatsellaan, tulostetaan tai lähetetään seuraavan kerran.

Voit nyt siirtyä asiakas- ja toimittajakortteihin ja määrittää, mitä asetteluita käytetään eri asiakirjoissa, joita lähetät kyseessä olevalle asiakkaalle tai toimittajalle – esimerkiksi tilausvahvistuksissa tai maksumuistutuksissa. Lisätietoja on kohdassa [Asiakkaiden ja toimittajien asiakirja-asettelujen määrittäminen ](ui-define-customer-vendor-document-layouts.md).

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics-365-business-centralindex" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Katso myös
[Raporttiasetteluiden hallinta](ui-manage-report-layouts.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
