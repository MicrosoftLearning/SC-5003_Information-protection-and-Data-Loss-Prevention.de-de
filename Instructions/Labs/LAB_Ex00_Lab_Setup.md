---
lab:
  task: Prepare your environment for administration
  exercise: Exercise 0 - Prepare your environment for administration
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Aufbau der Übung: Vorbereiten Ihrer Umgebung für die Verwaltung

In dieser Übung konfigurieren Sie Ihre Umgebung und bereiten sie für Verwaltungsaufgaben vor. Sie aktivieren die erforderlichen Funktionen, legen die administrativen Berechtigungen fest und sorgen für die richtige Konfiguration der wichtigsten Elemente.

**Aufgaben:**

- Aktivieren der Überwachung im Microsoft Purview-Portal
- Zuweisen von Konformitätsrollen
- Erkunden des Microsoft Purview-Portals

## Aufgabe – Aktivieren der Überwachung im Microsoft Purview-Portal

In dieser Aufgabe aktivieren Sie die Überwachung im Microsoft Purview-Portal, um Portalaktivitäten zu überwachen.

1. Melden Sie sich mit dem**Admin**-Konto bei der VM Client 1 (SC-401-CL1) an.

1. Öffnen Sie Microsoft Edge.

1. Navigieren Sie in**Microsoft Edge** zu`https://purview.microsoft.com`, und melden Sie sich als**MOD-Admin**`admin@WWLxZZZZZZ.onmicrosoft.com` an (wobei ZZZZZZ das eindeutige Präfix Ihres Mandanten ist, das von Ihrem Labhostinganbieter bereitgestellt wird). Das Passwort der administrierenden Person sollte von Ihrem Lab-Hosting-Anbieter bereitgestellt werden.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal,`https://purview.microsoft.com`, und melden sich an.

1. Auf dem Bildschirm erscheint eine Meldung über das neue Microsoft Purview-Portal. Wählen Sie**Erste Schritte**, um Zugriff auf das neue Portal zu erhalten.

    ![Screenshot des Bildschirms „Willkommen im neuen Microsoft Purview-Portal“.](../Media/welcome-purview-portal.png)

1. Wählen Sie**Lösungen** in der linken Seitenleiste und wählen Sie dann**Überwachen**.

