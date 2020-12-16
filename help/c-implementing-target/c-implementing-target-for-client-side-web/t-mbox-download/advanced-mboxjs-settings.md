---
keywords: advanced mbox.js settings;client;server domain;xdomain;compression level;client session id support;secureOnly;client pc id support;pass page;referring url;traffic level;traffic duration;mboxParameters() function body;mboxSupported() function body;mboxCookieDomain() function body;Extra JavaScript;SiteCatalyst plug-in;Get mbox.js as self-extracting JavaScript;flicker;body hiding;hide body
description: Informatie die u helpt bij het instellen van verschillende instellingen op de pagina mbox.js Settings.
title: mbox.js configureren
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 2%

---


# mbox.js{#configure-mbox-js} configureren

Informatie die u helpt bij het instellen van verschillende instellingen op de pagina mbox.js Settings.

De standaardinstellingen van de functiebibliotheek [!DNL mbox.js] voldoen aan de behoeften van de meeste klanten van [!DNL Target].

Neem indien nodig contact op met uw accountvertegenwoordiger om de [!DNL mbox.js]-instellingen te wijzigen.

De volgende instellingen zijn beschikbaar:

## Client

De clientcode voor uw account.

Als u [!UICONTROL Administration > Implementation] weergeeft, is de client bovenaan de clientcode voor uw account.

## Time-out

The Target request timeout.

Wanneer het bekijken van [!UICONTROL Administration > Implementation], is de Onderbreking (seconden) het plaatsen uw onderbreking van het Verzoek van het Doel. Deze waarde wordt standaard ingesteld op 15 seconden, maar u wordt aangeraden deze waarde in te stellen op een waarde tussen 2 seconden en 5 seconden.

## XDomain

Bepaalt of browser koekjes in uw eigen domein (1st partijkoekjes), het domein van het Doel, of allebei plaatst.

Het wijzigen van deze instelling heeft invloed op zowel mbox.js als at.js.

## Compressieniveau

Hiermee wordt bepaald hoe het bibliotheekbestand mbox.js wordt gecomprimeerd. Als u het compressieniveau verhoogt, neemt de laadtijd van de pagina af.

## hoofdtekst van de functie mboxParameters()

Keert extra parameters terug om tot elke mbox vraag over te gaan.

Bijvoorbeeld:

retourneert &quot;test=123&quot;;

## hoofdtekst van de functie mboxSupported()

Retourneert false om specifieke gebruikers uit te sluiten.

Bijvoorbeeld:

return !navigator.userAgent.indexOf(&#39;Safari&#39;) != -1;

De volgende browsers kunnen worden geaccepteerd of uitgesloten:

* IE 5.0 of hoger (Windows)
* Netscape 5.0 of hoger (Mac, Windows, Linux)
* Safari 1.2.4 of hoger (Mac)
* Mozilla Firefox 1.0 of hoger (Mac, Windows, Linux)

## hoofdtekst van de functie mboxCookieDomain()

Retourneert een tekenreeks die het domein beschrijft dat cookies van eerste partijen moet instellen.

Bijvoorbeeld:

&quot;UW-DOMAIN&quot; terugsturen;

## Extra JavaScript

Bevat alle extra JavaScript die u op elke pagina wilt uitvoeren.

## SiteCatalyst-plug-in

Schakelt de plug-in Analytics Target in.

Als deze optie is ingeschakeld, genereert de plug-in Analytics plug-incode in mbox.js. Hiermee worden de gegevens van de Analytics-tag naar de doelservers verzonden als een box request op elke pagina die is gelabeld met Analytics.

Er moet nog steeds naar de plug-in Analytics op de pagina worden verwezen.

## secureOnly

Geeft aan of mbox.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld.