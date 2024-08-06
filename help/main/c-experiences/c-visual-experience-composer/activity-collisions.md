---
keywords: richten;botsingen;conflicten
description: Vermijd botsingen van de inhoudslevering op de zelfde pagina door activiteiten correct in Adobe Target te vormen.
title: Hoe kan ik activiteitsbotsingen voorkomen?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: 5c963e97dae11326396a5c1c5e32d19f4d463c74
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Conflicten bij activiteit

Het tabblad [!UICONTROL Collisions] op de [!UICONTROL Activity Overview] pagina in [!DNL Adobe Target] geeft een overzicht van activiteitenbotsingen op uw site.

Een activiteitenbotsing komt voor wanneer de veelvoudige activiteiten opstelling zijn om inhoud aan de zelfde pagina te leveren. Als een activiteitenbotsing voorkomt, zou u niet de verwachte inhoud op uw pagina kunnen zien.

Het tabblad [!UICONTROL Collisions] is beschikbaar op de pagina met het activiteitenoverzicht en kan u informeren of uw activiteit mogelijke botsingen bevat.

Als u het tabblad [!UICONTROL Collisions] wilt openen, klikt u op **[!UICONTROL Activities]** > op de gewenste activiteit in de lijst > en vervolgens klikt u op **[!UICONTROL Collisions]** in de linkertrack.

Alle activiteiten op dezelfde URL worden vermeld, ongeacht de doelgroep in elke activiteit. Open dit tabblad voor een lijst met activiteiten die mogelijk aan elkaar botsen. Als de botsing de verwachte ervaring verandert, geef de activiteit uit.

De lijst [!UICONTROL Collisions] helpt u:

* Bepaal of een test al op een pagina wordt uitgevoerd voordat u een nieuwe activiteit instelt
* Een activiteit oplossen als de verwachte inhoud niet wordt weergegeven

In de lijst [!UICONTROL Collisions] worden alle [!DNL Target] -scenario&#39;s weergegeven waarin de box wordt gebruikt en die dezelfde URL gebruiken. Voor elke potentiële botsing, toont de lijst de Activiteit URL, de mbox naam waar de botsing zou kunnen voorkomen, en om het even welke activiteiten die beide criteria aanpassen. Als er meerdere vakken zijn, worden deze weergegeven.

De lijst toont de status en de prioriteit van elke potentiële botsing, samen met andere informatie. U kunt de status en de prioriteit gebruiken om u te helpen de waarschijnlijkheid bepalen van een botsing die voorkomt. Overweeg twee activiteiten die botsen. Als één activiteit momenteel niet actief is, kan een botsing niet voorkomen. Een botsing is slechts mogelijk als de inactieve activiteit actief wordt. Als de potentiële botsing tussen twee levende activiteiten met de zelfde prioriteit en het zelfde publiek is, komt een botsing voor. U kunt de prioriteit of de status veranderen om de botsing te verhinderen.

Als het publiek verschillend is, is er nog een potentiële botsing omdat het mogelijk is dat een bepaalde bezoeker tot veelvoudige soorten publiek zou kunnen behoren.
