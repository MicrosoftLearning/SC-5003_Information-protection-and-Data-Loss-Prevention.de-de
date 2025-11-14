---
lab:
  task: Create and publish a sensitivity label
  exercise: Exercise 2 - Create and publish a sensitivity label
---

# Qualifikationsaufgaben

Ihre Aufgabe besteht darin, Vertraulichkeitsbezeichnungen in Ihrer Organisation zu erstellen und zu veröffentlichen, die vertrauliche Daten entsprechend ihrer Vertraulichkeitsstufe und den erforderlichen Zugriffskontrollen klassifiziert und schützt.

**Aufgaben:**

1. Aktivieren der Unterstützung für Vertraulichkeitsbezeichnungen  
1. Erstellen einer Bezeichnungsgruppe  
1. Erstellen einer untergeordneten Bezeichnung  
1. Veröffentlichen von Bezeichnungen  
1. Konfigurieren automatischer Bezeichnungen  

## Aufgabe 1 – Aktivieren der Unterstützung für Vertraulichkeitsbezeichnungen in SharePoint und OneDrive

In dieser Aufgabe aktivieren Sie die Co-Authoring-Funktion für Vertraulichkeitsbezeichnungen, die auch Vertraulichkeitsbezeichnungen für Dateien in SharePoint und OneDrive ermöglicht.

1. Öffnen Sie **Microsoft Edge**, und navigieren Sie dann zu `https://purview.microsoft.com`.

1. Wählen Sie in der linken Navigation **Einstellungen** > **Informationsschutz**.

1. In den **Einstellungen für den Informationsschutz** stellen Sie sicher, dass Sie sich auf der Registerkarte **Co-Authoring für Dateien mit Vertraulichkeitsbezeichnungen** befinden.

1. Aktivieren Sie das Kontrollkästchen für **Ko-Authoring für Dateien mit Vertraulichkeitsbezeichnungen einschalten**.

1. Wählen Sie **Anwenden** am unteren Rand des Bildschirms.

Sie haben erfolgreich den Kundendienst für Vertraulichkeitsbezeichnungen für Dateien in SharePoint und OneDrive aktiviert.

<!--

## Task 2 – Create sensitivity labels

In this task, your HR department has requested a sensitivity label to apply to HR employee documents. You'll create a sensitivity label for internal documents and a sublabel for the HR department.

1. Open **Microsoft Edge** and navigate to **`https://purview.microsoft.com`**. Log into Microsoft Purview as the user you selected as the **Compliance Administrator**.

1. In the Microsoft Purview portal, select **Solutions** from the left sidebar, then select **Information Protection**.

1. On the **Microsoft Information Protection** page, on the left sidebar, select **Sensitivity labels**.

1. On the **Sensitivity labels** page select **+ Create a label**.

1. The **New sensitivity label** configuration will start. On the **Provide basic details for this label**, enter:

    - **Name**: `Internal`
    - **Display name**: `Internal`
    - **Description for users**: `Internal sensitivity label.`
    - **Description for admins**: `Internal sensitivity label for Contoso.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files** and **Emails**. If the checkbox for **Meetings** is selected, make sure it's deselected.

   > [!NOTE]
   > When **Meetings** is selected, you can't create a sublabel for the sensitivity label.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select **Next**.

1. On the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Don't create a policy yet**, then select **Done**.

1. On the **Sensitivity labels** page, find the newly created **Internal** sensitivity label. Select the vertical ellipsis (**...**) next to it, then select **+ Create sublabel** from the dropdown menu.

    ![Screenshot showing the Action menu to create a sublabel for a sensitivity label.](../Media/create-sublabel-button.png)

1. The **New sensitivity label** wizard will start. On the **Provide basic details for this label** page enter:

   - **Name**: `Employee data (HR)`
   - **Display name**: `Employee data (HR)`
   - **Description for users**: `This HR label is the default label for all specified documents in the HR Department.`
   - **Description for admins**: `This label was created with input from the Head of HR. Contact the HR department for any changes to the label settings.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files**, **Emails**, and **Meetings**.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select the **Control access** option, then select **Next**.

