---
title: So bereiten Sie ein  Konfigurations-Paket vor  | Microsoft Docs
description: "Wenn Sie einen neues Mandant konfigurieren, werden Tabellenrelationen festgestellt und verarbeitet. Daten werden in der richtigen Reihenfolge importiert und übernommen. Dimensionstabellen werden auch importiert, wenn sie im Konfigurationspaket enthalten sind."
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
ms.openlocfilehash: 02192888f95f8136e349764227e0bf1aac91c5d1
ms.contentlocale: de-at
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-a-configuration-package"></a>So bereiten Sie ein Konfigurationspaket vofr
Wenn Sie einen neues Mandant konfigurieren, werden Tabellenrelationen festgestellt und verarbeitet. Daten werden in der richtigen Reihenfolge importiert und übernommen. Dimensionstabellen werden auch importiert, wenn sie im Konfigurationspaket enthalten sind.  

Um Ihrem Debitoren zu helfen, das Konfigurationspaket zu verwenden, können Sie dem Paket einen Fragebogen oder einen Satz von Fragebogen hinzufügen. Der Fragebogen kann dem Debitor beim Verständnis der verschiedenen Setupoptionen helfen. Üblicherweise werden Fragebögen für die größten Einrichtungstabellen in  erstellt, wenn ein Debitor weitere Anleitung dazu anfordert, wie eine entsprechende Einstellung wählen soll. Weitere Informationen finden Sie unter [Sammeln von Debitoren-Einrichtungswerte](admin-gather-customer-setup-values.md).

Vergewissern Sie sich, dass Sie sich auf der RapidStart Services-Implementierer-Rollencenterseite für den Basismandanten befinden. Weitere Informationen finden Sie unter [So verwenden Sie das RapidStart Service Implementer Rollencenter, um den Status zu verfolgen.](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md)

> [!IMPORTANT]  
>  Wenn Sie Konfigurationspakete zwischen zwei Mandantendatenbanken exportieren und importieren, sollten die Datenbanken dasselbe Schema haben, damit sichergestellt ist, dass alle Daten erfolgreich übertragen werden. Das bedeutet, dass die Datenbanken dieselbe Tabelle und Feldstruktur aufweisen sollten, wobei die Tabellen dieselben Primärschlüssel und die Felder dieselben IDs und Datentypen haben.  
>   
>  Sie können ein Konfigurationspaket importieren, das aus einer Datenbank exportiert wurde, die ein anderes Schema als die Zieldatenbank hat. Allerdings werden Tabellen oder Felder im Konfigurationspaket, die in der Zieldatenbank fehlen, nicht importiert. Tabellen mit unterschiedlichen Primärschlüsseln und Felder mit unterschiedlichen Datentypen werden ebenfalls nicht erfolgreich importiert. Wenn das Konfigurationspaket beispielsweise die Tabelle **Debitor 50000** mit dem Primärschlüssel **Code20** enthält und die Datenbank, in die Sie das Paket importieren die Tabelle **Debitor Bankkonto 50000** mit dem Primärschlüssel **Code20 + Code 20** enthält, werden diese Daten nicht importiert.  

## <a name="to-create-a-configuration-package"></a>So erstellen Sie ein Konfigurationspaket.  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationspaket** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die restlichen Felder auf dem Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Um die Konfigurationsfragebögen, Konfigurationsvorlagen und Konfigurationsarbeitsblatttabellen aus dem Paket auszuschließen, wählen Sie das Kontrollkästchen **Konfigurationstabellen ausschließen**. Andernfalls werden diese Tabellen automatisch der Liste der Pakettabellen hinzugefügt, wenn Sie das Paket exportieren.  
5. Wählen Sie die Aktion **Tabellen abrufen** aus. Das Batchauftragsfenster **Tabellenpaket abrufen** wird geöffnet.  
6. Wählen Sie das Feld **Tabellen auswählen** aus. Das Fenster **Konfigurationsauswahl** wird geöffnet.  
7. Wählen Sie auf der Registerkarte Start in der Gruppe Vorgang die Option **Alles auswählen**, um alle Tabellen dem Paket hinzuzufügen, oder wählen Sie das Kontrollkästchen **Ausgewählt** für jede Tabelle in der Liste aus, die Sie hinzufügen möchten.
8. Wählen Sie die Schaltfläche **OK** aus. Die Anzahl der Tabellen, die Sie ausgewählt haben, wird im Feld **Tabellen auswählen** angegeben. Geben Sie die Zusatzfunktionen an und wählen Sie dann die Schaltfläche **OK** aus. [!INCLUDE[d365fin](includes/d365fin_md.md)] Tabellen werden in den Zeilen der Karte **Config. Paket** hinzugefügt.  

    > [!NOTE]  
    >  Diese Einstellung kann auch im Konfigurationsarbeitsblatt vorgenommen werden. Wählen Sie die Tabellen aus, die Sie in das Paket einschließen möchten, und wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Paket zuweisen**.

