---
keywords: a4t;A4T;Analyse als bron voor rapportage voor Target
description: Leer hoe te om een activiteit in Adobe te vormen [!DNL Target] die Adobe Analytics als rapportagebron (A4T) gebruikt.
title: Hoe maak ik een activiteit die A4T gebruikt?
feature: Analytics for Target (A4T)
exl-id: 6a09764a-8bf1-4f69-b871-fb23136f933e
source-git-commit: 981cff428d9e8849b9bbcbf7bef389dad0fbb32a
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Maak een activiteit die Analytics als rapportbron gebruikt

U kunt een activiteit vormen binnen [!DNL Adobe Target] te gebruiken [!DNL Adobe Analytics] als bron van rapportage (A4T).

Voordat u een activiteit instelt die [!DNL Analytics] als bron van rapportage, het doel voor de activiteit bepalen, zoals het verbeteren van opbrengst per bezoeker (RPV) of het verhogen van kliks op uw winkelwagentje. Kies een uiteindelijke succesmaatstaf voor de activiteit. Hoewel u op elk gewenst moment meer meetgegevens kunt selecteren [!DNL Analytics], moet u bepaalde metrisch nog specificeren u deze test om verwacht te beïnvloeden.

## De activiteit maken

Een [!DNL Target] activiteit die [!DNL Analytics] aangezien de bron van de rapportage vergelijkbaar is met het instellen van een [!DNL Target] activiteit, met enkele belangrijke verschillen. U kunt bijvoorbeeld geen segment selecteren voor rapportage terwijl u de activiteit maakt, omdat alle segmenten beschikbaar zijn in [!DNL Analytics] kan worden toegepast wanneer het bekijken van een rapport.

1. Klik op **[!UICONTROL Create Activity]**.

   >[!NOTE]
   >
   >Een activiteitennaam mag niet het teken &quot;%&quot; bevatten als [!DNL Analytics] wordt gebruikt als rapportagebron.
   >
   >Gebruik niet dezelfde activiteitsnaam voor twee afzonderlijke activiteiten [werkruimten](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) die gebruikmaken van A4T-rapportage.

1. Selecteer het type activiteit en begin met het instellen van de activiteit.

   Als u een [!UICONTROL Auto-Allocate] of [!UICONTROL Auto-Target] activiteit, zie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md) voor meer informatie .

1. Wanneer u de **[!UICONTROL Settings]** deel van de stroom van de activiteitsverwezenlijking, kies **[!UICONTROL Adobe Analytics]** en geef uw bedrijf op.
1. Selecteer een rapportsuite.

   U kunt elke rapportsuite kiezen die beschikbaar is in [!DNL Analytics]. De rapportsuite definieert waar de verzamelde gegevens beschikbaar zijn. Virtuele rapportsuites zijn niet inbegrepen in de lijst van de rapportreeks.

   U zou twee mogelijke fouten kunnen ontmoeten terwijl het selecteren van de rapportreeks:

   * Er is een fout opgetreden omdat er geen rapportsuites beschikbaar zijn, maar uw account is juist ingesteld.

     Controleer uw [!DNL Analytics] bedrijf. Als uw [!DNL Adobe Experience Cloud] account is gekoppeld aan meerdere [!DNL Analytics] bedrijf, logout van [!DNL Target]en aanmelden bij [!DNL Analytics] onder de juiste onderneming. Ga vervolgens terug naar [!DNL Target]en de rapportsuites worden geladen.

   * Je ziet de rapportsuite die je verwacht niet.

     Alleen rapportsuites die zijn ingericht voor verbinding met [!DNL Target] zijn beschikbaar voor selectie. Als u niet de rapportsuites ziet die u verwacht, probeer eerst het registreren uit en het registreren terug aan [!DNL Adobe Experience Cloud] om het opnieuw te proberen.

   Indien een of meer rapporteereeksen nog steeds ontbreken in de lijst, gelieve [Contact opnemen met de klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

1. Geef de trackingserver op.

   Zie [Een Analytics Tracking Server gebruiken](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

1. Definieer de ervaring.
1. Geef het doel van de activiteit op.

   U moet een succesmetrische waarde selecteren om als doel voor elke activiteit te gebruiken. Uw activiteitendoel is de omzettingsactiviteit die een succesvolle activiteit signaleert. Het is de beste praktijk om nooit een test uit te voeren zonder een doel te hebben om op een bepaalde manier te verbeteren. U kunt kiezen uit [!DNL Analytics] de metrische waarde beschikbaar in [!DNL Analytics] metrische kiezer.

   >[!NOTE]
   >
   >U kunt een op douaneDoel-Gebaseerde metrisch verzenden naar [!DNL Analytics] in plaats van alleen op [!DNL Analytics] gegevens. U kunt bijvoorbeeld controleren of op een pagina wordt geklikt, die gewoonlijk niet door [!DNL Analytics]. Deze aangepaste metrische waarde wordt verzonden naar [!DNL Analytics] automatisch uit de [!DNL Target] en wordt weergegeven als &quot;[!DNL Target] Conversion&quot; (metrische waarde) in de metrische kiezer in [!DNL Analytics]. De [!DNL Target] De omzettingsmetrisch is leeg als u verkiest te gebruiken [!DNL Analytics] metriek.

   Het plaatsen van een doel betekent niet u kunt geen andere metrisch gebruiken wanneer het evalueren van testresultaten. Het doel is echter een herinnering aan één ding dat u met de activiteit wilt verbeteren.

   De bezoeker blijft in de activiteit nadat zij het doel bereiken. De bezoeker blijft de inhoud van de activiteit zien, maar wordt niet geteld als een nieuwe ingang van de activiteit.

   >[!NOTE]
   >
   >Wanneer u een activiteit instelt na het instellen [!DNL Analytics] als uw rapporteringsbron, is er geen optie aan opstellingspubliek voor rapportering. [!DNL Analytics] de segmenten zijn beschikbaar in [!DNL Target] Activiteitenrapport.

1. Klik op **[!UICONTROL Save]**.

## A4T- en Auto-Allocate- en Auto-Target-activiteiten

Zie voor meer informatie [A4T-ondersteuning voor activiteiten voor automatisch toewijzen en automatisch richten](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).
