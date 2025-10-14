---
keywords: geautomatiseerde personalisatie;aanbieding;rapportering;groep;rapporteringsgroep;ap
description: Leer hoe te om aanbiedingsrapportgroepen in  [!DNL Adobe Target] [!UICONTROL Automated Personalization] activiteiten te gebruiken.
title: Kan ik rapportagegroepen voorstellen gebruiken bij [!UICONTROL Automated Personalization] -activiteiten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Rapportgroepen aanbieden in [!UICONTROL Automated Personalization]

Informatie over het gebruiken van rapporteringsgroepen in [!DNL Adobe Target] [&#x200B; Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) activiteiten.

Rapporterende groepen voeren twee belangrijke functies uit:

* Met rapportagegroepen kunt u uw voorstellen zien die zijn gegroepeerd in rapportage van AP-activiteiten.
* Rapporterende groepen spelen een sleutelrol bij de manier waarop de [!DNL Target] personalisatiemodellen functioneren.

Wanneer u rapportgroepen gebruikt, maakt [!DNL Target] één verpersoonlijkingsmodel voor elke rapportgroep met behulp van de gegevens van alle aanbiedingen in die groep. Zonder rapportagegroepen maakt [!DNL Target] een personalisatiemodel voor elke aanbieding in uw AP-activiteit.

Als uw activiteitenopstelling niet genoeg gegevens voor een verpersoonlijkingsmodel heeft om per aanbieding worden gebouwd, helpen de rapportagegroepen de gegevensvereisten verminderen om [!UICONTROL Automated Personalization] te gebruiken. Rapportagegroepen kunnen ook helpen het &quot;koudstartprobleem&quot; voor nieuwe aanbiedingen op te lossen door vergelijkbare aanbiedingen te groeperen zodat elk model meer gegevens krijgt om op te leiden. U kunt modelleringsgroepen ook gebruiken voor activiteiten waarbij regelmatig nieuwe aanbiedingen aan uw AP-activiteit worden toegevoegd.

Deze aanpak werkt goed als bezoekers op dezelfde manier reageren op alle aanbiedingen in een groep. De beste manier is om aanbiedingen te groeperen waarop vergelijkbare groepen bezoekers op dezelfde manier reageren. Met andere woorden, groepsobjecten met vergelijkbare conversiekoersen. Je mag niet alle voorstellen in één rapportagegroep plaatsen. Het groeperen van alle aanbiedingen of het groeperen van aanbiedingen met verschillende omzettingspercentages vermindert waarschijnlijk de doeltreffendheid van de [!DNL Target] verpersoonlijkingsmodellen.

>[!NOTE]
>
>Als een aanbieding uit een bepaalde modelleringsgroep wordt verwijderd of vervangen, wordt het historische verkeer dat die specifieke aanbieding zag ook geschrapt uit de modelleringsgroep. Met andere woorden, verwijderde aanbiedingen dragen niet bij aan welke gegevens worden gebruikt voor de [!DNL Target] personalisatiemodellen om te leren.

## Rapportgroepen instellen

1. Voor de **[!UICONTROL Experiences]** pagina van een AP activiteit, klik het **[!UICONTROL Manage Content]** pictogram ( ![&#x200B; leidt het pictogram van de Inhoud &#x200B;](/help/main/assets/icons/Experience.svg))
1. Klik op de tab **[!UICONTROL Offers]** boven in het dialoogvenster [!UICONTROL Manage Content] .
1. (Voorwaardelijk) voeg specifieke ervaringen aan een rapporteringsgroep toe door het [!UICONTROL More Actions] pictogram ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmall.svg)) voor de gewenste aanbieding te klikken en dan door **[!UICONTROL Reporting Group]** te klikken.

1. (Voorwaardelijk) De partij omvat ervaringen in een rapporteringsgroep door controledozen voor de relevante ervaringen te selecteren en dan te klikken **[!UICONTROL Reporting Group]** bij de bodem van de dialoogdoos.

1. Als u de geselecteerde aanbieding aan een bestaande rapportgroep wilt toewijzen, selecteert u **[!UICONTROL Existing]**, selecteert u de gewenste rapportagegroep in de vervolgkeuzelijst en klikt u op **[!UICONTROL Confirm]** .

   of

   Als u een rapportgroep wilt maken waaraan u de geselecteerde aanbieding wilt toewijzen, selecteert u **[!UICONTROL New]** , geeft u de nieuwe rapportgroep een naam en klikt u op **[!UICONTROL Confirm]** .

Met de lijst [!UICONTROL Location] kunt u aanbiedingen filteren op locatie. Gebruik de lijst [!UICONTROL Report Group] om aanbiedingen te filteren op rapportagegroepen. U kunt de lijst [!UICONTROL Report Group] ook gebruiken om te filteren voor [!UICONTROL Unassigned Offers] , zodat u een rapportgroep kunt toewijzen aan een aanbieding die momenteel niet aan een rapportgroep is toegewezen.

Voor informatie over het richten van een aanbieding aan specifiek publiek, zie [&#x200B; Aanbiedingen van het Doel [!UICONTROL Automated Personalization] &#x200B;](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Caveats

* Het is belangrijk om te begrijpen dat rapportgroepen invloed hebben op de manier waarop [!DNL Target] zijn modellen bouwt. Daarom raadt [!DNL Adobe] u aan alleen rapportgroepen te gebruiken als u nieuwe aanbiedingen wilt vervangen of toevoegen terwijl een activiteit actief is. Als een nieuwe aanbieding wordt geïntroduceerd in een live-activiteit, kan de machine de gegevens die reeds voor de andere aanbiedingen in haar groep zijn verzameld, gebruiken om meer te leren over de nieuwe aanbieding. Je mag niet alle voorstellen in één rapportagegroep plaatsen.

* AP-activiteiten hebben combinaties van locatie+aanbod (modellabels). Wanneer [!DNL Target] gegevens in rapporten registreert, [!DNL Target] dergelijke combinaties zodat is het duidelijk van welke gebeurtenis (vertoning, klik, etc.) de aanbieding kwam.

  Een activiteit kan bijvoorbeeld verschillende locaties en verschillende aanbiedingen hebben, die elkaar kunnen overlappen. Als een bezoeker meer dan een van deze aanbiedingen op verschillende locaties ziet, worden in [!DNL Target] alleen de gegevens voor die aanbiedingen vastgelegd. Als dezelfde bezoeker later op een aanbieding klikt, registreert [!DNL Target] alleen een gebeurtenis van die combinatie (niet voor alle combinaties).

  Op dezelfde manier als de klik uit een verschillende plaats komt, die in metrisch aanwezig is, maar geen aanbieding toont, wordt deze gebeurtenis geregistreerd onder de activiteit, maar niet voor om het even welke aanbod+locatie combinatie. Dientengevolge, verschijnt deze aanbieding niet in de aanbiedingsrapporteringsgroep.

  Dit gedrag is omdat de klik van een verschillende mbox en niet mbox zou kunnen worden gemaakt die de aanbieding vormde. Wegens dit, wordt metrisch geassocieerd met de activiteit, maar niet met de aanbieding.

## Voorstellen weergeven in een rapportgroep

1. Klik **[!UICONTROL Activities]**, klik de gewenste [!UICONTROL Automated Personalization] activiteit van de lijst, dan klik het **[!UICONTROL Reports]** lusje om het [&#x200B; Niveau van de Aanbieding &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md) rapport te tonen.

   Als u veel activiteiten hebt, klikt u op het pictogram [!UICONTROL Show Filters] (trechter) en schakelt u het selectievakje [!UICONTROL Automated Personalization] in om de lijst te filteren en alleen [!UICONTROL Automated Personalization] -activiteiten weer te geven.

1. Klik op **[!UICONTROL Control]** of **[!UICONTROL Targeted]** in de tabel om de niet-gegroepeerde voorstellen en voorstellen in rapportgroepen weer te geven.

   ![&#x200B; groepen van de Aanbieding: Controle en Gericht &#x200B;](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Voor informatie over het gebruiken van [!UICONTROL Automated Personalization] rapporten (met inbegrip van het [!UICONTROL Offer Level] rapport), zie [&#x200B; de Samenvattingsrapporten van Automated Personalization &#x200B;](/help/main/c-reports/personalization-reports/reports-ap.md).
