---
keywords: ervaring;controle;geautomatiseerde verpersoonlijking;auto-doel
description: Leer hoe u een ervaring selecteert die u als besturingselement wilt gebruiken tijdens het maken van een [!UICONTROL Automated Personalization] (AP) of [!UICONTROL Auto-Target] activiteit in [!DNL Adobe Target].
title: Hoe kan ik een bepaalde ervaring gebruiken als controle in een [!UICONTROL Automated Personalization] Activiteit?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization, Auto-Target
solution: Target,Analytics
exl-id: a0a36ace-3cba-4d8d-9bbd-e35204ff6453
source-git-commit: 29f8c19e24443e84b8d900f630495d163530f80e
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Selecteer het besturingselement voor uw [!UICONTROL Automated Personalization] of [!UICONTROL Auto-Target] activiteit

U kunt een willekeurig bediende ervaring selecteren of een specifieke ervaring die als controle moet worden gebruikt terwijl het creëren van een [[!UICONTROL Automated Personalization]](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het controleverkeer aan de relevante ervaringen leiden, die op het percentage van de verkeerstoewijzing worden gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die controle dan evalueren.

De opties voor het instellen van een besturingselement in [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] de activiteiten verschillen enigszins van andere soorten activiteiten . In een handleiding [!UICONTROL A/B Test], kunt u veranderen wat het melden toont aangezien uw controle, en de lift wordt berekend gebaseerd op het omzettingspercentage van die controleervaring. U kunt deze verandering gemakkelijk maken omdat het verkeer willekeurig aan elk van de ervaringen wordt gediend u in uw activiteit omvatte, geen kwestie wat de controle aanvankelijk aan wordt geplaatst. Met andere woorden, het selecteren van de controle beïnvloedt niet hoe het verkeer wordt gediend. In [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] activiteiten, uw besluit over wat te kiezen aangezien de controle beïnvloedt hoe het bezoekersverkeer wordt gediend. Daarom moet u uw beslissing zorgvuldiger overwegen.

Er zijn twee opties beschikbaar voor uw besturing in uw [!UICONTROL Automated Personalization] en [!UICONTROL Auto-Target] activiteiten:

* **willekeurig bediend**: Voor een willekeurige controle, dient het controlepercentage van verkeer willekeurig alle ervaringen in de activiteit, zonder het profiel van die bezoeker te overwegen. U kunt de controle zien als een handig antwoord op de vraag: &quot;Als ik alleen een willekeurige ervaring (of aanbieding) aan bezoekers betaal en geen rekening houdt met hun profielen, wat is dan de conversiekoers voor die ervaring (of die aanbieding)?&quot; De controle is als een [!UICONTROL A/B Test] binnen uw AI-activiteit. Deze informatie over de niet-gepersonaliseerde omrekeningskoers voor elke ervaring of aanbieding kan nuttig zijn om te begrijpen wanneer het analyseren van uw activiteitenresultaten.

* **Specifieke ervaring**: Een specifieke ervaringscontrole laat u uw verkeer vergelijken dat door wordt gediend [!DNL Target] personalisatiemodellen aan een specifieke marketer-bepaalde ervaring (bijvoorbeeld, uw standaardhomepage). Met deze optie, dient het controlepercentage van verkeer willekeurig verkeer voor slechts die één ervaring.

## Een specifieke ervaring opgeven als besturingselement

1. Terwijl u een [[!UICONTROL Automated Personalization] activiteit](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) of [[!UICONTROL Auto-Target] activiteit](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configureert u de ervaringen naar wens.
1. Op de [!UICONTROL Targeting] pagina (stap 2 van de geleide workflow met drie delen), selecteert u de gewenste ervaring als het besturingselement.
1. Specificeer de gewenste verkeerstoewijzing voor de controleervaring en de andere ervaringen.

   Voor een specifieke ervaringscontrole wordt 10% tot 30% aanbevolen.

1. Doorgaan met de [!UICONTROL Goals & Settings] pagina.

## Bekende beperkingen en overwegingen

Houd rekening met de volgende punten wanneer u een specifieke ervaring als besturingselement gebruikt:

* Het wordt niet aangeraden de besturingservaring in een bestaande activiteit te wijzigen. De meest recente geselecteerde ervaring met besturingselementen wordt vermeld in de rapportage (zelfs als oudere rapporten zijn gebaseerd op een andere ervaring).
* Het wordt niet aangeraden de besturingservaring te verwijderen.
* Het toevoegen van vele nieuwe aanbiedingen of ervaringen aan een levende activiteit met een specifieke ervaring aangezien de controle niet wordt geadviseerd.
* In [!UICONTROL Automated Personalization] activiteiten, waaronder het richten op de controleervaring die verder kan beperken wie kan zien dat de ervaring niet wordt geadviseerd.
* In [!UICONTROL Automated Personalization] activiteiten, lift- en vertrouwensinformatie is *NOT* beschikbaar in het verslag op aanbodniveau als een specifieke ervaring is geselecteerd. De informatie van het optillen en van het vertrouwen is beschikbaar bij het algemene &quot;gerichte&quot;versus &quot;controle&quot;verkeersniveau voor [!UICONTROL Automated Personalization] activiteit. Informatie over optillen en vertrouwen is beschikbaar als &quot;willekeurig&quot; is geselecteerd als het besturingselement. Dit verschil komt doordat het vergelijken van de conversiekoers van een specifieke ervaring met de conversiekoers van een aanbieding niet logisch is vanwege het verschil in eenheden. De informatie die beschikbaar is in een [!UICONTROL Auto-Target] activiteit is het zelfde, ongeacht welk type van controle wordt geselecteerd.
* Omdat al controleverkeer naar één enkele ervaring of reeks aanbiedingen gaat wanneer u de ervaring als controle selecteert (in vergelijking met willekeurig, waar de hoeveelheid controleverkeer over het aantal ervaringen of aanbiedingen in uw activiteit wordt verdeeld), hebt u over het algemeen niet zo veel verkeer aan de controle nodig. 10% is een goede startplaats.
* Als u één van het volgende aan een levende activiteit met een specifieke ervaring als controle doet, wordt de controle automatisch teruggesteld aan willekeurig gediende ervaringen (in plaats van de eerder geselecteerde specifieke ervaring):

   * Een ervaring verwijderen
   * Een locatie of aanbieding verwijderen ([!UICONTROL Automated Personalization] alleen)
   * Een ervaring handmatig uitsluiten via dubbele aanbiedingen verwijderen of via een uitsluitingsgroep ([!UICONTROL Automated Personalization] alleen)
