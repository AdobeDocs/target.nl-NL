---
keywords: ervaringsvoorvertoning;ervaring URL's;genereren URL's;belevenis weergeven
description: Leer hoe u URL's met voorvertoningen voor Adobe kunt gebruiken [!DNL Target] Automated Personalization-activiteiten om inhoud direct op uw site te bekijken voordat de activiteit actief is.
title: Hoe kan ik URL's van het ervaringsvoorbeeld in Automated Personalization-activiteiten gebruiken?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Automated Personalization
exl-id: 9f329b8a-5f86-4cae-a3be-eed24fa0a9cd
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Automated Personalization-activiteiten voorvertonen met voorbeeld-URL&#39;s

U kunt voorvertonings-URL&#39;s genereren voor [!DNL Target] [!UICONTROL Automated Personalization] activiteiten om inhoud direct op uw site te zien voordat de activiteit live is voor een voorvertoning en kwaliteitscontrole. Ervaar de voorvertoning van URL&#39;s en omzeilt het opgeven van doelen om een bepaalde ervaring geforceerd weer te geven.

>[!NOTE]
>
>U kunt voorvertonings-URL&#39;s maken voor andere typen [!DNL Target] activiteiten. Het proces is echter iets anders. Zie voor meer informatie [Activiteit QA](/help/main/c-activities/c-activity-qa/activity-qa.md#preview).

Gebruik de ervaring voorproef URLs om ervaringen met teamleden en aan ervaring van QA over browsers en milieu&#39;s te delen, zonder een afzonderlijke activiteit van QA te creëren. Deze functie is vooral handig als een site complex is of als het beveiligingsbeleid het niet toestaat dat de site in een simulator wordt weergegeven.

1. Een [Automated Personalization-activiteit](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9) of klik op de activiteit om deze te openen.

   De activiteit hoeft niet live te zijn voor een voorvertoning van een ervaring.

1. Klik op de pagina Overzicht activiteit op de drie verticale punten en klik vervolgens op **[!UICONTROL View Experience URLs]**.

1. Bekijk en/of geef uw URL&#39;s op.

   * Als u het [!UICONTROL Visual Experience Composer] (VEC) wordt de standaard-URL die u voor de activiteit hebt opgegeven automatisch ingevoerd en wordt een koppeling gegenereerd voor elke ervaring in uw activiteit. U kunt deze URL wijzigen en desgewenst andere URL&#39;s toevoegen.
   * Als u het [!UICONTROL Form-Based Experience Composer], wordt automatisch geen standaard-URL ingevoerd. Als u nog geen URL&#39;s met voorvertoningen hebt gemaakt, klikt u op **Nieuwe URL toevoegen**. U moet alle URL&#39;s opgeven die u wilt voorvertonen, en een naam voor elke URL.

   U kunt meerdere URL&#39;s toevoegen. Dit is handig wanneer u een test met meerdere pagina&#39;s of een sjabloontest uitvoert en u de activiteit op meerdere pagina&#39;s wilt voorvertonen.

   Een modaal venster toont verbindingen aan uw ervaringen op uw plaats om een &quot;ware voorproef&quot;van de ervaringen buiten te krijgen [!DNL Target] VEC. U moet de koppelingen vanuit het bericht delen om de voorvertoning te kunnen delen. Het klikken van een verbinding en dan het kopiëren van resulterende URL van de pagina zal niet werken omdat URL een parameter bevat die slechts de pagina correct toont wanneer u tot de pagina van de verbinding in het bericht toegang hebt. Kopieer in plaats daarvan de tekst in het modale venster en e-mail de hele tekst naar uw team.

1. Klikken **[!UICONTROL Generate All]** en klikt u op elke ervaring om deze voor te vertonen.

   Als u dan veranderingen in de ervaring aanbrengt, zorg ervoor om nieuwe voorproefverbindingen voor uw team te produceren door aan het modale venster terug te keren en te klikken **Koppelingen vernieuwen** voor nieuwe koppelingen.

   >[!NOTE]
   >
   >Als u een voorvertoning van koppelingen opent op nieuwe tabbladen, is het vereist dat de pop-upblokkering in uw browser is uitgeschakeld.

1. Klik op de naam van elke ervaring om een voorvertoning van de activiteit weer te geven.

   De pagina wordt geopend en de activiteit wordt weergegeven.

1. Klikken **[!UICONTROL Done]** om terug te keren naar het activiteitenoverzicht.

## Overwegingen {#example_9F2B333BC63143FF99AE331F57E8BA4C}

**URL&#39;s met voorvertoningen genereren**

* De URL van de ervaringsvoorvertoning wordt niet beïnvloed door de verkeersverdeling tussen ervaringen.
* Doelgerichtheid op publiek niveau heeft geen invloed op de voorvertoning.
* U kunt automatisch maximaal 300 ervaring-URL&#39;s per activiteit genereren. Daarna moet u de URL&#39;s handmatig genereren.
* Afhankelijk van het aantal ervaringen kan het maximaal vijf minuten duren om de URL&#39;s te genereren. Sluit het dialoogvenster niet en de gegenereerde URL&#39;s gaan verloren.
* De gegenereerde voorbeeldkoppelingen zijn twee maanden geldig. Hierna moet u de URL&#39;s van de voorvertoning opnieuw genereren.
* U moet telkens opnieuw genereren wanneer een ervaring wordt gewijzigd.

**Voorvertoning-URL&#39;s delen**

* U kunt een voorvertoning van een ervaring weergeven, zelfs als u geen deel uitmaakt van het doelpubliek.
* U kunt URL&#39;s met voorvertoningen delen met collega&#39;s die geen toegang hebben tot [!DNL Adobe Target].

**Ervaringen weergeven met URL&#39;s met voorvertoningen**

* De voorvertoning werkt voor opgeslagen activiteiten, zolang de pagina niet is gewijzigd.
* De voorbeeld-URL voor ervaring is beschikbaar, ongeacht of de activiteit actief of inactief is.
* U kunt geen voorvertoning weergeven van een ervaring in [!UICONTROL Draft] status.
* Rapportering wordt niet beïnvloed door het bekijken van voorbeeld-URL&#39;s.

**Voorvertoning-URL&#39;s voor probleemoplossing**

* Als u de voorvertoning niet kunt zien op het nieuwe tabblad (vanwege de cache van de browser), probeert u de koppeling twee of drie keer te vernieuwen of kopieert u de koppeling en opent u deze in een nieuwe browser, nieuwe sessie of in een modus voor een privébrowser.
