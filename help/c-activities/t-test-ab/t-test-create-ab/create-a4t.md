---
keywords: Doel;analyse;traceringsserver;analyse voor doel;a4t
description: Leer hoe u een activiteit in Adobe Target configureert om Adobe Analytics als bron voor rapportage te gebruiken. Deze integratie wordt genoemd Analytics voor Doel (A4T).
title: Hoe kan ik de analysegegevens als doel gebruiken?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Analysegegevens gebruiken

U kunt een activiteit in [!DNL Adobe Target] vormen om [!DNL Adobe Analytics] als rapporteringsbron (A4T) te gebruiken.

Voor gedetailleerde informatie over vestiging Analytics als gegevensbron voor Doel, zie [Adobe Analytics als Rapporterende Bron voor Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

Voordat u een activiteit instelt die Analytics als bron voor rapportage gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de campagne. Hoewel u extra metriek op elk ogenblik in Analytics kunt selecteren, moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

>[!NOTE]
>
>De optie Adobe Analytics is beschikbaar als u uw Adobe Experience Cloud-account aan zowel Analytics als Target hebt gekoppeld, zelfs als er voor uw account geen integratie tussen Target en Analytics is ingesteld.

Wanneer u Analytics selecteert als de rapporteringsbron voor Target, selecteert u een Analytics-rapportsuite die doelactiviteitgegevens ontvangt. Hiervoor kiest u eerst een van de Analytics-bedrijven waaraan uw account is gekoppeld en selecteert u vervolgens de juiste rapportsuite voor de activiteit. Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target, zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de Adobe Experience Cloud om het opnieuw te proberen. Neem contact op met de klantenservice als de rapportsuite nog steeds ontbreekt in de lijst.

Analytics for Target vereist een trackingserver om de resultaten correct te rapporteren. In het veld Trackingserver wordt een standaard traceringsserver weergegeven. Als u meerdere trackingservers gebruikt, moet u controleren of u de juiste trackingserver in dit veld opneemt. Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) gebruiken voor meer informatie.

>[!NOTE]
>
>Als u Adobe Analytics gebruikt als rapportagebron van uw activiteit, hoeft u tijdens het maken van activiteiten geen trackingserver op te geven als u mbox.js versie 61 (of hoger) of versie 0.9.1 (of hoger) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings].

Wanneer u activiteiten instelt nadat u Analytics hebt ingesteld als uw rapporteringsbron, is er geen optie voor het instellen van soorten publiek voor rapportage. De segmenten van Analytics zijn beschikbaar in het rapport van de Activiteiten van het Doel.

U wordt vereist om een succes metrisch aan gebruik als doel voor elke test te selecteren. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle campagne signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare metrische waarde voor Analytics kiezen in de metrische kiezer voor Analytics.

Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de test wilt verbeteren.

Nadat een bezoeker uw doel heeft voltooid, wordt die bezoeker niet meer opgenomen in de campagne. Als de bezoeker uw campagne weer betreedt nadat hij of zij een activiteit heeft voltooid, wordt hij of zij geteld als nieuwe bezoeker.
