---
keywords: problemen oplossen doel;het oplossen van problemendoel;standaardinhoud;test niet live;activiteit niet live;het richten van niet werkt;de vorige ervaringsvertoningen;kan geen activiteiten tot stand brengen;kan activiteiten creëren;de paginastructuur veranderde;de paginastructuur veranderde;foutenmelding;fout schrapt profielmanuscript;ajax werkt niet
description: Vind het oplossen van problemensuggesties als uw Adobe [!DNL Target] activiteit wordt niet op uw site weergegeven.
title: Hoe kan ik activiteiten problemen oplossen?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: f1cbc46323f71c2fa091cd2c9a3e49d34676e7a1
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---

# Problemen met activiteiten oplossen

Als uw [!DNL Adobe Target] activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.

>[!NOTE]
>
>Naast de volgende het oplossen van problemeninformatie, zie [Probleemoplossing](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) voor verbindingen aan extra het oplossen van problemenonderwerpen, FAQs, en andere nuttige informatie over het oplossen van problemenactiviteiten en andere eigenschappen in [!DNL Adobe Target].

De volgende secties bevatten problemen die u met voorgestelde oplossingen zou kunnen ontmoeten.

## Ik heb een activiteit gemaakt met de [!DNL Target] UI en ik kunnen het niet via API bijwerken.

Met de [!DNL Target] De gebruikersinterface moet via de [!DNL Target] UI. Activiteiten die via API zijn gemaakt, moeten via API worden bijgewerkt. Als u bijvoorbeeld oorspronkelijk een activiteit maakt met behulp van de API, maar de activiteit later bewerkt via de [!DNL Target] UI, niet alle veranderingen worden bijgewerkt. Alle wijzigingen worden opgeslagen op de achtergrond en kunnen worden bijgewerkt door een andere API-aanroep te maken.

Probeer de activiteit bij te werken met dezelfde methode (UI of API) die oorspronkelijk is gebruikt om de activiteit te maken.

## U ziet standaardinhoud.

Controleer of uw activiteit is voltooid en of deze is geactiveerd.

## De activiteit is niet actief.

**Valideren:** Ga naar [!UICONTROL Overview] en controleer of de test inactief of concept is gemarkeerd.

**Opties:**

* Test activeren.
* Gebruik Koppelingen voorvertonen om de inactieve test weer te geven.

## U komt niet in aanmerking voor de doelgerichte voorwaarden voor het publiek.

**Valideren:** Doelvoorwaarden controleren op overzichtspagina.

**Opties:**

* Kwalificeren en opnieuw proberen.
* Gebruik Koppelingen voorvertonen om de doelvoorwaarden te omzeilen.

## De pagina komt niet in aanmerking voor de voorwaarden voor paginagerichting.

**Valideren:** Op de [!UICONTROL Overview] pagina, bepaalt u of de pagina buiten de doelvoorwaarden valt.

**Opties:**

* Ga naar de [!UICONTROL Visual Experience Composer], klikt u op URL > Geavanceerd > huidige pagina.

## In plaats van de nieuwe ervaring wordt een vorige ervaring weergegeven.

**Valideren:** Probeer een van de onderstaande opties en probeer de ervaring opnieuw weer te geven.

**Opties:**

* Wis cache en cookies en probeer het opnieuw.
* Probeer een andere browser.
* Gebruik de modus Private/Incognito.

## Je bent onlangs toegevoegd aan [!DNL Target] maar kan geen activiteiten creëren .

**Valideren:** Klikken [!UICONTROL Create Activity]. Als de optie niet beschikbaar is, hebt u hoogstwaarschijnlijk niet voldoende rechten gekregen om een activiteit tot stand te brengen.

**Opties:**

Nadat u als gebruiker hebt toegevoegd in [!DNL Target], hebt u de [!UICONTROL Approver] rol voor het creëren van activiteiten.

