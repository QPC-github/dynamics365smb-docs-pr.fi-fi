---
title: Shopifyn yhdistimen käytön aloittaminen
description: Ensimmäiset vaiheet määritettäessä Business Centralin ja Shopifyn välistä yhteyttä
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Shopifyn yhdistimen käytön aloittaminen

Yhdistä Shopify-kauppasi [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelmaan ja maksimoi yrityksesi tuottavuus. Hallitse ja tarkastele yrityksesi ja Shopify-kauppasi merkityksellisiä tietoja yhtenä yksikkönä.

Jos haluat käyttää Shopifyta yhdessä [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa, sinun on ensin tehtävä joitakin asioita. Tämä artikkeli toimii oppaana, jonka avulla voit integroida Shopify-kaupan [!INCLUDE [prod_short](../includes/prod_short.md)] -ohjelman kanssa.

## Vaatimukset Shopifylle

Tarvitaan:

- Shopify-tili
- Shopify-verkkokauppa

Lisätietoja Shopify-kokeiluversioiden luomisesta ja suositelluista asetuksista on kohdassa [Shopify-tilin luominen ja määrittäminen](shopify-account.md).

## Business Centralin edellytykset

- Varmista **[Shopify-yhdistin](https://go.microsoft.com/fwlink/?linkid=2196238)**-sovellus on asennettuna.

  Sovellus on asennettu valmiiksi kaikille uusille kirjautumisyrityksille ja kokeiluversioihin. Tutustu tarkemmin sovellusten asentamiseen AppSourcesta: [Laajennusten asentaminen ja poistaminen](../ui-extensions-install-uninstall.md#install). Noudata alla mainittuja ohjeita, jos sinulla ei ole [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaa.

- Varmista, että käyttäjällä on oikeat käyttöoikeudet. Shopify-yhdistin sisältyy **Shopify – Admin (SHPFY – ADMIN)** -käyttöoikeuksien joukkoon. Lisätietoja on kohdissa [Luo käyttäjät käyttöoikeuksien mukaan](../ui-how-users-permissions.md) ja [Käyttöoikeuksien määrittäminen käyttäjille ja ryhmille](../ui-define-granular-permissions.md).

## Asenna Dynamics 365 Business Central -sovellus Shopify-verkkokauppaasi

Olemassa olevien [!INCLUDE[prod_short](../includes/prod_short.md)] -esiintymien osalta tämä vaihe on valinnainen, ja se voidaan ohittaa.

1. Etsi [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) -sovellus [Shopify AppStoresta](https://apps.shopify.com/)
2. Valitse **Lisää sovellus**-painike. Kirjaudu Shopify-tilillesi, jos ohjelma pyytää. Valitse verkkokauppa, jos sinulla on niitä useampia.
3. Kun olet tarkastanut tietosuojan ja käyttöoikeudet, valitse **Asenna sovellus** -painike.

   Voit etsiä ja avata asennetun **Dynamics 365 Business Central** -sovelluksen **Shopifyn hallinta** -sivupalkin osassa **Sovellukset**-sivulla.
4. Valitse **Rekisteröidy nyt** aloittaaksesi [!INCLUDE[prod_short](../includes/prod_short.md)]-kokeilun tai **Kirjaudu**, jos sinulla on jo [!INCLUDE[prod_short](../includes/prod_short.md)]. Sinut ohjataan uudelleen [Business Central](https://businesscentral.dynamics.com) -sivullesi.
5. Suorita seuraavat vaiheet [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa.

## Business Centralin yhdistäminen Shopify-verkkokauppaan

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](../media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvakkeeseen, syötä **Shopify-myymälä** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.  
3. Syötä **Koodi**-kenttään koodi, jonka avulla etsiminen on helppoa [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmassa. Nimi voi esimerkiksi kuvastaa sitä, mitä kauppa myy, kuten "huonekalut" tai "kahvi", tai maata tai aluetta, jossa se palvelee.
4. Syötä **Shopify URL** -kenttään URL-osoite verkkokauppaan, johon muodostat yhteyttä. Käytä seuraavaa muotoa: `https://{shop}.myshopify.com/`.
5. Ota käyttöön **Käytössä**-valitsin ja tarkista ja hyväksy sitten ehdot ja edellytykset.
6. Jos ohjelma pyytää, kirjaudu Shopify-tilillesi. Tarkasta tietosuojan ehdot ja käyttöoikeudet ja valitse sitten **Asenna sovellus** -painike.

Toista vaiheet 2-6 kaikille verkkokaupoille, jotka haluat yhdistää.

### Tunnetut ongelmat

- Selain estää ponnahdusikkunan. Kun **otat käyttöön** -vaihtonäppäimen [!INCLUDE [prod_short](../includes/prod_short.md)] avaa **Odotetaan vastausta - Älä sulje tätä sivua** -sivun, kun se odottaa Shopifyn käyttöoikeustunnusta. Jos sivu on suljettu tai estetty, et voi muodostaa yhteyttä Shopifyhin. Lisätietoja on kohdassa [pyydä käyttöoikeustunnusta](troubleshoot.md#request-the-access-token)
- [Virhe: Oauth-virhe invalid_request: Shopify-sovellusrajapintasovellusta ei löytynyt haulla api_key](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Yhteyttä ei voi muodostaa eritysympäristöstä](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)

## Seuraavat vaiheet

Nyt verkkokauppa on yhteydessä [!INCLUDE[prod_short](../includes/prod_short.md)] -ohjelmaan. Seuraavissa vaiheissa määritetään, miten ja mitä synkronoidaan.

- [Kohteiden synkronointi](synchronize-items.md)
- [Asiakkaiden synkronointi](synchronize-customers.md)
- [Tilausten synkronointi](synchronize-orders.md)

## Testistrategiat

Integraation testaamiseen on erilaisia lähestymistapoja, ja jokaisella lähestymistavalla on hyvät ja huonot puolensa.

Voit yhdistää [!INCLUDE[prod_short](../includes/prod_short.md)]- ja Shopify-tilit niin usein kuin haluat. Shopify-yhdistin vaikuttaa vain ympäristöön tai täsmällisemmin yritykseen, jossa se on käytössä. Voit muodostaa yhteyden samaan Shopify-verkkokauppaan useista eri ympäristöistä tai yrityksistä. Voit poistaa yhdistimen käytöstä ja ottaa sen uudelleen käyttöön.

Synkronointitestejä on helppo suorittaa uudelleen. Yhdistimen avulla voit poistaa tuotuja tietoja, kuten tuotteita, asiakkaita ja tilauksia, ja tuoda ne sitten uudelleen. Yksinkertaisesti [Palauta synkronointi](troubleshoot.md#reset-sync).

### Shopify-eristysympäristö ja Business Central -eristysympäristö

Tämä on todennäköisesti turvallisin tapa testata integraatiota. Shopify-eristysympäristön käyttämisen sijaan voit käyttää myös kokeiluversiotilausta tai kehityssäilöä. [!INCLUDE[prod_short](../includes/prod_short.md)]-ohjelmassa voi myös käyttää tuotantoympäristössä olevaa testiyritystä.

Saat lisätietoja [!INCLUDE[prod_short](../includes/prod_short.md)] -eristysympäristöistä siirtymällä kohtaan [Uuden ympäristön luominen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### Shopify-eristysympäristö ja Business Central -tuotanto

Tätä määritystä *ei* suositeltu testausmääritys, koska Shopify-yhdistin voi luoda tai muokata nimikkeitä ja asiakkaita. Se voi myös luoda myyntiasiakirjoja, kuten tilauksia ja laskuja. Näitä asiakirjoja voi olla vaikea kumota.
 
Jos sinun on käytettävä tätä määritystä, suosittelemme tarkistamaan ja todennäköisesti poistamaan käytöstä seuraavat asetukset:

* **Luo tuntematon nimike automaattisesti** -arvoksi älä luo nimikkeitä
* **Shopify voi päivittää nimikkeitä** -arvoksi ei päivitä yhdistettyjä kohteita
* **Luo Tuntematon asiakas automaattisesti** -arvoksi älä luo asiakkaita ja kontakteja
* **Shopify voi päivittää asiakkaita** -arvoksi ei päivitä nykyisiä asiakkaita
* **Luo myyntitilaus automaattisesti** -arvoksi älä luo myyntitilauksia ja myyntilaskuja

Lisätietoja on kohdassa [Ympäristön palautus](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).

### Shopify-tuotanto ja Business Central -eristysympäristö

Tietojen varmuuskopiointi kannattaa suorittaa. Voit esimerkiksi viedä tuotteita ja asiakkaita. Lisätietoja on kohdassa [Liikkeen tietojen varmuuskopiointi CSV-tiedostojen avulla](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Poista **Poista Salli tietojen synkronointi Shopifyhin** -vaihtonäppäin käytöstä, jotta [!INCLUDE[prod_short](../includes/prod_short.md)] ei kirjoittaisi Shopifyhin. Tässä tapauksessa pystyt tuomaan tuotteita, kuvia, asiakkaita ja tilauksia Shopifysta. Et voi kuitenkaan lähettää nimikettä, hintoja, varastomääriä, asiakkaita tai täyttämistietoja Shopifyhin.

Jos pidät **Salli tietojen synkronointi Shopifyhin** -vaihtonäppäimen käytössä, lisäsuojatoimet ovat seuraavat:

*   Valitse **Luo tuote -määritteen tila** -kentässä **luonnos**, jos haluat varmistua siitä, että viedyt tuotteet eivät ole ostajien saatavilla. Voit tarkistaa, miltä tuotteet näyttävät verkkokaupassa, ja synkronoida hinnat, optiot ja varastomäärät. Varmista vain, että käytät suodattimia **Lisää nimike Shopifyhin** -sivulla, kun haluat rajoittaa vietävien nimikkeiden määrää.
* Ota **Vie asiakas Shopifyhin** -vaihtonäppäin pois käytöstä, jotta et lähetä asiakkaita Shopifyhin.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/paths/use-shopify-connector-dynamics-365-business-central/)

## Katso myös

[Vaihekuvaus: Shopify-yhdistimen määrittäminen ja käyttäminen](walkthrough-setting-up-and-using-shopify.md)  

