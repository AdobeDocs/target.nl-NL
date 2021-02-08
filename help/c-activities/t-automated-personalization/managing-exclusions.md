---
keywords: dedupe;allow duplicates;exclude duplicate aanbiedingen;automatiseerd personalisatie;disallow duplicate aanbiedingen;exclude;default content;exclusion group;
description: Uitsluitingen beheren in Adobe Target Automated Personalization (AP)-activiteiten. Maak uitsluitingsgroepen en sluit dubbele aanbiedingen, specifieke ervaringen en standaardinhoud uit.
title: Hoe kan ik uitsluitingen in Automated Personalization-activiteiten beheren?
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 0%

---


# ![Premium-](/help/assets/premium.png) badgeUitsluitingen beheren

Uitsluitingen beheren door uitsluitingsgroepen te maken, met uitzondering van dubbele aanbiedingen, met uitzondering van specifieke ervaringen, en standaardinhoud in [!UICONTROL Automated Personalization] (AP)-activiteiten in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP)-activiteiten uitsluiten.

## Uitsluitingsgroepen {#task_AAAA6C7239A84F7696C8492F04B575A2} maken

Maak uitsluitingsgroepen in Automated Personalization(AP)-activiteiten om ervoor te zorgen dat ervaringen met de toegewezen aanbiedingen automatisch worden uitgesloten.

Uitsluitingsgroepen zijn een goede manier om ervoor te zorgen dat incompatibele aanbiedingen niet op verschillende plaatsen in dezelfde ervaring worden gepresenteerd. Stel dat u twee aanbiedingen hebt: de ene is voor 20 % van alle goederen en de andere voor 15 % korting . U wilt nooit dat deze twee aanbiedingen aan bezoekers in dezelfde ervaring worden getoond. Als u deze twee aanbiedingen aan een uitsluitingsgroep toevoegt, kunt u ervoor zorgen dat dit nooit het geval zal zijn.

U kunt ook beperken welke doelgroepen specifieke aanbiedingen kunnen zien in AP-activiteiten. Zie [Automated Personalization-doelaanbiedingen](/help/c-activities/t-automated-personalization/ap-target-offers.md) voor meer informatie.

**Een uitsluitingsgroep maken:**

1. Terwijl [een AP-activiteit maken of bewerken](/help/c-activities/t-automated-personalization/create-ap-activity.md), klikt u op **[!UICONTROL Manage Content]** in de koptekstbalk.

   ![Content-koppeling beheren](/help/c-activities/t-automated-personalization/assets/manage-content.png)

1. Klik in het dialoogvenster [!UICONTROL Manage Content] op **[!UICONTROL Exclusion Group]**.

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

## Dubbele aanbiedingen {#concept_4EF78013F80E48EFA024AE0274C9F037} uitsluiten

Voorkomen dat aanbiedingen uit de aanbiedingsbibliotheek worden gedupliceerd wanneer deze op verschillende locaties in [!UICONTROL Automated Personalization]-activiteiten worden gebruikt.

U hebt bijvoorbeeld een activiteit met zes locaties op een pagina met 12 aanbiedingen. Er bestaat een kans dat hetzelfde aanbod op een of meer locaties in de activiteit kan worden geplaatst. Met deze functie voorkomt u dat dubbele aanbiedingen tegelijkertijd worden weergegeven op verschillende locaties binnen dezelfde activiteit.

Klik **[!UICONTROL Configure]** > **[!UICONTROL Duplicate Offers]**, dan klik **[!UICONTROL Allow Duplicates]** of **[!UICONTROL Disallow Duplicates]**.

