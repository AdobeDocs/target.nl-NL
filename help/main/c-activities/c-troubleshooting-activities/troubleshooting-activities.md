---
keywords: problemen oplossen doel;het oplossen van problemendoel;standaardinhoud;test niet live;activiteit niet live;het richten van niet werkt;de vorige ervaringsvertoningen;kan geen activiteiten tot stand brengen;kan activiteiten creëren;de paginastructuur veranderde;de paginastructuur veranderde;foutenmelding;fout schrapt profielmanuscript;ajax werkt niet
description: Vind het oplossen van problemensuggesties als uw Adobe  [!DNL Target]  activiteit niet op uw plaats verschijnt.
title: Hoe kan ik activiteiten problemen oplossen?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: f1cbc46323f71c2fa091cd2c9a3e49d34676e7a1
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Problemen met activiteiten oplossen

Als uw [!DNL Adobe Target] activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.

>[!NOTE]
>
>Naast de volgende het oplossen van problemeninformatie, zie [&#x200B; Doel van het Oplossen van problemen &#x200B;](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) voor verbindingen aan extra het oplossen van problemenonderwerpen, FAQs, en andere nuttige informatie over het oplossen van problemenactiviteiten en andere eigenschappen in [!DNL Adobe Target].

De volgende secties bevatten problemen die u met voorgestelde oplossingen zou kunnen ontmoeten.

## Ik heb een activiteit gemaakt met de gebruikersinterface van [!DNL Target] en ik kan deze niet bijwerken via de API.

Activiteiten die zijn gemaakt met de gebruikersinterface van [!DNL Target] , moeten worden bijgewerkt via de gebruikersinterface van [!DNL Target] . Activiteiten die via API zijn gemaakt, moeten via API worden bijgewerkt. Als u bijvoorbeeld oorspronkelijk een activiteit maakt met behulp van de API, maar de activiteit later bewerkt via de [!DNL Target] -interface, worden niet alle wijzigingen bijgewerkt. Alle wijzigingen worden opgeslagen op de achtergrond en kunnen worden bijgewerkt door een andere API-aanroep te maken.

Probeer de activiteit bij te werken met dezelfde methode (UI of API) die oorspronkelijk is gebruikt om de activiteit te maken.

## U ziet standaardinhoud.

Controleer of uw activiteit is voltooid en of deze is geactiveerd.

## De activiteit is niet actief.

**bevestigt:** ga naar [!UICONTROL Overview] lusje en zie of is de test duidelijk inactief of ontwerp.

**Opties:**

* Test activeren.
* Gebruik Koppelingen voorvertonen om de inactieve test weer te geven.

## U komt niet in aanmerking voor de doelgerichte voorwaarden voor het publiek.

**bevestigt:** Overzicht richtend voorwaarden op overzichtspagina.

**Opties:**

* Kwalificeren en opnieuw proberen.
* Gebruik Koppelingen voorvertonen om de doelvoorwaarden te omzeilen.

## De pagina komt niet in aanmerking voor de voorwaarden voor paginagerichting.

**bevestigt:** op de [!UICONTROL Overview] pagina, bepaal als de pagina buiten de het richten voorwaarden valt.

**Opties:**

* Ga naar [!UICONTROL Visual Experience Composer] en klik op URL > Geavanceerd > huidige pagina.

## In plaats van de nieuwe ervaring wordt een eerdere ervaring weergegeven.

**bevestigt:** probeer één van de opties hieronder en probeer om de ervaring opnieuw te bekijken.

**Opties:**

* Cachegeheugen en cookies wissen en probeer het opnieuw.
* Probeer een andere browser.
* Gebruik de modus Private/Incognito.

## U bent onlangs toegevoegd aan [!DNL Target] , maar u kunt geen activiteiten maken.

**Valideren:** klik [!UICONTROL Create Activity]. Als de optie niet beschikbaar is, hebt u hoogstwaarschijnlijk niet voldoende rechten gekregen om een activiteit tot stand te brengen.

**Opties:**

Nadat u als gebruiker in [!DNL Target] bent toegevoegd, moet u de [!UICONTROL Approver] rol hebben om activiteiten tot stand te brengen.

* Vraag de beheerder van uw account om van u een fiatteur te maken.
* Geef uzelf de [!UICONTROL Approver] rol van **[!UICONTROL Administration]** > **[!UICONTROL Users]** in [!DNL Target] als u de beheerder bent.

  Zie [&#x200B; u toewijzen de Approver Rol &#x200B;](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## De structuur van de pagina is gewijzigd sinds het instellen van de activiteit.

**Valideren:** ga naar [!UICONTROL Visual Experience Composer] voor de bestaande activiteit. Let op het waarschuwingsbericht dat de kiezers (of structuur) zijn gewijzigd.

**Opties:**

* Maak de activiteit opnieuw.

Voor meer informatie over hoe de paginawijzigingen [!DNL Target] capaciteit beïnvloeden om te tonen, zie [&#x200B; Scenario&#39;s van de Wijziging van de Pagina &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## De structuur van de pagina wordt gewijzigd tijdens het laden van de pagina (bij uitvoering).

**bevestigt:** Vraag ontwikkelaar.

**Nota:** opdat [!DNL Target] herkent waar de activiteitenveranderingen zouden moeten worden toegepast, vermijd dynamisch het opnemen van een element met de zelfde klasse of dynamisch het wijzigen van de klasse van om het even welke siblings.

**Opties:**

* Werk paginacode bij om elk element uniek te identificeren dat wordt getest (gebruikend identiteitskaart).
* Hiermee wordt gestopt met het dynamisch wijzigen van de klasse of op hetzelfde niveau als hierboven is beschreven.

Voor meer informatie over hoe de paginawijzigingen [!DNL Target] capaciteit beïnvloeden om te tonen, zie [&#x200B; Scenario&#39;s van de Wijziging van de Pagina &#x200B;](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Andere activiteiten worden uitgevoerd op dezelfde pagina.

**Valideren:** gebruik het [!UICONTROL Collisions] lusje om te zien of lopen andere activiteiten.

**Nota:** het [!UICONTROL Collisions] lusje werkt niet met de het Testen van het Malplaatje module.

**Opties:**

* Verhoog de prioriteit van deze activiteit.
* De prioriteit van andere activiteiten verlagen.
* Andere activiteiten deactiveren.

## Er verschijnt een foutbericht wanneer u een profielscript verwijdert.

**bevestigt:** het schrappen van een profielmanuscript van [!DNL Target] toont het foutenbericht, &quot;Slaagde er niet in om profielmanuscript te schrappen.&quot;

**Opties:**

Voer een van de volgende handelingen uit:

* Verwijder het profielscript opnieuw. De succesboodschap wordt weergegeven.
* Wacht ongeveer 10 minuten tot de importmodule [!DNL Target] is uitgevoerd. De importer werkt de lijst met profielscripts bij.

## Sommige ajax [!DNL Target] -aanroepen werken niet.

**Nota:** Veelvoudige ajax [!DNL Target] vraag met de zelfde naam maar de verschillende parameters werken niet op de zelfde pagina. Slechts wordt de eerste vraag gemaakt.

## U activeerde een activiteit met de [!DNL Target] API, maar de activiteit toont een status van [!UICONTROL Inactive] in [!DNL Target] UI.

Wanneer u bepaalde handelingen uitvoert, zoals het activeren van een activiteit buiten de gebruikersinterface met de API van [!DNL Target] , kan het tien minuten duren voordat de update naar de gebruikersinterface wordt doorgegeven.

## Na het omzetten van activiteiten heeft de bezoeker geen ervaring.

In zeldzame gevallen, als de metrisch van de omzetting van de activiteit om voor een ervaring in aanmerking te komen in het zelfde verzoek wordt verzonden zoals activiteitenkwalificatie, zou de bezoeker in geen enkele ervaring kunnen zijn nadat het verzoek wordt verzonden. In dit geval ziet de bezoeker de standaardinhoud- en ervarings-id die via tokens wordt vastgelegd, op -1. [!DNL Adobe] raadt het verzenden van activiteitkwalificatie en conversie in dezelfde [!DNL Target] -aanvraag niet aan.

Als u beide gegevens in dezelfde aanvraag wilt verzenden, kunt u met [!UICONTROL Advanced Settings] opgeven dat de bezoeker na de conversie in dezelfde ervaring blijft.