1. On the **Access control** page, select **Configure access control settings**.

1. Configure the encryption settings with these options:

   - **Assign permissions now or let users decide?**: Assign permissions now
   - **User access to content expires**: Never
   - **Allow offline access**: Only for a number of days
   - **Users have offline access to the content for this many days**: 15
   - Select the **Assign permissions** link. On the **Assign permissions** flyout panel, select the **+ Add any authenticated users**, then select **Save** to apply this setting.

1. On the **Access control** page, select **Next**.

1. On the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Don't create a policy yet**, then select **Done**.

You have successfully created a sensitivity label for your organizations internal policies and a sensitivity sublabel for the Human Resources (HR) department.

## Task 3 – Publish sensitivity labels

You will now publish the Internal and HR sensitivity label so that the published sensitivity labels will be available for the HR users to apply to their HR documents.

1. In **Microsoft Edge**, the Microsoft Purview portal tab should still be open. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. On the **Sensitivity labels** page select **Publish labels**.

1. The publish sensitivity labels configuration will start.

1. On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.

1. On the **Sensitivity labels to publish** flyout panel, select the **Internal** and **Internal/Employee Data (HR)** checkboxes, then select **Add** at the bottom of the flyout panel.

1. Back on the **Choose sensitivity labels to publish** page, select **Next**.

1. On the **Assign admin units** page, select **Next**

1. On the **Publish to users and groups** page, select **Next**.

1. On the **Policy settings** page, select **Next**.

1. On the **Default settings for documents** page, select **Next**.

1. On the **Default settings for emails** page, select **Next**.

1. On the **Default settings for meetings and calendar events** page, select **Next**.

1. On the **Default settings for Fabric and Power BI content** page, select **Next**.

1. On the **Name your policy** page, enter:

   - **Name**: `Internal HR employee data`
   - **Enter a description for your sensitivity label policy**: `This HR label is to be applied to internal HR employee data.`

1. Select **Next**.

1. On the **Review and finish** page, select **Submit**.

1. On the **New policy created**, select **Done** to finish publishing your label policy.

You have successfully published the Internal and HR sensitivity labels. Note that it can take up to 24 hours for changes to replicate to all users and services.

## Task 4 – Create a client-side auto labeling policy

In this task, you'll create a client-side auto-labeling policy. Client-side auto-labels apply automatically to files and emails based on their content, ensuring that sensitive information is classified and protected before it leaves the user's device.

1. You should still be on the **Sensitivity labels** page in the Microsoft Purview portal. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. On the **Sensitivity labels** page, find the newly created **Internal** sensitivity label. Select the vertical ellipsis (**...**) next to it, then select **+ Create sublabel** from the dropdown menu.

