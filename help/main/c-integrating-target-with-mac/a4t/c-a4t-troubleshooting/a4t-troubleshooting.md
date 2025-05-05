---
keywords: analytische traceringsserver;A4T;analytische segmenten;rapportsuites;onjuiste gegevens;zwevend;sdid;VisitorAPI.js;mboxMCSDID;phantom;niet opgegeven
description: Ontdek de algemene problemen die klanten hebben ondervonden bij het gebruik van Analytics voor [!DNL Target] (A4T).
title: Hoe los ik Analytics en [!DNL Target] Integratie (A4T)
feature: Analytics for Target (A4T)
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Los Analytics en [!DNL Target] integratie (A4T)

In dit onderwerp worden enkele veelvoorkomende problemen besproken die zijn opgetreden bij het gebruik van [!DNL Adobe Analytics] als bron van rapportage voor [!DNL Adobe Target] (A4T).

## Activiteiten tonen geen gegevens in Analytics, maar worden in plaats daarvan vermeld als &quot;unspecified&quot;. {#unspecified}

Er zijn verschillende redenen waarom gegevens &#39;unspecified&#39; kunnen voorkomen:

* Indeling in [!DNL Target] niet volledig verwerkt.

   De classificatie duurt over het algemeen van 24 tot 72 uur om rapporten na eerste sparen te classificeren.

* De rapportsuite bevat geen gegevens, maar [!DNL Target] heeft geprobeerd hits te classificeren. [!DNL Target] kan geen gegevens classificeren tot de eerste treffer voorkomt.

   Zorg ervoor dat de rapportsuite ten minste één hit heeft gehad.

