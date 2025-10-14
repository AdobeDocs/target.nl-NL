---
keywords: omleidingsaanbod;maak omleidingsaanbod;voeg html-aanbieding toe;geef alle URL-parameters door in omleiding;geef mboxSessionId door in omleiding (alleen nodig wanneer de omleiding naar een ander domein gaat)
description: Leer hoe te om omleidingsaanbiedingen in Adobe  [!DNL Target]  tot stand te brengen om browser te veroorzaken om aan een nieuwe pagina om te leiden.
title: Hoe maak ik omleidingsvoorstellen?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# Omleidingsvoorstellen maken

Met Omleiding van voorstellen in [!DNL Adobe Target] wordt een browser omgeleid naar een nieuwe pagina.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testactiviteiten in met twee ervaringen: een die verwijst naar de standaardpagina A en de andere die wordt doorgestuurd naar pagina B. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
> * Omleiden aanbiedingen kunnen op [!UICONTROL Offers] > [!UICONTROL Code Offers] pagina of in [&#x200B; op Forms-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) worden gecreeerd. U kunt geen omleidingsaanbiedingen in Visual Experience Composer (VEC) tot stand brengen of toepassen. Inhoud wordt ingespoten op de aanvraaglocaties van [!DNL Target] , zodat deze niet geschikt zijn voor een algemene [!DNL Target] -aanvraag.
>
>* Je kunt geen omleidingsvoorstellen gebruiken in ajax-vakken (`mboxUpdate`).
>
>* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Voor meer informatie, zie [&#x200B; Aanbiedingen opnieuw richten - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Voor informatie over vestiging een ervaring die opnieuw richt, zie [&#x200B; opnieuw richten aan een URL &#x200B;](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

De omleidingsaanbieding voert de code van JavaScript uit om browser om te leiden. De methode `window.location.replace();` wordt gebruikt, zodat de pagina waarvan de bezoeker is omgeleid, niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

## Een omleidingsvoorstel maken op de pagina Codevoorstellen

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![&#x200B; de Aanbiedingen van de Code tabel &#x200B;](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]** .

   ![&#x200B; creeer Redirect de dialoogdoos van de Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de Assets-bibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **omvat alle parameters URL:** Schuif de knevel om deze optie toe te laten als u alle parameters URL die op de vorige pagina aanwezig zijn aan de opnieuw gerichte pagina wilt worden verspreid.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen hebt opgegeven in het vak URL `https://www.mycompany.com/mensShirts.html` .

   * **Identiteitskaart van de Methakersessie van de Controle:** Vereist om aan een verschillend domein opnieuw te richten. Schuif de schakeloptie om deze optie in te schakelen als u wilt dat de `sessionId` automatisch wordt opgenomen in de omleiding. Dit is alleen vereist wanneer u een e-mailbericht test of op een ander domein klikt. De `sessionId` komt overeen met het cookie van de bezoeker, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Een omleidingsvoorstel maken met de Form-Based Experience Composer

1. Terwijl het creëren van een activiteit die [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) gebruikt, selecteer de plaats om de **[!UICONTROL Content]** sectie te tonen.

   ![&#x200B; sectie van de Inhoud in vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de vervolgkeuzelijst **[!UICONTROL Default Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]** .

   ![&#x200B; Redirect de optie van de Aanbieding van de Verandering &#x200B;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]** .

   ![&#x200B; creeer Redirect de dialoogdoos van de Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de Assets-bibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **omvat alle parameters URL:** Schuif de knevel om deze optie toe te laten als u alle parameters URL die op de vorige pagina aanwezig zijn aan de opnieuw gerichte pagina wilt worden verspreid.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen hebt opgegeven in het vak URL `https://www.mycompany.com/mensShirts.html` .

   * **Identiteitskaart van de Methakersessie van de Controle:** Vereist om aan een verschillend domein opnieuw te richten. Schuif de schakeloptie om deze optie in te schakelen als u wilt dat de `sessionId` automatisch wordt opgenomen in de omleiding. Dit is alleen vereist wanneer u een e-mailbericht test of op een ander domein klikt. De `sessionId` komt overeen met het cookie van de bezoeker, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Omleidingsvoorstellen gebruiken voor activiteiten

U moet omleidingsvoorstellen toepassen gebruikend [!UICONTROL Form-Based Experience Composer]. Je kunt momenteel geen omleidingsvoorstellen toepassen met de VEC.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests] -, [!UICONTROL Experience Targeting] (XT) - [!UICONTROL Automated Personalization] - (AP) - en [!UICONTROL Recommendations] -activiteiten wanneer de composer voor visuele beleving niet beschikbaar of praktisch is voor gebruik. U kunt de [!UICONTROL Form-Based Experience Composer] bijvoorbeeld gebruiken om ervaringen te maken die omleidingsaanbiedingen gebruiken.

1. Maak of bewerk een activiteit in de [!UICONTROL Form-Based Experience Composer] .

   Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde geleidelijke instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in de sectie **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]** .

   ![&#x200B; Redirect de optie van de Aanbieding van de Verandering &#x200B;](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Selecteer het gewenste omleidingsaanbod in het dialoogvenster [!UICONTROL Select Remote Offer] en klik op **[!UICONTROL Done]** .

1. Voltooi de configuratie van de activiteit.

## De video van de opleiding: Op vorm-Gebaseerde Composer ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer, waarmee u omleidingsaanbiedingen kunt maken.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
