---
keywords: geautomatiseerde personalisatie;aanbieding;rapportering;groep;rapporteringsgroep;ap
description: Leer hoe u rapportgroepen kunt aanbieden in Adobe [!DNL Target] [!UICONTROL Automated Personalization] activiteiten.
title: Kan ik rapportagegroepen voor aanbiedingen gebruiken bij Automated Personalization-activiteiten?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 60655a93b515095bd8c67a4af2193d36789ab96e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Rapportgroepen aanbieden in [!UICONTROL Automated Personalization]

Informatie over het gebruik van rapportagegroepen in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Met rapportagegroepen kunt u uw voorstellen zien die zijn gegroepeerd in rapportage van AP-activiteiten.
* Rapporterende groepen spelen een sleutelrol bij de manier waarop [!DNL Target] personalisatiemodellen functioneren.

Wanneer u rapportgroepen gebruikt, [!DNL Target] leidt tot één verpersoonlijkingsmodel voor elke rapporteringsgroep gebruikend de gegevens van alle aanbiedingen in die groep. Zonder rapportagegroepen [!DNL Target] leidt tot een verpersoonlijkingsmodel voor elke aanbieding in uw AP activiteit.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft dat per aanbieding moet worden gebouwd, kunnen de rapportagegroepen helpen de gegevensvereisten aan gebruik verminderen [!UICONTROL Automated Personalization]. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot;voor nieuwe aanbiedingen op te lossen door gelijkaardige aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. U kunt modelleringsgroepen ook gebruiken voor activiteiten waarbij regelmatig nieuwe aanbiedingen aan uw AP-activiteit worden toegevoegd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met zeer verschillende omzettingspercentages vermindert waarschijnlijk de doeltreffendheid van de [!DNL Target] personalisatiemodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen leveren geen bijdrage aan de gegevens die worden gebruikt voor de [!DNL Target] personalisatiemodellen om te leren.

**Rapportagegroepen instellen:**

1. Op de **[!UICONTROL Experiences]** pagina van een AP-activiteit, klikt u op de **[!UICONTROL Manage Content]** pictogram.

   ![Het pictogram Inhoud beheren](/help/main/c-reports/assets/ap_manage_content.png)

1. Klik op de knop **[!UICONTROL Offers]** tabblad boven aan het dialoogvenster [!UICONTROL Manage Content] in.
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapporteringsgroep toe door over de gewenste aanbieding te hangen en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram.

   ![pictogram Rapportagegroep](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Voorwaardelijk) De partij omvat ervaringen in een rapporteringsgroep door checkbox voor de relevante ervaringen te selecteren en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram in de rechterbovenhoek van het dialoogvenster.

   ![pictogram Rapportagegroep](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Selecteer **[!UICONTROL Existing]** selecteert u de gewenste rapportgroep in de vervolgkeuzelijst en klikt u vervolgens op **[!UICONTROL Apply]**.

   of

   Als u een nieuwe rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]**, noem de nieuwe rapportgroep en klik vervolgens op **[!UICONTROL Apply]**.

   ![Nieuw pictogram om een nieuwe rapportgroep te maken](/help/main/c-reports/assets/ap_reporting_groups.png)
