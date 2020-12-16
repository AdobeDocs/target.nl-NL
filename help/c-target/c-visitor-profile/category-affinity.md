---
keywords: affinity;category affinity
description: Met de functie voor categorieaffiniteit in Adobe Target worden automatisch de categorieën vastgelegd die een gebruiker bezoekt en wordt vervolgens de affiniteit van de gebruiker voor de categorie berekend, zodat deze kan worden geactiveerd en gesegmenteerd. Dit helpt ervoor te zorgen dat de inhoud gericht is op bezoekers die het meest waarschijnlijk op die informatie handelen.
title: Categorieaffiniteit gebruiken in Adobe Target
feature: visitor profiles
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 3%

---


# Categorie-affiniteit{#category-affinity}

Met de functie voor affiniteit van categorieën worden automatisch de categorieën vastgelegd die een gebruiker bezoekt en wordt vervolgens de affiniteit van de gebruiker voor de categorie berekend, zodat deze kan worden geactiveerd en gesegmenteerd. Dit helpt ervoor te zorgen dat de inhoud gericht is op bezoekers die het meest waarschijnlijk op die informatie handelen.

## Categorieaffiniteitsgegevens doorgeven aan doel {#section_B0C8E46EEBAC4549AD90352A47787D04}

Wanneer een gebruiker uw site bezoekt, worden profielparameters die specifiek zijn voor de bezoeker opgenomen in de [!DNL Target]-database. Deze gegevens zijn gekoppeld aan de cookie van de gebruiker. Een bijzonder nuttige parameter is `user.categoryId`, een mbox-parameter die op een productpagina is toegewezen. Terwijl de bezoeker doorbladert of voor een andere sessie terugkeert, kunnen de productcategorieën van een bepaalde gebruikersweergave worden opgenomen. U kunt categorieinformatie ook registreren door het als mbox parameter `user.categoryId` in om het even welk vakje (met inbegrip van een genestelde mbox), als URL parameter `user.categoryId`, of in de paginaparameters van het Doel met een globale mbox door te geven. Raadpleeg uw accountvertegenwoordiger voor meer informatie.

Afzonderlijke rubrieken met een komma om een object in meerdere rubrieken op te nemen. Bijvoorbeeld:

* `user.categoryId=clothing,shoes,nike,running,nike clothing,nike shoes,nike running shoes`

Op basis van de frequentie en de frequentie van bezoeken aan de productcategorieën wordt de categoriaffiniteit (indien van toepassing) geregistreerd die een gebruiker heeft. De affiniteit van de categorie kan worden gebruikt om populaties voor uw activiteiten te richten.

U kunt `user.categoryAffinities[]` in een profielmanuscript gebruiken om een serie van de affiniteiten terug te keren die een bezoeker heeft bevolkt.

>[!IMPORTANT]
>
>Het `user.categoryId`-kenmerk dat wordt gebruikt voor het algoritme voor affiniteit van de categorie Adobe Target is anders dan het `entity.categoryId`-kenmerk dat wordt gebruikt voor de aanbevelingen voor producten en inhoud van Adobe Target Recommendations. `user.categoryId` is vereist om de favoriete rubriek van een gebruiker bij te houden. `entity.categoryId` is vereist om aanbevelingen te baseren op de categorie van de huidige pagina of van het huidige item. Geef beide waarden door aan Adobe Target als u beide mogelijkheden wilt gebruiken.

## Bedrijfscase voor categorieaffiniteit {#section_D6FF913E88E6486B8FBCE117CA8B253B}

De activiteit van een bezoeker in één zitting, zoals welke categorie hij of zij het vaakst bekijkt, kan worden gebruikt om zich bij volgende bezoeken te richten. Elke categoriepagina bevat een bezoeker die tijdens een sessie weergeeft, en zijn of haar categorie &quot;favoriet&quot; wordt berekend op basis van een recentiemodel en een frequentiemodel. Telkens wanneer de bezoeker terugkeert naar de homepage, kan het hoofdafbeeldingsgebied worden gebruikt om inhoud weer te geven die betrekking heeft op de favoriete categorie van die gebruiker.

## Voorbeeld van het gebruik van een categorieaffiniteit {#section_A4AC0CA550924CB4875F4F4047554C18}

Stel dat u muziekinstrumenten online verkoopt en verkoopbevorderende acties op basis van gitaren wilt richten op bezoekers die in het verleden al belangstelling voor gitaren hebben geuit. Met de affiniteit Categorie kunt u aanbiedingen maken die alleen worden weergegeven aan bezoekers met deze affiniteit Categorie.

