---
lab:
  task: Create a custom sensitive information type
  exercise: Exercise 1 - Create a custom sensitive information type
---

## WWL-Mandanten – Nutzungsbedingungen

Wenn Ihnen im Rahmen einer Präsenzschulung ein Mandant zugewiesen worden ist, steht dieser für Praxislabs innerhalb der Präsenzschulung zur Verfügung.

Mandanten sollten nicht für Zwecke außerhalb von Praxislabs freigegeben oder verwendet werden. Der in diesem Kurs verwendete Mandant ist ein Testmandant; er kann nach Abschluss des Kurses nicht verwendet oder erreicht werden und ist nicht für Erweiterungen geeignet.

Mandanten dürfen nicht in ein kostenpflichtiges Abonnement konvertiert werden. Die im Rahmen dieses Kurses erworbenen Mandanten verbleiben im Eigentum der Microsoft Corporation, und wir behalten uns das Recht vor, jederzeit auf Mandanten zuzugreifen und diese zurückzuziehen.

# Qualifikationsaufgaben

Ihre Aufgabe besteht darin, einen benutzerdefinierten vertraulichen Informationstyp (SIT) zu erstellen, der die erforderlichen Kriterien erfüllt:

- **Benutzerdefiniertes Regex-Muster für Mitarbeiter-ID**: Fügen Sie ein regex-Muster hinzu, das die eindeutige Mitarbeiter-ID-Konfiguration Ihrer Organisation identifiziert, die aus 9 Zeichen besteht: 3 Ziffern, ein Gedankenstrich, gefolgt von 5 Buchstaben (z. B. 123-abcde).
- **Schlüsselwortliste, die Mitarbeiter-IDs zugeordnet ist**: Integrieren Sie eine Liste von Schlüsselwörtern, die häufig mit Mitarbeiter-IDs verknüpft sind, um die Erkennungsgenauigkeit zu verbessern.

## Aufgabe 1 – Erstellen Sie einen vertraulichen Informationstyp

1. Rufen Sie das Microsoft Purview Compliance-Portal auf.
1. Erweitern Sie die **Datenklassifizierung** und wählen Sie dann **Klassifizierungen** aus.
1. Wählen Sie **Typen vertraulicher Informationen** aus und wählen Sie dann **+Vertraulichen Informationstyp** erstellen.
1. Geben Sie auf der Seite **Benennen Sie Ihren vertraulichen Informationstyp** einen aussagekräftigen **Namen** und eine **Beschreibung** ein und wählen Sie dann **Weiter**.
1. Wählen Sie auf der Seite **Muster für diesen vertraulichen Informationstyp definieren** die Option **Muster erstellen** aus.
1. Auf der Seite **Neues Muster** wählen Sie **+ Primärelement hinzufügen** > **Regulärer Ausdruck**.
1. Geben Sie auf der Seite **Einen regulären Ausdruck hinzufügen** dem regulären Ausdruck einen aussagekräftigen Namen für **ID** und geben Sie `\d{3}-[a-zA-Z]{5}` in das Feld **Regulärer Ausdruck** ein, was den Anforderungen der Organisation entspricht. Wählen Sie **Fertig** nach Abschluss aus.
1. Zurück auf der Seite **Neues Muster** unter **Unterstützende Elemente** wählen Sie **+ Unterstützende Elemente oder Elementgruppe hinzufügen** > **Schlüsselwortliste**.
1. Geben Sie auf der Seite **Schlüsselwortliste hinzufügen** Ihrer Schlüsselwortliste eine aussagekräftige **ID**. Geben Sie in der **Schlüsselwortgruppe Nr. 1** unter **Groß-/Kleinschreibung nicht beachtet** Folgendes ein:
   - `Employee ID`
   - `Staff number`
   - `Work ID`
1. Wählen Sie **Fertig** nach Abschluss aus.
1. Wählen Sie auf der Seite **Neues Muster** die Option **Erstellen** aus.
1. Wählen Sie **Weiter** auf der Seite **Muster für diesen vertraulichen Informationstyp definieren** aus.
1. Lassen Sie auf der Seite **Wählen Sie die empfohlene Konfidenzstufe für die Anzeige in den Konformitätsrichtlinien** die Standardeinstellung ausgewählt und wählen Sie dann **Weiter**.
1. Überprüfen Sie Ihre Einstellungen, und wählen Sie dann **Erstellen** aus.
1. Wählen Sie auf der Seite **Ihr vertraulicher Informationstyp ist erstellt** die Option **Fertig**.

Sie haben nun erfolgreich einen benutzerdefinierten vertraulichen Informationstyp (SIT) erstellt, um die Sicherheit und Verwaltung der eindeutigen Mitarbeiter-ID-Nummern Ihres Unternehmens zu verbessern.
