---
keywords: Klik op bijhouden;traceer klikken;klikken;AppMeasurement
description: Meer informatie [!DNL Adobe Target] laat u klikken op om het even welk element volgen als succes metrisch.
title: Wat volgt de klik?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---

# Klikken bijhouden

[!DNL Adobe Target] laat u klikken op om het even welk element volgen als succes metrisch.

>[!NOTE]
>
>Het bijhouden van klikken wordt niet ondersteund op de globale [!DNL Target] aanvragen als het wordt gebruikt als een locatie in een op formulieren gebaseerde activiteit.

## Klikspatiëring instellen {#section_5540C5A533114E57BAE022A600B02E72}

1. Wanneer u uw doelstellingen op de [!UICONTROL Goals & Settings] pagina voor uw activiteit, selecteer **[!UICONTROL Conversion]** succesmetrisch.
1. Selecteer bij de handeling **[!UICONTROL Clicked an element]** en klik vervolgens op **[!UICONTROL Select elements]**.

   De pagina wordt geopend in het dialoogvenster [!UICONTROL Visual Experience Composer] (VEC).

1. Selecteer de elementen die u wilt bijhouden.

   Zie de *Overwegingen* voor tips over het selecteren van elementen.

1. Klikken **[!UICONTROL Save]** boven aan het scherm om de selecties op te slaan.

Wanneer een deelnemer aan een activiteit op een geselecteerd element klikt, wordt die klik geteld als een omzetting.

## Deelvenster Geselecteerde elementen {#selected-elements}

Voor [!UICONTROL A/B Test], [!UICONTROL Experience Targeting] (XT), [!UICONTROL Automated Personalization] (AP), en [!UICONTROL Multivariate Test] (MVT) activiteiten, [!UICONTROL Selected Elements] bevat een lijst met de geselecteerde elementen voor klikken op bijhouden aan de rechterkant.

![Deelvenster Geselecteerde elementen](/help/main/c-activities/r-success-metrics/assets/selected-elements.png)

Er zijn verschillende acties die kunnen worden toegepast wanneer u de muisaanwijzer op een element in het dialoogvenster [!UICONTROL Selected Elements] deelvenster. In de volgende tabel wordt elke actie beschreven die op een element kan worden uitgevoerd:

| Handeling | Beschrijving |
| --- | --- |
| Informatie | Geeft het elementtype en het volledige DOM-pad naar de kiezer weer. |
| Bewerken | Hiermee kunt u de CSS-kiezer bewerken. |
| Verwijderen | Verwijdert het element. |

### Element toevoegen

Als u het DOM-pad naar de kiezer al kent, kunt u het handmatig toevoegen door op het pluspictogram boven in het deelvenster te klikken.

![Pictogram Element toevoegen](/help/main/c-activities/r-success-metrics/assets/add-element.png)

### Pop-up Geselecteerde elementen

Nadat u meerdere elementen hebt geselecteerd voor klikken op bijhouden, kunt u op de knop [!UICONTROL Elements Selected] link naar de activiteit [!UICONTROL Goals & Settings] stap om de volledige lijst met elementen te zien die voor klik het volgen worden geselecteerd. De lijst bevat het volledige DOM-pad voor het element, zodat u kunt controleren of het geselecteerde element moet worden gebruikt voor klikken op bijhouden.

![Geselecteerde Elements-koppeling](/help/main/c-activities/r-success-metrics/assets/elements-selected-link.png)

## Overwegingen {#considerations}

Bij het selecteren van elementen moet u rekening houden met verschillende zaken:

