---
keywords: automated traffic allocation;targeting;winner;statistical guarantee;confidence;determine winner;lift;confidence;default;default experience
description: Bepaal een winnaar in een Auto-Wijs A/B activiteit door indicatoren in het Doel UI te bekijken.
title: Een winnaar bepalen
feature: null
topic: Standard
uuid: 0bcc11b2-44bd-450c-a504-a8ff7a4d72e6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 0%

---


# Rapporten automatisch toewijzen interpreteren {#determine-a-winner}

Interpreeer de resultaten van een auto-Wijs A/B activiteit door belangrijke indicatoren, met inbegrip van lift en vertrouwen, in het Doel UI te onderzoeken.

Veel marketeers maken de fout om voortijdig een winnende ervaring te declareren voordat de resultaten de duidelijke winnaar aangeven. We hebben het nu gemakkelijker voor je gemaakt om de winnaar te bepalen.

>[!NOTE]
>
>Zie [Tien gemeenschappelijke testvalkuilen voor A/B en hoe u deze](/help/c-activities/t-test-ab/common-ab-testing-pitfalls.md)kunt voorkomen voor algemene informatie over het aangeven van de winnaar.

## De winnende ervaring identificeren {#section_24007470CF5B4D30A06610CE8DD23CE3}

Wanneer het gebruiken van de [!UICONTROL Auto-Allocate] eigenschap, [!DNL Target] toont een badge bij de bovenkant van de pagina van de activiteit erop wijst die &quot;Geen Winner nog&quot;tot de activiteit het minimumaantal omzettingen met voldoende vertrouwen bereikt.

![Geen Windows-badge](/help/c-activities/automated-traffic-allocation/assets/no-winner.png)

Wanneer een duidelijke winnaar wordt gedeclareerd, wordt &quot;Winner: [!DNL Target] Beleef X.&quot;

![](assets/winner.png)

>[!NOTE]
>
>De auto-Wijs activiteiten worden ontworpen om de beste ervaring onder alle opties te vinden en niet alleen om paarsgewijze vergelijkingen met controle te doen.

## Statistische garanties voor automatische toewijzing {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Aan het einde van een A/B-activiteit garandeert Automatische toewijzing dat de bepaalde winnaar een effectief vals-positief percentage van 5% heeft. Dit betekent dat slechts 5% van de tijd de gekozen winnaar niet de beste ervaring is van alle ervaringen in de activiteit. Voor een A/A-test (met identieke ervaringen) sluiten we een test die minder dan 5% van de tijd bedraagt. Het verwachte gedrag voor een A/A test (met identieke ervaringen) is dat het voor onbepaalde tijd loopt en zodat zou de winnaar badge nooit moeten verschijnen.

We gebruiken geen op p-waarde gebaseerd vertrouwen voor Automatisch toewijzen.

In de kolom Vertrouwd in een activiteit voor automatisch toewijzen (zie hieronder) wordt de waarschijnlijkheid weergegeven dat een ervaring de winnaar is binnen een foutenmarge van 1% (het algoritme gebruikt dus een detecteerbaar effect van minimaal 1% tussen de beste en de op één na beste conversiekoers). Merk op dat het algoritme [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_(probability_theory)) gebruikt om deze waarschijnlijkheid te berekenen.

Normale A/B-tests berekenen het vertrouwen op basis van p-waarden. Automatisch toewijzen gebruikt geen p-waarden. P-waarden berekenen de waarschijnlijkheid dat een bepaalde ervaring verschilt van het besturingselement. Deze p-waarden kunnen slechts worden gebruikt om te bepalen of een ervaring van de controle zou kunnen verschillend zijn. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