* De classificatieoproep van [!DNL Target] tot [!DNL Analytics] mislukt.

   [Contact opnemen met de klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor hulp.

Als u de rij &quot;unspecified&quot; onderverdeelt door de dimensie &quot;Analytics for Target&quot; en deze geen activiteit-id bevat, betekent dit dat alles correct is geclassificeerd. Als daar activiteit-id&#39;s worden vermeld, dient deze als indicatie voor een classificatieprobleem.

>[!NOTE]
>
>Soms worden gegevens correct weergegeven in rapporten, maar worden ze weer &quot;niet opgegeven&quot; omdat er een nieuwe activiteit is toegevoegd die de classificatie niet heeft voltooid. Vergeet niet dat het meestal 24 tot 72 uur duurt om rapporten te classificeren na de eerste keer opslaan.
>
>Er gaan geen gegevens verloren wanneer deze als &quot;niet opgegeven&quot; worden vermeld. De gegevens worden correct toegewezen aan de juiste activiteit of ervaring na de classificatieuitvoering.

## A4T Activiteitenrapporten bevatten een rij met veel &quot;niet-opgegeven&quot; gebeurtenissen. {#added_unspecified_events}

Er kan een &quot;[!UICONTROL Unspecified]&quot; de gebeurtenisrij die in uw rapport wordt getoond, afhankelijk van metrisch u gebruikt om uw gegevens met te tonen.

Typisch, toont deze rij als u gemeenschappelijke metrisch in het rapport kiest dat niet is [!DNL Target]-specific (bijvoorbeeld [!UICONTROL Page Views], [!UICONTROL Visits], [!UICONTROL Unique Visitors], enzovoort). In dit geval worden de [!UICONTROL "Unspecified"] de rij omvat alle [!UICONTROL Page Views], [!UICONTROL Visits], en [!UICONTROL Unique Visitors] die geen verband houden met [!DNL Target] activiteiten.

Die rij heeft geen [!DNL Target]-gerelateerde informatie (bijvoorbeeld geen bezoekers, bezoeken of indrukken). Zie voor meer informatie [&quot;Niet opgegeven,&quot; &quot;Geen,&quot; &quot;Overige&quot; en &quot;Onbekend&quot; in de rapportage](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=nl-NL) in de *Technische notities voor Analytics*.

Als u een [!DNL Target]- specifieke metrisch in het rapport, dat [!UICONTROL "Unspecified"] rij wordt niet weergegeven. De enige manier om dit in het verslag te vermijden is een [!DNL Target] roep op elk verzoek dat van die pagina wordt verzonden, wat niet gemeenschappelijk of noodzakelijk is.

## De geschatte lift in de metrische omzet geeft geen correcte gegevens aan. {#section_35D766E5E4D347C39E15D08AA883FBB0}

De details voor optillen en vertrouwen zijn niet beschikbaar in Analytics. Zij zijn echter beschikbaar in de Target-rapporten.

## Activiteiten worden niet weergegeven in analyserapporten. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T-activiteiten vereisen dat een analytische traceringsserver wordt opgegeven. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) om ervoor te zorgen dat de Analytics Tracking Server correct is ingesteld.

>[!NOTE]
>
>U hoeft tijdens het maken van activiteiten geen trackingserver op te geven als u at.js versie 0.9.1 (of hoger) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het creëren van activiteit, kunt u verlaten [!UICONTROL Tracking Server] veld leeg op [!UICONTROL Goals & Settings] pagina.

## Mijn segmenten Analytics verschijnen niet in Doel. {#section_DEE87F1557834F448E99381D3D02EEEF}

Zorg ervoor u de juiste toestemmingen hebt alvorens u begint te creëren A4T activiteiten:

* Behoort tot de groep van de Toegang van de Diensten van het Web in Adobe Analytics om Analytics als rapporteringsbron voor Doel te kunnen gebruiken
* Lid zijn van één of meerdere groepen van Experience Cloud die toegang tot Analytics en Doel hebben.
* Controleer of Analytics en Target worden weergegeven in de sectie Marketing Apps van de linkernavigatie.

## Stuittarieven, stuitingen en afsluitingsmetriek worden in rapporten als positief weergegeven. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Deze cijfers die als positieve elementen in rapporten verschijnen zijn een bekende kwestie.

Hoewel deze metriek negatief zijn, wordt de lift getoond alsof zij in de rapporten van het Doel positief waren. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

## De rapportsuite die ik nodig heb, wordt niet weergegeven. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

De lijst met rapportsuites die wordt weergegeven in [!DNL Target Standard/Premium] is de lijst van rapportsuites die voor zijn gevormd [!DNL Analytics] als bron van rapportage voor [!DNL Target] (A4T). Mogelijk ziet u niet elk rapportenpakket dat u hebt.

Als u veelvoudige rapporteringsbronnen gebruikt, moeten de rapportreeksen in de standaard rapporteringsbron aanwezig zijn die in [!DNL Target] ook. Als de rapportsuites niet in de standaard rapporteringsbron zijn, tonen de rapportseries niet.

Als u nog steeds de rapportsuite waarnaar u zoekt niet ziet, neemt u contact op met [Clientservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om deze in te schakelen.

## Ik zie niet zoveel gegevens in rapporten als verwacht. {#section_75002584FA63456D8D9086172925DD8D}

Controleer uw implementatie, vooral op pagina&#39;s waar uw bezoekers voor ervaringen in aanmerking komen en zorg ervoor dat de aanvullende gegevens-id&#39;s overeenkomen met de id&#39;s in het dialoogvenster [!DNL Target] en [!DNL Analytics] oproepen.

* **at.js 1.x**: In de [!DNL Target] vraag, is supplementaire identiteitskaart bevat in `mboxMCSDID` parameter. In de [!DNL Analytics] vraag, is supplementaire identiteitskaart bevat in `sdid` parameter.
* **at.js 2.x**: In de [!DNL Target] aanroep, is de supplementaire identiteitskaart teruggekeerd in de kopbal van HTTP als waarde voor `experienceCloud.analytics.supplementalDataId`. In de [!DNL Analytics] vraag, is supplementaire identiteitskaart bevat in `sdid` parameter.

De eenvoudigste manier om de aanvullende id te controleren is met de Adobe Experience Platform Debugger.

Als u debugger niet hebt geïnstalleerd, zie [Inleiding tot de Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html?lang=nl-NL).

![Foutopsporing](/help/main/c-integrating-target-with-mac/a4t/assets/debugger.png)

Als er geen aanvullende gegevens-id voorkomt in het dialoogvenster [!DNL Target] de [!DNL VisitorAPI.js] bestand is geladen voordat [!DNL at.js]. Als er geen aanvullende gegevens-id voorkomt in het dialoogvenster [!DNL Analytics] de [!DNL Target] oproepen branden vóór [!DNL Analytics] vraag.

Zie voor meer informatie [Analyses voor doelimplementatie](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) of contact opnemen [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
