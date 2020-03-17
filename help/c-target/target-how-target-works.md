---
keywords: targeting;cookie;first-party cookie;1st-party cookie
description: Adobe Target kan met uw webpagina's worden geïntegreerd via de JavaScript-bibliotheek at.js of mbox.js.
title: Hoe doelgericht werken
uuid: 8b5a36c0-555d-42c5-8b24-c08d07440a53
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Hoe doelgericht werken{#how-targeting-works}

Adobe Target kan met uw webpagina&#39;s worden geïntegreerd via de JavaScript-bibliotheek at.js of mbox.js.

[!DNL Target Classic] heeft vakken gebruikt rond elk gebied op de pagina waar u de doelinhoud wilt weergeven of gegevens wilt verzamelen. Deze vakken zijn niet vereist in [!DNL Target Standard]. In plaats daarvan is één JavaScript-bibliotheek waarnaar op elke pagina wordt verwezen, alles wat u nodig hebt om uw optimalisatieactiviteiten uit te voeren.

Telkens wanneer een bezoeker een pagina aanvraagt die geschikt is voor Doel, [!DNL Target] gebruikt u het volgende proces om aanbiedingen te verzenden:

1. Een klant vraagt om een pagina van uw server en het toont in browser.
1. In de browser van de klant wordt een cookie van de eerste partij ingesteld om een unieke bezoeker-id in te stellen.

   Er [!DNL Experience Cloud visitor ID] wordt ook een instelling ingesteld als u het Master Marketing Profile gebruikt.

1. De pagina doet een oproep aan [!DNL Target] of via het [!DNL target.js] dossier of een doos op uw pagina.
1. [!DNL Target] verwijst naar het profiel dat aan de bezoeker is gekoppeld.
1. [!DNL Target] Hiermee worden alle profielscripts uitgevoerd die aan dat profiel zijn gekoppeld.
1. [!DNL Target] berekent de reactie.
1. De inhoud wordt weergegeven op basis van de regels van uw activiteit of campagne.

Het aanbod dat in een basis A/B test wordt getoond wordt willekeurig gekozen. Als resultaat van deze willekeurige splitsing van verkeer, kan het veel eerste verkeer vóór de percentages uit nemen. Als u bijvoorbeeld een activiteit met twee ervaringen hebt, wordt de startervaring willekeurig gekozen. Als er weinig verkeer is, is het mogelijk dat het percentage bezoekers naar één ervaring kan worden scheefgetrokken. Naarmate het verkeer toeneemt, zouden de percentages gelijker moeten worden.
