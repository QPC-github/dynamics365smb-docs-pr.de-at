---
title: Senden von Belegen und E-Mails
description: 'Sie können Inhalt definieren, um in den Text eine E-Mail beispielsweise ein PayPal-Link einzufügen. Bestellanforderungen können auch Belege an eine E-Mail-Nachricht angehängt werden.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'SMTP, mail, Microsoft 365, cover, body, PayPal, layout'
ms.search.form: null
ms.date: 04/01/2021
ms.author: edupont
---
# Senden von Belegen und E-Mails

Sie können Informationen und Belege, wie z.B. Bestellungen, Verkaufsaufträge und Rechnungen, ganz einfach per E-Mail direkt von [!INCLUDE[prod_short](includes/prod_short.md)] aus weitergeben, ohne eine E-Mail App öffnen zu müssen.  

Sie können fast alle Arten von Dokumenten als PDF-Anhänge senden. Alternativ können Sie ein Berichtslayout einrichten, das Informationen aus dem Dokument im E-Mail-Text sowie Text enthält, der die E-Mail benutzerfreundlicher macht, z. B. eine Standardbegrüßung. Weitere Informationen finden Sie unter [Berichte- und Dokumentenlayouts verwalten](ui-manage-report-layouts.md). <!--this topic does not mention how to set up a layout for email. Need to investigate.-->

Wenn Sie Rechnungen senden, können Sie Kunden das Bezahlen über einen Zahlungsdienst wie PayPal erleichtern, indem Sie automatisch Informationen und einen Link zum Dienst in die E-Mail einfügen. Weitere Informationen finden Sie unter [Aktivieren Sie Zahlungen durch Zahlungsverkehr](sales-how-enable-payment-service-extensions.md)

Um E-Mails aus [!INCLUDE[prod_short](includes/prod_short.md)] zu aktivieren starten Sie den Leitfaden zur unterstützten Einrichtung **E-Mail einrichten** im Rollencenter. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt nur ausgehende E-Mail-Kommunikation. Sie können auch keine Antworten aus der App erhalten.

## Senden von Belegen über E-Mail

In diesem Verfahren wird beschrieben, wie Sie eine gebuchte Verkaufsrechnung als PDF-Datei und mit dokumentenspezifischem E-Mail-Text an eine E-Mail anhängen. <!--update this-->

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Gebuchte Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.
2. Markieren Sie die Rechnung, wählen Sie die Aktion **Drucken/Senden**, und wählen Sie dann **Senden**.
3. Wählen Sie dann im Feld **E-Mail** **Ja (Aufforderung für Einstellung)** aus. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).
    
    Wenn das Feld **E-Mail** auf der Seite **Dokument senden an** auf **Ja festgelegt wurde (Aufforderung für Einstellungen)**, dann wird die Seite **Senden per E-Mail** geöffnet und mit der Kontaktperson im Feld **Zu** ergänzt und das Dokument als PDF-Datei angehängt. Geben Sie im Feld **Text** entweder den Text manuell ein oder Sie können definieren, dass das Feld mit einem belegspezifischen E-Mail-Text ausgefüllt wird, den Sie eingerichtet haben.

4. Wählen Sie die Schaltfläche **OK** aus.
5. Im Feld **Zu** geben Sie eine gültige E-Mail-Adresse ein. Der Standardwert ist die E-Mail-Adresse des Debitors.
6. Geben Sie im Feld **Betreff** einen beschreibenden Betreff ein. Der Standardwert ist der Debitorennamen und die Rechnungsnummer.
7. Im Feld **Anhang** wird die generierte Rechnung standardmäßig als PDF\_Datei angehängt.
8. Geben Sie im **Nachrichtentext**-Feld eine kurze Mitteilung an den Empfänger ein.

    Wenn ein belegspezifischer E-Mail-Text auf der Seite **Berichts-Auswahl, Verkauf** eingerichtet wird, wird das Feld **Text** automatisch ausgefüllt. Weitere Informationen finden Sie unter [Wiederverwendbare E-Mail-Texte und -Layouts einrichten](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).
9. Wählen Sie die Schaltfläche **OK**, um die E-Mail zu senden.

