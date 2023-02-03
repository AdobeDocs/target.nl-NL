---
keywords: publiek;publieksregels;publiek maken;publiek maken
description: Leer hoe u een aangepast publiek kunt maken en deze kunt opslaan in de [!DNL Adobe Target] [!UICONTROL Audiences] bibliotheek voor gebruik in activiteiten.
title: Hoe kan ik publiek maken?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: a185edee86f6d07b488cf5dd3fe7e5dc3f4e87b3
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Stimuleer publiek in [!DNL Target]

U kunt een aangepast publiek maken en deze opslaan in de [!DNL Adobe Target] [!UICONTROL Audiences] bibliotheek voor gebruik in uw activiteiten. U kunt ook een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken en meerdere soorten publiek te combineren.

## Overzicht van het publiek

Het publiek wordt gedefinieerd door regels die bepalen wie van een [!DNL Target] activiteit. Een publieksdefinitie kan veelvoudige regels omvatten en elke regel kan veelvoudige parameters omvatten. Complexe publieksdefinities gebruiken de Booleaanse operatoren AND en OR om regels en parameters te combineren, zodat u precies kunt bepalen welke bezoekers van de site worden geteld als deelnemers aan de activiteit.

Wanneer u regels of parameters met AND combineert, moet om het even welk potentieel publiekslid ontmoeten *alles* omschreven voorwaarden die als gegadigde moeten worden opgenomen. Als u bijvoorbeeld een OS-regel EN een browserregel definieert, gebruiken alleen bezoekers beide gedefinieerde besturingssystemen *en* de gedefinieerde browser wordt in de activiteit opgenomen.

Wanneer u regels of parameters combineert met OR, hoeft elk mogelijk publiekslid slechts aan één gedefinieerde voorwaarde te voldoen om als een deelnemer te worden opgenomen. Als u bijvoorbeeld meerdere mobiele regels definieert die zijn verbonden door OR, komen bezoekers bijeen *alle* van de vastgestelde criteria worden in de activiteit opgenomen .

U kunt beide Booleaanse operatoren mengen om complexe regels te maken. operatoren op hetzelfde regelniveau moeten echter overeenkomen. De gebruikersinterface past automatisch de juiste operator toe.

De volgende regel geldt bijvoorbeeld voor bezoekers die Chrome gebruiken *of* Firefox op een Windows-computer:

![publiek maken](assets/audience_create.png)

>[!NOTE]
>
>Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Het is bijvoorbeeld niet mogelijk dat iemand een pagina bezoekt met Chrome *en* Firefox tegelijk.

## Een doelgroep maken

1. Klikken **[!UICONTROL Audiences]** in de bovenste menubalk.

   ![publiek_lijstafbeelding](assets/audiences_list.png)

1. Van de [!UICONTROL Audiences] lijst, klikt u op **[!UICONTROL Create Audience]**.

   of

   Om een bestaand publiek te kopiëren, van [!UICONTROL Audiences] lijst, klikt u op de knop **[!UICONTROL More Actions]** pictogram (het pictogram van de ellips), dan klik **[!UICONTROL Duplicate]**. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een unieke, beschrijvende publieksnaam en een optionele beschrijving.

   Namen van soorten publiek mogen niet beginnen met de volgende tekens:

   `=  +  -  !  @`

   Namen van doelgroepen mogen geen van de volgende tekenreeksen bevatten:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Sleep de gewenste kenmerken vanuit het menu **[!UICONTROL Attributes]** lijst op het recht aan de ruit van de publieksbouwer.

   ![Kenmerken voor slepen en neerzetten](assets/drag-attribute.png)

   Elk regeltype heeft zijn eigen parameters. Zie [Categorieën voor soorten publiek](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Definieer de regelparameters.

   Het volgende publiek richt zich bijvoorbeeld op bezoekers van Utah met behulp van het Macintosh-besturingssysteem.

   ![Utah-/Macintosh-publiek](assets/adience-builder.png)

1. (Voorwaardelijk) Ga verder met het toevoegen en definiëren van de gewenste kenmerken.

   Als u een andere container wilt maken, klikt u op **[!UICONTROL Add container]** of sleep gewoon een ander kenmerk naar het deelvenster Audience Builder. Vervolgens kunt u de operator (AND of OR) aanpassen met de vervolgkeuzelijst.

1. Klik op **[!UICONTROL Done]**.

   Nieuw gemaakt publiek wordt na een paar seconden verwerkingstijd in de lijst weergegeven. Als het publiek niet direct in de lijst wordt weergegeven, probeert u naar het publiek te zoeken of vernieuwt u de lijst.

## Trainingsvideo: Soorten publiek maken ![Overzicht badge](/help/main/assets/overview.png)

Deze video bevat informatie over het maken van soorten publiek.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
