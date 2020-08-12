---
keywords: experience preview;experience urls;generate urls;view experience urls
description: U kunt voorvertonings-URL's genereren voor Target Automated Personalization-activiteiten, zodat u direct op uw site inhoud kunt zien voordat de activiteit live is voor voorvertoning en kwaliteitscontrole. Ervaar de voorvertoning van URL's en omzeilt het opgeven van doelen om een bepaalde ervaring geforceerd weer te geven.
title: Automated Personalization-activiteiten voorvertonen met voorbeeld-URL's
feature: null
topic: Standard
uuid: 2ef07b6c-086d-43ac-bf02-efe217652a3a
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 0%

---


# ![PREMIUM](/help/assets/premium.png) Preview Automated Personalization-activiteiten met voorbeeld-URL&#39;s{#share-experience-urls-to-preview-automated-personalization-outside-of-target}

U kunt voorvertonings-URL&#39;s genereren voor Target Automated Personalization-activiteiten, zodat u direct op uw site inhoud kunt zien voordat de activiteit live is voor voorvertoning en kwaliteitscontrole. Ervaar de voorvertoning van URL&#39;s en omzeilt het opgeven van doelen om een bepaalde ervaring geforceerd weer te geven.

>[!NOTE]
>
>De voorvertoning-URL&#39;s voor Automated Personalization verschillen van de modus Activiteit-QA. Met de modus Activiteit-QA kunt u Activiteiten-URL&#39;s maken voor andere typen activiteiten. Zie [Activiteit QA](../../c-activities/c-activity-qa/activity-qa.md#concept_9329EF33DE7D41CA9815C8115DBC4E40)voor meer informatie.
>
>De voorproef URLs van de ervaring voor AP activiteiten zijn slechts beschikbaar wanneer het gebruiken van at.js 1.x. De voorproef URLs van de ervaring voor AP activiteiten wordt momenteel niet gesteund voor at.js 2.x.

Gebruik de ervaring voorproef URLs om ervaringen met teamleden en aan ervaring van QA over browsers en milieu&#39;s te delen, zonder een afzonderlijke activiteit van QA te creëren. Deze functie is vooral handig als een site complex is of als het beveiligingsbeleid het niet toestaat dat de site in een simulator wordt weergegeven.

1. Maak een [Automated Personalization-activiteit](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) of klik op de activiteit om deze te openen.

   De activiteit hoeft niet live te zijn voor een voorvertoning van een ervaring.
1. Klik op de overzichtspagina van de activiteit op de drie verticale punten en klik vervolgens **[!UICONTROL View Experience URLs]**.
1. Bekijk en/of geef uw URL&#39;s op.

   * Als u Composer van de Visuele Ervaring gebruikt, wordt het gebrek URL u voor de activiteit specificeerde automatisch ingegaan en een verbinding wordt geproduceerd voor elke ervaring in uw activiteit. U kunt deze URL wijzigen en desgewenst andere URL&#39;s toevoegen.
   * Als u de Form-Based Experience Composer gebruikt, wordt er niet automatisch een standaard-URL ingevoerd. Als u nog geen URL&#39;s met voorvertoningen hebt gemaakt, klikt u op Nieuwe URL **** toevoegen. U moet alle URL&#39;s opgeven die u wilt voorvertonen, en een naam voor elke URL.

   U kunt meerdere URL&#39;s toevoegen. Dit is handig wanneer u een test met meerdere pagina&#39;s of een sjabloontest uitvoert en u de activiteit op meerdere pagina&#39;s wilt voorvertonen.

   Een modaal venster toont verbindingen aan uw ervaringen op uw plaats om een &quot;ware voorproef&quot;van de ervaringen buiten Composer van de Visuele Ervaring van het Doel te krijgen. U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. Het klikken van een verbinding en dan het kopiëren van resulterende URL van de pagina zal niet werken omdat URL een parameter bevat die slechts de pagina correct toont wanneer u tot de pagina van de verbinding in het bericht toegang hebt. Kopieer in plaats daarvan de tekst in het modale venster en e-mail de hele tekst naar uw team.
1. Klik **[!UICONTROL Generate All]** en klik op elke ervaring om deze voor te vertonen.

   Als u dan veranderingen in de ervaring aanbrengt, zorg ervoor om nieuwe voorproefverbindingen voor uw team te produceren door aan het modale venster terug te keren en **Nieuwe Verbindingen** te klikken om nieuwe verbindingen te krijgen.

   **Opmerking:** De voorvertoningskoppelingen worden geopend op nieuwe tabbladen en vereisen dat de pop-upblokkering in uw browser is uitgeschakeld.

1. Klik op de naam van elke ervaring om een voorvertoning van de activiteit weer te geven.

   De pagina wordt geopend en de activiteit wordt weergegeven.
1. Klik **[!UICONTROL Done]** om terug te keren naar het activiteitenoverzicht.

## Overwegingen {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**URL&#39;s met voorvertoningen genereren**

* De URL van de ervaringsvoorvertoning wordt niet beïnvloed door de verkeersverdeling tussen ervaringen.
* Doelgerichtheid op publiek niveau heeft geen invloed op de voorvertoning.
* U kunt automatisch maximaal 300 ervaring-URL&#39;s per activiteit genereren. Daarna moet u de URL&#39;s handmatig genereren.
* U kunt automatisch maximaal 300 ervaring-URL&#39;s per activiteit genereren. Daarna moet u de URL&#39;s handmatig genereren.
* Afhankelijk van het aantal ervaringen kan het maximaal vijf minuten duren om de URL&#39;s te genereren. Sluit het dialoogvenster niet of de gegenereerde URL&#39;s gaan verloren.
* De gegenereerde voorbeeldkoppelingen zijn twee maanden geldig. Hierna moet u de URL&#39;s van de voorvertoning opnieuw genereren.
* U moet telkens opnieuw genereren wanneer een ervaring wordt gewijzigd.

**Voorvertoning-URL&#39;s delen**

* U kunt een voorvertoning van een ervaring weergeven, zelfs als u geen deel uitmaakt van het doelpubliek.
* U kunt voorbeeld-URL&#39;s delen met collega&#39;s die geen toegang hebben tot Adobe Target.

**Ervaringen weergeven met URL&#39;s met voorvertoningen**

* De voorvertoning werkt voor opgeslagen activiteiten, zolang de pagina niet is gewijzigd.
* De voorbeeld-URL voor ervaring is beschikbaar, ongeacht of de activiteit actief of inactief is.
* U kunt geen voorbeeld bekijken van een ervaring in de conceptstatus.
* Rapportering wordt niet beïnvloed door het bekijken van voorbeeld-URL&#39;s.

**Voorvertoning-URL&#39;s voor probleemoplossing**

* Als u de voorvertoning niet kunt zien op het nieuwe tabblad (vanwege de cache van de browser), probeert u de koppeling twee of drie keer te vernieuwen of kopieert u de koppeling en opent u deze in een nieuwe browser, nieuwe sessie of in de modus van een privébrowser.
