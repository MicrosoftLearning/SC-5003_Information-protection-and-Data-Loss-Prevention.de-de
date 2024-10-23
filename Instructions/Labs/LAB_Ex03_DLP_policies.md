---
lab:
  task: Create a data loss prevention (DLP) policy
  exercise: Exercise 3 - Create a data loss prevention (DLP) policy
---

# Qualifikationsaufgaben

**Aufgaben:**

1. Erstellen einer DLP-Richtlinie im Simulationsmodus
1. Ändern einer DLP-Richtlinie
1. Erstellen einer DLP-Richtlinie in PowerShell
1. Aktivieren einer Richtlinie im Simulationsmodus

## Aufgabe 1 – Erstellen einer DLP-Richtlinie im Simulationsmodus

In dieser Übung erstellen Sie eine Richtlinie zum Schutz vor Datenverlust (DLP), um sensible Daten vor der Weitergabe durch Benutzende zu schützen. Die von Ihnen erstellte DLP-Richtlinie informiert Ihre Benutzenden, wenn sie Inhalte teilen möchten, die Kreditkarteninformationen enthalten, und ermöglicht es ihnen, eine Begründung für das Senden dieser Informationen bereitzustellen. Die Richtlinie wird im Simulationsmodus implementiert, da Sie noch nicht wollen, dass sich die Sperrung auf Ihre Benutzenden auswirkt.

1. Navigieren Sie in **Microsoft Edge** zu **`https://purview.microsoft.com`** und melden Sie sich im Microsoft Purview-Portal als derjenige Benutzende an, den Sie als **Compliance Administrator** ausgewählt haben.

1. Wählen Sie **Lösungen** in der linken Seitenleiste und wählen Sie dann **Verhinderung von Datenverlust**.

1. Wählen Sie in der linken Seitenleiste **Richtlinien**.

1. Wählen Sie auf der Seite **Richtlinien** die Option **+ Richtlinie erstellen**, um die Konfiguration zum Erstellen einer neuen Richtlinie zum Schutz vor Datenverlust zu starten.

1. Wählen Sie auf der Seite **Starten Sie mit einer Vorlage oder erstellen Sie eine benutzerdefinierte Richtlinie** die Kategorie **Benutzerdefiniert** und dann **Benutzerdefinierte Richtlinie** unter **Vorschriften**.

1. Wählen Sie **Weiter** aus.

1. Geben Sie auf der Seite **DLP-Richtlinie benennen** Folgendes ein:

   - **Name**: `Credit Card DLP Policy`
   - **Beschreibung:** `Protect credit card numbers from being shared`

1. Wählen Sie **Weiter** aus.

1. Auf der Seite **Admineinheiten zuweisen** wählen Sie **Weiter**.

1. Aktivieren Sie auf der Seite **Wählen Sie Speicherorte für die Anwendung der Richtlinie** den Speicherort nur für **Teams Chat- und Channel-Nachrichten**. Wenn andere Speicherorte ausgewählt sind, heben Sie die Auswahl auf.

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Richtlinieneinstellungen definieren** die Option **Erweiterte DLP-Regeln erstellen oder anpassen** und dann **Weiter** aus.

1. Wählen Sie auf der Seite **Erweiterte DLP-Regeln anpassen** die Option **+ Regel erstellen**.

1. Auf der Flyout-Seite **Regel erstellen**, geben Sie `Credit card information` als Namen in das Feld **Name** ein.

1. Wählen Sie unter **Bedingungen** die Option **+ Bedingung hinzufügen**, und wählen Sie dann **Inhalt enthält**.

1. Im neuen Bereich **Inhalt enthält** wählen Sie **Hinzufügen**, dann wählen Sie **Typen vertraulicher Informationen**.

1. Auf der Seite **Typen vertraulicher Informationen** wählen Sie **Kreditkartennummer** und dann **Hinzufügen**.

1. Wählen Sie **+ Bedingung hinzufügen**, dann wählen Sie **Inhalt wird von Microsoft 365 freigegeben**.

1. Wählen Sie im neuen Abschnitt **Inhalt wird von Microsoft 365 freigegeben** die Option **Nur für Personen innerhalb meiner Organisation**.

1. Wählen Sie unter **Aktionen** die Option **+ Aktion hinzufügen** und dann **Zugriff einschränken oder Inhalte an Microsoft 365-Speicherorten verschlüsseln**.

