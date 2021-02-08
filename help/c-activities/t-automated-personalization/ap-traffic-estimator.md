---
keywords: verkeersraming;geautomatiseerde personalisatie;ap;schatting van verkeer
description: Leer hoe u de Verkeersschatter gebruikt die u laat weten of u voldoende verkeer hebt om uw Adobe Target Automated Personalization-activiteit te laten slagen.
title: Hoeveel verkeer is er nodig voor een Automated Personalization-activiteit?
feature: Automated Personalization
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMEstimate het verkeer dat voor succes wordt vereist

[!UICONTROL Traffic Estimator] verstrekt terugkoppelt die u laat weten of u voldoende verkeer voor uw [!DNL Adobe Target] activiteit hebt om te slagen.

Omdat een [!UICONTROL Automated Personalization] activiteit veelvoudige aanbiedingscombinaties gebruikt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. [!UICONTROL Traffic Estimator] gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de activiteit succesvol te maken.

[!UICONTROL Traffic Estimator] bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren, door de geschatte paginaaimpressies en de typische omzettingspercentage voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Hierdoor is er voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Onthoud dat [!DNL Target] willekeurig ervaringen dient tot de verpersoonlijkingsalgoritmen worden gebouwd. Het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en [!DNL Target] kan beginnen leverend gepersonaliseerde inhoud. Omdat de lift slechts wordt verwacht nadat de modellen klaar zijn, staat de visuele aanwijzing u toe om de juiste verwachting te plaatsen. Gebruik [!UICONTROL Traffic Estimator] in [!UICONTROL Visual Experience Composer] (VEC) om een richtlijn te krijgen van wanneer de modellen klaar zullen zijn.

## De schatter van het Verkeer gebruiken

1. Klik in [!UICONTROL Visual Experience Composer] op **[!UICONTROL Traffic]**.

   ![Verkeerspictogram](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   De [!UICONTROL Traffic Estimator] wordt geopend. U kunt **[!UICONTROL Traffic]** opnieuw klikken om [!UICONTROL Traffic Estimator] te verbergen.

   ![](assets/ap_est.png)

1. Geef de gemiddelde conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   * **Aantal voorstellen**: Automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * **Typische conversiesnelheid**: De omrekeningskoers wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem.
   * **Geschatte bezoeken per dag**: Dit is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Dit kan op uw analysegegevens worden gebaseerd. Dit nummer moet bezoeken zijn en geen unieke bezoekers.
   * **Testduur**: Het aantal dagen waarop de activiteit moet worden uitgevoerd.

   [!UICONTROL Traffic Estimato]r gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Boven aan [!UICONTROL Traffic Estimator] worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

   ![](assets/ap_est_no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en uw conversiesnelheid en -indrukkingen te laag zijn, toont [!UICONTROL Traffic Estimator] hoe lang de test moet duren om te slagen. Of, als uw verkeer laag is, [!UICONTROL Traffic Estimator] zou een lager aantal aanbiedingscombinaties kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren:

   * Overweeg een [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) activiteit in plaats van [!UICONTROL Automated Personalization] te gebruiken om ervaringen met verscheidene aanbiedingsveranderingen in één ervaringsvariatie tot stand te brengen.
   * Verminder het aantal aanbiedingscombinaties binnen uw [!UICONTROL Automated Personalization] activiteit.
   * Verhoog de duur van de activiteit.

   Pas de aantallen aan tot [!UICONTROL Traffic Estimator] zegt u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![](assets/ap_est_yes.png)

   Als het verkeer voldoende is, toont het [!UICONTROL Traffic] pictogram een groene controle. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.

## Veelgestelde vragen over de schatter van het Verkeer

Overweeg de volgende FAQs aangezien u met [!UICONTROL Traffic Estimator] werkt:

### Waarom bouwt [!DNL Target] geen gepersonaliseerde modellen wanneer mijn AP activiteit genoeg verkeer heeft?

In bepaalde omstandigheden, zou uw verkeer groot genoeg voor een gepersonaliseerd model kunnen zijn om worden gebouwd, maar dat verkeer zou [!DNL Target] kunnen informeren dat er geen zinvol verschil tussen het gepersonaliseerde model en willekeurig is. Hoewel het model is ingebouwd in [!DNL Target] en is getest, wordt het niet geïmplementeerd omdat het model niet significant beter is dan willekeurig.

Een mogelijke reden waarom het model niet beter dan willekeurig is, kan zijn dat de aanbiedingen niet significant van elkaar verschillen. Als dit het geval is, kunt u proberen makend de aanbiedingen visueel verschillend als het overseinen gelijkaardig is, of u kunt proberen veranderend het overseinen zelf.
