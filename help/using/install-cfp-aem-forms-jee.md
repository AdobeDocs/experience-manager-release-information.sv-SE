---
title: Installera kumulativa korrigeringspaket på AEM Forms JEE
description: Sammanfattning av steg för att installera och konfigurera ett kumulativt korrigeringspaket (CFP) på AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 0%

---

# Installerar kumulativa korrigeringspaket på AEM[!DNL &#x200B; Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installera CFP på AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Utför följande steg för att installera det kumulativa korrigeringspaketet AEM 6.3 [!DNL Forms JEE].

1. Kontakta [Adobe Support](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support) om du vill få installationsprogrammet för AEM 6.3 [!DNL Forms JEE] för CFP.
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivningen i [Installera och konfigurera AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installera den senaste AEM CFP 6.3.3.x
1. Installera tilläggspaketet [!DNL Forms] för AEM CFP [ 6.3.3.x](aem-forms-releases.md)

### Installera AEM [!DNL Forms JEE]-paketpaket {#install-aem-forms-jee-bundles-package}

AEM [!DNL &#x200B; Forms JEE]-paketet (aemfd-jee-bundles-package-6.3CFP1; version 1.0.2) ger [!DNL Forms] User on AEM [!DNL Forms JEE] samma rättigheter och funktioner som i AEM [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Fler instruktioner för CQ-4208044 {#additional-instructions-for-cq}

Om du använder AEM 6.3 [!DNL Forms JEE]-servern med Oracle-databasen ska du konfigurera följande inställningar efter distributionen av CFP1, det vill säga efter att Configuration Manager har körts. Den här inställningen krävs för att synkronisera användare, grupper och gruppmedlemmar när företagsdomänsynkroniseringen körs.

1. Logga in på användargränssnittet för **Admin**.
1. Navigera till **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exportera filen config.xml.
1. Ändra posten för `groupMemberDBQueryBatchSize` under dina domänkonfigurationer i *config.xml*. Exempelpost:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importera den ändrade filen igen och kör sedan synkroniseringen igen.

## Installera CFP på AEM 6.2 [!DNL &#x200B; Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Utför följande steg för att installera det kumulativa korrigeringspaketet AEM 6.2 [!DNL Forms JEE].

1. Kontakta [Adobe Support](https://experienceleague.adobe.com/?support-solution=General&amp;support-tab=home#support) om du vill få installationsprogrammet för AEM 6.2 [!DNL Forms JEE] för CFP.
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivningen i [Installera och konfigurera AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installera AEM hotfix 12785 version 7.0.
1. Installera AEM 6.2 Service Pack 1.
1. Installera den senaste release-notes-aem-6-2-cumulative-fix-pack.md.
1. Installera tilläggspaketet [!DNL Forms] för AEM 6.2 Service Pack 1 CFP.

### Installera AEM [!DNL Forms JEE]-paketpaket {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE-paket (aemfd-jee-bundles-package-6.2CFP5; version 1.0.2) ger [!DNL Forms] användare på AEM [!DNL Forms JEE] samma rättigheter och funktioner som på AEM [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Konfigurera timeout för åtgärder på komponentnivå (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Post AEM 6.2 CFP4 kan du använda följande anvisningar för att konfigurera timeout för DSC-åtgärder om du får problem på grund av timeout under uppgraderingsprocessen.

DSC-distributionen tar en varierande tid på grund av att den kan misslyckas. Om du vill ändra tidsgränsen för DSC-åtgärder som Install, Load, Start och Stop, måste du ange `adobe.component.registry.timeout` med JVM-argumentet med alternativet -D.

Ange värdet för nyckeln i sekunder. Till exempel: `-Dadobe.component.registry.timeout=300`

Du kan också ändra tidsgränser på komponentnivå med följande tre egenskaper:

1. `adobe.all-component.timeout`: skriver över timeout för alla tjänster i produkten.
1. `adobe.<serviceName>.timeout`: skriver bara över tidsgränsen för tjänsten (&lt;serviceName>) som anges i nyckeln. Om värdet på tjänstenivå anges skrivs timeoutvärdet för den angivna tjänsten bara över om det här kommandot används på programnivå.
1. `adobe.<serviceName>.<operationName>.timeout`: Tidsgränsen för den specifika tjänstens åtgärd skrivs bara över (&lt;serviceName>).&lt;operationName>) omnämns i nyckeln. Om värdet är inställt på åtgärdsnivå skriver det här kommandot bara över timeoutvärdet för den angivna tjänsten om det är inställt på programnivå eller tjänstnivå.

**Exempel:**

Använd följande kommandon för att ange timeout på komponentnivå:

1. Så här anger du timeout för alla serviceåtgärder till 600 sek:

   ange `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`

1. Om du vill ange tidsgränsen för `DesigntimeService`-åtgärdsvärden till 500 sek använder du:

   ange `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`

1. Om du vill ange tidsgränsen för åtgärden `DesigntimeService's previewLCA` till 700 sek använder du:

   ange `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`

1. Använd följande om du vill ange `DSC operations`, till exempel läsa in och installera, till 600 sekunder:

   ange `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`

## Installera och konfigurera AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Säkerhetskopiera /deploy-mappen. Det krävs om du bestämmer dig för att avinstallera snabbkorrigeringen.
1. Stoppa programservern.
1. Extrahera arkivfilen för patch-installationsprogrammet till hårddisken.
1. I katalogen som namnges enligt det operativsystem som du använder:

   **Windows**

   Navigera till katalogen på installationsmediet eller till mappen där du kopierade installationsprogrammet.

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   Dubbelklicka sedan på filen:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Navigera till rätt katalog:

   * (Linux®): Disk1/InstData/Linux/NoVM
   * (Solaris™): Disk1/InstData/Solaris/NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Skriv:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Installationsguiden startas för att vägleda dig genom installationen.

1. Klicka på **[!UICONTROL Next]** på introduktionspanelen.
1. Kontrollera att den standardplats som visas är korrekt för din befintliga installation på skärmen Välj installationsmapp. Du kan också klicka på **[!UICONTROL Browse]** för att markera den alternativa mappen där AEM [!DNL Forms] är installerad och sedan klicka på **[!UICONTROL Next]**.
1. Läs Quick Fix Patch Summary-informationen och klicka på **[!UICONTROL Next]**.
1. Läs informationen om sammanfattning av förinstallation och klicka på **[!UICONTROL Install]**.
1. När installationen är klar klickar du på **[!UICONTROL Next]** för att tillämpa snabbkorrigeringsuppdateringarna på de installerade filerna.
1. Kryssrutan Starta Configuration Manager är markerad som standard. Klicka på **[!UICONTROL Done]** för att köra Configuration Manager.

   Om du vill köra Configuration Manager senare avmarkerar du alternativet **[!UICONTROL Start Configuration Manager]** innan du klickar på **[!UICONTROL Done]**. Du kan starta Configuration Manager senare med rätt skript i katalogen *`[AEM_forms_root]`/configurationManager/bin*.

1. Beroende på vilken programserver du använder väljer du något av följande dokument och följer instruktionerna i avsnittet *Konfigurera och distribuera AEM[!DNL Forms]*.

   För AEM [!DNL Forms] 6.3, se:

   * Installerar och distribuerar AEM [!DNL Forms] för JBoss®
   * Installerar och distribuerar AEM [!DNL Forms] för WebSphere®
   * Installerar och distribuerar AEM [!DNL Forms] för WebLogic

1. Starta om JEE-servern AEM [!DNL Forms].
