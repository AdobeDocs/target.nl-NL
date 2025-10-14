---
keywords: omleiden aanbieding;aanbieding voor omleiding maken;aanbieding voor HTML toevoegen;Alle URL-parameters doorgeven in omleiding
description: Leer hoe u omleidingsvoorstellen maakt om browsers naadloos naar nieuwe pagina's te leiden.
title: Hoe maak ik omleidingsvoorstellen?
feature: Experiences and Offers
exl-id: b7b960cb-5057-455b-8fab-86dd37343a04
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 0%

---

# Omleidingsvoorstellen maken

Leer hoe u omleidingsvoorstellen maakt om browsers naadloos naar nieuwe pagina&#39;s te leiden.

U hebt misschien twee volledig verschillende pagina&#39;s om te testen in plaats van alleen maar stukken inhoud binnen een pagina te wijzigen. In dit geval vergelijkt uw A/B-test pagina A met pagina B. Stel een [!UICONTROL A/B Test] -activiteit in met twee ervaringen: een die verwijst naar de standaardpagina A en een andere die wordt doorgestuurd naar pagina B. De aanbieding is geconfigureerd om de bezoeker om te leiden naar een andere pagina.

>[!NOTE]
>
> * Omleiden aanbiedingen kunnen op [!UICONTROL Offers] > [!UICONTROL Code Offers] pagina of in [&#x200B; op Forms-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) worden gecreeerd. U kunt geen omleidingsvoorstellen maken of toepassen in [!UICONTROL Visual Experience Composer] (VEC). Inhoud wordt ingespoten op de aanvraaglocaties van [!DNL Target] , zodat deze locaties meestal niet geschikt zijn voor een algemene [!DNL Target] -aanvraag.
>
>* Je kunt geen omleidingsvoorstellen gebruiken in AJAX-vakken (`mboxUpdate`).
>
>* Voor omleidingsaanbiedingen in activiteiten die [[!UICONTROL Analytics as the reporting source]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) gebruiken, moet uw implementatie aan bepaalde minimumvereisten voldoen. Bovendien is er belangrijke informatie die u moet weten. Zie [&#x200B; Vergelijkende Aanbiedingen - Veelgestelde vragen A4T &#x200B;](/help/main/c-integrating-target-with-mac/a4t/r-a4t-faq/a4t-faq-redirect-offers.md#concept_21BF213F10E1414A9DCD4A98AF207905).
>
>* Voor informatie over vestiging een ervaring die opnieuw richt, zie [&#x200B; opnieuw richten aan een URL &#x200B;](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md#task_9578678D42784F5EB9638F8AC8C911FA).

De omleidingsaanbieding voert de code van JavaScript uit om browser om te leiden. De methode `window.location.replace();` wordt gebruikt, zodat de pagina waarvan de bezoeker is omgeleid, niet in de browsergeschiedenis wordt opgeslagen. Met dit proces kunnen bezoekers de knop Vorige in hun browsers gebruiken.

>[!NOTE]
>
>Als u de referentiewaarde van de landingspagina wilt doorgeven, gebruikt u een HTML-aanbieding in plaats van een omleidingsvoorstel.

## Een omleidingsvoorstel maken op de pagina [!UICONTROL Code Offers]

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.
1. Klik op **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]** .
1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Assets] -bibliotheek vinden.

1. (Voorwaardelijk) als u de rekening van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt, selecteer de gewenste [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geef de URL op voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Deze URL moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **[!UICONTROL Include all URL parameters]:** Schakel deze optie in als u wilt dat alle URL-parameters op de vorige pagina worden doorgegeven aan de omgeleide pagina.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u met deze methode kunt bijhouden of personen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen in het vak URL hebt opgegeven `https://www.mycompany.com/mensShirts.html` .

   * **[!UICONTROL Pass mbox session ID]:** vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u wilt dat de `sessionId` automatisch wordt opgenomen in de omleiding. Deze optie is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` komt overeen met het cookie van de bezoeker, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Vraag uw implementatieconsultant voordat u deze tests start.

## Een omleidingsvoorstel maken met de [!UICONTROL Form-Based Experience Composer]

1. Terwijl het creëren van een activiteit die [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) gebruikt, selecteer de plaats om de **[!UICONTROL Content]** sectie te tonen.
1. Klik de **[!UICONTROL Content]** drop-down lijst, klik het **[!UICONTROL List]** pictogram ( ![&#x200B; Lijst &#x200B;](/help/main/assets/icons/MoreSmallList.svg)), dan klik **[!UICONTROL Change Redirect Offer]**.
1. Klik op **[!UICONTROL Create Offer]** > **[!UICONTROL Redirect Offer]** .
1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Assets] -bibliotheek vinden.

1. Geef de URL op voor de unieke inhoud of bestemming waarnaar u wilt omleiden. Deze URL moet een absolute URL zijn.

   >[!NOTE]
   >
   >Aanbiedingen omleiden resulteert in een oneindige lus als de omleidings-URL ook de gebruiker voor dezelfde activiteit kwalificeert. Zorg ervoor dat de gebruiker na omleiding niet opnieuw in aanmerking komt voor de activiteit.

1. Selecteer de gewenste opties om uw omleidingsvoorstel aan te passen:

   * **[!UICONTROL Include all URL parameters]:** schuif de knevel om deze optie toe te laten als u alle parameters URL aanwezig op de vorige pagina aan de opnieuw gerichte pagina wilt worden verspreid.

     U wilt bijvoorbeeld mensen rechtstreeks van een mannenpagina omleiden naar de categoriepagina voor heren. U wilt ook dat de dynamische parameters in de URL worden doorgegeven, omdat u met deze methode kunt bijhouden of personen uw site via e-mail, banneradvertentie, zoekadvertentie of organisch hebben bereikt. Als u deze optie inschakelt, wordt uw omleidingsvoorstel op pagina `https://www.mycompany.com/mens.html?emailId=123` automatisch `https://www.mycompany.com/mensShirts.html?emailId=123` wanneer u alleen in het vak URL hebt opgegeven `https://www.mycompany.com/mensShirts.html` .

   * **[!UICONTROL Pass mbox session ID]:** vereist om naar een ander domein om te leiden. Schuif de schakeloptie om deze optie in te schakelen als u wilt dat de `sessionId` automatisch wordt opgenomen in de omleiding. Deze optie is alleen vereist wanneer u een e-mail test of op een ander domein klikt. De `sessionId` komt overeen met het cookie van de bezoeker, zodat de bezoeker kan blijven worden gevolgd en de juiste inhoud wordt weergegeven.

     Als u de setup van het cookie van de eerste en de derde partij gebruikt, hoeft u de sessie-id van de box niet door te geven wanneer u domeinen overschrijdt. De URL is blijvend in een cookie van een andere fabrikant, dus niet nodig in de URL.

1. Klik op **[!UICONTROL Create]**.

>[!IMPORTANT]
>
>Vraag uw implementatieconsultant voordat u deze tests start.

## Omleidingsvoorstellen gebruiken voor activiteiten

Pas omleidingsvoorstellen toe gebruikend [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md). U kunt momenteel geen omleidingsvoorstellen toepassen met behulp van [!UICONTROL Visual Experience Composer] (VEC).

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests] , [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Recommendations] -activiteiten wanneer [!UICONTROL Visual Experience Composer] niet beschikbaar of praktisch is voor gebruik. U kunt de [!UICONTROL Form-Based Experience Composer] bijvoorbeeld gebruiken om ervaringen te maken die omleidingsaanbiedingen gebruiken.

1. Maak of bewerk een activiteit in de [!UICONTROL Form-Based Experience Composer] .

   Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde geleidelijke instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik de **[!UICONTROL Content]** drop-down lijst, klik het **[!UICONTROL List]** pictogram ( ![&#x200B; Lijst &#x200B;](/help/main/assets/icons/MoreSmallList.svg)), dan klik **[!UICONTROL Change Redirect Offer]**.
1. Selecteer het gewenste omleidingsaanbod in het dialoogvenster [!UICONTROL Select Redirect Offer] en klik op **[!UICONTROL Add]** .
1. Voltooi de configuratie van de activiteit.
