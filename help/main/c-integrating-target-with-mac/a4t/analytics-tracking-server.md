---
keywords: analysetrackingserver;A4T;Adobe Experience Cloud-foutopsporing;Adobe Experience Platform-foutopsporing;bron rapporteren;ontwikkelprogramma's
description: 'Leer hoe u een Analytics-traceringsserver opgeeft voor activiteiten waarvoor Analytics wordt gebruikt [!DNL Target] (A4T) als u een oudere versie van at.js gebruikt. '
title: Hoe gebruik ik een Analytics Tracking Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Een Analytics-trackingserver gebruiken

Als u een oudere versie van at.js gebruikt, moet u een Analytics tracking-server opgeven voor activiteiten die [!DNL Adobe Analytics] for [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>U hoeft tijdens het maken van activiteiten geen trackingserver op te geven als u at.js versie 0.9.1 (of hoger) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het creëren van activiteit, kunt u verlaten [!UICONTROL Tracking Server] veld leeg op [!UICONTROL Goals & Settings] pagina.
>
>De [!DNL Target] team steunt allebei at.js 1.*x* en te.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Zie voor meer informatie [details van de at.js-versie](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/).

Om ervoor te zorgen dat gegevens van [!DNL Target] gaat naar de juiste locatie in [!DNL Analytics], A4T vereist een Analytics die server controleert om in alle vraag naar Modstats van te worden verzonden [!DNL Target]. Voor implementaties die meerdere trackingservers gebruiken, gebruikt u de opdracht [!DNL Adobe Experience Platform Debugger] of de ontwikkelaarsgereedschappen van uw browser om de juiste trackingserver voor uw activiteit te bepalen.

## De Analytics Tracking-server ophalen met de Adobe Experience Platform Debugger

Foutopsporing zou op een pagina moeten worden bekeken waar de activiteit wordt geleverd om te verzekeren u de correcte volgende server selecteert. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open vanaf de pagina waarop u uw activiteit maakt de [!DNL Adobe Experience Platform Debugger].

   Als u debugger niet hebt geïnstalleerd, zie [Inleiding tot de Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Klikken **[!UICONTROL Analytics]** in het navigatiemenu aan de linkerkant.

   De server voor het bijhouden van analyses is te vinden in het dialoogvenster [!UICONTROL Hostname] van het foutopsporingsprogramma.

   * **First-party tracking-server**: Als de hostnaam van de aanvraag overeenkomt met het domein waarop u zich bevindt, is het een eerstelijnsspatiëringsserver. Als u bijvoorbeeld ingeschakeld bent `adobe.com`, `adobe.com` is de eerstgenoemde trackingserver.
   * **Trackingserver van derden**: Een trackingserver van derden is doorgaans `[company].sc.omtrdc.net` waar het bedrijf de naam van uw bedrijf is, maar altijd eindigt in `sc.omtrdc.net`.
   * **CNAME-implementaties**: `sstats.adobe.com` Dit is een voorbeeld van een CNAME-server voor het bijhouden van een aanvraag voor https (secure). `stats.adobe.com` Dit is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. In de **[!UICONTROL Reporting Settings]** van de **[!UICONTROL Goal & Settings]** scherm van uw activiteit, plak de het volgen serverinformatie in het **[!UICONTROL Tracking Server]** veld.

   >[!NOTE]
   >
   >Selecteren [!UICONTROL Analytics as the Reporting Source] voor uw activiteiten voor de [!UICONTROL Tracking Server] beschikbaar te maken.

## Haal de Analytics tracking-server op met de Developer Tools van uw browser

De Developer Tools moet worden weergegeven op een pagina waarop de activiteit wordt geleverd, zodat u de juiste trackingserver kunt selecteren. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open de Developer Tools van de browser op de pagina waarop u uw activiteit maakt (klik in Google Chrome op de drie verticale ellipsen in de rechterbovenhoek > Meer gereedschappen > Gereedschappen voor ontwikkelaars).

   ![Gereedschappen voor Chrome-ontwikkelaars](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klik op de knop **[!UICONTROL Network]** tab.

1. Filter voor `/ss,` om de analyseverzoeken weer te geven.

   ![De ontwikkelaars van Chrome hulpmiddelen met /ss onderzoek](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   De volgende server is hostname van het verzoek.

   * **First-party tracking-server**: Als de hostnaam van de aanvraag overeenkomt met het domein waarop u zich bevindt, is het een eerstelijnsspatiëringsserver. Als u bijvoorbeeld ingeschakeld bent `adobe.com`, `adobe.com` is de eerstgenoemde trackingserver.
   * **Trackingserver van derden**: Een trackingserver van derden is doorgaans `[company].sc.omtrdc.net` waar het bedrijf de naam van uw bedrijf is, maar altijd eindigt in `sc.omtrdc.net`.
   * **CNAME-implementaties**: `sstats.adobe.com` Dit is een voorbeeld van een CNAME-server voor het bijhouden van een aanvraag voor https (secure). `stats.adobe.com` Dit is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. In de **[!UICONTROL Reporting Settings]** van de **[!UICONTROL Goal & Settings]** scherm van uw activiteit, plak de het volgen serverinformatie in het **[!UICONTROL Tracking Server]** veld.

   >[!NOTE]
   >
   >Selecteren [!UICONTROL Analytics as the Reporting Source] voor uw activiteiten voor de [!UICONTROL Tracking Server] beschikbaar te maken.
