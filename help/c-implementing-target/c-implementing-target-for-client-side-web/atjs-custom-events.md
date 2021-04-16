---
keywords: aangepaste gebeurtenissen;at.js;request is mislukt;request is geslaagd;content rendering is mislukt;content rendering is voltooid;bibliotheek geladen;request start;content rendering start;content rendering geen aanbiedingen;content rendering rediret
description: Gebruik aangepaste gebeurtenissen om de Adobe Target op .js JavaScript-bibliotheek op de hoogte te stellen wanneer een aanvraag of aanbieding voor een box mislukt of slaagt.
title: Hoe gebruik ik aangepaste gebeurtenissen at.js?
feature: at.js
role: Developer
exl-id: 4073210b-b782-48a7-8b69-29eb5cd98fd5
translation-type: tm+mt
source-git-commit: ac4452036f4df35cd80184fc3184f7b676b642dc
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# at.js, aangepaste gebeurtenissen

Informatie over `at.js custom events`, die u laat weten wanneer een mbox- verzoek of een aanbieding ontbreekt of slaagt.

Historisch gezien, liet mbox.js andere code JavaScript die op de pagina loopt niet weten wat achter de scènes gebeurt. Met de vooruitgang van om.js, hadden wij een unieke kans om deze kwestie op te lossen.

Volgens onze klanten zijn er verschillende scenario&#39;s waarvan zij op de hoogte willen worden gesteld, zoals:

* Een mbox-aanvraag is mislukt als gevolg van een time-out, onjuiste statuscode, JSON-parseringsfout, enzovoort.
* Een mbox-verzoek is uitgevoerd.
* Rendering van voorstel is mislukt omdat het element wrapping mbox ontbreekt, de kiezer niet is gevonden, enz.
* Rendering van aanbieding is gelukt. DOM-wijzigingen zijn toegepast.

Vooraf gedefinieerde gebeurtenissen hebben een structuur waarmee u de vereiste gegevens kunt extraheren op basis van het gebeurtenistype.

Om ervoor te zorgen dat gebeurtenissen in verschillende scenario&#39;s kunnen worden gebruikt, hebben de douanegebeurtenissen een ladingsvoorwerp dat aan het detailbezit van het gebeurtenisvoorwerp (dat wordt overgegaan tot de manager) wordt toegewezen. Als u wilt voorkomen dat tekenreeksen worden doorgegeven als naam van een gebeurtenis, worden de gebeurtenissen als constanten weergegeven met behulp van `adobe.target.event` naamruimte.

## Structuur {#section_0E5C9A13DE234A5DAECBCBF9F23F94FE}

