---
keywords: redirect offer;create redirect offer;add html offer;Pass all URL parameters in redirect;Pass mboxSessionId in redirect (only needed when the redirect is going to a different domain)
description: Informatie over omleidingsvoorstellen in Adobe Target die ervoor zorgen dat een browser omleidt naar een nieuwe pagina.
title: Omleidingsvoorstellen maken
feature: offers
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 1%

---


# Omleidingsaanbiedingen maken{#create-redirect-offers}

De omleidingsaanbieding leidt een browser om naar een nieuwe pagina.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testcampagne in met twee ervaringen: één die aan standaardpagina A richt, en andere die aan pagina B wordt opnieuw gericht. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
>Je kunt geen omleidingsvoorstellen gebruiken in ajax-vakken ( `mboxUpdate`).
>
>Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie [Aanbiedingen omleiden - A4T veelgestelde vragen](/help/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905) voor meer informatie.

Zie [Omleiden naar een URL](/help/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA) voor informatie over het instellen van een ervaring die omleidt.

De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. De methode `window.location.replace();` wordt gebruikt, zodat de pagina waarvan de bezoeker is omgeleid niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

**Een omleidingsvoorstel maken:**

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.
1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.
1. Typ een naam voor het voorstel.
1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

* **Alle URL-parameters opnemen:** Schakel dit selectievakje in als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

   U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u dit selectievakje inschakelt, wordt uw omleidingsvoorstel op pagina [!DNL `https://www.mycompany.com/mens.html?emailId=123`] automatisch [!DNL `https://www.mycompany.com/mensShirts.html?emailId=123`] wanneer u alleen [!DNL `https://www.mycompany.com/mensShirts.html`] hebt ingevoerd in het vak URL.

* **Geef de sessie-id van de box door (die vereist is voor omleiding naar een ander domein):** schakel dit vakje in als u wilt dat de sessie-id automatisch wordt opgenomen  `sessionId` in de omleiding. Dit is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

   Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van het postvak niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Trainingsvideo: De inhouds-opslagplaats (4:56) ![Overzichtsbadge](/help/assets/overview.png)

Deze video bevat informatie over het beheren van inhoud.

* Verbinding tussen de [Experience Cloud-elementenbibliotheek](https://experienceleague.adobe.com/docs/core-services/interface/assets/creative-cloud.html) en de doelinhoudsbibliotheek
* Aangepaste HTML-aanbiedingen
* Aangepaste HTML-aanbieding in de Visual Experience Composer

>[!VIDEO](https://video.tv.adobe.com/v/17387)
