---
keywords: browser options;type;browser type;browser language;language;version;browser version
description: U kunt in Adobe Target een publiek maken dat zich richt op gebruikers die een specifieke browser of browseropties gebruiken wanneer zij uw pagina bezoeken.
title: Browseropties in Adobe Target-publiek
feature: audiences
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# Browser{#browser}

U kunt zich richten op gebruikers die een specifieke browser of specifieke browseropties gebruiken wanneer zij uw pagina bezoeken.

U kunt de volgende browsers als doel instellen:

* Chroom
* Microsoft Edge
* Firefox
* Opera
* Safari
* iPad
* Internet Explorer
* iPhone|

Er zijn twee manieren om browsers als doel in te stellen:

**Vooraf samengesteld publiek:** Gebruik het vooraf gebouwde publiek als u slechts bezoekers wilt richten die een specifieke browser gebruiken om uw plaats te bezoeken. Als u bijvoorbeeld een Chrome-extensie aanbiedt, richt u zich alleen op Chrome-gebruikers.

1. Selecteer de browser in de vervolgkeuzelijst voor het publiek wanneer u uw activiteit instelt.

   Deze optie is alleen bestemd voor bezoekers die de opgegeven browser gebruiken.

**Aangepaste regel voor het publiek in de browser:** een aangepast publiek biedt u de mogelijkheid om meerdere browsers als doel in te stellen, of om regels of uitsluitingen in te stellen voor specifieke browsers, browserversies of browsertalen. Dit biedt aanzienlijke flexibiliteit bij het aanwijzen van een campagne op basis van browserkenmerken.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Browser]**.

   ![Regels > Brower](assets/target_browser.png)

1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

   * **Type:bepaalde browser** activeren of uitsluiten. Zie [Type](/help/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
   * **Taal:** doel of sluit bepaalde browsers uit die worden geplaatst om specifieke talen te gebruiken. Zie [Taal](/help/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
   * **Versie:bepaalde browserversies** activeren of uitsluiten. Zie [Versie](/help/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).

1. (Optioneel) Klik op **[!UICONTROL Add Rule]** en stel aanvullende regels in voor het publiek.
1. Klik op **[!UICONTROL Save]**.

In het volgende voorbeeld wordt een publiek getoond dat Internet Explorer-gebruikers in versie 10 of 11 omvat:

![Doel: IE 10 en 11](/help/c-target/c-audiences/c-target-rules/assets/target_ie-10-11.png)

## Browseropties {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Hiermee kunt u deelnemers aan activiteiten op basis van het browsertype, de taal of de versie activeren of uitsluiten.

### Tekst {#section_6ADC758F23F145B3A310151546D83D56}

Een bepaalde browser activeren of uitsluiten.

Selecteer **[!UICONTROL Type]** en kies een van beide gelijk aan of niet gelijk aan.

* Gelijk aan: Selecteer de geselecteerde browsers.
* Is niet gelijk aan: Sluit de geselecteerde browsers uit.

Selecteer een of meer browsers. Meerdere opties zijn verbonden met een OR.

### Taal {#section_7520D1AA464A45A6843EABE2D2B431A1}

Stel bepaalde browsers die zijn ingesteld op het gebruik van specifieke talen in of uit.

Als een aanbieding bijvoorbeeld alleen in het Engels beschikbaar is, kunt u zich richten op browsers waarvan de taal is ingesteld op Engels. Als de pagina niet dubbel-byte ingeschakeld is, kunt u ook browsers uitsluiten die zijn ingesteld op Oost-Aziatische talen.

Het opnemen of uitsluiten van de browsertaal kan een nauwkeurigere keuze voor bezoekers opleveren dan een voorkeur op basis van geografische ligging in gevallen waarin taal belangrijker is dan locatie. Als u bijvoorbeeld een artikel aanbiedt dat in het Engels is geschreven, kunt u zich richten op Engelstalige landen of op browsers die zijn ingesteld op Engels. Als u de browser als doel instelt, wordt het artikel beschikbaar voor Engelse luidsprekers in landen waar Engels niet de primaire taal is.

Selecteer **[!UICONTROL Language]** en kies een van beide gelijk aan of niet gelijk aan.

* Gelijk aan: Kies de geselecteerde browsertalen.
* Is niet gelijk aan: Sluit de geselecteerde browsertalen uit.

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

Als uw pagina bijvoorbeeld niet correct wordt weergegeven in Internet Explorer versie 11 of lager, kunt u een publiek maken dat deze versies uitsluit. In dat geval, zou u opstelling een regel waar browser type Internet Explorer evenaart en een tweede regel toevoegt waar de versie minder dan of gelijk aan 11 is.

Selecteer **[!UICONTROL Version]**, dan kies een exploitant:

* Gelijk
* Is niet gelijk aan
* Is groter dan
* Is groter dan of gelijk aan
* Is kleiner dan
* Is kleiner dan of gelijk aan

Typ het versienummer.

Alleen hoofdversies kunnen in het tekstveld worden ingevoerd. De opgegeven versie bevat een kleine versie van die versie. Als u bijvoorbeeld versie 10 opgeeft, worden bezoekers van versie 10.1 opgenomen.

Meerdere opties zijn verbonden met een OR.

## Trainingsvideo: Soorten publiek ![Zelfstudie-badge](/help/assets/tutorial.png) maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)