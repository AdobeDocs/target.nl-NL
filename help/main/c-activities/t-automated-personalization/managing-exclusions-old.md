---
keywords: dedupe;allow duplicates;exclude duplicate aanbiedingen;automatiseerd personalisatie;disallow duplicate aanbiedingen;exclude;default content;exclusion group;
description: Uitsluitingen beheren in  [!DNL Adobe Target] [!UICONTROL Automated Personalization] (AP)-activiteiten. Maak uitsluitingsgroepen en sluit dubbele aanbiedingen, specifieke ervaringen en standaardinhoud uit.
title: Hoe kan ik uitsluitingen in [!UICONTROL Automated Personalization] -activiteiten beheren?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
exl-id: d9e9f2a2-5914-4b81-acae-eaf388646652
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Uitsluitingen beheren

Uitsluitingen beheren door uitsluitingsgroepen te maken, met uitzondering van dubbele aanbiedingen, met uitzondering van specifieke ervaringen, en standaardinhoud in [!UICONTROL Automated Personalization] (AP)-activiteiten in [!DNL Adobe Target] uit te sluiten.

## Uitsluitingsgroepen maken {#task_AAAA6C7239A84F7696C8492F04B575A2}

Maak uitsluitingsgroepen in [!UICONTROL Automated Personalization] (AP)-activiteiten om ervoor te zorgen dat ervaringen met de toegewezen aanbiedingen automatisch worden uitgesloten.

Uitsluitingsgroepen zijn een goede manier om ervoor te zorgen dat incompatibele aanbiedingen niet op verschillende plaatsen in dezelfde ervaring worden gepresenteerd. Stel dat u twee aanbiedingen hebt: de ene is voor een korting van 20% voor alle producten en de andere voor een korting van 15%. U wilt nooit dat deze twee aanbiedingen aan bezoekers in dezelfde ervaring worden getoond. Als u deze twee aanbiedingen aan een uitsluitingsgroep toevoegt, kunt u ervoor zorgen dat deze situatie nooit het geval is.

U kunt ook beperken welke doelgroepen specifieke aanbiedingen kunnen zien in AP-activiteiten. Voor meer informatie, zie {de aanbiedingen van Automated Personalization van het 0} Doel [.](/help/main/c-activities/t-automated-personalization/ap-target-offers.md)

**om een uitsluitingsgroep tot stand te brengen:**

