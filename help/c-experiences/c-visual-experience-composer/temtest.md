---
keywords: sjabloon testen;sjabloon;zelfde ervaring op vergelijkbare pagina's;sjabloontest
description: Leer hoe te om Adobe Target Visual Experience Composer (VEC) te gebruiken om de zelfde ervaring op veelvoudige pagina's te omvatten die op gelijkaardige wijze gestructureerd zijn of de zelfde malplaatjeelementen bevatten.
title: Kan ik dezelfde ervaring opnemen op vergelijkbare pagina's?
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---


# Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s

Gebruik een paginamalplaatje in [!DNL Adobe Target] om structuur aan uw pagina&#39;s te verstrekken, of als uw pagina&#39;s gelijkaardige elementen bevatten, om variaties in op gelijkaardige structuur geplaatste paginaelementen of over uw volledig domein te testen.

Deze functie werkt alleen correct als deze wordt gebruikt op pagina&#39;s met een vergelijkbare structuur of sjabloonelementen die op alle pagina&#39;s dezelfde structuur hebben.

>[!IMPORTANT]
>
>Als u deze functie gebruikt om elementen op verschillende pagina&#39;s te wijzigen, leidt dit waarschijnlijk tot onverwachte resultaten.

U kunt deze functie bijvoorbeeld gebruiken om een van de volgende handelingen uit te voeren:

* Een algemene navigatiebalk testen door elementen opnieuw te rangschikken of te verwijderen
* Een item verwijderen uit alle productpagina&#39;s waarop een bepaalde paginasjabloon wordt gebruikt
* Een banner toevoegen aan alle productpagina&#39;s
* De lay-out van een artikelsjabloon wijzigen

U kunt pagina&#39;s specificeren die de veranderingselementen omvatten, of de verandering over uw plaats of domein toepassen.

1. Maak of bewerk een activiteit zoals beschreven in [Activiteiten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Als u de pagina&#39;s wilt opgeven waar de ervaring wordt weergegeven, klikt u in [!UICONTROL Visual Experience Composer] (VEC) op het tandwielpictogram en selecteert u **[!UICONTROL Page Delivery]**.

   ![Gear icon > Page Delivery](/help/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Klik **[!UICONTROL Add Template Rule]**, dan specificeer de criteria voor de pagina&#39;s u de ervaring aan wilt toevoegen.

1. Geef het paginabereik op. Het paginabereik kan een van de volgende zijn:

   * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie [Doelen en veelgestelde vragen ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Domein
   * Pad
   * Hash-fragment (#) (doel het deel van een URL dat volgt op het #-symbool.)
   * Query
   * Parameter

1. Kies een operator.

   De operator geeft aan hoe de items na de operator betrekking hebben op het paginabereik. Beschikbare operatoren zijn:

   * Bevat
   * Bevat niet
   * Is (hoofdlettergevoelig)
   * Is niet
   * Begint met
   * Eindigt met

1. Typ de tekenreeksen die bepalen waar de ervaring wordt toegevoegd, zoals het domein of de tekenreeksen in de paginanaam.

   Als u bijvoorbeeld **[!UICONTROL Domain]** en **[!UICONTROL Is (case sensitive)]** selecteert, typt u het domein waar u de ervaring aan alle pagina&#39;s wilt toevoegen.

   U kunt meerdere items opnemen.

   >[!IMPORTANT]
   >
   >Meerdere items gebruiken OR-logica, wat betekent dat een enkel item in de lijst de voorwaarde waar maakt.

1. Voer desgewenst aanvullende criteria in door op **[!UICONTROL Add Template Rule]** te klikken en de procedure in de vorige stappen te herhalen.

   De veelvoudige criteria worden aangesloten bij EN logica. [!DNL Target] Hiermee voegt u de ervaring toe aan alle pagina&#39;s die aan de opgegeven criteria voldoen.

>[!IMPORTANT]
>
> [!DNL Target] Kan de pagina&#39;s niet controleren om ervoor te zorgen dat ze er naar behoren uitzien. Het is dus altijd belangrijk dat u deze functie gebruikt om de desbetreffende pagina&#39;s te testen voordat u ze openbaar maakt.

## Gebruik hoofdletters

Bekijk de volgende gebruiksgevallen voor manieren om sjabloonregels op uw site te gebruiken:

### Dezelfde activiteit in het gehele domein renderen

U zou het gebruiken van malplaatjeregels kunnen overwegen om de zelfde activiteit over uw volledig domein voor de volgende gebruiksgevallen terug te geven:

* Een algemene kop- of voettekst opnemen
* Een globale banner opnemen (bijvoorbeeld COVID-19-aankondigingen)
* Een wereldwijde gratis verzendaanbieding opnemen

1. Maak of bewerk een activiteit zoals beschreven in [Activiteiten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Om het domein te specificeren waar de ervaring zal verschijnen, in Visual Experience Composer klikt het tandwielpictogram, dan uitgezocht **[!UICONTROL Page Delivery]**.

1. Klik op **[!UICONTROL Add Template Rule]** > **[!UICONTROL Domain]**.

1. Selecteer **[!UICONTROL Choose evaluator]** in de vervolgkeuzelijst **[!UICONTROL Contains]** en geef vervolgens het domein op.

   ![Domein bevat](/help/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Trainingsvideo: Visual Experience Composer (2 van 2) (7:29) ![Zelfstudie badge](/help/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)