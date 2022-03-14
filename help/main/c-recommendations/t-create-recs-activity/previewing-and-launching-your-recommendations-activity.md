---
keywords: Recommendations;aanbieding;voorvertoning;start;status;criteria;algoritme
description: 'Leer hoe u een voorvertoning van uw Adobe kunt weergeven [!DNL Target] Recommendations-activiteit om ervoor te zorgen dat resultaten beschikbaar zijn voordat de activiteit wordt gestart. '
title: Hoe kan ik een Recommendations-activiteit voorvertonen en starten?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# Recommendations-activiteiten voorvertonen en starten

Nadat u uw [!UICONTROL Recommendations], [!UICONTROL A/B Test], of [!UICONTROL Experience Targeting] (XT) activiteit die [Recommendations-aanbiedingen](/help/main/c-recommendations/recommendations-as-an-offer.md)Wilt u een voorvertoning van uw aanbevelingen weergeven om te controleren of de resultaten beschikbaar zijn voordat u de activiteit start. [!DNL Target Recommendations] biedt meerdere manieren om uw aanbevelingen voor te vertonen.

## Recommendations-algoritmestatus controleren

Na het maken van een activiteit, [!DNL Recommendations] stelt een algoritme in werking om aanbevelingen te produceren. Dit algoritme kan enkele uren duren.

U kunt controleren of het algoritme in het [!UICONTROL Activity] overzichtsdiagram waarin de status van de criteria wordt vermeld. De volgende illustratie toont de status in het activiteitendiagram op een [!DNL Recommendations] activiteiten [!UICONTROL Overview] pagina:

