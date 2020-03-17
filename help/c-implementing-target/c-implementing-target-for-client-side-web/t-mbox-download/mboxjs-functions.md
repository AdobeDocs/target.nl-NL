---
keywords: mbox functions
description: Lijst met mbox.js-functies die moeten worden gebruikt bij het implementeren met mbox.js.
title: mbox.js, functies
uuid: f503bc44-a664-4d09-82dc-80a1198ad9d0
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# mbox.js, functies{#mbox-js-functions}

Lijst met mbox.js-functies die moeten worden gebruikt bij het implementeren met mbox.js.

>[!NOTE]
>
>Deze methoden zijn niet van toepassing als u [!DNL at.js]ze gebruikt.

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