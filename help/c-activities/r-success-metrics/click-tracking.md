---
keywords: Klik op bijhouden;traceer klikken;klikken;AppMeasurement
description: Leer hoe [!DNL Adobe Target] u kliks op om het even welk element als succes metrisch laat volgen.
title: Wat volgt de klik?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: f4b490c489427130e78d84b573b2d290a8a60585
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Klikken bijhouden

[!DNL Adobe Target] laat u klikken op om het even welk element volgen als succes metrisch.

>[!NOTE]
>
>Het volgen van kliks wordt niet gesteund op het globale [!DNL Target] verzoek wanneer het als plaats in een op vorm-gebaseerde activiteit wordt gebruikt.

## Klikspatiëring instellen {#section_5540C5A533114E57BAE022A600B02E72}

1. Wanneer het plaatsen van uw doelstellingen op de [!UICONTROL Goals & Settings] pagina voor uw activiteit, selecteer **[!UICONTROL Conversion]** succesmetrisch.
1. Selecteer **[!UICONTROL Clicked an element]** voor de actie en klik op **[!UICONTROL Select elements]**.

   Uw pagina wordt geopend in [!UICONTROL Visual Experience Composer] (VEC).

1. Selecteer de elementen die u wilt bijhouden.

   Zie de sectie *Overwegingen* hieronder voor tips over het selecteren van elementen.

1. Klik **[!UICONTROL Save]** bij de bovenkant van het scherm om uw selecties te bewaren.

Wanneer een deelnemer aan een activiteit op een geselecteerd element klikt, wordt die klik geteld als een omzetting.

## Deelvenster Geselecteerde elementen {#selected-elements}

Voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Multivariate Test] (MVT) activiteiten, een [!UICONTROL Selected Elements] paneel maakt een lijst van de geselecteerde elementen voor klik het volgen op de rechterkant.

![Deelvenster Geselecteerde elementen](/help/c-activities/r-success-metrics/assets/selected-elements.png)

Er zijn verschillende handelingen die u kunt toepassen wanneer u de muisaanwijzer op een element in het deelvenster [!UICONTROL Selected Elements] plaatst. In de volgende tabel wordt elke actie beschreven die op een element kan worden uitgevoerd:

| Handeling | Beschrijving |
| --- | --- |
| Informatie | Geeft het elementtype en het volledige DOM-pad naar de kiezer weer. |
| Bewerken | Hiermee kunt u de CSS-kiezer bewerken. |
| Verwijderen | Verwijdert het element. |

### Element toevoegen

Als u het DOM-pad naar de kiezer al kent, kunt u het handmatig toevoegen door op het pluspictogram boven in het deelvenster te klikken.

![Pictogram Element toevoegen](/help/c-activities/r-success-metrics/assets/add-element.png)

### Pop-up Geselecteerde elementen

Nadat u meerdere elementen hebt geselecteerd voor klikken op bijhouden, kunt u op de [!UICONTROL Elements Selected]-koppeling in de stap [!UICONTROL Goals & Settings] van de activiteit klikken om de volledige lijst met elementen weer te geven die zijn geselecteerd voor klikken op bijhouden. De lijst bevat het volledige DOM-pad voor het element, zodat u kunt controleren of het geselecteerde element moet worden gebruikt voor klikken op bijhouden.

![Geselecteerde Elements-koppeling](/help/c-activities/r-success-metrics/assets/elements-selected-link.png)

## Overwegingen {#considerations}

Bij het selecteren van elementen moet u rekening houden met verschillende zaken:

