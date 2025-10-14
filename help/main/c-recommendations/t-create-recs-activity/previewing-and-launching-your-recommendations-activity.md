---
keywords: Aanbevelingen;aanbieding;voorvertoning;start;status;criteria;algoritme
description: Leer hoe te om uw activiteit van de Aanbevelingen van Adobe  [!DNL Target]  te voorproef om resultaten te verzekeren beschikbaar zijn alvorens de activiteit te lanceren.
title: Hoe kan ik een activiteit met aanbevelingen voorvertonen en starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 26b0c5455e82014dab92c925ecc88bddb3947d2f
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 0%

---

# Activiteiten van uw aanbevelingen voorvertonen en starten

Nadat u uw [!UICONTROL Recommendations] hebt gecreeerd, [!UICONTROL A/B Test], of [!UICONTROL Experience Targeting] (XT) activiteit die [&#x200B; aanbiedingen van Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md) bevat, zult u voorproef uw aanbevelingen willen ervoor zorgen dat de resultaten beschikbaar zijn alvorens de activiteit te lanceren. [!DNL Target Recommendations] biedt meerdere manieren om een voorbeeld van uw aanbevelingen te bekijken.

## Status van algoritme voor aanbevelingen controleren

Nadat [!DNL Recommendations] een activiteit heeft gemaakt, wordt een algoritme uitgevoerd om aanbevelingen te genereren. Dit algoritme kan een paar uur duren.

U kunt controleren of het algoritme in het [!UICONTROL Activity] overzichtsdiagram is gebeëindigd, waar de status van de criteria wordt vermeld. De volgende afbeelding toont de status in het activiteitsdiagram op de pagina [!DNL Recommendations] van een [!UICONTROL Overview] activiteit:

![&#x200B; pagina van het Overzicht van de activiteit van Aanbevelingen &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview-new.png)

De statusresultaten zijn als volgt:

* [!UICONTROL Results Ready]: geeft aan dat het algoritme resultaten heeft geretourneerd
* [!UICONTROL Results Not Ready]: geeft aan dat het algoritme niet is voltooid.
* [!UICONTROL Feed Failure]: geeft aan dat het feed-bestand met aangepaste criteria niet kan worden opgehaald.

![&#x200B; de dialoogdoos van Resultaten &#x200B;](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Hoe lang duurt het om het algoritme uit te voeren?

Nadat u een activiteit met criteria hebt opgeslagen, berekent [!DNL Target] aanbevelingen op basis van de geselecteerde verzameling, criteria, ontwerp en promoties. Deze berekening duurt enige tijd en het tijdsbestek verschilt op basis van de geselecteerde aanbevelingen logica, gegevensbereik, het aantal items in de catalogus, de hoeveelheid gedragsgegevens die uw klanten hebben gegenereerd en de geselecteerde gegevensbron voor gedragsgegevens.

De gedragsgegevensbron heeft het grootste effect op verwerkingstijd, als volgt:

### mboxes

Als vakjes als gedragsgegevensbron worden geselecteerd, zodra gecreeerd, loopt de criteria onmiddellijk. Afhankelijk van de hoeveelheid gebruikte gedragsgegevens en de grootte van de catalogus kan het uitvoeren van het algoritme maximaal 12 uur duren. Als u wijzigingen aanbrengt in de configuratie criteria, wordt het algoritme doorgaans opnieuw uitgevoerd. Afhankelijk van de aangebrachte wijziging zijn de eerder berekende aanbevelingen mogelijk pas beschikbaar wanneer een nieuwe uitvoering is voltooid, of voor grotere wijzigingen is alleen de back-up- of standaardinhoud beschikbaar totdat een nieuwe uitvoering is voltooid. Als een algoritme niet wordt gewijzigd, wordt het automatisch opnieuw uitgevoerd door [!DNL Target] om de 12-48 uur, afhankelijk van het geselecteerde gegevensbereik.

### [!DNL Adobe Analytics]

Als de criteria [!DNL Adobe Analytics] als gedragsgegevensbron gebruiken, zodra gecreeerd, hangt de tijd voor criteria beschikbaarheid af van of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria is gebruikt.

* **Eenmalige opstelling van de rapportreeks**: De eerste keer wordt een rapportreeks gebruikt met een bepaald venster van de gegevenswaaierraadpleging, [!DNL Target Recommendations] kan van twee tot zeven dagen nemen om de gedragsgegevens voor de geselecteerde rapportreeks van [!DNL Analytics] volledig te downloaden. Deze tijdlijn is afhankelijk van het laden van het [!DNL Analytics] -systeem.
* **Nieuwe of uitgegeven criteria die een reeds beschikbare rapportreeks** gebruiken: Wanneer het creëren van nieuwe criteria of het uitgeven van een bestaande criteria, als de geselecteerde rapportreeks reeds met [!DNL Target Recommendations], met een gegevenswaaier gelijk aan of minder dan de geselecteerde gegevenswaaier is gebruikt, zijn de gegevens onmiddellijk beschikbaar en geen eenmalig opstelling wordt vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
* **Doorlopende algoritmelooppas**: De stromen van gegevens van [!DNL Analytics] aan [!DNL Target Recommendations] op een dagelijkse basis. Voor de aanbeveling [!UICONTROL Viewed Affinity] geldt dat wanneer een gebruiker bijvoorbeeld een product bekijkt, een aanroep voor het bijhouden van de productweergave wordt doorgegeven aan [!DNL Analytics] dicht bij real-time. De [!DNL Analytics] -gegevens worden [!DNL Target] vroeg op de volgende dag weergegeven en [!DNL Target] voert het algoritme uit binnen minder dan 12 uur.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] vereist geen offline uitgevoerde algoritme en de resultaten zijn onmiddellijk beschikbaar. [!UICONTROL Top Viewed] en [!UICONTROL Top Sellers] algoritmen die zijn gebaseerd op mbox-gegevens leveren over het algemeen zeer snel resultaten op vanwege de eenvoudigere vereiste berekening. Dit kunnen goede opties zijn als u een voorbeeld van een ontwerpwijziging wilt bekijken of wilt bevestigen dat gedragsgegevens correct worden verzameld.

## QA-koppelingen gebruiken om aanbevelingen voor te vertonen

Nadat het algoritme resultaten klaar heeft, kunt u die resultaten voorproef gebruikend de [&#x200B; verbinding QA &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa.md) functionaliteit van [!DNL Adobe Target]. QA-koppelingen zijn beschikbaar in de sectie [!UICONTROL Activity Location] van de overzichtspagina van [!UICONTROL Activity] :

>[!NOTE]
>
>Standaard voegt [!DNL Target] u automatisch toe aan het vereiste publiek voor de koppeling voor kwaliteitscontrole. Als deze het plaatsen wordt uitgezet en uw activiteit het richten regels heeft, moet uw gebruikersprofiel die richten regels ontmoeten om de ervaring te zien die aanbevelingen bevat.

Als u een koppeling QA gebruikt, kunt u de aanbevelingen op uw pagina bekijken:

![&#x200B; Aanbevolen producten &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* De doel-QA-modus is &quot;plakken&quot; en wordt in een cookie opgeslagen. Als u de QA-modus niet afsluit, blijven de resultaten van de QA op de hele site zichtbaar. Om wijze QA weg te gaan, gebruik [&#x200B; bookmarklet &#x200B;](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* In de QA-modus heeft het bladeren door de site geen invloed op de profielen [!UICONTROL Recently Viewed Items] en [!UICONTROL Recently Purchased Items] van uw profiel. Dit gedrag gebeurt door het ontwerp om onopzettelijke verontreiniging van gedragsgegevens van de productie te voorkomen. Als u de resultaten wilt voorvertonen op basis van een [!UICONTROL Recently Viewed Items] - of [!UICONTROL User-Based Recommendations] -criterium, bladert u eerst naar de site buiten de QA-modus en opent u vervolgens met dezelfde sessie een koppeling in de QA-modus.

## De CSV-download gebruiken om aanbevelingen voor te vertonen

In sommige gevallen, zou u de specifieke punten kunnen willen controleren die worden geadviseerd. Dit is vooral handig bij het gebruik van algoritmen zoals [!UICONTROL People Who Viewed This, Viewed That] , waarbij een andere set items wordt aanbevolen afhankelijk van het item dat de gebruiker momenteel bekijkt, en u mogelijk duizenden of miljoenen verschillende items in uw catalogus hebt.

De resultaten zijn pas beschikbaar voor downloaden als de status [!UICONTROL Results Ready] wordt weergegeven voor ten minste één algoritme in de activiteit.

Als u de resultaten voor de voorvertoning wilt downloaden, klikt u op het menupictogram in de rechterbovenhoek van de pagina Activiteiten en klikt u vervolgens op **[!UICONTROL Download data]** .

![&#x200B; de gegevensoptie van de Download &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

Er wordt een CSV-bestand gedownload. Open het venster om de aanbevolen items weer te geven:

![&#x200B; Aanbevolen punten CSV dossier &#x200B;](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Van links naar rechts is een lijst met aanbevolen items, in dit geval de meest bekeken items. De aanbevelingen worden gescheiden door het milieu, in dit geval heeft alleen de productieomgeving aanbevelingen.

Als een asterisk (*) de eerste waarde van een rij is, wijst het op [&#x200B; reservepunten &#x200B;](/help/main/c-recommendations/c-algorithms/backup-recs.md). Back-upitems worden weergegeven als niet alle sleuven in een ontwerp kunnen worden ingevuld door de aanbevolen items van het algoritme (criteria).

Voor andere algoritmenypen die op een zeer belangrijke waarde, zoals [!UICONTROL People Who Viewed This, Viewed That] worden gebaseerd, zijn de zeer belangrijke waarden (d.w.z. de &quot;Deze&quot;punten) vermeld in de meest linkse kolom en de geadviseerde punten (d.w.z. de &quot;die&quot;punten) worden vermeld van links naar rechts in Recommendation_X kolommen.

>[!NOTE]
>
>Downloads van resultaten zijn niet beschikbaar voor activiteiten die een [!UICONTROL User-Based Recommendations] algoritme bevatten. Downloads van resultaten zijn niet beschikbaar voor criteria die de [!UICONTROL Recently-Viewed Items] aanbevelingen logica gebruiken.

### CSV-downloadindeling voor op populariteit gebaseerde en op sleutels gebaseerde algoritmen {#format}

Het CSV-downloadbestand geeft consistent de resultaten weer die zijn gegenereerd na uitvoering van de back-endcriteria.

* **voor populariteit-gebaseerde (niet op sleutel-gebaseerde) algoritmen, omvat het dossier:**

   * Een rij back-upaanbevelingen met * (een sterretje)
   * Aanbevelingen voor een aparte rij op basis van algoritme-instellingen

* **voor op sleutel-gebaseerde algoritmen, omvat het dossier:**

   * Een back-uprij vergelijkbaar met op populariteit gebaseerde algoritmen
   * Meerdere rijen in sleutelwaardeformaat, waarbij de eerste vermelding de product-id van de sleutel is, gevolgd door door door komma&#39;s gescheiden product-id&#39;s die de kandidaten van de aanbeveling vertegenwoordigen

## Activiteit voor aanbevelingen activeren

Klik op het tabblad [!UICONTROL Activity Overview] op de vervolgkeuzepijl Status en selecteer vervolgens **[!UICONTROL Activate]** .

Als uw [!UICONTROL Recommendations] activiteit momenteel in de [!UICONTROL Inactive] staat is, wordt de drop-down lijst geëtiketteerd [!UICONTROL Inactive].

Na een paar seconden tot een paar minuten verandert de status in [!UICONTROL Live] .

U kunt de activiteit ook deactiveren of archiveren gebruikend de zelfde drop-down lijst.

## Onderbrekingen voorkomen bij het wijzigen van aanbevelingen

Als u [!DNL Recommendations] -verzamelingen, -criteria, -promoties of -ontwerpinstellingen wijzigt in een live activiteit, kunnen de resultaten van het algoritme ongeldig worden en wordt de status van een algoritme gewijzigd in [!UICONTROL Results Not Ready] .

Om te voorkomen dat een live activiteit wordt onderbroken, raden we u aan de volgende aanpak te volgen bij het wijzigen van een live activiteit:

1. Dupliceer de oorspronkelijke activiteit (activiteit 1) en de criteria u wilt wijzigen om een nieuwe activiteit (activiteit 2) tot stand te brengen.
1. Breng wijzigingen aan in de gedupliceerde activiteit (activiteit 2) en de criteria en wacht tot het algoritme resultaten genereert.
1. Bekijk een voorvertoning van de nieuwe, gewijzigde activiteit (activiteit 2) en bevestig dat de resultaten naar wens zijn.
1. Activeer de nieuwe activiteit (activiteit 2).
1. De oorspronkelijke activiteit deactiveren (activiteit 1).

Als u historische rapporteringsresultaten in de zelfde activiteit moet behouden, is een alternatieve benadering mogelijk, die in een tijdelijke verstoring van aanbevelingen beschikbaarheid zou kunnen resulteren:

1. Dupliceer de oorspronkelijke activiteit (activiteit 1) en de criteria u wilt wijzigen om een nieuwe activiteit (activiteit 2) tot stand te brengen.
1. Breng wijzigingen aan in de gedupliceerde activiteit (activiteit 2) en de criteria en wacht tot het algoritme resultaten genereert.
1. Bekijk een voorvertoning van de nieuwe, gewijzigde activiteit (activiteit 2) en bevestig dat de resultaten naar wens zijn.
1. Pauzeer de nieuwe, gewijzigde activiteit (activiteit 2) en verander de montages/de criteria aan de originele activiteit (activiteit 1).
1. Geef een voorvertoning weer van de oorspronkelijke activiteit (activiteit 1) en bevestig dat de resultaten naar wens zijn.
1. De oorspronkelijke activiteit opnieuw activeren (activiteit 1).
