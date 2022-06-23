---
keywords: implementeren;implementeren;instellen;instellen;scriptprofielkenmerken
description: Gegevens ophalen in [!DNL Target] scriptprofielkenmerken gebruiken.
title: Hoe krijg ik gegevens in [!DNL Target] Kenmerken scriptprofiel gebruiken?
feature: Implementation
role: Developer
exl-id: c323fb4c-f263-43d4-8523-9f42c2913542
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Scriptprofielkenmerken

Scriptprofielkenmerken zijn naam-/waardeparen die zijn gedefinieerd in het dialoogvenster [!DNL Adobe Target] oplossing. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.

Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd.

## Indeling

Scriptprofielkenmerken worden gemaakt in de sectie Soorten publiek van Doel. Elke kenmerknaam is geldig en de waarde is het resultaat van een JavaScript-functie die door de doelgebruiker is geschreven. De kenmerknaam wordt automatisch voorafgegaan door &quot; gebruiker. &quot; in Doel om ze te onderscheiden van de profielkenmerken in de pagina.

Het codefragment wordt geschreven in de taal Rhino JS en kan naar tokens en andere waarden verwijzen.

## Voorbeelden

* **Afschaffing van winkelwagentjes**: Wanneer de bezoeker het winkelwagentje bereikt, stelt u het profielscript in op 1. Wanneer de bezoeker omzet, stel het aan 0 terug. Als de waarde =1 is, bevat de bezoeker een item in de winkelwagentje.
* **Aantal bezoeken**: Bij elk nieuw bezoek verhoogt u het aantal met 1 om te controleren hoe vaak een bezoeker naar de site terugkeert.

## Voordelen van de methode

Er zijn geen updates van paginacode vereist.

Voert uit vóór publiek en de besluiten van het activiteitenlidmaatschap, zodat kunnen deze attributen van het profielmanuscript lidmaatschap op één enkele servervraag beïnvloeden.

Kan zeer robuust zijn. Er kunnen maximaal 2000 instructies per script worden uitgevoerd.

## Caveats

Hiervoor is JavaScript-kennis vereist.

De uitvoeringsvolgorde van profielscripts kan niet worden gegarandeerd, zodat ze niet op elkaar kunnen vertrouwen.

Kan moeilijk zijn om fouten op te sporen.

## Codevoorbeelden

Profielscripts zijn tamelijk flexibel:

`user.purchase_recency: var dayInMillis = 3600 * 24 * 1000; if (mbox.name == 'orderThankyouPage') {  user.setLocal('lastPurchaseTime', new Date().getTime()); } var lastPurchaseTime = user.getLocal('lastPurchaseTime'); if (lastPurchaseTime) {  return ((new Date()).getTime()-lastPurchaseTime)/dayInMillis; }`

### Koppelingen naar relevante informatie

[Profielscriptkenmerken](/help/main/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)
