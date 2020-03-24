---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure
description: Sommige browsers blokkeren de weergave van een pagina als beveiligde inhoud wordt gemengd met onveilige inhoud.
title: Gemengde inhoud in uw browser inschakelen
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
translation-type: tm+mt
source-git-commit: 6542eb14daf7f9154fe33a4e4cfdb2bb35f4d44c

---


# Gemengde inhoud in uw browser inschakelen{#enabling-mixed-content-in-your-browser}

Sommige browsers blokkeren de weergave van een pagina als beveiligde inhoud wordt gemengd met onveilige inhoud.

Als Visual Experience Composer (VEC) probeert om een pagina te openen die gemengde (veilige en onveilige) inhoud bevat, toont een bericht dat toont hoe te om het blokkeren in uw browser onbruikbaar te maken zodat kunt u een plaats van HTTP openen of een plaats die gemengde vraag (HTTPS en HTTP) heeft.

![](assets/mixed_content_warning.gif)

Eerder, toen gemengde inhoud niet werd toegestaan, kon u sommige acties in Stap 1 van het drie-stap geleide werkschema nog uitvoeren wanneer het creëren van activiteiten. Doel blokkeert nu handelingen in stap 1. Wanneer dit bericht wordt weergegeven, moet u gemengde inhoud inschakelen voordat u verdergaat.

De beveiligingsinstellingen van uw browser kunnen voorkomen dat gemengde inhoud of onveilige (HTTP-) inhoud wordt geladen in een beveiligde (HTTPS-) pagina of frame (zoals de VEC). Als u de beveiligingsinstellingen van uw browser niet wilt uitschakelen, hebt u een HTTPS-website nodig.

Als uw website op een onbeveiligd (HTTP) domein loopt, moet u VEC toestaan om actieve gemengde inhoud te laden.

>[!NOTE]
>
>Het toestaan van gemengde inhoud beïnvloedt slechts VEC en niet uw levende website.

Zie [Gemengde inhoud](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) op de website *Mozilla Developer Network* (MDN) voor meer informatie.

## Gemengde inhoud inschakelen in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

Als u een site bezoekt via een beveiligde verbinding, controleert Google Chrome of de inhoud op de webpagina veilig is verzonden.

Zie [Deze pagina bevat onveilige inhoud](https://support.google.com/chrome/answer/1342714?hl=en) in de Help van Google Chrome.

### Trainingsvideo: De VEC inschakelen in Chrome versie 79.0.3945.117 of hoger (jan. 2020) - ![overzichtsbadge](/help/assets/overview.png)

Als u de VEC gebruikt met de nieuwste versie van Chrome (versie 79.0.3945.117 of hoger), moet u de site-instellingen bijwerken. Bezoekers van uw site hoeven deze stappen niet uit te voeren.

>[!VIDEO](https://www.youtube.com/v=6zGCi5Y8eVo)

In de bovenstaande video worden de vereiste stappen beschreven:

1. Klik op het pictogram Vergrendelen of Voorzichtigheid en klik vervolgens op Site-instellingen.

   ![Site-instellingen](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Blader naar onveilige inhoud en gebruik vervolgens de vervolgkeuzelijst om Blok (standaard) te wijzigen in Toestaan.

   ![Onveilige inhoud](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Laad de VEC-pagina opnieuw.

## Gemengde inhoud inschakelen in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

Standaard blokkeert Firebox pagina&#39;s die beveiligde en onveilige inhoud mengen. U wordt aangeraden deze instelling permanent te wijzigen in gebruik [!DNL Target].

1. Typ in Firefox `about:config` de adresbalk.
1. Bevestig het waarschuwingsbericht dat door Firefox wordt weergegeven.
1. Typ in de zoekbalk `block_active`.
1. Dubbelklik ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   De waarde verandert van &quot;Waar&quot; in &quot;Onwaar&quot;. Wanneer de waarde &quot;False&quot; weergeeft, bent u klaar.  Nadat u deze instelling hebt gewijzigd, kunt u de computer het beste opnieuw opstarten.

## Gemengde inhoud inschakelen in Microsoft Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}

Internet Explorer blokkeert standaard pagina&#39;s die beveiligde en onveilige inhoud mengen. U wordt aangeraden deze instelling permanent te wijzigen om Target te gebruiken.

1. Klik in Internet Explorer op het pictogram Instellingen > **[!UICONTROL Internetopties]**.
1. Open het tabblad [!UICONTROL Beveiliging] .
1. Selecteer **[!UICONTROL Internet]** en klik vervolgens op **[!UICONTROL Aangepast niveau]**.
1. Selecteer **[!UICONTROL Diversen]**.
1. Schakel onder [!UICONTROL Diversen]de optie **[!UICONTROL Gemengde inhoud]** weergeven in.
1. Klik op **[!UICONTROL OK]** > **[!UICONTROL Ja]** > **[!UICONTROL Toepassen]**.

We raden u aan de computer opnieuw op te starten nadat u deze instelling hebt gewijzigd.

