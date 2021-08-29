---
title: AEM 6.3 Cumulative Fix Pack
description: AEM 6.3 Cumulative Fix Pack Release Notes.
source-git-commit: 3c798116db7314f4220f8a183a989c2b37678054
workflow-type: tm+mt
source-wordcount: '15906'
ht-degree: 0%

---

# Versionsinformation om AEM 6.3 Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Versionsinformation {#release-information}

| **Produkt** | Adobe Experience Manager |
|---|---|
| **Version** | 6.3 |
| **Frigör** | Kumulativt korrigeringspaket 6.3.3.8 på [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8), [Software Distribution(Beta)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Förutsättning** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **Allmän tillgänglighet** | 5 mars 2020 |

### Kumulativt korrigeringspaket {#cumulative-fix-pack}

Adobe introducerade en modell för engångsleverans av korrigeringar. I stället för att släppa snabbkorrigeringar för enskilda utgåvor ger Adobe nu ut ett Cumulative Fix Pack (CFP) varje månad (med reservation för kvalitetskontroller). En CFP är ett aggregerat innehållspaket för flera korrigeringar. Bestrukna artiklar innehåller i första hand felkorrigeringar, men kan även innehålla funktionspaket. De har följande fördelar jämfört med enskilda snabbkorrigeringar:

* Kumulativt (t.ex. en bestruken finans innehåller korrigeringar som gjorts genom tidigare bestrukna finanser)
* Ökad kvalitetssäkring
* Förenklad installation (Användaren installerar en CFP som ett enskilt paket som inte har några beroenden, förutom det senaste Service Pack)

Mer information om CFP och andra typer av releaser finns i [definitioner av underhållsreleaser för fordon.](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)

## Om releasen {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.8 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.20.

>[!CAUTION]
>
>Om du använder bestruket papper utan att validera kompatibiliteten mellan installerade funktionspaket kan det leda till att systemet inte fungerar eller att anpassade konfigurationer går förlorade, vilket kan kräva återställning från säkerhetskopia för att kunna lösas.

>[!NOTE]
>
>För AEM instanser med en version lägre än 6.3.3.0 rekommenderar Adobe att du distribuerar SP/CFP via installationsmappen för kunder med ett stort antal användare på AEM.

>[!NOTE]
>
>MongoDB Enterprise 3.6 stöds från och med AEM version 6.3.3.1.

## Lista över problem {#changes}

I det här avsnittet listas alla problem och snabbkorrigeringar som ingår i den aktuella gemensamma fiskeripolitiken.

Dessutom innehåller denna CFP snabbkorrigeringar som levererats i [tidigare kumulativa korrigeringspaket](#previous).

### Assets {#assets}

* På sidan Lägg till i samling visas inte alla tillgängliga samlingar i kortvyn när du lägger till resurser i samlingen (NPR-32537).

### Sites {#sites}

* När du markerar en parameter och en komponent i den och använder kortkommandot för att ta bort markerade objekt, tar åtgärden bort både komponenten och dess överordnade parsys (NPR-32071).
* När egenskaperna för en sida sparas skapas en felaktig nod (NPR-31774).

### Integreringar {#integrations}

* ReportSuitesServlet är sårbart för SSRF (NPR-32162).

### Kampanjanpassning {#campaign-targeting}

* En komponents innehåll som har ändrats, i Author-instansen och sedan aktiverats, visas inte i Publish-instansen förrän komponenten har startats om **com.day.cq.pesonalization.impl.TargetedContentManagerImpl** (NPR-32489 och NPR-32232).
* Contexthub-prestanda kraschar vid publicering (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O är inte integrerat med Adobe Experience Manager 6.3 för Brand Portal (NPR-32056).

### Forms {#forms}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

#### Forms tilläggspaket {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms tilläggspaket hjälper till att anpassa formulärfunktionaliteten med AEM Service Pack och Cumulative Fix Packs. Därför är det viktigt att du installerar AEM Forms tilläggspaket när du har installerat AEM Service Pack, Cumulative Fix Pack eller Feature Pack.

* Designer: Om taggningsalternativet är aktiverat försvinner delformulärsramen i den genererade PDF-utdatafilen (NPR-32324 och NPR-32545).
* Designer: Om det finns sammanfogade celler i en tabell misslyckas hjälpmedelstestet för PDF-utdatafilen som konverterats från ett XDP-formulär med hjälp av utdatatjänsten (NPR-32068).
* Dokumentsäkerhet: En skyddad PDF-fil kan inte öppnas offline med alternativet `DisableGlobalOfflineSynchronizationData` inställt på `True` (NPR-32080).

## Programfixar och funktionspaket som ingår i tidigare Cumulative Fix-paket {#previous}

### Kumulativt korrigeringspaket 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.7 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Resurser {#assets-1}

* Markerade resurser (i kolumnvyn i Touch UI) innan du väljer filteralternativet i listrutan Endast innehåll och sedan väljer flyttningsalternativet flyttas också (NPR-30693).
* Variabeln `${extension}` återges inte i författarinstansen vid arbetsflödesbearbetning (NPR-31694).
* Det värde för förfallotid (klientens cachetid till live) som konfigurerats för Dynamic Media hybridläge replikeras inte till Dynamic Media leveransmiljö (NPR-3114).
* Resurserna replikeras till Publish-instansen från Author-instansen som körs på Dynamic Media - Scene7-distributionen, även efter att standardfiltren har använts (NPR-30856).

### Webbplatser {#sites-1}

* Det går inte att läsa in sidegenskaperna för en överordnad sida och ett NullPointerException returneras. Problemet löses när egenskapen cq:blueprint läggs till (NPR-30901).
* Utrullningskonfigurationer hämtas inte korrekt från blueprintConfig på rotnoden. Inaktiveringen aktiveras för både utkast och live-kopior. Inaktiveringen bör endast aktiveras för ritningen (NPR-30866).
* När en användare rullar ut en sida visar dialogrutan för konfiguration av utrullning dubbletter av direktkopieringssökvägar (NPR-30438).
* Utanför skalningsprogrammet kan du göra en RTF-redigerare (Rich Text Editor). använder textbunden teckensnittsstorlek för element, oväntat (NPR-31283, NPR-30922).
* Det går inte att synkronisera kampanjen i Adobe-kampanjen som innehåller importkomponenten för färdig design (NPR-30890).
* RTE (Rich Text Editor). tillåter inte att en inbäddad tabell infogas som listobjekt (NPR-30878).
* När en användare fokuserar på fält med vänster stödlinje och använder ett kortkommando för att klistra in innehåll, klistras innehållet i sidredigerarens urklipp in i stället för innehållet som kopieras från de vänstra fältspåren (NPR-31173).
* När en användare redigerar ett innehållsfragment återställs den redan borttagna varianten av innehållsfragmentet (NPR-31272).
* AEM kan inte skapa en språkkopia (NPR-30690).
* Sidredigerarens åtgärder saknar kontroller för att rulla ut live-kopior (NPR-30613).

### Communities {#communities}

* Aktiviteter och meddelandetitlar är inkonsekventa (NPR-30940).
* Analysrapporter är inte ifyllda i AEM författarmiljö, en tom sida visas (NPR-30905).
* Sidindelningen fungerar inte korrekt i webbgruppsbloggar (NPR-30827).

### Foundation {#foundation}

* Uppdateringar i buffertstorlekskonfigurationen för Jetty-baserad HTTP-tjänst sparas inte (NPR-30925).

### Forms {#forms-1}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms tilläggspaket hjälper till att anpassa formulärfunktionaliteten med AEM Service Pack och Cumulative Fix Packs. Därför är det viktigt att du installerar AEM Forms tilläggspaket när du har installerat AEM Service Pack, Cumulative Fix Pack eller Feature Pack.

#### Adaptiv Forms {#adaptive-forms}

* Flytande värden som beräknas med ett skript visas inte korrekt i ett format som är en del av ett format (NPR-30802).

#### HTML5 Forms {#html-forms}

* När du genererar HTML5-förhandsgranskning av ett XDP-formulär visas ett flimmer när instanser av ett delformulär läggs till (NPR-30908).

### Forms JEE-installationsprogram {#forms-jee-installer}

#### Dokumenttjänster {#document-services}

* OutputService visar ett felaktigt svar efter att ha tillämpat en korrigering för att korrigera HTML-problem i PDF-filer (NPR-31504).

#### PDFG-tjänst {#pdfg-service}

* Maximalt antal återanvändningar med JMX-konsolen visas inte för HTML2PDF-tjänsten (NPR-30305).

#### Foundation JEE {#foundation-jee}

* Maximalt antal återanvändningar med JMX-konsolen visas inte för HTML2PDF-tjänsten (NPR-30136).

### Kumulativt korrigeringspaket 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.6 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Resurser {#assets-2}

* Videoaggregering med dynamisk video returnerar bara de 100 främsta objekten i resultatuppsättningen. NPR-30441; Programfix för CQ-4213561
* Anslutningsproblem med Adobe Smart Tag via DataPower. NPR-30026: Programfix för CQ-4269457
* Det går inte att öppna ett arkiv med en mapp som har ett procenttecken (%) i namnet med hjälp av gränssnittet Resurser. NPR-29989: Programfix för CQ-4270467
* Bearbetning av delresurser i stora PDF-filer orsakar ett OOME-undantag (OutOfMemoryError). NPR-29851: Programfix för CQ-4269574

### Webbplatser {#sites-2}

* ContextHub-fel under AEM- och Campaign-integrering. NPR-30624: Programfix för CQ-4250790
* Metadataegenskaper för onTime eller offTime som sparats på resurser återkallas inte om AEM startas om. NPR-30412: Programfix för CQ-4272784
* När du genererar en CSV-export bryts rapporten om du lägger till anpassade kolumner för listvyn. NPR-30208: Programfix för CQ-4273344
* OTB-rapporter i /etc/reports/ fungerar inte korrekt och historisk datagraf visas inte. NPR-30016: Programfix för CQ-4220180
* Värdet för parametern resourceType request kopieras till värdet för ett HTML-taggattribut som är inkapslat med citattecken. NPR-29832: Programfix för CQ-4255365

### Communities {#communities-1}

* Problem med duplicerat innehåll med AEM Communities moderationskonsol. NPR-30667: Programfix för CQ-4276829

### Översättning {#translation}

* Översättningsproblem - Endast ett fåtal komponenter översätts med maskinöversättning. NPR-30079: Programfix för CQ-4273764
* När du använder översättningsramverket utlöses ett fel när sidor läggs till i flera översättningsjobb. NPR-29746: Programfix för CQ-4270953

### Forms {#forms-2}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms tilläggspaket hjälper till att anpassa formulärfunktionaliteten med AEM Service Pack och Cumulative Fix Packs. Därför är det viktigt att du installerar AEM Forms tilläggspaket när du har installerat AEM Service Pack, Cumulative Fix Pack eller Feature Pack.

#### HTML5 Forms {#html-forms-1}

* När du använder NonVisual Desktop Access i bläddringsläge för att läsa ett HTML5-formulär, läser webbläsaren Chrome &quot;graphic&quot; före varje Scalable Vector Graphic (SVG) i formulärdesignen. NPR-30451: Programfix för CQ-4274732

#### Forms - serverintegrering {#forms-backend-integration}

* Det gick inte att se tjänsten/datakällan för databasanslutningen när formulärdatamodellen (FDM) skapades. NPR-30108: Programfix för CQ-4273359

### Forms JEE-installationsprogram {#forms-jee-installer-1}

#### Forms - dokumenttjänster {#forms-document-services}

* När ett inläsningstest utförs på tjänsten HTML till PDF misslyckas det med ett fel och filtypsinställningarna tas bort från AEM formulärserver. NPR-30111, NPR-30086: Programfix för CQ-4271495

### Kumulativt korrigeringspaket 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.5 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.17.

### Resurser {#assets-3}

* DAM DMGGateway-gränssnittet för S3-multipart-stöd har uppdaterats. NPR-29740: Programfix för Q-4226303
* Det går inte att ta bort en bildåtergivning för en videoresurs från sidan med resursinformation. NPR-29417: Programfix för CQ-4268675
* Ägaren kan inte skapa en privat mapp i en privat mapp. NPR-29397: Programfix för CQ-4229830
* Om du överför en Adobe Illustrator-teckningsfil på mer än 2 GB genereras ett Java-heap space-fel. NPR-29265: Programfix för CQ-4226217
* Resurser blir oanvändbara efter att DAM CQ Mime Type Service har tillämpat text för m3u8. NPR-29259: Programfix för CQ-4264052
* Alternativet Skapa fungerar inte när du försöker skapa samlingar i Edge. NPR-29248: Programfix för CQ-4265699 och CQ-4265438
* Resurslänkresurs visar tomma grå kort för vissa resurser i mappen. NPR-29831: Programfix för CQ-4270187
* De nya taggarna som läggs till i resurserna kan inte sparas och försvinner från egenskaperna. Programfix för CQ-4271931, CQ-4270476

### Webbplatser {#sites-3}

* När CoralUI används med Multifield lagras fileReferenceParameter på komponentnivå i stället för på multifältnivå. NPR-29535: Programfix för CQ-4266129
* Problem vid jämförelse av den senaste och aktuella sidversionen AEM 6.3.3.3. NPR-29532: Programfix för CQ-4269639
* Sökvägsfältet öppnas på rotsökvägen oavsett vilken sökväg som har angetts för sökningen. NPR-29398: Programfix för CQ-4268897
* (Experience Fragments) FacebookApplication#setUpApp använder föråldrat API, som inte fungerar längre. NPR-29213: Programfix för CQ-4266630
* Felavisering genereras när komponenter läggs till på WCM-sidan när miniatyrbilder är aktiverade på instansen. NPR-29476: Programfix för CQ-4266197
* Tomma egenskaper och flera egenskaper sprids inte från utkast under utrullning. Det går inte att återställa live copy med utkast för komponenter.NPR-29252: Programfix för CQ-4264928, CQ-4264926, CQ-4267722
* Om du minimerar RTF-redigeraren från helskärmsläge i källredigeringsläge leder det till innehållsförlust. NPR-28838: Programfix för CQ-4260584

### Communities {#communities-2}

* Besökare och medlemmar utan moderatorbehörighet kan se ej godkända och väntande inlägg genom att klistra in URL:en. NPR-29726: Programfix för CQ-4271124
* En hög svarstid på upp till 40-50 sekunder observeras vid användarinloggning för Community. NPR-29679: Programfix för CQ-4269444
* Det går inte att återställa lösenordet när du är inloggad med ett annat användarnamn och e-postadress eftersom nyckeln verkar ha genererats med ett utbytt användarnamn och e-postadress. NPR-29281: Programfix för CQ-4268694

### Experience Fragments {#experience-fragments}

* Det går inte att exportera Experience Fragments till target när en smart bild används. Programfix för CQ-4269606

### Replikering {#replication}

* Replikeringsagentkomponenten är känslig för en sårbarhet som avslöjar känslig information för obehöriga användare. NPR-29613: Programfix för Granite-25070
* Data som tillhandahålls av användaren kan inte utelämnas vid utdata i `cq/replication/components/agent`komponenten, vilket resulterar i en lagrad XSS-säkerhetslucka (Cross-site scripting). NPR-29452: Programfix för CQ-4266263

### Forms {#forms-3}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-3}

* Inga nya AEM Forms-korrigeringar i Forms tilläggspaket.

### Forms JEE-installationsprogram {#forms-jee-installer-2}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

### OSGI-paket och innehållspaket som ingår i 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

Förteckning över OSGi-paket som ingår i AEM 6.3.3.5

[Hämta fil](assets/do-not-localize/6_5-bundle-list.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.3.5

[Hämta fil](assets/do-not-localize/content_packages6335.txt)

### Kumulativt korrigeringspaket 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.4 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.16.
* Lagt till sockettimeout och timeout för anslutning i Brand Portal replikeringsagenter.

### Resurser {#assets-4}

* Om du överför ett arkiv med samma namn på nytt genereras inte återgivningar för de nya bearbetade resurserna. NPR-28643: Programfix för CQ-4262286
* CommandLineProcess för arbetsflödet misslyckas med filnamn med ett enkelt citattecken. NPR-28805: Programfix för CQ-4262287
* Värdena skiljer sig mellan samlingssidan och samlingssidan med hjälp av filter. NPR-28642: Programfix för CQ-4261405
* CommitFailedException utlöser överföringar av stora zip-arkivresurser. NPR-28528: Programfix för CQ-4260903
* Mappmetadata sparas inte när en mapp som innehåller specialtecken redigeras. NPR-28211: Programfix för CQ-4260401
* Det går inte att ta bort bildåtergivningar av en videoresurs från sidan Resursinformation. NPR-29149: Programfix för CQ-4266073
* DMS7 DMComponent använder progressiv nedladdning för uppspelning av video i publiceringsläge och direktuppspelar inte video. NPR-28754: Programfix för CQ-4263732
* Det går inte att skapa/redigera bildförinställningar eftersom åtkomst till /etc/dam/video/dynamicmedia inaktiverar funktioner för bildhanterare. NPR-28662: Programfix för CQ-4263022
* Länkdelning med DMS7-kodade videofiler resulterar i tomma mappar. NPR-28851: Programfix för CQ-4206743
* Replikeringen från AEM till Brand Portal fastnar under lång tid. NPR-28913: Programfix för CQ-4254932

### Communities {#communities-3}

* Det går inte att öppna meddelanden som har bifogade filer i mappen Utseende skickat och Inkorgen. NPR-28559: Programfix för CQ-4217072

### Webbplatser {#sites-4}

* XSS (Cross-site scripting) i SuggestionHandler för 6.3. NPR-28692: Programfix för CQ-4253821
* Djupa utrullningar slutar utan att innehålla alla grenar i respektive LiveCopy. NPR-29175: Programfix för CQ-4239472
* (MSM) Implementera LiveCopyIndex med hjälp av index. NPR-29198: Programfix för CQ-422472
* Filen &#39;coral.js&#39; innehåller en sårbar version av biblioteket &#39;handlebars.js&#39;. NPR-26973: Programfix för CQ-4255377
* Om du använder en Target-komponent med en kapslad Layout Container och Text Component (Textkomponent) genereras JavaScript-felet&quot;Det går inte att läsa egenskapen currentPos av null&quot; när du redigerar text eller klickar på behållaren. NPR-29077: Programfix för CQ-4246594
* (Touch UI) Det går inte att uppdatera taggar till sidor som redan är taggade med olika taggar satsvis. NPR-28729: Programfix för CQ-4262922
* Om du öppnar variationen i kortvyn uppstår ett 500-fel. NPR-28611: Programfix för CQ-4263571
* Om en struktur som har flyttats i en överordnad förs över leder det till fel cq:moveTarget. NPR-28968: Programfix för CQ-4265280

### Integrering {#integration}

* (Cloud Service Configs) Kryssrutan &quot;inherited from&quot; som visas på rotnivån bör tas bort. NPR-28771: Programfix för CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler placeras i en oändlig slinga och orsakar uppdateringar av noder på publiceringsinstanser. NPR-28561: Programfix för CQ-4263096
* Det går inte att använda autentiseringsuppgifter för BrightStor med anslutningsfel. NPR-29167: Programfix för CQ-4265872
* Kompileringsfel i OfferproxyTandtProvider.java på grund av att import-sats saknas för klassen Resource: importsats som saknas: importera org.apache.sling.api.resource.Resource. NPR-28772

### Handel {#commerce}

* Sorteringsalternativet fungerar inte för resurser i Commerce-samlingen. NPR-28755: Programfix för CQ-4213622

### Jetty {#jetty}

* Jetty Exceptions in error.log for each 302 redirects after installing CFP2 on top of 6.3.3. NPR-28606: Backport för CQ-4262844

### UI - Foundation {#ui-foundation}

* Om du klickar på taggen tas den globala mushändelsen bort och dialogrutan låses i&quot;dragbart läge&quot;. NPR-28641: Programfix för CUI-7294

### WCM - MSM {#wcm-msm}

* PushOnModify-utrullning för PageManager-flytt verkställs flera gånger från två sessioner, vilket orsakar ett konkurrensvillkor. NPR-28880: Programfix för CQ-4266191

### Sårbarhet {#vulnerability}

* CSRF-skyddsramverket fungerar inte med AEM grundformulär. NPR-28612: Programfix för GRANITE-22231

### Forms {#forms-4}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

AEM Forms i korthet:

* Aktiverat alternativ för att markera objekt per sida på sidan för principuppsättningsvyn.
* Delningsköfunktionen har lagts till för alla webbläsare.

### Forms tilläggspaket {#forms-add-on-package-4}

#### Forms - arbetsflöde {#forms-workflow}

* Åtgärd för delat kösvar öppnar ett flash-element i HTML5-arbetsytan. NPR-29161: Programfix för CQ-4266498
* Det går inte att skicka från arbetsytan om knappen innehåller ett omgivande tecken. NPR-29014: Programfix för CQ-4263172

#### Forms - dokumentsäkerhet {#forms-document-security}

* Aktivera alternativet för att markera objekt per sida på sidan för principuppsättningsvyn. NPR-29243: Programfix för CQ-4268567 och CQ-4265132

#### Forms - dokumenttjänster {#forms-document-services-1}

* OSGi Forms Assembler fungerar inte med Acrobat-filer. NPR-29049: Programfix för CQ-4254426

#### HTML5 Forms {#html-forms-2}

* Olika beteenden inträffar när en XDP-fil förhandsgranskas som PDF jämfört med samma XDP-fil som HTML i Designer. NPR-28602: Programfix för CQ-4260239

### Forms JEE-installationsprogram {#forms-jee-installer-3}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

### OSGI-paket och innehållspaket som ingår i 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

Förteckning över OSGi-paket som ingår i AEM 6.3.3.4

[Hämta fil](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Förteckning över innehållspaket som ingår i AEM 6.3.3.4

[Hämta fil](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Kumulativt korrigeringspaket 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.3 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.16.
* Sidnumreringen för principuppsättningslistan ändras till att begränsa 50 poster per sida.
* Tillagd rep: cachelagra i Ignorerbara noder på AEM Communities User Sync Listener i publiceringsinstanser.
* Lagt till ariaetikett för list- och kortvyknappar.
* Ett escape-tecken för kommatecknet inkluderas när en sökning utförs.
* Stöd för syntetiska resurser har aktiverats för innehållsprincip.

#### Resurser {#assets-5}

* Det går inte att hämta flera filer av typen .jp2,.max,.oft,.msg. NPR-28002: Programfix för CQ-4210856
* ImageServer-publiceringsinställningarna replikeras inte till hybridleverans. NPR-28329: Programfix för CQ-4253030

#### Communities {#communities-4}

* Tangentbordsnavigering har aktiverats för AEM Communities Enabled-komponenter vid publicering. NPR-27739: Programfix för CQ-4253856
* Aktiverad tangentbordsnavigering för att aktivera uppspelning av innehåll. NPR-27738: Programfix för CQ-4254026
* Lagt till ariaetikett för list- och kortvyknappar. NPR-27736: Programfix för CQ-4254027
* (Backport) Tillagd representant: cachelagra i Ignorerbara noder på AEM Communities User Sync Listener i publiceringsinstanser. NPR-27841: Programfix för CQ-4247234
* Specialtecknen har ett utgångstecken (\) i sökrutan på gränssnittsnivå. NPR-27839: Programfix för CQ-4259757
* Fel vid sökning efter tecken som (, +,? i snabb sökning. NPR-28212: Programfix för CQ-4260969
* Det går inte att ta bort kommentarer i användargenererat innehåll med API. NPR-28075: Programfix för CQ-4260534
* Kommentarer som skickas till nästa sida markeras med gult när en ny kommentar publiceras. NPR-28148: Programfix för CQ-4259681
* Det går inte att öppna meddelanden som har bifogade filer i mappen Utseende skickat och Inkorgen. NPR-28559: Programfix för CQ-4217072

#### Webbplatser {#sites-5}

* När du kör versionsrensning i AEM 6.3 visas en konstant upprepad varning i loggarna. NPR-27750; Programfix för CQ-4206870
* Formatinsticksprogrammet stöds inte i fullskärmsläge i textredigeraren. NPR-27622: Programfix för CQ-4258674
* List &#39;loaderPromises&#39; rensas inte efter att innehållsramen har lästs in i editor.js NPR-27768: Programfix för CQ-4205337
* Det går inte att ange mallprincip för kapslade parsyer utan att ange inställningar för den överordnade komponenten. NPR-27987: Programfix för CQ-4246095
* Komponentwebbläsaren sanerar inte användarindata och kan därför orsaka javascript-fel. NPR-27986: Programfix för CQ-4247590
* Sidan visas tom när användaren försöker redigera innehållsfragmentet. NPR-27669
* Markeringen av anteckningen försvinner när användaren klickar på anteckningen. BPR-27196: Programfix för CQ-4254423

#### Integrering {#integration-1}

* ResourceResolver kunde inte matcha flera domäner för målkomponenten. NPR-28265: Programfix för CQ-107847
* LiveCopy-arvsannullering fungerar inte korrekt på målbehållare eftersom inga åtgärder visas. NPR-28129: Programfix för CQ-4259813

#### Replikering {#replication-1}

* DispatcherFlushRules bryter replikering i 6.3.3.1 NPR-28150: Programfix för CQ-4261401

#### Campaign - målinriktning {#campaign-targeting-1}

* NullPointerException i TargetedContentManager. Programfix för CQ-4263485

#### Socialt - SCORM {#social-scorm}

* Ta bort referens till SCORM-molnet (Shareable Content Object Reference Model) i spelaren. Programfix för CQ-4260779

#### DAM - Allmänt {#dam-general}

* Hämtning via länkdelnings-e-post returnerar en tom/skadad ZIP. Programfix för CQ-4259686

#### MAC - Test&amp;Target-integrering {#mac-test-target-integration}

* Alternativet för att konfigurera målkomponent är inte tillgängligt för målgrupperna förutom standardmålgruppen. Programfix för CQ-4261370

#### Översättning {#translation-1}

* Aktivera stöd för tjänsten MS Translator i AEM 6.3 efter uppgradering av MS Translator till API v3.0. NPR-28365: Programfix för CQ-4259096

### Forms {#forms-5}

### Forms tilläggspaket {#forms-add-on-package-5}

#### Forms - arbetsflöde {#forms-workflow-1}

* Det går inte att återge PDF forms på HTML5-arbetsytan. NPR-28059: Programfix för CQ-4260373

#### Forms - dokumenttjänster {#forms-document-services-2}

* Det går inte att se några principuppsättningar utöver de första 1 000 som anges i vyn Principuppsättningar i Admin Console. NPR-28060, NPR-26047: Programfix för CQ-4249865
* Ett undantag genereras med namnet java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE som förhindrar att den kortlivade processen slutförs. NPR-28652

#### Forms - Adaptiv Forms {#forms-adaptive-forms}

* Det går inte att lägga till/ta bort objekt i listrutan när kryssruteobjekten markeras. NPR-28224: Programfix för CQ-4252834

### Forms - JEE Installer {#forms-jee-installer-4}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

### OSGI-paket och innehållspaket som ingår i 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

Förteckning över OSGi-paket som ingår i AEM 6.3.3.3

[Hämta fil](assets/do-not-localize/6333_bundle_list.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.3.3

[Hämta fil](assets/do-not-localize/content_package_list_6333.txt)

### Kumulativt korrigeringspaket 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.2 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i AEM 6.3 Service Pack 3.

Viktiga faktorer i AEM Cumulative Fix Pack är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.15.
* Stöd har lagts till för fliken Regler och dess användning i resursmappen i mappmetadataschemat.
* Aktiverat sidnumreringsstöd för grupplistsida vid publicering.
* UnreadCount för aktiverade meddelanden som ska konfigureras med valfritt antal. Standardvärdet är 20.
* Korrigeringar i extern länkkontroll.

#### Resurser {#assets-6}

* Listrutan Cascading stöds inte i dynamiska listrutor. NPR-27044; Programfix för CQ-4252564
* Förbättra frågan så att funktionen ExpiryNotification används. NPR-26999: Programfix för CQ-4251188
* Regelmigrering från metadataschema till mappmetadataschema. NPR-27771: Backport för CQ-4257737, CQ-4257735, CQ-4259822
* Justering av resursreferens kan inte uppdatera referenser för resurser som ingår i Sling ResourceCollections. NPR-26759: Programfix för CQ-4252605
* Hämtning via länkdelnings-e-post returnerar en tom/skadad ZIP-fil. NPR-27997: Programfix för CQ-4259686
* Hybrid-videokodningen slutförs inte och ingen miniatyrbild skapas. NPR-27122: Programfix för CQ-4255080

#### Webbplatser {#sites-6}

* Om överordnad sida pausas tas cq bort: LiveRelationship-blandningstyp från sidan som saknas. NPR-26996: Programfix för CQ-4254113
* (Extern länkkontroll) Interna länkar visas som brutna på enskilda sidor, men samma fungerar inte för externa länkar. NPR-27481: Programfix för CQ-4257780
* Arv av Cloud Service Config bryts när andra sidegenskaper redigeras. NPR-27311: Programfix för CQ-4256785
* Null-pekarundantag när ett Core Components-formulär används tillsammans med ett Foundation-formulär. NPR-27333: Programfix för CQ-4249176
* RTF-redigeraren tar bort den tomma alt-taggen. NPR-26938: Programfix för CQ-4253267
* (Klassiskt användargränssnitt) Prestandaproblem med   selectionchanged   avlyssnare om det finns flera listrutor. NPR-27115: Programfix för CQ-4237215
* När RTF-redigeraren kombineras med flera fält visas ett TypeError-undantag: fieldAPI.getName är inte en funktion vid foundation.js-fel inträffar. NPR-27146: Programfix för CQ-4253155, CQ-4259967
* Fokus/markör finns kvar i RTF-redigeraren även när du klickar på en alternativknapp i webbläsaren Safari. NPR-27144: Programfix för CQ-4249635
* Sidan visas som tom när användaren försöker redigera innehållsfragmentet. NPR-27669
* Det går inte att skapa en version för Experience Fragments. NPR-27689: Programfix för CQ-4259009

#### Integrering {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever går igenom hela trädet för att samla tillgängliga varumärken. NPR-27060: Programfix för CQ-4255790
* The   cq: åtgärder beaktas inte för målkomponenter. NPR-27616: Programfix för CQ-4257497

#### Sling {#sling}

* När data används i klasser med samma namn skapas den kod som inte är kompatibel. NPR-27282: Programfix för Sling-7581

#### Handel {#commerce-1}

* Uppdatera till Apache Felix http Jetty 4.0.6. NPR-26472: Programfix för Granite-22916

#### DAM - DM-klient {#dam-dm-client}

* En bild visas inte när brytpunkter har angetts i en dynamisk mediekomponent. Programfix för CQ-4256168

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet med relaterad video synkroniseras inte korrekt. Programfix för CQ-4251650
* Video spelas inte upp i redigeraren för visningsförinställningar för den blandade medieuppsättningen. Programfix för CQ-4251442

#### DAM - Allmänt {#dam-general-1}

* Länken till innehållsfragmentmodellen saknas efter att SP3-korrigeringen har tillämpats. Programfix för CQ-4259029

#### DAM - UI {#dam-ui}

* Mappmetadataschemats användargränssnitt bryts efter installation av SP3. Programfix för CQ-4257737

#### Communities {#communities-5}

* Lägg till sidnumreringsstöd för grupplistor vid publicering. NPR-26953: Programfix för CQ-4246525
* Olästa räkningsmeddelanden kan inte anges efter 21. NPR-27496: Programfix för CQ-4252829
* Begränsningen för användarabonnemang är begränsad till 1 000. NPR-27615: Programfix för CQ-4254689
* Ett fel uppstod vid överföring av en annan bifogad fil än bilden (till exempel .pdf) i forum. NPR-27375: Programfix för CQ-4257753
* Länk för svar fungerar inte med radklickning. NPR-24556: Programfix för CQ-4256138
* Relationer till användargenererat innehåll tas inte bort när användargenererat innehåll tas bort. NPR-27631: Programfix för CQ-4258706
* Det går inte att söka efter adressvärde i nyckelordssökning om gruppen är inställd med DSRP (Database Storage Resource Provider). NPR-27652: Programfix för CQ-4253261
* När du klickar på papperskorgsikonen på bilden efter borttagningsbekräftelsen tas den bifogade filen bort permanent. NPR-27340: Programfix för CQ-4255150
* Formposter och svar läggs till ovanpå den andra sidan och när de uppdateras flyttas inlägget till rätt plats överst på den första sidan. NPR-27341: Programfix för CQ-4247338
* Statusetiketten för slutförandestatus för aktiveringsSkorm visas tom i användargränssnittet. NPR-27152: Programfix för CQ-4249994
* När du aktiverar Tillåt behöriga bör de behöriga medlemmarna endast kunna skapa för användare som är community-medlemmar. NPR-27901: Programfix för CQ-4251235

#### uthållighet {#sustenance}

* Aktivitetsloggar för pakethanteraren ska extraheras i en separat loggfil. NPR-27323: Programfix för Granite-14866

#### Översättning {#translation-2}

* Översättningsförhandsgranskning fungerar inte med exempelinnehållet .retail. NPR-27170: Programfix för CQ-4241179

* Proaktiva platform.login-korrigeringar. NPR-26961
* Spara och stäng för sidegenskaper återgår inte till rätt sida i AEM WAR med Tomcat. NPR-27567: Programfix för Granite-23671

* Den angivna texten försvinner med funktionen sourceEdit när den har sparats. Programfix för CQ-4259273

### Forms {#forms-6}

### Forms tilläggspaket {#forms-add-on-package-6}

#### Forms - dokumentsäkerhet {#forms-document-security-1}

* Problem med samtidighet med JEE Client SDK. NPR-27572: Programfix för CQ-4247156

#### Forms - dokumenttjänster {#forms-document-services-3}

* Det går inte att skapa en formulärdatamodell baserad på SOAP i WebSphere. NPR-27692: Programfix för CQ-4253702

#### Forms - Adaptiva formulär {#forms-adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27863: Programfix för CQ-4257315
* AEM Forms Container-komponenten blir osynlig när fel formulär konfigureras på webbplatssidan och kryssrutan &quot;Forms cover the entire width of the page&quot; är markerad. NPR-25972: Programfix för CQ-4239287, CQ-4249133

### Forms JEE-installationsprogram {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* Det går inte att skapa en formulärdatamodell baserad på SOAP i WebSphere. NPR-27692: Programfix för CQ-4253702

#### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included}

Förteckning över OSGi-paket som ingår i AEM 6.3.3.2

[Hämta fil](assets/do-not-localize/63332bundle_list.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.3.2

[Hämta fil](assets/do-not-localize/6332content_package.txt)

### Kumulativt korrigeringspaket 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 3 (6.3.3.0) i september 2018.

AEM Kumulativt korrigeringspaket 6.3.3.1 är beroende av AEM 6.3 Service Pack 3. Du måste därför installera AEM Cumulative Fix Pack 6.3.3.x-paketet när du har installerat AEM 6.3 Service Pack 3. Installationsanvisningar finns i [AEM 6.3 Service Pack 3 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.14.
* Prestandaförbättringar för prediktiv och sökning.
* Korrigerat problem i FormData-hanteringen för standardvärdet.
* Uppgraderade FormBuilder till den senaste Handlebars-versionen.
* Added config servlet for the edit config for the RTE in dialog mode.
* Stöd för sammansatta fält har lagts till.
* Aktiverade/inaktiverade verktygsfältsobjekt i RTF-redigeraren med en innehållsprincip för redigeringsdialogrutan.

#### Resurser {#assets-7}

* När IDS-frikoppling är aktiverat länkar arbetsflödet för DAM-uppdatering inte längre referenser. NPR-26135: Programfix för CQ-4250933
* Det går inte att packa upp ett arkiv som har skapats i unarchiver-steget med en mapp med namnet %. NPR-26275: Programfix för CQ-4251482
* Ett enkelt citattecken förhindrar att metadata uppdateras. NPR-26808: Programfix för CQ-4254305
* (Omnissearch) Prestandaproblem vid sökning i en samling. NPR-26714: Programfix för CQ-4253408
* Användning av GQLConverter med en fulltextsökning som innehåller bokstäverna &quot;OR&quot; i texten behandlas felaktigt. NPR-26564: Programfix för CQ-4247362
* Delning av resurslänk från multi-tenant-prefix skapar en ogiltig URL. NPR-26482: Programfix för CQ-4253540
* Inaktivera sökvägen till företagets rotmapp i användargränssnittet för Dynamic Media Cloud-konfigurationen. NPR-26361: Programfix för CQ-4249505
* Inflödet av .mos RAW-filer förlängs. NPR-26296: Programfix för CQ-4250661
* Resurslänkdelning tillåter inte att fler än en intern användare med numeriskt användar-ID läggs till. NPR-26206: Programfix för CQ-4251466
* Skador i ZIP-filer komprimerade med deflate64-algoritmen. NPR-26793: Programfix för CQ-4253995
* Det går inte att skapa miniatyrbilder på ett korrekt sätt för komplexa PDF-filer, vilket resulterar i miniatyrbilder där en del av bilden saknas. NPR-26057: Programfix för CQ-4250944
* Problem med minnesanvändning för heap med generering av miniatyrbilder. NPR-25545: Programfix för CQ-4246960
* Om du skapar ett stort antal relationer för en resurs uppstår ett fel. NPR-26309: Programfix för CQ-4250708
* Alternativet &quot;Ta bort återgivning&quot; fungerar inte och returnerar felet &quot;ingenting att ta bort&quot;. NPR-26007: Programfix för CQ-4213414
* Det går inte att ta bort standardvärden för flervärdesfält. NPR-25116: Programfix för CQ-4247856
* (DM Hybrid) Katalogreplikeringsavbrott för AEM 6.3.2 med Dynamic Media. NPR-26406: Programfix för CQ-4251306

#### Webbplatser {#sites-7}

* Proaktiv support för platskorrigeringar. NPR-26963
* Taggar skapas två gånger om det finns skillnader i skiftlägestypen Rubrik och Namn. NPR-26877: Programfix för CQ-4254134
* RTF-redigeringsfunktionerna i redigeringsdialogrutan styrs inte av profiler. NPR-27059, NPR-26750: Programfix för CQ-4241130
* Client Context segment.js caching vs. frågor som inte cachelagras. NPR-26622: Programfix för CQ-4253486
* Aktivering av segmenteringsregel (t.ex./segmentering) för underordnade regler i klassiska syften, publicering går ner. NPR-26601: Programfix för CQ-4253588
* Om du lägger till specialtecken rullas dialogrutan för textredigeraren högst upp. NPR-26435: Programfix för CQ-4249869
* (Touchgränssnitt) Verktygsfältet kan inte användas med flera textredigerare när du växlar från helskärm till flytande dialogruta. NPR-25652: Programfix för CQ-4206008
* Om du befordrar en flersidig start skapas flera versioner för varje sida. NPR-26810: Programfix för CQ-4254663
* Åtgärder för att flytta taggar återspeglas inte i taggfält för strukturerade innehållsfragment. NPR-26801: Programfix för CQ-4251805
* (Touch UI) Det går inte att avpublicera den underordnade sidan från sidredigeraren efter att sidan har bytt namn i designen. NPR-26774: Programfix för CQ-4254175
* Den opublicerade sidan fungerar inte med referenser. NPR-26749: Programfix för CQ-4254372
* Om du vill skapa varianter som live-kopior måste användaren uppdatera sidan för att spegla. NPR-26663: Programfix för CQ-4254328
* (Klassiskt användargränssnitt) När du går tillbaka till sidegenskaperna används inte längre arv av miniatyrbilden, den tas bort från webbplatsadministratören och sidinsparken och bilden visas som tom. NPR-26562: Programfix för CQ-4252346
* När en version av en sida skapas och en jämförelse aktiveras, visas noderna från /content/ versionshistory i listan över live-kopior för utkast. NPR-26506: Programfix för CQ-4243957
* URL:er i Experience Fragment Admin Editor tillåter inte övertäckningar. NPR-26318: Programfix för CQ-4252156

#### Plattform {#platform}

* Sessionsläckage i ReplicationEventListener med testhändelser. NPR-25937: Programfix för CQ-4251090
* Replikeringen använder den utgångna token för OAuth som orsakar flera fel. NPR-25894: Programfix för GRANITE-22388

#### Integrering {#integration-3}

* TSDK inbäddat med AEM bryts med en uppgradering till Handlebars 4 på grund av att inkompatibla mallar används. NPR-26699: Programfix för CQ-4248974
* När du publicerar en sida med en ny resurs inaktiveras den underordnade sidan från publiceringsinstansen utan meddelande. NPR-24869: Programfix för CQ-4247832
* Replikeringen använder en token som har gått ut för autentisering. NPR-25984: Programfix för Granite-22388

#### Replikering {#replication-2}

* Http-transport kan läcka öppna sessioner. Programfix för Granite-17434
* Undantag i loggar när åtkomst till tokennod sker samtidigt av mer än en replikeringsagent. NPR-26964: Programfix för GRANITE-23276, Granite-23155

#### ContextHub {#contexthub}

* Filen &#39;coral.js&#39; innehåller en sårbar version av biblioteket &#39;handlebars.js&#39;. Programfix för CQ-4255377

#### DAM - DM-klient {#dam-dm-client-1}

* Om du tar bort en kopia av en bildresurs blir den ursprungliga bildresursen oanvändbar. Programfix för CQ-4251648
* Överflödig hämtning av extra bildinnehåll från S7-servrar. Programfix för CQ-4248770

#### Granit {#granite}

* AEM OAuth-providern utför inte den skiftlägeskänsliga sökningen. NPR-26133: Programfix för GRANITE-22650
* Paketvalideraren validerar inte paket som ingår i CFP/SP. NPR-26775: Programfix för Granite-22825

#### Communities {#communities-6}

* Avgränsarfel med sökresultat. NPR-27051: Programfix för CQ-4248939
* Ändra listvärdet från Dallas till Virginia i Adobe Storage Resource Provider. NPR-26936: Programfix för CQ-4254434
* Aktivera stöd för lokaliserad titelsökning i SocialTagManager. NPR-26932: Programfix för CQ-4250276
* Bilder i bifogade filer visar inte miniatyrbilder när ett foruminlägg skapas. NPR-26380: Programfix för CQ-4253105
* Insticksprogrammet Klistra in från Word läser inte in mer än en bild. NPR-26728: Programfix för CQ-4253638
* Det går inte att filtrera innehållet på modereringssidan. NPR-26697: Programfix för CQ-4213766
* (Säkerhetslucka) Upptagning av konto på grund av felaktig JWT-konfiguration. NPR-26440: Programfix för CQ-4253314
* Det tar lång tid att hämta data från lagringsresursprovidern i Adobe. NPR-26237: Programfix för NPR-24152
* Den privata meddelandesidan fungerar felaktigt och tröttsamt. NPR-26120: Programfix för CQ-4250923
* Meddelandet&quot;Markera alla som lästa&quot; återger endast de första 10 som olästa utan att sidan uppdateras. NPR-27036: Programfix för CQ-4254058
* Sidnumrering för communitykommentaravsnitt, klicka och sidinläsning. NPR-27030: Programfix för CQ-4251228
* (Forumsökning) Bakåtknappen hoppar över sidan och överför den tillbaka till forum.html. NPR-26949: Programfix för CQ-4254804
* Olästa meddelanden ökar inte med mer än 21. NPR-26947: Programfix för CQ-4251251
* (jobbet SearchScheduledPosts) Lägg till en aktivera/inaktivera-switch i ConfigMgr. NPR-26924: Programfix för CQ-4250463
* Tomcat Context(/aempublish) Path släpps när du rullar på uppdragssidan. NPR-26919: Programfix för CQ-4254345
* NullPointerException uppstod när en grupp och medlem skapades. NPR-26778: Programfix för CQ-4248095
* Moderatorns upphäv- och understrykning av innehåll som inte finns fungerar inte med MySQL Single Responsibility Principle (SRP). NPR-26767: Programfix för CQ-4251520
* Sök efter funktionalitetsproblem med vissa tecken. NPR-26726: Programfix för CQ-4247744
* Aktivera djupa länkar för modereringsgränssnitt och aktiveringsresurser. NPR-26705: Programfix för CQ-4251381
* Sök i forumkomponenten. NPR-26577: Programfix för CQ-4251303
* Att söka med för- och efternamn tillsammans i communitymeddelanden returnerar inte det förväntade resultatet. NPR-26377: Programfix för CQ-4253150
* Sidindelningen uppdateras inte när svar tas bort. NPR-26327
* Borttagning av post fungerar men ger ett fel på konsolen och posten visas fortfarande i användargränssnittet. NPR-26292: Programfix för CQ-4252803
* Sidnumreringen uppdateras inte dynamiskt och listan med svar fortsätter att ta längre tid. NPR-26145: Programfix för CQ-4251586
* Gruppinställningar läses inte in i en grupp som innehåller 50 000-talsanvändare. NPR-25642: Programfix för CQ-4238426
* Katalogresursspelaren misslyckades för kontextsökvägar. NPR-25640: Programfix för CQ-4238426
* (Forum Search) - Sidnumrerade länkar till trådar med många inlägg fungerar inte med meddelanden. Programfix för CQ-4254202
* Moderationskonsolen visar bara 5 poster med Firefox. Programfix för CQ-4254128
* Grupper visas inte när du skapar en plats. NPR-27148: Programfix för CQ-4251788
* Null-pekarundantag när grupper och medlemmar läggs till i rollinställningarna och den behöriga medlemmen i bloggfunktionen tillåts. NPR-21732, NPR-27176: Programfix för CQ-4255909
* Om du redigerar webbplatsen och lägger till medlemmar i rollinställningarna genereras ett null-pekarundantag. NPR-27132: Programfix för CQ-4255909

#### Användargränssnitt {#user-interface}

* Proaktiva inloggningsåtgärder för plattformen. NPR-26961
* (Flerfält) Tillåt att sammansatta objekt har egna namn. NPR-26493: Programfix för Granite-20568
* Kolumnvyn uppdateras inte när du har klistrat in en sida förrän den har uppdaterats. NPR-26030: Programfix för CQ-4236346
* Proaktiva granite.ui.commons-korrigeringar. NPR-26960
* Proaktiva granite.ui.content-korrigeringar. NPR-26959
* Proaktiva CQ-/händelseloggkorrigeringar. NPR-26943
* Proaktiv grundläggande gränssnittssupport. NPR-26942
* (IE11) &quot;NaN&quot; visas i nummerfältet när ett negativt värde anges. NPR-26701: Programfix för CQ-100826
* (Koral. Multifält) Kapslade multifält använder fel mall för att skapa objekten. NPR-25649: Programfix för CUI-6743
* Uppdatera koralui2- och coralui3-klienter för att ta bort Handlebars från bygget. NPR-25606: Programfix för Granite-22116

### Forms {#forms-7}

### Forms tilläggspaket {#forms-add-on-package-7}

#### Forms - dokumentsäkerhet {#forms-document-security-2}

* Undantag för huvudnyckelrollover i serverloggar för inaktiva nycklar. NPR-26748: Programfix för CQ-4253705
* Det går inte att skapa eller ändra vattenstämpelinställningar för dokumentsäkerhet. NPR-26267, NPR-26129: Programfix för CQ-4250234

#### Forms - dokumenttjänster {#forms-document-services-4}

* PDF/A-valideringen är inte giltig med validera PDF/A. NPR-25934: Programfix för CQ-4248558

#### Forms - Interaktiv kommunikation {#forms-interactive-communication}

* PDF- och HTML-förhandsgranskningen av brevet är synliga och fungerar i samma fönster när en redigerbar modul redigeras, sparas och sedan PDF-förhandsvisningen öppnas/stängs. NPR-26770: Programfix för CQ-4253217

#### Forms - arbetsflöde {#forms-workflow-2}

* Arbetsytan låser sig ibland och visar startpunkterna upprepade gånger. NPR-26461: Programfix för CQ-4253439
* ESAPI-undantag genereras i loggarna när klammerparenteser används i aktivitetsnamnet. Programfix för CQ-4256627
* Undantag för null-pekare genereras när en icke-förfylld adaptiv form/formuläruppsättning som är associerad med startpunkten öppnas. Programfix för CQ-4256124
* Det går inte att skicka e-post med den globala inställningen. NPR-26163: Programfix för CQ-11110
* Det går inte att öppna arbetsytan när filen axis.jar har använts. NPR-26131: Programfix för CQ-4251126
* Uppdateringsknappen kan inte synkronisera de senaste data från servern till adaptiva formulär. Programfix för CQ-4255670
* Om du anger en sökmall från administratörsgränssnittet och sedan använder samma för att söka efter uppgiften i AEM Forms arbetsyta genereras ett undantag. Programfix för CQ-4255649
* Spårningsinformation för processerna under programmen med parentessymbol i namnet visas inte på HTML-arbetsytan. Programfix för CQ-4242101
* Om du sparar ändringar på inställningsskärmen i HTML-arbetsytan genereras ett undantag. Programfix för CQ-4241485
* Gruppgodkännande bryts vid den senaste JEE-konfigurationen. Programfix för CQ-4241486
* Utkast av uppgift/startpunkt misslyckas på den senaste 6.4 JEE-servern. Programfix för CQ-4241484
* Ställ in parametern Date().getTime().toString så att den initierar sessionen i stället för Date.toString(). Programfix för CQ-4241483
* När du öppnar /lc/ws uppstår ett känsligt teckenundantag i HTML-parametern. Programfix för CQ-4241481

#### Sårbarhet {#vulnerability-1}

* En XSS-säkerhetslucka (Cross-Site Scripting) har lagrats på fliken Anteckningar i Forms Manager. NPR-27157: Programfix för CQ-4255556

### Forms JEE-installationsprogram {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Kodgranskning för Enterprise Security API. Programfix för CQ-4255638
* Det gick inte att läsa in esapi.properties som klassinläsarresurs i WAS9. Programfix för CQ-4255631
* Om du klickar på Lägg till autentisering under Domänkonfiguration uppstår ett fel. Programfix för CQ-4255634
* Forms JEE har stöd för PKCS#11, ömsesidig autentisering. NPR-21372
* Åtgärdade problemen som rapporterades i den statiska kodanalysen av Core. Programfix för CQ-104446
* Distributionen av adobe.livecycle.weblogic.ear och adobe.livecycle.websphere.ear misslyckas under körning av LCM. Programfix för CQ-4255629, CQ-4255630
* Ogiltiga felmeddelanden i programhanteringen. NPR-23289: Programfix för CQ-4233163, CQ-4255636
* Om du klickar på Lägg till autentisering under Domänkonfiguration uppstår ett fel. Programfix för CQ-4255634

#### Forms - JEE Connector {#forms-jee-connector}

* Åtgärdar problem som rapporterats i statisk kodanalys av Connector. NPR-22260

#### PDFG-tjänst {#pdfg-service-1}

* org.jgroups.Message error in the logs after upgrade from LiveCycle to AEM 6.2 forms. NPR-26795: Programfix för CQ-4220415
* AEM - Fel vid migrering av format. Programfix för CQ-4251969
* Åtgärdade problemen som rapporterades i den statiska kodanalysrapporten för PDFG. NPR-23251: Programfix för CQ-4213930

#### OSGI-paket och innehållspaket som ingår i 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}

Förteckning över OSGi-paket som ingår i AEM 6.3.3.1

[Hämta fil](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.3.1

### Kumulativt korrigeringspaket 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av 6.3 Service Pack 2 (6.3.2.0) i april 2018.

AEM Kumulativt korrigeringspaket 6.3.2.2 är beroende av AEM 6.3 Service Pack 2. Du måste därför installera AEM Cumulative Fix Pack 6.3.2.x-paketet när du har installerat AEM 6.3 Service Pack 2. Installationsanvisningar finns i [AEM 6.3 Service Pack 2 versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html).

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.11.
* Aktiverade delresurser och visningsprogram för flersidiga resurser på Brand Portal.
* Längden på fälttypen har ändrats till 255 för att stödja alla möjliga MIME-typer för olika typer av bilagor.
* Konfigurerat felmeddelande från servern när en bild bryter mot överföringsvillkoren.
* Stöd för STARTTLS har lagts till i Day CQ Mail Service.
* Uppdatera till de senaste versionerna av cq-wcm-content och com.adobe.cq.launches.it.serverside.
* Uppdatera com.adobe.granite.ui.coralui3-hastighet till den senaste versionen som släppts.
* Försäkrat återgivningsvillkor returnerar ett tillräkneligt resultat om expressionResolver är null.
* Coral.ColumnView: Stöd för Skift+klick har lagts till.

### Resurser {#assets-8}

* Fältet CUG (Asset Folder Closed User Group) returnerar inte gruppen Alla. NPR-23163: Programfix för CQ-4239377
* Sökning efter sparade sökningar i smart samling returnerar inte alla resultat. NPR-23243: Programfix för CQ-4240355
* (ExpiryNotificationJobImpl) Optimering av den befintliga frågan. NPR-23330: Programfix för CQ-4205249
* (Metadataprofil) Standardvärden för taggar som anges när de skapas är inte tillgängliga när de har sparats. NPR-23370: Programfix för CQ-4235458
* (Touch UI) Det går inte att flytta flera resurser på grund av JS-fel. NPR-23395: Programfix för CQ-4241279
* Hämtningsstorleken stämmer inte överens med den information som visas, vilket kan skapa förvirring för användarna. NPR-23418: Programfix för CQ-4242774
* Den extraherade mimetypen för filtillägget LSR och SKETCH är felaktig och leder till ogiltig filhämtning. NPR-23644: Programfix för CQ-4243260
* (Firefox/Chrome) Det går inte att hämta resurser på sidan Resursdelning. NPR-23963: Programfix för CQ-4244391
* Sökfack för resursadministratörer försvinner i sökpaneler efter förhandsgranskning. NPR-23964: Programfix för CQ-4244410
* Om du avpublicerar sökformuläret tas standardsökformuläret bort helt. NPR-23291: Programfix för CQ-4241382
* (Brand Portal) Sökningen i katalogpredikatet bör filtreras bort vid replikering. NPR-23292: Programfix för CQ-4241385
* Det går inte att publicera till Brand Portal UI. NPR-23293: Programfix för CQ-4241161
* Knappen Publicera/avpublicera till Brand Portal ska inte vara tillgänglig för innehållsfragment. NPR-23318: Programfix för CQ-4245086
* (Brand Portal) Gör det möjligt att skapa underresurser när en resurs publiceras. NPR-23331: Programfix för CQ-4242018
* Dynamic Media-begäranden använder inte den gemensamma proxyklienten/HTTP-klienten. NPR-10727: Programfix för CQ-45695, CQ-88800
* Det går inte att anteckna i MP4-videoresurs för en rendering i Dynamic Media S7 (DMS7). NPR-22046: Programfix för CQ-4215912
* EmbedXMP-data anges alltid till&quot;active&quot; för Ptiff-genereringsprocessen. NPR-22903: Programfix för CQ-4234498
* Problem med visning/urval av dynamisk återgivning med stort antal förinställningar för bilder. NPR-23151: Programfix för CQ-4217511
* Problem med Dynamic Media Encode Video - Modification/Reupload Lacher. NPR-23237: Programfix för CQ-4240260
* Korrigering för proxyhantering för HTTP-vidarebefordrare i Dynamic Media S7. NPR-24001: Programfix för CQ-244140

### Webbplatser {#sites-8}

* Frågebyggaren-diskrepanser som resulterar i en annan xPath-översättning mellan 6.2 och 6.3. NPR-23245: Programfix för CQ-4240396
* Fliken Miniatyrbilder i sidegenskapen fungerar inte när du utökar dialogrutan. NPR-22844: Programfix för CQ-4241474
* Parsys bryter emulatorenhetens bildrutebredd och beskär alla komponenter som läggs till i den. NPR-22926: Programfix för CQ-4238224
* När du kör flera starter befordras starten i Författare, men ändringarna replikeras inte på publiceringsservern på grund av att replikeringsbehörighet saknas. NPR-22934: Programfix för CQ-4234746
* En sida som är låst av en användare i den första sessionen kan ändras av en annan användare i en annan session. NPR-23057; Programfix för CQ-4199017
* Åtgärda omsorteringsalternativ i listvyn. NPR-23065: Programfix för CQ-4239321
* (Sidredigerare) Bild på en bildkomponent försvinner när du öppnar dialogrutan igen. NPR-23156: Programfix för CQ-4239978
* Mallredigeraren visar bara upp till 20 mallar/mappar och läser inte in de andra när du bläddrar till sidans nedre del. NPR-23185: Programfix för CQ-4238483
* (Klassiskt användargränssnitt) Ett fel genereras när sidorna flyttas eller byter namn. NPR-23213: Programfix för CQ-4240971
* Det går inte att redigera/skapa ContextHub-segment. NPR-23218: Programfix för CQ-4226948
* (RTF-redigerare) - Åtgärden Ersätt ändrar ett ords format. NPR-23271: Programfix för CQ-4239677
* Knappen Övergång saknas på fliken Utskrift för XF-variationer. NPR-23320: Programfix för CQ-4240404
* Klassiskt användargränssnitt kan inte redigera CUG på grund av borttagning. NPR-24122: Programfix för 4241823
* Förebyggande åtgärder som skyddar mot oönskat innehåll. NPR-24387: Programfix för 4244993
* En gång. 80 fragment läggs till i en mapp i Resurser, fel som uppstår när arbetsflödet aktiveras från tidslinjekonsolen. NPR-23393; Programfix för CQ-4211216
* Det går inte att dra och släppa bilder i dialogrutan för textredigeraren från innehållssökaren. NPR-23403: Programfix för CQ-4242094
* Felet &#39;Ogiltigt värde för rekursionsväljare&#39; uppstod när en komponent skulle migreras från AEM 6.0 till AEM 6.2. NPR-23532: Programfix för CQ-4241258
* (RTF-redigerare) Verktygstips visar variabelnamnet för plugin-programmet i stället för det läsbara plugin-programnamnet. NPR-23550: Programfix för CQ-4243269
* Det går inte att spara dialogrutan med den valda listrutan som krävs i mobil-/surfplatteversion. NPR-23904: Programfix för CQ-4243096
* Alternativ för formatsystem visas på alla sidor efter 6.3.2.1-installation. NPR-23972: Programfix för CQ-4244394
* Klassiskt användargränssnitt kan inte redigera CUG på grund av borttagning. NPR-24122: Programfix för 4241823
* Förebyggande åtgärder som skyddar mot oönskat innehåll. NPR-24387: Programfix för 4244993
* Resursreferenser uppdateras inte när resurser flyttas. NPR-23208: Programfix för CQ-4239879

### Plattform {#platform-1}

* Smart samling visar inte resultat efter spara om taggpredikatet används i sökfunktionen. NPR-23401: Programfix för Granite-21278
* Patch jQuery 1.12.4 from clientlib to include security fix. NPR-24128: Programfix för Granite-20058
* Internationaliseringsöversättningar uppdateras inte om inte paketet startas om. NPR-23193: Programfix för Sling-7190
* Resurslösaren som inte stängts i ReplicationEventListener. NPR-23240: Programfix för CQ-4241350
* Stöd för STARTTLS i&quot;Day CQ Mail Service.&quot; NPR-23941: Programfix för CQ-4240397
* JCR-adresstaggens namn ska fyllas i automatiskt baserat på taggens titel. NPR-24173: Programfix för CQ-4199411

### Integrering {#integration-4}

* (Mål) Kampanjer aktiveras inte när API-typen används som XML. NPR-23199: Programfix för CQ-4240936****
* Konfigurationsreferensreplikeringen misslyckas med den mellanliggande mappstrukturen. NPR-23485: Programfix för CQ-4242751

### Sårbarhet {#vulnerability-2}

* Salesforce-integreringen är sårbar för SSRF (Server Side Request Forgery). NPR-24289: Programfix för CQ-424527
* XSS (Cross-site scripting) i Admin UI Project-länkar. NPR-23272: Programfix för CQ-4241795

### WCM - Foundation Components {#wcm-foundation-components}

* Foundation-tabellen är sårbar för lagrade korsskriptning mellan webbplatser. NPR-23214: Programfix för CQ-4240760

### Översättning {#translation-3}

* Live copy-egenskaper tas inte bort när språkkopior skapas. NPR-23123: Programfix för CQ-4230641

### Användargränssnitt {#user-interface-1}

* DatePicker har inte stöd för att manuellt ange ett externt texttips som angetts av dolda fält. Om du ändrar typtipset uppstår ett konverteringsfel. NPR-23371: Programfix för Granite-21194
* Coral.ColumnView: Lägg till stöd för Skift+klick. NPR-23404: Programfix för Granite-13338
* Markeringsdatatypen validerar inte när ett objekt med ett tomt värde är markerat. NPR-23405: Programfix för Granite-21283
* (OMEGA) Rapportera &quot;Feature&quot; (Funktion) endast på engelska. NPR-23990: Programfix för Granite-21231
* Korrigerar till Coral.Autocomplete API. NPR-23516

### Granit {#granite-1}

* Apache Http-klientspårningsanslutningar och högt heap-utnyttjande gör att AEM kraschar. NPR-23906: Programfix för Granite-21056

### Handel {#commerce-2}

* Kampanjens json-utdata innehåller inte serverkontextroten. NPR-23733: Programfix för CQ-4243827

### Communities {#communities-7}

* Det går inte att söka i communities på grund av få ord. NPR-23256: Programfix för CQ-4240717
* Det gick inte att tilldela grupper för rollproblem för community-chefer. NPR-23317: Programfix för CQ-4241233: CQ-4221399
* Problem med att skapa en resurs med liknande resursnamn. NPR-23319: Programfix för CQ-4240700
* (ContextPath) Brytande meddelandefunktionalitet bryts för Jetty-konfigurationer och fel vid sökning av gruppmedlemmar i medlemslistan för communitygrupper. NPR-23336: Programfix för CQ-4241519, CQ-4242080
* Överföring av en bild till ett webbforum visas inte i Adobe Storage Resource Provider (ASRP). NPR-23397: Programfix för CQ-4242497
* Borttagna idéer visas som aktiva länkar i aktiviteter. NPR-23406
* imsmanifest.xml kan inte läsas in med AEM som körs med kontextroten. NPR-23483: Programfix för CQ-4242193
* Säkerhetsluckor i en äldre version av Handlebars. NPR-23518: Programfix för CQ-4243055
* Tunneltjänsten fungerar inte. NPR-23543: Programfix för CQ-4242217
* Problem med communitykomponenter när de används via dispatcher och sling dynamic är aktiverade. NPR-23586: Programfix för CQ-4242360, CQ-4241522
* När du söker efter en sökterm som ger många resultat genom sökning och sedan anger en ny sökterm, återställs inte sidindelningen. NPR-23739: Programfix för CQ-422593
* Problem vid sökning i forumkomponenten. NPR-23838: Programfix för CQ-4243770
* (Flaggning för communitymoderering) Det går inte att skicka flaggade meddelanden gruppvis. NPR-23845: Programfix för CQ-4243962
* Text på sorteringsknappen som inte visar det markerade standardvärdet trots   för att välja standardsorteringsordning. NPR-23881: Programfix för CQ-4243375
* Webb- och e-postmeddelanden utlöses inte på grund av ett meddelandefel för grupperna. NPR-23934: Programfix för CQ-4242880
* Ingen information om flagganvändare och orsaker visas med DSRP-konfigurationen. NPR-23973: Programfix för CQ-4243205
* Flaggorsaker från oflaggade användare förblir synliga/NPR-23974: Programfix för CQ-4243822
* Om två filer med samma namn bifogas två gånger till ett formulärinlägg uppstår ett serverfel. NPR-24166: Programfix för CQ-4244367
* Det går inte att lagra bilagor med MIME-typer som är längre än 15 tecken med hjälp av DSRP (Database Storage Resource Developer). NPR-24174
* När en bild som bryter mot överföringsvillkoren dras och släpps i posttexten, genereras ett serverfel och ett generiskt felmeddelande visas för användaren. NPR-24243
* Korrigerar flera serverproblem från AEM Communities. NPR-23971: Programfix för CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Korrigeringar av flera Adobe Social-problem. NPR-24242: Programfix för CQ-4245054, CQ-4245120, CQ-4245296

### Campaign {#campaign}

* Kampanjens json-utdata innehåller inte serverkontextroten. NPR-23733: Programfix för CQ-4243827

### MSM {#msm}

* När du rullar ut sidan visas inte egenskaperna för På/av-tid som ärvts från överordnad. NPR-23873: Programfix för CQ-4243431
* LiveCopy-åtgärden ignorerar inte underordnade noder för borttagna komponenter. NPR-23058: Programfix för CQ-4211662

### Avlastning {#offloading}

* Begär en mekanism för att rensa resurser från arbetstagarinstanserna efter bearbetning eller regelbundet. NPR-23638: Programfix för Granite-21337

## Forms {#forms-8}

### Forms tilläggspaket {#forms-add-on-package-8}

#### Adaptiv Forms {#adaptive-forms-1}

* Flytta ReCaptchaConfigService till det interna paketet. Programfix för CQ-4217459
* Numeriskt fält uppfyller inte minimivärdet. NPR-23967: Programfix för CQ-4244830
* Stöd för Multi Shard i adaptiv Forms-integrering med Adobe Sign. NPR-23383

#### Integrering med backend {#backend-integration}

* (FDM) (WebService) Stöd för WSDL-tilläggets konstruktion i WSDL Parser. NPR-23640, NPR:23236: hotfix för 4205821
* Att inkludera SDLInvokerParams i Forms Add-on Client SDK. NPR-23157

### Forms JEE Installer {#forms-jee-installer-7}

#### Processhantering {#process-management}

* Det går inte att öppna arbetsytan när den nya filen axis.jar har använts. NPR-23316
* LiveCycle är sårbart för XSS på PMAdmin. NPR-23267
* När du har uppgraderat till AEM 6.1 Forms låser sig HTML Workspace vid åtkomst till uppgiftslistan för specifika användare. NPR-23943

#### Core {#core}

* Forms JEE har stöd för PKCS#11, ömsesidig autentisering. NPR-21372

#### PDFG-tjänst {#pdfg-service-2}

* Tjänsten Paper capture kraschar vid samtidig bearbetning av TIFF-filer (ca 50 kB storlek). NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output - alternativ beskrivning saknas för anteckningar. NPR-22207
* Stöd för PDF/UA i XML-formulär som genererats via Designer och Output Service. NPR-23132

### OSGI-paket och innehållspaket som ingår i 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

Förteckning över OSGi-paket som ingår i AEM 6.3.2.2

[Hämta fil](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.2.2

[Hämta fil](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Kumulativt korrigeringspaket 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av 6.3 Service Pack 2 (6.3.2.0) i april 2018.

Huvudinnehållet i **AEM Cumulative Fix Pack** är:

* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.10.
* Förbättrad rendering av Parsys-komponenter i Classic UI.
* Uppdaterade paket med segmentmodeller för att inkludera teckenuppsättningskorrigering.
* Publicera asynkront på Brand Portal för alla resurstyper.
* Uppdaterat coralui-component-richtexteditor.git från 0.1.15 till 0.1.16
* Korrigeringar i funktionerna för att visa/dölja i nedrullningsbara komponenter.
* Aktiverad bildbläddring för kärnbildkomponenten.
* Uppdaterad felix   http-paket för att aktivera sessionsattribut.

* Cachen=true har tagits bort för delningsmodeller på grund av minnesförbrukningsproblem.

### Resurser {#assets-9}

* När du ändrar titeln eller miniatyrbilden i Resursmappsinställningar åsidosätts mappens ursprungliga grupp och behörigheter. NPR-22171: Programfix för CQ-4216080
* Användargränssnittet genererar det falska felet&quot;Publicera till Brand Portal misslyckades&quot; medan jobbet läggs till i replikeringskön och resurser publiceras i Brand Portal. NPR-22179: Programfix för CQ-4205273
* (Touch UI) Standardplats för överföring av resurser i kolumnvyn. NPR-22465: Programfix för CQ-4237057
* AEM genererar ett StackOverflow-fel vid försök att kopiera ett objektschema från /conf/global till /conf/ mytenant. NPR-22489: Programfix för CQ-4235875
* Ett försök att packa upp ett ZIP-arkiv misslyckas på grund av att utrymmet i slutet av mappnamnet är slut. NPR-22522: Programfix för CQ-4238036
* Sortering med resursens titelkolumn fungerar inte för sökresultat. NPR-22908: Programfix för CQ-4239076
* YouTube-video taggas med hela sökvägen i stället för själva taggnamnet. NPR-22976: Programfix för CQ-4238669
* Det går inte att ändra ordning på mappar under en omsorteringsbar mapp. NPR-23125: Programfix för CQ-4231761
* HTTP 504: Gatewaytimeoutfel vid försök att dela samlingar med hjälp av delningslänk. NPR-21928: Programfix för CQ-4234507
* PDF-nyckelordsmetadata extraheras och ändras inte korrekt när flera nyckelord är associerade med en PDF-resurs. För att lösa problemet har metadataegenskapen för ämnesfältet tagits bort för PDF-resurser. Du kan emellertid redigera metadatarammet och lägga till ett textfält med flera värden för ämnesfältet. NPR-21972: Programfix för 4215741****
* Fel resurser tas bort om den valda mappen ändras mellan den tidpunkt då de två popup-fönstren visas. NPR-21980: Programfix för CQ-4233675
* (DAM) Flera XSS-säkerhetsluckor (Cross-site Scripting) när du lägger till i samlingsguiden. NPR-22432: Programfix för CQ-4327086
* Det går inte att hämta resurser när du använder Digital Rights Management i resurser på Safari. Användare kan inte hämta resurser med ansvarsfriskrivning och långa filnamn. NPR-22747: Programfix för CQ-4236460 och CQ-4235274
* Gör offentlig delning till standardalternativ när du publicerar material till Brand Portal. NPR-21931: Programfix för CQ-4218816

### Webbplatser {#sites-9}

* Ett nytt objekt i inkorgen för arbetsflöden visar sidsökvägen i stället för sidans rubrik. NPR-21634: Programfix för CQ-4230672
* Redigerbara strukturkomponenter förlorar CSS-klassnamn som behövs för det responsiva rutnätet när de redigeras. NPR-21741: Programfix för CQ-4232374
* (TouchUI) Sårbarheter med XSS (Multiple Cross-site scripting) för HTML-komponenter. NPR-21899: Programfix för CQ-4232511
* Det går inte att ändra innehållets fragmentresurstyp för blandad mediabild. NPR-21907: Programfix för CQ-4233401
* RTE-helskärm I dialogrutan Touch UI döljer RTE-plugin-program. NPR-22034: Programfix för CQ-4235457
* (Touch-gränssnittet) RTF-redigeraren tar bort alla andra attribut än id från taggen &lt;a>. NPR-22044: Programfix för CQ-4234133
* Flera staplade parsyer på grund av långvariga frågor (fler än 6) gör AEM trög. NPR-22134: Programfix för CQ-4233904
* Det går inte att ändra behörigheter för noder som har kolon i namnet. NPR-22136: Programfix för CQ-4236221
* (Klassiskt användargränssnitt) RTF-redigerarutdata html lägger till &quot;list-position-style: inside;&#39; som inline style to the &lt;ul> tag. NPR-22145: Programfix för CRTE-114
* Gör så att TreeNode återgår till namnattributet när texten är tom. NPR-22146: Programfix för CQ-4234724/CQ-4236300
* RSS-flödesproblem, port -1 till AEM 6.3. NPR-22176: Programfix för CQ-423339
* (Klassiskt användargränssnitt) Kortkommando för inklistring av text (Ctrl+V) fungerar inte för OTB-text-komponenten (RTF). NPR-2224: Programfix för CQ-4236224
* Taggfältets filtrering fungerar inte som förväntat när texten skrivs. NPR-22236: Programfix för CQ-4236655
* (Page Editor) När du klistrar in textdata i en bildschemakomponent klistras även textkomponenten in när du klistrar in textdata i en bildschemakomponent. NPR-22264: Programfix för CQ-4236230
* Det obligatoriska fältet Dialog FileUpload orsakar problem när dialogrutor skickas. NPR-22464: Programfix för CQ-422192
* Om du flyttar utan replikeringsbehörigheter startar en begäran om aktiveringsarbetsflöde om den flyttade sidan eller dess referenter inte kan aktiveras. NPR-22467: Programfix för CQ-4211765
* Prestandaproblem vid inläsning av en sida med stora (2 000+) målgrupper. NPR-22478; Programfix för CQ-4209567
* Persistensproblem när ContextHub lagrar överskrivningar av standardlager för beständighet under initieringen. NPR-22479: Programfix för CQ-4218399
* Launch med flera sidor publicerar inte undersidor till publiceringsservrar om Inkludera undersidor inte är markerat i den första innehållets rot. NPR-22482: Programfix för CQ-4237818
* (Touch UI) Borttagning av starter via Classic UI-konsolen gör att alla sidor inte kan redigeras. NPR-22491: Programfix för CQ-4225074
* Problem med bildkomponenten på grund av extra utrymme i dialogrutan. NPR-22528: Programfix för CQ-4238183
* När komponenten öppnas i inbyggt läge visas inte plugin-program som lästs in tidigare den andra gången. NPR-22591: Programfix för CQ-4236850
* Om du tar bort en start i en kapslad start blir delstarterna överblivna. NPR-22621; Programfix för CQ-4202639
* (Klassiskt användargränssnitt) Fliken Arbetsflöde är inaktiverad när sidan är i arbetsflödets låsstadium. NPR-22722: Programfix för CQ-4237557
* När du har bläddrat en bild som lagts till i bildkomponenten på en sida sparas inte ändringarna och originalbilden visas på sidan. Återgivningsstöd har lagts till i bildkärnkomponenten via [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: Programfix för CQ-4221539
* När användaren försöker ta bort den befintliga ankarpunkten från ankarmenyn stängs komponentfönstret för textredigeraren och ändringarna sparas inte. NPR-22802: Programfix för CQ-4238167
* Omsökningsfiltret visar inte alla åtgärder i webbplatskonsolen. NPR-22804: Programfix för CQ-4239007
* Problem med kopiera/klistra in i Touch-gränssnittet med operativsystemets Urklipp och det interna AEM Urklipp. NPR-22807: Programfix för CQ-4220383
* Inkonsekvent markering av utdrag som returnerats av Lucene Search. NPR-22879: Programfix för CQ-4238513
* Om du aktiverar en sida med publiceringsinstanser inaktiverade blir resultatet grönt i stället för gul. NPR-22927: Programfix för CQ-4236310
* (StyleSystem) Skärmpositionen hoppar när du väljer format på popup-menyn. NPR-23183: Programfix för CQ-4238867
* (Hantera publikation) Om du vill gå till nästa månad i kalendern måste du klicka flera gånger. NPR-23508: Programfix för CQ-4242732

### Plattform {#platform-2}

* Sling Exporter-servleten exporterar inte japanska tecken korrekt. NPR-22153: Programfix för CQ-4228920
* Schemaläggarens dödläge vid start. NPR-22440: Programfix för Sling-7004
* Det går inte att synkronisera grupper mellan två publiceringsinstanser. NPR-21943: Programfix för Granite-19564
* Prestandaproblem med org.apache.sling.i18n delad session/resurslösare. NPR-23390: Programfix för Sling-7543

### Integrering {#integration-5}

* Resurslösaren är inte stängd i com.day.cq.analytics.sitecatalyst. NPR-22323: Programfix för CQ-4236515
* TargetContentImpl gör AEM trög under långa frågor. NPR-22361: Programfix för CQ-4236907
* Målmotorn (mbox.js, at.js) använder inte inbyggda URL:er och URL:er som innehåller kolon som kan misslyckas vid vissa distributioner. NPR-22366: Programfix för CQ-4237854
* När du anger en anpassad at.js eller mbox.js skrivs inkluderingsskriptet på sidan som text i stället för som HTML-taggar. NPR-22441: Programfix för CQ-4203691
* I målläget kan författare ändra en komponent som ärvts från utkastet utan att avbryta arvet. NPR-22751: Programfix för CQ-4237907
* PersonalizationDataSource genererar ett Null-pekarundantag på grund av att jcr saknas: innehållsnod. NPR-22850: Programfix för CQ-422122
* AEM misslyckas när icke-engelskt språk används. NPR-22917: Programfix för CQ-4218213
* Relaterade resurser saknas när en sida med riktat innehåll publiceras. NPR-23064: Programfix för CQ-4227119
* Användare kan inte se testvärden för statiska parametrar i mbox-anropet som kan ses när de testar med AT.js som klientbibliotek i molnkonfiguration. NPR-21930: Programfix för CQ-4234520

### WCM-Foundation-komponenter {#wcm-foundation-components-1}

* iParsys skapar positionsförflyttningen efter avmarkering av kryssrutan Avbryt/inaktivera arv. NPR-21905: Programfix för CQ-4230951
* Visa/dölj-funktionen för den nedrullningsbara formulärkomponenten fungerar inte som förväntat. NPR-22327: Programfix för CQ-422853
* CAPTCHA-komponenten har tagits bort för bättre säkerhet, och om du använder CAPTCHA-komponenten visas meddelandet&quot;Captcha-komponenten är föråldrad och bör inte längre användas&quot;. kommer att visas när 6.3.2.1-versionen eller senare har installerats. AEM kan anpassas så att de innehåller reCAPTCHA för bättre säkerhet NPR-22151: Programfix för CQ-4220052

### WCM - sidredigeraren {#wcm-page-editor}

* XSS (Cross-site scripting) speglades när en ogiltig väljare användes. Programfix för CQ-4270397

### Översättning {#translation-4}

* Undersök problem med funktionen Förhandsgranska. NPR-22114: Programfix för CQ-4223753

### Användargränssnitt {#user-interface-2}

* Problem med kalenderns månadsväljare när datumintervallet min och max har angetts. NPR-22716: Programfix för CUI-7187
* (Klassiskt användargränssnitt) Komponenten visar standardvärdena även om den associerade datamodelltjänsten för formulär är inställd på ett tomt fält. NPR-22272: Programfix för GRANITE-19744

### Granit {#granite-2}

* Stabilitetsproblem med utgivarinstansen AEM resursen orsakade av minnesläckage. NPR-22205, NPR-23178: Programfix för Sling-5668, Sling-7292 och Sling-7470.
* Instabilt tjänst-ID får inte användas för sessionsattributnamn. NPR-22821: Programfix för Granite-21059
* När en http   whiteboard-hanterad session ogiltigförklaras, behållarsessionen ogiltigförklaras även om sessionen inte har några andra sessionsattribut. NPR-23059: Programfix för FELIX-5819
* LogbackManager kan sakna OSGi-konfigurationen när programmet startas. NPR-23060: Programfix för Granite-19791

### Handel {#commerce-3}

* Aktivera skapandet av arbetsflöde på menyn Experience Fragments. NPR-22347: Programfix för CQ-4221661
* Upplev fragmentfel som kan reproduceras på WeRetail. NPR-21958: Programfix för CQ-4220061
* När du aktiverar en sida som innehåller ett borttaget upplevelsefragment genereras ett NullPointerException. NPR-23179: Programfix för CQ-4239939

### Projekt {#projects}

* (Flerspråksprojekt) Projektet innehåller inte översättningsjobb för mer än 19 språk. NPR-22498: Programfix för CQ-4229978

### Arbetsflöde {#workflow}

* (Klassiskt användargränssnitt) Om du aktiverar eller inaktiverar en arbetsflödeskörare kan det leda till ett felaktigt beteende. NPR-22907: Programfix för CQ-4239153

## Forms {#forms-9}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

AEM Forms i korthet:

* Stöd för HTML5-indatatyp har lagts till.
* Fast grundläggande autentisering av SOAP-huvud.
* Stöd för rubrikattribut för hyperlänk har lagts till.
* Aktiverad PDF/UA-identifierare i tillgänglighetsträdet i Forms Designer.
* Aktiverad certifikatautentisering för Workbench-användare.
* Stöd för att skapa PDF-filer som är PDF/A-2a- eller PDF/A-3a-kompatibla har lagts till.

### Forms tilläggspaket {#forms-add-on-package-9}

#### Forms-administratörsgränssnitt {#forms-admin-ui}

* Lösenordet visas i oformaterad text vid kontroll av lösenordsfält för konfigurationssidor för ECM Connectors. NPR-22508: Programfix för CQ-4236065

#### Forms Service {#forms-service}

* När SSL är aktiverat fungerar inte händelserna Submit och Abandon med Form Analytics. NPR-22637; Programfix för CQ-4237973

#### Användarhantering {#user-management}

* Det gick inte att synkronisera LDAP på grund av en felaktig cglib-nodep-version. NPR-22493: Programfix för CQ-4234099

#### Adaptiv Forms {#adaptive-forms-2}

* Anpassade funktioner för regelredigeraren lägger till en extra funktion; efter funktionsanrop och därmed misslyckas valideringen även om den anpassade funktionen returnerar true. NPR-22481: Programfix för CQ-4235499
* Oavsett vilket datummönster som valts följer datumväljarkomponenten inte mönstret när min- och maxvalideringsmeddelanden visas. NPR-22444: Programfix för CQ-4236269
* Datumformatet som skickas i en förfrågan bör anpassas till mönstret som anges i datumväljarkomponenten. NPR-22384
* Det angivna maximala antalet tecken för en textruta med anpassningsbara formulär stöds inte på Android 6.0 Samsung-enheter. NPR-22363, NPR-22364: Programfix för CQ-4235205
* (Microsoft Edge) (IE11) Textfältskomponenten Adaptiv form med flerradsfält visar &quot;Null&quot; som standardvärde i stället för tomt. NPR-22284: Programfix för CQ-69107
* SOAP UTF-8 Input Encoding in Adaptive Forms returnerar fel med felaktig sidnumrering. NPR-20105: Programfix för CQ-422669
* AEM Forms Container Component kan inte redigeras när fel formulär har konfigurerats på webbplatssidan. Programfix för CQ-4237456
* Utvecklingstester misslyckas när de körs på JEE-servrar. Programfix för CQ-4222082
* AF-tester misslyckades på JEE-servrar på grund av minifieringsproblem i Calvin-ramverket. Programfix för CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) Det går inte att uppdatera XML-schemaegenskaperna för Adaptiv Forms eftersom alternativen i DOR (Document of Record) inte kommer som de är förinställda på egenskapssidan. NPR-22298: Programfix för CQ-4237402
* Forms som ändras efter att sidan har publicerats publiceras inte igen när webbplatsen publiceras. NPR-23013: Programfix för CQ-4236566

#### Integrering med backend {#backend-integration-1}

* OOTB grundläggande autentisering för SOAP-tjänster fungerar inte för grundläggande autentisering i FDM-integrering. NPR-23238: Programfix för CQ-4241308

#### Korrespondenshantering {#correspondence-management}

* OTB XDP:er visar innehållet som överlappar sidfoten när de används inuti bokstaven och förhandsvisas. Programfix för CQ-4212414

#### Assembler Service {#assembler-service}

* Felaktighet mellan Acrobat DC och AEM rapporterar om PDF/A-1b-kompatibilitetskontrollfel. NPR-22051, NPR-22050: Programfix för CQ-4226128, CQ-4227671

### Forms JEE-installationsprogram {#forms-jee-installer-8}

#### Workbench {#workbench}

* Aktiverad certifikatautentisering för Workbench-användare. NPR-20644: Programfix för CQ-4214488
* Det går bara att hämta serverlogg med Workbench för en server medan det inte fungerar för den andra servern. NPR-21079: Programfix för CQ-4229842

#### Processhantering {#process-management-1}

* (HTML-arbetsyta) Skärmstorlek problem med rullningslister. NPR-23288
* (HTML-arbetsyta) Processstartpunkter sorteras inte i alfanumerisk ordning. Programfix NPR-22841 för CQ-4238944
* (HTML-arbetsyta) Förbered data aktiveras när formuläret stängs på arbetsytan. NPR-21127: Programfix för CQ-4224574
* (HTML-arbetsyta) När du anropar en process som kräver anteckningar med långa beskrivningar fungerar inte expanderingsknappen Anteckningar. Programfix för CQ-4241488

#### Core {#core-1}

* Ett fel uppstod vid start när schemaläggaren startades. NPR-22990
* Förhindra att webbläsare lagrar inloggningsuppgifter som anges i HTML-formulär. NPR-21762: Programfix för CQ-4206543
* De problem som rapporteras i den statiska kodanalysen av Core bör åtgärdas. Programfix för CQ-104446

#### PDFG-tjänst {#pdfg-service-3}

* PDF Generator kan inte skapa PDF-dokument med angivna bokmärkesnivåer. NPR-22921, NPR-22285: Programfix för CQ-4230562
* Stöd för att skapa PDF-filer som är PDF/A-2a- eller PDF/A-3a-kompatibla har lagts till. NPR-23021: Programfix för CQ-4214172

#### Forms Designer {#forms-designer-1}

* PDF/UA-identifierare saknas när den sparas som PDF från Designer. NPR-23137
* Banobjekt, till exempel: kantlinjer, understrykningar och hyperlänkar taggas inte när de sparas som PDF från Designer. NPR-23136
* Bildobjektet har ingen begränsningsram när det sparas som PDF från Designer. NPR-23134
* Textbundna hyperlänkar som definieras i Designer taggas inte och de har ingen alternativ text när de sparas som PDF från Designer. NPR-23133
* Om du öppnar XML-datapaketet med AEM 6.3 tar Forms Designer bort XHTML-formatering från XML-källan. NPR-21178: Programfix för LC-3917046

#### Installera LCM {#install-lcm}

* Uppdatera Jsafe Jars till Cryptoj 6.1.3.1 i installationsprogrammet och LCM. NPR-21370

#### Signaturtjänst {#signatures-service}

* Ett undantag uppstod vid försök att signera/certifiera ett PDF-dokument digitalt via HSM. NPR-21154: Programfix för CQ-4226978

### OSGI-paket och innehållspaket som ingår i 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}

Förteckning över OSGi-paket som ingår i AEM 6.3.2.1

[Hämta fil](assets/do-not-localize/bundle-list_002_.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.2.1

[Hämta fil](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 1 (6.3.1.0) i oktober 2017.

Viktiga faktorer i AEM Cumulative Fix Pack är:

* Ändrat användargränssnitt som stöder implementering av CUG-funktioner i AEM Assets.
* Åtgärdade gränssnittsproblem på licenskontrollsidan för bättre upplevelse.
* Aktiverat stöd för OSGi-arbetsflödesuppgifter i AEM Forms App.

### Resurser {#assets-10}

* Ändrat användargränssnitt som stöder implementering av CUG-funktioner i AEM Assets. NPR-19485
* Ett problem uppstår om du överför en resurs som en direkt underordnad nod till sig själv med Touch-gränssnittet. Resursen överförs som ett direkt underordnat objekt till den tidigare valda resursen. NPR-19736
* Datumintervallpredikat och intervallpredikat fungerar inte när en sparad sökning/smart samling läses in. NPR-19844: Programfix för CQ-4220808
* AEM blir trög när flera resurser (fler än 4) publiceras till Brand Portal. NPR-2009: Programfix för CQ-4213426
* Det går inte att hämta resurser med blanksteg från licenskontrollsidan. NPR-20067: Programfix för CQ-4216557
* Bearbeta problem vid överföring av PSB-filer med flera alfalager. NPR-20250: Programfix för CQ-4220869
* Användare som inte kan hämta resurser med långa filnamn och en ansvarsfriskrivning har definierats. NPR-20254
* ProductAssetsUploader lämnar de temporära filerna för JAVA-cachen i Java TEMP-mappen. NPR-20256: Programfix för CQ-4221801
* Ersätt versionsjämförelsekod med Adobe på grund av licensproblem. NPR-20272: Programfix för CQ-4223758
* Metadata för en strängegenskap, documentNumber, visas som ett datum medan det bör vara ett tal. NPR-20291: Programfix för CQ-4223991
* Textextraheringen fastnar för en skadad PDF. NPR-20416: Programfix för CTG-4150375
* Komprimerade filer som innehåller resurser med icke UTF-8-kompatibla namn hämtas inte korrekt. NPR-20420: Programfix för CQ-4219961
* För många tecken i OmniSearch gör att AEM kraschar. NPR-20434: Programfix för CQ-4223602
* API-metadatadefekten för DAM-resurser bryter API:erna för xmp -write-back. NPR-20607: Programfix för CQ-4220455
* Prestandaproblem när användare läggs till i samlingar. NPR-20699: Programfix för CQ-4225733
* Publicera till Brand Portal från AEM tillåts inte för Dynamic Media-uppsättningar. NPR-20320: Programfix för CQ-4221147
* Video med mellanslag och accent ger ingen video för återgivningssidan. NPR-19961: Programfix för CQ-4221014
* Löste flera problem med mapphantering med Assets API:er. NPR-20569
* AEM Dynamic Media Classic (tidigare Scene7) kan inte synkronisera resurser från AEM när målsökvägen i molntjänstkonfigurationen pekar på en undermapp i rotsökvägen. CQ-4228265
* E-postpaketet med cachekommon `{org.apache.commons/commons-email/1.5}` har lagts till och ersätter `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`.

### Webbplatser {#sites-10}

* Problem med administratörsbehörighet: Det går inte att ta bort medlemmar i en stängd användargrupp från sidegenskaperna. NPR-20631
* Det angivna arbetsflödets namn ska vara tillgängligt i rutan Meddelande när sidan publiceras via Hantera publikation. NPR-20046: Programfix för CQ-4221586
* Om du använder formaterad text på två rader i RTF-redigeraren och sedan sammanfogar dem i ett stycke tas de formaterade intervallen bort. NPR-2010: Programfix för CQ-4223051
* Ändringar som görs i fältegenskaper på flera flikar i dialogrutan Redigera egenskap sparas ibland inte. NPR-20286
* Oväntad tagg i slutet av det inklistrade innehållet i innehållsfragmentet. NPR-20413: Programfix för CQ-4224014
* Implementerade en mekanism i Adobe Campaign för att hämta principen för en innehållsresurs från en extern målinriktningsresurs. NPR-20667
* Ritext-plugin fungerar inte för både textbundna fält och helskärmsfält i multifield Touch-gränssnittet. NPR-20973

### Campaign {#campaign-1}

* Platshållare visas inte på en sida som innehåller flera parsyskomponenter. NPR-20436; Programfix för CQ-4215000

### Handel {#commerce-4}

* Upplevelsefragment visas inte korrekt i Internet Explorer 11. NPR-20161: Programfix för CQ-4223319
* I handelsflöden infogas en tom bild automatiskt när du skapar en variant som baseras på en primärprodukt med flera bilder. NPR-20068: Programfix för CQ-4222048
* Det går inte att filtrera efter taggar på samlingssidor i produktkonsolen. NPR-20292: Programfix för CQ-4224023

### Communities {#communities-8}

* Inkonsekventa sökresultat med sökresultatskomponenten. NPR-20070: Programfix för CQ-4220913
* E-postmeddelanden aktiveras inte för någon av de moderatorrelaterade aktiviteterna för publicerade komponenter. NPR-2012
* Tom sidnumrering utan resultat visas för anonyma communityanvändare. NPR-20136: Programfix för CQ-4220738
* Konfigurera varningsutlösare när en UGC identifieras som skräppost eller när en användare publicerar på en förmodererad plats. NPR-20274: Programfix för CQ-96850
* Löste flera problem på AEM Communities webbplatssidor, bland annat felaktiga omdirigeringar och problem med uppdatering av sidor. NPR-20344
* CommunityUserOperationExtension kör i ett klassbytesundantag. NPR-20532: Programfix för CQ-4224385
* När en webbgruppswebbplats har skapats kan användare inte öppna den från webbplatskartan eftersom kontextsökvägen inte läggs till i webbadressen. NPR-20730

### Integrering {#integration-6}

* Migrerar befintliga autentiseringsuppgifter för Analytics till WSSE Authentication. NPR-19962: Programfix för CQ-4218071
* Återaktivering av segmentet efter att en ändring har misslyckats och ett fel uppstår. NPR-20054: Programfix för CQ-4218401
* Konfigurationen av molntjänsten ignorerar formulärhämtningsmetoden, vilket gör den oanvändbar på författarinstansen. NPR-20447: Programfix för CQ-4206076
* Tvetydig filterdefinition i innehållspaket gör att sökvägar skrivs över när Search &amp; Promote installeras. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* Metadataegenskaper för resurser av typen TXT som visas i olika metadataredigerare varje gång deras egenskaper visas. NPR-20239

### Plattform {#platform-3}

* Ett undantagsfel för resurslösare som inte stängts har åtgärdats. NPR-19749: Programfix för Granite - 19143
* Begäran om att anpassade kort ska visas tillsammans med standardhälsokontroller på kontrollpanelen för åtgärder. NPR-20145
* Anteckningslagret i sidredigeraren fungerar inte korrekt i Internet Explorer 11. NPR-2022: Programfix för CQ-422818
* Sessionsläckor när användaragenten ställs in som administratör i replikeringsagenten. NPR-20578
* requestAttributes har inte tagits bort för de andra programsatserna för datasynlig resurs. NPR-20639: Programfix för 4226206
* Korrigerade problem med url Head-begäranden för OOTB-resurser i AEM. NPR-20781: Programfix för CQ-4221520

### Projekt {#projects-1}

* Det tar längre tid att läsa in åtkomst till olika projekt från projektkonsolen. NPR-20314
* Om du installerar AEM 6.3.0.1 tas nyckelbehållaren för dam-update-service bort. NPR-2018
* I vissa anpassade distributioner tar det längre tid för användare som försöker välja tilldelad i modulen addTask att fylla i listan i användarväljaren. NPR-20283: Programfix för CQ-4224193

### Användargränssnitt {#user-interface-3}

* Färgfältet är inställt på&quot;alltid obligatoriskt&quot; trots attribut i dialogrutan. NPR-19702
* Rullningslisten visas inte för flerfältskomponenter i helskärmsläge i Internet Explorer 11. NPR-20261: Programfix för CQ-4219782
* Tidigare frågor avbryts inte om efterföljande frågor utlöses, vilket leder till felaktiga resultat. NPR-20398: Programfix för GRANITE-19306

### Arbetsflöde {#workflow-1}

* Användarna meddelas inte om de arbetsflödesuppgifter de får i sin inkorg. NPR-20213: Programfix för CQ-4221639
* OTB-beviljande användarväljare läser inte in några användare när de klickas på listrutan i dialogdeltagarsteget i arbetsflödesmodellen. NPR-20236

## Forms {#forms-10}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-10}

#### Adaptiv Forms {#adaptive-forms-3}

* Stöd för aggregeringsuttryck för upprepade paneler saknas. NPR-20861
* I listrutan visas det senast lagrade värdet även om den associerade datamodelltjänsten inte returnerar något värde. NPR-20710
* Det går inte att redigera befintliga regler med booleska begränsningar i regelredigeraren. NPR-21128

#### Formulärportal {#form-portal}

* HTML-profilen visas för ett adaptivt formulär även när dess resurstyp inte är XDP. NPR-20079

#### Integrering med backend {#backend-integration-2}

* Det går inte att ange ett värde för växlingskomponenten mellan sant/falskt. NPR-21111

#### OSGI-arbetsflöde {#osgi-workflow}

* Hantera arbetsflödets inlämningslistor innehåller endast tio program. CQ-4230193

#### HTML5 Forms {#html-forms-3}

* Namnet på ett XDP-formulärobjekt som delformulär visas som verktygstips när det inte är definierat i tillgänglighetskonfigurationerna. NPR-20523

### Forms JEE-installationsprogram {#forms-jee-installer-9}

#### Processhantering {#process-management-2}

* Startpunkten för FormSetPrefillApp förifyller inte formuläruppsättningsfält i AEM Forms-appen. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Installera det senaste CTJPEG2K-biblioteket för att få en allvarlig säkerhetsrisk. Detta påverkar modulerna XMLFM (AEM och IfBA), RM och PDFG. NPR-20625: NPR-21337.

### Funktionspaket ingår {#feature-packs-included}

#### AEM Forms App {#aem-forms-app}

* Aktiverat stöd för OSGi-arbetsflödesuppgifter i AEM Forms App. CQ-422638

### OSGI-paket och innehållspaket som ingår i 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

Förteckning över OSGi-paket som ingår i AEM 6.3.1.2

[Hämta fil](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Förteckning över innehållspaket som ingår i AEM 6.3.1.2

[Get ](assets/do-not-localize/6_3_1_2-content-package-list.txt)
FileAEM Cumulative Fix Pack 6.3.1.1 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 Service Pack 1 (6.3.1.0) i oktober 2017.

Viktiga faktorer i AEM Cumulative Fix Pack är:

* Aktiverad publicering till Brand Portal-åtgärd för standardmetadatamatchformulär.
* Beteendeändring i visning av titlar på bildkort för Image having DC: title-egenskapen är inställd på String [] (multifield).
* Ersatte tidsåtergivning på serversidan med komponenten Foundation-time.
* Aktiverade publiceringstaggar från AEM till Brand Portal från tagadmin/tagging-konsolen.
* Publicerat JSON API för att förbruka innehållsfragment.
* Den inbyggda databasen (Apache Jackrabbit Oak) uppdateras till version 1.6.5.

### Resurser {#assets-11}

* Om två fält mappas med samma egenskap med olika typer av egenskapsfält genereras ett internt fel. NPR-19462: HF för CQ-4216828
* dc: title and dc: description does not change to a multi-field value in crx /de. NPR-19570: HF för CQ-4209086
* Dynamic Viewer läser in videoåtergivning med låg kvalitet för att testa videouppspelning i redigeringsläge. NPR-19004
* Dynamisk återgivning kan inte hämtas för resurser som innehåller blanksteg i sina namn. NPR-19433: Programfix för CQ-4211738
* Det går inte att läsa in en fullständig lista med sidor/resurser i kolumnvyn med Chrome. NPR-19566: Programfix för CQ-4214248
* Alternativet Publicera till Brand Portal är inte tillgängligt när du väljer ett schema, en sökaspekt eller en förinställning. NPR-19550
* När du markerar en resurs i kolumnvyn och klickar på Redigera returneras ett fel. NPR-20301: Programfix för CQ-4224052
* Visa förfallodatum för tillgångar är inaktiverat när positiv och negativ tidszon korsas. NPR-20329: Programfix för CQ-4219333

### Campaign {#campaign-2}

* Komponenter för kampanjreglage visas inte när standardupplevelsen väljs för en kampanj. NPR-19213

### Integrering {#integration-7}

* Anpassad at at.js-fil publiceras inte när den används av den anonyma användaren. NPR-19542: Programfix för CQ-4219592
* Fältet Målmotor i konfigurationsguiden är inställt på ContextHub (AEM) i stället för Adobe Target. NPR-19320: HF för CQ-4218465
* Målgruppsavsnittet skadas när upplevelsen skapas. NPR-19110
* Måldialogrutan visas inte i målinriktningsläge när en målmodul redigeras och du sparar mer än en gång. NPR-19144: Programfix för CQ-4216708
* Åtkomstegenskaper för artiklar som inte har angetts korrekt i Adobe Digital Publishing Solution för Classic UI. NPR-19367
* Felaktigt beteende för automatisk vikning vid personalisering av erbjudanden via Campaign om användarna har tillgång till flera områden. NPR-19290: Programfix för CQ-4218029

### Webbplatser {#sites-11}

* Listrutevärden för flersammansatta fält fylls inte i på nytt på grund av att koden i Sidespark.js har ändrats efter att instansen uppgraderats till AEM 6.1SP2-CFP3. NPR-19450: HF för CQ-4194771
* WCMMode.EDIT fungerar inte för målkomponenter i redigeringsläge. NPR-19387
* Publicerat JSON API för att förbruka innehållsfragment. NPR-19500
* Funktionen fet, kursiv och understrykning fungerar inte för textredigeringsfält i författardialogrutan. NPR-19670: NPR-19718: Programfix för CQ-4219088

### Mobile On-Demand {#mobile-on-demand-1}

* Renderingsproblem med AEM artikelkonsol som användning av bilder i full storlek gör det trögt. NPR-19088

### Översättning {#translation-5}

* Det går inte att generera förhandsgranskning för översättningsprojekt. NPR-19289

### Dokumentskydd {#security}

* SSL-anslutningsfel. Det går inte att skapa en säker anslutning till servern. NPR-19628

### Communities {#communities-9}

* E-post aktiveras vid publicering av innehåll med förmodererade webbplatser. NPR-2008
* E-postmeddelanden fungerar inte för någon av de moderatorrelaterade aktiviteterna för publicerade komponenter. NPR-19767: HF för CQ-4218060

### Plattform {#platform-4}

* Stabilitetsproblem AEM driftsättningen av produktionsservrar. NPR-19707
* Anpassad tagg som refererar till taggar som implementerats som skript hittas inte efter uppgradering till AEM 6.3. NPR-19087
* HTML-felkorrigeringar för AEM 6.3.1. NPR-19161
* RTF-fältet kan inte redigeras i flerfältskomponenter. NPR-19604: Programfix för Granite-16755
* Tjänsten Adobe Email Template lägger till taggar i anpassade användarmallar. NPR-19190
* Programfix för Oak 1.6.5. NPR-19148

### Handel {#commerce-5}

* Knappen Starta arbetsflöde när du har valt en XF-variantredigerare har ingen effekt. NPR-19642: Programfix för CQ-4207796

### Projekt {#projects-2}

* Projektredigerare kan inte kopiera/klistra in resurser i projektresursmappen. NPR-19619: Programfix för CQ-4215321

### Web Content Management {#web-content-management}

* På skärmen Rollout kan kryssrutor som motsvarar livecopy-sidor inte markeras eller avmarkeras. NPR-19518
* Massredigering av sidegenskaper kan inte användas korrekt eftersom alla flikar och fält är tillgängliga för massutgåva. NPR-19451
* OTB-egenskaper och bildjusteringsegenskaper visas inte när du redigerar en bild i ett klassiskt användargränssnitt. NPR-19488: HF för CQ-4217914

### Användargränssnitt {#user-interface-4}

* När du använder webbläsaren Google Chrome kan användarna inte läsa in den fullständiga listan med sidor/resurser med kolumnvyn i TouchUI. NPR-19566: Programfix för CQ-4214248

### Brand Portal {#brand-portal-1}

* Det går inte att publicera resurser från AEM med kommentarer och anteckningar. NPR-19590: Programfix för CQ-4218386
* Aktivera publiceringstaggar från AEM till Brand Portal från tagadmin/tagging-konsolen. NPR-20271: Programfix för CQ-4223948
* Korrigera fältet&quot;aktiverat&quot; i användargränssnittet för Brand Portal molntjänst. Programfix för CQ-4211101
* Replikering av sökformulär misslyckades. Programfix för CQ-4220080

## Forms {#forms-11}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-11}

#### Anpassningsbara formulär {#adaptive-forms-4}

* Skicka till JEE-arbetsflödet returnerar inte utdataparametern från JEE-sidan till AEM och returnerar felet&quot;Ignorerar eftersom värdet inte är primitivt&quot;. NPR-20265
* Adaptiv Forms tillåter inte PDF som bilaga i Safari. NPR-19625
* RestoreGuideState skriver över anpassad kontextegenskapskarta. CQ-422877
* När du konfigurerar Google reCaptcha med Cloud Service, i miljöer som kräver konfiguration av org.apache.http.proxyconfigurator för externa anslutningar, verkar det som att POSTER inte går igenom PROXY. NPR-20454
* Adaptiv Forms baserad på XSD-scheman skickar felaktiga XML-värden för numeriska fält i installationer med andra språkversioner än &quot;.&quot; vilket resulterar i fel. NPR-20444
* Proxyinställningarna som angetts för Proxykonfigurationen för Apache HTTP Components respekteras inte när HTTP-begäran görs till tredjepartsserver. Timeoutproblem vid anslutning med HTTP-GET eller POST-anrop. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Forms dataintegrering {#forms-data-integration}

* UTF-8-tecken som utdata från SOAP-tjänsten kopieras inte korrekt till adaptiva Forms-fält för icke-engelska språk. NPR-20238: NPR-20103

#### Korrespondenshantering {#correspondence-management-1}

* Om du kopierar Klistra in innehåll från ordfilen förlorar du innehållsfärgen och teckensnittet i textredigeraren. NPR-19521

#### Assembler Services {#assembler-services}

* Skillnaden mellan resultat från Acrobat och AEM vid kompatibilitetsverifiering av ett dokument till PDFA-1b-format. NPR-19280

#### Arbetsflöde {#workflow-2}

* Signeringssteg för arbetsflöde som tillåter att http-anrop ansluter via proxyn. NPR-20529

#### HTML5 Forms {#html-forms-4}

* Stöd för preSubmit-händelse har lagts till. NPR-20604

### Forms JEE-installationsprogram {#forms-jee-installer-10}

#### Processhantering {#process-management-3}

* Bifogade arbetsflöden, anteckningar och informationsflikar fungerar inte på arbetsytan när formuläret maximeras/minimeras och sparas som ett utkast eller vidarebefordras. NPR-20243
* Flerradigt textfält (TextArea) behåller inte nya radtecken eller radbrytningar i text när data har skickats till HTML-arbetsytan. NPR-20085

#### Processrapportering {#process-reporting}

* Processrapporteringen hämtar inte data korrekt på grund av ett nollpekarundantag. NPR-19759

>[!NOTE]
>
>Installera LiveCycle embed-paketet som listas i [AEM Forms Releases](aem-forms-releases.md)-artikeln för att åtgärda problemet.

#### Standardtjänster {#standard-services}

* docConvertor stöder inte förenkling av genomskinlighet i PDF och kan inte skapa en PDF/A. NPR-16228: Programfix för CQ-4214488

#### Core {#core-2}

* När AEM Forms-servern som körs i en klusterkonfiguration i JBoss-programmet stoppas kopplas programservern från databasen. Det kan leda till problem med skadade data. NPR-19724

### Funktionspaket ingår {#feature-packs-included-1}

* Det går inte att göra ett nedrullningsbart metadatafält obligatoriskt eftersom obligatorisk fältvalidering saknas för resurser. NPR-17882: FP för CQ-4208373

### OSGI-paket och innehållspaket som ingår i 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}

Förteckning över OSGi-paket som ingår i AEM CFP 6.3.1.1

[Hämta fil](assets/do-not-localize/bundle-list.txt)

Förteckning över innehållspaket som ingår i AEM CFP 6.3.1.1

[Hämta fil](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 i april 2017.

Viktiga faktorer i AEM Cumulative Fix Pack är:

* Granskning av åtkomstkontroll
* Inkluderar version 1.6.2 av den inbyggda databasen (Apache Jackrabbit Oak)
* Löste problem med icke stängd resurslösare
* Förenklad konfiguration för smarta innehållstjänster
* Lösta problem med validering av innehållsfragment
* Förbättrad redigering av metadatamappningar på hybridenheter
* Löste problem med synkronisering på komponentnivå i live-kopior
* Förbättrad användbarhet för innehållsrika sidor i kolumnvyn
* Förbättrad överensstämmelse med sidnamnskonvention för sidor med långa titlar
* Förbättrad upplevelse av personalisering av kampanjer i Touch-gränssnittet
* Korrigeringar för olika problem med projektövertäckning

### Plattform {#platform-5}

* Programfix för Oak 1.6.2. NPR-16993
* Sökvägen anges inte längre när du öppnar en sökning med ett filter. NPR-17398: Programfix för CQ-4204870
* Krav på att användarbehörigheterna ska kunna läsas av AEM. NPR-17061
* Lingering av anslutningar till DM-Cloud Services orsakar &quot;för många öppna filer&quot;-undantag. CQ-4211407

### Resurser {#assets-12}

* Användbarhetsproblem vid konfiguration av smarta innehållstjänster med olika alternativ. NPR-18200: Programfix för CQ-4201557
* Resursläckage i binära strömmar till S3-datalager. NPR-18041: Programfix för CQ-4209506
* Ett fel inträffar när en ASCII/UTF-8-kodad textfil överförs till AEM Assets och genereringen av miniatyrbilder misslyckas. NPR-18006: CFP för CQ-4209345
* Standardmetadataschemat orsakar fel vid validering av innehållsfragment. NPR-17769: Programfix för CQ-4211111
* Ostängd resurslösare i com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP för CQ-4209018
* Begäran om att skapa flera replikeringsagenter för publicering av resurser på Brand Portal. NPR-17189
* Granskningsaktiviteten för resurser under den japanska språkmappen fungerar inte. CQ-4204782
* Null-pekarundantag inträffar när en resurs flyttas från sin egenskapssida. CQ-4204251
* AEM kan inte spåra efterföljande referenser till en resurs på egenskapssidan om den är länkad till ett InDesign-dokument flera gånger. CQ-4204186
* Problem med att lägga till nya flikar i schemaformuläret för metadata när det redigeras i Chrome på hybridenheter. CQ-4201810
* När duplicerade resurser överförs används alternativet (ta bort/behåll) för alla resurser även när det inte är markerat i en dialogruta som upptäcks. CQ-4201673
* Ett null-pekarundantag genereras när en resursmapp med fler än 150 inkommande referenser flyttas. CQ-4200981
* Om det uppstår en konflikt när innehållet i ZIP-filen extraheras i en resursmapp visas standardalternativet som Skapa version i stället för Behåll båda. CQ-97800
* Användare med skrivskyddad behörighet till programmet kan inte förhandsgranska innehåll från AEM Mobile innehållshantering. NPR-17486: CFP för CQ-4209690
* Knappen Skapa katalog fungerar inte i kolumnvyn i katalogkonsolen. CQ-4209952

### Webbplatser {#sites-12}

* Problem med inbäddning av bild-/videokomponenter via attribut för dataströmsresurs. NPR-18182: CFP for CQ-4212100
* Ändrade lokaliserade komponenter återställs inte till det ursprungliga formuläret när arv tillämpas på nytt i en LiveCopy. NPR-18172: Programfix för CQ-4211379
* Problem med att navigera på en innehållsrik sida i kolumnvyn i Touch-gränssnittet. NPR-17799: Programfix för CQ-4199611
* Resurslösaren som inte stängts i `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP för CQ-4211152
* Sidnamnet genereras inte som per konvention för långa sidrubriker. NPR-17633: Programfix för CQ-4209056
* Problem med att skapa sidor i Touch-gränssnittet i AEM 6.3 som körs i Jboss EAP 6.4. NPR-17589: Programfix från CQ-4210137
* Arbetsflödets statusprovider gör att instansen låses när det finns kapslade grupper. NPR-17556: Begäran om bestruket finpapper för CQ-4202056
* Resurslösare som inte stängts i följande objekt:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP för CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP för CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP för CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP for GRANITE-17404

### Integreringar {#integrations-1}

* Löste AEM sökkomponentfel som kan inträffa när AEM Day HTTP Client 3.1 OSGI har konfigurerats med en proxy som kräver sammanfattningsautentisering. NPR 18128: Programfix för NPR-18029
* Problem med personaliserade kampanjer och associerade upplevelser via det klassiska användargränssnittet. NPR-18127: Programfix för CQ-4211559
* När du anger ett varumärke/en zon på en rotsida på en webbplats kan arv som har avbrutits inte återställas för områden på undersidor. NPR-17753: Programfix för CQ-4210139

### Arbetsflöde {#workflow-3}

* I ett icke-tillfälligt arbetsflöde bevaras inte processhistoriken och metadataändringar som gjorts innan ett externt processsteg. NPR-17848: Programfix för GRANITE-17757
* Värden från arbetsflödesdialogrutefält sparas inte i arbetsobjektsnoden. NPR-17734: Programfix för CQ-4210369
* Ett otolkbart datumfel inträffar när en åtgärd redigeras från inkorgen. CQ-4208749

### Projekt {#projects-3}

* Korrigeringar för olika problem med projektövertäckning. NPR-17733
* Omstruktureringen av punkterna i projektmodulen gör den mindre konfigurerbar. CQ-4209859
* Sökvägen till resursens sökväg ändras till respektive lokaliserade platser när sidor läggs till i översättningsjobbet. CQ-4206007

### Dokumentskydd {#security-1}

* Problem med att överföra avatarbilder för LDAP-användare. NPR-16561
* Begär att en uppgraderad version av org.apache.sling.servlets.post servlet (2.3.22) i API:t för Apache Sling ska användas för att förhindra en XSS-säkerhetslucka. NPR-18963

## Forms {#forms-12}

AEM Forms-korrigeringar levereras via Forms tilläggspaket och andra patch-installationsprogram som ingår i releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

AEM Forms i korthet:

* Korrigeringar i textmoduler för korrespondenshantering, förhandsgranskning av brev och programstart skapar gränssnitt för korrespondenshantering.
* Korrigeringar för PDF/A-1b-validering, konvertering av stora bildfiler till PDF och japanska PDF-dokument i PDF Generator.
* Korrigeringar för korrespondenshantering, dokumentsäkerhet och arbetsflöde för formulär.
* Stöd har lagts till för att samla in granskningshändelser för signaturfältet i klotter.

### Forms tilläggspaket {#forms-add-on-package-12}

**Korrespondenshantering**

* När du redigerar ett korrespondenshanteringsfragment visas textredigeraren textbundna villkor tillsammans med den bearbetade texten. CQ-4211930
* Beskrivningen av brevet sparas inte när ett brev skapas. NPR-18089
* Ytterligare marginal ovanför och under en punktlista visas i textredigeraren men inte i HTML- och PDF-återgivning. NPR-18126
* När HTML-sändning använder metoden POST går det inte att starta gränssnittet för att skapa korrespondens. NPR-18202
* När en textmodul sparas och ett uttryck i textmodulen inte innehåller inledande eller avslutande uttryckstaggar, visas inget felmeddelande. Textmodulen visar ett felmeddelande och kan inte återges i brevet. NPR-18535
* När nytt innehåll läggs till eller Retur-tangenten trycks ned läggs en div-tagg till i textmodulen. NPR-18240

**Assembler**

* Vid validering av ett PDF-dokument för PDF/A-1b-kompatibilitet returnerar AEM Forms ett valideringsfel: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. PDF-dokumentet returnerar inte felet när det valideras med Adobe Preflight och program från tredje part. NPR-18011
* Vid validering av PDF-dokument för PDF/A-1b-kompatibilitet returnerar AEM Forms ett valideringsfel: Formulärfältet har flera utseenden. PDF-dokumenten är PDF/A-1b-kompatibla. NPR-18013

**Bevakad mapp**

* När du väljer att bearbeta filer med ett arbetsflöde och skapar en bevakad mapp, visas listrutan för arbetsflödesmodellval trunkerad. NPR-17566

**HTML5 Forms**

* AEM Forms samlar inte in granskningshändelser för signaturfältet. NPR-15286

**Forms Manger**

* I AEM Forms-gränssnittet visas alla resurser i den äldsta första ordningen. Användarna kan inte ändra ordning på resurserna i den senaste första ordningen. NPR-18450

**Java API-referens**

JavaDocs har lagts till för klassen com.adobe.livecycle.content. NPR-18468

### Forms JEE-installationsprogram {#forms-jee-installer-11}

**PDF Generator**

* Tjänsten PDF Generator kan inte konvertera bilder som är större än 100 MB till PDF-dokument. Ref# CQ-4208628
* När du använder PDF Generator-tjänsten med en japansk OCR-läsare genereras en inverterad PDF. NPR-17602

**Processhantering**

* Variabeln TaskContext är inte ifylld för AEM Forms-processer. NPR-18199

**Dokumentsäkerhet**

* Microsoft Excel och Microsoft PowerPoint tar mycket längre tid att öppna dokument som skyddas med AEM Document Security Extension för Microsoft Office. CQ-4212358
* När en ny princip skapas och en princip med samma namn som finns, inträffar ett internt serverfel. NPR-18247

## Inkluderade funktionspaket {#feature-packs-included-2}

* Krav på att användarbehörigheterna ska kunna läsas av AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 är en viktig uppdatering som innehåller flera interna korrigeringar och kundkorrigeringar sedan den allmänna tillgängligheten av AEM 6.3 i april 2017. De viktigaste nyheterna i AEM Cumulative Fix Pack är:

* Förbättringar inom följande område:

   * Komponenter för innehållsfragment, webbplatser och RTF-redigerare, regelredigerare och mallredigerare
   * Social Review och Facebook Social-inloggning
   * Konfigurera och starta översättningsjobb
   * Svarstid för åtkomst av meddelanden i sociala communities
   * Visa granskningsåtgärder i DAM-databasen

* Tillhandahåller valideringsalternativ i Package Manager för att identifiera konflikter mellan övertäckning och CFP

## Ladda ned instruktioner för CFP via Software Distribution {#download-instructions-for-cfp-via-package-share}

Du kan hämta CFP-paketet direkt från [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8) eller utföra följande steg:

1. Öppna [Programvarudistribution](https://experience.adobe.com/downloads). Du behöver en Adobe ID för att logga in på Software Distribution.
1. Tryck på **[!UICONTROL Adobe Experience Manager]** som finns i rubrikmenyn.
1. Tryck på paketnamnet, välj **[!UICONTROL Accept EULA Terms]** och tryck på **[!UICONTROL Download]**.

## Installationsanvisningar {#installation-instructions}

I det här avsnittet går du igenom kraven och stegen för att installera bestruket finpapper.

### Innan du installerar {#before-you-install}

>[!NOTE]
>
>De valfria funktionspaket som tillhandahålls av Adobe är beroende av releaseversionen och Cumulative Fix Pack. Om du har något funktionspaket installerat kontaktar du [AEM kundtjänstteam](https://helpx.adobe.com/marketing-cloud/contact-support.html) för att validera kompatibiliteten med detta Cumulative Fix Pack för AEM 6.3.

>[!NOTE]
>
>Vi rekommenderar att du kör valideringen på alla nya installationspaket innan du försöker installera paketet. Vid förvalideringen analyseras och alla fel som påträffats före installationen rapporteras. Användarna varnas aktivt för sådana fel.
>
>Dokumentation om valideringsalternativ finns på [https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 är en förutsättning för den gemensamma fiskeripolitiken. Mer information om hur du uppgraderar en AEM till AEM 6.3 finns i [Uppgraderingsdokumentation](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html).
* För en klusterdistribution med RDBMK eller MongoDB kan CFP-paketet installeras på alla Author-instanser som använder Package Manager.
* Innan du installerar det kumulativa korrigeringspaketet bör du ta en ögonblicksbild eller skapa en säkerhetskopia av AEM.
* Avinstallation av CFP stöds inte.

### Lägga till nya loggare {#adding-new-loggers}

Om du vill konfigurera loggning på felsökningsnivå och hämta en aktivitetslogg under installation av SP/CFP:er, kan du följa stegen nedan:

* Du kan lägga till en ny loggare på standardplatsen [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) med följande egenskaper:

   * Loggnivå: Felsök
   * Adderande: false
   * Loggfil: logs/activity.log
   * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

activity.log skapas i   crx -quickstart /logs mapp.

### Installera det ackumulerade korrigeringspaketet via programvarudistribution {#install-the-cumulative-fix-pack-via-package-share}

Så här installerar du Cumulative Fix Pack på en befintlig AEM 6.3-instans:

1. Klicka på länken [Programdistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) för att hämta paketet.

1. Öppna [Pakethanteraren](http://localhost:4502/crx/packmgr/index.jsp) och klicka på **[!UICONTROL Upload Package]** för att överföra paketet.

1. Markera paketnamnet och klicka på **[!UICONTROL Install]**.

### Automatisk installation {#automatic-installation}

Den gemensamma fiskeripolitiken kan installeras automatiskt i en instans som körs på följande sätt:

* Placera paketet i `../crx-quickstart/install` när servern körs. Paketet installeras automatiskt.
* Använd [HTTP-API:t från Package Manager](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/package-manager.html) - kontrollera att du använder `cmd=install&recursive=true` - så att det kapslade paketet installeras.

### Validera installation {#validate-installation}

1. Produktinformationssidan ( `/system/console/  productinfo`) ska nu visa den uppdaterade versionssträngen &quot;Adobe Experience Manager, version 6.3.3.8&quot; under Installerade produkter.
1. Alla OSGI-paket är antingen AKTIVA eller FRAGMENT i OSGI-konsolen (Använd webbkonsolen: `/system/console/bundles`).

>[!NOTE]
>
>När paketet har installerats visas ett informationsmeddelande i felloggarna som anger att innehållspaketet har installerats, t.ex.&quot;Innehållspaket **AEM-6.3.3-Cumulative-Fix-Pack-7** har installerats.&quot;

>[!NOTE]
>
>Sedan AEM 6.3.3.1 har loggnivån i Jackrabbit FileVault ändrats från INFO till DEBUG för de flesta meddelanden. Om du vill få installationsloggar för ett innehållspaket som är installerat på AEM 6.3.3.1 eller senare aktiverar du DEBUG-loggnivån för org.apache.jackrabbit.vault.packaging.impl.

### Installera AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Hoppa över det här avsnittet om du inte använder AEM Forms.

#### Installera AEM Forms-tillägg {#install-forms}

1. Kontrollera att du har installerat AEM 6.3.3.x CFP-paketet.
1. Ladda ned motsvarande tilläggspaket från Forms som finns på [AEM Forms releases](aem-forms-releases.md) för ditt operativsystem.
1. Installera Forms-tilläggspaketet enligt beskrivningen i [Installera AEM formulär-tilläggspaket](https://helpx.adobe.com/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### Installera AEM Forms JEE-paketpaket {#install-aem-forms-jee-bundles-package}

Korrigeringar i AEM Forms JEE levereras via ett separat installationsprogram. Information om hur du installerar en CFP på AEM Forms på JEE finns i [Installera CFP på AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Installationsprogram för Forms Designer {#designer-installer}

1. Kör filen Designer 6.2.0_&lt;Language>_Cumulative_QF.msp för att installera uppdateringen.
1. Klicka på **uppdatera** på välkomstskärmen. Installationen startar.
1. När installationen är klar klickar du på **slut**.

## Konfigurationsinställningar för AEM Forms JEE (JBoss EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Om du installerar version 6.3.3.0 eller senare utför du nedanstående procedur för att konfigurera inställningar för JBoss-programservern. Om du installerar 6.3.3.0 på en AEM Forms-server som körs på Oracle WebLogic- eller IBM WebSpehere-programservrar krävs ingen ytterligare konfiguration. Mer information finns i [AEM 6.3.3.0 Versionsinformation](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

## Konfigurationsuppdateringar för integrering av Search &amp; Promote {#configuration-updates-for-search-promote-integration}

Med AEM Cumulative Fix Pack 6.3.0.2 och senare versioner är den OSGi-konfiguration som används för Search &amp; Promote-integrering **Proxykonfiguration för Apache HTTP Components**. Proxykonfigurationen från Day Commons HTTP Client 3.1 används inte längre.

## Kända fel {#known-issues}

* Följande fel och varningar kan förekomma under installation av AEM CFP 6.3.3.x och kan ignoreras utan problem:

   * *WARN* [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallkrok-0.0.2-jar-with-berodencies.jar utlöste runtime-undantag.
   * *FEL* [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Timeout i väntan på att reg.ändringen ska slutföras. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServerResolver-tjänsten saknas, kan inte hantera begäranden, skickar status 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: det går inte att kontrollera resursen [/bin/receive], sidhanteraren är inte tillgänglig
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Anrop till felhanteraren resulterade i ett fel
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Originalfel null
   * org.apache.sling.engine.impl.DefaultErrorHandler Error handler failed:java.io.IOException
   * *FEL* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: Servicefabriken returnerade null. (Komponent: com.day.cq.dam.handler.standard.ps.PostScriptHandler)

**Brand Portal**

* Från och med 6.3.1.2 har knappen Publicera till Brand Portal för smarta samlingar tagits bort.

**Användargränssnitt**

>[!NOTE]
>
>Kontakta [AEM kundtjänst](https://helpx.adobe.com/marketing-cloud/contact-support.html) om du skulle påverkas av något av dessa två problem.

* Hög processoranvändning observeras på grund av många förfrågningar i administratörssökningsfunktionen. NPR-24229
* PathField markeras inte i pathBrowser när komponenten öppnas igen. NPR-24177

## Konfigurationsinställningar som krävs för NPR-27692 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Den här konfigurationsinställningen gäller för CFP 6.3.3.2 och senare. Du uppmanas att uppdatera egenskaperna för startdelegering i `sling` .properties-filen.

Följ stegen nedan för att uppdatera ändringar i adobe- livecycle - cq -author.ear/ cq.war manuellt:

* Stoppa AEM.
* Gå till adobe-livecycle-cq-author.ear/cq.war
* Öppna adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml för redigering:

   * uppdatera **sling.bootDelegera.ibm** param-name-värdet med:

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * Efter ovanstående ändring bör init-param se ut så här:

      * &lt;init-param>\
         &lt;param-name>sling.bootDelegera.&lt;/param-name> &lt;param-value>ibmcom.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* Avinstallera den tidigare EAR-filen (enterprise archive) från webbsfär-programservern och installera den uppdaterade EAR-filen enligt stegen i Avsnitt 10.2 i [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Spara filen och starta om servern. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Konfigurationsinställningar som krävs för NPR-23208 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Den här konfigurationsinställningen gäller för 6.3.2.2 och senare. Den instruerar dig att uppdatera ACL-principer (Access Control Lists) manuellt via CRX-DE eftersom ACL-listor inte uppdateras via den bestrukna installationen på grund av &quot;merge_preserve&quot; acHandling.

**Dokumentation för att lägga till åtkomstkontrollistor manuellt**

Om du vill uppdatera åtkomstkontrollistor lägger du till nedanstående åtkomstkontroller via CRX-DE:

`1)` Vid sökvägen &quot;/content&quot;\
`a)` Principal: referensjusteringstjänst\
Typ: Tillåt\
Behörigheter: jcr:read, jcr:modifyProperties\
Begränsningar: rep:glob=&quot;/*/jcr:content&quot;\
`b)` Principal: referensjusteringstjänst\
Typ: Tillåt\
Behörigheter: jcr:read, jcr:modifyProperties\
Begränsningar: rep:glob=&quot;/*/jcr:content/*&quot;

`2)` Vid sökvägen &quot;/content/usergenerated&quot;\
`a)` Principal: referensjusteringstjänst\
Typ: Tillåt\
Behörigheter: jcr:write

`3)` Vid sökvägen &quot;/etc&quot;\
`a)` Principal: referensjusteringstjänst\
Typ: Tillåt\
Behörigheter: jcr:read, jcr:modifyProperties\
Begränsningar: rep:glob=&quot;/*/jcr:content&quot;\
`b)` Principal: referensjusteringstjänst\
Typ: Tillåt\
Behörigheter: jcr:read, jcr:modifyProperties\
Begränsningar: rep:glob=&quot;/*/jcr:content/*&quot;

## Konfigurationsinställningar som krävs för NPR-19450 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Den här konfigurationsinställningen gäller för CFP 6.3.1.1 och senare.

**Konfigurera egenskapen CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

Egenskapen styr det maximala djupet för nodunderträdet under noden ` /  jcr   :content`, till vilket noderna som finns i databasen ska användas för att hämta sidegenskaperna. Alla noder som finns under det angivna djupet i den här egenskapen ignoreras.

Standardvärdet är 1. Värdet kan åsidosättas genom att filen constants.js (`/libs/cq/ui/widgets/source/constants.js`) tas bort från kommenteringen av egenskapen CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL och tilldelas det värde som krävs (maximalt djup under sidans / jcr :content till vilket sidegenskapens data lagras).

**Om användaren behöver skapa flera sidvarianter så att antalet noder under sidans/jcr :content-nod blir större än 1 000, gör du så här för att göra konfigurationsändringar:**

* Konfigurera egenskapen JSON Max-resultat för Apache Sling
* Hämta Servlet med `/system/console/  configMgr`
* Ange ett värde >1000 (som är det aktuella standardvärdet) så att det här värdet är större än det totala antalet noder i underträdet / jcr :content tills det konfigurerade djupet ovan.

På så sätt kan den GET-server som har Sets returnera alla noder som krävs.

## Uber Jar {#uber-jar}

Uber Jar för 6.3.3.8 finns på [Adobe Public Maven-databas](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

Om du vill använda Uber Jar i ett Maven-projekt kan du läsa artikeln [Använda Uber jar](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) och inkludera följande beroende i projektstrukturen:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Borttagna/inaktuella funktioner {#deprecated}

I det här avsnittet listas funktioner som har tagits bort eller tagits bort från AEM 6.3.

| Yta | Funktion | Ersättning | Version |
|----|-----|-----|-----|
| Resurser och integrering med Adobe Creative Cloud | [AEM till ](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/creative-cloud.html) mappdelning mellan Creative Cloud introducerades i AEM 6.2 som ett sätt att ge kreativa användare tillgång till resurser från AEM. En ny funktion i Creative Cloud, Adobe Asset Link, ger en mycket bättre användarupplevelse och kraftfullare åtkomst till AEM direkt inifrån Photoshop, InDesign och Illustrator.<br /> Adobe kommer inte att förbättra mappdelningsfunktionen ytterligare. Funktionen ingår i AEM, men kunderna rekommenderas att använda den. | Adobe Asset Link eller Desktop App. Mer information finns i [AEM Creative Cloud-integrering](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html)-artikeln. | AEM 6.3.3.x |

## OSGi-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-1}

Följande textdokument innehåller en lista över de OSGi-paket och innehållspaket som ingår i den gemensamma fiskeripolitiken.

* [Förteckning över OSGi-paket som ingår i AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Förteckning över innehållspaket som ingår i AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM och uppdateringar](https://helpx.adobe.com/experience-manager/aem-releases-updates.html)
>* [AEM 6.3 hotfixsida](https://helpx.adobe.com/experience-manager/kb/aem63-available-hotfixes.html)
>* [Versionsinformation för AEM 6.3](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM produktsida](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.3-dokumentation](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* Prenumerera på [produktuppdateringar med Adobe prioritet](https://www.adobe.com/subscription/priority-product-update.html)

