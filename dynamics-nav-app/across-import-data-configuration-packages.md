---
title: Verwenden von Excel, um Daten in Dynamics NAV zu importieren
description: "Verwenden Sie das Standardkonfigurationspaket, um Debitorendaten in Excel hinzuzufügen und Daten nach Dynamics NAV zu importieren."
author: edupont04
ms.prod: dynamics-nav-2017
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 4fefaef7380ac10836fcac404eea006f55d8556f
ms.openlocfilehash: eb9b7137ee31824ba845ff336c00c6f0e59f6f5c
ms.contentlocale: de-de
ms.lasthandoff: 10/16/2017

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="5cc47-103">Importieren von Daten aus der Vorgänger-Buchhaltungs-Software unter Verwendung eines Konfigurations-Pakets.</span><span class="sxs-lookup"><span data-stu-id="5cc47-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="5cc47-104">Sie können Transaktions-Masterdaten und die Daten aus anderen Finanzsysteme basierend auf dem Standardkonfigurationspaket in [!INCLUDE[d365fin](includes/d365fin_md.md)] importieren.</span><span class="sxs-lookup"><span data-stu-id="5cc47-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5cc47-105">Im Fenster **Konfigurationspakete** können Sie mit einem Paket arbeiten, um die Daten zu importieren und zu prüfen, bevor Sie die Paketnummer anwenden.</span><span class="sxs-lookup"><span data-stu-id="5cc47-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="5cc47-106">Wenn Sie mit RapidStart-Services für Microsoft Dynamics vertraut sind, sind Sie außerdem mit Konfigurationspaketen vertraut.</span><span class="sxs-lookup"><span data-stu-id="5cc47-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="5cc47-107">Das Standardkonfigurationspaket unterstützt die meisten allgemeinen Arten von Daten, die Sie von einem Legacysystem importieren möchten.</span><span class="sxs-lookup"><span data-stu-id="5cc47-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="5cc47-108">Dort können Sie die Daten aus Legacysystem hinzufügen und sie dann entsprechend der Geschäftslogik von [!INCLUDE[d365fin](includes/d365fin_md.md)] festlegen.</span><span class="sxs-lookup"><span data-stu-id="5cc47-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="5cc47-109">Alternativ verwenden Sie den Datenmigrationsassistenten, um die Daten aus QuickBooks oder von Dynamics GP zu importieren.</span><span class="sxs-lookup"><span data-stu-id="5cc47-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="5cc47-110">Weitere Informationen finden Sie unter [QuickBooks-Datenmigration](ui-extensions-quickbooks-data-migration.md) oder [Dynamics GP-Datenmigration](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="5cc47-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="5cc47-111">Arbeiten mit Daten in Excel</span><span class="sxs-lookup"><span data-stu-id="5cc47-111">Working with Data in Excel</span></span>
<span data-ttu-id="5cc47-112">Wenn Sie das Standardkonfigurationspaket in Excel exportieren, enthält die generierte Arbeitsmappe einen Vorschlag für jede Tabelle im Paket.</span><span class="sxs-lookup"><span data-stu-id="5cc47-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="5cc47-113">Um Ihre Aufgaben zu vereinfachen, können Sie die in Excel integrierten XML-Änderungswerkzeuge nutzen.</span><span class="sxs-lookup"><span data-stu-id="5cc47-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="5cc47-114">Sie können die in Excel integrierten Funktionen auch für die Datenformatierung und zum Verschieben von Daten in die richtige Zelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="5cc47-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="5cc47-115">Beispielsweise fügen Sie einen leeren Vorschlag hinzu und kopieren Sie die Stammdaten dazu.</span><span class="sxs-lookup"><span data-stu-id="5cc47-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="5cc47-116">Verwenden Sie eine Excel-Formel, um Daten im Arbeitsblatt für die Datenumwandlung zwischen den Feldern im exportierten Datenblatt und in den Debitorenstammdaten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5cc47-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="5cc47-117">Sobald Sie alle Daten zugeordnet haben, kopieren Sie den Bereich der Daten in das Arbeitsblatt mit der Migrationstabelle.</span><span class="sxs-lookup"><span data-stu-id="5cc47-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="5cc47-118">Ändern Sie nicht die Spalten in den Arbeitsblättern.</span><span class="sxs-lookup"><span data-stu-id="5cc47-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="5cc47-119">Wenn sie verschoben, geändert oder gelöscht werden, kann das Arbeitsblatt nicht in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden.</span><span class="sxs-lookup"><span data-stu-id="5cc47-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="5cc47-120">Tabellen im Standard-Konfigurations-Paket</span><span class="sxs-lookup"><span data-stu-id="5cc47-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="5cc47-121">Das Standardkonfigurationspaket unterstützt die folgenden Tabellen:</span><span class="sxs-lookup"><span data-stu-id="5cc47-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="5cc47-122">Zahlungsbedingungen</span><span class="sxs-lookup"><span data-stu-id="5cc47-122">Payment Terms</span></span>
-   <span data-ttu-id="5cc47-123">Debitorenpreisgruppe</span><span class="sxs-lookup"><span data-stu-id="5cc47-123">Customer Price Group</span></span>
-   <span data-ttu-id="5cc47-124">Lieferbedingung</span><span class="sxs-lookup"><span data-stu-id="5cc47-124">Shipment Method</span></span>
-   <span data-ttu-id="5cc47-125">Verkäufer/Einkäufer</span><span class="sxs-lookup"><span data-stu-id="5cc47-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="5cc47-126">Ort</span><span class="sxs-lookup"><span data-stu-id="5cc47-126">Location</span></span>
-   <span data-ttu-id="5cc47-127">Gegenkonto</span><span class="sxs-lookup"><span data-stu-id="5cc47-127">GL Account</span></span>
-   <span data-ttu-id="5cc47-128">Debitor</span><span class="sxs-lookup"><span data-stu-id="5cc47-128">Customer</span></span>
-   <span data-ttu-id="5cc47-129">Kreditor</span><span class="sxs-lookup"><span data-stu-id="5cc47-129">Vendor</span></span>
-   <span data-ttu-id="5cc47-130">Option</span><span class="sxs-lookup"><span data-stu-id="5cc47-130">Item</span></span>
-   <span data-ttu-id="5cc47-131">Verkaufskopf</span><span class="sxs-lookup"><span data-stu-id="5cc47-131">Sales Header</span></span>
-   <span data-ttu-id="5cc47-132">Verkaufszeile</span><span class="sxs-lookup"><span data-stu-id="5cc47-132">Sales Line</span></span>
-   <span data-ttu-id="5cc47-133">Einkaufskopf</span><span class="sxs-lookup"><span data-stu-id="5cc47-133">Purchase Header</span></span>
-   <span data-ttu-id="5cc47-134">Einkaufszeile</span><span class="sxs-lookup"><span data-stu-id="5cc47-134">Purchase Line</span></span>
-   <span data-ttu-id="5cc47-135">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="5cc47-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="5cc47-136">Artikel Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="5cc47-136">Item Journal Line</span></span>
-   <span data-ttu-id="5cc47-137">Debitorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5cc47-137">Customer Posting Group</span></span>
-   <span data-ttu-id="5cc47-138">Kreditorenbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5cc47-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="5cc47-139">Lagerbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5cc47-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="5cc47-140">Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="5cc47-140">Unit of Measure</span></span>
-   <span data-ttu-id="5cc47-141">Geschäftsbuchungsgrp.</span><span class="sxs-lookup"><span data-stu-id="5cc47-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="5cc47-142">Produktbuchungsgrp.</span><span class="sxs-lookup"><span data-stu-id="5cc47-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="5cc47-143">Buchungsmatrix Einrichtung</span><span class="sxs-lookup"><span data-stu-id="5cc47-143">General Posting Setup</span></span>
-   <span data-ttu-id="5cc47-144">Gebiet</span><span class="sxs-lookup"><span data-stu-id="5cc47-144">Territory</span></span>
-   <span data-ttu-id="5cc47-145">Artikelkategorie</span><span class="sxs-lookup"><span data-stu-id="5cc47-145">Item Category</span></span>
-   <span data-ttu-id="5cc47-146">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="5cc47-146">Sales Price</span></span>
-   <span data-ttu-id="5cc47-147">Einkaufspreis</span><span class="sxs-lookup"><span data-stu-id="5cc47-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="5cc47-148">So importieren Sie Debitorendaten</span><span class="sxs-lookup"><span data-stu-id="5cc47-148">Importing Customer Data</span></span>
<span data-ttu-id="5cc47-149">Nachdem die Debitorendaten in die Excel-Dateien für die Datenmigration eingegeben wurden, importieren Sie die Dateien in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="5cc47-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5cc47-150">Im Fenster **Konfigurationspakete** importieren Sie die Excel-Datei aus den Daten, und Sie können prüfen, ob die Daten mit [!INCLUDE[d365fin](includes/d365fin_md.md)] übereinstimmen, bevor Sie das Paket anwenden.</span><span class="sxs-lookup"><span data-stu-id="5cc47-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cc47-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cc47-151">See Also</span></span>
[<span data-ttu-id="5cc47-152">Geschäftsdaten aus anderen Finanzsystemen importieren</span><span class="sxs-lookup"><span data-stu-id="5cc47-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="5cc47-153">QuickBooks Datenmigration</span><span class="sxs-lookup"><span data-stu-id="5cc47-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="5cc47-154">Dynamics GP Datenmigration</span><span class="sxs-lookup"><span data-stu-id="5cc47-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)
