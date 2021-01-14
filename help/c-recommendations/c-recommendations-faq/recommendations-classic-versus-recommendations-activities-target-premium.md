---
keywords: Recommendations;recommendations algorithms;recommendations activity;recommendations classic
description: Informatie die u helpt bij het kiezen tussen Recommendations Classic- en Recommendations-activiteiten in Target Premium.
title: Recommendations Classic versus Recommendations-activiteiten in Target Premium
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMR-aanbevelingen Classic versus Recommendations-activiteiten in Target Premium{#recommendations-classic-versus-recommendations-activities-in-target-premium}

Informatie die u helpt bij het kiezen tussen Recommendations Classic- en Recommendations-activiteiten in Target Premium.

>[!NOTE]
>
>Recommendations-activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium]-oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.

In het klassieke [!DNL Recommendations] product, werden de aanbevelingen getoond door een doos van de gegevensinzameling op een pagina te creëren, toen toevoegend een vertoningsdoos in een specifieke paginalocatie. Met de activiteit [!DNL Recommendations] in [!DNL Target Premium] kunt u bezoekersinformatie verzamelen en uw aanbevelingen overal op de pagina maken zonder dat u een box hoeft te maken voor elke locatie waar u producten of inhoud wilt aanbevelen. Met een eenvoudige JavaScript-verwijzing in de koptekst van de pagina kunt u overal op de pagina aanbevelingen doen. Gebruik deze JavaScript-verwijzing om sleutels door te geven aan de globale [!DNL Target]-box, zoals de `entity.id`- en `entity.categoryId`-toetsen.

[!DNL Recommendations Classic] wordt weergegeven als een eigen kaart in de  [!DNL Experience Cloud] gebruikersinterface. Een [!DNL Recommendations] activiteit is beschikbaar binnen [!DNL Target Premium] werkschema.

[!DNL Recommendations Classic] gebruikers kunnen hun  [!DNL Recommendations] vakjes in blijven gebruiken  [!DNL Target Recommendations]. Ze kunnen ook de klassieke en [!DNL Target]-benaderingen combineren door hun vakken te bewaren en de JavaScript-code in de koptekst te gebruiken om de [!DNL Recommendations]-functionaliteit te activeren voor de andere elementen op de pagina. Als u de volledige [!DNL Target]-functionaliteit wilt benutten, willen [!DNL Recommendations Classic]-gebruikers mogelijk hun oude mbox verwijderen en alleen op [!DNL Target Recommendations] vertrouwen.

De [!DNL Recommendations] activiteit in [!DNL Target] verbetert op [!DNL Recommendations Classic] op de volgende belangrijkste gebieden:

## Recommendations als voorstel

U kunt aanbevelingen binnen [!UICONTROL A/B Test] (met inbegrip van [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten omvatten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Druk automatisch het verkeer naar de best-presterende aanbevelingen ervaring gebruikend [!UICONTROL Auto-Allocate].
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel met [!UICONTROL Auto-Target].

Als u aan de slag wilt gaan, maakt u een [!UICONTROL A/B Test]- of [!UICONTROL Experience Targeting]-activiteit met behulp van [!UICONTROL Visual Experience Composer] en gebruikt u de handeling [!UICONTROL Insert Before], [!UICONTROL Insert After] of [!UICONTROL Replace With] om aanbevelingen aan een ervaring toe te voegen.

Zie [Recommendations als een aanbieding](/help/c-recommendations/recommendations-as-an-offer.md) voor meer informatie.

## Criteria {#section_117709846DAA404580EBE879FFCBD9BA}

[!DNL Target Recommendations] bevat een bibliotheek met criteria die voorverpakte sets regels en configuraties bevat. In [!DNL Recommendations Classic], werd elke aanbeveling manueel gebouwd door een vorm in te vullen en van de grote lijst van regels te kiezen. Nu, wanneer het creëren van een [!DNL Recommendations] activiteit, kiest u eenvoudig een pre-gevormde reeks criteria. U kunt nog steeds aangepaste aanbevelingen maken, maar de Criteria Library bevat veel van de meest gebruikte configuraties, vooraf gebouwd om het proces te vereenvoudigen en taal te gebruiken die mensen begrijpen. Deze vooraf verpakte criteria kunnen worden gebruikt zoals is, of zij kunnen worden gekopieerd en worden uitgegeven om uw specifieke behoeften te passen.

![](assets/overview_criteria.png)

De criteria worden pre-gevormd en gesorteerd door de industrie verticals, paginatypen, en implementatie. U kunt bijvoorbeeld zoeken naar de criteria die van toepassing zijn op de verticale handelsversie, voor gebruik op een productpagina, waarbij producten uit een bepaalde categorie worden weergegeven (zoals gedefinieerd door de parameter `entity.categoryID`).

Zie [Criteria](/help/c-recommendations/c-algorithms/algorithms.md) voor meer informatie over het gebruik en het maken van criteria.

## Workflow {#section_76B4A26297BF422382DE2C79A2713D3C}

De [!DNL Recommendations]-workflow is vereenvoudigd. In plaats van ingewikkelde formulieren in te vullen, volgt u een visuele workflow om:

1. Selecteer de criteria.
1. Selecteer een vooraf geconfigureerd [ontwerp](/help/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).
1. Bekijk de resulterende aanbevelingen.

## Visuele voorvertoning {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

U kunt uw aanbevelingen voorvertonen nadat u ze hebt ingesteld en de benodigde wijzigingen aanbrengen zonder ze op de pagina te hoeven maken en ze vervolgens te testen. Voorvertoningen zijn beschikbaar vanuit [!DNL Target].

## Doelstelling {#section_93295EA0DBA14210B8518AF4802A459F}

In [!DNL Recommendations Classic], waren er zes het richten opties. Recommendations-activiteiten maken gebruik van het volledige scala aan doelopties van Target. Definieer een publiek met [!DNL Target] of andere [!DNL Adobe Experience Cloud] soorten publiek (zoals [!DNL Audience Manager] en [!DNL Analytics]) en selecteer vervolgens het percentage van de deelnemers aan de activiteit die elk ontwerp zien, en de percentages die het besturingselement zien.

![](assets/overview_targeting.png)

## {#section_25C2FCCE4BC1488496C517C0470B5CD6} rapporteren

In [!DNL Target] biedt [!DNL Recommendations] verbeterde rapportering die gebruikmaakt van de mogelijkheden die worden geboden door [!DNL Target] en [!DNL Experience Cloud]. In plaats van alleen maar de lift te tonen die door [!DNL Recommendations] wordt geleverd in vergelijking met de resultaten zonder deze, kunt u volledige informatie over uw [!DNL Recommendations] activiteit bekijken.

![](assets/overview_report.png)

