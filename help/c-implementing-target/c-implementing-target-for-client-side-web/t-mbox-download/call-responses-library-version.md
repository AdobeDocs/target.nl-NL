---
description: De manier waarop Doel maakt en reageert op aanroepen vanuit uw pagina is afhankelijk van de versie van de doelbibliotheek die u gebruikt, of de Experience Cloud Visitor ID-implementatie aanwezig is en of de bezoeker-id bestaat.
title: Methoden voor doelpagina's door bibliotheekversie mbox.js
feature: null
uuid: 66f7753e-d9c1-4efa-8b10-fd637c8f53f6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Methoden voor doelpagina&#39;s door bibliotheekversie mbox.js{#target-page-methods-by-mbox-js-library-version}

De manier waarop Doel maakt en reageert op aanroepen vanuit uw pagina is afhankelijk van de versie van de doelbibliotheek die u gebruikt, of de Experience Cloud Visitor ID-implementatie aanwezig is en of de bezoeker-id bestaat.

>[!NOTE]
>
>Als u gebruikt [!DNL at.js], worden alle vraag gemaakt gebruikend JSON. Deze pagina bevat informatie over [!DNL mbox.js] bibliotheekversies. De gedragingen die in de onderstaande scenario&#39;s worden beschreven, zijn niet van toepassing op [!DNL at.js].

Deze sectie verstrekt informatie over hoe elke versie van de [!DNL Target] bibliotheek aan de [!DNL Target] vraag van uw pagina in elk van de volgende scenario&#39;s antwoordt.

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
>Voor elk type behalve standaard moeten alle aangepaste code en aanbiedingen worden geschreven ter ondersteuning van een ajax-omgeving. Als u bijvoorbeeld een JavaScript gebruikt dat `document.write()`het script bevat, werkt het niet zoals u had verwacht.

## Geen implementatie van bezoeker-id {#section_C6F7213FDE4D48E8BBCB1A9A26310FEE}

Als u gebruikt [!DNL Target Standard] of [!DNL Premium] met [!DNL mbox.js], en u [!UICONTROL Create Global Mbox] voor uw rekening hebt toegelaten, **autocreate globaal mbox synchroon** type van vraag en reactie wordt gemaakt, ongeacht [!DNL mbox.js] versie.

Als u uw eigen douanecode eerder dan het gebruiken van de [!UICONTROL Visual Experience Composer] acties schrijft, zorg ervoor uw code voor een ajax milieu aangewezen is. Als u bijvoorbeeld een JavaScript gebruikt dat `document.write()`het script bevat, werkt het niet zoals u had verwacht.

>[!NOTE]
>
>Meerdere ajax-oproepen met dezelfde naam van de box maar verschillende parameters werken niet op dezelfde pagina. Slechts zal de eerste vraag worden gemaakt.

Als u &quot;auto-creeer globale mbox&quot;maar ook `mboxCreate` vraag op uw pagina gebruikt, bijvoorbeeld, als u implementeert [!DNL Target Standard] of [!DNL Premium] op een pagina die eerder in een erfenisimplementatie gebruikte, worden de globale mbox vraag gemaakt gebruikend het** autocreate globale mbox - standard** eindpunt en de `mboxCreate` vraag wordt gemaakt gebruikend het **standaardeindpunt** . Het **standaardeindpuntgebruik** `document.write()` om de vraag te maken en te antwoorden. Hierdoor wordt het laden van de pagina geblokkeerd, inclusief de inhoud die in het ajax-antwoord wordt geleverd, totdat alle informatie is gedownload.

Als u alleen mboxCreate gebruikt, bijvoorbeeld op pagina&#39;s die u hebt gemaakt [!DNL Target Classic], werkt de pagina zoals deze altijd werkt.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon |
| mboxCreate | standaard | standaard | standaard | standaard |

## Implementatie van bezoekersidentiteitskaart aanwezig, maar geen bezoekersidentiteitskaart ingesteld {#section_29888A119C7A4753AD287FC845AA63F4}

Als er geen bezoeker-id is ingesteld, is er geen [!DNL Experience Cloud] bezoekerscookie voor de gebruiker. De pagina roept aan de dienst van identiteitskaart van de Bezoeker uit om bezoekersidentiteitskaart te krijgen Het doel wacht op de reactie met identiteitskaart die de vraag aan maakt. [!DNL Target]

>[!NOTE]
>
>[!DNL Mbox.js] v58 wordt sterk geadviseerd om ervoor te zorgen dat bezoekersidentiteitskaart terugkeert alvorens de vraag van het Doel wordt gemaakt.

Als u versie 57 in dit scenario gebruikt, werkt alles zoals het doet als er geen implementatie van bezoekersidentiteitskaart is, zoals die in het vorige scenario wordt beschreven. [!DNL mbox.js] Vanaf [!DNL mbox.js] versie 58 retourneert de [!DNL Experience Cloud Visitor ID] service een bezoekersidentiteitskaart voordat er [!DNL Target] aanroepen worden uitgevoerd. Dit zorgt ervoor dat publieksgegevens die via de kernservice Profielen en Soorten publiek worden gedeeld, beschikbaar zijn voor de eerste [!DNL Target] oproep in de sessie van de bezoeker. Om flikkering van standaardinhoud te voorkomen alvorens de inhoud van de test terugkeert, [!DNL Target] verbergt het `<BODY>` tot de dienst van bezoekersidentiteitskaart terugkeert. In versie 58 `display:none` wordt gebruikt om de pagina te verbergen. Dit leidt tot sommige problemen met ontvankelijke plaatsen, zo begin met versie 59, `opacity:0` wordt gebruikt om de inhoud te verbergen.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - asynchroon | Automatisch globale box maken - asynchroon | Automatisch globale box maken - asynchroon |
| mboxCreate | standaard | ajax | ajax | ajax |

## Implementatie bezoeker-id is aanwezig en bezoeker-id bestaat {#section_9CD4AE4C8186425D886398BC3CE6C46D}

Als het cookie van de bezoeker-id bestaat, hoeft u [!DNL Target] geen aanroep te doen naar de service Bezoeker-id. In dit geval hoeft u niet te wachten op de service Bezoeker-id voordat u inhoud weergeeft. Voor versies 57 tot en met 59, wordt **autocreate globale mbox - synchroon** [!DNL Target] type gebruikt, zodat wacht de pagina op de vraag om terug te keren alvorens te blijven laden. Zo voorkomt u flikkering van de standaardinhoud. Voor v60, wordt het **globale mbox-asynchrone type** gebruikt om te verzekeren [!DNL Target] wacht op de [!DNL Experience Cloud] opt-out dienst om te antwoorden. De opt-out-service maakt deel uit van de Data Co-op-release in de herfst van 2016. Omdat alle vraag gebruikend ajax is teruggekeerd, `document.write()` zou niet met [!DNL mbox.js] versie 60 moeten worden gebruikt.

| Aanmaakmethode | mbox.js v57 | mbox.js v58 | mbox.js v59 | mbox.js v60 |
|---|---|---|---|---|
| globale mbox automatisch maken | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | Automatisch globale box maken - synchroon | autocreate global mbox - asynchroon (ter ondersteuning van de ontwikkeling van de Data Co-op, die later in 2016 zal worden uitgebracht) |
| mboxCreate | standaard | standaard | standaard | ajax |