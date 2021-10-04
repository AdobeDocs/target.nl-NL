---
keywords: publiek;publieksregels;publiek maken;publiek maken
description: Leer hoe u een aangepast publiek kunt maken en deze kunt opslaan in de  [!DNL Adobe Target] [!UICONTROL Audiences] bibliotheek voor gebruik in activiteiten.
title: Hoe kan ik publiek maken?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: b74cccdc43c34367819ed8a908a304b567d7ecbb
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# Stimuleer publiek in [!DNL Target]

U kunt aangepaste soorten publiek maken en deze opslaan in de [!DNL Adobe Target] [!UICONTROL Audiences]-bibliotheek voor gebruik in uw activiteiten. U kunt ook een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken en meerdere soorten publiek te combineren.

## Overzicht van het publiek

Het publiek wordt bepaald door regels die bepalen wie van [!DNL Target] activiteit inbegrepen of uitgesloten is. Een publieksdefinitie kan veelvoudige regels omvatten en elke regel kan veelvoudige parameters omvatten. Complexe publieksdefinities gebruiken de Booleaanse operatoren AND en OR om regels en parameters te combineren, zodat u precies kunt bepalen welke bezoekers van de site worden geteld als deelnemers aan de activiteit.

Wanneer u regels of parameters met AND combineert, moet om het even welk potentieel publiekslid *alle* bepaalde voorwaarden voldoen om als toetreder te worden omvat. Als u bijvoorbeeld een OS-regel EN een browserregel definieert, worden alleen bezoekers die zowel het gedefinieerde besturingssysteem *als* de gedefinieerde browser gebruiken, opgenomen in de activiteit.

Wanneer u regels of parameters combineert met OR, hoeft elk mogelijk publiekslid slechts aan één gedefinieerde voorwaarde te voldoen om als een deelnemer te worden opgenomen. Als u bijvoorbeeld meerdere mobiele regels definieert die zijn verbonden door OR, worden bezoekers die *om het even welke* van de gedefinieerde criteria ontmoeten, opgenomen in de activiteit.

U kunt beide Booleaanse operatoren mengen om complexe regels te maken. operatoren op hetzelfde regelniveau moeten echter overeenkomen. De gebruikersinterface past automatisch de juiste operator toe.

De volgende regel geldt bijvoorbeeld voor bezoekers die Chrome *of* Firefox gebruiken op een Windows-computer:

![publiek maken](assets/audience_create.png)

>[!NOTE]
>
>Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina gelijktijdig bezoekt met Chrome *en* Firefox.

## Een doelgroep maken

1. Klik op **[!UICONTROL Audiences]** in de bovenste menubalk.

   ![](assets/audiences_list.png)

1. Klik in de lijst [!UICONTROL Audiences] op **[!UICONTROL Create Audience]**.

   of

   Als u een bestaand publiek wilt kopiëren, klikt u in de lijst [!UICONTROL Audiences] op het pictogram **[!UICONTROL More Actions]** (het pictogram voor de ovaal) en vervolgens op **[!UICONTROL Duplicate]**. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een unieke, beschrijvende publieksnaam en een optionele beschrijving.
1. Sleep de gewenste kenmerken uit de lijst **[!UICONTROL Attributes]** rechts naar het deelvenster voor de publieksbuilder.

   ![Kenmerken voor slepen en neerzetten](assets/drag-attribute.png)

   Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor Soorten publiek](/help/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Definieer de regelparameters.

   Het volgende publiek richt zich bijvoorbeeld op bezoekers van Utah met behulp van het Macintosh-besturingssysteem.

   ![Utah-/Macintosh-publiek](assets/adience-builder.png)

1. (Voorwaardelijk) Ga verder met het toevoegen en definiëren van de gewenste kenmerken.

   Als u een andere container wilt maken, klikt u op **[!UICONTROL Add container]** of sleept u een ander kenmerk naar het deelvenster Audience Builder. Vervolgens kunt u de operator (AND of OR) aanpassen met de vervolgkeuzelijst.

1. Klik op **[!UICONTROL Done]**.

   Nieuw gemaakt publiek wordt na een paar seconden verwerkingstijd in de lijst weergegeven. Als het publiek niet direct in de lijst wordt weergegeven, probeert u naar het publiek te zoeken of vernieuwt u de lijst.

## Trainingsvideo: Soorten publiek maken ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het maken van soorten publiek.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
