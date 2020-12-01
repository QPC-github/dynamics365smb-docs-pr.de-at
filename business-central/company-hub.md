---
title: Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten
description: Erfahren Sie mehr über den Unternehmens-Hub in Dynamics 365 Business Central, mit dem Sie Ihre Arbeit unternehmensübergreifend verwalten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ed69f86a941a216ef948488d3756c06f298549d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-AT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927859"
---
# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten

Einige Personen arbeiten in mehreren Unternehmen in [!INCLUDE [prodshort](includes/prodshort.md)], und einige arbeiten auch in mehr als einer Organisation, beispielsweise externe Buchhalter oder Mitarbeiter und Manager von Unternehmen mit mehreren Tochterunternehmen. Für diese und viele andere Benutzer dient der Unternehmens-Hub als Landing Page, um die Arbeit in den verschiedenen Umgebungen, in denen sie arbeiten, über Unternehmen, Umgebungen und Regionen hinweg zu verwalten.  

Sie können auf den Unternehmens-Hub zugreifen, indem Sie zur Rolle **Unternehmens-Hub** in „Meine Einstellungen“ wechseln. Alternativ können Sie die Seite **Unternehmens-Hub** direkt öffnen. Sie können an beiden Stellen dieselbe Arbeit ausführen, die Aktionen in den Menüs sind jedoch etwas anders angeordnet.  

## <a name="company-hub-home-page"></a>Homepage des Unternehmens-Hubs

Wenn Sie die Rolle **Unternehmens-Hub** verwenden, wird auf Ihrer Homepage eine Liste der Unternehmen angezeigt, auf die Sie Zugriff haben, einschließlich Informationen zu KPI-Daten (Key Point of Interest) und Links zum Öffnen der einzelnen Unternehmen. Sie können das Dashboard anpassen, um die Datenpunkte zu zeigen, die Sie sehen möchten, indem Sie Spalten hinzufügen oder entfernen. Beispielsweise möchten Sie Steuern sehen, die fällig sind, wie viele offene Verkaufsbelege jedes Unternehmen hat oder die Anzahl der Einkaufsrechnungen, die nächste Woche fällig sind. Sie können die Ansicht konfigurieren, um Ihren Anforderungen zu entsprechen. Wenn Sie viele Unternehmen hinzugefügt haben, können Sie Filter setzen, um die Ansicht zu sortieren.  

Wählen Sie die Aktion **Unternehmens-Hub** aus, um den Unternehmens-Hub zu öffnen, in dem Sie enger mit den einzelnen Unternehmen zusammenarbeiten können.  

> [!TIP]
> Um auf ein bestimmtes Unternehmen in [!INCLUDE [prodshort](includes/prodshort.md)] zuzugreifen, wählen Sie den Namen des Unternehmens oder das Menüelement **Zu Unternehmen wechseln** aus. Sie werden dann automatisch in einer neuen Browserregisterkarte angemeldet.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Aktionen für ein Unternehmen, das im Unternehmens-Hub aufgeführt ist":::

Sie können neue Unternehmen hinzufügen, z. B. wenn Sie einen neuen Kunden erhalten oder wenn Ihr Unternehmen eine neue Tochtergesellschaft hinzufügt. Weitere Informationen finden Sie unter [Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu](company-hub-add-company.md).  

> [!TIP]
> Um die Daten im Unternehmens-Hub zu aktualisieren, müssen Sie Zugriff auf die Daten in den Unternehmen haben, von denen die Daten stammen.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Zugewiesene Aufgaben

In [!INCLUDE [prodshort](includes/prodshort.md)] können Sie sich selbst sowie anderen Aufgaben zuweisen, und andere Personen können Ihnen Aufgaben zuweisen. Der Unternehmens-Hub zeigt Ihnen eine Übersicht der zugewiesenen Aufgaben für jedes Unternehmen. Sie können ebenfalls auf eine Liste aller zugewiesenen Aufgaben zugreifen, indem Sie auf der Seite **Start** die Option **Meine Benutzeraufgaben** auswählen.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Meine Benutzeraufgaben

