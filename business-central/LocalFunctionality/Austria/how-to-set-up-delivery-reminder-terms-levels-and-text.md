---
title: 'Gewusst wie: Einrichten von Lieferbenachrichtigungsmethoden, -stufen und -text'
description: "Zur Erstellung von Lieferbenachrichtigungen müssen Sie bestimmte Dinge einrichten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e5e7c699cb743b1a45780005d1429a1baf93f716
ms.contentlocale: de-at
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-delivery-reminder-terms-levels-and-text"></a>Einrichten von Lieferbenachrichtigungsbestimmungen, Stufen und Text
Zur Erstellung von Lieferbenachrichtigungen müssen Sie Folgendes einrichten:  

- Lieferbenachrichtigungsmethoden  
- Lieferbenachrichtigungsstufen  
- Lieferbenachrichtigungstexte  

Jede Lieferbenachrichtigungsmethoden verfügt über mindestens zwei Lieferbenachrichtigungsstufe und für jede Lieferbenachrichtigungsstufe können Sie Text angeben, der in die Lieferbenachrichtigung aufgenommen wird.  

Weitere Informationen finden Sie unter [Lieferbenachrichtigungen](delivery-reminders.md).  

## <a name="to-set-up-delivery-reminder-terms"></a>So richten Sie Lieferbenachrichtigungsmethoden ein  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen"), geben Sie **Lieferbenachrichtigungsmethoden** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Der Code für die Lieferbenachrichtigungsmethode. Sie können bis zu 10 alphanumerische Zeichen eingeben.|  
    |**Beschreibung**|Der Beschreibung für die Lieferbenachrichtigungsmethode. Sie können bis zu 30 alphanumerische Zeichen eingeben.|  
    |**Max. Anzahl Lieferbenachrichtigungen**|Die maximale Anzahl von Lieferbenachrichtigungen, die für eine Bestellung erstellt werden kann.<br /><br /> **HINWEIS:** Diese Höchstgrenze gilt für alle Benachrichtigungsstufen dieser Benachrichtigungsmethode zusammen. Wenn Sie z. B. drei Stufen definiert haben und **Max. Anzahl Lieferbenachrichtigungen** auf 5 festlegen, wird die erste Mahnung auf Stufe 1, die Zweite auf Stufe 2, die Dritte auf Stufe 3 erstellt.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-add-delivery-reminder-levels-to-a-delivery-reminder-term"></a>So fügen Sie einer Lieferanmahnungsmethode Lieferanmahnungsstufen hinzu  

1.  Wählen Sie im Fenster **Lieferbenachrichtigungsmethoden** die Lieferbenachrichtigung aus, der Sie Stufen hinzufügen möchten, und wählen Sie dann die Aktion **Bearbeiten**.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nr.**|Die Nummer der Lieferbenachrichtigungsstufe. Dieses Feld wird automatisch ausgefüllt.|  
    |**Berechnung Fälligkeitsdatum**|Die Formel für die Fälligkeitsdatumsberechnung der Lieferbenachrichtigung. Sie können eine Kombination von Zahlen zwischen 0 und 9999 sowie Datumscodes (T für Tag, WT für Wochentag, W für Woche, M für Monat, Q für Quartal oder J für Jahr) eingeben. Die Datumscodes bezeichnen die Berechnung desFälligkeitsdatums der Lieferbenachrichtigung fest. Sie können bis zu 20 Zeichen für die Berechnungsformel für den Fälligkeitstermin eingeben.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

Für jede Lieferbenachrichtigungsstufe können Sie Textnachrichtigen definieren, die der Lieferbenachrichtigung hinzugefügt werden. Sie können Vortext definieren, der vor der Beschreibung der überfälligen Bestellung eingefügt wird, und Nachtext, der nach der Beschreibung der überfälligen Bestellung eingefügt wird.  

Im folgenden Verfahren wird beschrieben, wie Sie den Vortext einrichten. Diese Schritte gelten jedoch auch für das Einrichten von Nachtexten.  

## <a name="to-set-up-delivery-reminder-text-messages"></a>Einrichten von Lieferbenachrichtigungstexten  

1.  Wählen Sie im Fenster **Lieferbenachrichtigungsstufen** eine Stufe aus, und wählen Sie dann die Aktion **Vortext**.  
2.  Wählen Sie die Aktion **Neu**.  
3.  Geben Sie im Feld **Beschreibung** den Vortext für die Lieferbenachrichtigung ein.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
 [Lieferanmahnungen](delivery-reminders.md)   
 [Gewusst wie: Einrichten von Lieferbenachrichtigungen](how-to-set-up-delivery-reminders.md)   
 [So werden Lieferbenachrichtigungscodes zu Kreditoren zugewiesen](how-to-assign-delivery-reminder-codes-to-vendors.md)   
 [So erstellen Sie Lieferanmahnungen manuell](how-to-create-delivery-reminders-manually.md)   
 [Lieferbenachrichtigung registrieren](how-to-issue-delivery-reminders.md)
