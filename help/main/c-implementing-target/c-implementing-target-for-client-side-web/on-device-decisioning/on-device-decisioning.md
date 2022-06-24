---
keywords: implementatie;javascript-bibliotheek;js;atjs;apparaatbeslissingen;op apparaatbeslissingen;at.js;op apparaat;op apparaat
description: Leer hoe u apparaatbeslissingen kunt uitvoeren met de bibliotheek at.js
title: Hoe werkt een apparaatbeslissing met de JavaScript-bibliotheek at.js?
feature: at.js
role: Developer
exl-id: 5ad6032b-9865-4c80-8800-705673657286
source-git-commit: 719eb95049dad3bee5925dff794871cd65969f79
workflow-type: tm+mt
source-wordcount: '3455'
ht-degree: 1%

---

# Apparaatbeslissingen voor at.js

Vanaf versie 2.5.0 biedt at.js on-device beslissingen. Op apparaat kunt u de beslissing in de cache plaatsen [A/B-test](/help/main/c-activities/t-test-ab/test-ab.md) en [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md) (XT) activiteiten op browser om in geheugenbesluiten zonder een blokkerend netwerkverzoek aan browser uit te voeren [!DNL Adobe Target] Edge Network.

[!DNL Target] biedt ook de flexibiliteit om de meest relevante en meest recente ervaring van uw experimenteren en machine leergedreven (ML-gedreven) verpersoonlijkingsactiviteiten via een levende servervraag te leveren. Met andere woorden, wanneer de prestaties het belangrijkst zijn, kunt u verkiezen om op-apparatenbesluit te gebruiken. Nochtans, wanneer de meest relevante, bijgewerkte, en ML-gedreven ervaring nodig is, kan een servervraag in plaats daarvan worden gemaakt.

## Wat zijn de voordelen van apparaatbeslissingen?

De voordelen van apparaatbeslissingen zijn onder meer:

* **Kies voor supersnelle beslissingen en ervaringen.** De sluiting en de beslissing worden uitgevoerd in geheugen en op browser om het blokkeren van netwerkverzoeken te vermijden.
* **Verbeter de prestaties van de toepassing.** Voer experimenten uit en verpersoonlijking aan uw klanten en gebruikers zonder de ervaringen van de eindgebruiker in gevaar te brengen.
* **Kwaliteitsscore voor Google-site verbeteren.** Nu de beslissing in het geheugen plaatsvindt, verbetert u de score voor Google Site Quality van uw online bedrijf om deze beter zichtbaar te maken voor consumenten.
* **Leer van analyses in real time.** Krijg inzicht van uw activiteitsprestaties in real time via [Analyses voor doel](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) rapportage. A4T staat u toe om uw strategie op kritieke momenten te draaien.

## Ondersteunde functies

De Adobe Target JS SDK biedt klanten de flexibiliteit om te kiezen tussen prestaties en versheid van gegevens voor beslissingen. Met andere woorden, als het voor u van het grootste belang is om de meest relevante en engaging van gepersonaliseerde inhoud via computerleren te leveren, moet er een live serveroproep worden gedaan. Maar als de prestaties kritischer zijn, moet een on-device en in-memory beslissing worden genomen. Raadpleeg de lijst met functies die worden ondersteund voor het werken van apparaatbeslissingen:

* Typen activiteiten
* Doelgerichtheid publiek
* Toewijzingsmethode

Zie voor meer informatie [Ondersteunde functies voor apparaatbesluitvorming](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/){target=_blank}.

## Hoe werkt apparaatbesluitvorming?

Wanneer u bij.js opstelt en initialiseert met toegelaten op-apparatenbesluit, een [regelartefact](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank} die uw apparaatbeslissingen voor A/B- en XT-activiteiten, -publiek en -middelen bevat, wordt gedownload van de dichtstbijzijnde Akamai CDN naar uw bezoeker en lokaal in de browser van uw bezoeker in het cachegeheugen opgeslagen. Wanneer een verzoek van at.js wordt gedaan om een ervaring terug te winnen, wordt het besluit betreffende welke ervaring om in geheugen terug te keren wordt gemaakt, die op de meta-gegevens wordt gebaseerd in het caching regelartefact worden gecodeerd.

## Beslissingsmethode

met apparaatbesturing, [!DNL Target] introduceert een nieuwe instelling genaamd [!UICONTROL Decisioning Method]. De [!UICONTROL Decisioning Method] het plaatsen bepaalt hoe te.js uw ervaringen levert. [!UICONTROL Decisioning Method] heeft drie waarden:

