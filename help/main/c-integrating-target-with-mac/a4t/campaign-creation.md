---
keywords: a4t;A4T;Analyse als bron voor rapportage voor Target
description: Leer hoe te om een activiteit in Adobe  [!DNL Target]  te vormen die Adobe Analytics als rapporteringsbron (A4T) gebruikt.
title: Hoe maak ik een activiteit die A4T gebruikt?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Maak een activiteit die Analytics als rapportbron gebruikt

U kunt een activiteit in [!DNL Adobe Target] vormen om [!DNL Adobe Analytics] als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die [!DNL Analytics] als bron voor rapportage gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de omzet per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u op elk moment in [!DNL Analytics] meer metriek kunt selecteren, moet u toch een bepaalde metrische waarde specificeren die deze test naar verwachting zal beïnvloeden.

## De activiteit maken

Het maken van een [!DNL Target] -activiteit die [!DNL Analytics] als rapportagebron gebruikt, lijkt op het instellen van een normale [!DNL Target] -activiteit, met enkele belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in [!DNL Analytics], kunnen worden toegepast wanneer u een rapport weergeeft.

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitsnaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.
   >
   >Gebruik niet de zelfde activiteitennaam voor twee activiteiten van afzonderlijke [&#x200B; werkruimten &#x200B;](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) die A4T het melden gebruiken.

1. Selecteer het type activiteit en begin met het instellen van de activiteit.

   Als u [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit wilt tot stand brengen, zie [&#x200B; steun A4T voor auto-Toewijzing en Auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) voor meer informatie.

1. Wanneer u het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt elke rapportsuite kiezen die beschikbaar is in [!DNL Analytics] . De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

     Controleer uw [!DNL Analytics] bedrijf. Als uw [!DNL Adobe Experience Cloud] -account aan meerdere [!DNL Analytics] bedrijven is gekoppeld, meldt u zich af bij [!DNL Target] en meldt u zich aan bij [!DNL Analytics] onder het juiste bedrijf. Ga vervolgens terug naar [!DNL Target] en de rapportsuites worden geladen.

   * Je ziet de rapportsuite die je verwacht niet.

     Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuites niet ziet die u verwacht, probeer eerst het programma openen en opnieuw binnen aan [!DNL Adobe Experience Cloud] proberen opnieuw te proberen.

   Als één of meerdere rapportsuites nog van de lijst ontbreken, gelieve [&#x200B; de Zorg van de Klant van het contact &#x200B;](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [&#x200B; Gebruikend een Analytics die Server &#x200B;](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) volgen.

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare [!DNL Analytics] metrische waarde in de [!DNL Analytics] -metrische kiezer kiezen.

   >[!NOTE]
   >
   >U kunt een aangepaste, op doelen gebaseerde metrische waarde naar [!DNL Analytics] verzenden in plaats van alleen op [!DNL Analytics] -gegevens te vertrouwen. U kunt bijvoorbeeld controleren of u op een pagina klikt, die gewoonlijk niet wordt bijgehouden door [!DNL Analytics] . Deze aangepaste metrische waarde wordt automatisch verzonden naar [!DNL Analytics] vanaf de [!DNL Target] -server en wordt weergegeven als de metrische waarde voor &quot;[!DNL Target] Omzetting&quot; in de metrische kiezer in [!DNL Analytics] . De [!DNL Target] -omzettingsmaatstaf is leeg als u [!DNL Analytics] -meetgegevens wilt gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u [!DNL Analytics] hebt ingesteld als rapportbron, is er geen optie voor het instellen van soorten publiek voor rapportage. [!DNL Analytics] -segmenten zijn beschikbaar in het [!DNL Target] Activiteiten-rapport.

1. Klik op **[!UICONTROL Save]**.

## A4T- en Auto-Allocate- en Auto-Target-activiteiten

Voor meer informatie, zie [&#x200B; steun A4T voor auto-Wijs en auto-Doel activiteiten &#x200B;](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) toe.