![Opties voor dubbele aanbiedingen](/help/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Specifieke ervaringen {#task_C17D36EF58AF4908B17A3D84CA6DE85A} uitsluiten

Sluit specifieke ervaringen uit als je bepaalde aanbiedingscombinaties wilt uitsluiten van je Automated Personalization-activiteit.

Er zouden bepaalde combinaties kunnen zijn die niet goed samenwerken, of u zou het aantal geteste ervaringen kunnen beperken om verkeersvereisten voor uw activiteit te verminderen.

1. Terwijl [een AP-activiteit maken of bewerken](/help/c-activities/t-automated-personalization/create-ap-activity.md), klikt u **Inhoud beheren** in de koptekstbalk.

   ![Content-koppeling beheren](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   In de lijst [!UICONTROL Experiences] wordt elke ervaring weergegeven die is gegenereerd op basis van de permutaties van alle opties voor inhoud en locatie.

1. Ervaringen desgewenst uitsluiten.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![Ervaring uitsluiten door aanwijzen](/help/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Of u kunt ervaringen in batch uitsluiten/opnemen door het selectievakje voor de relevante ervaringen in te schakelen en vervolgens op het pictogram **[!UICONTROL Exclude]** in de rechterbovenhoek van het dialoogvenster te klikken. Het pictogram [!UICONTROL Exclude] wordt weergegeven wanneer een of meer ervaringen worden gecontroleerd.

   ![ervaringen uitsluiten](/help/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de vervolgkeuzelijst [!UICONTROL Status] te klikken.

   De ervaringen worden nu uitgesloten van de activiteit en hun [!UICONTROL Status] wordt weergegeven als [!UICONTROL Excluded].

   ![Uitgesloten ervaringen](/help/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standaardinhoud {#task_DCB4528989DF4C05A3A4729E5891D18F} uitsluiten

In sommige gevallen wilt u wellicht uw standaardinhoud niet opnemen in uw Automated Personalization-activiteit. De manier waarop u deze instelling opent, verschilt van het maken van uitsluitingsgroepen. U kunt deze methode gebruiken om slechts één aanbieding (verschillend van uw standaardinhoud) in een plaats als deel van uw AP activiteit te hebben.

Het uitsluiten van standaardinhoud is een goede manier om de vormgeving van de rest van de pagina aan te passen aan de aanbiedingen die u met uw AP-activiteit test. Stel dat u bijvoorbeeld het kleurenpalet wilt aanpassen van de aanbiedingen die u test, u de achtergrondkleur van de pagina kunt wijzigen en de standaardachtergrondkleur wilt uitsluiten.

**Om standaardinhoud uit te sluiten gebruikend Visual Experience Composer (VEC):**

1. Terwijl [een AP-activiteit maken of bewerken](/help/c-activities/t-automated-personalization/create-ap-activity.md), selecteert u de inhoud die u wilt vervangen en klikt u om toegang te krijgen tot **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]** of **[!UICONTROL Change Background Color]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel **Include** rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video in het scherm Inhoud selecteren uit).

   Afhankelijk van het type inhoud/aanbieding bevindt het selectievakje [!UICONTROL Include] zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![Selectievakje Opnemen in dialoogvenster Tekst bewerken/HTML](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Voor inhoud van afbeelding/video:

   ![Selectievakje Opnemen in dialoogvenster Inhoud selecteren](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Voor achtergrondkleur:

   ![Selectievakje Opnemen in dialoogvenster Achtergrondkleur bewerken](/help/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. Er worden geen ervaringen gemaakt in [!UICONTROL Manage Content] met de standaardaanbieding die u hebt uitgesloten.

   ![](assets/exclude_content_vec_4.png)

**Standaardinhoud uitsluiten met behulp van de Form-Based Experience Composer:**

1. Klik tijdens het maken of bewerken van een AP-activiteit op **[!UICONTROL Change Text/HTML]** of **[!UICONTROL Change Image Offer]** onder **[!UICONTROL Content]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel **[!UICONTROL Include]** rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video uit in het scherm Inhoud selecteren).

   Afhankelijk van het type inhoud/aanbieding bevindt het selectievakje Opnemen zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![](assets/exclude_content_form_1.png)

   Voor inhoud van afbeelding/video:

   ![](assets/exclude_content_form_2.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. Er worden geen ervaringen gemaakt in [!UICONTROL Manage Content] met de standaardaanbieding die u hebt uitgesloten.

   ![](assets/exclude_content_form_3.png)
