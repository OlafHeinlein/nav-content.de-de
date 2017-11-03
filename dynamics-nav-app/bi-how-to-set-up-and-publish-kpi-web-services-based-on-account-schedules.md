---
title: "Vorgehensweise beim Einrichten und Veröffentlichen von KPI-Webdienste auf der Basis von Kontenschemata"
description: Im Fenster **Kontopaln KPI Web-Service einrichten** richten Sie ein, wie die Kontenschema-KPI-Daten angezeigt werden, und auf welchen spezifischen Kontenschemata die KPIs basieren.
documentationcenter: 
author: SorenGP
ms.prod: dynamics-nav-2017
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4fefaef7380ac10836fcac404eea006f55d8556f
ms.openlocfilehash: b45fe6e1e5d4e5be00a6e8a34b7b4fea39b5d75b
ms.contentlocale: de-de
ms.lasthandoff: 10/16/2017

---
# <a name="how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules"></a><span data-ttu-id="1930c-103">Vorgehensweise: Einrichten und Veröffentlichen von KPI-Webdienste auf der Basis von Kontenschemata</span><span class="sxs-lookup"><span data-stu-id="1930c-103">How to: Set Up and Publish KPI Web Services Based on Account Schedules</span></span>
<span data-ttu-id="1930c-104">Im Fenster **Kontopaln KPI Web-Service einrichten** richten Sie ein, wie die Kontenschema-KPI-Daten angezeigt werden, und auf welchen spezifischen Kontenschemata die KPIs basieren.</span><span class="sxs-lookup"><span data-stu-id="1930c-104">In the **Account Schedule KPI Web Service Setup** window, you set up how to show the account-schedule KPI data and which specific account schedules to base the KPIs on.</span></span> <span data-ttu-id="1930c-105">Wenn Sie die Schaltfläche **Webdienst veröffentlichen** wählen, werden die angegebenen Kontenschema-KPI-Daten der Liste der veröffentlichten Webdienste im Fenster **Web-Dienste** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1930c-105">When you choose the **Publish Web Service** button, the specified account-schedule KPI data is added to the list of published web services in the **Web Services** window.</span></span>  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a><span data-ttu-id="1930c-106">So richten Sie einen KPI-Webdienst ein und veröffentlichen ihn, der auf Kontenschemata basiert</span><span class="sxs-lookup"><span data-stu-id="1930c-106">To set up and publish a KPI web service that is based on account schedules</span></span>  

1.  <span data-ttu-id="1930c-107">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Kontensalden KPI Webservice einrichten** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1930c-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedule KPI Web Service Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1930c-108">Füllen Sie im Inforegister **Allgemein** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="1930c-108">On the **General** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1930c-109">Feld</span><span class="sxs-lookup"><span data-stu-id="1930c-109">Field</span></span>|<span data-ttu-id="1930c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1930c-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1930c-111">**Anfang Geplante Werte**</span><span class="sxs-lookup"><span data-stu-id="1930c-111">**Forecasted Values Start**</span></span>|<span data-ttu-id="1930c-112">Geben Sie an, zu welchem Zeitpunkt prognostizierte Werte in der Grafik des Kontenschema-KPIs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1930c-112">Specify at what point in time forecasted values are shown on the account-schedule KPI graphic.</span></span><br /><br /> <span data-ttu-id="1930c-113">Die prognostizierten Werte werden aus dem Sachpostenbudget abgerufen, das Sie im Feld **Sachkostenbudgetname** auswählen.</span><span class="sxs-lookup"><span data-stu-id="1930c-113">The forecasted values are retrieved from the general ledger budget that you select in the **G/L Budget Name** field.</span></span> <span data-ttu-id="1930c-114">**Hinweis:**Um KPIs zu erhalten, die die prognostizierten Zahlen nach einem bestimmten Datum und die tatsächlichen Zahlen vor dem Datum anzeigen, können Sie das Feld **Buchungen zulassen ab** im Fenster **Sachkonto einrichten** ändern.</span><span class="sxs-lookup"><span data-stu-id="1930c-114">**Note:**  To obtain KPIs that show forecasted figures after a certain date and actual figures before the date, you can change the **Allow Posting From** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="1930c-115">Weitere Informationen finden Sie unter Einrichten von Gruppenbuchungen </span><span class="sxs-lookup"><span data-stu-id="1930c-115">For more information, see Allow Posting From.</span></span>|  
    |<span data-ttu-id="1930c-116">**Finanzbudgetname**</span><span class="sxs-lookup"><span data-stu-id="1930c-116">**G/L Budget Name**</span></span>|<span data-ttu-id="1930c-117">Geben Sie den Namen des Finanzbudgetpostens an, das prognostizierte Werte für den Webdienst des Kontenschema-KPIs bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1930c-117">Specify the name of the general ledger budget that provides forecasted values to the account-schedule KPI web service.</span></span>|  
    |<span data-ttu-id="1930c-118">**Periode**</span><span class="sxs-lookup"><span data-stu-id="1930c-118">**Period**</span></span>|<span data-ttu-id="1930c-119">Geben Sie die Periode an, auf dem der Kontenschema-KPI-Webservice basiert.</span><span class="sxs-lookup"><span data-stu-id="1930c-119">Specify the period that the account-schedule KPI web service is based on.</span></span>|  
    |<span data-ttu-id="1930c-120">**Anzeigen nach**</span><span class="sxs-lookup"><span data-stu-id="1930c-120">**View By**</span></span>|<span data-ttu-id="1930c-121">Geben Sie an, in welchem Zeitintervall der Kontenschema KPI gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1930c-121">Specify which time interval the account-schedule KPI is shown in.</span></span>|  
    |<span data-ttu-id="1930c-122">**Webdienstname**</span><span class="sxs-lookup"><span data-stu-id="1930c-122">**Web Service Name**</span></span>|<span data-ttu-id="1930c-123">Geben Sie den Namen des Kontenschema-KPIs an.</span><span class="sxs-lookup"><span data-stu-id="1930c-123">Specify the name of the account-schedule KPI web service.</span></span><br /><br /> <span data-ttu-id="1930c-124">Dieser Name wird im Feld **Servicename** im Fenster **Webservice** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1930c-124">This name will appear in the **Service Name** field in the **Web Services** window.</span></span>|  

    <span data-ttu-id="1930c-125">Fahren Sie fort, ein oder mehrere Kontenschemata anzugeben, die Sie als KPI-Webdienst gemäß der Einrichtung veröffentlichen möchten, die Sie in der vorhergegangenen Tabelle vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="1930c-125">Proceed to specify one or more account schedules that you want to publish as a KPI web service according to the setup that you made in the previous table.</span></span>  

