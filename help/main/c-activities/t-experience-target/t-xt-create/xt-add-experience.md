---
keywords: creëren ervaring;ervaring creëren;prioriteit;publiek;ervaring;visuele ervaringscomposer
description: Leer hoe te om  [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) te gebruiken om ervaringen op uw pagina in een [!UICONTROL Experience Targeting] (XT) activiteit tot stand te brengen en uit te geven.
title: Hoe maak ik ervaringen met een [!UICONTROL Experience Targeting] -activiteit?
feature: Experience Targeting
exl-id: ec3fcd93-5557-4f69-8f9c-4d00569188ad
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Ervaring maken met [!UICONTROL Experience Targeting] (XT)-activiteiten

[!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] biedt een visuele interface voor het bewerken van de ervaringen op uw pagina in een [!UICONTROL Experience Targeting] -activiteit (XT).

1. Selecteer de elementen die u wilt wijzigen en breng de gewenste wijzigingen aan.

   Terwijl [&#x200B; creërend een [!UICONTROL Experience Targeting] activiteit &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), stap één van het driedelige geleide werkschema ([!UICONTROL Experiences]) toont het gebrek [!UICONTROL Experience A] met een [!UICONTROL All Visitors] publiek.

   ![&#x200B; Alle bezoekers publiek &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/all-visitors-new.png)

   Alle wijzigingen die u nu aanbrengt, zijn van toepassing op [!UICONTROL Experience A] . In een onderstaande stap klikt u op **[!UICONTROL Add Experience Targeting]** om meer ervaringen te creëren.

   Terwijl u de muisaanwijzer over de elementen op de pagina beweegt, worden de elementen gemarkeerd. Om het even welk benadrukt element kan worden veranderd gebruikend VEC. Voor een lijst van acties die op een element kunnen worden uitgevoerd om de ervaring te veranderen, zie {de Opties van Composer van de 10} Visuele Ervaring [.](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

   >[!NOTE]
   >
   >Standaard staat de VEC geen wijzigingen toe in elementen die JavaScript bevatten, zoals draaiende banners. U kunt JavaScript uitschakelen om deze elementen te wijzigen met behulp van de VEC.

1. Om extra ervaringen tot stand te brengen, klik **[!UICONTROL Add]** ( ![&#x200B; voeg knoop &#x200B;](/help/main/assets/icons/Add.svg) toe).

   Het dialoogvenster [!UICONTROL Add Audience] wordt weergegeven. Als u een ervaring wilt richten tot een publiek, selecteert u het publiek voordat u de ervaring toevoegt.

   De publieksbibliotheek bevat publiek dat eerder is gedefinieerd, inclusief een aantal algemene doelgroepen die vooraf zijn gebouwd als onderdeel van [!DNL Target] . U kunt een publiek van de bibliotheek selecteren of [&#x200B; tot een nieuw publiek &#x200B;](/help/main/c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271) leiden.

   Naast het selecteren van een bestaand publiek, kunt u veelvoudige publiek combineren om op bestelling gecombineerd publiek tot stand te brengen eerder dan het creëren van een nieuw publiek. Voor meer informatie, zie [&#x200B; Combinerend Veelvoudige Soorten publiek &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   Wanneer u een publiek maakt, kunt u een locatie selecteren en parameters voor die locatie opgeven. Selecteer onder [!UICONTROL Custom] ([!UICONTROL Create Audience] > [!UICONTROL Custom] ) de locatie en geef vervolgens de gewenste parameters op.

   >[!NOTE]
   >
   >Soorten publiek worden automatisch op de achtergrond geïmporteerd wanneer u de lijst met doelgroepen opent en het geïmporteerde publiek meer dan tien minuten oud is.

1. Selecteer een of meer soorten publiek voor de ervaring en klik op **[!UICONTROL Assign Audience]** .

   De ervaring B wordt nu weergegeven in de voorgaande illustratie en deze ervaring is gericht op het juiste publiek.

1. Selecteer de elementen die u voor deze ervaring wilt wijzigen en breng de gewenste wijzigingen aan, zoals beschreven in Stap 1 hierboven.

1. Herhaal de voorgaande stappen om zo nodig extra gerichte ervaringen te creëren.

1. Klik op **[!UICONTROL Next]** wanneer u klaar bent met het ontwerpen van uw ervaringen.

   Het activiteitendiagram toont:

   ![&#x200B; XT richtend diagram &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/xt_diagram-refresh.png)

   >[!NOTE]
   >
   >U kunt een afbeelding leveren vanuit een andere bron dan de hoofdpagina (bijvoorbeeld een afbeelding die wordt gehost op `akamai.net` en wordt geleverd op `adobe.com` ). Afbeeldingen die elders worden gehost, worden niet weergegeven in de miniatuur van de pagina die in het stroomdiagram wordt weergegeven.

1. (Voorwaardelijk) Sleep publiek en ervaar paren tijdens het maken of bewerken van [!UICONTROL Experience Targeting] -activiteiten om de paren in de gewenste volgorde te rangschikken.

   Klik het Reorder pictogram ( ![&#x200B; pictogram van de Herschikking &#x200B;](/help/main/assets/icons/Reorder.svg)) om de [!UICONTROL Experiences] kolom op de rechterkant te tonen, dan de ervaringen opnieuw te rangschikken zoals gewenst.

   Bezoekers worden op volgorde geëvalueerd, van boven naar beneden.

   [!UICONTROL Experience Targeting] gaat ervan uit dat volgorde van belang is. Als een bezoeker in het eerste publiek valt en het eerste paar ervaart, wordt de eerste ervaring geleverd.

   Stel dat u er zich niet van bewust bent dat bestellen van belang is tijdens het maken van een [!UICONTROL Experience Targeting] -activiteit. U realiseert zich later tijdens het testen dat bezoekers die u denkt in aanmerking te komen voor ervaringen B of C in plaats daarvan in aanmerking komen voor ervaring A. Deze situatie zou kunnen zijn omdat het publiek niet wederzijds exclusief is en niet in de juiste orde (bijvoorbeeld, ervaring A = Verenigde Staten, ervaring B = San Francisco, en ervaring C = Californië) is. In dit scenario komen alle gebruikers uit de Verenigde Staten in aanmerking voor ervaring A, zelfs als zij in San Francisco of elders in Californië zijn. U kunt het publiek en de ervaringsparen van het meest restrictieve aan het minst beperkende (San Francisco > Californië > Verenigde Staten) opnieuw rangschikken zonder de volledige activiteit te ontspannen.

   Als u een [!UICONTROL All Visitors] publiek hebt, zorg ervoor dat het niet het eerste publiek in het diagram is. Een ervaring gericht op &quot;[!UICONTROL All Visitors]&quot; kan als laatste ervaring in de [!UICONTROL Experience Targeting] activiteit worden gebruikt om bezoekers te &quot;vangen&quot;die niet in een andere ervaring zijn gevallen.

## Ervaring hernoemen, bewerken, dupliceren of verwijderen

Klik op een ervaring in het diagram in een [!UICONTROL Experience Targeting] -activiteit om de kolom [!UICONTROL Experiences] rechts weer te geven.

![&#x200B; noem en geef opties &#x200B;](/help/main/c-activities/t-experience-target/t-xt-create/assets/experience_edit-refresh.png) anders uit

Kies desgewenst uit de volgende opties:

* **[!UICONTROL Rename]** : typ de gewenste naam in het veld [!UICONTROL Name] .
* **[!UICONTROL Edit]**: Klik het Edit pictogram ( ![&#x200B; geef pictogram &#x200B;](/help/main/assets/icons/Edit.svg) uit), dan breng uw gewenste veranderingen aan.
* **[!UICONTROL Duplicate]**: Kopieer een ervaring in een [!UICONTROL Experience Targeting] -activiteit zodat u er kleine wijzigingen in kunt aanbrengen zonder dat u de hele ervaring opnieuw hoeft te maken. Klik het [!UICONTROL Duplicate] pictogram ( ![&#x200B; Dupliceer pictogram &#x200B;](/help/main/assets/icons/Duplicate.svg)), dan geef zonodig de ervaring uit.
* **[!UICONTROL Delete]**: Klik het [!UICONTROL Delete] pictogram (![&#x200B; pictogram van de Schrapping &#x200B;](/help/main/assets/icons/Delete.svg)), dan bevestig uw schrapping.

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
