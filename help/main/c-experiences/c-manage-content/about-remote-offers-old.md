---
keywords: externe aanbieding;externe aanbiedingsselectiematrix;inhoud in cache;dynamische inhoud;url-type
description: Leer hoe te om verre aanbiedingen in Adobe  [!DNL Target]  te gebruiken om buiten inhoud (inhoud in een CMS of ander systeem) te ontvangen. Ontdek waarom u externe aanbiedingen zou kunnen willen gebruiken.
title: Hoe maak ik externe aanbiedingen?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: e8201198dc6ac36e803153d5c6b345a30716204a
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# Externe aanbiedingen maken

Gebruik externe aanbiedingen om inhoud te hosten buiten [!DNL Adobe Target] dat [!DNL Target] verwijst naar en levert aan websites van gebruikers. Deze inhoud kan zich in een inhoudsbeheer (CMS) of ander systeem bevinden, om redenen van gebruiksgemak of beveiliging.

>[!NOTE]
>
>De verre aanbiedingen kunnen op [!UICONTROL Offers] > [!UICONTROL Code Offers] pagina of in [&#x200B; op Forms-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) worden gecreeerd. U kunt geen verre aanbiedingen in de Visuele Composer van de Ervaring (VEC) tot stand brengen of toepassen. Inhoud wordt ingespoten op de aanvraaglocaties van [!DNL Target] , zodat deze niet geschikt zijn voor een algemene [!DNL Target] -aanvraag.
>
>[!DNL Target Classic] bevat vergelijkbare functies: [!UICONTROL Offer on Your Site] en [!UICONTROL Offer Outside Test&Target] .

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

* Als uw aanbieding zich in hetzelfde domein bevindt als de [!DNL Target] -aanvragen, kunt u met de optie [!UICONTROL Cached] relatieve URL&#39;s gebruiken om de locatie van uw aanbieding te beschrijven.

  Dit betekent dat wanneer u uw activiteit van uw testservers naar productie verplaatst, de inhoud automatisch toegankelijk zal zijn zonder het moeten URL manueel veranderen.

* Als bij de test gegevens worden gebruikt die dynamisch door de server worden gegenereerd, is de optie [!UICONTROL Dynamic] mogelijk de juiste keuze.
* Als u alleen de weergave van uw bestaande externe aanbiedingsinhoud wilt testen, gebruikt u [!UICONTROL Visual Experience Composer] om de weergave van de inhoud die wordt geretourneerd vanuit het inhoudsbeheersysteem te wijzigen.
* Gebruik de [&#x200B; Verre Matrijs van de Selectie van de Aanbieding &#x200B;](#reference_B23BEDD29DDD47709A7651AFD27E776B) (hieronder) om u te helpen de aanbieding het best geschikt voor uw specifiek geval kiezen. Vraag uw accountvertegenwoordiger.

## Een externe aanbieding maken op de pagina Codeaanbiedingen

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

   ![&#x200B; Aanbiedingen > de Aanbiedingen van de Code &#x200B;](/help/main/c-experiences/c-manage-content/assets/offers-code-offers.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]** .

   ![&#x200B; creeer Verre de dialoogdoos van de Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Assets] -bibliotheek vinden.

1. Geef het type Redirect URL op.

   Zie [&#x200B; Redirect URL Type: In cache geplaatst of Dynamisch &#x200B;](#url-type) hieronder voor meer informatie.

1. Geef de externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Save]**.

## Een externe aanbieding maken met de Form-Based Experience Composer

1. Terwijl het creëren van een activiteit die [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) gebruikt, selecteer de plaats om de **[!UICONTROL Content]** sectie te tonen.

   ![&#x200B; sectie van de Inhoud in vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-manage-content/assets/form-based-content.png)

1. Klik op de vervolgkeuzelijst **[!UICONTROL Default Content]** en klik vervolgens op **[!UICONTROL Change Remote Offer]** .

   ![&#x200B; de Verre optie van de Aanbieding van de Verandering &#x200B;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Klik op **[!UICONTROL Create]** > **[!UICONTROL Remote Offer]** .

   ![&#x200B; creeer Verre de dialoogdoos van de Aanbieding &#x200B;](/help/main/c-experiences/c-manage-content/assets/remote_offer_ui.png)

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Assets] -bibliotheek vinden.

1. Geef het type Redirect URL op.

   Zie [&#x200B; Redirect URL Type: In cache geplaatst of Dynamisch &#x200B;](#url-type) hieronder voor meer informatie.

1. Geef de externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Save]**.

## Type URL omleiden: in cache geplaatst of dynamisch {#url-type}

Aan de hand van de volgende informatie kunt u de verschillen tussen de twee opties beter begrijpen:

### URL in cache

De inhoud voor een externe aanbieding in cache wordt aangeboden vanuit [!DNL Target] .

[!DNL Target] haalt de inhoud om de twee uur op bij de externe URL en slaat de inhoud vervolgens op in [!DNL Target] . Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, wordt de aanbieding geleverd door [!DNL Target] .

Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand die zich heeft aangemeld bij [!DNL Target] de inhoud niet kan wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden bij het inhoudsbeheer of een ander systeem en de inhoud daar wijzigen.

U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst.

### Dynamische URL

Een dynamische aanbieding op afstand wordt aangeboden door het inhoudsbeheer of een ander systeem in plaats van door [!DNL Target] .

Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens door [!DNL Target] leveren wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch (of verschillend) voor elke gebruiker kan zijn. Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de balans van de account.

U kunt op **[!UICONTROL Add Parameter]** klikken om een of meer [!DNL Target] -aanvragen of aanvraagparameters toe te voegen.

## Externe aanbiedingen gebruiken in activiteiten

U moet externe aanbiedingen toepassen met de [!UICONTROL Form-Based Experience Composer] . U kunt momenteel geen verre voorstellen toepassen gebruikend VEC.

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests] -, [!UICONTROL Experience Targeting] (XT) - [!UICONTROL Automated Personalization] - (AP) - en [!UICONTROL Recommendations] -activiteiten wanneer de composer voor visuele beleving niet beschikbaar of praktisch is voor gebruik. U kunt de [!UICONTROL Form-Based Experience Composer] bijvoorbeeld gebruiken om ervaringen op te doen die gebruikmaken van externe aanbiedingen.

1. Maak of bewerk een activiteit in de [!UICONTROL Form-Based Experience Composer] .

   Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde geleidelijke instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik op de vervolgkeuzelijst in de sectie **[!UICONTROL Content]** en klik vervolgens op **[!UICONTROL Change Remote Offer]** .

   ![&#x200B; de Verre optie van de Aanbieding van de Verandering &#x200B;](/help/main/c-experiences/c-manage-content/assets/change-remote-offer.png)

1. Selecteer de gewenste aanbieding op afstand in het dialoogvenster [!UICONTROL Select Remote Offer] en klik op **[!UICONTROL Done]** .

1. Voltooi de configuratie van de activiteit.

## Hoe dynamisch externe aanbiedingen werken {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamische externe aanbiedingen gebruiken uw dynamische paginatechnologie om waarden aan de aanbieding door te geven.

De aanbieding wordt uitgevoerd nadat u de pagina teruggeeft. Een onzichtbaar iframe verzamelt de gegevens, kopieert het uit het frame en voegt in op de pagina en laadt de doorgegeven waarden.

![&#x200B; remote_offer_howitworks_2 beeld &#x200B;](assets/remote_offer_howitworks_2.jpeg)

## Selectiematrix voor externe aanbiedingen {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Met de selectiematrix voor externe aanbiedingen kunt u bepalen welk type externe aanbieding u wilt kiezen: [!UICONTROL Cached] of [!UICONTROL Dynamic] .

| Functie | cachegeheugen | Dynamisch |
|--- |--- |--- |
| Wordt bijgewerkt wanneer een bezoeker een aanvraag indient | Nee | Ja |
| Inhoud bijwerken | Wordt elke 2 uur in de cache geplaatst | Onmiddellijk bijgewerkt na elk verzoek |
| Tijd laden | Sneller | Langzamer vanwege verwerking van aanvragen |
| Kan JavaScript op pagina zien | Ja | Nee, maar kan wel via URL worden doorgegeven |
| Aanbiedingen kunnen JavaScript bevatten | Ja | Ja |
| Aanbiedings-URL | Absoluut of Relatief | Relatief |
| De computer aanvragen | Adobe-servers | De computer van de bezoeker, die de cookies van de bezoeker draagt |

## De video van de opleiding: Op vorm-Gebaseerde Composer ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat een demo van de op formulieren gebaseerde composer, waarmee u externe aanbiedingen kunt maken.

* Een activiteit maken met de Form-Based Experience Composer
* Begrijp wanneer om vorm-Gebaseerde Composer van de Ervaring tegenover Visual Experience Composer te gebruiken
* Verfijningen gebruiken om een locatie als doel in te stellen

>[!VIDEO](https://video.tv.adobe.com/v/17390)
