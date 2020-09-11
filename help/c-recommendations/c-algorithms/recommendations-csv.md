---
keywords: creating custom criteria;algorithms;criteria;recommendations criteria;csv;ftp;upload csv
description: Upload een CSV-bestand om uw aanbevelingen aan te passen.
title: Aangepaste criteria uploaden
feature: criteria
uuid: e0b4d320-db00-43ad-b49e-ce36c8532320
translation-type: tm+mt
source-git-commit: 381c405e55475f2474881541698d69b87eddf6fb
workflow-type: tm+mt
source-wordcount: '1794'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Uploaden, aangepaste criteria{#upload-custom-criteria}

Upload een CSV-bestand om uw aanbevelingen aan te passen.

## Het scherm Nieuwe criteria maken openen

Er zijn meerdere manieren om het [!UICONTROL Create New Criteria] scherm te bereiken. Sommige schermopties variëren afhankelijk van de manier waarop u het scherm bereikt.

* Klik in het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**. De criteria die u hier maakt, worden automatisch beschikbaar gesteld voor alle [!DNL Recommendations] activiteiten.
* Wanneer u een [!DNL Recommendations] activiteit gebruikend [!UICONTROL Visual Experience Composer] (VEC) creeert, wordt u onmiddellijk genomen aan het [!UICONTROL Select Criteria] scherm nadat u een element op uw pagina selecteert en klikt [!UICONTROL Replace w/ Recommendations], [!UICONTROL Insert Recommendations Before], of [!UICONTROL Insert Recommendations After]. U kunt dan een beschikbare criteria selecteren of u kunt klikken **[!UICONTROL Create Criteria]**. Als u nieuwe criteria maakt, kunt u uw criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten. Zie Een Recommendations-activiteit [maken voor meer informatie](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md).
* Als u een [!DNL Recommendations] activiteit bewerkt, klikt u in een [!UICONTROL Recommendations Location] vak op de pagina en selecteert u **[!UICONTROL Change Criteria]**. Klik op het [!UICONTROL Select Criteria] scherm **[!UICONTROL Create Criteria]**. U kunt de nieuwe criteria opslaan voor gebruik met andere [!DNL Recommendations] activiteiten.

In de volgende stappen wordt ervan uitgegaan dat u het [!UICONTROL Create New Criteria] scherm opent met de eerste methode: het scherm **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** Bibliotheek.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Upload Custom Criteria]**.

1. Configureer de informatie in de volgende secties.

## Basisinformatie {#info}

1. Typ een **[!UICONTROL Criteria Name]**.

   Dit is de &quot;interne&quot;naam die wordt gebruikt om de criteria te beschrijven. U kunt bijvoorbeeld uw criteria &quot;Hoogste margeproducten&quot; noemen, maar u wilt niet dat die titel openbaar wordt weergegeven. Zie de volgende stap om de naar buiten gerichte titel in te stellen.

   ![Sectie Basisinformatie](/help/c-recommendations/c-algorithms/assets/basic-information.png)

1. Typ een openbare verwijzing die op de pagina wordt weergegeven voor alle aanbevelingen die gebruikmaken van deze criteria. **[!UICONTROL Display Title]**

   U kunt bijvoorbeeld &quot;Personen die dit hebben bekeken, hebben dit weergegeven&quot; of &quot;Gelijksoortige producten&quot; weergeven wanneer u deze criteria gebruikt om aanbevelingen weer te geven.

1. Typ een korte **[!UICONTROL Description]** van de criteria.

   Aan de hand van deze beschrijving kunt u de criteria vaststellen en informatie over het doel van de criteria toevoegen.

1. Selecteer de industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

   | Verticale industrie | Goal |
   |--- |--- |
   | Detailhandel/e-handel | Conversie die tot aankoop leidt |
   | Genereren van leads/B2B/Financiële services | Omzetten zonder aankoop |
   | Media/Publiceren | Betrokkenheid |

   Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert.

