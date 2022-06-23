---
keywords: implementeren;implementeren;instellen;instellen;pagina, parameter;tomcat;url gecodeerd;in-page profiel, kenmerk;mbox, parameter;in-page profiel, kenmerken;script, profielkenmerk;bulk profiel, update-API;single file, update-API;klantkenmerken;gegevensproviders;data provider;data provider
description: Gegevens ophalen in [!DNL Target] (paginaparameters, profielkenmerken, scriptprofielkenmerken, gegevensproviders, API's voor één en één bulkprofielupdate, klantkenmerken).
title: Hoe krijg ik gegevens in het doel?
feature: Implementation
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Overzicht van methoden

Informatie over de verschillende methoden waarmee u gegevens kunt ophalen [!DNL Adobe Target].

Beschikbare methoden zijn:

| Methode | Details |
| --- | --- |
| [Paginaparameters](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/page-parameters/)<br>(Wordt ook wel &quot;parameters mbox&quot; genoemd) | Paginaparameters zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik.<br>Paginaparameters zijn handig voor het verzenden van paginagegevens naar Doel die niet met het profiel van de bezoeker hoeven te worden opgeslagen voor toekomstig doelgebruik. Deze waarden worden in plaats daarvan gebruikt om de pagina of de actie te beschrijven die de gebruiker op de specifieke pagina heeft ondernomen. |
| [Profielkenmerken in pagina](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/in-page-profile-attributes/)<br>(Wordt ook wel &#39;&#39;in-mbox-profielkenmerken&#39; genoemd) | Profielkenmerken in pagina zijn naam-/waardeparen die rechtstreeks door paginacode worden doorgegeven en die in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.<br>Met profielkenmerken van pagina&#39;s kunnen gebruikersspecifieke gegevens in het doelprofiel worden opgeslagen, zodat deze later kunnen worden toegewezen en gesegmenteerd. |
| [Scriptprofielkenmerken](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/script-profile-attributes/) | Scriptprofielkenmerken zijn naam-/waardeparen die zijn gedefinieerd in de doeloplossing. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.<br>Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd. |
| [Gegevensleveranciers](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/data-providers/) | Met gegevensproviders kunt u eenvoudig gegevens van derden aan Target doorgeven. |
| [Bulkprofielupdate-API](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/bulk-profile-update-api/) | Verzend via de API een CSV-bestand naar Target met updates van het bezoekersprofiel voor veel bezoekers. Elk bezoekersprofiel kan met veelvoudige in-pagina profielattributen in één vraag worden bijgewerkt. |
| [API voor bijwerken van één profiel](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/single-profile-update-api/) | Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand. |
| [Klantkenmerken](https://developer.adobe.com/target/before-implement/methods-to-get-data-into-target/customer-attributes/) | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik de gegevens in Adobe Analytics en Adobe Target nadat ze zijn geüpload. |