* De DOM-padfunctie is beschikbaar wanneer u klikt op bijhouden. Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Bovendien wordt het bijbehorende DOM-pad onder aan de pagina weergegeven. U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

   ![DOM-padillustratie](/help/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Net als bij het maken van ervaringen in stap 1 in de workflow voor het maken van activiteiten, kunt u met de padkiezer voor DOM onder aan de pagina een element kiezen. Bij het selecteren van een element van de weg DOM, toont het overeenkomstige element in VEC als &quot;Geselecteerd.&quot; Als u de selectie van een geselecteerd element wilt opheffen, klikt u opnieuw op het element in de DOM-padkiezer of klikt u op het vak &quot;Geselecteerd&quot; in de VEC.

   Zie [Navigeren door elementen met het DOM-pad](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Opties voor Visual Experience Composer* voor meer informatie.

* U kunt naar een andere pagina bladeren om te volgen klikt op een pagina waar u de inhoud wellicht niet wijzigt. Deze verschillende pagina moet in de activiteit worden omvat gebruikend [multipage eigenschap](/help/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) en [!DNL at.js] moet op het worden uitgevoerd.
* Als u meer dan één element selecteert, als een gegadigde op om het even welke gekozen elementen klikt, wordt de klik geteld. Als u elk onderdeel afzonderlijk wilt tellen, stelt u voor elk element afzonderlijke succesmaatstaven in. Als u één item wilt tellen door op meerdere elementen op een pagina te klikken, bewerkt u de CSS-elementkiezer zodat deze overeenkomt met meerdere elementen.
* Selecteer het niveau van het element dat u wilt bijhouden. Wanneer u bijvoorbeeld een knop opgeeft, moet u de koppeling selecteren en niet de knoptekst.
* Klik gebeurtenissen worden verzonden naar [!DNL Target] op de zelfde pagina zoals de klik.
* Als de metrische klikspatiëring de metrische waarde van het Doel van een [!UICONTROL Analytics for Target] (A4T) activiteit is, moet de bezoeker dit element binnen 60 seconden na het laden van de pagina klikken om metrisch te volgen.
* Klik op Tekstspatiëring om elementen te selecteren die beschermde tekens bevatten, zoals de volgende:

   | Teken | Beschrijving |
   |---|---|
   | Aantal | Nummerteken of Hash |
   | : | Colon |
   | . | Periode |
   | $ | Dollar-teken |
   | `[ ]` | Vierkante haken |

* Als u [!DNL at.js] klikt het volgen en u [!DNL Analytics] AppMeasurement ook gebruikt, [!DNL at.js] klikt het volgen annuleert alle andere managers van de klikgebeurtenis. Dientengevolge, voert de AppMeasurement klikmanager nooit uit.

   [!DNL at.js] heeft een speciale afhandeling voor het bijhouden van klikken wanneer het onderliggende element een  `A` (koppeling)tag of  `FORM` tag is.

   De volgende stappen worden uitgevoerd door [!DNL at.js] wanneer de gebeurtenis click tracking wordt gekoppeld aan een `A`-tag (link) of een `FORM`-tag:

   1. `event.preventDefault()` aanroepen.

   1. Verzoek [!DNL Target] vuur.

   1. Bij [!DNL Target] vraagsucces of foutencallback, voer standaardgedrag uit:

      * `A` (link) tag: Standaard wordt naar de URL gegaan die door het kenmerk HREF wordt gedefinieerd.
      * `FORM` tag: Standaard wordt het formulier verzonden.

   Dit standaardgedrag kan problemen opleveren met [!DNL Analytics] klikken op bijhouden. Als u [!DNL Analytics] gebruikt, zou u voor het volgen van klikken eerder dan [!DNL Target] moeten vertrouwen.[!DNL Analytics]

* Klik op Tekstspatiëring wordt niet opgenomen op pagina&#39;s waarvan de pagina en activiteit-URL tot verschillende eigenschappen behoren. De gebruikerstoestemmingen van de onderneming zijn een [!DNL Target Premium] eigenschap. Voor meer informatie, zie [De gebruikerstoestemmingen van de Onderneming](/help/administrating-target/c-user-management/property-channel/property-channel.md).

* Metrische gegevens voor het bijhouden van klikken zijn niet gekoppeld aan een specifieke ervaring in een activiteit.

* Gebruik een publiek als het nodig is om het bereik van de gegevens voor het bijhouden van klikken te beperken.

* De veelvoudige activiteiten kunnen klikken-spoor metrisch voor de zelfde selecteur bepalen. Als zo, wanneer een bezoeker voor één van die activiteiten kwalificeert en die selecteur klikt, klik-spoor metrische verhogingen voor alle verwante activiteiten die de bezoeker voor kwalificeerde.

## Trainingsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In deze video vindt u informatie over het maken van succesmetriek voor klikken en bijhouden.

* Begrijp &quot;doel&quot;metriek
* [!UICONTROL Conversion], [!UICONTROL Revenue] en [!UICONTROL Engagement] metriek begrijpen en bouwen
* Bouw metrisch klikken-volgend

>[!VIDEO](https://video.tv.adobe.com/v/17380)
