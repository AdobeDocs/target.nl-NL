---
keywords: analysetrackingserver;A4T;Adobe Experience Cloud-foutopsporing;Adobe Experience Platform-foutopsporing;bron rapporteren;ontwikkelprogramma's
description: Als u een oudere versie van at.js of mbox.js gebruikt, moet u een analytische volgende server voor activiteiten specificeren die Analytics voor Doel (A4T) gebruiken.
title: Een Analytics Tracking Server gebruiken
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---


# Een Analytics-trackingserver gebruiken

Als u een oudere versie van at.js of mbox.js gebruikt, moet u een Analytics tracking-server opgeven voor activiteiten die [!DNL Analytics] voor [!DNL Target] (A4T) gebruiken.

>[!NOTE]
>
>Als u [!DNL Analytics] als rapportbron van uw activiteit gebruikt, te hoeven u niet om een het volgen server tijdens activiteitenverwezenlijking te specificeren als u mbox.js versie 61 (of recenter) of bij.js versie 0.9.1 (of later) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings].
>
>Het [!DNL Target] team steunt allebei at.js 1.** xand at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Zie [at.js versiedetails](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) voor meer informatie.

Om ervoor te zorgen dat gegevens van [!DNL Target] naar de correcte plaats in [!DNL Analytics] gaan, vereist A4T dat een Analytics het volgen server in alle vraag van [!DNL Target] aan Modstats wordt verzonden. Voor implementaties die meerdere trackingservers gebruiken, kunt u [!DNL Adobe Experience Platform Debugger] of de Developer Tools van uw browser gebruiken om de juiste trackingserver voor uw activiteit te bepalen.

## De Analytics Tracking-server ophalen met de Adobe Experience Platform Debugger

Foutopsporing zou op een pagina moeten worden bekeken waar de activiteit zal worden geleverd om u te verzekeren de correcte volgende server selecteert. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open [!DNL Adobe Experience Platform Debugger] op de pagina waarop u uw activiteit maakt.

   Als u debugger niet hebt geïnstalleerd, zie [Inleiding aan de Debugger van Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klik **[!UICONTROL Analytics]** in het linkernavigatiemenu.

   De Analytics tracking-server bevindt zich in de sectie [!UICONTROL Hostname] van het foutopsporingsprogramma.

   * **First-party tracking-server**: Als de hostnaam van de aanvraag overeenkomt met het domein waarop u zich bevindt, is het een eerstelijnsspatiëringsserver. Als u bijvoorbeeld op `adobe.com` werkt, is `adobe.com` de eerstgenoemde trackingserver.
   * **De volgende server** van derden: Een server voor het bijhouden van gegevens door derden is doorgaans  `[company].sc.omtrdc.net` de locatie waar het bedrijf de naam van het bedrijf heeft, maar eindigt altijd  `sc.omtrdc.net`.
   * **CNAME-implementaties**:  `sstats.adobe.com` Dit is een voorbeeld van een CNAME-server voor het bijhouden van een aanvraag voor https (secure). `stats.adobe.com` Dit is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. Plak in de sectie **[!UICONTROL Reporting Settings]** van het **[!UICONTROL Goal & Settings]**-scherm van uw activiteit de informatie over de trackingserver in het veld **[!UICONTROL Tracking Server]**.

   >[!NOTE]
   >
   >Het veld [!UICONTROL Tracking Server] is alleen beschikbaar als u [!UICONTROL Analytics as the Reporting Source] hebt geselecteerd.

## Haal de Analytics tracking-server op met de Developer Tools van uw browser

De Developer Tools moet worden weergegeven op een pagina waarop de activiteit wordt geleverd, zodat u de juiste trackingserver selecteert. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open de Developer Tools van de browser op de pagina waarop u uw activiteit maakt (klik in Google Chrome op de drie verticale ellipsen in de rechterbovenhoek > Meer gereedschappen > Gereedschappen voor ontwikkelaars).

   ![Gereedschappen voor Chrome-ontwikkelaars](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klik op het tabblad **[!UICONTROL Network]**.

1. Filter voor `/ss,` om de verzoeken van Analytics te tonen.

   ![De ontwikkelaars van Chrome hulpmiddelen met /ss onderzoek](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   De volgende server is hostname van het verzoek.

   * **First-party tracking-server**: Als de hostnaam van de aanvraag overeenkomt met het domein waarop u zich bevindt, is het een eerstelijnsspatiëringsserver. Als u bijvoorbeeld op `adobe.com` werkt, is `adobe.com` de eerstgenoemde trackingserver.
   * **De volgende server** van derden: Een server voor het bijhouden van gegevens door derden is doorgaans  `[company].sc.omtrdc.net` de locatie waar het bedrijf de naam van het bedrijf heeft, maar eindigt altijd  `sc.omtrdc.net`.
   * **CNAME-implementaties**:  `sstats.adobe.com` Dit is een voorbeeld van een CNAME-server voor het bijhouden van een aanvraag voor https (secure). `stats.adobe.com` Dit is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. Plak in de sectie **[!UICONTROL Reporting Settings]** van het **[!UICONTROL Goal & Settings]**-scherm van uw activiteit de informatie over de trackingserver in het veld **[!UICONTROL Tracking Server]**.

   >[!NOTE]
   >
   >Het veld [!UICONTROL Tracking Server] is alleen beschikbaar als u [!UICONTROL Analytics as the Reporting Source] hebt geselecteerd.

