---
keywords: IP-adres;IP-adressen;whitelist;lijst van gewenste personen;firewall;recs;feed;servers;adobe-marketingcloud;aanbevelingen
description: Bekijk een lijst van IP adressen die in  [!DNL Target]  worden gebruikt de input-verwerkende servers van Aanbevelingen om u te helpen uw firewall vormen om IP adressen uit de servers van Adobe toe te staan.
title: Welke IP Adressen gebruiken de aanbevelingen van servers van de diervoeder-Verwerking?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=nl-NL#premium newtab=true" tooltip="Kijk wat er in Target Premium is opgenomen."
feature: Recommendations
exl-id: a666cfc4-ed74-44e8-9ff5-212e4fd65c03
source-git-commit: be5b3158c758fa08802c1dc0541c9e989a2c7740
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# IP-adressen die worden gebruikt door [!DNL Recommendations] feed-processing-servers

Lijst met IP-adressen die in [!DNL Adobe Target] [!DNL Recommendations] feed-processing-servers worden gebruikt, zodat u uw firewall kunt configureren om IP-adressen van [!DNL Adobe] -servers toe te staan.

>[!IMPORTANT]
>
>Het team [!DNL Target] werkt momenteel de NAT-gatewayadressen bij voor het downloaden van [!DNL Recommendations] -feeds. Als u IP voegend op lijst van gewenste personen  uitvoert, zorg ervoor dat u de volgende nieuwe gastheren van AWS voegt op lijst van gewenste personen. De bestaande hosts worden op 30 juni 2024 buiten bedrijf gesteld. Om een vlotte overgang te verzekeren, lijst van gewenste personen alle negen adressen. Er is geen urgentie om de bestaande adressen te verwijderen.

[!DNL Target] [!UICONTROL Recommendations] -activiteiten maken gebruik van de volgende AWS-hosts bij het openen van FTP-servers van klanten:

**Nieuwe gastheren**:

| Locatie | Host |
| --- | --- |
| Oregon | `52.40.124.129` |
| Oregon | `54.148.219.69` |
| Oregon | `54.189.208.212` |
| Oregon | `44.230.236.35` |
| Oregon | `54.190.78.243` |
| Oregon | `52.41.73.133` |

**Bestaande gastheren**:

| Locatie | Host |
| --- | --- |
| Oregon | `44.241.237.28` |
| Oregon | `44.232.167.82` |
| Oregon | `52.41.252.205` |

[!DNL Target] [!UICONTROL Recommendations] API&#39;s gebruiken ook dezelfde AWS-hosts.
