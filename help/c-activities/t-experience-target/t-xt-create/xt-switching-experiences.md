---
keywords: prioriteit;ervaring maken;prioriteit;ervaring;publiek;ervaring;schakelen tussen ervaringen;visuele ervaringscomposer
description: Leer hoe bezoekers kunnen schakelen tussen ervaringen in een Adobe Target Experience Targeting-activiteit (XT) terwijl hun profielen evolueren.
title: Kunnen bezoekers van ervaring in een ervaring veranderen richtend activiteit?
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---


# Overschakelen van ervaringen op het gebied van ervaring

Informatie over hoe bezoekers kunnen schakelen tussen ervaringen in een Experience Targeting (XT)-activiteit terwijl hun profielen evolueren.

>[!NOTE]
>
>**21 september 2017**
>
>Met de release op 21 september 2017 heeft Target de manier gewijzigd waarop gebruikers worden geplaatst in Experience Targeting (XT)-activiteiten (Landing Page Campagnes in Target Classic). Voor alle nieuwe en bestaande activiteiten moeten de gebruikers de ervaring in acht nemen die op regels gericht op elke indruk is om de inhoud van de ervaring te blijven zien en in rapporten te worden geteld. Eerder, als de gebruiker niet meer gekwalificeerd voor om het even welke ervaring was, zou de gebruiker de inhoud van blijven zien en in rapporten voor, de laatste ervaring worden geteld die zij kwalificeerden.
>
>Deze wijziging vond automatisch plaats als onderdeel van de release voor alle bestaande activiteiten en voor nieuwe activiteiten die na de release werden gemaakt. Als de vorige methode (van vóór 21 september) gewenst is, kunt u publiek tot stand brengen gebruikend profielmanuscripten zodat een gebruiker slechts aan een voorwaarde moet voldoen één keer om in dat publiek in de toekomst te blijven vallen. Gebruik vervolgens die soorten publiek voor elke ervaring in de activiteit.

Met Experience Targeting kunt u bepalen welke bezoekers zien hoe hun profielen evolueren. De volgende lijst bevat slechts een paar scenario&#39;s waarin bezoekersprofielen kunnen evolueren en u verschillende inhoud wilt voorstellen:

| Scenario | Details |
|--- |--- |
| Geografische locatie | bezoekers kunnen uw website of mobiele app vanuit verschillende geografische locaties bekijken terwijl ze voor zakelijke doeleinden of plezier reizen. |
| Klantstatus | Bezoekers kunnen als een vooruitzicht worden beschouwd voordat ze een account maken of een product kopen. |
| Categorie-affiniteit | Met de functie [Categorie affiniteit](/help/c-target/c-visitor-profile/category-affinity.md) in Target worden automatisch de categorieën vastgelegd die gebruikers bezoeken en wordt vervolgens de affiniteit van de gebruikers voor de categorie voor doeldoeleinden berekend. bezoekers die bijvoorbeeld verschillende artikelen over een bepaald onderwerp op uw website hebben weergegeven, kunnen inhoud over dat onderwerp krijgen. |
| Weekdag | Wanneer het weekend nadert, wilt u bezoekers wellicht inhoud laten zien over films, dineren of andere vormen van entertainment. |

Om deze mogelijkheden in [!DNL Target] te gebruiken, is het belangrijk om de volgende informatie te begrijpen aangezien u met XT activiteiten werkt:

* **De prioriteit wordt bepaald door de volgorde van de ervaringen, van boven naar beneden.** Als een bezoeker voor meer dan twee soorten publiek in aanmerking komt, ontvangt hij of zij inhoud uit de ervaring met hogere prioriteit.
* **Bezoekers schakelen tussen de ervaringen in een XT-activiteit als ze zich gaan kwalificeren voor een hogere prioriteit.**

   In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat deze bezoeker uw website vanuit Duitsland had bekeken, schakelde hij over op Experience B (bezoekers uit Duitsland).

   ![Priority US > Germany](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Bezoekers wisselen ook tussen ervaringen als ze niet langer voor hun huidige publiek in aanmerking komen, maar voor een ervaring met lagere prioriteit.**
* **Als bezoekers niet langer in aanmerking komen voor hun huidige ervaring en niet langer in aanmerking komen voor een andere ervaring, zien ze de standaardinhoud.**

   In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Frankrijk gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Frankrijk hebt bekeken, blijft deze bezoeker in de oorspronkelijke ervaring.

   ![Priority US > Germany](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Een ervaring die gericht is op &quot;Alle bezoekers&quot; kan worden gebruikt als de laatste ervaring in de ervaring die is opgedaan met activiteiten die erop gericht zijn bezoekers te &quot;vangen&quot; die geen andere ervaring hebben opgedaan. Als een ervaring gericht op &quot;Alle Bezoekers&quot;niet de laatste in de orde is, zullen andere gerichte gerangschikte ervaringen die lager zijn dan deze ervaring nog worden geëvalueerd.**

   In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Duitsland hebt bekeken, blijft deze bezoeker in Experience A (Amerikaanse bezoekers).

   ![Priority US > All Visitors](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

   Als dit ongewenst is, kunt u een nieuw publiek tot stand brengen dat uitdrukkelijk als omgekeerde van uw gericht publiek wordt bepaald, zoals aangetoond in het volgende voorbeeld:

   ![Priority US > Not US](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Met een XT-activiteit met één beleving blijven bezoekers in een beleving, zelfs als ze niet langer in aanmerking komen voor het publiek dat ze in die ervaring heeft geplaatst.**

   Als dit niet gewenst is, kunt u een andere ervaring maken die is gericht op het omgekeerde publiek (bijvoorbeeld &quot;Niet Verenigde Staten&quot; in tegenstelling tot &quot;Verenigde Staten&quot;).

   Als een andere optie, kon u A/B activiteit tot stand brengen die aan uw gewenste publiek met 100% verkeerstoewijzing wordt gericht, zoals hieronder getoond:

   ![Prioriteit één ervaring](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **De prioriteit van ervaringen wordt bepaald door hun orde (bovenkant neer) aangezien zij in het Doel UI tonen.**

   Dit is belangrijk om in gedachten te houden in scenario&#39;s waar een bezoeker voor meer dan één van uw publiek in aanmerking zou kunnen komen. Als u bijvoorbeeld twee ervaringen hebt: Een bezoeker in New York zou in aanmerking komen voor beide soorten publiek. Daarom moet u ervoor zorgen dat de &quot;ervaring van New York&quot;vóór de &quot;Verenigde Staten&quot;ervaring in het Doel UI wordt bepaald. Dit zorgt ervoor dat de gerichtere ervaring &quot;New York&quot;de hogere prioriteit heeft, zoals aangetoond in het volgende voorbeeld:

   ![Priority NY > US](/help/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)

