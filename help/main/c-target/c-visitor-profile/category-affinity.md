---
keywords: affiniteit;categorie-affiniteit
description: Meer informatie over rubriekaffiniteit in [!DNL Adobe Target] die automatisch categorieën vastlegt die een gebruiker bezoekt en vervolgens de affiniteit van de gebruiker voor de categorie berekent, zodat deze kan worden geactiveerd en gesegmenteerd.
title: Wat is rubriekaffiniteit?
feature: Audiences
exl-id: 9478a7fb-e4b5-46d9-be73-b72cb99c3e5e
source-git-commit: 80481a149d436f13bd510c4c4287d447799afbb4
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 3%

---

# Categorie-affiniteit

De categorie affiniteit in [!DNL Adobe Target] legt automatisch de categorieën vast op uw site die een gebruiker bezoekt en berekent vervolgens de affiniteit van de gebruiker voor elke categorie zodat deze kan worden aangewezen en gesegmenteerd. Categorie-affiniteit helpt ervoor te zorgen dat de inhoud gericht is op bezoekers die waarschijnlijk op die informatie reageren.

## Informatie over categorie-affiniteit overbrengen naar [!DNL Target] {#section_B0C8E46EEBAC4549AD90352A47787D04}

Wanneer een gebruiker uw site bezoekt, worden de profielparameters die specifiek zijn voor de bezoeker vastgelegd in het dialoogvenster [!DNL Target] database. Deze gegevens zijn gekoppeld aan de cookie van de gebruiker. Eén nuttige parameter is `user.categoryId`, een mbox-parameter die op een productpagina is toegewezen. Terwijl de bezoeker doorbladert of voor een andere sessie terugkeert, kunnen de productcategorieën van een bepaalde gebruikersweergave worden opgenomen. U kunt ook categoriegegevens opnemen door deze als parameter mbox door te geven `user.categoryId` in elke mbox (inclusief een genest mbox), als een URL-parameter `user.categoryId`, of in [!DNL Target] paginaparameters met een globale mbox. Raadpleeg uw accountvertegenwoordiger voor meer informatie.

Afzonderlijke rubrieken met een komma om een object in meerdere rubrieken op te nemen. Bijvoorbeeld:

* `user.categoryId=clothing,shoes,nike,running,nike clothing,nike shoes,nike running shoes`

Op basis van de frequentie en de frequentie van bezoeken aan de productcategorieën wordt de categoriaffiniteit (indien van toepassing) geregistreerd die een gebruiker heeft. De affiniteit van de categorie kan worden gebruikt om populaties voor uw activiteiten te richten.

