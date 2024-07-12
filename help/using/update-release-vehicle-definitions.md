---
title: Uppdatera definitioner för frisläppningsfordon
description: Den här artikeln innehåller information om de olika typerna av  [!DNL Experience Manager] releaser, inklusive fullständiga releaser, funktionspaket och servicepaket.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 2%

---

# Uppdateringsdefinitioner för [!DNL Experience Manager]-versionen {#update-release-vehicle-definitions}

Det här dokumentet innehåller information om de olika typerna av [!DNL Adobe Experience Manager]-utgåvor, inklusive fullständiga utgåvor, funktionspaket och servicepaket som [!DNL Adobe] levererar till sina kunder.

>[!NOTE]
>
>För releaseschema för [!DNL Experience Manager] uppdateringsreleaser, se [[!DNL Experience Manager] färdplan för uppdateringsreleaser](update-releases-roadmap.md)

## Fullversion {#full-release}

| Objekt | Beskrivning |
|-------|------|
| Definition | <ul> <li> Schemalagd release </li> <li> Stöder uppgraderingssökvägar för specifika versioner som definieras i versionsinformationen </li> </ul> |
| Namngivning | <ul> <li> Versionsnummer för större releaser ökar baserat på formeln X+1.Y.Z. </li> <li> Versionsnummer för mindre releaser ökar baserat på formeln X.Y+1.Z </li> </ul> Där X är det primära versionsnumret, är Y det sekundära versionsnumret och Z korrigeringsnumret. |
| Inkluderingar | <ul> <li> Nya funktioner </li> <li>  Förbättringar </li> <li>  Felkorrigeringar </li> </ul> |
| Dokumentation | <ul> <li> Versionsinformation finns på dokumentationsportalen </li> <li> Dokumentation om funktioner, förbättringar och felkorrigeringar finns på dokumentationsportalen </li> </ul> |
| Cadence | Årsvis |
| Tillgänglighet och installation | <ul> <li> Levereras som ett fristående installationsprogram </li> <li>  Finns på licenswebbplatsen och Managed Services </li> <li> Licenswebbplatsen kan kräva migrering av innehållsdatabas </li> </ul> |
| Testnivå | Fullt validerad av kvalitetskontrollen |

## Service Pack {#service-pack}

| Objekt | Beskrivning |
|-----|-----|
| Definition | <ul> <li> Schemalagd release </li> <li> Det kan för närvarande inte återställas </li> </ul> |
| Namngivning | <ul> <li> Patch release number is a single digit number </li> <li> Efter installationen ökar korrigeringssiffran för det installerade versionsnumret baserat på formeln X.Y.Z.SPx </li> </ul> Där X är det primära versionsnumret, är Y det sekundära versionsnumret och Z korrigeringsnumret. x är service pack-numret. |
| Inkluderingar | <ul> <li> Nya funktioner</li> <li>  Förbättringar </li> <li> Felkorrigeringar </li> <li> Funktionspaket för gemensamma intressen (om sådana finns) </li> </ul> |
| Dokumentation | <ul> <li> Versionsinformation finns på dokumentationsportalen </li> <li> Dokumentation om funktioner, förbättringar, felkorrigeringar på dokumentationsportalen </li> </ul> |
| Cadence | kvartalsvis |
| Tillgänglighet och installation | <ul> <li> Levereras som ett paket </li> <li> Finns för distribution av programvara</li> <li>  Kräver befintlig funktionell installation </li> </ul> |
| Testnivå | <ul> <li> Alla korrigeringar QA har validerats </li> <li>  Total paketsäkerhet med automatiserade körningar </li> </ul> |

## Kumulativt korrigeringspaket {#cumulative-fix-pack-aem}