1. The **New sensitivity label** configuration will start. On the **Provide basic details for this label** page, enter:

   - **Name**: `Confidential Research Data`
   - **Display name**: `Confidential Research Data`
   - **Description for users**: `This document or email contains sensitive research or development data that is proprietary to the organization.`
   - **Description for admins**: `This label is auto-applied to documents and emails containing information related to research, prototypes, or internal projects.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files**, **Emails**, and **Meetings**.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select **Apply content marking**, then select **Next**.

1. Select **Next**.

1. On the **Content marking** page, select the toggle to enable content marking.

1. If the checkbox for **Add a footer** is selected, deselect it, and select the checkbox for **Add a watermark**, then select **Customize text**.

1. In the **Customize watermark text** flyout pane, enter `Confidential - R&D Data` as **Watermark text**. Increase the **Font size** to `40`, then select **Save** at the bottom of the panel.

1. Back on the **Content marking** page, if other content marking options are enabled, disable them to ensure **Add a watermark** is the only option enabled.

1. Select **Next**.

1. On the **Auto-labeling for files and emails** page, set the **Auto-labeling for files and emails** to enabled.

1. In the **Detect content that matches these conditions** section, select **+ Add condition** > **Content contains**.

1. In **Content contains** section select the **Add** > **Trainable classifiers**.

1. In the **Trainable classifiers** flyout panel, add these trainable classifiers:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

1. Select **Add** at the bottom of the panel to add these trainable classifiers.

1. Back on the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Publish label to users' apps**, then select **Done**.

1. On the **Publish label** flyout panel, select **Create new label policy**.

1. On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.

1. Select the parent **Internal** label and the **Confidential Research Data** label that was just created, then select **Add**.

1. Back on the **Choose sensitivity labels to publish** page, select **Next**.

1. On the **Assign admin units** page, select **Next**.

1. On the **Publish to users and groups** page, select **Next**.

1. On the **Policy settings** page, select the checkbox for **Users must provide a justification to remove a label or lower its classification**, then select **Next**.

1. On the **Default settings for documents** page, select **Next** until you reach the **Name your policy** page.

1. On the **Name your policy** page, enter:

   - **Name**: `R&D Confidential Data Policy`
   - **Enter a description for your sensitivity label policy**: `Automatically applies labels to source code, project documents, and development files to protect sensitive R&D data.`

1. Select **Next**.

1. On the **Review and finish** page, select **Submit**.

1. On the **New policy created** page, select **Done**.

You have successfully created a client-side auto-labeling policy that will automatically apply the **Confidential Research Data** label to files and emails containing research and development data. It might take up to 24 hours for the policy to take full effect.

## Task 5 – Create a service-side auto labeling policy

In this task, you'll create a service-side auto-labeling policy. Service-side auto-labels are applied by cloud services like SharePoint, Exchange, and OneDrive after content is uploaded or received, ensuring that sensitive data is protected even if users don't manually classify it.

1. You should still be on the **Sensitivity labels** page in the Microsoft Purview portal. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. Expand the **Internal** label, then select the `Confidential Research Data` sublabel you created in a previous task.

1. In the **Confidential Research Data** flyout panel, you'll see the properties for the auto-label you created in a previous task. In this panel, select **Create auto-labeling policy**.

    ![Screenshot showing the option to create an auto-labeling policy.](../Media/create-auto-labeling-policy.png)

1. On the **Name your policy** page, enter:

   - **Name**: `R&D Confidential Data Container Policy`
   - **Enter a description for your sensitivity label policy**: `Automatically applies the Confidential Research Data label to content in SharePoint, Exchange, and OneDrive.`

1. Select **Next**.

1. On the **Assign admin units** page, select **Next**.

1. On the **Choose locations where you want to apply the label** page, leave **Exchange email**, **SharePoint sites**, and **OneDrive accounts** selected, then select **Next**.

1. On the **Set up common or advanced rules** page, leave **Common rules** selected, then select **Next**.

1. On the **Define rules for content in all locations** page, edit the **Confidential Research Data rule**.

    ![Screenshot where to edit the rule for a service-side auto-labeling policy.](../Media/auto-apply-labels-edit-rule.png)

1. In the **New rule** flyout panel, under **Conditions** > **Content contains** select the dropdown for **Add**, then select **Trainable classifiers**.

1. In the **Trainable classifiers** flyout panel, add these trainable classifiers:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

   This ensures consistent protection between client-side and service-side labels.

1. Select **Add** at the bottom of the panel to add these trainable classifiers.

1. Back on the **Define rules for content in all locations** page, select **Next**.

1. On the **Choose a label to auto-apply**, leave the **Internal/Confidential Research Data** chosen, then select **Next**.

1. On the **Decide if you want to test out the policy now or later** page, select **Run policy in simulation mode**, and select the checkbox for **Automatically turn on policy if not modified after 7 days in simulation**, then select **Next**.

1. On the **Review and finish** page, select **Create policy**.

1. On the **Your auto-labeling policy was created** page, select **Done**.

You have successfully created a service-side auto-labeling policy that will automatically apply the **Confidential Research Data** label to content stored or shared in SharePoint, Exchange, and OneDrive. It might take up to 24 hours for the policy to take effect.

-->
## Aufgabe 2 – Erstellen einer Bezeichnungsgruppe

In dieser Aufgabe erstellen Sie eine Bezeichnungsgruppe, um interne Vertraulichkeitsbezeichnungen zu organisieren. Bezeichnungsgruppen fungieren als Container für verwandte Bezeichnungen wie Klassifizierungen von Abteilungen oder Geschäftseinheiten.

1. Sie sollten weiterhin als Compliance-Admin beim Microsoft Purview-Portal angemeldet sein.

1. Navigieren Sie in **Microsoft Edge** zu `https://purview.microsoft.com`.

