---
title: "Währungswechselkurse"
description: "Am Ende des Geschäftsjahres, müssen Wechselkurse für Verbindlichkeiten und Forderungen reguliert werden, sodass sie ordnungsgemäß in der Jahresbilanz bewertet werden. Der Batchauftrag **Wechselkurse regulieren** unterstützt verschiedene Bewertungsmethoden, um so die rechtlichen Anforderungen in Deutschland zu erfüllen."
documentationcenter: 
author: SorenGP
ms.prod: dynamics-nav-2017
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b9b1f062ee6009f34698ea2cf33bc25bdd5b11e4
ms.openlocfilehash: 73b2e660abd30b1b9bb38c2445547bce7ae89127
ms.contentlocale: de-de
ms.lasthandoff: 10/23/2017

---
# <a name="currency-exchange-rates"></a><span data-ttu-id="1e9f0-104">Währungswechselkurse</span><span class="sxs-lookup"><span data-stu-id="1e9f0-104">Currency Exchange Rates</span></span>
<span data-ttu-id="1e9f0-105">Am Ende des Geschäftsjahres, müssen Wechselkurse für Verbindlichkeiten und Forderungen reguliert werden, sodass sie ordnungsgemäß in der Jahresbilanz bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-105">At the end of the fiscal year, you must adjust currency exchange rates for payables and receivables so that they are valued correctly in the annual balance.</span></span> <span data-ttu-id="1e9f0-106">Der Batchauftrag **Wechselkurse regulieren** unterstützt verschiedene Bewertungsmethoden, um so die rechtlichen Anforderungen in Deutschland zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-106">The **Adjust Exchange Rates** batch job supports different valuation methods in order to meet legal requirements in Germany.</span></span>  

## <a name="valuation-methods"></a><span data-ttu-id="1e9f0-107">Bewertungsmethoden</span><span class="sxs-lookup"><span data-stu-id="1e9f0-107">Valuation Methods</span></span>  
<span data-ttu-id="1e9f0-108">Gemäß dem Bilanzmodernisierungsgesetz (BilMoG) werden Verbindlichkeiten und Forderungen unterschiedlich bewertet, je nach Abweichung zwischen Referenzdatum und Fälligkeitsdatum.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-108">According to the Bilanz Modernisierungs Gesetz (BilMoG), payables and receivables are valued differently depending on the difference between the reference date and the due date.</span></span> <span data-ttu-id="1e9f0-109">Dies wird durch den Batchauftrag **Wechselkurse regulieren** verwaltet, in dem sie angeben können, welche Bewertungsmethode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-109">This is managed by the **Adjust Exchange Rates** batch job where you can specify which valuation method to use.</span></span> <span data-ttu-id="1e9f0-110">Wenn das Fälligkeitsdatum weniger als ein Jahr nach dem Referenzdatum liegt, muss der Batchauftrag **Wechselkurse regulieren** mit der Bewertungsmethode für den niedrigsten Wert ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-110">If the due date is less than one year after the reference date, the **Adjust Exchange Rates** batch job must be run using the lowest value valuation method.</span></span>  

<span data-ttu-id="1e9f0-111">In der folgenden Tabelle werden die Bewertungsmethoden näher erläutert.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-111">The following table describes the valuation methods.</span></span>  

