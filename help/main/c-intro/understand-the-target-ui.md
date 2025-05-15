---
keywords: doelgebruikersinterface;gebruikersinterface;ui;aankondigingen;gebeurtenissen;meldingen
description: Verken me met het gebruikersinterface en vind verbindingen aan meer diepgaande informatie om u te helpen het meeste uit  [!DNL Target] krijgen.
title: Hoe gebruik ik  [!DNL Target]  UI?
feature: Overview
exl-id: ce4c72b2-b635-406b-9830-650816445a64
source-git-commit: 84f2e590ee9fb984a3b272240b0373072057ca32
workflow-type: tm+mt
source-wordcount: '1387'
ht-degree: 0%

---

# De gebruikersinterface van [!DNL Target] begrijpen

De gebruikersinterface is geschikt in een logische en gebruikersvriendelijke indeling, zodat u optimaal kunt profiteren van [!DNL Adobe Target] . Het volgende korte overzicht helpt u vertrouwd te worden gemaakt met [!DNL Target] en biedt koppelingen voor meer uitgebreide informatie en stapsgewijze instructies.

## [!DNL Target] UI-koptekst

De koptekst boven aan de gebruikersinterface van [!DNL Target] bevat tabbladen en opties waarmee u door de verschillende mogelijkheden van de oplossing kunt navigeren. U kunt ook naar een andere organisatie en [!DNL Adobe Experience Cloud] -oplossing gaan, feedback geven als u deel uitmaakt van een Beta-programma, toegang krijgen tot AI Assistant, hulp en meldingen ontvangen, uw [!DNL Adobe] -profiel beheren en zich afmelden bij [!DNL Target] .

![ kopbal van het Doel ](/help/main/c-intro/assets/target-header.png)

Met de tabbladen aan de linkerkant hebt u toegang tot de verschillende mogelijkheden van [!DNL Target], die later wordt besproken. Laten we eerst de opties aan de rechterkant bespreken voordat we de tabbladen bespreken.

### [!UICONTROL Organization]

Een *organisatie* is de entiteit die een beheerder toelaat om groepen en gebruikers te vormen, en enige sign-on in te controleren [!DNL Adobe Experience Cloud]. De organisatie werkt als een aanmeldingsbedrijf dat alle [!DNL Experience Cloud] -producten en -oplossingen omvat. Meestal is een organisatie uw bedrijfsnaam. Een bedrijf kan echter veel organisaties hebben.

Selecteer de gewenste organisatie in de vervolgkeuzelijst [!UICONTROL Organization] als uw bedrijf meerdere organisaties heeft:

![ drop-down lijst van de Organisatie ](/help/main/c-intro/assets/organizations.png)

### [!UICONTROL Beta Feedback]

(Voorwaardelijk) Als u deel uitmaakt van een officieel [!DNL Target] Beta-programma, wordt mogelijk het pictogram [!UICONTROL Beta Feedback] weergegeven.

![ het pictogram van de Terugkoppeling van Beta ](/help/main/c-intro/assets/beta-feedback.png)

Geef een beschrijving voor uw feedback, neem desgewenst bestanden of schermafbeeldingen op en klik op **[!UICONTROL Submit]** .

### [!DNL AI Assistant]

(Voorwaardelijk) Als aan uw bedrijf rechten zijn verleend om [!DNL AI Assistant] te gebruiken, klikt u op het pictogram [!DNL AI Assistant] .

Voor meer informatie, zie [ de Medewerkingsoverzicht van Adobe Experience Platform AI ](/help/main/c-intro/ai-assistant.md).

### Help

Het klikken van het [!UICONTROL Help] pictogram ( ![ pictogram van de Hulp ](/help/main/assets/icons/HelpOutline.svg) ) laat u tot informatie, video&#39;s, blogs, en meer toegang hebben om u te helpen [!DNL Target] effectiever gebruiken. U kunt een ondersteuningsticket maken, telefoonnummers voor ondersteuning zoeken, vragen stellen via Twitter of feedback geven over [!DNL Target] om ons te laten weten hoe het [!DNL Target] -team werkt.

![ Hulp ](/help/main/c-intro/assets/help.png)

### Verzoeken, meldingen en aankondigingen {#notifications-announcements}

Met de deelvensters [!UICONTROL Requests] , [!UICONTROL Notifications] en [!UICONTROL Announcements] kunt u alles op de hoogte houden [!DNL Adobe Target] . Via proactieve meldingen kunt u op de hoogte blijven van de status van [!DNL Adobe Experience Cloud] -oplossingen en [!DNL Target] -gebeurtenissen. Proactieve aankondigingen waarschuwen u aan outage gebeurtenissen en onderhoudsgebeurtenissen.

