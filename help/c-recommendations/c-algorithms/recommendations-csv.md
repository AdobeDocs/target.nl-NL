---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Upload een CSV-bestand om uw aanbevelingen aan te passen.
title: Aangepaste criteria uploaden
feature: Recommendations
translation-type: tm+mt
source-git-commit: 7b86db4b45f93a3c6169caf81c2cd52236bb5a45
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---


# ![Aangepaste criteria ](/help/assets/premium.png) PREMIUMUpload{#upload-custom-criteria}

Upload een CSV-bestand om uw aanbevelingen aan te passen.

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations]-activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit gebruikend [!UICONTROL Visual Experience Composer] (VEC) creeert, wordt u onmiddellijk genomen aan het [!UICONTROL Select Criteria] scherm nadat u een element op uw pagina selecteert en [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After] klikt. U kunt dan een beschikbare criteria selecteren of u kunt **[!UICONTROL Create Criteria]** klikken. Als u nieuwe criteria creeert, hebt u de optie om uw criteria voor gebruik met andere [!DNL Recommendations] activiteiten te bewaren. Zie [Een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) voor meer informatie.
* Wanneer u een [!DNL Recommendations] activiteit uitgeeft, klik in [!UICONTROL Recommendations Location] doos op uw pagina, en selecteer **[!UICONTROL Change Criteria]**. Klik op [!UICONTROL Select Criteria] in het scherm **[!UICONTROL Create Criteria]**. U hebt de optie om uw nieuwe criteria voor gebruik met andere [!DNL Recommendations] activiteiten te bewaren.

In de volgende stappen wordt ervan uitgegaan dat u het scherm [!UICONTROL Create New Criteria] opent met de eerste methode: het **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Upload Custom Criteria]**.

1. Vul de gegevens in de sectie [Basisinformatie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) in.

1. Vul de informatie in [Gegevensbron](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) sectie in.

1. Vul de informatie in de sectie [Inhoud](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) in.

1. (Voorwaardelijk) Vul de informatie in de sectie [Vergelijkbare inhoud](/help/c-recommendations/c-algorithms/create-new-algorithm.md#similarity) in.

1. (Voorwaardelijk) Vul de informatie in [Regels voor opname](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) sectie in.

1. (Voorwaardelijk) Vul de informatie in [Kenmerkweging](/help/c-recommendations/c-algorithms/create-new-algorithm.md#weighting) sectie in.

1. Selecteer in de sectie **[!UICONTROL Upload CSV]** de **[!UICONTROL Location]** van het CSV-bestand.

   ![CSV-sectie uploaden](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

   Het CSV-bestand moet correct zijn opgemaakt om te kunnen worden geüpload. Klik **[!UICONTROL Download the CSV template]** om een correct geformatteerd Csv- dossier te krijgen.

   U hebt twee locatieopties:

   * **FTP:** Als u uw CSV-bestand vanaf een FTP-server wilt uploaden, selecteert u  **[!UICONTROL FTP]** en voert u de vereiste gegevens in. U hebt de optie om SSL te gebruiken, die het protocol van FTPS gebruikt om uw Csv- dossier veilig over te brengen.
   * **URL:** Als u uw CSV-bestand via een URL wilt uploaden, selecteert u  **[!UICONTROL URL]** en voert u vervolgens een URL in.

1. Klik op **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Entiteiten met aangepaste criteria (rijen) kunnen maximaal 1000 aanbevolen items (kolommen) bevatten.

Updates van aangepaste criteria zijn standaard &#39;cumulatief&#39;. Nieuwe sleutelwaardeparen die in het CSV-uploadbestand zijn opgegeven, overschrijven bestaande sleutelwaardeparen. Bestaande sleutel-waarde paren die geen sleutels hebben die in CSV uploaden worden gespecificeerd zullen nog voor levering beschikbaar zijn en zullen verlopen over 31 dagen vanaf de tijd zij als deel van het Csv- dossier het laatst worden geupload.

De Zorg van de Cliënt van het contact om het plaatsen toe te laten om de bestaande resultaten te verwerpen die niet inbegrepen in volgende Csv uploaden zijn. Als deze instelling is ingeschakeld, zijn alleen de sleutels in het aangepaste CSV-voederbestand beschikbaar voor levering. Deze instelling is van toepassing op alle aangepaste criteria.

Aangepaste criteria worden elke 24 uur bijgewerkt.

U kunt de upload- en synchronisatiestatus van uw aangepaste criteria bekijken onder aan elke criteria-kaart op de pagina Recommendations > Criteria. De status wordt ook weergegeven in het dialoogvenster Bewerken wanneer u aangepaste criteria bewerkt.

De stroom voor een foutloze upload moet zijn gepland > Feed-bestand downloaden > Importeren > Succesvol.

Hieronder volgen mogelijke foutberichten die u kunt ontvangen als [!DNL Target] een probleem tegenkomt met het uploaden:

| Foutbericht | Details |
|--- |--- |
| Onbekende fout | Geeft een interne technische fout aan. |
| Parseringsfout | Er is waarschijnlijk een probleem met de bestandsindeling feed. Corrigeer de bestandsindeling en sla het algoritme opnieuw op. Hiermee wordt het downloadproces van het bestand opnieuw gestart. |
| Server niet gevonden | Geef een IP- of hostnaam op die op internet zichtbaar is. |
| Credentials-fout | Geef een geldige gebruiker en een geldig wachtwoord op voor een actieve account op de server. |
| Map niet gevonden | Geef een map op die op de server bestaat. |
| Bestand niet gevonden | Geef de naam op van een bestand dat op de server in de aangegeven directory staat. |

## Trainingsvideo: Criteria maken in Recommendations (12:33) ![Zelfstudie badge](/help/assets/tutorial.png)

Deze video bevat de volgende informatie (details over het uploaden van aangepaste criteria beginnen om 11:43):

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)