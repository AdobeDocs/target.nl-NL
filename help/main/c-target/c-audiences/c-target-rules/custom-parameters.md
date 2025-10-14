---
keywords: aangepaste parameters;aangepaste doelparameters;doelparameters;doelparameters;doelframes;doelframes opgeven, parameters
description: Leer hoe te om douaneparameters tot  [!DNL Adobe Target]  voor gebruik in publiek over te gaan.
title: Kan ik bezoekers richten die op de Parameters van de Douane worden gebaseerd?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Aangepaste parameters

Aangepaste parameters zijn de parameters mbox in [!DNL Adobe Target] . Wanneer u parameters van het selectiekader doorgeeft aan selectievakjes of de functie `targetPageParams` gebruikt, worden deze parameters hier weergegeven voor gebruik bij het publiek.

Voor meer informatie, zie [&#x200B; parameters van de pas aan globale mbox &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/global-mbox/pass-parameters-to-global-mbox.html?lang=nl-NL){target=_blank}.

Wanneer u een aangepast publiek maakt op basis van een mbox-parameter, vraagt `mboxParameter` niet langer om `mboxName` . De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]** .
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Custom]** naar de Audience Builder.

   De gewenste parameter selecteren:

   * Selecteer tijdens het maken van een publiek een parameternaam in de lijst, typ de eerste tekens van de gewenste parameternaam of typ de volledige naam van de gewenste parameternaam.
   * Als u de naam van het selectievakje onthoudt, maar niet de naam van de parameter, gebruikt u de vervolgkeuzelijst [!UICONTROL Filter by] om te filteren op een bekende doos die de gewenste parameter doorgeeft.

   Bij beide methoden is er geen koppeling tussen de mbox en de parameter. Het publiek werkt op basis van de parameter in alle vakken die die parameter doorgeven.

   >[!NOTE]
   >
   >Het selectievakje dat u selecteert in de vervolgkeuzelijst [!UICONTROL Filter By] , wordt niet opgeslagen bij het maken van activiteiten. Met deze optie kunt u de parameters filteren op basis van het geselecteerde selectievakje.

   Als u een bestaand publiek bewerkt, worden de filtercriteria weergegeven met de naam van de box die tijdens het maken is opgegeven.

1. Kies een beoordelaar:

   * Bevat (hoofdlettergevoelig)
   * Bevat niet (hoofdlettergevoelig)
   * Gelijk
   * Is niet gelijk aan
   * Is groter dan
   * Is groter dan of gelijk aan
   * Is kleiner dan
   * Is kleiner dan of gelijk aan
   * Parameter is aanwezig
   * Parameter is niet aanwezig
   * Parameterwaarde is aanwezig
   * Parameterwaarde is niet aanwezig
   * Parameter of waarde is niet aanwezig
   * Beginnen met
   * Eindigt met

   ![&#x200B; de parameterpubliek van de Douane &#x200B;](assets/custom.png)

1. Voer elke waarde op een nieuwe regel in.
1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

De de definitiedetails van het publiek [&#x200B; pop-up kaart &#x200B;](/help/main/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) toont de parameternaam in de **[!UICONTROL Rules]** sectie. Er is geen verwijzing naar de box die voor het filtreren wordt gebruikt.

>[!NOTE]
>
>Voor aangepaste soorten publiek die vóór de release [!DNL Target] 18.5.1 (22 mei 2018) zijn gemaakt, worden de namen van de selectievakjes niet weergegeven in de definitie-pop-upkaart van het publiek. Sla het aangepaste publiek opnieuw op om de naam van het selectievakje weer te geven op de kaart.

## Overwegingen {#considerations}

* Soorten publiek en activiteiten worden voor een specifieke box geëvalueerd. Als de globale box bijvoorbeeld een bepaalde parameter doorgeeft, maar de regionale box niet, is de activiteit/het publiek die die parameter aanwijst niet gekwalificeerd voor de regionale box.
* Het richten wordt niet geëvalueerd op interne mbox parameters, zoals mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId, en mboxVersion.

## De video van de opleiding: Creërend publiek ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