![Pagina Overzicht van Recommendations-activiteiten](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

In de volgende afbeelding wordt de status op een [!UICONTROL A/B Test] of XT-activiteit [!UICONTROL Overview] pagina:

![A/B pagina Overzicht van tests](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

De statusresultaten zijn als volgt:

* [!UICONTROL Results Ready]: Geeft aan dat het algoritme resultaten heeft geretourneerd
* [!UICONTROL Results Not Ready]: Geeft aan dat het algoritme niet is voltooid.
* [!UICONTROL Feed Failure]: Geeft aan dat het feed-bestand met aangepaste criteria niet kan worden opgehaald.

![Het dialoogvenster Resultaten](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Hoe lang duurt het om het algoritme uit te voeren?

Na het opslaan van een activiteit die een criterium bevat, [!DNL Target] compileert aanbevelingen die op de geselecteerde inzameling, de criteria, het ontwerp, en de promoties worden gebaseerd. Deze berekening duurt enige tijd en het tijdsbestek verschilt op basis van de geselecteerde aanbevelingen logica, gegevensbereik, het aantal items in de catalogus, de hoeveelheid gedragsgegevens die uw klanten hebben gegenereerd en de geselecteerde gegevensbron voor gedragsgegevens.

De gedragsgegevensbron heeft het grootste effect op verwerkingstijd, als volgt:

### mboxes

Als vakjes als gedragsgegevensbron worden geselecteerd, zodra gecreeerd, loopt de criteria onmiddellijk. Afhankelijk van de hoeveelheid gebruikte gedragsgegevens en de grootte van de catalogus kan het uitvoeren van het algoritme maximaal 12 uur duren. Als u wijzigingen aanbrengt in de configuratie criteria, wordt het algoritme doorgaans opnieuw uitgevoerd. Afhankelijk van de aangebrachte wijziging zijn de eerder berekende aanbevelingen mogelijk pas beschikbaar wanneer een nieuwe uitvoering is voltooid, of voor grotere wijzigingen is alleen de back-up- of standaardinhoud beschikbaar totdat een nieuwe uitvoering is voltooid. Als een algoritme niet wordt gewijzigd, wordt het automatisch opnieuw in werking gesteld door [!DNL Target] om de 12-48 uur, afhankelijk van het geselecteerde gegevensbereik.

### Adobe Analytics

Indien de criteria worden gebruikt [!DNL Adobe Analytics] als gedragsgegevensbron, zodra gecreeerd, hangt de tijd voor criteria beschikbaarheid af van of de geselecteerde rapportreeks en het raadplegingsvenster voor een andere criteria is gebruikt.

* **Installatie van een eenmalige rapportsuite**: De eerste keer wordt een rapportreeks gebruikt met een bepaald venster van de gegevenswaaierraadpleging, [!DNL Target Recommendations] kan twee tot zeven dagen duren om de gedragsgegevens voor de geselecteerde rapportsuite volledig te downloaden van [!DNL Analytics]. Dit tijdsbestek is afhankelijk van de [!DNL Analytics] systeembelasting.
* **Nieuwe of bewerkte criteria met behulp van een reeds beschikbare rapportsuite**: Als de geselecteerde rapportsuite al is gebruikt bij het maken van nieuwe criteria of het bewerken van bestaande criteria [!DNL Target Recommendations]Met een gegevensbereik dat gelijk is aan of kleiner is dan het geselecteerde gegevensbereik, zijn de gegevens direct beschikbaar en is een eenmalige instelling niet vereist. In dit geval, of als de montages van een algoritme terwijl het wijzigen van de geselecteerde rapportreeks of gegevenswaaier worden uitgegeven, loopt het algoritme of herstelt binnen 12 uren.
* **Doorlopende algoritmeuitvoering**: Gegevensstromen uit [!DNL Analytics] tot [!DNL Target Recommendations] dagelijks. Bijvoorbeeld voor [!UICONTROL Viewed Affinity] aanbeveling, wanneer een gebruiker een product bekijkt, wordt een product-mening het volgen vraag overgegaan in [!DNL Analytics] dicht bij real-time. De [!DNL Analytics] gegevens worden doorgegeven aan [!DNL Target] vroeg de volgende dag en [!DNL Target] voert het algoritme in minder dan 12 uren uit.

>[!NOTE]
>
>[!UICONTROL Recently Viewed Items] vereist geen off-line algoritme looppas en de resultaten zijn onmiddellijk beschikbaar. [!UICONTROL Top Viewed] en [!UICONTROL Top Sellers] algoritmen die zijn gebaseerd op mbox-gegevens leveren over het algemeen zeer snel resultaten op vanwege de eenvoudigere vereiste berekening. Dit kunnen goede opties zijn als u een voorbeeld van een ontwerpwijziging wilt bekijken of wilt bevestigen dat gedragsgegevens correct worden verzameld.

## Een voorbeeld van Recommendations bekijken met QA-koppelingen

Nadat de resultaten van het algoritme klaar zijn, kunt u die resultaten voorvertonen met de [QA-koppeling](/help/main/c-activities/c-activity-qa/activity-qa.md) functionaliteit van [!DNL Adobe Target]. QA-koppelingen zijn beschikbaar in het dialoogvenster [!UICONTROL Activity QA] sectie van de overzichtspagina Activiteit:

![QA-koppeling voor activiteit](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Standaard, [!DNL Target] voegt u automatisch toe aan het vereiste publiek voor de koppeling QA. Als deze het plaatsen wordt uitgezet en uw activiteit het richten regels heeft, moet uw gebruikersprofiel die richten regels ontmoeten om de ervaring te zien die aanbevelingen bevat.

Als u een koppeling QA gebruikt, kunt u de aanbevelingen op uw pagina bekijken:

![Aanbevolen producten](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* De doel-QA-modus is &quot;plakken&quot; en wordt in een cookie opgeslagen. Als u de QA-modus niet afsluit, blijven de resultaten van de QA op de hele site zichtbaar. Als u de QA-modus wilt afsluiten, gebruikt u de optie [bladwijzer](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* In de QA-modus is het bladeren door de site niet van invloed op de [!UICONTROL Recently Viewed Items] of [!UICONTROL Recently Purchased Items]. Dit gedrag gebeurt door het ontwerp om onopzettelijke verontreiniging van gedragsgegevens van de productie te voorkomen. Als u een voorbeeld wilt weergeven van de resultaten van een [!UICONTROL Recently Viewed Items] of [!UICONTROL User-Based Recommendations] criteria, doorblader eerst de plaats buiten de wijze van QA, dan gebruik de zelfde zitting om een verbinding van de wijze van QA te openen.


## De CSV-download gebruiken om aanbevelingen voor te vertonen

In sommige gevallen, zou u de specifieke punten kunnen willen controleren die worden geadviseerd. Dit is vooral handig bij het gebruik van algoritmen als [!UICONTROL People Who Viewed This, Viewed That], waarbij een andere set items wordt aanbevolen afhankelijk van het item dat de gebruiker momenteel bekijkt, en u mogelijk duizenden of miljoenen verschillende items in uw catalogus hebt.

Resultaten kunnen pas worden gedownload nadat een [!UICONTROL Results Ready] status wordt weergegeven voor ten minste één algoritme in de activiteit.

Als u resultaten wilt downloaden voor een voorvertoning, klikt u op het menupictogram in de rechterbovenhoek van de pagina Activiteiten en klikt u vervolgens op **[!UICONTROL Download data]**.

![Gegevensoptie downloaden](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

Er wordt een CSV-bestand gedownload. Open het venster om de aanbevolen items weer te geven:

![CSV-bestand met aanbevolen items](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Van links naar rechts is een lijst met aanbevolen items, in dit geval de meest bekeken items. De aanbevelingen worden gescheiden door het milieu, in dit geval heeft alleen de productieomgeving aanbevelingen. Voor dit algoritme, hebben wij geen beperkingen toegepast die op zeer belangrijke waarde worden gebaseerd, zodat bevat de rij geëtiketteerd met een asterisk (*) de volledige reeks aanbevelingen. Voor andere algoritmenypen die op een zeer belangrijke waarde worden gebaseerd, zoals [!UICONTROL People Who Viewed This, Viewed That], zijn de belangrijkste waarden (d.w.z. de &quot;Deze&quot;punten) vermeld in de meest linkse kolom en de geadviseerde punten (d.w.z. de &quot;dat&quot;punten) worden vermeld links-aan-recht in de kolommen Recommendation_X.

>[!NOTE]
>
>Downloads van resultaten zijn niet beschikbaar voor activiteiten die een [!UICONTROL User-Based Recommendations] algoritme. Downloads van resultaten zijn niet beschikbaar voor criteria die [!UICONTROL Recently-Viewed Items] aanbevelingen.

## Recommendations-activiteit activeren

Van de [!UICONTROL Activity Overview] klikt u op de vervolgkeuzepijl naast de status en selecteert u vervolgens **[!UICONTROL Activate]**.

![Optie Activeren](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

De status wordt [!UICONTROL Activating]:

![Activeren](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

Na een paar seconden tot een paar minuten schakelt de status over naar [!UICONTROL Live]:

![Live](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

U kunt de activiteit ook deactiveren of archiveren met dezelfde vervolgkeuzelijst.

## Onderbrekingen voorkomen bij het wijzigen van Recommendations-instellingen

Wijzigen [!DNL Recommendations] verzamelingen, criteria, promoties of ontwerpinstellingen in een live activiteit kunnen ertoe leiden dat de resultaten van het algoritme ongeldig worden en dat de status van een algoritme verandert in [!UICONTROL Results Not Ready].

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