| Objekt | Beskrivning |
|-----|-----|
| Definition | <ul> <li> Enstaka leveransmodell för frisläppningsfixar </li> <li> Aggregator-innehållspaket som innehåller innehållspaket för enskilda komponenter </li> <li>  Bestruket finpapper är en överrullning av snabbkorrigeringar och inga förbättringar ingår i den.  </li> </ul> |
| Namngivning | X.Y.Z.CFPx <br> där X är det primära versionsnumret, Y är det sekundära versionsnumret och Z korrigeringsnumret. x är det kumulativa Service Pack-numret. |
| Inkluderingar | CFP är ett kumulativt korrigeringspaket som innehåller korrigeringar av alla komponenter under angivna datum. Om en kund till exempel tillämpar CFP3, blir CFP3 = CFP1 + CFP2. |
| Dokumentation | Versionsinformation finns på dokumentationsportalen |
| Cadence | kvartalsvis |
| Tillgänglighet och installation | <ul> <li> Levereras som ett paket </li> <li>  Finns för distribution av programvara </li> <li>  Beroende på det senaste Service Pack-versionen </li> <li>  Den gemensamma fiskeripolitiken är självberoende. Kunderna behöver inte bekymra sig om att hitta/lösa beroenden. Bestruket papper bör installeras på den senaste versionen av Service Pack. </li> <li>  CFP kan installeras som ett enda paket, vilket förbättrar kundupplevelsen.  </li> </ul> |
| Testnivå | QA validerat på integreringsnivå och regressionstestning |

## Övertäckning {#overlay}

| Objekt | Information |
|-------|--------|
| Namngivning | överlägg-&lt;biljett-ID> |
| Inkluderingar | Felkorrigering för en JS- eller JSP-fil |
| Dokumentation | Ingen |
| Cadence | Vid behov |
| Tillgänglighet och installation | <ul> <li> Levereras som paket av [!DNL Experience Manager] kundtjänst  </li> <li> Ingår inte nödvändigtvis i Service Pack eller fullständiga versioner </li> </ul> |
| Testnivå | Validerad av Kundtjänst |

## Funktionspaket {#feature-pack}

| Objekt | Information |
|--------|-----|
| Definition | <ul> <li>Funktionspaket är tilläggsfunktioner och levereras via ett Service Pack. Om en [!DNL Experience Manager]-version har släppt sitt senaste Service Pack kommer Adobe inte att leverera något funktionspaket till den i framtiden. </li> <li> FP:er innehåller produktförbättringar, schemalagda för en efterföljande produktrelease, men levererade tidigt baserat på beslut av [!DNL Adobe's] Product Management.</li> <li>  Funktionerna sammanfogas alltid med nästa större release. De porteras sedan till den [!DNL Experience Manager]-version som kunden kräver </li> <li>  Funktionspaket för gemensamt intresse och GA sammanfogas i nästa Service Pack  </li> </ul> |
| Namngivning | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inkluderingar | <ul> <li> Nya funktioner </li> <li> Förbättringar </li> <li> Felkorrigeringar (stegvisa produktuppdateringar) </li> </ul> |
| Dokumentation | Dokumentation finns på adobe.com. |
| Cadence | Varierar med produktområdet |
| Tillgänglighet och installation | <ul> <li>Levereras via Service Pack </li> <li> Finns för distribution av programvara. Kunder godkänner [!DNL Adobe's] villkor via programvarudistribution. </li> </ul> |
| Testnivå | Funktionspaket för allmän tillgänglighet är QA-validerade. |

* 1: Oak-korrigeringar levereras inte som enskilda snabbkorrigeringar. De ingår dock i den efterföljande snabbkorrigeringen för Cumulative Oak. Om det behövs kan en diagnostik som bygger på den senaste COFP göras tillgänglig. Förutsättningen är att kunden har den senaste COFP som körs. Diagnostiska byggen ger bara samma kvalitetssäkring som en snabbkorrigering. Därför ger de inte lika mycket kvalitetssäkring som ett kumulativt korrigeringspaket, Service Pack eller produktrelease. Den slutliga lösningen levereras med nästa gemensamma fiskeripolitik.
