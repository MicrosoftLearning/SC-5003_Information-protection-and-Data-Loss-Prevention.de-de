---
lab:
  task: Create and publish a sensitivity label
  exercise: Exercise 2 - Create and publish a sensitivity label
---

# Qualifikationsaufgabe

Ihre Aufgabe besteht darin, Vertraulichkeitsbezeichnungen in Ihrer Organisation zu erstellen und zu veröffentlichen, die vertrauliche Daten entsprechend ihrer Vertraulichkeitsstufe und den erforderlichen Zugriffskontrollen klassifiziert und schützt.

- **Erstellen Sie eine Vertraulichkeitsbezeichnung** zum Kategorisieren von Daten.
- **Erstellen Sie eine Unterbezeichnung** unter der übergeordneten Bezeichnung, um Daten zu gruppieren.
- **Erstellen Sie eine Bezeichnungsrichtlinie**, um Regeln und Richtlinien für die Verwaltung von Vertraulichkeitsbezeichnungen innerhalb der Organisation festzulegen.

**Ziel**: Erstellen und veröffentlichen Sie eine Vertraulichkeitsbezeichnung, um den Datenschutz in der Personalabteilung zu verbessern. Ihre Aufgabe besteht darin, eine übergeordnete Bezeichnung namens _Intern_ mit einer Unterbezeichnung namens _Mitarbeiterdaten (HR)_ einzurichten.

## Aufgabe 1 – Erstellen Sie eine Vertraulichkeitsbezeichnung

1. Rufen Sie das Microsoft Purview Compliance-Portal auf.
1. Erweitern Sie den **Informationsschutz**, und wählen Sie dann **Bezeichnungen** aus.
1. Wählen Sie unter **Bezeichnung** die Option **+ Bezeichnung erstellen** aus.
1. Geben Sie unter **Angeben von grundlegenden Details für diese Bezeichnung** die folgenden Informationen ein:

    - **Name**: `Internal`
    - **Anzeigename**: `Internal`
    - **Beschreibung für Benutzer**: `Internal sensitivity label.`
    - **Beschreibung für Administratoren**: `Internal sensitivity label for Contoso.`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Definieren des Bereichs für diese Bezeichnung** die Option **Elemente** und dann**Dateien** und **E-Mails** und dann **Weiter** aus.
1. Wählen Sie auf der Seite **Schutzeinstellungen auswählen** die Option **Weiter** aus.
1. Wählen Sie **Weiter** aus, und akzeptieren Sie die Standardeinstellungen, bis Sie die Seite **Einstellungen überprüfen und fertig stellen** erreicht haben, und wählen Sie dann **Bezeichnung erstellen** aus.
1. Wählen Sie auf der Seite **Vertraulichkeitsbezeichnung** die Option **Richtlinie noch nicht erstellen** aus, und wählen Sie dann **Fertig** aus.

## Aufgabe 2 – Erstellen einer Unterbezeichnungsbezeichnung

1. Markieren Sie auf der Seite "Informationsschutz" die neu erstellte **interne** Bezeichnung (ohne Auswahl), und wählen Sie die vertikale **...** ![Bild des vertikalen Punktmenüs](../Media/SensitivityLabelDotMenu.png)
1. Wählen Sie im Menü die **Unterbezeichnung +erstellen** aus.
1. Geben Sie unter **Angeben von grundlegenden Details für diese Bezeichnung** die folgenden Informationen ein:

   - **Name**: `Employee data (HR)`
   - **Anzeigename**: `Employee data (HR)`
   - **Beschreibung für Benutzer**: `This label is the default label for all documents in the HR Department.`
   - **Beschreibung für Administratoren**: `This label is created in consultation with the Director of HR.`
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Definieren des Bereichs für diese Bezeichnung** die Option **Elemente** und dann**Dateien** und **E-Mails** und dann **Weiter** aus.
1. Aktivieren Sie unter **Schutzeinstellungen für die ausgewählten Elementtypen auswählen** das Kontrollkästchen für den **Zugriffssteuerung** und wählen Sie dann **Weiter** aus.
1. Die Seite **Zugriffssteuerung** wird geöffnet:
   - Stellen Sie sicher, dass das Optionsfeld für die **Zugriffssteuerungseinstellungen** ausgewählt ist.
   - Wählen Sie unter **Zuweisung von Berechtigungen oder Benutzer entscheiden lassen?** Wählen **Berechtigungen jetzt zuweisen **.
   - Wählen Sie unter **Benutzerzugriff auf Inhalte läuft ab** die Option **Nie** aus.
   - Wählen Sie unter **Offlinezugriff zulassen** die Option **Nur eine Anzahl von Tagen**.
   - Im Feld **Benutzer haben Offlinezugriff auf den Inhalt für diese Anzahl von Tagen** Eingabe 14.
   - Wählen Sie unter **Berechtigungen für bestimmte Benutzer und Gruppen zuweisen** die Schaltfläche **Berechtigungen zuweisen** aus.
1. Wählen Sie auf der Seite **Berechtigungen zuweisen** **+ Alle authentifizierten Benutzer hinzufügen** und dann **Speichern** aus.
1. Wählen Sie auf der Seite **Zugriffssteuerung** **Weiter** aus.
1. Wählen Sie **Weiter** aus, und akzeptieren Sie die Standardwerte, bis Sie die Seite **Einstellungen überprüfen und fertig stellen**, und wählen Sie dann **Bezeichnung erstellen** aus.
1. Wählen Sie auf der Seite **Vertraulichkeitsbezeichnung** die Option **Richtlinie noch nicht erstellen** aus, und wählen Sie dann **Fertig** aus.

## Aufgabe 3 – Veröffentlichen einer Vertraulichkeitsbezeichnung

1. Aktivieren Sie auf der Seite **Bezeichnungen** die Kontrollkästchen neben der neu erstellten Unterbezeichnung **Intern** und **Mitarbeiterdaten (HR)**.
1. Stellen Sie auf der Seite **Zu veröffentlichende Vertraulichkeitsbezeichnungen auswählen** sicher, dass sowohl die Bezeichnungen "Interne" als auch "Mitarbeiterdaten (HR)" unter **Zu veröffentlichende Vertraulichkeitsbezeichnungen**, und wählen Sie dann **Weiter** aus.
1. Wählen Sie **Weiter** aus, bis Sie die Seite **Richtlinieneinstellungen** erreicht haben.
1. Aktivieren Sie auf der Seite **Richtlinieneinstellungen** das Kontrollkästchen für **Benutzer müssen eine Begründung für die Entfernung einer Kennzeichnung oder die Herabstufung ihrer Klassifizierung angeben**.
1. Wählen Sie **Weiter** aus, bis Sie die Seite **Ihre Richtlinie benennen** erreichen
1. Geben Sie auf der Seite **Ihre Richtlinie benennen** die folgenden Informationen ein:

   - **Name**: `Internal HR employee data`
   - **Geben Sie eine Beschreibung für Ihre Vertraulichkeitsbezeichnungsrichtlinie** ein: `This HR label is to be applied to internal HR employee data.`

1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Überprüfen und beenden** die Option **Absenden** aus.
1. Wählen Sie auf der Seite **Neue Richtlinie erstellt** die Option **Fertig** aus.

Sie haben nun erfolgreich eine Vertraulichkeitsbezeichnung erstellt, um Mitarbeiterdaten für die Personalabteilung zu klassifizieren.
