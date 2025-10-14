---
keywords: Aanbevelingen;aanbevelingen algoritmen;aanbevelingen activiteit;aanbevelingen klassieke
description: De informatie van het overzicht om u te helpen de verschillen tussen de Klassieke activiteiten van de erfenisAanbevelingen en van Aanbevelingen in  [!DNL Target]  Premium begrijpen.
title: Wat is het Verschil tussen Klassieke Aanbevelingen en Aanbevelingen in  [!DNL Target]  Premium?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 07548155-9548-4870-b886-6cb4ff37a0bd
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Activiteiten van Aanbevelingen voor Klassieke versus Aanbevelingen in [!DNL Target] Premium

Informatie die u helpt bij het kiezen tussen activiteiten in Target Premium op het gebied van Recommendations Classic en Recommendations.

>[!NOTE]
>
>De activiteiten van aanbevelingen zijn beschikbaar als deel van de [!DNL Target Premium] oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie.

In het klassieke [!DNL Recommendations] product werden aanbevelingen weergegeven door een gegevensverzamelingsvak op een pagina te maken en vervolgens een weergavekader op een specifieke paginalocatie toe te voegen. Met de [!DNL Recommendations] -activiteit in [!DNL Target Premium] kunt u bezoekersinformatie verzamelen en uw aanbevelingen overal op de pagina maken zonder dat u een box hoeft te maken voor elke locatie waar u producten of inhoud wilt aanbevelen. Met een eenvoudige JavaScript-verwijzing in de koptekst van de pagina kunt u overal op de pagina aanbevelingen doen. Gebruik deze JavaScript-verwijzing om sleutels door te geven aan de algemene [!DNL Target] -box, zoals de `entity.id` - en `entity.categoryId` -toets.

[!DNL Recommendations Classic] wordt als een eigen kaart weergegeven in de gebruikersinterface van [!DNL Experience Cloud] . Een [!DNL Recommendations] -activiteit is beschikbaar vanuit de [!DNL Target Premium] -workflow.

[!DNL Recommendations Classic] -gebruikers kunnen hun [!DNL Recommendations] box in [!DNL Target Recommendations] blijven gebruiken. Ze kunnen de klassieke en [!DNL Target] benaderingen ook combineren door hun vakjes bij te houden en de JavaScript-code in de koptekst te gebruiken om de [!DNL Recommendations] -functionaliteit voor de andere elementen op de pagina te activeren. [!DNL Target] -gebruikers kunnen echter liever hun oude mbox verwijderen en alleen op [!DNL Recommendations Classic] vertrouwen om de volledige functionaliteit van [!DNL Target Recommendations] te verkrijgen.

De [!DNL Recommendations] activiteit in [!DNL Target] verbetert [!DNL Recommendations Classic] op de volgende hoofdgebieden:

## Aanbevelingen als voorstel

U kunt aanbevelingen opnemen in [!UICONTROL A/B Test] (inclusief [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target]) en [!UICONTROL Experience Targeting] (XT) activiteiten.

Deze functionaliteit opent volledig nieuwe mogelijkheden, zoals:

* Test- en doelaanbevelingen en niet-aanbevolen inhoud binnen dezelfde activiteit.
* Experimenteer eenvoudig met het plaatsen van aanbevelingen op de pagina, inclusief de volgorde van meerdere aanbevelingen.
* Met [!UICONTROL Auto-Allocate] wordt het verkeer automatisch naar de best presterende aanbevelingen verschoven.
* Wijs bezoekers dynamisch toe aan op maat gemaakte aanbevelingen op basis van hun profiel met [!UICONTROL Auto-Target] .

Als u aan de slag wilt gaan, maakt u een [!UICONTROL A/B Test] - of [!UICONTROL Experience Targeting] -activiteit met behulp van [!UICONTROL Visual Experience Composer] en gebruikt u de handeling [!UICONTROL Insert Before] , [!UICONTROL Insert After] of [!UICONTROL Replace With] om aanbevelingen aan een ervaring toe te voegen.

Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md).

## Criteria {#section_117709846DAA404580EBE879FFCBD9BA}

[!DNL Target Recommendations] bevat een bibliotheek met criteria die voorverpakte sets regels en configuraties bevat. In [!DNL Recommendations Classic] is elke aanbeveling handmatig opgebouwd door een formulier in te vullen en een keuze te maken in de grote lijst met regels. Wanneer u nu een [!DNL Recommendations] -activiteit maakt, kiest u gewoon een vooraf geconfigureerde set criteria. U kunt nog steeds aangepaste aanbevelingen maken, maar de Criteria Library bevat veel van de meest gebruikte configuraties, vooraf gebouwd om het proces te vereenvoudigen en taal te gebruiken die mensen begrijpen. Deze vooraf verpakte criteria kunnen worden gebruikt zoals is, of zij kunnen worden gekopieerd en worden uitgegeven om uw specifieke behoeften te passen.

![&#x200B; overview_criteria beeld &#x200B;](assets/overview_criteria.png)

De criteria worden pre-gevormd en gesorteerd door de industrie verticals, paginatypen, en implementatie. U kunt bijvoorbeeld zoeken naar de criteria die van toepassing zijn op de verticale handelsversie, voor gebruik op een productpagina, waarbij producten uit een bepaalde categorie worden weergegeven (zoals gedefinieerd door de parameter `entity.categoryID` ).

Voor meer informatie over het gebruiken van en het creëren van criteria, zie [&#x200B; Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Workflow {#section_76B4A26297BF422382DE2C79A2713D3C}

De [!DNL Recommendations] -workflow is vereenvoudigd. In plaats van ingewikkelde formulieren in te vullen, volgt u een visuele workflow om:

1. Selecteer de criteria.
1. Selecteer een pre-gevormd [&#x200B; ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/create-design.md#task_CC5BD28C364742218C1ACAF0D45E0E14).
1. Bekijk de resulterende aanbevelingen.

## Visuele voorvertoning {#section_639B9E38C9EC4093BF9023EE0F2A15AC}

U kunt uw aanbevelingen voorvertonen nadat u ze hebt ingesteld en de benodigde wijzigingen aanbrengen zonder ze op de pagina te hoeven maken en ze vervolgens te testen. Voorvertoningen zijn beschikbaar vanuit [!DNL Target] .

## Targeting {#section_93295EA0DBA14210B8518AF4802A459F}

In [!DNL Recommendations Classic] waren er zes doelopties. Bij de activiteiten van de aanbevelingen wordt gebruikgemaakt van het volledige scala van doelopties. Definieer een publiek met [!DNL Target] of een ander [!DNL Adobe Experience Cloud] publiek (zoals [!DNL Audience Manager] en [!DNL Analytics] ) en selecteer vervolgens het percentage van de items in de activiteit die elk ontwerp zien, en de percentages die het besturingselement zien.

![&#x200B; overview_targeting beeld &#x200B;](assets/overview_targeting.png)

## Rapportage {#section_25C2FCCE4BC1488496C517C0470B5CD6}

In [!DNL Target] biedt [!DNL Recommendations] verbeterde rapportage die de mogelijkheden benut die worden geboden door [!DNL Target] en [!DNL Experience Cloud] . In plaats van alleen maar de lift te tonen die door [!DNL Recommendations] wordt geleverd in vergelijking met de resultaten zonder deze, kunt u volledige informatie over uw [!DNL Recommendations] -activiteit bekijken.

![&#x200B; overview_report beeld &#x200B;](assets/overview_report.png)
