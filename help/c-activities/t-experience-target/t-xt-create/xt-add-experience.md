---
keywords: create experience;experience create;priority;audience;experience;visual experience composer
description: De Adobe Target Visual Experience Composer (VEC) biedt een visuele interface voor het bewerken van de ervaringen op uw pagina in een Experience Targeting (XT)-activiteit.
title: Ervaring maken
feature: xt
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---


# Ervaring maken{#create-experience}

De [!UICONTROL Visual Experience Composer] (VEC) verstrekt een visuele interface voor het uitgeven van de ervaringen op uw pagina in een [!UICONTROL Experience Targeting] (XT) activiteit.

1. Selecteer de elementen die u wilt wijzigen en breng de gewenste wijzigingen aan.

   Terwijl [het creëren van een XT activiteit](/help/c-activities/t-experience-target/t-xt-create/xt-create.md), stap één van de driedelige geleide werkschema ([!UICONTROL Experiences]) toont het gebrek [!UICONTROL Experience A] met een [!UICONTROL All Visitors] publiek.

   ![Alle bezoekers](/help/c-activities/t-experience-target/t-xt-create/assets/all-visitors.png)

   Wijzigingen die u aanbrengt, zijn nu van toepassing op Experience A. In een onderstaande stap klikt u op **[!UICONTROL Add Experience Targeting]** om extra ervaringen te creëren.

   Terwijl u de elementen op de pagina plaatst, worden de elementen gemarkeerd. Om het even welk benadrukt element kan worden veranderd gebruikend VEC. Voor een lijst van acties die op een element kunnen worden uitgevoerd om de ervaring te veranderen, zie [Opties van Composer van de Visuele Ervaring](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   Als u een [!DNL Target] verzoek op de pagina gebruikend [!DNL Target Classic] creeerde, dat [!DNL Target] verzoek als element verschijnt dat de verzoeknaam toont, en kan als elk ander element worden gewijzigd.

   >[!NOTE]
   >
   >Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt selecteren om JavaScript onbruikbaar te maken om die elementen te veranderen gebruikend VEC.

1. Klik op **[!UICONTROL Add Experience Targeting]** om extra ervaringen op te doen.

   ![Koppeling Ervaring instellen toevoegen](/help/c-activities/t-experience-target/t-xt-create/assets/add-experience-targeting.png)

   Het dialoogvenster [!UICONTROL Choose Audience] wordt weergegeven. Als u een ervaring wilt toewijzen aan een publiek, moet u het publiek selecteren voordat u een ervaring kunt toevoegen.

   De publieksbibliotheek bevat publiek dat eerder is gedefinieerd, inclusief enkele algemene doelgroepen die vooraf zijn gebouwd als onderdeel van [!DNL Target]. U kunt een publiek selecteren uit de bibliotheek of [een nieuw publiek maken](/help/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271).

   >[!NOTE]
   >
   >Naast het selecteren van een bestaand publiek kunt u meerdere soorten publiek combineren om een gecombineerd ad-hocpubliek te maken in plaats van een nieuw publiek te maken. Zie [Meerdere soorten publiek combineren](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5) voor meer informatie.

   Wanneer u een publiek maakt, kunt u een locatie selecteren en parameters voor die locatie opgeven. Selecteer onder [!UICONTROL Custom] (Audience maken > Regel toevoegen > Aangepast) de locatie en geef vervolgens de gewenste parameters op.

   >[!NOTE]
   >
   >Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer u de publiekslijst opent en het geïmporteerde publiek langer dan 10 minuten oud is.

1. Selecteer een of meer soorten publiek die u wilt aanwijzen met de ervaring en klik op **[!UICONTROL Done]**.

   ![Ervaring B](/help/c-activities/t-experience-target/t-xt-create/assets/experience-b.png)

   U zult zien dat Experience B nu wordt weergegeven in de vorige illustratie en dat deze ervaring is bedoeld voor het publiek van de Amerikaanse bezoekers.

1. Selecteer de elementen die u voor deze ervaring wilt wijzigen en breng de gewenste wijzigingen aan, zoals uitgelegd in Stap 1.

1. Herhaal de voorgaande stappen om zo nodig extra gerichte ervaringen te creëren.

1. Klik **[!UICONTROL Next]** wanneer u klaar bent met het ontwerpen van uw ervaringen.

   Het activiteitendiagram toont:

   ![XT-richtingsdiagram](/help/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-new.png)

   >[!NOTE]
   >
   >Als u een afbeelding levert van een andere bron dan de hoofdpagina (bijvoorbeeld een afbeelding die wordt gehost op `akamai.net` en wordt geleverd op `adobe.com`), wordt die afbeelding niet weergegeven in de miniatuur van de pagina die wordt weergegeven in het stroomdiagram.

1. (Voorwaardelijk) belemmering en laat vallen publiek/ervaringsparen terwijl het creëren van of het uitgeven van XT activiteiten om de paren in de gewenste orde te schikken.

   Bezoekers worden op volgorde geëvalueerd, van boven naar beneden.

   ![Ervaringen verplaatsen](/help/c-activities/t-experience-target/t-xt-create/assets/move_experiences-new.png)

   [!UICONTROL Experience Targeting] gaat ervan uit dat volgorde van belang is. Als een bezoeker in het eerste publiek/ervaringspaar valt, wordt de eerste ervaring geleverd.

   Stel dat u zich er niet van bewust was dat bestellen belangrijk is tijdens het maken van een XT-activiteit. U realiseert zich later tijdens het testen dat bezoekers die u denkt in aanmerking te komen voor ervaringen B of C in plaats daarvan in aanmerking komen voor ervaring A. Dit zou kunnen zijn omdat het publiek niet wederzijds exclusief is en niet in de juiste orde (bijvoorbeeld, ervaart A = Verenigde Staten, ervaart B = San Francisco, en ervaring C = Californië) is. In dit scenario komen alle gebruikers uit de Verenigde Staten in aanmerking voor ervaring A, zelfs als ze zich in San Francisco of elders in Californië bevinden. U kunt de publiek/ervaringsparen van het meest restrictieve aan het minst beperkende (San Francisco > Californië > Verenigde Staten) opnieuw rangschikken zonder de volledige activiteit opnieuw te creëren.

   Als u een [!UICONTROL All Visitors] publiek hebt, zorg ervoor dat het niet het eerste publiek in het diagram is. Een ervaring die gericht is op &quot;Alle bezoekers&quot; kan worden gebruikt als de laatste ervaring in de ervaring die is opgedaan met activiteiten die erop gericht zijn bezoekers te &quot;vangen&quot; die geen andere ervaring hebben opgedaan.

## Ervaring hernoemen of bewerken

U kunt op het pictogram [!UICONTROL Edit] (drie verticale ellipsen) op een ervaring in een activiteit van de XT klikken en van de volgende opties kiezen, zonodig:

* Naam wijzigen
* Bewerken

![Opties voor Naam wijzigen en Bewerken](/help/c-activities/t-experience-target/t-xt-create/assets/experience_edit-new.png)

## Een ervaring verwijderen

Klik op de pagina **[!UICONTROL Experiences]** (de eerste stap in de driestapige geleide workflow) op de drie verticale ellipsen > **[!UICONTROL Delete]**.

![Ervaring verwijderen](/help/c-activities/t-experience-target/t-xt-create/assets/delete-experience.png)

## Een ervaring dupliceren

U kunt een ervaring in een XT-activiteit kopiëren zodat u er kleine wijzigingen in kunt aanbrengen zonder dat u de ervaring helemaal opnieuw hoeft te maken.

Klik op de pagina **[!UICONTROL Experiences]** (de eerste stap in de driestapige geleide workflow) op de drie verticale ellipsen > **[!UICONTROL Duplicate]**.

![Dubbele ervaring](/help/c-activities/t-experience-target/t-xt-create/assets/duplicate_experience-new.png)

## Trainingsvideo&#39;s:

De volgende video&#39;s bevatten meer informatie over de concepten die in dit artikel worden besproken.

### Van A/B-tests tot Experience Targeing

In deze video wordt beschreven hoe u A/B Testen naar een hoger niveau kunt tillen met Experience Targeting (XT).

* Beschrijf de drie-stap geleide werkschema om een XT activiteit te vormen
* Beschrijf hoe te om plaats-specifieke inhoud aan publiek te leveren dat in verschillende geografische gebieden wordt gevestigd
* Beschrijf hoe u ervaringen opnieuw kunt rangschikken om ervoor te zorgen dat de juiste inhoud aan het juiste publiek wordt geleverd

>[!VIDEO](https://video.tv.adobe.com/v/22418/)

### Typen activiteiten (9:03)

In deze video worden de activiteitstypen uitgelegd die beschikbaar zijn in Target Standard/Premium. Experience Targeting wordt besproken vanaf 5:15.

* Beschrijf de soorten activiteiten inbegrepen in [!DNL Adobe Target]
* Selecteer het juiste type activiteit om uw doelen te bereiken
* Beschrijf de driestappenworkflow met instructies die van toepassing is op alle typen activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17386)

### Het gebruiken van de Visuele Composer van de Ervaring

Deze video verstrekt informatie over het gebruiken van de Visuele opties van Composer van de Ervaring.

* De inhoud van een pagina wijzigen
* De lay-out van een pagina wijzigen

>[!VIDEO](https://video.tv.adobe.com/v/17399)