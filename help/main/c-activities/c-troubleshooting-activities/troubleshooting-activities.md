---
keywords: problemen oplossen doel;het oplossen van problemendoel;standaardinhoud;test niet live;activiteit niet live;het richten van niet werkt;de vorige ervaringsvertoningen;kan geen activiteiten tot stand brengen;kan activiteiten creëren;de paginastructuur veranderde;de paginastructuur veranderde;foutenmelding;fout schrapt profielmanuscript;ajax werkt niet
description: Vind het oplossen van problemensuggesties als uw Adobe [!DNL Target] activiteit wordt niet op uw site weergegeven.
title: Hoe kan ik activiteiten problemen oplossen?
feature: Activities
exl-id: 6aa0486a-9ca3-4545-ae06-9b02e586d777
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Problemen met activiteiten oplossen

Als uw [!DNL Adobe Target] activiteit niet op uw plaats verschijnt, zouden deze het oplossen van problemensuggesties u moeten helpen uw oplossing vinden.

>[!NOTE]
>
>Naast de volgende het oplossen van problemeninformatie, zie [Probleemoplossing](/help/main/r-troubleshooting-target/troubleshooting-target.md#reference_A9DB82675D044BD8861F6752A4EE6839) voor verbindingen aan extra het oplossen van problemenonderwerpen, FAQs, en andere nuttige informatie over het oplossen van problemenactiviteiten en andere eigenschappen in [!DNL Adobe Target].

De volgende secties bevatten problemen u met voorgestelde oplossingen zou kunnen ontmoeten.

## Ik heb een activiteit gemaakt met de [!DNL Target] UI en ik kunnen het niet via API bijwerken.

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

## In plaats van de nieuwe ervaring wordt een vorige ervaring weergegeven.

**Valideren:** Probeer een van de onderstaande opties en probeer de ervaring opnieuw weer te geven.

**Opties:**

* Wis cache en cookies en probeer het opnieuw.

* Probeer een andere browser.
* Gebruik de modus Private/Incognito.

## Je bent onlangs toegevoegd aan [!DNL Target] maar kan geen activiteiten creëren .

**Valideren:** Klik op Activiteit maken. Als de optie niet beschikbaar is, hebt u hoogstwaarschijnlijk niet voldoende rechten gekregen om een activiteit tot stand te brengen.

**Opties:**

Zodra u als gebruiker in Doel wordt toegevoegd moet u de rol hebben Approver om Activiteiten tot stand te brengen.

* Vraag de beheerder van uw account om van u een fiatteur te maken.
* Als u de beheerder bent, geef uzelf de rol fiatteur van **[!UICONTROL Administration]** > **[!UICONTROL Users]** in Doel.

   Zie [Wijs zelf de rol van fiatteur toe](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## De structuur van de pagina is gewijzigd sinds het instellen van de activiteit.

**Valideren:** Ga naar Visual Experience Composer voor de bestaande activiteit. Let op het waarschuwingsbericht dat de kiezers (of structuur) zijn gewijzigd.

**Opties:**

* Maak de activiteit opnieuw.

Voor meer informatie over hoe de paginawijzigingen de capaciteit van het Doel om beïnvloeden te tonen, zie [Paginawijzigingsscenario&#39;s](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

## De structuur van de pagina wordt gewijzigd tijdens het laden van de pagina (bij uitvoering).

**Valideren:** Vraag het de ontwikkelaar.

**Opmerking:** Als u wilt dat Target herkent waar wijzigingen in de activiteit moeten worden toegepast, moet u voorkomen dat elementen met dezelfde klasse dynamisch worden ingevoegd of dat de klasse op enigerlei wijze op hetzelfde niveau dynamisch wordt gewijzigd.

**Opties:**

* Werk paginacode bij om elk element uniek te identificeren dat (gebruikend identiteitskaart) zal worden getest.
* Hiermee wordt gestopt met het dynamisch wijzigen van de klasse of op hetzelfde niveau als hierboven is beschreven.

Voor meer informatie over hoe de paginawijzigingen de capaciteit van het Doel om beïnvloeden te tonen, zie [Paginawijzigingsscenario&#39;s](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-scenarios.md#concept_A458A95F65B4401588016683FB1694DB).

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

## Sommige ajax [!DNL Target] de vraag werkt niet.

**Opmerking:** Meerdere ajax [!DNL Target] Aanroepen met dezelfde naam maar verschillende parameters werken niet op dezelfde pagina. Slechts zal de eerste vraag worden gemaakt.

## U hebt een activiteit geactiveerd met de [!DNL Target] API, maar de activiteit geeft de status van [!UICONTROL Inactive] in de [!DNL Target] UI.

Wanneer u bepaalde acties uitvoert, zoals het activeren van een activiteit buiten de UI die het Doel API gebruikt, kan de update tot tien minuten duren om aan UI te verspreiden.
