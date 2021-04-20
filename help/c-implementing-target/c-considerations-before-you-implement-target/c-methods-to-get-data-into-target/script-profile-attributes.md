---
keywords: implementeren;implementeren;instellen;instellen;scriptprofielkenmerken
description: Gegevens naar doel ophalen met behulp van scriptprofielkenmerken.
title: Hoe krijg ik gegevens in doel gebruikend de Attributen van het Profiel van het Manuscript?
feature: Implementation
role: Developer
exl-id: c323fb4c-f263-43d4-8523-9f42c2913542
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Scriptprofielkenmerken

De profielattributen van het manuscript zijn naam/waardeparen die in de [!DNL Adobe Target] oplossing worden bepaald. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.

Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd.

## Indeling

Scriptprofielkenmerken worden gemaakt in de sectie Soorten publiek van Doel. Elke kenmerknaam is geldig en de waarde is het resultaat van een JavaScript-functie die door de doelgebruiker is geschreven. De kenmerknaam wordt automatisch voorafgegaan door &quot; gebruiker. &quot; in Doel om ze te onderscheiden van de profielkenmerken in de pagina.

Het codefragment wordt geschreven in de taal Rhino JS en kan naar tokens en andere waarden verwijzen.

## Voorbeelden

* **Afschaffing** van winkelwagentje: Wanneer de bezoeker het winkelwagentje bereikt, stelt u het profielscript in op 1. Wanneer de bezoeker omzet, stel het aan 0 terug. Als de waarde =1 is, bevat de bezoeker een item in de winkelwagentje.
* **Aantal** bezoeken: Bij elk nieuw bezoek verhoogt u het aantal met 1 om te controleren hoe vaak een bezoeker naar de site terugkeert.

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

[Profielscriptkenmerken](/help/c-target/c-visitor-profile/profile-parameters.md#concept_8C07AEAB0A144FECA8B4FEB091AED4D2)
