---
title: Installera kumulativa korrigeringspaket på AEM Forms JEE
description: Sammanfattning av steg för att installera och konfigurera Cumulative Fix Pack (CFP) på AEM Forms JEE
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 0%

---


# Installerar kumulativa korrigeringspaket på AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installera CFP på AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Utför följande steg i den angivna sekvensen för att installera kumulativa korrigeringspaket på AEM 6.3 [!DNL Forms JEE].

1. Kontakta [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html) för att få AEM 6.3 [!DNL Forms JEE] installationsprogram för CFP.
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivningen i [Installera och konfigurera AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Installera den senaste AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. Installera [!DNL Forms]-tilläggspaketet för AEM CFP [6.3.3.x](aem-forms-releases.md)

### Installera AEM [!DNL Forms JEE] paketpaket {#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1; version 1.0.2) ger  [!DNL Forms] användaren AEM  [!DNL Forms JEE] samma rättigheter och funktioner som AEM  [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Ytterligare instruktioner för CQ-4208044 {#additional-instructions-for-cq}

Om du använder AEM 6.3 [!DNL Forms JEE]-server med Oracle-databas konfigurerar du följande inställningar efter distributionen av CFP1, det vill säga efter att Configuration Manager har körts. Den här inställningen krävs för att synkronisera användare, grupper och gruppmedlemmar när företagsdomänsynkroniseringen körs. Se utgåva CQ-4208044 i [AEM 6.3 versionsinformation](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Logga in på gränssnittet **Admin**.
1. Navigera till **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Exportera filen config.xml.
1. Ändra posten för `groupMemberDBQueryBatchSize` under dina domänkonfigurationer i *config.xml*. Exempelpost:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Importera den ändrade filen igen och kör sedan synkroniseringen igen.

## Installera CFP på AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Utför följande steg i den angivna sekvensen för att installera kumulativa korrigeringspaket på AEM 6.2 [!DNL Forms JEE].

>[!NOTE]
>
>Om du använder AEM 6.2 [!DNL Forms OSGi] följer du installationsanvisningarna i [versionsinformationen för den gemensamma fiskeripolitiken AEM 6.2.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Kontakta [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html) för att få AEM 6.2 [!DNL Forms JEE] installationsprogram för CFP.
1. Kör CFP-installationsprogrammet och konfigurera AEM [!DNL Forms JEE] enligt beskrivningen i [Installera och konfigurera AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Installera [AEM hotfix 12785 version 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Installera [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Installera den senaste [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Installera [!DNL Forms]-tilläggspaketet för [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md).

### Installera AEM [!DNL Forms JEE] paketpaket {#install-aem-forms-jee-bundles-package-1}

[AEM Forms JEE package](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) (aemfd-jee-bundles-package-6.2CFP5; version 1.0.2) ger  [!DNL Forms] användaren AEM  [!DNL Forms JEE] samma rättigheter och funktioner som AEM  [!DNL Forms OSGi]. Kontrollera de installerade paketen i Package Manager och installera paketet om det inte redan är installerat.

### Konfigurera timeout för åtgärder på komponentnivå (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Efter AEM 6.2 CFP4 kan du använda följande anvisningar för att konfigurera timeout för DSC-åtgärder om du får problem på grund av timeout under uppgraderingsprocessen. (Se NPR-16774 i [AEM 6.2 Versionsinformation för CFP4](release-notes-aem-6-2-cumulative-fix-pack.md)).

DSC-distributionen tar en varierande tid på grund av att den kan misslyckas. Om du vill ändra tidsgränsen för DSC-åtgärder som Install, Load, Start och Stop måste du ange `adobe.component.registry.timeout` med JVM-argumentet med alternativet -D.

Ange värdet för nyckeln i sekunder. Till exempel: `-Dadobe.component.registry.timeout=300`

Du kan också ändra tidsgränser på komponentnivå med följande tre egenskaper:

1. `adobe.all-component.timeout`: skriver över tidsgränser för alla tjänster i produkten.
1. `adobe.<serviceName>.timeout`: skriver över timeout-värdet bara för den tjänst (&lt;servicename>) som anges i nyckeln. Om värdet på tjänstenivå anges skrivs timeoutvärdet för den angivna tjänsten bara över om det här kommandot används på programnivå.
1. `adobe.<serviceName>.<operationName>.timeout`: Tidsgränsen för den specifika tjänstens åtgärd (&lt;servicename> skrivs bara över.&lt;operationname>) i nyckeln. Om värdet är inställt på åtgärdsnivå skriver det här kommandot bara över timeoutvärdet för den angivna tjänsten om det är inställt på programnivå eller tjänstnivå.

**Exempel:**

Använd följande kommandon för att ange timeout på komponentnivå:

1. Så här anger du timeout för alla serviceåtgärder till 600 sek:

   uppsättning &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Om du vill ange tidsgränsen för `DesigntimeService`-åtgärdsvärden till 500 sek använder du:

   uppsättning &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Om du vill ange tidsgränsen för åtgärden `DesigntimeService's previewLCA` till 700 sek använder du:

   uppsättning `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Använd följande om du vill ställa in `DSC operations` till exempel load, install och så vidare till 600 sek:

   uppsättning &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installera och konfigurera AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Säkerhetskopiera /deploy-mappen. Det krävs om du bestämmer dig för att avinstallera snabbkorrigeringen.
1. Stoppa programservern.
1. Extrahera arkivfilen för patch-installationsprogrammet till hårddisken.
1. I katalogen som namnges enligt det operativsystem som du använder:

   **Windows**

   Navigera till rätt katalog på installationsmediet eller mappen på hårddisken där du kopierade installationsprogrammet:

   * (32-bitars Windows): Disk1\InstData\Windows\VM
   * (64-bitars Windows): Disk1\InstData\Windows_64bit\VM

   Dubbelklicka sedan på filen med namnet:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Navigera till rätt katalog:

   * (Linux): Disk1/InstData/Linux/ NoVM
   * (Solaris): Disk1/InstData/Solaris/ NoVM
   * (AIX): Disk1/InstData/AIX/VM

   I en kommandotolk skriver du:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Då startas en installationsguide som vägleder dig genom installationen.

1. Klicka på **[!UICONTROL Next]** på introduktionspanelen.
1. På skärmen Välj installationsmapp kontrollerar du att den standardplats som visas är korrekt för den befintliga installationen, eller klickar på **[!UICONTROL Browse]** och väljer den alternativa mappen där AEM [!DNL Forms] är installerad, och klickar sedan på **[!UICONTROL Next]**.
1. Läs Quick Fix Patch Summary-informationen och klicka på **[!UICONTROL Next]**.
1. Läs informationen i Sammanfattning av förinstallation och klicka på **[!UICONTROL Install]**.
1. När installationen är klar klickar du på **[!UICONTROL Next]** för att tillämpa snabbkorrigeringsuppdateringarna på de installerade filerna.
1. Kryssrutan Starta Configuration Manager är markerad som standard. Klicka på **[!UICONTROL Done]** för att köra Configuration Manager.

   Om du vill köra Configuration Manager senare avmarkerar du alternativet **[!UICONTROL Start Configuration Manager]** innan du klickar på **[!UICONTROL Done]**. Du kan starta Configuration Manager senare med lämpligt skript i katalogen *`[AEM_forms_root]`/configurationManager/bin*.

1. Beroende på vilken programserver du använder väljer du något av följande dokument och följer instruktionerna i *Konfigurera och distribuera AEM[!DNL Forms]*.

   För AEM [!DNL Forms] 6.3, se:

   * [Installera och distribuera  [!DNL Forms] AEMfor JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   För AEM [!DNL Forms] 6.2, se:

   * [Installera och distribuera  [!DNL Forms] AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   För AEM Forms 6.1, se:

   * [Installera och distribuera  [!DNL Forms] AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [Installera och distribuera  [!DNL Forms] AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Starta om AEM [!DNL Forms] JEE-server.
