---
title: Installera kumulativa korrigeringspaket på AEM Forms JEE
description: Sammanfattning av steg för att installera och konfigurera Cumulative Fix Pack (CFP) på AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 437dad5fffe71592b6f9f9b4099a253e3a55b0c8
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 0%

---

# Installerar kumulativa korrigeringspaket på AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installera CFP på AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Installera det kumulativa korrigeringspaketet på AEM 6.3 [!DNL Forms JEE]utför du följande stegsekvens.

1. För att få AEM 6.3 [!DNL Forms JEE] installationsprogram för CFP, kontakta [Stöd för Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support).
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivning i [Installera och konfigurera AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installera den senaste AEM CFP 6.3.3.x
1. Installera [!DNL Forms] Tilläggspaket för AEM CFP [6.3.3.x](aem-forms-releases.md)

### Installera AEM [!DNL Forms JEE] paket {#install-aem-forms-jee-bundles-package}

AEM [!DNL  Forms JEE] package (aemfd-jee-bundles-package-6.3CFP1; version 1.0.2) innehåller [!DNL Forms] Användare på AEM [!DNL Forms JEE] samma rättigheter och funktioner som AEM [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Fler instruktioner för CQ-4208044 {#additional-instructions-for-cq}

Om du använder AEM 6.3 [!DNL Forms JEE] oracle med konfigurationsdatabas konfigurerar du följande inställningar efter distributionen av CFP1, det vill säga efter att Configuration Manager har körts. Den här inställningen krävs för att synkronisera användare, grupper och gruppmedlemmar när företagsdomänsynkroniseringen körs.

1. Logga in på **Administratör** Gränssnitt.
1. Navigera till **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exportera filen config.xml.
1. Ändra posten för &quot; `groupMemberDBQueryBatchSize`&quot; under dina domänkonfigurationer i *config.xml*. Exempelpost:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importera den ändrade filen igen och kör sedan synkroniseringen igen.

## Installera CFP på AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Installera kumulativa korrigeringspaket i AEM 6.2 [!DNL Forms JEE]utför du följande stegsekvens.

1. För att få AEM 6.2 [!DNL Forms JEE] installationsprogram för CFP, kontakta [Stöd för Adobe](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support).
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivning i [Installera och konfigurera AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installera AEM hotfix 12785 version 7.0.
1. Installera AEM 6.2 Service Pack 1.
1. Installera den senaste release-notes-aem-6-2-cumulative-fix-pack.md.
1. Installera [!DNL Forms] Tillägg för AEM 6.2 Service Pack 1 CFP.

### Installera AEM [!DNL Forms JEE] paket {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE-paketet (aemfd-jee-bundles-package-6.2CFP5; version 1.0.2) innehåller [!DNL Forms] Användare på AEM [!DNL Forms JEE] samma rättigheter och funktioner som AEM [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Konfigurera timeout för åtgärder på komponentnivå (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Efter AEM 6.2 CFP4 kan du använda följande instruktioner för att konfigurera timeout-värdet för DSC-åtgärder om du får problem på grund av timeout under uppgraderingsprocessen.

DSC-distributionen tar en varierande tid på grund av att den kan misslyckas. Om du vill ändra tidsgränsen för DSC-åtgärder som Install, Load, Start och Stop måste du ange `adobe.component.registry.timeout` med JVM-argumentet med alternativet -D.

Ange värdet för nyckeln i sekunder. Till exempel: `-Dadobe.component.registry.timeout=300`

Du kan också ändra tidsgränser på komponentnivå med följande tre egenskaper:

1. `adobe.all-component.timeout`: skriver över timeout för alla tjänster i produkten.
1. `adobe.<serviceName>.timeout`: skriver över timeout-värdet bara för tjänsten (&lt;servicename>) som anges i nyckeln. Om värdet på tjänstenivå anges skrivs timeoutvärdet för den angivna tjänsten bara över om det här kommandot används på programnivå.
1. `adobe.<serviceName>.<operationName>.timeout`: Tidsgränsen för den specifika tjänstens åtgärd skrivs bara över(&lt;servicename>.&lt;operationname>) som anges i nyckeln. Om värdet är inställt på åtgärdsnivå skriver det här kommandot bara över timeoutvärdet för den angivna tjänsten om det är inställt på programnivå eller tjänstnivå.

**Exempel:**

Använd följande kommandon för att ange timeout på komponentnivå:

1. Så här anger du timeout för alla serviceåtgärder till 600 sek:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Så här anger du `DesigntimeService` timeout för operationsvärden till 500 sek. Använd:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Så här anger du `DesigntimeService's previewLCA` timeout för operationsvärden till 700 sek. Använd:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Så här anger du `DSC operations`, till exempel läsa in och installera, till 600 sek, använd:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installera och konfigurera AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Säkerhetskopiera /deploy-mappen. Det krävs om du bestämmer dig för att avinstallera snabbkorrigeringen.
1. Stoppa programservern.
1. Extrahera arkivfilen för patch-installationsprogrammet till hårddisken.
1. I katalogen som namnges enligt det operativsystem som du använder:

   **Windows**

   Navigera till rätt katalog på installationsmediet eller mappen på hårddisken där du kopierade installationsprogrammet:

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   Dubbelklicka sedan på filen:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Navigera till rätt katalog:

   * (Linux®): Disk1/InstData/Linux/ NoVM
   * (Solaris™): Disk1/InstData/Solaris/ NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Skriv:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Installationsguiden startas för att vägleda dig genom installationen.

1. Klicka på panelen Introduktion **[!UICONTROL Next]**.
1. Kontrollera att den standardplats som visas är korrekt för din befintliga installation på skärmen Välj installationsmapp. Eller klicka **[!UICONTROL Browse]** för att välja alternativ mapp där AEM [!DNL Forms] är installerat och klickar sedan på **[!UICONTROL Next]**.
1. Läs Quick Fix Patch Summary och klicka på **[!UICONTROL Next]**.
1. Läs mer i Förinstallationssammanfattning och klicka på **[!UICONTROL Install]**.
1. När installationen är klar klickar du **[!UICONTROL Next]** för att använda snabbkorrigeringsuppdateringar på dina installerade filer.
1. Kryssrutan Starta Configuration Manager är markerad som standard. Klicka **[!UICONTROL Done]** för att köra Configuration Manager.

   Om du vill köra Configuration Manager senare avmarkerar du **[!UICONTROL Start Configuration Manager]** innan du klickar **[!UICONTROL Done]**. Du kan starta Configuration Manager senare med rätt skript i *`[AEM_forms_root]`/configurationManager/bin* katalog.

1. Beroende på programservern väljer du ett av följande dokument och följer instruktionerna i *Konfigurera och distribuera AEM[!DNL Forms]* -avsnitt.

   För AEM [!DNL Forms] 6.3, se:

   * Installera och distribuera AEM [!DNL Forms] för JBoss®
   * Installera och distribuera AEM [!DNL Forms] för WebSphere®
   * Installera och distribuera AEM [!DNL Forms] för WebLogic

1. AEM [!DNL Forms] JEE-server.