* [!UICONTROL Server-side only]
* [!UICONTROL On-device only]
* [!UICONTROL Hybrid]

### Alleen server

[!UICONTROL Server-side only] is de standaardbepalingsmethode die uit de doos wordt geplaatst wanneer at.js 2.5.0+ wordt uitgevoerd en op uw Web-eigenschappen opgesteld.

Gebruiken [!UICONTROL server-side only] als de standaardconfiguratie betekent dat alle beslissingen worden genomen over de [!DNL Target] edge network, wat een blokkerende servervraag impliceert. Deze aanpak kan incrementele latentie introduceren, maar biedt ook aanzienlijke voordelen, zoals de mogelijkheid om de mogelijkheden van Target voor machinaal leren toe te passen, zoals [Recommendations](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP), en [Automatisch doel](/help/main/c-activities/auto-target/auto-target-to-optimize.md) activiteiten.

Bovendien kan het verbeteren van uw gepersonaliseerde ervaringen door het gebruikersprofiel van Target te gebruiken, dat over zittingen en kanalen wordt voortgeduurd, krachtige resultaten voor uw zaken verstrekken.

Tot slot: [!UICONTROL server-side only] Hiermee kunt u de Adobe Experience Cloud gebruiken en het publiek precies afstemmen waarop u zich kunt richten via de segmenten Audience Manager en Adobe Analytics.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, at.js 2.5.0+ en het Adobe Target Edge-netwerk. In dit stroomdiagram worden nieuwe bezoekers en terugkerende bezoekers vastgelegd.

![Stroomdiagram alleen op de server](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/server-side-only.png)

De volgende lijst komt overeen met de cijfers in het diagram:

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>   De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een aanvraag voor het laden van een pagina ingediend die alle geconfigureerde parameters bevat, zoals (ECID, Customer ID, Custom Parameters, User Profile, enzovoort). |
| 5 | Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de profielenwinkel.<br>De profielenopslag vraagt gekwalificeerd publiek aan uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], enzovoort.)<br>Klantkenmerken worden in een batchproces naar de profielopslag verzonden. |
| 6 | De profielenopslag wordt gebruikt voor publiekskwalificatie en het opnemen aan filteractiviteiten. |
| 7 | De resulterende inhoud wordt geselecteerd nadat de ervaring is bepaald op basis van live [!DNL Target] activiteiten. |
| 8 | De bibliotheek at.js verbergt de overeenkomstige elementen op de pagina die aan de ervaring worden geassocieerd die moet worden teruggegeven. |
| 9 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 10 | De bibliotheek at.js manipuleert DOM om de ervaring van het Netwerk van de Rand van het Doel terug te geven. |
| 11 | De ervaring wordt weergegeven voor de bezoeker. |
| 12 | De hele webpagina wordt geladen. |
| 13 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. |
| 14 | Gerichte gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics] rapporteringsopslag. [!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) verslagen. |

### Alleen op apparaat

[!UICONTROL On-Device only] is de besluitvormingsmethode die in at.js 2.5.0+ moet worden geplaatst wanneer de op-apparatenbeslissing slechts door uw Web-pagina&#39;s zou moeten worden gebruikt.

De besluitvorming op het apparaat kan uw ervaringen en verpersoonlijkingsactiviteiten bij het opblazen van snelle snelheid leveren omdat de besluiten van een caching regelartefact worden gemaakt dat al uw activiteiten bevat die voor op-apparaat besluitvorming kwalificeren.

Zie voor meer informatie over welke activiteiten in aanmerking komen voor beslissingen op het apparaat [Ondersteunde functies in apparaatbeslissingen](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/){target=_blank}.

Deze beslissingsmethode moet alleen worden gebruikt als de prestaties van essentieel belang zijn voor alle pagina&#39;s waarvoor beslissingen nodig zijn [!DNL Target]. Houd er bovendien rekening mee dat wanneer deze beslissingsmethode wordt geselecteerd, uw [!DNL Target] activiteiten die niet in aanmerking komen voor beslissingen op het apparaat worden niet uitgevoerd of uitgevoerd. De bibliotheek at.js 2.5.0+ wordt gevormd om het caching regelartefact slechts te zoeken om besluiten te nemen.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, at.js 2.5.0+ en de CDN van Akamai. De Akamai CDN slaat het artefact van de regels voor het eerste bezoek van de bezoeker in het voorgeheugen op. Voor het eerste paginabezoek voor een nieuwe bezoeker, moet het artefact van de JSON- regels van Akamai CDN worden gedownload om plaatselijk op browser van de bezoeker in het voorgeheugen onder te brengen. Nadat het artefact van JSON-regels is gedownload, wordt de beslissing onmiddellijk genomen zonder een blokkerende netwerkaanroep. In het volgende stroomdiagram worden nieuwe bezoekers vastgelegd.

