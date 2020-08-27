---
keywords: Recommendations;Recommendations criteria;recommendations algorithms;recommendations activity;criteria;recommendations targeting;recs
description: Recommendations-activiteiten in Adobe Target geven automatisch producten of inhoud weer die voor uw klanten interessant kan zijn op basis van eerdere gebruikersactiviteiten of andere algoritmen. Recommendations helpt klanten om relevante objecten te sturen waarvan ze anders wellicht niet op de hoogte zijn.
title: Adobe Target Recommendations
feature: recommendations general
uuid: 2aefd118-8fec-493d-ae4e-c1139c877a3f
translation-type: tm+mt
source-git-commit: 90a224475c645f9b5fcfd4aaeab6d189dd1ce9b1
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Recommendations{#recommendations}

[!DNL Adobe Target Recommendations] bij activiteiten worden automatisch producten, services of inhoud weergegeven die uw bezoekers interessant kunnen maken op basis van eerdere gebruikersactiviteiten, voorkeuren of andere criteria. [!DNL Target Recommendations] helpt directe bezoekers naar relevante objecten die zij anders wellicht niet kennen. [!DNL Recommendations] Hiermee kunt u uw bezoekers relevante inhoud op het juiste tijdstip en op de juiste plaats geven.

>[!NOTE]
>
>[!DNL Recommendations] activiteiten zijn beschikbaar als onderdeel van de [Target Premium-oplossing](/help/c-intro/intro.md#premium). Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] licentie.
>
>Als u momenteel [!DNL Recommendations Classic]beschikt, raadpleegt u [Recommendations Classic versus Recommendations Activity in Target Premium](../c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5) voor meer informatie over de twee oplossingen.

[!DNL Recommendations] helpt u suggesties in real time te optimaliseren en aan te passen over kanalen, apps, pagina&#39;s, e-mailberichten en andere leveringsopties om de betrokkenheid en conversie te verhogen en de beheerinspanningen te verminderen.

[!DNL Recommendations] helpt u:

* Geavanceerde criteria (regels) maken om aanbevelingen te automatiseren
* De aanbevelingen automatisch weergeven met behulp van enkele JavaScript-fragmenten
* Test en optimaliseer de aanbevelingen criteria en ontwerpen die de aanbevelingen tonen
* Rapport over de resultaten van uw aanbevelingen

In de volgende afbeelding worden aanbevelingen op een webpagina getoond:

![](assets/velocity_example.png)

Een aanbeveling bepaalt hoe een product aan een bezoeker wordt voorgesteld, afhankelijk van de activiteiten van die bezoeker op de plaats. Bijvoorbeeld:

| Gewenste actie | Aanbeveling |
|--- |--- |
| Moedig mensen die een rugzak kopen aan om wandelschoenen en wandelstokken te kopen. | Maak een aanbeveling waarin wordt aangegeven welke objecten vaak samen worden aangeschaft. Hierbij wordt gebruikgemaakt van de criteria &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. |
| Verhoog de tijd die bezoekers besteden aan uw mediasite door media-inhoud aan te bevelen die lijkt op wat ze bekijken. | Maak een aanbeveling die andere video&#39;s voorstelt. Gebruik hiervoor de criteria &quot;Personen die dit hebben bekeken&quot;. |
| Stel dat klanten die bij je bank informatie over spaarplannen hebben bekeken, ook informatie over IRA-rekeningen lezen. | Andere producten tonen die mensen hebben gekocht na het bekijken van één product zonder het eerste product in de aanbevelingen te tonen, met de criteria &quot;mensen die dit ook hebben bekeken&quot;. |

Zie [!DNL Recommendations] Criteria voor meer informatie over deze en andere [criteria](../c-recommendations/c-algorithms/algorithms.md#concept_4BD01DC437F543C0A13621C93A302750).

## Voorwaarden

Voordat u begint te gebruiken, is het handig om bekend te raken met enkele termen die in deze sectie worden gebruikt. [!DNL Recommendations] Maak u geen zorgen als u deze termen nog niet volledig begrijpt, zult u vertrouwd met hen worden aangezien u opstelling uw [!DNL Recommendations] activiteiten.

| Term | Definitie |
| --- | --- |
| Activiteit | Met de activiteiten in [!DNL Target] dit deelvenster kunt u inhoud aanpassen aan specifieke doelgroepen en pagina-ontwerpen testen. [!DNL Recommendations] is slechts één van de vele activiteitstypen beschikbaar in [!DNL Target]. Zie [Doelactiviteitstypen](/help/c-activities/target-activities-guide.md)voor meer informatie. |
| Entiteiten | Entiteiten verwijzen naar de items die u wilt aanbevelen. Entiteiten kunnen van alles zijn, zoals producten, inhoud (artikelen, presentaties, afbeeldingen, films en tv-programma&#39;s), aanbiedingen van taken, restaurants enzovoort.Zie [Entiteiten](/help/c-recommendations/c-products/products.md)voor meer informatie. |
| Feeds | Met feeds worden entiteiten geïmporteerd in [!DNL Recommendations]. Entiteiten kunnen worden verzonden met gebruik van CSV-bestanden, de Google Product Search-feed-indeling en Adobe Analytics-productclassificaties. Zie [Feeds](/help/c-recommendations/c-products/feeds.md)voor meer informatie. |
| Catalogus | De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen-manier bevatten om uw producten in logische emmers te organiseren. |
| Verzameling | Verzamelingen verwijzen naar een reeks vergelijkbare of verwante items, zoals één productcategorie. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten met een bepaalde prijs of kleur, of items die in een bepaald geografisch gebied interessant kunnen zijn. Zie [Verzamelingen](/help/c-recommendations/c-products/collections.md)voor meer informatie. |
| Criteria | Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.<br>Enkele voorbeelden van criteria zijn: <ul><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Items met vergelijkbare kenmerken</li><li>Laatst gekocht object</li><li>Favoriete rubriek</li></ul>  Zie [Criteria](/help/c-recommendations/c-algorithms/algorithms.md)voor meer informatie. |
| Ontwerpen | In ontwerpen wordt de vormgeving van de aanbevelingen in een [!DNL Recommendations] activiteit gedefinieerd, zoals een rij, kolom, tabel of raster. De illustratie boven aan dit artikel toont een ontwerp van 4 x 1. Zie Een ontwerp [maken voor meer informatie](/help/c-recommendations/c-design-overview/create-design.md). |
| Locaties | Locaties verwijzen naar een specifiek inhoudsgebied op een webpagina, mobiele app of e-mail waar u een activiteit uitvoert voor personalisatie en optimalisatie. |
| Soorten publiek | Publiek zijn groepen van gelijkaardige deelnemers aan activiteiten die een gerichte activiteit zullen zien. Een publiek is een groep mensen met dezelfde kenmerken, zoals een nieuwe bezoeker, een terugkerende bezoeker of terugkerende bezoekers uit het Midwesten. Met de functie Publiek kunt u verschillende inhoud en ervaringen toewijzen aan specifieke doelgroepen om uw digitale marketing te optimaliseren door de juiste berichten aan de juiste mensen op het juiste moment weer te geven. Zie [Soorten publiek](/help/c-target/target.md)voor meer informatie. |
| Recommendations als voorstel | Een eigenschap die u aanbevelingen binnen A/B Test (met inbegrip van auto-Toewijzing en auto-Doel) en de Gericht van de Ervaring (XT) activiteiten laat omvatten. Zie [Recommendations als een voorstel](/help/c-recommendations/recommendations-as-an-offer.md)voor meer informatie. |

## Trainingsvideo: Badge ![Overzicht activiteitstypen](/help/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium]. [!DNL Recommendations] wordt om 7:20 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Adobe Target Basics Webinar: Inleiding tot Recommendations- ![zelfstudie](/help/assets/tutorial.png) {#intro-to-recs}

De *introductie van het webinar van Recommendations* bevat een diepgaande analyse van hoe u de waarde van [!DNL Adobe Target Recommendations]kunt benutten. Kom te weten hoe deze [!DNL Target] activiteit automatisch producten of inhoud toont die uw klanten zouden kunnen interesseren door suggesties in real time te optimaliseren die op vorige bezoeken worden gebaseerd. Verder, duik in [!DNL Target] UI voor een geleidelijke overzicht van hoe te om een [!DNL Recommendations] activiteit te bouwen.

[Inleiding tot Recommendations](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)