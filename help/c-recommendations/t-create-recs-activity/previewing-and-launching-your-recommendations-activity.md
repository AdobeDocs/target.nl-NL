---
keywords: Recommendations;offer;preview;launch;status;criteria;algorithm
description: 'Nadat u de Recommendations-, A/B Test- of Experience Targeting-activiteit (XT) met Adobe Target Recommendations-aanbiedingen hebt gemaakt, wilt u deze eerst bekijken om te controleren of de resultaten beschikbaar zijn voordat u de activiteit start. Target Recommendations biedt meerdere manieren om je aanbevelingen voor te vertonen. '
title: 'Nadat u de Recommendations-, A/B Test- of Experience Targeting-activiteit (XT) met Adobe Target Recommendations-aanbiedingen hebt gemaakt, wilt u deze eerst bekijken om te controleren of de resultaten beschikbaar zijn voordat u de activiteit start. Target Recommendations biedt meerdere manieren om je aanbevelingen voor te vertonen. '
feature: recs creation
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 0%

---


# Recommendations-activiteiten voorvertonen en starten

Nadat u uw [!UICONTROL Recommendations], [!UICONTROL A/B Test], of [!UICONTROL Experience Targeting] (XT) activiteit hebt gecreeerd die [Recommendations aanbiedingen](/help/c-recommendations/recommendations-as-an-offer.md) bevat, zult u uw aanbevelingen willen voorproef om ervoor te zorgen dat de resultaten beschikbaar zijn alvorens de activiteit te lanceren. [!DNL Target Recommendations] biedt meerdere manieren om uw aanbevelingen voor te vertonen.

## Recommendations-algoritmestatus controleren

Na het creëren van een activiteit, [!DNL Recommendations] stelt een algoritme in werking om aanbevelingen te produceren. Dit algoritme kan enkele uren duren.

U kunt controleren of het algoritme het lopen in het [!UICONTROL Activity] overzichtsdiagram heeft gebeëindigd, waar de criteria status vermeld is. De volgende illustratie toont de status in het activiteitendiagram op een [!DNL Recommendations] pagina van de activiteit [!UICONTROL Overview]:

![Pagina Overzicht van Recommendations-activiteiten](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

De volgende afbeelding toont de status op een [!UICONTROL A/B Test]- of XT-pagina van [!UICONTROL Overview]:

![A/B pagina Overzicht van tests](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

De statusresultaten zijn als volgt:

* [!UICONTROL Results Ready]: Geeft aan dat het algoritme resultaten heeft geretourneerd
* [!UICONTROL Results Not Ready]: Geeft aan dat het algoritme niet is voltooid.
* [!UICONTROL Feed Failure]: Geeft aan dat het feed-bestand met aangepaste criteria niet kan worden opgehaald.

![Het dialoogvenster Resultaten](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Hoe lang duurt het om het algoritme uit te voeren?

Nadat u een activiteit hebt opgeslagen die een criterium bevat, berekent [!DNL Target] aanbevelingen op basis van de geselecteerde verzameling, criteria, ontwerp en promoties. Deze berekening duurt enige tijd en het tijdsbestek verschilt op basis van de geselecteerde aanbevelingen logica, gegevensbereik, het aantal items in de catalogus, de hoeveelheid gedragsgegevens die uw klanten hebben gegenereerd en de geselecteerde gegevensbron voor gedragsgegevens.

De gedragsgegevensbron heeft het grootste effect op verwerkingstijd, als volgt:

### mboxes

Als vakjes als gedragsgegevensbron worden geselecteerd, zodra gecreeerd, loopt de criteria onmiddellijk. Afhankelijk van de hoeveelheid gebruikte gedragsgegevens en de grootte van de catalogus kan het uitvoeren van het algoritme maximaal 12 uur duren. Als u wijzigingen aanbrengt in de configuratie criteria, wordt het algoritme doorgaans opnieuw uitgevoerd. Afhankelijk van de aangebrachte wijziging zijn de eerder berekende aanbevelingen mogelijk pas beschikbaar wanneer een nieuwe uitvoering is voltooid, of voor grotere wijzigingen is alleen de back-up- of standaardinhoud beschikbaar totdat een nieuwe uitvoering is voltooid. Als een algoritme niet wordt gewijzigd, wordt het automatisch opnieuw in werking gesteld door [!DNL Target] om de 12-48 uur, afhankelijk van de geselecteerde gegevenswaaier.

### Adobe Analytics

Als de criteria [!DNL Adobe Analytics] als gedragsgegevensbron gebruiken, zodra gecreeerd, hangt de tijd voor criteria beschikbaarheid af van of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria is gebruikt.

* **Eenmalige installatie** van rapportsuite: De eerste keer een rapportreeks met een bepaald venster van de gegevenswaaierraadpleging wordt gebruikt,  [!DNL Target Recommendations] kan van twee tot zeven dagen nemen om de gedragsgegevens voor de geselecteerde rapportreeks volledig te downloaden van  [!DNL Analytics]. Dit tijdframe is afhankelijk van de systeembelasting [!DNL Analytics].
* **Nieuwe of bewerkte criteria met behulp van een reeds beschikbare rapportsuite**: Als bij het maken van nieuwe criteria of het bewerken van bestaande criteria de geselecteerde rapportsuite al is gebruikt met  [!DNL Target Recommendations], met een gegevensbereik dat gelijk is aan of kleiner is dan het geselecteerde gegevensbereik, zijn de gegevens direct beschikbaar en is een eenmalige installatie niet vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
* **Doorlopende algoritme wordt uitgevoerd**: Gegevensstromen van  [!DNL Analytics] naar  [!DNL Target Recommendations] dagelijks. Bijvoorbeeld, voor de [!UICONTROL Viewed Affinity] aanbeveling, wanneer een gebruiker een product bekijkt, wordt een product-mening het volgen vraag overgegaan in [!DNL Analytics] dicht bij real time. De [!DNL Analytics] gegevens worden aan [!DNL Target] begin de volgende dag geduwd en [!DNL Target] stelt het algoritme in minder dan 12 uren in werking.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] vereist geen off-line algoritme looppas en de resultaten zijn onmiddellijk beschikbaar. [!UICONTROL Top Viewed] en  [!UICONTROL Top Sellers] algoritmen die op mbox-gegevens zijn gebaseerd, leveren doorgaans zeer snel resultaten op omdat eenvoudigere berekeningen nodig zijn. Dit kunnen goede opties zijn als u een voorbeeld van een ontwerpwijziging wilt bekijken of wilt bevestigen dat gedragsgegevens correct worden verzameld.

## Een voorbeeld van Recommendations bekijken met QA-koppelingen

Nadat het algoritme resultaten klaar heeft, kunt u voorproef die resultaten gebruikend de [QA verbinding](/help/c-activities/c-activity-qa/activity-qa.md) functionaliteit van [!DNL Adobe Target]. De verbindingen van QA zijn beschikbaar in de [!UICONTROL Activity QA] sectie van de overzichtspagina van de Activiteit:

![QA-koppeling voor activiteit](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standaard voegt [!DNL Target] u automatisch toe aan het vereiste publiek voor de koppeling QA. Als deze het plaatsen wordt uitgezet en uw activiteit het richten regels heeft, moet uw gebruikersprofiel die richten regels ontmoeten om de ervaring te zien die aanbevelingen bevat.

Als u een koppeling QA gebruikt, kunt u de aanbevelingen op uw pagina bekijken:

![Aanbevolen producten](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* De doel-QA-modus is &quot;plakken&quot; en wordt in een cookie opgeslagen. Als u de QA-modus niet afsluit, blijven de resultaten van de QA op de hele site zichtbaar. Als u de QA-modus wilt afsluiten, gebruikt u [bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).
   >
   >
* In de QA-modus heeft het bladeren door de site geen invloed op de [!UICONTROL Recently Viewed Items] of [!UICONTROL Recently Purchased Items] van uw profiel.&quot; Dit gedrag gebeurt door het ontwerp om onopzettelijke verontreiniging van gedragsgegevens van de productie te voorkomen. Als u resultaten wilt voorvertonen op basis van een [!UICONTROL Recently Viewed Items]- of [!UICONTROL User-Based Recommendations]-criterium, bladert u eerst naar de site buiten de QA-modus en opent u vervolgens dezelfde sessie voor een koppeling in de QA-modus.


## De CSV-download gebruiken om aanbevelingen voor te vertonen

In sommige gevallen, zou u de specifieke punten kunnen willen controleren die worden geadviseerd. Dit is met name handig wanneer u algoritmes gebruikt zoals [!UICONTROL People Who Viewed This, Viewed That], waar een andere set items wordt aanbevolen, afhankelijk van het item dat de gebruiker momenteel bekijkt, en waar mogelijk duizenden of miljoenen verschillende items in uw catalogus staan.

De resultaten zijn niet beschikbaar voor download tot een [!UICONTROL Results Ready] status voor minstens één algoritme in de activiteit wordt getoond.

Als u de resultaten voor de voorvertoning wilt downloaden, klikt u op het menupictogram in de rechterbovenhoek van de pagina Activiteiten en klikt u op **[!UICONTROL Download data]**.

![Gegevensoptie downloaden](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

Er wordt een CSV-bestand gedownload. Open het venster om de aanbevolen items weer te geven:

![CSV-bestand met aanbevolen items](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Van links naar rechts is een lijst met aanbevolen items, in dit geval de meest bekeken items. De aanbevelingen worden gescheiden door het milieu, in dit geval heeft alleen de productieomgeving aanbevelingen. Voor dit algoritme, hebben wij geen beperkingen toegepast die op zeer belangrijke waarde worden gebaseerd, zodat bevat de rij geëtiketteerd met een asterisk (*) de volledige reeks aanbevelingen. Voor andere algoritmetypes die op een zeer belangrijke waarde, zoals [!UICONTROL People Who Viewed This, Viewed That] worden gebaseerd, zijn de belangrijkste waarden (d.w.z. de &quot;Deze&quot;punten) vermeld in de meest linkse kolom en de geadviseerde punten (d.w.z. de &quot;die&quot;punten) worden vermeld links-aan-recht in Recommendation_X kolommen.

>[!NOTE]
>
>Downloads van resultaten zijn niet beschikbaar voor activiteiten die een [!UICONTROL User-Based Recommendations] algoritme bevatten. Downloads van resultaten zijn niet beschikbaar voor criteria die [!UICONTROL Recently-Viewed Items] aanbevelingslogica gebruiken.

## Recommendations-activiteit activeren

Klik op het tabblad [!UICONTROL Activity Overview] op de vervolgkeuzepijl naast de status en selecteer **[!UICONTROL Activate]**.

![Optie Activeren](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

De status wordt [!UICONTROL Activating]:

![Activeren](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Na een paar seconden aan een paar notulen, schakelt de status aan [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

U kunt de activiteit ook deactiveren of archiveren met dezelfde vervolgkeuzelijst.

## Onderbrekingen voorkomen bij het wijzigen van Recommendations-instellingen

Als u [!DNL Recommendations] verzamelingen, criteria, promoties of ontwerpinstellingen in een live activiteit wijzigt, worden de resultaten van het algoritme mogelijk ongeldig en verandert de status van een algoritme in [!UICONTROL Results Not Ready].

Om te voorkomen dat een live activiteit wordt onderbroken, raden we u aan de volgende aanpak te volgen bij het wijzigen van een live activiteit:

1. Dupliceer de activiteit en de criteria u wilt wijzigen.
1. Breng wijzigingen aan in de gedupliceerde activiteit en criteria en wacht tot het algoritme resultaten genereert.
1. Bekijk een voorvertoning van de nieuwe, gewijzigde activiteit en bevestig dat de resultaten naar wens zijn.
1. Activeer de nieuwe activiteit.
1. Deactiveer de oude activiteit.

Als u historische rapporteringsresultaten in de zelfde activiteit moet behouden, is een alternatieve benadering mogelijk, die in een tijdelijke verstoring van aanbevelingen beschikbaarheid zou kunnen resulteren:

1. Dupliceer de activiteit en de criteria u wilt wijzigen.
1. Breng wijzigingen aan in de gedupliceerde activiteit en criteria en wacht tot het algoritme resultaten genereert.
1. Bekijk een voorvertoning van de nieuwe, gewijzigde activiteit en bevestig dat de resultaten naar wens zijn.
1. Onderbreek de bestaande activiteit en verander de montages/de criteria aan de nieuwe criteria.
1. Geef een voorvertoning van de bestaande activiteit weer en bevestig dat de resultaten naar wens zijn.
1. Activeer de activiteit opnieuw.
