---
keywords: Click tracking;track clicks;clicks;AppMeasurement
description: Het doel laat u toe om kliks op om het even welk element te volgen als succes metrisch.
title: Klikken bijhouden
feature: success metrics
subtopic: Getting Started
topic: Standard
uuid: 4a8fbb23-93d8-49f3-aca3-dbbdd6da0178
translation-type: tm+mt
source-git-commit: 870f3dc0d4c154b282021384071699fa2d477d18
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---


# Klikken bijhouden{#click-tracking}

Het doel laat u toe om kliks op om het even welk element te volgen als succes metrisch.

>[!NOTE]
>
>Het volgen van kliks wordt niet gesteund op het globale verzoek van het Doel wanneer het als plaats in een vorm-gebaseerde activiteit wordt gebruikt.

## Klikspatiëring instellen {#section_5540C5A533114E57BAE022A600B02E72}

1. Wanneer het plaatsen van uw doelstellingen op de [!UICONTROL Goals & Settings] pagina voor uw activiteit, selecteer **[!UICONTROL Conversion]** succesmetrisch.
1. Selecteer voor de actie **[!UICONTROL Clicked an element]** en klik op **[!UICONTROL Select elements]**.

   De pagina wordt geopend in de map [!UICONTROL Visual Experience Composer] (VEC).

1. Selecteer de elementen die u wilt bijhouden.

   Zie de sectie Overwegingen hieronder voor tips over het selecteren van elementen.

1. Klik op het vinkje boven aan het scherm om de selecties op te slaan.

Wanneer een deelnemer aan een activiteit op een geselecteerd element klikt, wordt die klik geteld als een omzetting.

## Deelvenster Geselecteerde elementen {#selected-elements}

Voor A/B-test-, Experience Targeting- (XT), Automated Personalization- (AP) en MVT-activiteiten (Multivariate Test) bevat een [!UICONTROL Selected Elements] deelvenster alle geselecteerde elementen voor klik op tracking aan de rechterkant.

![Deelvenster Geselecteerde elementen](/help/c-activities/r-success-metrics/assets/selected-elements.png)

Er zijn verschillende acties die u kunt toepassen wanneer u de muisaanwijzer op een element in het [!UICONTROL Selected Elements] deelvenster plaatst. In de volgende tabel wordt elke actie beschreven die op een element kan worden uitgevoerd:

| Handeling | Beschrijving |
| --- | --- |
| Informatie | Geeft het elementtype en het volledige DOM-pad naar de kiezer weer. |
| Bewerken | Hiermee kunt u de CSS-kiezer bewerken. |
| Verwijderen | Verwijdert het element. |

### Element toevoegen

Als u het DOM-pad naar de kiezer al kent, kunt u het handmatig toevoegen door op het pluspictogram boven in het deelvenster te klikken.

![Pictogram Element toevoegen](/help/c-activities/r-success-metrics/assets/add-element.png)

### Geselecteerde elementen boven pop-up plaatsen

Nadat u meerdere elementen hebt geselecteerd voor klikken op bijhouden, kunt u op de [!UICONTROL Elements Selected] koppeling in de [!UICONTROL Goals & Settings] stap van de activiteit klikken om de volledige lijst met elementen weer te geven die zijn geselecteerd voor klikken op bijhouden. De lijst bevat het volledige DOM-pad voor het element, zodat u kunt controleren of het geselecteerde element moet worden gebruikt voor klikken op bijhouden.

![Geselecteerde Elements-koppeling](/help/c-activities/r-success-metrics/assets/elements-selected-link.png)

## Overwegingen {#considerations}

Bij het selecteren van elementen moet u rekening houden met verschillende zaken:

