---
keywords: implementeren;implementeren;instellen;instellen;bijwerken met één profiel
description: Gegevens naar doel ophalen met de API voor één profielupdate.
title: Hoe krijg ik gegevens in Doel met de Single Profile Update API?
feature: Implementatie
role: Developer
exl-id: 8331866c-0b84-4d08-83b4-f7f82c67cd21
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# API voor bijwerken van één profiel

Bijna identiek aan de API voor het bijwerken van het bulkprofiel, maar één bezoekersprofiel wordt tegelijk bijgewerkt, in lijn in de API-aanroep in plaats van met een .csv-bestand.

## Indeling

De bezoeker moet via de waarde van Target mboxPC of de waarde mboxThirdPartyId worden geïdentificeerd. De Experience Cloud-id (ECID) wordt niet ondersteund.

## Voorbeelden

U wilt Doel in real time bijwerken wanneer een bezoeker één of andere off-line actie uitvoert. De acties kunnen het bereiken van een callcenter omvatten, wordt een lening gefinancierd, gebruikend een loyaliteitskaart in opslag, die tot een kiosk toegang hebben, etc.

## Voordelen van de methode

Geen limiet voor het aantal profielkenmerken.

Profielkenmerken die via de site worden verzonden, kunnen via de API worden bijgewerkt en andersom.

## Caveats

Limiet van 1.000.000 API-aanroepen (1 miljoen) per periode van 24 uur

Alleen profielen worden bijgewerkt. Kan geen profiel maken voor een mogelijk gebruikersdoel dat nog niet is te zien.

## Codevoorbeelden

GET en POST ondersteund. `https://CLIENT.tt.omtrdc.net/m2/client/profile/update?mboxPC=1368007744041-575948.01_00&profile.attr1=0&profile.attr2=1...`

## Koppelingen naar relevante informatie

[Profielen bijwerken](https://developers.adobetarget.com/api/#updating-profiles)