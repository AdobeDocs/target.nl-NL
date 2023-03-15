---
keywords: Recommendations;Recommendations criteria;aanbevelingen algoritmen;aanbevelingen activiteit;criteria;aanbevelingen gericht;recs
description: Meer informatie over Recommendations-activiteiten in Adobe [!DNL Target] die automatisch inhoud weergeven die mogelijk van belang is voor uw klanten op basis van eerdere gebruikersactiviteiten of andere algoritmen.
title: Wat is [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: 0d986e17-bc99-4c08-a963-7f9a6619609a
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%

---

# Recommendations

[!DNL Adobe Target Recommendations] bij activiteiten worden automatisch producten, services of inhoud weergegeven die uw bezoekers interessant kunnen maken op basis van eerdere gebruikersactiviteiten, voorkeuren of andere criteria. [!DNL Target Recommendations] helpt directe bezoekers naar relevante objecten die zij anders wellicht niet kennen. [!DNL Recommendations] Hiermee kunt u uw bezoekers relevante inhoud op het juiste tijdstip en op de juiste plaats geven.

>[!NOTE]
>
>[!DNL Recommendations] zijn beschikbaar als onderdeel van de [Doelpremiumoplossing](/help/main/c-intro/intro.md#premium). Ze zijn niet beschikbaar in [!DNL Target Standard] zonder [!DNL Target Premium] licentie.
>
>Als u momenteel [!DNL Recommendations Classic], zie [Recommendations Classic versus Recommendations Activiteiten in Target Premium](/help/main/c-recommendations/c-recommendations-faq/recommendations-classic-versus-recommendations-activities-target-premium.md#concept_A80223EF66634EA380580C2823A581C5) voor meer informatie over de twee oplossingen.

[!DNL Recommendations] helpt u suggesties in real time te optimaliseren en aan te passen over kanalen, apps, pagina&#39;s, e-mailberichten en andere leveringsopties om de betrokkenheid en conversie te verhogen en de beheerinspanningen te verminderen.

[!DNL Recommendations] helpt u:

* Geavanceerde criteria (regels) maken om aanbevelingen te automatiseren
* De aanbevelingen automatisch weergeven met behulp van enkele JavaScript-fragmenten
* Test en optimaliseer de aanbevelingen criteria en ontwerpen die de aanbevelingen tonen
* Rapport over de resultaten van uw aanbevelingen

In de volgende afbeelding worden aanbevelingen op een webpagina getoond:

![snelheid_voorbeeldafbeelding](assets/velocity_example.png)

Een aanbeveling bepaalt hoe een product aan een bezoeker wordt voorgesteld, afhankelijk van de activiteiten van die bezoeker op de plaats. Bijvoorbeeld:

| Gewenste actie | Aanbeveling |
|--- |--- |
| Moedig mensen die een rugzak kopen aan om wandelschoenen en wandelstokken te kopen. | Maak een aanbeveling waarin wordt aangegeven welke objecten vaak samen worden aangeschaft. Hierbij wordt gebruikgemaakt van de criteria &quot;Personen die dit hebben gekocht, hebben dat ook gekocht&quot;. |
| Verhoog de tijd die bezoekers besteden aan uw mediasite door media-inhoud aan te bevelen die lijkt op wat ze bekijken. | Maak een aanbeveling die andere video&#39;s voorstelt. Gebruik hiervoor de criteria &quot;Personen die dit hebben bekeken&quot;. |
| Stel dat klanten die bij je bank informatie over spaarplannen hebben bekeken, ook informatie over IRA-rekeningen lezen. | Andere producten tonen die mensen hebben gekocht na het bekijken van één product zonder het eerste product in de aanbevelingen te tonen, met de criteria &quot;mensen die dit ook hebben bekeken&quot;. |

Meer informatie hierover en andere [!DNL Recommendations] criteria, zie [Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md).

## Voorwaarden

Voordat u aan de slag gaat met [!DNL Recommendations], is het nuttig om met sommige van de termen vertrouwd te worden die in deze sectie worden gebruikt. Maak u geen zorgen als u deze termen nog niet volledig begrijpt, zult u met hen vertrouwd worden aangezien u opstelling uw [!DNL Recommendations] activiteiten.

| Term | Definitie |
| --- | --- |
| Activiteit | Activiteiten in [!DNL Target] Hiermee kunt u de inhoud aanpassen aan specifieke doelgroepen en kunt u paginaontwerpen testen. [!DNL Recommendations] is slechts één van de vele activiteitstypen beschikbaar in [!DNL Target]. Zie voor meer informatie [Doelactiviteitstypen](/help/main/c-activities/target-activities-guide.md). |
| Entiteiten | Entiteiten verwijzen naar de items die u wilt aanbevelen. Entiteiten kunnen van alles zijn, zoals producten, inhoud (artikelen, presentaties, afbeeldingen, films en tv-programma&#39;s), aanbiedingen van taken, restaurants enzovoort. Zie voor meer informatie [Entiteiten](/help/main/c-recommendations/c-products/products.md). |
| Feeds | Feeds worden gebruikt om entiteiten te importeren in [!DNL Recommendations]. Entiteiten kunnen worden verzonden met gebruik van CSV-bestanden, de Google Product Search-feed-indeling en Adobe Analytics-productclassificaties. Zie voor meer informatie [Feeds](/help/main/c-recommendations/c-products/feeds.md). |
| Catalogus | De catalogi verwijzen naar uw volledige productreeks (entiteiten). Uw catalogus kan vele inzamelingen-manier bevatten om uw producten in logische emmers te organiseren. |
| Verzameling | Verzamelingen verwijzen naar een reeks vergelijkbare of verwante items, zoals één productcategorie. U kunt echter de objecten groeperen in een categorie die voor uw bedrijf zinvol is, zoals producten met een bepaalde prijs of kleur, of items die in een bepaald geografisch gebied interessant kunnen zijn. Zie voor meer informatie [Verzamelingen](/help/main/c-recommendations/c-products/collections.md). |
| Criteria | Criteria zijn regels die bepalen welke producten moeten worden aanbevolen op basis van een vooraf bepaalde reeks gedragingen van bezoekers.<br>Enkele voorbeelden van criteria zijn: <ul><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Items met vergelijkbare kenmerken</li><li>Laatst gekocht object</li><li>Favoriete rubriek</li></ul>  Zie voor meer informatie [Criteria](/help/main/c-recommendations/c-algorithms/algorithms.md). |
| Ontwerpen | De ontwerpen bepalen de verschijning van de aanbevelingen in a [!DNL Recommendations] activiteit, zoals een rij, kolom, lijst, of net. De illustratie boven aan dit artikel toont een ontwerp van 4 x 1. Zie voor meer informatie [Een ontwerp maken](/help/main/c-recommendations/c-design-overview/create-design.md). |
| Locaties | Locaties verwijzen naar een specifiek inhoudsgebied op een webpagina, mobiele app of e-mail waar u een activiteit uitvoert voor personalisatie en optimalisatie. |
| Soorten publiek | Publiek zijn groepen van gelijkaardige deelnemers aan activiteiten die een gerichte activiteit zullen zien. Een publiek is een groep mensen met dezelfde kenmerken, zoals een nieuwe bezoeker, een terugkerende bezoeker of terugkerende bezoekers uit het Midwesten. Met de functie Publiek kunt u verschillende inhoud en ervaringen toewijzen aan specifieke doelgroepen om uw digitale marketing te optimaliseren door de juiste berichten aan de juiste mensen op het juiste moment weer te geven. Zie voor meer informatie [Soorten publiek](/help/main/c-target/target.md). |
| Recommendations als voorstel | Een eigenschap die u aanbevelingen binnen A/B Test (met inbegrip van auto-Toewijzing en auto-Doel) en de Gericht van de Ervaring (XT) activiteiten laat omvatten. Zie voor meer informatie [Recommendations als voorstel](/help/main/c-recommendations/recommendations-as-an-offer.md). |

## Trainingsvideo: Activiteitstypen ![Overzicht badge](/help/main/assets/overview.png)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target Standard/Premium]. [!DNL Recommendations] wordt om 7:20 besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

## Adobe Target Basics Webinar: Inleiding tot Recommendations ![Zelfstudie-badge](/help/main/assets/tutorial.png) {#intro-to-recs}

De *Inleiding tot Recommendations* webinar bevat een diepgaande analyse van hoe u de waarde van [!DNL Adobe Target Recommendations]. Ontdek hoe dit [!DNL Target] De activiteit toont automatisch producten of inhoud die uw klanten zouden kunnen interesseren door suggesties in real time te optimaliseren die op vorige bezoeken worden gebaseerd. Verder duik in de [!DNL Target] UI voor een geleidelijke overzicht van hoe te om een [!DNL Recommendations] activiteit.

[Inleiding tot Recommendations](https://adobecustomersuccess.adobeconnect.com/p8gt31drhs3e/?OWASP_CSRFTOKEN=4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)
