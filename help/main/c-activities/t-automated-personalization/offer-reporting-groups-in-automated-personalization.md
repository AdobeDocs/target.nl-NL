---
keywords: geautomatiseerde personalisatie;aanbieding;rapportering;groep;rapporteringsgroep;ap
description: Leer hoe u rapportgroepen kunt aanbieden in Adobe [!DNL Target] [!UICONTROL Automated Personalization] activiteiten.
title: Kan ik rapportagegroepen voor aanbiedingen gebruiken bij Automated Personalization-activiteiten?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 748051dccf4a0df49ac05e699fa14801c148d45e
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# ![PREMIUM](/help/main/assets/premium.png) Rapportgroepen aanbieden in [!UICONTROL Automated Personalization]

Informatie over het gebruik van rapportagegroepen in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Met rapportagegroepen kunt u uw voorstellen zien die zijn gegroepeerd in rapportage van AP-activiteiten.
* Rapporterende groepen spelen een sleutelrol bij de manier waarop [!DNL Target] personalisatiemodellen functioneren.

Wanneer u rapportgroepen gebruikt, [!DNL Target] leidt tot één verpersoonlijkingsmodel voor elke rapporteringsgroep gebruikend de gegevens van alle aanbiedingen in die groep. Zonder rapportagegroepen [!DNL Target] leidt tot een verpersoonlijkingsmodel voor elke aanbieding in uw AP activiteit.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft dat per aanbieding moet worden gebouwd, kunnen de rapportagegroepen helpen de gegevensvereisten aan gebruik verminderen [!UICONTROL Automated Personalization]. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot;voor nieuwe aanbiedingen op te lossen door gelijkaardige aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. U kunt modelleringsgroepen ook gebruiken voor activiteiten waarbij regelmatig nieuwe aanbiedingen aan uw AP-activiteit worden toegevoegd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met verschillende omrekeningskoersen vermindert waarschijnlijk de doeltreffendheid van [!DNL Target] personalisatiemodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen leveren geen bijdrage aan de gegevens die worden gebruikt voor de [!DNL Target] personalisatiemodellen om te leren.

## Rapportgroepen instellen

1. Op de **[!UICONTROL Experiences]** pagina van een AP-activiteit, klikt u op de **[!UICONTROL Manage Content]** pictogram.

   ![Het pictogram Inhoud beheren](/help/main/c-reports/assets/ap_manage_content.png)

1. Klik op de knop **[!UICONTROL Offers]** tabblad boven aan het dialoogvenster [!UICONTROL Manage Content] in.
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapporteringsgroep toe door over de gewenste aanbieding te hangen en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram.

   ![pictogram Rapportagegroep](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Voorwaardelijk) De partij omvat ervaringen in een rapporteringsgroep door checkbox voor de relevante ervaringen te selecteren en dan door te klikken **[!UICONTROL Reporting Group]** mappictogram in de rechterbovenhoek van het dialoogvenster.

   ![pictogram Rapportagegroep](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Selecteer **[!UICONTROL Existing]** selecteert u de gewenste rapportgroep in de vervolgkeuzelijst en klikt u vervolgens op **[!UICONTROL Apply]**.

   of

   Als u een rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]**, noem de nieuwe rapportgroep en klik vervolgens op **[!UICONTROL Apply]**.

   ![Nieuw pictogram om een nieuwe rapportgroep te maken](/help/main/c-reports/assets/ap_reporting_groups.png)

U kunt de [!UICONTROL Location] lijst om aanbiedingen te filteren op locatie. Gebruik de [!UICONTROL Report Group] lijst aan filteraanbiedingen door rapporterende groepen. U kunt ook de opdracht [!UICONTROL Report Group] lijst die moet worden gefilterd voor [!UICONTROL Unassigned Offers] zodat kunt u een rapportgroep aan een aanbieding toewijzen die momenteel niet aan om het even welke rapporteringsgroep wordt toegewezen.

Voor informatie over het richten van een aanbieding aan specifiek publiek, zie [AP-doelaanbiedingen](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Caveats

* Het is belangrijk te begrijpen dat rapportagegroepen invloed hebben op de manier waarop [!DNL Target] bouwt zijn modellen. Dientengevolge [!DNL Adobe] U kunt alleen rapportgroepen gebruiken als u nieuwe voorstellen wilt vervangen of toevoegen terwijl een activiteit actief is. Als een nieuwe aanbieding wordt geïntroduceerd in een live-activiteit, kan de machine de gegevens die reeds voor de andere aanbiedingen in haar groep zijn verzameld, gebruiken om meer te leren over de nieuwe aanbieding. Je mag niet alle voorstellen in één rapportagegroep plaatsen.

* AP-activiteiten hebben combinaties van locatie+aanbod (modellabels). Wanneer [!DNL Target] gegevens in rapporten registreert; [!DNL Target] is van mening dat deze combinaties een dergelijke combinatie vormen, zodat duidelijk is uit welke gebeurtenis (weergave, klik, enzovoort) het aanbod afkomstig was.

   Een activiteit kan bijvoorbeeld verschillende locaties en verschillende aanbiedingen hebben, die elkaar kunnen overlappen. Als een bezoeker meer dan een van deze aanbiedingen op verschillende locaties ziet, [!DNL Target] registreert alleen gegevens voor deze aanbiedingen. Als dezelfde bezoeker later op een aanbieding klikt, [!DNL Target] registreert een gebeurtenis slechts van die combinatie (niet voor alle combinaties).

   Op dezelfde manier als de klik uit een verschillende plaats komt, die in metrisch aanwezig is, maar geen aanbieding toont, wordt deze gebeurtenis geregistreerd onder de activiteit, maar niet voor om het even welke aanbod+location combinatie. Dientengevolge, verschijnt deze aanbieding niet in de aanbiedingsrapporteringsgroep.

   Dit gedrag is toe te schrijven aan het feit dat de klik van een verschillende mbox en niet mbox zou kunnen worden gemaakt die de aanbieding vormde. Wegens dit, wordt metrisch geassocieerd met de activiteit, maar niet met de aanbieding.

## Voorstellen weergeven in een rapportgroep

1. Klikken **[!UICONTROL Activities]** klikt u op de gewenste [!UICONTROL Automated Personalization] in de lijst en klik vervolgens op de knop **[!UICONTROL Reports]** om de [Aanbiedingsniveau](/help/main/c-reports/personalization-reports/reports-ap.md) verslag.

   Als u veel activiteiten hebt, kunt u de lijst filteren door [!UICONTROL Automated Personalization] van de [!UICONTROL Type] vervolgkeuzelijst.

1. Klikken **[!UICONTROL Control]** of **[!UICONTROL Targeted]** in de tabel om de ongegroepeerde aanbiedingen en aanbiedingen binnen rapportagegroepen weer te geven.

   ![Groepen voorstellen: Control en gericht](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Voor informatie over het gebruik [!UICONTROL Automated Personalization] (inclusief de [!UICONTROL Offer Level] rapport), zie [Samenvattingsrapporten van Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).


