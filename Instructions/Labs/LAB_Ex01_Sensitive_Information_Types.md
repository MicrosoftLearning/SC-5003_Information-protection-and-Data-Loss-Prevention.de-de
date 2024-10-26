---
lab:
  task: Create a custom sensitive information type
  exercise: Exercise 1 - Create a custom sensitive information type
---

# Qualifikationsaufgabe

Ihre Aufgabe besteht darin, Vertraulichkeitsbezeichnungen in Ihrer Organisation zu erstellen und zu veröffentlichen, die vertrauliche Daten entsprechend ihrer Vertraulichkeitsstufe und den erforderlichen Zugriffskontrollen klassifiziert und schützt.

**Task:**

- Benutzerdefinierten Typ für vertrauliche Informationen erstellen

## Aufgabe – Erstellen eines benutzerdefinierten Typs für sensible Informationen

In dieser Aufgabe erstellen Sie einen neuen benutzerdefinierten sensiblen Informationstyp, der das Muster der Mitarbeitenden-IDs in der Nähe der Schlüsselwörter "Mitarbeitender" und "ID" erkennt.

1. Navigieren Sie in **Microsoft Edge** zu **`https://purview.microsoft.com`** und melden Sie sich beim Microsoft Purview-Portal als die bzw. der Benutzende an, die bzw. den Sie in einer früheren Aufgabe als **Complianceadministrator** festgelegt haben.

1. Wählen Sie in der linken Seitenleiste **Lösungen** und dann **Informationsschutz**.

1. Erweitern Sie in der linken Seitenleiste **Klassifizierer** und wählen Sie dann **Typen vertraulicher Informationen**.

1. Auf der Seite **Typen vertraulicher Informationen** wählen Sie **+ Typ vertraulicher Informationen erstellen**, um die Konfiguration des Typs vertraulicher Informationen zu starten.

1. Geben Sie auf der Seite **Benennen Sie den Typ Ihrer vertraulichen Informationen** ein:

    - **Name**: `Contoso Employee IDs`
    - **Beschreibung:** `Pattern for Contoso employee IDs.`

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Muster für diesen vertraulichen Informationstyp definieren** die Option **Muster erstellen** aus.

1. Wählen Sie im Bedienfeld **Neues Muster** auf der rechten Seite **+ Primärelement hinzufügen** > **Regulärer Ausdruck**.

1. Geben Sie im Flyout-Bedienfeld **+ Einen regulären Ausdruck hinzufügen** auf der rechten Seite ein:

    - **ID**: `Contoso IDs`
    - **Regulärer Ausdruck**: `[A-Z]{3}[0-9]{6}`
    - Wählen Sie die Optionsschaltfläche für *Zeichenfolgenübereinstimmung*

1. Wählen Sie **Erledigt** am unteren Rand des Flyout-Bedienfelds.

1. Zurück auf dem Flyout-Bedienfeld **Neues Muster** wählen Sie unter **Unterstützende Elemente** das Dropdownmenü **+ Unterstützende Elemente oder Elementgruppen hinzufügen** und wählen Sie **Schlüsselwortliste** aus.

1. Auf dem Flyout-Bedienfeld **Schlüsselwortliste hinzufügen** auf der rechten Seite, geben Sie ein:

    - **ID**: `Employee ID keywords`
    - **Keine Beachtung von Groß-/Kleinschreibung**:

       ```text
       Employee
       ID
       ```

    - Wählen Sie die Optionsschaltfläche für *Wortübereinstimmung*

1. Wählen Sie **Erledigt** am unteren Rand des Flyout-Bedienfelds.

1. Verringern Sie im Flyout-Bedienfeld **Neues Muster** unter **Zeichennähe** den Wert **Erkennen Sie primäre UND unterstützende Elemente** auf `100` Zeichen.

1. Wählen Sie die Schaltfläche **Erstellen** am unteren Rand des Flyout-Bedienfeldes.

1. Zurück auf der Seite **Muster für diesen sensiblen Informationstyp definieren** wählen Sie **Weiter**.

1. Verwenden Sie auf der Seite **Wählen Sie die empfohlene Stufe für die Anzeige in den Konformitätsrichtlinien** den Standardwert und wählen Sie **Weiter**.

1. Überprüfen Sie auf der Seite **Einstellungen überprüfen und fertigstellen** die Einstellungen, und wählen Sie **Erstellen** aus. Wenn sie erfolgreich erstellt wurde, wählen Sie **Fertig** aus.

Sie haben erfolgreich einen neuen sensiblen Informationstyp erstellt, um Mitarbeitende-IDs im Muster von drei Großbuchstaben, sechs Zahlen und den Schlüsselwörtern 'Mitarbeitender' oder 'IDs' innerhalb eines Bereichs von 100 Zeichen zu identifizieren.
