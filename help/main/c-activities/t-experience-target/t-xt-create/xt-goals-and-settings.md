---
keywords: activiteit montages;ervaring richtend doelstellingen en montages;xt doelstellingen en montages;ervaring richtend;rapporteringsmontages;doel metriek;afhankelijke succesmetriek;afhankelijke succesmetriek;primair doel;extra metriek;prioriteit;duur;rapporteringsoplossing;doel;publiek voor het melden;Welk succes metrisch moet worden bereikt alvorens deze metrisch te verhogen;Wat zal gebeuren nadat een gebruiker dit doel metrisch ontmoet;nota's
description: Leer hoe u de [!UICONTROL Goals & Settings] pagina in [!DNL Adobe Target] om informatie over de doelstellingen van te specificeren [!UICONTROL Experience Targeting] (XT) activiteit.
title: Hoe geef ik op [!UICONTROL Goals & Settings] in een [!UICONTROL Experience Targeting] Activiteit?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# Doelen en instellingen in [!UICONTROL Experience Targeting] (XT) activiteiten

De [!UICONTROL Goals & Settings] Op deze pagina voert u informatie in over de doelstellingen van de test:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

Welke instellingen beschikbaar zijn, is afhankelijk van het gebruik [!DNL Target] of [!DNL Analytics] als de bron van de rapportage.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

De volgende instellingen zijn beschikbaar:

### [!UICONTROL Objective]

Typ een optionele doelstelling. Het doel kan om het even welke informatie zijn die u en uw teamleden helpt de campagne identificeren.

### [!UICONTROL Priority]

Afhankelijk van uw instellingen worden [!DNL Target] UI en opties voor [!UICONTROL Priority] variëren. U kunt de oudere instellingen van [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High]of u kunt fijnkorrelige prioriteiten inschakelen van 0 tot en met 999.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, is de activiteit met de hoogste prioriteit vertoningen.

Als deze optie niet is ingeschakeld in [!UICONTROL Administration] (standaard) geeft u een prioriteit op: [!UICONTROL Low], [!UICONTROL Medium], of [!UICONTROL High].

Als u fijnkorrelige prioriteiten wilt inschakelen, klikt u op **[!UICONTROL Administration]** > **[!UICONTROL Reporting]** en schakelt u vervolgens de [!UICONTROL Enable Fine-Grained Priorities] aan de positie &quot;Aan&quot;.

Als deze optie is ingeschakeld, geeft u een waarde op tussen 0 en 999:

* 0 = Laag
* 999 = Hoog

Voor activiteiten die in vorige versies van [!DNL Target], [!UICONTROL Low] prioriteit wordt omgezet in 0, [!UICONTROL Medium] wordt omgezet in 5, en [!UICONTROL High] wordt omgezet in 10. U kunt deze waarden desgewenst aanpassen.

>[!NOTE]
>
>Voordat u deze optie kunt uitschakelen nadat u fijnkorrelige prioriteiten hebt gebruikt, moeten alle prioriteiten weer op 0, 5 en 10 worden ingesteld.

### [!UICONTROL Duration]

De activiteit kan beginnen wanneer goedgekeurd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen waarop de activiteit moet eindigen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

De volgende instellingen zijn beschikbaar:

### [!UICONTROL Reporting Source]

Geef op welke oplossingsgegevens worden verzameld:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Als een rapporteringsoplossing in uw wordt gespecificeerd [accountinstellingen](/help/main/administrating-target/reporting.md), wordt de opgegeven oplossing gebruikt en is deze instelling niet zichtbaar.

U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

**[!DNL Adobe Analytics]**: Zie [[!DNL Adobe Analytics] als bron van rapportage voor [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) kennis te nemen van de verschillen tussen de rapporteringsoplossingen en de voordelen van beide.

Als u [!DNL Analytics] als bron van rapportage voor [!DNL Target] (A4T) selecteert u een [!DNL Analytics] te ontvangen rapportsuite [!DNL Target] activiteitsgegevens. Kies eerst een van de opties [!DNL Analytics] bedrijven waaraan uw account is gekoppeld, en selecteer vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich weer aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Een standaard volgende server wordt weergegeven in het dialoogvenster [!UICONTROL Tracking Server] veld. Als u meer dan één volgende server gebruikt, zorg ervoor u de correcte het volgen server in dit gebied omvat. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) voor meer informatie .

**[!DNL Adobe Customer Journey Analytics]**: Zie [[!DNL Target] rapporteren in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) voor meer informatie over de integratie tussen [!DNL Adobe Customer Journey Analytics] en [!DNL Target].

### [!UICONTROL Goal Metric]

Selecteer de actie die een bezoeker heeft ondernomen om het doel te bereiken. Kies bijvoorbeeld een [!UICONTROL Conversion] metrisch, dan plaats de parameters die bepalen wanneer het succes wordt bereikt.

