---
title: XML-mallit tiedonsiirtomääritysten valmistelua varten
description: 'Käytä XML-malleja tiedonsiirtokehyksen määrittämiseen, jotta voit määrittää, minkä tietoelementtien kanssa haluat tehdä siirtoja.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions" />XML-mallien käyttäminen tiedonsiirtomääritysten valmisteluun

Voit ottaa XML-tiedostojen tietojen tuonnin ja viennin käyttöön [!INCLUDE[prod_short](includes/prod_short.md)]in tiedonsiirtokehyksessä määrittämällä [!INCLUDE[prod_short](includes/prod_short.md)]in kanssa vaihdettavat tietoelementit XML-mallien avulla. Se tehdään **XML-mallin tarkastelutoiminto** -sivulla lataamalla XML-rakennetiedosto, valitsemalla sopivat tietoelementit ja käynnistämällä siiten tiedonsiirtomääritys.  

 Kun olet määrittänyt XML-mallin perusteella sisällytettävät tietoelementit, voit käynnistää **Luo tiedonsiirtomääritys** -toiminnolla valittuihin tietoelementteihin perustuvan tiedonsiirtomäärityksen, joka sitten viimeistellään tiedonsiirtokehyksessä. Tällä tavoin **Kirjauksen tiedonsiirtomääritykset** -sivulla luodaan tietue. Jatka sivulla määrittämällä, mitkä tiedoston elementit ja mitkä [!INCLUDE[prod_short](includes/prod_short.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

 Tämä ohjeaihe sisältää seuraavat menettelyt:  

- XML-rakennetiedoston lataaminen  

- Solmujen valitseminen ja tyhjentäminen XML-rakenteessa  

- XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen  

## <a name="to-load-an-xml-schema-file" />XML-rakennetiedoston lataaminen

1. Varmista, että sopiva XML-rakennetiedosto on saatavilla. Tiedostotunniste on .xsd.  

2. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten vastaava linkki.  

3. Valitse **Uusi**-toiminto.  

4. Täytä kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**Koodi**|Määritä koodi, jolla identifioit XML-kaavan.|  
    |**Kuvaus**|Määritä XML-kaavan kuvaus.|  

     **Kohdenimitila**-kenttä määrittää riville ladatun XML-mallitiedoston nimitilan (joka voi olla mikä tahansa).  

5. Valitse **Lataa malli** -toiminto ja valitse XML-mallitiedosto.  

     Kun tiedosto on ladattu, rivin muihin kenttiin lisätään tiedoston tiedot ja **Malli on ladattu** -valintaruutu valitaan.  

    > [!NOTE]  
    >  Ladatun XML-rakenteen puu on oletusarvoisesti tiivistettynä. Solmun voi laajentaa **+**-painikkeella. Kaikki solmut voi laajentaa käyttämällä **Laajenna kaikki** -painiketta valintanauhasta.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema" />Solmujen valitseminen ja tyhjentäminen XML-rakenteessa

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallin tarkastelutoiminto** ja valitse sitten vastaava linkki.  

2. Täytä otsikon kentät seuraavassa taulukossa kuvatulla tavalla.  

    |Kenttä|Kuvaus|  
    |---------------------------------|---------------------------------------|  
    |**XML-mallin koodi**|Määritä vaiheessa 5 ladattu XML-rakennetiedosto XML-rakennetiedosto -osiossa.|  
    |**Uuden XMLportin numero**|Määritä niiden XMLporttien määrä, jotka luodaan tästä XML-kaavasta, kun valitset **Luo XMLport** -toiminnon.|  

     Rivit on nyt täytettä solmuilla, jotka edustavat kaikki XML-kaavan elementtejä. XML-mallin mukaan pakolliset elementtien solmut valitaan oletusarvoisesti.  

3. Laajenna ensimmäisellä rivillä **Solmun nimi**-sarakkeessa **Asiakirja**-solmu ja laajenna sitten vähitellen alapuolella olevia solmuja, joita haluat tarkastella.  

     Vaihtoehtoisesti, napsauta solmua hiiren kakkospainikkeella ja valitse sitten **Laajenna kaikki**.  

4. Valitse yksi seuraavista toiminnoista muuttaaksesi mitkä solmut näytetään.  

    |**Toiminto**|Kuvaus|  
    |----------------|---------------------------------------|  
    |**Näytä kaikki**|Kaikki solmut ovat näkyvissä.|  
    |**Piilota ei-pakollinen**|Ainoastaan XML-rakenteen perusteella pakollisia elementtejä esittävät solmut näytetään. Näiden solmujen merkintänä on yleensä **1** **MinOccurs**-kentässä.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  
    |**Piilota ei-valittu**|Vain solmut, joissa **Valittu**-valintaruutu on valittuna näytetään.<br /><br /> Käännä näkymä valitsemalla **Näytä kaikki**.|  

5. Valitse **Muokkaa** -toiminto.  

6. Määritä **Valittu**-valintaruutu jokaiselle solmulle, jonka elementin haluat olevan tuettuna liittyvän SEPA-pankkitiedoston tiedonsiirtomäärityksessä.  

    > [!NOTE]  
    >  Kun valitset pakollisen alisolmun, kaikki sen pääsolmut valitaan myös.  

7. Voit valita uudelleen kaikki solmut, jotka kuvaavat XML-mallin mukaan pakollisia elementtejä valitsemalla **Valitse kaikki pakolliset elementit** -toiminto.  

8. Poista kaikki valinnat valitsemalla **Poista kaikkien valinta** -toiminto.  

     **Valinta**-kenttä määrittää, että solmulla on vähintään kaksi sisarussolmua, jotka toimivat vaihtoehtoina.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema" />XML-rakenteeseen perustuvan tietojen vaihtamismäärityksen luominen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **XML-mallit** ja valitse sitten vastaava linkki.  

2. Valitse sopiva XML-malli ja valitse sitten **Avaa XML-mallin tarkastelutoiminto** -toiminto.  

3. Varmista, että tarvittavat solmut ovat valittuina. Lisätietoja on kohdassa Solmujen valitseminen ja tyhjentäminen XML-rakenteessa.  

4. Valitse **XML-mallin tarkastelutoiminto** -sivulla **Luo tiedonsiirtomääritys** -toiminto.  

 Tiedonsiirtomääritys luodaan **Kirjauksen tiedonsiirtomääritykset** -sivulla, jossa sen voi viimeistellä määrittämällä, mitkä tiedoston elementit ja [!INCLUDE[prod_short](includes/prod_short.md)]in kentät yhdistetään toisiinsa. Lisätietoja on kohdassa [Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md).  

> [!NOTE]  
> Voit käyttää myös **Kirjauksen tiedonsiirtomääritykset** -sivun **Hae tiedostorakenne** -toimintoa. Tämä sivu täyttää **Sarakkeen määritykset** -pikavälilehden valmiiksi **XML-mallin tarkastelutoiminto** -sivun toiminnoilla.  

> [!NOTE]
> Vuoden 2019 1. julkaisuaallossa ja sitä edeltävissä versioissa voitiin luoda rakenteeseen perustuva XMLport, joka sitten tuotiin ratkaisuun. Tämä ei ole enää mahdollista.

## <a name="see-also" />Katso myös

[Tietojenvaihtomääritysten määrittäminen](across-how-to-set-up-data-exchange-definitions.md)  
[Maksujen vienti pankkitiedostoon](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Maksujen kerääminen SEPA-suoraveloitusperintänä.](finance-collect-payments-with-sepa-direct-debit.md)  
[Tietoja tiedonvaihto-kehyksestä](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
