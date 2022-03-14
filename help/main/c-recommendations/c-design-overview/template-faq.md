---
keywords: aanbevelingen;veelgestelde vragen;faq
description: Bekijk een lijst met veelgestelde vragen (FAQ's) en hun antwoorden op Adobe [!DNL Target] Recommendations-ontwerpen.
title: Waar kan ik antwoorden om vragen te ontwerpen voor [!DNL Target] Recommendations?
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Veelgestelde vragen over ontwerp

Lijst met veelgestelde vragen (FAQ&#39;s) over [!DNL Adobe Target] [!DNL Recommendations] ontwerpen.

## De prijs van mijn aanbevolen object geeft beide waarden niet rechts van het decimaalteken weer. Hoe kan ik ze weergeven?

Numerieke waarden (zoals `entity.value`) geretourneerd in ontwerpsjablonen, worden na het decimaalteken geen volgnullen weergegeven. Als een item bijvoorbeeld $35.00 is, `entity.value` is gelijk aan 35 en slechts 35 wordt weergegeven op de pagina, niet $35.00.

Er zijn twee opties beschikbaar om dit probleem op te lossen:

* Met het script Velocity of JavaScript kunt u opmaak toepassen op de geretourneerde waarde.

* U kunt de prijs van het item doorgeven in twee aparte entiteitskenmerken. De eerste, `entity.value`, kan worden gebruikt voor numerieke vergelijkingen (zoals regels voor prijsvergelijking). De tweede waarde moet een aangepast kenmerk zijn, zoals `entity.displayValue` dat de waarde van de entiteit opslaat als een tekenreeks die een correcte rendering mogelijk maakt.

   Bijvoorbeeld:

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Waarom wordt categorie niet weergegeven in het ontwerp? Ik gebruik `$entity1.categoryId`. {#section_073309B8051049C7953D396A93EA0713}

Categorie-id kan niet worden weergegeven in het ontwerp. Omdat de veelvoudige categorieën kunnen worden opgeslagen, zou het systeem niet weten welke categorie aan vertoning.

## Hoe moet ik een ontwerp wijzigen om een directe update te krijgen? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Het bijwerken van het ontwerp dat momenteel in gebruik is, duurt enige tijd. Als u het ontwerp direct wilt wijzigen, maakt u een nieuw ontwerp, selecteert u het in de activiteit en slaat u de aanbeveling op.

## Hoe kan ik zeer belangrijke informatie voor vertoning in het ontwerp vangen? Voorbeeld: Hoe kan ik die waarde coderen in het snelheidsontwerp als we de categorie van het sleutelproduct willen weergeven? {#section_F08043B14BA24BC8815FEF25F4F84C39}

De `$key. *`value`*` parameter legt de meeste informatie van het sleutelproduct vast die binnen het ontwerp moet worden weergegeven. Voorbeeld: Als u de miniatuur van het sleutelproduct wilt weergeven, gebruikt u `$key.thumbnailURL`.

## Welke versie van Snelheid wordt gebruikt? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Versie 1.7 zonder extra hulpmiddelen of toegevoegde bibliotheken. De basisfunctionaliteit van de Snelheid is beschikbaar.

## Hoe vervang ik een bestaande entiteitwaarde door een lege waarde? Bijvoorbeeld, moet het entiteitsbericht van een punt worden ontruimd wanneer een bevordering beëindigt. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Dit lijkt te gebeuren door verzending in een vaste JavaScript-ruimte. Laat de ontwikkelaars inzenden `\u00A0` als de waarde. Voorbeeld: `entity.message=\u00A0`. U zou kunnen overwegen dat de standaardwaarde is wanneer geen waarde in plaats van ongeldig aanwezig is.

## Kan ik een profielscript gebruiken in een [!DNL Recommendations] ontwerp? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Ja. Een profielscript gebruiken in een [!DNL Recommendations] ontwerp, naam insluiten `\${...}`. Als uw profielscript bijvoorbeeld een naam heeft `user.basket`, doorverwijzen naar `\${user.basket}` in het ontwerp. Merk op dat backslash impliceert dat het profielmanuscript niet door Snelheid wordt teruggegeven. Daarom kunt u geen verrichtingen op het profielmanuscript in een malplaatje van de Snelheid uitvoeren. De waarde wordt rechtstreeks op de pagina afgedrukt.
