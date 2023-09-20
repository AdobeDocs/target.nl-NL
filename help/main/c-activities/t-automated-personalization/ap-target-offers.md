---
keywords: geautomatiseerde personalisatie;aanbiedingen;target;publiek;het richten van regels;het richten van gericht
description: Leer hoe u afzonderlijke aanbiedingen kunt richten op specifieke doelgroepen met behulp van een [!UICONTROL Automated Personalization] (AP) activiteit in [!DNL Adobe Target].
title: Hoe kan ik het doel bepalen [!UICONTROL Automated Personalization] Aanbiedingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 1%

---

# Doel [!UICONTROL Automated Personalization] aanbiedingen

In een [!DNL Adobe Target] [!DNL Automated Personalization] (AP) activiteit, kunt u aanbiedingen aan specifiek publiek richten.

Als u deze functie gebruikt, verkleint u het aantal aanbiedingen dat een specifieke bezoeker kan zien. Neem bijvoorbeeld een [!UICONTROL Automated Personalization] activiteit met drie aanbiedingen. Aanbieding 1 heeft een richtingsregel die zijn blootstelling aan Publiek A beperkt. Twee bezoekers zagen deze activiteit.

| | Bezoeker 1 | Bezoeker 2 |
|--- |--- |--- |
| kwalificatie publiek | Publiek A | Publiek B |
| Aanbieding 1 Doel-verpersoonlijkingsmodelscore | 90 | 90 |
| Aanbieding 2 score voor doel-verpersoonlijkingsmodel | 50 | 70 |
| Aanbieding 3 Streefverpersoonlijkingsmodelscore | 80 | 60 |

In dit scenario ziet bezoeker 1 aanbod 1 (omdat deze bezoeker in aanmerking komt als onderdeel van Audience A), wat de hoogste score van die bezoeker is. Visitor 2 ziet echter Aanbieding 2, ook al is de hoogste score voor Aanbieding 1, omdat Visitor 2 geen deel uitmaakt van Audience A. Dit voorbeeld toont aan waarom het richten van regels spaarzaam zou moeten worden gebruikt om aan bedrijfsbehoeften te voldoen. Het toevoegen van deze regels kan de doeltreffendheid van [!DNL Target] personalisatiemodellen.

## Doelstellingen instellen

1. Een [Automated Personalization-activiteit](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) bevat de aanbiedingen waarop u zich wilt richten.
1. Nadat u de aanbiedingen voor de activiteit in de [!UICONTROL Visual Experience Composer], klikt u op **[!UICONTROL Manage Content]**.

   ![Inhoud beheren](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   De [!UICONTROL Manage Content] wordt weergegeven.

1. Klik op de knop **[!UICONTROL Offers]** tab.

   ![Pagina met aanbiedingen](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Selecteer de gewenste aanbiedingen en kies vervolgens het publiek dat u in aanmerking wilt nemen om dat aanbod te zien.

   Als u een abonnement wilt nemen op één aanbieding, houdt u de muisaanwijzer boven het gewenste aanbod en klikt u op de knop **[!UICONTROL Targeting]** pictogram.

   Als u een keuze wilt maken voor meerdere aanbiedingen, schakelt u de selectievakjes voor de gewenste aanbiedingen in en klikt u op de knop **[!UICONTROL Targeting]** pictogram dat rechtsboven in de lijst wordt weergegeven.

1. In de [!UICONTROL Choose Audience] , selecteert u het gewenste publiek voor de aanbiedingen en klikt u vervolgens op **[!UICONTROL Done]** om terug te keren naar de [!UICONTROL Manage Content] in.

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie voor meer informatie [Meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt 50 locaties en maximaal 250 aanbiedingen per locatie instellen.
