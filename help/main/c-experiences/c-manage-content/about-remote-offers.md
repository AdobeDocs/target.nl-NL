---
keywords: externe aanbieding;inhoud in cache;dynamische inhoud;url-type
description: Ontdek hoe te hefboomwerking verre aanbiedingen in  [!DNL Target]  om externe inhoud van een CMS of andere systemen te ontvangen.
title: Hoe maak ik externe aanbiedingen?
feature: Experiences and Offers
exl-id: 6a5283ee-c1fb-49f7-8e7f-c23ccde26ade
source-git-commit: 856396264c4a7b7e3370cd268e7f010092e2eae2
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 0%

---

# Externe aanbiedingen maken

Gebruik externe aanbiedingen om inhoud buiten [!DNL Adobe Target] te hosten, zodat [!DNL Target] naar deze inhoud kan verwijzen en deze aan gebruikerswebsites kan leveren. Deze inhoud kan om redenen van gebruiksgemak of beveiliging in een inhoudsbeheersysteem (CMS) of een ander systeem worden opgeslagen.

De verre aanbiedingen kunnen op [!UICONTROL Offers] > [!UICONTROL Code Offers] pagina of in [&#x200B; op Forms-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) worden gecreeerd. U kunt geen externe aanbiedingen maken of toepassen in [!UICONTROL Visual Experience Composer] (VEC). Inhoud wordt ingespoten op de aanvraaglocaties van [!DNL Target] , zodat deze locaties meestal niet geschikt zijn voor een algemene [!DNL Target] -aanvraag.

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

* Externe aanbiedingen worden ondersteund in:

   * A/B-activiteiten
   * Experience Targeting (XT)-activiteiten
   * Op formulieren gebaseerde workflows

* Externe aanbiedingen worden niet ondersteund in:

   * [&#x200B; de eigenschappen van de Premie &#x200B;](/help/main/c-intro/intro.md#premium) (Automated Personalization (AP), auto-Doel, en Aanbevelingen)
   * Multivariate Testing (MVT), vanwege de afhankelijkheid van de VEC, die externe aanbiedingen niet ondersteunt.

* Als uw aanbieding zich in hetzelfde domein bevindt als de [!DNL Target] -aanvragen, kunt u met de optie [!UICONTROL Cached] relatieve URL&#39;s gebruiken om de locatie van uw aanbieding te beschrijven.

  Dit betekent dat wanneer u uw activiteit van uw het opvoeren servers aan productie verplaatst, de inhoud automatisch toegankelijk is zonder het moeten URL manueel veranderen.

* Als bij de test gegevens worden gebruikt die dynamisch door de server worden gegenereerd, is de optie [!UICONTROL Dynamic] mogelijk de juiste keuze.
* Als u alleen de weergave van uw bestaande externe aanbiedingsinhoud wilt testen, gebruikt u [!UICONTROL Visual Experience Composer] om de weergave van de inhoud die wordt geretourneerd vanuit het inhoudsbeheersysteem te wijzigen.
* Gebruik de [&#x200B; Verre Matrijs van de Selectie van de Aanbieding &#x200B;](#reference_B23BEDD29DDD47709A7651AFD27E776B) (hieronder) om u te helpen de aanbieding het best geschikt voor uw specifiek geval kiezen. Vraag uw accountvertegenwoordiger.

## Een externe aanbieding maken op de pagina [!UICONTROL Code Offers]

1. Klik op **[!UICONTROL Offers]** en selecteer vervolgens het tabblad **[!UICONTROL Code Offers]**.

1. Klik op **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]** .

1. Geef in het dialoogvenster [!UICONTROL Create Remote Offer] een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Offers] -bibliotheek vinden.

1. (Voorwaardelijk) als u de rekening van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt, selecteer de gewenste [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geef het type omleidings-URL op.

   Zie [&#x200B; Type URL omleiden: [!UICONTROL Onsite Cached] of [!UICONTROL Onsite Dynamic]](#url-type) hieronder voor meer informatie.

1. Geef de absolute externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Create]**.

## Een externe aanbieding maken met de [!UICONTROL Form-Based Experience Composer]

1. Terwijl het creëren van een activiteit die [&#x200B; op vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) gebruikt, selecteer de plaats om de **[!UICONTROL Content]** sectie te tonen.
1. Klik de **[!UICONTROL Content]** drop-down lijst, klik het **[!UICONTROL List]** pictogram ( ![&#x200B; Lijst &#x200B;](/help/main/assets/icons/MoreSmallList.svg)), dan klik **[!UICONTROL Change Remote Offer]**.

1. Klik op **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]** .

1. Geef een beschrijvende naam op voor de aanbieding.

   Met een beschrijvende naam kunnen u en anderen snel de aanbieding in de [!UICONTROL Assets] -bibliotheek vinden.

1. (Voorwaardelijk) als u de rekening van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) hebt, selecteer de gewenste [&#x200B; werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md##section_B82EB409B67C4D9D9D20CE30E48DB1DC).

1. Geef het type omleidings-URL op.

   Zie [&#x200B; Type URL omleiden: [!UICONTROL Onsite Cached] of [!UICONTROL Onsite Dynamic]](#url-type) hieronder voor meer informatie.

1. Geef de externe URL voor de externe aanbieding op.

1. Klik op **[!UICONTROL Create]**.

## Type URL omleiden: [!UICONTROL Onsite Cached] of [!UICONTROL Onsite Dynamic] {#url-type}

Aan de hand van de volgende informatie kunt u de verschillen tussen de twee opties beter begrijpen:

### [!UICONTROL Onsite Cached] URL

De inhoud voor een externe aanbieding in cache wordt aangeboden vanuit [!DNL Target] .

[!DNL Target] haalt de inhoud om de twee uur op bij de externe URL en slaat de inhoud vervolgens op in [!DNL Target] . Wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat, levert [!DNL Target] de aanbieding.

Externe aanbiedingen in cache bieden uitgebreide beveiliging omdat iemand die zich heeft aangemeld bij [!DNL Target] de inhoud niet kan wijzigen. Als u de inhoud wilt wijzigen, moet iemand zich aanmelden bij het inhoudsbeheer of een ander systeem en de inhoud daar wijzigen.

U kunt een absolute of relatieve URL opgeven voor een externe aanbieding die in cache wordt geplaatst.

### [!UICONTROL Onsite Dynamic] URL

Een dynamische aanbieding op afstand wordt aangeboden door het inhoudsbeheer of een ander systeem in plaats van door [!DNL Target] .

Mogelijk wilt u de inhoud niet periodiek in cache plaatsen en vervolgens door [!DNL Target] leveren wanneer bezoekers een site laden met een ervaring die een externe aanbieding bevat. In plaats daarvan, wilt u het systeem roepen dat de inhoud ontvangt, misschien in specifieke informatie overgaan zodat de teruggekeerde aanbieding dynamisch (of verschillend) voor elke gebruiker kan zijn. Als een gebruiker zich bijvoorbeeld bij een website aanmeldt voor een creditcard die een ervaring met een dynamische externe aanbieding bevat, kunt u parameters aan de URL doorgeven voor de accountgegevens van de gebruiker. Vervolgens kan de website gebruikersspecifieke informatie verstrekken, zoals de balans van de account.

U kunt op **[!UICONTROL Add Parameter]** klikken om een of meer [!DNL Target] -aanvragen of aanvraagparameters toe te voegen.

## Externe aanbiedingen gebruiken in activiteiten

Pas externe aanbiedingen toe met behulp van [!UICONTROL Form-Based Experience Composer] . U kunt momenteel geen externe aanbiedingen toepassen met de methode [!UICONTROL Visual Experience Composer] (VEC).

[!DNL Adobe Target] [!UICONTROL Form-Based Experience Composer] is een niet-visuele ervaring en biedt een aanmaakinterface die handig is voor het maken van ervaringen voor gebruik in [!UICONTROL A/B Tests] , [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP) en [!UICONTROL Recommendations] -activiteiten wanneer [!UICONTROL Visual Experience Composer] niet beschikbaar of praktisch is voor gebruik. U kunt de [!UICONTROL Form-Based Experience Composer] bijvoorbeeld gebruiken om ervaringen op te doen die gebruikmaken van externe aanbiedingen.

1. Maak of bewerk een activiteit in de [!UICONTROL Form-Based Experience Composer] .

   Zie [&#x200B; vorm-Gebaseerde Composer van de Ervaring &#x200B;](/help/main/c-experiences/form-experience-composer.md) voor gedetailleerde geleidelijke instructies.

1. Geef de gewenste locatie op en voeg desgewenst verfijningen voor de doelgroep toe.

1. Klik de **[!UICONTROL Content]** drop-down lijst, klik het **[!UICONTROL List]** pictogram ( ![&#x200B; Lijst &#x200B;](/help/main/assets/icons/MoreSmallList.svg)), dan klik **[!UICONTROL Change Remote Offer]**.

1. Selecteer de gewenste aanbieding op afstand in het dialoogvenster [!UICONTROL Change Remote Offer] en klik op **[!UICONTROL Create Offer]** > **[!UICONTROL Remote Offer]** .

1. Voltooi de configuratie van de activiteit.

## Hoe dynamisch externe aanbiedingen werken {#concept_CC2A969420B34364A9FA78C1CE251818}

Dynamische externe aanbiedingen gebruiken uw dynamische paginatechnologie om waarden aan de aanbieding door te geven.

De aanbieding wordt uitgevoerd nadat u de pagina teruggeeft. Een onzichtbare iFrame verzamelt de gegevens, kopieert deze uit het frame en voegt deze op de pagina in en laadt de doorgegeven waarden.

![&#x200B; remote_offer_howitworks_2 beeld &#x200B;](assets/remote_offer_howitworks_2.jpeg)

1. De browser van de bezoeker vraagt om een pagina van uw server.

2. De pagina wordt weergegeven in de browser, inclusief de vakken.

3. De aanroep van `mboxCreate` bevat parameters die nodig zijn om dynamische inhoud te renderen.

4. [!DNL Target] retourneert een URL met de locatie van dynamische inhoud en de bijbehorende parameters. Stelt een iFrame in het mbox-gebied in.

5. De browser vraagt om de URL en geeft deze op de pagina weer.

## Selectiematrix voor externe aanbiedingen {#reference_B23BEDD29DDD47709A7651AFD27E776B}

Met de selectiematrix voor externe aanbiedingen kunt u bepalen welk type externe aanbieding u wilt kiezen: [!UICONTROL Onsite Cached] of [!UICONTROL Onsite Dynamic] .

| Functie | Onsite caching | Onsite dynamisch |
|--- |--- |--- |
| Wordt bijgewerkt wanneer een bezoeker een aanvraag indient | Nee | Ja |
| Inhoud bijwerken | Wordt elke twee uur in de cache geplaatst | Onmiddellijk bijgewerkt na elk verzoek |
| Tijd laden | Sneller | Langzamer vanwege verwerking van aanvragen |
| Kan JavaScript op pagina zien | Ja | Nee, maar kan wel via URL worden doorgegeven |
| Aanbiedingen kunnen JavaScript bevatten | Ja | Ja |
| Aanbiedings-URL | Absoluut of Relatief | Relatief |
| De computer aanvragen | Adobe-servers | De computer van de bezoeker, die de cookies van de bezoeker draagt |
