---
keywords: implementeren;implementeren;instellen;instellen;pagina, parameter;tomcat;url gecodeerd;in-page profiel, kenmerk;mbox, parameter;in-page profiel, kenmerken;script, profielkenmerk;bulk profiel, update-API;single file, update-API;klantkenmerken;gegevensproviders;data provider;data provider
description: Gegevens ophalen in  [!DNL Target] (paginaparameters, profielkenmerken, kenmerken van scriptprofielen, gegevensproviders, API's voor één en één bulkprofielupdate, klantkenmerken).
title: Hoe krijg ik gegevens in het doel?
feature: Implementatie
role: Developer
exl-id: b42eb846-d423-4545-a8fe-0b8048ab689e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Overzicht van methoden

Informatie over de verschillende methodes u kunt gebruiken om gegevens in [!DNL Adobe Target] te krijgen.

Beschikbare methoden zijn:

| Methode | Details |
| --- | --- |
| [Paginaparameters](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/page-parameters.md)<br> (ook wel &quot;parameters mbox&quot; genoemd) | Paginaparameters zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker zijn opgeslagen voor toekomstig gebruik.<br>Paginaparameters zijn handig voor het verzenden van paginagegevens naar Doel die niet met het profiel van de bezoeker hoeven te worden opgeslagen voor toekomstig doelgebruik. Deze waarden worden in plaats daarvan gebruikt om de pagina of de actie te beschrijven die de gebruiker op de specifieke pagina heeft ondernomen. |
| [Profielkenmerken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/in-page-profile-attributes.md)<br> in pagina (ook wel &#39;in-mbox-profielkenmerken&#39; genoemd) | Profielkenmerken in pagina zijn naam-/waardeparen die rechtstreeks door paginacode worden doorgegeven en die in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.<br>Met profielkenmerken van pagina&#39;s kunnen gebruikersspecifieke gegevens in het doelprofiel worden opgeslagen, zodat deze later kunnen worden toegewezen en gesegmenteerd. |
| [Scriptprofielkenmerken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/script-profile-attributes.md) | Scriptprofielkenmerken zijn naam-/waardeparen die zijn gedefinieerd in de doeloplossing. De waarde wordt bepaald door het uitvoeren van een JavaScript-fragment op de server van Target per serveraanroep.<br>Gebruikers schrijven kleine codefragmenten die per mbox vraag uitvoeren, en alvorens een bezoeker voor publiek en activiteitenlidmaatschap wordt geëvalueerd. |
| [Gegevensleveranciers](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/data-providers.md) | Met gegevensproviders kunt u eenvoudig gegevens van derden aan Target doorgeven. |
| [Bulkprofielupdate-API](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/bulk-profile-update-api.md) | Verzend via de API een CSV-bestand naar Target met updates van het bezoekersprofiel voor veel bezoekers. Elk bezoekersprofiel kan met veelvoudige in-pagina profielattributen in één vraag worden bijgewerkt. |
| [API voor bijwerken van één profiel](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/single-profile-update-api.md) | Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand. |
| [Klantkenmerken](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/customer-attributes.md) | Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de Experience Cloud. Gebruik de gegevens in Adobe Analytics en Adobe Target nadat ze zijn geüpload. |












