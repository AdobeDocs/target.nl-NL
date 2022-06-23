---
keywords: sitepagina's;doelsitepagina's;doel;huidige pagina;doel huidige pagina;vorige pagina;doel vorige pagina;landingspagina;doel landingspagina;http header
description: Leer hoe u bezoekers kunt aanwijzen met [!DNL Adobe Target] die zich op een specifieke pagina op uw site bevinden.
title: Kan ik bezoekers richten op basis van sitepagina's?
feature: Audiences
exl-id: 4c770b7b-775f-4483-aced-43f18a9a68c1
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Sitepagina&#39;s

U kunt bezoekers als doel instellen met [!DNL Adobe Target] die toegang hebben tot een specifieke pagina op uw site.

1. In de [!DNL Target] interface, klik **[!UICONTROL Audiences]** > **[!UICONTROL Create Audience]**.
1. Geef een naam op voor het publiek en voeg een optionele beschrijving toe.
1. Slepen en neerzetten **[!UICONTROL Site Pages]** in het deelvenster voor publieksopbouw.

   ![Sitepagina&#39;s, publiek](assets/target_site_pages.png)

1. Klik op de knop **[!UICONTROL Select]** vervolgkeuzelijst, selecteert u een van de volgende opties en configureert u vervolgens de regel naar wens.

   Welke opties en beoordelaars beschikbaar zijn in vervolgkeuzelijsten in de regel, is afhankelijk van de optie die u kiest. In de volgende afbeelding worden de beschikbare opties weergegeven als u [!UICONTROL Current Page]:

   ![Huidige pagina](assets/current-page.png)

   De volgende opties zijn beschikbaar in de eerste vervolgkeuzelijst wanneer u [!UICONTROL Select].

   * **[!UICONTROL Current Page]:** De pagina die de gebruiker bekijkt.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Voor meer informatie over hoe [!DNL Target] evalueert URLs, zie [Veelgestelde vragen over doelen en doelgroepen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]
   * **[!UICONTROL Previous Page]:** De pagina die de gebruiker heeft bekeken voordat deze op de huidige pagina klikte. De pagina wordt alleen bijgehouden als de gebruiker van de vorige pagina naar de huidige pagina klikt. De vorige pagina wordt niet bijgehouden als de gebruiker een nieuwe URL in browser typt. De feitelijke inhoud van deze pagina is afhankelijk van het ontwerp van uw site. Als op de huidige pagina bijvoorbeeld informatie over een bepaald product wordt weergegeven, is de vorige pagina mogelijk een categoriepagina waarop de bezoeker het specifieke item selecteert. Een pagina die bijvoorbeeld verschillende camera&#39;s van een bepaald type weergeeft, of de pagina &quot;home&quot; die tot de uiteindelijke pagina leidt.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Voor meer informatie over hoe het Doel URLs evalueert, zie [Veelgestelde vragen over doelen en doelgroepen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
   * **[!UICONTROL Landing Page]:** De openingspagina is de eerste pagina die de bezoeker ziet wanneer hij of zij uw site opent. Als de bezoeker bijvoorbeeld op een koppeling op Google klikt die naar een categoriepagina leidt, is de categoriepagina de landingspagina. Als de koppeling naar uw startpagina leidt, is de startpagina de bestemmingspagina. De landingspagina wordt onthouden voor de sessie van de bezoeker. U kunt de site dieper plaatsen op basis van de bestemmingspagina van de bezoeker in deze sessie.

      De tweede vervolgkeuzelijst bevat de volgende opties als u deze optie kiest:

      * [!UICONTROL URL] (Voor meer informatie over hoe het Doel URLs evalueert, zie [Veelgestelde vragen over doelen en doelgroepen](/help/main/c-target/c-troubleshooting-targets-and-audiences/troubleshooting-targets-and-audiences.md).)
      * [!UICONTROL Domain]
      * [!UICONTROL Query]
      * [!UICONTROL Subdomain]
      * [!UICONTROL Top-Level Domain]
      * [!UICONTROL Path]
      * [!UICONTROL Hash (#) fragment]

      >[!NOTE]
      >
      >De `landing.url` object wordt opnieuw ingesteld op een subdomeinwijziging of directe URL-vervanging.

   * **[!UICONTROL HTTP Header]:** Met deze optie wordt de informatie in de HTTP-header van het dialoogvenster [!DNL Target] verzoek. Als de HTTP-header bijvoorbeeld taalinformatie bevat, kunt u een regel maken die de `Accept-Language: es` voorwaarde voor doelbezoekers die de pagina in het Spaans openen.

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

   Als u [!UICONTROL Current Page], [!UICONTROL Previous Page], of [!UICONTROL Landing Page]de [!UICONTROL Domain] en [!UICONTROL Query] zijn beschikbaar. Houd rekening met het volgende wanneer u deze opties kiest:

   * **Domein:** Het volledige domein van de pagina. Als u een domein opgeeft, kunt u het beste &#39;contains&#39; gebruiken. &quot;Domain equals facebook.com&quot; accepteert bijvoorbeeld niet `m.facebook.com` of `www.facebook.com`. &quot;Domein bevat facebook.com&quot; accepteert elke variant van facebook.com.
   * **Query:** De inhoud van de URL na het eerste vraagteken (?).

      `foo.html?e0a72cb2a2c7`





1. (Optioneel) Stel aanvullende regels voor het publiek in.
1. Klik op **[!UICONTROL Done]**.

U kunt ook doelgroepen voor sitepagina&#39;s maken met behulp van uw eigen queryparameter &quot;door de gebruiker gedefinieerd&quot; of &quot;door de gebruiker gedefinieerde koptekst&quot;.

Gebruik een:

* De parameter van de vraag als de regel door de gebruiker wordt geselecteerd is [!UICONTROL Current Page], [!UICONTROL Landing Page], of [!UICONTROL Previous Page]
* Koptekst als de regel die de gebruiker heeft geselecteerd, een HTTP-koptekst is

## Problemen oplossen {#ts}

* Om ervoor te zorgen dat het publiek op de bestemmingspagina correct kan functioneren, moeten de aanvragen `mboxReferrer` parameterset (voor de bezorgings-API wordt de `context.address.referringUrl` parameter) die de JavaScript-bibliotheek at.js van de pagina neemt met behulp van de `document.referrer` kenmerk. Dit `HTMLDocument` dit kenmerk retourneert de URI van de pagina waarvandaan de gebruiker is genavigeerd. De waarde van dit kenmerk is een lege tekenreeks wanneer de gebruiker rechtstreeks naar de pagina navigeert (niet via een koppeling, maar bijvoorbeeld via een bladwijzer).

   Als dit gedrag niet aan uw vereisten voldoet, kunt u een van de volgende handelingen uitvoeren:

   * Voldoende [mbox-parameters](https://developer.adobe.com/target/implement/client-side/atjs/global-mbox/pass-parameters-to-global-mbox/) tot [!DNL Target] voor doeldoeleinden te gebruiken.
   * Een [A/B Testactiviteit](/help/main/c-activities/t-test-ab/test-ab.md) in plaats van een activiteit op een bestemmingspagina. Bij de A/B-testactiviteiten wordt niet van ervaring gewisseld voor dezelfde bezoeker.
   * Een [bezoekersprofiel](/help/main/c-target/c-audiences/c-target-rules/visitor-profile.md) in plaats daarvan.

* Wanneer evaluatoren &quot;start/end with&quot; gebruiken voor tekenreeksen die komma&#39;s bevatten, worden deze tekenreeksen geëvalueerd als een array van waarden, waarin elke waarde die door komma&#39;s wordt gescheiden, wordt geëvalueerd. Als u bijvoorbeeld de waarde voor een koptekst hebt: `Accept-Language: en,zh;q=0.9,en-IN;q=0.8,zh-CN;q=0.7` het komt in aanmerking voor voorwaarden zoals :
   * begint met zh,
   * begint met en,
   * eindigt met 0,7,
   * eindigt met 0,8.

## Trainingsvideo: Soorten publiek maken

Deze video bevat informatie over het gebruik van publiekscategorieën.

* Soorten publiek maken
* Doelcategorieën definiëren

>[!VIDEO](https://video.tv.adobe.com/v/17392)
