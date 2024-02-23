---
keywords: IP-adres;IP-adressen;whitelist;lijst van gewenste personen;firewall;recs;feed;servers;adobe-marketingcloud;aanbevelingen
description: Een lijst weergeven met IP-adressen die worden gebruikt in [!DNL Target] Recommendations feed-processing servers helpen u bij het configureren van uw firewall om IP-adressen van Adobe servers toe te staan.
title: Welke IP adressen gebruiken de servers van de het voeder-Verwerking van Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Zie wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: be5b3158c758fa08802c1dc0541c9e989a2c7740
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# IP adressen die door worden gebruikt [!DNL Recommendations] feed-processing-servers

Lijst met IP-adressen gebruikt in [!DNL Adobe Target] [!DNL Recommendations] feed-processing servers om u te helpen uw firewall configureren zodat IP-adressen afkomstig van [!DNL Adobe] servers.

>[!IMPORTANT]
>
>De [!DNL Target] het team werkt momenteel de NATIONAAL gatewayadressen voor het downloaden bij [!DNL Recommendations] feeds. Als u IP voegend op lijst van gewenste personen  uitvoert, zorg ervoor dat u de volgende nieuwe gastheren van AWS voegt op lijst van gewenste personen. De bestaande hosts worden op 30 juni 2024 buiten bedrijf gesteld. Om een vlotte overgang te verzekeren, lijst van gewenste personen alle negen adressen. Er is geen urgentie om de bestaande adressen te verwijderen.

[!DNL Target] [!UICONTROL Recommendations] De activiteiten gebruiken de volgende gastheren van AWS wanneer het toegang tot de servers van FTP van klanten:

**Nieuwe hosts**:

| Locatie | Host |
| --- | --- |
| Oregon | `52.40.124.129` |
| Oregon | `54.148.219.69` |
| Oregon | `54.189.208.212` |
| Oregon | `44.230.236.35` |
| Oregon | `54.190.78.243` |
| Oregon | `52.41.73.133` |

**Bestaande hosts**:

| Locatie | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] API&#39;s gebruiken ook dezelfde AWS-hosts.
