---
keywords: Experience Targeting;xt;create
description: Leer hoe te om Visual Experience Composer (VEC) in Adobe te gebruiken [!DNL Target] om een Experience Targeting (XT) activiteit op een Target-Toegelaten pagina tot stand te brengen.
title: Hoe maak ik een ervaring die gericht is op activiteiten?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Een belevenis maken die gericht is op activiteit

Gebruik de [!UICONTROL Visual Experience Composer] (VEC) om een [!UICONTROL Experience Targeting] (XT) activiteit op een Doel-Toegelaten pagina en om gedeelten van de pagina binnen te wijzigen [!DNL Adobe Target].

Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

Gericht op ervaring, inclusief [gericht op geo](/help/main/c-target/c-audiences/c-target-rules/geo.md), is nuttig voor het definiëren van regels die gericht zijn op een specifieke ervaring of inhoud voor een bepaald publiek. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden.

Zie voor meer informatie over Experience Targeting, een gebruiksscenario en trainingsvideo&#39;s [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md).

**Een XT-activiteit maken:**

1. Van de [!UICONTROL Activities] lijst, klikt u op **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Activiteit maken > Gericht op ervaring](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw Target-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld: [!UICONTROL Automated Personalization] is een [Functie Doelpremium](/help/main/c-intro/intro.md#premium).
   >
   >Voor meer informatie over de verschillende soorten activiteiten die beschikbaar zijn in [!DNL Target] en hun verschillen, zie [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [Typen doelactiviteiten](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welke type activiteit beste reeksen uw behoeften.

1. Selecteren **[!UICONTROL Visual (Default)]**, indien nodig.

   ![Het dialoogvenster Activiteit bij gerichte ervaring maken](/help/main/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Selecteer [!UICONTROL Form]. Zie [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md) voor meer informatie .

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Voor meer informatie over de verschillende composers raadpleegt u [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie [Het oplossen van problemen de Visuele Composer van de Ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [Doelpremie](/help/main/c-intro/intro.md) gebruiken. Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.

1. (Voorwaardelijk) Als u een klant van de Premie van het Doel bent, [een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef uw [activiteit-URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)en klik vervolgens op **[!UICONTROL Next]**.

   Als uw account [geconfigureerd met een standaard-URL](/help/main/administrating-target/visual-experience-composer-set-up.md), wordt die URL standaard weergegeven. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De VEC wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![Gerichte ervaring binnen de VEC](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   De naam van de activiteit mag niet met een van de volgende tekens beginnen:

   | Teken | Beschrijving |
   |--- |--- |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Nieuwe ervaringen maken voor verschillende doelgroepen.

   Voor stapsgewijze instructies raadpleegt u [Ervaring toevoegen](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Geef de [doelstellingen en instellingen](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit.
