---
description: De manier waarop Doel maakt en reageert op aanroepen vanuit uw pagina is afhankelijk van de versie van de doelbibliotheek die u gebruikt, of de Experience Cloud Visitor ID-implementatie aanwezig is en of de bezoeker-id bestaat.
title: Methoden voor doelpagina's door bibliotheekversie mbox.js
feature: at.js
translation-type: tm+mt
source-git-commit: 88f6e4c6ad168e4f9ce69aa6618d8641b466e28a
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Methoden voor doelpagina&#39;s op versie van de bibliotheek mbox.js{#target-page-methods-by-mbox-js-library-version}

De manier waarop Doel maakt en reageert op aanroepen vanuit uw pagina is afhankelijk van de versie van de doelbibliotheek die u gebruikt, of de Experience Cloud Visitor ID-implementatie aanwezig is en of de bezoeker-id bestaat.

>[!NOTE]
>
>Als u [!DNL at.js] gebruikt, worden alle vraag gemaakt gebruikend JSON. Deze pagina bevat informatie over bibliotheekversies [!DNL mbox.js]. De gedragingen die in de onderstaande scenario&#39;s worden beschreven, zijn niet van toepassing op [!DNL at.js].

Deze sectie verstrekt informatie over hoe elke versie van [!DNL Target] bibliotheek aan de [!DNL Target] vraag van uw pagina in elk van de volgende scenario&#39;s antwoordt.

Er zijn verschillende typen of eindpunten, afhankelijk van uw implementatie en bibliotheekversie. U zou met elk type vertrouwd moeten zijn om te begrijpen hoe [!DNL Target] aan vraag in elk scenario antwoordt.

| Type/eindpunt | Aanroepmethode | Responsinhoud |
|--- |--- |--- |
| Automatisch globale box maken - synchroon | document.write om te roepen | JavaScript zonder document.write() |
| Automatisch globale box maken - asynchroon | createElement() om aanroep aan de hoofdtekst toe te voegen | JavaScript zonder document.write() |
| standaard | document.write om te roepen | JavaScript met document.write() |
| ajax | createElement() om aanroep aan de hoofdtekst toe te voegen | JavaScript zonder document.write() |
| json | XMLHTTPrequest() om aan te roepen | retourneert JSON-reactie |

>[!IMPORTANT]
>
>Voor elk type behalve standaard moeten alle aangepaste code en aanbiedingen worden geschreven ter ondersteuning van een ajax-omgeving. Als u bijvoorbeeld een JavaScript gebruikt dat `document.write()` bevat, werkt het script niet zoals verwacht.

## Geen implementatie van bezoekersidentiteitskaart {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

Als u [!DNL Target Standard] of [!DNL Premium] met [!DNL mbox.js] gebruikt, en u [!UICONTROL Create Global Mbox] voor uw rekening hebt toegelaten, **autocreate globaal synchroon** type van vraag en antwoord wordt gemaakt, ongeacht [!DNL mbox.js] versie.

Als u uw eigen douanecode eerder dan het gebruiken van [!UICONTROL Visual Experience Composer] acties schrijft, zorg ervoor uw code voor een ajax milieu aangewezen is. Als u bijvoorbeeld een JavaScript gebruikt dat `document.write()` bevat, werkt het script niet zoals verwacht.

>[!NOTE]
>
>Meerdere ajax-oproepen met dezelfde naam van de box maar verschillende parameters werken niet op dezelfde pagina. Slechts zal de eerste vraag worden gemaakt.

Als u &quot;auto-creeer globale mbox&quot;maar ook `mboxCreate` vraag op uw pagina gebruikt, bijvoorbeeld, als u [!DNL Target Standard] of [!DNL Premium] op een pagina uitvoert die eerder in een erfenis implementatie gebruikte, worden de globale mbox vraag gemaakt gebruikend het** autocreate globale mbox - standaard** eindpunt en `mboxCreate` vraag wordt gemaakt gebruikend het **standard** eindpunt. Het **standard** eindpuntgebruik `document.write()` om de vraag te maken en te antwoorden. Hierdoor wordt het laden van de pagina geblokkeerd, inclusief de inhoud die in het ajax-antwoord wordt geleverd, totdat alle informatie is gedownload.

