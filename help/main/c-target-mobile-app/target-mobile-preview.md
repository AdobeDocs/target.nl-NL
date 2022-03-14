---
keywords: qa;voorvertoning;voorvertoningskoppeling;mobiel;mobiele voorvertoning
description: Gebruik koppelingen voor mobiele voorvertoningen om end-to-end kwaliteitscontroles uit te voeren voor mobiele toepassingsactiviteiten. U kunt zich inschrijven voor verschillende ervaringen zonder speciale testapparaten.
title: Hoe gebruik ik de koppeling Mobiele voorvertoning in [!DNL Target] Mobiel?
feature: Implement Mobile
role: Developer
exl-id: c66325b3-3995-401e-a1e3-839fdb1cf762
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%

---

# Voorvertoning voor mobiele doelversie

Gebruik de koppeling voor mobiele voorvertoningen om eenvoudige end-to-end QA&#39;s voor mobiele app-activiteiten uit te voeren en uzelf in te schrijven voor verschillende ervaringen op uw apparaat zonder speciale testapparaten.

>[!NOTE]
>
>Voor de functie voor mobiele voorvertoningen moet u de juiste 4.14 (of hoger) versie van de Adobe Mobile SDK downloaden en installeren.

## Overzicht {#section_981D6FA4AEE64098809EA606E89E4A5E}

Met de functie voor mobiele voorvertoningen kunt u uw mobiele-toepassingsactiviteiten volledig testen voordat u deze live start.

## Vereisten {#section_A763C564C9E84B0EB448237B5B1E4068}

