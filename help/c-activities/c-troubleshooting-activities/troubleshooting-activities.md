---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;can't create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: Als uw activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.
title: Problemen met activiteiten oplossen
topic: Advanced,Standard,Classic
uuid: 5b22c369-0efc-48c0-a0dc-0179b18536fe
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Problemen met activiteiten oplossen{#troubleshoot-activities}

Als uw activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.

>[!NOTE]
>
>Naast de volgende het oplossen van problemeninformatie, zie het Doel [van het](../../r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) Oplossen van problemen voor verbindingen aan extra het oplossen van problemenonderwerpen, FAQs, en andere nuttige informatie over het oplossen van problemenactiviteiten en andere eigenschappen in [!DNL Adobe Target].

De volgende secties bevatten problemen u met voorgestelde oplossingen zou kunnen ontmoeten.

## Ik heb een activiteit gemaakt met de interface van het Doel en ik kan deze niet bijwerken via de API.

Activiteiten die zijn gemaakt met behulp van de doelinterface, moeten worden bijgewerkt via de doelinterface. Activiteiten die via API zijn gemaakt, moeten via API worden bijgewerkt. Als u bijvoorbeeld oorspronkelijk een activiteit gebruikend API creeerde, maar dan later de activiteit via het Doel UI uitgeeft, niet worden alle veranderingen bijgewerkt. Alle wijzigingen worden opgeslagen op de achtergrond en kunnen worden bijgewerkt door een andere API-aanroep te maken.

Probeer de activiteit bij te werken met dezelfde methode (UI of API) die oorspronkelijk is gebruikt om de activiteit te maken.

## U ziet standaardinhoud.

Zorg ervoor dat de activiteit is voltooid en geactiveerd.

## De activiteit is niet actief.

**Valideren:** Ga naar het overzichtstabblad en controleer of de test is gemarkeerd als inactief of concept.

**Opties:**

* Test activeren.
* Gebruik Koppelingen voorvertonen om de inactieve test weer te geven.

## U komt niet in aanmerking voor de doelvoorwaarden voor het publiek.

**Valideren:** Doelvoorwaarden controleren op overzichtspagina.

**Opties:**

* Kwalificeren en opnieuw proberen.
* Gebruik Koppelingen voorvertonen om de doelvoorwaarden te omzeilen.

## De pagina komt niet in aanmerking voor de voorwaarden voor het opgeven van paginaberichten.

**Valideren:** Bepaal op de overzichtspagina of de pagina buiten de doelvoorwaarden valt.

**Opties:**

* Ga naar Visual Experience Composer, klik URL \> Geavanceerd \>huidige pagina.

## In plaats van de nieuwe ervaring wordt een eerdere ervaring weergegeven.

**Valideren:** Probeer een van de onderstaande opties en probeer de ervaring opnieuw weer te geven.

**Opties:**

* Wis cache en cookies en probeer het opnieuw.

* Probeer een andere browser.
* Gebruik de modus Private/Incognito.

## U bent onlangs toegevoegd aan Target, maar u kunt geen activiteiten maken.

**Valideren:** Klik op Activiteit maken. Als de optie niet beschikbaar is, hebt u hoogstwaarschijnlijk niet voldoende rechten gekregen om een activiteit tot stand te brengen.

**Opties:**

Zodra u als gebruiker in Doel wordt toegevoegd moet u de rol hebben Approver om Activiteiten tot stand te brengen.

* Vraag de beheerder van uw account om van u een fiatteur te maken.
* Als u Admin bent, geef me de rol van fiatteur van Opstelling > Gebruikers in de Standaard van het Doel.

   Zie [Uw eigen rol](../../administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7)fiatteur toewijzen.

## De structuur van de pagina is gewijzigd sinds het instellen van de activiteit.

**Valideren:** Ga naar Visual Experience Composer voor de bestaande activiteit. Let op het waarschuwingsbericht dat de kiezers (of structuur) zijn gewijzigd.

**Opties:**

* Maak de activiteit opnieuw.

Zie Scenario&#39;s voor [paginawijzigingen voor meer informatie over de invloed die paginawijzigingen hebben op de weergavemogelijkheid van Target](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## De structuur van de pagina wordt gewijzigd tijdens het laden van de pagina (bij uitvoering).

**Valideren:** Vraag het de ontwikkelaar.

**Opmerking:** Als u wilt dat Target herkent waar wijzigingen in de activiteit moeten worden toegepast, moet u voorkomen dat elementen met dezelfde klasse dynamisch worden ingevoegd of dat de klasse op enigerlei wijze op hetzelfde niveau dynamisch wordt gewijzigd.

**Opties:**

* Werk paginacode bij om elk element uniek te identificeren dat (gebruikend identiteitskaart) zal worden getest.
* Hiermee wordt gestopt met het dynamisch wijzigen van de klasse of op hetzelfde niveau als hierboven is beschreven.

Zie Scenario&#39;s voor [paginawijzigingen voor meer informatie over de invloed die paginawijzigingen hebben op de weergavemogelijkheid van Target](../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## Mbox.js springt alle volgende code uit het hoofd en in het lichaam.

**Valideren:** Bron weergeven om te bepalen of declaraties het bestand mbox.js volgen vóór het sluiten </body> tag.

**Opties:**

* Plaats mbox.js als het laatste item binnen de `<head>` sectie van uw pagina.
* Gebruik unieke div-id&#39;s op de elementen op het hoogste niveau in het lichaam.

## Andere activiteiten worden uitgevoerd op dezelfde pagina.

**Valideren:** Gebruik het lusje van Aantekeningen om van andere activiteiten te zien lopen.

**Opmerking:** Het tabblad Botsingdetectie werkt niet met de testmodule Sjabloon.

**Opties:**

* Verhoog de prioriteit van deze activiteit.
* De prioriteit van andere activiteiten verlagen.
* Andere activiteiten deactiveren.

## Er verschijnt een foutbericht wanneer u een profielscript verwijdert.

**Valideren:** Als u een profielscript verwijdert uit Target Standard/Premium, wordt het foutbericht &#39;&#39;Kan profielscript niet verwijderen&#39;&#39; weergegeven.

**Opties:**

Voer een van de volgende handelingen uit:

* Opnieuw verwijderen. De succesboodschap wordt weergegeven.
* Wacht ongeveer 10 minuten tot de standaardimporteur van het Doel/de Premium wordt uitgevoerd. De importer werkt de lijst met profielscripts bij.

## Sommige ajax mbox-aanroepen werken niet.

**Opmerking:** Meerdere ajax-oproepen met dezelfde naam van de box maar verschillende parameters werken niet op dezelfde pagina. Slechts zal de eerste vraag worden gemaakt.

## U activeerde een activiteit gebruikend het Doel API, maar de activiteit toont een status van Inactief in het Doel UI.

Wanneer u bepaalde acties uitvoert, zoals het activeren van een activiteit buiten de UI die het Doel API gebruikt, kan de update tot tien minuten duren om aan UI te verspreiden.