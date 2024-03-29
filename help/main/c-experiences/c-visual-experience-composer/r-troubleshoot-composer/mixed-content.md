---
keywords: gemengde inhoud;veilig;onveilig;chroom;problemen;vec;visuele ervaringscomposer;onveilig;http;https;firefox;Internet Explorer
description: Leer hoe u gemengde inhoud inschakelt in [!DNL Chrome], [!DNL Firefox], en [!DNL Edge].
title: Hoe te om Gemengde Inhoud in Mijn Browser toe te laten
feature: Visual Experience Composer (VEC)
exl-id: a2209af6-65e5-427e-b2cb-53b803728ef3
source-git-commit: c5b43faa2fc55c2c8737e586cfdfaa1444a05880
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Gemengde inhoud in uw browser inschakelen

Gemengde inhoud komt voor als het aanvankelijke verzoek veilig over HTTPS is, maar HTTPS *en* HTTP-inhoud wordt geladen om de webpagina weer te geven. HTTPS-inhoud is beveiligd. HTTP-inhoud is onveilig.

Moderne browsers kunnen de weergave van een pagina blokkeren of waarschuwingsberichten weergeven als beveiligde inhoud wordt gemengd met onveilige inhoud.

Er verschijnt een waarschuwingsbericht als de [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] probeert een pagina met gemengde inhoud te openen. Dit bericht geeft aan hoe u blokkering in uw browser kunt uitschakelen. Als u het blokkeren uitschakelt, kunt u een HTTP-site of een site met gemengde inhoud (HTTPS en HTTP) openen.

![Waarschuwing gemengde inhoud](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/mixed_content_warning.png)

Eerder, toen gemengde inhoud niet werd toegestaan, kon u sommige acties in Stap 1 van het drie-stap geleide werkschema nog uitvoeren wanneer het creëren van activiteiten. [!DNL Target] blokkeert nu handelingen in stap 1. Wanneer dit bericht wordt weergegeven, moet u gemengde inhoud inschakelen voordat u verdergaat met het maken van de activiteit.

De beveiligingsinstellingen van uw browser kunnen voorkomen dat gemengde inhoud of onveilige (HTTP-) inhoud wordt geladen in een beveiligde (HTTPS-) pagina of frame (zoals de VEC). Als u de beveiligingsinstellingen van uw browser niet wilt uitschakelen, hebt u een HTTPS-website nodig.

Als uw website op een onbeveiligd (HTTP) domein loopt, moet u VEC toestaan om actieve gemengde inhoud te laden.

>[!IMPORTANT]
>
>Het toestaan van gemengde inhoud beïnvloedt slechts VEC en niet uw levende website.

Zie voor meer informatie [Gemengd](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) op de *Mozilla Developer Network* (MDN) website.

## Gemengde inhoud inschakelen in [!DNL Google Chrome] {#task_FF297A08F66E47A588C14FD67C037B3A}

Als u een site bezoekt via een veilige verbinding, [!DNL Chrome] controleert of de inhoud op de webpagina veilig is verzonden.

Zie &quot;[Waarschuwingen over onveilige sites beheren](https://support.google.com/chrome/answer/99020?hl=en)&quot; in Google Chrome Help.

Als u de VEC gebruikt met de meest recente versie van [!DNL Chrome] (versie 79.0.3945.117 of hoger), moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Klik op het pictogram Vergrendelen (voorzichtig) en klik vervolgens op **[!UICONTROL Site settings]**.

   ![Site-instellingen](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Schuiven naar **[!UICONTROL Insecure content]** en gebruikt u de vervolgkeuzelijst om &quot;Blok (standaard)&quot; te wijzigen in &quot;Toestaan&quot;.

   ![Onveilige inhoud](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laad de VEC-pagina opnieuw.

## Gemengde inhoud inschakelen in [!DNL Mozilla Firefox] {#task_5448763B8DC941FD80F84041AEF0A14D}

Standaard, [!DNL Firebox] blokkeert pagina&#39;s die veilige en onveilige inhoud mengen. Deze instelling moet u permanent wijzigen [!DNL Target]. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. Typ in Firefox `about:config` in de adresbalk.
1. Bevestig de waarschuwing die wordt weergegeven door [!DNL Firefox].

   ![Firefox-waarschuwing](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox.png)

1. Typ in de zoekbalk `block_active`.

   ![Firefox block_active setting](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox3.png)

1. Dubbelklikken ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   De waarde verandert van &quot;Waar&quot; in &quot;Onwaar&quot;. Wanneer de waarde &quot;False&quot; weergeeft, bent u klaar.

   ![Firefox-beveiliging](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/firefox2.png)

1. Start de computer opnieuw nadat u deze instelling hebt gewijzigd.

## Gemengde inhoud inschakelen in [!DNL Microsoft Edge]

Als u een site bezoekt via een veilige verbinding, [!DNL Edge] controleert of de inhoud op de webpagina veilig is verzonden.

Als u de VEC gebruikt met de meest recente versie van [!DNL Edge], moet u uw site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

1. In [!DNL Edge], klikt u op **[!DNL Microsoft Edge]** in de menubalk, **[!UICONTROL Settings]** en klik vervolgens op **Cookies en sitemachtigingen**.

1. Schuiven naar **[!UICONTROL Insecure content]**.

1. Klikken **[!UICONTROL Insecure content]** en klik vervolgens op **[!UICONTROL Add]** naast **[!UICONTROL Allow]** voegt u de site toe waarop onveilige inhoud is toegestaan en klikt u vervolgens op **[!UICONTROL Add]**.

1. Laad de VEC-pagina opnieuw.
