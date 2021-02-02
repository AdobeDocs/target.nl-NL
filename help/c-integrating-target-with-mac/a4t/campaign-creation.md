---
keywords: a4t;A4T;Analyse als bron voor rapportage voor Target
description: U kunt een activiteit in de Norm van het Doel/Premium vormen om Adobe Analytics als rapporteringsbron (A4T) te gebruiken.
title: Een activiteit maken die A4T als rapportagebron gebruikt
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4f0f1df1bcb6baad0e20c4dc1ae7e12751080d91
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---


# Maak een activiteit die Analytics als rapportbron gebruikt

U kunt een activiteit in [!DNL Target] vormen om [!DNL Adobe Analytics] als rapporteringsbron (A4T) te gebruiken.

Voordat u een activiteit instelt die [!DNL Analytics] als rapportagebron gebruikt, stelt u het doel voor de activiteit in, zoals het verbeteren van de inkomsten per bezoeker (RPV) of het verhogen van de klik op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u extra metriek op elk ogenblik in [!DNL Analytics] kunt selecteren, moet u nog bepaalde metrisch specificeren u deze test om verwacht te beïnvloeden.

## De activiteit maken

Het maken van een [!DNL Target] activiteit die [!DNL Analytics] als rapportbron gebruikt is gelijkaardig aan vestiging een regelmatige [!DNL Target] activiteit, met een paar belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten die beschikbaar zijn in [!DNL Analytics], kunnen worden toegepast wanneer u een rapport weergeeft.

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitsnaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.

1. Selecteer het type activiteit en stel de activiteit in.

   Als u een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit wilt tot stand brengen, zie [A4T steun voor auto-Toewijzing en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md) voor meer informatie.

1. Wanneer u aan het **[!UICONTROL Settings]** gedeelte van de stroom van de activiteitenverwezenlijking krijgt, kies **[!UICONTROL Adobe Analytics]** en specificeer uw bedrijf.
1. Selecteer een rapportsuite.

   U kunt om het even welke rapportreeks kiezen die aan u in [!DNL Analytics] beschikbaar is. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

      Mogelijk moet u uw [!DNL Analytics] bedrijf controleren. Als uw [!DNL Adobe Experience Cloud]-account aan meerdere [!DNL Analytics]-bedrijven is gekoppeld, meldt u zich af bij [!DNL Target] en meldt u zich aan bij [!DNL Analytics] onder het juiste bedrijf. Keer dan aan [!DNL Target] terug, en de rapportreeksen zullen laden.

   * Je ziet de rapportsuite die je verwacht niet.

      Alleen rapportsuites die zijn ingericht om verbinding te maken met [!DNL Target] zijn beschikbaar voor selectie. Als u de rapportsuite(s) die u verwacht niet ziet, probeert u zich eerst af te melden en zich weer aan te melden bij [!DNL Adobe Experience Cloud] om het opnieuw te proberen.
   Als de rapportsuite(s) nog steeds ontbreekt in de lijst, neemt u [contact op met de klantenservice](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) gebruiken.

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt om het even welke [!DNL Analytics] metrisch beschikbaar in [!DNL Analytics] metrische selecteur kiezen.

   >[!NOTE]
   >
   >U kunt een aangepaste op doel gebaseerde metrische waarde naar [!DNL Analytics] verzenden in plaats van alleen op [!DNL Analytics]-gegevens te vertrouwen. U kunt bijvoorbeeld controleren of er op een pagina wordt geklikt, wat gewoonlijk niet wordt bijgehouden door [!DNL Analytics]. Deze aangepaste metrische waarde wordt automatisch verzonden naar [!DNL Analytics] van de [!DNL Target] server, en verschijnt als &quot;[!DNL Target] Omzetting&quot;metrische metriek in [!DNL Analytics]. De omrekeningsnorm [!DNL Target] is leeg als u verkiest om [!DNL Analytics] metriek te gebruiken.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt nadat u [!DNL Analytics] hebt ingesteld als uw rapporteringsbron, is er geen optie voor het instellen van soorten publiek voor rapportage. [!DNL Analytics] de segmenten zijn beschikbaar in het  [!DNL Target] activiteitenverslag.

1. Klik op **[!UICONTROL Save]**.

## A4T- en Auto-Allocate- en Auto-Target-activiteiten

Voor meer informatie, zie [A4T steun voor auto-Wijs en auto-Doel activiteiten](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).