1. Wählen Sie im Microsoft Purview-Portal in der linken Seitenleiste **Lösungen** und dann **Informationsschutz**.

1. Wählen Sie auf der Seite **Microsoft Information Protection** in der linken Seitenleiste **Vertraulichkeitsbezeichnungen**.

1. Wählen Sie auf der Seite **Vertraulichkeitsbezeichnungen** die Option **+ Erstellen** > **Bezeichnungsgruppe** aus.

1. Die Konfiguration **Neue Bezeichnungsgruppe** wird gestartet. Geben Sie unter **Grundlegende Details für diese Bezeichnungsgruppe bereitstellen** Folgendes ein:

    - **Name**: `Internal`
    - **Anzeigename**: `Internal`
    - **Beschreibung für Benutzende**: `Internal sensitivity label.`
    - **Beschreibung für Administratoren**: `Internal sensitivity label group for Contoso.`

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Einstellungen überprüfen und fertigstellen** die Option **Bezeichnungsgruppe erstellen** aus.

1. Wählen Sie auf der Seite **Ihre Bezeichnungsgruppe wurde erfolgreich erstellt** die Option **Noch keine Bezeichnung erstellen** und dann **Fertig** aus.

Sie haben eine Bezeichnungsgruppe für die interne Verwendung erstellt. Diese Gruppe hilft Ihnen beim Verwalten verwandter Bezeichnungen für bestimmte Abteilungen oder Datenkategorien.

## Aufgabe 3 – Erstellen einer untergeordneten Bezeichnung

Nachdem Sie nun eine Bezeichnungsgruppe erstellt haben, fügen Sie eine untergeordnete Bezeichnung für Inhalte im Zusammenhang mit der Personalverwaltung hinzu. Diese Bezeichnung erzwingt Verschlüsselungs- und Inhaltsmarkierungen, um Personalverwaltungsdaten vor unbefugtem Zugriff zu schützen.

1. Suchen Sie auf der Seite **Vertraulichkeitsbezeichnungen** die Vertraulichkeitsbezeichnungsgruppe **Intern**. Wählen Sie die vertikalen Auslassungspunkte (**…**) daneben und dann im Dropdownmenü **+ Bezeichnung in Gruppe erstellen** aus.

    ![Screenshot des Aktionsmenüs, mit dem eine Bezeichnung in Gruppe für eine Vertraulichkeitsbezeichnung erstellt wird.](../Media/create-label-in-group.png)

1. Der Assistent **Neue Vertraulichkeitsbezeichnung** wird gestartet. Geben Sie auf der Seite **Basisdetails für diese Bezeichnung bereitstellen** Folgendes ein:

   - **Name**: `Employee data (HR)`
   - **Anzeigename**: `Employee data (HR)`
   - **Beschreibung für Benutzende**: `This HR label is the default label for all specified documents in the HR Department.`
   - **Beschreibung für Administratoren**: `This label is created in consultation with Ms. Jones (Head of the HR department). Contact her if you need to change the label settings.`

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Definieren Sie den Geltungsbereich für diese Kennzeichnung** **Dateien** und **E-Mails**. Wenn das Kontrollkästchen für **Besprechungen** aktiviert ist, stellen Sie sicher, dass es abgewählt ist.

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Schutzeinstellungen für bezeichnete Elemente auswählen** die Optionen **Zugriff kontrollieren** und **Inhaltsmarkierung anwenden** und wählen Sie dann **Weiter**.

