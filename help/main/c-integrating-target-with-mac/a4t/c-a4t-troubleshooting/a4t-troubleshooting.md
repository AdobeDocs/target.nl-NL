---
keywords: analytische traceringsserver;A4T;analytische segmenten;rapportsuites;onjuiste gegevens;zwevend;sdid;VisitorAPI.js;mboxMCSDID;phantom;niet opgegeven
description: Onderzoek gemeenschappelijke kwesties klanten hebben ontmoet wanneer het gebruiken van Analytics voor  [!DNL Target]  (A4T).
title: Hoe los ik Analytics en  [!DNL Target]  Integratie (A4T) problemen op
feature: Analytics for Target (A4T)
exl-id: 7d155cbe-e799-43b5-afc2-1aea43f432ba
source-git-commit: 0be54d82e25eb919102f6098c1b1db76ab291675
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# Problemen met de analyse en [!DNL Target] integratie oplossen (A4T)

Dit onderwerp behandelt enkele algemene problemen die zijn opgetreden bij het gebruik van [!DNL Adobe Analytics] als rapportagebron voor [!DNL Adobe Target] (A4T).

## Activiteiten tonen geen gegevens in Analytics, maar worden in plaats daarvan vermeld als &quot;unspecified&quot;. {#unspecified}

Er zijn verschillende redenen waarom gegevens &#39;unspecified&#39; kunnen voorkomen:

* Classificatie in [!DNL Target] is niet volledig verwerkt.

  De classificatie duurt over het algemeen van 24 tot 72 uur om rapporten na eerste sparen te classificeren.

* De rapportsuite bevat geen gegevens, maar [!DNL Target] heeft geprobeerd hits te classificeren. [!DNL Target] kan geen gegevens classificeren tot de eerste hit optreedt.

  Zorg ervoor dat de rapportsuite ten minste één hit heeft gehad.

