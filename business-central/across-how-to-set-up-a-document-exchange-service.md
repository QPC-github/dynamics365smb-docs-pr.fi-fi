---
title: "Document Exchange -palvelun määrittäminen | Microsoft Docs"
description: "Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 043034d281eb4b58fab8ab4344987d5d3ca5f494
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen
Ulkoista palveluntarjoajaa käytetään sähköisten asiakirjojen vaihtamiseen liikekumppaneiden kanssa. Lisätietoja on kohdassa [Sähköinen tiedonsiirto](across-data-exchange.md).  

## <a name="to-set-up-a-document-exchange-service"></a>Document Exchange -palvelun määrittäminen  
1. Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Document Exchange -palvelun asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2. Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Description|  
    |---------------------------------|---------------------------------------|  
    |**Käyttäjäagentti**|Anna teksti, jolla voidaan tunnistaa yrityksesi asiakirjan vaihtoprosesseissa.|  
    |**Document Exchange -palvelun vuokraajatunnus**|Anna vuokraaja document exchange -palvelussa, joka edustaa yritystäsi. Document exchange -palvelun tarjoaja tarjoaa tämän.|  
    |**Käytössä**|Määritä, onko palvelu käytössä. **Huomautus:** heti, kun palvelu otetaan käyttöön, ainakin kaksi työjonon tapahtumaa luodaan käsittelemään sähköisten asiakirjojen liikenne sisään ja ulos [!INCLUDE[d365fin](includes/d365fin_md.md)]:sta. Kun palvelu poistetaan käytöstä, työjonon tapahtumat poistetaan.|  
    |**Rekisteröinnin URL-osoite**|Määritä verkkosivu, jossa document exchange -palvelu rekisteröidään.|  
    |**Palvelun URL-osoite**|Määritä sen document exchange -palvelun osoite, joka kutsutaan, kun lähetät ja vastaanotat sähköisiä asiakirjoja.|  
    |**Sisäänkirjautumisen osoite**|Määritä document exchange -palvelun kirjautumissivu, johon kirjoitat yrityksesi käyttäjänimen ja salasanan kirjautuessasi palveluun.|  
    |**Kuluttajan avain**|Anna kolmen osapuolen OAuth-avain kuluttaja-avaimelle. Document exchange -palvelun tarjoaja tarjoaa tämän.|  
    |**Kuluttajan salainen avain**|Anna piilokoodi, joka suojaa kuluttaja-avainta. Saat sen Document exchange -palveluntarjoajalta.|  
    |**Tunnus**|Anna kolmen osapuolen OAuth-avain tunnukselle. Saat sen Document exchange -palveluntarjoajalta.|  
    |**Tunnuksen salainen avain**|Anna piilokoodi, joka suojaa tunnusta. Document exchange -palvelun tarjoaja tarjoaa tämän.|  

> [!NOTE]  
>  Suosittelemme, että suojaat **VAN-palvelun asetukset** -ikkunaan kirjoittamasi kirjautumistiedot. Palvelimen tiedot voi salata luomalla uusia salausavaimia tai tuomalla olemassa olevia salausavaimia, jotka otetaan käyttöön tietokantayhteyden muodostavassa palvelininstanssissa. Tämä kuvataan seuraavassa menettelytavassa.  

## <a name="to-encrypt-your-logon-information"></a>Kirjautumistietojen salaaminen  
1. Valitse **VAN-palvelun asetukset** -ikkunassa **Salauksen hallinta** -toiminto.  
2. Ota tietojen salaus käyttöön **Tietojen salauksen hallinta** -ikkunassa. <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a>Katso myös  
[Tiedonsiirron määrittäminen](across-set-up-data-exchange.md)  
[Sähköinen tiedonsiirto](across-data-exchange.md)
