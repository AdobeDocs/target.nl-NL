---
keywords: gericht;ec;visuele ervaringscomposer;problemen oplossen verbeterde ervaringscomposer;het oplossen van problemen
description: Leer hoe te om problemen problemen op te lossen die soms in Adobe [!DNL Target] Verbeterde Composer van de Ervaring (EEC) onder bepaalde voorwaarden voorkomen.
title: Hoe los ik problemen op met betrekking tot de Enhanced Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: b14c9bb4bc0363c77de084c7ae7110e73c5f2f13
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Problemen met de [!UICONTROL Enhanced Experience Composer] oplossen

Weergaveproblemen treden soms op in [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEC) onder bepaalde omstandigheden.

## De EEC laadt geen interne QA URL die niet toegankelijk is op openbare IP. {#section_D29E96911D5C401889B5EACE267F13CF}

Dit kan worden opgelost door de volgende IP adressen te voegend op lijst van gewenste personen. Deze IP adressen zijn voor Adobe die voor de EEG volmacht wordt gebruikt. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze op de lijst met gewenste personen staan IP-adressen niet nodig.

Vraag uw team van IT om de volgende IP adressen te lijsten van gewenste personen:

* 52 55 99 45
* 52.51.238.221
* 52 193 67,35

Het volgende foutbericht wordt mogelijk weergegeven in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![](assets/EEC_error.png)

Hieronder ziet u mogelijk een foutbericht en oplossingen voor het verhelpen van de situatie:

* **Probleem:** uw websitedomein (ISP) blokkeert de  [!UICONTROL Enhanced Experience Composer].

   **Oplossing:** Lijst van gewenste personen de IP hierboven vermelde adressen.

* **Probleem:** de IP-adressen worden op de lijst met gewenste personen staan, maar uw website biedt geen ondersteuning voor TLS versie 1.2.  [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór  [!DNL Target] 18.4.1 (25 april 2018) ondersteunde de standaardconfiguratie TLS 1.0. Voor meer informatie, zie de Veranderingen [ van de Encryptie van ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451)TLS (de Veiligheid van de Laag van het Vervoer).

   **Oplossing:** Zie de volgende vraag (De vraag wordt  [!UICONTROL Enhanced Visual Experience Composer] niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.2 gebruiken).

## De EEG wordt niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.0 gebruiken. (alleen EEG) {#section_C5B31E3D32A844F68E5A8153BD17551F}

Het bovenstaande foutbericht wordt mogelijk weergegeven in &quot;De [!UICONTROL Enhanced Visual Experience Composer] wordt niet geladen op beveiligde pagina&#39;s op mijn site.&quot; als de bovenstaande IP-adressen zijn gevoegd op lijst van gewenste personen, maar uw website biedt geen ondersteuning voor TLS versie 1.2. [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór [!DNL Target] 18.4.1 (25 april 2018), steunde de standaardconfiguratie TLS 1.0. Zie [TLS (Transport Layer Security) Encryption Changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) voor meer informatie.

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
