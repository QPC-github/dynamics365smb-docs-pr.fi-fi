---
title: Dimensioyhdistelmätapahtumien yleiskuva
description: 'Tässä artikkelissa on yleiskuvaus siitä, miten dimensioyhdistelmätapahtumat tallennetaan dimensioyhdistelmätapahtumina ja miten ne kirjataan.'
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/14/2021
ms.author: edupont
---
# <a name="dimension-set-entries-overview" />Dimensioyhdistelmätapahtumien yleiskuva
Tässä aiheessa kuvataan, kuinka dimensioyhdistelmän tapahtumat tallennetaan ja kirjataan kohteeseen [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="dimension-sets" />Dimensioyhdistelmät
Dimensioyhdistelmä on dimensioarvojen yksilöllinen yhdistelmä. Se tallennetaan dimensioyhdistelmän tapahtumiksi tietokantaan. Kukin dimensioyhdistelmän tapahtuma edustaa yksittäistä dimensioarvoa. Dimensioyhdistelmä tunnistetaan yhteisellä dimensioyhdistelmän tunnuksella, joka määritetään jokaiselle yhdistelmään kuuluvalle tapahtumalle.  

Seuraavassa esimerkissä näytetään dimensioyhdistelmä, jolla on kolme dimensioyhdistelmätapahtumaa. Dimensioyhdistelmä tunnistetaan dimensioyhdistelmän tunnuksella, joka on 108.  

|Dimensioyhdistelmän tunnus|Dimensiokoodi|Dimension arvokoodi|Dimensioarvon nimi|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|ALUE|70|Pohjois-Amerikka|  
|108|YRITYSRYHMÄ|HOME|Kotitalous|  
|108|OSASTO|MYYNTI|Myynti|  

## <a name="dimension-set-entries" />Dimensioyhdistelmän tapahtumat
Dimensioyhdistelmät tallennetaan **Dimensioyhdistelmän tapahtuma** -taulukkoon dimensioyhdistelmätapahtumina, joilla on sama dimensioyhdistelmän tunnus.  

![Dimensiojoukon tapahtumien prosessi.](media/dimensionentrynav7.png "Dimensiojoukon tapahtumien prosessi")  

Kun luot uuden päiväkirjarivin, asiakirjaotsikon tai asiakirjarivin, voit määrittää dimensioarvojen yhdistelmän. Sen sijaan, että tallentaisit jokaisen dimensioarvon erikseen tietokantaan, dimensioyhdistelmä määritetään päiväkirjan rivillä, asiakirjaotsikossa tai asiakirjan rivillä dimensioyhdistelmän tunnuksen avulla.  

Kun muokkaat **Muokkaa dimensioyhdistelmän tapahtumia** -sivua ja suljet sen, tarkastus on suoritettu nähdäksesi onko dimensioarvojen yhdistelmä olemassa dimensionyhdistelmänä taulukossa. Jos yhdistelmä tehdään taulukossa, vastaavan dimensioyhdistelmän tunnus liitetään päiväkirjariviin, asiakirjan otsikkoon tai asiakirjariville. Muussa tapauksessa taulukkoon lisätään uusi dimensioyhdistelmä ja uuden dimensioyhdistelmä tunnus määritetään päiväkirjariville, asiakirjaotsikkoon tai asiakirjariville.

## <a name="codeunit-408-dimension-management" />Codeunit 408 -dimension hallinta
Codeunit 408, dimension hallinta, on toimintokirjasto, joka käsittelee yleiset dimensioihin liittyvät tehtävät, kuten kopioinnin taulukosta toiseen tai yhdestä asiakirjasta toiseen.

## <a name="performance-improvement" />Suorituskyvyn parantaminen
Määrittämällä dimensioyhdistelmän kerran tietokannassa tietokannan tilaa säästyy ja yleinen suorituskyky on entistä parempi.  

## <a name="see-also" />Katso myös
[Rakennetiedot: dimensioyhdistelmien etsiminen](design-details-searching-for-dimension-combinations.md)   
[Rakennetiedot: taulukkorakenne](design-details-table-structure.md)   
[Rakennetiedot: Dimensioyhdistelmän tapahtumat](/dynamics365/business-central/design-details-dimension-set-entries-overview)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