* De DOM-padfunctie is beschikbaar wanneer u klikt op bijhouden. Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Bovendien wordt het bijbehorende DOM-pad onder aan de pagina weergegeven. U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

   ![DOM-padillustratie](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Net als bij het maken van ervaringen in stap 1 in de workflow voor het maken van activiteiten, kunt u met de padkiezer voor DOM onder aan de pagina een element kiezen. Bij het selecteren van een element van de weg DOM, toont het overeenkomstige element in VEC als &quot;Geselecteerd.&quot; Als u de selectie van een geselecteerd element wilt opheffen, klikt u opnieuw op het element in de DOM-padkiezer of klikt u op het vak &quot;Geselecteerd&quot; in de VEC.

   Voor meer informatie, zie [Navigeren elementen gebruikend de weg](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) DOM in de Opties *van de Composer van de* Visuele Ervaring.

* U kunt naar een andere pagina bladeren om te volgen klikt op een pagina waar u de inhoud wellicht niet wijzigt. Deze andere pagina moet worden opgenomen in de activiteit met behulp van de functie [voor](../../c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) meerdere pagina&#39;s [!DNL at.js] of [!DNL mbox.js] moet erop worden geïmplementeerd.
* Als u meer dan één element selecteert, als een gegadigde op om het even welke gekozen elementen klikt, wordt de klik geteld. Als u elk onderdeel afzonderlijk wilt tellen, stelt u voor elk element afzonderlijke succesmaatstaven in. Als u één item wilt tellen door op meerdere elementen op een pagina te klikken, bewerkt u de CSS-elementkiezer zodat deze overeenkomt met meerdere elementen.
* Selecteer het niveau van het element dat u wilt bijhouden. Wanneer u bijvoorbeeld een knop opgeeft, moet u de koppeling selecteren en niet de knoptekst.
* Klik gebeurtenissen worden verzonden naar [!DNL Target] op de zelfde pagina zoals de klik.
* Als de metrisch klikt-tracking metrisch de Metrische Goal van een activiteit A4T is, moet de bezoeker dit element binnen 60 seconden na het laden van de pagina klikken om metrisch te volgen.
* Klik op Tekstspatiëring om elementen te selecteren die beschermde tekens bevatten, zoals de volgende:

   | Teken | Beschrijving |
   |---|---|
   | # | Nummerteken of Hash |
   | : | Colon |
   | . | Periode |
   | $ | Dollar-teken |
   | `[ ]` | Vierkante haken |

* Als u [!DNL at.js] klik het volgen gebruikt en u ook Analytics AppMeasurement gebruikt, [!DNL at.js] het volgen annuleert alle andere handlers van de klikgebeurtenis. Dientengevolge, voert de AppMeasurement klikmanager nooit uit.

   [!DNL at.js] heeft een speciale afhandeling voor het bijhouden van klikken wanneer het onderliggende element een `A` (koppeling)tag of - `FORM` tag is.

   De volgende stappen worden uitgevoerd door [!DNL at.js] de gebeurtenis click tracking te koppelen aan een `A` (link)tag of een `FORM` tag:

   1. Oproepen `event.preventDefault()`.

   1. Verzoek branddoel.

   1. Voer het standaardgedrag uit als de aanvraag is geslaagd of er een fout is teruggeroepen:

      * `A` (link) tag: Standaard wordt naar de URL gegaan die door het kenmerk HREF wordt gedefinieerd.
      * `FORM` tag: Standaard wordt het formulier verzonden.

   Dit standaardgedrag kan problemen veroorzaken bij het bijhouden van klikken op Analytics. Als u Analytics gebruikt, zou u voor het volgen van klik eerder dan Doel op Analytics moeten vertrouwen.

* Klik op Tekstspatiëring wordt niet opgenomen op pagina&#39;s waarvan de pagina en activiteit-URL tot verschillende eigenschappen behoren. Machtigingen voor gebruikers in de onderneming zijn een Target Premium-functie. Zie [Gebruikersmachtigingen](/help/administrating-target/c-user-management/property-channel/property-channel.md)voor ondernemingen voor meer informatie.

## Trainingsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In deze video vindt u informatie over het maken van succesmetriek voor klikken en bijhouden.

* Begrijp &quot;doel&quot;metriek
* Omzetten, Inkomsten en Betrokkenheid begrijpen en bouwen
* Bouw metrisch klikken-volgend

>[!VIDEO](https://video.tv.adobe.com/v/17380)