![Stroomdiagram alleen op apparaat](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | De bibliotheek at.js vraagt om het JSON-regelartefact van de dichtstbijzijnde Akamai CDN naar de bezoeker op te halen. |
| 5 | De Akamai CDN reageert met het Artefact van de JSON-regel. |
| 6 | De JSON-regelartefact wordt lokaal in de browser van de bezoeker in cache geplaatst. |
| 7 | De bibliotheek at.js interpreteert het JSON-regelartefact en voert het besluit uit om de ervaring op te halen en verbergt de geteste elementen. |
| 8 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 9 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 10 | De ervaring wordt weergegeven voor de bezoeker. |
| 11 | De hele webpagina wordt geladen. |
| 12 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gerichte gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics] rapporteringsopslag. [!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en [!DNL Target] via Analytics voor Target (A4T)-rapporten. |

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, op .js 2.5.0+ en de JSON-regelartefact in de cache voor het volgende paginahit of terugkerend bezoek van de bezoeker. Omdat het artefact van JSON-regels al in het cachegeheugen is opgeslagen en beschikbaar is in de browser, wordt de beslissing onmiddellijk genomen zonder een blokkerende netwerkaanroep. Dit stroomdiagram legt volgende paginanavigatie of terugkerende bezoekers vast.

![Stroomdiagram alleen op apparaat voor paginanavigatie en herhaalde bezoeken](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-only-subsequent.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | De bibliotheek at.js interpreteert het JSON-regelartefact en voert de beslissing in het geheugen uit om de ervaring op te halen. |
| 5 | De geteste elementen zijn verborgen. |
| 6 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 7 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 8 | De ervaring wordt weergegeven voor de bezoeker. |
| 9 | De hele webpagina wordt geladen. |
| 10 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gerichte gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics] rapporteringsopslag. [!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) verslagen. |

### Hybride

[!UICONTROL Hybrid] is de besluitvormingsmethode die in at.js 2.5.0+ moet worden geplaatst wanneer zowel op-apparatenbesluit als activiteiten die een netwerkvraag aan het netwerk van de Rand van Adobe Target vereisen moeten worden uitgevoerd.

Wanneer u zowel op apparaat beslissingsactiviteiten als server-zijactiviteiten beheert, kan het een beetje gecompliceerd en vervelend zijn wanneer het denken over hoe te om en voorziening op te stellen [!DNL Target] op uw pagina&#39;s. met hybride als beslissingsmethode, [!DNL Target] weet wanneer het een servervraag aan het netwerk van Adobe Target Edge voor activiteiten moet maken die server-zijuitvoering vereisen, en ook wanneer om slechts op-apparatenbesluiten uit te voeren.

Het Artefact van JSON-regels bevat metagegevens om at.js te informeren of een box een serveractiviteit heeft die wordt uitgevoerd of een beslissingsactiviteit op het apparaat. Deze beslissingsmethode zorgt ervoor dat activiteiten die u snel wilt laten uitvoeren, worden uitgevoerd via apparaatbeslissingen en voor activiteiten die krachtigere, door ML gestuurde personalisatie vereisen, worden deze activiteiten uitgevoerd via het Adobe Target Edge-netwerk.

In het volgende diagram ziet u de interactie tussen uw bezoeker, de browser, in.js 2.5.0+, de Akamai CDN en het Adobe Target Edge Network voor een nieuwe bezoeker die uw pagina voor het eerst bezoekt. De afstand van dit diagram is dat het artefact van de JSON-regels asynchroon wordt gedownload terwijl de beslissingen via het Adobe Target Edge-netwerk worden genomen.

Deze aanpak zorgt ervoor dat de grootte van het artefact, dat vele activiteiten kan omvatten, de latentie van de beslissing niet negatief beïnvloedt. Het synchroon downloaden van de JSON-regels en het vervolgens nemen van de beslissing kan ook negatieve gevolgen hebben voor de latentie en kan inconsistent zijn. Daarom is de hybride besluitvormingsmethode een beste praktijkaanbeveling om altijd een server-zijvraag voor het besluit voor een nieuwe bezoeker te maken, en aangezien de JSON regels artefact parallel in het voorgeheugen wordt opgeslagen. Voor om het even welke verdere paginabezoeken en terugkeerbezoeken, worden de besluiten genomen van het geheime voorgeheugen en in geheugen door het JSON regelartefact.

![Hybride-stroomdiagram voor een eerste bezoeker](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-first-time-visitor.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een aanvraag ingediend voor het laden van een pagina in het Adobe Target Edge-netwerk, inclusief alle geconfigureerde parameters zoals (ECID, Customer ID, Custom Parameters, User Profile, enzovoort.) |
| 5 | Parallel hieraan vraagt at.js om het Artefact van de JSON-regel van de dichtstbijzijnde Akamai CDN naar de bezoeker op te halen. |
| 6 | (Adobe Target Edge Network) Profielscripts worden uitgevoerd en vervolgens toegevoegd aan de Profile Store. De profielenopslag vraagt gekwalificeerd publiek aan uit de Audience Library (bijvoorbeeld publiek dat wordt gedeeld vanuit [!DNL Adobe Analytics], [!DNL Adobe Audience Manager], enzovoort.) |
| 7 | De Akamai CDN reageert met het Artefact van de JSON-regel. |
| 8 | De profielenopslag wordt gebruikt voor publiekskwalificatie en het opnemen aan filteractiviteiten. |
| 9 | De resulterende inhoud wordt geselecteerd nadat de ervaring is bepaald op basis van live [!DNL Target] activiteiten. |
| 10 | De bibliotheek at.js verbergt de overeenkomstige elementen op de pagina die aan de ervaring worden geassocieerd die moet worden teruggegeven. |
| 11 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 12 | De bibliotheek at.js manipuleert DOM om de ervaring van het Netwerk van de Rand van het Doel terug te geven. |
| 13 | De ervaring wordt weergegeven voor de bezoeker. |
| 14 | De hele webpagina wordt geladen. |
| 15 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gerichte gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics] rapporteringsopslag. [!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) verslagen. |

Het volgende diagram illustreert de interactie tussen uw bezoeker, browser, at.js 2.5.0+, en het caching JSON regelt artefact voor een verdere paginanavigatie of een terugkeerbezoek. In dit diagram, concentreert zich slechts op het gebruiksgeval dat een op-apparatenbesluit voor de verdere paginanavigatie of terugkeerbezoek wordt genomen. Houd in mening dat afhankelijk van welke activiteiten voor bepaalde pagina&#39;s levend zijn, een server-zijvraag kan worden gemaakt om server-zijbesluiten uit te voeren.

![Hybride-stroomdiagram voor paginanavigatie en herhaalde bezoeken](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/hybrid-subsequent.png)

De volgende lijst komt overeen met de cijfers in het diagram:

>[!NOTE]
>
>[!DNL Adobe Target] Admin servers kwalificeren al uw activiteiten die voor op-apparatenbesluit verkiesbaar zijn, produceren het artefact van JSON-regels, en verspreidt het aan Akamai CDN. Uw activiteiten worden voortdurend gecontroleerd op updates om een nieuw Artefact van JSON-regels uit te voeren dat aan Akamai CDN moet worden doorgegeven.

| Stap | Beschrijving |
| --- | --- |
| 1 | De [!DNL Experience Cloud Visitor ID] wordt opgehaald uit de [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html). |
| 2 | De bibliotheek at.js wordt synchroon geladen en de hoofdtekst van het document verborgen.<br>De bibliotheek at.js kan ook asynchroon worden geladen met een optioneel vooraf verborgen fragment dat op de pagina is geïmplementeerd. |
| 3 | De bibliotheek at.js verbergt het lichaam om flikkering te voorkomen. |
| 4 | Er wordt een verzoek ingediend om een ervaring op te halen. |
| 5 | De bibliotheek at.js bevestigt dat het JSON-regelartefact al in de cache is geplaatst en voert het besluit in het geheugen uit om de ervaring op te halen. |
| 6 | De geteste elementen zijn verborgen. |
| 7 | De bibliotheek at.js toont het lichaam zodat de rest van de pagina voor uw bezoeker aan mening kan worden geladen. |
| 8 | De bibliotheek at.js manipuleert DOM om de ervaring van het caching JSON regelartefact terug te geven. |
| 9 | De ervaring wordt weergegeven voor de bezoeker. |
| 10 | De hele webpagina wordt geladen. |
| 11 | [!DNL Analytics] gegevens worden naar gegevensverzamelingsservers verzonden. Gerichte gegevens komen overeen met [!DNL Analytics] gegevens via de SDID en worden verwerkt in de [!DNL Analytics] rapporteringsopslag. [!DNL Analytics] gegevens kunnen vervolgens in beide worden weergegeven [!DNL Analytics] en [!DNL Target] via [!UICONTROL Analytics for Target] (A4T) verslagen. |

## Hoe laat ik op apparaat besluiten toe?

Beslissing op het apparaat is beschikbaar voor iedereen [!DNL Target] klanten die At.js 2.5.0+ gebruiken.

Om op apparaat het besluiten toe te laten:

>[!NOTE]
>
>U moet beschikken over de [!UICONTROL Admin] of [!UICONTROL Approver] [gebruikersrol](/help/main/administrating-target/c-user-management/user-management.md) om de beslissingstoegang op het apparaat in of uit te schakelen.

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Onder **[!UICONTROL Account Details]**, schuiven de **[!UICONTROL On-Device Decisioning]** schakelen naar de positie &quot;aan&quot;.

   ![Schakelen tussen besturingsapparaten](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-toggle.png)

   De &quot;[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]De optie &#39;&#39; wordt weergegeven als u de handeling op het apparaat inschakelt.
1. (Voorwaardelijk) schuif de knevel aan &quot;op&quot;positie als u al uw levende activiteiten van het Doel die voor op-apparatenbesluit in aanmerking komen automatisch in het artefact wilt worden omvat.

   Als u deze schakeloptie uitschakelt, moet u alle beslissingsactiviteiten op het apparaat opnieuw maken en activeren, zodat deze in het gegenereerde regelartefact kunnen worden opgenomen. Met andere woorden, elke activiteit in actieve staat voordat de [!UICONTROL On-Device Decisioning] toggle is niet opgenomen in het artefact van de regels.

Nadat u het dialoogvenster [!UICONTROL On-Device Decisioning] schakelen, [!DNL Target] begint het produceren en het verspreiden [regelartefacten](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/rule-artifact/){target=_blank} voor uw client.

>[!IMPORTANT]
>
>Zorg ervoor dat u de schakeloptie inschakelt voordat u de SDK van Adobe Target initialiseert om apparaatbeslissingen te gebruiken. De regelartefacten moeten eerst aan Akamai CDNs voor op-apparatenbesluit produceren en verspreiden om te werken. De propagatie kan vijf tot tien minuten voor het eerste regelartefact vergen om aan Akamai CDN te produceren en te verspreiden.

## Hoe vorm ik bij.js 2.5.0+ om op-apparatenbesluit te gebruiken?

1. Klik op **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!UICONTROL Account details]**.
1. Onder **[!UICONTROL Implementation Methods]** > **[!UICONTROL Main Implementation Method]**, klikt u op **[!UICONTROL Edit]** naast uw versie at.js (moet zich bevinden op .js 2.5.0 of hoger).

   ![Instellingen van hoofdimplementatiemethode bewerken](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/main-implementation-method.png)

   >[!IMPORTANT]
   >
   >Alvorens deze standaardmontages te veranderen, raadpleeg de Zorg van de Cliënt zodat beïnvloedt u uw huidige implementatie niet.

