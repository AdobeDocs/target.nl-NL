---
keywords: faq;veelgestelde vragen;analyses voor doel;a4t;provisioning;provisioning;adobe Experience Cloud
description: Vind antwoorden op vragen die vaak over leveringAnalytics voor  [!DNL Target] (A4T), which lets you use Analytics reporting for [!DNL Target] activiteiten worden gevraagd.
title: Waar kan ik informatie over A4T aanvankelijke levering vinden?
feature: Analyses voor doel (A4T)
exl-id: 4b098444-3e5b-45e3-b635-1857c2c8d183
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# Aanvankelijke levering - Veelgestelde vragen A4T

Dit onderwerp bevat antwoorden op vragen die vaak over levering [!DNL Adobe Analytics] als rapporteringsbron voor [!DNL Adobe Target] (A4T) worden gevraagd.

## Hoe kan ik opstelling een multi-pagina A4T activiteit?

Een standaard A4T-use-case met meerdere pagina&#39;s implementeren:

* Implementeer de JavaScript-bibliotheken voor zowel Doel (at.js of mbox.js) als Analytics op de activiteit die URL/pagina landt. Bij het implementeren van beide oplossingen worden de doelgegevens gekoppeld aan de analysegegevens voor elke bezoeker. Deze gegevens blijven in Analytics tot het met de standaardvervaldatum verloopt die aan 90 dagen wordt geplaatst.

* Voor de resterende pagina&#39;s op de site, waar alleen de gegevens van Analytics moeten worden bijgehouden, implementeert u Analytics op die pagina&#39;s. Het is niet nodig Target op deze pagina&#39;s te implementeren. De metriek Analytics die over die pagina&#39;s wordt gevangen wordt automatisch vastgemaakt aan de activiteit van het Doel de gebruiker oorspronkelijk voor kwalificeerde, die op de informatie van het Doel wordt gebaseerd aan die bezoeker van het voorafgaande kogel in bijlage.

## Hoe kan ik vertellen of A4T op mijn [!DNL Target] rekening wordt toegelaten? {#section_4437D284448F4313BF953D4B6EDBACA6}

Voordat u een rapportsuite kunt selecteren wanneer u een analyseactiviteit definieert, hebt u zowel een Analytics-gebruikersaccount als een Target-gebruikersaccount nodig. Uw gebruikersaccounts moeten zijn geconfigureerd zoals wordt beschreven in de documentatie. Zie [Vereisten voor gebruikersmachtigingen](/help/c-integrating-target-with-mac/a4t/account-reqs.md#concept_4BC06CAB00BF46FF9362AFE98656B083).

Nadat u lid bent van één of meerdere groepen van Experience Cloud die toegang tot Analytics en Doel hebben en u toegang tot alle rapportreeksen hebt, zou u de optie moeten zien om een A/B test tot stand te brengen gebruikend Analytics onder **[!UICONTROL Create Activity]**.

Als zich inrichtingsproblemen voordoen, controleert u of A4T correct is ingericht.

## Waarom laden mijn verslagen niet? {#section_6CC8B2B3568A46C499895EB9811FDC2E}

Controleer het volgende als een van deze problemen optreedt:

* Controleer of uw Analytics- en Target-accounts zijn gekoppeld in de Experience Cloud.
* Sommige klanten gebruiken veelvoudige het bedrijflogins van Analytics in het zelfde bedrijf van Experience Cloud. Als u veelvoudige logins gebruikt, zorg ervoor dat het laatste bedrijf van Analytics u aan het programma hebt geopend dat aan de rekening van het Doel voor de integratie gebonden is.
* Als u zich enkele uren hebt aangemeld bij de Experience Cloud, kan de sessie Analytics soms verlopen. Meld u af en meld u weer aan om het opnieuw te proberen.

## Waarom zie ik geen opties voor Analytics in Doel? {#section_EDD996AFB08B4DB196DD934BE55BF48D}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; Boven. De oorzaak van dit probleem is hetzelfde.

## Waarom zie ik geen A4T rapporten in Analytics? {#section_FEB41E7B7E4F4F78897E4D9F021DEA59}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; hierboven. De oorzaak van dit probleem is hetzelfde.

## Waarom zijn mijn rapporten in [!DNL Target] leeg? {#section_3837104757464CB488C5A83014A669A1}

Zie &quot;Waarom laden mijn rapportsuites niet?&quot; hierboven. De oorzaak van dit probleem is hetzelfde.
