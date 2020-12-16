---
keywords: Targeting;eec;visual experience composer;troubleshoot enhanced experience composer;troubleshooting
description: Weergaveproblemen doen zich soms onder bepaalde omstandigheden voor in de Enhanced Experience Composer (EEC).
title: Problemen met de Enhanced Experience Composer oplossen
feature: vec
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# Problemen oplossen met betrekking tot de Enhanced Experience Composer{#troubleshooting-issues-related-to-the-enhanced-experience-composer}

Weergaveproblemen doen zich soms onder bepaalde omstandigheden voor in de Enhanced Experience Composer (EEC).

## De EEC laadt geen interne QA URL die niet toegankelijk is op openbare IP. (alleen EEG) {#section_D29E96911D5C401889B5EACE267F13CF}

Dit kan worden opgelost door de volgende IP adressen te toevoegend op lijst van gewenste personen. Deze IP-adressen worden gebruikt voor de Adobe die wordt gebruikt voor de proxy van de Enhanced Experience Composer. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze IP-adressen niet nodig die zijn toegevoegd op lijst van gewenste personen

Vraag uw team van IT om de volgende IP adressen te lijsten van gewenste personen:

| Regio | IP-adressen | Hostnamen |
|--- |--- |--- |
| Verenigde Staten | 52 55 99 45 | `us1-proxy.adobemc.com` |
| Europa, Midden-Oosten en Afrika (EMEA) | 52.51.238.221 | `emea1-proxy.adobemc.com` |
| Azië-Stille Oceaan (APAC) | 52 193 67,35 | `apac1-proxy.adobemc.com` |

Het volgende foutbericht wordt mogelijk weergegeven in Target:

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can allowlist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Hieronder ziet u mogelijk een foutbericht en oplossingen voor het verhelpen van de situatie:

* **Probleem:** uw websitedomein (ISP) blokkeert de Enhanced Experience Composer.

   **Oplossing:** Lijst van gewenste personen de IP hierboven vermelde adressen.

* **Probleem:** de IP-adressen worden op de lijst met gewenste personen staan, maar uw website biedt geen ondersteuning voor TLS versie 1.2. Het doel gebruikt momenteel de standaardconfiguratie van 1.2. Vóór Doel 18.4.1 (25 april 2018), steunde de standaardconfiguratie TLS 1.0. Voor meer informatie, zie de Veranderingen [ van de Encryptie van ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)TLS (de Veiligheid van de Laag van het Vervoer).

   **Oplossing:** Zie de volgende vraag (Verbeterde Visual Experience Composer zal niet laden op veilige pagina&#39;s op mijn plaats die TLS 1.2 gebruiken).

## De EEG wordt niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.0 gebruiken. (alleen EEG) {#section_C5B31E3D32A844F68E5A8153BD17551F}

U zou het hierboven beschreven foutenbericht in &quot;Verbeterde Visuele Composer van de Ervaring niet op veilige pagina&#39;s op mijn plaats kunnen zien laden.&quot; als de bovenstaande IP-adressen zijn toegevoegd op lijst van gewenste personen, maar uw website biedt geen ondersteuning voor TLS versie 1.2. Het doel gebruikt momenteel de standaardconfiguratie van 1.2. Vóór Doel 18.4.1 (25 april 2018), steunde de standaardconfiguratie TLS 1.0. Zie [TLS (Transport Layer Security) Encryption Changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) voor meer informatie.

Als u de TLS-versie op uw website wilt controleren met Firefox (andere browsers hebben vergelijkbare stappen):

1. Open de desbetreffende website in Firefox.
1. Klik op het pictogram **[!UICONTROL Show Site Information]** op de adresbalk van de browser.

   ![](assets/firefox_more_info.png)

1. Klik op **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![](assets/firefox_more_info_2.png)

1. Bekijk de TLS-versiegegevens onder Technische details:

   ![](assets/firefox_more_info_3.png)

1. Als u vindt dat uw website TLS 1.0 toont, zie [TLS (de Veiligheid van de Laag van het Vervoer) de Veranderingen van de Encryptie ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) voor informatie over het de steunbeleid van TLS van het Doel. Als u de situatie voorlopig wilt verhelpen (geldig tot 12 september 2018), bereikt u [Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor configuratie met uw TLS-versie en het domein.

## Ik zie onderbrekingen of &quot;ontkende toegang&quot;fouten wanneer het laden van plaatsen met toegelaten volmacht. (alleen EEG) {#section_60CBB9022DC449F593606C0E6252302D}

Zorg ervoor volmacht IPs niet in uw milieu wordt geblokkeerd.
