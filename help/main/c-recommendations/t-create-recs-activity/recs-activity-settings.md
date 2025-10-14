---
keywords: Aanbevelingen;Instellingen;naam;doel;prioriteit;duur;rapportage-instellingen;andere metagegevens
description: Leer hoe te om de montages te vormen die worden gebruikt om een activiteit van Aanbevelingen in Adobe Target te beschrijven en te controleren.
title: Hoe vorm ik de montages van de Activiteit van Aanbevelingen?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: b7c7e8d85f7f39024ed5e57177e5c9f628460e9c
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Instellingen voor activiteiten met aanbevelingen

Informatie over de instellingen die u kunt gebruiken om een [!UICONTROL Recommendations] -activiteit in [!DNL Adobe Target] te beschrijven en te beheren.

In de volgende secties worden de beschikbare instellingen voor een [!UICONTROL Recommendations] -activiteit beschreven.

## Naam

Klik het Meer pictogram van Acties ( ![&#x200B; Meer pictogram van Acties &#x200B;](/help/main/assets/icons/MoreSmallListVert.svg)), dan klik **[!UICONTROL Rename]** om een beschrijvende naam te verstrekken die u en uw team zal helpen de activiteit identificeren.

De volgende tekens zijn niet toegestaan in een naam van een activiteit:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

Als u een [!UICONTROL Recommendations] naam van een activiteit opgeeft die al bestaat voor een andere activiteit in [!UICONTROL Recommendations Classic] , wordt de nieuwe activiteit opnieuw gesynchroniseerd met een nieuwe naam. De nieuwe naam is de oorspronkelijke naam die met een tijdstempel is toegevoegd om deze uniek te maken. Deze nieuwe naam wordt zowel in [!DNL Target Standard/Premium] als in [!UICONTROL Recommendations Classic] weergegeven.

## Doelstelling

(Optioneel) Beschrijf het doel van de activiteit.

## Prioriteit

Pas de schuifregelaar aan om het prioriteitsniveau te bepalen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.

## Duur

Stel de duur van de activiteit in.

De activiteit kan beginnen wanneer geactiveerd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdplukker gebruikt een klok van 24 uur, met 00 :00 die middernacht zijn. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## Rapportinstellingen

* **Meldend Source:** specificeer welke oplossingsgegevens worden verzameld van:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Als een rapporteringsoplossing in uw [&#x200B; rekeningsmontages &#x200B;](/help/main/administrating-target/reporting.md) wordt gespecificeerd, wordt de gespecificeerde oplossing gebruikt en dit het plaatsen is niet zichtbaar.

  U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

  **[!DNL Adobe Analytics]**: Zie [[!DNL Adobe Analytics]  als rapporteringsbron voor  [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) om over de verschillen tussen de het melden oplossingen en de voordelen van elk te leren.

  Wanneer u [!DNL Analytics] selecteert als de rapportbron voor [!DNL Target] (A4T), selecteert u een [!DNL Analytics] -rapportsuite die [!DNL Target] activiteitsgegevens ontvangt. Hiervoor kiest u eerst een van de [!DNL Analytics] -bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportreeks nog van de lijst mist, contacteer [&#x200B; de Zorg van de Klant &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Er wordt een standaard traceringsserver weergegeven in het veld [!UICONTROL Tracking Server] . Als u meer dan één volgende server gebruikt, zorg ervoor u de correcte het volgen server in dit gebied omvat. Zie [&#x200B; Gebruikend een Analytics die Server &#x200B;](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) volgen voor meer informatie.

  **[!DNL Adobe Customer Journey Analytics]**: Zie [[!DNL Target]  rapporterend in  [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) voor meer informatie over de integratie tussen [!DNL Adobe Customer Journey Analytics] en [!DNL Target].

* **Metrisch van het Goal:** selecteer metrisch succes dat bepaalt of de activiteit succesvol is.
* **Extra Metriek:** vorm extra succesmetriek die in uw rapporten moeten worden gebruikt.
* **Soorten publiek voor het Melden:** bepaal publiek dat kan worden gebruikt wanneer het filtreren van uw rapporten.

## Andere metagegevens

Voer opmerkingen in over je activiteiten.

## De video van de opleiding: De Montages van de activiteit (3 :02) ![&#x200B; badge van het Leerprogramma &#x200B;](/help/main/assets/tutorial.png)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
