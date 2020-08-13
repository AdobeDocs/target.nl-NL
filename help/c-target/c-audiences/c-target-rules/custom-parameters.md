---
keywords: custom parameters;target custom parameters;targetpageparams;targeting mbox parameters
description: Aangepaste parameters zijn parameters mbox. Als u om het even welke mbox parameters tot dozen, of de targetPageParams functie doorgeeft, verschijnen die parameters hier voor gebruik in publiek.
title: Aangepaste parameters in Adobe Target
feature: audiences
topic: Standard
uuid: a9eb62a6-e86a-4e7b-922c-ad87570435ba
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# Aangepaste parameters{#custom-parameters}

Aangepaste parameters zijn parameters mbox. Als u om het even welke mbox parameters tot dozen, of de targetPageParams functie doorgeeft, verschijnen die parameters hier voor gebruik in publiek.

Zie Parameters [doorgeven aan een globale box](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md)voor meer informatie.

Wanneer u een aangepast publiek maakt op basis van een mbox-parameter, vraagt u `mboxParameter` niet meer om `mboxName`. mbox name is nu optioneel. Met deze wijziging kunt u parameters uit meerdere vakken gebruiken of verwijzen naar een parameter die nog niet op de rand is opgenomen.

1. Klik in de [!DNL Target] interface op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Custom]**.

   De gewenste parameter selecteren:

   * Selecteer tijdens het maken van een nieuw publiek een parameternaam in de lijst, typ de eerste tekens van de gewenste parameternaam of typ de volledige naam van de gewenste parameternaam.
   * Als u de naam van het selectievakje, maar niet de naam van de parameter, onthoudt, gebruikt u het selectievakje om te filteren op een bekend selectievakje dat de gewenste parameter doorgeeft.

   Bij beide methoden is er geen koppeling tussen de mbox en de parameter. Het publiek werkt op basis van parameter in alle vakken die die parameter doorgeven.

   Als u een bestaand publiek bewerkt, worden de filtercriteria weergegeven met de naam van de box die tijdens het maken is opgegeven.

1. Kies een beoordelaar:

   * Bevat (hoofdlettergevoelig)
   * Bevat niet (hoofdlettergevoelig)
   * Gelijk

   ![Aangepast parameterpubliek](/help/c-target/c-audiences/c-target-rules/assets/custom.png)

1. Voer elke waarde op een nieuwe regel in.
1. (Optioneel) Klik op aanvullende regels voor het publiek **[!UICONTROL Add Rule]** en stel deze in.
1. Klik op **[!UICONTROL Save]**.

De pop-up kaart [van de](../../../c-target/c-audiences/audiences.md#section_11B9C4A777E14D36BA1E925021945780) definitiedetails van het publiek toont de parameternaam in de sectie van Regels. Er is geen verwijzing naar mbox gebruikt voor het filtreren.

>[!NOTE]
>
>Voor aangepast publiek dat vóór de doelversie 18.5.1 (22 mei 2018) is gemaakt, worden de namen van de box niet weergegeven in de definitie-pop-upkaart van het publiek. U moet het aangepaste publiek opnieuw opslaan om de naam van het selectievakje op de kaart weer te geven.

## Overwegingen {#considerations}

* Soorten publiek en activiteiten worden voor een specifieke box geëvalueerd. Als de globale box bijvoorbeeld een bepaalde parameter doorgeeft, maar de regionale box niet, wordt de activiteit/het publiek die die parameter aanwijst niet gekwalificeerd voor de regionale box.
* Het richten wordt niet geëvalueerd op interne mbox parameters, zoals mboxPC, mboxSession, mbox3rdPartyId, mboxMCSDID, mboxMCAVID, mboxMCGVID, mboxCount, mboxId, en mboxVersion.

## Trainingsvideo: Zelfstudie- ![badge voor soorten publiek maken](/help/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
