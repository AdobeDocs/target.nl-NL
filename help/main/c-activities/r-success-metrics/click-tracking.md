---
keywords: Klikken volgen;klikken bijhouden;klikken;AppMeasurement
description: Leer hoe  [!DNL Adobe Target]  u kliks op om het even welk element als metrisch succes laat volgen.
title: Wat volgt de klik?
feature: Success Metrics
exl-id: 9181424b-179e-49fc-b760-b764a0c3458a
source-git-commit: 43d2484e57b1e2d292cf65c041fb9f5f49b2084c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 0%

---

# Klikken bijhouden

Met [!DNL Adobe Target] kunt u op elk element klikken als een succesmetrische waarde. Klik op bijhouden verwijst naar het proces van het controleren en opnemen van gebruikersinteracties, waarbij u specifiek klikt, op elementen binnen een webpagina of ervaring. Dit is een essentieel onderdeel van het meten van betrokkenheid en prestaties bij A/B-tests, multivariate tests en personalisatieactiviteiten.

>[!NOTE]
>
>Het bijhouden van klikken wordt niet ondersteund voor de algemene [!DNL Target] -aanvraag wanneer deze wordt gebruikt als locatie in een op formulieren gebaseerde activiteit.

## Klikspatiëring instellen {#section_5540C5A533114E57BAE022A600B02E72}

1. Wanneer u uw doelstellingen op de pagina [!UICONTROL Goals & Settings] voor uw activiteit plaatst, selecteer **[!UICONTROL Conversion]** succesmetrisch.
1. Selecteer **[!UICONTROL Clicked an element]** voor de handeling en klik op **[!UICONTROL Select elements]** .

   De pagina wordt geopend in de map [!UICONTROL Visual Experience Composer] (VEC).

1. Selecteer de elementen die u wilt bijhouden.

   Zie de *sectie van Overwegingen* hieronder voor uiteinden bij het selecteren van elementen.

1. Klik op **[!UICONTROL Done]** boven aan het scherm om de selecties op te slaan.

Wanneer een deelnemer aan een activiteit op een geselecteerd element klikt, wordt die klik geteld als een omzetting.

## Deelvenster Geselecteerde elementen {#selected-elements}

Voor [!UICONTROL A/B Test]-, [!UICONTROL Experience Targeting] (XT)-, [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Multivariate Test] (MVT)-activiteiten worden in het deelvenster [!UICONTROL Selected Elements] de geselecteerde elementen weergegeven voor klik op bijhouden aan de linkerkant.

