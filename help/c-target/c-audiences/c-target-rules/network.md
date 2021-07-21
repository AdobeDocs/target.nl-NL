---
keywords: gericht;netwerk;doelnetwerk;isp;domeinnaam;verbindingssnelheid;doel isp;doeldomeinnaam;doelverbindingssnelheid
description: Leer hoe te om publiek in [!DNL Adobe Target] te creëren gebaseerd op netwerkdetails.
title: Kan ik Bezoekers richten op basis van netwerkopties?
feature: Soorten publiek
exl-id: 0a479d6d-ca17-43b8-9a42-8e68f31d4d54
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---

# Netwerk

U kunt publiek in [!DNL Adobe Target] tot stand brengen die op netwerkdetails, zoals ISP, domeinnaam, en verbindingssnelheid wordt gebaseerd.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Network]** in de ruit van de publieksbouwer.
1. Klik op **[!UICONTROL Select]** en selecteer een van de volgende opties:

   * **ISP:** ISP is een organisatie die Internet toegang tot zijn abonnees, gewoonlijk tegen een maandelijkse of jaarlijkse prijs verleent. Vele ISPs verleent de extra diensten, zoals Web het ontvangen of e-mail. Het ISP gebied is of commerciële ISP (zoals Comcast of TimeWarner) of een andere entiteit zoals een zaken of onderwijsinstelling.

      Hieronder volgen enkele voorbeelden van populaire ISP&#39;s in de Verenigde Staten:

      | Populaire naam | ISP-naam | Domeinnaam | Voorbeeld-IP-adres |
      |---|---|---|---|
      | Cablevision | Cablevision Systems Corp. | *.optonline.net | 68 196 130 239 |
      | CenturyLink | Qwest Communications Company, LLC | *.centurylink.net | 64 40 65,0 |
      | Chartercommunicatie | Chartercommunicatie | *.charter.com | 71 85 225 124 |
      | Comcast | Comcast Cable Communications, Inc. | *.comcast.net | 76.27.24.28 |
      | Cox | Cox Communications Inc. | *cox.net | 68 224 174,22 |
      | Luidsprekend | MegaPath Corporation | *.speakeasy.net | 66 93 240,0 |
      | Time Warner | Time Warner Cable Internet LLC | *.res.rr.com | 72 229 28 185 |
      | Verizon FiOS | MCI Communications Services, Inc. d/b/a Verizon Business | *.fios.verizon.net | 173 68 112,34 |
      | Vivint | Smartrove Inc. | *.vivintradio.net | 170 72 26 105 |
      | AT&amp;T Wireless | AT | *.mycingular.net |  |
      | Mobiel afdrukken | Persoonlijke communicatiesystemen afdrukken | ip-adres |  |
      | T-Mobile | T-Mobile USA, Inc. | ip-adres | 208 54 86,0 |
      | Verizon Wireless | Cellco Parternship DBA Verizon Wireless | *.myvzw.com | 70 195 74 199 |

      >[!NOTE]
      >
      >Wanneer het richten gebaseerd op ISP, gebruik de ISP naam, niet de populaire naam. Zorg ervoor dat u de regel maakt zodat deze niet hoofdlettergevoelig is of altijd de indeling in kleine letters gebruikt.

      U kunt de waarden voor de ISP- en domeinnaam testen. [https://www.whoismyisp.](https://www.whoismyisp.org) orgis een goede bron voor doelgerichte doeleinden. U kunt de steekproefIP adressen gebruiken die in de lijst hierboven worden gegeven, of uw ingaan. Dan gebruik `mboxOverride.browserIp= URL` parameter om dat IP adres na te bootsen.

   * **Domeinnaam:** deze naam is de domeinnaam voor het IP-adres van de bezoeker. Deze naam is niet de domeinnaam van de website die u gebruikt met [!DNL Target]. Deze domeinnaam is gerelateerd aan het IP-adres van de bezoeker en wordt soms een hostnaam genoemd. Het is gelijkaardig aan de ISP naam. Soms verwijzingen hostname oudere namen van bedrijven die hun ISP naam maar niet de domeinnaam hebben herbrandd.
   * **Verbindingssnelheid:** deze snelheid is de snelheid waarmee de bezoeker verbinding maakt met internet. De volgende opties zijn beschikbaar: breedband, kabel, dialup, mobiel, oc3, oc12, satelliet, t1, t2, en radio, en xdsl.

      Dit veld is gebaseerd op het type verbinding en niet op de werkelijke snelheid zelf. [!DNL Target] kan niet de nauwkeurige verbindingssnelheden van verbindingen bepalen. Het verbindingstype Breedband wordt gebruikt wanneer er geen aanwijzing van andere verbindingstypes is zodat kan een specifiek type niet worden gekozen.

1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

In de volgende afbeelding ziet u een publiek dat is gericht op bezoekers die AT&amp;T gebruiken met een verbindingssnelheid van [!UICONTROL Mobile].

![Netwerkdoel](assets/target_network.png)

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
