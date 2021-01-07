---
keywords: Browsers;Prerequisites;Requirements;internet explorer;chrome;firefox;safari;android;surface
description: De Adobe Target-toepassing en de levering van inhoud zijn getest voor een groot aantal browsers en apparaten.
title: Ondersteunde browsers
feature: Implementation
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---


# Ondersteunde browsers

De [!DNL Adobe Target]-toepassing en de levering van inhoud zijn getest voor een groot aantal browsers en apparaten.

Voor extra belangrijke informatie over TLS, zie [TLS (de Veiligheid van de Laag van het Vervoer) de Veranderingen van de Encryptie](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451).

## [!DNL Target] Standaard/Premium-interface  {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

De [!DNL Target] interface steunt de volgende browsers en de apparaten:

| Apparaattype | Browserversie |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome (nieuwste, nieuwste min 1)</li><li>Mozilla Firefox (nieuwste, nieuwste min 1)</li></ul> |
| Mac | <ul><li>Firefox (nieuwste, nieuwste min 1)</li><li>Chroom (nieuwste, nieuwste min 1)</li></ul> |

## Inhoudslevering {#section_1045A946056441268D40025529918D3D}

De levering van inhoud is getest in de volgende browsers en apparaten:

| Apparaattype | Browserversie |
|--- |--- |
| Windows | <ul><li>Internet Explorer 9 en 10. Getest in emulatiemodus.<br>**Opmerking**: in.js 1.3.0 (en hoger) biedt geen ondersteuning meer voor de levering van inhoud in Microsoft Internet Explorer 9.</li><li>Internet Explorer 11</li><li>Microsoft Edge</li><li>Chroom (nieuwste, nieuwste min 1)</li><li>Firefox (nieuwste, nieuwste min 1)</li></ul> |
| Mac | <ul><li>Apple Safari (Latest)<br>**Opmerking**: Voor meer informatie over hoe Safari eerste en derdekoekjes behandelt, zie [Cookie van het Doel](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/cookie-behavior.md).</li><li>Firefox (nieuwste, nieuwste min 1)</li><li>Chroom (nieuwste, nieuwste min 1)</li></ul> |
| Mobiel/tablet | <ul><li>Apple iOS (nieuwste)</li><li>Android-apparaten en -tablets (Android 4 en hoger)</li><li>Microsoft Surface (Windows 8.1)</li></ul> |

Let op het volgende:

* Voor [!DNL at.js]-implementaties geeft [!DNL Target] standaardinhoud weer in eerdere versies van Internet Explorer en mogelijk in eerdere versies van de hierboven vermelde browsers. Voor [!DNL mbox.js] implementaties, [!DNL Target] probeert om inhoud terug te geven maar zou niet succesvol kunnen zijn.
* Internet Explorer behandelt alle onbekende elementen (zoals aangepaste elementen) als hetzelfde elementtype. Dientengevolge, zal de levering niet met douaneelementen werken.
* [!DNL Target] Hiermee geeft u de standaardinhoud weer in browsers die hierboven niet worden vermeld en in browsers die de  [modus](https://en.wikipedia.org/wiki/Quirks_mode) Kirken gebruiken. at.js vereist een documenttype dat op standaardwijze teruggeeft, bijvoorbeeld: `<!DOCTYPE html>` .
* De Adobe-leveringsinfrastructuur wordt na 12 september 2018 beveiligd om GEEN TLS 1.0-apparaten en browsers te ondersteunen. Zie [TLS (de Veiligheid van de Laag van het Vervoer) de Veranderingen van de Encryptie ](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md#concept_CC1001E9D3AE4BABAF90B8311B0A6451) om het algemene effect van deze verandering te begrijpen.
