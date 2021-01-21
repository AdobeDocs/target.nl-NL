---
keywords: analytics tracking server;A4T;analytics segments;report suites;incorrect data;orphaned;sdid;VisitorAPI.js;mboxMCSDID;phantom;unspecified
description: Dit onderwerp behandelt sommige gemeenschappelijke kwesties die zijn ontmoet wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).
title: Los de Analytics en integratie van het Doel (A4T) problemen op
feature: a4t troubleshooting
translation-type: tm+mt
source-git-commit: d6ee46899813049c1fad7a358f800702730b3c2d
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---


# Los de Analytics en integratie van het Doel (A4T){#troubleshoot-the-analytics-and-target-integration-a-t} problemen op

Dit onderwerp behandelt sommige gemeenschappelijke kwesties die zijn ontmoet wanneer het gebruiken van Analytics als rapporteringsbron voor Doel (A4T).

## Activiteiten tonen geen gegevens in Analytics, maar worden in plaats daarvan vermeld als &quot;unspecified&quot;. {#unspecified}

Er zijn verschillende redenen waarom dit zou kunnen gebeuren:

* Classificatie in [!DNL Target] is niet volledig verwerkt.

   De classificatie duurt over het algemeen tussen 24 en 72 uur om rapporten na eerste sparen te classificeren.

* De rapportsuite bevat geen gegevens, maar [!DNL Target] heeft geprobeerd hits te classificeren. [!DNL Target] kan geen gegevens classificeren tot de eerste treffer voorkomt.

   Zorg ervoor dat de rapportsuite ten minste één hit heeft gehad.

* De classificatieaanroep van [!DNL Target] naar [!DNL Analytics] is mislukt.

   [Neem contact op met de ](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) klantenservice voor hulp.

>[!NOTE]
>
>Soms worden gegevens correct weergegeven in rapporten, maar er wordt teruggegaan naar &quot;niet opgegeven&quot; omdat er een nieuwe activiteit is toegevoegd die de classificatie niet heeft voltooid. Houd er rekening mee dat het meestal 24 tot 72 uur duurt voordat rapporten worden geclassificeerd na de eerste keer opslaan.
>
>Er gaan geen gegevens verloren wanneer deze als &quot;niet opgegeven&quot; worden vermeld. De gegevens worden correct toegewezen aan de juiste activiteit of ervaring na de classificatieuitvoering.

## A4T Activiteitenrapporten bevatten een rij met een groot aantal &quot;ongespecificeerde&quot; gebeurtenissen. {#added_unspecified_events}

Er wordt altijd een rij met niet-opgegeven gebeurtenissen weergegeven, afhankelijk van de maateenheid die u gebruikt om de gegevens weer te geven.\
Als u een metrische waarde gebruikt die alleen bestemd is, wordt die rij die &quot;niet is opgegeven&quot; niet weergegeven.
Als u gemeenschappelijkere metrisch gebruikt, zal die rij opnieuw in het rapport verschijnen.

Dit &quot;niet-gespecificeerde&quot;lijnpunt zal geen doel-geassocieerde informatie (b.v. geen bezoekers/bezoeken/impressies) hebben.\
De enige manier om dit in het verslag te vermijden, is om Target in te stellen op absoluut elk verzoek dat van die pagina wordt verzonden, wat geen zin heeft.

## Mijn Analytische gegevens laten een opgeblazen bezoek of bezoekeraantal zien sinds het begin van A4T. {#section_4BE374E573D44FB7918611699B74F58E}

Zie [Inflated Visit and Visitor Counts in A4T](/help/c-integrating-target-with-mac/a4t/c-a4t-troubleshooting/minimizing-inflated-visit-and-visitor-counts-a4t.md#concept_A515C2DE126E44B6AD97754C2C6D5235) minimaliseren voor meer informatie.

## De geschatte lift in de metrische omzet geeft geen correcte gegevens aan. {#section_35D766E5E4D347C39E15D08AA883FBB0}

De details voor optillen en vertrouwen zijn niet beschikbaar in Analytics. Zij zijn echter beschikbaar in de Target-rapporten.

## Activiteiten worden niet weergegeven in analyserapporten. {#section_F7001EB4670F4B3497CC7DA60BBDA6D5}

A4T-activiteiten vereisen dat een analytische traceringsserver wordt opgegeven. Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) gebruiken om ervoor te zorgen dat de Analytics Tracking Server op de juiste wijze is ingesteld.

