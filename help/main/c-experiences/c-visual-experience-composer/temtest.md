---
keywords: sjabloon testen;sjabloon;zelfde ervaring op vergelijkbare pagina's;sjabloontest
description: Leer hoe u de Adobe gebruikt [!DNL Target] Visuele Composer van de Ervaring (VEC) om de zelfde ervaring op veelvoudige pagina's te omvatten die gelijkaardig gestructureerd zijn of de zelfde malplaatjeelementen bevatten.
title: Kan ik dezelfde ervaring opnemen op vergelijkbare pagina's?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s

Een paginasjabloon gebruiken in [!DNL Adobe Target] om uw pagina&#39;s een structuur te geven, of als uw pagina&#39;s vergelijkbare elementen bevatten, om variaties in pagina-elementen met een vergelijkbare structuur of in het hele domein te testen.

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

1. Een activiteit maken of bewerken zoals beschreven in [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Als u de pagina&#39;s wilt opgeven waar de ervaring wordt weergegeven, gaat u naar het tabblad [!UICONTROL Visual Experience Composer] (VEC) klik op het tandwielpictogram en selecteer vervolgens **[!UICONTROL Page Delivery]**.

   ![Gear icon > Page Delivery](/help/main/c-experiences/c-visual-experience-composer/assets/icon-gear.png)

1. Klikken **[!UICONTROL Add Template Rule]** en geeft u vervolgens de criteria op voor de pagina&#39;s waaraan u de ervaring wilt toevoegen.

1. Geef het paginabereik op. Het paginabereik kan een van de volgende zijn:

   * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie [Veelgestelde vragen over doelen en doelgroepen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
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

   Als u bijvoorbeeld **[!UICONTROL Domain]** en **[!UICONTROL Is (case sensitive)]** Typ het domein waar u de ervaring aan alle pagina&#39;s wilt toevoegen.

   U kunt meerdere items opnemen.

   >[!IMPORTANT]
   >
   >Meerdere items gebruiken OR-logica, wat betekent dat een enkel item in de lijst de voorwaarde waar maakt.

1. Voer desgewenst aanvullende criteria in door op **[!UICONTROL Add Template Rule]** en de procedure in de vorige stappen te herhalen.

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

1. Een activiteit maken of bewerken zoals beschreven in [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03).

1. Om het domein te specificeren waar de ervaring zal verschijnen, in Visual Experience Composer klikt het tandwielpictogram, dan selecteren **[!UICONTROL Page Delivery]**.

1. Klik op **[!UICONTROL Add Template Rule]** > **[!UICONTROL Domain]**.

1. Van de **[!UICONTROL Choose evaluator]** vervolgkeuzelijst, selecteert u **[!UICONTROL Contains]** en geeft u het domein op.

   ![Domein bevat](/help/main/c-experiences/c-visual-experience-composer/assets/domain-template-rule.png)

## Trainingsvideo: Visual Experience Composer (2 van 2) (7:29) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

* Een ervaring hernoemen en dupliceren
* Omleiden maken
* Een activiteit als doel instellen op één URL of een groep URL&#39;s
* Een activiteit met meerdere pagina&#39;s maken
* Ervaring voor responsieve websites voorvertonen en opbouwen
* Overlays gebruiken om typen elementen te markeren

>[!VIDEO](https://video.tv.adobe.com/v/17401)