U kunt `user.categoryAffinities[]` in een profielscript om een array met affiniteiten te retourneren die een bezoeker heeft gevuld. Zie voor meer informatie [user.categoryAffinities onder Objecten en methoden in Profielkenmerken](/help/main/c-target/c-visitor-profile/profile-parameters.md#objects).

>[!IMPORTANT]
>
>De `user.categoryId` het kenmerk dat wordt gebruikt voor het algoritme voor affiniteit van de categorie, verschilt van het kenmerk dat wordt gebruikt voor het algoritme voor affiniteit `entity.categoryId` kenmerk gebruikt voor [!DNL Adobe Target Recommendations]aanbevelingen voor producten en inhoud. `user.categoryId` is vereist om de favoriete rubriek van een gebruiker bij te houden. `entity.categoryId` is vereist om aanbevelingen te baseren op de categorie van de huidige pagina of van het huidige item. Geef beide waarden door [!DNL Target] als u beide mogelijkheden wilt gebruiken.

## Bedrijfscase voor categorieaffiniteit {#section_D6FF913E88E6486B8FBCE117CA8B253B}

De activiteit van een bezoeker in één zitting, zoals welke categorie zij het vaakst bekijken, kan worden gebruikt voor het richten in volgende bezoeken. Elke categoriepagina bevat een bezoeker die tijdens een sessie weergeeft, en zijn of haar categorie &quot;favoriet&quot; wordt berekend op basis van een recentiemodel en een frequentiemodel. Telkens wanneer de bezoeker terugkeert naar de homepage, kan het hoofdafbeeldingsgebied worden gebruikt om inhoud weer te geven die betrekking heeft op de favoriete categorie van die gebruiker.

## Voorbeeld van het gebruik van een categorie-affiniteit {#section_A4AC0CA550924CB4875F4F4047554C18}

Stel dat u muziekinstrumenten online verkoopt en verkoopbevorderende acties op basis van gitaren wilt richten op bezoekers die in het verleden al belangstelling voor gitaren hebben geuit. Met de affiniteit Categorie kunt u aanbiedingen maken die alleen worden weergegeven aan bezoekers met deze affiniteit Categorie.

## Categorieaffiniteitalgoritme {#section_8B86C7FF50294208866ABF16F07D5EB9}

Het categorieaffiniteitsalgoritme werkt als volgt:

* Tien punten voor de eerste bekeken categorie
* Vijf punten voor elke categorie die na de eerste
* Wanneer op een nieuwe categorie wordt geklikt, wordt 1 afgetrokken van alle eerder geklikte categorieën
* Als er al op een categorie is geklikt (weergegeven), wordt 1 van alle andere categorieën niet verwijderd als u er nogmaals op klikt
* Als op een zesde nieuwe categorie wordt geklikt, wordt de laagste scorecategorie van de eerste vijf categorieën uit de berekening verwijderd
* Verdeel aan het einde van de sessie alle waarden door 2

>[!NOTE]
>
>Wanneer verscheidene categorieën binnen één enkele brievenbusvraag worden overgegaan, de orde van categorieën in `categoryAffinities` is niet gegarandeerd. Een willekeurige categorie wordt eerst opgenomen en krijgt een score van 10.

### Voorbeeld: categorieaffiniteitalgoritme

Als u bijvoorbeeld de `mens-clothing` categorie, dan `accessories`vervolgens `jewelry`vervolgens `accessories` opnieuw tijdens een zitting heeft de commissie de volgende affiniteiten :

* `accessories`: 9 (+5 - 1 + 5)

* `mens-clothing`: 8 (+10 - 1 - 1)

* `jewelry`: 5 (+5)

Wanneer de sessie wordt beëindigd en de gebruiker later terugkeert naar de site, worden de scores gehalveerd:

* `accessories`: 4,5 (9/2)

* `mens-clothing`: 4 (8/2)

* `jewelry`: 2,5 (5/2)

Ervan uitgaande dat de gebruiker dan de volgorde volgt, `jewelry`, `accessories`, `beauty`, `shoes`, en `womens-clothing`:

* `accessories`: 6,5 (4,5 + 5 - 1 - 1 - 1)

* `womens-clothing`: 5 (+5)

* `jewelry`: 4.5 (2.5 + 5 - 1 - 1 - 1)

* `shoes`: 4 (+5 - 1)

* `beauty`: 3 (+5 - 1 - 1)

* `mens-clothing` wordt verwijderd na de laatste klik van `womens-clothing` als laagste scoringcategorie met een score van 1 (4 - 1 - 1 - 1)

Wanneer de sessie wordt beëindigd en de gebruiker later terugkeert naar de site, worden de scores gehalveerd:

* `accessories`: 3.3 (6.5/2)

* `womens-clothing`: 2,5 (5/2)

* `jewelry`: 2,3 (4,5/2)

* `shoes`: 2 (4/2)

* `beauty`: 1,5 (3/2)

## Categorieaffiniteit gebruiken voor doelversie {#concept_5750C9E6C97A40F8B062A5C16F2B5FFC}

De volgende secties bevatten informatie om u te helpen een publiek van de categoriaffiniteit voor het richten in een activiteit gebruiken.

### Een publiek maken om de affiniteit van categorieën te gebruiken {#section_A27C600BBA664FE7A74F8FE076B78F40}

1. Van de **[!UICONTROL Audiences]** lijst, klikt u op **[!UICONTROL Create Audience]**.

   of

   Als u een bestaand publiek wilt kopiëren, houdt u de muisaanwijzer boven het gewenste publiek en klikt u op het pictogram Kopiëren in de lijst Soorten publiek. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een beschrijvende publieksnaam.
1. Klik op **[!UICONTROL + Add Rule]** > **[!UICONTROL Visitor Profile]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Visitor Profile]** de optie **[!UICONTROL Category Affinity]**.

   ![Bezoekersprofiel > Categorie-affiniteit](assets/affinity.png)

1. Selecteer de gewenste categorie:

   ![Categorie-affiniteit > Categorie](assets/affinity-category.png)

   Tot de categorieën behoren:

   * Favoriete rubriek
   * Eerste rubriek
   * Tweede rubriek
   * Derde rubriek
   * Vierde categorie
   * Vijfde categorie

   De opties Favoriete rubriek en Eerste rubriek zijn gelijk.

1. Kies de evaluator:

   * Bevat (hoofdlettergevoelig)
   * Bevat niet (hoofdlettergevoelig)
   * Gelijk

1. Geef elke nieuwe waarde op een aparte regel (bijvoorbeeld &quot;schoenen&quot;).
1. Klik op **[!UICONTROL Save]**.

### Het publiek met de affiniteit van de categorie gebruiken in een activiteit {#section_91526B942D1B4AEBB8FCDF4EBFF931CF}

U kunt het publiek met affiniteit gebruiken in elke activiteit. Tijdens de driestapsgestuurde workflow kunt u het volgende doen: [!UICONTROL Target] kiest u het gewenste publiek.
