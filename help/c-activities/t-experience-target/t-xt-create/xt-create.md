---
description: Gebruik Composer Visuele Ervaring om een Gerichte (XT) activiteit van de Ervaring op een Doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen het Doel van Adobe te wijzigen.
title: Een belevenis maken die gericht is op activiteit
subtopic: Multivariate Test
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Een belevenis maken die gericht is op activiteit{#create-an-experience-targeting-activity}

Gebruik [!UICONTROL Visual Experience Composer] (VEC) om een [!UICONTROL Experience Targeting] (XT) activiteit op een doel-Toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen te wijzigen [!DNL Adobe Target].

Experience Targeting (XT) levert inhoud aan een specifiek publiek die op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

Gerichte ervaring, inclusief [geo-targeting](/help/c-target/c-audiences/c-target-rules/geo.md), is nuttig voor het definiëren van regels die een specifieke ervaring of inhoud voor een bepaald publiek als doel hebben. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden.

Voor meer informatie over Ervaring richtend, een gebruik-case scenario, en trainingsvideo&#39;s, zie de [Ervaring richtend](/help/c-activities/t-experience-target/experience-target.md).

**Een XT-activiteit maken:**

1. From the [!UICONTROL Activities] list, click **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Activiteit maken > Gericht op ervaring](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw Target-account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Automated Personalization] is een eigenschap [van de Premie van het](/help/c-intro/intro.md#premium)Doel.
   >
   >Zie [!DNL Target] Activiteiten [voor meer informatie over de verschillende soorten activiteiten die beschikbaar zijn in](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03)en hun verschillen. Zie [Doelactiviteitstypen](/help/c-activities/target-activities-guide.md) om u te helpen bepalen welk type activiteit het beste geschikt is voor uw behoeften.

1. Selecteer **[!UICONTROL Visual (Default)]** indien nodig.

   ![Het dialoogvenster Activiteit bij gerichte ervaring maken](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)

   Selecteer [!UICONTROL Form]Formulier-based Experience Composer als u liever wilt gebruiken. Zie [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) voor meer informatie.

   >[!NOTE]
   >
   >Naast de VEC en Form-Based Experience Composer, biedt Target de Single Page Application VEC en de VEC voor Mobile Apps. Zie [Ervaringen en Aanbiedingen](/help/c-experiences/experiences.md)voor meer informatie over de verschillende composers.
   >
   >Voor het oplossen van problemeninformatie over VEC, als u problemen hebt, zie het Oplossen van [problemen de Visuele Composer](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md)van de Ervaring.
   >
   >De [!UICONTROL Choose Workplace] optie in de voorgaande illustratie is een [doelpremiumfunctie](/help/c-intro/intro.md) . Uw organisatie heeft een licentie voor Target Standard als deze optie niet wordt weergegeven.]

1. (Voorwaardelijk) Als u een klant van de Premium van het Doel bent, [kies een werkruimte](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Geef de URL [van uw](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)activiteit op en klik op **[!UICONTROL Next]**.

   Als uw account is [geconfigureerd met een standaard-URL](/help/administrating-target/r-target-account-preferences/target-account-preferences.md), wordt die URL standaard weergegeven. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De VEC wordt geopend en geeft de pagina weer die in de URL is opgegeven.

   ![Gerichte ervaring binnen de VEC](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Typ een naam voor de activiteit in de beschikbare ruimte.

   ![Naamveld](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   De volgende tekens zijn niet toegestaan in een naam van een activiteit:

   | Teken | Beschrijving |
   |--- |--- |
   | `/` | slash |
   | `?` | Vraagteken |
   | `#` | Nummerteken |
   | `:` | Colon |
   | `=` | Gelijk aan |
   | `+` | Plus |
   | `-` | Min |
   | `@` | Bij ondertekenen |

1. Nieuwe ervaringen maken voor verschillende doelgroepen.

   Zie Ervaring [toevoegen voor stapsgewijze instructies](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Geef de [doelen en instellingen](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit op.