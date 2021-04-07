---
keywords: implementeren;implementeren;instellen;instellen;pagina, parameter
description: Gegevens naar doel ophalen met de profielkenmerken van de pagina.
title: Hoe krijg ik gegevens in doel gebruikend de Attributen van het Profiel in-Pagina?
feature: Implementatie
role: Developer
translation-type: tm+mt
source-git-commit: 70d4c5b4166081751246e867d90d43b67efa5469
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Profielkenmerken in pagina

Profielkenmerken in pagina&#39;s in [!DNL Adobe Target] (ook wel &#39;in-mbox-profielkenmerken&#39; genoemd) zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.

Met profielkenmerken van pagina&#39;s kunnen gebruikersspecifieke gegevens in het doelprofiel worden opgeslagen, zodat deze later kunnen worden toegewezen en gesegmenteerd.

## Indeling

Profielkenmerken in pagina&#39;s worden doorgegeven aan Target via een serveraanroep als een naam-/waardepaar met het voorvoegsel &quot;profiel&quot;. vóór de kenmerknaam.

Kenmerknamen en -waarden kunnen worden aangepast (hoewel er enkele &#39;gereserveerde namen&#39; zijn voor specifieke toepassingen).

### Voorbeelden

* `profile.membershipLevel=silver`
* `profile.visitCount=3`

## Voorbeelden van gebruiksgevallen

* **Aanmeldingsgegevens**: Deel niet-PII (Persoonlijk Identificeerbare Informatie) gegevens aan Doel die op login van de gebruiker wordt gebaseerd. Dit kunnen lidmaatschapsstatus, ordergeschiedenis of meer zijn.
* **Winkelgegevens**: Houd bij welke winkel de voorkeurslocatie van deze gebruiker is.
* **Vorige interacties**: Volg wat de gebruiker eerder op de site heeft gedaan om toekomstige personalisatie te informeren.

## Voordelen van de methode

De gegevens worden verzonden naar Doel in echt - tijd, en kunnen op de zelfde servervraag worden gebruikt waarop de gegevens binnen komen.

## Caveats

Vereist updates van paginacode (direct of via een systeem van het markeringsbeheer).

Kenmerken en waarden zijn zichtbaar in serveraanroepen, zodat een bezoeker de waarden kan zien. Als het delen van informatie zoals kredietbereiken of andere potentieel particuliere informatie, zou deze methode niet de beste benadering kunnen zijn.

## Codevoorbeelden

targetPageParamsAll (voegt de kenmerken toe aan alle mbox-aanroepen op de pagina):

`function targetPageParamsAll() { return "profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

targetPageParams (voegt de kenmerken toe aan het globale mabox op de pagina):

`function targetPageParams() { return profile.param1=value1&profile.param2=value2&profile.p3=hello%20world"; }`

Attributen in mboxCreate code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','profile.param1=value1','profile.param2=value2'); </script>`

## Koppelingen naar relevante informatie

[Profielkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#concept_01A30B4762D64CD5946B3AA38DC8A201)

[Bezoekerprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E)