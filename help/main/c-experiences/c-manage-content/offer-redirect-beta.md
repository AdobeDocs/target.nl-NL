---
keywords: omleidingsaanbod;maak omleidingsaanbod;voeg html-aanbieding toe;geef alle URL-parameters door in omleiding;geef mboxSessionId door in omleiding (alleen nodig wanneer de omleiding naar een ander domein gaat)
description: Meer informatie over het maken van omleidingsvoorstellen in [!DNL Target] om ervoor te zorgen dat een browser omleidt naar een nieuwe pagina.
title: Hoe maak ik omleidingsvoorstellen?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: 3fe1094ff5a2610207034c38d749ae031e7b8caf
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 0%

---

# Omleidingsvoorstellen maken

Omleidingsvoorstellen maken in [!DNL Adobe Target] om ervoor te zorgen dat een browser omleidt naar een nieuwe pagina.

>[!NOTE]
>
>Dit artikel bevat informatie over updates van de [!DNL Target] gebruikersinterface die momenteel deel uitmaakt van een bètaprogramma. De [!DNL Adobe Target] team laat vaak nieuwe eigenschappen voor bepaalde klanten voor het testen en terugkoppelen doeleinden toe. Nadat de testperiode is voltooid, worden deze functies in de toekomst voor alle klanten ingeschakeld [!DNL Target Standard/Premium] releases en aankondigingen in de releaseopmerkingen.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Opstelling en [!UICONTROL A/B Test] activiteit met twee ervaringen: één die aan standaardpagina A richten, en andere die aan pagina B opnieuw richten. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
> * Aanbiedingen voor omleiding kunnen worden gemaakt op de [!UICONTROL Offers] > [!UICONTROL Code Offers] of in de [Op Forms gebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md). U kunt geen omleidingsvoorstellen maken of toepassen in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC). Inhoud wordt geïnjecteerd in de [!DNL Target] verzoek plaatsen, zodat zijn deze plaatsen zeer waarschijnlijk niet aangewezen voor een globaal [!DNL Target] verzoek.
>
>* Je kunt geen omleidingsvoorstellen gebruiken in AJAX (`mboxUpdate`).
>
>* Voor omleidingsaanbiedingen in activiteiten die Analytics als rapporteringsbron (A4T) gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie voor meer informatie [Omleidingsvoorstellen - Veelgestelde vragen A4T](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Voor informatie over vestiging een ervaring die omleidt, zie [Omleiden naar een URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

De omleidingsaanbieding voert code JavaScript uit om browser om te leiden. Het gebruikt de `window.location.replace();` methode, zodat de pagina waarvan de bezoeker wordt omgeleid niet in de browsergeschiedenis wordt opgeslagen. Met dit proces kunnen bezoekers de knop Vorige in hun browsers gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, gebruikt u een HTML-aanbieding in plaats van een omleidingsvoorstel.

## Een omleidingsvoorstel maken van de [!UICONTROL Code Offers] page

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![Tabblad Codeaanbiedingen](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. Klikken **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer-new.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in het dialoogvenster [!UICONTROL Assets] bibliotheek.

1. (Voorwaardelijk) Als u een [Target Premium-account](/help/main/c-intro/intro.md#premium)selecteert u de gewenste [werkruimte](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geef de URL op voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Deze URL moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Door deze optie in te schakelen, kunt u het omleidingsvoorstel op de pagina uitvoeren `https://www.mycompany.com/mens.html?emailId=123` automatisch wordt `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer alles wat u hebt ingevoerd in het vak URL was `https://www.mycompany.com/mensShirts.html`.

   * **ID van wachtwoordsessie doorgeven:** Vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u de optie `sessionId` automatisch in de omleiding worden opgenomen. Deze optie is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden bijgehouden en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Create]**.

>[!NOTE]
>
>Vraag uw Implementatie-consultant voordat u deze tests start.

## Een omleidingsvoorstel maken met de [!UICONTROL Form-Based Experience Composer]

1. Tijdens het maken van een activiteit met de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md)selecteert u de locatie waar u de **[!UICONTROL Content]** sectie.

   ![Sectie Inhoud in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de knop **[!UICONTROL Default Content]** vervolgkeuzelijst en vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option.png)

1. Klikken **[!UICONTROL Create]** > **[!UICONTROL Redirect Offer]**.

   ![Omleidingsvoorstel maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/create-redirect-offer.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in het dialoogvenster [!UICONTROL Assets] bibliotheek.

1. Geef de URL op voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Deze URL moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **Alle URL-parameters opnemen:** Schuif de schakeloptie om deze optie in te schakelen als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u op deze manier bijhoudt of mensen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Door deze optie in te schakelen, kunt u het omleidingsvoorstel op de pagina uitvoeren `https://www.mycompany.com/mens.html?emailId=123` automatisch wordt `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer alles wat u hebt ingevoerd in het vak URL was `https://www.mycompany.com/mensShirts.html`.

   * **ID van wachtwoordsessie doorgeven:** Vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u de optie `sessionId` automatisch in de omleiding worden opgenomen. Deze optie is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` past het cookie van de bezoeker aan, zodat de bezoeker kan blijven worden bijgehouden en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Vraag uw Implementatie-consultant voordat u deze tests start.

## Omleidingsvoorstellen gebruiken voor activiteiten

Je moet omleidingsvoorstellen toepassen met de [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). Je kunt momenteel geen omleidingsvoorstellen toepassen met de [!UICONTROL Visual Experience Composer] (VEC).

De [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Recommendations] activiteiten wanneer de composer voor visuele ervaring niet beschikbaar of praktisch voor gebruik is. U kunt bijvoorbeeld de opdracht [!UICONTROL Form-Based Experience Composer] om ervaringen te creëren die omleidingsaanbiedingen gebruiken.

1. Een activiteit maken of bewerken in het dialoogvenster [!UICONTROL Form-Based Experience Composer].

   Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde stapsgewijze instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in het dialoogvenster **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Redirect Offer]**.

   ![Omleidingsvoorstel wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-redirect-offer-option2.png)

1. Selecteer het gewenste omleidingsvoorstel van [!UICONTROL Select Remote Offer] en klikt u vervolgens op **[!UICONTROL Done]**.

1. Voltooi de configuratie van de activiteit.

## Trainingsvideo: Op formulieren gebaseerde composer ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat een demo van de [!UICONTROL Form-Based Experience Composer], waarmee je omleidingsvoorstellen kunt maken.

* Een activiteit maken met de [!UICONTROL Form-Based Experience Composer]
* Begrijp wanneer u de [!UICONTROL Form-Based Experience Composer] vs. de [!UICONTROL Visual Experience Composer]
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)