>[!IMPORTANT]
>
>Doel toont een winnaar na een vooraf bepaald minimumaantal omzettingen; de uiteindelijke beslissing om de winnaar te kiezen moet echter altijd gebaseerd zijn op de resultaten van de Adobe Target- [voorbeeldgroottecalculator](https://docs.adobe.com/content/target-microsite/testcalculator.html). Het doel houdt geen rekening met de basisomrekeningskoersen van een site en andere belangrijke aspecten die in de calculator worden ingevoerd om de duur van de activiteit te bepalen. Als gevolg hiervan kan Target een winnaar eerder dan gerechtvaardigd weergeven op basis van een minimumaantal omzettingen. Zie [Voorbeeldgroottecalculator](/help/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)voor meer informatie.

## Informatie over de rapportage van optillen en vertrouwen bij activiteiten voor automatisch toewijzen {#lift-confidence}

Bij Auto-Wijs activiteiten, wordt de eerste ervaring (door gebrek genoemd Ervaring A) altijd gedefinieerd als &quot;Controle&quot;ervaring op het lusje van Rapporten. Deze ervaring wordt niet behandeld als een echte statistische controle in de modellering die wordt gebruikt om de prestaties van ervaringen te bepalen, maar wordt behandeld als een referentie of basislijn voor sommige cijfers in het rapport.

De numerieke waarde &quot;Lift&quot; en de 95%-grenzen voor elke ervaring worden altijd berekend op basis van de gedefinieerde ervaring &quot;Control&quot;. De gedefinieerde ervaring met &quot;Besturing&quot; kan geen lift hebben ten opzichte van zichzelf, zodat een lege waarde &quot;—&quot; wordt gerapporteerd voor deze ervaring. In tegenstelling tot bij A/B-tests wordt bij Auto-Allocate-tests, als een ervaring slechter is dan de gedefinieerde controle, geen negatieve Liftwaarde gerapporteerd. in plaats daarvan wordt &quot;—&quot; weergegeven.

De getoonde bars van het Interval van het Vertrouwen vertegenwoordigen het 95% betrouwbaarheidsinterval rond de gemiddelde schatting van de de omzettingssnelheid van een ervaring. Deze zijn ook van kleur-gecodeerd met betrekking tot de bepaalde ervaring van de &quot;Controle&quot;. De balk &quot;Besturingservaring&quot; is altijd grijs. De betrouwbaarheidsintervallen onder het betrouwbaarheidsinterval &quot;Besturing&quot; zijn rood van kleur en de betrouwbaarheidsintervallen boven de ervaring &quot;Besturing&quot; zijn groen van kleur.

Een winnaar wordt gevonden wanneer het 95%-betrouwbaarheidsinterval van de toonaangevende ervaring niet overlapt met andere ervaringen. De winnende ervaring wordt aangeduid met een groene sterrenbadge links van de ervaringsnaam en in de banner &quot;Winner&quot;. Als er geen ster zichtbaar is, wordt op de banner &#39;&#39;Geen winnaar nog&#39;&#39; weergegeven en is er nog geen winnaar gevonden.

Er wordt ook een &quot;Vertrouwensnummer&quot; gerapporteerd naast de huidige leidende of winnende ervaring. Dit cijfer wordt slechts gerapporteerd tot het Vertrouwen van de leidende ervaring minstens 60% bereikt. Als er precies twee ervaringen aanwezig zijn in het Automatisch toewijzen-experiment, geeft dit getal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de andere ervaring. Als er meer dan twee ervaringen aanwezig zijn in het experiment voor automatisch toewijzen, geeft dit getal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de gedefinieerde ervaring voor besturing. Als de &quot;Controle&quot;ervaring het winnen is, wordt geen &quot;Vertrouwen&quot;cijfer gemeld.

## Veelgestelde vragen {#section_C8E068512A93458D8C006760B1C0B6A2}

**Het is een paar dagen in de activiteit geweest. Waarom zijn alle betrouwbaarheidswaarden nog steeds 0%?**

Om het even welke volgende redenen beschrijven waarom 0% in de [!UICONTROL Confidence] kolom van het rapport voor alle activiteiten toont:

* Handmatige A/B-tests en Automatisch toewijzen gebruiken verschillende statistieken om betrouwbaarheidswaarden weer te geven.

   Handmatige A/B-tests gebruiken p-waarden op basis van de t-test [van de](https://en.wikipedia.org/wiki/Student%27s_t-test)student. Een P-waarde is de waarschijnlijkheid om het waargenomen (of een meer extreme) verschil tussen een ervaring en de controle te vinden, aangezien er in werkelijkheid geen dergelijk verschil is. Deze P-waarden kunnen alleen worden gebruikt om te bepalen of waargenomen gegevens consistent zijn met een bepaalde ervaring en dat de controle hetzelfde is. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

   Automatisch toewijzen toont de waarschijnlijkheid dat een bepaalde ervaring een echte winnaar is in alle ervaringen in de activiteit. Dit betekent dat alleen een winnende ervaring (die waarschijnlijk de winnaar zal zijn) een betrouwbaarheidswaarde heeft die niet gelijk is aan nul. Alle anderen zullen waarschijnlijk verliezers zijn en 0%.

* Automatisch toewijzen begint pas vertrouwen te tonen nadat de winnende ervaring een betrouwbaarheid van 60% heeft opgeleverd. Deze betrouwbaarheidsniveaus worden doorgaans weergegeven in ongeveer de helft van de tijd die een normale A/B-test nodig heeft om te voltooien (hoewel dit niet gegarandeerd is). Om te bepalen hoe lang een normale A/B test zou lopen, gelieve een calculator [van de](https://docs.adobe.com/content/target-microsite/testcalculator.html)steekproefgrootte te gebruiken: de conversiesnelheid van de plug-in &#39;Baseline conversion rate&#39;, &#39;5%&#39; voor &#39;Lift&#39; en &#39;95% voor &#39;Trust&#39;. Doorgaans begint de betrouwbaarheid te worden aangetoond nadat elke ervaring ten minste 50% van de vereiste monsters per ervaring heeft genomen. Dit geeft u een idee wanneer er vertrouwen begint te ontstaan.
* Als het verslag over de hele linie 0% toont, is het waarschijnlijk te vroeg in de activiteit.

