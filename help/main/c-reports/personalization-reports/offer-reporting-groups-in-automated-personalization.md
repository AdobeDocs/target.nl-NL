---
keywords: geautomatiseerde personalisatie;aanbieding;rapportering;groep;rapporteringsgroep
description: Leer hoe u rapportgroepen kunt aanbieden in Adobe [!DNL Target] Automated Personalization-activiteiten. rapportagegroepen gebruiken, [!DNL Target] leidt slechts één verpersoonlijkingsmodel voor elke rapporteringsgroep.
title: Kan ik rapportagegroepen voor aanbiedingen gebruiken bij Automated Personalization-activiteiten?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: d90e541588f51e16dd9b11ead1ece77e9ca1408b
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Rapportagegroepen aanbieden in Automated Personalization

Informatie over het gebruik van rapportagegroepen in [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Ze laten u uw voorstellen zien gegroepeerd in AP activiteitenrapportering.
* Ze spelen een sleutelrol bij de manier waarop de [!DNL Target] personalisatiemodellen functioneren.

Wanneer u rapportgroepen gebruikt, [!DNL Target] creeert slechts één verpersoonlijkingsmodel voor elke rapportgroep in plaats van elke aanbieding in uw AP activiteit gebruikend de gegevens van alle aanbiedingen in die groep.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft om per aanbieding worden gebouwd, kunnen de rapportagegroepen helpen de gegevensvereisten verminderen om Automated Personalization te gebruiken. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot;voor nieuwe aanbiedingen op te lossen door gelijkaardige aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. De modelleringsgroepen kunnen ook voor activiteiten worden gebruikt waar de nieuwe aanbiedingen regelmatig aan uw AP activiteit worden geïntroduceerd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met zeer verschillende omzettingspercentages vermindert waarschijnlijk de doeltreffendheid van de [!DNL Target] personalisatiemodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen leveren geen bijdrage aan de gegevens die worden gebruikt voor de [!DNL Target] personalisatiemodellen om te leren.

**Rapportagegroepen instellen:**

1. Op de [!UICONTROL Experiences] pagina van een AP-activiteit, klikt u op de **[!UICONTROL Manage Content]** pictogram.

   ![](/help/main/c-reports/assets/ap_manage_content.png)

1. Klik op de knop **[!UICONTROL Offers]** tabblad boven aan het dialoogvenster [!UICONTROL Manage Content] in.
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapporteringsgroep toe door over de gewenste aanbieding te hangen en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram.

   ![](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Voorwaardelijk) De partij omvat ervaringen in een rapporteringsgroep door checkbox voor de relevante ervaringen te selecteren en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram in de rechterbovenhoek van het dialoogvenster.

   ![](/help/main/c-reports/assets/ap_manage_content_3.png)

1. (Voorwaardelijk) Als u de geselecteerde aanbieding aan een bestaande rapportagegroep wilt toewijzen, selecteert u **[!UICONTROL Existing]** selecteert u de gewenste rapportgroep in de vervolgkeuzelijst en klikt u vervolgens op **[!UICONTROL Apply]**.

   of

   Als u een nieuwe rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]**, noem de nieuwe rapportgroep en klik vervolgens op **[!UICONTROL Apply]**.

   ![](/help/main/c-reports/assets/ap_reporting_groups.png)
