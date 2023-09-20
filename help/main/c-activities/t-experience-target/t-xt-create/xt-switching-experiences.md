---
keywords: prioriteit;ervaring maken;prioriteit;ervaring;publiek;ervaring;schakelen tussen ervaringen;visuele ervaringscomposer
description: Leer hoe bezoekers kunnen schakelen tussen ervaringen in een [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activiteit aangezien hun profielen evolueren.
title: Bezoekers kunnen van ervaring wisselen in een [!UICONTROL Experience Targeting] Activiteit?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Overschakelen van ervaringen in [!UICONTROL Experience Targeting]

Met [!UICONTROL Experience Targeting]kunt u bepalen welke bezoekers zien hoe hun profielen evolueren.

De volgende lijst bevat slechts een paar scenario&#39;s waarin bezoekersprofielen kunnen evolueren en u verschillende inhoud wilt voorstellen die op die veranderingen wordt gebaseerd:

| Scenario | Details |
|--- |--- |
| Geografische locatie | bezoekers kunnen uw website of mobiele app vanuit verschillende geografische locaties bekijken terwijl ze voor zakelijke doeleinden of plezier reizen. |
| Klantstatus | Bezoekers kunnen als een vooruitzicht worden beschouwd voordat ze een account maken of een product kopen. |
| Categorie-affiniteit | De [categorie-affiniteit](/help/main/c-target/c-visitor-profile/category-affinity.md) functie in [!DNL Target] legt automatisch de bezoekersweergave van de categorieën vast en berekent vervolgens de affiniteit van de bezoekers voor de categorie voor doeldoeleinden. bezoekers die bijvoorbeeld verschillende artikelen over een bepaald onderwerp op uw website hebben weergegeven, krijgen inhoud over dat onderwerp te zien. |
| Weekdag | Wanneer het weekend nadert, wilt u bezoekers wellicht inhoud laten zien over films, dineren of andere vormen van entertainment. |

Als u deze mogelijkheden wilt gebruiken in [!DNL Target]is het belangrijk dat u de volgende informatie begrijpt terwijl u werkt met [!UICONTROL Experience Targeting] activiteiten:

* **De prioriteit wordt bepaald door de volgorde van de ervaringen, van boven naar beneden.** Als een bezoeker voor meer dan twee soorten publiek in aanmerking komt, ontvangt die bezoeker inhoud van de ervaring met hogere prioriteit.
* **Bezoekers schakelen tussen ervaringen in een [!UICONTROL Experience Targeting] activiteit als zij beginnen in aanmerking te komen voor het publiek van een ervaring met hogere prioriteit.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat deze bezoeker uw website vanuit Duitsland had bekeken, schakelde hij over op Experience B (bezoekers uit Duitsland).

  ![Priority US > Germany](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Bezoekers wisselen ook tussen ervaringen als ze niet langer voor hun huidige publiek in aanmerking komen maar voor een ervaring met een lagere prioriteit.**
* **Als bezoekers niet langer in aanmerking komen voor hun huidige ervaring en niet langer in aanmerking komen voor een andere ervaring, zien ze de standaardinhoud.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Frankrijk gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Frankrijk hebt bekeken, blijft deze bezoeker in de oorspronkelijke ervaring.

  ![Priority US > Germany](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **Als laatste ervaring in de [!UICONTROL Experience Targeting] activiteiten om bezoekers die niet voor een andere ervaring in aanmerking komen, te &quot;vangen&quot;. Als een ervaring die bedoeld is voor &quot;Alle bezoekers&quot; niet de laatste in de volgorde is, worden andere doelgerichte ervaringen die lager zijn vermeld dan deze ervaring nog geëvalueerd.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Duitsland hebt bekeken, blijft deze bezoeker in Experience A (Amerikaanse bezoekers).

  ![Priority US > All Visitors](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Als dit ongewenst is, kunt u een nieuw publiek tot stand brengen dat uitdrukkelijk als omgekeerde van uw gericht publiek wordt bepaald, zoals aangetoond in het volgende voorbeeld:

  ![Priority US > Not US](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **Met één ervaring [!UICONTROL Experience Targeting] de bezoekers blijven in een ervaring zelfs als zij niet langer in aanmerking komen voor het publiek dat hen in die ervaring plaatst .**

  Als dit niet gewenst is, kunt u een andere ervaring maken die is gericht op het omgekeerde publiek (bijvoorbeeld &quot;Niet Verenigde Staten&quot; in tegenstelling tot &quot;Verenigde Staten&quot;).

  Als andere optie kunt u een [!UICONTROL A/B Test] activiteit gericht aan uw gewenste publiek met 100% verkeerstoewijzing, zoals hieronder getoond:

  ![Prioriteit één ervaring](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **De prioriteit van ervaringen wordt bepaald door hun volgorde (boven naar beneden) zoals deze worden weergegeven in het dialoogvenster [!DNL Target] UI.**

  Dit is belangrijk om in gedachten te houden wanneer een bezoeker voor meer dan één van uw publiek in aanmerking zou kunnen komen. Als u bijvoorbeeld twee ervaringen hebt: een ervaring gericht op &quot;Verenigde Staten&quot; en een ervaring gericht op &quot;New York&quot;, komt een bezoeker in New York in aanmerking voor beide soorten publiek. Daarom moet u ervoor zorgen dat de &quot;New York&quot;ervaring vóór de &quot;Verenigde Staten&quot;ervaring in &quot;wordt bepaald [!DNL Target] UI. Deze praktijk zorgt ervoor dat de meer gerichte ervaring &quot;New York&quot;de hogere prioriteit heeft, zoals aangetoond in het volgende voorbeeld:

  ![Priority NY > US](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
