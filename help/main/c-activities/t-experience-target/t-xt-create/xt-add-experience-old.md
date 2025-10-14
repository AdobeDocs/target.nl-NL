---
keywords: creëren ervaring;ervaring creëren;prioriteit;publiek;ervaring;visuele ervaringscomposer
description: Leer hoe te om  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) te gebruiken om ervaringen op uw pagina in een [!UICONTROL Experience Targeting] (XT) activiteit tot stand te brengen en uit te geven.
title: Hoe maak ik ervaringen met een [!UICONTROL Experience Targeting] -activiteit?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Ervaring maken met [!UICONTROL Experience Targeting] (XT)-activiteiten

[!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] biedt een visuele interface voor het bewerken van de ervaringen op uw pagina in een [!UICONTROL Experience Targeting] -activiteit (XT).

1. Selecteer de elementen die u wilt wijzigen en breng de gewenste wijzigingen aan.

   Terwijl [&#x200B; creërend een [!UICONTROL Experience Targeting] activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), stap één van het driedelige geleide werkschema ([!UICONTROL Experiences]) toont het gebrek [!UICONTROL Experience A] met een [!UICONTROL All Visitors] publiek.

   ![&#x200B; Alle bezoekers publiek &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Alle wijzigingen die u nu aanbrengt, zijn van toepassing op [!UICONTROL Experience A] . In een onderstaande stap klikt u op **[!UICONTROL Add Experience Targeting]** om meer ervaringen te creëren.

   Terwijl u de muisaanwijzer over de elementen op de pagina beweegt, worden de elementen gemarkeerd. Om het even welk benadrukt element kan worden veranderd gebruikend VEC. Voor een lijst van acties die op een element kunnen worden uitgevoerd om de ervaring te veranderen, zie {de Opties van Composer van de 10} Visuele Ervaring [.](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

   >[!NOTE]
   >
   >Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt JavaScript uitschakelen om deze elementen te wijzigen met behulp van de VEC.

1. Klik op **[!UICONTROL Add Experience Targeting]** als u meer ervaringen wilt opdoen.

   ![&#x200B; voeg Ervaring toe richtend verbinding &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Het dialoogvenster [!UICONTROL Add Audience] wordt weergegeven. Als u een ervaring wilt richten tot een publiek, selecteert u het publiek voordat u de ervaring toevoegt.

   De publieksbibliotheek bevat publiek dat eerder is gedefinieerd, inclusief een aantal algemene doelgroepen die vooraf zijn gebouwd als onderdeel van [!DNL Target] . U kunt een publiek van de bibliotheek selecteren of [&#x200B; tot een nieuw publiek &#x200B;](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) leiden.

   Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Voor meer informatie, zie [&#x200B; Combinerend Veelvoudige Soorten publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Wanneer u een publiek maakt, kunt u een locatie selecteren en parameters voor die locatie opgeven. Selecteer onder [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom] ) de locatie en geef vervolgens de gewenste parameters op.

   >[!NOTE]
   >
   >Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer u de lijst met doelgroepen opent en het geïmporteerde publiek meer dan tien minuten oud is.

1. Selecteer een of meer soorten publiek voor de ervaring en klik op **[!UICONTROL Done]** .

   ![&#x200B; Ervaring B &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   De ervaring B wordt nu weergegeven in de voorgaande illustratie en deze ervaring is gericht op het publiek van de Amerikaanse bezoekers.

1. Selecteer de elementen die u voor deze ervaring wilt wijzigen en breng de gewenste wijzigingen aan, zoals beschreven in Stap 1 hierboven.

1. Herhaal de voorgaande stappen om zo nodig extra gerichte ervaringen te creëren.

1. Klik op **[!UICONTROL Next]** wanneer u klaar bent met het ontwerpen van uw ervaringen.

   Het activiteitendiagram toont:

   ![&#x200B; XT richtend diagram &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >U kunt een afbeelding leveren vanuit een andere bron dan de hoofdpagina (bijvoorbeeld een afbeelding die wordt gehost op `akamai.net` en wordt geleverd op `adobe.com` ). Afbeeldingen die elders worden gehost, worden niet weergegeven in de miniatuur van de pagina die in het stroomdiagram wordt weergegeven.

1. (Voorwaardelijk) Sleep publiek en ervaar paren tijdens het maken of bewerken van [!UICONTROL Experience Targeting] -activiteiten om de paren in de gewenste volgorde te rangschikken.

   Bezoekers worden op volgorde geëvalueerd, van boven naar beneden.

   ![&#x200B; ervaringen van de Beweging &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Experience Targeting] gaat ervan uit dat volgorde van belang is. Als een bezoeker in het eerste publiek valt en het eerste paar ervaart, wordt de eerste ervaring geleverd.

   Stel dat u er zich niet van bewust bent dat bestellen van belang is tijdens het maken van een [!UICONTROL Experience Targeting] -activiteit. U realiseert zich later tijdens het testen dat bezoekers die u denkt in aanmerking te komen voor ervaringen B of C in plaats daarvan in aanmerking komen voor ervaring A. Dit zou kunnen zijn omdat het publiek niet wederzijds exclusief is en niet in de juiste orde (bijvoorbeeld, ervaart A = Verenigde Staten, ervaart B = San Francisco, en ervaring C = Californië) is. In dit scenario komen alle gebruikers uit de Verenigde Staten in aanmerking voor ervaring A, zelfs als zij in San Francisco of elders in Californië zijn. U kunt het publiek en de ervaringsparen van het meest restrictieve aan het minst beperkende (San Francisco > Californië > Verenigde Staten) opnieuw rangschikken zonder de volledige activiteit te ontspannen.

   Als u een [!UICONTROL All Visitors] publiek hebt, zorg ervoor dat het niet het eerste publiek in het diagram is. Een ervaring gericht op &quot;[!UICONTROL All Visitors]&quot; kan als laatste ervaring in de [!UICONTROL Experience Targeting] activiteit worden gebruikt om bezoekers te &quot;vangen&quot;die niet in een andere ervaring zijn gevallen.

## Ervaring hernoemen of bewerken

U kunt op het pictogram [!UICONTROL Edit] (de verticale ellips) klikken op een ervaring in een [!UICONTROL Experience Targeting] -activiteit en indien nodig een van de volgende opties kiezen:

* [!UICONTROL Rename]
* [!UICONTROL Edit]

![&#x200B; noem en geef opties &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png) anders uit

## Een ervaring verwijderen

Klik op de pagina **[!UICONTROL Experiences]** (de eerste stap in de driestappenworkflow met instructies) op de verticale ellips > **[!UICONTROL Delete]** .

![&#x200B; ervaring van de Schrapping &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Een ervaring dupliceren

U kunt een ervaring in een [!UICONTROL Experience Targeting] activiteit kopiëren zodat kunt u kleine veranderingen in het aanbrengen zonder het moeten de volledige ervaring opnieuw creëren.

Klik op de pagina **[!UICONTROL Experiences]** (de eerste stap in de driestappenworkflow met instructies) op de verticale ellips > **[!UICONTROL Duplicate]** .

![&#x200B; Dubbele ervaring &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Van A/B-tests naar [!UICONTROL Experience Targeting]

In deze video wordt beschreven hoe u A/B-tests naar het volgende niveau kunt uitvoeren met [!UICONTROL Experience Targeting] (XT).

* Beschrijf de driestappenworkflow met instructies om een [!UICONTROL Experience Targeting] -activiteit te configureren
* Beschrijf hoe u locatiespecifieke inhoud aan het publiek in verschillende geografische gebieden kunt leveren
* Beschrijf hoe u ervaringen opnieuw kunt rangschikken om ervoor te zorgen dat de juiste inhoud aan het juiste publiek wordt geleverd

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Activiteitstypen (9:03)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in [!DNL Target] . [!UICONTROL Experience Targeting] wordt besproken beginnend bij 5 :15.

* Beschrijf de typen activiteiten die zijn opgenomen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### De [!UICONTROL Visual Experience Composer] gebruiken

Deze video bevat informatie over het gebruik van de opties [!UICONTROL Experience Targeting] (VEC).

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)