|<span data-ttu-id="1e9f0-112">Bewertungsmethode</span><span class="sxs-lookup"><span data-stu-id="1e9f0-112">Valuation method</span></span>|<span data-ttu-id="1e9f0-113">Description</span><span class="sxs-lookup"><span data-stu-id="1e9f0-113">Description</span></span>|  
|----------------------|---------------------------------------|  
|<span data-ttu-id="1e9f0-114">BilMoG (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="1e9f0-114">BilMoG (Germany)</span></span>|<span data-ttu-id="1e9f0-115">Beginnend mit dem Jahr 2010 wird jeder Sachkontoposten folgendermaßen reguliert:</span><span class="sxs-lookup"><span data-stu-id="1e9f0-115">Beginning in 2010, each ledger entry is adjusted as follows:</span></span><br /><br /> <span data-ttu-id="1e9f0-116">-   Wenn das Fälligkeitsdatum weniger als ein Jahr nach Referenzdatum liegt, werden Verbindlichkeits-/Forderungsbuchungen nach dem tatsächlichen Wechselkurs bewertet.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-116">-   If the due date is less than one year after the reference date, payable/receivable transactions are valued at the actual exchange rate.</span></span><br /><span data-ttu-id="1e9f0-117">-   Wenn das Fälligkeitsdatum mehr als ein Jahr nach dem Referenzatum liegt, werden Verbindlichkeits-/Forderungsbuchungen nach dem niedrigsten Wert bewertet, mit der Möglichkeit einer Aufwertung (Wertaufholung) bis um Ausgangswert.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-117">-   If the due date is more than one year after the reference date, payable/receivable transactions are valued at the lowest value, with the possibility of appreciation in value (Wertaufholung) up to the initial value.</span></span> <span data-ttu-id="1e9f0-118">**Hinweis:**  Sachkontoposten müssen ein Fälligkeitsdatum enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-118">**Note:**  Ledger entries must contain a due date.</span></span> <span data-ttu-id="1e9f0-119">Ein Posten, der kein Fälligkeitsdatum hat, wird als langfristige Verbindlichkeit behandelt.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-119">An entry that does not have a due date is treated as a long term liability.</span></span>|  
|<span data-ttu-id="1e9f0-120">Niedrigster Wert</span><span class="sxs-lookup"><span data-stu-id="1e9f0-120">Lowest value</span></span>|<span data-ttu-id="1e9f0-121">Wechselkurse werden unter Verwendung des niedrigsten Wertes der beiden Wechselkurse reguliert.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-121">Exchange rates are adjusted by using the lowest value of the two exchange rates.</span></span> <span data-ttu-id="1e9f0-122">Währungsverluste werden immer berechnet und gebucht.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-122">Currency losses are always calculated and posted.</span></span> <span data-ttu-id="1e9f0-123">Währungsgewinne werden nur bis zum ursprünglichen Landeswährungswert der Transaktion berechnet und gebucht.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-123">Currency gains are only calculated and posted up to the original local currency value of the transaction.</span></span><br /><br /> <span data-ttu-id="1e9f0-124">Dadurch wird sichergestellt, dass Forderungen nicht höher als ihre ursprünglichen Buchungsbeträge bewertet werden und dass Verbindlichkeiten nicht niedriger als ihre ursprünglichen Buchungsbeträge bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-124">This ensures that receivables are not valued above their original posting amounts, and that payables are not valued below their original posting amounts.</span></span>|  
|<span data-ttu-id="1e9f0-125">Standard</span><span class="sxs-lookup"><span data-stu-id="1e9f0-125">Standard</span></span>|<span data-ttu-id="1e9f0-126">Wechselkurse werden entsprechend den Standardbewertungsprinzipien reguliert.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-126">Exchange rates are adjusted according to standard valuation principles.</span></span> <span data-ttu-id="1e9f0-127">Volle unrealisierte Gewinne und Verluste werden berechnet und gebucht.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-127">Full unrealized gains and losses are calculated and posted.</span></span> <span data-ttu-id="1e9f0-128">Wenn die Transaktion teilweise angewendet wird, wird nur der Restbetrag in die Regulierung einbezogen.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-128">If the transaction is partially applied, only the remaining amount is included in the adjustment.</span></span> <span data-ttu-id="1e9f0-129">Weitere Informationen finden Sie unter „Wechselkurse regulieren”.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-129">For more information, see Adjust Exchange Rates.</span></span>|  

<span data-ttu-id="1e9f0-130">Deutsche Unternehmen müssen die Option **BilMoG (Deutschland)** verwenden, wenn sie den Batchauftrag **Wechselkurse regulieren** ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-130">German companies must use the **BilMoG (Germany)** option when they run the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="1e9f0-131">Dadurch ist sichergestellt, dass jede Transaktion mithilfe der entsprechenden Bewertungsmethode wie in Deutschland erforderlich reguliert wird.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-131">This ensures that each transaction is adjusted using the appropriate valuation method as required in Germany.</span></span> <span data-ttu-id="1e9f0-132">Dadurch werden außerdem zwei Felder im Anforderungsfenster aktiviert, in denen Sie die zwei Datumswerte angeben können, die verwendet werden müssen, um die Regulierung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-132">This also enables two fields in the request window, where you can specify the two dates that must be used to calculate the adjustment.</span></span> <span data-ttu-id="1e9f0-133">Die Felder werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-133">The following table describes the fields.</span></span>  

|<span data-ttu-id="1e9f0-134">Feld</span><span class="sxs-lookup"><span data-stu-id="1e9f0-134">Field</span></span>|<span data-ttu-id="1e9f0-135">Description</span><span class="sxs-lookup"><span data-stu-id="1e9f0-135">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="1e9f0-136">**Bewertungsreferenzdatum**</span><span class="sxs-lookup"><span data-stu-id="1e9f0-136">**Valuation Reference Date**</span></span>|<span data-ttu-id="1e9f0-137">Gibt das Basisdatum an, das verwendet wird, um zu berechnen, welche Posten kurzfristige Posten sind.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-137">Specifies the base date that is used to calculate which entries are short-term entries.</span></span>|  
|<span data-ttu-id="1e9f0-138">**Kurzfristige Verbindlichkeiten bis**</span><span class="sxs-lookup"><span data-stu-id="1e9f0-138">**Short term liabilities until**</span></span>|<span data-ttu-id="1e9f0-139">Gibt das Datum an, das kurzfristige Posten von langfristigen Posten trennt.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-139">Specifies the date that separates short-term entries from long-term entries.</span></span> <span data-ttu-id="1e9f0-140">Kurzfristige Posten können ein Fälligkeitsdatum aufweisen, das vor oder an diesem Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-140">Short-term entries have a due date that is before or on this date.</span></span> <span data-ttu-id="1e9f0-141">Der Standardwert ist der Wert des Feldes **Bewertungsreferenzdatum** plus ein Jahr.</span><span class="sxs-lookup"><span data-stu-id="1e9f0-141">The default value is the value of the **Valuation Reference Date** field plus one year.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="1e9f0-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e9f0-142">See Also</span></span>  
[<span data-ttu-id="1e9f0-143">Vorgehensweise: Aktualisieren von Währungswechselkursen</span><span class="sxs-lookup"><span data-stu-id="1e9f0-143">How to: Update Currency Exchange Rates</span></span>](../../finance-how-update-currencies.md)
