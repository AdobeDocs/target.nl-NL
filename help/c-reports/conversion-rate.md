---
keywords: Targeting
description: De conversiesnelheid, de lift, het vertrouwen (statistische significantie) en het betrouwbaarheidsinterval worden voor elke ervaring gerapporteerd.
title: Omrekeningskoers
topic: Advanced,Standard,Classic
uuid: c42d7683-2eec-4443-9545-5695a122c9de
translation-type: tm+mt
source-git-commit: 32217a752574f671b790880667ac869443778f51
workflow-type: tm+mt
source-wordcount: '1596'
ht-degree: 0%

---


# Omrekeningskoers{#conversion-rate}

De conversiesnelheid, de lift, het vertrouwen (statistische significantie) en het betrouwbaarheidsinterval worden voor elke ervaring gerapporteerd.

In de volgende afbeelding ziet u de diagramkop voor een voorbeeldactiviteit met de gemarkeerde [!UICONTROL Conversion Rate], [!UICONTROL Lift]en [!UICONTROL Confidence] kopteksten.

![](assets/conversion-rate.jpg)

>[!NOTE]
>
>In alle gegevens worden dubbele orders genegeerd als een instructie `orderID` wordt doorgegeven. In het auditrapport worden de genegeerde dubbele orders vermeld.

## Omzetsnelheid {#section_07A36846C4E84D0881906809B9CE5A74}

Hiermee geeft u de mediaan van de conversiesnelheid, het vertrouwen, het interval en het aantal conversies weer.

Kijk bijvoorbeeld naar de volgende rapportkolom Conversiesnelheid:

![](assets/conversion-rate-detail.jpg)

De eerste regel is de besturingservaring. Het toont een 15% omzettingspercentage, met drie omzettingen. De tweede regel, Experience B, toont een 15% conversiesnelheid, met een betrouwbaarheidsinterval van 15,65% of minder en drie conversies.

>[!NOTE]
>
>Momenteel, wordt het betrouwbaarheidsinterval berekend slechts voor binaire metriek.

## Optillen {#section_0F409572C720433D9378092ABC999982}

Vergelijkt de omrekeningskoers voor elke ervaring met controle.

Lift = (Experience CR - Control CR) / Control CR

Als de controle 0 is, is er geen percentagelift.

## Vertrouwen (statistische significantie) {#section_35DB6724813D40C7B0808DE18FE595C1}

Dit aantal vertegenwoordigt de waarschijnlijkheid dat de resultaten zouden worden gedupliceerd als de test opnieuw in werking werd gesteld. Het vertrouwen beloopt tot 100,00% wanneer het vertrouwen 99,995% of meer bedraagt.

