---
keywords: Doel;publiek, filter;publiek, filter;filter
description: Leer hoe te om publieksfilters in  [!DNL Adobe Target]  te gebruiken om gegevens van bezoekers te bekijken die eigenschappen delen.
title: Kan ik de Filters van het Publiek voor het Melden gebruiken?
feature: Audiences
exl-id: af8dae97-4b10-4edb-a0e6-0d8daf2f0d22
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Auditiefilters voor rapportage

De filters van het publiek (of publiek) in [!DNL Adobe Target] zijn groepen bezoekers die een specifiek kenmerk of een reeks kenmerken delen.

Gebruik publieksfilters om het publiek op te geven dat wordt gebruikt voor rapportage. U kunt een publiek selecteren en zijn prestaties met het algemene verkeer vergelijken. U zou kunnen willen begrijpen of uw winnaars voor de diverse verkeersbronnen verschillend waren, in vergelijking met algemeen verkeer. Met doelfilters kunt u soorten publiek detecteren die mogelijk op verschillende inhoud zijn gericht. Eén winnaar past in veel gevallen niet op alle verkeer.

Bezoekers die vanuit een bepaalde zoekfunctie op de pagina aankomen, kunnen bijvoorbeeld één doelgroep hebben. Andere soorten publiek zijn mogelijk gebaseerd op geslacht, leeftijd, locatie, registratiestatus, aankoopgeschiedenis of andere details die u over uw bezoekers kunt verzamelen. Gebruik publieksfilters om bezoekersverkeer te verdelen en ervaringsprestaties voor elk verkeerssegment te vergelijken.

Houd rekening met de volgende richtlijnen wanneer u publieksfilters wilt gebruiken voor een activiteit:

* **bezoekers kunnen in veelvoudige soorten publiek zijn.** Als er twee soorten publiek zijn ingesteld (bijvoorbeeld &quot;nieuwe bezoekers&quot; en &quot;bezoekers uit Google&quot;) en een persoon aan beide criteria voldoet, wordt deze bezoeker geteld en bijgehouden bij beide soorten publiek. Als gevolg hiervan komt de som van de bezoekers in het publiek niet overeen met het aantal bezoekers in een activiteit.
* **de opstellingspubliek alvorens de activiteit te lanceren.** Poortgegevens kunnen niet met terugwerkende kracht worden opgehaald. Als u publieksfilters niet configureert voordat u de activiteit start, besluit u deze te gebruiken nadat de activiteit een tijdje is uitgevoerd, zult u de gegevens niet verzamelen voor de tijd die al is verstreken.
* **begin met twee tot vier soorten publiek.** Focus op basisinformatie, zoals de verkeersbron.
* **noem zo nodig publiek anders.** U kunt de naam van een publiek wijzigen zonder dat dit invloed heeft op de gegevens, zodat de publieksnaam zinvoller wordt voor de resultaten die worden verzameld, zelfs als de activiteit actief is.
* **ga nauwkeurige waarden in.** Waarden voor het filter Publiek zijn hoofdlettergevoelig. Als u bijvoorbeeld een publiek gebruikt dat op steden filtert, moet u een &quot;OR&quot;-voorwaarde gebruiken om mogelijke spellings- en kapitalisatievariaties op te nemen, zoals &quot;Wenen&quot;, &quot;Wenen&quot;, &quot;Wenen&quot;, &quot;Wenen&quot; en &quot;Wenen&quot;.
* **publiek dat van de [!UICONTROL Audiences] lijst wordt gecreeerd is herbruikbaar.** Soorten publiek dat is gemaakt als onderdeel van een activiteit, kunnen niet opnieuw worden gebruikt.

In de volgende secties vindt u meer informatie over het instellen en rapporteren van doelgroepen:

| Taak | Onderwerp |
|--- |--- |
| Maak de gewenste activiteit of test. | [&#x200B; Activiteiten en Tests &#x200B;](/help/main/c-intro/target-key-concepts.md) |
| Maak zo nodig publiek. | [&#x200B; creeer een Publiek &#x200B;](/help/main/c-target/c-audiences/create-audience.md) |
| Combineer indien nodig meerdere soorten publiek. | [&#x200B; combineer Veelvoudige Soorten van publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md) |
| Pas een publiek toe op de pagina Doelstellingen en instellingen van de activiteit. | A/B Test: [&#x200B; Doelen en de Montages &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md)<br> Automated Personalization: [&#x200B; de Ervaring van Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md)<br> die richt: [&#x200B; Doelen en van de Montages &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md)<br> Multivariate Test: [&#x200B; Doelen en de Aanbevelingen van Montages &#x200B;](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/goals-and-settings.md)<br>: [&#x200B; de montages van de Activiteiten van de Aanbevelingen van de Activiteiten &#x200B;](/help/main/c-recommendations/t-create-recs-activity/recs-activity-settings.md)<br> de Montages van de Activiteit: [&#128279;](/help/main/c-activities/activity-settings.md) |
| Rapporten weergeven met informatie over uw publieksfilters. | [&#x200B; montages van het Rapport &#x200B;](/help/main/c-reports/c-report-settings/report-settings.md) |
