---
title: Pankkitilien täsmäytys
description: Opettele täsmäyttämään Business Centralin kauppatapahtumat pankin tiliotteilla.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Pankkitilien täsmäytys

Pankkitäsmäytyksen avulla varmistat, että kirjanpitosi tiedot vastaavat pankistasi vastaanottamiasi tietoja. Pankkitilien täsmäytys vertaa ja täsmäyttää [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa määrittämiesi pankkitilien merkintöjä pankkisi pankkitapahtumiin. Täsmäyttäminen voi sitten kirjata saldot pankkitilillesi [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa, jotta ne ovat rahoituksen haltijoiden käytettävissä. Pankkitilin täsmäytys on myös käytännöllinen tapa löytää ja ratkaista puuttuvat maksut ja kirjanpitovirheet.

Tässä artikkelissa kuvataan, miten pankkitilin täsmäytys suoritetaan **Pankkitilin täsmäytys** -sivulla.

Voit kuitenkin myös täsmäyttää pankkitilejä **Maksujen täsmäytyskirjauskansio** -sivulla, kun käsittelet maksuja. Sovellettuihin asiakas- tai toimittajareskontrakirjauksiin liittyvät avoimet pankkitilikirjaukset suljetaan, kun valitset **Kirjaa maksut ja täsmäytä pankkitili** -toiminnon. Tämä täsmäyttää automaattisesti pankkitilin päiväkirjaan kirjattaville maksuille. Lisätietoja on kohdassa [Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Pohjois-Amerikan versioissa tämän voi suorittaa myös **Pankin täsmäytyksen työkirja** -sivulla, joka sopii paremmin sekeille ja talletuksille mutta ei sisällä pankin tiliotetiedostojen tuontia. Voit käyttää tätä sivua **Pankkitilin täsmäytys** -sivun sijasta poistamalla **Pankin täsmäytys ja autom. vastaavuus** -kentän valinta **Pääkirjanpidon asetukset** -sivulla. Lisätietoja on kohdan [Pankkitilien täsmäyttäminen](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) Yhdysvaltain paikallisissa toimintoja käsittelevässä osassa.

**Pankkitilin täsmäytys** -sivun rivit jaetaan kahteen ruutuun. **Pankin tiliotteen rivit** -ruudussa näkyvät joko tuodut pankkitapahtumat tai tapahtumat, joilla on avoimia maksuja. **Pankkitilitapahtumat**-ruudussa näkyvät sisäisen pankkitilin tapahtumat.

Pankkitapahtumien täsmäytystä sisäisten pankkitapahtumien kanssa [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa kutsutaan *kohdistukseksi*. Tapahtumia voi täsmäyttää pankkitapahtumien kanssa kahdella tavalla:

* Automaattisesti **Kohdista automaattisesti** -toiminnon avulla.
* Manuaalisesti valitsemalla rivit molemmissa ruuduissa linkittääksesi jokaisen tilioterivin yhteen tai useampaan pankkitilin kirjanpitotapahtumaan ja käyttää sitten **Kohdista manuaalisesti** -toimintoa.

Jos rivi sisältää kohdistettavia tapahtumia, rivin **Kohdistettu**-valintaruutu valitaan. Lisätietoja on kohdassa [Määritä sääntöjä maksujen automaattiselle soveltamiselle](receivables-how-set-up-payment-application-rules.md). Jos syötät tiliotteen lopetuspäivämäärän pankkitilin täsmäytyksessä sen jälkeen, kun olet täsmäyttänyt sen riveihin, joilla on tapahtumia, [!INCLUDE [prod_short](includes/prod_short.md)] kumoaa vastaavat rivit ja tapahtumat, jotka ovat kyseisen päivämäärän jälkeen.

> [!NOTE]
> Sen jälkeen kun olet syöttänyt päivämäärän Tiliotteen lopetuspvm -kenttään,Pankkitilin täsmäytys -sivu suodattaa pankkitapahtumat niin, että tapahtumat näkyvät vain kyseiseen päivämäärään asti. Voit kirjata pankkitäsmäytykset pankkitapahtumien kanssa vain tiliotteen lopetuspäivämääränä tai sitä ennen. Suodatin varmistaa, että pankkitapahtumat on tiliotteen loppupäivämääränä tasapainotettu pankin tiliotteen kanssa, jolloin erona on avoimet maksut ja sekit.

Kun **Tiliotteen rivit** -ruudun **Kokonaissaldo**-kentän arvo on yhtä suuri kuin **Täsmäytettävä saldo** -kentän ja **Tilin reskontrakirjaukset** -ruudun **Viimeinen saldo** -kentän kokonaisarvo, voit valita **Kirjaa**-toiminnon. Täsmäyttämättömät pankkitilitapahtumat säilyvät sivulla, ja osoittavat eroa, joka tulee ratkaista pankkitilin täsmäyttämiseksi.

Jos haluat tarkistaa pankkitilin täsmäytyksen ennen kirjausta, voit valmistella täsmäytyksen esikatselun käyttämällä **testiraportti**-toimintoa. Raportti on käytettävissä seuraavissa yhteyksissä:

* Kun valmistelet pankkitilin täsmäytystä **pankkitilin täsmäytys** -sivulla.
* Kun täsmäytät maksuja **Maksujen täsmäytyskirjauskansiot** -sivulla.

Kaikki rivit, joita ei voi kohdentaa, ilmaistuina arvoina **Erotus**-kentässä, pysyvät **Pankkitilin täsmäytys** -sivulla kirjauksen jälkeen. Ne edustavat eroa, joka sinun on ratkaistava, ennen kuin voit suorittaa pankkitilin täsmäytyksen. Seuraavassa taulukossa kuvataan muutamia tavallisia liiketoimintatilanteita, jotka voivat aiheuttaa eroja.

| Ero | Syy | Ratkaisu |
|------------|--------|------------|
| Pankkitilisi tapahtuma [!INCLUDE[prod_short](includes/prod_short.md)] -ohjelmassa ei ole pankin tiliotteessa. | Pankkitapahtumaa ei luotu, vaikka kirjaus tehtiin kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. | Luo puuttuva tapahtuma (tai pyydä velallista tekemään se). Tuo sitten pankin tiliotteen tiedosto uudelleen tai syötä tapahtuma manuaalisesti. |
| Pankin tiliotteen tapahtumaa ei ole asiakirjana tai kirjauskansion rivinä järjestelmässä [!INCLUDE[prod_short](includes/prod_short.md)]. | Pankkitapahtuma tehtiin ilman vastaavaa kirjausta kohteessa [!INCLUDE[prod_short](includes/prod_short.md)], esimerkiksi kulun kirjauskansiorivin kirjausta varten. | Luo ja kirjaa puuttuva tapahtuma. Lisätietoja nopeasta tavasta tämän tekemiseksi on aiheessa [Puuttuvien tapahtumien luominen pankkitapahtumien kohdistamiseksi.](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines) kanssa. |
| Sisäisen pankkitilin tapahtuma vastaa pankkitapahtumaa, mutta jotkin tiedot ovat liian erilaisia, jotta ne antaisivat vastaavuuden. | Tiedot, kuten summa tai asiakkaan nimi, on syötetty eri tavalla pankkitapahtumassa tai sisäisessä kirjauksessa. | Tarkista tiedot ja kohdenna nämä kaksi manuaalisesti. Vaihtoehtoisesti voit korjata ristiriidan. |

Erot on ratkaistava esimerkiksi luomalla puuttuvia merkintöjä ja korjaamalla ei-vastaavia tietoja tai tekemällä puuttuvia rahatapahtumia, kunnes pankkitilin täsmäytys on suoritettu ja kirjattu.

Voit täyttää **Pankin tiliotteen rivit** -ruudun **Pankkitilin täsmäytys** -sivulla seuraavalla tavalla:

* Automaattisesti käyttämällä **Tuo pankin tiliote** -toimintoa täyttämään **Pankin tiliotteen rivit** -ruutu pankkitapahtumilla tuodun tiedoston tai pankin tarjoaman tietovirran mukaisesti.
* Manuaalisesti **Ehdota rivejä** -toiminnolla täyttämään **Pankin tiliotteen rivit** -ruutu niiden kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] olevien laskujen mukaisesti, joilla on maksamattomia maksuja.

## Pankin tiliotteen rivien lisääminen tiliotteen tuomisen avulla

**Pankin tiliotteen rivit** -ruutu täytetään pankkitapahtumilla tuodun tiedoston tai pankin antaman tietovirran mukaan.

Kun haluat tuoda tiliotteet pankkisyötteiksi, sinun täytyy määrittää Envestnet Yodlee Bank Feeds -palvelu. Määritys sisältää [!INCLUDE[prod_short](includes/prod_short.md)]in pankkitilien linkityksen liittyviin verkkopankkitileihin. Lisätietoja on kohdassa [Envestnet Yodlee Bank Feeds -palvelun määrittäminen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Tiliotetiedostoja voi tuoda myös pilkuin tai puolipistein erotellussa muodossa (.CSV). Tiliotteen tuontimuodot voidaan määrittää ja muoto liittää pankkitiliin käyttämällä asetusten ohjattua määritystä **Määritä tiliotetiedoston tuontimuoto**. Näitä muotoja voi sitten käyttää, kun tiliotteita tuodaan **Pankkitilin täsmäytys** -sivulla.

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Pankkitilin täsmäytys** ja valitse sitten vastaava linkki.
2. Valitse **Uusi**-toiminto.
3. Valitse **Pankkitilin nro** -kentässä asianmukainen pankkitilin koodi. Pankkitilillä olevat tapahtumat näkyvät **Pankkitilitapahtumat**-ruudussa.
4. Syötä **Tiliotteen pvm** -kenttään pankin tiliotteen päivämäärä.
5. Syötä **Tiliotteen loppusaldo** -kenttään pankin tiliotteen saldo.
6. Jos sinulla on tiliotetiedosto, valitse **Tuo pankin tiliote** -toiminto.
7. Etsi tiedosto ja valitse sitten **Avaa**-painike tuodaksesi pankkitilin tapahtumat **Pankin tiliotteen rivit** -ruutuun **Pankkitilin täsmäytys** -sivulla.

## Pankin täsmäytyksen rivien täyttäminen Ehdota rivejä -toiminnon avulla

**Pankin tiliotteen rivit** -ruutu täytetään niiden, kohteessa [!INCLUDE[prod_short](includes/prod_short.md)] olevien laskujen mukaan, joissa on maksamattomia maksuja.  

1. Valitse **Pankkitilin täsmäytys** -sivulla **Ehdota rivejä** -toiminto.
2. Syötä **Aloituspvm**-kenttään ensimmäinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.
3. Syötä **Lopetuspvm**-kenttään viimeinen mahdollinen kirjauspäivämäärä täsmäytettäviä tapahtumia varten.

    > [!NOTE]
    > Yleensä lopetuspvm on sama kuin **Tiliotteen pvm** -kentässä määritetty päivämäärä. Jos kuitenkin haluat täsmäyttää transaktiot vain jakson osaa varten, voit syöttää eri lopetuspäivämäärän.

4. Jos et halua, että pankkitilitapahtumissa on avoimia peruutettuja avoimia tapahtumia, valitse **Ohita peruutetut tapahtumat** -vaihto. Pankkitilitapahtumien luetteloon sisällytetään oletusarvoisesti peruutetut tapahtumat tiliotteen päivämäärään asti.
5. Valitse **OK**-painike.

## Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen automaattisesti

Sivu **Pankkitilin täsmäytys** tarjoaa automaattisen vastaavuustoiminnon, joka kohdistaa maksut niihin liittyviin avoimiin tapahtumiin pankin tiliotteen rivillä (vasemmassa ruudussa) olevan tekstin vastaavuuden perusteella verrattuna yhden tai useamman pankkitilitapahtuman (oikealla puolella) tekstiin. Ehdotetut automaattiset kohdistukset voidaan korvata toisilla. Voit myös olla käyttämättä automaattista kohdistusta. Lisäohjeita on kohdassa [Pankin tiliotteen rivien ja pankkitilin tapahtumien kohdistaminen manuaalisesti](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Voit tutkia vastaavuuksien perusteita käyttämällä **Vastaavuuden tiedot** -toimintoa. Tiedot sisältävät esimerkiksi niiden kenttien nimet, jotka sisälsivät vastaavat arvot.  

1. Valitse **Pankkitilin täsmäytys** -sivulla **Kohdista automaattisesti**. **Kohdista pankkitapahtumat** -sivu avautuu.
2. Määritä **Tapahtuman päivämäärätoleranssi (päivinä)** -kenttään ajanjakso ennen ja jälkeen pankkitilitapahtuman kirjauspäivämäärän, jonka aikana toiminto hakee vastaavia tapahtumapäivämääriä tiliotteesta.

    Jos kirjoitat arvon 0 tai jätät kentän tyhjäksi, **Kohdista automaattisesti** -toiminto etsii vain vastaavat tapahtumapäivämäärät pankkitilin kirjanpitotapahtuman kirjauspäivänä.
3. Valitse **OK**-painike.

    Rivit ovat värikoodattuja, mikä auttaa hahmottamaan, mitä niillä tehdään. Kaikkien pankin tiliotteen rivien ja täsmäytettävissä olevien pankkitilitapahtumien kirjasin muuttuu vihreäksi, ja **Kohdistettu**-valintaruutu on valittuna. Pankkitilitapahtumat, jotka on jo täsmäytetty muihin pankkitilien täsmäytyksiin, näkyvät sinisenä.
4. Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto.

> [!TIP]
> Voit yhdistellä manuaalista ja automaattista vastaavuutta. Jos olet täsmäyttänyt manuaalisesti, automaattinen täsmäytyksen toiminto ei korvaa valittuja kohteita.

## Pankin tiliotteen rivien ja pankkitilitapahtumien kohdistaminen manuaalisesti

> [!TIP]
> Kun rivit ja tapahtumat täsmäytetään manuaalisesti, **Näytä kaikki**, **Näytä peruutetut tapahtumat**, **Piilota peruutetut tapahtumat** ja **Näytä ei-kohdistetut** -toiminnot helpottavat yleiskuvauksen saamista. Oletusarvon mukaan pankkitilitapahtumat eivät sisällä täsmäyttämättömiä peruutettuja tapahtumia. Jos haluat sisällyttää nämä tapahtumat luetteloon ja sovittaa ne manuaalisesti, valitse **Näytä peruutetut tapahtumat** -toiminto. Jos haluat piilottaa peruutetut tapahtumat sen jälkeen, kun olet tehnyt yhden tai useampia vastaavuuksia, vastaavat tapahtumat näkyvät edelleen.

1. Valitse **Pankkitilin täsmäytys** -sivun **Pankin tiliotteen rivit** -ruudussa kohdistamaton rivi.
2. Valitse **Pankkitilitapahtumat** -ruudussa yksi tai useampia pankkitilitapahtumia, joihin voidaan kohdistaa valitun pankin tiliotteen rivi. Voit valita useita rivejä pitämällä <kbd>CTRL</kbd>-näppäimen painettuna ja valitsemalla sitten rivit.

   > [!TIP]
   > Voit myös manuaalisesti täsmäyttää useita pankin tiliotteen rivejä yhteen pankkitilitapahtumaan. Tämä voi olla hyödyllistä esimerkiksi silloin, jos pankkitalletuksessa on useita maksutapoja, kuten eri liikkeellelaskijoiden luottokortit, ja pankkisi luettelee ne erillisinä riveinä.
3. Valitse **Kohdista manuaalisesti** -toiminto.

    Valitun pankin tiliotteen rivin ja valittujen pankkitilitapahtumien fontti muuttuu vihreäksi, ja oikeanpuoleisen ruudun **Kohdistettu**-valintaruutu on valittuna.
4. Toista vaiheet 1–3 kaikille pankin tiliotteen riveille, joita ei ole kohdistettu.

> [!TIP]
> Voit poistaa kohdistuksen valitsemalla pankin tiliotteen rivin ja valitsemalla sitten **Poista kohdistus** -toiminto. Jos olet täsmäyttänyt useita pankin tiliotteen rivejä yhteen tapahtumaan ja haluat poistaa yhden tai useamman täsmäytetyn rivin, kaikki manuaaliset vastaavuudet poistetaan tapahtumakirjauksesta, kun valitset **Poista vastaavuus**.

## Puuttuvien tapahtumien luominen ja kohdistaminen pankin tiliotteen riveihin

Joskus pankin tiliote sisältää koron tai veloitetun maksun summia. Tällaisia tiliotteen rivejä ei voi kohdistaa, koska niillä ei ole vastaavia tapahtumia kohteessa [!INCLUDE[prod_short](includes/prod_short.md)]. Tällöin jokaiselle tapahtumalle on kirjattava päiväkirjarivi. Näin luodaan liittyvä tapahtuma, johon kohdistus voidaan tehdä.

1. Valitse **Pankkitilin täsmäytys** -sivulla **Siirrä yleiseen päiväkirjaan** -toiminto.  
2. Määritä käytettävä yleinen päiväkirja **Siirrä p-til. täsm. yl. pvk:aan** -sivulla ja valitse sitten **OK**.

    **Yleinen päiväkirja** -sivu avautuu. Se sisältää kaikkien puuttuvia tapahtumia sisältävien tiliotteiden päiväkirjarivit.
3. Syötä päiväkirjariville tarvittavat tiedot, kuten vastatili. Lisätietoja on kohdassa [Yleisten päiväkirjojen käyttäminen](ui-work-general-journals.md).  
4. Tarkastele kirjaamisen tulosta ennen kirjaamista valitsemalla **Testiraportti** -toiminto. **Pankin tiliote** -raportti avautuu ja näyttää samat kentät kuin **Pankkitilin täsmäytys** -sivun otsikot.
5. Valitse **Kirjaa**-toiminto.

    Kun tapahtuma on kirjattu, täsmäytä pankin tiliotteen rivi siihen.
6. Päivitä tai avaa **Pankkitilin täsmäytys** -sivu. Uusi tapahtuma näkyy **Pankkitilitapahtumat**-ruudussa.
7. Kohdista tiliotteen rivi pankkitilitapahtumaan manuaalisesti tai automaattisesti.

## Etsi avoimia tapahtumia edellisistä kausista

Voit käyttää pankin tiliotteen raporttia, kun haluat etsiä avoimia tapahtumia edellisiltä jaksoilta. Avoimet tapahtumat avattiin ennen tiliotteen päivämäärää, eikä niitä ole suljettu, tai ne suljettiin sen jälkeen, kun pankkitäsmäytys kirjattiin.

Kun suoritat pankin tiliotteen raportin pankin tiliotteen luettelosivulta, voit ottaa **Avoimet tapahtumat** -vaihtonäppäimen käyttöön ja sisällyttää raporttiin osan, jossa on luettelo avoimista tapahtumista.

**Esimerkki** Meillä on pankkitilitapahtumat A, B ja C pankkitilillämme elokuussa. Kun me täsmäytämme pankkitilin elokuussa löydämme tiliotteen rivin, joka vastaa merkintää A, mutta ei mitään B:lle ja C:lle. Joten kirjaamme A:n täsmäytetyksi ja B:n ja C:n avoimiksi tapahtumiksi.

Syyskuussa saamme maksun merkinnästä B ja päätämme täsmäyttää pankkitilin. Jos tiliotteen raportti suoritetaan ennen täsmäytyksen kirjaamista, saat yhden täsmäyttämäsi kauppatapahtuman ja yhden avoimena olevan.

Jos tulostamme elokuun raportin, meillä on B- ja C-merkinnöissämme maksamattomia tapahtumia, vaikka suljimme B-merkinnän syyskuussa.

## Pankkitilin täsmäytyksen peruuttaminen

Jos löydät virheen kirjatussa pankkitäsmäytyksessä, voit korjata sen käyttämällä **Pankkitilin tilioteluettelo** -sivun **Kumoa**-toimintoa. Kun peruutat kirjatun pankkitäsmäytyksen, tapahtumat siirretään **Pankkitilin täsmäytys** -sivulle ja merkitään **avoimiksi**, mikä tarkoittaa, että niitä ei ole täsmäytetty. Tämän jälkeen voit korjata pankkitäsmäytyksen ja kirjata sen uudelleen.

> [!NOTE]
> Pohjoisamerikkalaisessa versiossa voit käyttää Kumoa-toimintoa kirjattujen pankkitilien täsmäytysten ja tiliotteiden peruutukseen vain, kun otat käyttöön **Pankin täsmäytys ja autom. vastaavuus** -valitsimen **Pääkirjanpidon asetukset** -sivulla. Kumoa-toiminto ei ole käytettävissä pankkitiliotteissa, jotka on kirjattu pankkitilin täsmäytysten työkirjoista.

### Pankintiliotteen numeron uudelleenkäyttö

Uuden pankkitilin täsmäytyksen tiliotteen numero otetaan pankkitililtä Viimeisen tiliotteen saldo -tiliotteena. Voit muuttaa näitä arvoja ennen uuden pankkitäsmäytyksen aloittamista. Kun kuitenkin luot uuden pankkitäsmäytyksen, [!INCLUDE[d365fin](includes/d365fin_md.md)] tarkistaa, onko tiliotteen numero jo määritetty kirjatulle tiliotteelle. Jos numero on käytössä, mutta haluat sen sijaan käyttöön uuden tiliotteen, voit käyttää **Muuta tiliotteen nroa** -toimintoa **Pankkitilin täsmäytys** -sivulla.

### Esimerkkejä

Seuraavassa on esimerkkejä siitä, miten korjataan kirjatun pankkitäsmäytyksen virhe käyttämällä samaa tai eri tiliotteen numeroa.

#### Esimerkki 1

Teit pankkitäsmäytykset tammi-, helmi- ja maaliskuussa. Pankkitiliotteen numero oli maaliskuussa 100. Myöhemmin huomaat, että maaliskuu sisälsi merkinnät vain 30. päivä asti, mikä tarkoittaa merkinnät 31. päivältä puuttuvat. Joten sinun täytyy tehdä pankkitäsmäytys maaliskuulle uudelleen. Avaa tässä tapauksessa **Pankkitilin tiliote** -sivu, valitse maaliskuun tiliote ja valitse sitten **Kumoa**. 

Uudelle pankkitäsmäytykselle annetaan tilitteen numero 101. Voit määrittää numeron 100 uudelleen valitsemalla **Muuta tiliotteen nroa** ja syöttämällä arvon **100**. 

> [!TIP]
> Muista asettaa asianmukainen tilioteen lopetuspäivämäärä (tässä esimerkissä 31. maaliskuuta) ja muokkaa **Viimeisen tiliotteen saldo** -kenttää. 

#### Esimerkki 2

Teit pankkitäsmäytykset tammi-, helmi, kesä- ja heinäkuussa. Huomaat, että helmikuu oli virheellinen. Oletetaan, että helmikuun tiliotteen numero oli 100. Kuten esimerkissä 1, käytetään Kumoa- ja Muuta tiliotteen nroa -toimintoja, jotka muuttavat tiliotteen numeron kuten yllä olevassa esimerkissä 1, jotta nyt voit tehdä uudelleen helmikuun pankkitilin täsmäytyksen.  

Sen jälkeen kun olet kirjannut helmikuun oikaistun pankkitäsmäytyksen, vastaavas Pankkitili-kortin **Viimeinen tiliotteen nro** -kentässä näkyy **100**, ja **Viimeisen tiliotteen saldo** -kentässä näkyy helmikuun tiliotteen loppusaldo. 

Jos teet seuraavan pankkitäsmäytyksen maaliskuussa, [!INCLUDE[d365fin](includes/d365fin_md.md)] määrittää tiliotteen numeroksi 101 ja antaa sille oikean **Viimeisen tiliotteen saldo** -arvon.

Jos teet seuraavan pankkitäsmäytyksen elokuun osalta, harkitse arvojen muuttamista **Viimeinen tiliotteen nro**- ja **Viimeisen tiliotteen saldo** -kentissä **Pankkitili**-kortissa ennen seuraavan pankkitäsmäytyksen luomista tai käytä **Muuta tiliotteen nroa** -toimintoa ja muuta myös **Viimeisen tiliotteen saldo** -kentän arvoa pankkitilin täsmäytyssivulla.

> [!NOTE]
> Tiliotteen numero on tärkeä, kun teet pankkitäsmäytyksiä tuotujen CAMT-tiedostojen kanssa, jotka sisältävät tiliotteen numeroita, tai kun täsmäytetään tulostettujen tiliotteiden perusteella. Jos vain lataat joukon pankkitapahtumia verkkopankista, tiliotteen numero ei yleensä ole tärkeä.  
>
> Viimeisen tiliotteen saldo -arvoa pidetään pankkitilillä virheiden minimoimiseksi pankkitäsmäytyksiä tehtäessä. Sitä voi myös muokata, joten pankkitilin täsmäytykset voidaan tehdä missä tahansa järjestyksessä. Tämä tarkoittaa myös sitä, että jos peruutat pankin tiliotteen, uusi loppusaldo ei ehkä ole seuraavassa tiliotteessa Viimeisen tiliotteen saldo. Ei ole mitään toimintoa, jolla voi siirtää saldon eteenpäin kaikille myöhemmille tiliotteille. Tämä on hyvä ottaa huomioon Kumoa-toimintoa käytettäessä.  

## Vältä suorakirjausta

Älä käytä KP-tiliä, joka mahdollistaa suoran kirjauksen pankkitilin kirjausryhmässä. Suora kirjaus katkaisee yhteyden pankkitilitapahtuman ja KP-tilitapahtuman välillä. Kun täsmäytetään pankkitilisi, suoraan KP-tiliin kirjatut tapahtumat eivät sisälly toimitukseen, ja täsmäytyksen suorittaminen on hankalaa.

Tämä virhe tapahtuu usein, kun syötät avaussaldon pankkitilille. On tärkeää, että et kirjaa alkusaldoa suoraan pääkirjanpitoon. KP-tilin tapahtumat, jotka kirjataan suoraan KP-tilille, aiheuttavat ongelmia. Nämä tapahtumat voivat esimerkiksi estää sinua täsmäyttämästä pankkitiliäsi. Ulkomaan valuutan pankkitileille tapahtumat voivat aiheuttaa eroja kertymiseen sen jälkeen, kun olet kirjannut lisää pankkitäsmäytyksiä valuutanvaihtokurssien muutosten vuoksi. Usein pankin avaussaldo kirjataan suoraan pankkitilille, ja summa päätyy KP-tiliin. Voit vaihtoehtoisesti kumota sen myöhemmin sellaisen KP-tilin osalta, jota käytät pääkirjanpidon avaussaldon tasapainottamista varten. Molemmissa tapauksissa sinun on tasapainotettava mahdolliset suorat kirjaukset KP-tiliin ennen ensimmäisen pankkitäsmäytyksen aloittamista ja erityisesti silloin, kun pankkitili käyttää ulkomaan valuuttaa.

## Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## Katso myös
[Pankkitilien täsmäytys](bank-manage-bank-accounts.md)  
[Maksujen kohdistaminen automaattisesti ja pankkitilien täsmäyttäminen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Pankkitoiminnan määrittäminen](bank-setup-banking.md)  
[Automaattinen maksujen soveltamisen sääntöjen määrittäminen](receivables-how-set-up-payment-application-rules.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
