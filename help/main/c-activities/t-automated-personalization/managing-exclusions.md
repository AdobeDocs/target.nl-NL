---
keywords: dedupe;allow duplicates;exclude duplicate aanbiedingen;automatiseerd personalisatie;disallow duplicate aanbiedingen;exclude;default content;
description: Uitsluitingen beheren in [!UICONTROL Automated Personalization] (AP)-activiteiten.
title: Hoe kan ik uitsluitingen in [!UICONTROL Automated Personalization] -activiteiten beheren?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: c5016d212edafa908b8755044e73d28167e20e8a
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Uitsluitingen beheren

Uitsluitingen beheren door dubbele aanbiedingen uit te sluiten, specifieke ervaringen uit te sluiten en standaardinhoud in [!UICONTROL Automated Personalization] (AP)-activiteiten in [!DNL Adobe Target] uit te sluiten.

## Dubbele aanbiedingen uitsluiten {#concept_4EF78013F80E48EFA024AE0274C9F037}

Voorkomen dat aanbiedingen uit de aanbiedingsbibliotheek worden gedupliceerd wanneer deze op verschillende locaties in [!UICONTROL Automated Personalization] -activiteiten worden gebruikt.

U hebt bijvoorbeeld een activiteit met zes locaties op een pagina met 12 aanbiedingen. Er bestaat een kans dat hetzelfde aanbod op een of meer locaties in de activiteit kan worden geplaatst. Met deze functie voorkomt u dat dubbele aanbiedingen tegelijkertijd worden weergegeven op verschillende locaties binnen dezelfde activiteit.

Klik op het pictogram **[!UICONTROL Configure]** > **[!UICONTROL Duplicate Offers]** en klik vervolgens op **[!UICONTROL Allow Duplicates]** of **[!UICONTROL Disallow Duplicates]** .

![ de dubbel aanbiedingsopties van aanbiedingen ](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Specifieke ervaringen uitsluiten {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Sluit specifieke ervaringen uit als u bepaalde aanbiedingscombinaties wilt uitsluiten van uw [!UICONTROL Automated Personalization] -activiteit.

Er zouden bepaalde combinaties kunnen zijn die niet samenwerken, of u zou het aantal geteste ervaringen kunnen beperken om verkeersvereisten voor uw activiteit te verminderen.

1. Terwijl [ creërend of het uitgeven van een AP activiteit ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), klik **leidt Inhoud** in de kopbalbar.

   ![ beheer de verbinding van de Inhoud ](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   In de lijst [!UICONTROL Experiences] wordt elke ervaring weergegeven die is gegenereerd op basis van de permutaties van alle opties voor inhoud en locatie.

1. Ervaringen desgewenst uitsluiten.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![ sluit ervaring uit door te bedekken ](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   U kunt ervaringen ook in batch uitsluiten door het selectievakje voor relevante ervaringen in te schakelen en vervolgens op het pictogram **[!UICONTROL Exclude]** in de rechterbovenhoek van het dialoogvenster te klikken. Het pictogram [!UICONTROL Exclude] wordt weergegeven wanneer een of meer ervaringen worden gecontroleerd.

   ![ Partij sluit ervaringen ](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png) uit

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de vervolgkeuzelijst [!UICONTROL Status] te klikken.

   De ervaringen zijn nu uitgesloten van de activiteit en de [!UICONTROL Status] show as [!UICONTROL Excluded] .

   ![ Uitgesloten ervaringen ](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standaardinhoud uitsluiten {#task_DCB4528989DF4C05A3A4729E5891D18F}

Soms wilt u de standaardinhoud niet opnemen in uw [!UICONTROL Automated Personalization] -activiteit. De manier waarop u deze instelling opent, verschilt van het maken van uitsluitingsgroepen. U kunt deze methode gebruiken om slechts één aanbieding (verschillend van uw standaardinhoud) in een plaats als deel van uw AP activiteit te hebben.

Het uitsluiten van standaardinhoud is een goede manier om de vormgeving van de rest van de pagina aan te passen aan de aanbiedingen die u test met uw AP-activiteit. Stel dat u bijvoorbeeld het kleurenpalet wilt aanpassen van de aanbiedingen die u test, u de achtergrondkleur van de pagina kunt wijzigen en de standaardachtergrondkleur wilt uitsluiten.

**om standaardinhoud uit te sluiten gebruikend [!UICONTROL Visual Experience Composer] (VEC):**

1. Terwijl [ creërend of het uitgeven van een AP activiteit ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), selecteer de inhoud u wilt vervangen en klikken om tot **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]**, of **[!UICONTROL Change Background Color]** toegang te hebben.
1. In de dialoogdoos, creeer uw nieuwe inhoud en uncheck **omvatten** rechts van de standaardinhoud (of uncheck het StandaardBeeld/Video in het [!UICONTROL Select Content] scherm).

   Afhankelijk van het type inhoud of aanbieding bevindt het selectievakje [!UICONTROL Include] zich op een iets andere plaats.

   Voor Text/HTML-inhoud:

   ![ omvatten checkbox in Edit Text/HTML dialoogdoos ](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Voor inhoud van afbeelding/video:

   ![ omvatten checkbox in Uitgezochte de dialoogdoos van de Inhoud ](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Voor achtergrondkleur:

   ![ omvat checkbox in Edit de dialoogdoos van de Kleur van de Achtergrond ](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. U ziet dat er in [!UICONTROL Manage Content] geen ervaringen zijn gemaakt met de standaardaanbieding die u hebt uitgesloten.

   ![ exclude_content_vec_4 beeld ](assets/exclude_content_vec_4.png)

**om standaardinhoud uit te sluiten gebruikend [!UICONTROL Form-Based Experience Composer]:**

1. Klik tijdens het maken of bewerken van een AP-activiteit op **[!UICONTROL Change Text/HTML]** of **[!UICONTROL Change Image Offer]** onder **[!UICONTROL Content]** .
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel **[!UICONTROL Include]** rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video in het [!UICONTROL Select Content] -scherm uit).

   Afhankelijk van het type inhoud of aanbieding bevindt het selectievakje [!UICONTROL Include] zich op een iets andere plaats.

   Voor Text/HTML-inhoud:

   ![ exclude_content_form_1 beeld ](assets/exclude_content_form_1.png)

   Voor inhoud van afbeelding/video:

   ![ exclude_content_form_2 beeld ](assets/exclude_content_form_2.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. U ziet dat er in [!UICONTROL Manage Content] geen ervaringen zijn gemaakt met de standaardaanbieding die u hebt uitgesloten.

   ![ exclude_content_form_3 beeld ](assets/exclude_content_form_3.png)