1. Wählen Sie auf der Seite **Zugriffssteuerung** die Option **Konfigurieren der Einstellungen für die Zugriffssteuerung**.

1. Konfigurieren Sie die Verschlüsselungseinstellungen mit diesen Optionen:

   - **Berechtigungen jetzt zuweisen oder die Benutzenden entscheiden lassen?**: Berechtigungen jetzt zuweisen
   - **Benutzender-Zugriff auf Inhalte läuft ab**: Nie
   - **Offlinezugriff erlauben**: Nur für eine bestimmte Anzahl von Tagen
   - **Benutzende haben für so viele Tage Offlinezugriff auf den Inhalt**: 15
   - Wählen Sie den Link **Berechtigungen zuweisen**. Wählen Sie im Flyout-Bedienfeld **Berechtigungen zuweisen** die Option **+ Alle authentifizierten Benutzenden hinzufügen**, und wählen Sie dann **Speichern**, um diese Einstellung zu übernehmen.

1. Auf der Seite **Zugriffssteuerung** wählen Sie **Weiter**.

1. Wählen Sie auf der Seite **Inhaltsmarkierung** den Schalter, um die **Inhaltsmarkierung** zu aktivieren.

1. Aktivieren Sie für jeden der folgenden Typen das Kontrollkästchen und wählen Sie dann das Symbol „Bearbeiten“, um den Text einzugeben:

   |Kennzeichnungstyp|Text|
   |:---|:---|
   |Ein Wasserzeichen hinzufügen|`INTERNAL USE ONLY`|
   |Hinzufügen einer Kopfzeile|`Internal Document`|
   |Hinzufügen einer Fußzeile|`Contoso Confidential`|

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Automatische Bezeichnung für Dateien und E-Mails** **Weiter**.

1. Wählen Sie auf der Seite **Schutzeinstellungen für Gruppen und Standorte festlegen** die Option **Weiter**.

1. Wählen Sie auf der Seite **Einstellungen überprüfen und fertig stellen** die Option **Bezeichnung erstellen** aus.

1. Wählen Sie auf der Seite **Vertraulichkeitsbezeichnung** die Option **Richtlinie noch nicht erstellen** aus, und wählen Sie dann **Fertig** aus.

Sie haben eine untergeordnete Bezeichnung innerhalb der Bezeichnungsgruppe „Intern“ erstellt. Die Bezeichnung wendet Verschlüsselungs- und Inhaltsmarkierungen auf Personalverwaltungsdokumente an, wodurch vertrauliche Daten leicht zu identifizieren und durch Richtlinien geschützt werden können.

## Aufgabe 4 – Veröffentlichen von Bezeichnungen

Als Nächstes veröffentlichen Sie die Personalverwaltungsbezeichnung aus der Bezeichnungsgruppe „Intern“, damit Benutzende in der Personalabteilung sie auf ihre Dokumente anwenden können.

1. Sie sollten weiterhin als Compliance-Admin beim Microsoft Purview-Portal angemeldet sein.

1. In **Microsoft Edge** sollte die Registerkarte des Microsoft Purview-Portals noch geöffnet sein. Falls nicht, navigieren Sie zu **`https://purview.microsoft.com`** > **Lösungen** > **Informationsschutz** > **Vertraulichkeitsbezeichnungen**.

1. Auf der Seite **Vertraulichkeitsbezeichnungen** wählen Sie **Bezeichnungen veröffentlichen**.

1. Die Konfiguration der Veröffentlichung von Vertraulichkeitsbezeichnungen wird gestartet.

1. Wählen Sie auf der Seite **Wählen Sie die zu veröffentlichenden Vertraulichkeitsbezeichnungen** den Link **Wählen Sie die zu veröffentlichenden Vertraulichkeitsbezeichnungen**.

