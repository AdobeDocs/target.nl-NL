---
keywords: Aanbevelingen;Aanbevelingscriteria;aanbevelingen algoritmen;aanbevelingen activiteit;criteria;aanbevelingen gericht;recs
description: Leer over de activiteiten van Aanbevelingen in Adobe  [!DNL Target]  die automatisch inhoud tonen die uw klanten zou kunnen interesseren die op vorige gebruikersactiviteit of andere algoritmen wordt gebaseerd.
title: Wat is  [!DNL Target]  Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 0d986e17-bc99-4c08-a963-7f9a6619609a
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Aanbevelingen

[!DNL Adobe Target Recommendations] -activiteiten geven automatisch producten, services of inhoud weer die voor bezoekers interessant kan zijn op basis van eerdere gebruikersactiviteiten, voorkeuren of andere criteria. Met [!DNL Target Recommendations] kunt u rechtstreeks bezoekers naar relevante items sturen die ze anders wellicht niet kennen. Met [!DNL Recommendations] kunt u uw bezoekers relevante inhoud op het juiste moment en op de juiste plaats geven.

>[!NOTE]
>
>[!DNL Recommendations] de activiteiten zijn beschikbaar als deel van de [&#x200B; oplossing van Target Premium &#x200B;](/help/main/c-intro/intro.md#premium). Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie.
>
>Als u momenteel [!DNL Recommendations Classic] hebt, zie [&#x200B; Klassieke Aanbevelingen tegenover de Activiteiten van Aanbevelingen in Target Premium &#x200B;](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5) voor meer informatie over de twee oplossingen.

Met [!DNL Recommendations] kunt u suggesties in real-time optimaliseren en aanpassen voor kanalen, apps, pagina&#39;s, e-mailberichten en andere leveringsopties om de betrokkenheid en conversie te verhogen en de beheerinspanningen te verminderen.

[!DNL Recommendations] helpt u:

* Geavanceerde criteria (regels) maken om aanbevelingen te automatiseren
* De aanbevelingen automatisch weergeven met behulp van een paar JavaScript-fragmenten
* Test en optimaliseer de aanbevelingen criteria en ontwerpen die de aanbevelingen tonen
* Rapport over de resultaten van uw aanbevelingen

In de volgende afbeelding worden aanbevelingen op een webpagina getoond:

![&#x200B; snelheid_example beeld &#x200B;](assets/velocity_example.png)

Een aanbeveling bepaalt hoe een product aan een bezoeker wordt voorgesteld, afhankelijk van de activiteiten van die bezoeker op de plaats. Bijvoorbeeld:

| Gewenst | Aanbeveling |
|--- |--- |
| Moedig mensen die een rugzak kopen aan om wandelschoenen en wandelstokken te kopen. | Maak een aanbeveling waarin wordt aangegeven welke objecten vaak samen worden aangeschaft. Hierbij wordt gebruikgemaakt van de criteria &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. |
| Verhoog de tijd die bezoekers besteden aan uw mediasite door media-inhoud aan te bevelen die lijkt op wat ze bekijken. | Maak een aanbeveling die andere video&#39;s voorstelt. Gebruik hiervoor de criteria &quot;Personen die dit hebben bekeken&quot;. |
| Stel dat klanten die bij je bank informatie over spaarplannen hebben bekeken, ook informatie over IRA-rekeningen lezen. | Andere producten tonen die mensen hebben gekocht na het bekijken van één product zonder het eerste product in de aanbevelingen te tonen, met de criteria &quot;mensen die dit ook hebben bekeken&quot;. |

Voor meer informatie over deze en andere [!DNL Recommendations] criteria, zie [&#x200B; Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Voorwaarden

Voordat u [!DNL Recommendations] gaat gebruiken, is het handig om bekend te raken met enkele termen die in deze sectie worden gebruikt. Maak u geen zorgen als u deze termen nog niet volledig begrijpt, zult u vertrouwd met hen worden aangezien u opstelling uw [!DNL Recommendations] activiteiten.

| Term | Definitie |
| --- | --- |
| Activiteit | Met de activiteiten in [!DNL Target] kunt u inhoud aanpassen aan specifieke doelgroepen en pagina-ontwerpen testen. [!DNL Recommendations] is slechts een van de vele activiteitstypen die beschikbaar zijn in [!DNL Target] . Voor meer informatie, zie [&#x200B; de activiteitstypes van het Doel &#x200B;](/help/main/c-activities/target-activities-guide.md). |
| Entiteiten | Entiteiten verwijzen naar de items die u wilt aanbevelen. Entiteiten kunnen van alles zijn, zoals producten, inhoud (artikelen, presentaties, afbeeldingen, films en tv-programma&#39;s), aanbiedingen van taken, restaurants enzovoort. Voor meer informatie, zie [&#x200B; Entiteiten &#x200B;](/help/main/c-recommendations/c-products/products.md). |
| Feeds | Feeds worden gebruikt om entiteiten te importeren in [!DNL Recommendations] . Entiteiten kunnen worden verzonden met gebruik van CSV-bestanden, de Google Product Search-feed-indeling en Adobe Analytics-productclassificaties. Voor meer informatie, zie [&#x200B; Doopvonken &#x200B;](/help/main/c-recommendations/c-products/feeds.md). |
| Catalogus | De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen-manier bevatten om uw producten in logische emmers te organiseren. |
| Verzameling | Verzamelingen verwijzen naar een reeks vergelijkbare of verwante items, zoals één productcategorie. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten met een bepaalde prijs of kleur, of items die in een bepaald geografisch gebied interessant kunnen zijn. Voor meer informatie, zie [&#x200B; Inzamelingen &#x200B;](/help/main/c-recommendations/c-products/collections.md). |
| Criteria | Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.<br> een paar voorbeelden van criteria omvatten: <ul><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Items met vergelijkbare kenmerken</li><li>Laatst gekocht object</li><li>Favoriete rubriek</li></ul>  Voor meer informatie, zie [&#x200B; Criteria &#x200B;](/help/main/c-recommendations/c-algorithms/algorithms.md). |
| Ontwerpen | In ontwerpen wordt de vormgeving van de aanbevelingen in een [!DNL Recommendations] -activiteit gedefinieerd, zoals een rij, kolom, tabel of raster. De illustratie boven aan dit artikel toont een ontwerp van 4 x 1. Voor meer informatie, zie [&#x200B; een ontwerp &#x200B;](/help/main/c-recommendations/c-design-overview/create-design.md) creëren. |
| Locaties | Locaties verwijzen naar een specifiek inhoudsgebied op een webpagina, mobiele app of e-mail waar u een activiteit uitvoert voor personalisatie en optimalisatie. |
| Soorten publiek | Publiek zijn groepen van gelijkaardige deelnemers aan activiteiten die een gerichte activiteit zullen zien. Een publiek is een groep mensen met dezelfde kenmerken, zoals een nieuwe bezoeker, een terugkerende bezoeker of terugkerende bezoekers uit het Midwesten. Met de functie Publiek kunt u verschillende inhoud en ervaringen toewijzen aan specifieke doelgroepen om uw digitale marketing te optimaliseren door de juiste berichten aan de juiste mensen op het juiste moment weer te geven. Voor meer informatie, zie [&#x200B; Soorten publiek &#x200B;](/help/main/c-target/target.md). |
| Aanbevelingen als voorstel | Een eigenschap die u aanbevelingen binnen A/B Test (met inbegrip van auto-Toewijzing en auto-Doel) en de Gericht van de Ervaring (XT) activiteiten laat omvatten. Voor meer informatie, zie [&#x200B; Aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## De video van de opleiding: De Types van Activiteit ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium] . [!DNL Recommendations] wordt besproken beginnend bij 7 :20.

* Beschrijf de typen activiteiten die zijn opgenomen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Adobe Target Basics Webinar: Inleiding aan de badge van de Zelfstudie van Aanbevelingen ![&#x200B; &#x200B;](/help/main/assets/tutorial.png) {#intro-to-recs}

De *Inleiding aan Aanbevelingen* webinar omvat een diepgaande exploratie van hoe te hefboomwerking de waarde van [!DNL Adobe Target Recommendations]. Kom te weten hoe deze [!DNL Target] activiteit automatisch producten of inhoud toont die uw klanten zouden kunnen interesseren door suggesties in real time te optimaliseren die op vorige bezoeken worden gebaseerd. Blader verder in de [!DNL Target] -gebruikersinterface voor een stapsgewijs overzicht van het maken van een [!DNL Recommendations] -activiteit.

[&#x200B; Inleiding aan Aanbevelingen &#x200B;](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
