---
keywords: externe aanbieding;inhoud in cache;dynamische inhoud;url-type
description: Leer hoe u externe aanbiedingen kunt gebruiken in [!DNL Target] om externe inhoud te hosten (inhoud in een CMS of een ander systeem).
title: Hoe maak ik externe aanbiedingen?
feature: Experiences and Offers
badgeBeta: label="Beta" type="Informative" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html#beta newtab=true" tooltip="Wat zijn bètafuncties in [!DNL Adobe Target]."
hide: true
hidefromtoc: true
source-git-commit: 26cb9d6a2359714f41acaf91c6e26a7e0ac93238
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Externe aanbiedingen maken

Externe aanbiedingen gebruiken om inhoud buiten [!DNL Adobe Target] dat [!DNL Target] verwijzingen en aanbiedingen naar websites van gebruikers. Deze inhoud kan zich in een inhoudsbeheer (CMS) of ander systeem bevinden, om redenen van gebruiksgemak of veiligheid.

>[!NOTE]
>
>Dit artikel bevat informatie over updates van de [!DNL Target] gebruikersinterface die momenteel deel uitmaakt van een bètaprogramma. De [!DNL Adobe Target] team laat vaak nieuwe eigenschappen voor bepaalde klanten voor het testen en terugkoppelen doeleinden toe. Nadat de testperiode is voltooid, worden deze functies in de toekomst voor alle klanten ingeschakeld [!DNL Target Standard/Premium] releases en aankondigingen in de releaseopmerkingen.

Externe aanbiedingen kunnen op de [!UICONTROL Offers] > [!UICONTROL Code Offers] of in de [Op Forms gebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md). U kunt geen externe aanbiedingen maken of toepassen in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC). Inhoud wordt geïnjecteerd in de [!DNL Target] verzoek plaatsen, zodat zijn deze plaatsen zeer waarschijnlijk niet aangewezen voor een globaal [!DNL Target] verzoek.

Voorbeelden van externe aanbiedingen zijn:

* Verschillende versies van je crosssells
* Dynamische boodschappen in winkelwagentjes
* Forms
* Rekenmachines
* Renteverhoging
* E-mails
* Kiosks
* Spraakassistenten

## Aanbevolen procedures voor het gebruik van externe aanbiedingen {#section_7718512D08E14121B6F6B8C38134F4BC}

Aanbevolen procedures voor het gebruik van externe aanbiedingen in uw activiteiten:

* Als uw voorstel zich in het zelfde domein zoals bevindt [!DNL Target] aanvragen, met de [!UICONTROL Cached] Met deze optie kunt u relatieve URL&#39;s gebruiken om de locatie van uw aanbieding te beschrijven.

  Dit betekent dat wanneer u uw activiteit van uw het opvoeren servers aan productie verplaatst, de inhoud automatisch toegankelijk is zonder het moeten URL manueel veranderen.

