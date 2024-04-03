---
lab:
  task: Create a data loss prevention (DLP) policy
  exercise: Exercise 4 - Create a data loss prevention (DLP) policy
---

# Qualifikationsaufgabe

Ihre Aufgabe besteht darin, eine benutzerdefinierte DLP-Richtlinie (Data Loss Prevention, Verhinderung von Datenverlust) zu entwickeln und zu erzwingen, die auf die Sicherheit der vertraulichen Kundendaten Ihrer Organisation zugeschnitten ist, und gleichzeitig die Einhaltung der Datenschutzbestimmungen sicherzustellen.

- **Erstellen Sie eine benutzerdefinierte DLP-Richtlinie** im Testmodus, um Daten ohne Erzwingung zu überwachen.
- **Definieren Sie eine erweiterte DLP-Regel** für bestimmte vertrauliche Informationen.
- **Aktivieren Sie die DLP-Richtlinie**, um Schutz und Compliance aktiv zu erzwingen.

**Ziel**: Entwickeln und implementieren Sie eine benutzerdefinierte Richtlinie zur Verhinderung von Datenverlust (Data Loss Prevention, DLP), um vertrauliche Kundendaten zu schützen und die Einhaltung gesetzlicher Vorschriften zu gewährleisten. Zunächst erstellen Sie eine DLP-Richtlinie im Testmodus für die anfängliche Überwachung, fahren mit dem Entwerfen einer erweiterten Regel fort, die auf bestimmte Typen vertraulicher Informationen abzielt, und aktivieren Sie schließlich die Richtlinie, um den Datenschutz für E-Mails, SharePoint, OneDrive und Teams-Kommunikationen zu erzwingen.

## Aufgabe 1 – Erstellen einer benutzerdefinierten Richtlinie zur Verhinderung von Datenverlust (Data Loss Prevention, DLP)

1. Rufen Sie das Microsoft Purview Compliance-Portal auf.
1. Erweitern Sie **Verhinderung von Datenverlust** und wählen Sie **Richtlinien** aus.
1. Wählen Sie auf der Seite **Richtlinien** die Option **+ Richtlinie erstellen** aus.
1. Wählen Sie im DLP-Richtlinien-Assistenten im **Startmenü eine Vorlage aus, oder erstellen Sie eine benutzerdefinierte Richtlinienauswahl** :
   - Kategorien: **Custom** (Benutzerdefiniert)
   - Bestimmungen: **Benutzerdefinierte Richtlinie**
1. Wählen Sie **Weiter** aus.
1. Geben Sie auf der Seite **DLP-Richtlinie benennen** Folgendes ein:
   - **Name**: `Customer interaction protection policy`
   - **Beschreibung:** `This DLP policy protects customer data integrity and confidentiality in the Customer Service department by preventing unauthorized access and disclosure.`
1. Wählen Sie **Weiter** aus, bis Sie die Seite **Auswählen der Anwendung der Richtlinie** erreicht haben.
1. Wählen Sie auf der Seite **Auswählen der Anwendung der Richtlinie** nur Folgendes aus:
   - **Exchange-E-Mail**
   - **SharePoint-Websites**
   - **OneDrive Konten**
   - **Teams-Chats und -Kanalnachrichten**
1. Wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinieneinstellungen definieren** die Option **Erweiterte DLP-Regeln erstellen oder anpassen** und dann **Weiter** aus.
1. Wählen Sie unter **Erweiterte DLP-Regeln anpassen** die Option **+ Regel erstellen** aus.
1. Die Seite **Regel erstellen** wird angezeigt:
   - Geben Sie im Feld **Name** `Customer data` ein.
   - Wählen Sie unter **Bedingungen** die Option **+ Bedingung hinzufügen** > **Inhalt enthält**.
   - Wählen Sie unter **Inhalt** die Option **Vertrauliche Informationstypen** > **hinzufügen**.
   - Wählen Sie auf der Seite **Trainierbare Klassifizierer** auf der rechten Seite die Klassifizierer `Customer Complaints` und `Customer Files` aus, und wählen Sie dann unten auf der Seite **Hinzufügen** aus, um diese vortrainierten Klassifizierer hinzuzufügen.
   > [!tip] Verwenden Sie die Suchleiste, um trainierbare Klassifizierer auf einfache Weise zu finden.
   - Zurück auf der Seite **Regel erstellen** unter **Inhalt enthält** wählen Sie **+ Bedingung hinzufügen** > **Inhalt wird von Microsoft365 freigegeben**.
   - Unter **Inhalt wird von Microsoft365 freigegeben** wählen Sie **mit Personen außerhalb meiner Organisation** aus dem Dropdownmenü.
   - Wählen Sie unter **Aktionen** **+ Aktion hinzufügen** > **Inhalte an Microsoft 365-Speicherorten einschränken oder verschlüsseln**.
   - Stellen Sie unter **Inhalte an Microsoft 365-Speicherorten einschränken oder verschlüsseln** sicher, dass das Optionsfeld für **Nur Personen außerhalb Ihrer Organisation blockieren** ausgewählt ist.
   - Schalten Sie unter **Benutzerbenachrichtigungen** Benachrichtigungen **ein**, und aktivieren Sie dann das Kontrollkästchen **Benutzer im Office 365-Dienst mit einem Richtlinientipp benachrichtigen**.
   - Aktivieren Sie unter **Benutzeraußerkraftsetzungen** das Kontrollkästchen für **Außerkraftsetzungen von Microsoft 365-Diensten zulassen**
   - Legen Sie unter **Vorfallberichte** die Stufe**Diesen Schweregrad in Administratorwarnungen und -berichten verwenden** auf **Mittel** fest.
   - Wählen Sie unten in **Regel erstellen** die Option **Speichern** aus.
1. Wählen Sie auf der Seite **Erweiterte DLP-Regeln anpassen** die Option **Weiter** aus.
1. Wählen Sie auf der Seite **Richtlinienmodus** die Option **Richtlinie im Testmodus ausführen** aus, und stellen Sie sicher, dass die Option **Richtlinientipps im Simulationsmodus anzeigen** aktiviert ist, und wählen Sie **Weiter** aus.
1. Wählen Sie auf der Seite **Überprüfen und beenden** die Option **Absenden** aus.
1. Wählen Sie auf der Seite **Neue Richtlinie erstellen** die Option **Fertig** aus.

## Aufgabe 2: Ändern einer DLP-Richtlinie

1. Aktivieren Sie auf der Seite **Richtlinien** das Kontrollkästchen links neben der neu erstellten **Richtlinie zum Schutz der Kundeninteraktion**, und wählen Sie dann oben auf der Seite **Richtlinie bearbeiten** aus.
1. Wählen Sie im Assistent für das Erstellen von DLP-Richtlinien **Weiter**, bis Sie die Seite **Richtlinienmodus** erreichen, und wählen Sie dann **Richtlinie sofort aktivieren** aus, um die DLP-Richtlinie zu erzwingen.
1. Wählen Sie **Weiter** aus, um die DLP-Richtlinie zu überprüfen, und wählen Sie dann **Absenden** aus, nachdem Sie Ihre Änderungen überprüft haben.
1. Wählen Sie auf der Seite **Richtlinie aktualisiert** die Option **Fertig** aus.

Sie haben nun erfolgreich eine DLP-Richtlinie erstellt, um vertrauliche Kundendaten zu schützen.
