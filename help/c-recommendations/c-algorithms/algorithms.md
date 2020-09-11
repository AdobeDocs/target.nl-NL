---
keywords: recommendations;recommendations activity;criteria;algorithm;recommendation key;custom key;industry vertical;retail;eccommerce;lead generation;b2b;financial services;media;publishing
description: Criteria in Adobe Target zijn regels die bepalen welke producten of inhoud moet worden aanbevolen op basis van een vooraf bepaalde set gedragingen van bezoekers.
title: Criteria in Adobe Target Recommendations
feature: criteria
uuid: 738db164-174b-45b8-bb8a-778f6494f1d7
translation-type: tm+mt
source-git-commit: d276693eeab095b7f2f5fad293a03ab10eb1faf6
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Criteria

Criteria in [!DNL Adobe Target] zijn regels die bepalen welke producten of inhoud moet worden aanbevolen op basis van een vooraf bepaalde set gedragingen van bezoekers. De criteria kunnen op populaire tendensen, het huidige en vroegere gedrag van een bezoeker, of gelijkaardige producten en inhoud worden gebaseerd. U kunt veelvoudige aanbevelingstypes tegen elkaar testen door veelvoudige criteria toe te voegen.

In de volgende secties wordt meer uitgelegd over criteria en de logica van de aanbeveling die u voor elke toets kunt gebruiken. Klik op de koppelingen voor meer informatie.

## Verticale industrie {#section_936BCFCF234C49A2BEC1C38AAC2D71AF}

Terwijl het creëren van criteria, selecteert u een industrie verticaal die op de doelstellingen van uw aanbevelingen activiteit wordt gebaseerd.

| Verticale industrie | Goal |
|--- |--- |
| Detailhandel/e-handel | Conversie die tot aankoop leidt |
| Genereren van leads/B2B/Financiële services | Omzetten zonder aankoop |
| Media/Publiceren | Betrokkenheid |

Andere criteria worden gewijzigd op basis van de verticale industriestandaard die u selecteert. U kunt uw standaardindustrie verticaal op de **[!UICONTROL Recommendations > Settings]** pagina plaatsen of u kunt de industrie verticaal voor elke criteria specificeren.

## Aanbevelingssleutel {#section_885B3BB1B43048A88A8926F6B76FC482}

Het type criteria wordt bepaald door de toets die u voor de aanbeveling selecteert. Er zijn verschillende soorten criteria, die als criteria worden voorgesteld wanneer u een [!DNL Recommendations] activiteit instelt.

![Criteria pagina](/help/c-recommendations/c-algorithms/assets/criteria-page.png)

In de volgende tabel worden de verschillende typen criteria en de bijbehorende sleutels uitgelegd. Klik op de koppelingen voor meer informatie over elke toets.

