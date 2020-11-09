---
keywords: dedupe;allow duplicates;exclude duplicate offers;automated personalization;disallow duplicate offers
description: Uitsluitingen beheren door uitsluitingsgroepen te maken, met uitzondering van dubbele aanbiedingen, met uitzondering van specifieke ervaringen en met uitzondering van standaardinhoud in Adobe Target Automated Personalization (AP)-activiteiten.
title: Uitsluitingen beheren
feature: ap
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---


# ![Premium badge](/help/assets/premium.png) Uitsluitingen beheren{#manage-exclusions}

Uitsluitingen beheren door uitsluitingsgroepen te maken, met uitzondering van dubbele aanbiedingen, met uitzondering van specifieke ervaringen en met uitzondering van standaardinhoud in Automated Personalization-activiteiten (AP).

## Uitsluitingsgroepen maken {#task_AAAA6C7239A84F7696C8492F04B575A2}

Maak uitsluitingsgroepen in Automated Personalization(AP)-activiteiten om ervoor te zorgen dat ervaringen met de toegewezen aanbiedingen automatisch worden uitgesloten.

Uitsluitingsgroepen zijn een goede manier om ervoor te zorgen dat incompatibele aanbiedingen niet op verschillende plaatsen in dezelfde ervaring worden gepresenteerd. Stel dat u twee aanbiedingen hebt: de ene is voor 20 % van alle goederen en de andere voor 15 % korting . U wilt nooit dat deze twee aanbiedingen aan bezoekers in dezelfde ervaring worden getoond. Als u deze twee aanbiedingen aan een uitsluitingsgroep toevoegt, kunt u ervoor zorgen dat dit nooit het geval zal zijn.

U kunt ook beperken welke doelgroepen specifieke aanbiedingen kunnen zien in AP-activiteiten. Zie [Automated Personalization-aanbiedingen](/help/c-activities/t-automated-personalization/ap-target-offers.md)van Target voor meer informatie.

**Een uitsluitingsgroep maken:**

1. Klik tijdens het [maken of bewerken van een AP-activiteit](/help/c-activities/t-automated-personalization/create-ap-activity.md)op **[!UICONTROL Manage Content]** de kopbalk.

   ![Content-koppeling beheren](/help/c-activities/t-automated-personalization/assets/manage-content.png)