9. Um die Felder auszuwählen, die Sie einer Tabelle berücksichtigen möchten, wählen Sie Tabelle aus, und wählen Sie auf der Symbolleiste **Zeilen** im Menü Tabelle die Option **Felder**.
Geben Sie an, welche Felder im Paket enthalten sind. Standardmäßig sind alle Felder enthalten.

    - Um nur die Felder auszuwählen die Sie hinzufügen möchten, wählen Sie die **Eingeschlossene löschen** Aktion. Um alle Felder hinzuzufügen, wählen Sie **Eingeschlossene festlegen**.  
    - Um festzulegen, dass die Felddaten nicht bestätigt werden sollen, löschen Sie das Kontrollkästchen **Feld überprüfen** für das Feld.  

10. Bestimmen, ob Sie mögiche Fehler gemacht haben, indem Sie die **Paket überprüfen** Aktion auswählen. Dies kann eintreten, wenn Sie Tabellen nicht einschließen, auf denen die Konfiguration beruht.  
11. Wählen Sie die Schaltfläche **OK**.  

Nachdem Sie die Liste der Felder, die von einer Tabelle enthalten sein sollen, neu definiert haben, können Sie die Ergebnisse in Excel prüfen.  

### <a name="to-filter-and-review-your-dataset"></a>So filtern und überprüfen Sie Ihr Dataset.  
1. Um einen bestimmten Satz von Datensätzen zu filtern, um ihn im Konfigurationsarbeitsblatt zu berücksichtigen, wählen Sie auf der Registerkarte **Zeilen** die Option f**Filter** und definieren Sie dann den entsprechenden Filterwert.  
2. Wählen Sie auf der Paketkarte auf der Symbolleiste **Zeilen** im Menü Excel die Option **Nach Excel exportieren**.  
3. Bestätigen Sie die Meldungen, die das Exportieren von Daten nach Excel aktivieren. Die genannte XLSX-Datei wird geöffnet. Überprüfen Sie die Daten, die exportiert wurden.  
4. Schließen Sie Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>So schließen Sie eine Vorlage zum Übernehmen für eine Tabelle ein.  
Bei bestimmten Tabellen etwa eine, die Stammdaten enthält, können Sie eine Vorlage angeben, die auf die Daten angewendet wird. Die Vorlage kann die erforderlichen Felder enthalten, die Sie für alle Stammdaten übernehmen möchten und die niemals variieren sollen. Beispielsweise können Sie eine Vorlage erstellen, die mit Debitorendaten verwendet werden kann. Eine Vorlage kann alle erforderlichen Felder enthalten, die anschließend das konsistente Importieren von standardisierten Informationen ermöglicht. Informationen wie Debitorennamen, die nicht standardisiert werden können, werden dann verarbeitet, wenn Sie einen Importier von Debitorendaten durchführen

1. Wählen Sie im Fenster **Paketkarte konfigurieren** eine Tabelle aus, und wählen Sie das Feld **Datenvorlage** aus. Eine Liste von Vorlagen wird angezeigt, die auf der Tabelle basieren.
2. Wählen Sie eine Vorlage aus, und wählen Sie dann die Schaltfläche **OK**.  

Nachdem das Paket vollständig ist, verwenden Sie den folgenden Vorgang, um das Paket in eine Datei zu speichern. Sie können das Paket einem Debitor oder einem Partnerunternehmen zu Verwendung geben.

