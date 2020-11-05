---
keywords: faq;frequently asked questions;analytics for target;a4t;provisioning;provisioning;adobe Experience Cloud
description: Dit onderwerp bevat antwoorden op vragen die vaak over leveringAnalytics als rapporteringsbron voor Doel (A4T) worden gevraagd.
title: Aanvankelijke levering - Veelgestelde vragen A4T
feature: a4t troubleshooting
topic: Standard
uuid: cc80f879-ad2a-46d6-adc2-df616e8ab0b5
translation-type: tm+mt
source-git-commit: 95450abc32be19d04b791af3c62673e9411ab53c
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---


# Aanvankelijke levering - Veelgestelde vragen A4T{#initial-provisioning-a-t-faq}

Dit onderwerp bevat antwoorden op vragen die vaak over leveringAnalytics als rapporteringsbron voor Doel (A4T) worden gevraagd.

## Hoe kan ik opstelling een multi-pagina A4T activiteit?

Een standaard A4T-use-case met meerdere pagina&#39;s implementeren:

* Implementeer de JavaScript-bibliotheken voor zowel Doel (at.js of mbox.js) als Analytics op de activiteit die URL/pagina landt. Bij het implementeren van beide oplossingen worden de doelgegevens gekoppeld aan de analysegegevens voor elke bezoeker. Deze gegevens blijven in Analytics tot het met de standaardvervaldatum verloopt die aan 90 dagen wordt geplaatst.

* Voor de resterende pagina&#39;s op de site, waar alleen de gegevens van Analytics moeten worden bijgehouden, implementeert u Analytics op die pagina&#39;s. Het is niet nodig Target op deze pagina&#39;s te implementeren. De metriek Analytics die over die pagina&#39;s wordt gevangen wordt automatisch vastgemaakt aan de activiteit van het Doel de gebruiker oorspronkelijk voor kwalificeerde, die op de informatie van het Doel wordt gebaseerd aan die bezoeker van het voorafgaande kogel in bijlage.

## Hoe kan ik vertellen of A4T op mijn rekening van het Doel wordt toegelaten? {#section_4437D284448F4313BF953D4B6EDBACA6}

Voordat u een rapportsuite kunt selecteren wanneer u een analyseactiviteit definieert, hebt u zowel een Analytics-gebruikersaccount als een Target-gebruikersaccount nodig. Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de documentatie. Zie [Vereisten](/help/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083) voor gebruikersmachtigingen.

Als u lid bent van een of meer Experience Cloud-groepen die toegang hebben tot Analytics en Target en u toegang hebt tot alle rapportsuites, kunt u beter een A/B-test maken met Analytics onder **[!UICONTROL Create Activity]**.

Als zich inrichtingsproblemen voordoen, controleert u of A4T correct is ingericht.

## Waarom laden mijn verslagen niet? {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Controleer het volgende als een van deze problemen optreedt:

* Zorg ervoor dat uw Analytics- en Target-accounts zijn gekoppeld in de Experience Cloud.
* Als u veelvoudige het bedrijflogins van Analytics in het zelfde bedrijf van Experience Cloud gebruikt, zorg ervoor dat het laatste bedrijf van Analytics u het programma opent is die aan de rekening van het Doel voor de integratie gebonden is.
* Als u zich enkele uren hebt aangemeld bij de Experience Cloud, kan de sessie Analytics soms verlopen. Meld u af en meld u weer aan om het opnieuw te proberen.

## Waarom zie ik geen opties voor Analytics in Doel? {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; hierboven. De oorzaak van dit probleem is hetzelfde.

## Waarom zie ik geen A4T rapporten in Analytics? {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; hierboven. De oorzaak van dit probleem is hetzelfde.

## Waarom zijn mijn rapporten in Target leeg? {#section_3837104757464CB488C5A83014A669A1}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; hierboven. De oorzaak van dit probleem is hetzelfde.
