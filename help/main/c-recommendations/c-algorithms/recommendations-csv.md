---
keywords: maken, aangepaste criteria;algoritmen;criteria;aanbevelingen, criteria;csv;ftp;upload csv
description: Leer hoe u een CSV-bestand kunt uploaden om uw aanbevelingen in Adobe aan te passen [!DNL Target] Recommendations.
title: Hoe upload ik aangepaste criteria in Recommendations?
feature: Recommendations
exl-id: 33434121-e0ae-4b82-b1dd-78b9738026cb
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 1%

---

# ![PREMIUM](/help/main/assets/premium.png) Aangepaste criteria uploaden

Upload een CSV-bestand om uw aanbevelingen aan te passen in [!DNL Adobe Target].

Er zijn meerdere manieren om de [!UICONTROL Create New Criteria] scherm. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Op de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm, klik **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations] activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit met behulp van de [!UICONTROL Visual Experience Composer] (VEC), wordt u onmiddellijk naar de [!UICONTROL Select Criteria] het scherm nadat u een element op uw pagina selecteert en klikt [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After]. U kunt vervolgens een van de beschikbare criteria selecteren of op **[!UICONTROL Create Criteria]**. Als u nieuwe criteria maakt, kunt u uw criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten. Zie voor meer informatie [Een Recommendations-activiteit maken](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Wanneer u een [!DNL Recommendations] activiteit, klik in [!UICONTROL Recommendations Location] op de pagina en selecteer **[!UICONTROL Change Criteria]**. Op de [!UICONTROL Select Criteria] scherm, klikken **[!UICONTROL Create Criteria]**. U kunt uw nieuwe criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten.

De volgende stappen veronderstellen u tot [!UICONTROL Create New Criteria] scherm met de eerste methode: de **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** bibliotheekscherm.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]**.

1. Vul de gegevens in in de [Basisinformatie](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) sectie.

   1. Van de **[!UICONTROL Select Algorithm]** Vervolgkeuzelijst Type, selecteer **[!UICONTROL Custom Criteria]**.

   1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Algorithm]** de optie **[!UICONTROL Custom Algorithm]**.

      >[!NOTE]
      >
      >De volgende stappen veroorzaken [!UICONTROL Upload CSV] sectie die onder aan het dialoogvenster moet worden weergegeven [!UICONTROL Create New Criteria] in.

1. (Voorwaardelijk) Vul de informatie in in de [Back-upinhoud](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#content) sectie.

1. (Voorwaardelijk) Vul de informatie in in de [Opnameregels](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#inclusion) sectie.

1. In de **[!UICONTROL Upload CSV]** selecteert u de **[!UICONTROL Location]** van uw CSV-bestand.

   ![CSV-sectie uploaden](assets/upload-csv.png)

   Het CSV-bestand moet correct zijn opgemaakt om te kunnen worden geüpload. Klikken **[!UICONTROL Download the CSV template]** om een CSV-bestand met de juiste indeling te verkrijgen.

   U hebt twee locatieopties:

   * **FTP:** Als u uw CSV-bestand vanaf een FTP-server wilt uploaden, selecteert u **[!UICONTROL FTP]** Voer vervolgens de vereiste gegevens in. U kunt SSL gebruiken, dat het protocol van FTPS gebruikt om uw Csv- dossier veilig over te brengen.
   * **URL:** Als u uw CSV-bestand via een URL wilt uploaden, selecteert u **[!UICONTROL URL]** Voer vervolgens een feed-URL in.

1. Klik op **[!UICONTROL Save]**.

## Overwegingen

* Entiteiten met aangepaste criteria (rijen) kunnen maximaal 1000 aanbevolen items (kolommen) bevatten.

* Updates van aangepaste criteria zijn standaard &#39;cumulatief&#39;. Nieuwe sleutelwaardeparen die in het CSV-uploadbestand zijn opgegeven, overschrijven bestaande sleutelwaardeparen. Bestaande sleutel-waarde paren die geen sleutels hebben die in CSV worden gespecificeerd uploaden zijn nog beschikbaar voor levering en verlopen in 31 dagen vanaf de tijd zij als deel van het Csv- dossier het laatst worden geupload.

   De Zorg van de Cliënt van het contact om het plaatsen toe te laten om de bestaande resultaten te verwerpen die niet inbegrepen in volgende Csv uploaden zijn. Als deze instelling is ingeschakeld, zijn alleen de sleutels in het aangepaste CSV-voederbestand beschikbaar voor levering. Deze instelling is van toepassing op alle aangepaste criteria.

* Aangepaste criteria worden elke 24 uur bijgewerkt.

   U kunt de status van uploaden en synchroniseren van uw aangepaste criteria onder aan elke criteria bekijken op de [!UICONTROL Recommendations] > [!UICONTROL Criteria] pagina. U kunt de status ook zien in het dialoogvenster [!UICONTROL Edit] wanneer u aangepaste criteria bewerkt.

* De stroom voor een foutloze upload moet [!UICONTROL Scheduled] > [!UICONTROL Downloading Feed File] > [!UICONTROL Importing] > [!UICONTROL Successful].

* Hieronder volgen mogelijke foutberichten die u ontvangt als [!DNL Target] Er is een probleem opgetreden met het uploaden:

   | Foutbericht | Details |
   |--- |--- |
   | Onbekende fout | Geeft een interne technische fout aan. |
   | Parseringsfout | Er is waarschijnlijk een probleem met de bestandsindeling feed. Corrigeer de bestandsindeling en sla het algoritme opnieuw op, waardoor het downloadproces van het bestand opnieuw wordt gestart. |
   | Server niet gevonden | Geef een IP- of hostnaam op die op internet zichtbaar is. |
   | Credentials-fout | Geef een geldige gebruiker en een geldig wachtwoord op voor een actieve account op de server. |
   | Map niet gevonden | Geef een map op die op de server bestaat. |
   | Bestand niet gevonden | Geef de naam op van een bestand dat op de server in de aangegeven directory staat. |

## Trainingsvideo: Criteria maken in Recommendations (12:33) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat de volgende informatie (details over het uploaden van aangepaste criteria beginnen om 11:43):

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)