### <a name="to-save-and-export-a-configuration-package"></a>So speichern und exportieren Sie ein Konfigurationspaket.  
- Im Fenster **Config. Paketkarte** wählen Sie die **Paket exportieren** Aktion aus.  

Das Paket wird in einer .rapidstart-Datei erstellt werden, die Paketinhalte in einem komprimierten Format bereitstellt. Konfigurationsfragebögen, Konfigurationsvorlagen und das Konfigurationsarbeitsblatt werden dem Paket automatisch hinzugefügt, es sei denn, Sie sich speziell dafür entscheiden, sie auszuschließen.  

Sie können die Datei mit einem Namen speichern, der Ihnen sinnvoll ist, aber Sie können die Dateierweiterung der Datei nicht ändern. Es muss .rapidstart sein.  

### <a name="to-copy-a-configuration-package"></a>So kopieren Sie ein Konfigurationspaket.  
Nachdem Sie ein Paket erstellt haben, das die meisten Ihrer Anforderungen erfüllt, können Sie es als Basis für die Erstellung von ähnlichen Paketen verwenden. Dies kann die Implementierungszeit verkürzen und erhöht den Wiederholbarkeitsaspekt von RapidStart Services.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurationspaket** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein Paket aus der Liste und wählen sie die Aktion **Pakt kopieren** aus.  
3. Geben Sie in dem Feld **Neuer Paketcode** einen Code für das neue Paket ein.  
4. Aktivieren Sie das Kontrollkästchen **Daten kopieren**, wenn Sie auch Datenbankdaten aus dem vorhandenen Paket kopieren möchten.  
5. Wählen Sie die Schaltfläche **OK**.

## <a name="to-customize-a-configuration-package"></a>So passen Sie ein Konfigurationspaket an.
Verwenden Sie das Konfigurationsarbeitsblatt, um Informationen zu sammeln und zu kategorisieren, die Sie verwenden möchten, um einen neuen Mandanten zu konfigurieren und Tabellen auf eine logische Art anzuordnen. Die Formatierung im Arbeitsblatt basiert auf einer einfachen Hierarchie: Bereiche enthalten Gruppen, die wiederum Tabellen enthalten. Bereiche und Gruppen sind optional, sie sind jedoch notwendig, wenn Sie in der Lage sein möchten, eine Übersicht des Konfigurationsprozesses im RapidStart Services-Rollencenter anzuzeigen.

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Feld **Zeilenart** die Option **Bereich** aus. Geben Sie im Feld **Name** einen beschreibenden Namen ein.  
3.  Wählen Sie im Feld **Zeilenart** die Option **Gruppe** aus. Geben Sie im Feld **Name** einen beschreibenden Namen ein.  
4.  Wählen Sie im Feld **Zeilenart** die Option **Tabelle** aus. Geben Sie im Feld **Tabellen-ID** die Tabelle ein, die im Arbeitsblatt berücksichtigt werden soll.  

Jetzt können Sie die Tabellen bestimmten Konfigurationspaketen zuweisen, die Sie erstellt haben oder zu erstellen planen. Weitere Informationen finden Sie unter Vorgehensweise: Zuordnen von Tabellen zu einem Konfigurations-Paket.

## <a name="to-work-with-promoted-tables"></a>So arbeiten Sie mit heraufgestuften Tabellen.  
1. Wählen Sie das Kontrollkästchen **Höhergestufte Tabelle**, um eine Tabelle anzugeben, die häufig während des Setupprozesses von einem typischen Debitor verwendet wird, beispielsweise die Tabelle **Sachkonto**. Wenn eine Tabelle diese Bezeichnung hat, kann ein Debitor das Arbeitsblatt leicht filtern, um nur die Liste der höhergestuften Tabellen anzuzeigen, die Aufmerksamkeit erfordern.  
2. Um eine gefilterte Ansicht anzuzeigen, wählen Sie die **Nur heraufgestufte** Aktion. Die Liste enthält nur die Tabellen, deren Kontrollkästchen aktiviert ist.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>So weisen Sie eine Tabelle einem Konfigurationspaket zu.  
Nachdem Sie die Tabellen festgelegt haben, die Sie als Teil der Konfiguration behanden möchten, können Sie die Tabellen einfach den Konfigurationspaketen zuweisen. Sie können eine Tabelle nur einem Paket zuweisen. Im folgenden Verfahren weisen Sie das Paket aus dem Kontext des Konfigurationsarbeitsblatts zu.  

