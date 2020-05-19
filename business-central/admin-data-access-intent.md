---
title: Tietokannan käyttötarkoituksen hallinta Business Centralissa | Microsoft Docs
description: Tietokannan käyttötarkoituksen muuttaminen raportteja, API-sivuja ja kyselyjä varten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/30/2020
ms.author: jswymer
ms.openlocfilehash: b46786b60d7c5799b056c49188785bd595db57ff
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333906"
---
# <a name="managing-database-access-intent"></a>Tietokannan käyttötarkoituksen hallinta 

Superkäyttäjä ja järjestelmänvalvoja voivat muuttaa tietokannan käyttötarkoitusta raporteissa, API-tyyppisillä sivuilla ja kyselyissä. Näin parannetaan palvelun suorituskykyä.

## <a name="overview"></a>Yleiskuvaus

[!INCLUDE[d365fin](includes/d365fin_md.md)] voidaan määrittää käyttämään ensisijaisen (vain luku) tietokannan vain luku -replikoita. Tietokannan replikan käyttäminen vähentää ensisijaisen tietokannan työkuormaa. Joissakin tapauksissa se parantaa myös tietojen tarkastelemisen suorituskykyä asiakasohjelmassa. Replikat ovat hyödyllisiä objekteille, kuten raporteille, kyselyille ja API-sivuille, joita käytetään vain tietojen tarkastelemiseen tietojen muokkaamisen sijaan.

Kun objektit suoritetaan, tietokannan käyttötarkoitus määrittää, käytetäänkö vain luku -replikaa (jos se on käytettävissä) vai ensisijaista tietokantaa. Raportit, API-sivut ja kyselyt kehitetään ennalta määritetyn tietokannan käyttötarkoituksen kanssa (katso [DatabaseAccessIntent-ominaisuus](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

**Tietokannan käyttötarkoitusluettelo** -sivulla voit ohittaa objektien ennalta määritetyn tietokannan käyttötarkoituksen objektien suorituksen aikana.

Tietokannan termeissä tätä ominaisuutta kutsutaan yleisesti *lukemisen skaalaamiseksi*. Lisätietoja lukemisen skaalaamisesta ja tietokannan käyttötarkoituksesta [!INCLUDE[prodshort](includes/prodshort.md)]:ssä on kohdassa [Lukemisen skaalautumisen käyttäminen paremman suorituskyvyn saavuttamiseksi](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) [!INCLUDE[prodshort](includes/prodshort.md)]:n kehittäjän ja hallinnon ohjeessa.

## <a name="to-change-the-database-access-intent"></a>Tietokannan käyttötarkoituksen muuttaminen

1. Valitse ![Lamppu, joka avaa Kerro, mitä haluat tehdä -toiminnon](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Tietokannan käyttötarkoitusluettelo** ja valitse sitten liittyvä linkki.

    Sivulla on luettelo kaikista raporteista, sivuista ja kyselyistä. **Käyttötarkoitus**-sarakkeessa on jokin seuraavista arvoista:

    |**Asetus**|**Kuvaus**|  
    |------------|-------------|  
    |**Oletus**|Osoittaa, että objekti käyttää ennalta määritettyä tietokannan käyttötarkoitusta.|
    |**Salli kirjoitus**|Asettaa objektin käyttämään ensisijaista tietokantaa, jolloin käyttäjä voi muokata tietoja.|
    |**Vain luku**|Asettaa objektin käyttämään tietokannan replikaa. Tämä tarkoittaa sitä, että käyttäjä voi vain katsella tietoja, ei muuttaa niitä.|

2. Valitse **Muokkaa luetteloa** -toiminto.

3. Muuta **Muokkaa - Tietokannan käyttötarkoitusluettelo** -sivulla **Käyttötarkoitus**-kenttää objekteille.

    > [!NOTE]
    > Jos muokattavan objektin, kuten asiakaskortin, tilaksi määritetään **Vain luku**, käytetään yhä ensisijaista tietokantaa käyttötarkoituksesta huolimatta. Näin käyttäjät voivat tehdä muutoksia normaaliin tapaan.

## <a name="see-related-training-at-microsoft-learn"></a>Aiheeseen liittyviä kursseja on saatavilla kohteessa [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Katso myös
[Liiketoiminnan toiminnallisuus](across-business-functionality.md)  
[Yleiset liiketoimintatoiminnot](ui-across-business-areas.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] -ohjelman käyttäminen](ui-work-product.md)  
[Käytön aloittaminen](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  