Klik het [!UICONTROL Notifications] pictogram ( ![ pictogram van Meldingen ](/help/main/assets/icons/Bell.svg)) van de kopbal aan meningsberichten:

Het deelvenster bevat tabbladen voor [!UICONTROL Requests] , [!UICONTROL Notifications] en [!UICONTROL Announcements] .

![ Meldingen ](assets/notifications.png)

De volgende secties bevatten informatie over elk lusje, en hoe te om berichten en aankondigingen te vormen:

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

U kunt afzonderlijke meldingen markeren als gelezen door de muisaanwijzer op de gewenste melding te plaatsen en vervolgens op het vinkje te klikken. U kunt alle meldingen als gelezen markeren of alle meldingen weergeven door op [!UICONTROL "Mark as Read"] of [!UICONTROL "View All"] onder in het deelvenster te klikken.

U kunt een herinnering ook plaatsen om opnieuw op de hoogte te worden gebracht door over een bericht te hangen, het &quot;[!UICONTROL Remind me]&quot;pictogram te klikken, dan te selecteren wanneer u wilt worden op de hoogte gebracht: 5 minuten, 15 minuten, één uur, of morgen.

#### Aankondigingen

Proactieve aankondigingen waarschuwen u aan outage gebeurtenissen en onderhoudsgebeurtenissen.

