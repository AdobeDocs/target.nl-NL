---
keywords: remote offer;remote offer selection matrix;cached content;dynamic content
description: Kan ik externe aanbiedingen gebruiken om externe inhoud te hosten?
title: Externe aanbiedingen maken
feature: Experiences and Offers
translation-type: tm+mt
source-git-commit: 67d11820d32bb3518de59801b71df4c0a9485cae
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 0%

---


# Externe aanbiedingen maken

Gebruik externe aanbiedingen om inhoud te hosten buiten [!DNL Adobe Target] die [!DNL Target] verwijzingen en aan de websites van gebruikers levert. Deze inhoud kan zich in een inhoudsbeheer (CMS) of ander systeem bevinden, om redenen van gebruiksgemak of veiligheid.

>[!NOTE]
>
>Externe aanbiedingen kunnen worden gemaakt op de pagina Aanbiedingen > Codeaanbiedingen of in de [Op Forms gebaseerde Experience Composer](/help/c-experiences/form-experience-composer.md). U kunt geen verre aanbiedingen in de Visuele Composer van de Ervaring (VEC) tot stand brengen. De inhoud zal in de [!DNL Target] verzoekplaatsen worden geïnjecteerd, zodat zijn deze hoogstwaarschijnlijk niet aangewezen voor een globaal [!DNL Target] verzoek.
>
>[!DNL Target Classic] meegeleverde vergelijkbare functies:  [!UICONTROL Offer on Your Site] en  [!UICONTROL Offer Outside Test&Target].

Voorbeelden van externe aanbiedingen zijn:

* Verschillende versies van je crosssells
* Dynamische boodschappen in winkelwagentjes
* Forms
* Rekenmachines
* Renteverhoging

