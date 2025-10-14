---
keywords: tijdframe;begindatum;einddatum;begin/einddatum;tijdframe;doelschema;week parteren;dag parteren;parkeren
description: Leer hoe u begin- en einddatums en -tijden kunt gebruiken voor gebruikers die uw site gedurende een bepaald tijdsbestek bezoeken.
title: Kan ik mij richten op bezoekers die mijn site op specifieke tijdstippen bezoeken?
feature: Audiences
exl-id: 814d545d-baee-4f8b-a2ed-ed68fceaeb7f
source-git-commit: 0e4698935b90cc0236abe6a47a6183c7fd2a7b20
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# [!UICONTROL Time Frame]

U kunt begin- en einddatums en -tijden in [!DNL Adobe Target] toevoegen aan doelgebruikers die uw site gedurende een bepaald tijdsbestek bezoeken. U kunt ook de opties voor Week- en Dagscheiding instellen om herhalende patronen te maken voor doelgroepen.

Bijvoorbeeld, gebruikend de [&#x200B; gecombineerde, ad hoc eigenschap van toehoorders &#x200B;](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5), kunt u laag-financiers met specifieke inhoud tijdens de drie dagen die tot Zwarte Vrijdag en andere inhoud na Zwarte Vrijdag leiden richten.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]** .
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Time Frame]** naar het deelvenster van de publieksbuilder.

   ![&#x200B; target_timeframe_dialog beeld &#x200B;](assets/target_timeframe_dialog.png)

1. Geef de [!UICONTROL Start] - en [!UICONTROL End] -datums en -tijden op voor het publiek.

   Laat de begindatum leeg om de focus te starten volgens het schema van de activiteit. Laat de einddatum leeg om verder te gaan met zoeken tot de einddatum en -tijd van de activiteit.

   U kunt zowel de begin- als de einddatum leeg laten. Met deze functie kunt u hetzelfde publiek in meerdere activiteiten gebruiken (zonder een kopie van het publiek te maken) en tegelijk de begin- en einddatums op activiteitsniveau beheren.

   >[!NOTE]
   >
   >Overweeg het volgende:
   >
   >* De tijdzone voor begin/einddata wordt getoond als GMT +/- NN :NN, waar NN :NN de compensatie van GMT is en op rekening-niveau tijdzone eerder dan de tijdzone van de bezoeker wijst. Bijvoorbeeld, zou de tijdzone van Californië als GMT - 08 :00 worden getoond.
   >
   >* [!DNL Target] tijdpubliek houdt geen rekening met DST-wijzigingen (Daylight Saving Time). U moet het publiek handmatig opnieuw opslaan om rekening te houden met DST-wijzigingen.

1. (Voorwaardelijk) Klik **[!UICONTROL Set frequency]** om terugkerende patronen in te stellen, inclusief de dagen van de weken en tijden.

   ![&#x200B; Week en Dag die &#x200B;](assets/week_and_day_parting.png) ontleden

   U kunt de opties van [!UICONTROL Frequency] bijvoorbeeld gebruiken om een optie &quot;Nu chatten&quot; alleen aan bezoekers weer te geven tijdens de dagen en uren dat uw callcenter bemand is.

   Selecteer een of meer dagen van de week en stel vervolgens de begin- en eindtijd in. Klik op **[!UICONTROL Add frequency]** om aanvullende patronen op te geven.

   >[!NOTE]
   >
   >De tijdzone voor [!UICONTROL Week and Day Parting] wordt getoond als GMT +/- NN :NN, waar NN :NN de compensatie van GMT is en op rekeningsniveau de tijdzone eerder dan de tijdzone van de bezoeker wijst. Bijvoorbeeld, zou de tijdzone van Californië voor de Tijd van het Daglicht van de Stille Oceaan als GMT -07 :00 worden getoond.

1. (Optioneel) Stel aanvullende regels voor het publiek in.

   Desgewenst kunt u Stap 5 voor elke regel herhalen.

1. Klik op **[!UICONTROL Done]**.

## De video van de opleiding: Creërend publiek ![&#x200B; badge van het Overzicht &#x200B;](/help/main/assets/overview.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
