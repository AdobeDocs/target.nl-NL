---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;reporting source
description: Als u een oudere versie van at.js of mbox.js gebruikt, moet u een analytische volgende server voor activiteiten specificeren die Analytics voor Doel (A4T) gebruiken.
title: Een Analytics-trackingserver gebruiken
feature: null
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Een Analytics-trackingserver gebruiken{#use-an-analytics-tracking-server}

Als u een oudere versie van at.js of mbox.js gebruikt, moet u een analysetrackingserver voor activiteiten specificeren die [!DNL Analytics] voor [!DNL Target] (A4T) gebruiken.

>[!NOTE]
>
>Als u [!DNL Analytics] als rapporteringsbron van uw activiteit gebruikt, te hoeven u niet om een het volgen server tijdens activiteitenverwezenlijking te specificeren als u mbox.js versie 61 (of recenter) of versie 0.9.1 van .js (of later) gebruikt. De bibliotheek mbox.js of at.js verzendt automatisch het volgen serverwaarden naar [!DNL Target]. Tijdens het maken van activiteiten kunt u het [!UICONTROL Tracking Server] veld leeg laten op de [!UICONTROL Goals & Settings] pagina.

Om ervoor te zorgen dat de gegevens van [!DNL Target] naar de correcte plaats binnen gaan [!DNL Analytics], vereist A4T een analytische het volgen server om in alle vraag naar Modstats van [!DNL Target]. worden verzonden. Voor implementaties die meerdere trackingservers gebruiken, kunt u het programma gebruiken [!DNL Adobe Experience Cloud Debugger] om de juiste trackingserver voor uw activiteit te bepalen.

Foutopsporing zou op een pagina moeten worden bekeken waar de activiteit zal worden geleverd om u te verzekeren de correcte volgende server selecteert. U kunt ook een standaard traceringsserver opgeven voor elk account. Neem contact op met de klantenservice om de standaardinstelling op te geven of te wijzigen.

1. Open de [!DNL Adobe Experience Cloud Debugger]pagina op de pagina waarop u uw activiteit maakt.

   Zie Experience Cloud Debugger [installeren als u de foutopsporing niet hebt geïnstalleerd](https://docs.adobe.com/content/help/en/debugger/using/install-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

   De analytische traceringsserver vindt u in de [!UICONTROL SiteCatalyst Image] sectie van het foutopsporingsprogramma. Het veld wordt, afhankelijk van de implementatie, Cookies van *eerste partij* of Cookies *van* derden genoemd en de waarde van de [!DNL Analytics] trackingserver wordt in een van de volgende notaties gebruikt:

   * (voor CNAME-implementaties)
   * (voor niet-regionale implementaties)
   * (voor de uitvoering van de regionale distributieovereenkomst)

   *Het bedrijf* vertegenwoordigt de [!DNL Analytics] bedrijfsnaam, *metriek* is een voorbeeld van een waarde CNAME, en *d1* is een voorbeeld van een [!DNL Analytics] gegevenscentrum.
1. Kopieer de volledige inhoud van het veld.
1. Plak in het [!UICONTROL Reporting Settings] gedeelte van het [!UICONTROL Goal & Settings] scherm van uw activiteit de trackingserverinformatie in het **[!UICONTROL Tracking Server]** veld.

   >[!NOTE]
   >
   >U moet uw activiteit selecteren [!UICONTROL Analytics as the Reporting Source] om het [!UICONTROL Tracking Server] gebied beschikbaar te maken.

