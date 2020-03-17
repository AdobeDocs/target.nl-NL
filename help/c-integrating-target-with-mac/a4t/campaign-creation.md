---
keywords: a4t;A4T;Analytics as the reporting source for Target
description: U kunt een activiteit in Standaard/Premium van het Doel vormen om de Analytics van Adobe als rapporteringsbron (A4T) te gebruiken.
title: Activiteitenschepping
topic: Advanced,Standard,Classic
uuid: b04ad535-62fb-4dd3-ab3f-23da60fbffbd
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Activiteitenschepping{#activity-creation}

U kunt een activiteit in Standaard/Premium van het Doel vormen om de Analytics van Adobe als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die Analytics als bron voor rapportage gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u extra metriek op elk ogenblik in Analytics kunt selecteren, moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

Het creëren van een Standaardactiviteit van het Doel die Analytics als rapporteringsbron gebruikt is gelijkaardig aan vestiging een regelmatige Standaardactiviteit van het Doel, met een paar belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in Analytics kunnen worden toegepast wanneer u een rapport weergeeft.

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitsnaam mag niet het teken &quot;%&quot; bevatten als Analytics wordt gebruikt als rapportagebron.

1. Selecteer het type activiteit en stel de activiteit in.
1. Wanneer u aan het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt elke rapportsuite kiezen die beschikbaar is in Adobe Analytics. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.
   Mogelijk moet u het bedrijf Analytics controleren. Als uw Experience Cloud-account aan meerdere Analytics-bedrijven is gekoppeld, meldt u zich af bij Target en meldt u zich aan bij Analytics onder het juiste bedrijf. Dan terugkeer aan Doel, en de rapportsuites zullen laden.

   * Je ziet de rapportsuite die je verwacht niet.
   Alleen rapportsuites die zijn ingericht voor verbinding met Adobe Target zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, meldt u zich eerst af en meldt u zich opnieuw aan bij Adobe Experience Cloud om het opnieuw te proberen.

   Als de rapportsuite(s) nog steeds ontbreekt in de lijst, [neemt u contact op met de klantenservice](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).
1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server](../../c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823)gebruiken.

1. Definieer de ervaring..
1. Geef het doel van de activiteit op.

   U wordt vereist om een succes metrisch te selecteren als doel voor elke test te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt elke beschikbare metrische waarde voor Analytics kiezen in de metrische kiezer voor Analytics.

   >[!NOTE]
   >
   >U kunt een aangepaste, op doelen gebaseerde metrische waarde naar Analytics verzenden in plaats van alleen op Analytics-gegevens te vertrouwen. U kunt bijvoorbeeld controleren of er op een pagina wordt geklikt, wat gewoonlijk niet wordt bijgehouden door Analytics. Deze aangepaste metrische waarde wordt automatisch vanuit de doelserver naar Analytics verzonden en wordt als de metrische waarde voor Doelconversie weergegeven in de metrische kiezer in Analytics. De metrische waarde voor doelomzetting is leeg als u de metriek Analytics wilt gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u Analytics hebt ingesteld als uw rapportbron, is er geen optie voor het instellen van soorten publiek voor rapportage. De segmenten van Analytics zijn beschikbaar in het rapport van de Activiteiten van het Doel.

1. Klik op **[!UICONTROL Save]**.

