---
keywords: doelgebruikersinterface;gebruikersinterface;ui;aankondigingen;gebeurtenissen;meldingen
description: Verken me met het gebruikersinterface en vind verbindingen aan meer diepgaande informatie om u te helpen het meeste uit  [!DNL Target] krijgen.
title: Hoe gebruik ik  [!DNL Target]  UI?
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: 3f7c81654d4f7982acf166b314cc332822cc87a6
workflow-type: tm+mt
source-wordcount: '1355'
ht-degree: 0%

---

# De gebruikersinterface van [!DNL Target] begrijpen

De gebruikersinterface is geschikt in een logische en gebruikersvriendelijke indeling, zodat u optimaal kunt profiteren van [!DNL Adobe Target] . Het volgende korte overzicht helpt u vertrouwd te worden gemaakt met [!DNL Target] en biedt koppelingen voor meer uitgebreide informatie en stapsgewijze instructies.

{{updated-ui}}

## [!DNL Target] UI-koptekst

De koptekst boven aan de gebruikersinterface van [!DNL Target] bevat tabbladen en opties waarmee u door de verschillende mogelijkheden van de oplossing kunt navigeren. U kunt ook naar een andere organisatie en [!DNL Adobe Experience Cloud] -oplossing gaan, feedback geven als u deel uitmaakt van een Beta-programma, toegang krijgen tot AI Assistant, hulp en meldingen ontvangen, uw [!DNL Adobe] -profiel beheren en zich afmelden bij [!DNL Target] .