* De DOM-padfunctie is beschikbaar wanneer u klikt op bijhouden. Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Bovendien wordt het bijbehorende DOM-pad onder aan de pagina weergegeven. U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

   ![DOM-padillustratie](/help/main/c-activities/r-success-metrics/assets/click-tracking-dom.png)

   Net als bij het maken van ervaringen in stap 1 in de workflow voor het maken van activiteiten, kunt u met de padkiezer voor DOM onder aan de pagina een element kiezen. Bij het selecteren van een element van de weg DOM, toont het overeenkomstige element in VEC als &quot;Geselecteerd.&quot; Als u de selectie van een geselecteerd element wilt opheffen, klikt u opnieuw op het element in de DOM-padkiezer of klikt u op het vak &quot;Geselecteerd&quot; in de VEC.

   Zie voor meer informatie [Navigeren door elementen met het DOM-pad](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *Opties voor composer visuele ervaring*.

* U kunt naar een andere pagina bladeren om te volgen klikt op een pagina waar u de inhoud wellicht niet wijzigt. Deze andere pagina moet worden opgenomen in de activiteit die de [multipage, functie](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) en [!DNL at.js] moeten worden uitgevoerd.
* Als u meer dan één element selecteert, als een gegadigde op om het even welke gekozen elementen klikt, wordt de klik geteld. Als u elk onderdeel afzonderlijk wilt tellen, stelt u voor elk element afzonderlijke succesmaatstaven in. Als u één item wilt tellen door op meerdere elementen op een pagina te klikken, bewerkt u de CSS-elementkiezer zodat deze overeenkomt met meerdere elementen.
* Selecteer het niveau van het element dat u wilt bijhouden. Wanneer u bijvoorbeeld een knop opgeeft, moet u de koppeling selecteren en niet de knoptekst.
* Klikgebeurtenissen worden verzonden naar [!DNL Target] op dezelfde pagina als de klik.
* Als de klik-volgende metrische waarde de metrische Goal van een is [!UICONTROL Analytics for Target] (A4T), moet de bezoeker op dit element klikken binnen 60 seconden na het laden van de pagina om de metrische waarde bij te houden.
* Klik op Tekstspatiëring om elementen te selecteren die beschermde tekens bevatten, zoals de volgende:

   | Teken | Beschrijving |
   |---|---|
   | Aantal | Nummerteken of Hash |
   | : | Colon |
   | . | Periode |
   | $ | Dollar-teken |
   | `[ ]` | Vierkante haken |

* Als u [!DNL at.js] klik het volgen en u ook gebruikt [!DNL Analytics] AppMeasurement, [!DNL at.js] klik het volgen annuleert alle andere managers van de klikgebeurtenis. Dientengevolge, voert de AppMeasurement klikmanager nooit uit.

   [!DNL at.js] heeft speciale behandeling voor klik het volgen wanneer het onderliggende element een `A` (link) tag of `FORM` tag.

   De volgende stappen worden uitgevoerd door [!DNL at.js] wanneer de gebeurtenis click tracking aan een `A` (link) of een `FORM` tag:

   1. Invoeden `event.preventDefault()`.

   1. Vuur [!DNL Target] verzoek.

   1. Aan [!DNL Target] request success of error callback, execute default behavior:

      * `A` (link) tag: Standaard wordt naar de URL gegaan die door het kenmerk HREF wordt gedefinieerd.
      * `FORM` tag: Standaard wordt het formulier verzonden.

   Dit standaardgedrag kan [!DNL Analytics] klik op bijhouden. Als u [!DNL Analytics]moet u erop vertrouwen [!DNL Analytics] voor klik het volgen eerder dan [!DNL Target].

* Klik op Tekstspatiëring wordt niet opgenomen op pagina&#39;s waarvan de pagina en activiteit-URL tot verschillende eigenschappen behoren. Gebruikersmachtigingen voor ondernemingen zijn [!DNL Target Premium] gebruiken. Zie voor meer informatie [Machtigingen voor Enterprise-gebruikers](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

* Metrische gegevens voor het bijhouden van klikken zijn niet gekoppeld aan een specifieke ervaring in een activiteit.

* Gebruik een publiek als het nodig is om het bereik van de gegevens voor het bijhouden van klikken te beperken.

* De veelvoudige activiteiten kunnen klikken-spoor metrisch voor de zelfde selecteur bepalen. Als zo, wanneer een bezoeker voor één van die activiteiten kwalificeert en die selecteur klikt, klik-spoor metrische verhogingen voor alle bijbehorende activiteiten die de bezoeker voor kwalificeerde.

## Trainingsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In deze video vindt u informatie over het maken van succesmetriek voor klikken en bijhouden.

* Begrijp &quot;doel&quot;metriek
* Begrijpen en bouwen [!UICONTROL Conversion], [!UICONTROL Revenue], en [!UICONTROL Engagement] cijfers
* Bouw metrisch klikken-volgend

>[!VIDEO](https://video.tv.adobe.com/v/17380)
