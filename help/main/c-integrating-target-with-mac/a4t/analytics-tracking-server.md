---
keywords: analysetrackingserver;A4T;Adobe Experience Cloud-foutopsporing;Adobe Experience Platform-foutopsporing;bron rapporteren;ontwikkelprogramma's
description: Leer hoe te om een het volgen van Analytics server voor activiteiten te specificeren die Analytics voor  [!DNL Target]  (A4T) gebruiken als u een oudere versie van at.js gebruikt.
title: Hoe gebruik ik een Analytics Tracking Server?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Een [!DNL Analytics] tracking-server gebruiken

Als u een oudere versie van at.js gebruikt, moet u een [!DNL Analytics] tracking-server opgeven voor activiteiten die [!DNL Adobe Analytics] for [!DNL Adobe Target] (A4T) gebruiken.

>[!NOTE]
>
>U hoeft tijdens het maken van activiteiten geen trackingserver op te geven als u at.js versie 0.9.1 (of hoger) gebruikt. De bibliotheek at.js verzendt automatisch de waarden van de volgende server naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het veld [!UICONTROL Tracking Server] leeg laten op de pagina [!UICONTROL Goals & Settings] .
>
>Het team van [!DNL Target] ondersteunt beide at.js 1.*x* en at.js 2.*x*. Voer een upgrade uit naar de meest recente update van een van de belangrijkste versies van at.js om ervoor te zorgen dat u een ondersteunde versie uitvoert. Voor meer informatie, zie [&#x200B; at.js versiedetails &#x200B;](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=nl-NL){target=_blank}.

Om ervoor te zorgen dat gegevens van [!DNL Target] naar de correcte plaats in [!DNL Analytics] gaan, vereist A4T dat een [!DNL Analytics] volgende server in alle vraag van [!DNL Target] naar Modstats wordt verzonden. Voor implementaties die meerdere trackingservers gebruiken, gebruikt u [!DNL Adobe Experience Platform Debugger] of de Developer Tools van uw browser om de juiste trackingserver voor uw activiteit te bepalen.

## De [!DNL Analytics] tracking-server ophalen met [!DNL Adobe Experience Platform Debugger]

Foutopsporing zou op een pagina moeten worden bekeken waar de activiteit wordt geleverd om te verzekeren u de correcte volgende server selecteert. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open [!DNL Adobe Experience Platform Debugger] vanaf de pagina waarop u uw activiteit maakt.

   Als u debugger niet hebt geïnstalleerd, zie [&#x200B; overzicht van Adobe Experience Platform Debugger &#x200B;](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html?lang=nl-NL).

1. Klik op **[!UICONTROL Analytics]** in het navigatiemenu links.

   ![&#x200B; Screen_DebuggerTrackServ beeld &#x200B;](assets/Screen_DebuggerTrackServ.png)

   De [!DNL Analytics] tracking-server bevindt zich in de [!UICONTROL Hostname] -sectie van het foutopsporingsprogramma.

   * **Eerste partij die server** volgt: Als hostname van het verzoek het domein aanpast u bent, dan is het een eerste partij volgende server. Als u bijvoorbeeld op `adobe.com` werkt, is `adobe.com` de server voor het eerst bijhouden.
   * **het volgen van de derde server**: Een derde het volgen server is typisch `[company].sc.omtrdc.net` waar het bedrijf de naam van uw bedrijf is, maar eindigt altijd in `sc.omtrdc.net`.
   * **implementaties CNAME**: `sstats.adobe.com` is een voorbeeld van een CNAME eerste partij volgende server voor een (veilige) HTTP- verzoek. `stats.adobe.com` is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. Plak in de sectie **[!UICONTROL Reporting Settings]** van het scherm **[!UICONTROL Goal & Settings]** van uw activiteit de informatie over de trackingserver in het veld **[!UICONTROL Tracking Server]** .

   >[!NOTE]
   >
   >Selecteer [!UICONTROL Analytics as the Reporting Source] als het veld [!UICONTROL Tracking Server] beschikbaar moet zijn.

## De [!DNL Analytics] tracking-server ophalen met de Developer Tools van uw browser

De Developer Tools moet worden weergegeven op een pagina waarop de activiteit wordt geleverd, zodat u de juiste trackingserver kunt selecteren. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open de Developer Tools van de browser op de pagina waarop u uw activiteit maakt (klik in Google Chrome op de drie verticale ellipsen in de rechterbovenhoek > Meer gereedschappen > Gereedschappen voor ontwikkelaars).

   ![&#x200B; de ontwikkelaarshulpmiddelen van Chrome &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Klik op de tab **[!UICONTROL Network]** .

1. Filter voor `/ss,` om de [!DNL Analytics] -aanvragen weer te geven.

   ![&#x200B; de ontwikkelaarshulpmiddelen van Chrome met /ss onderzoek &#x200B;](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   De volgende server is hostname van het verzoek.

   * **Eerste partij die server** volgt: Als hostname van het verzoek het domein aanpast u bent, dan is het een eerste partij volgende server. Als u bijvoorbeeld op `adobe.com` werkt, is `adobe.com` de server voor het eerst bijhouden.
   * **het volgen van de derde server**: Een derde het volgen server is typisch `[company].sc.omtrdc.net` waar het bedrijf de naam van uw bedrijf is, maar eindigt altijd in `sc.omtrdc.net`.
   * **implementaties CNAME**: `sstats.adobe.com` is een voorbeeld van een CNAME eerste partij volgende server voor een (veilige) HTTP- verzoek. `stats.adobe.com` is een voorbeeld van een CNAME-aanvraag van de eerste partij voor een http-pagina (niet-beveiligd).

1. Kopieer de volledige inhoud van het veld.

1. Plak in de sectie **[!UICONTROL Reporting Settings]** van het scherm **[!UICONTROL Goal & Settings]** van uw activiteit de informatie over de trackingserver in het veld **[!UICONTROL Tracking Server]** .

   >[!NOTE]
   >
   >Selecteer [!UICONTROL Analytics as the Reporting Source] als het veld [!UICONTROL Tracking Server] beschikbaar moet zijn.
