---
title: Installieren von Cumulative Fix Packs in AEM Forms JEE
description: Zusammenfassung der Schritte zur Installation und Konfiguration des Cumulative Fix Packs (CFP) für AEM Forms JEE
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 894a2a98b9d1a135a2f488f2167ec3302c122339
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 100%

---

# Installieren von Cumulative Fix Packs für AEM [!DNL  Forms] JEE {#installing-cumulative-fix-packs-on-aem-forms-jee}

## Installieren von CFP in AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Führen Sie die folgenden Schritte in der angegebenen Reihenfolge durch, um das Cumulative Fix Pack für AEM 6.3 [!DNL Forms JEE] zu installieren.

1. Wenden Sie sich an den [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html), um das Installationsprogramm von AEM 6.3 [!DNL Forms JEE] für das CFP zu erhalten.
1. Führen Sie das CFP-Installationsprogramm aus und konfigurieren Sie AEM [!DNL Forms JEE] wie in [Installieren und Konfigurieren von AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee) beschrieben.
1. Installieren Sie das neueste AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md).
1. Installieren Sie das [!DNL Forms]-Add-on-Paket für AEM CFP [6.3.3.x](aem-forms-releases.md).

### Installieren des AEM [!DNL Forms JEE]-Bundle-Pakets {#install-aem-forms-jee-bundles-package}

Das [AEM [!DNL  Forms JEE]-Paket](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1; Version 1.0.2) bietet den [!DNL Forms]-Benutzern in AEM [!DNL Forms JEE] die gleichen Berechtigungen und Möglichkeiten wie in AEM [!DNL Forms OSGi]. Überprüfen Sie Ihre installierten Pakete im Package Manager und installieren Sie das Paket, falls es noch nicht installiert ist.

### Zusätzliche Anweisungen für CQ-4208044 {#additional-instructions-for-cq}

Wenn Sie AEM 6.3 [!DNL Forms JEE]-Server mit einer Oracle-Datenbank verwenden, konfigurieren Sie die folgenden Einstellungen nach der Bereitstellung von CFP1, d. h. nach der Ausführung von Configuration Manager. Diese Einstellung ist erforderlich, um Benutzer, Gruppen und Gruppenmitglieder zu synchronisieren, wenn die Synchronisierung der Unternehmens-Domain ausgeführt wird. Siehe Problem CQ-4208044 in den [Versionshinweisen zu AEM 6.3](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205).

1. Melden Sie sich bei der **Administrator-Benutzeroberfläche** an.
1. Navigieren Sie zu **[!UICONTROL Einstellungen]** > **[!UICONTROL Benutzerverwaltung]** > **[!UICONTROL Konfiguration]** > **[!UICONTROL Konfigurationsdateien importieren und exportieren]**
1. Exportieren Sie die Datei „config.xml“.
1. Ändern Sie den Eintrag für „`groupMemberDBQueryBatchSize`“ in Ihren Domain-Konfigurationen in *config.xml*. Beispieleintrag:

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importieren Sie die geänderte Datei erneut und führen Sie dann die Synchronisierung erneut aus.

## Installieren von CFP in AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Führen Sie die folgenden Schritte in der angegebenen Reihenfolge durch, um das Cumulative Fix Pack für AEM 6.2 [!DNL Forms JEE] zu installieren.

>[!NOTE]
>
>Wenn Sie AEM 6.2 [!DNL Forms OSGi] verwenden, befolgen Sie die Installationsanweisungen in den [Versionshinweisen zu AEM 6.2 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).