> [!NOTE]  
>  Sie können ein Paket auch direkt erstellen und ihm Tabellen hinzufügen. Weitere Informationen zum Erstellen einer Vorlage finden Sie unter Vorgehensweise: Ein Konfigurationspaket erstellen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Konfigurationsarbeitsblatt eine Zeile oder mehrere Zeilen aus, die Sie einem Konfigurationspaket zuordnen möchten und wählen Sie **Paket zuweisen**.  
3.  Wählen Sie ein Paket in der Liste aus, oder wählen Sie die **Neu** Aktion aus, um ein Paket neu zu erstellen, und wählen Sie dann die Schaltfläche **OK** aus.  

    Wenn eine Tabelle nicht bereits im Paket enthalten ist, wird sie diesem jetzt hinzugefügt. Das Paketcodefeld in der Arbeitsblattzeile wird mit dem Code des Pakets ausgefüllt, dem die Tabelle zugeordnet ist.  
4. Wenn Sie eine vorhandenes Paket auswählen, können Sie sehen, wie viele Tabellen bereits im Paket sind, indem Sie die Informationen im Feld **Anzahl Tabellen** zur Kenntnis nehmen.

## <a name="to-review-or-customize-existing-database-data"></a>So können Sie vorhandene Datenbank-Daten prüfen und anpassen.
Wenn Sie ein Konfigurationspaket für eine Lösung erstellen, können Sie die verfügbaren Datenbankdaten anzeigen und anpassen, um Ihren Debitoranforderungen entsprechen. Die Datenbanktabelle muss eine zugeordnete Seite haben.  

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Identifizieren Sie im Konfigurationsarbeitsblatt die Tabellen, deren Daten Sie anzeigen oder anpassen möchten.  

    > [!NOTE]  
    >  Stellen Sie sicher, dass jede Tabelle eine Seiten-ID hat, die ihr zugeordnet ist. Für Standard [!INCLUDE[d365fin](includes/d365fin_md.md)]-Tabellen wird dieser Wert automatisch ausgefüllt. Für benutzerdefinierte Tabellen müssen Sie die ID zur Verfügung stellen

3. Wählen Sie die **Datenbankdaten** Aktion aus. Das Fenster für die zugehörige Seite wird geöffnet.
4. Überprüfen Sie die verfügbaren Informationen. Ändern Sie sie bei Bedarf, indem Sie Datensätze löschen, die nicht relevant sind oder indem Sie neue hinzufügen.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>So kopieren Sie Daten aus der Testumgebung in die Produktionsumgebung  
Nachdem Sie alle Ihre Setupinformationen untersucht und getestet haben, können Sie mit dem Kopieren von Daten in Ihre Produktionsumgebung fortfahren. Erstellen Sie in derselben Datenbank einen neuen Mandanten.

1. Öffnen und initialisieren Sie den neuen Mandanten.  
2. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Konfigurations-Arbeitsblatt** ein. Wählen Sie dann den zugehörigen Link aus.  
3. Wählen Sie **Daten vom Mandanten kopieren**.  
4. Wählen Sie im Fenster **Mandantendaten kopieren** das Feld **Kopieren von** aus. Das Fenster **Mandanten** wird geöffnet.  
5. Wählen Sie die Version aus, den Sie kopieren möchten, und wählen Sie die Schaltfläche **OK**. Ein Liste der im Konfigurationsarbeitsblatt ausgewählten Tabellen wird geöffnet. Nur Tabellen, die Datensätze enthalten, sind in dieser Übersicht enthalten.
6. Wählen Sie die Tabellen aus, aus denen Sie Daten kopieren möchten, und wählen Sie **Daten kopieren**. Wählen Sie im Fenster **Mandantendaten kopieren** die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
[Sammeln von Einrichtungswerten für Debitoren](admin-gather-customer-setup-values.md)  
[Richten Sie eine Unternehmenskonfiguration ein.](admin-set-up-company-configuration.md)  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
