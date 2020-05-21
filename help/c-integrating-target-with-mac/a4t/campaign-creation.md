---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: U kunt een activiteit in Standaard/Premium van het Doel vormen om de Analytics van Adobe als rapporteringsbron (A4T) te gebruiken.
title: Activiteitenschepping
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: 68f356b0711abf9acf7ef631edf3656bd3dd49e3
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---


# Activiteitenschepping{#activity-creation}

U kunt een activiteit binnen vormen [!DNL Target] [!DNL Adobe Analytics] om als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die [!DNL Analytics] als bron voor rapportage wordt gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u extra metriek op elk ogenblik binnen kunt selecteren [!DNL Analytics], moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

Het maken van een [!DNL Target] activiteit die gebruikt wordt [!DNL Analytics] als de bron van de rapportage is vergelijkbaar met het instellen van een reguliere [!DNL Target] activiteit, met enkele belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in, kunnen worden toegepast wanneer u een rapport weergeeft. [!DNL Analytics]

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitennaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.

1. Selecteer het type activiteit en stel de activiteit in.
1. Wanneer u aan het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt elke rapportsuite kiezen die voor u beschikbaar is in [!DNL Analytics]. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

      Mogelijk moet u uw [!DNL Analytics] bedrijf controleren. Als uw [!DNL Adobe Experience Cloud] account aan meerdere [!DNL Analytics] bedrijven is gekoppeld, meldt u zich af [!DNL Target]en meldt u zich aan bij [!DNL Analytics] het juiste bedrijf. Keer dan terug naar [!DNL Target], en de rapportsuites zullen laden.

   * Je ziet de rapportsuite die je verwacht niet.

      Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] worden geselecteerd. Als u de rapportsuite(s) die u verwacht, niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij de [!DNL Adobe Experience Cloud] groep om het opnieuw te proberen.
   Als de rapportsuite(s) nog steeds ontbreekt in de lijst, [neemt u contact op met de klantenservice](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)gebruiken.

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare [!DNL Analytics] metrische waarde in de [!DNL Analytics] metrische kiezer kiezen.

   >[!NOTE]
   >
   >U kunt een op doel-Gebaseerde metrisch van de douane verzenden naar [!DNL Analytics] eerder dan het baseren slechts op [!DNL Analytics] gegevens. U kunt bijvoorbeeld controleren of er op een pagina wordt geklikt. Dit wordt meestal niet door [!DNL Analytics]bijgehouden. Deze aangepaste metrische waarde wordt [!DNL Analytics] automatisch van de [!DNL Target] server verzonden en wordt in de metriekkiezer in weergegeven als de metrische waarde &quot;[!DNL Target] Conversie&quot; [!DNL Analytics]. De metrische waarde voor [!DNL Target] omzetten is leeg als u [!DNL Analytics] metriek wilt gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u deze hebt ingesteld [!DNL Analytics] als bron voor rapportage, kunt u geen publiek instellen voor rapportage. [!DNL Analytics] de segmenten zijn beschikbaar in het [!DNL Target] activiteitenverslag.

1. Klik op **[!UICONTROL Save]**.
