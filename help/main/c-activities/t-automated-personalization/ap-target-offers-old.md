---
keywords: geautomatiseerde personalisatie;aanbiedingen;target;publiek;het richten van regels;het richten van gericht
description: Leer hoe te om individuele aanbiedingen aan specifiek publiek te richten door een [!UICONTROL Automated Personalization] (AP) activiteit in  [!DNL Adobe Target] te gebruiken.
title: Hoe kan ik [!UICONTROL Automated Personalization] aanbiedingen richten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# Doelaanbiedingen [!UICONTROL Automated Personalization]

In een [!DNL Adobe Target] [!DNL Automated Personalization] -activiteit (AP) kunt u aanbiedingen richten op specifieke doelgroepen.

Als u deze functie gebruikt, verkleint u het aantal aanbiedingen dat een specifieke bezoeker kan zien. Neem bijvoorbeeld een [!UICONTROL Automated Personalization] -activiteit met drie mogelijkheden. Aanbieding 1 heeft een richtingsregel die zijn blootstelling aan Publiek A beperkt. Twee bezoekers zagen deze activiteit.

| | Bezoeker 1 | Bezoeker 2 |
|--- |--- |--- |
| kwalificatie publiek | Publiek A | Publiek B |
| Aanbieding 1 Doel-verpersoonlijkingsmodelscore | 90 | 90 |
| Aanbieding 2 score voor doel-verpersoonlijkingsmodel | 50 | 70 |
| Aanbieding 3 Streefverpersoonlijkingsmodelscore | 80 | 60 |

In dit scenario ziet bezoeker 1 aanbod 1 (omdat deze bezoeker in aanmerking komt als onderdeel van Audience A), wat de hoogste score van die bezoeker is. Visitor 2 ziet echter Aanbieding 2, ook al is de hoogste score voor Aanbieding 1, omdat Visitor 2 geen deel uitmaakt van Audience A. Dit voorbeeld toont aan waarom het richten van regels spaarzaam zou moeten worden gebruikt om aan bedrijfsbehoeften te voldoen. Het toevoegen van deze regels kan de doeltreffendheid van [!DNL Target] verpersoonlijkingsmodellen verminderen.

## Doelstellingen instellen

1. Creeer een [&#x200B; activiteit van Automated Personalization &#x200B;](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) die de aanbiedingen bevat die u wilt richten.
1. Klik op [!UICONTROL Visual Experience Composer] nadat u de aanbiedingen voor de activiteit in de **[!UICONTROL Manage Content]** hebt ingesteld.

   ![&#x200B; beheert Inhoud &#x200B;](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Het dialoogvenster [!UICONTROL Manage Content] wordt weergegeven.

1. Klik op de tab **[!UICONTROL Offers]** .

   ![&#x200B; pagina van Aanbiedingen &#x200B;](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Selecteer de gewenste aanbiedingen en kies vervolgens het publiek dat u in aanmerking wilt nemen om dat aanbod te zien.

   Als u de focus voor één aanbieding wilt instellen, houdt u de muisaanwijzer boven de gewenste aanbieding en klikt u op het pictogram **[!UICONTROL Targeting]** .

   Als u de doelgroep voor meerdere aanbiedingen wilt instellen, schakelt u de selectievakjes voor de gewenste aanbiedingen in en klikt u op het pictogram **[!UICONTROL Targeting]** dat rechtsboven in de lijst wordt weergegeven.

1. Selecteer in het dialoogvenster [!UICONTROL Choose Audience] het gewenste publiek voor de aanbiedingen en klik vervolgens op **[!UICONTROL Done]** om terug te keren naar het dialoogvenster [!UICONTROL Manage Content] .

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Voor meer informatie, zie [&#x200B; Combinerend Veelvoudige Soorten publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt 50 locaties en maximaal 250 aanbiedingen per locatie instellen.