1. Klik in het [!UICONTROL Manage Content] dialoogvenster op **[!UICONTROL Exclusion Group]**.

   ![Inhoud beheren > Dialoogvenster Uitsluitingsgroepen](/help/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Als u eerder uitsluitingsgroepen hebt gemaakt, worden deze weergegeven in de lijst. Als u nog geen uitsluitingsgroep hebt gemaakt, wordt u gevraagd om er een te maken.

1. Klik op **[!UICONTROL Create Exclusion Group.]**

   ![Uitsluitingsgroep maken, dialoogvenster](/help/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Vereist) Geef een beschrijvende naam op voor de uitsluitingsgroep.

   Met een beschrijvende naam kunt u snel het doel van een groep vinden en begrijpen.

1. Zoek en selecteer de gewenste aanbiedingen die u aan de uitsluitingsgroep wilt toevoegen.

   U kunt meerdere voorstellen selecteren op dezelfde locatie in een uitsluitingsgroep.

1. Klik op **[!UICONTROL Save]**.

De aanbiedingen in de uitsluitingsgroep zullen automatisch worden uitgesloten van dezelfde ervaringen die in de toekomst worden opgedaan.

## Dubbele aanbiedingen uitsluiten {#concept_4EF78013F80E48EFA024AE0274C9F037}

Voorkomen dat aanbiedingen uit de aanbiedingsbibliotheek worden gedupliceerd wanneer deze op verschillende locaties in [!UICONTROL Automated Personalization] activiteiten worden gebruikt.

U hebt bijvoorbeeld een activiteit met zes locaties op een pagina met 12 aanbiedingen. Er bestaat een kans dat hetzelfde aanbod op een of meer locaties in de activiteit kan worden geplaatst. Met deze functie voorkomt u dat dubbele aanbiedingen tegelijkertijd worden weergegeven op verschillende locaties binnen dezelfde activiteit.

Klik **[!UICONTROL Configure]** > **[!UICONTROL Duplicate Offers]**, klik dan **[!UICONTROL Allow Duplicates]** of **[!UICONTROL Disallow Duplicates]**.

![Opties voor dubbele aanbiedingen](/help/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Specifieke ervaringen uitsluiten {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Sluit specifieke ervaringen uit als je bepaalde aanbiedingscombinaties wilt uitsluiten van je Automated Personalization-activiteit.

Er zouden bepaalde combinaties kunnen zijn die niet goed samenwerken, of u zou het aantal geteste ervaringen kunnen beperken om verkeersvereisten voor uw activiteit te verminderen.

1. Klik tijdens het [maken of bewerken van een AP-activiteit](/help/c-activities/t-automated-personalization/create-ap-activity.md)op Inhoud **** beheren op de kopbalk.

   ![Content-koppeling beheren](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   In de [!UICONTROL Experiences] lijst ziet u elke ervaring die is gegenereerd op basis van de permutaties van alle opties voor inhoud en locatie.

1. Ervaringen desgewenst uitsluiten.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![Ervaring uitsluiten door aanwijzen](/help/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Of u kunt ervaringen in batch uitsluiten/opnemen door het selectievakje voor de relevante ervaringen in te schakelen en vervolgens op het **[!UICONTROL Exclude]** pictogram in de rechterbovenhoek van het dialoogvenster te klikken. Het [!UICONTROL Exclude] pictogram wordt weergegeven wanneer een of meer ervaringen worden gecontroleerd.

   ![ervaringen uitsluiten](/help/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de [!UICONTROL Status] vervolgkeuzelijst te klikken.

   De ervaringen zullen nu van de activiteit worden uitgesloten en hun [!UICONTROL Status] bereidheid zal blijken [!UICONTROL Excluded].

   ![Uitgesloten ervaringen](/help/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standaardinhoud uitsluiten {#task_DCB4528989DF4C05A3A4729E5891D18F}

In sommige gevallen wilt u wellicht uw standaardinhoud niet opnemen in uw Automated Personalization-activiteit. De manier waarop u deze instelling opent, verschilt van het maken van uitsluitingsgroepen. U kunt deze methode gebruiken om slechts één aanbieding (verschillend van uw standaardinhoud) in een plaats als deel van uw AP activiteit te hebben.

Het uitsluiten van standaardinhoud is een goede manier om de vormgeving van de rest van de pagina aan te passen aan de aanbiedingen die u met uw AP-activiteit test. Stel dat u bijvoorbeeld het kleurenpalet wilt aanpassen van de aanbiedingen die u test, u de achtergrondkleur van de pagina kunt wijzigen en de standaardachtergrondkleur wilt uitsluiten.

**Om standaardinhoud uit te sluiten gebruikend Visual Experience Composer (VEC):**

1. Selecteer tijdens het [maken of bewerken van een AP-activiteit](/help/c-activities/t-automated-personalization/create-ap-activity.md)de inhoud die u wilt vervangen en klik om deze te openen **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]** of **[!UICONTROL Change Background Color]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel de optie **Opnemen** rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video uit in het scherm Inhoud selecteren).

   Afhankelijk van het type inhoud/aanbieding bevindt het [!UICONTROL Include] selectievakje zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![Selectievakje Opnemen in dialoogvenster Tekst bewerken/HTML](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Voor inhoud van afbeelding/video:

   ![Selectievakje Opnemen in dialoogvenster Inhoud selecteren](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Voor achtergrondkleur:

   ![Selectievakje Opnemen in dialoogvenster Achtergrondkleur bewerken](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klik op **[!UICONTROL Save]**.

   Je kunt de ervaringen zien die zijn opgedaan met de aanbiedingen die je onder hebt opgegeven [!UICONTROL Manage Content]. Er zijn geen ervaringen opgedaan bij het [!UICONTROL Manage Content] gebruik van het standaardvoorstel dat u hebt uitgesloten.

   ![](assets/exclude_content_vec_4.png)

**Standaardinhoud uitsluiten met behulp van de Form-Based Experience Composer:**

1. Klik tijdens het maken of bewerken van een AP-activiteit **[!UICONTROL Change Text/HTML]** of **[!UICONTROL Change Image Offer]** onder **[!UICONTROL Content]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel de optie rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video uit in het scherm Inhoud selecteren). **[!UICONTROL Include]**

   Afhankelijk van het type inhoud/aanbieding bevindt het selectievakje Opnemen zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![](assets/exclude_content_form_1.png)

   Voor inhoud van afbeelding/video:

   ![](assets/exclude_content_form_2.png)

1. Klik op **[!UICONTROL Save]**.

   Je kunt de ervaringen zien die zijn opgedaan met de aanbiedingen die je onder hebt opgegeven [!UICONTROL Manage Content]. Er zijn geen ervaringen opgedaan bij het [!UICONTROL Manage Content] gebruik van het standaardvoorstel dat u hebt uitgesloten.

   ![](assets/exclude_content_form_3.png)
