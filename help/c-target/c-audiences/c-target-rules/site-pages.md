---
keywords: sitepagina's;doelsitepagina's;doel;huidige pagina;doel huidige pagina;vorige pagina;doel vorige pagina;landingspagina;doel landingspagina;http header
description: Leer hoe u bezoekers kunt aanwijzen met [!DNL Adobe Target] die zich op een specifieke pagina op uw site bevinden.
title: Kan ik bezoekers richten op basis van sitepagina's?
feature: Soorten publiek
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: b46966a8dbb2ff6d2efbfb8f126783f750c2f08c
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Sitepagina&#39;s

U kunt bezoekers als doel instellen met [!DNL Adobe Target] die een specifieke pagina op uw site openen.

1. Klik in de interface [!DNL Target] op **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Sleep **[!UICONTROL Site Pages]** in de ruit van de publieksbouwer.

   ![Sitepagina&#39;s, publiek](assets/target_site_pages.png)

1. Klik **[!UICONTROL Select]** drop-down lijst, selecteer één van de volgende opties, dan vorm de regel zoals gewenst.

   Welke opties en beoordelaars beschikbaar zijn in vervolgkeuzelijsten in de regel, is afhankelijk van de optie die u kiest. In de volgende afbeelding ziet u de beschikbare opties als u [!UICONTROL Current Page] kiest:

   ![Huidige pagina](assets/current-page.png)

   De volgende opties zijn beschikbaar in de eerste vervolgkeuzelijst wanneer u [!UICONTROL Select] kiest.

   * **[!UICONTROL Current Page]:** De pagina die de gebruiker bekijkt.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Zie Veelgestelde vragen over  [!DNL Target] doelen en doelgroepen voor meer informatie over hoe URL&#39; [s worden geëvalueerd](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]
   * **[!UICONTROL Previous Page]:** De pagina die de gebruiker heeft bekeken voordat deze op de huidige pagina klikte. De pagina wordt alleen bijgehouden als de gebruiker van de vorige pagina naar de huidige pagina klikt. De vorige pagina wordt niet bijgehouden als de gebruiker een nieuwe URL in browser typt. De feitelijke inhoud van deze pagina is afhankelijk van het ontwerp van uw site. Als op de huidige pagina bijvoorbeeld informatie over een bepaald product wordt weergegeven, is de vorige pagina mogelijk een categoriepagina waarop de bezoeker het specifieke item selecteert. Een pagina die bijvoorbeeld verschillende camera&#39;s van een bepaald type weergeeft, of de pagina &quot;home&quot; die tot de uiteindelijke pagina leidt.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Zie Veelgestelde vragen over  [doelen en soorten publiek voor meer informatie over hoe Doel URL&#39;s evalueert](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
   * **[!UICONTROL Landing Page]:** De landingspagina is de eerste pagina die de bezoeker ziet wanneer hij of zij uw site opent. Als de bezoeker bijvoorbeeld op een koppeling op Google klikt die naar een categoriepagina leidt, is de categoriepagina de bestemmingspagina. Als de koppeling naar uw startpagina leidt, is de startpagina de bestemmingspagina. De landingspagina wordt onthouden voor de sessie van de bezoeker. U kunt de site dieper plaatsen op basis van de bestemmingspagina van de bezoeker in deze sessie.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Zie Veelgestelde vragen over  [doelen en soorten publiek voor meer informatie over hoe Doel URL&#39;s evalueert](/help/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

      >[!NOTE]
      >
      >Het object `landing.url` wordt opnieuw ingesteld op een subdomeinwijziging of directe URL-vervanging.

   * **[!UICONTROL HTTP Header]:** Deze optie evalueert de informatie in de kopbal van HTTP van het  [!DNL Target] verzoek. Als de HTTP-header bijvoorbeeld taalgegevens bevat, kunt u een regel maken die de voorwaarde `Accept-Language: es` bevat om bezoekers die de pagina in het Spaans openen, te bereiken.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL Accept]
      * [!UICONTROL Accept-Charset]
      * [!UICONTROL Accept-Encoding]
      * [!UICONTROL Accept-Language]
      * [!UICONTROL Authorization]
      * [!UICONTROL Cache-Control]
      * [!UICONTROL Connection]
      * [!UICONTROL Content-Length]
      * [!UICONTROL Content-MDS]
      * [!UICONTROL Content-Type]
      * [!UICONTROL Date]
      * [!UICONTROL Expect]
      * [!UICONTROL From]
      * [!UICONTROL Host]
      * [!UICONTROL If-Match]
      * [!UICONTROL If-Modified-Since]
      * [!UICONTROL If-None-Match]
      * [!UICONTROL If-Range]
      * [!UICONTROL If-Unmodified-Since]
      * [!UICONTROL Max-Forwards]
      * [!UICONTROL Pragma]
      * [!UICONTROL Proxy-Authorization]
      * [!UICONTROL Range]
      * [!UICONTROL Referrer]
      * [!UICONTROL TE]
      * [!UICONTROL Upgrade]
      * [!UICONTROL User-Agent]
      * [!UICONTROL Via]
      * [!UICONTROL Warning]

   Als u [!UICONTROL Current Page], [!UICONTROL Previous Page], of [!UICONTROL Landing Page] kiest, zijn de [!UICONTROL Domain] en [!UICONTROL Query] opties beschikbaar. Houd rekening met het volgende wanneer u deze opties kiest:

   * **Domein:** het volledige domein van de pagina. Als u een domein opgeeft, kunt u het beste &#39;contains&#39; gebruiken. &quot;Domain equals facebook.com&quot; accepteert bijvoorbeeld `m.facebook.com` of `www.facebook.com` niet. &quot;Domein bevat facebook.com&quot; accepteert elke variant van facebook.com.
   * **Query:** De inhoud van de URL na het eerste vraagteken (?).

      `foo.html?e0a72cb2a2c7`





1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

U kunt ook doelgroepen voor sitepagina&#39;s maken met behulp van uw eigen queryparameter &quot;door de gebruiker gedefinieerd&quot; of &quot;door de gebruiker gedefinieerde koptekst&quot;.

Gebruik een:

* De parameter van de vraag als de regel door de gebruiker wordt geselecteerd [!UICONTROL Current Page], [!UICONTROL Landing Page], of [!UICONTROL Previous Page] is
* Koptekst als de regel die de gebruiker heeft geselecteerd, een HTTP-koptekst is

## Problemen oplossen {#ts}

* Om ervoor te zorgen dat het publiek van de bestemmingspagina correct kan functioneren, moeten aanvragen de `mboxReferrer`-parameter hebben ingesteld (voor de bezorgings-API de parameter `context.address.referringUrl`) die de JavaScript-bibliotheek at.js van de pagina neemt met behulp van het `document.referrer`-kenmerk. Dit `HTMLDocument` attribuut keert URI van de pagina terug de gebruiker heeft genavigeerd van. De waarde van dit kenmerk is een lege tekenreeks wanneer de gebruiker rechtstreeks naar de pagina navigeert (niet via een koppeling, maar bijvoorbeeld via een bladwijzer).

   Als dit gedrag niet aan uw vereisten voldoet, kunt u een van de volgende handelingen uitvoeren:

   * Geef [mbox-parameters](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/pass-parameters-to-global-mbox.md) door aan [!DNL Target] om te gebruiken voor doeldoeleinden.
   * Gebruik een [A/B Test activity](/help/c-activities/t-test-ab/test-ab.md) in plaats van een openingspagina-activiteit. Bij de A/B-testactiviteiten wordt niet van ervaring gewisseld voor dezelfde bezoeker.
   * Gebruik in plaats hiervan een [bezoekersprofiel](/help/c-target/c-audiences/c-target-rules/visitor-profile.md).

* Wanneer evaluatoren &quot;start/end with&quot; gebruiken voor tekenreeksen die komma&#39;s bevatten, worden deze tekenreeksen geëvalueerd als een array van waarden, waarin elke waarde die door komma&#39;s wordt gescheiden, wordt geëvalueerd. Als u bijvoorbeeld de waarde voor een koptekst hebt: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` komt in aanmerking voor voorwaarden zoals:
   * begint met zh,
   * begint met en,
   * eindigt met 0,7,
   * eindigt met 0,8.

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
