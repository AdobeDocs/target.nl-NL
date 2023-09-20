---
keywords: Doel;analyse;traceringsserver;analyse voor doel;a4t
description: Leer hoe u een activiteit configureert in [!DNL Adobe Target] te gebruiken [!DNL Adobe Analytics] als bron van rapportage (A4T).
title: Hoe kan ik [!DNL Analytics] Gegevens in [!DNL Target]?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Gebruiken [!DNL Adobe Analytics] data

U kunt een activiteit vormen binnen [!DNL Adobe Target] te gebruiken [!DNL Adobe Analytics] als bron van rapportage (A4T).

Voor gedetailleerde informatie over het instellen van [!DNL Analytics] als gegevensbron voor [!DNL Target], zie [Adobe Analytics als rapportagebron voor Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Voordat u een activiteit instelt die [!DNL Analytics] als bron van rapportage, het doel voor de activiteit bepalen, zoals het verbeteren van opbrengst per bezoeker (RPV) of het verhogen van klikt uw het winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u op elk gewenst moment aanvullende metriek kunt selecteren [!DNL Analytics], moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

>[!NOTE]
>
>De [!DNL Adobe Analytics] is beschikbaar als u een koppeling hebt gemaakt naar [!DNL Adobe Experience Cloud] account met beide [!DNL Analytics] en [!DNL Target], zelfs als integratie tussen [!DNL Target] en [!DNL Analytics] is niet ingesteld voor uw account.

Als u [!DNL Analytics] als bron van rapportage voor [!DNL Target]selecteert u een [!DNL Analytics] te ontvangen rapportsuite [!DNL Target] activiteitsgegevens. Als u een rapportbron wilt opgeven, kiest u eerst een van de volgende opties: [!DNL Analytics] bedrijven waaraan uw account is gekoppeld, en selecteer vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Adobe Target] zijn beschikbaar voor selectie. Als u de rapportsuite die u verwacht niet ziet, meldt u zich eerst af en meldt u zich weer aan bij de [!DNL Adobe Experience Cloud] om het opnieuw te proberen. Als de rapportsuite nog steeds ontbreekt in de lijst, neemt u contact op met de klantenservice.

[!UICONTROL Analytics for Target] (A4T) vereist een volgende server om resultaten correct te melden. Een standaard volgende server wordt weergegeven in het dialoogvenster [!UICONTROL Tracking Server] veld. Als u meer dan één volgende server gebruikt, zorg ervoor dat u de correcte het volgen server in dit gebied omvat. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) voor meer informatie .

>[!NOTE]
>
>Als u [!DNL Adobe Analytics] als rapportbron van uw activiteit, te hoeven u niet om een het volgen server tijdens activiteitenverwezenlijking te specificeren als u at.js versie 0.9.1 (of later) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het creëren van activiteit, kunt u verlaten [!UICONTROL Tracking Server] veld leeg op [!UICONTROL Goals & Settings] pagina.

Als u activiteiten instelt na het instellen [!DNL Analytics] als uw rapporteringsbron, is er geen optie aan opstellingspubliek voor rapportering. [!DNL Analytics] de segmenten zijn beschikbaar in [!DNL Target] [!UICONTROL Activities] verslag.

U moet een succes metrisch selecteren als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt kiezen uit [!DNL Analytics] de metrische waarde beschikbaar in [!DNL Analytics] metrische kiezer.

Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de test wilt verbeteren.

Nadat een bezoeker uw doel heeft voltooid, wordt die bezoeker niet meer opgenomen in de activiteit. Als de bezoeker na het voltooien van een activiteit weer aan de slag gaat, wordt die bezoeker geteld als een nieuwe bezoeker.
