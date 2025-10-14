---
keywords: Experience Targeting;xt;create
description: Leer hoe te om [!UICONTROL Visual Experience Composer] (VEC) in  [!DNL Adobe Target]  te gebruiken om een [!UICONTROL Experience Targeting] (XT) activiteit tot stand te brengen.
title: Hoe maak ik een [!UICONTROL Experience Targeting] -activiteit?
feature: Experience Targeting
exl-id: fc7fc37f-40bf-4947-a4d0-e51fa09b6c56
source-git-commit: 9cc1eb4c5c95ea51bc0a1fc9e89b245a18c9914b
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Een [!UICONTROL Experience Targeting] (XT) activiteit maken

Gebruik [!UICONTROL Visual Experience Composer] (VEC) om een [!UICONTROL Experience Targeting] (XT) activiteit op een [!DNL Target] toegelaten pagina tot stand te brengen en gedeelten van de pagina binnen [!DNL Adobe Target] te wijzigen.

[!UICONTROL Experience Targeting] (XT) levert inhoud aan een specifiek publiek dat op een reeks van tellers-bepaalde regels en criteria wordt gebaseerd.

[!UICONTROL Experience Targeting], met inbegrip van [&#x200B; geo-gericht &#x200B;](/help/main/c-target/c-audiences/c-target-rules/geo.md), is waardevol voor het bepalen van regels die een specifieke ervaring of inhoud aan een bepaald publiek richten. Verschillende regels kunnen in een activiteit worden gedefinieerd om verschillende inhoudvariaties aan verschillende doelgroepen te bieden.

Voor meer informatie over [!UICONTROL Experience Targeting], een gebruik-geval scenario, en trainingsvideo&#39;s, zie [&#x200B; Begeleidende Ervaring &#x200B;](/help/main/c-activities/t-experience-target/experience-target.md).

**om een [!UICONTROL Experience Targeting] activiteit tot stand te brengen:**

1. Klik in de lijst [!UICONTROL Activities] op **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]** .

   >[!NOTE]
   >
   >De beschikbare activiteitstypen zijn afhankelijk van uw [!DNL Target] -account. Sommige typen activiteiten worden mogelijk niet in de lijst weergegeven. Bijvoorbeeld, [!UICONTROL Automated Personalization] is de eigenschap van a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium).
   >
   >Voor meer informatie over de diverse activiteitentypes beschikbaar in [!DNL Target] en hun verschillen, zie [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03). Zie [&#x200B; de types van Activiteit van het Doel &#x200B;](/help/main/c-activities/target-activities-guide.md) om u te helpen beslissen welk type van activiteit beste reeksen uw behoeften.

1. Selecteer **[!UICONTROL Visual]**, indien nodig.

   Als u verkiest om [&#x200B; vorm-Gebaseerde Composer van de Ervaring te gebruiken &#x200B;](/help/main/c-experiences/form-experience-composer.md), selecteer [!UICONTROL Form].

   >[!NOTE]
   >
   >Naast de VEC en [!UICONTROL Form-Based Experience Composer] biedt [!DNL Target] de toepassing VEC voor één pagina. Voor meer informatie over de diverse composers, zie [&#x200B; Ervaringen en Aanbiedingen &#x200B;](/help/main/c-experiences/experiences.md).
   >
   >Voor het oplossen van problemeninformatie over VEC, zie [&#x200B; het Oplossen van problemen de Visuele Composer van de Ervaring &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Voorwaardelijk) als u a [!DNL Target Premium] klant bent, [&#x200B; kies een werkruimte &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   De [!UICONTROL Choose Workplace] optie is a [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md) eigenschap. Als uw organisatie een [!DNL Target Standard] licentie heeft en deze optie niet wordt weergegeven.

1. Specificeer uw [&#x200B; activiteit URL &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), dan klik **[!UICONTROL Create]**.

   Als uw rekening [&#x200B; met een gebrek URL &#x200B;](/help/main/administrating-target/visual-experience-composer-set-up.md) wordt gevormd, verschijnt die URL door gebrek. U kunt desgewenst van de standaard naar een andere URL overschakelen.

   De VEC wordt geopend en geeft de pagina weer die in de URL is opgegeven.

1. Om de activiteit te noemen, klik het **[!UICONTROL Edit]** pictogram ( ![&#x200B; geef pictogram &#x200B;](/help/main/assets/icons/Edit.svg)) naast &quot; [!UICONTROL Untitled Activity] uit,&quot;specificeer een beschrijvende naam voor de activiteit, en klik dan **[!UICONTROL Save]**.

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

   Voor geleidelijke instructies, zie [&#x200B; ervaring &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-add-experience.md) toevoegen.

1. Specificeer de [&#x200B; doelstellingen en de montages &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) voor de activiteit.
