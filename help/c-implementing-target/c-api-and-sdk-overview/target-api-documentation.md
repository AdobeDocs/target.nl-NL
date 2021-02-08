---
keywords: api;adobe i/o
description: Leer hoe u van de klassieke Adobe Target API's van oudere API's naar de nieuwe API's op Adobe I/O overschakelt.
title: Hoe kan ik overstappen van verouderde API's naar Adobe I/O?
feature: Implement Server-side
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---


# Overgang van verouderde API&#39;s van Target naar Adobe I/O

Informatie die u helpt bij het gebruik van de overgang van de verouderde API&#39;s van het Doel naar de nieuwe API&#39;s op Adobe I/O.

Met de buitenbedrijfstelling van Adobe Target Classic zijn de API&#39;s die zijn verbonden met uw Target Classic-account ook niet beschikbaar. Dit document helpt u bij de overgang van uw verouderde API-integratie naar de doel-API&#39;s die door Adobe I/O worden aangedreven.

Voor meer informatie over de documentatie van doel API, zie [Doel APIs en NodeJS SDK](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md#concept_5718EC1FF2ED4436935D0BCCD7AA29A6).

## Terminologie {#section_D8286EDAE3B24D208DA432AEF2E88FD9}

| Term | Beschrijving |
|--- |--- |
| Verouderde API | API&#39;s die zijn gekoppeld aan uw Classic-doelaccount. Deze API-aanroepen zijn gebaseerd op een gebruikersbenaming en op een wachtwoord gebaseerde verificatie en gebruiken de hostnaam `testandtarget.omniture.com`. Als uw API-aanroepen een gebruikersnaam en wachtwoord bevatten in de aanvraag-URL, moet u een overgang maken naar Adobe I/O API&#39;s. |
| Adobe I/O | Adobe I/O is de nieuwe gateway voor doel APIs. Deze API&#39;s zijn verbonden met uw Target Standard/Premium-account. De doel-API&#39;s op Adobe I/O maken gebruik van een JWT-verificatie, de industriestandaard voor veilige bedrijf-API&#39;s. |

## Tijdlijn {#section_A478EBF637554A2DB5A31661955121ED}

De oudere API&#39;s worden uit bedrijf genomen wanneer u de optie voor het uit bedrijf nemen van de Classic-doelserver gebruikt:

| Datum | Details |
|--- |--- |
| 17 oktober 2017 | Alle API methodes die een schrijfverrichting (`saveCampaign`, `copyCampaign`, `saveHTMLOfferContent`, en `setCampaignState`) uitvoeren werden ontmanteld.<br>Dit is dezelfde datum waarop alle Classic doelgebruikersaccounts zijn ingesteld op de status Alleen-lezen. |
| 14 november 2017 | De overige API&#39;s zijn uit bedrijf genomen. Dit is de datum waarop de Klassieke gebruikersinterface van het Doel werd ontmanteld |

Recommendations Classic API&#39;s worden niet beïnvloed door deze tijdlijn.

## Equivalente methoden {#section_DDB42CCC172545B09CB728D794CC466B}

De volgende tabel bevat een lijst met equivalente nieuwe doel-API-methoden voor de oudere API-methoden. De nieuwe API&#39;s retourneren JSON in vergelijking met de XML-respons van de verouderde API&#39;s.

De nieuwe API-methoden zijn gekoppeld aan de corresponderende sectie in de API-documentatiesite. Voor elke API-methode wordt een voorbeeld gegeven. U kunt ook de Admin Postman Collection gebruiken die steekproefAPI vraag voor alle nieuwe Adobe API methodes op Adobe I/O bevat.

| Groepering | Oudere API-methode | Nieuwe API-methode | Notities |
|--- |--- |--- |--- |
| Campagne/activiteit | Campagne maken | [AB-](http://developers.adobetarget.com/api/#create-ab-activity)<br>[activiteit maken](http://developers.adobetarget.com/api/#create-xt-activity) | De nieuwe APIs verstrekt afzonderlijke creeert methodes voor AB en XT |
|  | Campagne bijwerken | [AB ](http://developers.adobetarget.com/api/#update-ab-activity)<br>[ActivityUpdate XT-activiteit bijwerken](http://developers.adobetarget.com/api/#update-xt-activity) |  |
|  | Campagne kopiëren | N.v.t. | De API&#39;s voor het maken van activiteiten gebruiken |
|  | Lijst met campagnes | [Lijstactiviteiten](http://developers.adobetarget.com/api/#list-activities) |  |
|  | Campagnestaat | [Activiteitenstatus bijwerken](http://developers.adobetarget.com/api/#update-activity-state) |  |
|  | Campagneweergave | [Krijg Activiteit van AB door ](http://developers.adobetarget.com/api/#get-ab-activity-by-id)<br>[activiteit IDGet XT door identiteitskaart](http://developers.adobetarget.com/api/#get-xt-activity-by-id) |  |
|  | Campagne-id van derden | N.v.t. | Als u een id van een andere leverancier gebruikt, kunnen de relevante activiteitsmethoden worden gebruikt |
| Aanbiedingen | Voorstel maken | [Voorstel maken](http://developers.adobetarget.com/api/#create-offer) |  |
|  | Voorstel ophalen | [Voorstel ophalen op ID](http://developers.adobetarget.com/api/#get-offer-by-id) |  |
|  | Aanbiedingslijst | [Aanbiedingen](http://developers.adobetarget.com/api/#list-offers) |  |
|  | Maplijst | N.v.t. | Mappen worden niet ondersteund in Target Standard/Premium |
| Rapportage | Rapport Campagneprestaties | [Get AB Performance ](http://developers.adobetarget.com/api/#get-ab-performance-report)<br>[ReportGet XT Performance Report](http://developers.adobetarget.com/api/#get-xt-performance-report) |  |
|  | Controlerapport | [Controlerapport ophalen](http://developers.adobetarget.com/api/#get-audit-report) |  |
|  | 1-1 Inhoudsrapport | [AP-prestatierapport ophalen](http://developers.adobetarget.com/api/#get-ap-activity-performance-report) |  |
| Accountinstellingen | Hostgroepen ophalen | [Omgevingen weergeven](http://developers.adobetarget.com/api/#list-environments) |  |

## Uitzonderingen {#section_09CF9A0E289149279783B4801D1B6D4C}

Neem contact op met de succesmanager van de klant als u een uitzondering nodig hebt.

## Help {#section_591F850E2B7A4342B1C233693425415C}

Neem contact op met de Adobe Target Client Care (tt-support@adobe.com) als u vragen hebt of hulp nodig hebt bij de overgang naar de nieuwe doel-API&#39;s op Adobe I/O.
