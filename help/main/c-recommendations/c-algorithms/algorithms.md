---
keywords: aanbevelingen;aanbevelingen activiteit;criteria;algoritme;aanbeveling sleutel;douane sleutel;industrie verticaal;kleinhandel;handel;lood generatie;b2b;financiële diensten;media;het publiceren
description: Meer informatie over het gebruik van criteria in Adobe [!DNL Target] [!DNL Recommendations].
title: Hoe gebruik ik criteria in [!DNL Target] Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Criteria

Criteria in [!DNL Adobe Target] [!DNL Recommendations] zijn regels die bepalen welke producten of inhoud moet worden aanbevolen op basis van een vooraf bepaalde set gedragingen van bezoekers. De criteria kunnen op populaire tendensen, het huidige en vroegere gedrag van een bezoeker, of gelijkaardige producten en inhoud worden gebaseerd. U kunt veelvoudige aanbevelingstypes tegen elkaar testen door veelvoudige criteria toe te voegen.

In de volgende secties wordt meer uitgelegd over criteria en de logica van de aanbeveling die u voor elke toets kunt gebruiken. Klik op de koppelingen voor meer informatie.

## Verticale industrie {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Terwijl het creëren van criteria, selecteert u een industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

| Verticale industrie | Goal |
|--- |--- |
| Detailhandel/e-handel | Conversie die tot aankoop leidt |
| Genereren van leads/B2B/Financiële services | Omzetten zonder aankoop |
| Media/Publiceren | Betrokkenheid |

Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert. U kunt de standaardindustrie verticaal instellen op de **[!UICONTROL Recommendations > Settings]** of u kunt de industrie verticaal voor elke criteria specificeren.

## Type algoritme {#section_885B3BB1B43048A88A8926F6B76FC482}

Het algoritmetype dat u selecteert, bepaalt de beschikbare algoritmen. Er zijn verscheidene algoritmenypes die als criteria kaarten worden vertegenwoordigd wanneer u opstelling een [!DNL Recommendations] activiteit.

![Criteria pagina](assets/criteria-page.png)

In de volgende tabel worden de verschillende algoritmische typen en de bijbehorende algoritmen beschreven.

| Het type Algorithm | Wanneer gebruiken | Beschikbare algoritmen |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Aanbevelingen doen op basis van de inhoud van het winkelwagentje van de gebruiker. | <ul><li>Personen die ze bekeken, bekeken ze</li><li>Mensen die ze bekeken, kochten hen</li><li>Mensen die deze hebben gekocht, hebben de</li></ul>Zie voor meer informatie [Op basis van winkelwagentje](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *De aanbeveling baseren op een aanbevelingen*. |
| [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. | <ul><li>Meest bekeken op de site</li><li>Meest bekeken op rubriek</li><li>Meest bekeken door kenmerk Item</li><li>Topverkopers op de hele site</li><li>Topverkopers op rubriek</li><li>Topverkopers op objectkenmerk</li><li>Metrisch, boven op Analytics</li></ul> |
| [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. | <ul><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Mensen die dit bekeken hebben, hebben het volgende gekocht</li><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Objecten met vergelijkbare kenmerken</li></ul> |
| [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. | <ul><li>Onlangs bekeken objecten</li><li>Aanbevolen voor u</li></ul> |
| [!UICONTROL Custom Criteria] | Aanbevelingen doen op basis van een aangepast bestand dat u uploadt. | <ul><li>Aangepast algoritme</li></ul> |

Voor meer informatie over elk algoritme, zie [De aanbeveling baseren op een aanbevelingen](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Een aangepaste aanbevolen toets gebruiken {#custom-key}

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel ook baseren.

>[!NOTE]
>
>Aangepaste profielparameters kunnen worden doorgegeven aan [!DNL Target] via JavaScript, API of integratie. Zie voor meer informatie over aangepaste profielkenmerken [Bezoekerprofielen](/help/main/c-target/c-visitor-profile/visitor-profile.md).

Stel dat u aanbevolen films wilt weergeven op basis van de film die een gebruiker het laatst aan de wachtrij heeft toegevoegd.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Vul de gegevens in in de [Sectie Basisinformatie](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info).

1. In de [Aanbevolen algoritme](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) sectie, selecteert u **[!UICONTROL Item Based]** van de **[!UICONTROL Algorithm Type]** lijst.

1. Selecteren **[!UICONTROL People Who Viewed This, Viewed That]** van de **[!UICONTROL Algorithm]** lijst.

1. Selecteer het aangepaste profielkenmerk in het menu **[!UICONTROL Recommendation Key]** list (bijvoorbeeld [!UICONTROL Last Show Added to Watchlist]).

   ![Nieuwe criteria maken, dialoogvenster](assets/custom-key1.png)

## Informatie over criteria weergeven {#section_7162DE58E4594FD688A4D7FDB829FD8B}

U kunt de details van de criteria weergeven op een pop-upkaart door de muisaanwijzer op een kaart te plaatsen en door op het pictogram Informatie op een kaart te klikken zonder de criteria te hoeven openen.

![Toetsenbord](/help/main/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klik op de knop **[!UICONTROL Algorithm Info]** -tabblad voor algemene informatie over de geselecteerde criteria, zoals de naam, beschrijvingen, Verticaal, Paginatype(n), Aanbeveling-sleutel, Aanbevelingenlogica en Algoritme-id.

![Tabblad Algorituurinfo](/help/main/c-recommendations/c-algorithms/assets/criteria_info.png)

Klik op de knop **[!UICONTROL Algorithm Usage]** om een lijst weer te geven met activiteiten die naar de geselecteerde criteria verwijzen. De kaart maakt een lijst van actieve, inactieve, en ontwerp activiteiten. Klik op de vervolgkeuzelijsten Live-activiteiten/Inactieve activiteiten/Conceptactiviteiten om de volledige lijst met activiteiten te bekijken waarin naar die criteria wordt verwezen. U kunt op de koppeling naar de activiteit klikken om de activiteit voor bewerken te openen.

![Het tabblad Algoritmegebruik](/help/main/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>De [!UICONTROL Algorithm Usage] Deze functie wordt momenteel alleen ondersteund voor Recommendations-activiteiten. Deze functie wordt momenteel niet ondersteund voor activiteiten van het type A/B Test, Auto-Allocate, Auto-Target en Experience Targeting (XT) die omvatten [aanbevelingen als aanbod](/help/main/c-recommendations/recommendations-as-an-offer.md).
