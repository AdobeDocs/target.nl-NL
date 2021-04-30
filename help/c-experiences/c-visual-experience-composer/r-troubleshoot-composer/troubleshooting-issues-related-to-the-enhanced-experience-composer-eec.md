---
keywords: gericht;ec;visuele ervaringscomposer;problemen oplossen verbeterde ervaringscomposer;het oplossen van problemen
description: Leer hoe te om problemen problemen op te lossen die soms in Adobe [!DNL Target] Verbeterde Composer van de Ervaring (EEC) onder bepaalde voorwaarden voorkomen.
title: Hoe los ik problemen op met betrekking tot de Enhanced Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
translation-type: tm+mt
source-git-commit: 28e21ea0b0e2306a54c9353ae57de7de5d94f564
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 1%

---

# Problemen met de Enhanced Experience Composer oplossen

Weergaveproblemen treden soms op in [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) onder bepaalde omstandigheden.

## De EEC laadt geen interne QA URL die niet toegankelijk is op openbare IP. (alleen EEG) {#section_D29E96911D5C401889B5EACE267F13CF}

Dit kan worden opgelost door de volgende IP adressen te voegend op lijst van gewenste personen. Deze IP-adressen worden gebruikt voor de Adobe die wordt gebruikt voor de proxy van de Enhanced Experience Composer. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze IP-adressen niet nodig die zijn gevoegd op lijst van gewenste personen

Vraag uw team van IT om de volgende IP adressen te lijsten van gewenste personen:

* 52 16 72 74
* 52.5.174,79
* 54 246 238,65
* 54 249 183 154
* 54 65 105 214
* 54 82 142 68

Het volgende foutbericht wordt mogelijk weergegeven in Target:

`Error: Your website domain (ISP) is blocking the Enhanced Experience Composer. You can allowlist the Enhanced Experience Composer's IP addresses or turn off Enhanced Experience Composer in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Hieronder ziet u mogelijk een foutbericht en oplossingen voor het verhelpen van de situatie:

* **Probleem:** uw websitedomein (ISP) blokkeert de Enhanced Experience Composer.

   **Oplossing:** Lijst van gewenste personen de IP hierboven vermelde adressen.

* **Probleem:** de IP-adressen worden op de lijst met gewenste personen staan, maar uw website biedt geen ondersteuning voor TLS versie 1.2. Het doel gebruikt momenteel de standaardconfiguratie van 1.2. Vóór Doel 18.4.1 (25 april 2018), steunde de standaardconfiguratie TLS 1.0. Voor meer informatie, zie de Veranderingen [ van de Encryptie van ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)TLS (de Veiligheid van de Laag van het Vervoer).

   **Oplossing:** Zie de volgende vraag (Verbeterde Visual Experience Composer zal niet laden op veilige pagina&#39;s op mijn plaats die TLS 1.2 gebruiken).

## De EEG wordt niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.0 gebruiken. (alleen EEG) {#section_C5B31E3D32A844F68E5A8153BD17551F}

U zou het hierboven beschreven foutenbericht in &quot;Verbeterde Visuele Composer van de Ervaring niet op veilige pagina&#39;s op mijn plaats kunnen zien laden.&quot; als de bovenstaande IP-adressen zijn gevoegd op lijst van gewenste personen, maar uw website biedt geen ondersteuning voor TLS versie 1.2. Het doel gebruikt momenteel de standaardconfiguratie van 1.2. Vóór Doel 18.4.1 (25 april 2018), steunde de standaardconfiguratie TLS 1.0. Zie [TLS (Transport Layer Security) Encryption Changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) voor meer informatie.

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
