---
keywords: traffic estimator;automated personalization;ap
description: De schatter van het Verkeer verstrekt terugkoppelen die u laat weten of u voldoende verkeer voor uw activiteit van Adobe Target hebt om te slagen.
title: Schatting van het verkeer dat voor succes wordt vereist
feature: ap
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: df9cb5c4a3cd44917ee9136300e4ad68f922d3c9
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Schat het verkeer dat voor succes wordt vereist{#estimate-the-traffic-required-for-success}

Het [!UICONTROL Traffic Estimator] verstrekt terugkoppelt dat u laat weten of u voldoende verkeer voor uw [!DNL Adobe Target] activiteit hebt om te slagen.

Omdat een [!UICONTROL Automated Personalization] activiteit veelvoudige aanbiedingscombinaties gebruikt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. De [!UICONTROL Traffic Estimator] gebruiks statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de activiteit succesvol te maken.

Het [!UICONTROL Traffic Estimator] bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren, door de geschatte paginaamafbeeldingen en de typische omzettingspercentage voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Hierdoor is er voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Herinner dat [!DNL Target] willekeurig ervaringen tot de verpersoonlijkingsalgoritmen worden gebouwd dient. Het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en kan beginnen leverend gepersonaliseerde inhoud. [!DNL Target] Omdat de lift slechts wordt verwacht nadat de modellen klaar zijn, staat de visuele aanwijzing u toe om de juiste verwachting te plaatsen. Gebruik de [!UICONTROL Traffic Estimator] instructies in [!UICONTROL Visual Experience Composer] (VEC) om te bepalen wanneer de modellen klaar zijn.

## De schatter van het Verkeer gebruiken

1. From the [!UICONTROL Visual Experience Composer], click **[!UICONTROL Traffic]**.

   ![Verkeerspictogram](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   De [!UICONTROL Traffic Estimator] knop wordt geopend. U kunt **[!UICONTROL Traffic]** opnieuw klikken om het [!UICONTROL Traffic Estimator]te verbergen.

   ![](assets/ap_est.png)

1. Geef de gemiddelde conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   * **Aantal voorstellen**: Automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * **Typische conversiesnelheid**: De omrekeningskoers wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem.
   * **Geschatte bezoeken per dag**: Dit is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Dit kan op uw analysegegevens worden gebaseerd. Dit nummer moet bezoeken zijn en geen unieke bezoekers.
   * **Testduur**: Het aantal dagen waarop de activiteit moet worden uitgevoerd.

   De [!UICONTROL Traffic Estimato]r gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Boven aan het [!UICONTROL Traffic Estimator]scherm worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

   ![](assets/ap_est_no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en uw conversiesnelheid en -indrukkingen te laag zijn, [!UICONTROL Traffic Estimator] toont de code hoe lang de test moet duren om te slagen. Of, als uw verkeer laag is, [!UICONTROL Traffic Estimator] zou het lagere aantal aanbiedingscombinaties kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren:

   * U kunt een [Auto-Target](/help/c-activities/auto-target-to-optimize.md) -activiteit gebruiken in plaats van ervaringen [!UICONTROL Automated Personalization] te maken met verschillende wijzigingen van de aanbieding in één ervaringsvariatie.
   * Verminder het aantal aanbiedingscombinaties binnen uw [!UICONTROL Automated Personalization] activiteit.
   * Verhoog de duur van de activiteit.

   Pas de aantallen aan tot het [!UICONTROL Traffic Estimator] zegt u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![](assets/ap_est_yes.png)

   Als het verkeer voldoende is, toont het [!UICONTROL Traffic] pictogram een groene controle. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.

## Veelgestelde vragen over de schatter van het Verkeer

Houd rekening met de volgende veelgestelde vragen wanneer u met de [!UICONTROL Traffic Estimator]website werkt:

### Waarom bouwt [!DNL Target] geen gepersonaliseerde modellen wanneer mijn AP activiteit genoeg verkeer heeft?

In bepaalde omstandigheden, zou uw verkeer groot genoeg voor een gepersonaliseerd model kunnen zijn om worden gebouwd, maar dat verkeer zou kunnen erop wijzen [!DNL Target] dat er geen zinvol verschil tussen het gepersonaliseerde model en willekeurig is. Hoewel het model is ingebouwd [!DNL Target] en getest, wordt het niet geïmplementeerd omdat het model niet significant beter is dan willekeurig.

Een mogelijke reden waarom het model niet beter dan willekeurig is, kan zijn dat de aanbiedingen niet significant van elkaar verschillen. Als dit het geval is, kunt u proberen makend de aanbiedingen visueel verschillend als het overseinen gelijkaardig is, of u kunt proberen veranderend het overseinen zelf.
