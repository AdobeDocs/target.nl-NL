---
keywords: troubleshoot target;troubleshooting target;default content;test not live;activity not live;targeting not working;previous experience displays;cannot create activities;can't create activities;create activities;page structure changed;page structure modified;error message;error delete profile script;ajax not working
description: Als uw activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.
title: Problemen met activiteiten oplossen
feature: activities
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Problemen met activiteiten oplossen{#troubleshoot-activities}

Als uw activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.

>[!NOTE]
>
>Naast de volgende het oplossen van problemeninformatie, zie [het Doel van het Oplossen van problemen](/help/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) voor verbindingen aan extra het oplossen van problemenonderwerpen, FAQs, en andere nuttige informatie over het oplossen van problemenactiviteiten en andere eigenschappen in [!DNL Adobe Target].

De volgende secties bevatten problemen u met voorgestelde oplossingen zou kunnen ontmoeten.

## Ik heb een activiteit gemaakt met de interface van het Doel en ik kan deze niet bijwerken via de API.

Activiteiten die zijn gemaakt met behulp van de doelinterface, moeten worden bijgewerkt via de doelinterface. Activiteiten die via API zijn gemaakt, moeten via API worden bijgewerkt. Als u bijvoorbeeld oorspronkelijk een activiteit gebruikend API creeerde, maar dan later de activiteit via het Doel UI uitgeeft, niet worden alle veranderingen bijgewerkt. Alle wijzigingen worden opgeslagen op de achtergrond en kunnen worden bijgewerkt door een andere API-aanroep te maken.

Probeer de activiteit bij te werken met dezelfde methode (UI of API) die oorspronkelijk is gebruikt om de activiteit te maken.

## U ziet standaardinhoud.

Zorg ervoor dat de activiteit is voltooid en geactiveerd.

## De activiteit is niet actief.

**Valideren:** Ga naar overzichtstag en controleer of de test is gemarkeerd als inactief of concept.

**Opties:**

* Test activeren.
* Gebruik Koppelingen voorvertonen om de inactieve test weer te geven.

## U komt niet in aanmerking voor de doelvoorwaarden voor het publiek.

**Valideren:** voorwaarden controleren voor activeren op overzichtspagina.

**Opties:**

* Kwalificeren en opnieuw proberen.
* Gebruik Koppelingen voorvertonen om de doelvoorwaarden te omzeilen.

## De pagina komt niet in aanmerking voor de voorwaarden voor het opgeven van paginaberichten.

**Valideren:** Op de overzichtspagina bepaalt u of de pagina buiten de doelvoorwaarden valt.

**Opties:**

* Ga naar Visual Experience Composer, klik URL \> Geavanceerd \>huidige pagina.

## In plaats van de nieuwe ervaring wordt een vorige ervaring weergegeven.

**Valideren:** probeer een van de onderstaande opties en probeer de ervaring opnieuw weer te geven.

**Opties:**

* Wis cache en cookies en probeer het opnieuw.

* Probeer een andere browser.
* Gebruik de modus Private/Incognito.

## U bent onlangs toegevoegd aan Target, maar u kunt geen activiteiten maken.

**Valideren:** klik op Activiteit maken. Als de optie niet beschikbaar is, hebt u hoogstwaarschijnlijk niet voldoende rechten gekregen om een activiteit tot stand te brengen.

**Opties:**

Zodra u als gebruiker in Doel wordt toegevoegd moet u de rol hebben Approver om Activiteiten tot stand te brengen.

* Vraag de beheerder van uw account om van u een fiatteur te maken.
* Als u de beheerder bent, geeft u uzelf de rol fiatteur vanuit **[!UICONTROL Administration]** > **[!UICONTROL Users]** in Doel.

   Zie [De rol van de fiatteur toewijzen](/help/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## De structuur van de pagina is gewijzigd sinds het instellen van de activiteit.

**Valideren:** Ga naar Visual Experience Composer voor de bestaande activiteit. Let op het waarschuwingsbericht dat de kiezers (of structuur) zijn gewijzigd.

**Opties:**

* Maak de activiteit opnieuw.

Zie [Paginawijzigingsscenario&#39;s](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB) voor meer informatie over de invloed die paginawijzigingen hebben op de weergavemogelijkheid van Target.

## De structuur van de pagina wordt gewijzigd tijdens het laden van de pagina (bij uitvoering).

**Valideren:** Vraag het de ontwikkelaar.

**Opmerking:** Als Target wil weten waar wijzigingen in de activiteit moeten worden toegepast, moet u voorkomen dat er dynamisch elementen met dezelfde klasse worden ingevoegd of dat de klasse van een item op hetzelfde niveau dynamisch wordt gewijzigd.

**Opties:**

* Werk paginacode bij om elk element uniek te identificeren dat (gebruikend identiteitskaart) zal worden getest.
* Hiermee wordt gestopt met het dynamisch wijzigen van de klasse of op hetzelfde niveau als hierboven is beschreven.

Zie [Paginawijzigingsscenario&#39;s](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB) voor meer informatie over de invloed die paginawijzigingen hebben op de weergavemogelijkheid van Target.

## Mbox.js springt alle volgende code uit het hoofd en in het lichaam.

**Valideren:bron** weergeven om te bepalen of declaraties het bestand mbox.js volgen vóór de afsluitende  `</body>` tag.

**Opties:**

* Plaats mbox.js als het laatste item binnen de sectie `<head>` van uw pagina.
* Gebruik unieke div-id&#39;s op de elementen op het hoogste niveau in het lichaam.

## Andere activiteiten worden uitgevoerd op dezelfde pagina.

**Valideren:** gebruik het tabblad Botsinglussen om te zien of andere activiteiten worden uitgevoerd.

**Opmerking:** het tabblad Botsingdetectie werkt niet met de testmodule Sjabloon.

**Opties:**

* Verhoog de prioriteit van deze activiteit.
* De prioriteit van andere activiteiten verlagen.
* Andere activiteiten deactiveren.

## Er verschijnt een foutbericht wanneer u een profielscript verwijdert.

**Valideren:** wanneer u een profielscript verwijdert uit Target Standard/Premium, wordt het foutbericht &#39;&#39;Kan profielscript niet verwijderen&#39;&#39; weergegeven.

**Opties:**

Voer een van de volgende handelingen uit:

* Opnieuw verwijderen. De succesboodschap wordt weergegeven.
* Wacht ongeveer 10 minuten tot de standaardimporteur van het Doel/de Premium wordt uitgevoerd. De importer werkt de lijst met profielscripts bij.

## Sommige ajax [!DNL Target] vraag werkt niet.

**Opmerking:** meerdere ajax- [!DNL Target] aanroepen met dezelfde naam maar verschillende parameters werken niet op dezelfde pagina. Slechts zal de eerste vraag worden gemaakt.

## U activeerde een activiteit gebruikend het Doel API, maar de activiteit toont een status van [!UICONTROL Inactive] in het Doel UI.

Wanneer u bepaalde acties uitvoert, zoals het activeren van een activiteit buiten de UI die het Doel API gebruikt, kan de update tot tien minuten duren om aan UI te verspreiden.