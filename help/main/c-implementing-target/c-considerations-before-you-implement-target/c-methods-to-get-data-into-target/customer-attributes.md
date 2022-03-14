---
keywords: implementeren;implementeren;instellen;instellen;klantkenmerken
description: Gegevens ophalen in [!DNL Target] het gebruik van klantkenmerken.
title: Hoe krijg ik gegevens in [!DNL Target] Klantkenmerken gebruiken?
feature: Implementation
role: Developer
exl-id: b6c4a286-7994-492d-bde9-346af7aa314f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Klantkenmerken

Met klantkenmerken kunt u gegevens van bezoekersprofielen uploaden via FTP naar de [!DNL Adobe Experience Cloud]. Gebruik de gegevens in [!DNL Adobe Analytics] en [!DNL Adobe Target].

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

[Een bron voor klantkenmerken maken en het gegevensbestand uploaden](https://experienceleague.adobe.com/docs/core-services/interface/customer-attributes/t-crs-usecase.html).
