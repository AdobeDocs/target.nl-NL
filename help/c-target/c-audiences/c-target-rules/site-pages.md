---
keywords: sitepagina's;doelsitepagina's;doel;huidige pagina;doel huidige pagina;vorige pagina;doel vorige pagina;landingspagina;doel landingspagina;http header
description: U kunt zich richten op bezoekers die zich op een specifieke pagina op uw site bevinden.
title: Opties voor sitepagina's in soorten publiek
feature: Audiences
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Sitepagina&#39;s{#site-pages}

U kunt zich richten op bezoekers die zich op een specifieke pagina op uw site bevinden.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Noem het publiek.
1. Klik op **[!UICONTROL Add Rule]** > **[!UICONTROL Site Pages]**.

   ![Sitepagina&#39;s, publiek](assets/target_site_pages.png)

1. Klik **[!UICONTROL Select]** drop-down lijst, selecteer één van de volgende opties, dan vorm de regel zoals gewenst.

   Welke opties en beoordelaars beschikbaar zijn in vervolgkeuzelijsten in de regel, is afhankelijk van de optie die u kiest. In de volgende afbeelding ziet u de beschikbare opties als u [!UICONTROL Current Page] kiest:

   ![Huidige pagina](/help/c-target/c-audiences/c-target-rules/assets/current-page.png)

   De volgende opties zijn beschikbaar in de eerste vervolgkeuzelijst wanneer u [!UICONTROL Select] kiest.

   * **Huidige pagina:** de pagina waarop de gebruiker momenteel staat.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie [Doelen en veelgestelde vragen ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domein
      * Query
      * Subdomein
      * Domein op hoofdniveau
      * Pad
      * Hash-fragment (#)
   * **Vorige pagina:** De pagina waarop de gebruiker stond voordat deze op de huidige pagina klikte. (De gebruiker moet van de vorige pagina tot de huidige pagina klikken voor de pagina om worden gevolgd. De vorige pagina wordt niet bijgehouden als de gebruiker een nieuwe URL in browser typt.) De feitelijke inhoud van deze pagina is afhankelijk van het ontwerp van uw site. Als op de huidige pagina bijvoorbeeld informatie over een specifiek product wordt weergegeven, is de vorige pagina mogelijk een categoriepagina waarop de bezoeker het specifieke item selecteert (bijvoorbeeld een pagina waarop meerdere camera&#39;s van een bepaald type worden weergegeven), of de pagina die naar de laatste pagina leidt.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie [Doelen en veelgestelde vragen ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domein
      * Query
      * Subdomein
      * Domein op hoofdniveau
      * Pad
   * **Openingspagina:** De bestemmingspagina is de eerste pagina die de bezoeker ziet wanneer hij uw site opent. Als de bezoeker bijvoorbeeld op een koppeling op Google klikt die naar een categoriepagina leidt, is de categoriepagina de bestemmingspagina. Als de koppeling naar uw startpagina leidt, is de startpagina de bestemmingspagina. De landingspagina wordt onthouden voor de sessie van de bezoeker. U kunt de site dieper plaatsen op basis van de bestemmingspagina van de bezoeker in deze sessie.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * URL (Voor meer informatie over hoe het Doel URLs evalueert, zie [Doelen en veelgestelde vragen ](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * Domein
      * Query
      * Subdomein
      * Domein op hoofdniveau
      * Pad
      * Hash-fragment (#)

      >[!NOTE]
      >
      >Het object `landing.url` wordt opnieuw ingesteld op een subdomeinwijziging of directe URL-vervanging.

   * **HTTP-koptekst:** Deze optie evalueert de informatie in de HTTP-koptekst van de aanvraag Doel. Als de HTTP-header bijvoorbeeld taalgegevens bevat, kunt u een regel maken die de voorwaarde `Accept-Language: es` bevat om bezoekers die de pagina in het Spaans openen, te bereiken.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * Accepteren
      * Accepteren-tekenset
      * Codering accepteren
      * Accept-Language
      * Toestemming
      * Cachebeheer
      * Verbinding
      * Content-Length
      * Content-MDS
      * Inhoudstype
      * Datum
      * Verwacht
      * Van
      * Host
      * If-Match
      * If-Modified-Since
      * If-None-Match
      * If-Range
      * If-Unmodified-Since
      * Max-Forwards
      * Pragma
      * Proxy-autorisatie
      * Bereik
      * Verwijzing
      * TE
      * Upgrade
      * Gebruikersagent
      * Via
      * Waarschuwing

   Als u [!UICONTROL Current Page], [!UICONTROL Previous Page], of [!UICONTROL Landing Page] kiest, zijn de [!UICONTROL Domain] en [!UICONTROL Query] opties beschikbaar. Houd rekening met het volgende wanneer u deze opties kiest:

   * **Domein:** het volledige domein van de pagina. Als u een domein opgeeft, kunt u het beste &#39;contains&#39; gebruiken. &quot;Domain equals facebook.com&quot; accepteert bijvoorbeeld `m.facebook.com` of `www.facebook.com` niet. &quot;Het domein bevat facebook.com&quot;zal om het even welke variant van facebook.com goedkeuren.
   * **Query:** De inhoud van de URL na het eerste vraagteken (?).

      `foo.html?e0a72cb2a2c7`





1. (Optioneel) Klik op **[!UICONTROL Add Rule]** en stel aanvullende regels in voor het publiek.
1. Klik op **[!UICONTROL Save]**.

U kunt ook doelgroepen voor sitepagina&#39;s maken met behulp van uw eigen queryparameter &quot;door de gebruiker gedefinieerd&quot; of &quot;door de gebruiker gedefinieerde koptekst&quot;.

Gebruik een:

* De parameter van de vraag als de regel die door de gebruiker wordt geselecteerd Huidige Pagina, het Landen Pagina, of Vorige Pagina is.
* Koptekst als de regel die door de gebruiker is geselecteerd, een HTTP-koptekst is.

zoals hieronder wordt geïllustreerd:

![](assets/site_pages.png)

## Problemen oplossen {#ts}

* Om ervoor te zorgen dat het publiek van de bestemmingspagina correct kan functioneren, moeten aanvragen de `mboxReferrer`-parameter hebben ingesteld (voor de bezorgings-API de parameter `context.address.referringUrl`) die de JavaScript-bibliotheek at.js van de pagina neemt met behulp van het `document.referrer`-kenmerk. Dit `HTMLDocument` attribuut keert URI van de pagina terug de gebruiker heeft genavigeerd van. De waarde van dit kenmerk is een lege tekenreeks wanneer de gebruiker rechtstreeks naar de pagina navigeert (niet via een koppeling, maar bijvoorbeeld via een bladwijzer).

   Als dit gedrag niet aan uw vereisten voldoet, kunt u een van de volgende handelingen uitvoeren:

   * Geef [mbox-parameters](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) door aan [!DNL Target] om te gebruiken voor doeldoeleinden.
   * Gebruik een [A/B Test activity](/help/c-activities/t-test-ab/test-ab.md) in plaats van een openingspagina-activiteit. Bij de A/B-testactiviteiten wordt niet van ervaring gewisseld voor dezelfde bezoeker.
   * Gebruik in plaats hiervan een [bezoekersprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md).

* Wanneer het gebruiken &quot;begint/beëindigt met&quot;beoordelaars op koorden die komma&#39;s bevatten, houd er rekening mee dat deze
worden geëvalueerd als een array van waarden, waarin elke waarde die door komma&#39;s wordt gescheiden, wordt geëvalueerd. Als we bijvoorbeeld de waarde voor een header hebben: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` komt in aanmerking voor voorwaarden zoals:
   * begint met zh,
   * begint met en,
   * eindigt met 0,7,
   * eindigt met 0,8.

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
