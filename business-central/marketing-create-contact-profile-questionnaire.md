---
title: Profiilien avulla voit luokitella kontaktisi
description: Liiketoimintakontaktien luokittelu profiilikyselyiden avulla
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Liiketoimintakontaktien luokittelu profiilikyselyiden avulla
Voit määrittää kyselyprofiileja niille kyselyille, joita haluat käyttää, kun syötät tietoja kontaktiesi profiileista. Jokaisessa kyselyssä voit määrittää eri kysymykset, jotka aiot esittää kontakteillesi.  

Voit saada ohjelman vastaamaan automaattisesti joihinkin kysymyksiin kontakti-, asiakas- tai toimittajatietojen pohjalta.  

## <a name="to-add-a-profile-questionnaire"></a>Profiilikyselyjen lisääminen
1.  Valitse ![Etsi sivu tai raportti](media/ui-search/search_small.png "Etsi sivu tai raportti -kuvake") -kuvake, kirjoita **Kyselyn asetukset** ja valitse sitten aiheeseen liittyvä linkki.  
2.  Valitse **Kotisivu**-välilehden **Uusi**-ryhmässä **Uusi**.  
3.  Täytä tarvittavat kentät. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Kysymyksien lisääminen profiilikyselyyn
1.  Valitse haluttu profiilikysely. Valitse sitten **Koti**-välilehdellä **Prosessi**-ryhmässä **Muokkaa kyselyn asetuksia**.  
2.  Valitse ensimmäisellä tyhjällä rivillä **Tyyppi**-kenttä, valitse **Kysymys** ja kirjoita kysymys **Kuvaus**-kenttään. Täytä rivin muut kentät.  
3.  Napsauta seuraavalla tyhjällä rivillä **Tyyppi**-kenttää, valitse **Vastaus** ja kirjoita vastaus **Kuvaus**-kenttään.  
4.  Valitse **Priority**-kentässä prioriteetti. Määritä **Arvosta**- ja **Arvoon**-kenttiin pisteväli. Kontaktit, jotka saavat pisteitä määritetyltä väliltä, saavat vastauksen.  

Toista nämä vaiheet ja syötä kaikki profiilikyselyn kysymykset ja vastaukset.

Kun olet luonut kyselyn, sinun on luotava kontaktin luokituksia luokitellaksesi kontaktisi. Voit myös määrittää automaattisesti kysymyksiä, jotka on luokiteltu kontaktikortin tietojen perusteella.  

> [!NOTE]
> Jos syötät kysymyksen, johon ohjelma vastaa automaattisesti, napsauta <STRONG>Rivi</STRONG>, <STRONG>Kysymyskortti</STRONG>, niin voit syöttää ne kriteerit, joita ohjelma käyttää vastatessaan kysymykseen automaattisesti.

## <a name="the-automatic-classification-of-contacts"></a>Kontaktien automaattinen luokittelu
Voit saada ohjelman luokittelemaan kontaktisi automaattisesti asiakkaan, toimittajan tai kontaktitietojen mukaan, kun määrittelet automaattisesti vastattuja profiilikysymyksiä **Profiilikyselyjen asetukset** -ikkunassa.  

> [!NOTE]
> Asiakastietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu asiakkaina, ja toimittajatietoihin perustuva luokittelu voidaan liittää vain sellaisiin kontakteihin, jotka on tallennettu toimittajina. Automaattista luokittelua ei päivitetä automaattisesti. Haluat siten ehkä päivittää profiilikyselyjäsi, sen jälkeen kun olet päivittänyt ne asiakas-, toimittaja- tai kontaktitiedot, joille profiilikysely perustuu.  

Kun olet määrittänyt automaattisesti vastattuja profiilikysymyksiä, jos liität niistä koostuvan profiilikyselyn kontaktiin, [!INCLUDE[d365fin](includes/d365fin_md.md)] liittää kontaktiin automaattisesti oikeat vastaukset.  

## <a name="example"></a>Esimerkki
Voit luokitella kontaktisi sen mukaan, kuinka paljon he ostivat sinulta:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Vastaus</strong></th>
<th><strong>Pätee seuraaviin</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>kontaktit, jotka ovat ostaneet vähintään 500 000 PVA</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>kontaktit, jotka ovat ostaneet 100 000 - 499 999 PVA</p></td>
</tr>
<tr class="odd">
<td><p>C</p></td>
<td><p>kontaktit, jotka ovat ostaneet enintään 99 999 PVA</p></td>
</tr>
</tbody>
</table>

Jotta voisit tehdä tämän, täytä **Profiilikyselyjen asetukset** -ikkuna seuraavalla tavalla:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tyyppi</strong></th>
<th><strong>Kuvaus</strong></th>
<th><strong>Automaattinen luokittelu</strong></th>
<th><strong>Arvosta</strong></th>
<th><strong>Arvoon</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Kysymys</p></td>
<td><p>ABC-luokittelu</p></td>
<td><p>Lisää rasti napsauttamalla</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Vastaus</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Vastaus</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100 000</p></td>
<td><p>499 999</p></td>
</tr>
<tr class="even">
<td><p>Vastaus</p></td>
<td><p>N</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99 999</p></td>
</tr>
</tbody>
</table>

Täytä sitten **Profiilikyselyn yksityiskohdat** -ikkuna seuraavalla tavalla:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Kenttä</strong></th>
<th><strong>Arvo</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Asiakkaan luokituskenttä</strong></td>
<td><emphasis>Myynti (PVA)</emphasis></td>
</tr>
<tr>
<td><strong>Luokittelutapa</strong></td>
<td><emphasis>Määritetty arvo</emphasis></td>
</tr>
</tbody>
</table>

Kun liität sen profiilikyselyn, jossa tämä kysymys on, kontaktiin, ohjelma lisää automaattisesti asianomaisen vastauksen tälle kontaktille kontaktikortin profiiliriveille.

## <a name="see-also"></a>Katso myös
[Kontaktihenkilöiden luominen](marketing-create-contact-persons.md)  
[Kontaktihenkilöiden luominen](marketing-how-create-contact-persons.md)  
[Kontaktiyrityksen luominen](marketing-create-contact-companies.md)  