1. Selecteer de gewenste beslissingsmethode:

   * [!UICONTROL Server-side only]
   * [!UICONTROL On-device only]
   * [!UICONTROL Hybrid]

   ![Bewerken bij.js, instellingenvenster](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/global-settings.png)

### Algemene instellingen

U kunt een standaard configureren [!UICONTROL Decisioning Method] voor alle [!DNL Target] besluiten. De verschillende besluitvormingsmethoden zijn [!UICONTROL Server-side only], [!UICONTROL On-device only], en [!UICONTROL Hybrid]. De besluitvormingsmethode die in het Doel UI wordt geselecteerd wordt gevormd binnen `window.targetGlobalSettings` onder de `decisioningMethod` veld. Meer informatie over de `decisioningMethod` in [targetGlobalSettings()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/){target=_blank}.

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

Als u de `decisioningMethod` in `window.targetGlobalSettings`, maar wil de `decisioningMethod` voor elke Adobe Target-beslissing kunt u deze procedure uitvoeren door `decisioningMethod` in At.js2.5.0+&#39;s [getOffers()](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/){target=_blank} aanroep.

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
>Als u &quot;op apparaat&quot; of &quot;hybride&quot; wilt gebruiken als een beslissingsmethode in de aanroep getOffers(), moet u ervoor zorgen dat de algemene instelling `decisioningMethod` als &quot;op apparaat&quot; of &quot;hybride&quot;. De bibliotheek at.js 2.5.0+ moet weten of om het Artefact van de regels JSON onmiddellijk na het laden op de pagina te downloaden en in het voorgeheugen onder te brengen. Als de besluitvormingsmethode voor het globale plaatsen aan &quot;server-kant&quot;wordt geplaatst, en &quot;op-apparaat&quot;of &quot;hybride&quot;besluitvormingsmethode wordt overgegaan in de getOffers () vraag, zou at.js 2.5.0+ niet het JSON regelartefact in het voorgeheugen ondergebracht hebben om uw op-apparatenbesluiten uit te voeren.

