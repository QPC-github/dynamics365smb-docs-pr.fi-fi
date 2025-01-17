---
title: 'Liitteiden, linkkien ja muistioiden lisääminen tietueisiin'
description: 'Liitä hyperlinkki asiakirjaan tai sivusto tiettyyn tietueeseen, kuten asiakkaaseen tai asiakirjaan.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 02/24/2023
ms.custom: bap-template
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents" />Korttien ja asiakirjojen liitteiden, linkkien ja muistioiden hallinta

Tiedostoja voi liittää, linkkejä lisätä ja muistiinpanoja kirjoittaa useimpien luettelosivujen, korttien ja asiakirjojen **Tietoruutu**-ruudun **Liitteet**-välilehdessä. Välilehden otsikossa oleva luku ilmaisee, kuinka monta liitettyä tiedostoa, linkkiä tai muistiinpanoa kortissa tai asiakirjassa on.

**Rivit**-pikavälilehdessä vodaan lisäksi liittää asiakirjoja tietylle riville **Liitteet**-toiminnolla. Esimerkiksi rakenteen tekniset tiedot halutaan ehkä liittää ostolaskun nimikkeeseen.

Liitteet, linkit ja muistiinpanot pysyvät korttiin tai asiakirjaan liitettyinä muihin tiloihin käsiteltäessä. Kyse voi olla esimerkiksi jatkuvasta myyntitilauksesta kirjattuun myyntilaskuun. Järjestelmä ei kuitenkaan käsittele mitään liitetyyppiä esimerkiksi tulostettaessa tai tallennettaessa tiedostoon.

Liitteitä voi lisätä myös [!INCLUDE [prod_short](includes/prod_short.md)]ista lähetettäviin sähköposteihin. Kun sähköposti lähetetään asiakirjasta, kuten myyntitarjouksesta, **Lisää tiedosto lähdeasiakirjasta** -toiminto sallii siihen liitettyjen tiedostojen valitsemisen. Vain asiakirjaan liitettyjä tiedostoja voidaan valita. Riveihin liitettyjä tiedostoja ei voida valita.

> [!NOTE]
> Kun toimitat ja laskutat myynti- tai ostotilauksen osittain, liite liitetään vain kyseisen tilauksen lopulliseen laskuun. Vastaavasti kun laskutuksessa käytetään lykkäysominaisuutta, liite liitetään asiakirjan KP-tapahtumiin mutta ei lykkäystapahtumiin.
>
> Jos tilaus poistetaan ennen laskutusta, myös liite poistetaan. Jos ostotilaukset laskutetaan käyttämällä ostolaskun Hae vastaanoton rivit -toiminto, ostotilauksen liitettä ei lisätä ostolaskuun.

## <a name="to-attach-a-file-to-a-purchase-invoice" />Tiedoston liittäminen ostolaskuun

Korttiin, asiakirjaan tai asiakirjan riviin liitettävän tiedoston tyypillä ei ole merkitystä, sillä kyse voi olla teksti-, kuva- tai videotiedostossa. Tämä on kätevää esimerkiksi silloin, kun haluat tallentaa toimittajan laskun PDF-tiedostona liittyvään [!INCLUDE[prod_short](includes/prod_short.md)]in ostolaskuun.

> [!NOTE]
> Saapuvat asiakirjat -ominaisuudella liitetyt tiedostot eivät sisälly **Liitteet**-välilehteen. Lisätietoja on kohdassa [Saapuvat asiakirjat](across-income-documents.md). Sama koskee myös asiakirjojen riveihin liitettyjä tiedostoja.

Seuraava toimenpide perustuu ostolaskuun. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

> [!TIP]
> Jos liite on asiakirjan rivikohtainen, se voidaan liittää riviin. Valitse ensin rivi ja sitten **Liitteet**-toiminto.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Ostolaskut** ja valitse sitten vastaava linkki.
2. Avaa ostotilaus, johon tiedosto halutaan liittää.
3. Valitse **tietoruudussa** **Liitteet**.
4. Valitse **Asiakirjat**-kentässä arvo, kuten 0.
5. Valitse **Liitetyt asiakirjat** -sivun **Liite**-kentässä **Valitse tiedosto** -toiminto.
6. Valitse tiedosto haluamastasi sijainnista ja valitse sitten **Avaa**-painike.

