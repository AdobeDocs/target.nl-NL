---
keywords: aanbevelingen;aanbevelingen activiteit;criteria;algoritme;aanbeveling sleutel;douane sleutel;industrie verticaal;kleinhandel;handel;lood generatie;b2b;financiële diensten;media;het publiceren
description: Leer hoe te om criteria in Adobe te gebruiken [!DNL Target] [!DNL Recommendations].
title: Hoe gebruik ik criteria in [!DNL Target] Recommendations?
feature: Recommendations
exl-id: a6e4c857-f991-4293-9d33-8d7c2ca5dade
source-git-commit: 7a52f7c046fb00672ef1b13704308be39f89c7ad
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# ![](/help/assets/premium.png) PREMIUMCCriteria

Criteria in [!DNL Adobe Target] [!DNL Recommendations] zijn regels die bepalen welke producten of inhoud moet worden aanbevolen op basis van een vooraf bepaalde set bezoekersgedrag. De criteria kunnen op populaire tendensen, het huidige en vroegere gedrag van een bezoeker, of gelijkaardige producten en inhoud worden gebaseerd. U kunt veelvoudige aanbevelingstypes tegen elkaar testen door veelvoudige criteria toe te voegen.

In de volgende secties wordt meer uitgelegd over criteria en de logica van de aanbeveling die u voor elke toets kunt gebruiken. Klik op de koppelingen voor meer informatie.

## Verticale industrie {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Terwijl het creëren van criteria, selecteert u een industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

| Verticale industrie | Goal |
|--- |--- |
| Detailhandel/e-handel | Conversie die tot aankoop leidt |
| Genereren van leads/B2B/Financiële services | Omzetten zonder aankoop |
| Media/Publiceren | Betrokkenheid |

Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert. U kunt uw standaardindustrie verticaal op **[!UICONTROL Recommendations > Settings]** pagina plaatsen of u kunt de industrie verticaal voor elke criteria specificeren.

## Type algoritme {#section_885B3BB1B43048A88A8926F6B76FC482}

Het algoritmetype dat u selecteert, bepaalt de beschikbare algoritmen. Er zijn verscheidene algoritmenypes, die als criteria kaarten worden vertegenwoordigd wanneer u opstelling een [!DNL Recommendations] activiteit.

![Criteria pagina](assets/criteria-page.png)

In de volgende tabel worden de verschillende algoritmische typen en de bijbehorende algoritmen beschreven.

| Het type Algorithm | Wanneer gebruiken | Beschikbare algoritmen |
| --- | --- | --- |
| [!UICONTROL Popularity-Based] | Aanbevelingen doen op basis van de algemene populariteit van een item op uw site of op basis van de populariteit van items in de favoriete of meest bekeken categorie, het merk, het genre enzovoort van een gebruiker. | <ul><li>Meest bekeken op de site</li><li>Meest bekeken op rubriek</li><li>Meest bekeken door kenmerk Item</li><li>Topverkopers op de hele site</li><li>Topverkopers op rubriek</li><li>Topverkopers op objectkenmerk</li><li>Metrisch, boven op Analytics</li></ul> |
| [!UICONTROL Item-Based] | Aanbevelingen doen op basis van het zoeken naar objecten die vergelijkbaar zijn met een item dat de gebruiker momenteel bekijkt of onlangs heeft bekeken. | <ul><li>Personen die dit hebben bekeken, zagen het volgende</li><li>Mensen die dit bekeken hebben, hebben het volgende gekocht</li><li>Mensen die dit hebben gekocht, hebben het volgende gekocht</li><li>Objecten met vergelijkbare kenmerken</li></ul> |
| [!UICONTROL User-Based] | Aanbevelingen doen op basis van het gedrag van de gebruiker. | <ul><li>Onlangs bekeken objecten</li><li>Aanbevolen voor u</li></ul> |
| Op basis van winkelwagentje | (Binnenkort beschikbaar) Aanbevelingen doen op basis van de inhoud van het winkelwagentje van de gebruiker. | <ul><li>Personen die ze bekeken, bekeken ze</li><li>Mensen die ze bekeken, kochten hen</li><li>Mensen die deze hebben gekocht, hebben de</li></ul> |
| [!UICONTROL Custom Criteria] | Aanbevelingen doen op basis van een aangepast bestand dat u uploadt. | <ul><li>Aangepast algoritme</li></ul> |

Voor meer informatie over elk algoritme, zie [Baseer de aanbeveling op een aanbeveling sleutel](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md).

## Een aangepaste aanbevolen toets gebruiken {#custom-key}

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel ook baseren.

>[!NOTE]
>
>Aangepaste profielparameters kunnen worden doorgegeven aan [!DNL Target] via JavaScript, API of integratie. Zie [Bezoekersprofielen](/help/c-target/c-visitor-profile/visitor-profile.md) voor meer informatie over kenmerken van aangepaste profielen.

Stel dat u aanbevolen films wilt weergeven op basis van de film die een gebruiker het laatst aan de wachtrij heeft toegevoegd.

1. Klik op **[!UICONTROL Recommendations]** > **[!UICONTROL Criteria]**.

1. Klik op **[!UICONTROL Create Criteria]** > **[!UICONTROL Create Criteria]**.

1. Vul de informatie in [Basisinformatie sectie](/help/c-recommendations/c-algorithms/create-new-algorithm.md#info) in.

1. Selecteer **[!UICONTROL Item Based]** in de lijst [Aanbevolen algoritme](/help/c-recommendations/c-algorithms/create-new-algorithm.md#rec-algo) in de sectie **[!UICONTROL Algorithm Type]**.

1. Selecteer **[!UICONTROL People Who Viewed This, Viewed That]** in de lijst **[!UICONTROL Algorithm]**.

1. Selecteer het kenmerk Aangepast profiel in de lijst **[!UICONTROL Recommendation Key]** (bijvoorbeeld [!UICONTROL Last Show Added to Watchlist]).

   ![Nieuwe criteria maken, dialoogvenster](assets/custom-key1.png)

## Informatie over criteria weergeven {#section_7162DE58E4594FD688A4D7FDB829FD8B}

U kunt de details van de criteria weergeven op een pop-upkaart door de muisaanwijzer op een kaart te plaatsen en door op het pictogram Informatie op een kaart te klikken zonder de criteria te hoeven openen.

![Toetsenbord](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klik op het tabblad **[!UICONTROL Algorithm Info]** om algemene informatie weer te geven over de geselecteerde criteria, zoals de naam, beschrijvingen, Verticaal, Paginatype(s), Aanbeveling-sleutel, Aanbeveling-logica en Algorithm-id.

![Tabblad Algorituurinfo](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Klik op het tabblad **[!UICONTROL Algorithm Usage]** om een lijst weer te geven met activiteiten die naar de geselecteerde criteria verwijzen. De kaart maakt een lijst van actieve, inactieve, en ontwerp activiteiten. Klik op de vervolgkeuzelijsten Live-activiteiten/Inactieve activiteiten/Conceptactiviteiten om de volledige lijst met activiteiten te bekijken waarin naar die criteria wordt verwezen. U kunt op de koppeling naar de activiteit klikken om de activiteit voor bewerken te openen.

![Het tabblad Algoritmegebruik](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>De functie [!UICONTROL Algorithm Usage] wordt momenteel alleen ondersteund voor Recommendations-activiteiten. Deze functie wordt momenteel niet ondersteund voor activiteiten van het type A/B Test, Auto-Allocate, Auto-Target en Experience Targeting (XT) die [aanbevelingen als aanbieding](/help/c-recommendations/recommendations-as-an-offer.md) omvatten.
