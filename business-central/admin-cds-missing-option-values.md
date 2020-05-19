---
title: Puuttuvien asetusarvojen käsitteleminen
description: Lisätietoja täyden synkronoinnin epäonnistumisen estämisestä yhdistettyjen kenttien erilaisten asetusten vuoksi.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 42ad388e6c07ca259d4ef6095b9f8c908b509407
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196852"
---
# <a name="handling-missing-option-values"></a>Puuttuvien asetusarvojen käsitteleminen
[!INCLUDE[d365fin](includes/cds_long_md.md)] sisältää vain kolme asetusjoukkokenttää, jotka sisältävät Asetus-tyyppiset [!INCLUDE[d365fin](includes/d365fin_md.md)] -kenttiin yhdistettävissä olevat asetusarvot<!-- Option type, not enum? @Onat can you vertify this? --> automaattista synkronointia varten. Synkronoinnin aikana muut kuin yhdistetyt asetukset ohitetaan ja puuttuvat asetukset liitetään liittyvään [!INCLUDE[d365fin](includes/d365fin_md.md)] -tauluun ja lisätään **CDS-asetuksen yhdistäminen** -järjestelmätauluun myöhemmin tapahtuvaa manuaalista käsittelemistä varten. Voit esimerkiksi lisätä puuttuvat asetukset tuotteeseen ja päivittää sitten yhdistämismäärityksen. Tässä osassa kuvataan, miten tämä tehdään.

**Integrointitaulukon yhdistämismääritys** -sivulla on kolme kenttäyhdistämistä, jotka sisältävät vähintään yhden yhdistetyn asetusarvon. Täyden synkronoinnin jälkeen **CDS-asetuksen yhdistäminen** -sivu sisältää vastaavasti kolmen kentän muut kuin yhdistetyt asetukset.

|         Tietue             | Asetusarvo | Asetusarvon otsikko |
|----------------------------|--------------|----------------------|
| Maksuehdot: NET30       | 1            | Netto 30               |
| Maksuehdot: 2%10NET30   | 2            | 2 % 10; Netto 30        |
| Maksuehdot: NET45       | 3            | Netto 45               |
| Maksuehdot: NET60       | 4            | Netto 60               |
| Toimitusehto: FOB       | 1            | FOB                  |
| Toimitusehto: NOCHARGE  | 2            | Ei veloitusta            |
| Kuljetusliike: AIRBORNE   | 1            | Lentoposti             |
| Kuljetusliike: DHL        | 2            | DHL                  |
| Kuljetusliike: FEDEX      | 3            | FedEx                |
| Kuljetusliike: UPS        | 4            | UPS                  |
| Kuljetusliike: POSTALMAIL | 5            | Posti          |
| Kuljetusliike: FULLLOAD   | 6            | Täysi kuorma            |
| Kuljetusliike: WILLCALL   | 7            | Noutoasiakas            |