![&#x200B; kopbal van het Doel &#x200B;](/help/main/c-intro/assets/target-header.png)

Met de tabbladen aan de linkerkant hebt u toegang tot de verschillende mogelijkheden van [!DNL Target], die later wordt besproken. Laten we eerst de opties aan de rechterkant bespreken voordat we de tabbladen bespreken.

### [!UICONTROL Organization]

Een *organisatie* is de entiteit die een beheerder toelaat om groepen en gebruikers te vormen, en enige sign-on in te controleren [!DNL Adobe Experience Cloud]. De organisatie werkt als een aanmeldingsbedrijf dat alle [!DNL Experience Cloud] -producten en -oplossingen omvat. Meestal is een organisatie uw bedrijfsnaam. Een bedrijf kan echter veel organisaties hebben.

Selecteer de gewenste organisatie in de vervolgkeuzelijst [!UICONTROL Organization] als uw bedrijf meerdere organisaties heeft:

![&#x200B; drop-down lijst van de Organisatie &#x200B;](/help/main/c-intro/assets/organizations.png)

### [!UICONTROL Beta Feedback]

(Voorwaardelijk) Als u deel uitmaakt van een officieel [!DNL Target] Beta-programma, wordt mogelijk het pictogram [!UICONTROL Beta Feedback] weergegeven.

![&#x200B; het pictogram van de Terugkoppeling van Beta &#x200B;](/help/main/c-intro/assets/beta-feedback.png)

Geef een beschrijving voor uw feedback, neem desgewenst bestanden of schermafbeeldingen op en klik op **[!UICONTROL Submit]** .

### [!DNL AI Assistant]

(Voorwaardelijk) Als uw organisatie u de gebruiksrechten voor [!DNL AI Assistant] heeft verleend, klikt u op het pictogram [!DNL AI Assistant] .

Voor meer informatie, zie [&#x200B; de Medewerkingsoverzicht van Adobe Experience Platform AI &#x200B;](/help/main/c-intro/ai-assistant.md).

### Help

Het klikken van het [!UICONTROL Help] pictogram ( ![&#x200B; pictogram van de Hulp &#x200B;](/help/main/assets/icons/HelpOutline.svg) ) laat u tot informatie, video&#39;s, blogs, en meer toegang hebben om u te helpen [!DNL Target] effectiever gebruiken. U kunt een ondersteuningsticket maken, telefoonnummers voor ondersteuning zoeken, vragen stellen via Twitter of feedback geven over [!DNL Target] om ons te laten weten hoe het [!DNL Target] -team werkt.

![&#x200B; Hulp &#x200B;](/help/main/c-intro/assets/help.png)

### Verzoeken, meldingen en aankondigingen {#notifications-announcements}

Met de deelvensters [!UICONTROL Requests] , [!UICONTROL Notifications] en [!UICONTROL Announcements] kunt u alles op de hoogte houden [!DNL Adobe Target] . Via proactieve meldingen kunt u op de hoogte blijven van de status van [!DNL Adobe Experience Cloud] -oplossingen en [!DNL Target] -gebeurtenissen. Proactieve aankondigingen waarschuwen u aan outage gebeurtenissen en onderhoudsgebeurtenissen.

Klik het [!UICONTROL Notifications] pictogram ( ![&#x200B; pictogram van Meldingen &#x200B;](/help/main/assets/icons/Bell.svg)) van de kopbal aan meningsberichten:

Het deelvenster bevat tabbladen voor [!UICONTROL Requests] , [!UICONTROL Notifications] en [!UICONTROL Announcements] .

![&#x200B; Meldingen &#x200B;](assets/notifications.png)

De volgende secties bevatten informatie over elk lusje, en hoe te om berichten en aankondigingen te vormen:

#### [!UICONTROL Requests]

Ontvang belangrijke informatie over [!DNL Adobe] producten en oplossingen, uw samenwerking met collega gebruikers, en andere relevante updates in het [!UICONTROL Requests] paneel.

Wanneer iemand u een verzoek stuurt om een object goed te keuren of toegang te verlenen tot een object, wordt dat verzoek weergegeven in het deelvenster [!UICONTROL Requests] .

#### Meldingen {#notifications}

[!DNL Target] -gebeurtenismeldingen bevatten het volgende:

* **Activiteiten**: Meldingen voor alle activiteitstypes wanneer een activiteit wordt goedgekeurd of, of manueel of wanneer het zijn begin of einddatum bereikt. Het bericht bevat de naam van de activiteit met een koppeling naar de overzichtspagina van de activiteit.

  Meldingen zijn configureerbaar en worden standaard ontvangen door productbeheerders, uitgevers en fiatteurs in de werkruimte van de activiteit voor [!DNL Target Premium] -accounts. Voor [!DNL Target Standard] -accounts worden meldingen ontvangen door alle uitgevers en fiatteurs.

  Meldingen worden als de volgende voorbeelden opgemaakt:

   * `Activity {target.activity.name} has been activated`

   * `Activity {target.activity.name} has been deactivated`

* **manuscripten van het Profiel**: Meldingen wanneer een profielmanuscript wordt geactiveerd of, of manueel of door [!DNL Target] gedeactiveerd.

  Meldingen kunnen worden geconfigureerd en worden standaard ontvangen door productbeheerders en fiatteurs voor zowel [!DNL Target Premium] - als [!DNL Target Standard] -accounts.

  Meldingen worden als de volgende voorbeelden opgemaakt:

   * `Profile Script {target.profileScript.name} has been activated`
   * `Profile Script {target.profileScript.name} has been deactivated`

* **het voer van Aanbevelingen**: Meldingen wanneer een [!DNL Recommendations] voer wordt geactiveerd of, of manueel of door [!DNL Target] gedeactiveerd. Meldingen worden ook verzonden wanneer een [!DNL Recommendations] -feed mislukt.

  Meldingen kunnen worden geconfigureerd en worden standaard ontvangen door productbeheerders en fiatteurs voor [!DNL Target Premium] -accounts. [!DNL Recommendations] is een [!DNL Target Premium] -functie en is niet beschikbaar in [!DNL Target Standard] .

  Meldingen worden als de volgende voorbeelden opgemaakt:

   * `Feed  {target.feed.name} has been activated`
   * `Feed {target.feed.name} has been deactivated`
   * `Feed {target.feed.name} has failed`
   * `Feed {target.feed.name} has failed to import from source`

U kunt individuele berichten zoals gelezen merken door over het gewenste bericht te hangen en dan het [!UICONTROL Mark as Read] ( ![&#x200B; Teken als Gelezen pictogram &#x200B;](/help/main/assets/icons/CheckmarkCircle.svg)) te klikken pictogram. U kunt alle meldingen als gelezen markeren of alle meldingen weergeven door op [!UICONTROL Mark as Read] of [!UICONTROL View All] onder in het deelvenster te klikken.

U kunt een herinnering ook plaatsen om opnieuw op de hoogte worden gebracht door over een bericht te hangen, klikkend [!UICONTROL Snooze] ( ![&#x200B; het pictogram van de Snoze &#x200B;](/help/main/assets/icons/Clock.svg)). U kunt vervolgens selecteren wanneer u een melding wilt ontvangen: 5 minuten, 15 minuten, 1 uur of morgen.

#### Aankondigingen

Proactieve aankondigingen waarschuwen u aan outage gebeurtenissen en onderhoudsgebeurtenissen.

Meer diepgaande informatie kan op de [&#x200B; de Status van Adobe &#x200B;](https://status.adobe.com/) pagina worden gevonden.

### Meldingen en aankondigingen configureren

Je berichtgevingsvoorkeuren bewerken:

1. Klik [!UICONTROL Edit Preferences] ( ![&#x200B; geef pictogram van Voorkeur &#x200B;](/help/main/assets/icons/Setting.svg) uit), dan klik **[!UICONTROL Notifications]** in het linkerspoor.
1. Selecteer onder **[!UICONTROL Target]** de manier waarop u een melding wilt ontvangen:

   * [!UICONTROL In-app]
   * [!UICONTROL Email]
   * [!DNL Slack]

1. Selecteer de categorieën die u als hoge prioriteit wilt worden beschouwd.

   >[!NOTE]
   >
   >&quot;[!UICONTROL New releases]&quot; en &quot;[!UICONTROL Updates on content]&quot; zijn de enige berichtcategorieën die van toepassing zijn op [!DNL Target] . De andere categorieën zijn van toepassing op andere [!DNL Adobe] oplossingen.

1. Selecteer de meldingen waarvoor u waarschuwingen wilt weergeven in uw browser.

   Deze waarschuwingen worden een paar seconden in de rechterbovenhoek van uw browser weergegeven. U kunt kiezen of u categorieën met hoge prioriteit, alle categorieën of alle pop-ups met meldingen wilt verbergen. U kunt ook configureren als u wilt dat de meldingen zichtbaar blijven totdat u ze sluit of u kunt de meldingsduur configureren.

1. Selecteer de frequentie waarop u e-mailberichten wilt ontvangen:

   * [!UICONTROL Don't send emails]
   * [!UICONTROL Instant notifications]
   * [!UICONTROL Daily digest]
   * [!UICONTROL Weekly digest]

1. Configureer Slack-meldingen voor een werkruimte.

### Apps-schakeloptie

Met de schakeloptie Apps hebt u snel toegang tot de [!DNL Adobe Experience Cloud] -oplossingen die u kunt gebruiken.

![&#x200B; Apps schakelaar &#x200B;](/help/main/c-intro/assets/apps.png)

### Profiel

Klik op de profielavatar om uw [!DNL Adobe Experience Cloud] -voorkeuren te bewerken of om u af te melden bij [!DNL Target] . U kunt ook uw [!DNL Adobe] -profiel openen of bewerken.

![&#x200B; avatar van het Profiel &#x200B;](/help/main/c-intro/assets/change-language.png)

Nu, bespreken de lusjes langs de linkerkant van de [!DNL Target] kopbal.

## Activiteiten

De lijst **[!UICONTROL Activities]** is de standaardweergave wanneer u [!DNL Target] opent. U kunt activiteiten maken op deze pagina en bestaande activiteiten beheren.

Zie [&#x200B; Activiteiten &#x200B;](/help/main/c-activities/activities.md) voor diepgaande informatie over de activiteitentypes beschikbaar in [!DNL Target] en meer over het [!UICONTROL Activity] gebruikersinterface van de lijst te leren.

## Soorten publiek

Klik op het tabblad **[!UICONTROL Audiences]** om de lijst met [!UICONTROL Audiences] weer te geven waarin u een publiek kunt maken en bestaande soorten publiek kunt beheren.

Een publiek is een groep van gelijkaardige activiteitendeelnemers die een gerichte activiteit zien. Een publiek is een groep mensen met dezelfde kenmerken, zoals een nieuwe bezoeker, een terugkerende bezoeker of terugkerende bezoekers uit het Midwesten. Met de functie [!UICONTROL Audience] kunt u verschillende inhoud en ervaringen toewijzen aan specifieke doelgroepen om uw digitale marketing te optimaliseren door de juiste berichten aan de juiste mensen op het juiste moment weer te geven. Als een bezoeker wordt geïdentificeerd als onderdeel van een doelpubliek, bepaalt [!DNL Target] welke ervaring moet worden weergegeven op basis van criteria die zijn gedefinieerd tijdens het maken van activiteiten.

Zie [&#x200B; publiek &#x200B;](/help/main/c-target/c-audiences/create-audience.md) voor diepgaande informatie over de publiekstypes in [!DNL Target] creëren en meer over het [!UICONTROL Audience] gebruikersinterface van de lijst leren.

## Aanbiedingen

Klik op het tabblad **[!UICONTROL Offers]** om de [!UICONTROL Offers] -lijst weer te geven waarin u ervaringen en aanbiedingen kunt maken en bestaande ervaringen en aanbiedingen kunt beheren.

Een ervaring kan een aanbieding, beeld, tekst, knoop, video, combinatie van deze diverse elementen op een pagina, een volledige Web-pagina, of een reeks pagina&#39;s zijn die misschien een aanschaftrechter of een andere logische opeenvolging van pagina&#39;s vormen. Het kan ook de reactie van een stemmedewerker, een manuscript van de klantendienst, of zelfs een gepersonaliseerd aroma van een drankenmachine zijn. U kunt ervaringen in [!DNL Target] -activiteiten testen of personaliseren.

Zie [&#x200B; Aanbiedingen &#x200B;](/help/main/c-experiences/c-manage-content/manage-content.md) voor diepgaande informatie over de aanbiedingstypes in [!DNL Target] en meer over het [!UICONTROL Offer] gebruikersinterface van de lijst leren.

## Aanbevelingen

Klik op de tab **[!UICONTROL Recommendations]** om [!DNL Target Recommendations] te openen.

>[!NOTE]
>
>[!UICONTROL Recommendations] -activiteiten zijn beschikbaar als onderdeel van de [!DNL Target Premium] -oplossing. [!UICONTROL Recommendations] -activiteiten zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie. Voor meer informatie, zie [&#x200B; Target Premium &#x200B;](/help/main/c-intro/intro.md#premium) in *Inleiding aan Doel*.

[!UICONTROL Recommendations] -activiteiten geven automatisch producten of inhoud weer die voor uw klanten interessant kan zijn op basis van eerdere gebruikersactiviteiten of andere algoritmen. De aanbevelingen helpen klanten aan relevante punten leiden die zij anders niet zouden kunnen kennen.

Zie [&#x200B; Aanbevelingen &#x200B;](/help/main/c-recommendations/recommendations.md) voor diepgaande informatie over [!UICONTROL Recommendations] in [!DNL Target] en meer over het [!UICONTROL Recommendations] gebruikersinterface te leren.

## Administratie

Klik op de tab **[!UICONTROL Administration]** om de [!UICONTROL Administration] -pagina&#39;s te openen.

Met de [!UICONTROL Administration] -pagina&#39;s kunt u [!DNL Target] beheren, inclusief configuratie-instellingen voor de [!UICONTROL Visual Experience Composer] -pagina (VEC), rapportage, [!DNL Scene7] -configuratie, implementatie, hosts, omgevingen, reactietokens, gebruikers en aanbevelingen.

Zie [&#x200B; het overzicht van het Doel beheren &#x200B;](/help/main/administrating-target/administrating-target.md) voor diepgaande informatie en meer over het gebruikersinterface te leren.

## Visual Experience Composer (VEC)

Naast [!DNL Target] UI, zou u met VEC UI vertrouwd moeten maken. Voor meer informatie, zie [[!DNL Visual Experience Composer]  opties &#x200B;](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).
