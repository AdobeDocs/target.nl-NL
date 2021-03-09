---
keywords: implementeren;implementeren;whitelist;witte lijst;lijst van gewenste personen;lijst van gewenste personen;edge;edges
description: Bekijk een lijst van gastheren om u te helpen de randen van Adobe Target lijsten van gewenste personen (geografisch verdeelde het dienen knopen die optimale reactietijden eind - gebruikers verzekeren).
title: Hoe Voegt op lijst van gewenste personen ik de knopen van de Rand van het Doel?
feature: Privacy en beveiliging
role: Ontwikkelaar
translation-type: tm+mt
source-git-commit: 806c52e69cce636a56eb067759612f80829418f9
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 5%

---


# Lijst van gewenste personen randknooppunten doel

Informatie en een bijgewerkte lijst van gastheren om u te helpen [!DNL Adobe Target] randen lijsten van gewenste personen.

Een rand is een geografisch verspreide serverende architectuur die optimale reactietijden voor eindgebruikers verzekert die om inhoud verzoeken, ongeacht waar zij worden gevestigd. Elk Edge-knooppunt heeft alle informatie die nodig is om te reageren op de aanvraag van de inhoud van de gebruiker en om analysegegevens over die aanvraag bij te houden. Gebruikersverzoeken worden naar het dichtstbijzijnde randknooppunt gerouteerd. Zie [Het Edge-netwerk](/help/c-intro/how-target-works.md#concept_0AE2ED8E9DE64288A8B30FCBF1040934) in *Hoe werkt Adobe [!DNL Target]* voor meer informatie.

U kunt de randknooppunten [!DNL Target] desgewenst lijsten van gewenste personen.

## IP-adressen (NAT) van het netwerkadres van doelranden

Lijst met IP-adressen van egress-randen van [!DNL Target]. Lijst van gewenste personen deze IPs als u het bereik van het Doel aan uw diensten wilt hebben.

| Locatie rand | IP van de uitgang Adressen |
| --- | --- |
| Edge31 (Mumbai) | 13.126.131.246<br>13.234.229.8 |
| Edge32 (Tokio) | 3.115.154.28<br>3.115.227.146 |
| Edge34 (East Coast US) | 34.232.149.249<br>52.21.139.93 |
| Edge35 (West Coast US) | 52.10.11.139<br>44.231.171.161 |
| Edge36 (Sydney) | 13.237.227.20<br>13.210.93.142 |
| Edge37 (Ierland) | 54.72.21.68<br>52.208.139.19 |
| Edge38 (Singapore) | 18.141.132.96<br>54.179.187.167 |

## IP-adressen doelrand

Lijst van IP adressen van [!DNL Target] randen. Lijst van gewenste personen deze IPs als u API vraag aan de randen van het Doel wilt maken.

| Locatie rand | Domein | IP-adressen |
| --- | --- | --- |
|  | `CLIENTCODE.tt.omtrdc.net`<br>(waarbij CLIENTCODE uw  [!DNL Target] client-id is) |  |
| Edge31 (Mumbai) | `mboxedge31.tt.omtrdc.net` | 15.207.157.131<br>15.206.8.201 |
| Edge32 (Tokio) | `mboxedge32.tt.omtrdc.net` | 54.199.66.101<br>54.64.93.37 |
| Edge34 (East Coast US) | `mboxedge34.tt.omtrdc.net` | 3.225.56.36<br>3.230.207.249<br>34.198.55.51<br>52.3.14.12<br>52.21.22.9 3<br>52.55.235.132<br>52.70.52.52<br>54.165.204.89 |
| Edge35 (West Coast US) | `mboxedge35.tt.omtrdc.net` | 52.10.244.20<br>52.36.232.38<br>52.88.209.29<br>54.214.180.56<br>35.162.2 74.35<br>34.214.12.211<br>52.42.35.202<br>54.148.71.13 |
| Edge36 (Sydney) | `mboxedge36.tt.omtrdc.net` | 13.238.34.185<br>3.24.250.17<br>3.104.234.91<br>13.211.248.241 |
| Edge37 (Ierland) | `mboxedge37.tt.omtrdc.net` | 52.212.193.208<br>52.19.133.54<br>52.51.251.137<br>34.252.156.174<br>5 2.213.168.74<br>34.252.166.160<br>52.18.150.20<br>18.203.205.32 |
| Edge38 (Singapore) | `mboxedge38.tt.omtrdc.net` | 52.221.145.65<br>52.220.44.99<br>13.250.75.226<br>54.151.139.123 |





