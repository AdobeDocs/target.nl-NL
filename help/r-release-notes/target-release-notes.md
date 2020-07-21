---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Opmerkingen bij de release die informatie bevatten over functies, verbeteringen en oplossingen voor de nieuwste of komende DNL Adobe Target-releases.
title: Voorlopige Adobe Target-opmerkingen
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 26447c745cf56f3e04ad477bc05446e5d8ab76c1
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---


# Opmerkingen bij de release van Target (preRelease){#target-release-notes-prerelease}

Dit artikel bevat pre-releasegegevens. Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.

**Laatst bijgewerkt: 22 juli 2020**

Zie Opmerkingen bij de release van [Target voor informatie over de huidige release](release-notes.md). De informatie op deze pagina&#39;s kan gelijk zijn, afhankelijk van de timing van releases. De uitgiftenummers tussen haakjes zijn bedoeld voor intern [!DNL Adobe] gebruik.

>[!NOTE]
>
>* **afdruk** mbox.js: Op 30 augustus 2020 biedt Adobe Target geen ondersteuning meer voor de bibliotheek mbox.js. Na 30 augustus 2020 zullen alle aanroepen van mbox.js op elegante wijze mislukken en van invloed zijn op uw pagina&#39;s waarop Target-activiteiten worden uitgevoerd door de standaardinhoud te bedienen. Wij adviseren dat alle klanten aan de meest recente versie van de bibliotheek at.js vóór deze datum migreren om het even welke potentiële kwesties met uw plaatsen te vermijden. Voor meer informatie, zie [Hoe werkt](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) At.js en [de Bouwer van de Vaardigheid van Adobe Target: Chat ontwikkelaar, migrate Adobe Target mbox.js aan at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Hoewel mbox.js momenteel wordt ondersteund, hebben we sinds juli 2017 geen functie-updates voor deze bibliotheek beschikbaar gesteld. Het nieuwere bestand at.js biedt veel voordelen ten opzichte van mbox.js. Met at.js verbetert u onder andere de laadtijden van pagina&#39;s voor webimplementaties, verbetert u de beveiliging en biedt u betere implementatieopties voor toepassingen op één pagina.
   >
   >   
   Door alle klanten naar at.js te verplaatsen, kunnen onze technici en ondersteunend personeel u nieuwe functionaliteit bieden en de ondersteuning bieden die u van Adobe hebt verwacht.
   >
   >
* **Aankondigingen** van Target: Zie de Target-aankondigingspagina voor informatie over aanstaande gebeurtenissen, zoals Target Skill Builder-sessies, ontwikkelaarstekkers, webinars en Target Coffee Break-sessies. Zie [Target-aankondigingen](/help/r-release-notes/target-announcements.md)voor meer informatie.


## Target Standard/Premium 20.7.1 (22 juli 2020)

Deze release bevat de volgende verbeteringen:

### [!UICONTROL Administration] sectie-UI vernieuwen

We herschrijven geleidelijk de gehele [!DNL Target] gebruikersinterface met behulp van een nieuwe technologiestapel om verbeterde prestaties te kunnen bieden, de vereiste onderhoudstijd bij het vrijgeven van nieuwe functies te verminderen en de gebruikerservaring in het hele product te verbeteren. De eerste sectie die is vernieuwd, is de [!UICONTROL Setup] sectie, die is hernoemd [!UICONTROL Administration].

Als onderdeel van deze vernieuwing kunt u gemakkelijk veel handelingen uitvoeren met de pagina&#39;s in de [!UICONTROL Administration] sectie, zoals:

* Download het meest recente bestand at.js van het [!UICONTROL Implementation] tabblad (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Pas de instellingen op at.js aan en bekijk de wijzigingen eenvoudig (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**).
* Wijzig verbeterde rapporteringsmontages, zoals de standaardmunt en tijdzone, IPs om van rapportering uit te sluiten, etc. (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]**)
* IP-adressen van bezoekers om privacyredenen verduisteren (**[!UICONTROL Administration]** > **[!UICONTROL Implementation]**)
* Bekijk de bestaande lijst met gebruikers per werkruimte en hun rollen voordat u deze in Adobe Admin Console (**[!UICONTROL Administration]** > **[!UICONTROL Users]**) beheert.
* Alle tabellen in de [!UICONTROL Administration] sectie zoeken en filteren.

### Verbeteringen, correcties en wijzigingen

Deze release bevat de volgende verbeteringen, correcties en wijzigingen:

* Probleem verholpen waarbij sitevoorkeuren niet konden worden behouden na vernieuwen. (TGT-37239)
* Probleem verholpen waarbij het functioneren van > [!UICONTROL Insert After] [!UICONTROL Image] met SVG-afbeeldingen (Scalable Vector Graphics) werd verhinderd. (TGT-37242)
* Oplossing voor een probleem voor gebruikers met de [!UICONTROL Publisher] rol die het verwijderen van conceptactiviteiten heeft verhinderd. (TGT-37358)
* Probleem verholpen waardoor gebruikers een activiteit niet konden bewerken wanneer deze [!UICONTROL All My Workspaces] is geselecteerd. (TGT-37276)

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Meld u aan voor de Adobe Priority Product Update als u geavanceerde meldingen wilt ontvangen over toekomstige productverbeteringen voor Target en andere Adobe Experience Cloud-oplossingen:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
