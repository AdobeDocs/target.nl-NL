---
keywords: Doel;analyse;traceringsserver;analyse voor doel;a4t
description: Leer hoe te om een activiteit in Adobe te vormen [!DNL Target] om Adobe Analytics als rapportagebron te gebruiken. Deze integratie wordt Analytics genoemd voor [!DNL Target] (A4T).
title: Hoe kan ik de analysegegevens als doel gebruiken?
feature: Analytics for Target (A4T)
exl-id: 85605ff9-c09a-4a1a-9784-bdacda377e1d
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Analysegegevens gebruiken

U kunt een activiteit vormen binnen [!DNL Adobe Target] te gebruiken [!DNL Adobe Analytics] als bron van rapportage (A4T).

Voor gedetailleerde informatie over vestiging Analytics als gegevensbron voor Doel, zie [Adobe Analytics als rapportagebron voor Adobe Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Voordat u een activiteit instelt die Analytics als bron voor rapportage gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de campagne. Hoewel u op elk gewenst moment aanvullende metriek kunt selecteren in Analytics, moet u toch een bepaalde metrische waarde opgeven die deze test waarschijnlijk beïnvloedt.

>[!NOTE]
>
>De optie Adobe Analytics is beschikbaar als u uw Adobe Experience Cloud-account aan zowel Analytics als Target hebt gekoppeld, zelfs als er voor uw account geen integratie tussen Target en Analytics is ingesteld.

Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt. Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target, zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst.

Analytics for Target vereist een trackingserver om de resultaten correct te rapporteren. In het veld Trackingserver wordt een standaard traceringsserver weergegeven. Als u meerdere trackingservers gebruikt, moet u controleren of u de juiste trackingserver in dit veld opneemt. Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) voor meer informatie .

>[!NOTE]
>
>Als u Adobe Analytics gebruikt als rapportagebron van uw activiteit, hoeft u tijdens het maken van activiteiten geen trackingserver op te geven als u versie 0.js 0.9.1 (of hoger) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het creëren van activiteit, kunt u verlaten [!UICONTROL Tracking Server] veld leeg op [!UICONTROL Goals & Settings] pagina.

Wanneer u activiteiten instelt nadat u Analytics hebt ingesteld als uw rapporteringsbron, is er geen optie voor het instellen van soorten publiek voor rapportage. De segmenten van Analytics zijn beschikbaar in het rapport van de Activiteiten van het Doel.

U wordt vereist om een succes metrisch aan gebruik als doel voor elke test te selecteren. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle campagne signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare metrische waarde voor Analytics kiezen in de metrische kiezer voor Analytics.

Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de test wilt verbeteren.

Nadat een bezoeker uw doel heeft voltooid, wordt die bezoeker niet meer opgenomen in de campagne. Als de bezoeker uw campagne weer betreedt nadat hij of zij een activiteit heeft voltooid, wordt hij of zij geteld als nieuwe bezoeker.
