---
description: De schatter van het Verkeer verstrekt terugkoppelt die u laat weten of u voldoende verkeer voor uw activiteit hebt om te slagen.
title: Schatting van het verkeer dat voor succes wordt vereist
topic: Standard
uuid: 9961ebaa-8761-431d-9605-852025ca580f
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# ![PREMIUM](/help/assets/premium.png) Schat het verkeer dat voor succes wordt vereist{#estimate-the-traffic-required-for-success}

De schatter van het Verkeer verstrekt terugkoppelt die u laat weten of u voldoende verkeer voor uw activiteit hebt om te slagen.

Omdat een Geautomatiseerde activiteit van de Personalisatie veelvoudige aanbiedingscombinaties gebruikt, is het belangrijk om te weten hoeveel verkeer wordt vereist om betekenisvolle resultaten te verstrekken. De schatter van het Verkeer gebruikt statistieken over uw pagina en het aantal ervaringen die worden getest om de hoeveelheid verkeer en de testduur te schatten nodig om de activiteit succesvol te maken.

De schatter van het Verkeer bepaalt als er genoeg verkeer is om gepersonaliseerde modellen te produceren, door de geschatte paginaaimpressies en de typische omzettingspercentage voor de pagina&#39;s te vergelijken. In het ideale geval zorgt de juiste voorbeeldgrootte voor een geslaagde activiteit ervoor dat gepersonaliseerde inhoud binnen 50% van de activiteitsperiode of 14 dagen gereed is, afhankelijk van welke datum het minst is. Hierdoor is er voldoende tijd om persoonlijke inhoud te verkrijgen en te leren welke inhoud moet worden geleverd.

Herinner dat Doel willekeurig ervaringen dient tot de verpersoonlijkingsalgoritmen worden gebouwd. Het vinkje naast elke aanbieding toont wanneer het model voor die aanbieding klaar is en Target kan beginnen met het leveren van gepersonaliseerde inhoud. Omdat de lift slechts wordt verwacht nadat de modellen klaar zijn, staat de visuele aanwijzing u toe om de juiste verwachting te plaatsen. Gebruik de verkeersschatter in Visual Experience Composer (VEC) om een richtlijn te krijgen van wanneer de modellen klaar zullen zijn.

1. Klik op Composer ervaring **[!UICONTROL Traffic]**.

   ![Verkeerspictogram](/help/c-activities/t-automated-personalization/assets/icon-traffic.png)

   De schatter van het Verkeer opent. U kunt **[!UICONTROL Traffic]** opnieuw klikken om de schatter van het Verkeer te verbergen.

   ![](assets/ap_est.png)

1. Geef de gemiddelde conversiesnelheid (of de conversiesnelheid die u van deze activiteit verwacht), de geschatte activiteitsimpressies per dag en de testduur op.

   * Aantal inhoudscombinaties: Automatisch berekend op basis van het aantal ervaringen dat wordt gemaakt als onderdeel van uw activiteit na eventuele uitsluitingen.
   * Typische conversiesnelheid: De omrekeningskoers wordt uitgedrukt als een percentage, op basis van uw schatting of gegevens uit het verleden van uw analysesysteem.
   * Geschatte bezoeken per dag: Dit is het aantal bezoeken per dag van bezoekers die de activiteit kunnen bekijken, op basis van de doelcriteria. Dit kan op uw analysegegevens worden gebaseerd. Dit nummer moet bezoeken zijn en geen unieke bezoekers.
   * Duur test: Het aantal dagen waarop de activiteit moet worden uitgevoerd.
   De schatter van het Verkeer gebruikt deze statistieken om te bepalen welke aanpassingen nodig zijn om een succesvolle test in werking te stellen.

   Vlak bij de bovenkant van de schatter van het Verkeer, worden de waarden u inging berekend en de resultaten worden getoond.

   ![](assets/ap_est_no.png)

   Terwijl u de getallen wijzigt, verandert de schatting. Als u bijvoorbeeld een groot aantal combinaties test en uw conversiesnelheid en indrukken te laag zijn, toont de Verkeersschatting hoe lang de test moet duren om succesvol te zijn. Of, als uw verkeer laag is, zou de schatter van het Verkeer een lager aantal aanbiedingscombinaties kunnen voorstellen zodat kunt u de test het gewenste aantal dagen in werking stellen.

   Als u onvoldoende verkeer hebt, kunt u een van de volgende handelingen uitvoeren:

   * Overweeg Auto-Doel in plaats van Geautomatiseerde Personalisatie te gebruiken om ervaringen met verscheidene aanbiedingsveranderingen in één ervaringsvariatie tot stand te brengen.
   * Verminder het aantal aanbiedingscombinaties binnen uw Geautomatiseerde Personaliseringsactiviteit.
   * Verhoog de duur van de activiteit.
   Pas de aantallen aan tot de schatter van het Verkeer zegt u voldoende verkeer hebt, dan ontwerp dienovereenkomstig uw test.

   ![](assets/ap_est_yes.png)

   Als het verkeer voldoende is, toont het pictogram van het Verkeer een groene controle. Als dit niet voldoende is, wordt een rood waarschuwingslabel weergegeven.