### Artefactcache TTL

[!DNL Target] vertegenwoordigt uw activiteiten die in aanmerking komen voor apparaatbesluitvorming als een artefact dat bestaat uit metagegevens, regels en voorwaarden. Dit artefact wordt in het cachegeheugen opgeslagen op de Akamai CDN. Tijdens het eerste bezoek van uw gebruiker, downloadt browser van de gebruiker en caches het artefact dat uw op-apparaat beslissingsactiviteiten vertegenwoordigt.

Bij volgende bezoeken aan uw site controleert de browser automatisch of deze een nieuwere versie van het artefact moet downloaden. Met deze controle wordt latentie toegevoegd. De Artefacache TTL definieert het aantal minuten dat de browser niet mag controleren op een bijgewerkt artefact sinds de laatste geslaagde download. Hoe langer het tijdsbestek, hoe beter de prestaties. Hoe korter het tijdkader, hoe beter de gegevens, maar ten koste van extra latentie.

## Hoe weet ik dat een activiteit op apparaat besluit in aanmerking komt?

Nadat u een activiteit creeert die op apparaat beslist geschikt is, een etiket dat leest [!UICONTROL On-Device Decisioning Eligible], is zichtbaar in de activiteit [!UICONTROL Overview] pagina.

![Op Apparaatbeslissingsniveau komt in aanmerking voor label op de overzichtspagina van de activiteit.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-eligible-label.png)

