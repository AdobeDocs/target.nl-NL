---
keywords: Recommendations;Instellingen;naam;doel;prioriteit;duur;rapportage-instellingen;andere metagegevens
description: Leer hoe u de instellingen configureert die worden gebruikt om een Recommendations-activiteit in Adobe Target te beschrijven en te besturen.
title: Hoe configureer ik Recommendations Activity Settings?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: 77bb14fc-342d-41cd-8084-e21067f277af
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Instellingen Recommendations-activiteit

Informatie over de instellingen die u kunt gebruiken om een [!UICONTROL Recommendations] activiteit in [!DNL Adobe Target].

![Recommendations-pagina Doelen en instellingen](/help/main/c-recommendations/t-create-recs-activity/assets/recs-settings.png)

In de volgende secties worden de beschikbare instellingen voor een [!UICONTROL Recommendations] activiteit.

## Naam

Geef een beschrijvende naam op die u en uw team helpt de activiteit te identificeren.

De volgende tekens zijn niet toegestaan in een naam van een activiteit:

`/`
`?`
`#`
`:`
`=`
`+`
`-`
`@`

Als u een [!UICONTROL Recommendations] naam van activiteit die al bestaat voor een andere activiteit in [!UICONTROL Recommendations Classic], wordt de nieuwe activiteit opnieuw gesynchroniseerd met een nieuwe naam. De nieuwe naam is de oorspronkelijke naam die met een tijdstempel is toegevoegd om deze uniek te maken. Deze nieuwe naam wordt in beide weergegeven [!DNL Target Standard/Premium] en [!UICONTROL Recommendations Classic].

## Doelstelling

(Optioneel) Beschrijf het doel van de activiteit.

## Prioriteit

Pas de schuifregelaar aan om het prioriteitsniveau te bepalen.

De prioriteit wordt gebruikt als de veelvoudige activiteiten aan de zelfde plaats met het zelfde publiek worden toegewezen. Als twee of meer activiteiten aan de plaats worden toegewezen, de activiteit met de hoogste prioritaire vertoningen.

## Duur

Stel de duur van de activiteit in.

De activiteit kan beginnen wanneer geactiveerd, of u kunt een specifieke datum en een tijd plaatsen. Op dezelfde manier kan de activiteit eindigen wanneer deze wordt gedeactiveerd of kunt u een datum en tijd instellen. De tijdkiezer gebruikt een 24-uurs klok, waarbij 00:00 middernacht is. De tijdzone wordt geplaatst aan de tijdzone die in uw browser wordt gevormd. Als u een andere tijdzone wilt gebruiken, stelt u de browser in op een andere tijdzone en start u de browser opnieuw.

## Rapportinstellingen

* **Bron rapporteren:** Geef op welke oplossingsgegevens worden verzameld:

   * [!DNL Adobe Target]
   * [!DNL Adobe Analytics]
   * [!DNL Adobe Customer Journey Analytics]

  Als een rapporteringsoplossing in uw wordt gespecificeerd [accountinstellingen](/help/main/administrating-target/reporting.md), wordt de opgegeven oplossing gebruikt en is deze instelling niet zichtbaar.

  U kunt de rapportbron niet wijzigen nadat de activiteit live gaat om rapporten consistent te houden.

  **[!DNL Adobe Analytics]**: Zie [[!DNL Adobe Analytics] als bron van rapportage voor [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) kennis te nemen van de verschillen tussen de rapporteringsoplossingen en de voordelen van beide.

  Als u [!DNL Analytics] als bron van rapportage voor [!DNL Target] (A4T) selecteert u een [!DNL Analytics] te ontvangen rapportsuite [!DNL Target] activiteitsgegevens. Kies eerst een van de opties [!DNL Analytics] bedrijven waaraan uw account is gekoppeld, en selecteer vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich weer aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

  [!DNL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Een standaard volgende server wordt weergegeven in het dialoogvenster [!UICONTROL Tracking Server] veld. Als u meer dan één volgende server gebruikt, zorg ervoor u de correcte het volgen server in dit gebied omvat. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) voor meer informatie .

  **[!DNL Adobe Customer Journey Analytics]**: Zie [[!DNL Target] rapporteren in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) voor meer informatie over de integratie tussen [!DNL Adobe Customer Journey Analytics] en [!DNL Target].

* **Metrisch doel:** Selecteer de succesmaatstaf die bepaalt of de activiteit succesvol is.
* **Extra cijfers:** Vorm extra succesmetriek die in uw rapporten moet worden gebruikt.
* **Soorten publiek voor rapportage:** Bepaal publiek dat kan worden gebruikt wanneer het filtreren van uw rapporten.

## Andere metagegevens

Voer opmerkingen in over je activiteiten.

## Trainingsvideo: Instellingen voor activiteit (3:02) ![Zelfstudie-badge](/help/main/assets/tutorial.png)

Deze video bevat informatie over instellingen voor activiteit.

* Voer een doel in voor uw activiteit
* Het prioriteitsniveau van uw activiteiten instellen
* Begin- en eindtijd van activiteit plannen
* Voeg publiek voor rapportering toe om rapportfilters tot stand te brengen
* Notities invoeren voor uw activiteiten

>[!VIDEO](https://video.tv.adobe.com/v/17381)
