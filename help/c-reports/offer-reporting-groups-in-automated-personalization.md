---
keywords: automated personalization;offer;reporting;group;reporting group
description: Informatie over het gebruik van rapportagegroepen in Automated Personalization (AP)-activiteiten in Adobe Target.
title: Rapportgroepen aanbieden in Automated Personalization (AP)-activiteiten in Adobe Target
feature: reports
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# ![](/help/assets/premium.png) PREMIUMObied rapportagegroepen in Automated Personalization{#offer-reporting-groups-in-automated-personalization}

Informatie over het gebruik van rapportgroepen in [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Ze laten u uw voorstellen zien gegroepeerd in AP activiteitenrapportering.
* Zij spelen een zeer belangrijke rol met hoe de [!DNL Target] verpersoonlijkingsmodellen functioneren.

Wanneer u rapportgroepen gebruikt, [!DNL Target] creeert slechts één verpersoonlijkingsmodel voor elke rapportgroep in plaats van elke aanbieding in uw AP activiteit gebruikend de gegevens van alle aanbiedingen in die groep.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft om per aanbieding worden gebouwd, kunnen de rapportagegroepen helpen de gegevensvereisten verminderen om Automated Personalization te gebruiken. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot; voor nieuwe aanbiedingen op te lossen door vergelijkbare aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. De modelleringsgroepen kunnen ook voor activiteiten worden gebruikt waar de nieuwe aanbiedingen regelmatig aan uw AP activiteit worden geïntroduceerd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met zeer verschillende omzettingspercentages vermindert waarschijnlijk de doeltreffendheid van [!DNL Target] verpersoonlijkingsmodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen dragen niet bij aan welke gegevens worden gebruikt voor de [!DNL Target] verpersoonlijkingsmodellen om te leren.

**Rapportagegroepen instellen:**

1. Op [!UICONTROL Experiences] pagina van een AP activiteit, klik **[!UICONTROL Manage Content]** pictogram.

   ![](assets/ap_manage_content.png)

1. Klik op het tabblad **[!UICONTROL Offers]** boven in het dialoogvenster [!UICONTROL Manage Content].
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapportgroep toe door over de gewenste aanbieding te hangen en dan door het **[!UICONTROL Reporting Group]** omslagpictogram te klikken.

   ![](assets/ap_manage_content_2.png)

1. (Voorwaardelijk) De partij omvat ervaringen in een rapportgroep door checkbox voor de relevante ervaringen te selecteren en dan door het **[!UICONTROL Reporting Group]** omslagpictogram in de hoogste juiste hoek van de dialoogdoos te klikken.

   ![](assets/ap_manage_content_3.png)

1. (Voorwaardelijk) om de geselecteerde aanbieding aan een bestaande rapportgroep toe te wijzen, selecteer **[!UICONTROL Existing]**, selecteer de gewenste rapportagegroep van de drop-down lijst, dan klik **[!UICONTROL Apply]**.

   of

   Als u een nieuwe rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]**, geeft u de nieuwe rapportgroep een naam en klikt u op **[!UICONTROL Apply]**.

   ![](assets/ap_reporting_groups.png)