1. **Gebruik een ondersteunde versie van de SDK:** Voor de functie voor mobiele voorvertoningen moet u de juiste versie 4.14 (of hoger) van de Adobe Mobile SDK downloaden en installeren in de corresponderende apps.

   Voor instructies voor het downloaden van de juiste SDK raadpleegt u:

   * **iOS:** [Voordat u begint](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/requirements.html) in de *iOS Help voor mobiele services*.
   * **Android:** [Voordat u begint](https://experienceleague.adobe.com/docs/mobile-services/android/getting-started-android/requirements.html) in de *Help bij Mobile Services Android*.

1. **Een URL-schema instellen:** De voorbeeldkoppeling gebruikt een URL-schema om uw app te openen. U moet een uniek URL-schema opgeven voor de voorvertoning.

   De volgende illustratie is een voorbeeld op iOS:

   ![](assets/mobile-preview-url-scheme-ios.png)

   De volgende afbeelding is een voorbeeld op Android:

   ![](assets/Android_Deeplink.png)

1. **Track Adobe DeepLink**

   **iOS:** In de toepassingsafgevaardigde, vraag `[ADBMobile trackAdobeDeepLink:url` wanneer de gedelegeerde wordt gevraagd om de bron te openen met het URL-schema dat in de vorige stap is opgegeven.

   Het volgende codefragment is een voorbeeld:

   ```javascript
   - (BOOL) application:(UIApplication *)app openURL:(NSURL *)url 
                options:(NSDictionary<NSString *,id> *)options { 
   
       if ([[url scheme] isEqualToString:@"com.adobe.targetmobile"]) { 
           [ADBMobile trackAdobeDeepLink:url]; 
           return YES; 
       } 
       return NO; 
   } 
   ```

   **Android:** In de app roept u `Config.trackAdobeDeepLink(URL);` wanneer de bezoeker wordt gevraagd om het middel met het URL-schema te openen dat in de vorige stap werd gespecificeerd.

   ```javascript
    private Boolean shouldOpenDeeplinkUrl() { 
        Intent appLinkIntent = getIntent(); 
        String appLinkAction = appLinkIntent.getAction(); 
        Uri appLinkData = appLinkIntent.getData; 
        if (appLinkData.toString().startsWith("com.adobe.targetmobile")) { 
            Config.trackAdobeDeepLink(appLinkData); 
            return true; 
        } 
        return false; 
     }
   ```

   Als u mobiele voorvertoning wilt laten werken voor Android, moet u ook het volgende codefragment toevoegen in [!DNL AndroidManifest.xml] bij gebruik van versie 5 van de Adobe Mobile SDK:

   ```javascript
   <activity android:name="com.adobe.marketing.mobile.FullscreenMessageActivity" />
   ```

   Gebruik het volgende codefragment als u versie 4 van de Adobe Mobile SDK gebruikt:

   ```javascript
   <activity android:name="com.adobe.mobile.MessageFullScreenActivity" />
   ```

## Een voorbeeldkoppeling genereren {#section_D9D58173FFF34E9BB75EBF357273F128}

1. Klik in de interface Doel op de knop **[!UICONTROL More Options]** pictogram (drie verticale ovalen), en selecteer vervolgens **[!UICONTROL Create Mobile Preview]**.

   ![](assets/mobile-preview-create.png)

1. Selecteer de activiteiten die u wilt voorvertonen en klik vervolgens op **[!UICONTROL Generate Mobile Preview LInk]**.

   >[!NOTE]
   >
   >Alleen op formulieren gebaseerde AB- en XT-activiteiten kunnen worden geselecteerd.

   ![](assets/mobile-preview-select-activities.png)

1. Geef het URL-schema van uw app op.

   Dit moet hetzelfde zijn als wat er aanwezig is in uw iOS- of Android-app. Herhaal dit proces desgewenst afzonderlijk voor iOS en Android.

   ![](assets/mobile-preview-enter-url-scheme.png)

1. Klikken **[!UICONTROL Generate Mobile Preview Link]** kopieert u de koppeling.

   ![](assets/mobile-preview-generate-and-copy.png)

## Voorvertonen op uw apparaat {#section_521F0D46F3DE4A2A98283A1B73FF69F6}

Open de koppeling in een mobiele browser op een apparaat waarop uw app is geïnstalleerd. Deze app kan de productie-app zijn die u hebt gedownload van de Apple App Store of de Google Play Store. Het hoeft geen speciale build te zijn. Als u een actieve voorproefverbinding hebt, zult u de ervaringen op apparaat kunnen bekijken.

1. Open de koppeling in uw mobiele browser.

   Deel de koppeling die u in de vorige stap van de doelgebruikersinterface naar uw mobiele apparaat hebt gekopieerd op een handige manier, bijvoorbeeld met tekst, e-mail of Slack.

   |![voorvertoning van diepe koppeling 1](/help/main/c-target-mobile-app/assets/mobile-preview-open-deeplink.png)|![voorvertoning van diepe koppeling 2](/help/main/c-target-mobile-app/assets/mobile-preview-open-app.png)|

   Uw app wordt geopend en de modus Mobiele voorvertoning voor doelapparaten wordt gestart.

1. Selecteer de combinatie van ervaringen die u wilt zien en klik op **[!UICONTROL Launch Experiences]**.

   |![mobiele voorvertoning 1](/help/main/c-target-mobile-app/assets/mobile-preview-experience-selection-1.png)|![mobiele voorvertoning 2](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-1-france.png)|![mobiele voorvertoning 3](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-1-shipfree.png)| |![mobiele voorvertoning 4](/help/main/c-target-mobile-app/assets/mobile-preview-experience-selection-2.png)|![mobiele voorvertoning 5](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-2-aus.png)|![mobiele voorvertoning 6](/help/main/c-target-mobile-app/assets/mobile-preview-experience-result-2-10off.png)|

## Beperkingen {#section_4E9BDED0F718485292527EFB508305BD}

* De nieuwe inhoud wordt pas na het dialoogvenster [!UICONTROL Launch Experiences] wordt geklikt. De eenvoudigste manier is om over te schakelen op een ander scherm en vervolgens terug te keren naar het scherm waar de wijziging naar verwachting zal plaatsvinden.
* Mobiele voorvertoning wordt niet ondersteund voor Android-versies ouder dan API-19 (KitKat).
