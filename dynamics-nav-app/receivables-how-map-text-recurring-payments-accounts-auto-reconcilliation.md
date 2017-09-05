---
title: 'Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung'
author: SorenGP
ms.custom: na
ms.date: 09/22/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics-nav-2017
ms.translationtype: Human Translation
ms.sourcegitcommit: 51adfb3588099c496f0946ff71da5c6fe518f070
ms.openlocfilehash: 7f9bf8b0550f7da1cced995234e15ad7aab484ba
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017

---

# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung
Im Fenster **Zuordnung Text zu Konto**, das Sie im Fenster **Zahlungsabstimmungsbuch.-Blatt** öffnen, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungsbuch.-Blatt buchen.

**Hinweis**: Dieses Thema bezieht sich auch auf die Verwendung der Funktion **Text zu Konto zuordnen** bei einem Eingangsbeleg, um das Konvertieren von elektronischen Belegen von Fremdleistungen in Belege in Dynamics NAV zu unterstützen. Weitere Informationen finden Sie unter [So gehts: Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).   

Ähnliche Funktionen sind vorhanden, um Mehrbeträge auf Zahlungsabstimmungsbuch.-Blattzeilen fallweise abzustimmen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Zuordnung](receivables-how-reconcile-payments-cannot-apply-auto.md).

Die Zahlungen, die anhand der Text-zu-Kontenzuordnung gebucht wurden, werden nicht auf offene Einträge angewendet, sondern sie werden nur für die angegebenen Konten sowie das Erstellen von Bankposten gebucht. Entsprechend eignet sich die Text-zu-Konto-Zuordnung für wiederkehrende Zahlungseingänge oder Ausgaben wie häufig auftretende Einkäufe von Autobrennstoff, Bankgebühren und Zinsen, die regelmäßig im Bankkontoauszug auftreten und kein zugehöriges Geschäftsdokument benötigen. Weitere Informationen finden Sie im Abschnitt “Beispiel - Text-zu-Konten-Zuordnung für Brennstoff-Ausgaben” in diesem Thema.

**Hinweis**: Zahlungen auf Abstimmungsbuch.-Blattzeilen werden nur dann für das Buchen entsprechend der Text-zu-Kontenzuordnung festgelegt, wenn die automatische Anwendungsfunktion lediglich eine Abgleichungsfrage zwischen **Niedrig** und **Mittel** darstellt. Wenn die automatische Anwendungsfunktion eine Übereinstimmungsgenauigkeit von "Hoch" liefert, wird die Zahlung eines oder mehrerer offener Posten automatisch angewendet, und die Zahlung wird nicht auf die Konten gebucht, die im Fenster **Zuordnung Text zu Konto** angegeben wurde. Anders ausgedrückt, ein Abgleichungsvertrauen **Hoch** überschreibt eine Text-zu-Konto-Zuordnung.

In einer Zahlungsabstimmungsbuch.-Blattzeile, in der die Zahlung entsprechend der Text-zu-Kontenzuordnung zur Buchung festgelegt wurde, enthält das Feld **Übereinstimmungsgenauigkeit** **Hoch - Text-Kontozuordnung** und den **Kontenart** und die **Kontennummer**. Felder enthalten die zugehörigen Konten.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Zuordnen von text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung
1. Wählen Sie in der rechten oberen Ecke das Symbol **Nach Seite oder Bericht suchen** und geben **Zahlungsabstimmungsbuch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie ein Zahlungsabstimmungsbuch.-Blatt. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Wählen Sie die Aktion **Text zu Konto zuordnen**. Das Fenster **Text zu Konto zuordnen** öffnet sich.
4. Geben Sie im Feld **Text zuordnen** einen beliebigen Text ein, der in Zahlungen auftritt, die Sie an die angegebenen Konten ohne Anwendung auf einen offenen Posten buchen möchten. Sie können bis zu 50 Zeichen eingeben.

    **Hinweis**: Wenn keine anderen Zahlungen oder eingehende Belege mit dem jeweiligen Zuordnungstext vorhanden sind, dann erfolgt die Text-Konto-Zuordnung auch, wenn nur ein Teil des Texts auf der Zahlung oder den eingehenden Beleg als Zuordnungstext vorhanden ist.
5. Im Feld **Kreditorennr** geben Sie die Nummer des Kreditors an, für den eingehende Belege erstellt werden, die den Zuordnungstext enthalten, oder auf den diese Zahlungen gebucht werden. Weitere Informationen finden Sie unter [So gehts: Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).      
6. Im **Sollkonto Nr.** Feld geben Sie im Konto ein, dass Zahlungen, die den Zuordnungstext enthalten, gebucht werden, wenn diese eingehende Zahlungen sind. Für eingehende Zahlungen ist das Vorzeichen des Werts im Feld **Auszugsbetrag** positiv.
7. Im **Kreditkonto Nr.** Feld geben Sie im Konto ein, dass Zahlungen, die den Zuordnungstext enthalten, gebucht werden, wenn diese ausgehende Zahlungen sind. Für ausgehende Zahlungen ist das Vorzeichen des Werts im Feld **Auszugsbetrag** negativ.
8. Geben Sie im Feld **Herkunftsart Saldo** an, ob die Zahlung auf ein Sachkonto oder auf ein Debitoren- oder Kreditorenkonto gebucht wird.
9. Im Feld **Herkunftsart Saldo** Feld definieren Sie das Konto, auf das die Zahlung gebucht wird, abhängig von Ihrer Wahl im Feld **Herkunftsart Saldo**.
10. Wiederholen Sie die Schritte 4 bis 8 für alle Texte auf Zahlungen, die Sie zuordnen möchten, um die entsprechenden Posten direkt, ohne Anwendung, zu buchen.

Beim nächsten Mal, wenn Sie eine Bankkontoauszugsdatei importieren oder die Funktion **Automatisch anwenden** im Fenster **Zahlungsabstimmungsbuch.-Blatt** wählen, enthalten die Buch.-Blattzeilen für die Zahlungen, die den angegebenen Zuordnungstext enthalten, die zugehörigen Konten im Feld **Kontoart** und **Kontonummer**. Felder. Das Feld **Übereinstimmungsgenauigkeit** enthält **Hoch - Text zu Konto Zuordnung**. Dies ist unter der Bedingung der Fall, dass die automatische Anwendungsfunktion nur ein Abgleichungsvertrauen von **Niedrig** oder **Normal** zur Verfügung stellen kann.

##<a name="example-text-to-account-mapping-for-fuel-expense"></a>Beispiel: Text-zu-Konto-Zuordnung für Brennstoff-Ausgaben

Um die Brennstoffausgaben an Shell-Tankstellen immer in das Sachkonto für Benzin (Konto 8510) zu buchen, füllen Sie eine Zeile im Fenster **Text-zu-Konto-Zuordnung** wie folgt aus.

|Abbildungstext |Sollkonto Nr. |Habenkonto Nr. |Saldo Herkunftsart |Saldo Herkunftsnr. |
|-------------|---------------|----------------|-----------------|----------------|
|Shell |LEER |8510 |Sachkonto|LEER|

**Tipp**: Weitere Informationen darüber, wie mit Feldern und Spalten gearbeitet wird, finden Sie unter [Arbeiten mit Dynamics NAV](ui-work-product.md). Weitere Informationen zur Suche nach spezifischen Seiten finden Sie unter [Suche](ui-search.md).

## <a name="see-also"></a>Siehe auch
[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf verwalten](sales-manage-sales.md)  
[Gewusst wie: Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md)  
[Anpassen des Dynamics NAV mithilfe der Erweiterungen](ui-extensions.md)
