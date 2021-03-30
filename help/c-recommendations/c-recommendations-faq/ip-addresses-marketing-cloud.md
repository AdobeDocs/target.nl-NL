---
keywords: IP-adres;IP-adressen;whitelist;lijst van gewenste personen;firewall;recs;feed;servers;adobe-marketingcloud;aanbevelingen
description: Bekijk een lijst van IP adressen die in de voer-verwerkingsservers van Recommendations van het Doel worden gebruikt om u te helpen uw firewall vormen om IP adressen uit de servers van Adobe toe te staan.
title: Welke IP adressen gebruiken de servers van de het voederverwerking van Recommendations?
feature: Recommendations
translation-type: tm+mt
source-git-commit: d90069169a23bc432c7731b3129ca7c9572f6cf4
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# ![PREMIUMIP-](/help/assets/premium.png) adressen die worden gebruikt door Recommendations-voederverwerkingsservers

Lijst met IP-adressen die worden gebruikt in [!DNL Adobe Target] [!DNL Recommendations] feed-processing-servers om u te helpen uw firewall te configureren om IP-adressen van Adobe-servers toe te staan.

[!DNL Target] [!UICONTROL Recommendations] De activiteiten gebruiken de volgende gastheren van AWS wanneer het toegang tot van klanten tot de servers van FTP:

| Locatie | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] API&#39;s gebruiken ook dezelfde AWS-hosts.

>[!NOTE]
>
>Deze IP-adressen zijn voor het laatst bijgewerkt op 16 maart 2021. Eerder waren de servers die tot de servers van FTP toegang hadden in het 192.243.242.0/24 IP adresblok CIDR. De servers die als host fungeren voor Recommendations API&#39;s bevinden zich in het 192.243.224.0/20 IP-adresblok CIDR.

