---
keywords: verkeersraming;geautomatiseerde personalisatie;ap;schatting van verkeer
description: Gebruik [!UICONTROL Traffic Estimator] om te beoordelen of u voldoende verkeer hebt om een [!UICONTROL Automated Personalization] -activiteit te laten slagen.
title: Hoeveel verkeer is nodig voor een succesvolle [!UICONTROL Automated Personalization] activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
exl-id: 11f9e239-700b-45cd-bf77-39f7f8967a2e
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Schatting van het verkeer dat voor succes wordt vereist

[!DNL Adobe Target] [!UICONTROL Traffic Estimator] verstrekt terugkoppelen die u laat weten of u voldoende verkeer voor uw [!UICONTROL Automated Personalization] (AP) activiteit hebt om te slagen.

Omdat [!UICONTROL Automated Personalization] de activiteiten veelvoudige aanbiedingscombinaties gebruiken, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. [!UICONTROL Traffic Estimator] gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten noodzakelijk om de activiteit succesvol te maken.

[!UICONTROL Traffic Estimator] bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren door de geschatte paginaaimpressies en de typische omzettingssnelheid voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Dit proces biedt voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Vergeet niet dat [!DNL Target] op willekeurige wijze ervaringen oplevert totdat de verpersoonlijkingsalgoritmen zijn gemaakt. Het pictogram van het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en [!DNL Target] kan beginnen leverend gepersonaliseerde inhoud. Omdat de lift pas wordt verwacht nadat de modellen klaar zijn, kunt u met de visuele indicatie de juiste verwachting instellen. Gebruik [!UICONTROL Traffic Estimator] in [!UICONTROL Visual Experience Composer] (VEC) om een richtlijn te krijgen over wanneer de modellen klaar zijn.

## De schatter van het Verkeer gebruiken

1. Van de [!UICONTROL Experiences] pagina van [!UICONTROL Visual Experience Composer] in een [!UICONTROL Automated Personalization] activiteit, klik het **[!UICONTROL Traffic]** pictogram ( ![&#x200B; pictogram van de Schatter van het Verkeer &#x200B;](/help/main/assets/icons/Gauge2.svg)) in de hoogste linkerhoek van de [!UICONTROL Experiences] pagina.

   De lus [!UICONTROL Traffic Estimator] wordt geopend.

   ![&#x200B; het gebruikersinterface van de schatter van het Verkeer &#x200B;](assets/ap-est.png)

   U kunt opnieuw op het pictogram klikken om de [!UICONTROL Traffic Estimator] te verbergen.

1. Geef de gebruikelijke conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   | Metrisch | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Number of Offers]** | Deze metrische waarde wordt automatisch berekend gebaseerd op het aantal ervaringen die als deel van uw activiteit, na om het even welke uitsluitingen worden gecreeerd. |
   | **[!UICONTROL Typical Conversion Rate]** | Deze maatstaf wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem. |
   | **[!UICONTROL Estimated Visits Per Day]** | Deze maatstaf is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Deze metrische waarde kan worden gebaseerd op de analysegegevens. Dit aantal moet bezoeken zijn, niet unieke bezoekers. |
   | **[!UICONTROL Test Duration]** | Het aantal dagen waarop de activiteit moet worden uitgevoerd. |

   [!UICONTROL Traffic Estimator] gebruikt deze metriek om te bepalen welke aanpassingen noodzakelijk zijn om een succesvolle test in werking te stellen.

   Boven aan de [!UICONTROL Traffic Estimator] worden de ingevoerde waarden berekend en worden de resultaten weergegeven.

   ![&#x200B; Schatting van het Verkeer met getoonde waarden en resultaten &#x200B;](assets/ap-est-no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en de conversiesnelheid en -indrukkingen te laag zijn, geeft de [!UICONTROL Traffic Estimator] aan hoe lang de test moet duren om te slagen. Als uw verkeer laag is, kan [!UICONTROL Traffic Estimator] een lager aantal aanbiedingscombinaties voorstellen zodat u de test het gewenste aantal dagen kunt uitvoeren.

   Als u niet voldoende verkeer hebt, overweeg het volgende:

   * U kunt een [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteit in plaats van [!UICONTROL Automated Personalization] gebruiken om ervaringen te maken met verschillende wijzigingen in de aanbieding in één ervaringsvariatie.
   * Verminder het aantal aanbiedingscombinaties binnen uw [!UICONTROL Automated Personalization] activiteit.
   * Verhoog de duur van de activiteit.

   Pas de getallen aan totdat [!UICONTROL Traffic Estimator] aangeeft dat u voldoende verkeer hebt en stel vervolgens de test dienovereenkomstig in.

   ![&#x200B; die de schatter van het Verkeer voldoende verkeersbericht &#x200B;](assets/ap-est-yes.png) toont

   Als het verkeer voldoende is, wordt op het pictogram [!UICONTROL Traffic] een groene controle weergegeven. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.

## Veelgestelde vragen over de schatter van het Verkeer

Houd rekening met de volgende veelgestelde vragen wanneer u met de [!UICONTROL Traffic Estimator] werkt:

### Waarom worden gepersonaliseerde modellen niet gebouwd alhoewel mijn AP activiteit genoeg verkeer heeft?

In bepaalde omstandigheden is uw verkeer groot genoeg voor de bouw van een gepersonaliseerd model, maar dat verkeer zou [!DNL Target] kunnen informeren dat er geen zinvol verschil tussen het gepersonaliseerde model en willekeurig is. Hoewel het model is ingebouwd in [!DNL Target] en getest, wordt het niet geïmplementeerd omdat het model niet beter is dan willekeurig.

Een mogelijke reden waarom het model niet beter dan willekeurig is, zou kunnen zijn dat de aanbiedingen niet verschillend genoeg van elkaar zijn. Als zo, kunt u proberen makend de aanbiedingen visueel verschillend als het overseinen gelijkaardig is, of u kunt proberen veranderend het overseinen zelf.