## Een externe aanbieding maken op de pagina Codeaanbiedingen

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![Voorstel > Codevoorstellen](/help/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Externe aanbieding maken, dialoogvenster](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de bibliotheek [!UICONTROL Assets].

1. Geef de externe URL voor de externe aanbieding op:

   | Option | Beschrijving |
   |--- |--- |
   | cachegeheugen | De inhoud voor een externe aanbieding in cache wordt aangeboden vanaf [!DNL Target].<br>Om de twee uur  [!DNL Target] haalt u de inhoud op bij de externe URL en slaat u de inhoud vervolgens in  [!DNL Target]. Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, wordt de aanbieding geleverd door [!DNL Target].<br>Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand zich heeft aangemeld om de inhoud  [!DNL Target] niet te kunnen wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden bij het inhoudsbeheer of een ander systeem en de inhoud daar wijzigen.<br>U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst. |
   | Dynamisch | Een dynamische aanbieding op afstand wordt aangeboden door het contentbeheer of een ander systeem in plaats van door [!DNL Target].<br>Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens leveren  [!DNL Target] wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch (of verschillend) voor elke gebruiker kan zijn.<br>Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de accountbalans.<br>Klik  **[!UICONTROL Add Parameter]** om een of meer  [!DNL Target] aanvragen of aanvraagparameters toe te voegen. |

1. Klik op **[!UICONTROL Save]**.

## Een externe aanbieding maken met de Form-Based Experience Composer

1. Selecteer tijdens het maken van een activiteit met de [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) de locatie waar u de **[!UICONTROL Content]**-sectie wilt weergeven.

   ![Sectie Inhoud in Form-Based Experience Composer](/help/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de vervolgkeuzelijst **[!UICONTROL Default Content]** en klik vervolgens op **[!UICONTROL Change Remote Offer]**.

   ![Externe aanbieding wijzigen, optie](/help/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]**.

   ![Externe aanbieding maken, dialoogvenster](/help/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen het aanbod snel vinden in de bibliotheek [!UICONTROL Assets].

1. Geef de externe URL voor de externe aanbieding op:

   | Option | Beschrijving |
   |--- |--- |
   | cachegeheugen | De inhoud voor een externe aanbieding in cache wordt aangeboden vanaf [!DNL Target].<br>Om de twee uur  [!DNL Target] haalt u de inhoud op bij de externe URL en slaat u de inhoud vervolgens in  [!DNL Target]. Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, wordt de aanbieding geleverd door [!DNL Target].<br>Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand zich heeft aangemeld om de inhoud  [!DNL Target] niet te kunnen wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden bij het inhoudsbeheer of een ander systeem en de inhoud daar wijzigen.<br>U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst. |
   | Dynamisch | Een dynamische aanbieding op afstand wordt aangeboden door het contentbeheer of een ander systeem in plaats van door [!DNL Target].<br>Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens leveren  [!DNL Target] wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch (of verschillend) voor elke gebruiker kan zijn.<br>Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de accountbalans.<br>Klik  **[!UICONTROL Add Parameter]** om een of meer  [!DNL Target] aanvragen of aanvraagparameters toe te voegen. |

1. Klik op **[!UICONTROL Save]**.

## Aanbevolen procedures voor het gebruik van externe aanbiedingen {#section_7718512D08E14121B6F6B8C38134F4BC}

Aanbevolen procedures voor het gebruik van externe aanbiedingen in uw activiteiten:

* Als uw aanbieding zich in hetzelfde domein bevindt als de [!DNL Target]-aanvragen, kunt u met de optie [!UICONTROL Cached] relatieve URL&#39;s gebruiken om de locatie van uw aanbieding te beschrijven.

   Dit betekent dat wanneer u uw activiteit van uw testservers naar productie verplaatst, de inhoud automatisch toegankelijk zal zijn zonder het moeten URL manueel veranderen.

* Als uw test gegevens bevat die dynamisch door uw server worden gegenereerd, is de optie [!UICONTROL Dynamic] mogelijk de juiste keuze.
* Als u alleen de weergave van uw bestaande externe aanbiedingsinhoud wilt testen, gebruikt u [!UICONTROL Visual Experience Composer] om de vormgeving van de inhoud die wordt geretourneerd vanuit het inhoudsbeheersysteem te wijzigen.
* Gebruik de Selectiematrix voor externe aanbiedingen (hieronder) om u te helpen het aanbod te kiezen dat het meest geschikt is voor uw specifieke geval. Vraag uw accountvertegenwoordiger.

## Hoe dynamisch externe aanbiedingen werken {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamische externe aanbiedingen gebruiken uw dynamische paginatechnologie om waarden aan de aanbieding door te geven.

De aanbieding wordt uitgevoerd nadat u de pagina teruggeeft. Een onzichtbaar iframe verzamelt de gegevens, kopieert het uit het frame en voegt in op de pagina en laadt de doorgegeven waarden.

![](assets/remote_offer_howitworks_2.jpeg)

## Selectiematrix {#reference_B23BEDD29DDD47709A7651AFD27E776B} op afstand aanbieden

Met de Matrix Selectie voor externe aanbiedingen kunt u bepalen welk type externe aanbieding u wilt kiezen: [!UICONTROL Cached] of [!UICONTROL Dynamic].

| Functie | cachegeheugen | Dynamisch |
|--- |--- |--- |
| Wordt bijgewerkt wanneer een bezoeker een aanvraag indient | Nee | Ja |
| Inhoud bijwerken | Wordt elke 2 uur in de cache geplaatst | Onmiddellijk bijgewerkt na elk verzoek |
| Tijdstip van laden | Sneller | Langzamer vanwege verwerking van aanvragen |
| Kan JavaScript op pagina zien | Ja | Nee, maar kan wel via URL worden doorgegeven |
| Aanbiedingen kunnen JavaScript bevatten | Ja | Ja |
| Aanbiedings-URL | Absoluut of Relatief | Relatief |
| De computer aanvragen | Adobe-servers | De computer van de bezoeker, die de cookies van de bezoeker draagt |