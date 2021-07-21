---
keywords: Overzicht en referentie
description: Meer informatie over wanneer een bezoekersprofiel in  [!DNL Adobe Target] verloopt.
title: Wat is de levensduur van het bezoekersprofiel en kan ik deze verlengen?
feature: Soorten publiek
exl-id: 70cb5e3b-ed6d-450d-8c6e-f1bfe8d26e54
source-git-commit: c19163020cdcb41a17ea6b65b5b500fadc9c7512
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Levensduur bezoekersprofiel

Een bezoekersprofiel in [!DNL Adobe Target] vervalt standaard na 14 dagen inactiviteit voor die bezoeker. Deze profiellevensduur kan worden verlengd.

[Neem contact op met de klantenservice of uw ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) consultant van de Adobe om de levensduur van het profiel zonder extra kosten te verlengen. De levensduur kan worden ingesteld op wel 90 dagen.

U hoeft geen nieuw [!DNL Platform Web SDK]- of at.js-bestand te downloaden als uw profiel de standaardwaarden overschrijdt.

De vervaldatum wordt niet opnieuw ingesteld voor bestaande profielen. Als een vorige bezoeker 15 dagen niet terugkeert, verloopt dat profiel. Als een vorige bezoeker terugkeert vóór het originele twee-weekprofiel verloopt, wordt het profiel teruggesteld aan het uitgebreide leven. Alle nieuwe bezoekersprofielen worden ingesteld op de uitgebreide levensduur van het profiel.

In het volgende scenario, veronderstel dat één of beide plaatsen met [!DNL Platform Web SDK] worden uitgevoerd. Als beide sites onder één clientcode vallen en een bezoeker beide sites bezoekt, wordt het profiel ingesteld op de levensduur van de profielen op de site die het laatst is bezocht. Stel bijvoorbeeld dat Site 1 een levensduur van 84 dagen heeft. Site 2 heeft een levensduur van 14 dagen. Als de bezoeker Site 1 en Site 2 bezoekt, vervalt het profiel van die bezoeker in 14 dagen van inactiviteit. Als de bezoeker Site 1 bezoekt na een bezoek aan Site 2, verloopt het profiel over 84 dagen inactiviteit.
