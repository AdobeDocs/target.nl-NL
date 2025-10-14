---
keywords: automatische verkeerstoewijzing;gericht;winnaar;statistische garantie;vertrouwen;bepalen winnaar;hef;vertrouwen;gebrek;standaardwaarde;automatisch toewijzen;automatisch toewijzen
description: Leer hoe te om de resultaten van een [!UICONTROL Auto-Allocate] activiteit A/B in Adobe  [!DNL Target]  te interpreteren door belangrijke indicatoren, met inbegrip van lift en vertrouwen te onderzoeken.
title: Hoe interpreteer ik [!UICONTROL Auto-Allocate] -rapporten?
feature: Auto-Allocate
exl-id: 4ed00eee-8939-4958-9be6-b45a8c08afbc
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Rapporten automatisch toewijzen interpreteren

Interpreteer de resultaten van een [!UICONTROL Auto-Allocate] A/B-activiteit in [!UICONTROL Adobe Target] door belangrijke indicatoren, zoals lift en vertrouwen, te onderzoeken.

Veel marketeers maken de fout om voortijdig een winnende ervaring te declareren voordat de resultaten de duidelijke winnaar aangeven. Met [!DNL Target] kunt u gemakkelijker bepalen wie de winnaar is.

Voor algemene informatie over het verklaren van een winnaar, zie [&#x200B; gemeenschappelijke A/B testende valkuilen en hoe te om hen te vermijden &#x200B;](/help/main/c-activities/t-test-ab/common-ab-testing-pitfalls.md).

## De winnende ervaring identificeren {#section_24007470CF5B4D30A06610CE8DD23CE3}

Wanneer u de functie [!UICONTROL Auto-Allocate] gebruikt, geeft [!DNL Target] boven aan de pagina van de activiteit een symbool weer dat &#39;Geen winnaar nog&#39; aangeeft, totdat de activiteit het minimale aantal conversies met voldoende vertrouwen bereikt.

![&#x200B; Geen badge van de Winner &#x200B;](/help/main/c-activities/automated-traffic-allocation/assets/no-winner.png)

Wanneer een duidelijke winnaar wordt verklaard, [!DNL Target] vertoningen &quot;Winner: Ervaring *X*.&quot;

![&#x200B; winnaar beeld &#x200B;](assets/winner.png)

>[!NOTE]
>
>De auto-Wijs activiteiten worden ontworpen om de beste ervaring onder alle opties te vinden en niet alleen om paarsgewijze vergelijkingen met controle te doen.

## Statistische garanties voor automatische toewijzing {#section_7AF3B93E90BA4B80BC9FC4783B6A389C}

Aan het einde van een A/B-activiteit garandeert [!UICONTROL Auto-Allocate] dat de bepaalde winnaar een effectief fout-positief percentage van 5% heeft. Dit betekent dat slechts 5% van de tijd de gekozen winnaar niet de beste ervaring is van alle ervaringen in de activiteit. Voor een [&#x200B; test A/A &#x200B;](/help/main/c-activities/t-test-ab/aa-testing.md) (met identieke ervaringen), [!DNL Target] concludeert een test minder dan 5% van de tijd. Het verwachte gedrag voor een A/A test (met identieke ervaringen) is dat het voor onbepaalde tijd loopt en zodat zou de winnaar badge nooit moeten verschijnen.

[!DNL Target] gebruikt geen op p-waarde gebaseerde betrouwbaarheid voor [!UICONTROL Auto-Allocate] .

De kolom [!UICONTROL Confidence] in een [!UICONTROL Auto-Allocate] -activiteit (zie hieronder) geeft de kans weer dat een ervaring de winnaar wordt binnen de foutmarge van 1%. Het algoritme gebruikt een minimum waarneembaar effect van 1% tussen de beste en de op één na beste omzettingspercentages. Het algoritme gebruikt [&#x200B; ongelijkheid van Bernstein &#x200B;](https://en.wikipedia.org/wiki/Bernstein_inequalities_%28probability_theory%29) om deze waarschijnlijkheid gegevens te verwerken.

Normale A/B-tests berekenen het vertrouwen op basis van p-waarden. [!UICONTROL Auto-Allocate] gebruikt geen p-waarden. P-waarden berekenen de waarschijnlijkheid dat een bepaalde ervaring verschilt van het besturingselement. Deze p-waarden kunnen slechts worden gebruikt om te bepalen of een ervaring van de controle zou kunnen verschillend zijn. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

>[!IMPORTANT]
>
>In [!DNL Target] wordt een winnaar weergegeven na een vooraf gedefinieerd minimumaantal conversies. De uiteindelijke beslissing om de winnaar te kiezen, moet echter altijd gebaseerd zijn op de resultaten van de [!DNL Adobe Target] samplegroottecalculator. [!DNL Target] houdt geen rekening met de basisconversiekoersen van een site en andere belangrijke aspecten die in de calculator worden gebruikt om de duur van de activiteit te bepalen. Als gevolg hiervan kan [!DNL Target] een winnaar eerder weergeven dan op basis van een minimumaantal conversies gerechtvaardigd is. Voor meer informatie, zie {de calculator van de Grootte van 0} Steekproef [.](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6)

## De rapportage van optillen en vertrouwen in [!UICONTROL Auto-Allocate] -activiteiten begrijpen {#lift-confidence}

Bij [!UICONTROL Auto-Allocate] -activiteiten wordt de eerste ervaring (standaard Ervaring A genoemd) altijd gedefinieerd als een &#39;Controle&#39;-ervaring op het tabblad [!UICONTROL Reports] . Deze ervaring wordt niet behandeld als een echte statistische controle in de modellering die wordt gebruikt om de prestaties van ervaringen te bepalen, maar wordt behandeld als een referentie of basislijn voor sommige cijfers in het rapport.

De numerieke waarde &quot;Lift&quot; en de 95%-grenzen voor elke ervaring worden altijd berekend op basis van de gedefinieerde ervaring &quot;Control&quot;. De gedefinieerde ervaring met &quot;Besturing&quot; kan geen lift hebben ten opzichte van zichzelf, zodat een lege waarde &quot;—&quot; wordt gerapporteerd voor deze ervaring. In tegenstelling tot bij A/B tests, wordt bij [!UICONTROL Auto-Allocate] tests, als een ervaring slechter dan de bepaalde controle uitvoert, een negatieve waarde van de Lift niet gemeld; in plaats daarvan wordt &quot;—&quot; getoond.

De weergegeven [!UICONTROL Confidence Interval] balken geven het 95%-betrouwbaarheidsinterval weer rond de gemiddelde schatting van de conversiesnelheid van een ervaring. Deze balken hebben ook een kleurcodering voor de gedefinieerde ervaring &quot;Besturing&quot;. De balk &quot;Besturingservaring&quot; is altijd grijs. De betrouwbaarheidsintervallen onder het betrouwbaarheidsinterval van de ervaring &quot;Besturing&quot; zijn rood van kleur en de betrouwbaarheidsintervallen boven de ervaring &quot;Besturing&quot; zijn groen van kleur.

Er wordt een winnaar gevonden wanneer de 95% [!UICONTROL Confidence Interval] van de toonaangevende ervaring niet overlapt met andere ervaringen. De winnende ervaring wordt aangeduid met een groene sterrenbadge links van de ervaringsnaam en in de banner &quot;Winner&quot;. Als er geen ster zichtbaar is, wordt op de banner &#39;&#39;Geen winnaar nog&#39;&#39; weergegeven en is er nog geen winnaar gevonden.

Er wordt ook een &quot;Vertrouwensnummer&quot; gerapporteerd naast de huidige leidende of winnende ervaring. Dit cijfer wordt alleen gerapporteerd als de [!UICONTROL Confidence] -ervaring van de regelaar ten minste 60% bereikt. Als de [!UICONTROL Auto-Allocate] -activiteit twee ervaringen bevat, geeft dit getal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de andere. Als de [!UICONTROL Auto-Allocate] -activiteit meer dan twee ervaringen bevat, geeft dit getal het betrouwbaarheidsniveau aan dat de ervaring beter presteert dan de gedefinieerde &#39;Ctrl&#39;-ervaring. Als de &quot;Controle&quot;ervaring het winnen is, wordt geen &quot;Vertrouwen&quot;cijfer gemeld.

## Veelgestelde vragen {#section_C8E068512A93458D8C006760B1C0B6A2}

Bekijk de volgende antwoorden op veelgestelde vragen:

### Het is een paar dagen in de activiteit geweest. Waarom zijn alle betrouwbaarheidswaarden nog steeds 0%?

Om een van de volgende redenen wordt beschreven waarom 0% wordt weergegeven in de kolom [!UICONTROL Confidence] van het rapport voor alle activiteiten:

* Handmatige A/B-tests en [!UICONTROL Auto-Allocate] gebruiken verschillende statistieken om [!UICONTROL Confidence] -waarden weer te geven.

  De handmatige A/B tests gebruiken p-waarden die op [&#x200B; worden gebaseerd t-test van het Welch &#x200B;](https://en.wikipedia.org/wiki/Welch%27s_t-test). Een P-waarde is de waarschijnlijkheid om het waargenomen (of een meer extreme) verschil tussen een ervaring en de controle te vinden, aangezien er in werkelijkheid geen dergelijk verschil is. Deze P-waarden kunnen alleen worden gebruikt om te bepalen of waargenomen gegevens consistent zijn met een bepaalde ervaring en dat de controle hetzelfde is. Deze waarden kunnen niet worden gebruikt om te bepalen als een ervaring van een andere ervaring (niet controle) verschillend is.

  [!UICONTROL Auto-Allocate] toont de waarschijnlijkheid dat een bepaalde ervaring een ware winnaar is over alle ervaringen in de activiteit. Alleen een winnende ervaring (die waarschijnlijk de winnaar zal zijn) heeft een betrouwbaarheidswaarde die niet gelijk is aan nul. Alle andere zijn hoogstwaarschijnlijk verliezers en tonen 0%.

* [!UICONTROL Auto-Allocate] begint pas vertrouwen te tonen nadat de winnende ervaring een betrouwbaarheid van 60% heeft verzameld. Deze betrouwbaarheidsniveaus worden doorgaans weergegeven in ongeveer de helft van de tijd die een normale A/B-test nodig heeft om te voltooien (hoewel dit tijdsbestek niet is gegarandeerd). Om te bepalen hoe lang een normale A/B test zou lopen, gebruik de [!DNL Adobe Target] [&#x200B; calculator van de Grootte van de Steekproef &#x200B;](/help/main/c-activities/t-test-ab/sample-size-determination.md#section_6B8725BD704C4AFE939EF2A6B6E834E6): de conversie-tarief van de stop controle in &quot;de omzettingssnelheid van de Basislijn,&quot;5%&quot;voor &quot;Lift,&quot;en 95% voor &quot;Vertrouwen.&quot; Doorgaans begint de betrouwbaarheid te worden aangetoond nadat elke ervaring ten minste 50% van de vereiste monsters per ervaring heeft genomen. Dit geeft je een idee van wanneer vertrouwen begint te verschijnen.

* Als het verslag over de hele linie 0% toont, is het waarschijnlijk te vroeg in de activiteit.

### Zijn de badges &quot;No Winner&quot;, &quot;Winner&quot; en &quot;star&quot; beschikbaar voor [!UICONTROL Auto-Allocate] -activiteiten die [!UICONTROL Analytics as the reporting source] (A4T) gebruiken?

De badges &quot;Geen winnaar nog&quot; en &quot;Winner&quot; zijn momenteel niet beschikbaar in het deelvenster [!UICONTROL A4T] in [!DNL Analysis Workspace] . Deze badges zijn ook niet beschikbaar als hetzelfde rapport wordt weergegeven in [!DNL Target] . Een winnares-&quot;star&quot;-badge in een [!DNL Target] -rapport voor een [!UICONTROL Auto-Allocate] -activiteit met A4T moet worden genegeerd.

Voor meer informatie over dit en andere beperkingen en nota&#39;s, zie [&#x200B; auto-Wijs &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#aa) in *steun A4T voor [!UICONTROL Auto-Allocate] en [!UICONTROL Auto-Target] activiteiten* toe.


