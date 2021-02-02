---
keywords: publiek;publieksregels;publiek maken;publiek maken
description: U kunt aangepaste doelgroepen maken en deze opslaan in de doelbibliotheek voor gebruik in uw activiteiten. U kunt een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken en meerdere soorten publiek te combineren.
title: Soorten publiek maken
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Stimuleer publiek in doel{#build-audiences-in-target}

U kunt aangepaste doelgroepen maken en deze opslaan in de doelbibliotheek voor gebruik in uw activiteiten. U kunt een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken en meerdere soorten publiek te combineren.

## Overzicht van het publiek

Het publiek wordt bepaald door regels die bepalen wie van [!DNL Target] activiteit inbegrepen of uitgesloten is. Een publieksdefinitie kan veelvoudige regels omvatten en elke regel kan veelvoudige parameters omvatten. Complexe publieksdefinities gebruiken de Booleaanse operatoren AND en OR om regels en parameters te combineren, zodat u precies kunt bepalen welke bezoekers van de site worden geteld als deelnemers aan de activiteit.

Wanneer u regels of parameters met AND combineert, moet om het even welk potentieel publiekslid *all* van de bepaalde voorwaarden voldoen om als toetreder te worden omvat. Als u bijvoorbeeld een OS-regel EN een browserregel definieert, worden alleen bezoekers die zowel het gedefinieerde besturingssysteem *als* de gedefinieerde browser gebruiken, opgenomen in de activiteit.

Wanneer u regels of parameters combineert met OR, hoeft elk mogelijk publiekslid slechts aan één gedefinieerde voorwaarde te voldoen om als een deelnemer te worden opgenomen. Als u bijvoorbeeld meerdere mobiele regels definieert die zijn verbonden door OR, worden bezoekers die *om het even welke* van de gedefinieerde criteria ontmoeten, opgenomen in de activiteit.

U kunt beide Booleaanse operatoren mengen om complexe regels te maken. operatoren op hetzelfde regelniveau moeten echter overeenkomen. De gebruikersinterface past automatisch de juiste operator toe.

De volgende regel geldt bijvoorbeeld voor bezoekers die Chrome *of* Firefox gebruiken op een Windows-computer:

![publiek maken](assets/audience_create.png)

>[!NOTE]
>
>Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina gelijktijdig bezoekt met Chrome *en* Firefox.

## Een nieuw publiek maken

1. Klik op **[!UICONTROL Audiences]** in de bovenste menubalk.

   ![](assets/audiences_list.png)

1. Klik in de lijst [!UICONTROL Audiences] op **[!UICONTROL + Create Audience]**.

   of

   Als u een bestaand publiek wilt kopiëren, klikt u in de lijst [!UICONTROL Audiences] op het pictogram **[!UICONTROL Copy]**. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een unieke, beschrijvende publieksnaam.
1. Klik op **[!UICONTROL + Add Rule]**.

   Regels maken het mogelijk om uw publiek te beperken tot een subset van uw sitebezoekers.
1. Selecteer een regeltype.

   Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor Soorten publiek](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.
1. Definieer de regelparameters.
1. Klik op **[!UICONTROL Save]**.

   Nieuw gemaakt publiek wordt na een paar seconden verwerkingstijd in de lijst weergegeven. Als het publiek niet direct in de lijst wordt weergegeven, probeert u naar het publiek te zoeken of vernieuwt u de lijst.

## Trainingsvideo: Soorten publiek maken ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het maken van soorten publiek.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)