Dit label betekent niet dat de activiteit altijd via beslissingen op het apparaat zal worden geleverd. Slechts wanneer at.js 2.5.0+ wordt gevormd om op-apparatenbesluit te gebruiken zal deze activiteit op-apparaat worden uitgevoerd. Als at.js 2.5.0+ niet wordt gevormd om op-apparaat te gebruiken, dan zal deze activiteit nog via een servervraag worden geleverd die van at.js wordt gemaakt.

U kunt filteren op alle activiteiten die op apparaat in aanmerking komen voor besluitvorming op de [!UICONTROL Activities] pagina via de [!UICONTROL On-Device Decisioning Eligible] filter.

![In aanmerking komend filter voor besluitvorming op het apparaat op de pagina Activiteiten.](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/assets/on-device-decisioning-filter.png)

>[!NOTE]
>
>Na het creëren van en het activeren van een activiteit die op apparaat het besluiten in aanmerking komt, kan het vijf tot tien minuten nemen alvorens het in het regelvervorming wordt omvat die aan het punt van aanwezigheid Akamai CDN wordt geproduceerd en verspreid.

## Overzicht van stappen om ervoor te zorgen dat mijn beslissingsactiviteiten op het apparaat via At.js 2.5.0+ worden geleverd?

1. Open de gebruikersinterface van Adobe Target en navigeer naar **[!UICONTROL Administration]** > **[!UICONTROL Implementation]** > **[!DNL Account Details]** de **[!UICONTROL On-Device Decisioning]** schakelen.
1. De optie **&quot;[!UICONTROL Include all existing on-device decisioning qualified activities in the artifact]&quot;** schakelen.

   De eerste JSON-regels kunnen tot 10 minuten duren.

1. Een [Type activiteit dat door op apparaat het besluit wordt gesteund](https://developer.adobe.com/target/implement/client-side/atjs/on-device-decisioning/supported-features/){target=_blank} en controleer of deze geschikt is voor apparaatbesluitvorming.
1. Stel de **[!UICONTROL Decisioning Method]** hetzij **[!UICONTROL “Hybrid”]** of **[!UICONTROL “On-device only”]** via de interface voor instellingen bij.js.
1. Download en implementeer At.js 2.5.0+ op uw pagina&#39;s.
