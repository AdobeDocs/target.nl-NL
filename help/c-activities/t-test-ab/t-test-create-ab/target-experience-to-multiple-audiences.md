---
keywords: multiple audiences;experience versions;target experience versions
description: U kunt versies van dezelfde ervaring richten op verschillende soorten publiek in A/B-activiteiten. U kunt veelvoudige toehoorders voor een ervaring in de Visuele Composer van de Ervaring of in Form-Based Composer van de Ervaring plaatsen.
title: Meerdere ervaringsversies in een A/B-test
feature: ab
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Meerdere ervaringsdoelgroepen in een A/B-test{#multiple-experience-versions-in-an-a-b-test}

U kunt versies van dezelfde ervaring richten op verschillende soorten publiek in A/B-activiteiten. U kunt veelvoudige toehoorders voor een ervaring in de Visuele Composer van de Ervaring of in Form-Based Composer van de Ervaring plaatsen.

Gebruikers kunnen schakelen tussen verschillende soorten publiek wanneer hun profiel verandert. Ze zitten niet vast in dezelfde ervaring gedurende de levensduur van de activiteit.

Als uw site bijvoorbeeld een consistent ontwerp gebruikt voor verschillende pagina&#39;s of producten en u dezelfde ervaring wilt gebruiken voor meerdere doelgroepen (zoals bezoekers met verschillende browsertalen), kunt u meerdere versies van de ervaring instellen. U kunt dezelfde ervaring ook presenteren aan Engelse en Japanse sprekers, met als enige verschil dat de tekst in de taal van de bezoeker wordt weergegeven. De gegevens worden verzameld voor de ervaring, ongeacht taal, zodat toont het rapport de prestaties van de ervaring, eerder dan de versie.

Zonder de capaciteit aan opstellingservaringsversies, zou u verschillende tests voor elke taal (in dit voorbeeld) moeten opzetten, dan manueel bijeenvoegen de resultaten om een idee te krijgen hoe één enkele ervaring met beide talen zou kunnen presteren. Dit levert minder nauwkeurige resultaten op. Voor sommige tests zijn deze berekeningen misschien niet eens nuttig vanwege de manier waarop bezoekers worden gerandomiseerd.

Door verschillende versies van een ervaring te maken, ontvangt u nauwkeurigere informatie zonder dat u handmatige berekeningen en aannames hoeft te maken.

**Scenario**

U test twee ervaringen, een geo-gerichte banner versus een generische banner. De banner voor elke geografie moet verschillend zijn, maar de algemene test is te bepalen of het gericht maken beter is dan het tonen van generische inhoud. Als u opstelling een afzonderlijke ervaring voor elke plaats, zou u eigenlijk meten hoe elke geo tegen elkaar presteert, eerder dan of het richten helpt uw succesdoelstellingen bereiken wanneer gemeten tegen de generische banner.

In dit geval, wat u nodig hebt zijn geo-specifieke versies van de ervaring, zodat kunt u de gerichte ervaring tegen een niet-gerichte controle testen.

1. [Maak een A/B-](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md) activiteit zoals u dat normaal zou doen.

   Wanneer het vormen van de ervaring die veelvoudige versies zal hebben, selecteer het publiek voor elke versie, zoals aangetoond in de volgende stappen.

1. Selecteer de ervaring, dan klik **[!UICONTROL Configure]** > **[!UICONTROL Audiences]** > **[!UICONTROL Multiple Audiences]**.

   ![Meerdere soorten publiek, optie](/help/c-activities/t-test-ab/t-test-create-ab/assets/multiple-audiences-new.png)

1. Klik **[!UICONTROL Add Audience]**, dan selecteer het eerste publiek u wilt richten. Herhaal dit voor elk publiek.

   ![](assets/exp-versions.png)

   Als het publiek nog niet bestaat, klik [Create Publiek](/help/c-target/c-audiences/create-audience.md#task_E18BD77A9A8F4ED0AC50569F94556558) en plaats het op.

   Als een bezoeker voor meer dan één publiek in aanmerking komt, wordt de inhoud voor alle soorten publiek geretourneerd, waarbij de laatste in de lijst daadwerkelijk op de pagina wordt weergegeven.

1. Ga door met het instellen van de activiteit.

**Aanbevolen werkwijzen**

* Kies een publiek dat elkaar uitsluitt. Als de activiteit in VEC werd gecreeerd, als een bezoeker meer dan één publiek aanpast, is de inhoud voor elk publiek teruggekeerd, met de inhoud voor het publiek dat voor het laatst op de pagina wordt vermeld.
* Het in het diagram gedefinieerde publiek voor activiteit en toegang wordt gecombineerd met het ervaringspubliek met behulp van een AND-voorwaarde. Om de activiteit binnen te gaan, moet een bezoeker voor het activiteitenpubliek, en één van de ervaringspubliek in aanmerking komen.
* Voeg hetzelfde publiek toe als segmenten voor rapporten. Hierdoor kunt u de testresultaten bekijken op het hoge niveau van ervaring A versus B, en op het lagere niveau van ervaring A versus B voor enkel &quot;browser lang ja_JP.&quot; Dit werkt slechts voor op doel-gebaseerde rapporten, niet op Analytics-Gebaseerde rapporten.

