---
keywords: Experience Targeting;xt;create
description: Leer hoe u de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] om een [!UICONTROL Experience Targeting] (XT) activiteit.
title: Hoe maak ik een [!UICONTROL Experience Targeting] Activiteit?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 4faafcef38d02674072d8b20ae03d3e2ef2115d6
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Een [!UICONTROL Experience Targeting] (XT) activiteit

Gebruik de [!UICONTROL Visual Experience Composer] (VEC) om een [!UICONTROL Experience Targeting] (XT) activiteit op een [!DNL Target]-enabled pagina en om gedeelten van de pagina binnen te wijzigen [!DNL Adobe Target].

[!UICONTROL Experience Targeting] (XT) levert inhoud aan een specifiek publiek dat op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

[!UICONTROL Experience Targeting], inclusief [gericht op geo](/help/main/c-target/c-audiences/c-target-rules/geo.md), is nuttig voor het definiëren van regels die gericht zijn op een specifieke ervaring of inhoud voor een bepaald publiek. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden.

Voor meer informatie over [!UICONTROL Experience Targeting], een gebruiksscenario, en trainingsvideo&#39;s, zie [Gericht op ervaring](/help/main/c-activities/t-experience-target/experience-target.md).

**Om een [!UICONTROL Experience Targeting] activiteit:**

1. Van de [!UICONTROL Activities] lijst, klik **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Activiteit maken > Gericht op ervaring](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld: [!UICONTROL Automated Personalization] is een [Functie Doelpremium](/help/main/c-intro/intro.md#premium).
   >
   >Voor meer informatie over de verschillende activiteitstypen die beschikbaar zijn in [!DNL Target] en hun verschillen, zie [Activiteiten](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [Typen doelactiviteiten](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welke type activiteit beste reeksen uw behoeften.

1. Selecteren **[!UICONTROL Visual (Default)]**, indien nodig.

   Als u liever het [Formuliergebaseerde Experience Composer](/help/main/c-experiences/form-experience-composer.md), selecteert u [!UICONTROL Form].

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer], [!DNL Target] biedt de Single Page Application VEC aan. Zie voor meer informatie over de verschillende composers [Ervaringen en aanbiedingen](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, zie [Problemen oplossen met de composer voor visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) Als u een [!DNL Target Premium] klant, [een werkruimte kiezen](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   De [!UICONTROL Choose Workplace] optie is [Doelpremie](/help/main/c-intro/intro.md) gebruiken. Als uw organisatie een [!DNL Target Standard] Als u deze optie niet ziet.

1. Geef uw [activiteit-URL](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90)en klik vervolgens op **[!UICONTROL Create]**.

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

   De naam van de activiteit mag geen van de volgende tekenreeksen bevatten:

   | Tekenreeks | Beschrijving |
   |--- |--- |
   | ;= | Semicolon, is gelijk aan |
   | ;+ | Puntkomma, plus |
   | ;- | Puntkomma, min |
   | ;@ | Puntkomma, bij teken |
   | ,= | Komma, is gelijk aan |
   | ,+ | Komma, plus |
   | ,- | Komma, min |
   | ,@ | Komma, bij teken |
   | `[`&quot; | Vierkante haak openen, dubbele aanhalingstekens |
   | &quot;`]` | Dubbele aanhalingstekens, vierkant haakje sluiten |

1. Nieuwe ervaringen maken voor verschillende doelgroepen.

   Zie voor stapsgewijze instructies [Ervaring toevoegen](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

1. Geef de [doelstellingen en instellingen](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit.
