---
keywords: geautomatiseerde personalisatie;aanbiedingen;target;publiek;het richten van regels;het richten van richten
description: Leer hoe u afzonderlijke aanbiedingen kunt richten op specifieke doelgroepen met behulp van een Automated Personalization-activiteit (AP) in Adobe Target.
title: Hoe kan ik [!DNL Target] Automated Personalization-aanbiedingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: 07062b7df75300bd7558a24da5121df454520e42
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 1%

---

# [!DNL Target] Automated Personalization-aanbiedingen

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

1. Een [Automated Personalization-activiteit](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) met de aanbiedingen waarop u zich wilt richten.
1. Na vestiging de aanbiedingen voor de activiteit in de Visuele Composer van de Ervaring **[!UICONTROL Manage Content]**.

   ![Inhoud beheren](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Het dialoogvenster Inhoud beheren wordt geopend.

1. Klik op het tabblad Aanbiedingen.

   ![Aanbiedingspagina](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Selecteer de gewenste aanbieding(en) en kies het publiek dat u in aanmerking wilt nemen om dat aanbod te zien.

   Als u een abonnement wilt nemen op één aanbieding, houdt u de muisaanwijzer boven het gewenste aanbod en klikt u op de knop **[!UICONTROL Targeting]** pictogram.

   Als u de doelgroep voor meerdere aanbiedingen wilt instellen, schakelt u de selectievakjes voor de gewenste aanbiedingen in en klikt u op **[!UICONTROL Targeting] pictogram dat rechtsboven in de lijst wordt weergegeven.

1. In de [!UICONTROL Choose Audience] , selecteert u de gewenste doelgroep(en) voor de aanbieding(en) en klikt u op **[!UICONTROL Done]** om terug te keren naar de [!UICONTROL Manage Content] in.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie voor meer informatie [Meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt 50 locaties en maximaal 250 aanbiedingen per locatie instellen.
