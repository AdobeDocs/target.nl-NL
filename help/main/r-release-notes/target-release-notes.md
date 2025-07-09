---
keywords: releaseopmerkingen;releases;updates;toekomstige release;verbeteringen;nieuwe functies;oplossingen;updates;vooruitgave;vroege toegang
description: Leer over de nieuwe eigenschappen, de verhogingen, en de moeilijke situaties inbegrepen in de aanstaande versie van  [!DNL Adobe Target], met inbegrip van SDKs, APIs, en de bibliotheken van JavaScript.
title: Welke Nieuwe Eigenschappen en de Verbeteringen worden omvat in de aanstaande  [!DNL Target]  Versie?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: dd7ec2fe38ea5bb6d34bdbf44876c291b356fc17
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# [!DNL Target] releaseopmerkingen (pre-release)

Dit artikel bevat pre-releasegegevens voor komende [!DNL Adobe Target] versies, waaronder SDK&#39;s, API&#39;s en JavaScript-bibliotheken.

**Laatst bijgewerkt: 9 juli, 2025**

>[!NOTE]
>
>* Releasedatums, -functies en andere informatie kunnen zonder voorafgaande kennisgeving worden gewijzigd.
>
>* Om informatie over de huidige versie te bekijken, zie {de Nota&#39;s van de Versie van het 0} Doel [.](release-notes.md)
>
>* De uitgiftenummers tussen haakjes zijn bedoeld voor intern gebruik door [!DNL Adobe] .

## [!DNL Target Standard/Premium] 25.7.1 (9 juli 2025)

Vanwege recente problemen die zijn vastgesteld en die voornamelijk verband houden met complexe klantaanpassingen, bevat deze release de volgende oplossingen en updates:

**Activiteiten**

* Probleem verholpen waarbij de URL van [!UICONTROL Activity QA] een overbodige queryparameter bevatte: `at_preview_evaluate_as_true_audience_ids` . (TGT-52907)
* Probleem verholpen waarbij voorvertoning-URL&#39;s ten onrechte meer soorten publiek bevatte dan expliciet door de gebruiker werd getypt. Dit gedrag is gecorrigeerd om ervoor te zorgen dat alleen het opgegeven publiek wordt toegepast wanneer een koppeling voor een kwaliteitscontrole of voorvertoning wordt gegenereerd. (TGT-52912)
* Probleem verholpen waardoor gebruikers [!UICONTROL Auto-Target] (AT)-activiteiten niet konden maken als [!UICONTROL Auto-Allocate] (AA) als eerste is geselecteerd tijdens de installatie van de verkeerstoewijzing. Dit probleem heeft geresulteerd in een validatiefout voor de back-end en voorkomt dat de activiteit wordt opgeslagen. (TGT-53096)

**Soorten publiek**

* Probleem verholpen waarbij gebruikers met de rol [!UICONTROL Approver] geen publieksverfijningen met alleen activiteit konden toevoegen of opslaan. Het proberen dit te doen resulteerde in een 403 Verboden fout, die dat het &quot;[ redacteur ]&quot;voorrecht werd vereist, alhoewel de gebruiker voldoende toestemmingen had om activiteiten goed te keuren en te beheren. (TGT-52984)
* Probleem verholpen waarbij een activiteitsspecifiek publiek werd verwijderd met de optie [!UICONTROL Remove Audience Refinement] , wordt het publiek niet langer weergegeven in de publiekslijst voor herselectie binnen dezelfde activiteit. Dit gedrag verhindert gebruikers het zelfde publiek opnieuw toe te voegen tenzij het van kras wordt ontspannen. (TGT-52979)
* Probleem verholpen waarbij de alleen voor activiteit bedoelde publieksverfijningen direct uit de gebruikersinterface verdwenen nadat ze van een locatie waren verwijderd, zelfs voordat de activiteit was opgeslagen. Dit gedrag druist in tegen de verwachte functionaliteit en de knopinfo-richtlijnen, die als volgt luiden: &quot;Alle ongebruikte soorten publiek uit deze bibliotheek worden verwijderd wanneer de activiteit wordt opgeslagen.&quot; (TGT-52982)
* Probleem verholpen bij pogingen om een ander publiek dan [!UICONTROL All Visitors] toe te wijzen aan een activiteit. Na het opslaan wordt het volgende foutbericht weergegeven: &quot;We kunnen uw verzoek niet voltooien. Neem contact op met [!UICONTROL Adobe Client Care] als het probleem zich blijft voordoen.&quot; (TGT-53008)
* Probleem verholpen waarbij het opslaan van een activiteit werd geblokkeerd na het maken en toewijzen van een nieuw publiek in de activity editor. Het weergegeven foutbericht was: &quot;We kunnen uw verzoek niet voltooien. Neem contact op met [!UICONTROL Adobe Client Care] als het probleem zich blijft voordoen.&quot; (TGT-52977)

**[!UICONTROL Analytics for Target] (A4T)**

* Probleem verholpen waarbij het kopiëren van een bestaande activiteit en het wijzigen van de rapportbron in [!DNL Adobe Analytics] (A4T) zou resulteren in een fout met betrekking tot &quot;Ongeldige gebruikersinvoer&quot;. De fout werd geactiveerd wanneer bepaalde metrische handelingen die niet compatibel zijn met [!DNL Analytics] -rapportage, zoals `restart_same_experience` , `restart_random_experience` en `restart_new_experience` , niet in de oorspronkelijke activiteit zijn opgenomen. (TGT-52900)
* Probleem verholpen waarbij klanten werden verhinderd een activiteit te maken of op te slaan wanneer ze [!DNL Adobe Analytics] (A4T) als rapportbron in de stap [!UICONTROL Goals & Settings] selecteerden. Het probleem is specifiek opgetreden bij het selecteren van een [!UICONTROL Custom Event] metrische waarde (bijvoorbeeld &#39;Aangepaste gebeurtenis 16&#39;). Dit heeft de volgende fout tot gevolg: &#39;Ongeldige gebruikersinvoer&#39;. (TGT-52910)
* Probleem verholpen waarbij gebruikers door te klikken op de koppeling &quot;[!UICONTROL View in Analytics]&quot; werden omgeleid naar de startpagina in plaats van naar het bedoelde [!DNL Analytics] -dashboard. (TGT-53092 &amp; TGT-53093)
* Probleem verholpen waarbij een bestaande activiteit werd gekloond en de rapportbron werd gewijzigd van [!DNL Target] in [!DNL Adobe Analytics] , kregen gebruikers een fout van het type &quot;400 - Ongeldige gebruikersinvoer&quot; te zien, waardoor de activiteit niet kon worden opgeslagen. (TGT-52875)
* Probleem verholpen waarbij een [!DNL Recommendations] -activiteit in de bijgewerkte [!UICONTROL Overview] UI werd weergegeven. De sectie [!UICONTROL Goals & Settings] wordt niet geladen wanneer [!DNL Adobe Analytics] (A4T) als rapportbron is geselecteerd. Het volgende foutbericht werd weergegeven: &quot;Er is iets misgegaan. Je aanvraag kan niet worden voltooid. Neem contact op met de Adobe Client Care als het probleem zich blijft voordoen.&quot; (TGT-52999)

**[!UICONTROL Experiences]en[!UICONTROL Offers]**

* Probleem verholpen waarbij het gebruik van de functie [!UICONTROL Manage Content] in [!UICONTROL Automated Personalization] -activiteiten (AP) ertoe leidde dat de pagina vastliep en leeg bleef. Dit probleem is opgetreden nadat u in inhoudsbeheer op [!UICONTROL Done] had geklikt, met name bij activiteiten die in de bijgewerkte gebruikersinterface zijn gemaakt of bewerkt. (TGT-53047)
* Probleem verholpen waarbij de functie [!UICONTROL Manage Content] de status van een locatie niet correct valideerde nadat alle inhoudsopties waren verwijderd. Dit kan leiden tot inconsistente gedragingen of fouten bij het opslaan of doorgaan met de activiteitenconfiguratie. (TGT-52801)
* Probleem verholpen waarbij gebruikers een &#39;&#39;Ongeldige invoerfout&#39;&#39; tegenkwamen bij het toevoegen van een nieuwe pagina en het verwijderen van specifieke elementen uit verschillende ervaringen. De fout werd veroorzaakt door dubbel `LocalIds` die tijdens elementmanipulatie wordt geproduceerd, in het bijzonder wanneer het schakelen tussen ervaringen en het wijzigen van gedeelde paginastructuren. (TGT-52720)
* Het probleem waarbij het gebruik van de functie [!UICONTROL Generate Adhoc Offer] tot ongedefinieerde locaties in het deelvenster [!UICONTROL Manage Content] leidde, is opgelost. (TGT-53076 &amp; TGT-53070)
* Verduidelijkt het gedrag voor de klant waar wijzigingen die met een HTML-aanbieding zijn aangebracht, mogelijk ontbreken wanneer u van de stap [!UICONTROL Targeting] terug naar [!UICONTROL Experiences] navigeert. Voor deze klant heeft de desbetreffende website dynamisch meerdere DOM-kiezers gegenereerd die zijn gewijzigd bij het laden van elke pagina. Hierdoor kan de kiezer die oorspronkelijk voor de wijziging is gebruikt, niet worden gevonden wanneer de editor opnieuw wordt geopend, waardoor de wijziging ontbreekt of ongeldig wordt weergegeven. Dit werkt zoals ontworpen. Om ervoor te zorgen dat de wijzigingen in de redacteur visueel blijven, adviseert men dat de cliënten stabiele, verenigbare selecteurs gebruiken die niet over paginaatherladingen veranderen. (TGT-52874)
* Probleem verholpen waarbij het verwijderen of deactiveren van een aanbieding die deel uitmaakte van een uitgesloten ervaring, leidde tot een fout met betrekking tot &quot;Ongeldige gebruikersinvoer&quot;. Dit probleem kwam aan de orde, ook al werd het aanbod niet actief gebruikt in de meegeleverde ervaringen. (TGT-52917)

**vorm-Gebaseerde Composer van de Ervaring**

* Probleem verholpen met op formulieren gebaseerde activiteiten waarbij het dupliceren van een ervaring en het bewerken van de aangepaste code in een van de gedupliceerde ervaringen onbedoeld deze wijzigingen op alle gedupliceerde ervaringen toepast. Elke ervaring behoudt nu zijn eigen aangepaste code onafhankelijk na duplicatie. (TGT-51600)

**Localization**

* Probleem met contextuele vertaling in de Koreaanse landinstelling (ko-KR) voor de tekenreeks &quot;Preview Experience&quot; opgelost. (TGT-52928)
* Correctie van terminologische inconsistenties die zijn geïdentificeerd in de Vereenvoudigde Chinese (zh_CN) vertaling van verschillende tekstreeksen. (TGT-52954 &amp; TGT-52955)

**[!DNL Recommendations]**

* Toegevoegd een nieuwe [!DNL Recommendations] voer [ status ](/help/main/c-recommendations/c-products/feeds.md#status): [!UICONTROL Partial Import Failed]. (kB-2215)
* Probleem verholpen dat invloed had op de workflow voor het maken van activiteiten tijdens het toevoegen van [!DNL Recommendations] met [!UICONTROL promotions] . Wanneer de gebruikers &quot; [!UICONTROL Promote by Attribute]&quot;selecteerden en een het filtreren regel (bijvoorbeeld, [!UICONTROL Parameter Matching]) toevoegden, werden het geselecteerde regeltype en de operandwaarden niet bewaard na het bewaren en het heruitgeven van de activiteit. Bij het opnieuw openen zou het filterregeltype onverwacht veranderen en zouden operandwaarden ontbreken. (TGT-53059)
* Probleem verholpen in de gebruikersinterface van [!DNL Recommendations] waarbij een promotie die met één regel is gemaakt, onjuist werd geïnterpreteerd en weergegeven als een promotietype Lijst met objecten, ongeacht de logica van de regel. (TGT-53063)
* Oplossing een kwestie toen het gebruiken van bijgewerkte [!UICONTROL Overview] UI, de &quot;[!UICONTROL Download Recommendations Data]&quot;knoop mist voor [!UICONTROL Experience Targeting] (XT) activiteiten die [!DNL Recommendations] omvatten. (TGT-52730 &amp; TGT-52756)
* Eerder werd in de gebruikersinterface van Aanbevelingen alleen het aantal entiteiten weergegeven dat is geïmporteerd uit een feed. De notatie voor het achterste bericht bevat echter zowel het aantal geïmporteerde entiteiten als het totale aantal entiteiten in de notatie:

  `# of entities imported / # of total entities`

  Door deze discrepantie zagen gebruikers alleen de eerste waarde (geïmporteerd aantal) in de gebruikersinterface, wat tot verwarring leidde. In de gebruikersinterface worden nu beide getallen weergegeven. (TGT-53073)

**Rapporten**

* Probleem verholpen waarbij door het selecteren van &quot;[!UICONTROL Export order details to CSV]&quot; op de [!UICONTROL Reports] -pagina een leeg bestand werd gedownload. Deze kwestie kwam zelfs voor wanneer de geldige ordegegevens in de activiteit aanwezig waren. (TGT-5225)
* Probleem verholpen tijdens het opslaan van een activiteit na het maken en toewijzen van een nieuw rapportagepubliek. Het geretourneerde foutbericht is: &quot;Toegang geweigerd. Om deze verrichting uit te voeren, worden alle volgende voorrechten vereist: [ redacteur ].&quot; Dit probleem is opgetreden ondanks het feit dat de gebruiker toegang op goedkeuringsniveau heeft. (TGT-53103)

**[!UICONTROL Visual Experience Composer] (VEC)**

* Oplossing voor een probleem waarbij het toepassen van een wijziging op een weergave ertoe zou leiden dat de weergave wordt gedupliceerd en dat de activiteit een fout met &quot;Ongeldige gebruikersinvoer&quot; retourneert. Met deze correctie zorgt u ervoor dat weergavewijzigingen correct worden toegepast zonder dat er fouten optreden bij het dupliceren of valideren. (TGT-52886)
* Probleem verholpen waarbij aangepaste codewijzigingen onjuist werden weergegeven voor een verkeerde ervaring. Met name veranderingen die voor één ervaring bedoeld waren, werden in een andere ervaring aangetoond, wat tot verwarring en mogelijke verkeerde configuratie van de activiteiten in het leven heeft geleid. (TGT-52776)
* Probleem verholpen waarbij het bewerken of opslaan van aangepaste codewijzigingen in de nieuwe VEC-interface werd voorkomen. Specifiek:

   * Nadat u een aangepast codeblok hebt bewerkt en opgeslagen, zijn de wijzigingen niet doorgevoerd in de gebruikersinterface of in de voorvertoning van de kwaliteitscontrole.
   * In sommige gevallen kunnen wijzigingen alleen worden verwijderd als de activiteit wordt gesloten en opnieuw wordt geopend.
   * Als tussenoplossing moesten gebruikers de code kopiëren, de wijziging verwijderen en handmatig opnieuw maken met de bijgewerkte inhoud. (TGT-53072)

* Probleem verholpen waarbij het bewerken en opslaan van aangepaste code ertoe leidde dat het deelvenster [!UICONTROL Modifications] niet meer reageerde. (TGT-53075)
* Correctie van een probleem waarbij wijzigingen die in ervaringen met varianten in aangepaste code zijn aangebracht, onbedoeld in de [!UICONTROL Control] -ervaring werden doorgevoerd. Dit leidde tot onbedoelde veranderingen in het gedrag van de bevalling. De ervaring van [!UICONTROL Control] blijft nu geïsoleerd van aangepaste code-bewerkingen die op andere ervaringen zijn toegepast. (TGT-52413)
* Probleem verholpen waarbij wijzigingen die zijn aangebracht in een ervaring (bijvoorbeeld Experience B) per ongeluk werden gedupliceerd naar een andere ervaring (Experience A) als de gebruiker op de tweede ervaring had geklikt voordat de editor volledig geladen was. Dit gedrag kan er ook toe leiden dat wijzigingen verloren gaan als de oorspronkelijk geselecteerde ervaring geen wijzigingen bevat. (TGT-52597)
* Correctie van een probleem waarbij wijzigingen die zijn aangebracht in de stap [!UICONTROL Modifications] voor het maken van activiteiten, niet consistent werden opgeslagen. In sommige gevallen zou het aangepaste script dat u in de sectie [!UICONTROL Save] hebt toegevoegd, na alle stappen te hebben voltooid en op [!UICONTROL Modifications] te hebben geklikt, niet meer op de livesite worden weerspiegeld, ondanks geen zichtbare fouten tijdens het opslagproces. (TGT-52661)
* Probleem verholpen waarbij wijzigingen in aangepaste code niet correct werden opgeslagen en onbedoeld werden weerspiegeld in meerdere ervaringen binnen dezelfde activiteit. Bovendien stuitten gebruikers op toegangsproblemen bij het openen of vernieuwen van bepaalde activiteiten, wat leidde tot lege schermen. Deze problemen zijn nu opgelost om te zorgen voor een stabiele bewerking van activiteiten en een nauwkeurige isolatie van ervaringen. (TGT-52594)
* Probleem verholpen waarbij gebruikers in [!UICONTROL Browse Mode] niet naar een andere URL konden bladeren. Hierdoor konden testers en editors geen alternatieve pagina&#39;s valideren of voorvertonen binnen dezelfde activiteitensessie. (TGT-53052)
* Probleem verholpen waarbij meerdere [!UICONTROL Visual Experience Composer] (VEC) instanties tegelijkertijd werden geopend tijdens het maken van activiteiten. Dit probleem is opgetreden wanneer gebruikers [!UICONTROL Enhanced Experience Composer] (EEC) hadden uitgeschakeld en de slash van de URL van de website in de stap [!UICONTROL Page Delivery] hadden verwijderd. (TGT-52782)
* Probleem verholpen waarbij de [!UICONTROL Revenue] metrische vervolgkeuzelijst in de stap [!UICONTROL Goals & Settings] onjuist zou worden standaard op [!UICONTROL Revenue per Visit] (RPVISIT), zelfs nadat de gebruiker een andere maatstaf had geselecteerd.  Er is een probleem opgetreden bij het samenvouwen en opnieuw uitvouwen van het configuratievenster voor metrische gegevens, waardoor de eerder geselecteerde waarde opnieuw is ingesteld. (TGT-52811 &amp; TGT-52878)
* Oplossing voor verschillende problemen in de workflow voor het maken van activiteiten met betrekking tot het aanbieden van naamgeving en het vertalen van inhoud in [!UICONTROL Automated Personalization] (AP)- en [!UICONTROL Multivariate Testing] (MVT)-activiteiten:

  Belangrijkste problemen opgelost:

   * Het maken van meerdere HTML-aanbiedingen met dezelfde naam (bijvoorbeeld &#39;Experience&#39;) heeft geleid tot de fout &#39;Dubbele aanbiedingsnamen zijn niet toegestaan&#39;, maar de interface gaf niet duidelijk aan welke aanbiedingen het conflict veroorzaakten.
   * Als de naam van aanbiedingen wordt gewijzigd via het rechterdeelvenster, wordt de naam bijgewerkt in de gebruikersinterface, maar de wijziging wordt niet doorgevoerd op het tabblad [!UICONTROL Manage Content] of [!UICONTROL Offers] , waardoor er permanente validatiefouten optreden.
   * In MVT-activiteiten bleef de fout met de dubbele naam weliswaar niet bestaan na het wijzigen van de naam, maar de interface gaf nog steeds geen consistente weerspiegeling van bijgewerkte aanbiedingsnamen op de verschillende tabbladen. (TGT-52933)

## Aanvullende opmerkingen bij de release en versiedetails

| Bron | Details |
|--- |--- |
| [ de nota&#39;s van de Versie: Het Web SDK van de Ervaring van het Platform van Adobe Target ] (https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=e n) | Details over veranderingen in elke versie van het Web SDK van het Platform. |
| [ at.js versiedetails ](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank} | Informatie over de wijzigingen in elke versie van de JavaScript-bibliotheek [!DNL Adobe Target] at.js. |

## Prerelease-informatie {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Als u geavanceerde meldingen wilt ontvangen over aanstaande productverbeteringen in [!DNL Target] en andere [!DNL Adobe Experience Cloud] -oplossingen, meldt u zich aan voor [!DNL Adobe Priority Product Update] :

[ https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
