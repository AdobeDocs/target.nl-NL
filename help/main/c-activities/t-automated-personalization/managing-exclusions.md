---
keywords: dedupe;allow duplicates;exclude duplicate aanbiedingen;automatiseerd personalisatie;disallow duplicate aanbiedingen;exclude;default content;exclusion group;
description: Uitsluitingen beheren in [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP) activiteiten. Maak uitsluitingsgroepen en sluit dubbele aanbiedingen, specifieke ervaringen en standaardinhoud uit.
title: Hoe kan ik uitsluitingen beheren in [!UICONTROL Automated Personalization] Activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: b5f06878a6ca8b4c571bfe05a52bfb3f471a697e
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Uitsluitingen beheren

Uitsluitingen beheren door uitsluitingsgroepen te maken, met uitzondering van dubbele aanbiedingen, met uitzondering van specifieke ervaringen, en standaardinhoud uitsluiten in [!UICONTROL Automated Personalization] (AP) [!DNL Adobe Target].

## Uitsluitingsgroepen maken {#task_AAAA6C7239A84F7696C8492F04B575A2}

Uitsluitingsgroepen maken in [!UICONTROL Automated Personalization] (AP) activiteiten om ervoor te zorgen dat ervaringen met de aangewezen aanbiedingen automatisch worden uitgesloten.

Uitsluitingsgroepen zijn een goede manier om ervoor te zorgen dat incompatibele aanbiedingen niet op verschillende plaatsen in dezelfde ervaring worden gepresenteerd. Stel dat u twee aanbiedingen hebt: de ene is voor een korting van 20% voor alle producten en de andere voor een korting van 15%. U wilt nooit dat deze twee aanbiedingen aan bezoekers in dezelfde ervaring worden getoond. Als u deze twee aanbiedingen aan een uitsluitingsgroep toevoegt, kunt u ervoor zorgen dat deze situatie nooit het geval is.

U kunt ook beperken welke doelgroepen specifieke aanbiedingen kunnen zien in AP-activiteiten. Zie voor meer informatie [Automated Personalization-doelaanbiedingen](/help/main/c-activities/t-automated-personalization/ap-target-offers.md).

**Een uitsluitingsgroep maken:**