1. Wählen Sie im neuen Bereich **Zugriff einschränken oder Inhalte in Microsoft 365-Speicherorten verschlüsseln** die Option **Alle sperren.**

1. Aktivieren Sie unter **Benutzerbenachrichtigungen** die Option **Ein** für **Benachrichtigungen verwenden, um Ihre Benutzenden zu informieren und sie über den richtigen Umgang mit sensiblen Daten aufzuklären.**, und aktivieren Sie dann das Kontrollkästchen für **Benutzende im Office 365-Dienst mit einem Richtlinienhinweis benachrichtigen**.

1. Aktivieren Sie unter **Außerkraftsetzungen durch Benutzende** das Kontrollkästchen **Benutzenden das Außerkraftsetzen von Richtlinieneinschränkungen erlauben Fabric (einschließlich Power BI), Exchange, SharePoint, OneDrive und Teams.**

1. Aktivieren Sie das Kontrollkästchen **Eine geschäftliche Begründung für die Außerkraftsetzung ist erforderlich**.

1. Wählen Sie unter **Incident-Berichte** in der Dropdown-Liste **Diesen Schweregrad in Admin-Warnungen und Berichten verwenden** die Option **Niedrig**.

1. Wählen Sie am unteren Rand des Flyout-Bedienfelds **Regel erstellen** die Option **Speichern**.

1. Wählen Sie auf der Seite **Erweiterte DLP-Regeln anpassen** die Option **Weiter**.

1. Wählen Sie auf der Seite **Richtlinienmodus** die Option **Richtlinie im Simulationsmodus ausführen** und aktivieren Sie das Kontrollkästchen für **Richtlinientipps im Simulationsmodus anzeigen**.

1. Wählen Sie **Weiter** aus.

1. Auf der Seite **Überprüfen und beenden** überprüfen Sie Ihre Einstellungen und wählen dann **Absenden**.

1. Wählen Sie auf der Seite **Neue Richtlinie erstellt** die Option **Fertig** aus.

Sie haben nun eine DLP-Richtlinie erstellt, die in Microsoft Teams-Chats und -Kanälen nach Kreditkartennummern scannt und es den Benutzenden ermöglicht, eine geschäftliche Rechtfertigung für die Außerkraftsetzung der Richtlinie bereitzustellen.

## Aufgabe 2 – Ändern einer DLP-Richtlinie

In dieser Aufgabe ändern Sie die bestehende DLP-Richtlinie, die in der vorherigen Aufgabe erstellt wurde, um auch E-Mails auf Kreditkarteninformationen zu scannen. Diese Änderung gewährleistet, dass sensible Daten über mehrere Kommunikationskanäle hinweg geschützt sind.

1. Sie sollten weiterhin bei Microsoft 365 als der Benutzende angemeldet sein, den Sie als **Complianceadministrator** ausgewählt haben.

1. Sie sollten sich immer noch auf der Seite **Richtlinien** in Microsoft Purview befinden. Falls nicht, öffnen Sie **Microsoft Edge** und navigieren Sie zu `https://purview.microsoft.com`. Wählen Sie **Lösungen** > **Verhinderung von Datenverlust** > **Richtlinien**.

1. Aktivieren Sie auf der Seite **Richtlinien** das Kontrollkästchen für die kürzlich erstellte **Kreditkarten-DLP-Richtlinie** und wählen Sie dann **Richtlinie bearbeiten** aus, um die Richtlinienkonfiguration zu öffnen.

1. Wählen Sie auf der Seite **Benennen Sie Ihre DLP-Richtlinie** die Option **Weiter**.

1. Auf der Seite **Admineinheiten zuweisen** wählen Sie **Weiter**.

1. Aktivieren Sie auf der Seite **Auswahl der Speicherorte, auf die die Richtlinie angewendet werden soll** das Kontrollkästchen für **Exchange-E-Mail**, um diesen Speicherort zu Ihrer DLP-Richtlinie hinzuzufügen.

1. Wählen Sie **Weiter**, bis Sie die Seite **Überprüfen und beenden** erreichen.

1. Wählen Sie **Absenden** auf der Seite **Überprüfen und beenden**, um die Änderung, die Sie an der Richtlinie vorgenommen haben, anzuwenden.

