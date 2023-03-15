---
keywords: verkeersschatting;geautomatiseerde personalisatie;ap;schatting van verkeer;auto-target
description: De Adobe gebruiken [!DNL Target] Verkeersschatting om te bepalen of je voldoende verkeer hebt om je Automated Personalization-activiteit te laten slagen.
title: Hoeveel verkeer is nodig voor een succesvolle activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# Schatting van het verkeer dat voor succes wordt vereist

De [!DNL Adobe Target] [!UICONTROL Traffic Estimator] verstrekt terugkoppelt die u laat weten of u voldoende verkeer voor uw hebt [!UICONTROL Automated Personalization] activiteit om te slagen.

Omdat [!UICONTROL Automated Personalization] de activiteit gebruikt veelvoudige aanbiedingscombinaties, is het belangrijk om te weten hoeveel verkeer wordt vereist om zinvolle resultaten te verstrekken. De [!UICONTROL Traffic Estimator] gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten noodzakelijk om de activiteit succesvol te maken.

De [!UICONTROL Traffic Estimator] bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren door de geschatte paginaamafbeeldingen en de typische omzettingspercentage voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Dit proces biedt voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Vergeet niet dat [!DNL Target] dient willekeurig ervaringen tot de verpersoonlijkingsalgoritmen worden gebouwd. Het pictogram van het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en [!DNL Target] kan beginnen met het leveren van gepersonaliseerde inhoud. Omdat de lift slechts wordt verwacht nadat de modellen klaar zijn, staat de visuele aanwijzing u toe om de juiste verwachting te plaatsen. Gebruik de [!UICONTROL Traffic Estimator] in de [!UICONTROL Visual Experience Composer] (VEC) om een richtlijn te krijgen over wanneer de modellen klaar zijn.

## De schatter van het Verkeer gebruiken

1. Van de [!UICONTROL Visual Experience Composer], klikt u op **[!UICONTROL Traffic]**.

   ![Verkeerspictogram](/help/main/c-activities/t-automated-personalization/assets/icon-traffic.png)

   De [!UICONTROL Traffic Estimator] wordt geopend. U kunt op **[!UICONTROL Traffic]** opnieuw om de [!UICONTROL Traffic Estimator].

   ![Gebruikersinterface voor verkeersschatting](assets/ap_est.png)

1. Geef de gebruikelijke conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   | Metrisch | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Deze metrische waarde wordt automatisch berekend gebaseerd op het aantal ervaringen die als deel van uw activiteit, na om het even welke uitsluitingen worden gecreeerd. |
   | **[!UICONTROL Typical Conversion Rate]** | Deze maatstaf wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem. |
   | **[!UICONTROL Estimated Visits Per Day]** | Deze maatstaf is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Deze metrische waarde kan worden gebaseerd op de analysegegevens. Dit aantal moet bezoeken zijn, niet unieke bezoekers. |
   | **[!UICONTROL Test Duration]** | Het aantal dagen waarop de activiteit moet worden uitgevoerd. |

   De [!UICONTROL Traffic Estimator] gebruikt deze metriek om te bepalen welke aanpassingen noodzakelijk zijn om een succesvolle test in werking te stellen.

   Boven aan [!UICONTROL Traffic Estimator]De ingevoerde waarden worden berekend en de resultaten worden weergegeven.

   ![Verkeersschatting met weergegeven waarden en resultaten](assets/ap_est_no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en de conversiesnelheid en -indrukkingen te laag zijn, worden de [!UICONTROL Traffic Estimator] toont hoe lang de test moet lopen om succesvol te zijn. Of, als uw verkeer laag is, [!UICONTROL Traffic Estimator] U kunt een lager aantal aanbiedingscombinaties voorstellen, zodat u de test het gewenste aantal dagen kunt uitvoeren.

   Als u niet voldoende verkeer hebt, overweeg het volgende:

   * Overweeg een [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteit in plaats van [!UICONTROL Automated Personalization] om ervaringen te creëren met verschillende aanbiedingen die veranderen in één ervaringsvariatie.
   * Verminder het aantal aanbiedingscombinaties binnen uw [!UICONTROL Automated Personalization] activiteit.
   * Verhoog de duur van de activiteit.

   Pas de getallen aan tot de [!UICONTROL Traffic Estimator] wijst erop dat u voldoende verkeer hebt, dan ontwerp uw test dienovereenkomstig.

   ![Verkeersschatting die voldoende verkeersbericht toont](assets/ap_est_yes.png)

   Als het verkeer toereikend is, [!UICONTROL Traffic] wordt een groene controle weergegeven. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.

## Veelgestelde vragen over de schatter van het Verkeer

Neem de volgende veelgestelde vragen in overweging wanneer u met de [!UICONTROL Traffic Estimator]:

### Waarom worden gepersonaliseerde modellen niet gebouwd alhoewel mijn AP activiteit genoeg verkeer heeft?

In bepaalde omstandigheden is uw verkeer groot genoeg voor een gepersonaliseerd model om worden gebouwd, maar dat verkeer kon informeren [!DNL Target] dat er geen zinvol verschil is tussen het gepersonaliseerde model en het willekeurige model. Hoewel het model is ingebouwd [!DNL Target] en getest, wordt het niet opgesteld omdat het model niet beter dan willekeurig is.

Een mogelijke reden waarom het model niet beter dan willekeurig is, zou kunnen zijn dat de aanbiedingen niet verschillend genoeg van elkaar zijn. Als zo, kunt u proberen makend de aanbiedingen visueel verschillend als het overseinen gelijkaardig is, of u kunt proberen veranderend het overseinen zelf.