1. Wählen Sie auf der Seite**Suche** die Leiste**Aufzeichnung von Benutzenden- und Admin-Aktivitäten starten** aus, um die Überwachungsprotokollierung zu aktivieren.

    ![Der Screenshot zeigt die Schaltfläche „Aufzeichnung von Benutzenden- und Admin-Aktivitäten starten".](../Media/enable-audit-button.png)

1. Sobald Sie diese Option wählen, sollte der blaue Balken von dieser Seite verschwinden.

    >[!Note] **Hinweis: Wenn die Protokollierung nicht durch die Schaltfläche „Überwachung“ nicht aktiviert:**
    >
    >In einigen Mandanten wird die Überwachung möglicherweise nicht durch die Auswahl von**Aufzeichnung von Benutzer- und Administratoraktivitäten starten** aktiviert.  
    >
    >In diesem Fall können Sie die Überwachung stattdessen über PowerShell aktivieren:
    >
    >1. Öffnen Sie ein Terminalfenster mit erhöhten Rechten, indem Sie mit der rechten Maustaste auf die Windows-Schaltfläche klicken und**Terminal (Administrator)** auswählen.  
    >
    >1. Installieren Sie das neueste**Exchange Online PowerShell**-Modul:
    >
    >     ```powershell
    >     Install-Module ExchangeOnlineManagement
    >     ```
    >
    >     Bestätigen Sie alle Eingabeaufforderungen, indem Sie**Y** für „Ja“ (Yes) eingeben und die**EINGABETASTE** drücken.
    >
    >1. Führen Sie den folgenden Befehl aus, um Ihre Ausführungsrichtlinie zu ändern:
    >
    >     ```powershell
    >     Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
    >     ```
    >
    >1. Schließen Sie das Terminalfenster mit erhöhten Rechten, und öffnen Sie eine normale PowerShell-Sitzung.
    >
    >1. So stellen Sie eine Verbindung mit Exchange Online her
    >
    >     ```powershell
    >     Connect-ExchangeOnline
    >     ```
    >
    >    Melden Sie sich als`admin@WWLxZZZZZZ.onmicrosoft.com` an (wobei ZZZZZZ das eindeutige Präfix Ihres Mandanten ist, das von Ihrem Labhostinganbieter bereitgestellt wird). Das Passwort der administrierenden Person sollte von Ihrem Lab-Hosting-Anbieter bereitgestellt werden.
    >
    >1. So überprüfen Sie, ob die Überwachung aktiviert ist:
    >
    >     ```powershell
    >     Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    >     ```
    >
    >    Wenn**_FALSE_** zurückgegeben wird, aktivieren Sie „Überwachung“:
    >
    >     ```powershell
    >     Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    >     ```
    >
    >1. So vergewissern Sie sich, dass sie jetzt aktiviert ist:
    >
    >     ```powershell
    >     Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
    >     ```
    >
    >    Der Befehl sollte**_TRUE_** zurückgeben, sobald die Überwachung aktiv ist.

Sie haben die Überwachung in Microsoft 365 erfolgreich aktiviert.

## Aufgabe – Zuweisen von Compliancerollen

In dieser Aufgabe weisen Sie dem Benutzenden, den Sie mithilfe dieser Übungen verwenden werden, den**Complianceadministrator** zu.

1. Öffnen Sie**Microsoft Edge** und navigieren Sie zum Microsoft 365 Admin Center,`https://admin.microsoft.com`. Sie müssen sich als ein Benutzender anmelden, der**globale Administrator**-Rechte hat.

1. Erweitern Sie**Benutzende** in der linken Seitenleiste und wählen Sie dann**Aktive Benutzende**.

1. Wählen oder erstellen Sie einen Benutzenden, um mit diesen Übungen fortzufahren.

   Wenn Sie einen vorhandenen Benutzenden verwenden möchten, wählen Sie einen Benutzenden mit minimalen Rechten, um ihm den geringsten Zugriff zu ermöglichen.

   1. Wenn Sie einen neuen Benutzenden anlegen, weisen Sie ihm eine Lizenz zu, die für diese Übungen geeignet ist. Der Benutzende muss über eine Microsoft 365 E5-Lizenz oder ein kompatibles Add-on für diese Übungen verfügen. Weisen Sie dem Benutzenden die Rolle**Complianceadministrator** in den optionalen Einstellungen beim Einrichten des neuen Benutzenden zu und schließen Sie die Erstellung des neuen Benutzenden ab.

   1. Wenn Sie die Barrierefreiheit eines bestehenden Benutzenden ändern möchten, wählen Sie ihn aus und wählen Sie dann**Rollen verwalten**. Weisen Sie dem Benutzenden die Rolle**Complianceadministrator** zu und speichern Sie Ihre Änderungen.

1. Melden Sie sich von dem Konto mit dem Zugriff des globalen Administrators ab, indem Sie das Symbol der bzw. des Benutzenden oben rechts auswählen und dann**Abmelden** auswählen.

   Beispiel:

   ![Screenshot zeigt den Navigationspfad zur Abmeldung vom MOD-Administratorkonto.](../Media/sign-out.png)

Sie haben einem Benutzenden erfolgreich die Rolle**Complianceadministrator** zugewiesen, die zur Durchführung der verschiedenen Übungen in dieser Übung erforderlich ist.

## Aufgabe – Erkunden des Microsoft Purview-Portals

In dieser Aufgabe melden Sie sich als der Benutzende an, dem Sie zuvor die Rolle**Complianceadministrator** zugewiesen haben, um das Microsoft Purview-Portal zu erkunden. Diese Rolle wird in den nächsten Übungen als Ihr**Complianceadministrator** bezeichnet.

1. Navigieren Sie in**Microsoft Edge** zu**`https://purview.microsoft.com`**.

1. Wenn das Fenster**Konto auswählen** angezeigt wird, wählen Sie**Ein anderes Konto verwenden**.

1. Wenn das Fenster**Anmelden** angezeigt wird, melden Sie sich als der Benutzende an, den Sie zuvor als**Complianceadministrator** ausgewählt haben.

1. Machen Sie sich mit dem neuen Microsoft Purview-Portal vertraut. Wenn Sie fertig sind, lassen Sie das Browserfenster geöffnet.

Sie haben erfolgreich zum Konto des** Complianceadministrators** gewechselt und sind nun bereit, die Übung zu starten.
