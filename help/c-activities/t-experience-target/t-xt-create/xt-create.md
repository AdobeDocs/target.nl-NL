---
keywords: Experience Targeting;xt;create
description: Leer hoe te om Visual Experience Composer (VEC) in Adobe Target te gebruiken om een Ervaring te creëren richtend (XT) activiteit op een doel-Toegelaten pagina.
title: Hoe maak ik een ervaring die gericht is op activiteiten?
feature: Gericht op ervaring
translation-type: tm+mt
source-git-commit: 675c4a3383e384f017bdc0c5a70c988bc354189d
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# Een belevenis maken die gericht is op activiteit

Gebruik [!UICONTROL Visual Experience Composer] (VEC) om een [!UICONTROL Experience Targeting] (XT) activiteit op een doel-toegelaten pagina tot stand te brengen en om gedeelten van de pagina binnen [!DNL Adobe Target] te wijzigen.

Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

Gericht op ervaring, met inbegrip van [geo-targeting](/help/c-target/c-audiences/c-target-rules/geo.md), is nuttig voor het bepalen van regels die een specifieke ervaring of inhoud aan een bepaald publiek richten. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden.

Zie [Experience Targeting](/help/c-activities/t-experience-target/experience-target.md) voor meer informatie over Experience Targeting, een use-case-scenario en trainingsvideo&#39;s.

**Een XT-activiteit maken:**

1. Klik in de lijst [!UICONTROL Activities] op **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Activiteit maken > Gericht op ervaring](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw Target-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. [!UICONTROL Automated Personalization] is bijvoorbeeld een [Doelpremiumfunctie](/help/c-intro/intro.md#premium).
   >
   >Zie [Activiteiten](/help/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) voor meer informatie over de verschillende activiteitstypen die beschikbaar zijn in [!DNL Target] en hun verschillen. Zie [Doelactiviteitstypen](/help/c-activities/target-activities-guide.md) om u te helpen bepalen welk type activiteit het beste geschikt is voor uw behoeften.

1. Selecteer **[!UICONTROL Visual (Default)]**, indien nodig.

   ![Het dialoogvenster Activiteit bij gerichte ervaring maken](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Selecteer [!UICONTROL Form] als u liever de Form-Based Experience Composer wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Zie [Ervaringen en aanbiedingen](/help/c-experiences/experiences.md) voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Problemen oplossen Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [!UICONTROL Choose Workplace] optie in de voorafgaande illustratie is een [eigenschap van de Premium ](/help/c-intro/intro.md) van het Doel. Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant van de Premium van het Doel bent, [kies een werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef uw [activiteit-URL](/help/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90) op en klik vervolgens op **[!UICONTROL Next]**.

   Als uw account [is geconfigureerd met een standaard-URL](/help/administrating-target/visual-experience-composer-set-up.md), wordt die URL standaard weergegeven. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De VEC wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![Gerichte ervaring binnen de VEC](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Nieuwe ervaringen maken voor verschillende doelgroepen.

   Zie [Ervaring toevoegen](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md) voor stapsgewijze instructies.

1. Geef de [doelen en instellingen](/help/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit op.