## Categorieaffiniteitsalgoritme {#section_8B86C7FF50294208866ABF16F07D5EB9}

Het categorieaffiniteitsalgoritme werkt als volgt:

* 10 punten voor de eerste bekeken categorie
* 5 punten voor elke categorie waarop na de eerste
* Wanneer op een nieuwe categorie wordt geklikt, wordt 1 afgetrokken van alle eerder geklikte categorieën
* Als er al op een categorie is geklikt (weergegeven), wordt 1 van alle andere categorieën niet afgetrokken als u er nogmaals op klikt
* Als op een zesde nieuwe categorie wordt geklikt, wordt de laagste scorecategorie van de eerste vijf categorieën uit de berekening verwijderd
* Verdeel aan het einde van de sessie alle waarden door 2

### Voorbeeld: categorieaffiniteitalgoritme

Als u bijvoorbeeld de categorie `mens-clothing` weergeeft, vervolgens `accessories`, vervolgens `jewelry` en vervolgens `accessories` opnieuw in een sessie, resulteert dit in affiniteiten van:

* `accessories`: 9 (+5 - 1 + 5)

* `mens-clothing`: 8 (+10 - 1 - 1)

* `jewelry`: 5 (+5)

Wanneer de sessie wordt beëindigd en de gebruiker later terugkeert naar de site, worden de scores gehalveerd:

* `accessories`: 4,5 (9/2)

* `mens-clothing`: 4 (8/2)

* `jewelry`: 2,5 (5/2)

Ervan uitgaande dat de gebruiker dan `jewelry`, `accessories`, `beauty`, `shoes` en `womens-clothing` op volgorde bekijkt:

* `accessories`: 6,5 (4,5 + 5 - 1 - 1 - 1)

* `womens-clothing`: 5 (+5)

* `jewelry`: 4.5 (2.5 + 5 - 1 - 1 - 1)

* `shoes`: 4 (+5 - 1)

* `beauty`: 3 (+5 - 1 - 1)

* `mens-clothing` wordt verwijderd na de laatste klik van  `womens-clothing` de categorie met de laagste score met een score van 1 (4 - 1 - 1 - 1)

Wanneer de sessie wordt beëindigd en de gebruiker later terugkeert naar de site, worden de scores gehalveerd:

* `accessories`: 3.3 (6.5/2)

* `womens-clothing`: 2,5 (5/2)

* `jewelry`: 2,3 (4,5/2)

* `shoes`: 2 (4/2)

* `beauty`: 1,5 (3/2)

## Categorieaffiniteit gebruiken voor het aanwijzen van {#concept_5750C9E6C97A40F8B062A5C16F2B5FFC}

Informatie om u te helpen een [!UICONTROL Category Affinity] publiek voor het richten in een activiteit gebruiken.

Deze sectie bevat de volgende informatie:

* [Een publiek maken om rubriekaffiniteit te gebruiken](/help/c-target/c-visitor-profile/category-affinity.md#section_A27C600BBA664FE7A74F8FE076B78F40)
* [Het publiek Categorie affiniteit gebruiken in een activiteit](/help/c-target/c-visitor-profile/category-affinity.md#section_91526B942D1B4AEBB8FCDF4EBFF931CF)

## Een publiek maken om de affiniteit categorie {#section_A27C600BBA664FE7A74F8FE076B78F40} te gebruiken

1. Klik in de lijst **[!UICONTROL Audiences]** op **[!UICONTROL + Create Audience]**.

   of

   Als u een bestaand publiek wilt kopiëren, houdt u de muisaanwijzer boven het gewenste publiek en klikt u op het pictogram Kopiëren in de lijst Soorten publiek. Vervolgens kunt u het publiek bewerken om een vergelijkbaar publiek te maken.

1. Typ een beschrijvende publieksnaam.
1. Klik op **[!UICONTROL + Add Rule]** > **[!UICONTROL Visitor Profile]**.
1. Selecteer in de vervolgkeuzelijst **[!UICONTROL Visitor Profile]** de optie **[!UICONTROL Category Affinity]**.

   ![Bezoekersprofiel > Categorie-affiniteit](assets/affinity.png)

1. Selecteer de gewenste categorie:

   ![Categorie-affiniteit > Categorie](/help/c-target/c-visitor-profile/assets/affinity-category.png)

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

## Gebruik het publiek van de categorieaffiniteit in een activiteit {#section_91526B942D1B4AEBB8FCDF4EBFF931CF}

U kunt het publiek Categorieaffiniteit gebruiken in elke activiteit. Kies tijdens de driestappenworkflow met instructies het gewenste publiek in de stap Doel.
