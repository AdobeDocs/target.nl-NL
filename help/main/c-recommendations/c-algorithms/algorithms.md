---
keywords: aanbevelingen;aanbevelingen activiteit;criteria;algoritme;aanbeveling sleutel;douane sleutel;industrie verticaal;kleinhandel;handel;lood generatie;b2b;financiële diensten;media;het publiceren
description: Leer hoe te om criteria in Adobe  [!DNL Target] [!DNL Recommendations] te gebruiken.
title: Hoe gebruik ik Criteria in  [!DNL Target]  Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: 02ffe8da6cdf96039218656b9690fa719a77910c
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# [!UICONTROL Criteria]

[!UICONTROL Criteria] in [!DNL Adobe Target] [!DNL Recommendations] zijn regels die bepalen welke producten of inhoud moeten worden aanbevolen op basis van een vooraf bepaalde set gedragingen van bezoekers. De criteria kunnen op populaire tendensen, het huidige en vroegere gedrag van een bezoeker, of gelijkaardige producten en inhoud worden gebaseerd. U kunt veelvoudige aanbevelingstypes tegen elkaar testen door veelvoudige criteria toe te voegen.

In de volgende secties wordt meer uitgelegd over de criteria en de logica van de aanbeveling die u voor elke toets kunt gebruiken. Klik op de koppelingen voor meer informatie.

## Verticale industrie {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Terwijl het creëren van criteria, selecteert u een industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

| Verticale industrie | Goal |
|--- |--- |
| [!UICONTROL Retail/Ecommerce] | Conversie die tot aankoop leidt |
| [!UICONTROL Lead Generation/B2B/Financial Services] | Omzetten zonder aankoop |
| [!UICONTROL Media/Publishing] | Betrokkenheid |

Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert. U kunt de standaardindustrie verticaal plaatsen op de **[!UICONTROL Administration]>[!UICONTROL Recommendations]** pagina of u kunt de industrie verticaal voor elke criteria specificeren.

## Type algoritme {#section_885B3BB1B43048A88A8926F6B76FC482}

Het algoritmetype dat u selecteert, bepaalt de beschikbare algoritmen.

In de volgende tabel worden de verschillende algoritmische typen en de bijbehorende algoritmen beschreven.

| Het type Algorithm | Wanneer gebruiken | Beschikbare algoritmen |
| --- | --- | --- |
| [!UICONTROL Cart-Based] | Aanbevelingen doen op basis van de inhoud van het winkelwagentje. | <ul><li>[!UICONTROL People Who Viewed These, Also Viewed]</li><li>[!UICONTROL People Who Viewed These, Also Bought]</li><li>[!UICONTROL People Who Bought These, Also Bought]</li></ul>Voor meer informatie, zie [&#x200B; op klei-Gebaseerd &#x200B;](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#cart-based) in *Baseer de aanbeveling op een aanbeveling sleutel*. |
| [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. | <ul><li>[!UICONTROL Most Viewed Across the Site]</li><li>[!UICONTROL Most Viewed by Category]</li><li>[!UICONTROL Most Viewed by Item Attribute]</li><li>[!UICONTROL Top Sellers Across the Site]</li><li>[!UICONTROL Top Sellers by Category]</li><li>[!UICONTROL Top Sellers by Item Attribute]</li><li>[!UICONTROL Top by Analytics Metric]</li></ul> |
| [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. | <ul><li>[!UICONTROL People Who Viewed This, Viewed That]</li><li>[!UICONTROL People Who Viewed This, Bought That]</li><li>[!UICONTROL People Who Bought This, Bought That]</li><li>[!UICONTROL Items with Similar Attributes]</li></ul> |
| [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. | <ul><li>[!UICONTROL Recently Viewed Items]</li><li>[!UICONTROL Recommended for You]</li></ul> |
| [!UICONTROL Custom Criteria] | Aanbevelingen doen op basis van een aangepast bestand dat u uploadt. | <ul><li>Aangepast algoritme</li></ul> |

Voor meer informatie over elk algoritme, zie [&#x200B; Baseer de aanbeveling op een aanbeveling sleutel &#x200B;](/help/main/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Een aangepaste aanbevolen toets gebruiken {#custom-key}

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel ook baseren.

>[!NOTE]
>
>Aangepaste profielparameters kunnen worden doorgegeven aan [!DNL Target] via JavaScript, API of integratie. Voor meer informatie over de attributen van het douaneprofiel, zie {profielen van 0} Bezoeker [.](/help/main/c-target/c-visitor-profile/visitor-profile.md)

Stel dat u aanbevolen films wilt weergeven op basis van de film die een gebruiker het laatst aan de wachtrij heeft toegevoegd.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]** .

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]** .

1. Vul de informatie in de [&#x200B; Basissectie van de Informatie &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#info) in.

1. In de [&#x200B; Geadviseerde sectie van het Algoritme &#x200B;](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo), uitgezochte **[!UICONTROL Item Based]** van de **[!UICONTROL Algorithm Type]** lijst.

1. Selecteer **[!UICONTROL People Who Viewed This, Viewed That]** in de lijst **[!UICONTROL Algorithm]** .

1. Selecteer het aangepaste profielkenmerk in de lijst **[!UICONTROL Recommendation Key]** (bijvoorbeeld [!UICONTROL Last Show Added to Watchlist] ).

## Informatie over criteria weergeven {#section_7162DE58E4594FD688A4D7FDB829FD8B}

U kunt de details van de criteria weergeven door op de gewenste criteria in de kolom [!UICONTROL Name] te klikken.

In de secties **[!UICONTROL Attributes]** en Details kunt u algemene informatie weergeven over de geselecteerde criteria, zoals [!UICONTROL Name] , [!UICONTROL Description] , [!UICONTROL Industry Vertical] , [!UICONTROL Page Types] , [!UICONTROL Recommendation Key] , [!UICONTROL Recommendation Logic] , [!UICONTROL Algorithm ID] en Laatst gewijzigd (datum en persoon die het algoritme heeft gewijzigd).

In de sectie **[!UICONTROL Usage]** kunt u een lijst weergeven met activiteiten die naar de geselecteerde criteria verwijzen.

>[!NOTE]
>
>De functie [!UICONTROL Algorithm Usage] wordt momenteel alleen ondersteund voor [!DNL Recommendations] -activiteiten. Deze eigenschap wordt momenteel niet gesteund voor [!UICONTROL A/B Test], [!UICONTROL Auto-Allocate], [!UICONTROL Auto-Target], en [!UICONTROL Experience Targeting] (XT) activiteiten die [&#x200B; aanbevelingen als aanbieding &#x200B;](/help/main/c-recommendations/recommendations-as-an-offer.md) omvatten.