* De classificatieaanroep van [!DNL Target] naar [!DNL Analytics] is mislukt.

  [&#x200B; de Zorg van de Klant van het Contact &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor hulp.

Als u de rij &quot;unspecified&quot; onderverdeelt door de dimensie &quot;Analytics for Target&quot; en deze geen activiteit-id bevat, betekent dit dat alles correct is geclassificeerd. Als daar activiteit-id&#39;s worden vermeld, dient deze als indicatie voor een classificatieprobleem.

>[!NOTE]
>
>Soms worden gegevens correct weergegeven in rapporten, maar worden ze weer &quot;niet opgegeven&quot; omdat er een nieuwe activiteit is toegevoegd die de classificatie niet heeft voltooid. Vergeet niet dat het meestal 24 tot 72 uur duurt om rapporten te classificeren na de eerste keer opslaan.
>
>Er gaan geen gegevens verloren wanneer deze als &quot;niet opgegeven&quot; worden vermeld. De gegevens worden correct toegewezen aan de juiste activiteit of ervaring na de classificatieuitvoering.

## A4T Activiteitenrapporten bevatten een rij met veel &quot;niet-opgegeven&quot; gebeurtenissen. {#added_unspecified_events}

Er zou een &quot;[!UICONTROL Unspecified]&quot;gebeurtenisrij kunnen zijn in uw rapport wordt getoond, afhankelijk van metrisch u gebruikt om uw gegevens met te tonen.

Doorgaans wordt deze rij weergegeven als u een algemene metrische waarde kiest in het rapport die niet [!DNL Target] specifiek is (bijvoorbeeld [!UICONTROL Page Views] , [!UICONTROL Visits] , [!UICONTROL Unique Visitors] enzovoort). In dit geval bevat de [!UICONTROL "Unspecified"] -rij alle [!UICONTROL Page Views] , [!UICONTROL Visits] en [!UICONTROL Unique Visitors] die niet aan [!DNL Target] -activiteiten zijn gekoppeld.

Die rij bevat geen aan [!DNL Target] gekoppelde informatie (bijvoorbeeld geen bezoekers, bezoekers of impressies). Voor meer informatie, zie [&#x200B; &quot;Niet gespecificeerd,&quot;&quot;niets,&quot;&quot;Andere,&quot;en &quot;Onbekend&quot;in het melden van &#x200B;](https://experienceleague.adobe.com/docs/analytics/technotes/unspecified.html?lang=nl-NL) in de *technische nota&#39;s van de Analyse*.

Als u een [!DNL Target] -specifieke metrische waarde kiest in het rapport, wordt die [!UICONTROL "Unspecified"] -rij niet weergegeven. De enige manier om te voorkomen dat dit in het rapport wordt opgenomen, is het instellen van een [!DNL Target] -aanroep op elk verzoek dat van die pagina wordt verzonden, wat niet gebruikelijk of noodzakelijk is.

## De geschatte lift in de metrische omzet geeft geen correcte gegevens aan. {#section_35D766E5E4D347C39E15D08AA883FBB0}

De details voor optillen en vertrouwen zijn niet beschikbaar in Analytics. Deze zijn echter wel beschikbaar in de Target-rapporten.

## Activiteiten worden niet weergegeven in analyserapporten. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T-activiteiten vereisen dat een analytische traceringsserver wordt opgegeven. Zie [&#x200B; Gebruikend een Analytics die Server &#x200B;](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) volgen om ervoor te zorgen dat uw Analytics die Server volgen correct opstelling is.

>[!NOTE]
>
>U hoeft tijdens het maken van activiteiten geen trackingserver op te geven als u at.js versie 0.9.1 (of hoger) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings] .

## Mijn segmenten Analytics verschijnen niet in Doel. {#section_DEE87F1557834F448E99381D3D02EEEF}

Zorg ervoor u de juiste toestemmingen hebt alvorens u begint te creëren A4T activiteiten:

* Behoort tot de groep van de Toegang van de Diensten van het Web in Adobe Analytics om Analytics als rapporteringsbron voor Doel te kunnen gebruiken
* Lid zijn van één of meerdere groepen van Experience Cloud die toegang tot Analytics en Doel hebben.
* Controleer of Analytics en Target worden weergegeven in de sectie Marketing Apps van de linkernavigatie.

## Stuittarieven, stuitingen en afsluitingsmetriek worden in rapporten als positief weergegeven. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Deze cijfers die als positieve elementen in rapporten verschijnen zijn een bekende kwestie.

Hoewel deze metriek negatief zijn, wordt de lift getoond alsof zij in de rapporten van het Doel positief waren. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

## De rapportsuite die ik nodig heb, wordt niet weergegeven. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

De lijst met rapportsuites die in [!DNL Target Standard/Premium] wordt weergegeven, is de lijst met rapportsuites die zijn geconfigureerd voor [!DNL Analytics] als rapportagebron voor [!DNL Target] (A4T). Mogelijk ziet u niet elk rapportenpakket dat u hebt.

Als u meerdere rapporteringsbronnen gebruikt, moeten de rapportsuites ook aanwezig zijn in de standaard rapporteringsbron die is ingesteld in [!DNL Target] . Als de rapportsuites niet in de standaard rapporteringsbron zijn, tonen de rapportseries niet.

Als u nog niet de rapportreeks ziet die u zoekt, contacteer [&#x200B; de Zorg van de Cliënt 0&rbrace; om het toegelaten te krijgen.](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C)

## Ik zie niet zoveel gegevens in rapporten als verwacht. {#section_75002584FA63456D8D9086172925DD8D}

Controleer uw implementatie, vooral op pagina&#39;s waar uw bezoekers voor ervaring in aanmerking komen en zorg ervoor dat de extra gegevens IDs in de [!DNL Target] en [!DNL Analytics] vraag aanpast.

* **at.js 1.x**: In de [!DNL Target] vraag, is supplementaire identiteitskaart bevat in de `mboxMCSDID` parameter. In de aanroep van [!DNL Analytics] bevindt de aanvullende id zich in de parameter `sdid` .
* **at.js 2.x**: In de [!DNL Target] vraag, is supplementaire identiteitskaart teruggekeerd in de kopbal van HTTP als waarde voor `experienceCloud.analytics.supplementalDataId`. In de aanroep van [!DNL Analytics] bevindt de aanvullende id zich in de parameter `sdid` .

De eenvoudigste manier om de aanvullende id te controleren is met de Adobe Experience Platform Debugger.

Als u debugger niet hebt geïnstalleerd, zie [&#x200B; Inleiding aan Adobe Experience Platform Debugger &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html?lang=nl-NL).

![&#x200B; Debugger &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/debugger.png)

Als de aanroep van [!DNL Target] geen aanvullende gegevens-id bevat, controleert u of het bestand [!DNL VisitorAPI.js] is geladen vóór [!DNL at.js] . Als de aanroep van [!DNL Analytics] geen aanvullende gegevens-id bevat, controleert u of de aanroep van [!DNL Target] wordt geactiveerd vóór de aanroep van [!DNL Analytics] .

Voor meer informatie, zie [&#x200B; Analytics voor de Implementatie van het Doel &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) of contacteer [&#x200B; de Zorg van de Klant &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