![&#x200B; Geselecteerde paneel van Elementen &#x200B;](/help/main/c-activities/r-success-metrics/assets/selected-elements.png)

Er zijn verschillende acties die u kunt toepassen wanneer u op een element klikt in het deelvenster [!UICONTROL Tracked Components] . In de volgende tabel wordt elke actie beschreven die op een element kan worden uitgevoerd:

| Handeling | Beschrijving |
| --- | --- |
| [!UICONTROL Tracked actions] | Geeft de handeling voor het element weer. |
| [!UICONTROL CSS selector] | Hiermee kunt u de CSS-kiezer bewerken. |
| [!DNL Delete] | Verwijdert het element. |

### Element toevoegen

Als u het DOM-pad naar de kiezer al kent, kunt u het handmatig toevoegen door op het pictogram [!UICONTROL Add Component] boven in het deelvenster te klikken.

## Overwegingen {#considerations}

Bij het selecteren van elementen moet u rekening houden met verschillende zaken:

* De DOM-padfunctie is beschikbaar wanneer u klikt op bijhouden. Wanneer u een element op de pagina klikt, toont het VEC optiesmenu. Bovendien wordt het bijbehorende DOM-pad onder aan de pagina weergegeven. U kunt het DOM-pad gebruiken om snel informatie over het geselecteerde element (type, id en klasse) weer te geven en het DOM-pad omhoog of omlaag te verplaatsen om het gewenste element te selecteren.

  Net als bij het maken van ervaringen in stap 1 in de workflow voor het maken van activiteiten, kunt u met de padkiezer voor DOM onder aan de pagina een element kiezen. Bij het selecteren van een element van de weg DOM, toont het overeenkomstige element in VEC als &quot;Geselecteerd.&quot; Als u de selectie van een geselecteerd element wilt opheffen, klikt u opnieuw op het element in de DOM-padkiezer of klikt u op het vak &quot;Geselecteerd&quot; in de VEC.

  Voor meer informatie, zie [&#x200B; elementen navigeren gebruikend de weg DOM &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) in *de Opties van Composer van de Ervaring van de Visuele*.

* U kunt naar een andere pagina bladeren om te volgen klikt op een pagina waar u de inhoud wellicht niet wijzigt. Deze verschillende pagina moet in de activiteit worden omvat gebruikend de [&#x200B; multipage eigenschap &#x200B;](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48) en [!DNL at.js] moet op het worden uitgevoerd.
* Als u meer dan één element selecteert, als een gegadigde op om het even welke gekozen elementen klikt, wordt de klik geteld. Als u elk onderdeel afzonderlijk wilt tellen, stelt u voor elk element afzonderlijke succesmaatstaven in. Als u één item wilt tellen door op meerdere elementen op een pagina te klikken, bewerkt u de CSS-elementkiezer zodat deze overeenkomt met meerdere elementen.
* Selecteer het niveau van het element dat u wilt bijhouden. Wanneer u bijvoorbeeld een knop opgeeft, moet u de koppeling selecteren en niet de knoptekst.
* Klikgebeurtenissen worden naar [!DNL Target] verzonden op dezelfde pagina als de klik.
* Als de metrische waarde voor klikken bijhouden de metrische waarde van het doel van een [!UICONTROL Analytics for Target] (A4T)-activiteit is, moet de bezoeker binnen 60 seconden na het laden van de pagina op dit element klikken om de metrisch te volgen.
* Klik op Tekstspatiëring om elementen te selecteren die beschermde tekens bevatten, zoals de volgende:

  | Teken | Beschrijving |
  |---|---|
  | Aantal | Nummerteken of Hash |
  | : | Colon |
  | . | Periode |
  | $ | Dollar-teken |
  | `[ ]` | Vierkante haken |

* Als u [!DNL at.js] klik het volgen gebruikt en u ook [!DNL Analytics] AppMeasurement gebruikt, [!DNL at.js] klik het volgen annuleert alle andere handlers van de klikgebeurtenis. Het resultaat is dat de AppMeasurement-klikhandler nooit wordt uitgevoerd.

  [!DNL at.js] heeft een speciale afhandeling voor het bijhouden van klikken wanneer het onderliggende element een `A` (link)tag of `FORM` -tag is.

  De volgende stappen worden uitgevoerd door [!DNL at.js] wanneer de gebeurtenis click tracking wordt gekoppeld aan een `A` (link)-tag of een `FORM` -tag:

   1. Roep `event.preventDefault()` aan.

   1. Fire [!DNL Target] request.

   1. Voer standaardgedrag uit bij een verzoek van [!DNL Target] om succes of callback van fouten:

      * `A` -tag (link): standaard navigeert u naar de URL die door het HREF-kenmerk wordt gedefinieerd.
      * `FORM` -tag: het standaardgedrag is dat het formulier wordt verzonden.

  Dit standaardgedrag kan problemen opleveren met [!DNL Analytics] klikken bijhouden. Als u [!DNL Analytics] gebruikt, moet u voor het bijhouden van klikken op [!DNL Analytics] vertrouwen in plaats van op [!DNL Target] .

* Klik op Tekstspatiëring wordt niet opgenomen op pagina&#39;s waarvan de pagina en activiteit-URL tot verschillende eigenschappen behoren. Machtigingen voor Enterprise-gebruikers zijn een [!DNL Target Premium] -functie. Voor meer informatie, zie [&#x200B; de gebruikerstoestemmingen van de Onderneming &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

* Metrische gegevens voor het bijhouden van klikken zijn niet gekoppeld aan een specifieke ervaring in een activiteit.

* Gebruik een publiek als het nodig is om het bereik van de gegevens voor het bijhouden van klikken te beperken.

* De veelvoudige activiteiten kunnen klikken-spoor metrisch voor de zelfde selecteur bepalen. Als zo, wanneer een bezoeker voor één van die activiteiten kwalificeert en die selecteur klikt, klik-spoor metrische verhogingen voor alle bijbehorende activiteiten die de bezoeker voor kwalificeerde.

## Trainingsvideo {#section_36607204DAE146E3B8E2C609D244EDB1}

In deze video vindt u informatie over het maken van succesmetriek voor klikken en bijhouden.

* Begrijp &quot;doel&quot;metriek
* Metrische waarden [!UICONTROL Conversion] , [!UICONTROL Revenue] en [!UICONTROL Engagement] begrijpen en bouwen
* Een metrisch object voor klikken bijhouden maken

>[!VIDEO](https://video.tv.adobe.com/v/17380)
