---
title: Äldre versioner av AEM, CQ och CRX
description: Dokumentationspaket för äldre versioner av Adobe Experience Manager, CQ och CRX.
translation-type: tm+mt
source-git-commit: 47b391ed659264b611f08d2fa9e45a923be5c445
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---


# Äldre versioner av [!DNL Adobe Experience Manager], CQ och CRX {#older-versions-aem-cq-crx}

## Äldre versioner av [!DNL Experience Manager]-dokumentation {#older-version-aem-documentation}

Versionerna av [!DNL Experience Manager], CQ och CRX som anges på den här sidan är &quot;End of Life&quot; och säljs inte längre officiellt av Adobe. Våra senaste versioner av officiell dokumentation för dessa äldre versioner finns tillgängliga för dina självhjälpsbehov. Vi rekommenderar att du uppgraderar till den senaste versionen (som för närvarande är [[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)).

>[!NOTE]
>
>Om du vill veta när en [!DNL Experience Manager]-version kommer att få slut på kärnsupporten kan du läsa [produkter och perioder för teknisk support](https://helpx.adobe.com/support/programs/eol-matrix.html) och söka i `AEM`.

### Innan du installerar {#before-installation}

Innan du laddar ned paketet bör du bestämma vem som ska konsumera innehållet. Detta beslut kommer att avgöra hur det ska distribueras:

* Utvecklare kan installera lokalt för snabb referens.
* För större dokumentationsbehov rekommenderar vi att paketet distribueras på en internt tillgänglig, icke-produktionsbaserad AEM Author-instans.

>[!NOTE]
>
>Användare måste vara inloggade i [!DNL Experience Manager]-instansen för att komma åt det här innehållet på [!DNL Experience Manager] Author. Det här innehållet är inte tillgängligt som standard i AEM Publish (som det finns under /libs).

## Platser för programvarudistribution {#software-distribution-locations}

Du behöver en giltig Adobe ID:

* Om du inte har någon Adobe ID kan du skapa en på www.adobe.com
Om du behöver hjälp med att skapa eller hantera din Adobe ID [kan du läsa den här guiden](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] Version | Software Distribution Link |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.1 | [Hämta AEM-DOCS-6.1 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-1.zip) |
| [!DNL Experience Manager] 6.0 | [Ladda ned AEM-DOCS-6.0 från Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [Hämta AEM-DOCS-5.6.1 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5.6 | [Ladda ned AEM-DOCS-5.6 från Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [Ladda ned CQ-DOCS-5.5 från Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [Ladda ned CQ-DOCS-5.4 från Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [Ladda ned CQ-DOCS-5.3 från Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [Hämta CRX-DOCS-2.3 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [Hämta CRX-DOCS-2.2 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [Hämta CRX-DOCS-2.1 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [Hämta CRX-DOCS-2.0 från programvarudistribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## Installera ett dokumentationspaket {#how-to-install-documentation-package}

Om du vill installera ett äldre dokumentationspaket måste du ha [!DNL Experience Manager] installerat och igång på den lokala enheten eller nätverksenheten.

### Hämta dokumentationspaketet {#download-documentation-package}

1. I tabellen ovan väljer du länken för den [!DNL Experience Manager]-dokumentationsversion som ska hämtas. Till exempel AEM 5.6.1.

1. Logga in med din Adobe ID. Om du inte har något ID skapar du ett.

1. Välj knappen **[!UICONTROL Download]**.

1. Här är ett exempel på vad du kommer att se:

![Exempel på programvarudistribution](assets/screen_shot_2020-07-10at161922.jpg)

### Installera paketet på den lokala instansen {#install-package-local-instance}

1. Öppna [!DNL Experience Manager]-användargränssnittet. I en webbläsare anger du: `http://localhost:4502/`. Logga in som administratör.

1. Välj **[!UICONTROL Tools]** > **[!UICONTROL Deployment]** > **[!UICONTROL Packages]**.

1. Välj **[!UICONTROL Upload Package]** i pakethanterarens användargränssnitt.

1. Bläddra till den plats där du hämtade AEM 5.6.1-paketet (aem-docs-5-6-1.zip).

1. Markera paketet och klicka på **[!UICONTROL OK]**.

1. När paketet har överförts måste du installera det.

1. Leta reda på paketet och välj **[!UICONTROL Install]** i Pakethanterarens användargränssnitt.

1. Välj **[!UICONTROL Install]** igen i bekräftelsedialogrutan. Obs! installationen tar några minuter.

1. Starta dokumentationssidan i en webbläsare. Med hjälp av AEM 5.6.1 blir URL:en: http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html.

## Få hjälp från [!DNL Experience Manager]-communityn {#get-help-from-aem-community}

Om du har frågor om hur du använder Experience Manager rekommenderar vi att du [kontaktar våra erfarna community-experter i [!DNL Experience Manager] forumen](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).
