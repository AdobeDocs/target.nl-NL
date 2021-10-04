---
keywords: aangepaste parameters;aangepaste doelparameters;doelparameters;doelparameters;doelframes;doelframes opgeven, parameters
description: Leer hoe te om douaneparameters tot  [!DNL Adobe Target] voor gebruik in publiek over te gaan.
title: Kan ik bezoekers richten die op de Parameters van de Douane worden gebaseerd?
feature: Audiences
exl-id: f0669888-6b9e-4738-9ed4-0418ea56fffa
source-git-commit: b74cccdc43c34367819ed8a908a304b567d7ecbb
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Aangepaste parameters

Aangepaste parameters zijn parameters mbox in [!DNL Adobe Target]. Als u parameters van een box aan vakjes, of de functie `targetPageParams` doorgeeft, verschijnen die parameters hier voor gebruik in publiek.

Zie [Parameters doorgeven aan een globale box](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) voor meer informatie.

Wanneer u een aangepast publiek maakt op basis van een mbox-parameter, vraagt `mboxParameter` u niet meer om `mboxName`. De naam van het selectievakje is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Custom]** in de Bouwer van de Publiek.

   De gewenste parameter selecteren:

   * Selecteer tijdens het maken van een publiek een parameternaam in de lijst, typ de eerste tekens van de gewenste parameternaam of typ de volledige naam van de gewenste parameternaam.
   * Als u de naam van de box, maar niet de parameternaam herinnert, gebruik [!UICONTROL Filter by] drop-down lijst aan filter op een bekende doos die de gewenste parameter overgaat.

   Bij beide methoden is er geen koppeling tussen de mbox en de parameter. Het publiek werkt op basis van de parameter in alle vakken die die parameter doorgeven.

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

   ![Aangepast parameterpubliek](assets/custom.png)

1. Voer elke waarde op een nieuwe regel in.
1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

De [definitiedetails pop-up kaart](/help/c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) van het publiek toont de parameternaam in **[!UICONTROL Rules]** sectie. Er is geen verwijzing naar mbox gebruikt voor het filtreren.

>[!NOTE]
>
>Voor aangepast publiek dat vóór de [!DNL Target] 18.5.1-release (22 mei 2018) is gemaakt, worden de namen van de box niet weergegeven in de definitie-pop-upkaart van het publiek. Sla het aangepaste publiek opnieuw op om de naam van het selectievakje weer te geven op de kaart.

## Overwegingen {#considerations}

* Soorten publiek en activiteiten worden voor een specifieke box geëvalueerd. Als de globale box bijvoorbeeld een bepaalde parameter doorgeeft, maar de regionale box niet, is de activiteit/het publiek die die parameter aanwijst niet gekwalificeerd voor de regionale box.
* Het richten wordt niet geëvalueerd op interne mbox parameters, zoals mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId, en mboxVersion.

## Trainingsvideo: Soorten publiek ![Zelfstudie-badge](/help/assets/tutorial.png) maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