Als u alleen mboxCreate gebruikt, bijvoorbeeld op pagina&#39;s die zijn gemaakt met [!DNL Target Classic], werkt de pagina zoals altijd.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon |
| mboxCreate | standaard | standaard | standaard | standaard |

## Implementatie van bezoekersidentiteitskaart aanwezig, maar geen bezoekersidentiteitskaart ingesteld {#section_29888A119C7A4753AD287FC845AA63F4}

Als er geen bezoeker-id is ingesteld, is er geen [!DNL Experience Cloud] bezoekerscookie voor de gebruiker. De pagina roept aan de dienst van identiteitskaart van de Bezoeker uit om bezoekersidentiteitskaart te krijgen Het doel wacht op de reactie met identiteitskaart die de vraag aan [!DNL Target] maakt.

>[!NOTE]
>
>[!DNL Mbox.js] v58 wordt sterk geadviseerd om ervoor te zorgen dat bezoekersidentiteitskaart terugkeert alvorens de vraag van het Doel wordt gemaakt.

Als u [!DNL mbox.js] versie 57 in dit scenario gebruikt, werkt alles zoals het doet als er geen implementatie van bezoekersidentiteitskaart is, zoals die in het vorige scenario wordt beschreven. Vanaf [!DNL mbox.js] versie 58 wordt de [!DNL Experience Cloud Visitor ID] service geretourneerd met een bezoeker-id voordat [!DNL Target] aanroepen worden uitgevoerd. Dit zorgt ervoor dat publieksgegevens die via de kernservice Profielen en Soorten publiek worden gedeeld, beschikbaar zijn voor de eerste [!DNL Target]-oproep in de sessie van de bezoeker. [!DNL Target] verbergt `<BODY>` totdat de bezoeker-id-service terugkeert om te voorkomen dat de standaardinhoud wordt geflikkerd voordat de testinhoud wordt geretourneerd. In versie 58 wordt `display:none` gebruikt om de pagina te verbergen. Dit leidt tot sommige problemen met ontvankelijke plaatsen, zo begin met versie 59, `opacity:0` wordt gebruikt om de inhoud te verbergen.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - asynchroon | Automatisch globale box maken - asynchroon | Automatisch globale box maken - asynchroon |
| mboxCreate | standaard | ajax | ajax | ajax |

## Implementatie van bezoekersidentiteitskaart aanwezig, en bezoekersidentiteitskaart bestaat {#section_9CD4AE4C8186425D886398BC3CE6C46D}

Als het cookie van de bezoeker-id bestaat, hoeft [!DNL Target] de service Bezoeker-id niet aan te roepen. In dit geval hoeft u niet te wachten op de service Bezoeker-id voordat u inhoud weergeeft. Voor versies 57 tot en met 59, wordt **autocreate globale mbox - synchroon** type gebruikt, zodat wacht de pagina op de vraag aan [!DNL Target] om terug te keren alvorens te blijven laden. Zo voorkomt u flikkering van de standaardinhoud. Voor v60 wordt het **globale mbox-asynchrone type** gebruikt om ervoor te zorgen dat [!DNL Target] wacht tot de [!DNL Experience Cloud]-opt-out-service reageert. De opt-out-service maakt deel uit van de Data Co-op-release in de herfst van 2016. Omdat alle vraag gebruikend ajax is teruggekeerd, `document.write()` zou niet met [!DNL mbox.js] versie 60 moeten worden gebruikt.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | autocreate global mbox - asynchroon (ter ondersteuning van de ontwikkeling van de Data Co-op, die later in 2016 zal worden uitgebracht) |
| mboxCreate | standaard | standaard | standaard | ajax |