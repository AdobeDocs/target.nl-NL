---
keywords: Overview and Reference
description: Standaard worden bezoekersprofielen 14 dagen opgeslagen. Deze profiellevensduur kan worden verlengd.
title: Levensduur bezoekersprofiel
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Levensduur bezoekersprofiel{#visitor-profile-lifetime}

Een bezoekersprofiel verloopt standaard na 14 dagen inactiviteit voor die bezoeker. Deze profiellevensduur kan worden verlengd.

[Neem contact op met de klantenservice of uw Adobe-consultant](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om de levensduur van het profiel zonder extra kosten te verlengen. De levensduur kan worden ingesteld op wel 90 dagen.

De [!DNL Target] JavaScript-bibliotheek die u gebruikt ( [!DNL at.js] of [!DNL mbox.js]) bepaalt of u een nieuw bestand moet downloaden:

| Doelbibliotheek | Details |
|--- |--- |
| at.js | U hoeft geen nieuw bestand van het type at.js te downloaden als uw profiel de standaardwaarde overschrijdt. |
| mbox.js | Als uw profiel is uitgebreid tot na de standaardperiode van 14 dagen, moet u een nieuw bestand mbox.js downloaden nadat uw consultant of de klantenservice uw instellingen heeft gewijzigd. De cookieuitbreiding ter ondersteuning van de gewijzigde profiellevensduur is opgenomen in het bijgewerkte bestand mbox.js. Nadat u de nieuwe bibliotheek hebt gebruikt, worden de levensduur van uw bezoekersprofiel bijgewerkt. |

De vervaldatum wordt niet opnieuw ingesteld voor bestaande profielen. Als een vorige bezoeker 15 dagen niet terugkeert, verloopt dat profiel. Als een vorige bezoeker terugkeert vóór het originele twee-weekprofiel verloopt, wordt het profiel teruggesteld aan het uitgebreide leven. Alle nieuwe bezoekersprofielen worden ingesteld op de uitgebreide levensduur van het profiel.

In het volgende scenario, veronderstel dat één of beide plaatsen met mbox.js worden uitgevoerd, die een codeupdate vereist nadat het profiel wordt bijgewerkt. Als beide sites onder één clientcode vallen en een bezoeker beide sites bezoekt, wordt het profiel ingesteld op de levensduur van de profielen op de site die het laatst is bezocht. Als Site 1 bijvoorbeeld een 84-daagse profiellevensduur heeft en Site 2 een levensduur van 14 dagen heeft en de bezoeker Site 1 en Site 2 bezoekt, verloopt het profiel van die bezoeker over 14 dagen inactiviteit. Als de bezoeker Site 1 bezoekt na een bezoek aan Site 2, verloopt het profiel over 84 dagen inactiviteit.
