---
keywords: aanbevelingen;veelgestelde vragen;faq
description: Veelgestelde vragen (FAQs) en hun antwoorden over  [!DNL Target Recommendations]  ontwerpen.
title: Waar kan ik Antwoorden aan de Vragen van het Ontwerp voor  [!DNL Target Recommendations] krijgen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: e970f734-9bc7-43b8-af1b-75e527d6353c
source-git-commit: eba9e0b02ce74fea127d2cb2d08d04dcd2da2d76
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Veelgestelde vragen over ontwerp

Lijst met veelgestelde vragen (FAQ&#39;s) over [!DNL Adobe Target] [!DNL Recommendations] -ontwerpen.

## De prijs van mijn aanbevolen object geeft beide waarden niet rechts van het decimaalteken weer. Hoe kan ik ze weergeven?

Standaard geven numerieke waarden (zoals `entity.value` ) die in ontwerpsjablonen worden geretourneerd, geen volgnullen na het decimaalteken weer. Als een item bijvoorbeeld $35.00 is, is `entity.value` gelijk aan 35 en wordt alleen 35 weergegeven op de pagina, niet $35.00.

Er zijn twee opties beschikbaar om dit probleem op te lossen:

* Met het script Velocity of JavaScript kunt u opmaak toepassen op de geretourneerde waarde.

* U kunt de prijs van het item doorgeven in twee aparte entiteitskenmerken. Het eerste, `entity.value` , kan worden gebruikt voor numerieke vergelijkingen (zoals regels voor prijsvergelijking). Het tweede kenmerk moet een aangepast kenmerk zijn, zoals `entity.displayValue` , dat de waarde van de entiteit opslaat als een tekenreeks om een correcte rendering mogelijk te maken.

  Bijvoorbeeld:

  `"entity.value" : 35.00, "entity.displayValue" : "$35.00"`

## Waarom wordt categorie niet weergegeven in het ontwerp? Ik gebruik `$entity1.categoryId` . {#section_073309B8051049C7953D396A93EA0713}

Categorie-id kan niet worden weergegeven in het ontwerp. Omdat meerdere categorieën kunnen worden opgeslagen, weet het systeem niet welke categorie moet worden weergegeven.

## Hoe moet ik een ontwerp wijzigen om een directe update te krijgen? {#section_28EE35A5B10B47ECA4A332F0E5B2598F}

Het bijwerken van het ontwerp dat momenteel in gebruik is, duurt enige tijd. Als u het ontwerp direct wilt wijzigen, maakt u een nieuw ontwerp, selecteert u het in de activiteit en slaat u de aanbeveling op.

## Hoe kan ik zeer belangrijke informatie voor vertoning in het ontwerp vangen? Voorbeeld: Als we de categorie van het sleutelproduct willen weergeven, hoe zou ik die waarde dan in het snelheidsontwerp coderen? {#section_F08043B14BA24BC8815FEF25F4F84C39}

De `$key. *` waarde `*` parameter vangt de meeste informatie van het zeer belangrijke product aan vertoning binnen het ontwerp. Als u bijvoorbeeld de miniatuur van het sleutelproduct wilt weergeven, gebruikt u `$key.thumbnailURL` .

## Welke versie van Snelheid wordt gebruikt? {#section_28F00E15A4A54A768782A3F5BB0CDB21}

Versie 1.7 zonder extra hulpmiddelen of toegevoegde bibliotheken. De basisfunctionaliteit van de Snelheid is beschikbaar.

## Hoe vervang ik een bestaande entiteitwaarde door een lege waarde? De waarde `entity.message` van een object moet bijvoorbeeld worden gewist wanneer een aanbieding afloopt. {#section_B88F2C2925DC4508974B2F8B13F961CB}

Verzenden in een vaste JavaScript-ruimte lijkt dit te doen. Laat de ontwikkelaars `\u00A0` als waarde verzenden. Voorbeeld: `entity.message=\u00A0` . U zou kunnen overwegen dat de standaardwaarde is wanneer geen waarde in plaats van ongeldig aanwezig is.

## Kan ik een profielscript gebruiken in een [!DNL Recommendations] -ontwerp? {#section_6BD55203984A4D80A0C6F241AD7806DF}

Ja. Als u een profielscript wilt gebruiken in een [!DNL Recommendations] -ontwerp, plaatst u de naam in `\${...}` . Als uw profielscript bijvoorbeeld de naam `user.basket` heeft, verwijst u het als `\${user.basket}` in het ontwerp. Merk op dat backslash impliceert dat het profielmanuscript niet door Snelheid wordt teruggegeven. Daarom kunt u geen verrichtingen op het profielmanuscript in een malplaatje van de Snelheid uitvoeren. De waarde wordt rechtstreeks op de pagina afgedrukt.
