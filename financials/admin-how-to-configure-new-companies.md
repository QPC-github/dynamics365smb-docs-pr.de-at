---
title: 'Vorgehensweise: Konfigurieren neuer Unternehmen | Microsoft Docs'
description: "Sie können ein neues Unternehmen, das Sie erstellt haben, konfigurieren und anpassen. Um Ihre Implementierung abzustimmen, gehen Sie in drei Phasen vor, um die Konfiguration abzuschließen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f99f4f7576e72d1ca0fbc6ecaa51d6c7bc15aa9f
ms.contentlocale: de-at
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies"></a>So konfigurieren Sie einen neuen Mandanten.
Um einen neuen Mandanten in der Lösungsimplementierung zu konfigurieren, folgen Sie in der Regel drei Phasen. In der ersten Phase importieren Sie das Konfigurationspaket, eine .rapidstart-Datei mit den Konfigurationsinformationen. In der zweiten Phase ändern Sie die Konfigurationsinformationen und übernehmen sie dann für Ihren neuen Mandanten. In der letzten Phase überprüfen Sie auf Fehler und korrigieren diese.  

In den folgenden Verfahren wird davon ausgegangen, dass Sie ein Konfigurationspaket erstellt und gespeichert haben. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen eines Konfigurations-Paket](admin-how-to-prepare-a-configuration-package.md).  

Bevor Sie den folgenden Verfahren übernehmen, vergewissern Sie sich, dass Ihr neues Unternehmen initialisiert ist und Sie das RapidStart Services-Implementierer Rollencenter nutzen.

## <a name="to-import-a-configuration-package"></a>So importieren Sie ein Konfigurationspaket.  
1. Öffnen Sie das neue Unternehmen im [!INCLUDE[d365fin](includes/d365fin_md.md)] Datenbank.  
2. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationspaket** ein. Wählen Sie dann den zugehörigen Link aus.  
3. Wählen Sie die **Paket importieren**-Aktion aus.  
4. Navigieren Sie zum gewünschten Speicherort, in dem Sie die .rapidstart-Konfigurationspaketdatei gespeichert haben, und wählen Sie  **Öffnen** aus.  
5. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol "Nach Seite oder Bericht suchen"") aus, geben Sie **Unternehmensdaten** ein, und wählen Sie dann den verknüpften Link aus. Geben Sie Informationen über den Mandanten in der Mandanteninformationenkarte ein. Schließen Sie Informationen wie Bankdetails ein. Sie können ein Logo für den Mandanten bereitstellen.  

Alle Tabellen, die Sie zum Einschließen in den neuen Mandanten festgelegt haben, werden importiert. Zu diesem Zeitpunkt können Sie die Paketdaten zur Datenbank zuordnen, oder die Tabellendaten anpassen und ändern, um Ihren Debitorspezifikationen zu entsprechen.  

## <a name="to-apply-package-data"></a>So wenden Sie Paketdaten an  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie eine Tabelle, in das Sie Daten ändern möchten, und wählen die **Daten übernehmen** Aktion aus. Klicken Sie auf die Schaltfläche **Ja**, um die Anwendung zu bestätigen.
3. Um zu bestätigen dass die Daten nun in der Datenbank sind und dass die Anwendung erfolgreich war, kehren Sie zum Fenster **Arbeitsblatt konfigurieren**zurück und wählen die Aktion **Datenbank** aus.  

> [!NOTE]  
>  Nachdem Sie Daten zugeordnet haben, können Sie diese nur in der Datenbank anzeigen. Sie befinden sich nicht mehr im Paket.  

## <a name="to-modify-and-apply-package-data"></a>So können Sie Paketdaten ändern und zuordnen  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie eine Tabelle, in das Sie Daten ändern möchten, und wählen die **Datenpaket** Aktion aus.  
3. Im Fenster **Config. Paket-Datensätze** führen Sie Ihre Änderungen durch. Beispielsweise können Sie Optionen zu löschen, die nicht zutreffen.  
4. Wählen Sie die Schaltfläche **Daten anwenden** und dann die Schaltfläche **OK** aus.  
5. Um zu bestätigen dass die Daten nun in der Datenbank sind und dass die Anwendung erfolgreich war, kehren Sie zum Fenster **Arbeitsblatt konfigurieren**zurück und wählen die Aktion **Datenbank** aus.  

## <a name="to-locate-and-identify-a-configuration-error"></a>So lokalisieren und identifizieren Sie einen Konfigurationsfehler  
Es gibt bestimmte Arten von Fehlern, die auftreten können, wenn Sie Daten auf eine Datenbank anwenden. Der häufigste Fehler ist, nicht alle zugehörigen Tabellen, die erforderlich sind, eingeschlossen waren. Sie korrigieren solche Fehler im Konfigurationsvorschlag.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationspaket** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die fertig zu stellende Aktivität aus, und klicken Sie anschließend auf die Aktion **Bearbeiten**.  

    Jede Tabelle, die Fehler enthält, wird hervorgehoben. Die Anzahl der Paketfehlern wird im Feld **Anzahl Paket-Fehlern** wird im Feld angezeigt.  

3. Wählen Sie das Feld **Anzahl Paketfehler**, um das Fenster **Paket-Datensätze konfig.** zu öffnen, die die Liste der Datensätze mit Fehler aufführt.  

### <a name="to-fix-an-error"></a>So korrigieren Sie einen Fehler.  
1. Öffnen Sie den Mandanten, auf dem Sie Ihr Konfigurationspaket basierten.  
2. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
3. Korrigieren Sie Fehler und fügen Sie dem Arbeitsblatt fehlende verknüpfte Tabellen hinzu.  
4. Fügen Sie die Tabellen dem bestehenden Konfigurationspaket hinzu, oder erstellen Sie ein neues Paket, das nur die neuen Tabellen enthält. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen eines Konfigurations-Paket](admin-how-to-prepare-a-configuration-package.md).  
5. Öffnen Sie den neuen Mandanten, für den Sie die Konfiguration übernehmen, erneut.  
6. So importieren Sie das Konfigurationspaket.  

    > [!NOTE]  
    >  Wenn Sie das gleiche Paket wieder importieren, überschreiben Sie sämtliche Datenänderungen, die Sie bereits vorgenommen haben. Aus diesem Grund sollten Sie neue Tabellen in einem neuen Paket hinzufügen und dieses stattdessen importieren.  

7. Wenden Sie die Daten auf die Datenbank an, die im Abschnitt "Paketdatenen ändern und übernehmen " erläutert sind.

## <a name="see-also"></a>Siehe auch  
[Übernehmen von Konfiguration in neue Mandanten](admin-apply-configuration-to-new-companies.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
