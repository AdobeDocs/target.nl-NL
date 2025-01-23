---
keywords: geautomatiseerde personalisatie;aanbiedingen;target;publiek;het richten van regels;het richten van gericht
description: Ontdek hoe u afzonderlijke aanbiedingen kunt richten op specifieke doelgroepen met behulp van [!UICONTROL Automated Personalization] (AP)-activiteiten.
title: Hoe kan ik [!UICONTROL Automated Personalization] aanbiedingen richten?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Automated Personalization
solution: Target,Analytics
hide: true
hidefromtoc: true
exl-id: 2897c4d1-116d-483c-8fc0-64857b9cbdaf
source-git-commit: 2c10ec521ceed1901ef8c3f95eb11654a7182590
workflow-type: tm+mt
source-wordcount: '370'
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

1. Creeer of geef een [ activiteit van Automated Personalization ](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) uit die de aanbiedingen bevat die u wilt richten.
1. Na vestiging klikken de aanbiedingen voor de activiteit in [!UICONTROL Visual Experience Composer], het **[!UICONTROL Manage Content]** pictogram ( ![ leidt het pictogram van de Inhoud ](/help/main/assets/icons/Experience.svg)).

   Het dialoogvenster [!UICONTROL Manage Content] wordt weergegeven.

1. Klik op de tab **[!UICONTROL Offers]** .

1. Selecteer de gewenste aanbiedingen en kies vervolgens het publiek dat u in aanmerking wilt nemen om dat aanbod te zien.

   Aan opstelling richtend voor één enkele aanbieding, klik Meer Info ( ![ Meer pictogram van Info ](/help/main/assets/icons/MoreSmallList.svg)) naast de gewenste aanbieding, dan klik **[!UICONTROL Target Audience]** om de [!UICONTROL Add Audiences] dialoogdoos te tonen.

   Als u de doelgroep voor meerdere aanbiedingen wilt instellen, schakelt u de selectievakjes voor de gewenste aanbiedingen in en klikt u op de koppeling **[!UICONTROL Target Audience]** die onder aan de lijst wordt weergegeven.

1. Selecteer in het dialoogvenster [!UICONTROL Add Audiences] het gewenste publiek voor de aanbiedingen en klik vervolgens op **[!UICONTROL Assign Audience]** om terug te keren naar het dialoogvenster [!UICONTROL Manage Content] .

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om op aanvraag gecombineerde soorten publiek te maken in plaats van een nieuw publiek te maken. Voor meer informatie, zie [ Combinerend Veelvoudige Soorten publiek ](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Klik op **[!UICONTROL Done]**.

>[!NOTE]
>
>U kunt 50 locaties en maximaal 250 aanbiedingen per locatie instellen.
