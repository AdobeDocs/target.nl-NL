---
keywords: publiek;publieksregels;publiek maken;publiek maken
description: Leer hoe te om tot aangepast publiek te leiden en hen te bewaren aan de  [!DNL Adobe Target] [!UICONTROL Audiences] bibliotheek voor gebruik in activiteiten.
title: Hoe kan ik soorten publiek opbouwen?
feature: Audiences
exl-id: 59057461-d958-4d38-9725-53aacbe1f7eb
source-git-commit: 19d2b14f137fe4dbf95e9f9f9b84f80b93d1e281
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Soorten publiek maken in [!DNL Target]

Maak een aangepast publiek en sla dit op in de [!DNL Adobe Target] [!UICONTROL Audiences] -bibliotheek voor gebruik in uw activiteiten. U kunt ook een bestaand publiek kopiëren dat u vervolgens kunt bewerken om een vergelijkbaar publiek te maken en meerdere soorten publiek te combineren.

## Overzicht van het publiek

Soorten publiek worden gedefinieerd door regels die bepalen wie wordt opgenomen in of uitgesloten van een [!DNL Target] -activiteit. Een publieksdefinitie kan veelvoudige regels omvatten en elke regel kan veelvoudige parameters omvatten. Complexe publieksdefinities gebruiken de Booleaanse operatoren AND en OR om regels en parameters te combineren, zodat u precies kunt bepalen welke bezoekers van de site worden geteld als deelnemers aan de activiteit.

Wanneer u regels of parameters met EN combineert, moet om het even welk potentieel publiekslid *alle* bepaalde voorwaarden ontmoeten om als ingang worden omvat. Bijvoorbeeld, als u een OS regel EN een browser regel bepaalt, slechts zijn de bezoekers die zowel bepaald OS *gebruiken als* bepaalde browser inbegrepen in de activiteit.

Wanneer u regels of parameters combineert met OR, hoeft elk mogelijk publiekslid slechts aan één gedefinieerde voorwaarde te voldoen om als een deelnemer te worden opgenomen. Bijvoorbeeld, als u veelvoudige mobiele regels bepaalt die door OF worden verbonden, bezoekers die *om het even welke* van de bepaalde criteria ontmoeten zijn inbegrepen in de activiteit.

U kunt beide Booleaanse operatoren vermengen om complexe regels te maken. Operatoren op hetzelfde regelniveau moeten echter overeenkomen. De gebruikersinterface past automatisch de juiste operator toe.

Bijvoorbeeld, richt de volgende regel bezoekers die of [!DNL Chrome] *of* [!DNL Firefox] op een [!DNL Windows] computer gebruiken:

![&#x200B; creeer publiek &#x200B;](assets/audience_create.png)

>[!NOTE]
>
>Zorg ervoor dat u geen regels maakt die alle mogelijke publieksleden uitsluiten. Bijvoorbeeld, is het niet mogelijk voor iemand om een pagina te bezoeken gebruikend [!DNL Chrome] *en* [!DNL Firefox] gelijktijdig.

## Een publiek maken

1. Klik op **[!UICONTROL Audiences]** in de bovenste menubalk.

   ![&#x200B; publiek_list beeld &#x200B;](assets/audiences_list.png)

1. Klik in de lijst [!UICONTROL Audiences] op **[!UICONTROL Create Audience]** .

   of

   Om een bestaand publiek, van de [!UICONTROL Audiences] lijst te kopiëren, klik het **[!UICONTROL More Actions]** pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)) voor het publiek dat u wilt kopiëren, dan klikken **[!UICONTROL Duplicate]**. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een unieke, beschrijvende publieksnaam en een optionele beschrijving.

   Namen van soorten publiek mogen niet beginnen met de volgende tekens:

   `=  +  -  !  @`

   Namen van doelgroepen mogen geen van de volgende tekenreeksen bevatten:

   `;=  ;+  ;-  ;@  ,=  ,+  ,-  ,@  ["  "]  ['  ]'`

1. Sleep de gewenste kenmerken uit de lijst **[!UICONTROL Attributes]** aan de linkerkant naar het deelvenster van de publieksbuilder.

   ![&#x200B; belemmering en dalingsattributen &#x200B;](assets/drag-attribute.png)

   Elk regeltype heeft zijn eigen parameters. Zie [&#x200B; Categorieën voor Soorten publiek &#x200B;](/help/main/c-target/c-audiences/c-target-rules/target-rules.md#concept_E3A77E42F1644503A829B5107B20880D) voor meer informatie bij het vormen van elk type van publieksregel.

1. Definieer de regelparameters.

   Het volgende publiek richt zich bijvoorbeeld op bezoekers van Utah via het besturingssysteem [!DNL Macintosh] .

   ![&#x200B; Utah/Macintosh publiek &#x200B;](assets/adience-builder.png)

1. (Voorwaardelijk) Ga verder met het toevoegen en definiëren van de gewenste kenmerken.

   Als u een andere container wilt maken, klikt u op **[!UICONTROL Add container]** of sleept u een ander kenmerk naar het deelvenster Audience Builder. Vervolgens kunt u de operator (AND of OR) aanpassen met de vervolgkeuzelijst.

1. Klik op **[!UICONTROL Done]**.

   Nieuw gemaakt publiek wordt na een paar seconden verwerkingstijd in de lijst weergegeven. Als het publiek niet direct in de lijst wordt weergegeven, probeert u naar het publiek te zoeken of vernieuwt u de lijst.

## De video van de opleiding: Creërend publiek ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat informatie over het maken van soorten publiek.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
