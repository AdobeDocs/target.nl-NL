---
keywords: mbox-functies
description: Meer informatie over de oudere mbox.js-implementatie van Adobe Target. Migreer naar de Adobe Experience Platform Web SDK (AEP Web SDK) of naar de nieuwste versie van at.js.
title: Welke Functies steunt mbox.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# mbox.js functies{#mbox-js-functions}

Lijst met mbox.js-functies die moeten worden gebruikt bij het implementeren met mbox.js.

>[!IMPORTANT]
>
>**mbox.js end-of-life**: Op 31 maart 2021  [!DNL Adobe Target] wordt de bibliotheek mbox.js niet meer ondersteund. Na 31 maart 2021 zullen alle aanroepen van mbox.js netjes mislukken en van invloed zijn op uw pagina&#39;s die [!DNL Target] activiteiten hebben die door standaardinhoud te dienen worden uitgevoerd.
>
>We raden alle klanten aan vóór deze datum te migreren naar de meest recente versie van de nieuwe [!DNL Adobe Experience Platform Web SDK] of de JavaScript-bibliotheek at.js om mogelijke problemen met uw sites te voorkomen. Voor meer informatie, zie [Overzicht: Implementeer Doel voor client-side web](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

>[!NOTE]
>
>Als u [!DNL at.js] gebruikt, zijn deze methodes niet van toepassing.

| Methode | Notities |
|--- |--- |
| `mbox.getName()` |  |
| `mbox.getURL()` |  |
| `mbox.getDiv()` | Hiermee wordt de div geretourneerd die aan de mbox is gekoppeld (met standaardinhoud of een aanbieding) |
| `mbox.getParameters()` | Een array van parameters met twee velden, naam en waarde |
| `mbox.setOnError()` | Voorbeeld:<br>`mbox.setOnError(function() { alert(this.getName() +" had error"});` |
| `mbox.setMessage(message)` | U kunt een bericht zien in het venster Foutopsporing. |
| `mboxCurrent.activate()` |  |
| `mboxCurrent.cancelTimeout()` |  |
| `mboxCurrent.finalize()` |  |
| `mboxCurrent.getDefaultDiv()` |  |
| `mboxCurrent.getDiv()` | Hiermee wordt de div geretourneerd die aan de mbox is gekoppeld (met standaardinhoud of een aanbieding) |
| `mboxCurrent.getEventTimes()` |  |
| `mboxCurrent.getFetcher()` |  |
| `mboxCurrent.getId()` |  |
| `mboxCurrent.getImportName()` |  |
| `mboxCurrent.getName()` |  |
| `mboxCurrent.getOffer()` |  |
| `mboxCurrent.getParameters()` | Een array van parameters met twee velden, naam en waarde. |
| `mboxCurrent.getURL()` |  |
| `mboxCurrent.getURLBuilder()` |  |
| `mboxCurrent.hide()` |  |
| `mboxCurrent.isActivated`() |  |
| `mboxCurrent.load()` |  |
| `mboxCurrent.loaded()` |  |
| `mboxCurrent.setEventTime()` |  |
| `mboxCurrent.setFetcher()` |  |
| `mboxCurrent.setMessage()` |  |
| `mboxCurrent.setMessage(message)` | Bericht weergeven in venster Foutopsporing. |
| `mboxCurrent.setOffer()` |  |
| `mboxCurrent.setOnError()` | Voorbeeld:<br>`mboxCurrent.setOnError(function(){ alert(this.getName() +" had error"});` |
| `mboxCurrent.setOnLoad()` | Voorbeeld:<br>`mboxCurrent.setOnLoad(function(){alert(this.getName()+" loaded")});` |
| `mboxCurrent.show()` |  |
| `mboxCurrent.showContent()` |  |
| `mboxFactoryDefault.addOnLoad(action)` | Actie wordt aangeroepen wanneer de pagina wordt geladen. |
| `mboxFactoryDefault.getMboxes().each()` | Voorbeeld:<br>`mboxFactoryDefault.getMboxes().each(function() { alert(mbox.getName()) };` |
| `mboxFactoryDefault.getMboxes().length()` |  |
| `mboxFactoryDefault.getPageId()` |  |
| `mboxFactoryDefault.getPCId().getId()` |  |
| `mboxFactoryDefault.getSessionId().getId()` |  |
| `mboxFactories.get('default').getSessionId()&#x200B;.forceId("1276011116668");` |  |
| `mboxFactories.get('default').getPCId()&#x200B;.forceId("1276011116668");` |  |
| `mboxFactoryDefault.create()` |  |
| `mboxFactoryDefault.disable()` |  |
| `mboxFactoryDefault.enable()` |  |
| `mboxFactoryDefault.get()` |  |
| `mboxFactoryDefault.getCookieManager()` |  |
| `mboxFactoryDefault.getDisableReason()` |  |
| `mboxFactoryDefault.getEllapsedTime()` |  |
| `mboxFactoryDefault.getEllapsedTimeUntil()` |  |
| `mboxFactoryDefault.getMboxes()` | Retourneert een `mboxList`. |
| `mboxFactoryDefault.getSignaler()` |  |
| `mboxFactoryDefault.getURLBuilder()` |  |
| `mboxFactoryDefault.isAdmin()` |  |
| `mboxFactoryDefault.isDomLoaded()` |  |
| `mboxFactoryDefault.isEnabled()` |  |
| `mboxFactoryDefault.isSupported()` |  |
| `mboxFactoryDefault.limitTraffic()` |  |
| `mboxFactoryDefault.update()` |  |
| `mboxFactoryDefault.getCookieManager()&#x200B;.getCookie("name")//!= null) {` |  |
| `mboxFactoryDefault.getCookieManager()&#x200B;.setCookie(_name,_value, _duration);` |  |