---
keywords: browseropties;type;browsertype;browsertaal;taal;versie;browserversie
description: Leer hoe u een publiek kunt maken in [!DNL Adobe Target] om gebruikers te richten die een specifieke browser of specifieke browser opties gebruiken wanneer zij uw pagina bezoeken.
title: Kan ik bezoekers richten die op Browser type worden gebaseerd?
feature: Audiences
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: 968f9982299156d3f4d599d00322106fe3629610
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 0%

---

# Browser

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
>Vanaf 30 april 2024, [!DNL iPad] en [!DNL iPhone] wordt verwijderd uit de beschikbare [!UICONTROL Browser] Typ een vervolgkeuzelijst bij het maken van categorieën voor het publiek. Zie voor instellingen voor tijdelijke oplossing [Afschrijving van iPad en iPhone van kenmerk Browser-publiek (30 april 2024)](#deprecation) hieronder.

Er zijn twee manieren om browsers als doel in te stellen:

* **Vooraf gebouwd publiek:** Gebruik het vooraf gebouwde publiek als u alleen bezoekers wilt aanspreken die een specifieke browser gebruiken om uw site te bezoeken. Als u bijvoorbeeld een [!DNL Chrome] extensie, alleen als doel instellen [!DNL Chrome] gebruikers.

   1. Selecteer de browser in de vervolgkeuzelijst wanneer u uw activiteit instelt.

      Deze optie is alleen bestemd voor bezoekers die de opgegeven browser gebruiken.

      ![Doelgebruikers van Chrome](/help/main/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Aangepaste regel browserpubliek:** Met een aangepast publiek kunt u zich richten op meerdere browsers of op het instellen van regels of uitsluitingen voor specifieke browsers, browserversies of browsertalen. Deze functionaliteit biedt aanzienlijke flexibiliteit bij het kiezen van een activiteit op basis van browserkenmerken.

   1. In de [!DNL Target] interface, klik **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
   1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
   1. Slepen en slepen **[!UICONTROL Browser]** in de Audience Builder.

      ![Regels > Browser](assets/target_browser.png)

   1. Klikken **[!UICONTROL Select]** Selecteer vervolgens een van de volgende opties:

      * **Type:** Een bepaalde browser activeren of uitsluiten. Zie [Type](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Taal:** Stel bepaalde browsers die zijn ingesteld op het gebruik van specifieke talen in of uit. Zie [Taal](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versie:** Bepaalde browserversies activeren of uitsluiten. Zie [Versie](/help/main/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

   1. (Optioneel) Stel aanvullende regels voor het publiek in.
   1. Klik op **[!UICONTROL Done]**.

  In het volgende voorbeeld wordt een publiek getoond dat [!DNL Microsoft Edge] gebruikers in versie 91 of 92:

  ![Doelrand 91 of 92](assets/target_edge.png)

## Browseropties {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Hiermee kunt u deelnemers aan activiteiten op basis van het browsertype, de taal of de versie activeren of uitsluiten.

### Type {#section_6ADC758F23F145B3A310151546D83D56}

Een bepaalde browser activeren of uitsluiten.

Selecteren **[!UICONTROL Type]** kiest u een van beide gelijk aan of niet gelijk aan.

* [!UICONTROL Equals]: Kies voor de geselecteerde browsers.
* [!UICONTROL Does not equal]: Sluit de geselecteerde browsers uit.

Selecteer een of meer browsers. Meerdere opties zijn verbonden met een OR.

### Taal {#section_7520D1AA464A45A6843EABE2D2B431A1}

Stel bepaalde browsers die zijn ingesteld op het gebruik van specifieke talen in of uit.

Als een aanbieding bijvoorbeeld alleen in het Engels beschikbaar is, kunt u zich richten op browsers waarvan de taal is ingesteld op Engels. Als de pagina niet dubbel-byte ingeschakeld is, kunt u ook browsers uitsluiten die zijn ingesteld op Oost-Aziatische talen.

Het opnemen of uitsluiten van de browsertaal kan een nauwkeurigere keuze voor bezoekers opleveren dan een voorkeur op basis van geografische ligging in gevallen waarin taal belangrijker is dan locatie. Als u bijvoorbeeld een artikel aanbiedt dat in het Engels is geschreven, kunt u zich richten op Engelstalige landen of op browsers die zijn ingesteld op Engels. Als u de browser als doel instelt, wordt het artikel beschikbaar voor Engelse luidsprekers in landen waar Engels niet de primaire taal is.

Selecteren **[!UICONTROL Language]** kiest u een van beide gelijk aan of niet gelijk aan.

* [!UICONTROL Equals]: Kies de geselecteerde browsertalen.
* [!UICONTROL Does not equal]: Sluit de geselecteerde browsertalen uit.

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

Als uw pagina bijvoorbeeld niet correct wordt weergegeven in [!DNL Internet Explorer] In versie 11 of lager kunt u een publiek maken dat deze versies uitsluit. In dat geval zou u een regel instellen waarbij het browsertype gelijk is [!DNL Internet Explorer] en voeg een tweede regel toe waar de versie 11 of lager is.

Selecteren **[!UICONTROL Version]** kiest u vervolgens een operator:

* [!UICONTROL Equals]
* [!UICONTROL Does not equal]
* [!UICONTROL Is greater than]
* Is groter dan of gelijk aan
* [!UICONTROL Is less than]
* [!UICONTROL Is less than or equal to]

Typ het versienummer. Alleen hoofdversies kunnen in het tekstveld worden ingevoerd. De opgegeven versie bevat een kleine versie van die versie. Als u bijvoorbeeld versie 10 opgeeft, worden bezoekers van versie 10.1 ook opgenomen.

Meerdere opties zijn verbonden met een OR.

## Trainingsvideo: Soorten publiek maken ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Categorieën publiek definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)

## Afschrijving van iPad en iPhone van kenmerk Browser-publiek (30 april 2024) {#deprecation}

[!DNL Adobe Target] laat u [doel op een van de verschillende categoriekenmerken](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusief gebruikers die een specifieke browser of browseropties gebruiken wanneer ze uw pagina bezoeken.

Vanaf 30 april 2024 worden iPad en iPhone van de beschikbare [!UICONTROL Browser] Typ een vervolgkeuzelijst bij het maken van categorieën voor het publiek.

Ingebouwd publiek, zoals &quot;Browser: iPad&quot; en &quot;Browser: iPhone&quot;, wordt automatisch naar de nieuwe definitie van het publiek verplaatst. Alle profielscripts die &quot;user.browserType&quot; gebruiken, worden *niet* automatisch worden bijgewerkt: als u deze niet handmatig bijwerkt, kan de kwalificatie van de gebruiker niet naar behoren plaatsvinden.

Als u een publiek hebt dat iPads of iPhones als doel heeft met de [!UICONTROL Browser] moet u deze instellingen vóór 30 april 2024 wijzigen om ervoor te zorgen dat dit publiek naar behoren blijft functioneren.

### Soorten publiek gemaakt met de [!DNL Target] UI

De volgende instellingen kunnen in de toekomst worden gebruikt:

* **Voor browserovereenkomsten[!DNL Apple]**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL matches] [!DNL Apple]

  ![Apple](/help/main/r-release-notes/assets/apple.png)

* **Voor browserovereenkomsten met tablet**: [!UICONTROL Mobile] > [!UICONTROL is Tablet] > [!UICONTROL true]

  ![mobile is tablet](/help/main/r-release-notes/assets/is-tablet.png)

* **Voor browsers komt iPad overeen**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPad] met een en-container [!UICONTROL Mobile] > [!UICONTROL Is Tablet] is [!DNL true]

  ![iPad](/help/main/r-release-notes/assets/ipad.png)

* **Voor browsers komt iPhone overeen**: [!UICONTROL Mobile] > [!UICONTROL Device Marketing Name] [!UICONTROL matches] [!DNL iPhone] met een en-container [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] is [!DNL true]

  ![iPhone](/help/main/r-release-notes/assets/iphone.png)

Er zijn vele andere mogelijke montages die zouden kunnen worden gebruikt, bijvoorbeeld wanneer de voorwaarden worden ontkend. Voorbeelden van negatiefactoren kunnen er als volgt uitzien:

* **Voor browser komt niet overeen met iPhone**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] met een of container met [!UICONTROL Mobile] > [!UICONTROL Is Mobile Phone] is [!UICONTROL false]

  ![Geen mobiele telefoon](/help/main/r-release-notes/assets/mobile-phone-false.png)

* **Voor browser komt niet overeen met iPad**: [!UICONTROL Mobile] > [!UICONTROL Device Vendor] [!UICONTROL does not match] [!UICONTROL Apple] met een of container met [!UICONTROL Mobile] > [!UICONTROL Is Tablet] is [!UICONTROL false].

  ![Geen tablet](/help/main/r-release-notes/assets/tablet-false.png)

### Soorten publiek gemaakt met behulp van profielscripts

Als u `user.browserType` in soorten publiek die profielscripts gebruiken, zoals wordt uitgelegd in [Profiel en verklarende woordenlijst voor variabelen](/help/main/c-target/c-visitor-profile/variables-profiles-parameters-methods.md), moeten de volgende wijzigingen worden aangebracht:

>[!NOTE]
>
>De volgende profielen zullen naar verwachting de komende dagen, vanaf 24 januari 2024, worden vrijgegeven. De [Opmerkingen bij de huidige release](/help/main/r-release-notes/release-notes.md) worden bijgewerkt wanneer deze profielen beschikbaar zijn.
>
>Deze profielen maken de volgende wijzigingen mogelijk:
>
>* `profile.mobile.isTablet`
>
>* `profile.mobile.isMobilePhone`

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