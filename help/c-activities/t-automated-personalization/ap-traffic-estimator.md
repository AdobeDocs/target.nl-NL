---
keywords: verkeersschatting;geautomatiseerde personalisatie;ap;schatting van verkeer;auto-target
description: Gebruik de Adobe Target Traffic Estimator om te bepalen of u voldoende verkeer hebt om uw Automated Personalization-activiteit te laten slagen.
title: Hoeveel verkeer is nodig voor een succesvolle activiteit?
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
translation-type: tm+mt
source-git-commit: 094756ac64e2740e81834fde4b07d4b643ac39b9
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# ![](/help/assets/premium.png) PREMIUMEstimate het verkeer dat voor succes wordt vereist

[!DNL Adobe Target] [!UICONTROL Traffic Estimator] verstrekt terugkoppelt die u laat weten of u voldoende verkeer voor uw [!UICONTROL Automated Personalization] activiteit hebt om te slagen.

Omdat een [!UICONTROL Automated Personalization] activiteit veelvoudige aanbiedingscombinaties gebruikt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. [!UICONTROL Traffic Estimator] gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten noodzakelijk om de activiteit succesvol te maken.

[!UICONTROL Traffic Estimator] bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren door de geschatte paginaaimpressies en de typische omzettingspercentage voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Dit proces biedt voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Onthoud dat [!DNL Target] willekeurig ervaringen dient tot de verpersoonlijkingsalgoritmen worden gebouwd. Het pictogram van het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en [!DNL Target] kan beginnen leverend gepersonaliseerde inhoud. Omdat de lift slechts wordt verwacht nadat de modellen klaar zijn, staat de visuele aanwijzing u toe om de juiste verwachting te plaatsen. Gebruik [!UICONTROL Traffic Estimator] in [!UICONTROL Visual Experience Composer] (VEC) om een richtlijn te krijgen van wanneer de modellen klaar zijn.

## De schatter van het Verkeer gebruiken

1. Klik in [!UICONTROL Visual Experience Composer] op **[!UICONTROL Traffic]**.

   ![Verkeerspictogram](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   De [!UICONTROL Traffic Estimator] wordt geopend. U kunt **[!UICONTROL Traffic]** opnieuw klikken om [!UICONTROL Traffic Estimator] te verbergen.

   ![Gebruikersinterface voor verkeersschatting](assets/ap_est.png)

1. Geef de gebruikelijke conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   | Metrisch | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Deze metrische waarde wordt automatisch berekend gebaseerd op het aantal ervaringen die als deel van uw activiteit, na om het even welke uitsluitingen worden gecreeerd. |
   | **[!UICONTROL Typical Conversion Rate]** | Deze maatstaf wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem. |
   | **[!UICONTROL Estimated Visits Per Day]** | Deze maatstaf is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Deze metrische waarde kan worden gebaseerd op de analysegegevens. Dit aantal moet bezoeken zijn, niet unieke bezoekers. |
   | **[!UICONTROL Test Duration]** | Het aantal dagen waarop de activiteit moet worden uitgevoerd. |

   [!UICONTROL Traffic Estimator] gebruikt deze metriek om te bepalen welke aanpassingen noodzakelijk zijn om een succesvolle test in werking te stellen.

   Boven aan [!UICONTROL Traffic Estimator] worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

   ![Verkeersschatting met weergegeven waarden en resultaten](assets/ap_est_no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en de conversiesnelheid en -indrukkingen te laag zijn, geeft [!UICONTROL Traffic Estimator] aan hoe lang de test moet duren om te slagen. Of, als uw verkeer laag is, [!UICONTROL Traffic Estimator] zou een lager aantal aanbiedingscombinaties kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u niet voldoende verkeer hebt, overweeg het volgende:

   * Overweeg een [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) activiteit in plaats van [!UICONTROL Automated Personalization] te gebruiken om ervaringen met verscheidene aanbiedingsveranderingen in één ervaringsvariatie tot stand te brengen.
   * Verminder het aantal aanbiedingscombinaties binnen uw [!UICONTROL Automated Personalization] activiteit.
   * Verhoog de duur van de activiteit.

   Pas de aantallen aan tot [!UICONTROL Traffic Estimator] erop wijst dat u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![Verkeersschatting die voldoende verkeersbericht toont](assets/ap_est_yes.png)

   Als het verkeer voldoende is, toont het [!UICONTROL Traffic] pictogram een groene controle. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.

## Veelgestelde vragen over de schatter van het Verkeer

Overweeg de volgende FAQs aangezien u met [!UICONTROL Traffic Estimator] werkt:

### Waarom bouwt [!DNL Target] geen gepersonaliseerde modellen wanneer mijn AP activiteit genoeg verkeer heeft?

In bepaalde omstandigheden, is uw verkeer groot genoeg voor een gepersonaliseerd model om worden gebouwd, maar dat verkeer zou [!DNL Target] kunnen informeren dat er geen zinvol verschil tussen het gepersonaliseerde model en willekeurig is. Hoewel het model is ingebouwd in [!DNL Target] en getest, wordt het niet geïmplementeerd omdat het model niet beter is dan willekeurig.

Een mogelijke reden waarom het model niet beter dan willekeurig is, zou kunnen zijn dat de aanbiedingen niet verschillend genoeg van elkaar zijn. Als zo, kunt u proberen makend de aanbiedingen visueel verschillend als het overseinen gelijkaardig is, of u kunt proberen veranderend het overseinen zelf.