Meer diepgaande informatie kan op de [ de Status van Adobe ](https://status.adobe.com/) pagina worden gevonden.

### Meldingen en aankondigingen configureren

Je berichtgevingsvoorkeuren bewerken:

1. Klik op het tandwielpictogram en klik vervolgens op **[!UICONTROL Notifications]** .
1. Klik onder **[!UICONTROL Target]** op **[!UICONTROL Customize]** .
1. Selecteer of deselecteer de categorieën waarvoor u meldingen wilt ontvangen:

   * Verzoeken: wanneer iemand u een verzoek stuurt om een object goed te keuren of om toegang tot een object te verlenen. Je kunt je abonnement op deze rubriek niet opzeggen.
   * Toegewezen aan mij: wanneer iemand een object aan u toewijst.
   * Opmerkingen: wanneer iemand u in een opmerking noemt.
   * Nieuwe releases: wanneer een nieuwe release beschikbaar is voor een product of een service waartoe u toegang hebt.
   * Gedeeld met mij: Wanneer iemand een object met jou deelt.
   * Updates over inhoud: wanneer iemand een object bewerkt, verwijdert of opmerkingen maakt die u hebt gemaakt of volgt.
   * Overige:

   >[!NOTE]
   >
   >De &quot;Nieuwe versies&quot;en &quot;Updates op inhoud&quot;zijn de enige berichtcategorieën die op [!DNL Target] van toepassing zijn. De andere categorieën gelden voor andere Adobe-oplossingen.

1. Selecteer de categorieën die u als hoge prioriteit wilt worden beschouwd.
1. Selecteer de meldingen waarvoor u waarschuwingen wilt weergeven in uw browser.

   Deze waarschuwingen worden een paar seconden in de rechterbovenhoek van uw browser weergegeven. U kunt kiezen of u categorieën met hoge prioriteit, alle categorieën of alle pop-ups met meldingen wilt verbergen. U kunt ook configureren als u wilt dat de meldingen zichtbaar blijven totdat u ze sluit of u kunt de meldingsduur configureren.

1. Selecteer de frequentie waarop u e-mailberichten wilt ontvangen:

   * Geen e-mails verzenden
   * Directe meldingen
   * Dagelijks overzicht
   * Wekelijks overzicht

### Apps-schakeloptie

Met de schakeloptie Apps hebt u snel toegang tot de [!DNL Adobe Experience Cloud] -oplossingen die u kunt gebruiken.

![ Apps schakelaar ](/help/main/c-intro/assets/apps.png)

### Profiel

Klik op de profielavatar om uw [!DNL Adobe Experience Cloud] -voorkeuren te bewerken of om u af te melden bij [!DNL Target] . U kunt ook uw [!DNL Adobe] -profiel openen of bewerken.

![ avatar van het Profiel ](/help/main/c-intro/assets/change-language.png)

Nu bespreken de lusjes langs de linkerkant van de [!DNL Target] kopbal.

## Activiteiten

De lijst **[!UICONTROL Activities]** is de standaardweergave wanneer u [!DNL Target] opent. U kunt activiteiten maken op deze pagina en bestaande activiteiten beheren.

![ lijst van Activiteiten ](/help/main/c-intro/assets/activities-list.png)

Zie [ Activiteiten ](/help/main/c-activities/activities.md) voor diepgaande informatie over de activiteitentypes beschikbaar in [!DNL Target] en meer over het [!UICONTROL Activity] gebruikersinterface van de lijst te leren.

## Soorten publiek

Klik op het tabblad **[!UICONTROL Audiences]** om de lijst met [!UICONTROL Audiences] weer te geven waarin u een publiek kunt maken en bestaande soorten publiek kunt beheren.

![ lijst van het publiek ](/help/main/c-intro/assets/audience-list.png)

Een publiek is een groep van gelijkaardige activiteitendeelnemers die een gerichte activiteit zien. Een publiek is een groep mensen met dezelfde kenmerken, zoals een nieuwe bezoeker, een terugkerende bezoeker of terugkerende bezoekers uit het Midwesten. Met de functie [!UICONTROL Audience] kunt u verschillende inhoud en ervaringen toewijzen aan specifieke doelgroepen om uw digitale marketing te optimaliseren door de juiste berichten aan de juiste mensen op het juiste moment weer te geven. Als een bezoeker wordt geïdentificeerd als onderdeel van een doelpubliek, bepaalt [!DNL Target] welke ervaring moet worden weergegeven op basis van criteria die zijn gedefinieerd tijdens het maken van activiteiten.

Zie [ publiek ](/help/main/c-target/c-audiences/create-audience.md) voor diepgaande informatie over de publiekstypes in [!DNL Target] creëren en meer over het [!UICONTROL Audience] gebruikersinterface van de lijst leren.

## Aanbiedingen

Klik op het tabblad **[!UICONTROL Offers]** om de [!UICONTROL Offers] -lijst weer te geven waarin u ervaringen en aanbiedingen kunt maken en bestaande ervaringen en aanbiedingen kunt beheren.

![ lijst van Aanbiedingen ](/help/main/c-intro/assets/offers.png)

Een ervaring kan een aanbieding, beeld, tekst, knoop, video, combinatie van deze diverse elementen op een pagina, een volledige Web-pagina, of een reeks pagina&#39;s zijn die misschien een aanschaftrechter of een andere logische opeenvolging van pagina&#39;s vormen. Het kan ook de reactie van een stemmedewerker, een manuscript van de klantendienst, of zelfs een gepersonaliseerd aroma van een drankenmachine zijn. U kunt ervaringen in [!DNL Target] -activiteiten testen of personaliseren.

Zie [ Aanbiedingen ](/help/main/c-experiences/c-manage-content/manage-content.md) voor diepgaande informatie over de aanbiedingstypes in [!DNL Target] en meer over het [!UICONTROL Offer] gebruikersinterface van de lijst leren.

## Aanbevelingen

Klik op de tab **[!UICONTROL Recommendations]** om [!DNL Target Recommendations] te openen.

>[!NOTE]
>
>De activiteiten van aanbevelingen zijn beschikbaar als deel van de [!DNL Target Premium] oplossing. Ze zijn niet beschikbaar in [!DNL Target Standard] zonder een [!DNL Target Premium] -licentie. Voor meer informatie, zie [ Target Premium ](/help/main/c-intro/intro.md#premium) in *Inleiding aan Doel*.

![ Aanbevelingen ](/help/main/c-intro/assets/recommendations.png)

[!UICONTROL Recommendations] -activiteiten geven automatisch producten of inhoud weer die voor uw klanten interessant kan zijn op basis van eerdere gebruikersactiviteiten of andere algoritmen. De aanbevelingen helpen klanten aan relevante punten leiden die zij anders niet zouden kunnen kennen.

Zie [ Aanbevelingen ](/help/main/c-recommendations/recommendations.md) voor diepgaande informatie over [!UICONTROL Recommendations] in [!DNL Target] en meer over het [!UICONTROL Recommendations] gebruikersinterface te leren.

## Administratie

Klik op de tab **[!UICONTROL Administration]** om de [!UICONTROL Administration] -pagina&#39;s te openen.

![ de pagina&#39;s van het Beleid ](/help/main/c-intro/assets/administration.png)

Met de [!UICONTROL Administration] -pagina&#39;s kunt u [!DNL Target] beheren, inclusief configuratie-instellingen voor de [!UICONTROL Visual Experience Composer] (VEC), rapportage, [!DNL Scene7] -configuratie, implementatie, hosts, omgevingen, responstokens en gebruikers.

Zie [ het overzicht van het Doel beheren ](/help/main/administrating-target/administrating-target.md) voor diepgaande informatie en meer over het gebruikersinterface te leren.