**CDS-asetuksen yhdistäminen** -sivu perustuu **CDS-tili**-taulun enum-arvoihin. [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksessa tilientiteetin seuraavat kentät yhdistetään asiakas- ja toimittajatietueiden kenttiin:

- **Osoite 1: Kuljetusehdot**, jonka tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Osoite 1: Toimitustapa**, jonka tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Maksuehdot**, joiden tietojen tyyppi on Enum ja jonka arvot määritetään seuraavasti:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Kaikki [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen yllä mainitut enum-arvot yhdistetään [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen asetusjoukkoihin.

### <a name="extending-option-sets-in-d365fin"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen asetusjoukkojen laajentaminen
1. Luo uusi AL-laajennus.

2. Lisää Enum-laajennus laajennettaville asetuksille. Varmista, että käytät samaa arvoa. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Sinun on käytettävä [!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen samoja asetuksen tunnusten arvoja kuin [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksen enum-arvon laajennuksen yhteydessä. Muussa tapauksessa synkronointi epäonnistuu.

> [!NOTE]
> Uusien asetusarvojen nimien ja otsikoiden kymmenen ensimmäisen merkin on oltava samoja. Esimerkiksi kaksi asetusta, joiden nimet ovat Siirretään 20 työpäivää ja Siirretään 20 kalenteripäivää, aiheuttavat virheen, koska molemmissa on samat 10 ensimmäistä merkkiä (Siirretään). Anna nimiksi esimerkiksi SIIR20 TP ja SIIR20 KP.

### <a name="update-d365fin-option-mapping"></a>[!INCLUDE[d365fin](includes/cds_long_md.md)] -sovelluksen asetusten yhdistämisen päivittäminen
Nyt voit luoda uudelleen [!INCLUDE[d365fin](includes/cds_long_md.md)] -asetusten ja [!INCLUDE[d365fin](includes/d365fin_md.md)] -tietueiden välisen yhdistämismäärityksen.

Valitse **Integrointitaulukon yhdistämismääritys** -sivulla rivi **Maksuehdot**-yhdistämistä varten. Valitse sitten **Synkronoi muokatut tietueet** -toiminto. **CDS-asetuksen yhdistäminen** -sivulle päivitetään alla olevat lisätietueet.

|         Tietue                 | Asetusarvo   | Asetusarvon otsikko |
|--------------------------------|----------------|----------------------|
| Maksuehdot: NET30           | 1              | Netto 30               |
| Maksuehdot: 2%10NET30       | 2              | 2 % 10; Netto 30        |
| Maksuehdot: NET45           | 3              | Netto 45               |
| Maksuehdot: NET60           | 4              | Netto 60               | 
| **Maksuehdot: CASH PAYME**  | **779800001**  | **Kassamaksu**     |
| **Maksuehdot: TRANSFER**    | **779800002**  | **Siirto**         |

**Maksuehdot**-taulukko [!INCLUDE[d365fin](includes/d365fin_md.md)] -sovelluksessa sisältää nyt [!INCLUDE[d365fin](includes/cds_long_md.md)] -palvelun asetusten uudet tietueet. Seuraavassa taulukossa uudet asetukset ovat lihavoituna. Kursivoidut rivit edustavat kaikkia asetuksia, jotka voidaan nyt synkronoida. Jäljellä olevat rivit kuvaavat asetuksia, joita ei käytetä. Ne ohitetaan synkronoinnin aikana. Voit poistaa ne tai laajentaa CDS-asetukset käyttämällä samoja nimiä.)

| Koodi       | Eräpäivän laskenta | Alennuspvm:n laskenta | Alennus-% | Laske maksualen. hyvityslask. | Kuvaus       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 PÄIVÄÄ    | 10P                  |                           | 0.         | EPÄTOSI                         | 10 päivää netto       |
| 14 PÄIVÄÄ    | 14D                  |                           | 0.         | EPÄTOSI                         | 14 päivää netto       |
| 15 PÄIVÄÄ    | 15D                  |                           | 0.         | EPÄTOSI                         | 15 päivää netto       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | EPÄTOSI                         | 1 kuukausi / 2 % 8 päivää |
| 2 PÄIVÄÄ     | 2D                   |                           | 0.         | EPÄTOSI                         | 2 päivää netto        |
| *2%10NET30* |                      |                           | 0.         | EPÄTOSI                         |                   |
| 21 PÄIVÄÄ    | 21D                  |                           | 0.         | EPÄTOSI                         | 21 päivää netto       |
| 30 PÄIVÄÄ    | 30D                  |                           | 0.         | EPÄTOSI                         | 30 päivää netto       |
| 60 PÄIVÄÄ    | 60D                  |                           | 0.         | EPÄTOSI                         | 60 päivää netto       |
| 7 PÄIVÄÄ     | 7D                   |                           | 0.         | EPÄTOSI                         | 7 päivää netto        |
| ***CASH PAYME*** |                      |                           | 0.         | EPÄTOSI                         |                   |
| NK         | NK                   |                           | 0.         | EPÄTOSI                         | Nykyinen kuukausi     |
| JV        | 0D                   |                           | 0.         | EPÄTOSI                         | Jälkivaatimuksella  |
| *NET30*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| *NET45*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| *NET60*      |                      |                           | 0.         | EPÄTOSI                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | EPÄTOSI                         |                   |

## <a name="see-also"></a>Katso myös