> [!NOTE]  
> Wenn Sie die E-Mail-Einstellungen nicht jedes Mal ändern wollen, wenn Sie einen Beleg per E-Mail senden, können Sie die Option **Ja** (Standardeinstellungen verwenden) im Feld **E-Mail** auf der Seite **Beleg senden** an auswählen. In diesem Fall wird die Seite **E-Mail senden** nicht geöffnet. Siehe dazu auch Schritt 4. Weitere Informationen finden Sie unter [Einrichten von Sendeprofilen](sales-how-setup-document-send-profiles.md).  

## Zum Verfassen und Senden einer E-Mail

Sie können E-Mails für Kontakte, Kunden, Lieferanten, Verkäufer/Einkäufer und Bankkonten direkt von den Seiten für diese Entitäten aus verfassen. Wählen Sie einfach **Verarbeiten** und dann **E-Mail senden**, um den E-Mail-Editor zu öffnen. Für Bankkonten finden Sie die Aktion **E-Mail senden** unter **Aktionen**.

> [!TIP]
> Wenn Sie häufig Nachrichten versenden, die sich ähneln, oder wenn Sie eine Massenkommunikation versenden möchten, z.B. um eine Verkaufskampagne zu bewerben, kann die Verwendung von Word-Vorlagen mit E-Mail den Prozess beschleunigen. Sie können eine Vorlage für Entitäten wie Kunden, Kreditor und Kontakte erstellen, die den Inhalt einer E-Mail-Nachricht für Sie generiert und sogar den Inhalt für den Empfänger anhand der Daten in [!INCLUDE[prod_short](includes/prod_short.md)] personalisiert. Weitere Informationen finden Sie unter [Word-Vorlagen für Massenkommunikation verwenden](ui-mail-merge.md).  

Wenn Sie einem E-Mail-Szenario zugewiesen sind, das sich auf die Entität bezieht, an die Sie die E-Mail senden, oder auf das Dokument, das Sie senden, wird Ihrer Nachricht möglicherweise automatisch ein Anhang hinzugefügt. Das liegt daran, dass dem E-Mail-Szenario ein Standardanhang zugewiesen wurde. Sie können den Anhang löschen, wenn Sie ihn nicht mit Ihrer Nachricht senden möchten. Weitere Informationen finden Sie unter [Weisen Sie E-Mail-Konten E-Mail-Szenarien zu](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts). 

## Belege, die beim Senden als gedruckt markiert sind

Einige Belege in [!INCLUDE[prod_short](includes/prod_short.md)] verfügen über ein Feld, das angibt, wie oft der Beleg gedruckt worden ist. Die Nummer in diesem Feld <!--"that field?" need a name...--> wird auch aktualisiert, wenn Sie das Dokument per E-Mail senden, da eine PDF-Datei dafür generiert wird. Die Nummer wird aktualisiert, auch wenn Sie die E-Mail nicht senden. <!--guessing this is because emails are technically reports, so the counter bumps up whenever someone creates an email. Need to verify.-->

## Gesendete E-Mails und Ihr E-Mail-Postausgang

[!INCLUDE[prod_short](includes/prod_short.md)] speichert die E-Mails, die Sie auf der Seite **Gesendete Objekte** senden. Damit können Sie E-Mails erneut senden oder an eine andere Person weiterleiten. Wenn Sie in Ihren gesendeten Artikeln keine E-Mail finden können, suchen Sie diese auf der Seite **E-Mail-Postausgang**. 

> [!NOTE]
> Abhängig von der Erweiterung, die Ihr Unternehmen für E-Mails verwendet, können Administratoren eine Liste der von allen gesendeten Nachrichten anzeigen, jedoch nicht den Inhalt der Nachrichten

Im **E-Mail-Postausgang** finden Sie die E-Mails, die Sie als Entwürfe gespeichert haben, und E-Mails, die nicht gesendet werden konnten, z. B. wenn die E-Mail-Adresse ungültig war. Für Nachrichten, die nicht gesendet werden konnten, können Sie **Fehler anzeigen** oder **Fehler untersuchen** anzeigen, um das Problem beheben.  

## Siehe verwandte [Microsoft Schulungen](/training/modules/set-up-email/)

## Siehe auch

[Verwaltung von Berichts- und Beleg-Layouts](ui-manage-report-layouts.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