Tiedosto on nyt liitetty ostolaskuun.

## <a name="to-view-an-attached-file" />Tarkastele liitettyä tiedostoa

1. Avaa **Liitteet**-välilehti **tietoruudussa**.
2. Valitse **Asiakirjat**-kentässä arvo, kuten 1.
3. Valitse **Liitetyt asiakirjat** -sivulla **Esikatselu**-toiminto.
4. Ladatun tiedoston avaaminen.

## <a name="to-save-a-document-as-a-pdf-attachment" />Asiakirjan tallentaminen PDF-liitteenä

Kun asiakirja on tallennettava tiedostoksi, voit käyttää **Liitä PDF-tiedostona** -toimintoa ja tallentaa nykyisen asiakirjan sisällön PDF-tiedostoksi, joka on liitetty asiakirjan tietoruutuun. Tämä on hyödyllistä esimerkiksi silloin, kun asiakirjat noudattavat useita vaiheita prosessissa, kuten esimerkiksi myyntiprosessissa ja hyväksynnän työnkulussa, ja haluat viitata edellisen vaiheen tulostukseen.

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse ensin myyntitilaus ja valitse sitten **Liitä PDF-tiedostona** -toiminto.

PDF-tiedosto ja sen sisältö myyntitilauksesta lisätään **Liitteet**-välilehteen tietoruudussa.

## <a name="to-add-a-link-from-an-item-card" />Linkin lisääminen nimikekortista

Voit lisätä kortista tai asiakirjasta linkin mihin tahansa URL-osoitteeseen. Tämä kätevää esimerkiksi silloin, kun haluat linkittää nimikekortin toimittajan nimikeluetteloon.

Seuraava toimenpide perustuu nimikekorttiin. Vaiheet ovat samanlaiset kaikissa tuetuissa korteissa ja asiakirjoissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Nimikkeet** ja valitse sitten vastaava linkki.
2. Valitse nimike, josta haluat lisätä linkin, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Linkit**-kohdassa **+**-kuvake.
4. Anna linkki **Linkin osoite** -kentässä.

    Linkin on oltava kelvollinen Internet- tai intranet-osoite.

5. Kirjoita **Kuvaus**-kenttään linkkiä koskevia tietoja.  
6. Valitse **OK**-painike.

Linkki on nyt liitetty nimikekorttiin.  

## <a name="to-write-a-note-on-a-sales-order" />Muistion kirjoittaminen myyntitilaukseen

Voit kirjoittaa asiakirjaan tai korttiin muistion, jossa on esimerkiksi ohjeita muille asiakirjan tai kortin käyttäjille. Voit sisällyttää muistioihin tiedostolinkkejä ja URL-osoitteita.

> [!NOTE]
> **Liitteet**-välilehdessä olevat muistiot eivät liity sisäiseen muistiotoimintoon, jota käytetään lähinnä työnkulujen käyttäjien keskinäiseen viestintään. Lisätietoja on kohdassa [Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md).

Seuraava toimenpide perustuu myyntitilaukseen. Vaiheet ovat samanlaiset kaikissa tuetuissa asiakirjoissa ja korteissa.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Myyntitilaukset** ja valitse sitten vastaava linkki.
2. Valitse myyntitilaus, johon haluat kirjoittaa muistion, ja valitse sitten tietoruudussa **Liitteet**-välilehti.
3. Valitse **Muistiot**-osassa **+**-kuvake.
4. Kirjoita **Huomautus**-kenttään tekstiä, kuten Tämä on kiireellinen tilaus.
5. Valitse **OK**-painike.

Huomautus on nyt liitetty myyntitilaukseen.

## <a name="see-also" />Katso myös
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Saapuvat asiakirjat](across-income-documents.md)  
[Työnkulkuilmoitusten määrittäminen](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
