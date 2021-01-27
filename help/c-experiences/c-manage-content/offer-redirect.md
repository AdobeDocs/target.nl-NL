---
keywords: redirect offer;create redirect offer;add html offer;Pass all URL parameters in redirect;Pass mboxSessionId in redirect (only needed when the redirect is going to a different domain)
description: Kan ik aanbiedingen omleiden gebruiken om een browser naar een nieuwe pagina te laten omleiden?
title: Omleidingsvoorstellen maken
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 15eb3050b4263358d0747b09a8afd2b4c102294c
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 0%

---


# Omleidingsvoorstellen maken

Met omleiding van voorstellen in [!DNL Adobe Target] wordt een browser omgeleid naar een nieuwe pagina.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testactiviteit in met twee ervaringen: één die aan standaardpagina A richt, en andere die aan pagina B wordt opnieuw gericht. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
> * Aanbiedingen voor omleiding kunnen worden gemaakt op de pagina [!UICONTROL Offers] [!UICONTROL Code Offers] of in de [Op Forms gebaseerde Experience Composer](/help/c-experiences/form-experience-composer.md). U kunt geen omleidingsaanbiedingen in Visual Experience Composer (VEC) tot stand brengen of toepassen. De inhoud zal in de [!DNL Target] verzoekplaatsen worden geïnjecteerd, zodat zijn deze hoogstwaarschijnlijk niet aangewezen voor een globaal [!DNL Target] verzoek.
   >
   >
* U kunt geen omleidingsvoorstellen in ajax dozen (`mboxUpdate`) gebruiken.
   >
   >
* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie [Aanbiedingen omleiden - A4T veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905) voor meer informatie.
   >
   >
* Zie [Omleiden naar een URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) voor informatie over het instellen van een ervaring die omleidt.


De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. De methode `window.location.replace();` wordt gebruikt, zodat de pagina waarvan de bezoeker is omgeleid niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

## Een omleidingsvoorstel maken op de pagina Codevoorstellen

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![Tabblad Codeaanbiedingen](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de middelenbibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

      U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen `https://www.mycompany.com/mensShirts.html` hebt ingevoerd in het vak URL.

   * **Sessie-id voor hoofdvak doorgeven:** vereist voor omleiding naar een ander domein. Schuif de schakeloptie om deze optie in te schakelen als u de `sessionId` automatisch wilt opnemen in de omleiding. Dit is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

      Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Een omleidingsvoorstel maken met de Form-Based Experience Composer

1. Selecteer tijdens het maken van een activiteit met de [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) de locatie waar u de **[!UICONTROL Content]**-sectie wilt weergeven.

   ![Sectie Inhoud in Form-Based Experience Composer](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de vervolgkeuzelijst **[!UICONTROL Default Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de middelenbibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

      U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen `https://www.mycompany.com/mensShirts.html` hebt ingevoerd in het vak URL.

   * **Sessie-id voor hoofdvak doorgeven:** vereist voor omleiding naar een ander domein. Schuif de schakeloptie om deze optie in te schakelen als u de `sessionId` automatisch wilt opnemen in de omleiding. Dit is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

      Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Omleidingsvoorstellen gebruiken voor activiteiten

U moet omleidingsvoorstellen toepassen gebruikend [!UICONTROL Form-Based Experience Composer]. Je kunt momenteel geen omleidingsvoorstellen toepassen met de VEC.

De [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Recommendations]-activiteiten wanneer de visuele ervaringscomposer niet beschikbaar of praktisch is voor gebruik. U kunt bijvoorbeeld [!UICONTROL Form-Based Experience Composer] gebruiken om ervaringen te maken die omleidingsaanbiedingen gebruiken.

1. Maak of bewerk een activiteit in [!UICONTROL Form-Based Experience Composer].

   Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor gedetailleerde stapsgewijze instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in de sectie **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Selecteer de gewenste omleidingsaanbieding van [!UICONTROL Select Remote Offer] dialoogdoos, dan klik **[!UICONTROL Done]**.

1. Voltooi de configuratie van de activiteit.

## Trainingsvideo: De inhouds-opslagplaats (4:56) ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het beheren van inhoud.

* Verbinding tussen de [Experience Cloud-elementenbibliotheek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) en de doelinhoudsbibliotheek
* Aangepaste HTML-aanbiedingen
* Aangepaste HTML-aanbieding in de Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)
