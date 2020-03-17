---
keywords: automated personalization;offer;reporting;group;reporting group
description: Informatie over het gebruik van rapportgroepen in activiteiten van Automated Personalization (AP) in Adobe Target.
title: Rapportgroepen aanbieden in activiteiten van Automated Personalization (AP) in Adobe Target
topic: Advanced
uuid: 5b111a68-bd05-4ef1-8156-d064f2c7e257
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# ![PREMIUM](/help/assets/premium.png) biedt rapportgroepen in Geautomatiseerde Personalisatie aan{#offer-reporting-groups-in-automated-personalization}

Informatie over het gebruiken van rapporteringsgroepen in [Geautomatiseerde Personalisatie](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Ze laten u uw voorstellen zien gegroepeerd in AP activiteitenrapportering.
* Ze spelen een sleutelrol bij de manier waarop de [!DNL Target] personalisatiemodellen functioneren.

Wanneer u rapportgroepen gebruikt, [!DNL Target] creeert slechts één verpersoonlijkingsmodel voor elke rapportgroep in plaats van elke aanbieding in uw AP activiteit gebruikend de gegevens van alle aanbiedingen in die groep.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft om per aanbieding worden gebouwd, kunnen de rapporteringsgroepen helpen de gegevensvereisten verminderen om Geautomatiseerde Personalisatie te gebruiken. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot;voor nieuwe aanbiedingen op te lossen door gelijkaardige aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. De modelleringsgroepen kunnen ook voor activiteiten worden gebruikt waar de nieuwe aanbiedingen regelmatig aan uw AP activiteit worden geïntroduceerd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met zeer verschillende omzettingspercentages vermindert waarschijnlijk de doeltreffendheid van de [!DNL Target] verpersoonlijkingsmodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen dragen niet bij aan welke gegevens worden gebruikt voor de [!DNL Target] personalisatiemodellen om te leren.

**Rapportagegroepen instellen:**

1. Klik op het [!UICONTROL Experiences] **[!UICONTROL Manage Content]** pictogram op de pagina van een AP-activiteit.

   ![](assets/ap_manage_content.png)

1. Klik op het **[!UICONTROL Offers]** tabblad boven in het [!UICONTROL Manage Content] dialoogvenster.
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapportgroep toe door over de gewenste aanbieding te hangen en dan door het **[!UICONTROL Reporting Group]** omslagpictogram te klikken.

   ![](assets/ap_manage_content_2.png)

1. (Voorwaardelijk) De partij omvat ervaringen in een rapportgroep door checkbox voor de relevante ervaringen te selecteren en dan door het **[!UICONTROL Reporting Group]** omslagpictogram in de hoogste juiste hoek van de dialoogdoos te klikken.

   ![](assets/ap_manage_content_3.png)

1. (Voorwaardelijk) om de geselecteerde aanbieding aan een bestaande rapportgroep toe te wijzen, selecteer **[!UICONTROL Existing]**, selecteer de gewenste rapportagegroep van de drop-down lijst, dan klik **[!UICONTROL Apply]**.

   of

   Als u een nieuwe rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]** de nieuwe rapportgroep en klikt u op **[!UICONTROL Apply]**.

   ![](assets/ap_reporting_groups.png)

