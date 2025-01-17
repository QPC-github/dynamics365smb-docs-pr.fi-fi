---
title: Varastotyöntekijöiden määrittäminen
description: 'Jokainen varastotoimintoja tekevä käyttäjä on määritettävä varastotyöntekijäksi ja liitettävä yhteen oletussijaintiin ja mahdollisesti muihin sijainteihin, jotka eivät ole oletussijainteja.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees" />Varastotyöntekijöiden määrittäminen

Jokainen varastotoimintoja suorittava käyttäjä on määritettävä varastotyöntekijäksi ja määritettävä oletussijaintiin. [!INCLUDE [prod_short](includes/prod_short.md)] suodattaa varastotoiminnot työntekijän oletussijaintiin. He voivat suorittaa varastotoimintoja vain sijainnissa. Voit myös määrittää käyttäjän muihin sijainteihin. He voivat käyttää niitä, mutta he eivät voi suorittaa aktiviteetteja näissä sijainneissa.

## <a name="to-set-up-warehouse-employees" />Varastotyöntekijöiden määrittäminen

1. Valitse ![Lamppu, joka avaa Kerro-ominaisuuden.](media/ui-search/search_small.png "Kerro, mitä haluat tehdä") -kuvake, syötä **Fyysisen varaston työntekijät** ja valitse sitten vastaava linkki.  
2. Valitse **Uusi**-toiminto.  
3. Valitse **Käyttäjätunnus**-kenttä ja valitse sitten käyttäjä, joka lisätään varaston työntekijäksi. Valitse **OK**-painike.  
4. Syötä **Sijaintikoodi**-kenttään käyttäjän työskentelypaikan sijainnin koodi.  
5. Ota käyttöön **Oletus**-vaihto, jos haluat määrittää, että tämä on ainoa sijainti, jossa työntekijä voi suorittaa varastotoimintoja.  
6. Liitä sijainteihin muita työntekijöitä tai liitä aiemmin luoduille varastotyöntekijöille muita sijainteja toistamalla nämä vaiheet.  

## <a name="see-related-microsoft-trainingtrainingmodulesget-started-warehouse-management" />Lue aiheeseen liittyen [Microsoftin koulutukset](/training/modules/get-started-warehouse-management/)

## <a name="see-also" />Katso myös

[Varastohallinnan yleiskuvaus](design-details-warehouse-management.md)
[Varasto](inventory-manage-inventory.md)  
[Varastoinninhallinnan määrittäminen](warehouse-setup-warehouse.md)  
[Kokoonpanon hallinta](assembly-assemble-items.md)  
[Käsittele kohdetta [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Laskun kirjauskäytännön määrittäminen käyttäjille](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
