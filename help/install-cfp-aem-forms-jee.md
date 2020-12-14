---
title: Kumulative Fix Packs auf AEM Forms JEE installieren
description: Übersicht der Schritte zur Installation und Konfiguration des Cumulative Fix Pack (CFP) auf AEM Forms JEE
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 23%

---


# Kumulative Fix Packs auf AEM[!DNL  Forms] JEE installieren{#installing-cumulative-fix-packs-on-aem-forms-jee}

## CFP auf AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3} installieren

Führen Sie die folgenden Schritte in der angegebenen Reihenfolge durch, um das kumulative Fix Pack auf AEM 6.3 [!DNL Forms JEE] zu installieren.

1. Wenden Sie sich an den [Support für Adoben](https://www.adobe.com/de/account/sign-in.supportportal.html), um das AEM 6.3 [!DNL Forms JEE]-Installationsprogramm für die CFP abzurufen.
1. Führen Sie das CFP-Installationsprogramm aus und konfigurieren Sie AEM [!DNL Forms JEE] wie unter [AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee) installieren und konfigurieren beschrieben.
1. Installieren Sie die neueste AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. [!DNL Forms] Hinzufügen-On-Paket für AEM CFP [6.3.x](aem-forms-releases.md) installieren

### Installieren AEM [!DNL Forms JEE]-Pakete {#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1; Version 1.0.2) bietet  [!DNL Forms] Benutzer AEM  [!DNL Forms JEE] dieselben Rechte und Funktionen wie AEM  [!DNL Forms OSGi]. Überprüfen Sie die installierten Pakete im Package Manager und installieren Sie das Paket, falls es noch nicht installiert ist.

### Zusätzliche Anweisungen für CQ-4208044 {#additional-instructions-for-cq}

Wenn Sie AEM 6.3 [!DNL Forms JEE]-Server mit Oracle-Datenbank verwenden, konfigurieren Sie die folgenden Einstellungen nach der Bereitstellung von CFP1, d. h. nach der Ausführung von Configuration Manager. Diese Einstellung ist erforderlich, um Benutzer, Gruppen und Gruppenmitglieder zu synchronisieren, wenn die Synchronisierung der Unternehmensdomäne ausgeführt wird. Siehe Problem CQ-4208044 in [AEM 6.3 Versionshinweise](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Melden Sie sich bei der Benutzeroberfläche **Admin** an.
1. Navigieren Sie zu **[!UICONTROL Einstellungen]** > **[!UICONTROL Benutzerverwaltung]** > **[!UICONTROL Konfiguration]** > **[!UICONTROL Konfigurationsdatei importieren und exportieren]**
1. Exportieren Sie die Datei &quot;config.xml&quot;.
1. Ändern Sie den Eintrag für &quot;`groupMemberDBQueryBatchSize`&quot;unter Ihren Domänenkonfigurationen in *config.xml*. Beispieleintrag:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. Importieren Sie die geänderte Datei erneut und führen Sie dann die Synchronisierung erneut aus.

## CFP auf AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee} installieren

Führen Sie die folgenden Schritte in der angegebenen Reihenfolge durch, um das kumulative Fix Pack auf AEM 6.2 [!DNL Forms JEE] zu installieren.

>[!NOTE]
>
>Wenn Sie AEM 6.2 [!DNL Forms OSGi] verwenden, befolgen Sie die Installationsanweisungen in den Versionshinweisen zu [AEM 6.2 CFP.](release-notes-aem-6-2-cumulative-fix-pack.md)

1. Wenden Sie sich an den [Support für Adoben](https://www.adobe.com/account/sign-in.supportportal.html), um das AEM 6.2 [!DNL Forms JEE]-Installationsprogramm für die CFP abzurufen.
1. Führen Sie das CFP-Installationsprogramm aus und konfigurieren Sie AEM [!DNL Forms JEE] wie unter [AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee) installieren und konfigurieren beschrieben.
1. Installieren Sie [AEM Hotfix 12785 Version 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Installieren Sie [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Installieren Sie das neueste [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Installieren Sie das Hinzufügen-On-Paket für [!DNL Forms]AEM 6.2 Service Pack 1 CFP[.](aem-forms-releases.md)

### Installieren AEM [!DNL Forms JEE]-Pakete {#install-aem-forms-jee-bundles-package-1}

[AEM Forms JEE-Paket](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) (aemfd-jee-bundles-package-6.2CFP5; Version 1.0.2) bietet  [!DNL Forms] Benutzer AEM  [!DNL Forms JEE] dieselben Rechte und Funktionen wie AEM  [!DNL Forms OSGi]. Überprüfen Sie die installierten Pakete im Package Manager und installieren Sie das Paket, falls es noch nicht installiert ist.

### Konfigurieren des Timeouts für Vorgänge auf Komponentenebene (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Nach AEM 6.2 CFP4 können Sie die folgenden Anweisungen verwenden, um die Zeitüberschreitung für DSC-Vorgänge zu konfigurieren, falls während des Aktualisierungsprozesses Probleme aufgrund einer Zeitüberschreitung auftreten sollten. (Siehe NPR-16774 in [AEM 6.2 CFP4 Versionshinweise](release-notes-aem-6-2-cumulative-fix-pack.md)).

Die Bereitstellung von DSC dauert je nach Bedarf, da sie fehlschlagen kann. Um den Timeout-Wert von DSC-Vorgängen wie &quot;Installieren&quot;, &quot;Laden&quot;, &quot;Beginn&quot;und &quot;Stopp&quot;zu ändern, müssen Sie `adobe.component.registry.timeout` mit dem JVM-Argument und der Option -D festlegen.

Geben Sie den Wert für den Schlüssel in Sekunden an. Beispiel: `-Dadobe.component.registry.timeout=300`

Sie können die Timeouts auch auf Komponentenebene mithilfe der folgenden drei Eigenschaften ändern:

1. `adobe.all-component.timeout`: überschreibt die Timeouts aller Dienste des Produkts.
1. `adobe.<serviceName>.timeout`: überschreibt die Zeitüberschreitung nur für den im Schlüssel erwähnten Dienst (&lt;servicename>). Wenn der Wert auf Dienstebene festgelegt ist, überschreibt die Verwendung dieses Befehls nur den Timeout-Wert für den angegebenen Dienst, wenn er auf Anwendungsebene festgelegt ist.
1. `adobe.<serviceName>.<operationName>.timeout`: Es überschreibt nur den Timeout für den Vorgang des jeweiligen Dienstes(&lt;servicename>.&lt;operationname>) im Schlüssel erwähnt. Wenn der Wert auf Vorgangsebene festgelegt ist, überschreibt die Verwendung dieses Befehls nur den Timeout-Wert für den angegebenen Dienst, wenn er auf Anwendungs- oder Dienstebene festgelegt ist.

**Beispiele:**

Verwenden Sie die folgenden Befehle, um den Timeout auf Komponentenebene festzulegen:

1. So legen Sie die Zeitüberschreitung für alle Dienstvorgänge auf 600 Sek fest:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Verwenden Sie zum Einstellen des Zeitlimits für die Vorgänge `DesigntimeService` auf 500 Sekunden Folgendes:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Verwenden Sie Folgendes, um das Zeitlimit für die Vorgänge von `DesigntimeService's previewLCA` auf 700 Sekunden festzulegen:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Verwenden Sie zum Festlegen von `DSC operations` wie Laden, Installieren usw. auf 600 Sekunden Folgendes:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installieren und konfigurieren Sie AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Erstellen Sie eine Sicherung des Ordners /deploy. Das ist erforderlich, wenn Sie die Schnellkorrektur deinstallieren.
1. Stoppen Sie den Anwendungsserver.
1. Extrahieren Sie die Patch-Installationsarchivdatei auf Ihre Festplatte.
1. Im Ordner mit dem Namen entsprechend des von Ihnen verwendeten Betriebssystems:

   **Windows**

   Navigieren Sie zum entsprechenden Ordner auf dem Installationsdatenträger oder dem Ordner auf der Festplatte, in den Sie das Installationsprogramm kopiert haben:

   * (Windows 32-Bit): Disk1\InstData\Windows\VM
   * (Windows 64-Bit): Disk1\InstData\Windows_64bit\VM

   Klicken Sie dann bei Dublette und dann auf die Datei mit dem Namen:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Navigieren Sie zum entsprechenden Ordner:

   * (Linux): Disk1/InstData/Linux/NoVM
   * (Solaris): Disk1/InstData/Solaris/NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Geben Sie an einer Eingabeaufforderung Folgendes ein:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Hierdurch wird das Installieren des Assistenten gestartet, der Sie durch die Installation führt.

1. Klicken Sie im Begrüßungsbildschirm auf **[!UICONTROL Weiter]**.
1. Überprüfen Sie im Bildschirm &quot;Installationsordner auswählen&quot;, ob der für die vorhandene Installation angezeigte Standardspeicherort korrekt ist, oder klicken Sie auf **[!UICONTROL Durchsuchen]**, um den alternativen Ordner auszuwählen, in dem AEM [!DNL Forms] derzeit installiert ist, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Lesen Sie die Schnellkorrekturzusammenfassung und klicken Sie auf **[!UICONTROL Weiter]**.
1. Lesen Sie die Informationen zur „Zusammenfassung vor der Installation“ und klicken Sie auf **[!UICONTROL Installieren]**.
1. Wenn die Installation abgeschlossen ist, klicken Sie auf **[!UICONTROL Weiter]**, um die Schnellkorrektur-Updates auf Ihre installierten Dateien anzuwenden.
1. Das Kontrollkästchen Configuration Manager starten ist standardmäßig aktiviert. Klicken Sie auf **[!UICONTROL Fertig]**, um Configuration Manager auszuführen.

   Um Configuration Manager später auszuführen, deaktivieren Sie die Option **[!UICONTROL Configuration Manager starten]**, bevor Sie auf **[!UICONTROL Fertig]** klicken. Sie können Configuration Manager später mit dem entsprechenden Beginn im Ordner *`[AEM_forms_root]`/configurationManager/bin* ausführen.

1. Wählen Sie je nach Anwendungsserver eines der folgenden Dokumente aus und befolgen Sie die Anweisungen im Bereich *Konfigurieren und Bereitstellen von AEM[!DNL Forms]*.

   AEM [!DNL Forms] 6.3 finden Sie unter:

   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf) 
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   AEM [!DNL Forms] 6.2 finden Sie unter:

   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62_de) 
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62_de)
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62_de)

   AEM Forms 6.1:

   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61) 
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [ [!DNL Forms] Installieren und Bereitstellen von AEM für WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Starten Sie AEM [!DNL Forms] JEE-Server neu.
