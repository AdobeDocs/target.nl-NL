---
keywords: browsers;Eerste vereisten;Eisen;Internet Explorer;chroom;Firefox;safari;android;oppervlak
description: Ontdek welke internetbrowsers Adobe [!DNL Target] ondersteunt de interface en de levering van inhoud.
title: Wat browsers doen [!DNL Target] Ondersteuning?
feature: Implementation
role: Developer
exl-id: 8a366c79-d944-4d44-be5a-7c4f65385beb
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Ondersteunde browsers

De [!DNL Adobe Target] de toepassing en de inhoudslevering zijn getest in een groot aantal browsers en apparaten.

Voor meer belangrijke informatie over TLS raadpleegt u [Wijzigingen in TLS-codering (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/).

## [!DNL Target] Standaard/Premium-interface {#section_1B73CA4B7BBC460BB7009DF00A2AFC4D}

De [!DNL Target] interface ondersteunt de volgende browsers en apparaten:

| Apparaattype | Browserversie |
|--- |--- |
| Windows | <ul><li>Microsoft Edge</li><li>Google Chrome (laatste, laatste min 1)</li><li>Mozilla Firefox (laatste, laatste min 1)</li></ul> |
| Mac | <ul><li>Firefox (laatste, laatste min 1)</li><li>Chrome (nieuwste, laatste min 1)</li></ul> |

## Inhoud leveren {#section_1045A946056441268D40025529918D3D}

De levering van inhoud is getest in de volgende browsers en apparaten:

| Apparaattype | Browserversie |
|--- |--- |
| Windows | <ul><li>Microsoft Internet Explorer 9 en 10. Getest in emulatiemodus.<br>**Opmerking**: Inhoudslevering op IE 9 wordt niet meer ondersteund met at.js 1.3.0 (en hoger). De levering van inhoud op IE 10, 11, en alle oudere versies wordt niet meer gesteund met at.js 2.5.0 (en later).</li><li>Internet Explorer 11 <br>**Opmerking**: De levering van inhoud op IE 10, 11, en alle oudere versies wordt niet meer gesteund met at.js 2.5.0 (en later).</li><li>Microsoft Edge</li><li>Chrome (nieuwste, laatste min 1)</li><li>Firefox (laatste, laatste min 1)</li></ul> |
| Mac | <ul><li>Apple Safari (nieuwste)<br>**Opmerking**: Voor meer informatie over hoe Safari first- en derdekoekjes behandelt, zie [Doelcookie](https://developer.adobe.com/target/before-implement/privacy/cookie-behavior/).</li><li>Firefox (laatste, laatste min 1)</li><li>Chrome (nieuwste, laatste min 1)</li></ul> |
| Mobiel/tablet | <ul><li>Apple iOS (nieuwste)</li><li>Android-apparaten en -tablets (Android 4 en hoger)</li><li>Microsoft-oppervlak (Windows 8.1)</li></ul> |

Let op het volgende:

* Voor [!DNL at.js] implementaties, [!DNL Target] Hiermee geeft u standaardinhoud weer in eerdere versies van Internet Explorer en mogelijk in eerdere versies van de hierboven vermelde browsers.
* Internet Explorer behandelt alle onbekende elementen (zoals aangepaste elementen) als hetzelfde elementtype. Dientengevolge, werkt de levering niet met douaneelementen.
* [!DNL Target] geeft standaardinhoud weer in browsers die hierboven niet worden vermeld en in browsers die [quirks, modus](https://en.wikipedia.org/wiki/Quirks_mode). at.js vereist een documenttype dat op standaardwijze teruggeeft, bijvoorbeeld: `<!DOCTYPE html>` .
* De Adobe-leveringsinfrastructuur wordt na 12 september 2018 beveiligd om GEEN TLS 1.0-apparaten en browsers te ondersteunen. Zie [Wijzigingen in TLS-codering (Transport Layer Security)](https://developer.adobe.com/target/before-implement/tls-transport-layer-security-encryption/) inzicht te krijgen in de algemene gevolgen van deze wijziging.