1. Aktivieren Sie im Flyout-Bereich **Vertraulichkeitsbezeichnungen zum Veröffentlichen**das Kontrollkästchen **Interne/Mitarbeiterdaten (HR)** und wählen Sie dann unten auf der Flyout-Seite **Hinzufügen** aus.

1. Zurück auf der Seite **Wählen Sie die zu veröffentlichenden Vertraulichkeitsbezeichnungen aus**, wählen Sie **Weiter**.

1. Wählen Sie auf der Seite **Admineinheiten zuweisen** **Weiter**

1. Wählen Sie auf der Seite **Veröffentlichen für Benutzer und Gruppen** die Option **Weiter**.

1. Wählen Sie auf der Seite **Richtlinieneinstellungen** **Weiter**.

1. Auf der Seite **Standardeinstellungen für Dokumente** wählen Sie **Weiter**.

1. Auf der Seite **Standardeinstellungen für E-Mails** wählen Sie **Weiter**.

1. Auf der Seite **Standardeinstellungen für Besprechungen und Kalenderereignisse** wählen Sie **Weiter**.

1. Wählen Sie auf der Seite **Standardeinstellungen für Fabric- und Power BI-Inhalte** die Option **Weiter**.

1. Auf der Seite **Benennen Sie Ihre Richtlinie**, geben Sie ein:

   - **Name**: `Internal HR employee data`

   - **Geben Sie eine Beschreibung für Ihre Vertraulichkeitsbezeichnungsrichtlinie** ein: `This HR label is to be applied to internal HR employee data.`

1. Wählen Sie **Weiter** aus.

1. Auf der Seite **Überprüfen und beenden** wählen Sie **Absenden**.

1. Wählen Sie auf der Seite **Neue Richtlinie erstellt** die Option **Erledigt**, um die Veröffentlichung Ihrer Bezeichnungsrichtlinie zu beenden.

Sie haben die Bezeichnungsgruppe „Intern“ und die zugehörige Personalverwaltungsbezeichnung veröffentlicht, damit Benutzende sie auf Personalverwaltungsdokumente anwenden können. Es kann bis zu 24 Stunden dauern, bis die Richtlinie auf die Dienste verteilt wird.

## Aufgabe 5 – Konfigurieren automatischer Bezeichnungen

Sie erstellen nun eine untergeordnete Bezeichnung für Finanzdaten und konfigurieren sie so, dass sie automatisch auf Inhalte angewendet wird, die Finanz-IDs wie Kreditkarten- oder Bankleitzahlen enthalten.

1. Sie sollten weiterhin als Compliance-Admin beim Microsoft Purview-Portal angemeldet sein.

1. Navigieren Sie in **Microsoft Edge** zu `https://purview.microsoft.com` und melden Sie sich beim als Compliance-Admin beim Microsoft Purview-Portal an.

1. Wählen Sie im Microsoft Purview-Portal **Lösungen** > **Informationsschutz** > **Vertraulichkeitsbezeichnungen**.

1. Auf der Seite **Vertraulichkeitsbezeichnungen** finden Sie die Vertraulichkeitsbezeichnung **Intern**. Wählen Sie die vertikalen Auslassungspunkte (**…**) und dann im Dropdownmenü **+ Bezeichnung in Gruppe erstellen** aus.

1. Geben Sie auf der Seite **Basisdetails für diese Bezeichnung bereitstellen** Folgendes ein:

   |Details|Text|
   |---|---|
   |**Name**|`Financial Data`|
   |**Anzeigename**|`Financial Data`|
   |**Beschreibung für Benutzende**|`This content contains financial data that must be labeled and protected.`|
   |**Beschreibung für Admins**|`This label is used for content that includes sensitive financial identifiers.`|

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Definieren Sie den Geltungsbereich für diese Kennzeichnung** **Dateien** und **E-Mails**. Wenn das Kontrollkästchen für **Besprechungen** aktiviert ist, stellen Sie sicher, dass es abgewählt ist.

1. Wählen Sie **Weiter** aus.

