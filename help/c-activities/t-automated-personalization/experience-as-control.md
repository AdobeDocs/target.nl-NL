---
keywords: experience;control;automated personalization;auto-target
description: Selecteer een ervaring die u als besturingselement wilt gebruiken tijdens het maken van een Automated Personalization- (AP) of Auto-Target-activiteit in Adobe Target.
title: Een specifieke ervaring gebruiken als controle in Adobe Target
feature: ap
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMSselecteer het besturingselement voor uw Automated Personalization- of Auto-Target-activiteit

U kunt een willekeurig bediende ervaring selecteren of een specifieke ervaring die als controle moet worden gebruikt terwijl het creëren van een [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) of [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md) (AT) activiteit.

Deze eigenschap laat u het controleverkeer aan de relevante ervaringen leiden, die op het percentage van de verkeerstoewijzing worden gebaseerd dat in de activiteit wordt gevormd. U kunt de prestatiesrapporten van het gepersonaliseerde verkeer tegen controleverkeer aan die controle dan evalueren.

De opties voor het instellen van een besturingselement in AP- en AT-activiteiten wijken af van andere soorten activiteit. In een handmatige A/B Test, kunt u veranderen wat het melden als uw controle toont, en de lift wordt berekend gebaseerd op de omrekeningssnelheid van die controleervaring. U kunt deze verandering gemakkelijk maken omdat het verkeer willekeurig aan elk van de ervaringen wordt gediend u in uw activiteit omvatte, geen kwestie wat de controle aanvankelijk aan wordt geplaatst. Met andere woorden, het selecteren van het besturingselement heeft geen invloed op de manier waarop het verkeer wordt weergegeven. In AP en bij activiteiten, beïnvloedt uw besluit wat om als controle te kiezen hoe het bezoekersverkeer wordt gediend. Als gevolg daarvan moet u zorgvuldiger nadenken over uw beslissing.

Er zijn twee opties beschikbaar voor uw controle in uw AP en bij activiteiten: willekeurig bediende ervaringen of een specifieke ervaring.

* **Willekeurig geserveerd**: Voor een willekeurige controle, dient het controlepercentage van verkeer willekeurig alle ervaringen in de activiteit, zonder het profiel van die bezoeker te overwegen. U kunt de controle beschouwen als een handig antwoord op de vraag: &quot;Als ik alleen een willekeurige ervaring (of aanbieding) voor bezoekers betaal en geen rekening houd met hun profielen, wat is de conversiekoers voor die ervaring (of die aanbieding)?&quot; Het besturingselement is vergelijkbaar met een A/B-test binnen uw AI-activiteit. Deze informatie over de niet-gepersonaliseerde omrekeningskoers voor elke ervaring of aanbieding kan nuttig zijn om te begrijpen wanneer het analyseren van uw activiteitenresultaten.

* **Specifieke ervaring**: Een specifieke ervaringscontrole laat u uw verkeer vergelijken dat door de verpersoonlijkingsmodellen van het Doel wordt gediend aan een specifieke marketer-bepaalde ervaring (bijvoorbeeld, uw standaardhomepage). Met deze optie, dient het controlepercentage van verkeer willekeurig verkeer voor slechts die één ervaring.

## Een specifieke ervaring opgeven als besturingselement

1. Tijdens het creëren van een [AP activiteit](/help/c-activities/t-automated-personalization/create-ap-activity.md) of [AT activiteit](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), vorm de ervaringen zoals gewenst.
1. Selecteer op de pagina [!UICONTROL Targeting] (stap 2 van de geleide workflow met drie delen) de gewenste ervaring als besturingselement.
1. Specificeer de gewenste verkeerstoewijzing voor de controleervaring en de andere ervaringen.

   Voor een specifieke controle wordt 10% tot 30% aanbevolen.

1. Ga verder met de pagina [!UICONTROL Goals & Settings].

## Bekende beperkingen en overwegingen

Houd rekening met de volgende punten wanneer u een specifieke ervaring als controle gebruikt:

* Het wordt niet aangeraden de besturingservaring in een bestaande activiteit te wijzigen. De meest recente geselecteerde ervaring met besturingselementen wordt vermeld in de rapportage (zelfs als oudere rapporten zijn gebaseerd op een andere ervaring).
* Het wordt niet aangeraden de besturingservaring te verwijderen.
* Het toevoegen van een groot aantal nieuwe aanbiedingen/ervaringen aan een levende activiteit met een specifieke ervaring aangezien de controle niet wordt geadviseerd.
* In AP activiteiten, met inbegrip van het richten op de controleervaring die kan verder beperken wie kan zien dat de ervaring niet wordt geadviseerd.
* Bij AP-activiteiten is informatie over optillen en vertrouwen *NOT* beschikbaar in het rapport op aanbodniveau als een specifieke ervaring is geselecteerd. Informatie over optillen en vertrouwen is beschikbaar bij de algemene &quot;gerichte&quot; vs. &quot;controle&quot;verkeersniveau voor de AP activiteit. Informatie over optillen en vertrouwen is beschikbaar als &quot;willekeurig&quot; is geselecteerd als het besturingselement. Dit verschil komt doordat het vergelijken van de conversiekoers van een specifieke ervaring met de conversiekoers van een aanbieding niet logisch is vanwege het verschil in eenheden. De informatie beschikbaar in een activiteit van AT is het zelfde, ongeacht welk type van controle wordt geselecteerd.
* Omdat al controleverkeer naar één enkele ervaring of reeks aanbiedingen gaat wanneer u de ervaring als controle selecteert (in vergelijking met willekeurig, waar de hoeveelheid controleverkeer over het aantal ervaringen of aanbiedingen in uw activiteit wordt verdeeld), hebt u over het algemeen niet zo veel verkeer aan de controle nodig. 10% is een goede startplaats.
* Als u één van het volgende aan een levende activiteit met een specifieke ervaring als controle doet, wordt de controle automatisch teruggesteld aan willekeurig gediende ervaringen (in plaats van de eerder geselecteerde specifieke ervaring):

   * Een ervaring verwijderen
   * Een locatie of aanbieding verwijderen (alleen AP)
   * Een ervaring handmatig uitsluiten door dubbele aanbiedingen te verwijderen of via een uitsluitingsgroep (alleen AP)

