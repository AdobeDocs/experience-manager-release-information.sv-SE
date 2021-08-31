---
title: AEM 6.2 Cumulative Fix Pack
description: AEM 6.2 Cumulative Fix Pack Release Notes.
source-git-commit: 69f4db4e2ef94c370ed590ec7e9859781a909270
workflow-type: tm+mt
source-wordcount: '19890'
ht-degree: 0%

---

# AEM 6.2 Cumulative Fix Pack Release Notes{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Versionsinformation {#release-information}

| **Produkt** | Adobe Experience Manager |
|---|---|
| **Version** | 6.2 |
| **Frigör** | Kumulativt korrigeringspaket 6.2 SP1-CFP20 |
| **Förutsättning** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Allmän tillgänglighet** | 6 juni 2019 |

### Kumulativt korrigeringspaket {#cumulative-fix-pack}

Adobe introducerade en modell för engångsleverans av korrigeringar. I stället för att släppa snabbkorrigeringar för enskilda utgåvor ger Adobe nu ut ett Cumulative Fix Pack (CFP) varje månad (med reservation för kvalitetskontroller). En CFP är ett aggregerat innehållspaket för flera korrigeringar. Bestrukna artiklar innehåller i första hand felkorrigeringar, men kan även innehålla funktionspaket. De har följande fördelar jämfört med enskilda snabbkorrigeringar:

* Kumulativt (t.ex. en bestruken finans innehåller korrigeringar som gjorts genom tidigare bestrukna finanser)
* Ökad kvalitetssäkring
* Förenklad installation (Användaren installerar en CFP som ett enskilt paket som inte har några beroenden, förutom det senaste Service Pack)

