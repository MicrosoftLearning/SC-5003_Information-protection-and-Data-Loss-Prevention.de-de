---
lab:
  task: Create and assign an auto-labeling policy
  exercise: Exercise 3 - Create and assign an auto-labeling policy
---

# Qualifikationsaufgaben

Ihre Aufgabe besteht darin, Vertraulichkeitsbezeichnungen in Ihrer Organisation zu erstellen und zu veröffentlichen, die vertrauliche Daten entsprechend ihrer Vertraulichkeitsstufe und den erforderlichen Zugriffskontrollen klassifiziert und schützt.

- **Erstellen Sie eine Vertraulichkeitsbezeichnung** zum Kategorisieren von Daten.
- **Konfigurieren Sie die Bezeichnung für die automatische Bezeichnung** für Dateien und E-Mails.
- **Konfigurieren Sie eine Richtlinie für die automatische Bezeichnung** zur automatischen Klassifizierung von Daten in SharePoint und OneDrive.
- **Veröffentlichen Sie die Richtlinie für die automatische Bezeichnung**, um die Bezeichnung in Ihrer Organisation bereitzustellen, und automatisieren Sie die Klassifizierung für erhöhte Sicherheit und Konformität.

**Ziel**: Erstellen und Veröffentlichen einer Richtlinie für die automatische Bezeichnung für die Finanzabteilung. Ihre Aufgabe besteht darin, eine Vertraulichkeitsbezeichnung einzurichten, die automatisch Bezeichnungen auf Dateien und E-Mails basierend auf Finanzdaten anwendet. Sie müssen auch eine Richtlinie für die automatische Bezeichnung erstellen, die diese Bezeichnungen automatisch auf Inhalte in SharePoint und OneDrive anwendet.

## Aufgabe 1 – Erstellen Sie eine Vertraulichkeitsbezeichnung

1. Rufen Sie das Microsoft Purview Compliance-Portal auf.
1. Erweitern Sie den **Informationsschutz** und wählen Sie dann **Bezeichnungen** aus.
1. Wählen Sie auf der Schaltfläche **Bezeichnungen** die Option **+ Bezeichnung erstellen ** aus.
1. Geben Sie unter **Grundlegende Details für diese Bezeichnung angeben** die folgenden Informationen ein:

    - **Name**: `Protected Financial Records`
    - **Anzeigename**: `Protected Financial Records`
    - **Beschreibung für Benutzende**: `Use for documents with sensitive financial data.`
    - **Beschreibung für Administratoren**: `Applies encryption and access controls to financial documents.`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Bereich für diese Bezeichnung definieren** die Option **Elemente** und dann **Dateien** und **E-Mails ** und dann **Weiter** aus.
1. Wählen Sie auf der Seite **Schutzeinstellungen auswählen** die Option **Weiter** aus.
1. Auf der **automatischen Bezeichnung für Dateien und E-Mails**:
   - Legen Sie den Umschalter fest, um die **automatische Bezeichnung für Dateien und E-Mails** zu aktivieren
   - Wählen Sie unter **Inhalt erkennen, der diesen Bedingungen entspricht** die Option **+Bedingung hinzufügen** > **Inhalt enthält**.
   - Wählen Sie unter **Inhalt enthält** die Option **Typen vertraulicher Informationen** > ** hinzufügen**.
   - Suchen Sie auf der Seite **Typen vertraulicher Informationen** nach dem Typ „Vertrauliche Informationen“ und fügen Sie diesen für `Credit Card Number`, `U.S. Bank Account Number` und `ABA Routing Number` hinzu. **Hinzufügen**, um die drei Typen vertraulicher Informationen hinzuzufügen und wählen Sie dann **Speichern**.
   - Wählen Sie unter **Wenn Inhalt diesen Bedingungen entspricht** die Option **die Bezeichnung automatisch anwenden** aus.
   - Lassen Sie das optionale Feld **Diese Meldung für Benutzende anzeigen, wenn die Bezeichnung angebracht wird** leer.
1. Wählen Sie **Weiter** aus und akzeptieren Sie die Standardwerte, bis Sie die Seite **Einstellungen überprüfen und beenden** erreicht haben, und wählen Sie dann **Bezeichnung erstellen** aus.
1. Wählen Sie auf der Seite **Vertraulichkeitsbezeichnung** die Option **Richtlinie noch nicht erstellen** aus, und wählen Sie dann **Fertig** aus.

## Aufgabe 2 – Erstellen Sie eine Richtlinie für die automatische Bezeichnung

1. Aktivieren Sie auf der Seite **Bezeichnungen** das Kontrollkästchen neben der neu erstellten Bezeichnung **Geschützte Finanzdatensätze** und wählen Sie **Richtlinie für die automatische Bezeichnung erstellen** aus.
1. Geben Sie auf der Seite **Richtlinie für die automatische Bezeichnung benennen** die folgenden Informationen ein:

   - **Name**: `Finance Auto-Label Policy`
   - **Geben Sie eine Beschreibung für Ihre Richtlinie für die Vertraulichkeitsbezeichnung ein**: `Automates the labeling of financial documents.`
1. Wählen Sie **Weiter** aus, bis Sie die Seite **Regeln für Inhalte an allen Speicherorten definieren** erreichen.
1. Wählen Sie unter **Regeln für Inhalte an allen Speicherorten definieren** die Option **Neue Regel** aus.
1. Auf der Seite **Neue Regel**:
   - Geben Sie `Financial data` als **Namen** ein.
   - Wählen Sie unter **Bedingungen** die Option **+Bedingung hinzufügen** > **Inhalt enthält**.
   - Wählen Sie unter **Inhalt enthält** die Option **Vertraulichen Informationstyp** > **hinzufügen**.
   - Suchen Sie auf der Seite **Typen vertraulicher Informationen** nach dem Typ „Vertrauliche Informationen“ und fügen Sie diesen für `Credit Card Number`, `U.S. Bank Account Number` und `ABA Routing Number` hinzu. **Hinzufügen**, um die drei Typen vertraulicher Informationen hinzuzufügen und wählen Sie dann **Speichern**.
1. Wählen Sie **Weiter**, bis Sie die Seite **Entscheiden Sie, ob Sie die Richtlinie jetzt oder später testen möchten** erreichen.
1. Wählen Sie auf der Seite **Entscheiden Sie, ob Sie die Richtlinie jetzt oder später testen möchten** die Option **Richtlinie im Simulationsmodus ausführen** und wählen Sie dann **Weiter**.
1. Wählen Sie auf der Seite **Überprüfen und beenden** die Option **Richtlinie erstellen**.
1. Wählen Sie auf der Seite Ihre **Richtlinie für die automatische Bezeichnung wurde erstellt** die Option **Fertig**.

Sie haben nun erfolgreich eine Vertraulichkeitsbezeichnung erstellt, um Finanzdaten für die Finanzabteilung zu klassifizieren.
