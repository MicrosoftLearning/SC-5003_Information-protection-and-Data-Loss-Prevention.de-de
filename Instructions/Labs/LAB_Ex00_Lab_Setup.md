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

In dieser Aufgabe aktivieren Sie die Überwachung im Microsoft Purview-Portal, um Portalaktivitäten zu überwachen. Für die Aufgaben in diesen Übungen ist die Überwachung erforderlich, um eine Richtlinie für die automatische Bezeichnung zu erstellen.

1. Navigieren Sie in Microsoft Edge zum Microsoft Purview-Portal, `https://purview.microsoft.com`, und melden Sie sich als Benutzender mit **Global Administrator**-Rechten an.

1. Auf dem Bildschirm erscheint eine Meldung über das neue Microsoft Purview-Portal. Wählen Sie die Option, um den Bedingungen für die Veröffentlichung des Datenflusses und der Datenschutzerklärung zuzustimmen, und wählen Sie dann **Jetzt testen** aus.

    ![Screenshot des Bildschirms „Willkommen im neuen Microsoft Purview-Portal“.](../Media/welcome-purview-portal.png)

1. Wählen Sie **Lösungen** in der linken Seitenleiste und wählen Sie dann **Überwachen**.

1. Wählen Sie auf der Seite **Suche** die Leiste **Aufzeichnung von Benutzenden- und Admin-Aktivitäten starten** aus, um die Überwachungsprotokollierung zu aktivieren.

    ![Der Screenshot zeigt die Schaltfläche „Aufzeichnung von Benutzenden- und Admin-Aktivitäten starten".](../Media/enable-audit-button.png)

1. Sobald Sie diese Option wählen, sollte der blaue Balken von dieser Seite verschwinden.

Sie haben die Überwachung in Microsoft 365 erfolgreich aktiviert.

## Aufgabe – Zuweisen von Compliancerollen

In dieser Aufgabe weisen Sie dem Benutzenden, den Sie mithilfe dieser Übungen verwenden werden, den **Complianceadministrator** zu.

1. Öffnen Sie **Microsoft Edge** und navigieren Sie zum Microsoft 365 Admin Center, `https://admin.microsoft.com`. Sie müssen sich als ein Benutzender anmelden, der **globale Administrator**-Rechte hat.

1. Erweitern Sie **Benutzende** in der linken Seitenleiste und wählen Sie dann **Aktive Benutzende**.

1. Wählen oder erstellen Sie einen Benutzenden, um mit diesen Übungen fortzufahren.

   Wenn Sie einen vorhandenen Benutzenden verwenden möchten, wählen Sie einen Benutzenden mit minimalen Rechten, um ihm den geringsten Zugriff zu ermöglichen.

   1. Wenn Sie einen neuen Benutzenden anlegen, weisen Sie ihm eine Lizenz zu, die für diese Übungen geeignet ist. Der Benutzende muss über eine Microsoft 365 E5-Lizenz oder ein kompatibles Add-on für diese Übungen verfügen. Weisen Sie dem Benutzenden die Rolle **Complianceadministrator** in den optionalen Einstellungen beim Einrichten des neuen Benutzenden zu und schließen Sie die Erstellung des neuen Benutzenden ab.

   1. Wenn Sie die Barrierefreiheit eines bestehenden Benutzenden ändern möchten, wählen Sie ihn aus und wählen Sie dann **Rollen verwalten**. Weisen Sie dem Benutzenden die Rolle **Complianceadministrator** zu und speichern Sie Ihre Änderungen.

1. Melden Sie sich von dem Konto mit dem Zugriff des globalen Administrators ab, indem Sie das Symbol der bzw. des Benutzenden oben rechts auswählen und dann **Abmelden** auswählen.

   Beispiel:

   ![Screenshot zeigt den Navigationspfad zur Abmeldung vom MOD-Administratorkonto.](../Media/sign-out.png)

Sie haben einem Benutzenden erfolgreich die Rolle **Complianceadministrator** zugewiesen, die zur Durchführung der verschiedenen Übungen in dieser Übung erforderlich ist.

## Aufgabe – Erkunden des Microsoft Purview-Portals

In dieser Aufgabe melden Sie sich als der Benutzende an, dem Sie zuvor die Rolle **Complianceadministrator** zugewiesen haben, um das Microsoft Purview-Portal zu erkunden. Diese Rolle wird in den nächsten Übungen als Ihr **Complianceadministrator** bezeichnet.

1. Navigieren Sie in **Microsoft Edge** zu **`https://purview.microsoft.com`**.

1. Wenn das Fenster **Konto auswählen** angezeigt wird, wählen Sie **Ein anderes Konto verwenden**.

1. Wenn das Fenster **Anmelden** angezeigt wird, melden Sie sich als der Benutzende an, den Sie zuvor als **Complianceadministrator** ausgewählt haben.

1. Machen Sie sich mit dem neuen Microsoft Purview-Portal vertraut. Wenn Sie fertig sind, lassen Sie das Browserfenster geöffnet.

Sie haben erfolgreich zum Konto des ** Complianceadministrators** gewechselt und sind nun bereit, die Übung zu starten.