1. while [AP-activiteiten maken of bewerken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), klikt u op **[!UICONTROL Manage Content]** in de koptekstbalk.

   ![Content-koppeling beheren](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

1. In de [!UICONTROL Manage Content] klikt u op **[!UICONTROL Exclusion Groups]**.

   ![Inhoud beheren > Het dialoogvenster Uitsluitingsgroepen](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Als u eerder uitsluitingsgroepen hebt gemaakt, worden deze weergegeven in de lijst. Als u nog geen uitsluitingsgroep hebt gemaakt, wordt u gevraagd om er een te maken.

1. Klik op **[!UICONTROL Create Exclusion Group.]**

   ![Uitsluitingsgroep maken, dialoogvenster](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Vereist) Geef een beschrijvende naam op voor de uitsluitingsgroep.

   Met een beschrijvende naam kunt u snel het doel van een groep vinden en begrijpen.

1. Zoek en selecteer de gewenste aanbiedingen die u aan de uitsluitingsgroep wilt toevoegen.

   U kunt meerdere voorstellen selecteren op dezelfde locatie in een uitsluitingsgroep.

1. Klik op **[!UICONTROL Save]**.

De aanbiedingen in de uitsluitingsgroep worden automatisch uitgesloten van dezelfde ervaringen die in de toekomst worden opgedaan.

## Dubbele aanbiedingen uitsluiten {#concept_4EF78013F80E48EFA024AE0274C9F037}

Voorkomen dat aanbiedingen uit de aanbiedingsbibliotheek worden gedupliceerd wanneer deze op verschillende locaties worden gebruikt in [!UICONTROL Automated Personalization] activiteiten.

U hebt bijvoorbeeld een activiteit met zes locaties op een pagina met 12 aanbiedingen. Er bestaat een kans dat hetzelfde aanbod op een of meer locaties in de activiteit kan worden geplaatst. Met deze functie voorkomt u dat dubbele aanbiedingen tegelijkertijd worden weergegeven op verschillende locaties binnen dezelfde activiteit.

Klik op de knop **[!UICONTROL Configure]** tandwieloptie > **[!UICONTROL Duplicate Offers]** en klik vervolgens op **[!UICONTROL Allow Duplicates]** of **[!UICONTROL Disallow Duplicates]**.

![Opties voor dubbele aanbiedingen](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Specifieke ervaringen uitsluiten {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Sluit specifieke ervaringen uit als u bepaalde aanbiedingscombinaties van uw wilt uitsluiten [!UICONTROL Automated Personalization] activiteit.

Er zouden bepaalde combinaties kunnen zijn die niet samenwerken, of u zou het aantal geteste ervaringen kunnen beperken om verkeersvereisten voor uw activiteit te verminderen.

1. while [AP-activiteiten maken of bewerken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), klikt u op **Inhoud beheren** in de koptekstbalk.

   ![Content-koppeling beheren](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   De [!UICONTROL Experiences] in de lijst wordt elke ervaring weergegeven die is gegenereerd op basis van de permutaties van alle opties voor inhoud en locatie.

1. Ervaringen desgewenst uitsluiten.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![Ervaring uitsluiten door aanwijzen](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   Of u kunt ervaringen in batch uitsluiten door het selectievakje voor de relevante ervaringen in te schakelen en vervolgens op de knop **[!UICONTROL Exclude]** in de rechterbovenhoek van het dialoogvenster. De [!UICONTROL Exclude] wordt weergegeven wanneer een of meer ervaringen worden gecontroleerd.

   ![ervaringen uitsluiten](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png)

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de knop [!UICONTROL Status] vervolgkeuzelijst.

   De ervaringen zijn nu uitgesloten van de activiteit en hun [!UICONTROL Status] tonen als [!UICONTROL Excluded].

   ![Uitgesloten ervaringen](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standaardinhoud uitsluiten {#task_DCB4528989DF4C05A3A4729E5891D18F}

Soms wilt u de standaardinhoud niet opnemen in uw [!UICONTROL Automated Personalization] activiteit. De manier waarop u deze instelling opent, verschilt van het maken van uitsluitingsgroepen. U kunt deze methode gebruiken om slechts één aanbieding (verschillend van uw standaardinhoud) in een plaats als deel van uw AP activiteit te hebben.

Het uitsluiten van standaardinhoud is een goede manier om de vormgeving van de rest van de pagina aan te passen aan de aanbiedingen die u test met uw AP-activiteit. Stel dat u bijvoorbeeld het kleurenpalet wilt aanpassen van de aanbiedingen die u test, u de achtergrondkleur van de pagina kunt wijzigen en de standaardachtergrondkleur wilt uitsluiten.

**Standaardinhoud uitsluiten met de opdracht [!UICONTROL Visual Experience Composer] (VEC)**

1. while [AP-activiteiten maken of bewerken](/help/main/c-activities/t-automated-personalization/create-ap-activity.md)selecteert u de inhoud die u wilt vervangen en klikt u om deze te openen **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]**, of **[!UICONTROL Change Background Color]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel de optie uit **Inclusief** rechts van de standaardinhoud (of schakel de optie Standaardafbeelding/video in het deelvenster [!UICONTROL Select Content] scherm).

   Afhankelijk van het type inhoud of aanbieding wordt het [!UICONTROL Include] het selectievakje bevindt zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![Selectievakje Opnemen in dialoogvenster Tekst bewerken/HTML](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Voor inhoud van afbeelding/video:

   ![Selectievakje Opnemen in dialoogvenster Inhoud selecteren](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Voor achtergrondkleur:

   ![Selectievakje Opnemen in dialoogvenster Achtergrondkleur bewerken](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn opgedaan met de aanbiedingen die u onder [!UICONTROL Manage Content]. U merkt dat er geen ervaringen zijn gemaakt in [!UICONTROL Manage Content] met het standaardvoorstel dat je hebt uitgesloten.

   ![exclude_content_vec_4 afbeelding](assets/exclude_content_vec_4.png)

**Standaardinhoud uitsluiten met de opdracht [!UICONTROL Form-Based Experience Composer]:**

1. Klik tijdens het maken of bewerken van een AP-activiteit op **[!UICONTROL Change Text/HTML]** of **[!UICONTROL Change Image Offer]** krachtens **[!UICONTROL Content]**.
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel de optie uit **[!UICONTROL Include]** rechts van de standaardinhoud (of schakel de optie Standaardafbeelding/video in het deelvenster [!UICONTROL Select Content] scherm).

   Afhankelijk van het type inhoud of aanbieding wordt het [!UICONTROL Include] het selectievakje bevindt zich op een iets andere plaats.

   Voor tekst/HTML-inhoud:

   ![exclude_content_form_1 afbeelding](assets/exclude_content_form_1.png)

   Voor inhoud van afbeelding/video:

   ![exclude_content_form_2 afbeelding](assets/exclude_content_form_2.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn opgedaan met de aanbiedingen die u onder [!UICONTROL Manage Content]. U merkt dat er geen ervaringen zijn gemaakt in [!UICONTROL Manage Content] met het standaardvoorstel dat je hebt uitgesloten.

   ![exclude_content_form_3 afbeelding](assets/exclude_content_form_3.png)