* Als de test gegevens bevat die dynamisch door de server worden gegenereerd, wordt [!UICONTROL Dynamic] de juiste keuze is.
* Als u alleen de weergave van uw bestaande externe aanbiedingsinhoud wilt testen, gebruikt u de optie [!UICONTROL Visual Experience Composer] om het uiterlijk te wijzigen van de inhoud die wordt geretourneerd van het contentbeheersysteem.
* Gebruik de [Selectiematrix voor externe aanbieding](#reference_B23BEDD29DDD47709A7651AFD27E776B) (hieronder) om je te helpen het voorstel te kiezen dat het meest geschikt is voor je specifieke kwestie. Vraag uw accountvertegenwoordiger.

## Maak een externe aanbieding van de [!UICONTROL Code Offers] page

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![Voorstel > Codevoorstellen](/help/main/c-experiences/c-manage-content/assets/offers-code-offers-new.png)

1. Klikken **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]**.

   ![Externe aanbieding maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui_new.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in het dialoogvenster [!UICONTROL Assets] bibliotheek.

1. (Voorwaardelijk) Als u een [Target Premium-account](/help/main/c-intro/intro.md#premium)selecteert u de gewenste [werkruimte](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geef het type omleidings-URL op.

   Zie [Type URL omleiden: in cache geplaatst of dynamisch](#url-type) hieronder voor meer informatie .

1. Geef de absolute externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Create]**.

## Een externe aanbieding maken met de [!UICONTROL Form-Based Experience Composer]

1. Tijdens het maken van een activiteit met de [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md)selecteert u de locatie waar u de **[!UICONTROL Content]** sectie.

   ![Sectie Inhoud in Form-Based Experience Composer](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de knop **[!UICONTROL Default Content]** vervolgkeuzelijst en vervolgens op **[!UICONTROL Change Remote Offer]**.

   ![Externe aanbieding wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klikken **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Externe aanbieding maken, dialoogvenster](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in het dialoogvenster [!UICONTROL Assets] bibliotheek.

1. Geef het type omleidings-URL op.

   Zie [Type URL omleiden: in cache geplaatst of dynamisch](#url-type) hieronder voor meer informatie .

1. Geef de externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Save]**.

## Type URL omleiden: in cache geplaatst of dynamisch {#url-type}

Aan de hand van de volgende informatie kunt u de verschillen tussen de twee opties beter begrijpen:

### URL in cache

De inhoud voor een aanbieding op afstand in de cache wordt aangeboden vanaf [!DNL Target].

Om de twee uur, [!DNL Target] haalt de inhoud bij externe URL op en slaat de inhoud vervolgens in [!DNL Target]. Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, [!DNL Target] levert het voorstel.

Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand zich heeft aangemeld bij [!DNL Target] kan de inhoud niet wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden of een ander systeem en de inhoud daar wijzigen.

U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst.

### Dynamische URL

Een dynamische aanbieding op afstand wordt aangeboden via het contentbeheer of een ander systeem in plaats van via [!DNL Target].

Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens leveren via [!DNL Target] wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch (of verschillend) voor elke gebruiker kan zijn. Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de balans van de account.

U kunt op **[!UICONTROL Add Parameter]** om een of meer [!DNL Target] aanvragen of parameters aanvragen.

## Externe aanbiedingen gebruiken in activiteiten

U moet externe aanbiedingen toepassen met de [!UICONTROL Form-Based Experience Composer]. U kunt momenteel geen externe aanbiedingen toepassen met de [!UICONTROL Visual Experience Composer] (VEC).

De [!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Recommendations] wanneer de [!UICONTROL Visual Experience Composer] niet beschikbaar of praktisch is voor gebruik. U kunt bijvoorbeeld de opdracht [!UICONTROL Form-Based Experience Composer] om ervaringen te creëren die verre aanbiedingen gebruiken.

1. Een activiteit maken of bewerken in het dialoogvenster [!UICONTROL Form-Based Experience Composer].

   Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde stapsgewijze instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in het dialoogvenster **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Remote Offer]**.

   ![Externe aanbieding wijzigen, optie](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Selecteer de gewenste aanbieding op afstand in het menu [!UICONTROL Select Remote Offer] en klikt u vervolgens op **[!UICONTROL Done]**.

1. Voltooi de configuratie van de activiteit.

## Hoe dynamisch externe aanbiedingen werken {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamische externe aanbiedingen gebruiken uw dynamische paginatechnologie om waarden aan de aanbieding door te geven.

De aanbieding wordt uitgevoerd nadat u de pagina teruggeeft. Een onzichtbare iFrame verzamelt de gegevens, kopieert deze uit het frame en voegt deze op de pagina in en laadt de doorgegeven waarden.

![image remote_offer_howitworks_2](assets/remote_offer_howitworks_2.jpeg)

1. De browser van de bezoeker vraagt een pagina van uw server.

2. De pagina wordt weergegeven in de browser, inclusief de vakken.

3. `mboxCreate` de vraag omvat parameters noodzakelijk om dynamische inhoud terug te geven.

4. [!DNL Target] retourneert URL met locatie van dynamische inhoud en de bijbehorende parameters. Hiermee wordt een iFrame in het mbox-gebied ingesteld.

5. Browser vraagt URL en geeft op pagina terug.

## Selectiematrix voor externe aanbiedingen {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Met de Matrix Selectie voor externe aanbiedingen kunt u bepalen welk type externe aanbieding u wilt kiezen: [!UICONTROL Cached] of [!UICONTROL Dynamic].

| Functie | cachegeheugen | Dynamisch |
|--- |--- |--- |
| Wordt bijgewerkt wanneer een bezoeker een aanvraag indient | Nee | Ja |
| Inhoud bijwerken | Wordt elke twee uur in de cache geplaatst | Onmiddellijk bijgewerkt na elk verzoek |
| Tijd laden | Sneller | Langzamer vanwege verwerking van aanvragen |
| Kan JavaScript op pagina zien | Ja | Nee, maar kan wel via URL worden doorgegeven |
| Aanbiedingen kunnen JavaScript bevatten | Ja | Ja |
| Aanbiedings-URL | Absoluut of Relatief | Relatief |
| De computer aanvragen | Adobe-servers | De computer van de bezoeker, die de cookies van de bezoeker draagt |

## Trainingsvideo: Op formulieren gebaseerde composer ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat een demo van de [!UICONTROL Form-Based Experience Composer], waarmee u externe aanbiedingen kunt maken.

* Een activiteit maken met de [!UICONTROL Form-Based Experience Composer]
* Begrijpen wanneer [!UICONTROL Form-Based Experience Composer] vs. de [!UICONTROL Visual Experience Composer]
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)