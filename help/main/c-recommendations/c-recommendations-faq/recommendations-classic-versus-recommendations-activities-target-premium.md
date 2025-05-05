---
keywords: Recommendations;aanbevelingen algoritmen;aanbevelingen activiteit;aanbevelingen klassieke
description: Bekijk informatie om u te helpen inzicht te krijgen in de verschillen tussen de oude Recommendations Classic en Recommendations activiteiten in [!DNL Target] Premium.
title: Wat is het verschil tussen Recommendations Classic en Recommendations in [!DNL Target] Premium?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Recommendations Classic versus Recommendations-activiteiten in [!DNL Target] Premium

Informatie die u helpt bij het kiezen tussen Recommendations Classic- en Recommendations-activiteiten in Target Premium.

>[!NOTE]
>
>De activiteiten van Recommendations zijn beschikbaar als deel van [!DNL Target Premium] oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie.

In het klassieke [!DNL Recommendations] aanbevelingen werden weergegeven door een gegevensverzamelingsvak op een pagina te maken en vervolgens een weergavekader op een specifieke paginalocatie toe te voegen. De [!DNL Recommendations] activiteit in [!DNL Target Premium] kunt u bezoekersinformatie verzamelen en uw aanbevelingen overal op de pagina tot stand brengen zonder de behoefte om een mbox voor elke plaats te creëren waar u producten of inhoud wilt adviseren. Met een eenvoudige JavaScript-verwijzing in de koptekst van de pagina kunt u overal op de pagina aanbevelingen doen. Gebruik deze JavaScript-verwijzing om sleutels door te geven aan het algemene [!DNL Target] mbox, zoals de `entity.id` en `entity.categoryId` toetsen.

[!DNL Recommendations Classic] verschijnt als zijn eigen kaart in [!DNL Experience Cloud] UI. A [!DNL Recommendations] activiteit is beschikbaar vanuit de [!DNL Target Premium] workflow.

[!DNL Recommendations Classic] gebruikers kunnen hun [!DNL Recommendations] vakken in [!DNL Target Recommendations]. Zij kunnen ook de klassieke [!DNL Target] benaderingen door hun dozen te houden en de code JavaScript in de kopbal te gebruiken om te activeren [!DNL Recommendations] functionaliteit voor de andere elementen op de pagina. Om volledig te worden [!DNL Target] echter [!DNL Recommendations Classic] gebruikers kunnen liever hun oude mbox verwijderen en alleen vertrouwen op [!DNL Target Recommendations].

De [!DNL Recommendations] activiteit in [!DNL Target] verbetert op [!DNL Recommendations Classic] op de volgende hoofdgebieden:

## Recommendations als voorstel

U kunt aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Druk automatisch het verkeer aan de best presterende aanbevelingen ervaring gebruikend [!UICONTROL Auto-Allocate].
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel [!UICONTROL Auto-Target].

Om aan de slag te gaan, maakt u een [!UICONTROL A/B Test] of [!UICONTROL Experience Targeting] activiteit met behulp van de [!UICONTROL Visual Experience Composer] en gebruiken de [!UICONTROL Insert Before], [!UICONTROL Insert After], of [!UICONTROL Replace With] actie om aanbevelingen aan een ervaring toe te voegen.

Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md).

## Criteria {#section_117709846DAA404580EBE879FFCBD9BA}

[!DNL Target Recommendations] bevat een bibliotheek met criteria die voorverpakte sets regels en configuraties bevat. In [!DNL Recommendations Classic], werd elke aanbeveling manueel opgebouwd door een vorm in te vullen en van de grote lijst van regels te kiezen. Bij het maken van een [!DNL Recommendations] activiteit, kiest u eenvoudig een pre-gevormde reeks criteria. U kunt nog steeds aangepaste aanbevelingen maken, maar de Criteria Library bevat veel van de meest gebruikte configuraties, vooraf gebouwd om het proces te vereenvoudigen en taal te gebruiken die mensen begrijpen. Deze vooraf verpakte criteria kunnen worden gebruikt zoals is, of zij kunnen worden gekopieerd en worden uitgegeven om uw specifieke behoeften te passen.

![overview_criteria, afbeelding](assets/overview_criteria.png)

De criteria worden pre-gevormd en gesorteerd door de industrie verticals, paginatypen, en implementatie. U kunt bijvoorbeeld zoeken naar de criteria die van toepassing zijn op de verticale detailhandel, voor gebruik op een productpagina, waarbij producten uit een bepaalde categorie worden weergegeven (zoals gedefinieerd door de `entity.categoryID` parameter).

Voor meer informatie over het gebruiken van en het creëren van criteria, zie [Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Workflow {#section_76B4A26297BF422382DE2C79A2713D3C}

De [!DNL Recommendations] de workflow is vereenvoudigd . In plaats van ingewikkelde formulieren in te vullen, volgt u een visuele workflow om:

1. Selecteer de criteria.
1. Selecteer een vooraf geconfigureerd [ontwerp](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).
1. Bekijk de resulterende aanbevelingen.

## Visuele voorvertoning {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

U kunt uw aanbevelingen voorvertonen nadat u ze hebt ingesteld en de benodigde wijzigingen aanbrengen zonder ze op de pagina te hoeven maken en ze vervolgens te testen. Voorvertoningen zijn beschikbaar vanuit [!DNL Target].

## Doelstelling {#section_93295EA0DBA14210B8518AF4802A459F}

In [!DNL Recommendations Classic], er waren zes opties voor doelgerichte acties. Recommendations-activiteiten maken gebruik van het volledige scala aan doelopties van Target. Een publiek definiëren met een van beide [!DNL Target] of andere [!DNL Adobe Experience Cloud] publiek (zoals [!DNL Audience Manager] en [!DNL Analytics]) selecteert u vervolgens het percentage actieve deelnemers dat elk ontwerp ziet en de percentages die het besturingselement zien.

![overview_targeting, afbeelding](assets/overview_targeting.png)

## Rapportage {#section_25C2FCCE4BC1488496C517C0470B5CD6}

In [!DNL Target], [!DNL Recommendations] biedt verbeterde rapportering die gebruik maakt van de mogelijkheden die worden geboden door [!DNL Target] en de [!DNL Experience Cloud]. In plaats van simpelweg de door [!DNL Recommendations] in vergelijking met de resultaten zonder resultaten kunt u volledige informatie over uw [!DNL Recommendations] activiteit.

![overview_report, afbeelding](assets/overview_report.png)