3.  <span data-ttu-id="1930c-126">Füllen Sie im Inforegister **Kontenschemata** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="1930c-126">On the **Account Schedules** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1930c-127">Feld</span><span class="sxs-lookup"><span data-stu-id="1930c-127">Field</span></span>|<span data-ttu-id="1930c-128">Description</span><span class="sxs-lookup"><span data-stu-id="1930c-128">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1930c-129">**Kontenschemaname**</span><span class="sxs-lookup"><span data-stu-id="1930c-129">**Acc. Schedule Name**</span></span>|<span data-ttu-id="1930c-130">Geben Sie das Kontenschema, auf dem der Kontenschema-KPI-Webservice basiert.</span><span class="sxs-lookup"><span data-stu-id="1930c-130">Specify the account schedule that the KPI web service is based on.</span></span>|  
    |<span data-ttu-id="1930c-131">**Kontenschemabeschreibung**</span><span class="sxs-lookup"><span data-stu-id="1930c-131">**Acc. Schedule Description**</span></span>|<span data-ttu-id="1930c-132">Geben Sie die Beschreibung des Kontenschemas an, auf dem der KPI-Webservice basiert.</span><span class="sxs-lookup"><span data-stu-id="1930c-132">Specify the description of the account schedule that the KPI web service is based on.</span></span>|  

4.  <span data-ttu-id="1930c-133">Wiederholen Sie Schritt 3 für alle Kontenschemata, auf denen der Webdienst des Kontenschema-KPI basieren soll.</span><span class="sxs-lookup"><span data-stu-id="1930c-133">Repeat step 3 for all the account schedules that you want to base the account-schedule KPI web service on.</span></span>  
5.  <span data-ttu-id="1930c-134">Um das ausgewählte Kontenschema einzusehen oder zu bearbeiten, wählen Sie auf dem Inforegister **Kontenschema** **Kontenschema bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="1930c-134">To view or edit the selected account schedule, on the **Account Schedule** FastTab, choose the **Edit Account Schedule** action.</span></span>  
6.  <span data-ttu-id="1930c-135">Um die Daten der Kontenschemas-KPIs anzuzeigen, die Sie eingerichtet haben, wählen Sie auf der Registerkarte Navigieren, in der Gruppe **Allgemein Kontoschema KPI Webservice**.</span><span class="sxs-lookup"><span data-stu-id="1930c-135">To view the account-schedule KPI data that you have set up, choose the **Account Schedule KPI Web Service** action.</span></span>  
7.  <span data-ttu-id="1930c-136">Veröffentlichen Sie den Kontenplan KPI  Webdienst. Wählen Sie die Aktion **Webdient veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="1930c-136">To publish the account-schedule KPI web service, choose the **Publish Web Service** action.</span></span> <span data-ttu-id="1930c-137">Der Webdienst wird der Liste der veröffentlichten Webdienste im Fenster **Webservices** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1930c-137">The web service is added to the list of published web services in the **Web Services** window.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1930c-138">Sie können auch den KPI-Webdienst veröffentlichen, indem Sie im Feld **Webdienst-Setup für KPI-Kontenschema** aus dem Seitenobjekt **Webdienste** verweisen.</span><span class="sxs-lookup"><span data-stu-id="1930c-138">You can also publish the KPI web service by pointing to the **Account Schedule KPI Web Service Setup** page object from the **Web Services** window.</span></span> <span data-ttu-id="1930c-139">Weitere Informationen finden Sie unter [So gehts: Veröffentlichen eines Webservice](https://msdn.microsoft.com/en-us/library/dd338978.aspx) auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="1930c-139">For more information, see [How to: Publish a Web Service](https://msdn.microsoft.com/en-us/library/dd338978.aspx) on MSDN.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1930c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1930c-140">See Also</span></span>  
[<span data-ttu-id="1930c-141">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="1930c-141">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="1930c-142">Finanzen</span><span class="sxs-lookup"><span data-stu-id="1930c-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="1930c-143">Finance einrichten</span><span class="sxs-lookup"><span data-stu-id="1930c-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="1930c-144">Die Finanzbuchhaltung und der Kontenplan</span><span class="sxs-lookup"><span data-stu-id="1930c-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="1930c-145">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1930c-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