1. Selecteer een **[!UICONTROL Page Type]**.

   U kunt meerdere paginatypen selecteren.

   Samen, worden de industrie verticale en paginatypes gebruikt om uw bewaarde criteria te categoriseren, die het gemakkelijker maken om criteria voor andere [!DNL Recommendations] activiteiten opnieuw te gebruiken.

1. Selecteer een **[!UICONTROL Recommendation Key]**.

   Voor meer informatie over het baseren van criteria op een sleutel, zie de aanbeveling [baseren op een aanbeveling sleutel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

1. Selecteer de **[!UICONTROL Recommendation Logic]**.

   Zie [Criteria](../../c-recommendations/c-algorithms/algorithms.md)voor meer informatie over de opties van de aanbevolen logica.

   >[!NOTE]
   >
   >Als u **[!UICONTROL Items]**/ **[!UICONTROL Media with Similar Attributes]** selecteert, kunt u regels [voor gelijkenis van de](#similarity)inhoud instellen.

## Inhoud {#content}

De regels van de inhoud bepalen wat gebeurt als het aantal geadviseerde punten uw [aanbevelingen ontwerp](/help/c-recommendations/c-design-overview/design-overview.md)niet vult. Het is mogelijk dat [!DNL Recommendations] criteria minder aanbevelingen teruggeven dan uw ontwerp vraagt. Als uw ontwerp bijvoorbeeld sleuven voor vier items bevat, maar uw criteria slechts twee items aanbevolen laten, kunt u de resterende sleuven leeg laten of back-upaanbevelingen gebruiken om de extra sleuven te vullen.

![Sectie Inhoud](/help/c-recommendations/c-algorithms/assets/content.png)

1. (Optioneel) Sleep de **[!UICONTROL Partial Design Rendering]** schakeloptie naar de positie &quot;aan&quot;.

   Er worden zoveel mogelijk sleuven ingevuld, maar in de ontwerpsjabloon kan lege ruimte voor de resterende sleuven zijn opgenomen. Als deze optie is uitgeschakeld en er onvoldoende inhoud is om alle beschikbare sleuven te vullen, worden geen aanbevelingen gedaan en wordt in plaats daarvan standaardinhoud weergegeven.

   Schakel deze optie in als u wilt dat aanbevelingen worden gedaan met lege sleuven. Gebruik back-upaanbevelingen als u wilt dat de aanbevolen sleuven worden gevuld met inhoud op basis van uw criteria met lege sleuven die zijn gevuld met vergelijkbare of populaire inhoud van uw site, zoals in de volgende stap wordt uitgelegd.

1. (Optioneel) Sleep de **[!UICONTROL Show Backup Recommendations]** schakeloptie naar de positie &quot;aan&quot;.

   Vul eventueel resterende lege sleuven in het ontwerp met een willekeurige selectie van de meest bekeken producten van de hele site.

   Het gebruik van aanbevelingen voor back-ups zorgt ervoor dat het ontwerp van uw aanbeveling alle beschikbare sleuven vult. Stel dat u een ontwerp van 4 x 1 hebt, zoals hieronder wordt geïllustreerd:

   ![4 x 1 ontwerp](/help/c-recommendations/c-design-overview/assets/velocity_example.png)

   Op basis van uw criteria worden slechts twee objecten aanbevolen. Als u de [!UICONTROL Partial Design Rendering] optie inschakelt, worden de eerste twee sleuven gevuld, maar blijven de resterende twee sleuven leeg. Als u de [!UICONTROL Show Backup Recommendations] optie echter inschakelt, worden de eerste twee sleuven gevuld op basis van uw opgegeven criteria en worden de resterende twee sleuven gevuld op basis van uw aanbevelingen voor back-up.

   De volgende matrix toont het resultaat dat u zult waarnemen wanneer u de opties [!UICONTROL Partial Design Rendering] en [!UICONTROL Backup Recommendations] opties gebruikt:

   | Gedeeltelijke rendering van ontwerp | Backup Recommendations | Resultaat |
   |--- |--- |--- |
   | Uitgeschakeld | Uitgeschakeld | Als er minder aanbevelingen worden geretourneerd dan door het ontwerp wordt gevraagd, wordt het ontwerp van de aanbevelingen vervangen door de standaardinhoud en worden er geen aanbevelingen weergegeven. |
   | Ingeschakeld | Uitgeschakeld | Het ontwerp wordt teruggegeven, maar kan lege ruimte omvatten als minder aanbevelingen zijn teruggekeerd dan het ontwerp verzoekt. |
   | Ingeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp gedeeltelijk teruggegeven.<br>Als de criteria geen aanbevelingen terugkeren, en de integratieregels reserveaanbevelingen tot nul beperken, wordt het ontwerp vervangen met standaardinhoud. |
   | Uitgeschakeld | Ingeschakeld | Back-upaanbevelingen vullen de beschikbare &quot;sleuven&quot; van het ontwerp volledig in.<br>Als het toepassen van inclusieregels op reserveaanbevelingen het aantal kwalificerende reserveaanbevelingen tot het punt beperkt dat het ontwerp niet kan worden gevuld, wordt het ontwerp vervangen door standaardinhoud en geen aanbevelingen worden getoond. |

   Zie [Een back-upaanbeveling](/help/c-recommendations/c-algorithms/backup-recs.md)gebruiken voor meer informatie.

1. (Voorwaardelijk) Als u **[!UICONTROL Show Backup Recommendations]** in de vorige stap selecteerde, kunt u toelaten **[!UICONTROL Apply inclusion rules to backup recommendations]**.

   In de insluitingsregels wordt bepaald welke items in uw aanbevelingen worden opgenomen. Welke opties beschikbaar zijn, is afhankelijk van de verticale situatie in uw branche.

   Zie [Opnameregels](#inclusion) hieronder opgeven voor meer informatie.

1. (Optioneel) Sleep de **[!UICONTROL Recommend Previously Purchased Items]** schakeloptie naar de positie &quot;aan&quot;.

   Deze instelling is gebaseerd op de `productPurchasedId`sjabloon. Standaard wordt eerder aangeschafte items niet aanbevolen. In de meeste gevallen wilt u geen objecten promoten die een klant onlangs heeft aangeschaft. Het is handig om objecten te verkopen die mensen doorgaans slechts eenmaal kopen, zoals kajaks. Als je objecten verkoopt die mensen herhaaldelijk kunnen kopen, zoals shampoo of andere persoonlijke objecten, moet je deze optie inschakelen.

## Opnameregels {#inclusion}

Met behulp van verschillende opties kunt u de items beperken die in uw aanbevelingen worden weergegeven. U kunt inclusieregels gebruiken terwijl het creëren van criteria of bevorderingen.

![Opnameregels](/help/c-recommendations/c-algorithms/assets/inclusion-rules.png)

Opnameregels zijn facultatief; nochtans, geeft het plaatsen van deze details u meer controle over de punten die in uw aanbevelingen verschijnen. Elk detail dat u vormt vernauwt verder de vertoningscriteria.

U kunt er bijvoorbeeld voor kiezen alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar. U kunt ook elk kenmerk van elkaar voorzien, zodat de items die voor uw bedrijf belangrijker zijn, meestal worden weergegeven.

U kunt er ook voor kiezen om vacatures weer te geven voor bezoekers die uw site alleen vanuit bepaalde steden bezoeken en die de vereiste universitaire graden hebben.

De opties voor de inclusieregel variëren per verticale branche. Standaard worden inclusieregels toegepast op back-upaanbevelingen.

>[!IMPORTANT]
>
>U moet opnemingsregels voorzichtig gebruiken. Ze zijn bijvoorbeeld handig als uw organisatie regels heeft die vereisen dat één merk niet wordt aanbevolen terwijl een ander merk wordt weergegeven. Er zijn echter alternatieve kosten voor deze functie. U kunt mogelijk een percentage aan lift verliezen door bepaalde items te beperken zodat ze niet kunnen worden weergegeven wanneer ze normaal gesproken aan de hand van de activiteitscriteria worden weergegeven.

De inclusieregels worden aangesloten bij EN. Aan alle regels moet worden voldaan om een punt in een aanbeveling te omvatten.

Voer de volgende stappen uit om een eenvoudige regel voor insluiting te maken, zoals eerder vermeld, om alleen vrouwenschoenen weer te geven met een voorraad van meer dan 50 en een prijs tussen 25 en 45 dollar:

1. Stel een prijsbereik in voor de producten die u wilt aanbevelen.
1. Stel het minimale voorraadbedrag in voor de producten die u wilt aanbevelen.
1. Vorm de aanbeveling om punten slechts te tonen wanneer zij aan bepaalde criteria voldoen.

   ![](assets/Recs_InclusionRules.png)

   U kunt opgeven dat items alleen worden opgenomen wanneer een van de kenmerken in de lijst voldoet aan een of meer opgegeven voorwaarden of niet overeenkomt.

   De beschikbare beoordelaars zijn afhankelijk van de waarde die u kiest in de eerste vervolgkeuzelijst. U kunt meerdere items weergeven. Deze items worden geëvalueerd met OR.

   De veelvoudige regels worden gecombineerd met EN.

   >[!NOTE]
   >
   >Met deze optie beperkt u de items die in de aanbeveling worden weergegeven. Het heeft geen invloed op de pagina&#39;s waarop de aanbeveling wordt weergegeven. Als u wilt beperken waar de aanbeveling wordt weergegeven, selecteert u de pagina&#39;s in de ervaringscomposer.

Zie [Dynamische en statische inclusieregels](/help/c-recommendations/c-algorithms/use-dynamic-and-static-inclusion-rules.md)gebruiken voor meer informatie.

## CSV uploaden

1. Selecteer het **[!UICONTROL Location]** CSV-bestand.

   ![CSV-sectie uploaden](/help/c-recommendations/c-algorithms/assets/upload-csv.png)

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

U kunt de upload- en synchronisatiestatus van uw aangepaste criteria bekijken onder aan elke criteria-kaart op de pagina Recommendations > Criteria. De status wordt ook weergegeven in het dialoogvenster Bewerken wanneer u aangepaste criteria bewerkt.

De stroom voor een foutloze upload moet zijn gepland > Feed-bestand downloaden > Importeren > Succesvol.

Hieronder ziet u mogelijke foutberichten die u kunt ontvangen als er een probleem [!DNL Target] optreedt met het uploaden:

| Foutbericht | Details |
|--- |--- |
| Onbekende fout | Geeft een interne technische fout aan. |
| Parseringsfout | Er is waarschijnlijk een probleem met de bestandsindeling feed. Corrigeer de bestandsindeling en sla het algoritme opnieuw op. Hiermee wordt het downloadproces van het bestand opnieuw gestart. |
| Server niet gevonden | Geef een IP- of hostnaam op die op internet zichtbaar is. |
| Credentials-fout | Geef een geldige gebruiker en een geldig wachtwoord op voor een actieve account op de server. |
| Map niet gevonden | Geef een map op die op de server bestaat. |
| Bestand niet gevonden | Geef de naam op van een bestand dat op de server in de aangegeven directory staat. |

## Trainingsvideo: Criteria maken in Recommendations (12:33) - ![Zelfstudie](/help/assets/tutorial.png)

Deze video bevat de volgende informatie (details over het uploaden van aangepaste criteria beginnen om 11:43):

* Criteria maken
* Criteria-reeksen maken
* Aangepaste criteria uploaden

>[!VIDEO](https://video.tv.adobe.com/v/27694?quality=12)