* Vraag de beheerder van uw account om van u een fiatteur te maken.
* Als u de Admin bent, geef dan uzelf de [!UICONTROL Approver] rol van **[!UICONTROL Administration]** > **[!UICONTROL Users]** in [!DNL Target].

   Zie [Wijs zelf de rol van fiatteur toe](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## De structuur van de pagina is gewijzigd sinds het instellen van de activiteit.

**Valideren:** Ga naar de [!UICONTROL Visual Experience Composer] voor de bestaande activiteit. Let op het waarschuwingsbericht dat de kiezers (of structuur) zijn gewijzigd.

**Opties:**

* Maak de activiteit opnieuw.

Voor meer informatie over de invloed van paginawijzigingen op [!DNL Target]Kan worden weergegeven, zie [Paginawijzigingsscenario&#39;s](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## De structuur van de pagina wordt gewijzigd tijdens het laden van de pagina (bij uitvoering).

**Valideren:** Vraag het de ontwikkelaar.

**Opmerking:** Om [!DNL Target] om te herkennen waar activiteitsveranderingen zouden moeten worden toegepast, vermijd dynamisch het opnemen van een element met de zelfde klasse of dynamisch het wijzigen van de klasse van om het even welke siblings.

**Opties:**

* Werk paginacode bij om elk element uniek te identificeren dat wordt getest (gebruikend identiteitskaart).
* Hiermee wordt gestopt met het dynamisch wijzigen van de klasse of op hetzelfde niveau als hierboven is beschreven.

Voor meer informatie over de invloed van paginawijzigingen op [!DNL Target]Kan worden weergegeven, zie [Paginawijzigingsscenario&#39;s](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Andere activiteiten worden uitgevoerd op dezelfde pagina.

**Valideren:** Gebruik de [!UICONTROL Collisions] om te zien of andere activiteiten worden uitgevoerd.

**Opmerking:** De [!UICONTROL Collisions] werkt niet met de testmodule Sjabloon.

**Opties:**

* Verhoog de prioriteit van deze activiteit.
* De prioriteit van andere activiteiten verlagen.
* Andere activiteiten deactiveren.

## Er verschijnt een foutbericht wanneer u een profielscript verwijdert.

**Valideren:** Een profielscript verwijderen uit [!DNL Target] geeft het foutbericht &#39;&#39;Kan profielscript niet verwijderen&#39;&#39; weer.

**Opties:**

Voer een van de volgende handelingen uit:

* Verwijder het profielscript opnieuw. De succesboodschap wordt weergegeven.
* Wacht ongeveer 10 minuten op de [!DNL Target] importeur die moet worden uitgevoerd. De importer werkt de lijst met profielscripts bij.

## Sommige ajax [!DNL Target] de vraag werkt niet.

**Opmerking:** Meerdere ajax [!DNL Target] Aanroepen met dezelfde naam maar verschillende parameters werken niet op dezelfde pagina. Slechts wordt de eerste vraag gemaakt.

## U hebt een activiteit geactiveerd met de [!DNL Target] API, maar de activiteit geeft de status van [!UICONTROL Inactive] in de [!DNL Target] UI.

Wanneer u bepaalde acties uitvoert, zoals het activeren van een activiteit buiten UI gebruikend [!DNL Target] API, kan de update tot tien minuten duren om aan UI te verspreiden.

## Na het omzetten van activiteiten heeft de bezoeker geen ervaring.

In zeldzame gevallen, als de metrisch van de omzetting van de activiteit om voor een ervaring in aanmerking te komen in het zelfde verzoek wordt verzonden zoals activiteitenkwalificatie, zou de bezoeker in geen enkele ervaring kunnen zijn nadat het verzoek wordt verzonden. In dit geval ziet de bezoeker de standaardinhoud- en ervarings-id die via tokens wordt vastgelegd, op -1. [!DNL Adobe] adviseert het verzenden van activiteitenkwalificatie en omzetting in het zelfde niet [!DNL Target] verzoek.

Als u beide metriek in het zelfde verzoek wilt verzenden, kunt u gebruiken [!UICONTROL Advanced Settings] om aan te geven dat de bezoeker na de conversie in dezelfde ervaring blijft.
