---
keywords: implementeren;implementeren;instellen;instellen;klantkenmerken
description: Krijg gegevens in Doel gebruikend klantenattributen.
title: Hoe krijg ik gegevens in doel gebruikend de Attributen van de Klant?
feature: Implementation
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
translation-type: tm+mt
source-git-commit: 20daf4510e754d77cd16be64770105932178fec5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Klantkenmerken

Met klantkenmerken kunt u gegevens van bezoekersprofielen via FTP uploaden naar [!DNL Adobe Experience Cloud]. Na het uploaden gebruikt u de gegevens in [!DNL Adobe Analytics] en [!DNL Adobe Target].

De standaardklanten van het doel kunnen vijf attributen toepassen, de klanten van de Premie van het Doel kunnen 200 attributen toepassen.

## Indeling

Een .csv-bestand met Experience Cloud-id&#39;s (ECID&#39;s) en paren van kenmerknaam/waarde wordt geüpload via FTP of handmatig in de gebruikersinterface van de Experience Cloud.

## Voorbeelden van gebruiksgevallen

Uw CRM of ander intern systeem slaat waardevolle informatie op u met Adobe Experience Cloud, met inbegrip van Doel en Analytics wilt delen.

## Voordelen van de methode

Als u klantgegevens uploadt, wordt voor die bezoeker in Target een profielvermelding gemaakt, zelfs als Target de bezoeker nog niet heeft kunnen zien.

Dezelfde gegevens zijn automatisch beschikbaar in Doel en Analyse.

FTP kan een eenvoudigere implementatiemethode zijn dan API.

## Caveats

De standaardklanten van het doel kunnen vijf attributen toepassen, de klanten van de Premie van het Doel kunnen 200 attributen toepassen

Kan waarden alleen bijwerken via Customer Attributes, niet op pagina.

Vereist Experience Cloud ID-implementatie (ECID).

## Codevoorbeelden

Details vindt u in [Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).

### Koppelingen naar relevante informatie

[Maak een bron voor klantkenmerken en upload het gegevensbestand](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
