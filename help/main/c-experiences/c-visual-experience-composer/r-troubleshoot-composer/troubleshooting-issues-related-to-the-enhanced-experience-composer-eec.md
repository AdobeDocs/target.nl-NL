---
keywords: gericht;ec;visuele ervaringscomposer;problemen oplossen verbeterde ervaringscomposer;het oplossen van problemen
description: Leer hoe te om problemen op te lossen die soms in de Adobe voorkomen [!DNL Target] Enhanced Experience Composer (EEC) onder bepaalde voorwaarden.
title: Hoe los ik problemen op met betrekking tot de Enhanced Experience Composer?
feature: Visual Experience Composer (VEC)
exl-id: 7dea7707-5d9f-49c4-9ccd-618eeb7b3568
source-git-commit: cb16350389e1504c88f1cf97aeda243e1300b65e
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Problemen met het oplossen van problemen in verband met de [!UICONTROL Enhanced Experience Composer]

Er kunnen weergaveproblemen optreden in het dialoogvenster [!DNL Adobe Target] [!UICONTROL Enhanced Experience Composer] (EEG) onder bepaalde voorwaarden.

## De EEC laadt geen interne QA URL die niet toegankelijk is op openbare IP. {#section_D29E96911D5C401889B5EACE267F13CF}

Dit kan worden opgelost door de volgende IP adressen te voegend op lijst van gewenste personen. Deze IP adressen zijn voor de server van de Adobe die voor de EEG volmacht wordt gebruikt. Ze zijn alleen vereist voor het bewerken van activiteiten. Bezoekers van uw site hebben deze op de lijst met gewenste personen staan IP-adressen niet nodig.

Vraag uw team van IT om de volgende IP adressen te lijsten van gewenste personen:

* 99 80 139 221
* 54 78 56 224
* 54 247 179 246
* 54 80 219 243
* 34.201.235,54
* 54 196 224 236
* 35.75.212,45
* 52 199 184 130
* 18 180 161 176

U ziet mogelijk het volgende foutbericht in [!DNL Target]:

`Error: Your website domain (ISP) is blocking the [!UICONTROL Enhanced Experience Composer]. You can allowlist the [!UICONTROL Enhanced Experience Composer]'s IP addresses or turn off [!UICONTROL Enhanced Experience Composer] in [!UICONTROL Configure] > [!UICONTROL Page Delivery] menu.`

![EEC_error-afbeelding](assets/EEC_error.png)

Hieronder ziet u mogelijk een foutbericht en oplossingen voor het verhelpen van de situatie:

* **Probleem:** Uw websitedomein (ISP) blokkeert het [!UICONTROL Enhanced Experience Composer].

  **Oplossing:** Lijst van gewenste personen de IP hierboven vermelde adressen.

* **Probleem:** De IP-adressen worden op de lijst met gewenste personen staan, maar uw website biedt geen ondersteuning voor TLS versie 1.2. [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór de [!DNL Target] 18.4.1 (25 april 2018), de standaardconfiguratie ondersteunde TLS 1.0. Zie voor meer informatie [De Veranderingen van de Encryptie van TLS (de Veiligheid van de Laag van het Vervoer)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

  **Oplossing:** Zie de volgende vraag [!UICONTROL Enhanced Visual Experience Composer] niet laden op beveiligde pagina&#39;s op mijn site die TLS 1.2 gebruiken.

## De EEG wordt niet geladen op beveiligde pagina&#39;s op mijn site die TLS 1.0 gebruiken. (alleen EEG) {#section_C5B31E3D32A844F68E5A8153BD17551F}

U ziet mogelijk het hierboven beschreven foutbericht in &quot;The [!UICONTROL Enhanced Visual Experience Composer] niet laden op beveiligde pagina&#39;s op mijn site.&quot; als de bovenstaande IP-adressen zijn gevoegd op lijst van gewenste personen, maar uw website biedt geen ondersteuning voor TLS versie 1.2. [!DNL Target] gebruikt momenteel de standaardconfiguratie van 1.2. Vóór de [!DNL Target] 18.4.1 (25 april 2018), de standaardconfiguratie ondersteunde TLS 1.0. Zie voor meer informatie [De Veranderingen van de Encryptie van TLS (de Veiligheid van de Laag van het Vervoer)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank}.

Als u de TLS-versie op uw website wilt controleren met Firefox (andere browsers hebben vergelijkbare stappen):

1. Open de desbetreffende website in Firefox.
1. Klik op de knop **[!UICONTROL Show Site Information]** op de adresbalk van de browser.

   ![firefox_more_info image](assets/firefox_more_info.png)

1. Klikken **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![afbeelding firefox_more_info_2](assets/firefox_more_info_2.png)

1. Bekijk de TLS-versiegegevens onder Technische details:

   ![firefox_more_info_3 afbeelding](assets/firefox_more_info_3.png)

1. Als u ziet dat op uw website TLS 1.0 wordt weergegeven, raadpleegt u [De Veranderingen van de Encryptie van TLS (de Veiligheid van de Laag van het Vervoer)](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/tls-transport-layer-security-encryption.html){target=_blank} for information about Target's TLS support policy. To remedy the situation for now (valid until September 12, 2018){target=_blank}, bereik [Klantenservice](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) voor configuratie met uw versie van TLS en het domein.

## Ik zie onderbrekingen of &quot;ontkende toegang&quot;fouten wanneer het laden van plaatsen met toegelaten volmacht. (alleen EEG) {#section_60CBB9022DC449F593606C0E6252302D}

Zorg ervoor volmacht IPs niet in uw milieu wordt geblokkeerd.