1. Terwijl [&#x200B; creërend of het uitgeven van een AP activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), klik **[!UICONTROL Manage Content]** in de kopbalbar.

   ![&#x200B; beheer de verbinding van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

1. Klik in het dialoogvenster [!UICONTROL Manage Content] op **[!UICONTROL Exclusion Groups]** .

   ![&#x200B; beheert Inhoud > de dialoogdoos van de Groepen van de Uitsluiting &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create-new.png)

   Als u eerder uitsluitingsgroepen hebt gemaakt, worden deze weergegeven in de lijst. Als u nog geen uitsluitingsgroep hebt gemaakt, wordt u gevraagd om er een te maken.

1. Klikken **[!UICONTROL Create Exclusion Group.]**

   ![&#x200B; creeer de dialoogdoos van de Groep van de Uitsluiting &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclusion_group_create_dialog-new.png)

1. (Vereist) Geef een beschrijvende naam op voor de uitsluitingsgroep.

   Met een beschrijvende naam kunt u snel het doel van een groep vinden en begrijpen.

1. Zoek en selecteer de gewenste aanbiedingen die u aan de uitsluitingsgroep wilt toevoegen.

   U kunt meerdere voorstellen selecteren op dezelfde locatie in een uitsluitingsgroep.

1. Klik op **[!UICONTROL Save]**.

De aanbiedingen in de uitsluitingsgroep worden automatisch uitgesloten van dezelfde ervaringen die in de toekomst worden opgedaan.

## Dubbele aanbiedingen uitsluiten {#concept_4EF78013F80E48EFA024AE0274C9F037}

Voorkomen dat aanbiedingen uit de aanbiedingsbibliotheek worden gedupliceerd wanneer deze op verschillende locaties in [!UICONTROL Automated Personalization] -activiteiten worden gebruikt.

U hebt bijvoorbeeld een activiteit met zes locaties op een pagina met 12 aanbiedingen. Er bestaat een kans dat hetzelfde aanbod op een of meer locaties in de activiteit kan worden geplaatst. Met deze functie voorkomt u dat dubbele aanbiedingen tegelijkertijd worden weergegeven op verschillende locaties binnen dezelfde activiteit.

Klik op **[!UICONTROL Configure]** versnelling > **[!UICONTROL Duplicate Offers]** en klik vervolgens op **[!UICONTROL Allow Duplicates]** of **[!UICONTROL Disallow Duplicates]** .

![&#x200B; de dubbel aanbiedingsopties van aanbiedingen &#x200B;](/help/main/c-activities/t-automated-personalization/assets/duplicate_offers-new.png)

## Specifieke ervaringen uitsluiten {#task_C17D36EF58AF4908B17A3D84CA6DE85A}

Sluit specifieke ervaringen uit als u bepaalde aanbiedingscombinaties wilt uitsluiten van uw [!UICONTROL Automated Personalization] -activiteit.

Er zouden bepaalde combinaties kunnen zijn die niet samenwerken, of u zou het aantal geteste ervaringen kunnen beperken om verkeersvereisten voor uw activiteit te verminderen.

1. Terwijl [&#x200B; creërend of het uitgeven van een AP activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), klik **leidt Inhoud** in de kopbalbar.

   ![&#x200B; beheer de verbinding van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   In de lijst [!UICONTROL Experiences] wordt elke ervaring weergegeven die is gegenereerd op basis van de permutaties van alle opties voor inhoud en locatie.

1. Ervaringen desgewenst uitsluiten.

   U kunt specifieke ervaringen uitsluiten door de muisaanwijzer boven de gewenste ervaring te houden en vervolgens op het pictogram voor uitsluiten te klikken.

   ![&#x200B; sluit ervaring uit door te bedekken &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_1a.png)

   U kunt ervaringen ook in batch uitsluiten door het selectievakje voor relevante ervaringen in te schakelen en vervolgens op het pictogram **[!UICONTROL Exclude]** in de rechterbovenhoek van het dialoogvenster te klikken. Het pictogram [!UICONTROL Exclude] wordt weergegeven wanneer een of meer ervaringen worden gecontroleerd.

   ![&#x200B; Partij sluit ervaringen &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_2a.png) uit

   U kunt deze lijstweergave filteren om alleen uitgesloten of alleen opgenomen activiteiten weer te geven door op de vervolgkeuzelijst [!UICONTROL Status] te klikken.

   De ervaringen zijn nu uitgesloten van de activiteit en de [!UICONTROL Status] show as [!UICONTROL Excluded] .

   ![&#x200B; Uitgesloten ervaringen &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_exp_3a.png)

## Standaardinhoud uitsluiten {#task_DCB4528989DF4C05A3A4729E5891D18F}

Soms wilt u de standaardinhoud niet opnemen in uw [!UICONTROL Automated Personalization] -activiteit. De manier waarop u deze instelling opent, verschilt van het maken van uitsluitingsgroepen. U kunt deze methode gebruiken om slechts één aanbieding (verschillend van uw standaardinhoud) in een plaats als deel van uw AP activiteit te hebben.

Het uitsluiten van standaardinhoud is een goede manier om de vormgeving van de rest van de pagina aan te passen aan de aanbiedingen die u test met uw AP-activiteit. Stel dat u bijvoorbeeld het kleurenpalet wilt aanpassen van de aanbiedingen die u test, u de achtergrondkleur van de pagina kunt wijzigen en de standaardachtergrondkleur wilt uitsluiten.

**om standaardinhoud uit te sluiten gebruikend [!UICONTROL Visual Experience Composer] (VEC):**

1. Terwijl [&#x200B; creërend of het uitgeven van een AP activiteit &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md), selecteer de inhoud u wilt vervangen en klikken om tot **[!UICONTROL Change Text/HTML]**, **[!UICONTROL Change Image]**, of **[!UICONTROL Change Background Color]** toegang te hebben.
1. In de dialoogdoos, creeer uw nieuwe inhoud en uncheck **omvatten** rechts van de standaardinhoud (of uncheck het StandaardBeeld/Video in het [!UICONTROL Select Content] scherm).

   Afhankelijk van het type inhoud of aanbieding bevindt het selectievakje [!UICONTROL Include] zich op een iets andere plaats.

   Voor Text/HTML-inhoud:

   ![&#x200B; omvatten checkbox in Edit Text/HTML dialoogdoos &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_1a.png)

   Voor inhoud van afbeelding/video:

   ![&#x200B; omvatten checkbox in Uitgezochte de dialoogdoos van de Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_2a.png)

   Voor achtergrondkleur:

   ![&#x200B; omvat checkbox in Edit de dialoogdoos van de Kleur van de Achtergrond &#x200B;](/help/main/c-activities/t-automated-personalization/assets/exclude_content_vec_3a.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. U ziet dat er in [!UICONTROL Manage Content] geen ervaringen zijn gemaakt met de standaardaanbieding die u hebt uitgesloten.

   ![&#x200B; exclude_content_vec_4 beeld &#x200B;](assets/exclude_content_vec_4.png)

**om standaardinhoud uit te sluiten gebruikend [!UICONTROL Form-Based Experience Composer]:**

1. Klik tijdens het maken of bewerken van een AP-activiteit op **[!UICONTROL Change Text/HTML]** of **[!UICONTROL Change Image Offer]** onder **[!UICONTROL Content]** .
1. Maak in het dialoogvenster uw nieuwe inhoud en schakel **[!UICONTROL Include]** rechts van de standaardinhoud uit (of schakel de optie Standaardafbeelding/video in het [!UICONTROL Select Content] -scherm uit).

   Afhankelijk van het type inhoud of aanbieding bevindt het selectievakje [!UICONTROL Include] zich op een iets andere plaats.

   Voor Text/HTML-inhoud:

   ![&#x200B; exclude_content_form_1 beeld &#x200B;](assets/exclude_content_form_1.png)

   Voor inhoud van afbeelding/video:

   ![&#x200B; exclude_content_form_2 beeld &#x200B;](assets/exclude_content_form_2.png)

1. Klik op **[!UICONTROL Save]**.

   U kunt de ervaringen zien die zijn gemaakt met de aanbiedingen die u onder [!UICONTROL Manage Content] hebt opgegeven. U ziet dat er in [!UICONTROL Manage Content] geen ervaringen zijn gemaakt met de standaardaanbieding die u hebt uitgesloten.

   ![&#x200B; exclude_content_form_3 beeld &#x200B;](assets/exclude_content_form_3.png)