Zie [Vertrouwensniveau en Vertrouwensinterval](../c-reports/conversion-rate.md#concept_0D0002A1EBDF420E9C50E2A46F36629B).

## Detailgegevens {#section_30A674731BA6440E9BB93C421BE990EE}

De AOV-, RPV- en verkoopgegevens worden voor elke ervaring weergegeven als u een [plaatsorde](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/orderconfirm-create.md) ( `orderConfirmPage`) box hebt ingevoegd en deze als het conversiemabox hebt geselecteerd.

## Vertrouwensniveau en betrouwbaarheidsinterval {#concept_0D0002A1EBDF420E9C50E2A46F36629B}

Voor elke ervaring worden het betrouwbaarheidsniveau en het betrouwbaarheidsinterval weergegeven.

Conversies en doorlopende variabelen voor op Target gebaseerde metriek, zoals omzet- en betrokkenheidsmetriek, worden als volgt berekend:

* **Conversie:** Ja of nee
* **Alle andere:** Waarden over een bereik

U kunt offlineberekeningen uitvoeren voor Analytics for Target (A4T), maar hiervoor is een stap vereist met gegevens die worden geëxporteerd naar [!DNL Analytics]. Zie &quot;Offlineberekeningen uitvoeren voor Analytics for Target (A4T)&quot; hieronder voor meer informatie.

### Vertrouwensniveau {#section_26FE5E44BDD5478792A65FCFD83DCCDC}

Het *betrouwbaarheidsniveau* wordt voor elke ervaring weergegeven met het donkerdere percentage in de kolom Conversiesnelheid.

![](assets/conf_report.png)  ![](assets/conf_report_detail.png)

Het betrouwbaarheidsniveau, of statistische significantie, geeft aan hoe waarschijnlijk het is dat het succes van een ervaring niet te wijten was aan toeval. Een hoger betrouwbaarheidsniveau geeft aan:

* De ervaring verschilt aanzienlijk van de controle.
* De ervaringsprestaties zijn niet alleen te wijten aan ruis.
* Als u deze test opnieuw uitvoert, is het waarschijnlijk dat u dezelfde resultaten zult zien.

Als het betrouwbaarheidsniveau boven 90% of 95% ligt, kan het resultaat als statistisch significant worden beschouwd. Alvorens om het even welke bedrijfsbesluiten te nemen, probeer om te wachten tot uw steekproefgrootte groot genoeg is en dat de vier bars van vertrouwen op één of meerdere ervaringen voor een ononderbroken tijdsduur verenigbaar blijven om de resultaten te verzekeren stabiel zijn.

>[!NOTE]
>
>Het vertrouwen beloopt tot 100,00% wanneer het vertrouwen 99,995% of meer bedraagt.

### Vertrouwelijk interval {#section_F582738DFE1648C78B93D81EBC6CACF7}

>[!NOTE]
>
>Momenteel, wordt het betrouwbaarheidsinterval berekend slechts voor binaire metriek.

Het *betrouwbaarheidsinterval* is een bereik waarbinnen de werkelijke waarde op een bepaald betrouwbaarheidsniveau kan worden gevonden. Het betrouwbaarheidsinterval wordt weergegeven als een lichtgrijs +/- percentage in de kolom Conversiesnelheid. In het onderstaande voorbeeld is het betrouwbaarheidsinterval voor de lift van Experience B plus of min 15,65%.

![](assets/conversion_rate.png)

**Voorbeeld:** De RPV van een ervaring is $10, zijn betrouwbaarheidsniveau is 95% en zijn **betrouwbaarheidsinterval** is $5 tot $15. Als we deze test meerdere keren zouden uitvoeren, zou 95% van de tijd de RPV tussen $5 en $15 liggen.

**Wat beïnvloedt het vertrouwensinterval?** De formule volgt de statistische standaardmethoden voor de berekening van betrouwbaarheidsintervallen.

* **Voorbeeldformaat:** Als het monster groeit, zal het interval krimpen of smal. Dit wordt geprefereerd aangezien het betekent uw rapporten dichter aan de ware waarde van succes metrisch raken.
* **Standaardafwijking kleiner:** Vergelijkbare resultaten, zoals vergelijkbare AOV&#39;s of vergelijkbare nummers of bezoekers die elke dag converteren, verminderen de standaardafwijking.

## De Berekening van het vertrouwen en hoe te om het off-line uit te voeren {#section_86F7C231943043A5B8B6BFE67B706E3B}

Het [gedownloade CSV-rapport](../c-reports/downloading-data-in-csv-file.md#concept_3F276FF2BBB2499388F97451D6DE2E75) bevat alleen onbewerkte gegevens en bevat geen berekende meetgegevens, zoals inkomsten per bezoeker, lift of betrouwbaarheid die worden gebruikt voor A/B-tests.

Als u deze berekende meetgegevens wilt berekenen, downloadt u het Excel-bestand met de [Complete Trust Calculator](/help/assets/complete_confidence_calculator.xlsx) van Target om de waarde van de activiteit in te voeren of bekijkt u de [statistische berekeningen die Target](/help/assets/statistical-calculations.pdf)gebruikt.

>[!NOTE]
>
>Deze rekenmachine is bedoeld voor Target-gebaseerde rapportage en niet voor A4T-rapportage.

## Offlineberekeningen uitvoeren voor Analytics for Target (A4T) {#section_B34BD016C8274C97AC9564F426B9607E}

U kunt offlineberekeningen voor A4T uitvoeren, maar het vereist een stap met gegevens het uitvoeren binnen [!DNL Analytics].

Voor A4T, gebruiken wij t-test van een Student berekening voor ononderbroken variabelen (eerder dan binaire metriek). In Analytics wordt een bezoeker altijd bijgehouden en wordt elke actie geteld. Daarom als de bezoeker veelvoudige tijden koopt of een succes metrisch veelvoudige tijden bezoekt, worden die extra treffers geteld. Dit maakt metrisch een ononderbroken variabele. Om de t-test berekening van de Student uit te voeren, wordt de &quot;som vierkanten&quot;vereist. Dit kan worden opgehaald van [!DNL Analytics]. Om de som gegevens van vierkanten te krijgen, moet u een bezoekersvlakke uitvoer voor metrisch uitvoeren u aan optimaliseert, voor een steekproeftijdspanne.

Als u bijvoorbeeld optimaliseert voor paginaweergaven per bezoeker, exporteert u een voorbeeld van het totale aantal paginaweergaven per bezoeker voor een bepaald tijdsbestek, misschien een paar dagen (een paar duizend gegevenspunten is alles wat u nodig hebt). Vervolgens vigeert u elke waarde en somt u de totalen op (de volgorde van de bewerkingen is hier van essentieel belang). Deze &quot;som van vierkanten&quot;waarde wordt dan gebruikt in de Volledige Berekening van het Vertrouwen. Gebruik de sectie &quot;opbrengst&quot; van dat spreadsheet voor deze waarden.

**Hiervoor gebruikt u de functie voor het exporteren van[!DNL Analytics]gegevens:**

1. Meld u aan bij [!DNL Adobe Analytics].
1. Klik op **[!UICONTROL Tools]** > **[!UICONTROL Data Warehouse]**.
1. Vul op het **[!UICONTROL Data Warehouse Request]** tabblad de velden in.

   Zie &quot;Data warehouse-beschrijvingen&quot; in [Data warehouse voor meer informatie over elk veld](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse.html).

   | Veld | Instructies |
   |--- |--- |
   | Naam aanvraag | Geef een naam op voor uw aanvraag. |
   | Datum van rapportage | Geef een tijdsperiode en granulariteit op.<br>Als beste praktijken, kies niet meer dan een uur of één dag van gegevens voor uw eerste verzoek.  Het duurt langer om Data warehouse-bestanden te verwerken met een langere periode. Het is dus altijd aan te raden om eerst gegevens over een kleine periode aan te vragen om ervoor te zorgen dat het bestand het gewenste resultaat oplevert. Ga vervolgens naar de Request Manager, dupliceer uw verzoek en vraag de tweede keer om meer gegevens. Ook, als u granularity aan om het even wat buiten &quot;niets&quot;schakelt, zal de dossiergrootte drastisch stijgen.<br>![Data warehouse](/help/c-reports/assets/datawarehouse.png) |
   | Beschikbare segmenten | Pas indien nodig een segment toe. |
   | Uitsplitsingen | Selecteer de gewenste afmetingen:  Standaard is OOTB (out-of-the-box) en Aangepast bevat Vars en props. Je kunt het beste &#39;Bezoeker-id&#39; gebruiken als je informatie op bezoekersidentiteitsniveau nodig hebt in plaats van &#39;Experience Cloud Bezoeker-id&#39;.<ul><li>De bezoeker-id is de laatste id die Analytics gebruikt. Het zal of HULP (als de klant erfenis is) of MID (als de klant nieuwe of ontruimde koekjes is sinds de dienst van bezoekersidentiteitskaart van MC werd gelanceerd) zijn.</li><li>De Experience Cloud Bezoeker-id wordt alleen ingesteld voor klanten die nieuwe of verwijderde cookies zijn sinds de service MC bezoeker-id is gestart.</li></ul> |
   | Metrisch | Selecteer de gewenste meetgegevens. Standaard is OOTB, terwijl Aangepast aangepaste gebeurtenissen bevat. |
   | Voorvertoning van rapport | Controleer uw instellingen voordat u het rapport plant.<br>![Data warehouse 2](/help/c-reports/assets/datawarehouse2.png) |
   | Levering plannen | Voer een e-mailadres in waarnaar het bestand moet worden verzonden, geef het bestand een naam en selecteer [!UICONTROL Send Immediately].<br>Opmerking: Het bestand kan via FTP worden geleverd onder [!UICONTROL Advanced Delivery Options]<br>![Planningslevering](/help/c-reports/assets/datawarehouse3.png). |

1. Klik op **[!UICONTROL Request this Report]**.

   De levering van het dossier kan tot 72 uren, afhankelijk van de gevraagde hoeveelheid gegevens vergen. U kunt de voortgang van uw verzoek op elk gewenst moment controleren door op [!UICONTROL Tools] > [!UICONTROL Data Warehouse] > [!UICONTROL Request Manager]te klikken.

   Als u gegevens die u in het verleden hebt aangevraagd opnieuw wilt aanvragen, kunt u zo nodig een oude aanvraag van het [!UICONTROL Request Manager] bedrijf dupliceren.

Raadpleeg de volgende koppelingen in de documentatie bij de Help voor meer informatie over [!DNL Data Warehouse][!DNL Analytics] :

* [Een Data warehouse-aanvraag maken](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/t-dw-create-request.html)
* [Aanbevolen werkwijzen voor Data warehouse](https://docs.adobe.com/content/help/en/analytics/export/data-warehouse/data-warehouse-bp.html)

## Telmethode {#concept_EC19BC897D66411BABAF2FA27BCE89AA}

U kunt ervoor kiezen om rapporten te bekijken met verschillende telmethoden om te begrijpen hoe uw activiteiten van invloed zijn op uw gebruikers gedurende hun levensduur of tijdens één sessie.

De telmethode wordt ondersteund voor de volgende soorten activiteiten:

* A/B-test

   Bij wijze van uitzondering ondersteunen Auto-Target A/B-activiteiten alleen de standaardmethode voor het tellen van bezoekers.

* Gericht op ervaring (XT)
* MVT (Multivariate Test)

   Voor het MVT Element Contribution Report biedt Target geen ondersteuning voor Activity Impressions for Revenue Metric types.

* Aanbevelingen

Momenteel wordt alleen de standaardtelmethode (Visit) ondersteund voor activiteiten van Automated Personalization (AP).

U kunt rapporten weergeven met de volgende telmethoden:

* **Bezoeker:** Een unieke deelnemer aan de activiteit, gedurende de levensduur van de activiteit.

   Een persoon wordt als nieuwe gegadigde beschouwd als hij of zij de site bezoekt vanuit een nieuwe computer of een nieuwe browser; verwijdert het cookie; of converteert en retourneert de activiteit met dezelfde cookie. Een deelnemer wordt geïdentificeerd door de PCID in het cookie van de bezoeker. Als de PCID verandert, wordt de persoon beschouwd als een nieuwe bezoeker.

* **Bezoek:** Een unieke deelnemer aan een ervaring tijdens een enkele browsersessie van 30 minuten.

   Als een conversie is bereikt of een bezoeker na minimaal 30 minuten weer naar de site terugkeert, telt een terugkerende bezoeker als een nieuw bezoek. Een bezoek wordt geïdentificeerd door de `sessionID` in het koekje van de bezoeker. Wanneer de `sessionID` situatie verandert, wordt het bezoek als nieuw beschouwd.

* **Afdruk-/paginaweergave:** Telkens wanneer een bezoeker een pagina van de activiteit laadt.

   Eén bezoek kan verschillende indrukken van bijvoorbeeld uw homepage bevatten.

>[!NOTE]
>
>Meestal worden tellingen bepaald door cookies en sessieactiviteit. Als u echter het laatste conversiepunt van een activiteit bereikt en vervolgens de activiteit weer betreedt, wordt u beschouwd als een nieuwe deelnemer en een nieuw bezoek aan de activiteit. Dit geldt ook als uw PCID en `sessionID` -waarden niet veranderen.