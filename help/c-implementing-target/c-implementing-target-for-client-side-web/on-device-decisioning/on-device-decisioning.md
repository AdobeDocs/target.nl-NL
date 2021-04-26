---
keywords: implementatie;javascript-bibliotheek;js;atjs;apparaatbeslissingen;op apparaatbeslissingen;at.js;op apparaat;op apparaat
description: Leer hoe u apparaatbeslissingen kunt uitvoeren met de bibliotheek at.js
title: Hoe werkt een apparaatbeslissing met de JavaScript-bibliotheek at.js?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
translation-type: tm+mt
source-git-commit: a73525a7c2096235d583f54865fcdcbc4b36e7c0
workflow-type: tm+mt
source-wordcount: '3401'
ht-degree: 1%

---

# Apparaatbeslissingen voor at.js

>[!NOTE]
>
>Beslissing op het apparaat is beschikbaar met de aanstaande [at.js 2.5.0 release](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md). De datum die binnenkort bekend zal worden gemaakt.

Vanaf versie 2.5.0 biedt at.js on-device beslissingen. Door op het apparaat te beslissen kunt u uw [A/B Test](/help/c-activities/t-test-ab/test-ab.md) en [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) (XT) activiteiten op de browser in het cachegeheugen plaatsen om in het geheugen te beslissen zonder een blokkerende netwerkaanvraag aan het [!DNL Adobe Target] Netwerk van de Rand.

[!DNL Target] biedt ook de flexibiliteit om de meest relevante en meest recente ervaring van uw experimenteren en machine leergedreven (ML-gedreven) verpersoonlijkingsactiviteiten via een levende servervraag te leveren. Met andere woorden, wanneer de prestaties het belangrijkst zijn, kunt u verkiezen om op-apparatenbesluit te gebruiken. Nochtans, wanneer de meest relevante, bijgewerkte, en ML-gedreven ervaring nodig is, kan een servervraag in plaats daarvan worden gemaakt.

## Wat zijn de voordelen van apparaatbeslissingen?

De voordelen van apparaatbeslissingen zijn onder meer:

* **Kies voor supersnelle beslissingen en ervaringen.** De sluiting en de beslissing worden uitgevoerd in geheugen en op browser om het blokkeren van netwerkverzoeken te vermijden.
* **Verbeter de prestaties van de toepassing.** Voer experimenten uit en verpersoonlijking aan uw klanten en gebruikers zonder de ervaringen van de eindgebruiker in gevaar te brengen.
* **Kwaliteitsscore van Google-site verbeteren.** Nu de beslissing in het geheugen plaatsvindt, verbetert u de score van Google Site Quality van uw online bedrijf om deze beter te kunnen ontdekken door de consument.
* **Leer van analyses in real time.** Verbeter inzicht van uw activiteitenprestaties in echt - tijd via  [Analytics voor Doel](/help/c-integrating-target-with-mac/a4t/a4t.md)  (A4T) rapportering. A4T staat u toe om uw strategie op kritieke momenten te draaien.

## Ondersteunde functies

De Adobe Target JS SDK biedt klanten de flexibiliteit om te kiezen tussen prestaties en versheid van gegevens voor beslissingen. Met andere woorden, als het voor u van het grootste belang is om de meest relevante en engaging van gepersonaliseerde inhoud via computerleren te leveren, moet er een live serveroproep worden gedaan. Maar als de prestaties kritischer zijn, moet een on-device en in-memory beslissing worden genomen. Raadpleeg de lijst met functies die worden ondersteund voor het werken van apparaatbeslissingen:

* Typen activiteiten
* Doelgerichtheid publiek
* Toewijzingsmethode

Zie [Ondersteunde functies voor apparaatbesluitvorming](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md) voor meer informatie.

## Hoe werkt apparaatbesluitvorming?

Wanneer u bij.js opstelt en initialiseert met toegelaten op-apparatenbesluit, wordt [rule artfact](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md) die uw op-apparatenbesluit voor A/B en XT activiteiten, publiek, en activa omvat, gedownload van dichtst Akamai CDN aan uw bezoeker en plaatselijk cached op browser van uw bezoeker. Wanneer een verzoek van at.js wordt gedaan om een ervaring terug te winnen, wordt het besluit betreffende welke ervaring om in geheugen terug te keren wordt gemaakt, die op de meta-gegevens wordt gebaseerd in het caching regelartefact worden gecodeerd.

