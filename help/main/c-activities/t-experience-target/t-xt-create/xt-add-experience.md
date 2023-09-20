---
keywords: creëren ervaring;ervaring creëren;prioriteit;publiek;ervaring;visuele ervaringscomposer
description: Leer hoe u de [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) om ervaringen op uw pagina te maken en te bewerken in een [!UICONTROL Experience Targeting] (XT) activiteit.
title: Hoe maak ik ervaringen in een [!UICONTROL Experience Targeting] Activiteit?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 0dfdd995c00961ed2aed91ec03406e8493292af7
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# Ervaring maken in [!UICONTROL Experience Targeting] (XT) activiteiten

De [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] biedt een visuele interface voor het bewerken van de ervaringen op uw pagina in een [!UICONTROL Experience Targeting] (XT) activiteit.

1. Selecteer de elementen die u wilt wijzigen en breng de gewenste wijzigingen aan.

   while [een [!UICONTROL Experience Targeting] activiteit](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), stap een van de driedelige geleide workflow ([!UICONTROL Experiences]) geeft de standaardwaarde weer [!UICONTROL Experience A] met een [!UICONTROL All Visitors] publiek.

   ![Alle bezoekers](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Wijzigingen die u nu aanbrengt, zijn van toepassing op [!UICONTROL Experience A]. In een onderstaande stap klikt u op **[!UICONTROL Add Experience Targeting]** om extra ervaringen te creëren.

   Terwijl u de muisaanwijzer over de elementen op de pagina beweegt, worden de elementen gemarkeerd. Om het even welk benadrukt element kan worden veranderd gebruikend VEC. Voor een lijst met acties die op een element kunnen worden uitgevoerd om de ervaring te veranderen, zie [Opties voor composer visuele ervaring](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt JavaScript uitschakelen om deze elementen te wijzigen met behulp van de VEC.

1. Als u meer ervaringen wilt opdoen, klikt u op **[!UICONTROL Add Experience Targeting]**.

   ![Koppeling Ervaring instellen toevoegen](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   De [!UICONTROL Add Audience] wordt weergegeven. Als u een ervaring wilt richten tot een publiek, selecteert u het publiek voordat u de ervaring toevoegt.

   De publieksbibliotheek bevat publiek dat eerder is gedefinieerd, inclusief een aantal algemene doelgroepen die vooraf zijn gebouwd als onderdeel van [!DNL Target]. U kunt een publiek selecteren in de bibliotheek of [een nieuw publiek maken](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie voor meer informatie [Meerdere soorten publiek combineren](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Wanneer u een publiek maakt, kunt u een locatie selecteren en parameters voor die locatie opgeven. Onder [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom]), selecteert u de locatie en geeft u de gewenste parameters op.

   >[!NOTE]
   >
   >Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer u de lijst met doelgroepen opent en het geïmporteerde publiek meer dan tien minuten oud is.

1. Selecteer een of meer soorten publiek voor de ervaring en klik op **[!UICONTROL Done]**.

   ![Ervaring B](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   De ervaring B wordt nu weergegeven in de voorgaande illustratie en deze ervaring is gericht op het publiek van de Amerikaanse bezoekers.

1. Selecteer de elementen die u voor deze ervaring wilt wijzigen en breng de gewenste wijzigingen aan, zoals beschreven in Stap 1 hierboven.

1. Herhaal de voorgaande stappen om zo nodig extra gerichte ervaringen te creëren.

1. Klikken **[!UICONTROL Next]** wanneer u klaar bent met het ontwerpen van uw ervaringen.

   Het activiteitendiagram toont:

   ![XT-richtingsdiagram](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >U kunt een afbeelding leveren van een andere bron dan de hoofdpagina (bijvoorbeeld een afbeelding die wordt gehost op `akamai.net` en geleverd op `adobe.com`). Afbeeldingen die elders worden gehost, worden niet weergegeven in de miniatuur van de pagina die in het stroomdiagram wordt weergegeven.

1. (Voorwaardelijk) Sleep publiek en ervaar paren tijdens het maken of bewerken [!UICONTROL Experience Targeting] activiteiten om de paren in de gewenste volgorde te rangschikken.

   Bezoekers worden op volgorde geëvalueerd, van boven naar beneden.

   ![Ervaringen verplaatsen](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Experience Targeting] gaat ervan uit dat volgorde van belang is. Als een bezoeker in het eerste publiek valt en het eerste paar ervaart, wordt de eerste ervaring geleverd.

   Stel dat u zich er niet van bewust bent dat bestellen van belang is tijdens het maken van een [!UICONTROL Experience Targeting] activiteit. U realiseert zich later tijdens het testen dat bezoekers die u denkt in aanmerking te komen voor ervaringen B of C in plaats daarvan in aanmerking komen voor ervaring A. Dit zou kunnen zijn omdat het publiek niet wederzijds exclusief is en niet in de juiste orde (bijvoorbeeld, ervaart A = Verenigde Staten, ervaart B = San Francisco, en ervaring C = Californië) is. In dit scenario komen alle gebruikers uit de Verenigde Staten in aanmerking voor ervaring A, zelfs als zij in San Francisco of elders in Californië zijn. U kunt het publiek en de ervaringsparen van het meest restrictieve aan het minst beperkende (San Francisco > Californië > Verenigde Staten) opnieuw rangschikken zonder de volledige activiteit te ontspannen.

   Als u een [!UICONTROL All Visitors] publiek, zorg ervoor dat het niet het eerste publiek in het diagram is. Een ervaring gericht op &quot;[!UICONTROL All Visitors]&quot; kan worden gebruikt als laatste ervaring in de [!UICONTROL Experience Targeting] activiteiten om bezoekers te &quot;vangen&quot; die niet in een andere ervaring zijn beland.

## Ervaring hernoemen of bewerken

U kunt op de knop [!UICONTROL Edit] pictogram (de verticale ellips) op een ervaring in een [!UICONTROL Experience Targeting] activiteit en kies van de volgende opties, zonodig:

* [!UICONTROL Rename]
* [!UICONTROL Edit]

![Opties voor Naam wijzigen en Bewerken](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Een ervaring verwijderen

Op de **[!UICONTROL Experiences]** pagina (de eerste stap in de driestappenworkflow met instructies), klikt u op de verticale ellips > **[!UICONTROL Delete]**.

![Ervaring verwijderen](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Een ervaring dupliceren

U kunt een ervaring kopiëren in een [!UICONTROL Experience Targeting] activiteit zodat kunt u kleine veranderingen in het aanbrengen zonder het moeten de volledige ervaring opnieuw creëren.

Op de **[!UICONTROL Experiences]** pagina (de eerste stap in de driestappenworkflow met instructies), klikt u op de verticale ellips > **[!UICONTROL Duplicate]**.

![Dubbele ervaring](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Van A/B-tests tot [!UICONTROL Experience Targeting]

In deze video wordt beschreven hoe u A/B-tests naar het volgende niveau kunt uitvoeren met [!UICONTROL Experience Targeting] (XT).

* Beschrijf de driestappenworkflow met instructies om een [!UICONTROL Experience Targeting] activiteit
* Beschrijf hoe u locatiespecifieke inhoud aan het publiek in verschillende geografische gebieden kunt leveren
* Beschrijf hoe u ervaringen opnieuw kunt rangschikken om ervoor te zorgen dat de juiste inhoud aan het juiste publiek wordt geleverd

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Typen activiteiten (9:03)

In deze video wordt uitgelegd welke soorten activiteiten beschikbaar zijn in [!DNL Target]. [!UICONTROL Experience Targeting] wordt om 17.15 uur besproken.

* Beschrijf de soorten activiteiten die onder [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Met de [!UICONTROL Visual Experience Composer]

Deze video bevat informatie over het gebruik van de [!UICONTROL Experience Targeting] (VEC).

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)
