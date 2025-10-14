---
keywords: Doel;analyse;traceringsserver;analyse voor doel;a4t
description: Leer hoe te om een activiteit in  [!DNL Adobe Target]  te vormen om  [!DNL Adobe Analytics]  als rapporteringsbron (A4T) te gebruiken.
title: Hoe kan ik  [!DNL Analytics]  Gegevens in  [!DNL Target] gebruiken?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe Analytics] -gegevens gebruiken

U kunt een activiteit in [!DNL Adobe Target] vormen om [!DNL Adobe Analytics] als rapporteringsbron (A4T) te gebruiken.

Voor gedetailleerde informatie over vestiging [!DNL Analytics] als gegevensbron voor [!DNL Target], zie [&#x200B; Adobe Analytics als Rapporterende Source voor Adobe Target &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Voordat u een activiteit instelt die [!DNL Analytics] als bron voor rapportage gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de omzet per bezoeker (RPV) of het verhogen van de klikt op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u op elk moment in [!DNL Analytics] aanvullende metriek kunt selecteren, moet u toch een bepaalde metrische waarde opgeven die deze test waarschijnlijk beïnvloedt.

>[!NOTE]
>
>De optie [!DNL Adobe Analytics] is beschikbaar als u uw [!DNL Adobe Experience Cloud] -account hebt gekoppeld aan zowel [!DNL Analytics] als [!DNL Target] , zelfs als de integratie tussen [!DNL Target] en [!DNL Analytics] niet is ingesteld voor uw account.

Wanneer u [!DNL Analytics] selecteert als de rapportbron voor [!DNL Target] , selecteert u een [!DNL Analytics] -rapportsuite die [!DNL Target] activiteitsgegevens ontvangt. Als u wel een rapportbron wilt opgeven, kiest u eerst een van de [!DNL Analytics] -bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Adobe Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met de klantenservice.

[!UICONTROL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Er wordt een standaard traceringsserver weergegeven in het veld [!UICONTROL Tracking Server] . Als u meer dan één volgende server gebruikt, zorg ervoor dat u de correcte het volgen server in dit gebied omvat. Zie [&#x200B; Gebruikend een Analytics die Server &#x200B;](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) volgen voor meer informatie.

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron van uw activiteit gebruikt, te hoeven u niet om een het volgen server tijdens activiteitenverwezenlijking te specificeren als u versie 0.js 0.9.1 (of later) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings] .

Wanneer u activiteiten instelt nadat u [!DNL Analytics] hebt ingesteld als rapportbron, is er geen optie voor het instellen van soorten publiek voor rapportage. [!DNL Analytics] -segmenten zijn beschikbaar in het [!DNL Target] [!UICONTROL Activities] -rapport.

U moet een succes metrisch selecteren als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare [!DNL Analytics] metrische waarde in de [!DNL Analytics] -metrische kiezer kiezen.

Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de test wilt verbeteren.

Nadat een bezoeker uw doel heeft voltooid, wordt die bezoeker niet meer opgenomen in de activiteit. Als de bezoeker na het voltooien van een activiteit weer aan de slag gaat, wordt die bezoeker geteld als een nieuwe bezoeker.
