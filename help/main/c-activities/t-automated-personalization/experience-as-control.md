---
keywords: ervaring;controle;geautomatiseerde verpersoonlijking;auto-doel
description: Leer hoe te om een ervaring te selecteren die als controle moet worden gebruikt terwijl het creëren van een [!UICONTROL Automated Personalization] (AP) of [!UICONTROL Auto-Target] activiteit in  [!DNL Adobe Target].
title: Hoe kan ik een specifieke ervaring als controle in een [!UICONTROL Automated Personalization] activiteit gebruiken?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Selecteer het besturingselement voor uw [!UICONTROL Automated Personalization] - of [!UICONTROL Auto-Target] -activiteit

U kunt een willekeurig bediende ervaring of een specifieke ervaring selecteren die als controle moet worden gebruikt terwijl het creëren van een [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het controleverkeer aan de relevante ervaringen leiden, die op het percentage van de verkeerstoewijzing worden gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die controle dan evalueren.

De opties voor het instellen van een besturingselement in [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten verschillen enigszins van andere typen activiteiten. In een handleiding [!UICONTROL A/B Test] kunt u wijzigen wat er in de rapportage wordt weergegeven terwijl u het besturingselement gebruikt en wordt de lift berekend op basis van de conversiesnelheid van dat besturingselement. U kunt deze verandering gemakkelijk maken omdat het verkeer willekeurig aan elk van de ervaringen wordt gediend u in uw activiteit omvatte, geen kwestie wat de controle aanvankelijk aan wordt geplaatst. Met andere woorden, het selecteren van de controle beïnvloedt niet hoe het verkeer wordt gediend. Bij [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten is uw beslissing over wat u wilt kiezen als besturingselement wel van invloed op de manier waarop het bezoekersverkeer wordt uitgevoerd. Daarom moet u uw beslissing zorgvuldiger overwegen.

Er zijn twee opties beschikbaar voor uw besturing in uw [!UICONTROL Automated Personalization] - en [!UICONTROL Auto-Target] -activiteiten:

* **willekeurig gediend**: Voor een willekeurige controle, dient het controlepercentage van verkeer willekeurig alle ervaringen in de activiteit, zonder het profiel van die bezoeker te overwegen. U kunt de controle zien als een handig antwoord op de vraag: &quot;Als ik alleen een willekeurige ervaring (of aanbieding) aan bezoekers betaal en geen rekening houdt met hun profielen, wat is dan de conversiekoers voor die ervaring (of die aanbieding)?&quot; Het besturingselement is een soort [!UICONTROL A/B Test] binnen uw AI-activiteit. Deze informatie over de niet-gepersonaliseerde omrekeningskoers voor elke ervaring of aanbieding kan nuttig zijn om te begrijpen wanneer het analyseren van uw activiteitenresultaten.

* **Specifieke ervaring**: Een specifieke ervaringscontrole laat u uw verkeer vergelijken dat door [!DNL Target] wordt gediend verpersoonlijkingsmodellen aan een specifieke marketer-bepaalde ervaring (bijvoorbeeld, uw standaardhomepage). Met deze optie, dient het controlepercentage van verkeer willekeurig verkeer voor slechts die één ervaring.

## Een specifieke ervaring opgeven als besturingselement

1. Tijdens het creëren van of het uitgeven van een [[!UICONTROL Automated Personalization] activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) of [[!UICONTROL Auto-Target] activiteit &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), vorm de ervaringen zoals gewenst.
1. Klik op de pagina [!UICONTROL Targeting] (stap 2 van de geleide workflow met drie delen) op de besturingservaring om [!UICONTROL Control] -opties weer te geven in het rechterdeelvenster.

   ![&#x200B; ruit van de Controle &#x200B;](/help/main/c-activities/t-automated-personalization/assets/control.png)

1. Selecteer [!UICONTROL Control] in de vervolgkeuzelijst [!UICONTROL Random Experience] of selecteer de gewenste ervaring die u voor het besturingselement wilt gebruiken.

1. Klik de [!UICONTROL Traffic Allocation] controle, dan specificeer de gewenste verkeerstoewijzing voor de controleervaring en de andere ervaringen.

   ![&#x200B; spoorstaaf van de Verkeerstoewijzing van het Verkeer &#x200B;](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation.png)

   Voor een specifieke ervaringscontrole wordt 10% tot 30% aanbevolen.

1. Ga verder met de pagina [!UICONTROL Goals & Settings] .

## Bekende beperkingen en overwegingen

Houd rekening met de volgende punten wanneer u een specifieke ervaring als besturingselement gebruikt:

* Het wordt niet aangeraden de besturingservaring in een bestaande activiteit te wijzigen. De meest recente geselecteerde ervaring met besturingselementen wordt vermeld in de rapportage (zelfs als oudere rapporten zijn gebaseerd op een andere ervaring).
* Het wordt niet aangeraden de besturingservaring te verwijderen.
* Het toevoegen van vele nieuwe aanbiedingen of ervaringen aan een levende activiteit met een specifieke ervaring aangezien de controle niet wordt geadviseerd.
* Bij [!UICONTROL Automated Personalization] -activiteiten, waaronder het activeren op de ervaring met besturingselementen die de gebruiker nog meer beperkingen kunnen opleggen om te zien dat deze ervaring niet wordt aangeraden.
* In [!UICONTROL Automated Personalization] activiteiten, wordt de lift en vertrouwelijkheidsinformatie *NIET* beschikbaar in het aanbieding-vlakke rapport als een specifieke ervaring wordt geselecteerd. Informatie over optillen en vertrouwen is beschikbaar op het algemene verkeersniveau &quot;gericht&quot; versus &quot;controle&quot; voor de [!UICONTROL Automated Personalization] -activiteit. Informatie over optillen en vertrouwen is beschikbaar als &quot;willekeurig&quot; is geselecteerd als het besturingselement. Dit verschil komt doordat het vergelijken van de conversiekoers van een specifieke ervaring met de conversiekoers van een aanbieding niet logisch is vanwege het verschil in eenheden. De informatie die beschikbaar is in een [!UICONTROL Auto-Target] -activiteit is gelijk, ongeacht het type besturingselement dat is geselecteerd.
* Omdat al controleverkeer naar één enkele ervaring of reeks aanbiedingen gaat wanneer u de ervaring als controle selecteert (in vergelijking met willekeurig, waar de hoeveelheid controleverkeer over het aantal ervaringen of aanbiedingen in uw activiteit wordt verdeeld), hebt u over het algemeen niet zo veel verkeer aan de controle nodig. 10% is een goede startplaats.
* Als u één van het volgende aan een levende activiteit met een specifieke ervaring als controle doet, wordt de controle automatisch teruggesteld aan willekeurig gediende ervaringen (in plaats van de eerder geselecteerde specifieke ervaring):

   * Een ervaring verwijderen
   * Een locatie of aanbieding verwijderen ([!UICONTROL Automated Personalization] alleen)
   * Een ervaring handmatig uitsluiten via dubbele aanbiedingen verwijderen of via een uitsluitingsgroep ([!UICONTROL Automated Personalization] only)