1. Sobald die Richtlinie aktualisiert ist, wählen Sie **Erledigt** auf der Seite **Richtlinie aktualisiert**.

Sie haben die DLP-Richtlinie erfolgreich geändert, um das Scannen von E-Mails einzubeziehen und so den Schutz sensibler Daten zu verbessern.

## Aufgabe 3 – Erstellen einer DLP-Richtlinie in PowerShell

In dieser Aufgabe erstellen Sie mithilfe von PowerShell eine DLP-Richtlinie, um die IDs der Mitbearbeitenden von Contoso zu schützen und zu verhindern, dass sie über Exchange freigegeben werden. Diese Richtlinie benachrichtigt Benutzende, die versuchen, diese sensiblen Daten weiterzugeben, und blockiert die E-Mail, wenn sie Mitarbeitende-IDs enthält.

1. Öffnen Sie auf Ihrem Desktop ein erweitertes PowerShell-Fenster, indem Sie mit der rechten Maustaste auf die Schaltfläche Windows in der Taskleiste klicken und dann **Terminal (Admin)** wählen.

1. Führen Sie das Cmdlet **Connect- IPPSSession** aus, um eine Verbindung mit der Security & Compliance PowerShell herzustellen:

   ```powershell
   Connect-IPPSSession
   ```

1. Melden Sie sich als derjenige Benutzende an, den Sie als **Complianceadministrator** im Pop-up-Fenster **Anmelden in Ihrem Konto** ausgewählt haben.

1. Führen Sie das Cmdlet **New-DlpCompliancePolicy** aus, um eine DLP-Richtlinie zu erstellen, die alle Exchange-Postfächer scannt:

   ```powershell
   New-DlpCompliancePolicy -Name "EmployeeID DLP Policy" -Comment "This policy blocks sharing of Employee IDs" -ExchangeLocation All
   ```

1. Führen Sie das Cmdlet **New-DlpComplianceRule** aus, um eine DLP-Regel zu der im vorherigen Schritt erstellten DLP-Richtlinie hinzuzufügen:

   ```powershell
   New-DlpComplianceRule -Name "EmployeeID DLP rule" -Policy "EmployeeID DLP Policy" -BlockAccess $true -ContentContainsSensitiveInformation @{Name="Contoso Employee IDs"}
   ```

1. Führen Sie das Cmdlet **Get-DLPComplianceRule** aus, um die DLP-Regel **EmployeeID** zu überprüfen:

   ```powershell
   Get-DLPComplianceRule -Identity "EmployeeID DLP rule"
   ```

Sie haben mithilfe von PowerShell erfolgreich eine DLP-Richtlinie erstellt, die in Exchange nach den IDs Mitarbeitender von Contoso scannt.

## Aufgabe 4 – Aktivierung einer Richtlinie im Simulationsmodus

In dieser Aufgabe aktivieren Sie die **Kreditkarten-DLP-Richtlinie**, die Sie im Simulationsmodus erstellt haben, damit sie ihre Schutzmaßnahmen erzwingt.

1. Sie sollten weiterhin bei Microsoft 365 als der Benutzende angemeldet sein, den Sie als **Complianceadministrator** ausgewählt haben.

1. Navigieren Sie in **Microsoft Edge** zu den DLP-Richtlinien, indem Sie zu `https://purview.microsoft.com` > **Lösungen** > **Vermeidung von Datenverlust** gehen und dann **Richtlinien** in der linken Seitenleiste auswählen.

1. Aktivieren Sie auf der Seite **Richtlinien** das Kontrollkästchen für die **Kreditkarten-DLP-Richtlinie** und wählen Sie **Richtlinie bearbeiten** aus, um die Richtlinienkonfiguration zu öffnen.

1. Wählen Sie **Weiter**, bis Sie die Seite **Richtlinienmodus** erreichen, und wählen Sie **Sofort die Richtlinie einschalten**.

1. Auf der Seite **Überprüfen und beenden** wählen Sie **Absenden**.

1. Wählen Sie auf der Seite **Richtlinie aktualisiert** die Option **Fertig** aus.

Sie haben die DLP-Richtlinie erfolgreich aktiviert und sichergestellt, dass alle Versuche, Kreditkarteninformationen weiterzugeben, blockiert werden und eine geschäftliche Begründung erfordern.
