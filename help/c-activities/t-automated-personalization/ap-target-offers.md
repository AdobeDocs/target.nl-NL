---
keywords: geautomatiseerde personalisatie;aanbiedingen;target;publiek;het richten van regels;het richten van gericht
description: Leer hoe u afzonderlijke aanbiedingen kunt richten op specifieke doelgroepen met behulp van een Automated Personalization-activiteit (AP) in Adobe Target.
title: Hoe kan ik me richten op Automated Personalization-aanbiedingen?
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---


# ![automated personalization-aanbiedingen voor ](/help/assets/premium.png) PREMIUMTarget{#target-automated-personalization-offers}

In een [!DNL Adobe Target] [!DNL Automated Personalization] (AP) activiteit, kunt u aanbiedingen aan specifiek publiek richten.

Als u deze functie gebruikt, verkleint u het aantal aanbiedingen dat een specifieke bezoeker kan zien. Neem bijvoorbeeld een AP-activiteit met drie aanbiedingen. Aanbieding 1 heeft een richtingsregel die zijn blootstelling aan Publiek A beperkt. Twee bezoekers zagen deze AP-activiteit.

|  | Bezoeker 1 | Bezoeker 2 |
|--- |--- |--- |
| Poortkwalificatie | Publiek A | Publiek B |
| Aanbieding 1 Doel-verpersoonlijkingsmodelscore | 90 | 90 |
| Aanbieding 2 score voor doel-verpersoonlijkingsmodel | 50 | 70 |
| Aanbieding 3 Streefverpersoonlijkingsmodelscore | 80 | 60 |

In dit scenario, zou Bezoeker 1 Aanbieding 1 zien (omdat hij of zij als deel van Publiek A) kwalificeert, die de hoogste score van die bezoeker is. Visitor 2 ziet echter Aanbieding 2 ook al is zijn hoogste score voor Aanbieding 1, omdat bezoeker 2 geen deel uitmaakt van Publiek A. Dit voorbeeld toont aan waarom het richten van regels spaarzaam zou moeten worden gebruikt om aan bedrijfsbehoeften te voldoen. Het toevoegen van deze regels kan de doeltreffendheid van de verpersoonlijkingsmodellen van Target verminderen.

## Doelstellingen instellen

1. Maak een [Automated Personalization-activiteit](/help/c-activities/t-automated-personalization/create-ap-activity.md) die de aanbiedingen bevat die u als doel wilt instellen.
1. Na vestiging de aanbiedingen voor de activiteit in de Visuele Composer van de Ervaring, klik **[!UICONTROL Manage Content]**.

   ![Inhoud beheren](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Het dialoogvenster Inhoud beheren wordt geopend.

1. Klik op het tabblad Aanbiedingen.

   ![Aanbiedingspagina](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Selecteer de gewenste aanbieding(en) en kies het publiek dat u in aanmerking wilt nemen om dat aanbod te zien.

   Als u de doelversie voor één aanbieding wilt instellen, houdt u de muisaanwijzer boven de gewenste aanbieding en klikt u op het pictogram **[!UICONTROL Targeting]**.

   Als u de doelversie voor meerdere aanbiedingen wilt instellen, schakelt u de selectievakjes voor de gewenste aanbiedingen in en klikt u op het pictogram **[!UICONTROL Targeting] dat rechtsboven in de lijst wordt weergegeven.

1. Selecteer in het dialoogvenster [!UICONTROL Choose Audience] de gewenste doelgroep(en) voor de aanbieding(en) en klik vervolgens op **[!UICONTROL Done]** om terug te keren naar het dialoogvenster [!UICONTROL Manage Content].

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie [Meerdere soorten publiek combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) voor meer informatie.

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt 50 locaties en maximaal 250 aanbiedingen per locatie instellen.
