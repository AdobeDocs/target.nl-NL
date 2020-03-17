---
keywords: advanced mbox.js settings;client;server domain;xdomain;compression level;client session id support;secureOnly;client pc id support;pass page;referring url;traffic level;traffic duration;mboxParameters() function body;mboxSupported() function body;mboxCookieDomain() function body;Extra JavaScript;SiteCatalyst plug-in;Get mbox.js as self-extracting JavaScript;flicker;body hiding;hide body
description: Informatie die u helpt bij het instellen van verschillende instellingen op de pagina mbox.js Settings.
title: mbox.js configureren
uuid: e79c7af7-f8bd-4e2b-8e67-b04eddf0c65d
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# mbox.js configureren{#configure-mbox-js}

Informatie die u helpt bij het instellen van verschillende instellingen op de pagina mbox.js Settings.

De standaardinstellingen van de [!DNL mbox.js] functiebibliotheek voldoen aan de behoeften van de meeste [!DNL Target] klanten.

Neem indien nodig contact op met uw accountvertegenwoordiger om de [!DNL mbox.js] instellingen te wijzigen.

De volgende instellingen zijn beschikbaar:

## Client

De clientcode voor uw account.

Bij weergave [!UICONTROL Setup > Implementation > Edit Mbox.js Settings]is de client bovenaan de clientcode voor uw account.

## Time-out

The Target request timeout.

Bij weergave [!UICONTROL Setup > Implementation > Edit Mbox.js Settings]is de time-out voor time-out na compressieniveau de time-out voor uw doelverzoek. Deze waarde wordt standaard ingesteld op 15 seconden, maar u wordt aangeraden deze waarde in te stellen op een waarde tussen 2 seconden en 5 seconden.

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

## Insteekmodule SiteCatalyst

Schakelt de plug-in Analytics Target in.

Als deze optie is ingeschakeld, genereert de plug-in Analytics plug-incode in mbox.js. Hiermee worden de gegevens van de Analytics-tag naar de doelservers verzonden als een box request op elke pagina die is gelabeld met Analytics.

Er moet nog steeds naar de plug-in Analytics op de pagina worden verwezen.

## secureOnly

Geeft aan of mbox.js alleen HTTPS mag gebruiken of mag schakelen tussen HTTP en HTTPS op basis van het paginaprotocol. Dit is een geavanceerde instelling die standaard op Onwaar wordt ingesteld.