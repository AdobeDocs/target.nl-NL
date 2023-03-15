---
keywords: IP-adres;IP-adressen;whitelist;lijst van gewenste personen;firewall;recs;feed;servers;adobe-marketingcloud;aanbevelingen
description: Een lijst weergeven met IP-adressen die worden gebruikt in [!DNL Target] Recommendations feed-processing servers helpen u bij het configureren van uw firewall om IP-adressen van Adobe-servers toe te staan.
title: Welke IP adressen gebruiken de servers van de het voederverwerking van Recommendations?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# IP-adressen die worden gebruikt door Recommendations-voederverwerkingsservers

Lijst met IP-adressen die worden gebruikt in [!DNL Adobe Target] [!DNL Recommendations] feed-processing-servers om u te helpen uw firewall configureren om IP-adressen van Adobe-servers toe te staan.

[!DNL Target] [!UICONTROL Recommendations] De activiteiten gebruiken de volgende gastheren van AWS wanneer het toegang tot de servers van FTP van klanten:

| Locatie | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] API&#39;s gebruiken ook dezelfde AWS-hosts.

>[!NOTE]
>
>Deze IP-adressen zijn voor het laatst bijgewerkt op 16 maart 2021. Eerder waren de servers die tot de servers van FTP toegang hadden in het 192.243.242.0/24 IP adresblok CIDR. De servers die als host fungeren voor Recommendations API&#39;s bevinden zich in het 192.243.224.0/20 IP-adresblok CIDR.