>[!NOTE]
>
>Als u Adobe Analytics gebruikt als rapportagebron van uw activiteit, hoeft u tijdens het maken van activiteiten geen trackingserver op te geven als u mbox.js versie 61 (of hoger) of versie 0.9.1 (of hoger) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings].

## Mijn segmenten Analytics verschijnen niet in Doel. {#section_DEE87F1557834F448E99381D3D02EEEF}

Zorg ervoor u de juiste toestemmingen hebt alvorens u begint te creëren A4T activiteiten:

* U moet tot de groep van de Toegang van de Diensten van het Web in Adobe Analytics behoren om Analytics als rapporteringsbron voor Doel te kunnen gebruiken.
* U moet lid zijn van een of meer Experience Cloud-groepen die toegang hebben tot Analytics en Target.
* Controleer of Analytics en Target worden weergegeven in de sectie Marketing Apps van de linkernavigatie.

## Stuittarieven, stuitingen en afsluitingsmetriek worden in rapporten als positief weergegeven. {#section_B5C3D56EF0344407AE67ABEB93037F5A}

Dit is een bekend probleem.

Hoewel deze metriek negatief zijn, wordt de lift getoond alsof zij in de rapporten van het Doel positief waren. Hoewel u bijvoorbeeld een lagere stuitsnelheid wilt, wordt de hogere stuitsnelheid weergegeven als de winnaar met de hoogste lift. Houd rekening met deze en vergelijkbare cijfers en geef aan of u het aantal wilt verlagen of verhogen wanneer u beslissingen neemt op basis van uw rapporten.

## De rapportsuite die ik nodig heb, wordt niet weergegeven. {#section_BD8F956E41D6475B98B7BF0C74CC387C}

De lijst van rapportsuites die in [!DNL Target Standard/Premium] verschijnt is de lijst van rapportsuites die voor [!DNL Analytics] als rapporteringsbron voor [!DNL Target] (A4T) zijn gevormd. Dit betekent dat u niet elke rapportsuite ziet die u hebt.

Bovendien, als u veelvoudige rapporteringsbronnen gebruikt, moeten de rapportreeksen in de standaard rapporteringsbron aanwezig zijn die in [!DNL Target] eveneens wordt geplaatst; anders worden de rapporten niet weergegeven .

Als u nog steeds niet de rapportreeks ziet u zoekt, contacteer [Clientzorg](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) om het toegelaten te krijgen.

## Ik zie niet zoveel gegevens in rapporten als verwacht. {#section_75002584FA63456D8D9086172925DD8D}

Herzie uw implementatie, vooral op pagina&#39;s waar uw bezoekers voor ervaringen kwalificeren en zorg ervoor dat de extra gegevens IDs in [!DNL Target] en [!DNL Analytics] vraag aanpast.

* **at.js 1.x**: In de  [!DNL Target] vraag, is supplementaire identiteitskaart bevat in de  `mboxMCSDID` parameter. In [!DNL Analytics] vraag, is supplementaire identiteitskaart bevat in de `sdid` parameter.
* **at.js 2.x**: In de  [!DNL Target] vraag, is supplementaire identiteitskaart teruggekeerd in de kopbal van HTTP als waarde voor  `experienceCloud.analytics.supplementalDataId`. In [!DNL Analytics] vraag, is supplementaire identiteitskaart bevat in de `sdid` parameter.

De eenvoudigste manier om de aanvullende id te controleren is met de Adobe Experience Platform Debugger.

Als u debugger niet hebt geïnstalleerd, zie [Inleiding aan de Debugger van Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

![Foutopsporing](/help/c-integrating-target-with-mac/a4t/assets/debugger.png)

Als de [!DNL Target]-aanroep geen aanvullende gegevens-id bevat, controleert u of het [!DNL VisitorAPI.js]-bestand is geladen vóór [!DNL at.js] of [!DNL mbox.js]. Als er geen extra gegevens identiteitskaart in [!DNL Analytics] vraag is, bevestig dat [!DNL Target] vraag vóór [!DNL Analytics] vraag brandt.

Zie [Analytics for Target Implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md#concept_CE78750AC2A4487D8ACD9369B3EAC85A) of neem contact op met [Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor meer informatie.