## Beslissingsmethode

Met op-apparatenbepaling, [!DNL Target] introduceert een nieuw die plaatsen [!UICONTROL Decisioning Method] wordt genoemd. Met de instelling [!UICONTROL Decisioning Method] bepaalt u hoe at.js uw ervaringen biedt. [!UICONTROL Decisioning Method] heeft drie waarden:

* [!UICONTROL Server-side only]
* [!UICONTROL On-device only]
* [!UICONTROL Hybrid]

### Alleen server

[!UICONTROL Server-side only] is de standaardbepalingsmethode die uit de doos wordt geplaatst wanneer at.js 2.5.0+ wordt uitgevoerd en op uw Web-eigenschappen opgesteld.

Als u [!UICONTROL server-side only] gebruikt als de standaardconfiguratie, worden alle beslissingen genomen op het [!DNL Target] Edge-netwerk, dat een blokkerende serveraanroep omvat. Deze benadering kan incrementele latentie introduceren, maar biedt ook aanzienlijke voordelen, zoals de mogelijkheid om de mogelijkheden van Target voor machinaal leren toe te passen, zoals [Recommendations](/help/c-recommendations/recommendations.md), [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) en [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md)-activiteiten.

Bovendien kan het verbeteren van uw gepersonaliseerde ervaringen door het gebruikersprofiel van Target te gebruiken, dat over zittingen en kanalen wordt voortgeduurd, krachtige resultaten voor uw zaken verstrekken.

Tot slot [!UICONTROL server-side only] laat u Adobe Experience Cloud gebruiken en verfijnen publiek dat tegen door Audience Manager en de segmenten van Adobe Analytics kan worden gericht.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, at.js 2.5.0+ en het Adobe Target Edge-netwerk. In dit stroomdiagram worden nieuwe bezoekers en terugkerende bezoekers vastgelegd.

