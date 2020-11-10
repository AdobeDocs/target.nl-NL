---
keywords: recommendations;frequently asked questions;faq
description: Lijst met veelgestelde vragen (FAQ's) over ontwerpen met Adobe Target-aanbevelingen.
title: Veelgestelde vragen over ontwerp
feature: designs
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---


# ![Veelgestelde vragen over PREMIUM](/help/assets/premium.png) -ontwerp {#design-faq}

Lijst met veelgestelde vragen (FAQ&#39;s) over [!DNL Adobe Target] aanbevolen ontwerpen.

## De prijs van mijn aanbevolen object geeft beide waarden niet rechts van het decimaalteken weer. Hoe kan ik ze weergeven?

Standaard geven numerieke waarden (zoals `entity.value`) die in ontwerpsjablonen worden geretourneerd, geen volgnullen na het decimaalteken weer. Als een item bijvoorbeeld $35.00 is, `entity.value` is gelijk aan 35 en wordt slechts 35 weergegeven op de pagina, niet $35.00.

Er zijn twee opties beschikbaar om dit probleem op te lossen:

* Met het script Velocity of JavaScript kunt u opmaak toepassen op de geretourneerde waarde.

* U kunt de prijs van het item doorgeven in twee aparte entiteitskenmerken. Het eerste, `entity.value`, kan voor numerieke vergelijkingen (zoals prijsvergelijkingsregels) worden gebruikt. De tweede moet een aangepast kenmerk zijn, bijvoorbeeld `entity.displayValue` dat de waarde van de entiteit opslaat als een tekenreeks om een correcte rendering mogelijk te maken.

   Bijvoorbeeld:

   `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Waarom wordt categorie niet weergegeven in het ontwerp? Ik gebruik $entiteit1.categoryId. {#section_073309B8051049C7953D396A93EA0713}

Categorie-id kan niet worden weergegeven in het ontwerp. Omdat de veelvoudige categorieën kunnen worden opgeslagen, zou het systeem niet weten welke categorie aan vertoning.

## Hoe moet ik een ontwerp wijzigen om een directe update te krijgen? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Het bijwerken van het ontwerp dat momenteel in gebruik is, duurt enige tijd. Als u het ontwerp direct wilt wijzigen, maakt u een nieuw ontwerp, selecteert u het in de activiteit en slaat u de aanbeveling op.

## Hoe kan ik zeer belangrijke informatie voor vertoning in het ontwerp vangen? Voorbeeld: Hoe kan ik die waarde coderen in het snelheidsontwerp als we de categorie van het sleutelproduct willen weergeven? {#section_F08043B14BA24BC8815FEF25F4F84C39}

De parameter `$key. *`value`*` legt de meeste informatie van het sleutelproduct vast die binnen het ontwerp moet worden weergegeven. Voorbeeld: Als u de miniatuur van het sleutelproduct wilt weergeven, gebruikt u `$key.thumbnailURL`.

## Welke versie van Snelheid wordt gebruikt? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Versie 1.7 zonder extra hulpmiddelen of toegevoegde bibliotheken. De basisfunctionaliteit van de Snelheid is beschikbaar.

## Hoe vervang ik een bestaande entiteitwaarde door een lege waarde? Bijvoorbeeld, moet het entiteitsbericht van een punt worden ontruimd wanneer een bevordering beëindigt. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Dit lijkt te gebeuren door verzending in een vaste JavaScript-ruimte. Laat de ontwikkelaars inzenden `\u00A0` als waarde. Voorbeeld: `entity.message=\u00A0`. U zou kunnen overwegen dat de standaardwaarde is wanneer geen waarde in plaats van ongeldig aanwezig is.

## Kan ik een profielscript gebruiken in een Recommendations-ontwerp? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Ja. U moet echter een backslash (\) toevoegen vóór de $ in de naam van het profielscript.
