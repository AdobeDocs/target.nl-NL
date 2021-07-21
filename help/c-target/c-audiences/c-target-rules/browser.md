---
keywords: browseropties;type;browsertype;browsertaal;taal;versie;browserversie
description: Leer hoe u een publiek kunt maken in  [!DNL Adobe Target] om gebruikers die een specifieke browser of specifieke browseropties gebruiken, als ze uw pagina bezoeken, als doel in te stellen.
title: Kan ik bezoekers richten die op Browser type worden gebaseerd?
feature: Soorten publiek
exl-id: 8420bbe3-b58a-4ddb-89bb-0265dab6b5fc
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Browser

U kunt zich richten op gebruikers die een specifieke browser of specifieke browseropties gebruiken wanneer zij uw pagina bezoeken.

U kunt de volgende browsers als doel instellen:

* Chroom
* Firefox
* Safari
* Internet Explorer
* Microsoft Edge
* Opera
* iPad
* iPhone|

Er zijn twee manieren om browsers als doel in te stellen:

* **Vooraf samengesteld publiek:** Gebruik het vooraf gebouwde publiek als u slechts bezoekers wilt richten die een specifieke browser gebruiken om uw plaats te bezoeken. Als u bijvoorbeeld een Chrome-extensie aanbiedt, richt u zich alleen op Chrome-gebruikers.

   1. Selecteer de browser in de vervolgkeuzelijst wanneer u uw activiteit instelt.

      Deze optie is alleen bestemd voor bezoekers die de opgegeven browser gebruiken.

      ![Doelgebruikers van Chrome](/help/c-target/c-audiences/c-target-rules/assets/target-chrome.png)

* **Aangepaste regel voor het publiek in de browser: met** een aangepast publiek kunt u meerdere browsers als doel instellen of regels of uitsluitingen instellen voor specifieke browsers, browserversies of browsertalen. Deze functionaliteit biedt aanzienlijke flexibiliteit bij het kiezen van een activiteit op basis van browserkenmerken.

   1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
   1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
   1. Sleep **[!UICONTROL Browser]** in de ruit van de publieksbouwer.

      ![Regels > Browser](assets/target_browser.png)

   1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

      * **Type:bepaalde browser** activeren of uitsluiten. Zie [Type](/help/c-target/c-audiences/c-target-rules/browser.md#section_6ADC758F23F145B3A310151546D83D56).
      * **Taal:bepaalde browsers** die zijn ingesteld op het gebruik van bepaalde talen, als doel instellen of uitsluiten. Zie [Taal](/help/c-target/c-audiences/c-target-rules/browser.md#section_7520D1AA464A45A6843EABE2D2B431A1).
      * **Versie:bepaalde browserversies** activeren of uitsluiten. Zie [Versie](/help/c-target/c-audiences/c-target-rules/browser.md#section_37CC8CE45DA04E8682AE6388321BA6EF).
   1. (Optioneel) Stel aanvullende regels voor het publiek in.
   1. Klik op **[!UICONTROL Done]**.

   In het volgende voorbeeld ziet u een publiek dat Microsoft Edge-gebruikers in versie 91 of 92 omvat:

   ![Doelrand 91 of 92](assets/target_edge.png)

## Browseropties {#concept_221D8EEF53CC45AEACEB17CF336A3658}

Hiermee kunt u deelnemers aan activiteiten op basis van het browsertype, de taal of de versie activeren of uitsluiten.

### Type {#section_6ADC758F23F145B3A310151546D83D56}

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

Typ het versienummer. Alleen hoofdversies kunnen in het tekstveld worden ingevoerd. De opgegeven versie bevat een kleine versie van die versie. Als u bijvoorbeeld versie 10 opgeeft, worden bezoekers van versie 10.1 ook opgenomen.

Meerdere opties zijn verbonden met een OR.

## Trainingsvideo: Soorten publiek ![Zelfstudie-badge](/help/assets/tutorial.png) maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
