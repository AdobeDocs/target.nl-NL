---
keywords: implementeren;implementeren;instellen;instellen;pagina, parameter
description: Gegevens naar doel ophalen met behulp van paginaparameters.
title: Hoe krijg ik Gegevens in Doel gebruikend de Parameters van de Pagina?
feature: Implementatie
role: Developer
translation-type: tm+mt
source-git-commit: 5783ef25c48120dc0beee6f88d499a31a0de8bdc
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Paginaparameters

Paginaparameters (ook wel &quot;parameters mbox&quot; genoemd) zijn naam-/waardeparen die rechtstreeks via paginacode worden doorgegeven en die niet in het profiel van de bezoeker worden opgeslagen voor toekomstig gebruik.

Paginaparameters zijn handig voor het verzenden van paginagegevens naar Doel die niet met het profiel van de bezoeker hoeven te worden opgeslagen voor toekomstig doelgebruik. Deze waarden worden in plaats daarvan gebruikt om de pagina of de actie te beschrijven die de gebruiker op de specifieke pagina heeft ondernomen.

## Indeling

De parameters van de pagina worden overgegaan in Doel via een servervraag als koordnaam/waardepaar. Parameternamen en -waarden kunnen worden aangepast (hoewel er enkele &#39;gereserveerde namen&#39; zijn voor specifieke toepassingen).

### Voorbeelden:

* `page=productPage`

* `categoryId=homeLoans`

## Voorbeelden

* **Productpagina**&#39;s: Informatie verzenden over het bekeken specifieke product (deze methode is hoe Recommendations werkt)
* **Bestelgegevens**: Order-id, orderTotal enzovoort verzenden voor het verzamelen van bestellingen
* **Categorie-affiniteit**: Door een categorie bekeken informatie naar Doel verzenden om kennis van de affiniteit van de gebruiker met bepaalde sitecategorieën te vergroten
* **Gegevens** van derden: Verstuur informatie van derde gegevensbronnen, zoals weergerichte leveranciers, rekeningsgegevens (bijvoorbeeld, DemandBase), demografische gegevens (bijvoorbeeld Experian), en meer.

## Voordelen van methode

De gegevens worden verzonden naar Doel in echt - tijd, en kunnen op de zelfde servervraag worden gebruikt de gegevens waarop het binnen komt.

## Caveats

* Vereist een update van de paginacode (direct of via een systeem van het markeringsbeheer).
* Als de gegevens voor het richten op een volgende pagina/servervraag moeten worden gebruikt, moet het in een profielmanuscript worden vertaald.
* De koorden van de vraag kunnen slechts karakters zoals volgens [de norm ](https://www.ietf.org/rfc/rfc3986.txt) van de Techniek van Internet van de Taakmacht (IETF) bevatten.

   Naast de tekens die op de IETF-site worden vermeld, staat Target de volgende tekens in querytekenreeksen toe:

   `&lt; > # % &quot; { } | \\ ^ \[\] \&quot;

   Al het andere moet met url gecodeerd zijn. De standaard geeft de volgende notatie aan ( [https://www.ietf.org/rfc/rfc1738.txt](https://www.ietf.org/rfc/rfc1738.txt) ), zoals hieronder wordt geïllustreerd:

   ![](assets/ietf1.png)

   Of, de volledige lijst voor eenvoud:

   ![](assets/ietf2.png)

## Codevoorbeelden

targetPageParamsAll (voegt de parameters aan alle mbox vraag op de pagina toe):

`function targetPageParamsAll() { return "param1=value1&param2=value2&p3=hello%20world";`

targetPageParams (voegt de parameters aan globale mbox op de pagina toe):

`function targetPageParams() { return "param1=value1&param2=value2&p3=hello%20world";`

Parameters in mboxCreate-code:

`<div class="mboxDefault"> default content to replace by offer </div> <script> mboxCreate('mboxName','param1=value1','param2=value2'); </script>`

## Koppelingen naar relevante informatie

Recommendations: [Implementatie volgens paginatype](/help/c-recommendations/plan-implement.md#reference_DE38BB07BD3C4511B176CDAB45E126FC)

Bevestiging van bestelling: [Conversies bijhouden](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#task_E85D2F64FEB84201A594F2288FABF053)

Categorie-affiniteit: [Categorie-affiniteit](/help/c-target/c-visitor-profile/category-affinity.md#concept_75EC1E1123014448B8B92AD16B2D72CC)

