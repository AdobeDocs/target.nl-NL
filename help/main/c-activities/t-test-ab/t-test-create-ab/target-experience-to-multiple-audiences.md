---
keywords: meerdere soorten publiek;ervaringsversies;doelervaringsversies
description: Ontdek hoe te om verschillende publiekssegmenten met versies van de zelfde ervaring in A/B activiteiten te richten.
title: Kan ik veelvoudige ervaringsversies in een activiteit A/B gebruiken?
feature: A/B Tests
exl-id: 7afe36f0-ec46-4d63-bfff-45d2c8923a04
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Meerdere ervaringsdoelgroepen in een A/B-test

U kunt versies van dezelfde ervaring richten op verschillende soorten publiek in [!DNL Adobe Target] A/B-activiteiten. U kunt meerdere soorten publiek instellen voor een ervaring in de [!UICONTROL Visual Experience Composer] (VEC) of in de Form-Based Experience Composer.

Bezoekers kunnen schakelen tussen ervaringspersoneel wanneer hun profiel verandert. Bezoekers zitten niet vast in dezelfde ervaring gedurende de levensduur van de activiteit.

Als uw site bijvoorbeeld een consistent ontwerp gebruikt voor verschillende pagina&#39;s of producten en u dezelfde ervaring wilt gebruiken voor meerdere doelgroepen (zoals bezoekers met verschillende browsertalen), kunt u meerdere versies van de ervaring instellen. U kunt dezelfde ervaring ook presenteren aan Engelse en Japanse luidsprekers, met als enige verschil dat de tekst in de taal van de bezoeker wordt weergegeven. De gegevens worden verzameld voor de ervaring, ongeacht taal, zodat toont het rapport de prestaties van de ervaring, eerder dan de versie.

Zonder de capaciteit aan opstellingservaringsversies, zou u verschillende tests voor elke taal (in dit voorbeeld) moeten opzetten, dan manueel bijeenvoegen de resultaten om een idee te krijgen hoe één enkele ervaring met beide talen zou kunnen presteren. Dit levert minder nauwkeurige resultaten op. Voor sommige tests zijn deze berekeningen misschien niet eens nuttig vanwege de manier waarop bezoekers worden gerandomiseerd.

Door verschillende versies van een ervaring te maken, ontvangt u nauwkeurigere informatie zonder dat u handmatige berekeningen en aannames hoeft te maken.

## Scenario

U test twee ervaringen, een geo-gerichte banner versus een generische banner. De banner voor elke geografie moet verschillend zijn, maar de algemene test is te bepalen of geo-gericht beter is dan het tonen van generische inhoud. Als u opstelling een afzonderlijke ervaring voor elke plaats, zou u eigenlijk meten hoe elke geo tegen elkaar presteert, eerder dan of de geo-richtende hulp uw succesdoelstellingen wanneer gemeten tegen de generische banner beantwoordt.

In dit geval hebt u geospecifieke versies van de ervaring nodig, zodat u de geo-gerichte ervaring kunt testen tegen een niet-geo-gerichte controle.

1. [&#x200B; creeer een activiteit A/B &#x200B;](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) aangezien u normaal zou.

   Wanneer het vormen van de ervaring die veelvoudige versies zal hebben, selecteer het publiek voor elke versie, zoals aangetoond in de volgende stappen.

1. Selecteer de ervaring en klik vervolgens op **[!UICONTROL Configure]** > **[!UICONTROL Multiple Audiences]** .

1. Klik het **[!UICONTROL Add Audience]** pictogram ( ![&#x200B; voeg pictogram &#x200B;](/help/main/assets/icons/Add.svg) toe) in de [!UICONTROL Experience Audiences] ruit, dan selecteer het eerste publiek u wilt richten. Herhaal dit voor elk publiek.

   Als het publiek nog niet bestaat, klik [&#x200B; leidt tot Audience &#x200B;](/help/main/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558) en opstelling het.

   Als een bezoeker voor meer dan één publiek in aanmerking komt, wordt de inhoud voor alle soorten publiek geretourneerd, waarbij de laatste in de lijst daadwerkelijk op de pagina wordt weergegeven.

1. Ga door met het instellen van de activiteit.

## Aanbevolen procedures

* Kies wederzijds exclusief publiek. Als de activiteit in VEC werd gecreeerd, als een bezoeker meer dan één publiek aanpast, is de inhoud voor elk publiek teruggekeerd, met de inhoud voor het publiek dat voor het laatst op de pagina wordt vermeld.
* Het in het diagram gedefinieerde publiek voor activiteit en toegang wordt gecombineerd met het ervaringspubliek met behulp van een AND-voorwaarde. Om de activiteit binnen te gaan, moet een bezoeker voor het activiteitenpubliek, en één van de ervaringspubliek in aanmerking komen.
* Voeg hetzelfde publiek toe als segmenten voor rapporten. Dit helpt u de testresultaten bij het hoge niveau van ervaring A tegenover B bekijken, en op het lagere niveau van ervaring A tegenover B voor enkel &quot;browser lang ja_JP.&quot; Dit werkt alleen voor [!DNL Target] -rapporten, niet voor [!DNL Analytics] -rapporten.