1. Wählen Sie auf der Seite **Schutzeinstellungen für gekennzeichnete Elemente festlegen** **Weiter**.

1. Auf der Seite **Automatische Bezeichnungen für Dateien und E-Mails** legen Sie die **Automatische Bezeichnungen für Dateien und E-Mails** auf „aktiviert" fest.

1. Wählen Sie im Abschnitt **Inhalt erkennen, der diesen Bedingungen entspricht** die Option **+ Bedingung hinzufügen** > **Inhalt enthält**.

1. Wählen Sie im Abschnitt **Inhalt enthält** die Option **Hinzufügen** > **Typen vertraulicher Informationen**.

1. Suchen Sie auf der Flyout-Seite **Typen vertraulicher Informationen** nach den Typen vertraulicher Informationen und wählen Sie diese aus:

   - `Credit Card Number`
   - `ABA Routing Number`
   - `SWIFT Code`

1. Wählen Sie **Hinzufügen**.

1. Zurück auf der Seite **Automatische Bezeichnung für Dateien und E-Mails**, wählen Sie **Weiter**.

1. Wählen Sie auf der Seite **Schutzeinstellungen für Gruppen und Standorte festlegen** die Option **Weiter**.

1. Wählen Sie auf der Seite **Einstellungen überprüfen und fertig stellen** die Option **Bezeichnung erstellen** aus.

1. Wählen Sie auf der Seite **Ihre Vertraulichkeitsbezeichnung wurde erstellt** die Option **Kennzeichnung automatisch auf vertrauliche Inhalte anwenden** und dann **Erledigt**.

1. Wählen Sie auf der Flyout-Seite **Automatische Bezeichnung erstellen** die Option **Review-Richtlinie**.

1. Auf der Seite **Benennen Sie Ihre automatische Bezeichnung** belassen Sie die Voreinstellung und wählen Sie dann **Weiter**.

1. Überprüfen Sie auf der Seite **Wählen Sie eine Kennzeichnung, die automatisch angewendet werden soll**, ob die Kennzeichnung _Interne/Finanzdaten_ ausgewählt ist, und wählen Sie dann **Weiter**.

1. Wählen Sie auf der Seite **Admineinheiten zuweisen** **Weiter**.

1. Wählen Sie auf der Seite **Wählen Sie Standorte aus, an denen Sie die Kennzeichnung anwenden möchten** die Optionen für:

   - Exchange-E-Mail
   - SharePoint-Websites
   - OneDrive Konten

1. Wählen Sie **Weiter** aus.

1. Lassen Sie auf der Seite **Gemeinsame oder erweiterte Regeln einrichten** die Standardeinstellung **Gemeinsame Regeln** ausgewählt, und wählen Sie dann **Weiter**.

1. Erweitern Sie auf der Seite **Regeln für Inhalte an allen Standorten definieren** die Regeln für _Finanzdatenregel_, um sicherzustellen, dass die erwarteten Regeln definiert sind, und wählen Sie dann **Weiter**.

1. Wählen Sie auf der Seite **Zusätzliche Einstellungen für E-Mail** **Weiter**.

1. Wählen Sie auf der Seite **Entscheiden Sie, ob Sie die Richtlinie jetzt oder später testen möchten** die Option **Richtlinie im Simulationsmodus ausführen** und aktivieren Sie das Kontrollkästchen für **Richtlinie automatisch einschalten, wenn sie nach 7 Tagen in der Simulation nicht geändert wurde**.

1. Wählen Sie **Weiter** aus.

1. Auf der Seite **Überprüfen und beenden** wählen Sie **Richtlinie erstellen**.

1. Wählen Sie auf der Seite Ihre **Richtlinie für die automatische Bezeichnung wurde erstellt** die Option **Fertig**.

Sie haben Bezeichnungen in einer Gruppe organisiert, sie für Benutzende veröffentlicht und automatische Bezeichnungen aktiviert, sodass vertrauliche Inhalte geschützt sind, ohne dass Benutzende dafür verantwortlich sind.
