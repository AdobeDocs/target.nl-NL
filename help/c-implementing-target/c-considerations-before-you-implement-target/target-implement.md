---
keywords: document.write;target;Implementeren;doel implementeren;dtm;at.js;mbox.js;target.js;mbox;mbox;adobe Experience platform web skd;aep web sdk;web sdk
description: Voer Adobe [!DNL Target] by referencing the [!DNL Target] bibliotheken (at.js of mbox.js) op uw Web-pagina's uit.
title: De [!DNL Target] JavaScript-bibliotheken begrijpen
feature: Implementatie
source-git-commit: dd20791535e47c83d0f0ac60addfe0888748f86a
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# De JavaScript-bibliotheken [!DNL Target] begrijpen

Implementeer [!DNL Adobe Target] door te verwijzen naar de [!DNL Adobe Target]-bibliotheken (Adobe Experience Platform Web SDK of at.js) op uw webpagina&#39;s.

>[!NOTE]
>
>De bibliotheek mbox.js wordt niet meer ontwikkeld. Alle klanten moeten vóór 31 maart 2021 migreren van mbox.js naar at.js of naar [!UICONTROL Adobe Experience Platform Web SDK].

## Verschillen tussen de JavaScript-bibliotheken [!DNL Target] {#section_40117C78C2F84FECAC4F1BA40CC4F171}

In de volgende tabel worden de verschillen tussen de JavaScript-bibliotheken [!DNL Target] uitgelegd:

| Bibliotheekreferentie | Beschrijving |
|--- |--- |
| Adobe Experience Platform Web SDK | Met [!UICONTROL Adobe Experience Platform Web SDK] kunt u via het Adobe Experience Edge Network communiceren met de verschillende services in [!DNL Experience Cloud] (inclusief [!DNL Target]). Als u ervoor kiest om naar [!DNL Adobe Experience Platform Web SDK] te migreren, zie [Wat is Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) in *Web SDK Guide*. |
| at.js | at.js vervangt mbox.js voor [!DNL [!DNL Target]] implementaties.<br>Met at.js worden onder andere de laadtijden voor webimplementaties verbeterd, wordt de beveiliging verbeterd, wordt voorkomen dat documenten.write-waarschuwingen in Google Chrome verschijnen en worden betere implementatieopties geboden voor toepassingen van één pagina. |

## Effect van at.js op de tijd van het laden van de pagina {#section_16630CD0FF0A498EB596A51381366A5A}

Veel klanten en consultants willen weten wat de impact is van [!DNL at.js] op de laadtijd van pagina&#39;s, met name in de context van nieuwe gebruikers of gebruikers die de pagina&#39;s retourneren. Jammer genoeg, is het moeilijk om concrete aantallen betreffende te meten en te geven hoe [!DNL at.js] paginaladingstijd wegens de implementatie van elke klant beïnvloedt.

Als de API voor bezoekers echter aanwezig is op de pagina, kan [!DNL Target] beter begrijpen hoe [!DNL at.js] de laadtijd van pagina&#39;s beïnvloedt.

>[!NOTE]
>
>De API voor bezoekers en [!DNL at.js] hebben alleen invloed op de laadtijd van de pagina wanneer u de globale box gebruikt (vanwege de techniek voor het verbergen van de hoofdtekst). De regionale mboxes worden niet beïnvloed door de integratie van de Bezoeker API.

De volgende secties beschrijven de opeenvolging van acties voor nieuwe en terugkerende bezoekers:

### Nieuwe bezoekers

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js wordt geladen, geparseerd en uitgevoerd.
1. Als global mbox auto-create is ingeschakeld, gebruikt u de JavaScript-bibliotheek [!DNL Target]:

   * Instantieert het object Visitor.
   * De [!DNL Target] bibliotheek probeert [!UICONTROL Experience Cloud Visitor ID] gegevens terug te winnen.
   * Voor een nieuwe bezoeker wordt door de API van de bezoeker een aanvraag voor een ander domein geactiveerd naar `demdex.net`.
   * Nadat [!UICONTROL Experience Cloud Visitor ID] gegevens worden teruggewonnen, wordt een verzoek aan Doel in brand gestoken.

### Bezoekers terugsturen

1. De bezoeker-API wordt geladen, geparseerd en uitgevoerd.
1. at.js wordt geladen, geparseerd en uitgevoerd.
1. Als global mbox auto-create is ingeschakeld, gebruikt u de JavaScript-bibliotheek [!DNL Target]:

   * Instantieert het object Visitor.
   * De [!DNL Target] bibliotheek probeert [!UICONTROL Experience Cloud Visitor ID] gegevens terug te winnen.
   * De bezoeker-API haalt gegevens op uit cookies.
   * Nadat [!UICONTROL Experience Cloud Visitor ID] gegevens worden teruggewonnen, wordt een verzoek aan [!DNL Target] in brand gestoken.

>[!NOTE]
>
>Wanneer de Bezoeker-API aanwezig is voor nieuwe bezoekers, gaat [!DNL Target] meerdere keren over de kabel om ervoor te zorgen dat [!DNL Target]-aanvragen [!UICONTROL Experience Cloud Visitor ID]-gegevens bevatten. Voor het terugkeren van bezoekers, [!DNL Target] gaat over de draad slechts aan [!DNL Target] om de gepersonaliseerde inhoud terug te winnen.
