---
keywords: richten;botsingen;conflicten
description: Er treden conflicten op wanneer meerdere activiteiten zijn ingesteld om inhoud aan dezelfde pagina te leveren. Leer hoe u conflicten kunt voorkomen wanneer u Adobe Target gebruikt.
title: Hoe kan ik activiteitsbotsingen voorkomen?
feature: Visual Experience Composer (VEC)
exl-id: 1af90dd1-69c9-41ec-8785-095dcc557b32
source-git-commit: 430b2ebb053460ec04c01da53aadacaba9e99599
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Conflicten bij activiteit

De [!UICONTROL Collisions] op het tabblad [!UICONTROL Activity Overview] pagina in [!DNL Adobe Target] maakt een lijst van activiteitenbotsingen op uw plaats.

Een activiteitenbotsing komt voor wanneer de veelvoudige activiteiten opstelling zijn om inhoud aan de zelfde pagina te leveren. Als er een conflict optreedt met een activiteit, ziet u mogelijk niet de verwachte inhoud op de pagina.

Als uw activiteit potentiële botsingen bevat, [!UICONTROL Collisions] is beschikbaar op de pagina met het activiteitenoverzicht. Alle activiteiten op dezelfde URL worden vermeld, ongeacht de doelgroep in elke activiteit. Open dit tabblad voor een lijst met activiteiten die mogelijk aan elkaar botsen. Klik op een activiteit in de lijst om de overzichtspagina voor die activiteit weer te geven. Als de botsing de verwachte ervaring verandert, geef de activiteit uit.

De [!UICONTROL Collisions] de lijst helpt u:

* Bepaal of een test al op een pagina wordt uitgevoerd voordat u een nieuwe activiteit instelt
* Een activiteit oplossen als de verwachte inhoud niet wordt weergegeven

De [!UICONTROL Collisions] lijst toont elke [!DNL Target] scenario waar mbox wordt gebruikt en dat zelfde URL gebruikt. Voor elke potentiële botsing, toont de lijst de Activiteit URL, de mbox naam waar de botsing zou kunnen voorkomen, en om het even welke activiteiten die beide criteria aanpassen. Als er meerdere vakken zijn, worden deze weergegeven.

De lijst toont de status en de prioriteit van elke potentiële botsing, samen met andere informatie. U kunt de status en de prioriteit gebruiken om u te helpen de waarschijnlijkheid bepalen van een botsing die voorkomt. Bijvoorbeeld, als er een potentiële botsing tussen twee activiteiten is en één inactief is, zal er geen daadwerkelijke botsing zijn tenzij de inactieve activiteit wordt geactiveerd. Als de potentiële botsing tussen twee levende activiteiten met de zelfde prioriteit en het zelfde publiek is, zal een botsing voorkomen. U kunt de prioriteit of de status veranderen om de botsing te verhinderen.

Als het publiek verschillend is, is er nog een potentiële botsing omdat het mogelijk is dat een bepaalde bezoeker tot veelvoudige soorten publiek zou kunnen behoren.
