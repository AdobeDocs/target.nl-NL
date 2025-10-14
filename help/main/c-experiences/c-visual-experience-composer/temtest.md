---
keywords: sjabloon testen;sjabloon;zelfde ervaring op vergelijkbare pagina's;sjabloontest
description: Leer hoe te om Adobe  [!DNL Target]  Visuele Composer van de Ervaring (VEC) te gebruiken om de zelfde ervaring op veelvoudige pagina's te omvatten die gelijkaardig gestructureerd zijn of de zelfde malplaatjeelementen bevatten.
title: Kan ik dezelfde ervaring opnemen op vergelijkbare pagina's?
feature: Experiences and Offers
exl-id: 4ea95794-496c-4eff-96ec-8a9d1f732c4a
source-git-commit: be9996c4dce0a3135a39fcbf0608b57b6e742ac3
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Dezelfde ervaring opnemen op vergelijkbare pagina&#39;s

Gebruik een paginasjabloon in [!DNL Adobe Target] om uw pagina&#39;s een structuur te geven, of als uw pagina&#39;s vergelijkbare elementen bevatten, om variaties in pagina-elementen met een vergelijkbare structuur of in het gehele domein te testen.

Deze functie werkt alleen correct als deze wordt gebruikt op pagina&#39;s met een vergelijkbare structuur of sjabloonelementen die op alle pagina&#39;s dezelfde structuur hebben.

>[!IMPORTANT]
>
>Als u deze functie gebruikt om elementen te wijzigen op verschillende pagina&#39;s, heeft dit waarschijnlijk onverwachte resultaten.

U kunt deze functie bijvoorbeeld gebruiken om een van de volgende handelingen uit te voeren:

* Een algemene navigatiebalk testen door elementen opnieuw te rangschikken of te verwijderen
* Een item verwijderen uit alle productpagina&#39;s waarop een bepaalde paginasjabloon wordt gebruikt
* Een banner toevoegen aan alle productpagina&#39;s
* De lay-out van de artikelsjabloon wijzigen

U kunt pagina&#39;s specificeren die de veranderingselementen omvatten, of de verandering over uw plaats of domein toepassen.

1. Creeer of geef een activiteit uit zoals die in [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) wordt beschreven.

1. Om de pagina&#39;s te specificeren waar de ervaring verschijnt, in [!UICONTROL Visual Experience Composer] (VEC) klik het [!UICONTROL Configure] pictogram ( ![&#x200B; vormt pictogram &#x200B;](/help/main/assets/icons/Setting.svg)), dan uitgezochte **[!UICONTROL Page Delivery]**.

1. Klik op **[!UICONTROL Add Rule]** en geef vervolgens de criteria op voor de pagina&#39;s waaraan u de ervaring wilt toevoegen.

1. Geef het paginabereik op. Het paginabereik kan een van de volgende zijn:

   * [!UICONTROL URL] (Voor meer informatie over hoe [!DNL Target] URLs evalueert, zie [&#x200B; Doelen en veelgestelde vragen van publiek &#x200B;](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
   * [!UICONTROL Domain]
   * [!UICONTROL Path]
   * [!UICONTROL Hash (#) Fragment] (doel het deel van een URL dat volgt op het #-symbool.)
   * [!UICONTROL Query]
   * [!UICONTROL Custom]

1. Kies een operator.

   De operator geeft aan hoe de items na de operator betrekking hebben op het paginabereik. Beschikbare operatoren zijn:

   * [!UICONTROL Contains]
   * [!UICONTROL Does not contain]
   * [!UICONTROL Is (case sensitive)]
   * [!UICONTROL Is not]
   * [!UICONTROL Starts with]
   * [!UICONTROL Ends with]

1. Typ de tekenreeksen die bepalen waar de ervaring wordt toegevoegd, zoals het domein of de tekenreeksen in de paginanaam.

   Als u bijvoorbeeld **[!UICONTROL Domain]** en **[!UICONTROL Is (case sensitive)]** selecteert, typt u het domein waar u de ervaring aan alle pagina&#39;s wilt toevoegen.

   U kunt meerdere items opnemen.

   >[!IMPORTANT]
   >
   >Meerdere items gebruiken OR-logica, wat betekent dat een enkel item in de lijst de voorwaarde waar maakt.

1. Voer desgewenst aanvullende criteria in door op **[!UICONTROL Add Rule]** te klikken en de procedure in de vorige stappen te herhalen.

   De veelvoudige criteria worden aangesloten bij EN logica. [!DNL Target] voegt de ervaring toe aan alle pagina&#39;s die aan de opgegeven criteria voldoen.

>[!IMPORTANT]
>
> [!DNL Target] kan de pagina&#39;s niet controleren om er zeker van te zijn dat ze er naar behoren uitzien. Het is daarom altijd belangrijk dat u deze functie gebruikt om de desbetreffende pagina&#39;s te testen voordat u ze openbaar maakt.

## Gebruik hoofdletters

Bekijk de volgende gebruiksgevallen voor manieren om sjabloonregels op uw site te gebruiken:

### Dezelfde activiteit in het gehele domein renderen

U zou het gebruiken van malplaatjeregels kunnen overwegen om de zelfde activiteit over uw volledig domein voor de volgende gebruiksgevallen terug te geven:

* Een algemene kop- of voettekst opnemen
* Een globale banner opnemen (bijvoorbeeld COVID-19-aankondigingen)
* Een wereldwijde gratis verzendaanbieding opnemen

1. Creeer of geef een activiteit uit zoals die in [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) wordt beschreven.

1. Om het domein te specificeren waar de ervaring verschijnt, in [!UICONTROL Visual Experience Composer] klik het [!UICONTROL Configure] pictogram ( ![&#x200B; vormt pictogram &#x200B;](/help/main/assets/icons/Setting.svg)), dan selecteren **[!UICONTROL Page Delivery]**.

1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Domain]** .

1. Selecteer **[!UICONTROL Choose evaluator]** in de vervolgkeuzelijst **[!UICONTROL Contains]** en geef vervolgens het domein op.
