---
source-git-commit: 437dad5fffe71592b6f9f9b4099a253e3a55b0c8
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---
# Riktlinjer för att bidra till Adobe Experience Manager-dokumentation

## Dokumentationsfilosofi

Adobe Experience Manager-användare arbetar i mycket konkurrenskraftiga miljöer och strävar efter att skapa digitala upplevelser som skiljer dem från deras konkurrenter. När Adobe levererar avancerade nya verktyg i AEM kompletteras dessa verktyg därför med korrekt och tydlig dokumentation som gör att kunderna omedelbart kan utnyttja sin AEM och maximera avkastningen.

Målet med den AEM dokumentationen är att ge AEM tillgång till dokumentation så snart som möjligt. Därför skapas korrekt och användbar dokumentation som uppdateras kontinuerligt och förbättras.

## Dokumentationsbidrag

För att ständigt förbättra AEM dokumentation är AEM välkommen att bidra till dokumentationen. Vare sig det gäller förfrågningar eller frågor kan förbättringar av dokumentationen vara korrigeringar, klargöranden, tillägg och fler exempel.

## Dokumentationsstandarder

Bidrag till dokumentationen tas emot. Alla bidrag till AEM, antingen i form av en begäran om att tjänsten ska fyllas i eller i form av en utlysning, bör uppfylla Adobe krav på bidrag och dokumentation.

Bidrag som inte uppfyller dessa standarder kan avvisas.

### Adobe-dokument - standardanvändningsexempel.

AEM dokumentation täcker standardanvändningsfall. Användningsfall som inte omfattas av standardinstallationer och standardanvändning av produkten ingår inte i AEM.

### Adobe dokumenterar vanligtvis inte buggar eller deras temporära lösningar.

AEM dokumentation täcker standardanvändningsfall. Av den anledningen dokumenteras inte buggar, effekter orsakade av buggar och tillfälliga lösningar för buggar.

Undantag från den här regeln gäller versionsinformationen där kända problem kan listas med möjliga lösningar som har godkänts av AEM produkthantering.

### Dokumentationsbidragen är inte till för att besvara tekniska frågor.

Alla idéer du kan behöva förbättra AEM dokumentation är välkomna som bidrag. Kommentarer, problem och pull-förfrågningar är dock avsedda för *avgifter* endast. De är inte avsedda att besvara dina frågor om hur du använder AEM, implementerar ditt AEM eller löser tekniska problem.

Om du har frågor om hur AEM eller tekniska fel har använts ska du rapportera via den normala supportprocessen via [Experience Cloud Enterprise Support Portal](https://experienceleague.adobe.com/?support-solution=General#support) eller diskuteras i [Experience Manager community](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).

***AEM bidrag till dokumentationen ersätter inte Adobe kundtjänst*** och alla sådana bidrag som söker svar på frågor som rör stöd avvisas.

### Bidragen ska tydligt hänvisa till berörda dokumentationssidor.

Om du skapar ett problem som kan föreslå förbättringar av dokumentationen måste du inkludera länkar till de sidor som påverkas. Om du skapar ett problem med hjälp av **Redigera den här sidan** på en dokumentationssida skapas problemet automatiskt med en länk till sidan.

Detta gäller inte för pull-begäranden eftersom pull-begäranden till sin natur refererar till den eller de berörda sidorna.

## Riktlinjer för dokumentation

Alla bidrag till dokumentationen måste följa vissa riktlinjer för format.

Genom att följa dessa riktlinjer blir det enklare att granska ditt bidrag och det går därför snabbare att integrera det i dokumentationen.

### Språk och format

#### Språk

* AEM dokumentation skrivs och underhålls på amerikansk engelska.
* Håll meningar så enkla som möjligt.
* Se till att språket är klart och koncist.

Kom ihåg att läsarna av AEM är från hela världen och inte kan förväntas vara inbyggda eller flytande engelska. Undvik kollokvialism och håll språket så tydligt och enkelt som möjligt.

#### Följ Microsoft® Manual of Style

[The Microsoft® Manual of Style](https://learn.microsoft.com/en-us/style-guide/welcome/) är en kostnadsfri handbok för dokumentationsformat som fokuserar på programvarudokumentation och AEM dokumentation följer den här handboken när det är möjligt.

### Formatering

| Objekt | Stil |
|---|---|
| Element eller alternativ i användargränssnittet | **fet** |
| Filnamn, sökväg, användarindata, parametervärden | `monospaced` |
| Kod, kommandorad | ```Code Block``` |

### Skärmbilder

Skärmbilder ska användas med omdöme och endast när en textbeskrivning är otillräcklig.

Markörer eller andra anteckningar i skärmbilder (som röda ramar, pilar eller text) bör inte användas. På så sätt är skärmbilderna enklare att återanvända eller replikera i lokaliserade versioner av dokumentationen.

### Versionsspecifika referenser

Undvik om möjligt direkta referenser till en viss version i dokumentationsinnehållet. Detta gör dokumentationen mer flexibel och utbyggbar för framtida versioner.

### Användning av dag, AEM, CQ, CRX

Använd alltid produktens fullständiga namn **Adobe Experience Manager** för första gången i en artikel kan den sedan kallas **AEM**.

Day, Day Software, CQ och CRX bör inte användas utom när det är oundvikligt, t.ex. i klassnamn eller med hänvisning till AEM.