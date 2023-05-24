---
keywords: omleidingsaanbod;maak omleidingsaanbod;voeg html-aanbieding toe;geef alle URL-parameters door in omleiding;geef mboxSessionId door in omleiding (alleen nodig wanneer de omleiding naar een ander domein gaat)
description: Meer informatie over het maken van omleidingsvoorstellen in Adobe [!DNL Target] om ervoor te zorgen dat een browser omleidt naar een nieuwe pagina.
title: Hoe maak ik omleidingsvoorstellen?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 0%

---

# Omleidingsvoorstellen maken

Aanbiedingen omleiden in [!DNL Adobe Target] zorgt ervoor dat een browser omleidt naar een nieuwe pagina.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een A/B-testactiviteit in met twee ervaringen: één die aan standaardpagina A richt, en andere die aan pagina B wordt opnieuw gericht. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
> * Aanbiedingen voor omleiding kunnen worden gemaakt op de [!UICONTROL Offers] > [!UICONTROL Code Offers] of in de [Op Forms gebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md). U kunt geen omleidingsaanbiedingen in Visual Experience Composer (VEC) tot stand brengen of toepassen. De inhoud wordt geïnjecteerd in de [!DNL Target] aanvraaglocaties, zodat deze meestal niet geschikt zijn voor een globale [!DNL Target] verzoek.
>
>* Je kunt geen omleidingsvoorstellen gebruiken in ajax-vakken (`mboxUpdate`).
>
>* Voor omleidingsaanbiedingen in activiteiten die A4T gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie voor meer informatie [Omleidingsvoorstellen - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Voor informatie over vestiging een ervaring die omleidt, zie [Omleiden naar een URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).


De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. Het gebruikt de `window.location.replace();` methode, zodat de pagina waarvan de bezoeker wordt omgeleid niet in de browsergeschiedenis wordt opgeslagen. Hierdoor kan de bezoeker de knop Terug in zijn browser nog steeds gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, kunt u het beste een HTML-aanbieding gebruiken in plaats van een omleidingsvoorstel.

## Een omleidingsvoorstel maken op de pagina Codevoorstellen

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![Tabblad Codeaanbiedingen](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de middelenbibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

      U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Door deze optie in te schakelen, kunt u het omleidingsvoorstel op de pagina uitvoeren `https://www.mycompany.com/mens.html?emailId=123` wordt automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer alles wat u hebt ingevoerd in het vak URL was `https://www.mycompany.com/mensShirts.html`.

   * **ID van wachtwoordsessie doorgeven:** Vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u de optie `sessionId` automatisch in de omleiding worden opgenomen. Dit is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden bijgehouden en de juiste inhoud wordt weergegeven.

      Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Een omleidingsvoorstel maken met de Form-Based Experience Composer

1. Tijdens het maken van een activiteit met de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md)selecteert u de locatie waar u de **[!UICONTROL Content]** sectie.

   ![Sectie Inhoud in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de knop **[!UICONTROL Default Content]** vervolgkeuzelijst en vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de middelenbibliotheek.

1. Voer de URL in voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Dit moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

      U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Door deze optie in te schakelen, kunt u het omleidingsvoorstel op de pagina uitvoeren `https://www.mycompany.com/mens.html?emailId=123` wordt automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer alles wat u hebt ingevoerd in het vak URL was `https://www.mycompany.com/mensShirts.html`.

   * **ID van wachtwoordsessie doorgeven:** Vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u de optie `sessionId` automatisch in de omleiding worden opgenomen. Dit is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden bijgehouden en de juiste inhoud wordt weergegeven.

      Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementation Consultant voordat u deze tests start.

## Omleidingsvoorstellen gebruiken voor activiteiten

Je moet omleidingsvoorstellen toepassen met de [!UICONTROL Form-Based Experience Composer]. Je kunt momenteel geen omleidingsvoorstellen toepassen met de VEC.

De [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Recommendations] activiteiten wanneer de composer voor visuele ervaring niet beschikbaar of praktisch voor gebruik is. U kunt bijvoorbeeld de opdracht [!UICONTROL Form-Based Experience Composer] om ervaringen te creëren die omleidingsaanbiedingen gebruiken.

1. Een activiteit maken of bewerken in het dialoogvenster [!UICONTROL Form-Based Experience Composer].

   Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde stapsgewijze instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in het dialoogvenster **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Selecteer het gewenste omleidingsaanbod in het menu [!UICONTROL Select Remote Offer] en klikt u vervolgens op **[!UICONTROL Done]**.

1. Voltooi de configuratie van de activiteit.

## Trainingsvideo: Op formulieren gebaseerde composer ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer, waarmee u omleidingsaanbiedingen kunt maken.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
