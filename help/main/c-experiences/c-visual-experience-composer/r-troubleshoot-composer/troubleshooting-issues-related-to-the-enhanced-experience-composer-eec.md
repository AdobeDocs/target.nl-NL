---
keywords: gericht;ec;visuele ervaringscomposer;problemen oplossen verbeterde ervaringscomposer;het oplossen van problemen
description: Leer hoe te om problemen op te lossen die soms in de Adobe voorkomen [!DNL Target] Enhanced Experience Composer (EEC) onder bepaalde voorwaarden.
title: Hoe los ik problemen op met betrekking tot de Enhanced Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 2%

---

# Problemen met de [!UICONTROL Enhanced Experience Composer]

Er kunnen weergaveproblemen optreden in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEG) onder bepaalde voorwaarden.

## De EEC laadt geen interne QA URL die niet toegankelijk is op openbare IP. {#section_D29E96911D5C401889B5EACE267F13CF}

Dit kan worden opgelost door de volgende IP adressen te voegend op lijst van gewenste personen. Deze IP adressen zijn voor Adobe die voor de EEG volmacht wordt gebruikt. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze op de lijst met gewenste personen staan IP-adressen niet nodig.

Vraag uw team van IT om de volgende IP adressen te lijsten van gewenste personen:

* 34 253 100 20
* 34 248 100,23
* 52 49 228 246
* 54.205.42.123
* 107 22 177 39
* 52.201.5.105
* 52 193 211 177
* 18 180 24 249
* 52 194 154 154

U ziet mogelijk het volgende foutbericht in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Hieronder ziet u mogelijk een foutbericht en oplossingen voor het verhelpen van de situatie:

* **Probleem:** Uw websitedomein (ISP) blokkeert het [!UICONTROL Enhanced Experience Composer].

   **Oplossing:** Lijst van gewenste personen de IP hierboven vermelde adressen.

* **Probleem:** De IP-adressen worden op de lijst met gewenste personen staan, maar uw website biedt geen ondersteuning voor TLS versie 1.2. [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór de [!DNL Target] 18.4.1 (25 april 2018), de standaardconfiguratie ondersteunde TLS 1.0. Zie voor meer informatie [Wijzigingen in TLS-codering (Transport Layer Security)](/help/main/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

   **Oplossing:** Zie de volgende vraag [!UICONTROL Enhanced Visual Experience Composer] niet laden op beveiligde pagina&#39;s op mijn site die TLS 1.2 gebruiken.

## De EEG wordt niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.0 gebruiken. (alleen EEG) {#section_C5B31E3D32A844F68E5A8153BD17551F}

U ziet mogelijk het hierboven beschreven foutbericht in &quot;The [!UICONTROL Enhanced Visual Experience Composer] niet laden op beveiligde pagina&#39;s op mijn site.&quot; als de bovenstaande IP-adressen zijn gevoegd op lijst van gewenste personen, maar uw website biedt geen ondersteuning voor TLS versie 1.2. [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór de [!DNL Target] 18.4.1 (25 april 2018), de standaardconfiguratie ondersteunde TLS 1.0. Zie voor meer informatie [Wijzigingen in TLS-codering (Transport Layer Security)](/help/main/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

Als u de TLS-versie op uw website wilt controleren met Firefox (andere browsers hebben vergelijkbare stappen):

1. Open de desbetreffende website in Firefox.
1. Klik op de knop **[!UICONTROL Show Site Information]** op de adresbalk van de browser.

   ![](assets/firefox_more_info.png)

1. Klik op **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![](assets/firefox_more_info_2.png)

1. Bekijk de TLS-versiegegevens onder Technische details:

   ![](assets/firefox_more_info_3.png)

1. Als u ziet dat op uw website TLS 1.0 wordt weergegeven, raadpleegt u [Wijzigingen in TLS-codering (Transport Layer Security)](/help/main/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) voor informatie over het TLS-ondersteuningsbeleid van Target. Om de situatie voor nu te verhelpen (geldig tot 12 september 2018), moet u [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor configuratie met uw versie van TLS en het domein.

## Ik zie onderbrekingen of &quot;ontkende toegang&quot;fouten wanneer het laden van plaatsen met toegelaten volmacht. (alleen EEG) {#section_60CBB9022DC449F593606C0E6252302D}

Zorg ervoor volmacht IPs niet in uw milieu wordt geblokkeerd.