1. Wenden Sie sich an den [Adobe Support](https://www.adobe.com/account/sign-in.supportportal.html), um das Installationsprogramm von AEM 6.2 [!DNL Forms JEE] für das CFP zu erhalten.
1. Führen Sie das CFP-Installationsprogramm aus und konfigurieren Sie AEM [!DNL Forms JEE] wie in [Installieren und Konfigurieren von AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee) beschrieben.
1. Installieren Sie [AEM Hotfix 12785 Version 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785).
1. Installieren Sie [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).
1. Installieren Sie das neueste [AEM 6.2 Service Pack 1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md).
1. Installieren Sie das [!DNL Forms]-Add-on-Paket für [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md).

### Installieren des AEM [!DNL Forms JEE]-Bundle-Pakets {#install-aem-forms-jee-bundles-package-1}

Das [AEM Forms JEE-Paket](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) (aemfd-jee-bundles-package-6.2CFP5; Version 1.0.2) bietet [!DNL Forms]-Benutzern in AEM [!DNL Forms JEE] die gleichen Berechtigungen und Möglichkeiten wie in AEM [!DNL Forms OSGi]. Überprüfen Sie Ihre installierten Pakete im Package Manager und installieren Sie das Paket, falls es noch nicht installiert ist.

### Konfigurieren der Zeitüberschreitung für Vorgänge auf Komponentenebene (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Nach der Installation von AEM 6.2 CFP4 können Sie mit dieser Anleitung die Zeitüberschreitung für DSC-Vorgänge konfigurieren. Dies ist sinnvoll, falls es während des Aktualisierungsprozesses zu Problemen aufgrund einer Zeitüberschreitung kommen sollte. (Siehe NPR-16774 in den [Versionshinweisen zu AEM 6.2 CFP4](release-notes-aem-6-2-cumulative-fix-pack.md)).

Die Bereitstellung von DSC nimmt unterschiedlich viel Zeit in Anspruch, sodass sie fehlschlagen kann. Um den Wert für die Zeitüberschreitung von DSC-Vorgängen wie „Installieren“, „Laden“, „Starten“ und „Stopp“ zu ändern, müssen Sie den Wert `adobe.component.registry.timeout` mit dem JVM-Argument und der Option -D festlegen.

Geben Sie den Wert für den Schlüssel in Sekunden an. Beispiel: `-Dadobe.component.registry.timeout=300`

Sie können die Zeitüberschreitungen auch auf Komponentenebene mithilfe der folgenden drei Eigenschaften ändern:

1. `adobe.all-component.timeout`: überschreibt die Zeitüberschreitungen aller Services des Produkts.
1. `adobe.<serviceName>.timeout`: überschreibt die Zeitüberschreitung nur für den im Schlüssel erwähnten Service (&lt;Service-Name>). Wenn der Wert auf Service-Ebene festgelegt ist, überschreibt dieser Befehl nur den Zeitüberschreitungswert für den angegebenen Service, wenn er auf Programmebene festgelegt ist.
1. `adobe.<serviceName>.<operationName>.timeout`: Überschreibt nur den Zeitüberschreitungswert für den Vorgang des jeweiligen Service (&lt;Service-Name>.&lt;Vorgangsname>), der im Schlüssel erwähnt wird. Wenn der Wert auf Vorgangsebene festgelegt ist, überschreibt dieser Befehl nur den Zeitüberschreitungswert für den angegebenen Service, wenn er auf Programm- oder Service-Ebene festgelegt ist.

**Beispiele:**

Mit den folgenden Befehlen legen Sie den Wert für die Zeitüberschreitung auf Komponentenebene fest:

1. So legen Sie die Zeitüberschreitung für alle Service-Vorgänge auf 600 Sekunden fest:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. Setzen Sie den folgenden Befehl zum Einstellen des Zeitüberschreitungwerts für den Vorgang `DesigntimeService` auf 500 Sekunden:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. Setzen Sie den folgenden Befehl zum Einstellen des Zeitüberschreitungwerts für den Vorgang `DesigntimeService's previewLCA` auf 700 Sekunden:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. Setzen Sie den folgenden Befehl zum Einstellen des Zeitüberschreitungwerts für den Vorgang `DSC operations` (z. B. Laden oder Installieren) auf 600 Sekunden:

   set &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## Installieren und Konfigurieren von AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Erstellen Sie eine Sicherungskopie des Ordners /deploy. Das ist erforderlich, wenn Sie die Schnellkorrektur deinstallieren.
1. Stoppen Sie den Programm-Server.
1. Extrahieren Sie die Archivdatei des Patch-Installationsprogramms auf Ihrer Festplatte.
1. Im Ordner mit dem Namen entsprechend des von Ihnen verwendeten Betriebssystems:

   **Windows**

   Wechseln Sie zum entsprechenden Verzeichnis auf dem Installationsdatenträger oder zu dem Ordner auf der Festplatte, in den Sie das Installationsprogramm kopiert haben:

   * (Windows 32-Bit): Disk1\InstData\Windows\VM
   * (Windows 64-Bit): Disk1\InstData\Windows_64bit\VM

   Doppelklicken Sie dann auf die folgende Datei:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux, Solaris, AIX**

   Navigieren Sie zum entsprechenden Verzeichnis:

   * (Linux): Disk1/InstData/Linux/ NoVM
   * (Solaris): Disk1/InstData/Solaris/ NoVM
   * (AIX): Disk1/InstData/AIX/VM

   Geben Sie in einer Eingabeaufforderung Folgendes ein:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   Hierdurch wird das Installieren des Assistenten gestartet, der Sie durch die Installation führt.

1. Klicken Sie im Begrüßungsbildschirm auf **[!UICONTROL Weiter]**.
1. Stellen Sie auf dem Bildschirm „Installationsordner auswählen“ sicher, dass der angezeigte Standardspeicherort für Ihre bestehende Installation korrekt ist, oder klicken Sie auf **[!UICONTROL Durchsuchen]**, um den alternativen Ordner auszuwählen, in dem AEM [!DNL Forms] aktuell installiert ist, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Lesen Sie die Schnellkorrekturzusammenfassung und klicken Sie auf **[!UICONTROL Weiter]**.
1. Lesen Sie die Informationen zur „Zusammenfassung vor der Installation“ und klicken Sie auf **[!UICONTROL Installieren]**.
1. Wenn die Installation abgeschlossen ist, klicken Sie auf **[!UICONTROL Weiter]**, um die Schnellkorrektur-Updates auf Ihre installierten Dateien anzuwenden.
1. Das Kontrollkästchen „Configuration Manager starten“ ist standardmäßig aktiviert. Klicken Sie auf **[!UICONTROL Fertig]**, um Configuration Manager auszuführen.

   Um Configuration Manager später auszuführen, deaktivieren Sie die Option **[!UICONTROL Configuration Manager starten]**, bevor Sie auf **[!UICONTROL Fertig]** klicken. Sie können Configuration Manager mithilfe des entsprechenden Skripts im Verzeichnis *`[AEM_forms_root]`/configurationManager/bin* starten

1. Wählen Sie je nach Programm-Server eines der folgenden Dokumente aus und befolgen Sie die Anweisungen im Abschnitt *Konfigurieren und Bereitstellen von AEM [!DNL Forms]*.

   Für AEM [!DNL Forms] 6.3:

   * [Installieren und Bereitstellen von AEM [!DNL Forms] für JBoss](https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebSphere](https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebLogic](https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   Für AEM [!DNL Forms] 6.2:

   * [Installieren und Bereitstellen von AEM [!DNL Forms] für JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62_de)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62_de)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62_de)

   Für AEM Forms 6.1:

   * [Installieren und Bereitstellen von AEM [!DNL Forms] für JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [Installieren und Bereitstellen von AEM [!DNL Forms] für WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. Starten Sie den AEM [!DNL Forms] JEE-Server neu.
