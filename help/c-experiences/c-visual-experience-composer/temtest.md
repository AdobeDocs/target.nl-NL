---
keywords: template testing;template;same experience on similar pages;template test
description: Als u een paginasjabloon gebruikt om uw pagina's een structuur te geven of als uw pagina's vergelijkbare elementen bevatten, kunt u met deze functie variaties in pagina-elementen met een vergelijkbare structuur testen.
title: Dezelfde ervaring opnemen op vergelijkbare pagina's
uuid: 055b276e-2492-40d8-b48e-849dffa93f35
translation-type: tm+mt
source-git-commit: 65a4fd0d05ad065c9291a83dc0b3066451f7373e

---


# Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s{#include-the-same-experience-on-similar-pages}

Als u een paginasjabloon gebruikt om uw pagina&#39;s een structuur te geven of als uw pagina&#39;s vergelijkbare elementen bevatten, kunt u met deze functie variaties in pagina-elementen met een vergelijkbare structuur testen.

Deze functie werkt alleen correct als deze wordt gebruikt op pagina&#39;s met een vergelijkbare structuur. of sjabloonelementen bevatten die op alle pagina&#39;s op dezelfde manier zijn gestructureerd.

>[!IMPORTANT]
>
>Als u deze functie gebruikt om elementen op verschillende pagina&#39;s te wijzigen, leidt dit waarschijnlijk tot onverwachte resultaten.

U kunt deze functie bijvoorbeeld gebruiken om een van de volgende handelingen uit te voeren:

* Een algemene navigatiebalk testen door elementen opnieuw te rangschikken of te verwijderen
* Een item verwijderen uit alle productpagina&#39;s waarop een bepaalde paginasjabloon wordt gebruikt
* Een banner toevoegen aan alle productpagina&#39;s
* De lay-out van een artikelsjabloon wijzigen

De volgende demo-video bevat informatie over het gebruik van een sjabloon:

U kunt pagina&#39;s specificeren die de veranderingselementen omvatten, of de verandering over uw plaats toepassen.

1. Maak een activiteit zoals beschreven in [Activiteiten](../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).
1. Om de pagina&#39;s te specificeren waar de ervaring zal verschijnen, in Visual Experience Composer klikt het tandwielpictogram, dan uitgezocht **[!UICONTROL Page Delivery]**.
1. Klik **[!UICONTROL Add Template Rule]** en geef de criteria op voor de pagina&#39;s waaraan u de ervaring wilt toevoegen.

1. Geef het paginabereik op. Het paginabereik kan een van de volgende zijn:

   * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie de Veelgestelde vragen van [Doelen en van het publiek](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * Domein
   * Pad
   * Hash-fragment (#) (Doel het deel van een URL dat volgt op het #-symbool.)
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

   Als u bijvoorbeeld de optie selecteert **[!UICONTROL Domain]** en **[!UICONTROL Is (case sensitive)]** typt, typt u het domein waar u de ervaring aan alle pagina&#39;s wilt toevoegen.

   U kunt meerdere items opnemen.

   >[!IMPORTANT]
   >
   >Meerdere items gebruiken `OR` logica. Dit betekent dat elk item in de lijst de voorwaarde waar maakt.

1. Voer desgewenst aanvullende criteria in door op de procedure in de vorige stap te klikken **[!UICONTROL Add Template Rule]** en deze te herhalen.

   De veelvoudige criteria worden aangesloten bij EN logica. Adobe Target voegt de ervaring toe aan alle pagina&#39;s die aan de opgegeven criteria voldoen.

>[!IMPORTANT]
>
> Doel kan de pagina&#39;s niet controleren om ervoor te zorgen dat ze er naar behoren uitzien. Het is dus altijd belangrijk dat u deze functie gebruikt om de desbetreffende pagina&#39;s te testen voordat u ze openbaar maakt.

## Trainingsvideo: Videozelfstudie-badge Visual Experience Composer (2 van 2) (7:29) ![](/help/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)