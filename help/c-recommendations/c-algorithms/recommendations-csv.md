---
keywords: maken, aangepaste criteria;algoritmen;criteria;aanbevelingen, criteria;csv;ftp;upload csv
description: Leer hoe u een CSV-bestand uploadt om uw aanbevelingen aan te passen in Adobe [!DNL Target] Recommendations.
title: Hoe upload ik aangepaste criteria in Recommendations?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 7a52f7c046fb00672ef1b13704308be39f89c7ad
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 1%

---

# ![](/help/assets/premium.png) PREMIUMUpload, aangepaste criteria

Upload een CSV-bestand om uw aanbevelingen in [!DNL Adobe Target] aan te passen.

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. Criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations]-activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit gebruikend [!UICONTROL Visual Experience Composer] (VEC) creeert, wordt u onmiddellijk genomen aan het [!UICONTROL Select Criteria] scherm nadat u een element op uw pagina selecteert en [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After] klikt. U kunt dan een beschikbare criteria selecteren of u kunt **[!UICONTROL Create Criteria]** klikken. Als u nieuwe criteria creeert, kunt u uw criteria voor gebruik met andere [!DNL Recommendations] activiteiten bewaren. Zie [Een Recommendations-activiteit maken](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md) voor meer informatie.
* Wanneer u een [!DNL Recommendations] activiteit uitgeeft, klik in [!UICONTROL Recommendations Location] doos op uw pagina, en selecteer **[!UICONTROL Change Criteria]**. Klik op [!UICONTROL Select Criteria] in het scherm **[!UICONTROL Create Criteria]**. U kunt uw nieuwe criteria voor gebruik met andere [!DNL Recommendations] activiteiten bewaren.

In de volgende stappen wordt ervan uitgegaan dat u het scherm [!UICONTROL Create New Criteria] opent met de eerste methode: het **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]**.

1. Vul de gegevens in de sectie [Basisinformatie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) in.

   1. Selecteer **[!UICONTROL Custom Criteria]** in de vervolgkeuzelijst **[!UICONTROL Select Algorithm]** Type.

   1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Algorithm]** de optie **[!UICONTROL Custom Algorithm]**.

      >[!NOTE]
      >
      >De voorgaande stappen zorgen ervoor dat de sectie [!UICONTROL Upload CSV] onder in het dialoogvenster [!UICONTROL Create New Criteria] wordt weergegeven.

1. (Voorwaardelijk) Vul de informatie in [Backup Content](/help/c-recommendations/c-algorithms/create-new-algorithm.md#content) sectie in.

1. (Voorwaardelijk) Vul de informatie in [Regels voor opname](/help/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) sectie in.

1. Selecteer in de sectie **[!UICONTROL Upload CSV]** de **[!UICONTROL Location]** van het CSV-bestand.

   ![CSV-sectie uploaden](assets/upload-csv.png)

   Het CSV-bestand moet correct zijn opgemaakt om te kunnen worden geüpload. Klik **[!UICONTROL Download the CSV template]** om een correct geformatteerd Csv- dossier te krijgen.

   U hebt twee locatieopties:

   * **FTP:** Als u uw CSV-bestand vanaf een FTP-server wilt uploaden, selecteert u  **[!UICONTROL FTP]** en voert u de vereiste gegevens in. U kunt SSL gebruiken, dat het protocol van FTPS gebruikt om uw Csv- dossier veilig over te brengen.
   * **URL:** Als u uw CSV-bestand via een URL wilt uploaden, selecteert u  **[!UICONTROL URL]** en voert u vervolgens een URL in.

1. Klik op **[!UICONTROL Save]**.

## Overwegingen

* Entiteiten met aangepaste criteria (rijen) kunnen maximaal 1000 aanbevolen items (kolommen) bevatten.

* Updates van aangepaste criteria zijn standaard &#39;cumulatief&#39;. Nieuwe sleutelwaardeparen die in het CSV-uploadbestand zijn opgegeven, overschrijven bestaande sleutelwaardeparen. Bestaande sleutel-waarde paren die geen sleutels hebben die in CSV worden gespecificeerd uploaden zijn nog beschikbaar voor levering en verlopen in 31 dagen vanaf de tijd zij als deel van het Csv- dossier het laatst worden geupload.

   De Zorg van de Cliënt van het contact om het plaatsen toe te laten om de bestaande resultaten te verwerpen die niet inbegrepen in volgende Csv uploaden zijn. Als deze instelling is ingeschakeld, zijn alleen de sleutels in het aangepaste CSV-voederbestand beschikbaar voor levering. Deze instelling is van toepassing op alle aangepaste criteria.

* Aangepaste criteria worden elke 24 uur bijgewerkt.

   U kunt de upload- en synchronisatiestatus zien van uw aangepaste criteria die u uploadt onder aan elke criteria op de pagina [!UICONTROL Recommendations] > [!UICONTROL Criteria]. U kunt de status in het [!UICONTROL Edit] dialoogvakje ook zien wanneer het uitgeven van douanecriteria.

* De stroom voor een foutloze upload moet [!UICONTROL Scheduled] > [!UICONTROL Downloading Feed File] > [!UICONTROL Importing] > [!UICONTROL Successful] zijn.

* Hieronder volgen mogelijke foutberichten die u kunt ontvangen als [!DNL Target] een probleem tegenkomt met het uploaden:

   | Foutbericht | Details |
   |--- |--- |
   | Onbekende fout | Geeft een interne technische fout aan. |
   | Parseringsfout | Er is waarschijnlijk een probleem met de bestandsindeling feed. Corrigeer de bestandsindeling en sla het algoritme opnieuw op, waardoor het downloadproces van het bestand opnieuw wordt gestart. |
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