Die Liste **Meine Benutzeraufgaben** hilft Ihnen dabei, Ihren Tag zu priorisieren, indem weitere Informationen über die Aufgaben angezeigt werden, die Ihnen über alle Ihre Unternehmen hinweg zugewiesen wurden.  

Sie können z. B. nach Fälligkeitsdatum, oder einem beliebigen anderen Datentyp sortieren, der dabei hilft, den Tag zu priorisieren. Standardmäßig zeigt die Liste alle Aufgaben an, die Ihnen zugeordnet wurden, aber Sie können Filter setzen, um z.B. nur Aufgaben anzuzeigen, die mit hoher Priorität markiert wurden.  

Um eine Aufgabe aufzunehmen, wählen Sie sie einfach aus der Liste der ausstehenden Benutzeraufgaben aus. Im Menüband öffnet der Link **Zu Aufgabenelement wechseln** die Seite, in dem Sie die Arbeit ausführen können.  

Wenn Sie eine Aufgabe abgeschlossen haben, kennzeichnen Sie sie einfach als abgeschlossen.  

Weitere Informationen zu Unternehmen und Umgebungen finden Sie unter [Umgebungslinks](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Auf den Unternehmens-Hub zugreifen

Um auf den Unternehmens-Hub zugreifen zu können, müssen Sie entweder über die *D365-UNTERNEHMENS-HUB* -Benutzergruppe oder über den *D365-UNTERNEHMENS-HUB* -Berechtigungssatz Zugriff haben. Sie müssen auch Zugriff auf die Unternehmen haben, die in Ihrem Unternehmens-Hub aufgeführt sind. Dies bedeutet, dass Sie ein Benutzer in diesen Unternehmen sein müssen. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Der Unternehmens-Hub ist eine unternehmensweite Liste. Daher kann jeder Benutzer, dem Zugriff auf den Unternehmens-Hub gewährt wird, alle Unternehmen in seinem eigenen [!INCLUDE [prodshort](includes/prodshort.md)]-Tenant sowie alle KPIs für die Unternehmen, auf die sie Zugriff haben, sehen.

Falls Sie den Unternehmens-Hub nicht finden können und sich sicher sind, dass Ihnen Zugriff darauf gewährt wurde, wenden Sie sich an Ihren Administrator, wenn der Unternehmens-Hub auf der Seite **Erweiterungsmanagement** aufgeführt ist. Weitere Informationen finden Sie unter [Anpassen von Business Central über Erweiterungen](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Unternehmens-Hub einrichten

Um den Unternehmens-Hub verwenden zu können, müssen Sie Ihrem Dashboard ein oder mehrere Unternehmen hinzufügen. Weitere Informationen finden Sie unter [Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu](company-hub-add-company.md).  

Sie können jedoch nur dann ein Unternehmen hinzufügen, wenn Ihnen Zugriff auf eine oder mehrere Instanzen von [!INCLUDE [prodshort](includes/prodshort.md)] sowie auf das Unternehmen gewährt wurde, in dem Sie den Unternehmens-Hub verwenden.  

Wenn Sie beispielsweise Buchhalter sind, können Ihre Kunden Sie in ihr [!INCLUDE [prodshort](includes/prodshort.md)] einladen. Weitere Informationen finden Sie unter [Ihren externen Buchhalter in Ihr Business Central einladen](finance-accounting.md#inviteaccountant).  

Administratoren können dieselbe Anleitung zur unterstützten Einrichtung verwenden, um Sie zu ihrem [!INCLUDE [prodshort](includes/prodshort.md)] hinzuzufügen. Sie können Sie auch zum entsprechenden Azure AD-Konto im Microsoft 365 Admin Center hinzufügen. Weitere Informationen finden Sie unter [Benutzer und Gruppen verwalten](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Siehe auch

[Fügen Sie Unternehmen zu Ihrem Unternehmens-Hub hinzu](company-hub-add-company.md)  
[Buchhaltungs-Erfahrung in Business Central](finance-accounting.md)  
[Die Erweiterung Unternehmens-Hub für Business Central](ui-extensions-company-hub.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  