Mer information om CFP och andra typer av releaser finns i [Underhållsrelease Vehicle](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## Om releasen {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 är det sista Cumulative Fix Pack för AEM 6.2 och är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>Om du använder bestruket papper utan att validera kompatibiliteten mellan installerade funktionspaket kan det leda till att systemet inte fungerar eller att anpassade konfigurationer går förlorade, vilket kan kräva återställning från säkerhetskopia för att kunna lösas.

>[!NOTE]
>
>* En ny Sling `discovery-  api` bundle Johnzon 1.0.0 ingår i AEM Cumulative Fix Pack 6.2 SP1-CFP10. Dessutom har en tjänstanvändares sling-discovery lagts till med läs- och skrivbehörighet för noden */var/discovery* i CRX-databasen.
>
>* E-postpaket med apache-kombinationer **org.apache.Commons/Commons-email/1.5** har lagts till som ersättning för **com.day.Commons.wrapper/com.day.Commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Adobe rekommenderar att man driftsätter CFP via installationsmappen för kunder som har ett stort antal användare AEM instansen.

>


## Inkluderade problem {#issues-included}

I det här avsnittet listas alla problem och snabbkorrigeringar som ingår i den aktuella gemensamma fiskeripolitiken.

Dessutom innehåller denna CFP snabbkorrigeringar som levererats i [tidigare kumulativa korrigeringspaket](#previous).

### Integrering {#integration}

* Stöd för flera personaliseringsförbättringar för Campaign-målgruppsanpassning. NPR-29163: Programfix för CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler placeras i en oändlig slinga och orsakar uppdateringar av noder på publiceringsinstanser. NPR-28561: Programfix för CQ-4263096

### DAM - Allmänt {#dam-general}

* Det går inte att visa/dölja replikeringsknappen för användare som inte är administratörer i specifika mappmappar. NPR-29026: Programfix för CQ-4265361

### Sårbarhet {#vulnerability}

* CSRF-skyddsramverket fungerar inte med AEM grundformulär. NPR-28612: Programfix för GRANITE-22231

### Forms {#forms}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package}

>[!NOTE]
>
>För AEM Forms-kunder är det viktigt att installera AEM Forms-tilläggspaket efter installation av AEM Service Pack, Cumulative Fix Pack eller Feature Pack.

>[!NOTE]
>
>AEM Forms tilläggspaket hjälper till att anpassa formulärfunktionaliteten med AEM Service Pack och Cumulative Fix Packs. Därför är det viktigt att du installerar AEM tilläggspaket för formulär när du har installerat AEM Service Pack, Cumulative Fix Pack eller Feature Pack.

#### Adaptiv Forms {#adaptive-forms}

* Användbarhetsproblem med klotterkomponenter för iOS 12.1-enheter. NPR-29082: Programfix för CQ-4261765

#### Forms - dokumentsäkerhet {#forms-document-security}

* Om alla signaturer i en PDF-fil verifieras med hjälp av PDF Advanced Electronic Signatures (PAdES) genereras InvalidOperationException. NPR-27848: Programfix för CQ-4244837

#### Forms - korrespondens {#forms-correspondence}

* När du förhandsgranskar bokstaven som PDF uppfyller inte textfält som placerats på den överordnad sidan det värde som angetts på datafliken eller enligt den angivna datalänkningen. NPR-29239: Programfix för CQ-4266856.

#### Forms - Interaktiv kommunikation {#forms-interactive-communication}

* När du lägger till en apostrof visas de förifyllda fälten i bokstaven som ASCII-tecken i stället för vanliga alfabet. NPR-28863: Programfix för CQ-4262900

### Forms JEE Installer {#forms-jee-installer}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

## Programfixar och funktionspaket som ingår i tidigare Cumulative Fix-paket {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Kumulativt korrigeringspaket 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Huvudinnehållet i det här Cumulative Fix Pack är:

* Stöd för MS Translator API v3.0 som AEM 6.2 har aktiverats
* Loggmeddelandet har lagts till efter att paketet har installerats för alla SP, CFP och HF.

### Assets {#assets}

* Det går inte att byta namn på DAM-mappen om behörigheten Redigera ACL saknas. NPR-27555: Programfix för CQ-104652
* Bildförinställningsredigeringsverktyget svarar inte i 6.2.1 CFP 17 och senare. NPR-28147: Programfix för CQ-4261041

### Sites {#sites}

* Länkkontrollen slutför inte jobbet, fastnar med länkar som inte svarar. NPR-27373: Programfix för CQ-4256030
* Segmentfilen läses inte in korrekt på grund av en ytterligare rotsökväg som bryter segmentets sökväg. NPR-28014: Programfix för CQ-4260332

### Integrering {#integration-1}

* LiveCopy-arvsannullering fungerar inte korrekt på målbehållare. NPR-28129: Programfix för CQ-4259813
* Cq:actions tas inte med i beräkningen för en målkomponent. NPR-27616: Programfix för CQ-4257497

* Visningen av ikonen för att bryta arv är inte konsekvent. NPR-27671: Programfix för CQ-4257779

### Felix {#felix}

* Komponentdetaljer för webbkonsol misslyckas med 500 efter installation av CFP 18 på AEM 6.2 SP1-instans. NPR-28350: Programfix för CQ-4261095

### Översättning {#translation}

* Aktivera stöd för tjänsten MS Translator i AEM 6.3 efter uppgradering av MS Translator till API v3.0. NPR-28123: Programfix för CQ-4259096

### UI - Foundation {#ui-foundation}

* OTB Sites Calendar visar felaktiga datum. NPR-28392

### Granit {#granite}

* Ordlistan är inte ogiltig för resurspaket som använder sling:basename . NPR-27624

### uthållighet {#sustenance}

* Aktivitetsloggar för pakethanteraren ska extraheras i en separat loggfil. NPR-27323: Programfix för Granite-14866
* En standardiserad fras/ordalydelse/loggrad(er) i error.log som ska visas när installationen är klar. NPR-27835
* Plugin-programmet för Granite-paket väljer beroende av en lägre version av org.apache.sling.i18n. Programfix för CQ-4263245
* com.adobe.cq.com.adobe.cq.ui.commons-paketet tas bort när den senaste CFP-filen installeras efter 6.2SP1-CFP15. Programfix för CQ-4258808

### Forms {#forms-1}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-1}

#### Adaptiv Forms {#adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27843: Programfix för CQ-4257315

### Forms JEE Installer {#forms-jee-installer-1}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included}

Följande text innehåller en förteckning över OSGI-paket och innehållspaket som ingår i den gemensamma fiskeripolitiken.

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP19

[Hämta fil](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP19

[Hämta fil](assets/do-not-localize/cfp19_content_packages.txt)

### Kumulativt korrigeringspaket 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Huvudinnehållet i det här Cumulative Fix Pack är:

* Stöd har lagts till i DAM CommandLineProcess för att avsluta den långvariga processen.
* Sessionsläckan i ReplicationEventListener har åtgärdats.
* Stöd för omdirigering har lagts till i kärnsideskomponenten.

### Resurser {#assets-1}

* Camera Raw processer fastnar under perioder med stort intag och blockerar till slut all arbetsflödesbearbetning. NPR-26990: Programfix för NPR-23860
* Hämtningsfunktionen utnyttjar AEM Assets via en resurshämtningsserver som gör det möjligt för anonyma användare att hämta alla resurser. NPR-27054, programfix för CQ-4254732
* Specialtecken visas som brutna på ämnesraden i e-postmallar i AEM. NPR-26470: Programfix för CQ-4252368

### Webbplatser {#sites-1}

* På grund av ett felaktigt beteende för klassen ConfigPostProcessor tas cq bort när den överordnade bilden pausas: LiveRelationship-blandningstyp från den underordnade sidan. NPR-26745: Programfix för CQ-4254163
* Lägg till stöd för omdirigering i kärnsideskomponenten. NPR-26576: Programfix för CQ-110529
* Migrera kontextnav till jquery 3. NPR-26956: Programfix för CQ-4255472
* Ankarindatafält visas utanför de webbläsare som visas i dialogrutan tills de maximeras. NPR-26852: Programfix för CQ-4255019
* Kopiera inklistring av text som infogar oönskad &lt;br> i innehållsfragmentet. NPR-26660: Programfix för CRTE-151
* Klassisk platsadministratör återger inte listan i den högra rutan för vissa sidor. NPR-27247: Programfix för CQ-4251621
* (Klassiskt användargränssnitt) Försök att flytta/byta namn på sidor genererar ett fel, &quot;Ett fel inträffade när sidan flyttades.&quot; NPR-27179: Programfix för CQ-4235907

### Integrering {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever går igenom hela trädet för att samla tillgängliga varumärken. NPR-27060: Programfix för CQ-4255790

### WCM - Foundation Components {#wcm-foundation-components}

* Problem med sökfunktioner i komponenten Foundation-lista. NPR-26817: Programfix för CQ-4250324

### Plattform {#platform}

* På grund av specialtecken med långt tankstreck måste utgivaren inte tömma cachen. NPR-27199: Programfix för CQ-4242790

### Granit {#granite-1}

* Paketvalideraren validerar inte paket som ingår i CFP/SP. NPR-26775: Programfix för Granite-22825

### Replikering {#replication}

* JCR-sessionsläcka i ReplicationListener. NPR-27063: Programfix för CQ-4232088

### Forms {#forms-2}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-2}

* Inga nya AEM Forms-korrigeringar i Forms tilläggspaket.

### Forms JEE Installer {#forms-jee-installer-2}

* Inga nya AEM Forms-korrigeringar i Forms JEE-installationsprogrammet.

#### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-1}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP18

[Hämta fil](assets/do-not-localize/62cfp18updated_bundles.txt)

Förteckning över innehållspaket som ingår i AEM 6.2 SP1-CFP18

[Hämta fil](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Kumulativt korrigeringspaket 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Huvudinnehållet i det här Cumulative Fix Pack är:

* Stöd har lagts till för URL:er utan tillägg för webbplatser i at-integration.js
* S7-avsökningsimporten har tagits bort från molntjänstkonfigurationen för S7.
* Ändringar i målgruppsvyn som har stöd för mappstruktur för implementering av flera innehavare.
* Uppdatera till jqueryui   clientlib v1.12.1.

### Resurser {#assets-2}

* När arbetsflöden startas från resursanvändargränssnittet måste användaren ha behörighet att skriva/ta bort/ändra. NPR-25688: Programfix för CQ-4250140
* Knapparna för publicering och avpublicering är fortfarande synliga även för användare som saknar replikeringsbehörighet. NPR-25094
* (Arbetsflöde) Arbetsflödet för resurser för smarta taggar bearbetas inte via AEM proxykonfiguration. NPR-25915: Programfix för CQ-4248202
* Ta bort importören för S7-avsökning från molntjänstkonfigurationen för S7. NPR-25239: Programfix för CQ-95236

### Webbplatser {#sites-2}

* Arbetsflöden som har startats från redigeraren -> Sidinformation innehåller kontextsökvägen i nyttolasten. NPR-26389: Programfix för CQ-76804
* (Extern länkkontroll) Ogiltiga https-länkar visas som giltiga länkar. NPR-25541: Programfix för CQ-4201333
* (Klassiskt användargränssnitt) När du skapar en fristående sida under en live-kopia skapas sidan som en live-kopia. NPR-25610: Programfix för CQ-4249801
* Problem med publiceringsresurser som är kopplade till designimporterarkomponenten när en sida aktiveras. NPR-25638: Programfix för CQ-102532
* RTE-verktygsfältet innehåller en lista med markeringar. NPR-25165: Programfix för CQ-4248948
* Migrera kontexthub till jquery 3. NPR-25059: Programfix för Granite-19902
* För kapslade parsyskomponenter tillämpas alltid den första (med den minst kapslade sökvägen) som uppfyller designen från flera tillgängliga komponenter. Mer information finns i [Upplösning för designsökväg](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: Programfix för CQ-4246276

### Integrering {#integration-3}

* När du använder OTB-målintegrering återges hela sidan i stället för en tom målkomponent när du aktiverar en komponent. NPR-25273: Programfix för CQ-4248003
* Om arvet bryts i målläget visas komponenten fortfarande som den är avsedd för med arvet som inte bryts i redigeringsläget. NPR-25324: Programfix för CQ-4248162
* När en personalisering definieras på en sida och en målgrupp är löst visas motsvarande upplevelse i redigeringsläge. NPR-25731: Programfix för CQ-4249465
* Felaktig URL för suddgummi när AEM används med en icke-standardkontextsökväg. NPR-25971: Programfix för CQ-4250953
* Tom återgivning när du använder alternativknappen. NPR-25295: Programfix för CQ-4246792
* Upplevelser som tas bort från författarmiljön tas aldrig bort från publiceringswebbplatsen när sidan aktiveras. NPR-24869: Programfix för CQ-4247832

### DAM - DM-klient {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignorerar musklick på enheter med pekskärm. Programfix för CQ-4247370

### Plattform {#platform-1}

* Tillåt konfiguration av maximalt antal återförsök när ett paket hämtas/släpps. NPR-25328: Programfix för Granite-22376
* Felaktig loggning vid replikeringsfel. NPR-25308: Programfix för CQ-4249402
* Om du installerar Forms AEM 6.2 Forms CFP8 till CFP14 misslyckas Apache POI. NPR-25053: Programfix för Granite-21771

### Granit {#granite-2}

* Användarsynkroniseringsprocessen misslyckas med OakConstraint0022-undantag. NPR-25729: Programfix för Oak-7428

### Communities {#communities}

* cq -social-as-provider-paketet börjar inte med mongo driver 3.x-versioner. NPR-26271: Programfix för CQ-4252710

### UI - Foundation {#ui-foundation-1}

* Uppdatera till jqueryui   clientlib v1.12.1. NPR-25090: Programfix för Granite-21981, CQ-4248897

* (Omnisearch): Egenskapen Title är sårbar för XSS-skriptning (Cross-site) på Sites. NPR-24994: Programfix för Granite-19933

### Forms {#forms-3}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-3}

#### Anpassningsbara formulär {#adaptive-forms-2}

* Felaktig kodning när data skickas från adaptiv form. NPR-25539

#### Forms - hantering {#forms-management}

* Ej relaterade formulärresurser rapporteras som referenser när sidan publiceras. NPR-26167: Programfix för CQ-4251004

### Forms - JEE Installer {#forms-jee-installer-3}

#### Dokumentsäkerhet {#document-security}

* Variabeln fylls i som datatypen List, undertypen är sträng, men ett&quot;cannot force object&quot;-fel genereras. NPR-26194: Programfix för CQ-4252287
* Det går inte att komma åt vattenstämpelkonfigurationer efter installation av 6.2-SP1-CFP15. NPR-26130: Programfix för CQ-4250984

### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-2}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP17

[Hämta fil](assets/do-not-localize/62cfp17updated_bundles.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP17

[Hämta fil](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Kumulativt korrigeringspaket 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Huvudinnehållet i det här Cumulative Fix Pack är:

* Stöd för STARTTLS har lagts till i Day CQ Mail Service.
* Justering av ContextHub-ikoner i profilpover har korrigerats.
* Korrigeringar i funktionerna för att visa/dölja i nedrullningsbara komponenter.
* Uppgradera till den senaste versionen av Jackson 2.8.11

### Resurser {#assets-3}

* Det går inte att initiera ett arbetsflöde från en listvy. NPR-24393: Programfix för CQ-4245788
* (Firefox/Chrome) Det går inte att hämta resurser på sidan Resursdelning. NPR-24523: Programfix för CQ-4224408
* Högre standardkvalitet för videoförhandsgranskning i AEM. NPR-24148: Programfix för CQ-4244310

### Integrering {#integration-4}

* När en komponent är avsedd för en publiceringsinstans visas flimmer som visar standardupplevelsen före den valda. NPR-23992: Programfix för CQ-4242038
* Upplevelser som tas bort från författarmiljön tas aldrig bort från publiceringswebbplatsen när sidan aktiveras. NPR-24869: Programfix för CQ-4247832

### Plattform {#platform-2}

* Patch jQuery 1.12.4 from clientlib to include security fix. NPR-24129: Programfix för Granite-20058
* Stöd för STARTTLS har lagts till i Day CQ Mail Service. NPR-23941: Programfix för CQ-4240397
* Ta bort standard MERGE_PRESERVE aclHandling. NPR-24593: Programfix för Granite-21889
* LineChecker kan inte externalisera länkar när begäran innehåller ogiltiga frågeparametrar. NPR-24127: Programfix för CQ-4241893

### MSM {#msm}

* Proaktiva snabbkorrigeringar för XSS-attacker (Cross-Site Scripting). NPR-21893: Programfix för CQ-4223385
* MSM LiveRelationship: effektiv RolloutConfig är fel om BlueprintConfig finns i roten. NPR-23999: Programfix för CQ-4243000

### Webbplatser {#sites-3}

* Om du vill skapa en ny upplevelse i ett område med live-kopior måste arvet brytas för att kunna konfigureras. NPR-24995, programfix för CQ-4248209
* (Touchgränssnitt) Flera ikoner i det övre verktygsfältet försvinner när du låser eller låser upp en sida. NPR-23954: Programfix för CQ-4243345
* Fälten är inte korrekt justerade i kontextub. NPR-23958
* Publiceringsåtgärd vid redigering av låsta sidbrytningar. NPR-23970: Programfix för CQ-4243203
* OTB-rapporter i /etc/reports/ fungerar inte som de ska och visar inget historisk datagram. NPR-20035: Programfix för CQ-4220180
* Det går inte att starta när arbetsflödet Begär start initieras för ett projekt. NPR-24255: Programfix för CQ-4245030
* HTML-taggar och -attribut som ignoreras av e-postmeddelanden efter installationen av CFP10. NPR-24287: Programfix för CQ-4240028
* TagPicker: Lägg till märkord i taggmetadatataggsfältet i taggarna taggningsbara noder, vilket tar lång tid att läsa in. NPR-24347: Programfix för CQ-4244291
* Salesforce-integrering misslyckas med proxykonfigurationer. NPR-24418: Programfix för CQ-4245300
* (WCM) PageManager lämnar Sida incheckad vid undantag när Revision skapas. NPR-24565: Programfix för CQ-4246203
* Enhetsemulatorknappen tas bort från redigerings- och förhandsgranskningsläget när CFP14 har använts. NPR-24566: Programfix för CQ-4247060
* (Klassiskt användargränssnitt) Hela taggarna visas som tomma när de har skapats i dialogrutan. NPR-24688, programfix för CQ-4246407
* Det går inte att skapa versionen vid första försöket. NPR-24774: Programfix för CQ-4232176
* OTB-rapporter i /etc/reports/ fungerar inte som de ska och visar inget historisk datagram. NPR-24138: Programfix för CQ-4220180

### Sårbarhet {#vulnerability-1}

* Salesforce-integreringen är sårbar för SSRF (Server Side Request Forgery). NPR-24289: Programfix för CQ-4245277
* SSRF-säkerhetslucka (Server Side Request Forgery) i ReportingServicesProxyServlet. NPR-24657: Programfix för CQ-4246880

### Granit {#granite-3}

* Läsåtgärder för metadata avslutas inte. NPR-24240: Programfix för Granite-19866
* Uppdatera Jetty till 9.4.11.v20180605 för att åtgärda säkerhetsluckor. NPR-25033: Programfix för Granite-22120

### WCM - Foundation Components {#wcm-foundation-components-1}

* PageComparator genererar ClassCastException när sidorna sorteras. NPR-24123: Programfix för CQ-4244048
* Visa/dölj-funktionen för den nedrullningsbara formulärkomponenten fungerar inte som förväntat. NPR-24562: Programfix för CQ-422853

### Användargränssnitt {#user-interface}

* Hög processoranvändning observeras på grund av många förfrågningar i administratörssökningsfunktionen. NPR-23588: Programfix för Granite-21286
* (Klassiskt användargränssnitt) Komponenten visar standardvärdena även om den associerade datamodelltjänsten för formulär är inställd på ett tomt fält. NPR-21903: Programfix för GRANITE-19744
* Multifält som genererar NPE när det inte finns några FormData för begäran. NPR-24513: Programfix för Granite-21055

## Forms {#forms-4}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-4}

#### Core {#core}

* (OSGI) AEM Forms OSGI har påverkats av Jackson databindningssäkerhetsvarning. NPR-24274: Programfix för CQ-4230245

#### Rights Management {#rights-management}

* Apache POI misslyckas efter installation AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Programfix för CQ-4245898, CQ-4244778

#### HTML5 Forms {#html-forms}

* Data fylls inte i med förifyllning av flerradiga fält i HTML-förhandsvisning. NPR-23357: Programfix för CQ-4244212
* När en bokstav förhandsgranskas via standardförhandsgranskning visas inte mappning av layoutfragment när samma visas korrekt när användaren klickar på knappen Förhandsgranska. NPR-22993: Programfix för CQ-4237745
* Problem med HTML-förhandsgranskning av ett textfält när ett mönster för socialförsäkringsnummer används i en mall. NPR-23205

#### Adaptiv Forms {#adaptive-forms-3}

* Felet &quot;Guidelib is not defined&quot; när AEM läggs till i en parsys-komponent. NPR-24269: Programfix för CQ-4244546

### Forms JEE Installer {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Fönsterradslut i Shell-skriptfiler gör att LCM inte körs i UNIX. NPR-22958

### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-3}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP16

[Hämta fil](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP16

[Hämta fil](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Kumulativt korrigeringspaket 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

Huvudinnehållet i det här Cumulative Fix Pack är:

* Proaktiv säkerhetskorrigering i Foundation-registret för att bibehålla en konsekvent design.
* Stöd för typeHint har lagts till för att spara värden som sträng.
* Förbättrad säkerhet för Forms förifyllningstjänst
* Uppdatera till den senaste filen adobe-reader-extensions-dsc.jar för korrigeringar i Reader Extension.
* Justerad valideringskrok för att ta hänsyn till &quot;:invalid&quot;-objekt för ökning av talindata.

### Resurser {#assets-4}

* EmbedXMP-data anges alltid till&quot;active&quot; för Ptiff-genereringsprocessen. NPR-22776: Programfix för CQ-4234498
* Det går inte att ange flera standardvärden i flervärdesfält. NPR-22900: Programfix för CQ-4239000
* (Dynamic Media) När du markerar kryssrutan Dynamiska återgivningar får den hämtade zip-filen den ursprungliga TIFF-bilden med en byte-fil som är noll. NPR-22410: Programfix för CQ-4198471
* (Touch UI) Standardplats för överföring av resurser i kolumnvyn. NPR-23475: Programfix för CQ-4237057

### Integrering {#integration-5}

* I målläget kan författare ändra en komponent som ärvts från utkastet utan att avbryta arvet. NPR-22751: Programfix för CQ-4237907
* Sökvägsvariabeln är inte korrekt kodad, vilket leder till icke-beständig korsskriptning (XSS). NPR-22851

### MSM {#msm-1}

* Om en ResourceNameConflict uppstår under roten, avslutas utrullningsflödet utan att alla grenar inkluderas, när en LiveCopy-konfiguration med flera rollout-konfigurationer körs. NPR-22842: Programfix för CQ-4236188

### Plattform {#platform-3}

* Implementera en avsökningsgräns i en begäran om omvänd tillämpning. NPR-23351: Programfix för Granite-21135****
* Ändringen av meddelandemönstret återspeglas inte i anpassade loggare. NPR-23486: Programfix för CQ-4241974

### Webbplatser {#sites-4}

* Det går inte att skapa en länk i en text i en textredigerare till ett dokument med blanksteg eller andra specialtecken. NPR-22289: Programfix för CQ-4224321
* Om du sparar segmentet med ett mycket stort värde (100000000) blir ökningen 0, vilket ger ett felmeddelande. NPR-22524: Programfix för CQ-4237006
* Det går inte att klicka på Lägg till objekt i flerfältskomponenten. NPR-22552: Programfix för CQ-4237404
* Den vågräta rullningslisten visas inte när segmentet har en lång titel. NPR-22615: Programfix för CQ-4237001
* Inläsning av en tom publik genererar en felaktig JavaScript-kod. NPR-22974: Programfix för CQ-4238734
* När du schemalägger en aktivering eller inaktivering är arbetsflödets titel obligatorisk, vilket innebär att den anpassade arbetsflödets titel inte översätts på tidslinjen. NPR-23121: Programfix för CQ-4237552
* Begär korrigeringar av problem runt målsegment i Sites. NPR-23128
* (Firefox) Kryssrutan för den valda personen är inte korrekt. NPR-23345
* Etiketter för de olika lägena visas tillsammans med ikoner. NPR-23275
* Felet &#39;Ogiltigt värde för rekursionsväljare&#39; uppstod när en komponent skulle migreras från AEM 6.0 till AEM 6.2. NPR-23503: Programfix för CQ-4241258

### Communities {#communities-1}

* Webb- och e-postmeddelanden utlöses inte på grund av ett meddelandefel för grupperna. NPR-23447: Programfix för CQ-4242880

### Översättning {#translation-1}

* Kopior av tillgångsspråk skapas när resursen &quot;Do not translate&quot; anges i översättningskonfigurationen. NPR-22540: Programfix för CQ-4237962

### Användargränssnitt {#user-interface-1}

* Om du använder Omnissearch med bindestreck returneras ett serverfel. NPR-22999: Programfix för Granite-19674
* DatePicker har inte stöd för att manuellt ange ett externt texttips som angetts av dolda fält. Om du ändrar typtipset uppstår ett konverteringsfel. NPR-23333: Programfix för Granite-21194

### WCM - Foundation Components {#wcm-foundation-components-2}

* CAPTCHA-komponenten har tagits bort för bättre säkerhet, och om du använder CAPTCHA-komponenten visas meddelandet&quot;Captcha-komponenten är föråldrad och bör inte längre användas&quot;. visas efter installation av version 6.2 SP2-CFP15 eller senare. AEM kan anpassas så att de innehåller reCAPTCHA för bättre säkerhet NPR-22151: Programfix för CQ-4224052
* WCM Foundation-komponenten Table är sårbar för lagrade korsskriptning mellan webbplatser. NPR-23206: Programfix för CQ-4240760

### Sårbarhet {#vulnerability-2}

* XSS (Cross-site scripting) i Admin UI Project-länkar. NPR-23272: Programfix för CQ-4241795

## Forms {#forms-5}

### Forms tilläggspaket {#forms-add-on-package-5}

#### Korrespondenshantering {#correspondence-management}

* När en bokstav förhandsgranskas via standardförhandsgranskning visas inte mappning av layoutfragment när samma visas korrekt när användaren klickar på knappen Förhandsgranska. NPR-23335: Programfix för CQ-4237745
* Data i bokstaven som motsvarar bindningar som definieras i XDP fylls inte i med URL för direktbrev. NPR-24145: Programfix för CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Korrespondenshantering) Felpassning av data vid inläsning av brev med mål-XML. NPR-22993: Programfix för CQ-4237663

#### Tjänsten Reader Extensions {#reader-extensions-service}

* Det går inte att använda läsartillägg på Adobe PDF. NPR-23067

#### Forms Manager {#forms-manager}

* Forms som är inbäddat i Site publiceras inte när du publicerar om Webbplatssidan. NPR-23014: Programfix för CQ-4236566

#### Sårbarhet {#vulnerability-3}

* Proaktiva snabbkorrigeringar för korsskriptning mellan webbplatser. NPR-20624: Programfix för CQ-4206055
* En XSS-säkerhetslucka (Cross-Site Scripting) har lagrats på fliken Anteckningar i Forms Manager. NPR-27157: Programfix för CQ-4255556

#### Krypteringstjänst {#encryption-service}

* (OSGI) [JEE] Felaktig signaturstatus för PDF med bifogad fil vid verifiering med &quot;Validera PDF-process&quot;. NPR-23269, NPR-23737

### Forms JEE Installer {#forms-jee-installer-5}

#### Core {#core-1}

* De problem som rapporteras i den statiska kodanalysen av Core-ext bör åtgärdas. NPR-13947

#### PDFG-tjänst {#pdfg-service}

* Konverteraren HTML till PDF fungerar inte. NPR-21545

### OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-4}

Följande text innehåller en förteckning över OSGI-paket och innehållspaket som ingår i den gemensamma fiskeripolitiken.

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP15

[Hämta fil](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP15

[Hämta fil](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Kumulativt korrigeringspaket 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Förbättrad redigering av metadataegenskaper för resurser.
* Lösenordets förfalloaviseringsjobb har konfigurerats om för resurser som redan har förfallit.
* Anpassad Touch UI-konsol för ytterligare språk.
* Uppdaterad cq-msm-core för effektiv Livecopyindexsynkronisering.
* Effektivare replikeringsfunktioner för olika utrullningar.

### Resurser {#assets-5}

* Användare kan inte hämta resurser med ansvarsfriskrivning och långa filnamn. NPR-22163: Programfix för CQ-4235274
* Ett enkelt citattecken förhindrar att metadata uppdateras i vyn och gränssnittet bryts helt när du öppnar egenskaperna för en resurs med hjälp av snabbverktygsfältets åtgärder. NPR-22317, NPR-22353: Programfix för CQ-4236990, CQ-4236469
* Meddelandejobbet Förfallodatum för tillgång inaktiverar inte de förfallna resurserna. NPR-22346: Programfix för CQ-4237188
* Det går inte att hämta resurser när du använder Digital Rights Management i resurser på Safari. NPR-22378: Programfix för CQ-4236460
* Webbåtergivning för små bilder har felaktig pixelstorlek. NPR-22435: Programfix för CQ-4236742

### Webbplatser {#sites-5}

* (Touchgränssnitt) Den flyttade taggen visas på den gamla och nya platsen i sidegenskaperna. NPR-21921, programfix för CQ-4238598
* (Touch-gränssnittet) RTF-redigeraren tar bort alla andra attribut än id från taggen &lt;a>. NPR-22045: Programfix för CQ-4234133
* Om du klistrar in innehåll direkt i RTF-redigeraren med CTRL+V hoppas radbrytningarna över. NPR-22117: Programfix för CUI-5881
* (Touch UI) Det går inte att visa fler än 40 taggar under namnutrymmet. NPR-22290: Programfix för CQ-99114
* RSS-flödesproblem, port -1 till AEM 6.2 NPR-22158: Programfix för CQ-423339
* (IE) När du redigerar ett tecken i RTF-fältet för första gången läggs ett avslutande blanksteg till i tecknet. NPR-22443: Programfix för CQ-4235343
* När Java Use-objektet försöker matcha paketnamnet fryser det SightlyJavaCompilerService på grund av ett avslutande blankstegstecken i paketdeklarationen. NPR-22557: Programfix för Granite-20836
* Touch UI-konsolen kan inte identifiera nya språk för taggning. NPR-22250: Programfix för CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Både Publication Date (Publiceringsdatum) och cover Date (Omslagsdatum) var obligatoriska fält som skulle anges för folios innan de överfördes till DPS. NPR-22484

### Handel {#commerce}

* XSS-säkerhetsluckor (Multiple Cross-site scripting) vid skapande av katalog för e-handel. NPR-22344: Programfix för CQ-4237017

### MSM {#msm-2}

* LiveCopyIndex-synkronisering leder till överbelastning av trådar under långa indexuppdateringar. NPR-22214: Programfix för CQ-90667
* cq:cugEnabled-egenskapen inaktiveras när ett annat fält i en livecopy redigeras, vilket gör sidan oskyddad. NPR-22246: Programfix för CQ-4236050
* Åtgärden för sidutrullning kan inte uppdatera underordnade när en sida är inaktiverad. NPR-22483: Programfix för CQ-4236956
* Om en struktur som har flyttats i en överordnad förs över leder det till fel cq:moveTarget. NPR-22373: Programfix för CQ-4232536

### Integrering {#integration-6}

* Om du försöker sortera erbjudanden i erbjudandeväljarbiblioteket uppstår ett osäkert beteende. NPR-22208: Programfix för CQ-4235439
* TargetContentImpl gör AEM trög under långa frågor. NPR-22361: Programfix för CQ-4236907
* Målmotorn (mbox.js, at.js) använder inte inbyggda URL:er och URL:er som innehåller kolon som kan misslyckas vid vissa distributioner. NPR-22366: Programfix för CQ-4237854
* Sidanpassning kräver publicering direkt i varumärkesnoden. NPR-22370: Programfix för CQ-4236895

### Foundation {#foundation}

* Apache Sling Scripting Simtly Models använder providerpaketet **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: Programfix för Sling-5944, Sling-6866

### Projekt {#projects}

* Arbetsflödesstartaren kan inte acceptera TypeHint-värdet för String. NPR-22436: Programfix för CQ-4237855

### Översättning {#translation-2}

* Undersök problem med funktionen Förhandsgranska. NPR-22201: Programfix för CQ-4223753

### Användargränssnitt {#user-interface-2}

* (Klassiskt användargränssnitt) Komponenten visar standardvärdena även om den associerade datamodelltjänsten för formulär är inställd på ett tomt fält. NPR-21903: Programfix för GRANITE-19744

### WCM - Foundation Components  {#wcm-foundation-components-3}

* Fel vid publicering av en Live Copy-sida som pekar på en importsida i Adobe Campaigns. NPR-22470: Programfix för CQ-4237164
* JavaScript-fel när Experience Fragments Editor öppnas. NPR-22598: Programfix för CQ-4238415

### Arbetsflöde {#workflow}

* Day CQ Workflow Email Notification Service utlöser ett e-postmeddelande per Mongo-nod för WorkflowCompleted- och WorkflowAborted-meddelanden. NPR-22486: Programfix för CQ-4238172

## Forms {#forms-6}

### Forms tilläggspaket {#forms-add-on-package-6}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

#### Adaptiv Forms {#adaptive-forms-4}

* Inkonsekvent värde för nedrullningsbar platshållare i adaptiv form i IE11 och Chrome. NPR-22405: Programfix för CQ-4227096

### Forms JEE-installationsprogram {#forms-jee-installer-6}

#### Installera LCM {#install-lcm}

* Uppdatera Jsafe Jars till Cryptoj 6.1.3.1 i installationsprogrammet och LCM. NPR-22744

### Funktionspaket ingår {#feature-packs-included}

#### Processhantering {#process-management}

* (HTML-arbetsyta) När en användare gör anspråk på en uppgift uppdateras antalet köer för den aktuella användaren, men inte för andra användare, såvida inte sidan uppdateras. NPR-19778: Programfix för CQ-4233665

### OSGI-paket och innehållspaket som ingår i CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP14

[Hämta fil](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP14

[Get ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Aktiverade fältkonfiguration för statiska parametrar i inställningarna för målkomponenter när AT.js användes som klientbibliotek.
* Korrigeringar i funktionerna för att visa/dölja i nedrullningsbara komponenter.
* Korrigeringar för målsynkronisering.
* Ökade mångsidigheten i Correspondence Management för att kunna hantera specialtecken.

### Resurser {#assets-6}

* Det går inte att ta bort tidigare versioner av resurser med Rensning av version. NPR-21682: Programfix för CQ-4212996
* Det går inte att ändra ordning på mappar under en omsorteringsbar mapp. NPR-21964: Programfix för CQ-4231761

### Webbplatser {#sites-6}

* (TouchUI)(ClassicUI) Sårbarheter med flera serveröverskridande skript (XSS) i HTML och kärnkomponenter. NPR-21532: Programfix för CQ-4232305 och CQ-4232511
* Det går inte att skapa/formatera innehåll (t.ex. tilldela/ta bort nya listformat) för en markerad text i Internet Explorer 11. NPR-21533: Programfix för CQ-4230689
* (Safari) Användare kan inte visa alla resurser på panelen Sök efter resurser. NPR-21981: Programfix för CQ-4213720
* Time Warp returnerar felet &quot;RecursionTooDeepException&quot; med förvrängd sida och ingen ny version skapas även när datumet ändras. NPR-21707: Programfix för CQ-4199536
* När du läser in en sida i redigeraren läses WorkflowStatusProvider (pageinfo.json) in tre gånger vilket gör att AEM körs långsamt. NPR-21778: Programfix för CQ-59232

### Integrering {#integration-7}

* Det går inte att skapa målgrupper med Mobile Type &amp; Browser i redigeringsläget Target i AEM. NPR-21676, NPR-21681: Programfix för CQ-4232100
* Under hög latens vid en uppdatering av en målkomponent är det möjligt att lägga till ytterligare ett erbjudande innan komponenten uppdateras helt. NPR-21744: Programfix för CQ-4233158/CQ-4234293
* Användare kan inte se testvärden för statiska parametrar i mbox-anropet som kan ses när de testar med AT.js som klientbibliotek i molnkonfiguration. NPR-21930: Programfix för CQ-4234520

### Plattform {#platform-4}

* Prestandaproblem med användarsynkronisering när antalet användare eller grupper är stort. NPR-20431: Programfix för CQ-4223282
* Användare som inte är synkroniserade med användarsynkronisering med hjälp av Sling Distribution. NPR-21911: Programfix för Granite-20404
* Förhindra att stoppord markeras i sökutdrag (på en Geometrixx). NPR-21835: Programfix för Granite-21067\
   Obs! Denna korrigering kräver Oak CFP 1.4.20 eller senare.

### Översättning {#translation-3}

* jcr-egenskapen saknas för initierarens användar-ID när översättningsprojektet skapas. NPR-21715: Programfix för CQ-4230713

### WCM - Foundation Components {#wcm-foundation-components-4}

* Visa/dölj-funktionen för den nedrullningsbara formulärkomponenten fungerar inte som förväntat. NPR-22164: Programfix för CQ-4235288

## Forms {#forms-7}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-7}

#### Adaptiv Forms {#adaptive-forms-5}

* XML-injektion av extern enhet (XXE) i Adaptiv Forms. NPR-21982: Programfix för CQ-109878
* (iOS11) När du klickar på en komponent för bifogad fil öppnas kameran i stället för enhetens filläsare. NPR-21928: Programfix för CQ-4214348
* Titel som saknas i gränssnittet för att skapa teman orsakar undantag och återgivning av dialogrutan misslyckas. Programfix för CQ-4236143

#### Korrespondenshantering {#correspondence-management-1}

* Återgivningen ger problem med XML-data som innehåller specialtecken. NPR-21712: Programfix för CQ-4229137

### Forms JEE-installationsprogram {#forms-jee-installer-7}

#### Assembler Service {#assembler-service}

* PDF-filen som genererats med 6.2.0-ASM-1017-003 är skadad. NPR-21427: Programfix för CQ-4228046

#### PDFG-tjänst {#pdfg-service-1}

* OCR-fel på grund av oväntad sidstorlek (PDF) från PNG-, JPEG- och TIFF-filer. NPR-19489: Programfix för CQ-4209079

## OSGI-paket och innehållspaket som ingår i CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP13

[Hämta fil](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lista över innehållspaket som ingår i AEM 6.2SP1-CFP13

[Hämta fil](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Förbättrad metadatahantering för fält med flera värden.
* Stöd för landskoder med flera tecken (fler än två) i arbetsflöden för översättning.
* Förbättrad återgivning av sidor med flera kapslade komponenter.
* Förbättrad synkronisering av publiceringsdatum för resurser mellan AEM och Adobe Digital Publishing Suite.

### Resurser {#assets-7}

* För många tecken i OmniSearch gör att AEM kraschar. NPR-21083: Programfix för CQ-4223602
* Värden som anges i det andra alternativet i ett fält med flera värden i metadataschemat läggs inte till de värden som tidigare angetts i CRX-de. NPR-21220: Programfix för CQ-4224526
* Det går inte att hämta resurser när du använder Digital Rights Management i resurser på Safari. NPR-21387: Programfix för CQ-4230287

### Webbplatser {#sites-7}

* (DAM) (ClassicUI) Flera serveröverskridande skriptproblem (XSS) i vissa SWF-filer i AEM CQ Author/Publish quickstart. NPR-21073, NPR-21074: Programfix för NPR-20612
* Taggväljaren översätter inte de taggar som finns på flera språk.NPR-21221: Programfix för CQ-78855
* Renderingsproblem med AEM artikelkonsol som användning av flera kapslade komponenter gör det trögt. NPR-21271: Programfix för CQ-4224158

### Integrering {#integration-8}

* När du lägger till ett målramverk är målläget inte tillgängligt i listan över valda lägen i redigeraren. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Publiceringsdatum för folios i AEM matchar inte de datum som visas i Folio Producer. NPR-21145

### MSM {#msm-3}

* Återställningen av Live Copy stoppas när den första lokala sidan i LC har tagits bort. NPR-21276: Programfix för CQ-4229743

### Plattform {#platform-5}

* Anpassad tagg som refererar till taggar som implementerats som skript hittas inte efter uppgradering till AEM 6.3. NPR-20149: Programfix för Granite-18433

### Översättning {#translation-4}

* Översättningsarbetsflöden fungerar inte med lang_country-koder som är längre än två tecken. NPR-21088: Programfix för CQ-4197439
* Resurssidan får inte skickas igen till ett översättningsprojekt förrän projektet har slutförts. NPR-21219: Programfix för CQ-4209908

### Användargränssnitt {#user-interface-3}

* Select-komponenten tar inte bort target-egenskapen när formulär skickas. NPR-21163: Programfix för GRANITE-14125
* HTTP.encodePathOfURI expanderar dubbelkodar plustecknet +. NPR-21417: Programfix för GRANITE-16340

### Sårbarhet {#vulnerability-4}

* XSS (Cross-site scripting) i DAM-metadataredigeraren. NPR-21434: Programfix för CQ-83472
* Flera SWF-filer är sårbara för XSS (Cross-site scripting). NPR-20612: Programfix för CQ-4213297

## Forms {#forms-8}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-8}

#### Korrespondenshantering {#correspondence-management-2}

* (IE11) Den inledande återgivningen av HTML-innehållet sker bara på den vänstra sidan medan den högra sidan läses in regelbundet när hela användargränssnittet har lästs in. NPR-21554
* Skicka-knappen för förhandsgranskning av brev inaktiveras efter installation av AEM 6.2 SP1-CFP9. NPR-21547
* När du väljer resurslänkningstyp öppnas inte fönstret Resursväljare i guiden Redigera bokstavsdatabindning. NPR-21164: Programfix för CQ-4194567
* Om du vill redigera en textbunden eller redigerbar textmodul trycker du på motsvarande redigeringsikon eller dubbelklickar på motsvarande textmodul i förhandsvisningen av bokstaven. NPR-21402

#### Adaptiv Forms {#adaptive-forms-6}

* AEM Forms-komponenten för skicka-knappen visar type=&quot;button&quot; i stället för type=&quot;submit&quot;. NPR-21007
* Data är beständiga när du lägger till eller tar bort nya paneler för repeterbara paneler. NPR-21408

### Forms JEE-installationsprogram {#forms-jee-installer-8}

#### Core {#core-2}

* Uppgradering till den senaste Java 8-uppdateringen 131 ger ett undantag: &quot;JsafeJCE-providern är inaktiverad, en självintegritetskontroll som krävs för FIPS 140 misslyckades.&quot; NPR-21355

   **Obs!** Den här NPR-funktionen kräver ytterligare inställningar. Mer information finns i  [Senaste Java 8-uppdateringen](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr).

* Uppdatera jsafe jars till cryptoj 6.1.3.1 i Core, Encryption, Signature &amp; Document Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Installera LCM {#install-lcm-1}

* Uppdatera Jsafe Jars till Cryptoj 6.1.3.1 i installationsprogrammet och LCM. NPR-21362

#### PDFG-tjänst {#pdfg-service-2}

* Uppdatera Jsafe Jars till Cryptoj 6.1.3.1 i PDFG. NPR-21359

#### Processhantering {#process-management-1}

* (HTML-arbetsyta) Aktivera storleksändring av kolumner så att namnkategorin inte ser trunkerad ut. NPR-19770: Programfix för CQ-4233668

#### Tjänsten Reader Extensions {#reader-extensions-service-1}

* Uppdatera jsafe jars till cryptoj 6.1.3.1 i RE. NPR-21357

## OSGI-paket och innehållspaket som ingår i CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP12.1

[Hämta fil](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lista över innehållspaket som ingår i AEM 6.2 SP1-CFP12.1

[Hämta fil](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Uppdaterad cq-msm-core för effektiv Livecopyindexsynkronisering.
* Förbättrad redigeringseffektivitet för innehållsfragment.
* Tillhandahåller valideringsalternativ i pakethanteraren för att identifiera ACL-behörigheter.
* Introducerade möjligheten att Campaign kunde inkludera e-post-ID för kundkorrespondens.
* Förbättrade videokodningsfunktioner för Dynamic Media-filer.
* Korrigeringar i Sightly Component och LiveCopies.

### Resurser {#assets-8}

* Dynamic Media videokodning misslyckas för filer som innehåller blanksteg i sina namn. NPR-20818: Programfix för CQ-102469
* Flera XSS-säkerhetsluckor (cross-site scripting) i vissa SWF-filer i AEM CQ Author/Publish quickstart. NPR-21071, NPR-21072
* Användare kan inte hämta resurser med ansvarsfriskrivning och långa filnamn. NPR-20255: Programfix för CQ-422139

### Webbplatser {#sites-8}

* AEM och Campaign-integrering: Speciallänkar skrivs om i Adobe Campaign och förhindrar att kunder skickar e-post till: hyperlänkar i deras e-postmeddelanden. NPR-20787: Programfix för CQ-4225760
* (Touch UI) AEM användbarhetsproblem och prestandaproblem när språket är inställt på franska. NPR-20854: Programfix för CQ-4227628
* Om du länkar en kodad resursfil med ett länkplugin-program i RTE returneras en tom länk. NPR-20626, NPR-21059: Programfix för CQ-4223011
* Metadataredigeraren för innehållsfragment förhindrar att innehållsförfattare sparar ändringar i innehållsfragment. NPR-20641: Programfix för CQ-4224755
* Alias för sidegenskaper leder till Begär publikation/Begär avpublicering. NPR-20731: Programfix för CQ-4226227
* Textkomponenten har problem med länkkodning i RTE-element. NPR-20755: Programfix för CQ-4224321

### Plattform {#platform-6}

* ResourceResolverImpl.map() anropar inte ResourceDecorator. NPR-20788: Programfix för GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver kan inte bearbeta begäranden via org.apache.sling.engine.SlingRequestProcessor. NPR-20706: Programfix för CQ-94880
* Begär att lägga till ett valideringsalternativ i Pakethanteraren för att identifiera om några behörigheter/behörigheter för åtkomstkontrollistor har ändrats för ett visst paket. Programfix för CQ-4229196

### Integrering {#integration-9}

* (Search &amp; Promote) Tvetydig filterdefinition för innehållspaketet leder till överskrivna sökvägar vid installationen. NPR-20808: Programfix för CQ-4227615

### Arbetsflöde {#workflow-1}

* Stabilitetsproblem AEM driftsättningen av produktionsservrar. NPR-20979: Programfix för Granite-19104

### Projekt {#projects-1}

* (Touch UI) Det går inte att lägga till teammedlemmar i ett projekt. NPR-20990: Programfix för CQ-4205375

### WCM-Foundation-komponenter {#wcm-foundation-components-5}

* Bildkomponenten &quot;link to&quot; genererar 403-fel på grund av att tillägget .html saknas. NPR-20823: Programfix för CQ-4195909
* Om du försöker ta bort en Form-komponent på en ritningswebbplats med LiveCopy genereras ett NullPointerException och Form-komponenten läggs till i stället för att den tas bort. NPR-20855: Programfix för CQ-4204628
* LiveCopyIndex-synkronisering leder till överbelastning av trådar under långa indexuppdateringar. NPR-20634: Programfix för CQ-90667

### Dokumentskydd {#security}

* Proaktiv uppdatering av XSS-bibliotek. NPR-21174
* Uppgradera till Apache Commons E-post 1.5 som visar ett förenklat API för att skicka e-post. NPR-20509: Programfix för Granite-18240
* Säkerhetsuppdatering för API:t för Apache Sling XSS-skydd eliminerar risken för att XSS kringgås. NPR-21290: Programfix för GRANITE-19924
* XSS-förbikoppling i funktionen XSSAPI#getValidHref. NPR-21174: Programfix för Granite-19924

### Mobilappar {#mobile-apps}

* Korrigerade problem med url Head-begäranden för OOTB-resurser i AEM. NPR-20511: Programfix för CQ-4221520 och CQ-103024

## Forms {#forms-9}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

AEM Forms i korthet:

* Aktiverad certifikatautentisering för Workbench-användare.
* Korrigeringar för Correspondence Management, HTML5-formulär och AEM Forms-arbetsytan.

### Forms tilläggspaket {#forms-add-on-package-9}

#### HTML5 Forms {#html-forms-1}

* Användbarhetsproblem med klotterkomponenter på iOS 10- och 11-enheter. NPR-21092

#### Korrespondenshantering {#correspondence-management-3}

* (Motsvarandegränssnitt) Inaktivera skicka-knappen efter ett klick. NPR-21078

### Forms JEE-installationsprogram {#forms-jee-installer-9}

#### Assembler Service {#assembler-service-1}

* docConvertor kan inte skapa PDF/A. Felmeddelandet &quot;stEvt&quot; för elementet &quot;stEvt:action&quot; är inte bundet. NPR-21032: Programfix för CQ-422540
* Ett undantag genereras med namnet java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE när tjänsten OMPFSubmission/PDFA/PDFtoPDFA anropas. Detta förhindrar att den kortvariga signaturverifieringsprocessen slutförs tills servern har startats om. NPR-20792

#### Workbench {#workbench}

* Aktivera certifikatautentisering för Workbench-användare. NPR-17548: Programfix för CQ-4214486

#### Processhantering {#process-management-2}

* Förbered dataprocess anropar flera gånger när mobilformulär återges med dataref-parametrar. NPR-19801: Programfix för CQ-4230427: CQ-4230400

## OSGI-paket och innehållspaket som ingår i CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP11

[Hämta fil](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lista över innehållspaket som ingår i AEM 6.2 SP1-CFP11

[Hämta fil](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* En ny verktygsfunktion onDialogLoaded har lagts till för test.
* Lagt till frontend-enhetstester och konfigurationer i ClientLibraryProxyServlet.
* Prestandakorrigeringar i en redigeringskomponent för flera bilder på plats.
* Konfigurationsuppdateringar i Apache Sling JCR ResourceBundleProvider.

### Resurser {#assets-9}

* Förhandsgranskning av resurser fungerar inte om arbetsflöden för resursuppdatering är inaktiverade. NPR-20543: Programfix för CQ-4204986
* Återgivningsproblem med klass som lagts till i graniten: class property (cq-damadmin-admin-assets-upload). NPR-20514: Programfix för CQ-4219238
* Miniatyrbilder med specialtecken i titeln visar java-objekt i alt-attributet för NPR-20347: Programfix för CQ-4223620
* Ersätt versionsjämförelsekod med Adobe på grund av licensproblem. NPR-20273: Programfix för CQ-4223758
* Bearbeta problem vid överföring av CMYK PSB-filer med flera alfalager. NPR-20251: Programfix för CQ-4220869
* Internationaliseringsordlistor fungerar inte om inte servern startas om i org.apache.sling.i18n 2.5.6. NPR-20525: Programfix för Granite - 19490
* Inga tråddumpar genereras enligt schemaläggningsperioden med standardkonfigurationen för insamling av tråddumpar (standard AEM start). NPR-20288: Programfix för GRANITE-19488 / GRANITE-12741 / CQ-90647.

### Webbplatser {#sites-9}

* Om det ändrade datumfiltret ändras efter att den sparade sökningen har öppnats, påverkas inte resultaten och de resultat som visas är desamma som det tidigare sparade värdet för det ändrade datumfiltret. NPR-19739: Programfix för CQ-4219425
* Det gick inte att läsa in sidor med kapslade komponenter. NPR-20312
* Arbetsflödet för borttagning aktiveras när arbetsflödespaket tas bort. NPR-20266: Programfix för CQ-4221686
* (Touch UI) Problem med Kopiera/Klistra in med operativsystemets Urklipp och det interna AEM Urklipp. NPR-2028: Programfix för CQ-4220383
* AEM blir trög med listvyn när flera resurser (fler än 100) läses in. NPR-20034: Programfix för CQ-422695
* (Touch UI) Borttagning av starter via Classic UI-konsolen gör att alla sidor inte kan redigeras. NPR-20520: Programfix för CQ-4225074
* Listrutan Mål fungerar inte med flera RTE-komponenter i en dialogruta. NPR-20345: Programfix för CQ-4220981

### Plattform {#platform-7}

* När ClientLibraryProxyServlet används med en anonym session proxybegäranden till klientbibliotek på publiceringsinstansen, och HTTP 404 hittas inte. NPR-20195: Programfix för Granite-14409

### Integrering {#integration-10}

* Om du väljer målmotor som Adobe Target hindras komponenten från att läsas in och ett fel genereras i serverloggen. NPR-20058: Programfix för CQ-88071, CQ-109698, CQ-4201600

### Handel {#commerce-1}

* Inget meddelande om bekräftelse eller omdirigering visas när du skapar produkter på samma sida. NPR-20257: Programfix för CQ-4223414

### Användargränssnitt {#user-interface-4}

* När Datepicker är ett fält i ett multifält bevaras inte värden som sparats i datumfält när komponenten redigeras. NPR-20077: Programfix för GRANITE-19147
* Tidigare frågor avbryts inte om efterföljande frågor utlöses, vilket leder till felaktiga resultat. NPR-20397: Programfix för GRANITE-19306

### WCM - Foundation Components {#wcm-foundation-components-6}

* Egenskapen ImageMap finns fortfarande även efter att du har tagit bort bilderna från redigeringskomponenten Multiple image på plats. NPR-20142: Programfix för CQ-422982

## Forms {#forms-10}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-10}

#### Adaptiv Forms {#adaptive-forms-7}

* valueCommit-skript körs två gånger för DropDownList när det ändras via UI. NPR-1989: Programfix för CQ-110212

### Forms JEE Installer {#forms-jee-installer-10}

**Processhantering**

* CFP-paketet innehåller AEM Forms HTML Workspace version 2.2.26. NPR-20099
* Det förifyllda formuläret fungerar inte när mobilformuläret är konfigurerat att visas som PDF. NPR-20566

**Rights Management**

* Dialogrutan Välj certifikat för ömsesidig autentisering ska visa certifikat med EKU (Enhanced Key Usage) som klientautentisering eller smartkortsinloggning. NPR-20708
* Forms JEE har stöd för PKCS#11, ömsesidig autentisering. NPR-15001

## OSGI-paket och innehållspaket som ingår i CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Förteckning över OSGi-paket som ingår i AEM CFP 6.2 SP1-CFP10

[Hämta fil](assets/do-not-localize/bundle-list-cfp10.txt)

Förteckning över innehållspaket som ingår i AEM CFP 6.2 SP1-CFP10

[Hämta fil](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Anpassad Analytics Classic-gränssnittskonfiguration för hemlig inmatning.
* Korrigeringar för oberoende beständig cache för Contexthub.
* Korrekt beräkning av tillgångsdimensioner.
* Optimerade AEM vid publicering av material till Brand Portal.
* Korrigerar resurstypsvärdet i Canvas-noden.
* Aktiverade funktioner för skiftlägeskänslig sökning och sökning av specialtecken för dokumentfragmentinnehåll.
* Förbättrad adaptiv Forms för att bifoga PDF som bilagor i Safari.\
   Tillhandahåller en ny Dynamic Media som ansluter till den nya Dynamic Media Publishing Infrastructure för snabbare och mer skalbar replikering.

### Resurser {#assets-10}

* AEM Assets kan inte extrahera underresursreferenser för InDesign-resurser. De innehåller dubblettlänkar till resursen. NPR-19006: Programfix för CQ-4204186
* Sorteringsalternativet fungerar inte för resurser i samlingen under Commerce. NPR-19508: Programfix för CQ-4213622
* När en resurs med samma namn som en befintlig resurs flyttas till samma plats, blir värdet för cq: lastReplicationAction för resurserna växlas mellan dem vilket skapar fel metadata. NPR-19531
* Ett felmeddelande visas när ett stort antal resurser publiceras trots att alla resurser har publicerats korrekt. NPR-19629: Programfix för CQ-4219611
* Statiska återgivningar visas med fasta dimensioner och återspeglar inte storleken på den faktiska återgivningen. NPR-20004
* AEM blir trög när flera resurser (fler än 4) publiceras till Brand Portal. NPR-2009

### Webbplatser {#sites-10}

* AEM visar ett oväntat beteende när en användare försöker publicera/avpublicera/skapa en version av en sida som är låst av en annan användare. NPR-19249; Programfix för CQ-4215298 och CQ-4203856
* När du befordrar den kapslade starten manuellt tas den underordnade sidan bort. NPR-19704
* Persistensproblem när ContextHub lagrar överskrivningar av standardlager för beständighet under initieringen. NPR-19979: Programfix för CQ-4218399
* Innehållsfragment överlappar andra knappar. NPR-19980: Programfix för CQ-4221519
* Webbplatssidan visas inte när den visas med alias i SiteAdmin. NPR-20053: Programfix för CQ-4221478
* Fel vid publicering av en Live Copy-sida som pekar på en importsida i Adobe Campaigns. NPR-2006: Programfix för CQ-4220846

### Plattform {#platform-8}

* Uppgraderade Apache POI till version 3.16 som stöd för inkludering av bakgrundsbilder av PPT-bilder i renderingar. NPR-18286
* Återgivningsproblem med Internet Browser 11 och Edge när flera resurser överförs till samma mapp. NPR-20062

### Integrering {#integration-11}

* Anpassad at at.js-fil publiceras inte när den används av den anonyma användaren. NPR-19542: Programfix för CQ-4219592
* Migrerar befintliga autentiseringsuppgifter för Analytics till WSSE Authentication. NPR-19962

### Brand Portal {#brand-portal}

* Aktivera publiceringstaggar från AEM till Brand Portal från tagadmin/tagging-konsolen. NPR-20271

## Forms {#forms-11}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

### Forms tilläggspaket {#forms-add-on-package-11}

#### Korrespondenshantering {#correspondence-management-4}

* Aktiverade funktioner för att söka efter faktisk text i dokumentfragment när en bokstav förhandsgranskas. NPR-19712

#### Adaptiv Forms {#adaptive-forms-8}

* Förbättrad adaptiv Forms för att bifoga PDF som bilagor i Safari. För att ha stöd för samma funktioner i befintliga formulär måste vi göra ändringen i konfigurationen i widgeten för bilagor och i&quot;Filtyper som stöds&quot; uppdatera värdet application/pdf i stället för .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* Om validationState är odefinierad i ett fält med adaptiv form och elementFocusChanged-händelsen inträffar, returneras en error-händelse (errorState) till Adobe Analytics-servern. NPR-19513

### Forms JEE Installer {#forms-jee-installer-11}

#### Core {#core-3}

* Anslutningshanteraren är inte tillgänglig under avstängning. Jboss tar bort JDBC-beroendet innan författaren EAR tas bort från distributionen vilket kan orsaka korruptionsproblem. NPR-19703

## Inkluderade funktionspaket {#feature-packs-included-1}

* Korrigering av miniatyrbilder och förbättrad genomskinlighet i Dynamic Media. NPR-15207

## OSGI-paket och innehållspaket som ingår i CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lista över innehållspaket som uppdaterats i AEM 6.2SP1-CFP9

[Hämta fil](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lista över OSGi-paket som uppdaterats i AEM 6.2SP1-CFP9

[Hämta fil](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Nu finns taggar för anpassade användarmallar i Adobe e-postmalltjänst.
* Förbättrade TouchUI-knappar i skrivbordsappen.
* Inaktiverad skicka-knapp vid klickning för att förhindra att flera formulär skickas på en översättningssida.
* Konfigurerade flera RTE-komponenter i en dialogruta.
* Förstärkt ReferenceUpdates in live copy.
* Aktiverade skiftlägeskänsliga sökfunktioner för dokumentfragmentinnehåll.
* En lista över Linux-bibliotek har lagts till i AEM Forms installationsdokumentation.

### Resurser {#assets-11}

* Problem med att använda Omnissearch-filtret på smarta samlingar i webbläsaren Safari. NPR-19511
* PDF-nyckelordsmetadata extraheras och ändras inte korrekt när flera nyckelord är associerade med en PDF-resurs. För att lösa problemet har metadataegenskapen för ämnesfältet tagits bort för PDF-resurser. Du kan emellertid redigera metadatarammet och lägga till ett textfält med flera värden för ämnesfältet. NPR-19126
* Tjänsten för arbetsflödesmeddelanden kodar inte länkarna i e-postmeddelanden, vilket förhindrar att de läses in efter att användarna har klickat på dem. NPR-19490: Programfix för CQ-4218055
* Det går inte att läsa in en fullständig lista med sidor/resurser i kolumnvyn med Chrome. NPR-19458: Programfix för CQ-4214248
* Felaktig ikon för fråntid visas i AEM inkorg när arbetsflödet&quot;Begär aktivering&quot; aktiveras. NPR-19365: CQ-4216174
* Problem med sortering i listvyn. NPR-19217: CQ-95602
* När du ändrar titeln eller miniatyrbilden i Resursmappsinställningar åsidosätts mappens ursprungliga grupp och behörigheter. NPR-19283: Programfix för CQ-4216080
* Windows 10-arbetsstationer växlar automatiskt till pekskärmsläge och inaktiverar vissa av knapparna. NPR-19183

### Webbplatser {#sites-11}

* Problem med att ha flera RTE-komponenter i en dialogruta. NPR-19311: NPR-19587
* Automatisk versionsrensning i vanilj AEM 6.2 fungerar bara en gång efter att VersionManagerImpl har initierats. NPR-19315: Programfix för CQ-4217175
* Arbetsflödesinstansen fastnar i arbetsflödessteget&quot;Salesforce.com Export&quot;. NPR-19222: Programfix för CQ-4212976
* Språkkopior av sidor som skapats från live-kopior går inte att redigera. NPR-18967
* ReferencesUpdateAction uppdaterar inte länkar till en kapslad LiveCopy med hierarkiändring. NPR-18715: Programfix för CQ-4214105

### Plattform {#platform-9}

* Tjänsten Adobe Email Template lägger till taggar i anpassade användarmallar. NPR-19190: Programfix för CQ-4217113

### Projekt {#projects-2}

* Projektredigerare kan inte kopiera/klistra in resurser i projektresursmappen. NPR-19619
* Det går inte att generera förhandsgranskning för översättningsprojekt efter installation av 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integrering {#integration-12}

* Åtkomstegenskaper för artiklar som inte har angetts korrekt i Adobe Digital Publishing Solution för Classic UI. NPR-19366
* Smidig återgivning av miniatyrbilder på grund av artiklar i full storlek i AEM artikelkonsol. NPR-19086: CQ-4217148
* Felaktigt beteende för automatisk vikning vid personalisering av erbjudanden via Campaign om användarna har tillgång till flera områden. NPR-19290: Programfix för CQ-4218029
* Måldialogrutan visas inte i målinriktningsläge när en målmodul redigeras och du sparar mer än en gång. NPR-19144: Programfix för CQ-4216708

### Arbetsflöde {#workflow-2}

* Användare kan inte filtrera meddelanden i Inkorgen efter användare/grupp i Inkorgen Classic UI. NPR-19122: Programfix för CQ-4215374
* Bildschemat behåller inte markerade koordinater i HTML-bildkomponenten. NPR-18911: CQ-4211584

## Forms {#forms-12}

* AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-12}

* När innehåll kopieras från Microsoft Word eller en webbläsare till textredigeraren för korrespondenshanteraren går formatet förlorat. NPR-19530
* Innehåll utan radbrytning i textredigeraren radbryts inte. NPR-19481
* Aktiverade funktioner för att söka efter faktisk text i dokumentfragment när en bokstav förhandsgranskas. NPR-17792: Programfix för CQ-4214501

#### Korrespondenshantering {#correspondence-management-5}

>[!NOTE]
>
>Den här sökfunktionen för textfragment har vissa begränsningar:-
>
>* Dokumentfragmentinnehåll är skiftlägeskänsligt och titlar är inte skiftlägeskänsliga.
>* Sökresultaten markeras inte när en del av det sökda ordet har en annan stil eller innehåller specialtecken som &quot; eller &quot; eller \&quot;.
>* Sökfunktionen fungerar inte för dynamiskt innehåll (som elementvärden i dataordlistan eller variabelvärden) i dokumentfragmentet.


#### Forms Manager {#forms-manager-2}

* Det går inte att redigera XML-schemaegenskaper för Adaptiv Forms efter användning av CFP6 på AEM 6.2. Programfix för CQ-4219684
* Alla tjänster i AEM Forms Manager-kärnpaketet startas inte när servern startas om. Programfix för CQ-4217014

### Forms JEE Installer {#forms-jee-installer-12}

#### Installera LCM {#install-lcm-2}

* Administratörsskärmen i Microsoft Windows visar version 6.0 efter installation av CFP6. Programfix för CQ-4217573

## Inkluderade funktionspaket {#feature-packs-included-2}

* Förbättrade TouchUI-knappar i skrivbordsappen. NPR-18676

## OSGi-paket som ingår i CFP8 {#osgi-bundles-included-in-cfp}

Lista över OSGi-paket som uppdaterats i AEM 6.2SP1-CFP8

[Hämta fil](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lista över innehållspaket som uppdaterats i AEM 6.2SP1-CFP8

[Hämta fil](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Beteendeändring i visning av titlar på bildkort för Image having DC: title-egenskapen är inställd på String [] (multifield).
* Korrigeringar i prestandaproblem med Dynamic Media-Cloud Services, gränssnittsgränssnitt för pekskärmar och säkerhetsgränssnitt.
* Korrigeringar i Apache Felix Http Bridge 3.0.8
* BLR (Binary-less Replication) mellan författar- och publiceringsmiljön har lösts.
* Stöd för målbiblioteksfilen AT.JS, ett implementeringsbibliotek för integrering på klientsidan med Adobe Target som är utformat för både vanliga webbimplementeringar och enkelsidiga program.
* Förbättrade AEM prestanda genom att införa en tidsgräns för användarkonfigurerad anslutning för Marketing Cloud-lösningar (Analytics, DTM, Target och S&amp;P).

### Resurser {#assets-12}

* När videoimporten testas med AEM 6.3 konfigurerad med Dynamic Media-Cloud Services, genereras ett undantagsfel av typen &quot;För många öppna filer&quot;. NPR-18734; Programfix för CQ-4211407
* Vanity URL-inställningen för resurser på en sida fungerar inte efter att AEM startats om. NPR-18634; Programfix för Granite-18085
* I TouchUI visas knappen Publicera för användare utan behörighet att publicera resurser. NPR-18620; Programfix för CQ-4214042
* Alternativet för dynamisk återgivning finns inte i hämtningsdialogrutan för en mediefil när licensavtalet har ställts in för den. NPR-18607; Programfix för CQ-4212342
* Dynamisk återgivning kan inte hämtas för resurser som innehåller blanksteg i sina namn. NPR-18571; Programfix för CQ-4211738
* Det går inte att spara mer än en användare när resursmappen delas med Creative Cloud. NPR-18489; Programfix för CQ-103297
* dc: title &amp; dc: beskrivningen ändras inte till ett flerfältsvärde i crx/de. NPR-18474; Programfix för CQ-4209086
* Åtgärden Flytta resurser orsakar prestandaförsämring. NPR-18346
* Inga objekt visas i tidslinjen när den öppnas med standardalternativet Visa alla. NPR-18302; Programfix för CQ-4211957
* Ett fel inträffar när en ASCII/UTF-8-kodad textfil överförs till AEM Assets och genereringen av miniatyrbilder misslyckas. NPR-18006: CFP för CQ-4209345
* Åtgärdsknappar för publicering visas även när användaren inte har åtkomst till repliken. NPR-17353; Programfix för CQ-4209269
* Både platsadmin och Miscadmin fungerar inte när minification är aktiverat med min:gcc;obfuscate=true. NPR-18593; Programfix för CQ-4209220
* Anpassade menyalternativ visas inte förrän skärmen uppdateras varje gång. NPR-18500 Programfix för CQ-4213581
* Uppgradera stund.js till 2.10.6. NPR-18596; Programfix för Granite-11881
* Använd behörigheter för DM-makron för att dela upp vy för Admin-användare. NPR-18544; Programfix för CQ-4211729
* Publicera senare för resurser genererar ett otillåtet ArgumentException. CQ-4214532

### Webbplatser {#sites-12}

* På ett aktivt/aktivt författarkluster med MongoDB försöker båda författarna utlösa replikering för samma innehåll när tiden når den angivna tiden för innehållet. NPR-18708; Programfix för CQ-4210982
* NPE när en resurs flyttas med en referens som inte har jcr: innehållsnod. NPR-18664
* Platshållare visas inte på en sida som innehåller flera parsyskomponenter. NPR-18645; Programfix för CQ-110253
* Samtidighetsproblem i AbstractCopyMoveCommand. NPR-18591
* När du kopierar text till en parsys-komponent från en annan AEM skapas parsys utan någon resourceType-uppsättning. NPR-18511; Programfix för CQ-4212306

### Plattform {#platform-10}

* JCR-installationsprogrammet uppdaterar inte paketversionen efter paketinstallationen. NPR-18728; Programfix för NPR-15135
* BLR (Binaryless Replication) fungerar inte med binärfilerna för författar- och publiceringsmiljön. NPR-18704
* Apache Felix Http Bridge - begäran om upplösning i AEM. NPR-18297
* Replikeringen misslyckas när flera sidor med en liknande struktur replikeras samtidigt med Sling Content Distribution. NPR-18665; Programfix för Granite-13712
* Sling-distributionspaket byggs upp och är inte självrensade. NPR-18601; Programfix för Granite-16183

### Integrering {#integration-13}

* Om du visar erbjudanden som publicerats från biblioteksmappar blir resultatet NPE. NPR-18732; Programfix för CQ-4214593
* Start-/slutdatumet för en aktivitet uppdateras inte i JCR och Target när det ändras från ett specifikt datum till&quot;Vid aktivering/inaktivering&quot;. NPR-18612; Programfix för CQ-104831
* Analysintegreringen med AEM har inga anslutnings- eller sockettidsgränser angivna för httpclient-anslutningarna. NPR-18497
* DTM-integreringen med AEM har inga anslutnings- eller sockettidsgränser angivna för httpclient-anslutningarna. NPR-18495
* Målintegreringen med AEM har inga anslutnings- eller sockettidsgränser angivna för httpclient-anslutningarna. NPR-18494
* Integreringen av Sök och Befordra med AEM har inga anslutnings- eller sockettidsgränser angivna för httpclient-anslutningarna. NPR-18493
* Målaktiviteten inaktiveras när en extra upplevelse har lagts till. NPR-18227; Programfix för CQ-4201895

### WCM-Foundation-komponenter {#wcm-foundation-components-7}

* Bildscheman behåller inte markerade koordinater i HTML-bildkomponenten. NPR-18530; Programfix för CQ-4211584

### Översättning {#translation-5}

* Översättningssökresultaten innehåller inte namn på översättningsprojekt. NPR-18224; Programfix för CQ-4210658

### Brand Portal {#brand-portal-1}

* Aktivera publiceringstaggar från AEM till Brand Portal från tagadmin/tagging-konsolen. CQ-4212165

## Forms {#forms-13}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-13}

#### Korrespondenshantering {#correspondence-management-6}

* Korrekta data visas inte på redigeringspanelen förrän fragmentet sparas. NPR-19092
* Det tar lång tid att lägga till dokumentfragment i ett brev. NPR-18958
* Om det finns en XML-deklaration i en XML-datafil och teckenåtergivningen initieras via en POST-begäran, visas inte data med motsvarande bokstav. NPR-18870
* Inga granskningsloggar genereras för åtgärder som utförs på CM-resurser. NPR-16618

>[!NOTE]
>
>Installera inte detta CFP-tilläggspaket om du påverkas av följande två problem:
>
>* Kopiera Klistra in från Word/webb till CM-textredigeraren visar radbrytningsinnehåll. NPR-19530
>* Innehåll utan radbrytning i CM-textredigeraren radbryts inte. NPR-19449

>
>Dessa skulle tas upp i den framtida gemensamma fiskeripolitiken.

#### Adaptiv Forms {#adaptive-forms-9}

* När du lägger till en ny panel för repeterbara paneler tas värdet för listrutan i den föregående panelen bort. NPR-18772
* Anpassningsbara formulärfält som markerats för att endast acceptera heltal accepterar även ett fåtal specialtecken från det numeriska tangentbordet. NPR-18680
* Skript för att ändra knappens titel vid händelsen initialize på guideroot-panelen fungerar inte. NPR-18476
* Rullningslisten visas inte på den högra panelen för regler som har skapats med regelredigeraren. NPR-18716

#### AEM Forms App {#aem-forms-app}

* Forms återges inte korrekt i AEM Forms App när det är i offlineläge eller inte är anslutet till nätverket. CQ-4218368

### Forms JEE Installer  {#forms-jee-installer-13}

#### PDFG-tjänst {#pdfg-service-3}

* PDF Generator kan inte skapa PDF-dokument med angivna bokmärkesnivåer. Programfix för CQ-4211102

## OSGi-paket som ingår i CFP7 {#osgi-bundles-included-in-cfp-1}

Lista över OSGi-paket som uppdaterats i AEM 6.2SP1-CFP7

[Hämta fil](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lista över innehållspaket som uppdaterats i AEM 6.2SP1-CFP7

[Hämta fil](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Effektiv hantering av dolda komponenter i layoutläge på surfplattor.
* Vi presenterar snabbfunktioner på hybridenheter.
* Löser problem med synkronisering på komponentnivå med live-kopior.

### Resurser {#assets-13}

* Kunden blockeras när en användare som inte har den behörighet som krävs försöker flytta en åtgärd för en resurs. NPR-18330; Programfix för CQ-4212560
* Om du sammanfogar flera konfigurationer av smarta innehållstjänster uppstår ett användbarhetsproblem. NPR-18273; Programfix för CQ-4201557
* Utcheckningsåtgärd/Arbetsflöden är inte tillgängliga från tidslinjekonsolen när de är ca. 80 fragment läggs till i resursmappen. NPR-18257; Programfix för CQ-4211214 och NPR-18251. Programfix för CQ-4211216.
* Systemet kraschar vid slut på minne och sidnumrering saknas under Assets-rapporter. NPR-17865; Programfix för CQ-4209759
* Den publicerade videon kan inte spelas upp på den kodade videoresursen. NPR-17849; Programfix för CQ-4210739
* Miniatyrbild för PDF genereras inte. NPR-17831, NPR-17750. Programfix för CQ-4210547
* Utgångna mediefiler inaktiveras inte av Adobe CQ DAM-förfalloaviseringsjobb. NPR-17666; Programfix för CQ-107766
* Resursernas förfalloaktiviteter avbryts om en tillgång inte har en tilldelad ägare. NPR-17665; Programfix för CQ-4197946
* Ett null-pekarundantag genereras när en resursmapp med fler än 150 inkommande referenser flyttas. CQ-4200981

### Webbplatser {#sites-13}

* Personalisering fungerar bara för den första IP-adressen när segmenteringsregeln har angetts för ett IP-intervall. NPR-18121; Programfix för CQ-83767
* Inloggningen misslyckas på grund av NumberFormatException när egenskapen historyShow är aktiverad. NPR-18073; Programfix för CQ-101965
* Borttagna sidor som är markerade visas i Touch UI. NPR-18025; Programfix för CQ-86694
* Prestandaproblem vid inläsning av en sida med stora (2 000+) målgrupper. NPR-17884; Programfix för CQ-4209567
* Det går inte att markera en bild efter att ha tagit bort en annan bild på sidan. NPR-17711; Programfix för CQ-4201323

### Plattform {#platform-11}

* Användargränssnittskontroller för pekfunktioner är inte dolda för användare som inte har de behörigheter som krävs. NPR-17945; Programfix för CQ-4211231
* Japanska taggar saknas i taggväljarfältet. NPR-17768; Programfix för CQ-4210456
* Frågan getsize() returnerar felaktiga resultat när FastQuerySize är aktiverat. NPR-18018
* Webbkonsolen i standby-instansen är inte tillgänglig. NPR-17861; Programfix för Granite-14582

### Handel {#commerce-2}

* Frågetraversering sker när katalogutkast inte har något villkor definierat för ett avsnitt. NPR-18229; Programfix för CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. fördröjningar AEM avstängning. NPR-18298; Programfix för CQ-96133

### Integreringar {#integrations}

* Löste AEM sökkomponentfel som kan inträffa när AEM Day HTTP Client 3.1 OSGI har konfigurerats med en proxy som kräver sammanfattningsautentisering. NPR 18128
* Kryssruta saknas för att återställa arv. NPR-17753; Hotfix-begäran för CQ-4210139
* Användarna kan inte ange prioriteten när de riktar sig till en komponent med flera aktiviteter. NPR-18658; Programfix för CQ-4210727
* Användare kan inte bläddra i mappen /etc/segmentation för att välja en målgrupp som skapats under mappen /etc/segmentation/group1. NPR-18522

### Dokumentskydd {#security-1}

* Guiden Flytta resurs låser sig om användaren inte har skrivbehörighet för målmappen. NPR-18300
* Begär att en uppgraderad version av org.apache.sling.servlets.post servelet (2.3.22) i API:t för Apache Sling ska användas för att förhindra en XSS-säkerhetslucka. NPR-18963

### Översättning {#translation-6}

* Resurssidan får inte skickas igen till ett översättningsprojekt förrän projektet har slutförts. NPR-18249; Programfix för CQ-4209908

### WCM-Foundation-komponenter {#wcm-foundation-components-8}

* Det går inte att använda WCM Foundation iparsys-komponenten i redigerbara mallar. NPR-18223; Programfix för CQ-4210384
* Bildschemat behåller inte markerade koordinater i HTML-bildkomponenten. NPR-18032; Programfix för CQ-4211584
* När en HTML-bildkomponent återges får webbadressen ett nytt namn som orsakar en skadad URL. NPR-17908; Programfix för CQ-4211587
* Det går inte att avsluta Sidegenskaper efter att ändringarna har gjorts. NPR-17832; Programfix för CQ-96110

## Forms {#forms-14}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i [AEM Forms Releases](aem-forms-releases.md).

### Forms tilläggspaket {#forms-add-on-package-14}

**Korrespondenshantering**

* Dataordlistan läses upprepade gånger under bokstavsåtergivning. NPR-18482, programfix för CQ-4210805
* JavaDocs har lagts till för klassen com.adobe.livecycle.content. NPR-18467
* Beskrivningen av brevet sparas inte när en bokstav skapas. NPR-18039
* När en textmodul sparas och ett uttryck i textmodulen inte innehåller inledande eller avslutande uttryckstaggar, visas inget felmeddelande. Textmodulen visar ett felmeddelande och kan inte återges i brevet. NPR-17798
* Oväntade fel i loggar vid installation av tilläggspaket. NPR-18295

**Forms Manager**

* I AEM Forms-gränssnittet visas alla resurser i den äldsta första ordningen. Användarna kan inte ändra ordning på resurserna i den senaste första ordningen. NPR-18451

### Forms JEE Installer  {#forms-jee-installer-14}

**Utdatatjänst**

* Förbättrat prestandaproblem i Output Service för AEM 6.2. NPR-18033

**Signaturtjänst**

* Det går inte att signera ett PDF-dokument med en fjärrmodul för maskinvarusäkerhet. NPR-18017

## OSGi-paket som ingår i CFP6 {#osgi-bundles-included-in-cfp-2}

Lista över OSGi-paket som uppdaterats i AEM 6.2SP1-CFP6

[Hämta fil](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lista över innehållspaket som uppdaterats i AEM 6.2SP1-CFP6

[Hämta fil](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Löste flera gränssnittsproblem med delning, flyttning, publicering och hämtning av resurser.
* Ökad kapacitet för dialogrutan Flytta när refererade resurser visas.
* Löste flera problem med WCM-komponenter och arbetsflöden, som Unpublish och Version Renge.
* Åtgärdsfältets svarstider har förbättrats när det gäller att visa verktygsfältsåtgärder och Coral-komponenter.

### Resurser {#assets-14}

* Prestandaförbättringar för publicering till Brand Portal. NPR-17189; Programfix för CQ-4204150
* När du delar en resurs med alternativet Dela länk skapas ingen zip-fil med en platt mappstruktur för hämtning. NPR-17513; Programfix för CQ-4209381
* Om du markerar en resurs i DAM och klickar på Publicera visas inte alternativet Publicera till Brand Portal på sidan Resursinformation. NPR-17351; Programfix för CQ-94905
* I DAM-arbetsflödessteg måste binära strömmar som hämtas från Session eller ResourceResolver stängas i ett slutligt block för att säkerställa att inga resursläckor inträffar. NPR-17385; Programfix för CQ-4209452
* Om du överför ett Word-dokument i DAM genereras ett null-pekarundantag och arbetsflödesinstansen förblir fast i körningsläget. NPR-17160; Programfix för CQ-4207358
* Knapparna Dela, Flytta, Publicera och Hämta visas för resurser som har upphört att gälla på sidan Metadataredigeraren för användare som inte är administratörer. NPR-16903; Programfix för CQ-101440/CQ-104535
* Åtgärder som Dela, Flytta, Publicera och Kopiera ska vara synliga för administrativa användare i resurskonsolen. NPR-16902; Programfix för CQ-4207111

### Webbplatser {#sites-14}

* När du flyttar en sida med hjälp av Classic och Touch UI visas inga referenser längre än 150 i dialogrutan Flytta, vilket gör att användarna inte kan uppdatera referenserna och publicera sidan på nytt. Problemet har åtgärdats genom att en egenskap för Classic UI har introducerats: &#39;maxRefNo&#39; som kan konfigureras på platsadminnoden: &#39;/libs/wcm/core/content/siteadmin&#39;. This property specifies maximum number of references (default value 150) that is displayed before a tung move operation and if a page has more number of references, they are not shown in the movePage dialog. Den här konfigurationen fungerar även för admin och feladministratör genom att tillämpa konfigurationen på noderna: `'/libs/wcm/core/content/damadmin'` och `'/libs/wcm/core/content/miscadmin'`. NPR-17222; Programfix för CQ-85878

* När du arbetar med WCM-komponenter tas hyperlänkar med mellanslag bort i redigeraren för RTF-text i Touch UI. NPR-17698, NPR-17570. Programfix för CQ-4206768
* JavaScript-fel visas för användare utan replikeringsrättigheter när arbetsflödet för begäran om borttagning av publicering aktiveras från sidegenskaper. NPR-17294; Programfix för CQ-102064
* Om du återger eller exporterar en HTML-bildkomponent ändras URL:en till ett nummer och filnamnet ändras, vilket orsakar brutna länkar. NPR-17245; Programfix för CQ-59616
* Om du tar bort en start i en kapslad start blir delstarterna överblivna. NPR-17228; Programfix för CQ-4202639
* Om du kör tömning av version i AEM 6.2 med Oak 1.4.13 aktiverat får du en konstant upprepad varning i loggarna. NPR-17391; Programfix för CQ-4206870
* När du har installerat en snabbkorrigering eller en uppgradering för ContextHub-komponenten skriver innehållspaketet över alla segment i /etc/segmentation/contexthub, vilket resulterar i en förlust av alla anpassade ContextHub-segment. NPR-17250; Programfix för CQ-79958
* När du kör ett arbetsflöde med kapslade grupper som arbetsflödesanvändare låser WorkflowStatusProvider (pageinfo.json) arbetsflödesinstansen. NPR-17555; Programfix för CQ-4202056
* När du använder WCM-Page Editor-komponenterna finns det ett mycket tomt utrymme i slutet av sidan i redigeringsläget för Touch-gränssnittet i författarinstansen. NPR-17510; Programfix för CQ-4205441
* Om du återger eller exporterar en HTML-bildkomponent ändras URL:en till ett tal, vilket orsakar brutna länkar. NPR-17245; Programfix för CQ-59616

### UI {#ui}

* När du väljer en resurs och klickar på Utvecklarverktyg visas inte alltid verktygsfältets åtgärder i åtgärdsfältet i långsamma anslutningar och sidan måste läsas in igen. NPR-17568; Programfix för CQ-108365
* Åtgärdsfältet bör uppdateras så att två behållare används: coral-actionbar-primary och coral-actionbar-secondary, istället för coral-actionbar-container. NPR-17591; Programfix för GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Användare med skrivbehörighet för AEM Mobile kan inte förhandsgranska innehåll från AEM Mobile Content Management-sidan. NPR-17390; Programfix för CQ-4209690

### Dokumentskydd {#security-2}

* XSS-sårbarhet i utdata som genererats av HTMLRendererServlet. NPR-17136
* Begäran om att förhindra AEM i webbsyndikeringsfeeds på AEM. NPR-16219

### Forms {#forms-15}

#### Forms tilläggspaket {#forms-add-on-package-15}

AEM Forms-korrigeringar levereras via tilläggspaket och andra patch-installerare som medföljer releasen. Mer information finns i AEM Forms Releases.

**Adaptiv Forms**

* För ett anpassat formulär med en bifogad fil skapas dubblettposter för afSubmissionInfo-taggar i den skickade XML-filen när formuläret skickas för andra gången. NPR-17364
* När du använder webbläsaren Google Chrome genereras ett fel när du har tagit bort en bifogad fil från ett formulär och försöker bifoga den igen. NPR-17297
* Om det finns kapslade, repeterbara, lazy loaded-paneler i XSD-baserade eller No-Form-modellbaserade adaptiva Forms, behålls inte värden som fyllts i formuläret i DOR (Document of Record). NPR-17176
* Fel som visas i felloggen för Regelredigeraren ska läggas till i catch-blocket för JavaScript-koden för try/catch-blocket. NPR-16757
* Om du klickar på en bifogad fil i ett formulär uppstår ett webbläsarkonsolfel och förhandsgranskningen av den bifogade filen visas inte. NPR-17174

**Korrespondenshantering**

* Gränssnittet Skapa korrespondens bryts om textbunden text eller en tom rad läggs till i användargränssnittet. NPR-17748
* Webbläsaren flimrar när ett brev öppnas för redigering. NPR-17576
* När du lägger till fjärrfunktioner i element i en beräknad dataordlista visas inte rullningslisten på fliken om antalet funktioner är större än längden på fliken med fjärrfunktioner. NPR-17359
* API-metoden import com.adobe.icc.services.api.LetterInstanceService fungerar inte. NPR-17922, NPR-16008
* En variabel som läggs till i en textmodul visas inte i panelen Databindning när du redigerar en bokstav. NPR-17940
* Gränssnittet för korrespondenshantering startar inte när HTML-överföringsåtgärden använder metoden POST. NPR-17595

**Forms Manager**

* Om du har konfigurerat ett adaptivt formulär för AB-testning startas inte testet när du klickar på Start AB Testing och ett fel uppstår i webbläsarkonsolen. NPR-17838

**Forms Service**

* De problem som rapporteras i den statiska kodanalysen av OSGI-formulär bör åtgärdas. NPR-13951

#### Forms JEE Installer {#forms-jee-installer-15}

**Utdatatjänst**

* Att använda AEM formulär 6.2 Output Service för att sammanfoga ett specifikt formulär med data-XML tar 20 gånger mer tid jämfört med den tid som LiveCycle ES4 SP1-servern tar för samma åtgärd. Den har åtgärdats i Windows- och Linux-miljöer. NPR-17501

**Installera LCM**

* När du har installerat AEM Forms 6.2 GM build och tillämpat AEM 6.2 CFP, visas ett oönskat semikolon i versionsinformationen när du kör LiveCycle Configuration Manager och korrigeringsinstallationsdatumet uppdateras inte. NPR-14322

**Processhantering**

* Variabeln TaskContext är inte ifylld för AEM Forms-processer. CQ-4211857

#### AEM Forms JEE Bundles Package {#aem-forms-jee-bundles-package}

* Funktionerna för formuläranvändare, oavsett om de använder JEE Admin UI-konsolen eller OSGi-konsolen, bör vara desamma. NPR-17670

### Funktionspaket som ingår i CFP5 {#feature-packs-included-in-cfp}

**Forms JEE Package**

Processhantering - HTML-arbetsyta

* När du tilldelar ett arbetsytans steg bör fliken Bifogade filer i arbetsytan visa en räknare för de bifogade filerna eller anteckningarna om det finns fler än en bifogad fil eller anteckning. NPR-17771
* Begäran om stöd för Office 365 i AEM JEE Forms för e-postfunktioner i formulärarbetsflödet. NPR-13866

**Forms tilläggspaket**

Korrespondenshantering

* När du redigerar fragment i textredigeraren under en förhandsgranskning av en bokstav bör den bearbetade texten visas för redigering i stället för de infogade villkor som används i fragment. NPR-15748, NPR-17504

### OSGi-paket som ingår i CFP5 {#osgi-bundles-included-in-cfp-3}

Lista över OSGi-paket som uppdaterats mellan AEM6.2 SP1-CFP5

[Hämta fil](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lista över innehållspaket som uppdaterats mellan AEM6.2 SP1-CFP5

[Hämta fil](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 är en viktig uppdatering som innehåller viktiga kundkorrigeringar som släppts sedan den allmänna tillgängligheten av AEM 6.2 SP1.

Huvudinnehållet i det här Cumulative Fix Pack är:

* Korrigeringar i resurser för Camera Raw filåtergivning, tidslinjevy och bildorientering
* Förbättringar i

   * WCM startar för webbplatser
   * Projektarbetsflöde
   * ContextHub-komponenter

* Korrigeringar för Campaign, Mobile on-demand och Translation
* Förbättrad användbarhet i anpassad formulärregelredigerare
* Förbättrad redigerare för infogade villkor för korrespondenshantering i formulär
* Processhantering och programfixar för AEM på JEE
* Forms Designer-relaterad korrigering för skriptredigeraren

### Plattform {#platform-12}

* Sökformuläret för Search &amp; Promote ignorerar inställningen `environment` när molntjänsten har konfigurerats, vilket gör det oanvändbart på författarinstansen. NPR-16594: Programfix för CQ-4206076
* Det går inte att lägga till eller anpassa kolumner i **Resurser OmniSearch**-resultaten genom att täcka över dem i /apps. NPR-16737: Programfix för CQ-4206785
* **Diagnosverktyget **page fungerar inte efter en uppgradering på plats från AEM 6.1 SP2 till AEM 6.2 SP1. NPR-17121; Programfix för CQ-4196786
* HTML: När du väljer ett forum, skapar ett ämne och ett inlägg lägger `Sightly SightlyCompiledScript` till en felaktig `addSelectors`-egenskap till `RequestDispatcherOption`. NPR-17008: Programfix för GRANITE-16384

* Stöd för `CRON expressions` har lagts till i `ManagedPollConfigs` som används av `ReportImporter`. NPR-16608: Hotfix-begäran för CQ-4206066

* Det går inte att överföra en avatarbild för en LDAP-användare. NPR-16561; Programfix för Granite-17013
* Antalet resultat som visas på skärmen för användarhantering skiljer sig åt i kort- och listvyn. NPR-16241; Programfix för GRANITE-16914
* Arbetsflödesmeddelanden läses inte in på ett lat sätt när du visar i webbläsaren Google Chrome i helskärmsläge. NPR-17013: Programfix för CQ-4207567

### Resurser {#assets-15}

* Bildorienteringen används inte korrekt när du importerar en bild med en definierad orientering. NPR-16750: Programfix för CQ-4204356
* Resursernas tidslinjevy visar inga resurser trots att Visa alla är inställt som standard. NPR-16957: Programfix för CQ-98780
* Camera Raw-filer (inklusive ARW, CR2, NEF, DNG och EPS) kan inte markeras eller tas bort när de läggs till som återgivning i resurser. Sådana filer hämtas automatiskt när användaren klickar på dem. NPR-16949: Programfix för CQ-4206846
* När du skapar en PDF-fil i en annan PDF-fil i resursgränssnittet visas inte de skapade PDF-filerna i DAM-gränssnittet, trots att de är synliga i crx-databasen. NPR-16833: Programfix för CQ-4206501
* Ett problem uppstår om du överför en resurs som en direkt underordnad nod till sig själv med Touch-gränssnittet. Resursen överförs som ett direkt underordnat objekt till den tidigare valda resursen. NPR-16534: Programfix för CQ-4204287
* Kommentarer om en resurs och taggning av en användare i kommentaren i DAM-gränssnittet genererar inget e-postmeddelande. NPR-16589: Programfix för CQ-102318

### Projekt {#projects-3}

Arbetsflödeskonsolen för projekt visar ett NullPointerException på sidan när arbetsflöden rensas. NPR-17017: Programfix för CQ-4194269

### Webbplatser {#sites-15}

* Filer i `ContextHub` minimeras inte för författarinstansen. NPR-17022: Programfix för CQ-79456
* Starthöjningen WCM-Launches tar lång tid att marknadsföra en lansering som består av ett stort träd på en sida. NPR-16480: Programfix för CQ-82731
* `ClientContext` Segmentvillkorsåtergivning kraschar när ett segment (eller en målgrupp) skapas med en regel som inte fungerar eller är färdig. NPR-16759: Programfix för CQ-4205104
* I WCM Launches avpubliceras inte sidor som är kopplade till en Launch när åtgärden initieras inifrån sidegenskaperna i Touch-gränssnittet. NPR-16560: Programfix för CQ-4204681
* Link Rewriter skriver felaktigt om href-värden som innehåller ett kolon, förutsatt att kolon &quot;:&quot; definierar ett JCR-namnutrymme. NPR-16753: Programfix för CQ-4203762
* I WCM-Design Importer uppstår problem om en testimportsida öppnas och en ZIP-fil laddas upp och tas bort tidigare. NPR-16486: Programfix för CQ-90962
* Navigering till rutan **[!UICONTROL Global Navigation]** med webbläsarna Safari för Firefox och Google Chrome ger en annan användarupplevelse. Webbläsaren i Firefox visar menyn **[!UICONTROL Tools]** medan webbläsaren i Google Chrome visar menyn **[!UICONTROL Navigation]**. NPR-16770; Programfix för CQ-4200456

### Campaign {#campaign}

* När du testar AEM kampanjmallar och ändrar dirigerade adresser så att de innehåller&quot;Ytterligare data&quot;, försvinner listrutan för Adobe Campaign i Touch-gränssnittets kontextnav. NPR-16771: Programfix för CQ-105748

### Mobil on demand {#mobile-on-demand-3}

* När en preflight-åtgärd tar längre tid än 5 sekunder vid preflight av en publikation från AEM redigeringsmiljö uppstår en ovanlig topp på AEMM - AEM PECS Integration-kontrollpanelen med ett stort antal statusbegäranden per sekund. NPR-16908: Programfix för CQ-4207055
* Konfigurationshanteringen för AEM Mobile misslyckas efter installation av uppdateringen AEM-6.2-SP1-CFP1-1.0. NPR-16909: Programfix för CQ-4204892

### Översättning {#translation-7}

* Förhandsgranskning av översättningsjobb fungerar inte efter installation av 6.2 SP1 - CFP1. NPR-16481; Programfix för CQ-4204655
* Den språkkopia som skapas med Översättning pekar på Överordnad Root i stället för på den lokala landsidekopian. NPR-17257; Programfix för CQ-4208287

### Dokumentskydd {#security-3}

* Ingen MIME-typvalidering utförs när binärfiler överförs till AEM. NPR-16617
* Problem med att överföra avatarbilder för LDAP-användare. NPR-16561

### Forms {#forms-16}

#### Forms tilläggspaket {#forms-add-on-package-16}

**Adaptiv Forms**

* I den adaptiva Forms-redigeraren ska målinställningskommentaren i head.jsp ersättas med den nya satsen Context Hub. NPR-17173
* I den adaptiva Forms-regelredigeraren visar **[!UICONTROL Choose an Item]** händelsen som &#39;null&#39;. NPR-17139
* Det skickade formuläret skickas om när du navigerar framåt med pilen (>). NPR-17080
* När du skickar ett anpassat formulär via AJAX anropas aldrig callback-funktionen error om ett fel uppstår. NPR-17034
* Formuläret sparas inte om du klickar på knappen **[!UICONTROL Save Form]** i regelredigeraren vid körning. NPR-16905
* Statisk text ska uteslutas från tabbordningen i adaptiv form. NPR-16749
* Det beräknade värdet för ett decimalfält visas felaktigt. NPR-16596
* Ikonen för att visa hjälpinnehåll bör finnas med i tabbordningen i adaptiva formulär. NPR-16484
* Stöd för användning av reguljära uttryck av typen `dataRef=C:/Users/`i **[!UICONTROL Default Prefill Service Configuration]** för förifyllda data för Adaptiv Forms. NPR-16425

* Valideringar aktiveras inte korrekt för alla paneler om det finns ett kapslat inläst scenario. NPR-15821

**Korrespondenshantering**

* Letter-återgivningen misslyckas om en bokstav innehåller en tom textmodul (en utan text). NPR-17054
* Radbrytningar och tabbavstånd tas bort från innehållet när de har klistrats in i textredigeraren. NPR-17039
* Visningen av referenser i en textmodul tar lång tid om textmodulen refereras med många bokstäver. NPR-17035
* Det tar lång tid att redigera, spara, ta bort och ange referens för dokumentfragment. NPR-17033
* Justerad text återges i ett annat teckensnitt när du förhandsgranskar bokstaven. NPR-16976
* Sökfunktionen fungerar inte korrekt om den sökta texten innehåller flera förekomster. NPR-16920
* Verktygsfältet för textredigeraren visas då och då i webbläsaren. NPR-16919
* Konstruktionen **[!UICONTROL Save Form]** från Regelredigeraren fungerar inte. NPR-16905
* Listrutan Teckensnitt fyller inte i teckensnittsfamiljen när du skapar en textmodul som är baserad på datamordlista i Internet Explorer. NPR-16944
* När du har skapat ett textfragment ändras bokstavsteckensnittet när du förhandsgranskar brevet. NPR-16830
* Bokstäver med tabbavstånd i början eller mellan uttryck i dokumentfragmentet kan inte återges eller förhandsgranskas. NPR-16769

**Mobile Forms**

* Förhandsgranskning av mobilformulär visar överlappat innehåll, även om formuläret visas korrekt för PDF-återgivning. NPR-17105

**Forms Portal**

* Om du klickar på länken **[!UICONTROL Download]** för ett skickat formulär öppnas en HTML-sida i stället för ett PDF-formulär. NPR-17082

* `Upload Comments` för bifogade filer visas inte i användargränssnittet för skickade instanser, även om de finns i XML-filen som lagras i crx-databasen. NPR-17075

**Tjänsten Reader Extensions**

* En specifik fil är inte Reader Extended AEM OSGI-installation. NPR-16625

#### Forms JEE Installer  {#forms-jee-installer-16}

**Core**

* Under uppgraderingsprocessen misslyckas Configuration Manager med timeout. NPR-16774 (Se [Konfigurera timeout för åtgärder på komponentnivå](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Processhantering - HTML-arbetsyta**

* Startpunkten från en Start-aktivitet börjar inte med de data som skickades när startpunkten skickades. NPR-16917
* Om du klickar på knappen **[!UICONTROL Return]** för ett formulär i HTML-arbetsytan stängs inte formuläret, utan det returneras till gruppkön.\
   NPR-16352

**Processhantering**

* Tillåt användare att ange visningsnamnet för tidigare uppgifter till någon av de följande uppgifterna i en processinstans. NPR-15382

**Utdatatjänst**

* Utdatatjänsten kan inte bearbeta en PDF-fil som har ändrats så att den innehåller ytterligare ett milli-sek-fält i `date-time format`-metadata. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer-skriptredigeraren respekterar inte standardinställningarna för formuläregenskaper för `Calculate Event`och `Validate Event`. NPR-15921

### Funktionspaket som ingår i CFP4 {#feature-packs-included-in-cfp-1}

**Forms tilläggspaket**

* Förbättring i redigeraren för infogade villkor för korrespondenshantering. NPR-10981

### OSGi-paket som ingår i CFP4 {#osgi-bundles-included-in-cfp-4}

Lista över OSGi-paket som uppdaterats mellan AEM 6.2 SP1 och CFP4

De viktigaste nyheterna i CFP3 är:

* Effektivare sökfunktion för Classic UI och AEM Search-komponenten med proxy med sammanfattningsautentisering
* Åtgärdar problem vid överföring av resurser och visning av metadata för resurser
* Åtgärdar problem när mappar och sidor skapas om titeln har specialtecken.
* Korrigeringar för målgruppssynkronisering, publiceringskampanjer och val av målmått i Touch-gränssnittet
* Åtgärdar synkroniseringsproblem för översättningsjobb
* Förbättrad säkerhet för Forms förifyllningstjänst
* Förbättringar av formulärportalutkast och inskickskomponenter samt i Barcoded Forms Service
* Användbarhetsförbättringar för adaptiva formulär som innehåller widgetar för bifogade filer eller lazy loaded fragments.
* Förbättrad användbarhet i Correspondence Management, bland annat förbättrad sökfunktion, loggning av borttagna resurser och import av dataordlistor.

### Plattform {#platform-13}

* Ett konkurrensvillkor i **ModelAdapterFactory**, som är möjligt när två trådar försöker mata in samma fält, resulterar i att modellen inte kan skapas. NPR-16443: Programfix för SLING-6584
* Valideringsalternativ i pakethanteraren för att upptäcka eventuella konflikter mellan överlappande filer (JSP- eller JavaScript-fil) under /apps och den som finns i en hotfix under /libs. Den påverkade övertäckningen kan sedan ombaseras så att den innehåller ändringar från filen under /libs. NPR-16216: Programfix för CQ-81729
* Loggning in the error.log stoppar ibland några sekunder efter att utgivaren startats och måste rensas för att kunna köras igen. Begär att loggningsramverket ska uppdateras och att Sling-loggning ska tillhandahållas. NPR-15913: Programfix för Granite-15452
* Begär att JavaScript-API:t `use"` ska uppdateras för att undvika fel i HTL JavaScript-implementeringen av API:t för användning. NPR-16461: Programfix för SLING-6780

### Webbplatser {#sites-16}

* Efter uppgradering från AEM 6.0 till AEM 6.2 visas det klassiska användargränssnittet långsamt vid sökning av taggar på grund av många frågor. För att lösa problemet kan du följa stegen som anges under [Inaktivera replikeringsstatus i taggkonsolen (klassiskt användargränssnitt)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr). NPR-15842: Programfix för CQ-4201748.

* När du skapar en sida i Touch-gränssnittet kontrolleras inte specialtecknet Apostrof (samma som i det klassiska användargränssnittet) vid inmatningskontrollen för fältet name. Därför kan sidan inte flyttas. NPR-16404: Programfix för CQ-4205321.
* Om du använder olika format på två rader i RTF-redigeraren och sedan sammanfogar dem tas det format som används på den andra raden bort. NPR-16389: Programfix för CQ-4203835.
* Om du försöker klistra in en sida i en sida som inte har några undersidor på skärmen Touch UI Sites fungerar inte det som knappen Klistra in inte visas. NPR-15894: Programfix för CQ-4201696.
* När du bläddrar på fliken Sidor i panelen Innehållssökning visas några uppsättningar sidor i oändlighet i det klassiska gränssnittet, medan Touch-gränssnittet visar en begränsad uppsättning icke-upprepade sidor. NPR-16271: Programfix för CQ-4202371
* När du öppnar Page-Properties för en LiveCopy i Touch-gränssnittet och klickar på Save without any changes, skrivs en LiveCopy-flik ned och en LiveSync Config-nod skapas. NPR-16327: Programfix för CQ-108562
* Formulärbegränsningen kan inte läsa egenskapen `ConstraintMessage`. NPR-16388: Programfix för CQ-101330
* `wcm/foundation/components/parsys`-komponenten visar inte platshållaren för **[!UICONTROL 'Drag components here]**. NPR: 16748: Programfix för CQ-4205187

### Resurser {#assets-16}

* PDF-rastreraren slutar att fungera och orsakar minnesproblem efter installation av 6.2 SP1 eller hotfix 12430. NPR-15991
* Metadata för en strängegenskap, `documentNumber`, visas som ett datum medan det bör vara ett tal. NPR-16134: Programfix för GRANITE-16916
* Texttrunkeringar i händelseballong för tidslinje. NPR-16226: Programfix för CQ-85226
* När du skapar en mapp under innehållshierarkin med en titel med specialtecken visas specialtecknets kodade form. NPR-15935: Programfix för CQ-4202987
* Användaren kan inte överföra resurser eller skapa mappar när han/hon navigerar bland resurser på grund av inkonsekvent beteende som visas när knappen Skapa används. NPR-16410: Programfix för CQ-4204793
* Oväntade fel påträffades när delade HTML-resurser överfördes från artikelvyn i AEM. NPR-16133: Programfix för AEMM-4155970

### Integrering {#integration-14}

* När du aktiverar proxyautentisering med sammanfattad autentisering genereras ett ConcurrentModificationException av AEM Search-komponenten. NPR-15309: Programfix för CQ-4199191
* När målgruppen skapar en A/B-testaktivitet i AEM synkroniseras den inte upp till målgruppen och visar&quot;ingen målgrupp&quot;. NPR-16229: Programfix för CQ-4204210
* När du har installerat SP1+NPR-11577 v1.2 och väljer &#39;Använd ett analysmått&#39; för målmåttet när du anger mål i TouchUI läses aldrig listrutan över mätvärden. NPR-16129: Programfix för CQ-4204316
* När ni använder målinriktning publicerar kampanjen inte automatiskt hela trädet, inklusive varumärket och överordnad. NPR-15855: Programfix för CQ-94630

### Översättning {#translation-8}

* Synkroniseringsöversättningsjobbet aktiveras inte automatiskt och AEM avsökningen sker inte utan att översättningsprojekten öppnas. NPR-15163: Programfix för CQ-90856

### Forms {#forms-17}

#### Forms tilläggspaket {#forms-add-on-package-17}

**Adaptiv Forms**

* När du sparar ett anpassat formulär med en bifogad fil läggs den fullständiga sökvägen till den bifogade filen till i taggen `fileAttachment` för den genererade XML-filen i stället för namnet på den bifogade filen. NPR-16529
* I XDP-baserade adaptiva formulär finns `afData/afBoundData`-omslutningen i den inskickade XML-filen, även om förifylld XML inte har `afData/afBoundData`-omslutningar. NPR-16118

* Exponentiell notering i fältet Nummer: Om ett tal med ett decimaltal som överskrider totalt tio tecken anges med adaptiva former blir talet exponentiell notation i den skickade XML-filen. NPR-16106
* För formulär som innehåller både en bifogad fil och ett lazy loaded fragment innehåller den skickade XML-datafilen inte informationen för den bifogade filkomponenten. NPR-16022
* För en lazy loaded repetable-panel som inte har någon repeterbar överordnad kan repeterbara underordnade objekt i en andra instans av panelen inte upprepas. NPR-15944
* När du försöker spara ett fragment inuti ett fragment i en formulärredigerare fylls inte värdet för det underordnade fragmentet i fragmentmodellroten. NPR-15943
* När du skapar en kryssruta med endast ett objekt och försöker visa kryssrutans titel med objektets titel dold, kommer åtgärden för att skapa ordlista att generera ett `ArrayIndexOutOfBoundException`-värde om objektets text är tom. Ordlistan skapas inte och inget felsvar genereras på skärmen. NPR-15816
* För anpassningsbara formulär med widgetar för bifogade filer inaktiveras vissa delar av formuläret när den bifogade filen förhandsgranskas.\
   NPR: 16611

* För widgetar för bifogade filer där flera bilagor tillåts, och om en ny formulärinstans med en bifogad fil skickas till en widget med en tidigare bifogad fil, visas en felkod när den tillagda bilagan öppnas i stället för det faktiska innehållet. NPR-16258
* Skydda förifyllningstjänsten för formulär från obehörig åtkomst via protokoll som `file://`, `http://` och `ftp://`. Se &quot; [Konfigurera förifyllningstjänsten med Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754).&quot; NPR-15414

* Begär att det adaptiva formuläret ska återges i PDF-format i stället för i HTML i steget Verifiera och bifoga alla bilagor till PDF-filen så att hela formuläret visas i utskriften. NPR-9011

**Korrespondenshantering**

* När du arbetar med textfragment i en bokstav i läget Förhandsgranska/Redigera, och text konverteras till en lista, bryts hela bokstavsfunktionaliteten och ett JavaScript-fel genereras. NPR-16460
* Importering av en XSD-fil för att skapa en datamordlista i noden Korrespondenshantering misslyckas eftersom webbläsaren inte svarar varje gång XSD-filen överförs och rotnoden väljs. Problemet är webbläsaroberoende och visas inte i serverloggar. NPR-16452
* När du förhandsgranskar ett brev i webbläsaren Internet Explorer och försöker redigera teckensnittsstorleken för innehållet, visas dubblettvärden mellan 8 och 72 i listrutan för teckensnittsstorlek. NPR-16387
* Om ett flytande fält visas som ett indatafält från ett XDP-fragment, expanderas inte fältet i förhandsgranskningen av bokstaven när webbläsaren Internet Explorer används. NPR-16367
* När du försöker skicka ett brev direkt från förhandsgranskningen visas inte popup-fönstret för brevet korrekt eftersom det är dolt. NPR-16353
* Radavstånd som läggs till när du redigerar en bokstav visas inte i förhandsgranskningsfönstret. För listor i textfragment visas inte rätt avstånd i PDF-utdata. NPR-16267
* När du arbetar med ett textdokumentfragment i webbläsaren Internet Explorer misslyckas försök att skapa indrag i texten eftersom markören inte tillåter indrag av text. NPR-16128
* Det tar lång tid att lägga till eller ändra ett datalexikon i ett befintligt textdokumentfragment och användaren meddelas inte alltid. NPR-16102
* När du förhandsgranskar en bokstav som har rullningsbart innehåll i webbläsaren Internet Explorer överlappar webbläsarens rullningslist rullningslist och hela innehållet kan inte visas för fragment på den högra sidan. NPR-16068
* När du skapar eller redigerar textdokumentfragment med webbläsaren Google Chrome öppnas listrutan för färgval automatiskt och kan inte tas bort. Användaren måste välja en lista som typ av datainmatning för att kunna redigera fragmentet. NPR-16067
* Metoden `import com.adobe.icc.services.api.LetterInstanceService` fungerar inte när Letterinstance-API används. NPR-16008
* Att ändra datumvisningsformat till `locale=en_US; dateFormat=MMM dd,yyyy;` i Resursdispositionskonfigurationen fungerar inte som förväntat och datumformatet visas som skräptecken. NPR-16007
* Datalänkningstyp med bokstäver när du redigerar om visas som &quot;Användare&quot;, även om inställningen är annorlunda tidigare. NPR-16619

**Forms Portal**

* Uppgraderingsscenarier för utkast- och inskickskomponenter fungerar inte med implementering av databasexempel. NPR: 16752

**Barcoded Forms Service (BCF)**

* Den statiska kodanalysen av Barcoded Forms Service (BCF) rapporterar problem. NPR-13855

#### Forms JEE Installer  {#forms-jee-installer-17}

**Processhantering - HTML-arbetsyta**

* Skydda förifyllningstjänsten för formulär från obehörig åtkomst via protokoll som&quot;file://&quot;,&quot;http://&quot; och ftp://. Mer information finns i [Konfigurera förifyllningstjänsten med Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**Användarhantering **

* På inloggningsskärmen för SAML visas felaktig version (6.1.0) på AEM 6.2-servern. NPR-13825
* Om användarautentiseringen misslyckas vid inloggning returneras felkoden 404 när AEM Forms har konfigurerats för autentisering med enkel inloggning (Kerberos). Användaren omdirigeras till inloggningswebbplatsen först när sidan har uppdaterats. NPR-15015

#### Forms Designer {#forms-designer-1}

* Det går inte att ändra formulärets nationella inställning till franska (Kanada) i stavningskontrollen för ordlista i AEM Forms Designer.\
   NPR-15896

### Funktionspaket som ingår i CFP3 {#feature-packs-included-in-cfp-2}

**Forms tilläggspaket**

* När du tar bort en resurs i korrespondenshanteringen bör ett varningsmeddelande loggas i filen error.log. NPR-13225
* Förbättra sökfunktionen när du förhandsgranskar en bokstav i korrespondenshanteringen, så att du kan söka efter text i textfragmentets innehåll i stället för att bara söka efter bokstavsrubriken eller etiketten. NPR-16103

### OSGi-paket som ingår i CFP3 {#osgi-bundles-included-in-cfp-5}

Lista över OSGi-paket som uppdaterats mellan AEM 6.2 SP1 och CFP3

[Hämta ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
filDe viktigaste funktionerna i Cumulative Fix Pack 2 är:

* Stabilitetskorrigeringar och prestandaförbättringar på AEM plattform, inklusive Sling-ramverk och -åtgärder
* Förbättrad resurshantering med flera korrigeringar för åtkomst, flyttning, sökning, överföring och publicering av resurser
* Förbättrad redigering och hantering av webbplatser med korrigeringar i komponenterna Content Fragments, Anchor plugin, Slideshow och Context Hub
* Flera korrigeringar i Touch-gränssnittet, inklusive textredigerare, Omnisearch och skapandet av varianter
* Förbättrade arbetsflöden för översättning förbättrad Microsoft-anslutning för att använda nya översättnings-API:er för Azure-portalen
* Korrigeringar i projekt och kampanj
* Förbättrad redigering och hantering med korrigeringar av adaptiva formulär, korrespondenshantering och funktioner för formulärportalen
* Korrigeringar i Forms JEE Core-, XTG- och HTML-arbetsytekomponenter

### Plattform {#platform-14}

* `SlingPostProcessor` aktiveras om sidan som refererar till Sling-ramverket redigeras. NPR-15754: Programfix för CQ-104153

* Värdet för taggar med egenskapen `tagBasePath` hämtas inte i den klassiska gränssnittsdialogrutan när du navigerar till en sidkomponent. NPR-15543: Programfix för CQ-4199950

* När du utför Sling-åtgärder körs en oändlig slinga med tomma segment när du har ett segment med namnet &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk`. NPR-15455: Programfix för SLING-5701

* När ett gränssnitt utökar ett annat gränssnitt injiceras inte de injicerbara metoderna i supergränssnittet korrekt. NPR-15202: Programfix för SLING- 5710
* Ett potentiellt null-pekarundantag förhindras inte när du använder funktionsanropet `com.adobe.granite.infocollector.impl.FilesTraversal`. Programfix NPR-15169 för CQ-4197640
* Arbetsflödets tillstånd är inkonsekvent för vissa sekundära noder och ett fel visas när observationshändelser skickas för den noden. NPR-15701: Programfix för GRANITE-13786
* När användaren väljer en nod i CRXDE (till exempel /content/dam/) och sedan fliken Åtkomstkontroll, och ser till att det finns en åtkomstkontrollista, flyttas de element som inte är markerade när du drar och släpper några element. Programfix NPR-15696 för GRANITE-16300
* Om du väljer en användare i listrutan när du försöker personifiera döljs hela användarens popup-fönster. NPR-15774: HotFix för CQ-4201738/GRANITE-11895
* Det går inte att söka efter taggar med automatiskt ifyllda förslag i Omnissearch. NPR-15088: Programfix för GRANITE-14426.\
   Obs! Denna korrigering kräver Oak CFP 1.4.11 eller senare.

### Mobile AEM Author {#mobile-aem-author}

* När du använder AEM Mobile- och ContentSync-paket med ett hybridprogram svarar AEM på en hämtningsbegäran (med tidsstämplar) som görs av programmet med det äldsta paketet i stället för det som begärs av programmet. NPR-15749: Programfix för CQ-104153

### Webbplatser {#sites-17}

* Ändringsstatus för Workflow Inbox i WCM-kärnan ändras inte om användaren ändrar en sida efter att ha aktiverat ett arbetsflöde. NPR-15684: Snabbkorrigering för CQ-4196974
* Plugin-programmet Fästpunkt i RTF-redigeraren för Touch UI genererar ej kompatibel HTML5 när användaren klickar på ankarikonen och lägger till ett namn. Det ska lägga till attributet id i stället för attributet name i HTML5-taggen för ankarelementet. NPR-15650: Programfix för CQ-89782
* När ett metadataschema med flera fält skapas och används på metadata för innehållsfragment, skapas ingen rullningslist på metadataskärmen för innehållets fragment som gör att fälten inte kan redigeras. NPR-15478: Programfix för CQ-4202622
* När du redigerar fältkomponenten `TagInput` visas inte tidigare konfigurerade värden mot dialogfälten. NPR-15464: HotFix för CQ-4200360

* Om många varianter av ett innehållsfragment skapas i gränssnittet för redigeringsprogrammet för innehållsfragment visas inte rullningslisten på sidpanelen för att navigera i alla variationer. NPR-15445: HotFix för CQ-4199444
* När användare tas bort från direktgrupper läggs de till i ärvda grupper. NPR-15400: Programfix för CQ-98758
* WCM-utveckling: Touch UI-författaren tillåter inte redigering av sidor som har kommatecken i namnet. NPR-15396: Programfix för CQ-4199723
* När du använder Touch-gränssnittet för redigering skickar funktionen `Granite.author.editableHelper.doSelectParent` argument i fel ordning vilket leder till ett JavaScript-fel. NPR-15349: Programfix för CQ-4198594
* ContextHub-segmentet visar upplevelsen även om den cookie som ska avanmäla sig finns. NPR-15293: Programfix för CQ-4198024
* Bildspelskomponenten i det klassiska gränssnittet kan inte skapa bildrutor eller dra och släppa bilder för att skapa nya bildrutor. NPR-15281: Programfix för CQ-4194164
* Oberoende av behörighet visas menyalternativen för att skapa, till exempel Skapa sida, Skapa webbplats, Skapa Live-kopia, Skapa start och Skapa katalog på Admin Console för platsen. NPR-15278: Programfix för CQ-94436
* När du har installerat AEM 6.2 Service Pack 1 slutar reglaget Inkludera undersidor att fungera när sidan startar. NPR-15230: Programfix för CQ-4198449
* Begär att version Rensa ska kunna hämta och bearbeta versioner i block och även kunna använda en angiven sökväg i en XPath-fråga. NPR-15186: Programfix för CQ-109205
* Knappen Rensa saknas på fliken Sidegenskaper i Sites-komponenten. Programfix NPR-15143 för CQ-4196997
* Om du markerar kryssrutan Live Copy i rutan Kolumner på webbplatsens administrationskonsol visas inte Live Copy-status korrekt och endast HTML-kod visas för en webbplats som använder Live-kopior. NPR-15108: Programfix för CQ-97086
* När användaren redigerar innehållsfragment och klickar på Klart (&#39;¢&#39;) för att redigera innan svaret på posten hämtas, sparas det redigerade innehållet inte korrekt. NPR-15014: Programfix för CQ-4194095
* Om du stänger sidan Redigera i Timewarp-läge och försöker öppna den igen från Siteadmin genereras ett fel med statusen 500 i stället för att sidan öppnas igen. NPR-14965: Programfix för CQ-109647:
* I DAM-gränssnittet (Digital Asset Manager) orsakar sökningen efter auktoriseringsfiler för användarväljaren ett undantagsfel, &quot;Slut på minne&quot;. NPR: 15307: HotFix för CQ-98542

### Resurser {#assets-17}

* När du har sökt efter en resurs i Omnissearch kan du markera en resurs och försöka redigera egenskaper genom att klicka på Visa egenskaper och sedan på knappen Spara omdirigeras användarna till en tom sida. NPR-15900: Programfix för CQ-4202372
* Resursens användargränssnitt svarar inte på händelser. Om du markerar en resurs och klickar på Publicera eller Återgivning resulterar det inte i någon aktivitet. NPR-15828: Programfix för CQ-4202247
* När du publicerar en resurs från kortvyn uppdateras inte kortet så att det visar ett publicerat tillstånd om inte sidan uppdateras. NPR-15826: HotFix för CQ-102732
* Kumulativ programfix som innehåller Assets Hotfixes. NPR-15225
* Om ett et-tecken (&#39;&amp;&#39;) ingår i namnet på en objektmapp visas inte mappnamnet korrekt vid navigering till resursen. NPR-15775: Programfix för CQ-4201735
* Om du använder et-tecknet (&#39;&amp;&#39;) i namnet på en resursfil uppstår problem vid åtkomst till dess egenskaper. NPR-15770: Programfix för CQ-4201737
* Om användaren uppdaterar sidan efter att ha markerat och klickat på en resurs visas resursinformationen i stället för det uppdaterade innehållet när användaren navigerar i resurser och använder kolumnvyn. NPR-15768: Programfix för CQ-4201727
* PDS-inmatning tar upp 100 % processoranvändning med en hög med bibliotek för PDF-tjänster. NPR-15606 HotFix för GRANITE-12929
* Om du använder gränssnittet My Link Shares med webbläsaren Firefox visas inte de delade objekten eller användarna och skärmen är oanvändbar. NPR-15539: HotFix för CQ-4200992
* Om en sida är kopplad till en uppsättning bilder när du använder Digital Asset Manager bryts sidkopplingen när du flyttar bilderna till en ny mapp och en del av bilderna saknas på den associerade sidan. NPR-15538: Programfix för CQ-111479
* I Dam Viewer-komponenten orsakar körningsläget &quot;nosampling content&quot; fel med dynamiska media. NPR-15449: Programfix för CQ-4195425
* När du skapar videoprofiler sparas inte ändringarna om du väljer både en förinställning för hög kvalitet och en videokodning med medelhög kvalitet. NPR-15447: Programfix för CQ-4195482
* Även om överföringen av en resurs till Brand Portal misslyckas på grund av serverfelsvar uppdateras statusen till&quot;Publicerad&quot; i användargränssnittet på varumärkesportalen, vilket gör det svårt att spåra den saknade filen. NPR-15442: Programfix för CQ-4197968
* När du publicerar en resursmapp på Brand Portal, där publiceringen tar mer än en timme, kan vissa filer inte publiceras. NPR-15441: Programfix för CQ-4199493
* När du använder konsolen Resurssökning i kolumnvyn misslyckas försök att skapa en mapp en gång, även om det lyckas att försöka igen. NPR-15370: Programfix för CQ-4199448
* Om en resurs eller mapp som valts i DAM-gränssnittet har ett kommatecken i namnet är fliken Referenser inte tillgänglig och meddelandet&quot;Lista över referenser är inte tillgänglig för flera val&quot; visas. NPR-15362: Programfix för CQ-4199721
* När du publicerar en mapp till Brand Portal ändras inte mappens publiceringstillstånd, även om resurserna i mappen har publicerats korrekt. NPR-15292: Programfix för CQ-4197667
* När du navigerar till Resurskonsolen i Touch-gränssnittet visas ett undantag när vissa resurser aktiveras. NPR-15217: HotFix för CQ-108779
* Publicera en video på Youtube när anslutningen är via en proxyserver. NPR-15109: HotFix för CQ-110332
* Använda en resurs med ett namn som innehåller en punkt eller punkt (.) i data-sly-resource inte tolkas till samma resurs och utdatasökvägen avslutas vid punkten. NPR-15069: Programfix för CQ-4195914
* När du har uppgraderat AEM 6.2 till Service Pack 1 misslyckas synkroniseringen av resurser till Scene7. Egenskapen dam:Scene7FileStatus visar statusen `UploadFailed` även för publicerade resurser. NPR-15269: Programfix för CQ-4197708

### Användargränssnitt {#user-interface-5}

* I **[!UICONTROL Touch UI]** visas inte det sparade datumet för datumfält som inte har type=&#39;datetime&#39; när webbläsaren Internet Chrome version 56.0.2924.87 används. NPR-15383: Programfix för GRANITE-16481
* I **[!UICONTROL Touch UI]** tar textredigeraren bort kopplingen och bildtextelementen från HTML-tabeller när de återges. NPR-15267: Programfix för CRTE-41
* `FileUpload Validator` hanterar inte fall när autostart är true eller när  `uploadFile()` anropas manuellt och genererar en ogiltig valideringsrapport i dessa fall. NPR-15295: Programfix för GRANITE-13499

* Omnisearch tillåter inte att kunder som använder /apps lägger till en kolumndatakälla eftersom den antar att platskonfigurationen listas under */libs/granite/omnisearch/content/metadata/*. Programfix NPR-13188 för GRANITE-16479
* När du använder **[!UICONTROL Touch UI]** skapas inte produktvarianter på samma nivå som produkten. Användaren informeras inte om statusen för skapandet av varianten. NPR-15345: HotFix för CQ-4198948

**Scen 7**

* Om du kör Scene7-arbetsflödet skapas öppna filer som inte stängs. Begär att AEM-S7-tjänsten ska förbättras så att den underhåller och återanvänder en enda HttpClient-instans med delad poolkonfiguration. NPR-15357: HotFix för CQ-109958

### Översättning {#translation-9}

* När du använder översättningsprojekt och uppdaterar språkkopior från den engelska överordnad genererar 11 separata starter med samma namn och källrot, men med något annorlunda startrötter, om sidnamnet följer ett angivet mönster. NPR-15605: Programfix för CQ-4200699
* Översättningsprojekt skapas inte för sidor när språkrötterna har bindestreck och streck i namnet. NPR-15171: HotFix för CQ-96286
* Begär att Microsoft Connector ska uppdateras för att kunna använda Microsoft Translator-API:erna, som Microsoft gör tillgängliga på Azure-portalen. NPR-15320: Programfix för CQ-101010

### Projekt {#projects-4}

* Endast 20 inaktiva projekt visas på projektskärmen, men det finns fler än 20 inaktiva projekt i databasen. NPR-15656: Programfix för CQ-4200903

### Campaign {#campaign-1}

* När du använder komponenterna Campaign - Targeting och MAC - Test och Target Integration uppdateras inte aktivitetsstatusen i det Överordnad användargränssnittet när aktiviteter depubliceras. NPR-15401: HotFix för CQ-4199839
* När du flyttar en produkt i AEM Commerce missar guiden för flyttning av produkter de förfyllda värdena för produktnamn, titel, refererade sidor, skapare och skapat datum. NPR-15228: Programfix för CQ-98617

### Dokumentskydd {#security-4}

* En CSRF-tokenparameter har lagts till i formulär med en GET-metod. NPR-15229

### Forms {#forms-18}

#### Forms tilläggspaket {#forms-add-on-package-18}

`**Adaptive Forms**`

* Standardvärden åsidosätts av tomma värden i xml vid förifyllning av det adaptiva formuläret med XML-indata. NPR-15721
* Omslutningen `afData/afBoundData` finns i inskickad XML, även om förifylld XML inte har `afData/afBoundData`-omslutning i XML-schemabaserade adaptiva formulär. NPR-15541

* Titlarna i dragspelsfältet ska vara redigerbara HTML-rubriker av typen &#39;h2&#39; i stället för taggen &#39;a&#39;. NPR-15475
* Dragspelslayouten för en formulärpanel är inte tillgänglig för användare med skärmläsare. Användare kan inte navigera till dragspelsfliken enbart med hjälp av tangentbordet med skärmläsarprogram som JAWS eller NVDA. NPR-15474

`**Correspondence Management**`

* Det tar lång tid att spara, ta bort och ange referens för ett dokumentfragment. NPR-15939
* Tabbjustering som angetts i Hantera resurser på text som innehåller flera rubrikbrytningar i CCR-gränssnittet. NPR-15818
* Miniatyrbilder av textmoduler visar inte justerat innehåll även om texten innehåller justerat innehåll som skapats med Tabbar i Google Chrome. NPR-15819

`**Forms Portal**`

* Prefill Service fungerar inte för XDP Forms. NPR-15466
* När adaptiva formulär lagras och skickas till databasen skadas tillståndet för det adaptiva formuläret när databaskopplingen av någon anledning misslyckas (till exempel efter en lång tid av inaktivitet). NPR-15297

#### Forms JEE Installer  {#forms-jee-installer-18}

`**Core**`

* När du har uppgraderat till den senaste versionen av Java 1.8.0_121-b13 är administratörsgränssnittet inte tillgängligt i AEM Forms. NPR-15330

`**XTG**`

* När du använder Output Service för att sammanfoga ett specifikt formulär med en dataxml är svarstiden 20 gånger jämfört med den tid som används av ES4 SP1-servern för samma åtgärd. NPR-15283

#### AEM Forms App {#aem-forms-app-1}

* När du återställer osparade uppgifter måste meddelandet som visas vid återställning av osparade uppgifter göras tydligare för att minska användarfelen. NPR-15377
* AEM Forms-appen återger inte formulär som skapats från anpassade mallar. NPR-15892
* Användare kan inte logga in i AEM Forms-appen. NPR-15891

Viktiga egenskaper i AEM 6.2 SP2-CFP1 är:

* Effektiviserar replikeringsfunktionen på platser:

   * Korrigeringar av olika problem med utrullning, LiveCopy och felskrivningar

* Förbättrar Touchgränssnittets svarstider under:

   * Resurssökningar
   * storleksbaserad sortering

* Förbättrad tagghantering i smarta samlingar
* Åtkomstkontroller under CRUD-åtgärder på mappar

### Plattform {#previous}

* Begär att `ReplicationQueue#forceRetry` API-anrop ska tas bort när replikeringsagenter startas eftersom sådana anrop gör instansen betydligt långsammare, särskilt när den har många replikeringsagenter. NPR-14032: Programfix för GRANITE-13095
* Begär `DurboImportConfigurationProviderService` OSGi-konfiguration som stöder fält som kan lagra en array med värden. NPR-14570: Programfix för CQ-108684
* Om du använder Sightly-komponenten på en sida efter att du har migrerat till AEM 6.2 slutar dialogrutan Egenskaper på sidan att fungera. NPR-14328: Programfix för CQ-108355
* Om du avschemalägger ett tidigare schemalagt jobb tas inte motsvarande nod under */var/eventing/schedule-job* bort. NPR-14253: Programfix för SLING-5666
* När en administratör försöker personifiera som en borttagen användare, uppdateras inte användargränssnittet. NPR-14247: Programfix för CQ-107446
* XSS-skyddskontrollen orsakar felaktig kodning i Sightly-komponenten. NPR-14004: Programfix för CQ-93821
* Begär att uppgradera Jackrabbit Filevault till 3.1.30 för att lösa flera problem. NPR-13454
* Cachefel inträffar när Sling-distribution synkroniserar distributionspaketen från författare till publicering. NPR-13034: Programfix för GRANITE-13970

### Webbplatser {#sites-18}

* Problem med att VersionManagerImpl rensar felaktiga versioner från versionshistorik. NPR-14372
* Komponenten WCM Sightly Foundation ignorerar komponentdeklarationens taggnamn, `cq:htmlTag / cq:tagName`. NPR-14225
* När Smart parsys används för att återge komponenter som infogats via JavaScript i Touch-gränssnittet, ignoreras den anpassade dekorationen när sidan har uppdaterats. NPR-14122
* Listrutor med mål fungerar inte i Touch UI-dialogrutan när flera Richtext-fält, t.ex. länkar, skapas. NPR-13911
* När du redigerar ett textfält med flera RTF-egenskaper (Rich Text Editor) i en dialogruta (Touch UI) flyttas fokus slumpmässigt till en viss RTE-egenskap. NPR-13703
* Videokomponenten återger inte videominiatyren som standard utanför rutan. NPR-14976
* Informationen läses långsamt in på fliken Live-användning i mallredigeraren. NPR-14880: Programfix för CQ-83417
* Om du installerar hotfix-10936 på en AEM 6.2-instans inaktiveras iparsys-komponenten. NPR-14330: Programfix för CQ-106982
* Flera problem med komponenten Rollout och ett problem med Live Copy efter migrering till AEM 6.1 SP1. NPR-15256
* Åtgärden för sidutrullning kan inte skapa underordnade objekt på en högre nivå än den första, inte ens för flera utrullningskonfigurationer. NPR-15055
* När du skickar dialogrutan Sidegenskaper från redigeraren skrivs oförändrade data på LiveCopy-flikar om. NPR-14693
* När dialogrutan Sidegenskaper skickas från redigeraren skriver MSM Post Processor några parametrar från begäran i stället för parametern `msm:writeLiveCopyConfig`. NPR-14434
* Flera problem som gäller komponenten Rollout, Live-kopior och andra aspekter av MSM. NPR-12235

### Resurser {#assets-18}

* Det går inte att hantera bilder med specialtecken i bildfilens namn i arbetsflödet för att packa. NPR-15227: Programfix för CQ-103887
* Resurser med uttrycket Repeat med Condition visas inte korrekt. När användaren förhandsgranskar bokstavsmallen `*CDN3835RLCEN*` visas inga resurser som finns i målområdet för brödtexten. När resursen `*VIPReassement*`, som är en valfri resurs, som är förmarkerad inte är markerad, visas de andra resurserna som är förmarkerade i bokstaven. NPR-14844

* När du skapar en smart samling bevaras inte formattaggen när den smarta samlingen sparas. NPR-15081: Programfix för CQ-4195494
* Resurssökningsfrågor som körs långsamt i användargränssnittet vid samtidiga sökningar av flera användare. NPR-15019: Hotifx för CQ-4195405
* Metadata som extraheras för en egenskap av typen `Long[]` konverteras till typen `String[]` när den ursprungliga resursen överförs till en annan plats. NPR-15016: Programfix från CQ-4195005

* Användare kan inte ta bort en sparad sökning eller en smart samling. NPR-14924: Programfix för CQ-108494
* Om du redigerar flera metadata för resurser (tilläggsläge) samtidigt som du använder ett booleskt värde för TypeHint i ett nedrullningsbart fält i det underliggande metadataschemat genereras ett fel. NPR-14529: Programfix för CQ-106876
* Användare utan replikeringsrättigheter kan inte ta bort resursmappar. NPR-14321: Programfix för CQ-88271
* När du försöker redigera videoprofilerna för en video i kanalredigeraren öppnas inte designdialogrutan och ett Null-pekarundantag genereras i felloggen. NPR-14144: Programfix för CQ-81101
* Den systemgenererade tidsstämpelegenskapen&quot;Skapad&quot; som visas på egenskapssidan för en resurs är felaktig. NPR-13992: Programfix för CQ-95029
* Begäran om att aktivera identifiering av dubblettresurser för användare utan läsåtkomst i AEM Assets NPR-13851: Programfix för CQ-102281
* Användare kan inte redigera metadata för resurser i grupp från egenskapssidan. NPR-13721: Programfix för CQ-100703
* Felaktigt felmeddelande i Classic UI när en dubblettresurs överförs. Felmeddelandet anger inte varför överföringen misslyckades. NPR-13691: Programfix för CQ-99272
* AEM Assets kan inte sortera mer än 50 resurser efter storlek samtidigt i listvyn när mappen innehåller flera resurser. CQ-100588
* Om du väljer flera resurser uppstår ett fel med svarskod - 414 (begäran-URI för lång) om resurs-/mapp-URI:n är för lång. NPR-13516: Programfix för CQ-76076
* Sidan Resursrapport svarar inte när användaren väljer alla alternativ i dialogrutan Konfigurera kolumner. NPR-13187: Programfix för CQ-95589
* Oväntat beteende för taggväljaren i Safari och Internet Explorer. NPR-13134
* Om du redigerar sparad sökning från Resursens administratörssökspår kan du spara dem som kapslade smarta markeringar, vilket orsakar problem med miljöstabiliteten. NPR-13119: Programfix för CQ-99460
* När du har flyttat en fil (eller mapp) och sedan bytt namn på den, återspeglar inte cq:name-metadata det nya filnamnet (mappnamn). NPR-13036: Programfix för CQ-99141
* Resurser med namn som innehåller specialtecken kan inte laddas ned från nedladdningslänken som delas via e-post. NPR-12872: Programfix för CQ-95795
* Enkla tillgångsrapporter som genereras när det finns ett stort antal resurser orsakar stora genomgångar där sökningen inte når några index- och CPU-användningstoppar. NPR-12811: Programfix för CQ-84409
* Användare på AMS AEM Assets-författarinstansåtkomst från olika nätverk kan inte överföra resurser med hjälp av segmentöverföring utan borttagningsbehörighet för mappar. NPR-12768: Programfix för CQ-82715
* I taggbaserade sökningar efter resurser med hjälp av resurssökningsfunktionen begränsas inte funktionen Type Ahead till rotsökvägen och visar taggar från alla namnutrymmen. NPR-12666
* Komponenten StaticRenditions genererar ett null-pekarundantag. NPR-12665
* Begäran om att inaktivera MissingMetadataNotificationJob eftersom den gör att användargränssnittet för badge-meddelanden bryter sidan med körningsundantaget&quot;Det går inte att skanna indata&quot;. NPR-12500: Programfix för CQ-93573
* Alternativet Inaktivera redigering för ett taggfält fungerar inte i resursegenskapssidor i TouchUI. NPR-12429: Programfix för CQ-88835
* API-korrigeringar i AEM Assets 6.2 för implementering av Companion App SMB. NPR-11099
* Sedan jQuery-uppdateringen kan användare inte markera en resurssamling och bekräfta valet på panelen Associera innehåll för ett innehållsfragment. NPR-14847: Backport för CQ-4194209
* Trots att oändlig sortering anropas på klientsidan sorteras endast artiklar, banners och samlingar som för närvarande visas i användargränssnittet. NPR-14493: Programfix för CQ-109926
* Begär att få implementera en informationsfunktion för AEM-on-demand-tjänst. Nyckelordssökning för artiklar, samlingar eller banderoller returnerar inga träffar. NPR-14093: Programfix för CQ-101394
* När du använder Coral-select-komponenten (*granite/ui/components/coral/foundation/form/select*) i en dialogruta fungerar inte värdeinitieringen korrekt i Internet Explorer (IE11 eller Edge-webbläsare) när det markerade värdet innehåller ett enskilt objekt. NPR-13395: Programfix för CQ-101013

### Projekt {#projects-5}

* När du exporterar ett översättningsprojekt som skapats med Översättningsmetod som&quot;human&quot; och översättningsprovider som&quot;none&quot;, genereras ingen translation_export_summary.xml-fil eftersom GUID-mappningsfilen saknas. NPR-13137: Programfix för CQ-91976
* I AEM projekt, när du skapar ett projekt med egenskapen för förfallodatum, ställer datumkonverteringen in tiden felaktigt på grund av skillnaden i tidszon mellan server och klient. NPR-13003: Programfix för CQ-98288
* Alternativet Visa i platser saknas i översättningsjobbet när ett översättningsprojekt uppdateras. NPR-12966: Programfix för CQ-93740
* När ett översättningsprojekt skapas för en exporterad webbplatssida återges det inte korrekt i förhandsvisningen. NPR-12964: Programfix för CQ-84627

### Arbetsflöde {#workflow-3}

* Nyttolastlänken på fliken Arkiv i arbetsflödeskonsolen returnerar ett fel med svarskoden 404 när du klickar på den. NPR-14993: Programfix för CQ-4194977
* När du använder AEM standardarbetsflöden kan CQ Mailer inte skicka ett e-postmeddelande till gruppen som saknar e-postadressen för en enskild medlem. NPR-14804: Hotfix-begäran för CQ-91499
* Prestandaförbättringar för inkorg och meddelandemärkning i Touch-gränssnittet. NPR-14145: Programfix för CQ-101125
* Användare kan inte förhandsgranska nyttolasten från Inkorgskonsolen för arbetsflödet när arbetsflöden initieras. NPR-13226: Programfix för CQ-100275
* Cookien saml_request_path som konfigurerats med SAML Authentication Handler visar cookie som angetts med ett extra &quot;?&quot; tecken. När ett SAML-svar skickas tillbaka till AEM returnerar AEM cookie-fil för saml_request_path ett ogiltigt värde på grund av redan kodade tecken. NPR-13517: Proaktiv programfix för GRANITE-11722 och GRANITE-14414

### Integrering av lösningar {#solution-integration}

* Om en användare söker efter en term som returnerar en banderoll efter att ha integrerat AEM 6.2 med Search &amp; Promote, svarar inte sökfunktionen. NPR-14549: CFP för CQ-109631

### Dynamic Media {#dynamic-media}

* Många AEM-Scene7-försäljningsjobb som skapades och avbröts när AEM aktiverades loggas som arkivjobb under replikering. NPR-12835: Programfix för CQ-86115

### Dokumentskydd {#security-5}

* Begäran om att lösa indatavalideringsfel i WCMDebug-filter. NPR-12444: Hotfix-begäran för CQ-94890
* Förebyggande begäran om att korrigera XSS-beteende när du använder guiden Skapa start.\
   NPR-13062: Hotfix-begäran för CQ-99577

#### Forms tilläggspaket {#forms-add-on-package-19}

`Adaptive Forms`

* När du skapar en upprepningsbar panel med adaptiva formulär kan paneltiteln inte uppdateras vid körning. NPR-15325
* När standardvärdet för en alternativknapp är inställt och ett annat värde än standardvärdet är valt när du sparar eller skickar, visas inte värdet vid förifyllning. NPR-15304
* Google Chrome visar felaktigt beteende vid användning av händelsen options för att dynamiskt fylla i den nedrullningsbara listan och skicka det valda objektets värde. NPR-15198
* När du skapar en upprepningsbar panel med adaptiva formulär kan paneltiteln inte uppdateras vid körning. NPR-15181
* När du använder redigeringsläge för adaptiva formulär påträffas JavaScript-fel som - &#39;Komponenthanteraren är ogiltig&#39; och &#39;guidelib är odefinierad&#39;. NPR-15112
* Lazy Läser in fragment i en upprepad panel fungerar inte som förväntat. NPR-13916, NPR-14785

`Correspondence Management`

* Correspondence Management-resurser med `'Repeat with condition'`uttryck angivet visas inte korrekt. NPR-14844
* När du söker efter en Correspondence Management-resurs (t.ex. ett brev, dokumentfragment eller någon annan typ) saknas ikonen Kö för hämtning i verktygsfältet. NPR-14745
* När du skapar en List-modul fungerar inte aktivering av objektspecifika egenskaper (som redigerbar, obligatorisk). NPR-14689
* Panelen Dataelement i verktyget Expression Builder läses in hela tiden om en villkorsmodul skapas utan att du behöver välja en dataordlista. NPR-14688
* Vid förhandsgranskning av en bokstav kan man inte använda tabbmellanrum för att justera innehållet i tabellformat. NPR-14481
* När du exporterar flera Correspondence Management-resurser samtidigt från användargränssnittet genererar AEM Forms-servern onödiga loggar. NPR-15226
* När en bokstav förhandsgranskas visas marginaljusterad text i ett annat teckensnitt. NPR-15468

`**Forms Portal**`

* Bifogade filer från inskickade formulär på Forms-portalen visas inte när ett nytt utkast från portalinlämning skickas. NPR-13515

`**Forms Manager**`

* När du navigerar i katalogen *FormsandDocuments* visas inte knappen Klistra in när användaren kopierar en resurs och sedan navigerar till en annan mapp. CQ-111327

#### Forms JEE Installer {#forms-jee-installer-19}

`Rights Management`

* Den inloggningsrelaterade granskningshändelsen loggas med ogiltig tid. Det går inte att spåra rätt tid för granskningshändelsen. NPR-13107
* Adobe Acrobat Reader och Microsoft Office kan inte öppna dokument som skyddas med utökad autentisering. NPR-14482

`Process Management`

* När ett vidarebefordrat utkast i HTML-arbetsytan återställs till den första användaren visas inte uppgiften i den första användarens kö. NPR-15178

`Assembler Service`

* AEM Forms kan inte validera en PDF/A-2b med mer än två signaturer. NPR-14101

`XTG`

* När du skriver ut ett dokument med hjälp av ett skrivarens bypass-fack går det inte att hämta papper från det högra bypass-fältet med funktionen `GeneratePrintedOutput`. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer kraschar när användaren kör stavningskontrollen med det valda språkområdet för formulär som franska (Kanada). NPR-13740
* Forms Designer kraschar när användaren väljer händelsen calculate eller validate för ett formulärfält och ändrar språket till JavaScript och anger `this.` i fönstret **[!UICONTROL Script Editor]**. NPR-12974

### Funktionspaket som ingår i CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms tilläggspaket):

* När ett adaptivt formulär skapas från en XDP-fil följer inte tabbning för tillgänglighet det angivna mönstret. NPR-12562

`Adaptive forms` (Forms tilläggspaket):

* Regelbyggaren för anpassade formulär ger ingen rollbaserad åtkomst. Ändringar som har gjorts av en författare går inte att spåra. NPR-12840

`Core` (Forms JEE Installer):

* Funktionen CoreCross Origin Resource Sharing (CORS) som ett serverletfilter är inte aktiverad för Jboss+. NPR-13050

## Ladda ned instruktioner för CFP via Software Distribution {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>För AEM Forms-kunder är det nödvändigt att installera AEM tilläggspaket efter installation av AEM Service Pack, Cumulative Service Pack eller Feature Pack.

Du kan hämta CFP-paketet direkt från programvarudistribution eller utföra följande steg:

1. Öppna [Programvarudistribution](https://experience.adobe.com/downloads). Du behöver en Adobe ID för att logga in på Software Distribution.
1. Tryck på **[!UICONTROL Adobe Experience Manager]** som finns i rubrikmenyn.
1. Tryck på paketnamnet, välj **[!UICONTROL Accept EULA Terms]** och tryck på **[!UICONTROL Download]**.

## Installationsanvisningar för bestruket finpapper {#installation-instructions-for-cfp}

I det här avsnittet går du igenom kraven och stegen för att installera bestruket finpapper.

### Innan du installerar {#before-you-install}

>[!NOTE]
>
>De valfria funktionspaket som tillhandahålls av Adobe är beroende av releaseversionen och Cumulative Fix Pack. Om du har något funktionspaket installerat kontaktar du [AEM kundtjänstteam](https://helpx.adobe.com/marketing-cloud/contact-support.html) för att validera kompatibiliteten med detta Cumulative Fix Pack för AEM 6.2.

>[!NOTE]
>
>Vi rekommenderar att du kör valideringen på alla nya installationspaket innan du försöker installera paketet. Vid förhandsverifieringen analyseras och rapporteras eventuella fel som påträffats före installationen. Användarna varnas för sådana fel, överlägg och behörigheter.
>
>Dokumentation om valideringsalternativ finns på [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 är en förutsättning för den gemensamma fiskeripolitiken. Installationsanvisningar finns i [AEM 6.2 Service Pack 1 versionsinformation](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* Hämtningen av Cumulative Fix Pack är tillgänglig på [Programdistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html), som du kommer åt direkt från AEM.
* För en klusterdistribution med ( RDBMK eller MongoDB) kan CFP-paketet installeras på alla Author-instanser som använder Package Manager.

* Innan du installerar det kumulativa korrigeringspaketet bör du ta en ögonblicksbild eller skapa en säkerhetskopia av AEM.
* Avinstallation av CFP stöds inte.

### Installera CFP via Software Distribution {#install-the-cfp-via-package-share}

Så här installerar du Cumulative Fix Pack på en befintlig AEM 6.2 SP1-instans:

1. Klicka på länken [Programdistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) för att hämta paketet.

1. Öppna [Pakethanteraren](http://localhost:4502/crx/packmgr/index.jsp) och klicka på **[!UICONTROL Upload Package]** för att överföra paketet.

1. Markera paketnamnet och klicka på **[!UICONTROL Install]**.

### Automatisk installation {#automatic-installation}

Den gemensamma fiskeripolitiken kan installeras automatiskt i en instans som körs på följande sätt:

* Placera paketet i ../crx-quickstart/install medan servern körs. Paketet installeras automatiskt.
* Använd [HTTP-API:t från Package Manager](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) - kontrollera att du använder `cmd=install&recursive=true` - så att det kapslade paketet installeras.

### Validera installation {#validate-installation}

1. Produktinformationssidan (/system/console/ productinfo ) ska nu visa den uppdaterade versionssträngen &quot;Adobe Experience Manager, version 6.2.0.SP1-CFP20&quot; under Installerade produkter.
1. Alla OSGI-paket är antingen AKTIVA eller FRAGMENT i OSGI-konsolen (Använd webbkonsolen: /system/console/bundles).

>[!NOTE]
>
>När paketet har installerats visas ett informationsmeddelande som anger att innehållspaketet har installerats, till exempel&quot;Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 har installerats korrekt.&quot;

>[!NOTE]
>
>Sedan AEM 6.2 SP1-CFP1 har loggnivån i Jackrabbit FileVault ändrats från INFO till DEBUG för de flesta meddelanden. Om du vill få installationsloggar för ett innehållspaket som är installerat på AEM 6.2 SP1-CFP1 eller senare aktiverar du DEBUG-loggnivån för `org.apache.jackrabbit.vault.packaging.impl`.

### Installera AEM Forms {#install-forms}

>[!NOTE]
>
>Hoppa över det här avsnittet om du inte använder AEM Forms.

#### Installera AEM Forms-tillägg {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms endast på JEE**) Hur du installerar en CFP på AEM Forms på JEE beskrivs i [Installera CFP på AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Kontrollera att du har installerat AEM 6.2 SP1 CFP-paketet.
1. Ladda ned motsvarande tilläggspaket från Forms som finns på [AEM Forms releases](aem-forms-releases.md) för ditt operativsystem.
1. Installera Forms-tilläggspaketet enligt beskrivningen i [Installera AEM formulär-tilläggspaket](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Installera AEM Forms JEE-paketpaket {#install-aem-forms-jee-bundles-package}

Korrigeringar i AEM Forms JEE levereras via ett separat installationsprogram. Information om hur du installerar en CFP på AEM Forms på JEE finns i [Installera CFP på AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Installationsprogram för Forms Designer {#designer-installer}

1. Installera uppdateringen genom att köra filen Designer6.2.0_&lt;språk>_Cumulative_QF.msp.
1. Klicka på **uppdatera** på välkomstskärmen. Installationen startar.
1. När installationen är klar klickar du på **slut**.

## Parametrar för användarkonfigurerbar tidsgräns för DTM, Analytics, Target, Search &amp; Promote Connections {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Med AEM Cumulative Fix Pack 6.2 SP1-CFP7 och senare versioner har timeout-perioder gjorts konfigurerbara för alla anslutningar ovan enligt informationen nedan:

| **Anslutningar** | **Tidsgräns för anslutning*** | **Tidsgräns för socket**** |
|---|---|---|
| DTM | 30000ms | 30000ms |
| Analyser | 30000ms | 30000ms |
| Mål | 60000ms | 30000ms |
| Sök och marknadsför | 30000ms | 30000ms |

* **Anslutningens timeout***- Timeout i millisekunder tills en anslutning upprättas. Ett timeout-värde på noll tolkas som en oändlig timeout.
* **Socket-timeout****- Timeout i millisekunder för väntan på data eller en maximal inaktivitetsperiod mellan två på varandra följande datapaket.

>[!NOTE]
>
>Med AEM Cumulative Fix Pack 6.2 SP1-CFP6 och senare versioner är den OSGi-konfiguration som används för integrering av sökning och befordran Apache HTTP Components Proxy Configuration. Proxykonfigurationen från Day Commons HTTP Client 3.1 används inte längre.

## Inaktivera replikeringsstatus i taggningskonsolen (Classic UI) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Om du använder CFP3 eller senare följer du dessa anvisningar för att inaktivera replikeringsstatus i taggningskonsolen i det klassiska användargränssnittet:

* Överlägg *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* i */apps*

* Lägg till `replicationStateRequired`: &quot;false&quot; efter rad nr 416.

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## Senaste Java 8-uppdatering 131 genererar ett undantag (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Dessa konfigurationsinställningar är specifika för AEM Forms-kunder som använder dokumentsäkerhet.

NPR-21355 ingår i CFP12.1. Om du installerar CFP12.1 eller senare utför du följande procedur för att konfigurera NPR-21355 på JBoss-programservern. Om du installerar CFP12.1 på en AEM Forms-server som körs på Oracle WebLogic- eller IBM WebSpehere-programservrar krävs ingen ytterligare konfiguration:

1. Säkerhetskopiera, ta bort och skapa en ny module.xml-fil. Filens standardplats är [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. Öppna den nyligen skapade filen module.xml för redigering. Lägg till följande kod i filen:

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. Skapa en säkerhetskopia av filerna jsafeFIPS.jar, jsafeJCEFIPS.jar och certjFIPS.jar på [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ och ta bort filerna från den här katalogen.

   Kontakta [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) om du vill hämta nya JAR-filer. Placera JAR-filer som hämtats från [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) på [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Endast Windows) Ändra konfigurationsfilerna för `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` eller `domain.conf.bat`:

   * För JBoss-servern i fristående konfiguration öppnar du standalone.conf.bat för redigering.
   * För JBoss-servern i klusterkonfigurationen öppnar du domain.conf.bat för redigering.

   Lägg till följande rader i slutet och spara filen:

   ange &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   ange &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (Endast Linux-baserat OS) Ändra konfigurationsfilerna [AEM_Forms_Installation_directory]/jboss/standalone.conf eller domain.conf:

   * Om du har en fristående JBoss-server öppnar du filen standalone.conf för redigering.
   * För JBoss-servern i klusterkonfigurationen öppnar du domain.conf för redigering.

   Lägg till följande rader i slutet och spara filen:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## Konfigurationsinställningar som krävs för NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 är en del av CFP14.

Antalet delade köer uppdateras inte som standard för andra användare när en användare gör anspråk på en uppgift. För detta har vi infört en ny fastighet. Följ stegen nedan för att konfigurera den här egenskapen på AEM:

1. Gå till Admin UI -> Tjänster -> Arbetsyta -> Global administration.
1. Exportera globala inställningar.
1. Lägg till taggen `<client_tasksPollingInterval>10</client_tasksPollingInterval>` här i den hämtade XML-filen. 10 är exempelvärdet i sekunder. Du kan ändra den därefter.
1. Spara filen.
1. Gå tillbaka till Admin UI -> Tjänster -> Arbetsyta -> Global administration.
1. Importera XML-filen i avsnittet Importera globala inställningar.
1. Du kan nu logga ut från systemet och logga in igen.
1. Antalet delade köer börjar uppdateras för andra användare på arbetsytan.
1. Om du vill stänga av avsökningen ändrar du värdet till 0 och importerar XML-filen igen.

## Ändringar i användargränssnittet {#ui-changes}

* Beteendeändring i visning av titlar på bildkort för Image having DC: title-egenskapen är inställd på String [] ( multifield ): Endast den senaste ändrade titeln visas på bildkortet i användargränssnittet, men alla titlar sparas i CRX. Programfix för CQ-4217165

## Kända fel {#known-issues}

* Om du uppdaterar AEM 6.2SP1-CFP19 och AEM 6.2SP1-CFP20 från CFP18 ändras rotomdirigeringen till den klassiska gränssnittets välkomstsida i stället för /sites.html/content. Du kan behöva korrigera sling: target property from /welcome.html to /index.html with CRX Explorer. Problemet uppstår inte vid uppdatering från CFP17 eller en äldre version.

Följande tillfälliga fel kan uppstå när du installerar AEM 6.2 SP1-CFPx. Ingen upplösning krävs dock för dessa fel eftersom de inte påverkar AEM och försvinner när bestruket finpapper har installerats:

* När du uppgraderar AEM 6.2SP1-CFP20-instansen till AEM 6.5 kanske vissa URL-adresser inte fungerar som:

   * */projects.html*
   * */sites.html*

Du kan dock lösa problemet genom att starta om AEM efter en uppgradering.

* HTTP 500 Internal Server Error is eived when the Webconsole component detail page is opened.
* Fel som **skapa komponentinstans** och **Tjänstfabriken returnerade null** inträffar på grund av databasomstart:

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Det går inte att skapa komponentinstansen eftersom det inte gick att binda referensprofileManager
   * org.apache.sling.Commons.eduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Servicefabriken returnerade null. (Komponent: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Ett fel uppstod i CFP-installationen i Mongo och DB2: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Undantag: java.lang.NullPointerException**. Det här felet inträffar inte när en CFP har installerats över CFP8.
* (Adobe Granite Maintenance Scheduler Update Task) com.adobe.granite.Maintenance.impl.TaskScheduler: Det gick inte att hitta någon underhållsaktivitet med namnet WorkflowPurgeTask för fönstergranit:week
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* När du installerar CFPx på AEM 6.2 SP1 som innehåller funktionspaketet för smarta taggar, tas det tidigare tillagda arbetsflödessteget för resurser för smarta taggar bort från arbetsflödet för DAM-uppdatering av resurser.

Se lista med [Kända fel i AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known problem).

## Uber Jar {#uber-jar}

Uber Jar för 6.2 SP1-CFP20 finns på [Adobe Public Maven-databasen](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

Om du vill använda Uber Jar i ett Maven-projekt inkluderar du följande beroende i projektstrukturen:

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## OSGI-paket och innehållspaket som ingår {#osgi-bundles-and-content-packages-included-5}

Följande text innehåller en förteckning över OSGI-paket och innehållspaket som ingår i den gemensamma fiskeripolitiken.

* [Förteckning över OSGi-paket som ingår i AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Lista över innehållspaket som ingår i AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 hotfixsida](https://helpx.adobe.com/experience-manager/kb/aem62-available-hotfixes.html)
>* [Versionsinformation för AEM 6.2 SP1](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [Versionsinformation för AEM 6.2](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
>* [AEM produktsida](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.2-dokumentation](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [Produktuppdateringar för Adobe Priority](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

