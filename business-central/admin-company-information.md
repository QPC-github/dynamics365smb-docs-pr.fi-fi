---
title: Yrityksen tietojen yleiskatsaus
description: 'Yritystiedot-sivu määrittää liiketoimintayksikön perustiedot, kuten nimen, osoitteen ja toimitustiedot.'
author: edupont04
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: edupont
---

# <a name="company-information-overview" />Yrityksen tietojen yleiskatsaus

[!INCLUDE[prod_short](includes/prod_short.md)] organisoi liiketoimintayksiköt *yrityksiksi*. **Yrityksen tiedot** -sivulla on täytettävä tietyt yrityksen perustiedot ja muut tarvittavat tiedot kullekin yritykselle. Ohjelma käyttää [**Yritystiedot**](https://businesscentral.dynamics.com/?page=1)-sivun tietoja asiakirjoissa, muun muassa laskujen otsikoissa. Voit perustaa useampia yrityksiä, kuten emo- ja tytäryrityksen.  

Jos yrityksen varasto sijaitsee eri osoitteessa kuin yrityksen pääkonttori, voit täyttää eri toimituskentät ja **Sijaintikoodi**-kentän **Toimitus**-pikavälilehdessä. Näiden kenttien tiedot tulostetaan sitten esimerkiksi ostotilauksiin, jotta toimittajat osaavat toimittaa nimikkeet oikeaan osoitteeseen.  

Jokaiselle määritetylle yritykselle on täytettävä **Yritystiedot**-sivu sekä **Pääkirjanpidon asetukset** -sivu. Kullekin yritykselle täytyy myös määrittää jokainen alue [!INCLUDE [prod_short](includes/prod_short.md)]issa, esimerkiksi **Myyntien ja myyntisaamisten asetukset** -sivu. Lue lisätietoja kohdasta [[!INCLUDE[prod_short](includes/prod_short.md)]in määritystehtävien yleiskatsaus](setup.md).  

**Yritystiedot**-sivulla on eri kenttiä ja pikavälilehtiä oman maasi/alueesi mukaan. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Seuraavassa taulukossa kuvataan yleisimmät pikavälilehdet.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Kun olet täyttänyt tiedot, voit sulkea sivun.  

## <a name="working-with-multiple-companies" />Useamman yrityksen käsitteleminen

Jos [!INCLUDE [prod_short](includes/prod_short.md)] -ohjelmassa on mukana useampia yrityksiä, käyttäjät voivat haluta tunnistaa nopeasti ja seurata *yrityksen merkkejä*. Lisätietoja on ohjeaiheessa [Yrityksen merkkien näyttäminen](#badge).

Tiettyjen ominaisuuksien avulla voidaan siirtyä yritysten välillä työskentelyn aikana, kuten yrityksen vaihtaja (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Lue lisää kohdasta [Siirtyminen toiseen yritykseen tai ympäristöön](ui-organization-switch.md).

## <a name="a-namebadgeadisplay-a-company-badge" /><a name="badge"></a>Näytä yrityksen merkki

Kun yrityksiä tai ympäristöjä on enemmän kuin kaksi, yrityksen vaihtaja näkyy sovelluspalkin oikeassa yläkulmassa, sovelluspalkin hakukuvakkeen lähellä. Oletusarvon mukaan yrityksen vaihtaja käyttää ![yrityksen kuvakkeen aloituksen](media/ui-experience/company-icon.png "Näyttää yrityksen vaihtajan kuvakkeen, kun käytössä on yksittäinen ympäristö") tapaan yrityksen vakiokuvaketta ja ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Näyttää yrityksen vaihtajan kuvakkeen, kun käytössä on useita ympäristöjä").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Näyttää yrityksen vaihtaja -kuvakkeen Business Central -asiakkaan otsikossa.":::  

**Yritystiedot**-sivulla voit korvata yrityksen vakiokuvakkeen käyttämällä mukautettua merkkiä yrityskohtaisesti, jos yrityksen merkki helpottaa käyttäjien tunnistamista yrityksen tunnistetiedoilla.

1. Täytä **Yrityksen tunnus**-pikavälilehden kentät tarvittaessa. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Kun olet valmis, päivitä tunnus asiakasohjelmassa päivittämällä selain (käyttämällä näppäinyhdistelmää <kbd>Ctrl</kbd>+<kbd>F5</kbd>).  

> [!NOTE]
> Yrityksen vaihtaja otettiin käyttöön vuonna 2022 julkaisuaalto 2:ssa, versiossa 21. Aiemmissa versioissa yrityksen merkkiä ei käytetä yritysten vaihtamiseen. Se näkyy useimpien sivujen oikeassa yläkulmassa, vaikka yrityksiä on vain yksi. Sen valitseminen näyttää yrityksen koko nimen ja ympäristön nimen.

## <a name="change-company-display-name" />Yrityksen näyttönimen muuttaminen

Yrityksen nimi näkyy aina vasemmassa yläkulmassa. Se on myös toiminto, jonka valitsemalla voit palata roolikeskukseen. Tämän nimen voi muuttaa **Yrityksen tiedot** -sivulla.

1. Valitse ![Hammaspyörä-kuvake, joka avaa Asetukset-valikon.](media/ui-experience/settings_icon_small.png) -kuvake ja valitse sitten **Yrityksen tiedot** -toiminto.
2. Anna uuden yrityksen nimi **Nimi**-kentässä.
3. Poistu sivulta. Järjestelmä käynnistyy uudelleen ja uusi yritys näkyy vasemmassa yläkulmassa.

## <a name="experience" />Kokemus

[!INCLUDE [prod_short](includes/prod_short.md)] -kokeiluversion oletuskäyttökokemus ei paljasta kaikkia ominaisuuksia. Voit vaihtaa koko käyttökokemusta **Yritystiedot**-sivulla. Lisätietoja on kohdassa [Näytettävien ominaisuuksien muuttaminen](ui-experiences.md).  

## <a name="see-related-microsoft-trainingtrainingmodulescreate-new-companies-dynamics-365-business-central" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/create-new-companies-dynamics-365-business-central/)

## <a name="see-also" />Katso myös

[[!INCLUDE[prod_short](includes/prod_short.md)]in määritystehtävien yleiskatsaus](setup.md)  
[Yritystietojen pika-aloitus](quick-start-company-information.md)  
[Yrityksen tietojen määrittäminen Italiassa](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Perusasetusten muuttaminen](ui-change-basic-settings.md)  
[Näytettävien ominaisuuksien muuttaminen](ui-experiences.md)  
[Uusien yritysten luominen](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
