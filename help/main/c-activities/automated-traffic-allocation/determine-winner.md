---
keywords: automatische verkeerstoewijzing;gericht;winnaar;statistische garantie;vertrouwen;bepalen winnaar;hef;vertrouwen;gebrek;standaardwaarde;automatisch toewijzen;automatisch toewijzen
description: Leer hoe u de resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit in Adobe [!DNL Target] door belangrijke indicatoren te bestuderen , waaronder lift en vertrouwen .
title: Hoe interpreteer ik [!UICONTROL Auto-Allocate] Rapporten?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: e9976135c46f6658030b07fce384364f0c9ff0ed
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 0%

---

# Rapporten automatisch toewijzen interpreteren

De resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit [!UICONTROL Adobe Target] door belangrijke indicatoren te bestuderen , waaronder lift en vertrouwen .

Veel marketeers maken de fout om voortijdig een winnende ervaring te declareren voordat de resultaten de duidelijke winnaar aangeven. [!DNL Target] maakt het voor u gemakkelijker om de winnaar te bepalen.

Zie voor algemene informatie over het opgeven van een winnaar [Tien gemeenschappelijke A/B-testvalkuilen en hoe deze te vermijden](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## De winnende ervaring identificeren {#section_24007470CF5B4D30A06610CE8DD23CE3}

Wanneer u de opdracht [!UICONTROL Auto-Allocate] functie, [!DNL Target] toont een badge bij de bovenkant van de pagina van de activiteit erop wijst die &quot;Geen Winner nog&quot;tot de activiteit het minimumaantal omzettingen met voldoende vertrouwen bereikt.

![Geen Windows-badge](/help/main/c-activities/automated-traffic-allocation/assets/no-winner.png)

Wanneer een duidelijke winnaar wordt uitgeroepen, [!DNL Target] toont &quot;Winner: Experience *X*.&quot;

![winnende afbeelding](assets/winner.png)

>[!NOTE]
>
>De auto-Wijs activiteiten worden ontworpen om de beste ervaring onder alle opties te vinden en niet alleen om paarsgewijze vergelijkingen met controle te doen.

## Statistische garanties voor automatische toewijzing {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Aan het einde van een A/B-activiteit [!UICONTROL Auto-Allocate] garandeert dat de vastgestelde winnaar een effectief vals-positief percentage van 5% heeft. Dit betekent dat slechts 5% van de tijd de gekozen winnaar niet de beste ervaring is van alle ervaringen in de activiteit. Voor een [A/A-test](/help/main/c-activities/t-test-ab/aa-testing.md) (met identieke ervaringen), [!DNL Target] een test afsluit die minder dan 5 % van de tijd bedraagt. Het verwachte gedrag voor een A/A test (met identieke ervaringen) is dat het voor onbepaalde tijd loopt en zodat zou de winnaar badge nooit moeten verschijnen.

[!DNL Target] gebruikt geen op p-waarde gebaseerd vertrouwen voor [!UICONTROL Auto-Allocate].

De [!UICONTROL Confidence] kolom in een [!UICONTROL Auto-Allocate] activiteit (zie hieronder) toont de waarschijnlijkheid dat een ervaring de winnaar is binnen 1% foutenmarge. Het algoritme gebruikt een minimum waarneembaar effect van 1% tussen de beste en de op één na beste omzettingspercentages. Het algoritme gebruikt [Bernstein Inequality](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) om deze waarschijnlijkheid te berekenen.

Normale A/B-tests berekenen het vertrouwen op basis van p-waarden. [!UICONTROL Auto-Allocate] gebruikt geen p-waarden. P-waarden berekenen de waarschijnlijkheid dat een bepaalde ervaring verschilt van het besturingselement. Deze p-waarden kunnen slechts worden gebruikt om te bepalen of een ervaring van de controle zou kunnen verschillend zijn. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

>[!IMPORTANT]
>
>[!DNL Target] toont een winnaar na een vooraf bepaald minimumaantal omzettingen; de uiteindelijke beslissing om de winnaar te kiezen moet echter altijd op de resultaten van de [!DNL Adobe Target] Voorbeeldgroottecalculator. [!DNL Target] houdt geen rekening met de basisomrekeningskoersen van een locatie en andere belangrijke aspecten die in de rekenmachine worden verwerkt om de duur van de activiteit te bepalen. Dientengevolge, [!DNL Target] Een winnaar kan eerder dan gewarrantiseerd worden weergegeven op basis van een minimumaantal conversies. Zie voor meer informatie [Voorbeeldgroottecalculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6).

## Begrijp Lift en Vertrouwenrapportage in [!UICONTROL Auto-Allocate] activiteiten {#lift-confidence}

In [!UICONTROL Auto-Allocate] activiteiten, wordt de eerste ervaring (door gebrek genoemd Ervaring A) altijd gedefinieerd als &quot;Controle&quot;ervaring op [!UICONTROL Reports] tab. Deze ervaring wordt niet behandeld als een echte statistische controle in de modellering die wordt gebruikt om de prestaties van ervaringen te bepalen, maar wordt behandeld als een referentie of basislijn voor sommige cijfers in het rapport.

De numerieke waarde &quot;Lift&quot; en de 95%-grenzen voor elke ervaring worden altijd berekend op basis van de gedefinieerde ervaring &quot;Control&quot;. De gedefinieerde ervaring met &quot;Besturing&quot; kan geen lift hebben ten opzichte van zichzelf, zodat een lege waarde &quot;—&quot; wordt gerapporteerd voor deze ervaring. In tegenstelling tot A/B tests, in [!UICONTROL Auto-Allocate] tests, als een ervaring slechter presteert dan de bepaalde controle, wordt een negatieve waarde van de Lift niet gemeld; in plaats daarvan wordt &quot;—&quot; getoond.

De weergegeven [!UICONTROL Confidence Interval] staven geven het 95 %-betrouwbaarheidsinterval weer rond de gemiddelde schatting van de omrekeningskoers van een ervaring. Deze balken hebben ook een kleurcodering voor de gedefinieerde ervaring &quot;Besturing&quot;. De balk &quot;Besturingservaring&quot; is altijd grijs. De betrouwbaarheidsintervallen onder het betrouwbaarheidsinterval van de ervaring &quot;Besturing&quot; zijn rood van kleur en de betrouwbaarheidsintervallen boven de ervaring &quot;Besturing&quot; zijn groen van kleur.

Een winnaar wordt gevonden wanneer 95% van de toonaangevende ervaring [!UICONTROL Confidence Interval] overlapt niet met andere ervaringen. De winnende ervaring wordt aangeduid met een groene sterrenbadge links van de ervaringsnaam en in de banner &quot;Winner&quot;. Als er geen ster zichtbaar is, wordt op de banner &#39;&#39;Geen winnaar nog&#39;&#39; weergegeven en is er nog geen winnaar gevonden.

Er wordt ook een &quot;Vertrouwensnummer&quot; gerapporteerd naast de huidige leidende of winnende ervaring. Dit cijfer wordt alleen gerapporteerd tot de ervaring van de eerste [!UICONTROL Confidence] ten minste 60% bereikt. Als er twee ervaringen zijn in de [!UICONTROL Auto-Allocate] dit aantal is het betrouwbaarheidsniveau dat de ervaring beter presteert dan de andere ervaring. Als er meer dan twee ervaringen aanwezig zijn in de [!UICONTROL Auto-Allocate] Deze waarde geeft het betrouwbaarheidsniveau weer dat de ervaring beter presteert dan de gedefinieerde ervaring bij &quot;Besturing&quot;. Als de &quot;Controle&quot;ervaring het winnen is, wordt geen &quot;Vertrouwen&quot;cijfer gemeld.

## Veelgestelde vragen {#section_C8E068512A93458D8C006760B1C0B6A2}

Bekijk de volgende antwoorden op veelgestelde vragen:

### Het is een paar dagen in de activiteit geweest. Waarom zijn alle betrouwbaarheidswaarden nog steeds 0%?

Om een van de volgende redenen wordt beschreven waarom 0% wordt weergegeven in het rapport [!UICONTROL Confidence] kolom voor alle activiteiten:

* Handmatige A/B-tests en [!UICONTROL Auto-Allocate] verschillende statistieken gebruiken om weer te geven [!UICONTROL Confidence] waarden.

  Handmatige A/B-tests gebruiken p-waarden op basis van [T-test van Welch](https://en.wikipedia.org/wiki/Welch%27s_t-test). Een P-waarde is de waarschijnlijkheid om het waargenomen (of een meer extreme) verschil tussen een ervaring en de controle te vinden, aangezien er in werkelijkheid geen dergelijk verschil is. Deze P-waarden kunnen alleen worden gebruikt om te bepalen of waargenomen gegevens consistent zijn met een bepaalde ervaring en dat de controle hetzelfde is. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

  [!UICONTROL Auto-Allocate] toont de waarschijnlijkheid dat een bepaalde ervaring een echte winnaar zal zijn over alle ervaringen in de activiteit. Alleen een winnende ervaring (die waarschijnlijk de winnaar zal zijn) heeft een betrouwbaarheidswaarde die niet gelijk is aan nul. Alle andere zijn hoogstwaarschijnlijk verliezers en tonen 0%.

* [!UICONTROL Auto-Allocate] pas nadat de winnende ervaring 60 % vertrouwen heeft gewekt , begint men vertrouwen te tonen . Deze betrouwbaarheidsniveaus worden doorgaans weergegeven in ongeveer de helft van de tijd die een normale A/B-test nodig heeft om te voltooien (hoewel dit tijdsbestek niet is gegarandeerd). Om te bepalen hoe lang een normale A/B test zou lopen, gebruik [!DNL Adobe Target] [Voorbeeldgroottecalculator](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): conversiesnelheid van de plug-in &quot;Baseline conversion rate&quot;, &quot;5%&quot; voor &quot;Lift&quot; en 95% voor &quot;Trust&quot;. Doorgaans begint de betrouwbaarheid te worden aangetoond nadat elke ervaring ten minste 50% van de vereiste monsters per ervaring heeft genomen. Dit geeft je een idee van wanneer vertrouwen begint te verschijnen.

* Als het verslag over de hele linie 0% toont, is het waarschijnlijk te vroeg in de activiteit.

### Zijn de &quot;Geen Winner,&quot; &quot;Winner,&quot;en &quot;ster&quot;badges beschikbaar voor [!UICONTROL Auto-Allocate] activiteiten die [!UICONTROL Analytics as the reporting source] (A4T)?

De badges &quot;Geen Winner nog&quot; en &quot;Winner&quot; zijn momenteel niet beschikbaar in de [!UICONTROL A4T] deelvenster in [!DNL Analysis Workspace]. Deze badges zijn ook niet beschikbaar als hetzelfde rapport wordt weergegeven in [!DNL Target]. Een winnares-&quot;ster&quot;-badge weergegeven in een [!DNL Target] verslag [!UICONTROL Auto-Allocate] activiteit die A4T gebruikt zou moeten worden genegeerd.

Zie voor meer informatie over deze en andere beperkingen en opmerkingen [Automatisch toewijzen](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *A4T-ondersteuning voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten*.


