---
keywords: prioriteit;ervaring maken;prioriteit;ervaring;publiek;ervaring;schakelen tussen ervaringen;visuele ervaringscomposer
description: Leer hoe de bezoekers tussen ervaringen in een  [!DNL Adobe Target] [!UICONTROL Experience Targeting] (XT) activiteit kunnen schakelen aangezien hun profielen evolueren.
title: Kunnen bezoekers van ervaring wisselen in een [!UICONTROL Experience Targeting] -activiteit?
feature: Experience Targeting
exl-id: 8d931764-8ba7-4eac-99db-60659086b8be
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Overschakelen tussen ervaringen in [!UICONTROL Experience Targeting]

Met [!UICONTROL Experience Targeting] kunt u bepalen welke bezoekers zien hoe hun profielen evolueren.

De volgende lijst bevat slechts een paar scenario&#39;s waarin bezoekersprofielen kunnen evolueren en u verschillende inhoud wilt voorstellen die op die veranderingen wordt gebaseerd:

| Scenario | Details |
|--- |--- |
| Geografische locatie | bezoekers kunnen uw website of mobiele app vanuit verschillende geografische locaties bekijken terwijl ze voor zakelijke doeleinden of plezier reizen. |
| Klantstatus | Bezoekers kunnen als een vooruitzicht worden beschouwd voordat ze een account maken of een product kopen. |
| Categorie-affiniteit | De [&#x200B; eigenschap van de categorieaffiniteit &#x200B;](/help/main/c-target/c-visitor-profile/category-affinity.md) in [!DNL Target] vangt automatisch de mening van categoriebezoekers en berekent dan de affiniteit van bezoekers voor de categorie voor het richten van doeleinden. bezoekers die bijvoorbeeld verschillende artikelen over een bepaald onderwerp op uw website hebben weergegeven, krijgen inhoud over dat onderwerp te zien. |
| Weekdag | Wanneer het weekend nadert, wilt u bezoekers wellicht inhoud laten zien over films, dineren of andere vormen van entertainment. |

Als u deze functies wilt gebruiken in [!DNL Target] , is het belangrijk dat u de volgende informatie begrijpt terwijl u met [!UICONTROL Experience Targeting] -activiteiten werkt:

* **Prioriteit wordt gecontroleerd door de orde van ervaringen, van boven tot onder.** Als een bezoeker voor meer dan twee soorten publiek in aanmerking komt, ontvangt die bezoeker inhoud van de ervaring met hogere prioriteit.
* **bezoekers schakelen tussen ervaringen in een [!UICONTROL Experience Targeting] activiteit als zij voor het publiek van een hoog-prioritaire ervaring beginnen kwalificeren.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat deze bezoeker uw website vanuit Duitsland had bekeken, schakelde hij over op Experience B (bezoekers uit Duitsland).

  ![&#x200B; Prioriteit US > Duitsland &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **bezoekers schakelen ook tussen ervaringen als zij ophouden kwalificerend voor hun huidige publiek maar beginnen kwalificerend voor een lager-prioritaire ervaring.**
* **als de bezoekers ophouden kwalificerend voor hun huidige ervaring, en niet voor een andere ervaring kwalificeren, zien zij standaardinhoud.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Frankrijk gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Frankrijk hebt bekeken, blijft deze bezoeker in de oorspronkelijke ervaring.

  ![&#x200B; Prioriteit US > Duitsland &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_germany-new.png)

* **een ervaring die aan &quot;Alle Bezoekers&quot;wordt gericht kan als laatste ervaring in de [!UICONTROL Experience Targeting] activiteit worden gebruikt om het even welke bezoekers &quot;te &quot;vangen&quot;die niet voor een andere ervaring gekwalificeerd hebben. Als een ervaring gericht op &quot;Alle Bezoekers&quot;niet de laatste in de orde is, worden andere gerichte gerangschikte ervaringen die lager dan deze ervaring worden vermeld nog geëvalueerd.**

  In de volgende activiteiteninstellingen heeft een bezoeker bijvoorbeeld uw website geopend vanuit de Verenigde Staten en vervolgens naar Duitsland gereisd en een tweede keer naar uw website bezocht. Tijdens het eerste bezoek kwam deze bezoeker in aanmerking voor Experience A (Amerikaanse bezoekers). Nadat u uw website vanuit Duitsland hebt bekeken, blijft deze bezoeker in Experience A (Amerikaanse bezoekers).

  ![&#x200B; Prioriteit US > Alle Bezoekers &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_all_visitors-new.png)

  Als dit ongewenst is, kunt u een nieuw publiek tot stand brengen dat uitdrukkelijk als omgekeerde van uw gericht publiek wordt bepaald, zoals aangetoond in het volgende voorbeeld:

  ![&#x200B; Prioriteit US > niet US &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_us_not_us-new.png)

* **met een enig-ervaring [!UICONTROL Experience Targeting] activiteit, blijven de bezoekers in een ervaring zelfs als zij niet kwalificeren voor het publiek dat hen in die ervaring zet.**

  Als dit niet gewenst is, kunt u een andere ervaring maken die is gericht op het omgekeerde publiek (bijvoorbeeld &quot;Niet Verenigde Staten&quot; in tegenstelling tot &quot;Verenigde Staten&quot;).

  Als een andere optie kunt u een [!UICONTROL A/B Test] -activiteit maken voor het gewenste publiek met een verkeerstoewijzing van 100%, zoals hieronder wordt getoond:

  ![&#x200B; Prioriteit één ervaring &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_one_experience-new.png)

* **de prioriteit van ervaringen wordt bepaald door hun orde (bovenkant neer) aangezien zij in [!DNL Target] UI tonen.**

  Dit is belangrijk om in gedachten te houden wanneer een bezoeker voor meer dan één van uw publiek in aanmerking zou kunnen komen. Als u bijvoorbeeld twee ervaringen hebt: een ervaring gericht op &quot;Verenigde Staten&quot; en een ervaring gericht op &quot;New York&quot;, komt een bezoeker in New York in aanmerking voor beide soorten publiek. Daarom moet u ervoor zorgen dat de ervaring &quot;New York&quot;vóór de &quot;Verenigde Staten&quot;ervaring in [!DNL Target] UI wordt bepaald. Deze praktijk zorgt ervoor dat de meer gerichte ervaring &quot;New York&quot;de hogere prioriteit heeft, zoals aangetoond in het volgende voorbeeld:

  ![&#x200B; Prioriteit NY > VS &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_priority_ny_us-new.png)