Voor meer informatie over het plaatsen van metriek, zie [Metrisch instellen](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Als de rapporteringsoplossing wordt geplaatst aan [!DNL Analytics], de enige beschikbare doelstelling metrisch is [!UICONTROL Conversion]. [!DNL Analytics] metriek kan niet als doel worden geselecteerd.

Wanneer u uw succesmetrisch selecteert, toont een selecteur. Gebruik deze kiezer om de specificaties voor de succesmetrische gegevens te kiezen.

Indien ingeschakeld, wordt de [!UICONTROL Estimated Value of the Conversion] veld (niet beschikbaar voor [!UICONTROL Page Score] metriek) verstrekt een waarde voor uw doel, maar niet voor andere metriek. Deze waarde schakelt [!DNL Target] een geraamde verhoging van de inkomsten te berekenen. Dit veld is facultatief, maar incrementele inkomsten voor elke metrische waarde zonder inkomsten kunnen niet worden berekend. Voor alle inkomstenmetriek ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], en [!UICONTROL Orders]), [!UICONTROL Revenue per Visitor]. Het gegevenstype is currency.

Na het bereiken van het activiteitendoel, blijft een bezoeker de activiteiteninhoud zien, tenzij die bezoeker voor een prioritaire activiteit kwalificeert. Als de bezoeker het doel opnieuw bereikt, wordt het geteld als een andere conversie. Dit gedrag verschilt van het standaardgedrag in [!DNL Target Classic], die bezoekers als nieuw telde als ze de test opnieuw zien.

### [!UICONTROL Additional Metrics]

Maak aanvullende succeswaarden.

Deze instelling is niet beschikbaar als de rapportoplossing is ingesteld op [!DNL Analytics]. In dit geval worden de maatstaven voor de [!DNL Analytics] rapportsuite wordt toegepast.

### [!UICONTROL Audiences for Reporting]

Standaard tonen rapporten resultaten voor alle gekwalificeerde bezoekers. U kunt rapportdoelgroepen toevoegen om alleen informatie over specifieke doelgroepen weer te geven.

Deze instelling is niet beschikbaar als u [!DNL Analytics] als uw rapportoplossing. Het publiek dat is gedefinieerd voor de [!DNL Analytics] rapportsuite is toegepast.

## [!UICONTROL Other Meta Data]

Typ alle informatie over uw activiteiten die nuttig is voor uzelf of andere teamleden. De [!UICONTROL Notes] is resizable.

## [!UICONTROL Advanced Settings] {#section_E2FE441AFB324E498793ABB025ED9974}

Geavanceerde instellingen zijn beschikbaar voor [!UICONTROL Experience Targeting] maatstaven van het doel.

![Geavanceerde instellingen](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Als u [!DNL Analytics] als uw rapporteringsbron, worden de montages beheerd door [!DNL Analytics] server. De [!UICONTROL Advanced Settings] is niet beschikbaar.

De volgende instellingen zijn beschikbaar:

### [!UICONTROL Which success metric must be reached before incrementing this metric?]

Gebruik deze optie om bezoekers slechts te tellen zoals het bereiken van metrisch succes als zij eerder een verschillend succes metrisch hebben bereikt. Een testconversie is bijvoorbeeld alleen geldig als de bezoeker op de aanbieding klikt of een bepaalde pagina bereikt voordat de conversie plaatsvindt.

U kunt gebiedsdeel op veelvoudige metriek samen met de flexibiliteit verstrekken om te kiezen of metrisch zou moeten worden bereikt of niet voor de telling om worden bereikt te verhogen.

U moet beide (of veelvoudige) succesmetriek bepalen alvorens u één van een andere kunt afhankelijk maken.

De [!UICONTROL Add Dependency] optie staat succesmetrisch toe om te verhogen als een ander succes metrisch is bereikt of niet bereikt.

Een afhankelijkheid toevoegen:

1. Klik op **[!UICONTROL Advanced Settings]**.
2. Klikken **[!UICONTROL Add Dependency]**:

   ![Koppeling voor afhankelijkheid toevoegen](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Sleep de gewenste metriek vanuit het linkerdeelvenster naar het rechterdeelvenster en klik vervolgens op **[!UICONTROL Reached]** om de instelling tussen [!UICONTROL Reached] en [!UICONTROL Not Reached].

   ![Dialoogvenster Metrische afhankelijkheid toevoegen](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

U kunt afhankelijkheden bewerken of verwijderen nadat u deze hebt toegevoegd.

### [!UICONTROL What will happen after a user encounters this goal metric?]

Er zijn drie opties voor wat gebeurt wanneer een bezoeker het doel metrisch bereikt:

* Selecteren [!UICONTROL Increment Count & Keep User in Activity] om op te geven hoe het aantal wordt verhoogd.
* Selecteren [!UICONTROL Increment Count, Release User & Allow Reentry] om de ervaring op te geven die de gebruiker ziet als hij of zij de activiteit opnieuw betreedt.
* Selecteren [!UICONTROL Increment Count, Release User & Bar from Reentry] om op te geven wat de gebruiker te zien krijgt in plaats van de inhoud van de activiteit.

Zie [Succeswaarden](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) voor meer informatie over geavanceerde instellingen.

## Trainingsvideo: Instellingen voor activiteit (3:02)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