| Criteria Type | Toetsen |
|--- |--- |
| Activiteit huidige pagina | Aanbevolen items op basis van wat gebruikers op de huidige pagina doen. bezoekers die bijvoorbeeld een bepaald artikel bekijken, kunnen andere artikelen uit dezelfde categorie bekijken.<ul><li>[Huidig item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-item)</li><li>[Huidige rubriek](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#current-category)</li></ul> |
| Aangepast | Aanbevolen items op basis van aangepaste kenmerken.<ul><li>[Aangepast kenmerk](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#custom)</li></ul>Wanneer u aanbevelingen baseert op douanekenmerken, moet u het douanekenmerk selecteren en dan het aanbevelingstype selecteren. |
| Gedrag in verleden | Aanbevolen objecten op basis van hoe bezoekers in het verleden op een object hebben gereageerd. Mensen die bijvoorbeeld een bepaald merk hebben aangeschaft, hebben meer kans om een ander product van dat merk te kopen.<ul><li>[Laatst gekocht object](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-purchased)</li><li>[Laatst weergegeven item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#last-viewed)</li><li>[Meest bekeken item](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed-logic)</li><li>[Favoriete rubriek](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#favorite-category)</li></ul> |
| Populariteit | Aanbevelen de populairste items, zoals de populairste video&#39;s in een verwante categorie of de producten die het meest op uw site zijn weergegeven.<ul><li>[Populariteit](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#popularity)</li></ul> |
| [Onlangs bekeken objecten](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#recently-viewed) | Aanbevolen objecten die een bezoeker het laatst heeft bekeken, zoals de objecten die een bezoeker voor het laatst heeft bekeken op het moment dat hij of zij uw site heeft bezocht, of de artikelen die momenteel het meest trending hebben. |

## Een aangepaste aanbevolen toets gebruiken {#custom-key}

U kunt aanbevelingen op de waarde van een attribuut van het douaneprofiel ook baseren.

>[!NOTE]
>
>Aangepaste profielparameters kunnen aan Doel worden doorgegeven via JavaScript, API of integratie. Zie [Bezoekersprofielen](/help/c-target/c-visitor-profile/visitor-profile.md)voor meer informatie over aangepaste profielkenmerken.

Stel dat u aanbevolen films wilt weergeven op basis van de film die een gebruiker het laatst aan de wachtrij heeft toegevoegd.

1. Selecteer het kenmerk Aangepast profiel in de [!UICONTROL Recommendation Key] vervolgkeuzelijst (bijvoorbeeld [!UICONTROL Last Show Added to Watchlist]).

1. Selecteer uw [!UICONTROL Recommendation Logic] (bijvoorbeeld [!UICONTROL People Who Viewed This, Viewed That]).

   ![Nieuwe criteria maken, dialoogvenster](/help/c-recommendations/c-algorithms/assets/custom-key1.png)

Als uw attribuut van het douaneprofiel niet direct met één enkele entiteitidentiteitskaart aanpast, is het noodzakelijk om aan te verklaren [!DNL Recommendations] hoe u de gelijke aan een entiteit wilt voorkomen.

Stel dat u de meest verkochte objecten van het favoriete merk van een gebruiker wilt weergeven.

1. Selecteer het kenmerk Aangepast profiel in de [!UICONTROL Recommendation Key] vervolgkeuzelijst (bijvoorbeeld [!UICONTROL Favorite Brand]).

1. Selecteer de toets die [!UICONTROL Recommendation Logic] u met deze toets wilt gebruiken (bijvoorbeeld [!UICONTROL Top Sellers]).

   De [!UICONTROL Group By Unique Value Of] optie wordt weergegeven.

1. Selecteer het entiteitskenmerk dat overeenkomt met de gekozen sleutel. In dit geval [!UICONTROL Favorite Brand] komt overeen met `entity.brand`.

   [!DNL Recommendations] produceert nu een lijst met &#39;Topverkopers&#39; voor elk merk en geeft de gebruiker de juiste lijst met &#39;Topverkopers&#39; weer op basis van de waarde die is opgeslagen in het [!UICONTROL Favorite Brand] profielkenmerk.

   ![Kenmerk topverkopers](/help/c-recommendations/c-algorithms/assets/custom-key2.png)

## Criteria/algoritmen {#criteria-algorithms}

[!DNL Target Recommendations] gebruikt geavanceerde algoritmen om te bepalen wanneer de acties van een bezoeker voor de criteria in uw activiteit kwalificeren. De advisesleutel bepaalt de aanbevelingen logische opties die beschikbaar zijn.

| Criteria | Beschrijving |
|--- |--- |
| [Items/media met vergelijkbare kenmerken](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#similar-attributes) | Aanbevolen items of media die vergelijkbaar zijn met items of media op basis van de huidige paginageactiviteit of het gedrag van een bezoeker. |
| [Personen die dit hebben bekeken, zagen het volgende](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-viewed) | Hiermee worden items aanbevolen die het vaakst worden weergegeven in dezelfde sessie als waarin het opgegeven item wordt weergegeven. |
| [Mensen die dit bekeken hebben, hebben het volgende gekocht](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#viewed-bought) | raadt objecten aan die het vaakst worden aangeschaft in dezelfde sessie als waarin het opgegeven item wordt weergegeven. |
| [Mensen die dit hebben gekocht, hebben het volgende gekocht](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#bought-bought) | Aanbevolen objecten die het meest door klanten tegelijk met het opgegeven item worden gekocht. |
| [Affiniteit site](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#site-affinity) | Aanbevolen items op basis van de zekerheid van een relatie tussen items. |
| [Topverkopers](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#top-sellers) | De items die zijn opgenomen in de meest voltooide orders. Meerdere eenheden van hetzelfde item in één volgorde worden als één volgorde geteld. |
| [Meest bekeken](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#most-viewed) | De items of media die het vaakst worden weergegeven. |
| [Op gebruiker gebaseerde Recommendations](/help/c-recommendations/c-algorithms/base-the-recommendation-on-a-recommendation-key.md#user-based) | Aanbevolen objecten op basis van de browsergeschiedenis, weergavegeschiedenis en aankoopgeschiedenis van elke bezoeker. Deze objecten worden doorgaans &#39;Aanbevolen voor je&#39; genoemd. |

>[!NOTE]
>
>Als u een aanbeveling uitvoert en de criteria wijzigt, gaan de rapportgegevens verloren.

U kunt ook aanvullende bekende informatie over een bezoeker gebruiken om uw aanbevelingen te verbeteren.

Alle criteria van één dag worden tweemaal daags uitgevoerd. Alle criteria van één week en langer lopen eenmaal per dag. De criteria voor affiniteit van de site worden eenmaal daags uitgevoerd. Back-upcriteria worden tweemaal daags uitgevoerd.

## Informatie over criteria weergeven {#section_7162DE58E4594FD688A4D7FDB829FD8B}

U kunt de details van de criteria weergeven op een pop-upkaart door de muisaanwijzer op een kaart te plaatsen en door op het pictogram Informatie op een kaart te klikken zonder de criteria te hoeven openen.

![Toetsenbord](/help/c-recommendations/c-algorithms/assets/criteria_hover.png)

Klik op het **[!UICONTROL Algorithm Info]** tabblad om algemene informatie weer te geven over de geselecteerde criteria, zoals de naam, beschrijvingen, Verticaal, Paginatype(s), Aanbeveling-sleutel, Aanbeveling-logica en Algorithm-id.

![Tabblad Algorituurinfo](/help/c-recommendations/c-algorithms/assets/criteria_info.png)

Klik op het **[!UICONTROL Algorithm Usage]** tabblad om een lijst weer te geven met activiteiten die naar de geselecteerde criteria verwijzen. De kaart maakt een lijst van actieve, inactieve, en ontwerp activiteiten. Klik op de vervolgkeuzelijsten Live-activiteiten/Inactieve activiteiten/Conceptactiviteiten om de volledige lijst met activiteiten te bekijken waarin naar die criteria wordt verwezen. U kunt op de koppeling naar de activiteit klikken om de activiteit voor bewerken te openen.

![Het tabblad Algoritmegebruik](/help/c-recommendations/c-algorithms/assets/criteria_usage.png)

>[!NOTE]
>
>De [!UICONTROL Algorithm Usage] functie wordt momenteel alleen ondersteund voor Recommendations-activiteiten. Deze functie wordt momenteel niet ondersteund voor activiteiten van het type A/B Test, Auto-Allocate, Auto-Target en Experience Targeting (XT) die [aanbevelingen als aanbieding](/help/c-recommendations/recommendations-as-an-offer.md)bevatten.
