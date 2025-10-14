---
keywords: browseropties;type;browsertype;browsertaal;taal;versie;browserversie
description: Leer hoe te om publiek in  [!DNL Adobe Target]  tot stand te brengen om gebruikers te richten die specifieke browser of specifieke browser opties gebruiken wanneer zij uw pagina bezoeken.
title: Kan ik bezoekers richten die op Browser type worden gebaseerd?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '1015'
ht-degree: 0%

---

# [!UICONTROL Browser]

U kunt zich richten op gebruikers die een specifieke browser of specifieke browseropties gebruiken wanneer zij uw pagina bezoeken.

U kunt de volgende browsers als doel instellen:

* [!UICONTROL Chrome]
* [!UICONTROL Firefox]
* [!UICONTROL Safari]
* [!UICONTROL Internet Explorer]
* [!UICONTROL Microsoft Edge]
* [!UICONTROL Opera]
* [!DNL iPad]
* [!DNL iPhone]

>[!IMPORTANT]
>
>Vanaf [!DNL Target] Standard/Premium 24.3.1 (4-6 maart 2024) zijn ingebouwde doelgroepen, zoals `Browser:iPad` en `Browser:iPhone` , bijgewerkt en worden ze op de juiste manier voor [!DNL iPad] en [!DNL iPhone] using `profile.mobile.deviceVendor` , `profile.mobile.isMobilePhone` en `profile.mobile.isTablet` gebruikt.
>
>Deze update vereist geen actie aan de kant van de klanten. De etiketten in [!DNL Target] UI zullen in de toekomst worden veranderd en zullen in [[!DNL Target]  versienota&#39;s (huidig) &#x200B;](/help/main/r-release-notes/release-notes.md) worden aangekondigd wanneer deze veranderingen worden aangebracht.
>
>Voor alternerende montages, zie [&#x200B; Updates voor  [!DNL iPad]  en  [!DNL iPhone]  in [!UICONTROL Browser] publieksattributen (30 april, 2024) &#x200B;](#updates) hieronder.

Er zijn twee manieren om browsers als doel in te stellen:

* **Vooraf gebouwd publiek:** gebruik het pre-gebouwde publiek als u slechts bezoekers wilt richten die specifieke browser gebruiken om uw plaats te bezoeken. Als u bijvoorbeeld een extensie [!DNL Chrome] aanbiedt, richt u zich alleen op [!DNL Chrome] -gebruikers.

   1. Selecteer de browser in de vervolgkeuzelijst wanneer u uw activiteit instelt.

      Deze optie is alleen bestemd voor bezoekers die de opgegeven browser gebruiken.

      ![&#x200B; de gebruikers van Chrome van het Doel &#x200B;](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Aangepaste Browser de Regel van het Publiek:** Een aangepast publiek laat u veelvoudige browsers, of aan opstellingsregels of uitsluitingen voor specifieke browsers, browser versies, of browser talen richten. Deze functionaliteit biedt aanzienlijke flexibiliteit bij het kiezen van een activiteit op basis van browserkenmerken.

   1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]** .
   1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
   1. Sleep **[!UICONTROL Browser]** naar de Audience Builder.

      ![&#x200B; Regels > Browser &#x200B;](assets/target_browser.png)

   1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

      * **Type:** Doel of sluit bepaalde browser uit. Zie [&#x200B; Type &#x200B;](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Taal:** Doel of sluit bepaalde browsers uit die worden geplaatst om specifieke talen te gebruiken. Zie [&#x200B; Taal &#x200B;](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versie:** Doel of sluit bepaalde browser versies uit. Zie [&#x200B; Versie &#x200B;](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Optioneel) Stel aanvullende regels voor het publiek in.
   1. Klik op **[!UICONTROL Done]**.

  In het volgende voorbeeld wordt een publiek getoond dat [!DNL Microsoft Edge] -gebruikers in versies 91 of 92 bevat:

  ![&#x200B; Doel Edge 91 of 92 &#x200B;](assets/target_edge.png)

## Browseropties {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Hiermee kunt u deelnemers aan activiteiten op basis van het browsertype, de taal of de versie activeren of uitsluiten.

### Type {#section_6ADC758F23F145B3A310151546D83D56}

Een bepaalde browser activeren of uitsluiten.

Selecteer **[!UICONTROL Type]** en kies een van beide gelijk aan of niet gelijk aan.

* [!UICONTROL Equals]: wijs de geselecteerde browsers aan.
* [!UICONTROL Does not equal]: sluit de geselecteerde browsers uit.

Selecteer een of meer browsers. Meerdere opties zijn verbonden met een OR.

### Taal {#section_7520D1AA464A45A6843EABE2D2B431A1}

Stel bepaalde browsers die zijn ingesteld op het gebruik van specifieke talen in of uit.

Als een aanbieding bijvoorbeeld alleen in het Engels beschikbaar is, kunt u zich richten op browsers waarvan de taal is ingesteld op Engels. Als de pagina niet dubbel-byte ingeschakeld is, kunt u ook browsers uitsluiten die zijn ingesteld op Oost-Aziatische talen.

Het opnemen of uitsluiten van de browsertaal kan een nauwkeurigere keuze voor bezoekers opleveren dan een voorkeur op basis van geografische ligging in gevallen waarin taal belangrijker is dan locatie. Als u bijvoorbeeld een artikel aanbiedt dat in het Engels is geschreven, kunt u zich richten op Engelstalige landen of op browsers die zijn ingesteld op Engels. Als u de browser als doel instelt, wordt het artikel beschikbaar voor Engelse luidsprekers in landen waar Engels niet de primaire taal is.

Selecteer **[!UICONTROL Language]** en kies een van beide gelijk aan of niet gelijk aan.

* [!UICONTROL Equals]: wijs de geselecteerde browsertalen aan.
* [!UICONTROL Does not equal]: sluit de geselecteerde browsertalen uit.

Selecteer een of meer talen. Meerdere opties zijn verbonden met een OR.

De volgende browsertalen kunnen worden aangewezen of uitgesloten:

* Engels
* Frans
* Duits
* Japans
* Koreaans
* Portugees
* Russisch
* Spaans
* Traditioneel Chinees

### Versie {#section_37CC8CE45DA04E8682AE6388321BA6EF}

Bepaalde browserversies activeren of uitsluiten.

Als de pagina bijvoorbeeld niet correct wordt weergegeven in [!DNL Internet Explorer] versie 11 of lager, kunt u een publiek maken dat deze versies uitsluit. In dat geval stelt u een regel in waarbij het browsertype gelijk is aan [!DNL Internet Explorer] en voegt u een tweede regel toe waar de versie kleiner dan of gelijk is aan 11.

Selecteer **[!UICONTROL Version]** en kies vervolgens een operator:

* [!UICONTROL Equals]
* [!UICONTROL Does not equal]
* [!UICONTROL Is greater than]
* Is groter dan of gelijk aan
* [!UICONTROL Is less than]
* [!UICONTROL Is less than or equal to]

Typ het versienummer. Alleen hoofdversies kunnen in het tekstveld worden ingevoerd. De opgegeven versie bevat een kleine versie van die versie. Als u bijvoorbeeld versie 10 opgeeft, worden bezoekers van versie 10.1 ook opgenomen.

Meerdere opties zijn verbonden met een OR.

## De video van de opleiding: Creërend publiek ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Updates voor [!DNL iPad] en [!DNL iPhone] in [!UICONTROL Browser] publiekskenmerken (30 april 2024) {#updates}

[!DNL Adobe Target] laat u [&#x200B; richten op om het even welk van verscheidene categoriekenmerken &#x200B;](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), met inbegrip van gebruikers die specifieke browser of browser opties gebruiken wanneer zij uw pagina bezoeken.

Vanaf [!DNL Target] Standard/Premium 24.3.1 (4-6 maart 2024) zijn ingebouwde doelgroepen, zoals `Browser:iPad` en `Browser:iPhone` , bijgewerkt en worden ze op de juiste manier voor [!DNL iPad] en [!DNL iPhone] using `profile.mobile.deviceVendor` , `profile.mobile.isMobilePhone` en `profile.mobile.isTablet` gebruikt.

Ingebouwde soorten publiek die zijn gemaakt met de gebruikersinterface van [!DNL Target] , zoals `Browser:iPad` en `Browser:iPhone` , worden automatisch naar de nieuwe definitie van het publiek verplaatst en hoeven aan de zijde van de klanten niet te worden geactiveerd. Nochtans, zou u door:gaan, de hieronder beschreven montages [&#x200B; moeten gebruiken &#x200B;](#ui).

Als u `user.browserType` in om het even welke profielmanuscripten gebruikt om te controleren of is het [!DNL iPhone] of [!DNL iPad] (bijvoorbeeld, `user.browserType == 'iphone'` of `user.browserType != 'ipad'`), zouden die profielmanuscripten moeten worden veranderd zoals [&#x200B; hieronder &#x200B;](#profile-scripts) vóór 30 April, 2024 wordt geïnstrueerd om ervoor te zorgen dat deze publiek blijft functioneren zoals verwacht.

JavaScript-doelgroepen zijn verouderde doelgroepen die [!DNL Target] -expressies gebruiken die zijn vervangen door de [!DNL Target Classic] -gebruikersinterface. Deze soorten publiek kunnen alleen via de API worden gewijzigd. Klanten moeten deze soorten publiek alleen bijwerken als ze hun verouderde publiek blijven gebruiken voor activiteiten.

### Soorten publiek gemaakt met de gebruikersinterface van [!DNL Target] {#ui}

De volgende instellingen kunnen in de toekomst worden gebruikt:

* **Voor browserovereenkomsten[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![&#x200B; Apple &#x200B;](/help/main/r-release-notes/assets/apple.png)

* **voor browser past tablet** aan: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![&#x200B; mobiel is tablet &#x200B;](/help/main/r-release-notes/assets/is-tablet.png)

* **voor browser past iPad** aan: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] met een en container met [!UICONTROL Mobile] > [!UICONTROL Is Tablet] is [!DNL true]

  ![&#x200B; iPad &#x200B;](/help/main/r-release-notes/assets/ipad.png)

* **voor browser past iPhone** aan: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] met een en container met [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] is [!DNL true]

  ![&#x200B; iPhone &#x200B;](/help/main/r-release-notes/assets/iphone.png)

Er zijn vele andere mogelijke montages die zouden kunnen worden gebruikt, bijvoorbeeld wanneer de voorwaarden worden ontkend. Voorbeelden van negatiefactoren kunnen er als volgt uitzien:

* **voor browser past geen iPhone** aan: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] met een of container met [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] is [!UICONTROL false]

  ![&#x200B; niet mobiele telefoon &#x200B;](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **voor browser past geen iPad** aan: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] met een of container met [!UICONTROL Mobile] > [!UICONTROL Is Tablet] is [!UICONTROL false].

  ![&#x200B; niet tablet &#x200B;](/help/main/r-release-notes/assets/tablet-false.png)

### Soorten publiek gemaakt met behulp van profielscripts {#profile-scripts}

Als u `user.browserType` gebruikt in verouderde [!DNL Target Classic] soorten publiek of in profielscripts, moeten de volgende wijzigingen worden doorgevoerd:

* **BrowserType is iPhone**:

  Vervangen:

  `user.browserType=="iphone"`

  Met:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isMobilePhone`

* **BrowserType is geen iPhone**:

  Vervangen:

  `user.browserType!="iphone"`

  Met:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isMobilePhone`

* **BrowserType is iPad**:

  Vervangen:

  `user.browserType=="ipad"`

  Met:

  `profile.mobile.deviceVendor == "Apple" && profile.mobile.isTablet`

* **BrowserType is geen iPad**:

  Vervangen:

  `user.browserType!="ipad"`

  Met:

  `profile.mobile.deviceVendor != "Apple" || !profile.mobile.isTablet`