![Stroomdiagram alleen op de server](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

De volgende lijst komt overeen met de cijfers in het diagram:

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>   De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een aanvraag voor het laden van een pagina ingediend die alle geconfigureerde parameters bevat, zoals (ECID, Customer ID, Custom Parameters, User Profile, enzovoort). |
| 5 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel.<br>In het profielarchief wordt een gekwalificeerd publiek gevraagd uit de Audience Library (bijvoorbeeld een publiek dat wordt gedeeld vanuit  [!DNL Adobe Analytics],  [!DNL Adobe Audience Manager]enzovoort).<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 6 | De profielenopslag wordt gebruikt voor publiekskwalificatie en het opnemen aan filteractiviteiten. |
| 7 | De resulterende inhoud wordt geselecteerd nadat de ervaring van levende [!DNL Target] activiteiten wordt bepaald. |
| 8 | De bibliotheek at.js verbergt de overeenkomstige elementen op de pagina die aan de ervaring worden geassocieerd die moet worden teruggegeven. |
| 9 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 10 | De bibliotheek at.js manipuleert DOM om de ervaring van het Netwerk van de Rand van het Doel terug te geven. |
| 11 | De ervaring wordt weergegeven voor de bezoeker. |
| 12 | De hele webpagina wordt geladen. |
| 13 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. |
| 14 | Gericht gegeven wordt aangepast aan [!DNL Analytics] gegevens via SDID en wordt verwerkt tot [!DNL Analytics] rapporterend opslag. [!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als  [!DNL Target] via  [!UICONTROL Analytics for Target] (A4T) rapporten worden bekeken. |

### Alleen op apparaat

[!UICONTROL On-Device only] is de besluitvormingsmethode die in at.js 2.5.0+ moet worden geplaatst wanneer de op-apparatenbeslissing slechts door uw Web-pagina&#39;s zou moeten worden gebruikt.

De besluitvorming op het apparaat kan uw ervaringen en verpersoonlijkingsactiviteiten bij het opblazen van snelle snelheid leveren omdat de besluiten van een caching regelartefact worden gemaakt dat al uw activiteiten bevat die voor op-apparaat besluitvorming kwalificeren.

Zie [Ondersteunde functies in apparaatbeslissingen](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md) voor meer informatie over welke activiteiten in aanmerking komen voor apparaatbesluitvorming.

Deze beslissingsmethode moet alleen worden gebruikt als de prestaties van essentieel belang zijn voor alle pagina&#39;s waarvoor beslissingen van [!DNL Target] vereist zijn. Houd er bovendien rekening mee dat wanneer deze beslissingsmethode wordt geselecteerd, uw [!DNL Target]-activiteiten die niet in aanmerking komen voor beslissingen op het apparaat niet worden uitgevoerd of uitgevoerd. De bibliotheek at.js 2.5.0+ wordt gevormd om het caching regelartefact slechts te zoeken om besluiten te nemen.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, at.js 2.5.0+ en de CDN van Akamai. De Akamai CDN slaat het artefact van de regels voor het eerste bezoek van de bezoeker in het voorgeheugen op. Voor het eerste paginabezoek voor een nieuwe bezoeker, moet het artefact van de JSON- regels van Akamai CDN worden gedownload om plaatselijk op browser van de bezoeker in het voorgeheugen onder te brengen. Nadat het artefact van JSON-regels is gedownload, wordt de beslissing onmiddellijk genomen zonder een blokkerende netwerkaanroep. In het volgende stroomdiagram worden nieuwe bezoekers vastgelegd.

![Stroomdiagram alleen op apparaat](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | De bibliotheek at.js vraagt om het JSON-regelartefact van de dichtstbijzijnde Akamai CDN naar de bezoeker op te halen. |
| 5 | De Akamai CDN reageert met het Artefact van de JSON-regel. |
| 6 | De JSON-regelartefact wordt lokaal in de browser van de bezoeker in cache geplaatst. |
| 7 | De bibliotheek at.js interpreteert het JSON-regelartefact en voert het besluit uit om de ervaring op te halen en verbergt de geteste elementen. |
| 8 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 9 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 10 | De ervaring wordt weergegeven voor de bezoeker. |
| 11 | De hele webpagina wordt geladen. |
| 12 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gericht gegeven wordt aangepast aan [!DNL Analytics] gegevens via SDID en wordt verwerkt tot [!DNL Analytics] rapporterend opslag. [!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als  [!DNL Target] via Analytics for Target (A4T)-rapporten worden weergegeven. |

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, op .js 2.5.0+ en de JSON-regelartefact in de cache voor het volgende paginahit of terugkerend bezoek van de bezoeker. Omdat het artefact van JSON-regels al in het cachegeheugen is opgeslagen en beschikbaar is in de browser, wordt de beslissing onmiddellijk genomen zonder een blokkerende netwerkaanroep. Dit stroomdiagram legt volgende paginanavigatie of terugkerende bezoekers vast.

![Stroomdiagram alleen op apparaat voor paginanavigatie en herhaalde bezoeken](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | De bibliotheek at.js interpreteert het JSON-regelartefact en voert de beslissing in het geheugen uit om de ervaring op te halen. |
| 5 | De geteste elementen zijn verborgen. |
| 6 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 7 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 8 | De ervaring wordt weergegeven voor de bezoeker. |
| 9 | De hele webpagina wordt geladen. |
| 10 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gericht gegeven wordt aangepast aan [!DNL Analytics] gegevens via SDID en wordt verwerkt tot [!DNL Analytics] rapporterend opslag. [!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als  [!DNL Target] via  [!UICONTROL Analytics for Target] (A4T) rapporten worden bekeken. |

### Hybride

[!UICONTROL Hybrid] is de besluitvormingsmethode die in at.js 2.5.0+ moet worden geplaatst wanneer zowel op-apparatenbesluit als activiteiten die een netwerkvraag aan het netwerk van de Rand van Adobe Target vereisen moeten worden uitgevoerd.

Wanneer u zowel beslissingsactiviteiten op het apparaat als serveractiviteiten beheert, kan het een beetje ingewikkeld en vervelend zijn wanneer u nadenkt over hoe u [!DNL Target] op uw pagina&#39;s kunt implementeren en plaatsen. Met hybride als beslissingsmethode weet [!DNL Target] wanneer het een serveraanroep naar het Adobe Target Edge-netwerk moet uitvoeren voor activiteiten die uitvoering op de server vereisen, en ook wanneer alleen beslissingen op het apparaat moeten worden uitgevoerd.

Het Artefact van JSON-regels bevat metagegevens om at.js te informeren of een box een serveractiviteit heeft die wordt uitgevoerd of een beslissingsactiviteit op het apparaat. Deze beslissingsmethode zorgt ervoor dat activiteiten die u snel wilt laten uitvoeren, worden uitgevoerd via apparaatbeslissingen en voor activiteiten die krachtigere, door ML gestuurde personalisatie vereisen, worden deze activiteiten uitgevoerd via het Adobe Target Edge-netwerk.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, in.js 2.5.0+, de Akamai CDN en het Adobe Target Edge Network voor een nieuwe bezoeker die uw pagina voor het eerst bezoekt. De afstand van dit diagram is dat het artefact van de JSON-regels asynchroon wordt gedownload terwijl de beslissingen via het Adobe Target Edge-netwerk worden genomen.

Deze aanpak zorgt ervoor dat de grootte van het artefact, dat vele activiteiten kan omvatten, de latentie van de beslissing niet negatief beïnvloedt. Het synchroon downloaden van de JSON-regels en het vervolgens nemen van de beslissing kan ook negatieve gevolgen hebben voor de latentie en kan inconsistent zijn. Daarom is de hybride besluitvormingsmethode een beste praktijkaanbeveling om altijd een server-zijvraag voor het besluit voor een nieuwe bezoeker te maken, en aangezien de JSON regels artefact parallel in het voorgeheugen wordt opgeslagen. Voor om het even welke verdere paginabezoeken en terugkeerbezoeken, worden de besluiten genomen van het geheime voorgeheugen en in geheugen door het JSON regelartefact.

![Hybride-stroomdiagram voor een eerste bezoeker](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een aanvraag ingediend voor het laden van een pagina in het Adobe Target Edge-netwerk, inclusief alle geconfigureerde parameters zoals (ECID, Customer ID, Custom Parameters, User Profile, enzovoort.) |
| 5 | Parallel hieraan vraagt at.js om het Artefact van de JSON-regel van de dichtstbijzijnde Akamai CDN naar de bezoeker op te halen. |
| 6 | (Adobe Target Edge Network) Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de Profile Store. De Opslag van het Profiel vraagt gekwalificeerd publiek van de Bibliotheek van het Publiek (bijvoorbeeld, publiek dat van [!DNL Adobe Analytics], [!DNL Adobe Audience Manager] wordt gedeeld, etc.). |
| 7 | De Akamai CDN reageert met het Artefact van de JSON-regel. |
| 8 | De profielenopslag wordt gebruikt voor publiekskwalificatie en het opnemen aan filteractiviteiten. |
| 9 | De resulterende inhoud wordt geselecteerd nadat de ervaring van levende [!DNL Target] activiteiten wordt bepaald. |
| 10 | De bibliotheek at.js verbergt de overeenkomstige elementen op de pagina die aan de ervaring worden geassocieerd die moet worden teruggegeven. |
| 11 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 12 | De bibliotheek at.js manipuleert DOM om de ervaring van het Netwerk van de Rand van het Doel terug te geven. |
| 13 | De ervaring wordt weergegeven voor de bezoeker. |
| 14 | De hele webpagina wordt geladen. |
| 15 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gericht gegeven wordt aangepast aan [!DNL Analytics] gegevens via SDID en wordt verwerkt tot [!DNL Analytics] rapporterend opslag. [!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als  [!DNL Target] via  [!UICONTROL Analytics for Target] (A4T) rapporten worden bekeken. |

Het volgende diagram illustreert de interactie tussen uw bezoeker, browser, at.js 2.5.0+, en het caching JSON regelt artefact voor een verdere paginanavigatie of een terugkeerbezoek. In dit diagram, concentreert zich slechts op het gebruiksgeval dat een op-apparatenbesluit voor de verdere paginanavigatie of terugkeerbezoek wordt genomen. Houd in mening dat afhankelijk van welke activiteiten voor bepaalde pagina&#39;s levend zijn, een server-zijvraag kan worden gemaakt om server-zijbesluiten uit te voeren.

![Hybride-stroomdiagram voor paginanavigatie en herhaalde bezoeken](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 1 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een verzoek ingediend om een ervaring op te halen. |
| 5 | De bibliotheek at.js bevestigt dat het JSON-regelartefact al in de cache is geplaatst en voert het besluit in het geheugen uit om de ervaring op te halen. |
| 6 | De geteste elementen zijn verborgen. |
| 7 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 8 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 9 | De ervaring wordt weergegeven voor de bezoeker. |
| 10 | De hele webpagina wordt geladen. |
| 11 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gericht gegeven wordt aangepast aan [!DNL Analytics] gegevens via SDID en wordt verwerkt tot [!DNL Analytics] rapporterend opslag. [!DNL Analytics] gegevens kunnen vervolgens zowel in  [!DNL Analytics] als  [!DNL Target] via  [!UICONTROL Analytics for Target] (A4T) rapporten worden bekeken. |

## Hoe laat ik op apparaat besluiten toe?

Beslissing op het apparaat is beschikbaar voor alle [!DNL Target] klanten die At.js 2.5.0+ gebruiken.

Om op apparaat het besluiten toe te laten:

>[!NOTE]
>
>U moet [!UICONTROL Admin] of [!UICONTROL Approver] [gebruikersrol](/help/administrating-target/c-user-management/user-management.md) hebben om de op-Apparaatbeslissingsknevel toe te laten of onbruikbaar te maken.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Schuif onder **[!UICONTROL Account Details]** de schakeloptie **[!UICONTROL On-Device Decisioning]** in de stand &quot;on&quot;.

   ![Schakelen tussen besturingsapparaten](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   De optie &quot;[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]&quot; wordt weergegeven als u de besluitvorming op het apparaat inschakelt.
1. (Voorwaardelijk) schuif de knevel aan &quot;op&quot;positie als u al uw levende activiteiten van het Doel die voor op-apparatenbesluit in aanmerking komen automatisch in het artefact wilt worden omvat.

   Als u deze schakeloptie uitschakelt, moet u alle beslissingsactiviteiten op het apparaat opnieuw maken en activeren, zodat deze in het gegenereerde regelartefact kunnen worden opgenomen. Met andere woorden, elke activiteit in live-toestand voordat de schakeloptie [!UICONTROL On-Device Decisioning] wordt ingeschakeld, is niet opgenomen in het artefact van de regels.

Nadat [!UICONTROL On-Device Decisioning] schakelt, [!DNL Target] begint producerend en verspreidend [regelartefacten](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/rule-artifact.md) voor uw cliënt.

>[!IMPORTANT]
>
>Zorg ervoor dat u de schakeloptie inschakelt voordat u de SDK van Adobe Target initialiseert om apparaatbeslissingen te gebruiken. De regelartefacten moeten eerst aan Akamai CDNs voor op-apparatenbesluit produceren en verspreiden om te werken. De propagatie kan vijf tot tien minuten voor het eerste regelartefact vergen om aan Akamai CDN te produceren en te verspreiden.

## Hoe vorm ik bij.js 2.5.0+ om op-apparatenbesluit te gebruiken?

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Klik onder **[!UICONTROL Implementation Methods]** > **[!UICONTROL Main Implementation Method]** op **[!UICONTROL Edit]** naast uw versie at.js (moet zich bevinden op .js 2.5.0 of hoger).

   ![Instellingen van hoofdimplementatiemethode bewerken](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Alvorens deze standaardmontages te veranderen, raadpleeg de Zorg van de Cliënt zodat beïnvloedt u uw huidige implementatie niet.

1. Selecteer de gewenste beslissingsmethode:

   * [!UICONTROL Server-side only]
   * [!UICONTROL On-device only]
   * [!UICONTROL Hybrid]

   ![Bewerken bij.js, instellingenvenster](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Algemene instellingen

U kunt een gebrek [!UICONTROL Decisioning Method] voor alle [!DNL Target] besluiten vormen. De verschillende beslissingsmethoden zijn [!UICONTROL Server-side only], [!UICONTROL On-device only] en [!UICONTROL Hybrid]. De besluitvormingsmethode die in het Doel UI wordt geselecteerd wordt gevormd op `window.targetGlobalSettings` onder het `decisioningMethod` gebied. Meer informatie over `decisioningMethod` in [targetGlobalSettings()](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md).

```javascript
<head> 
    <script type="text/javascript">

        window.targetGlobalSettings = { 
            clientCode: "yourClientCodeHere", 
            imsOrgId: "imsOrgId@AdobeOrg", 
            decisioningMethod: "on-device"

        }; 
    </script>

    <script type="text/javascript" src="at.js"></script> 
</head>
```

### Aangepaste instelling

Als u `decisioningMethod` in `window.targetGlobalSettings` plaatst, maar `decisioningMethod` voor elke beslissing van Adobe Target volgens uw gebruiksgeval zou willen met voeten treden, kunt u deze procedure doen door `decisioningMethod` in At.js2.5.0+ [getOffers () ](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) te specificeren vraag.

```javascript
adobe.target.getOffers({ 

  decisioningMethod:"on-device", 
  request: { 
    execute: { 
      mboxes: [ 
        { 
          index: 0, 
          name: "homepage" 
        } 
      ] 
    } 
 } 
});
```

>[!NOTE]
>
>Als u &quot;op apparaat&quot; of &quot;hybride&quot; wilt gebruiken als een beslissingsmethode in de aanroep getOffers(), moet u ervoor zorgen dat de algemene instelling `decisioningMethod` heeft als &quot;op apparaat&quot; of &quot;hybride&quot;. De bibliotheek at.js 2.5.0+ moet weten of om het Artefact van de regels JSON onmiddellijk na het laden op de pagina te downloaden en in het voorgeheugen onder te brengen. Als de besluitvormingsmethode voor het globale plaatsen aan &quot;server-kant&quot;wordt geplaatst, en &quot;op-apparaat&quot;of &quot;hybride&quot;besluitvormingsmethode wordt overgegaan in de getOffers () vraag, zou at.js 2.5.0+ niet het JSON regelartefact in het voorgeheugen ondergebracht hebben om uw op-apparatenbesluiten uit te voeren.

### Artefactcache TTL

[!DNL Target] vertegenwoordigt uw activiteiten die in aanmerking komen voor apparaatbesluitvorming als een artefact dat bestaat uit metagegevens, regels en voorwaarden. Dit artefact wordt in het cachegeheugen opgeslagen op de Akamai CDN. Tijdens het eerste bezoek van uw gebruiker, downloadt browser van de gebruiker en caches het artefact dat uw op-apparaat beslissingsactiviteiten vertegenwoordigt.

Bij volgende bezoeken aan uw site controleert de browser automatisch of deze een nieuwere versie van het artefact moet downloaden. Met deze controle wordt latentie toegevoegd. De Artefacache TTL definieert het aantal minuten dat de browser niet mag controleren op een bijgewerkt artefact sinds de laatste geslaagde download. Hoe langer het tijdsbestek, hoe beter de prestaties. Hoe korter het tijdkader, hoe beter de gegevens, maar ten koste van extra latentie.

## Hoe weet ik dat een activiteit op apparaat besluit in aanmerking komt?

Nadat u een activiteit creeert die op apparaat het besluiten geschikt is, is een etiket dat [!UICONTROL On-Device Decisioning Eligible] leest, zichtbaar in de pagina [!UICONTROL Overview] van de activiteit.

![Op Apparaatbeslissingsniveau komt in aanmerking voor label op de overzichtspagina van de activiteit.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

Dit label betekent niet dat de activiteit altijd via beslissingen op het apparaat zal worden geleverd. Slechts wanneer at.js 2.5.0+ wordt gevormd om op-apparatenbesluit te gebruiken zal deze activiteit op-apparaat worden uitgevoerd. Als at.js 2.5.0+ niet wordt gevormd om op-apparaat te gebruiken, dan zal deze activiteit nog via een servervraag worden geleverd die van at.js wordt gemaakt.

Via het filter [!UICONTROL On-Device Decisioning Eligible] kunt u filteren op alle activiteiten die geschikt zijn voor apparaatbesluitvorming op de pagina [!UICONTROL Activities].

![In aanmerking komend filter voor besluitvorming op het apparaat op de pagina Activiteiten.](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>Na het creëren van en het activeren van een activiteit die op apparaat het besluiten in aanmerking komt, kan het vijf tot tien minuten nemen alvorens het in het regelvervorming wordt omvat die aan het punt van aanwezigheid Akamai CDN wordt geproduceerd en verspreid.

## Overzicht van stappen om ervoor te zorgen dat mijn beslissingsactiviteiten op het apparaat via At.js 2.5.0+ worden geleverd?

1. Open de gebruikersinterface van Adobe Target en navigeer naar **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!DNL Account Details]** om de **[!UICONTROL On-Device Decisioning]**-schakeloptie in te schakelen.
1. Schakel de schakeloptie **&quot;[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]&quot;** in.

   De eerste JSON-regels kunnen tot 10 minuten duren.

1. Creeer en activeer een [activiteitstype dat door op-apparatenbesluit ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/supported-features.md) wordt gesteund, en verifieer dat het op-apparatenbesluit geschikt is.
1. Stel **[!UICONTROL Decisioning Method]** in op **[!UICONTROL “Hybrid”]** of **[!UICONTROL “On-device only”]** via de interface voor instellingen at.js.
1. Download en implementeer At.js 2.5.0+ op uw pagina&#39;s.
