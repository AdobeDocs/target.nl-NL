---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Upload een CSV-bestand om uw aanbevelingen aan te passen.
title: Aangepaste criteria uploaden
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 7e94e3f9aae0f710e1dff72c82c1c132bd4239b5

---


# ![PREMIUM](/help/assets/premium.png) Uploaden, aangepaste criteria{#upload-custom-criteria}

Upload een CSV-bestand om uw aanbevelingen aan te passen.

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Wanneer u een [!UICONTROL Recommendations] activiteit creeert, klik **[!UICONTROL Create New]** op het [!UICONTROL Select Criteria] scherm. U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Als u een [!UICONTROL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik op het [!UICONTROL Select Criteria] scherm **[!UICONTROL Create New]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!UICONTROL Recommendations] activiteiten.
* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!UICONTROL Recommendations] activiteiten.

1. Klik op **[!UICONTROL Create Criteria]**.

   ![Nieuwe criteria maken](/help/c-recommendations/c-algorithms/assets/button_CreateCriteria_new.png)

1. Selecteer **[!UICONTROL Upload Custom Criteria]**.

   ![](assets/CreateNewCriteria_csv.png)

1. Typ een **[!UICONTROL Criteria Name]**.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de criteria te beschrijven.  U kunt bijvoorbeeld uw criteria &quot;Hoogste margeproducten&quot; noemen, maar u wilt niet dat die titel openbaar wordt weergegeven. Zie de volgende stap om de naar buiten gerichte titel in te stellen.
1. Typ een openbare verwijzing die op de pagina wordt weergegeven voor alle aanbevelingen die gebruikmaken van deze criteria. **[!UICONTROL Display Title]**

   U kunt bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dit weergegeven&quot; of &quot;Gelijksoortige producten&quot; weergeven wanneer u deze criteria gebruikt om aanbevelingen weer te geven.
1. Typ een korte **[!UICONTROL Description]** van de criteria.

   Aan de hand van deze beschrijving kunt u de criteria vaststellen en informatie over het doel van de criteria toevoegen.
1. Selecteer een **[!UICONTROL Industry Vertical]**.

   Andere criteria kunnen veranderen afhankelijk van de industrie verticaal u selecteert.

1. Selecteer een **[!UICONTROL Page Type]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde criteria te categoriseren, die het gemakkelijker maken om criteria voor andere [!UICONTROL Recommendations] activiteiten opnieuw te gebruiken.
1. Selecteer een **[!UICONTROL Recommendation Key]**.

   Voor meer informatie over het baseren van criteria op een sleutel, zie [Baseer de Aanbeveling op een Sleutel](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_2B0ED54AFBF64C56916B6E1F4DC0DC3B)van de Aanbeveling.
1. Stel uw **[!UICONTROL Content]** regels in.

   De regels van de inhoud bepalen wat gebeurt als het aantal geadviseerde punten uw ontwerp niet vult. Als uw ontwerp bijvoorbeeld ruimte voor vijf items bevat, maar uw criteria slechts drie items aanbevolen, kunt u de resterende ruimte leeg laten of back-upaanbevelingen gebruiken om de extra ruimte te vullen. Selecteer de juiste gereedschappen. Zie [Inhoud-instellingen](../../c-recommendations/c-algorithms/create-new-algorithm.md#concept_BC16005C7A1E4F1A87E33D16221F4A96).
1. Stel uw **[!UICONTROL Inclusion Rules]** waarde in.

   Met insluitingsregels kunt u de items beperken die in uw aanbevelingen worden weergegeven. Zie [Insluitingsregels](../../c-recommendations/c-algorithms/create-new-algorithm.md#task_28DB20F968B1451481D8E51BAF947079). 1. Selecteer het **[!UICONTROL Location]** CSV-bestand.

   Het CSV-bestand moet correct zijn opgemaakt om te kunnen worden geüpload. Klik **[!UICONTROL Download the CSV template]** om een correct geformatteerd Csv- dossier te krijgen.

   U hebt twee locatieopties:

   * **FTP:** Als u uw CSV-bestand vanaf een FTP-server wilt uploaden, selecteert u **[!UICONTROL FTP]** en voert u de vereiste gegevens in. U hebt de optie om SSL te gebruiken, die het protocol van FTPS gebruikt om uw Csv- dossier veilig over te brengen.
   * **URL:** Als u uw CSV-bestand via een URL wilt uploaden, selecteert u **[!UICONTROL URL]** en voert u vervolgens een URL in.

1. Klik op **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Entiteiten met aangepaste criteria (rijen) kunnen maximaal 1000 aanbevolen items (kolommen) bevatten.

Updates van aangepaste criteria zijn standaard &#39;cumulatief&#39;. Nieuwe sleutelwaardeparen die in het CSV-uploadbestand zijn opgegeven, overschrijven bestaande sleutelwaardeparen. Bestaande sleutel-waarde paren die geen sleutels hebben die in CSV uploaden worden gespecificeerd zullen nog voor levering beschikbaar zijn en zullen verlopen over 31 dagen vanaf de tijd zij als deel van het Csv- dossier het laatst worden geupload.

De Zorg van de Cliënt van het contact om het plaatsen toe te laten om de bestaande resultaten te verwerpen die niet inbegrepen in volgende Csv uploaden zijn. Als deze instelling is ingeschakeld, zijn alleen de sleutels in het aangepaste CSV-voederbestand beschikbaar voor levering. Deze instelling is van toepassing op alle aangepaste criteria.

Aangepaste criteria worden elke 24 uur bijgewerkt.

U kunt de upload- en synchronisatiestatus zien van uw aangepaste criteria die u uploadt onder aan elke criteria op de pagina Aanbevelingen > Criteria. De status wordt ook weergegeven in het dialoogvenster Bewerken wanneer u aangepaste criteria bewerkt.

De stroom voor een foutloze upload moet zijn gepland > Feed-bestand downloaden > Importeren > Succesvol.

Het volgende is mogelijke foutmeldingen die u kunt ontvangen als Target een probleem tegenkomt met het uploaden:

| Foutbericht | Details |
|--- |--- |
| Onbekende fout | Geeft een interne technische fout aan. |
| Parseringsfout | Er is waarschijnlijk een probleem met de bestandsindeling feed. Corrigeer de bestandsindeling en sla het algoritme opnieuw op. Hiermee wordt het downloadproces van het bestand opnieuw gestart. |
| Server niet gevonden | Geef een IP- of hostnaam op die op internet zichtbaar is. |
| Credentials-fout | Geef een geldige gebruiker en een geldig wachtwoord op voor een actieve account op de server. |
| Map niet gevonden | Geef een map op die op de server bestaat. |
| Bestand niet gevonden | Geef de naam op van een bestand dat op de server in de aangegeven directory staat. |

## Trainingsvideo: Criteria maken in ![zelfstudie voor aanbevelingen (12:33)](/help/assets/tutorial.png)

Deze video bevat de volgende informatie (details over het uploaden van aangepaste criteria beginnen om 11:43):

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)