| Sleutel | Type | Beschrijving |
|--- |--- |--- |
| type | String | Er zijn verscheidene scenario&#39;s waarin u zou willen worden op de hoogte gebracht om in het vinden, het zuiveren, en het aanpassen van interactie met at.js te helpen.<br>Elke hieronder vermelde aangepaste gebeurtenis heeft twee indelingen: een &quot;constante&quot; en een &quot;tekenreekswaarde&quot;.<ul><li>**Constanten**: Voorafgegaan door  `adobe.target.event.`, in kapitalen weergegeven en onderstrepingstekens bevatten. Als u wilt abonneren op aangepaste gebeurtenissen *after* at.js laadt maar *before* de mbox-reactie is ontvangen, gebruikt u de constante.</li><li>**Tekenreekswaarden**: Kleine letters en bevatten streepjes. Als u zich wilt abonneren op aangepaste gebeurtenissen *before* at.js laadt, gebruikt u de tekenreekswaarde.</li></ul>**Verzoek**<br> FailedConstant:  `adobe.target.event.REQUEST_FAILED`<br>Tekenreekswaarde:  `at-request-failed`<br>Omschrijving: Een mbox-aanvraag is mislukt als gevolg van een time-out, onjuiste statuscode, JSON-parseringsfout, enzovoort.<br>**Verzoek**<br> succesvolConstant:  `adobe.target.event.REQUEST_SUCCEEDED`<br>Tekenreekswaarde:  `at-request-succeeded`<br>Omschrijving: Een box-aanvraag is gelukt.<br>**Renderen van inhoud**<br> FailedConstant:  `adobe.target.event.CONTENT_RENDERING_FAILED`<br>Tekenreekswaarde:  `at-content-rendering-failed`<br>Omschrijving: Rendering van voorstel is mislukt omdat het element wrapping mbox ontbreekt, de kiezer niet is gevonden, enz.<br>**Inhoud renderen**<br> geslaagdConstant:  `adobe.target.event.CONTENT_RENDERING_SUCCEEDED`<br>Tekenreekswaarde:  `at-content-rendering-succeeded`<br>Omschrijving: Rendering van voorstel is gelukt. DOM-wijzigingen zijn toegepast.<br>**Bibliotheek**<br> LoadedConstant:  `adobe.target.event.LIBRARY_LOADED`<br>Tekenreekswaarde:  `at-library-loaded`<br>Omschrijving: Deze gebeurtenis is ideaal om te volgen wanneer at.js volledig geladen is. U kunt deze gebeurtenis gebruiken om de uitvoering van het globale selectievakje aan te passen. U kunt deze gebeurtenis ook gebruiken om de globale mbox onbruikbaar te maken en dan naar deze gebeurtenis te luisteren om globale mbox later te branden.<br>**Request**<br> StartConstant:  `adobe.target.event.REQUEST_START`<br>Tekenreekswaarde:  `at-request-start`<br>Omschrijving: Deze gebeurtenis wordt geactiveerd voordat een HTTP-aanvraag wordt uitgevoerd. U kunt deze gebeurtenis voor prestatiemetingen gebruiken gebruikend het Middel Timing API.<br>**Renderen van inhoud**<br> StartConstant:  `adobe.target.event.CONTENT_RENDERING_START`<br>Tekenreekswaarde:  `at-content-rendering-start`<br>Omschrijving: Deze gebeurtenis wordt geactiveerd voordat de kiezersopiniepeiling wordt gestart en inhoud naar de pagina wordt gerenderd. U kunt deze gebeurtenis gebruiken om de voortgang van de rendering van inhoud bij te houden.<br>**Inhoud renderen geen**<br> OffersConstant:  `adobe.target.event.CONTENT_RENDERING_NO_OFFERS`<br>Tekenreekswaarde:  `at-content-rendering-no-offers`<br>Omschrijving: Deze gebeurtenis wordt geactiveerd wanneer er geen voorstellen worden geretourneerd.<br>**Inhoud renderen**<br> RedirectConstant:  `adobe.target.event.CONTENT_RENDERING_REDIRECT`<br>Tekenreekswaarde:  `at-content-rendering-redirect`<br>Omschrijving: Deze gebeurtenis wordt geactiveerd wanneer een aanbieding een omleiding is en het Doel wordt omgeleid naar een andere URL. |
| mbox | String | naam van mbox |
| message | String | Bevat een beschrijving die leesbaar is voor mensen, zoals wat er is gebeurd, het foutbericht, enzovoort. |
| bijhouden | Object | Bevat `sessionId` en `deviceId`. In sommige gevallen kan `deviceId` ontbreken omdat [!DNL Target] het niet van de Edge-server kan ophalen. |
| type | String | **Artefact voor**<br> succestatie op apparaat:<br>`adobe.target.event.ARTIFACT_DOWNLOAD_SUCCEEDED`<br>tekenreekswaarde:  `artifactDownloadSucceeded`<br>Omschrijving: Wordt aangeroepen wanneer het beslissingsartefact op het apparaat correct is gedownload.<br>**Artefact voor beslissingen op een apparaat**<br> is misluktConstant:  `adobe.target.event.ARTIFACT_DOWNLOAD_FAILED`<br>Tekenreekswaarde:  `artifactDownloadFailed`<br>Omschrijving: Wordt aangeroepen wanneer het beslissingsartefact op het apparaat niet kon worden gedownload. |

## Gebruik {#section_0500FF09D3A04450B5DC8F85C6F793E0}

```javascript
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(event) { 
  console.log('Event', event); 
});
```

## Trainingsvideo: Response Tokens en de aangepaste gebeurtenissen at.js ![Zelfstudie-badge](/help/assets/tutorial.png) {#section_ED304A7137DC42A4BDCD6D57C989F1FA}

Bekijk de volgende video om te leren hoe u de Tokens van de Reactie en de Gebeurtenissen van de Douane bij.js om profielinformatie van Doel aan derdesystemen te delen gebruikt.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
