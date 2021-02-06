---
title: AEM 6.2 Cumulative Fix Pack
description: Experience Manager 6.2 Versionshinweise zu den insgesamt Fix-Paketen. Informieren Sie sich über die Probleme, die in verschiedenen kumulativen Fix Packs in Experience Manager-Komponenten behoben wurden.
translation-type: tm+mt
source-git-commit: 98d91e0367912d8962bb2f45ae972f50ccb71b5f
workflow-type: tm+mt
source-wordcount: '19975'
ht-degree: 21%

---


# AEM 6.2 Versionshinweise zur kumulativen Fehlerbehebung{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Versionsinformationen {#release-information}

| **Produkt** | Adobe Experience Manager |
|---|---|
| **Version** | 6.2 |
| **Version** | [Cumulative Fix Pack 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **Voraussetzung** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **Allgemeine Verfügbarkeit** | Juni 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe hat ein Modell für die einmalige Bereitstellung für die Veröffentlichung von Fehlerbehebungen eingeführt. Anstatt Hotfixes für einzelne Probleme freizugeben, veröffentlicht Adobe jetzt jeden Monat ein Cumulative Fix Pack (CFP) (vorbehaltlich der Qualitätssicherung). Ein CFP ist ein aggregiertes Inhaltspaket für mehrere Fehlerbehebungen. CFPs enthalten in erster Linie Fehlerbehebungen, können aber auch Feature Packs enthalten. Sie haben folgende Vorteile gegenüber einzelnen Hotfix-Versionen:

* Kumulierter Charakter (ein CFP enthält beispielsweise Korrekturen, die über frühere CFPs geliefert wurden)
* Erhöhte Qualitätssicherung
* Vereinfachte Installation (Benutzer installieren CFPs als einzelnes Paket ohne Abhängigkeiten, abgesehen vom neuesten Service-Pack)

Weitere Informationen zu CFP und anderen Versionstypen finden Sie unter [Maintenance Release Vehicle](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## Informationen zur Version {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 ist das letzte Cumulative Fix Pack für AEM 6.2 und ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

>[!CAUTION]
>
>Die Anwendung von CFPs ohne Überprüfung der Kompatibilität zwischen installierten Feature Packs kann zu einem Systemausfall oder zum Verlust benutzerdefinierter Konfigurationen führen, bei denen die Wiederherstellung von der Sicherung bis zur Behebung erforderlich sein könnte.

>[!NOTE]
>
>* Ein neues Sling `discovery-  api` Bundle Johnzon 1.0.0 ist in AEM Cumulative Fix Pack 6.2 SP1-CFP10 enthalten. Darüber hinaus wird ein Dienstbenutzer-Sling-Discovery mit Lese- und Schreibberechtigungen für den Knoten */var/discover* im CRX-Repository hinzugefügt.
   >
   >
* Das E-Mail-Bundle der Apache-Kommas **org.apache.commons/commons-email/1.5** wurde hinzugefügt und ersetzt **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
   >
   >
* Adobe empfiehlt die Bereitstellung von CFP über den Installationsordner für Kunden, die eine große Anzahl von Benutzern auf AEM Instanz haben.

>



## Behandelte Probleme: {#issues-included}

In diesem Abschnitt werden alle im aktuellen CFP enthaltenen Probleme und Hotfixes aufgeführt.

Darüber hinaus enthält diese CFP Hotfixes, die in [vorherigen kumulativen Fixpacks](#previous) geliefert werden.

### Integrationen {#integration}

* Unterstützung mehrerer Verbesserungen der Kampagne-Targeting-Personalisierung. NPR-29163: Hotfix für CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler wird in eine unendliche Schleife verschoben und führt bei Veröffentlichungsinstanzen zu Aktualisierungen der Knoten. NPR-28561: Hotfix für CQ-4263096

### DAM - Allgemeines {#dam-general}

* Die Replikationsschaltfläche für Benutzer ohne Admin-Berechtigungen kann nicht in bestimmten DAM-Ordnern angezeigt/ausgeblendet werden. NPR-29026: Hotfix für CQ-4265361

### Schwachstelle {#vulnerability}

* CSRF-Schutz-Framework funktioniert nicht mit AEM Foundation-Formularen. NPR-28612: Hotfix für GRANITE-22231

### Formulare {#forms}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms-Kunden müssen unbedingt beachten, dass das AEM Forms-Add-on-Paket erst nach der Installation jeglicher Service Packs, Cumulative Fix Packs oder Feature Packs von AEM installiert werden darf.

>[!NOTE]
>
>AEM Forms-Add-on-Pakete helfen, die Formularfunktionalität mit AEM Service Packs und Cumulative Fix Packs abzustimmen. Daher müssen Sie AEM Forms Add-On-Paket nach der Installation von AEM Service Pack, Cumulative Fix Pack oder Feature Pack installieren.

#### Adaptive Formulare {#adaptive-forms}

* Probleme mit der Benutzerfreundlichkeit bei der Scribble-Komponente für iOS 12.1-Geräte. NPR-29082: Hotfix für CQ-4261765

#### Forms - Document Security {#forms-document-security}

* Beim Überprüfen aller Signaturen in einer PDF-Datei mit PDF Advanced Electronic Signatures (PAdES) wird InvalidOperationException ausgelöst. NPR-27848: Hotfix für CQ-4244837

#### Forms - Korrespondenz {#forms-correspondence}

* Bei der Vorschau des Briefs als PDF wird der auf der Seite &quot;Übergeordnet&quot;platzierte Textwert nicht berücksichtigt, der auf der Registerkarte &quot;Daten&quot;oder gemäß der angegebenen Datenverknüpfung eingegeben wurde. NPR-29239: Hotfix für CQ-4266856.

#### Forms – Interaktive Kommunikation {#forms-interactive-communication}

* Wenn ein Apostroph-Zeichen hinzugefügt wird, erscheinen die vorausgefüllten Felder im Brief als ASCII-Zeichen anstelle von regulären Alphabeten. NPR-28863: Hotfix für CQ-4262900

### Forms JEE-Installationsprogramm {#forms-jee-installer}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

## Hotfixes und Feature Packs, die in früheren Cumulative Fix Packs enthalten waren {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Unterstützung für MS Translator API, Version 3.0, für AEM 6.2 aktiviert
* Protokollmeldung nach erfolgreicher Installation des Pakets für alle SPs, CFPs und HFs hinzugefügt.

### Assets {#assets}

* DAM-Ordner kann nicht umbenannt werden, wenn die Berechtigung ACL bearbeiten fehlt. NPR-27555: Hotfix für CQ-104652
* Bildvorgabe-Editor-Tool in 6.2.1 CFP 17 und höher nicht reagiert. NPR-28147: Hotfix für CQ-4261041

### Sites {#sites}

* Der Link-Checker schließt den Auftrag nicht ab, er wird mit Links ohne Antwort blockiert. NPR-27373: Hotfix für CQ-4256030
* Die Segmentdatei wird aufgrund eines zusätzlichen Stammpfads, der den Pfad des Segments umbricht, nicht ordnungsgemäß geladen. NPR-28014: Hotfix für CQ-4260332

### Integrationen {#integration-1}

* Die Absage der LiveCopy-Vererbung funktioniert auf zielgerichteten Containern nicht ordnungsgemäß. NPR-28129: Hotfix für CQ-4259813
* Die cq:actions werden für eine zielgerichtete Komponente nicht berücksichtigt. NPR-27616: Hotfix für CQ-4257497

* Die Anzeige des Symbols zum Umbrechen der Vererbung ist nicht kohärent. NPR-27671: Hotfix für CQ-4257779

### Felix {#felix}

* Die Details zur Webkonsole-Komponente schlagen mit 500 nach der CFP 18-Installation auf AEM 6.2 SP1-Instanz fehl. NPR-28350: Hotfix für CQ-4261095

### Übersetzung {#translation}

* Aktivieren Sie die Unterstützung für den MS Translator-Dienst in AEM 6.3 nach der Aktualisierung von MS Translator auf API Version 3.0. NPR-28123: Hotfix für CQ-4259096

### Benutzeroberfläche - Foundation {#ui-foundation}

* OOTB Sites Kalender zeigt falsche Daten an. NPR-28392

### Granite {#granite}

* Das Wörterbuch ist für Ressourcenpakete mit sling :basename nicht ungültig. NPR-27624

### Unterstützung {#sustenance}

* Die Aktivitätsprotokolle von Package Manager sollten in einer separaten Protokolldatei extrahiert werden. NPR-27323: Hotfix für Granite-14866
* Eine standardisierte Wortgruppe/Wortgruppe/Logline(n) in error.log wird angezeigt, wenn die Installation abgeschlossen ist. NPR-27835
* Das Granite-Paket-Plugin wählt die Abhängigkeit einer niedrigeren Version von org.apache.sling.i18n. Hotfix für CQ-4263245
* com.adobe.cq.com.adobe.cq.ui.commons bundle wird bei der Installation der neuesten CFP nach 6.2SP1-CFP15 gelöscht. Hotfix für CQ-4258808

### Formulare {#forms-1}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-1}

#### Adaptive Formulare {#adaptive-forms-1}

* XML-Injection-Schwachstelle mit AEM Forms. NPR-27843: Hotfix für CQ-4257315

### Forms JEE-Installationsprogramm {#forms-jee-installer-1}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

### OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included}

Der folgende Text Dokumente die Liste von OSGI-Bundles und Inhaltspaketen, die in der CFP enthalten sind.

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP19 enthalten sind

[Datei laden](assets/do-not-localize/cfp19_osgi_bundles.txt)

Liste der in AEM 6.2SP1-CFP19 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Unterstützung in DAM CommandLineProcess hinzugefügt, um den lang andauernden Prozess zu beenden.
* Sitzungsfehler in ReplicationEventListener behoben.
* Unterstützung für Umleitungen zur Kernseitenkomponente hinzugefügt.

### Assets {#assets-1}

* Camera Raw werden Prozesse in Phasen der massiven Erfassung blockiert, was schließlich die gesamte Workflow-Verarbeitung blockiert. NPR-26990: Hotfix für NPR-23860
* Die Download-Funktion nutzt AEM Assets über assetdownload-Servlet, sodass anonyme Benutzer alle Assets herunterladen können. NPR-27054, Hotfix für CQ-4254732
* Sonderzeichen werden in der Betreffzeile der E-Mail-Vorlagen in AEM angezeigt. NPR-26470: Hotfix für CQ-4252368

### Sites {#sites-1}

* Aufgrund des fehlerhaften Verhaltens der ConfigPostProcessor-Klasse wird beim Aussetzen des übergeordneten Bildes cq entfernt: LiveRelationship-Mischungstyp von der untergeordneten Seite. NPR-26745: Hotfix für CQ-4254163
* hinzufügen Unterstützung der Umleitung zur Kernseitenkomponente. NPR-26576: Hotfix für CQ-110529
* Kontextknoten zu jquery 3 migrieren. NPR-26956: Hotfix für CQ-4255472
* Ankereingabefelder werden aus dem sichtbaren Browser-Abschnitt im Dialogfeld angezeigt, bis sie maximiert sind. NPR-26852: Hotfix für CQ-4255019
* Kopieren Sie den Einfügetext, der unerwünschte &lt;br> in das Inhaltsfragment eingefügt hat. NPR-26660: Hotfix für CRTE-151
* Classic siteadmin gibt die Liste für einige Seiten nicht im rechten Bereich wieder. NPR-27247: Hotfix für CQ-4251621
* (Klassische Benutzeroberfläche) Der Versuch, Seiten zu verschieben/umzubenennen, führt zu einem Fehler: &quot;Beim Verschieben der Seite ist ein Fehler aufgetreten.&quot; NPR-27179: Hotfix für CQ-4235907

### Integrationen {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever durchsucht den gesamten Baum, um die verfügbaren Marken zu sammeln. NPR-27060: Hotfix für CQ-4255790

### WCM - Foundation-Komponenten {#wcm-foundation-components}

* Problem mit der Suchfunktion bei der Foundation-Liste. NPR-26817: Hotfix für CQ-4250324

### Plattform {#platform}

* Aufgrund des Geviertstrichs mit Sonderzeichen hat der Herausgeber ein Problem beim Löschen des Cache. NPR-27199: Hotfix für CQ-4242790

### Granite {#granite-1}

* Package Validator überprüft keine Pakete, die in CFP/SP enthalten sind. NPR-26775: Hotfix für Granite-22825

### Replikation {#replication}

* JCR-Sitzung undicht in ReplicationListener. NPR-27063: Hotfix für CQ-4232088

### Formulare {#forms-2}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-2}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms-Add-on-Paket.

### Forms JEE-Installationsprogramm {#forms-jee-installer-2}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

#### OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included-1}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP18 enthalten sind

[Datei laden](assets/do-not-localize/62cfp18updated_bundles.txt)

Liste der in AEM 6.2 SP1-CFP18 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Unterstützung für URLs ohne Site-Erweiterung in at-integration.js hinzugefügt
* Der S7-Abrufimporteur wurde aus der Konfiguration des S7-Cloud-Dienstes entfernt.
* Änderungen an der Ansicht &quot;Audiencen&quot;zur Unterstützung der Ordnerstruktur für die Implementierung mit mehreren Mandanten.
* Aktualisieren auf jqueryui   clientlib v1.12.1.

### Assets {#assets-2}

* Zum Starten von Workflows über die Asset-Benutzeroberfläche muss der Benutzer über die Berechtigung zum Schreiben/Löschen/Ändern verfügen. NPR-25688: Hotfix für CQ-4250140
* Schaltflächen zum Veröffentlichen und Rückgängigmachen der Veröffentlichung bleiben auch für Benutzer ohne Berechtigung zum &quot;Replizieren&quot;sichtbar. NPR-25094
* (Workflow) Der Arbeitsablauf für intelligente Tags für Assets wird nicht über die AEM Proxykonfiguration verarbeitet. NPR-25915: Hotfix für CQ-4248202
* Entfernen Sie den S7-Abrufimporteur aus der Konfiguration des S7-Cloud-Dienstes. NPR-25239: Hotfix für CQ-95236

### Sites {#sites-2}

* Workflows, die vom Editor gestartet werden -> Seiteninformationen enthalten den Kontextpfad in der Nutzlast. NPR-26389: Hotfix für CQ-76804
* (Externer Link-Prüfer) Ungültige HTTPS-Links werden als gültige Links angezeigt. NPR-25541: Hotfix für CQ-4201333
* (Klassische Benutzeroberfläche) Beim Erstellen einer eigenständigen Seite unter einer Live-Kopie wird die Seite als Live-Kopie erstellt. NPR-25610: Hotfix für CQ-4249801
* Probleme mit Veröffentlichungsressourcen, die mit der Design Importer-Komponente verknüpft sind, wenn eine Seite aktiviert wird. NPR-25638: Hotfix für CQ-102532
* Die RTE-Rich-Text-Symbolleiste deckt ausgewählte Listen ab. NPR-25165: Hotfix für CQ-4248948
* Migrieren Sie contexthub zu jquery 3. NPR-25059: Hotfix für Granite-19902
* Bei verschachtelten parsys-Komponenten wird immer der erste (mit dem am wenigsten verschachtelten Pfad) passende Entwurf aus mehreren verfügbaren Komponenten angewendet. Weitere Informationen finden Sie unter [Designpfad-Auflösung](https://helpx.adobe.com/de/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: Hotfix für CQ-4246276

### Integrationen {#integration-3}

* Bei Verwendung der OOTB-Zielgruppe-Integration rendert das Targeting einer Komponente die ganze Seite anstelle einer leeren, zielgerichteten Komponente. NPR-25273: Hotfix für CQ-4248003
* Wenn die Vererbung im Targeting-Modus abgebrochen wird, wird die Komponente weiterhin als Ziel angezeigt, wobei die Vererbung im Bearbeitungsmodus nicht unterbrochen wird. NPR-25324: Hotfix für CQ-4248162
* Wenn eine Personalisierung auf einer Seite definiert und eine Audience aufgelöst wird, wird das entsprechende Erlebnis im Bearbeitungsmodus angezeigt. NPR-25731: Hotfix für CQ-4249465
* Falsche Teaser-URL bei Verwendung von AEM mit einem nicht standardmäßigen Kontextpfad. NPR-25971: Hotfix für CQ-4250953
* Leeres Rendering bei Verwendung von Optout. NPR-25295: Hotfix für CQ-4246792
* Erlebnisse, die aus der Autorenversion gelöscht wurden, werden bei der Aktivierung der Seite nie von der Veröffentlichungs-Site entfernt. NPR-24869: Hotfix für CQ-4247832

### DAM - DM Client {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignoriert Mausklicks auf berührungsempfindlichen Geräten. Hotfix für CQ-4247370

### Plattform {#platform-1}

* Erlauben Sie, die maximale Anzahl von weiteren Zustellversuchen beim Erwerben/Loslassen eines Pakets zu konfigurieren. NPR-25328: Hotfix für Granite-22376
* Falsche Protokollierung bei Replizierungsfehlern. NPR-25308: Hotfix für CQ-4249402
* Die Installation von Forms AEM 6.2 Forms CFP8 auf CFP14 führt dazu, dass Apache POI fehlschlägt. NPR-25053: Hotfix für Granite-21771

### Granite {#granite-2}

* Die Benutzersynchronisierung schlägt mit der Ausnahme OakConstraint0022 fehl. NPR-25729: Hotfix für Oak-7428

### Communities {#communities}

* cq -social-as-provider bundle Beginn nicht mit den Mongo Driver 3.x Versionen. NPR-26271: Hotfix für CQ-4252710

### Benutzeroberfläche - Foundation {#ui-foundation-1}

* Aktualisieren auf jqueryui   clientlib v1.12.1. NPR-25090: Hotfix für Granite-21981, CQ-4248897

* (Omnese): Die Eigenschaft &#39;title&#39; ist anfällig für Cross-Site-(XSS-)Skripterstellung in Sites. NPR-24994: Hotfix für Granite-19933

### Formulare {#forms-3}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-3}

#### Adaptive Formulare {#adaptive-forms-2}

* Falsche Kodierung beim Senden von Daten aus dem adaptiven Formular. NPR-25539

#### Forms – Verwaltung {#forms-management}

* Nicht verwandte Formular-Assets werden beim Veröffentlichen der Seite als Verweise gemeldet. NPR-26167: Hotfix für CQ-4251004

### Forms - JEE-Installationsprogramm {#forms-jee-installer-3}

#### Document Security {#document-security}

* Variable wird als Liste des Datentyps ausgefüllt, Untertyp ist Zeichenfolge, es wird jedoch die Fehlermeldung &quot;Objekt kann nicht zwingend werden&quot;angezeigt. NPR-26194: Hotfix für CQ-4252287
* Nach der Installation von 6.2-SP1-CFP15 kann nicht auf Wasserzeichenkonfigurationen zugegriffen werden. NPR-26130: Hotfix für CQ-4250984

### OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included-2}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP17 enthalten sind

[Datei laden](assets/do-not-localize/62cfp17updated_bundles.txt)

Liste der in AEM 6.2SP1-CFP17 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* STARTTLS-Unterstützung im Day CQ Mail Service hinzugefügt.
* Die Ausrichtung der ContextHub-Symbole im Profil-Popup wurde korrigiert.
* Korrekturen in der Ein-/Ausblenden-Funktion der Dropdown-Komponente.
* Upgrade auf die neueste Jackson-Version 2.8.11

### Assets {#assets-3}

* Workflow kann nicht von einer Liste-Ansicht aus initiiert werden. NPR-24393: Hotfix für CQ-4245788
* (Firefox/Chrome) Assets können nicht auf der Seite &quot;Asset-Freigabe&quot;heruntergeladen werden. NPR-24523: Hotfix für CQ-4224408
* Die Standardqualität für die Video-Vorschau in AEM wurde verbessert. NPR-24148: Hotfix für CQ-4244310

### Integrationen {#integration-4}

* Wenn eine Komponente auf eine Veröffentlichungsinstanz ausgerichtet ist, wird das Flackern angezeigt, das das Standarderlebnis vor der Zielinstanz anzeigt. NPR-23992: Hotfix für CQ-4242038
* Erlebnisse, die aus der Autorenversion gelöscht wurden, werden bei der Aktivierung der Seite nie von der Veröffentlichungs-Site entfernt. NPR-24869: Hotfix für CQ-4247832

### Plattform {#platform-2}

* Patch jQuery 1.12.4 von clientlib enthält Sicherheitskorrektur. NPR-24129: Hotfix für Granite-20058
* STARTTLS-Unterstützung im Day CQ Mail Service hinzugefügt. NPR-23941: Hotfix für CQ-4240397
* Entfernen Sie die standardmäßige MERGE_PRESERVE aclHandling. NPR-24593: Hotfix für Granite-21889
* LineChecker kann Links nicht extern verarbeiten, wenn eine Anforderung ungültige Abfragen-Parameter enthält. NPR-24127: Hotfix für CQ-4241893

### MSM {#msm}

* Proaktive Hotfixes für Cross-Site Scripting-Angriffe (XSS). NPR-21893: Hotfix für CQ-4223385
* MSM LiveRelationship: effektive RolloutConfig falsch, wenn BlueprintConfig sich im Stammordner befindet. NPR-23999: Hotfix für CQ-4243000

### Sites {#sites-3}

* Zum Erstellen eines neuen Erlebnisses in einem Live-Kopierbereich muss die Vererbung abgebrochen werden, damit sie konfiguriert werden kann. NPR-24995, Hotfix für CQ-4248209
* (Touch-Benutzeroberfläche) Mehrere Symbole in der oberen Symbolleiste verschwinden beim Sperren oder Entsperren einer Seite. NPR-23954: Hotfix für CQ-4243345
* Die Felder sind im Kontext nicht richtig ausgerichtet. NPR-23958
* Die Veröffentlichungsaktion auf gesperrten Seiten macht das Authoring unterbrochen. NPR-23970: Hotfix für CQ-4243203
* OOTB-Berichte in /etc/reports/ funktionieren nicht ordnungsgemäß und zeigen kein Diagramm mit Verlaufsdaten an. NPR-20035: Hotfix für CQ-4220180
* Die Erstellung des Startvorgangs schlägt beim Initiieren des Arbeitsablaufs zum Anfordern eines Projekts fehl. NPR-24255: Hotfix für CQ-4245030
* HTML-Tags und -Attribute, die von E-Mails nach der Installation von CFP10 ignoriert werden. NPR-24287: Hotfix für CQ-4240028
* TagPicker: Tag-Vorschlag in den Tag-Metadaten-Schema-Tag-Abfragen taggable Knoten, daher dauert das Laden lange. NPR-24347: Hotfix für CQ-4244291
* Die Salesforce-Integration schlägt mit Proxy-Konfigurationen fehl. NPR-24418: Hotfix für CQ-4245300
* (WCM) PageManager lässt Seite bei der Erstellung der Revision bei Ausnahme einchecken. NPR-24565: Hotfix für CQ-4246203
* Die Schaltfläche Geräteemulator wird nach der Anwendung von CFP14 aus dem Bearbeitungs- und Vorschau-Modus ausgeblendet. NPR-24566: Hotfix für CQ-4247060
* (Klassische Benutzeroberfläche) Die gesamten Tags werden als leer angezeigt, sobald sie im Dialogfeld erstellt wurden. NPR-24688, Hotfix für CQ-4246407
* Version kann beim ersten Versuch nicht erstellt werden. NPR-24774: Hotfix für CQ-4232176
* OOTB-Berichte in /etc/reports/ funktionieren nicht ordnungsgemäß und zeigen kein Diagramm mit Verlaufsdaten an. NPR-24138: Hotfix für CQ-4220180

### Schwachstelle {#vulnerability-1}

* Die Salesforce-Integration ist anfällig für Server-seitige Anforderungsfälschung (SSRF, Server Side Request Forgery). NPR-24289: Hotfix für CQ-4245277
* Serverseitige Anforderungsfälschung (SSRF) in ReportingServicesProxyServlet. NPR-24657: Hotfix für CQ-4246880

### Granite {#granite-3}

* Vorgänge zum Lesen von Metadaten werden nicht beendet. NPR-24240: Hotfix für Granite-19866
* Aktualisieren Sie Jetty auf 9.4.11.v20180605, um Sicherheitslücken zu schließen. NPR-25033: Hotfix für Granite-22120

### WCM - Foundation-Komponenten {#wcm-foundation-components-1}

* PageComparator gibt ClassCastException beim Sortieren von Seiten aus. NPR-24123: Hotfix für CQ-4244048
* Die Funktion zum Anzeigen/Ausblenden der Formular-Dropdown-Komponente funktioniert nicht wie erwartet. NPR-24562: Hotfix für CQ-4222853

### Benutzeroberfläche {#user-interface}

* Eine hohe CPU-Auslastung wird durch viele Anforderungen in der Funktionalität der Admin-Suche festgestellt. NPR-23588: Hotfix für Granite-21286
* (Klassische Benutzeroberfläche) Die Komponente zeigt die Standardwerte an, selbst wenn der zugehörige Formulardatenmodelldienst auf ein leeres Feld eingestellt ist. NPR-21903: Hotfix für GRANITE-19744
* Multifield throwing NPE, wenn keine FormData zur Anforderung vorhanden ist. NPR-24513: Hotfix für Granite-21055

## Formulare {#forms-4}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-4}

#### Core {#core}

* (OSGI) AEM Forms OSGI von Jackson Data Binding Security Alert beeinflusst. NPR-24274: Hotfix für CQ-4230245

#### Rights Management {#rights-management}

* Apache POI schlägt nach der Installation AEM 6.2 SP1-CFP14 fehl. NPR-25054, NPR-25052: Hotfix für CQ-4245898, CQ-4244778

#### HTML5-Formulare {#html-forms}

* Die Daten werden nicht mit dem Vorausfüllen von mehrzeiligen Feldern in der HTML-Vorschau gefüllt. NPR-23357: Hotfix für CQ-4244212
* Wenn eine Vorschau eines Briefs über eine Standardschaltfläche angezeigt wird, wird die Zuordnung von Layout-Fragmenten nicht angezeigt, während das entsprechende Symbol beim Klicken auf die Schaltfläche &quot;Vorschau&quot;korrekt angezeigt wird. NPR-22993: Hotfix für CQ-4237745
* Problem mit der HTML-Vorschau eines Textfelds, wenn ein Muster für die Sozialversicherungsnummer auf eine Vorlage angewendet wird. NPR-23205

#### Adaptive Formulare {#adaptive-forms-3}

* Fehler &quot;Guidelib ist nicht definiert&quot;beim Hinzufügen AEM Formulars zur parsys-Komponente. NPR-24269: Hotfix für CQ-4244546

### Forms JEE-Installationsprogramm {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Fensterzeilenendungen in Shell-Skriptdateien führen dazu, dass LCM nicht in UNIX ausgeführt wird. NPR-22958

### OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included-3}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP16 enthalten sind

[Datei laden](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Liste der in AEM 6.2SP1-CFP16 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Proaktive Sicherheitskorrektur in der Foundation-Tabelle, um die Konsistenz des Designs zu gewährleisten.
* Unterstützung für typeHint zum Speichern von Werten als Zeichenfolge hinzugefügt.
* Bietet erweiterte Sicherheit für den Forms Prefill-Dienst
* Aktualisieren Sie auf die neueste Datei &quot;adobe-reader-extensions-dsc.jar&quot;für Fehlerbehebungen in der Reader-Erweiterung.
* Überprüfungshaken wurde so angepasst, dass &quot;:ungültige&quot;Elemente für die Eingabe der Steigerungszahl berücksichtigt werden.

### Assets {#assets-4}

* EmbedXMP-Daten werden für den Ptiff-Generierungsprozess immer auf „aktiv“ gesetzt. NPR-22776: Hotfix für CQ-4234498
* Es können nicht mehrere Standardwerte in Feldern mit mehreren Werten festgelegt werden. NPR-22900: Hotfix für CQ-4239000
* (Dynamic Media) Wenn Sie das Kontrollkästchen &quot;Dynamische Darstellungen&quot;aktivieren, gibt die heruntergeladene ZIP-Datei das Original-TIFF-Bild mit einer Nullbyte-Datei zurück. NPR-22410: Hotfix für CQ-4198471
* (Touch-Benutzeroberfläche) Standardmäßiger Upload-Speicherort für Assets in der Ansicht der Spalten. NPR-23475: Hotfix für CQ-4237057

### Integrationen {#integration-5}

* Im Modus &quot;Zielgruppe&quot;können Autoren eine aus dem Blueprint geerbte Komponente ändern, ohne die Vererbung abzubrechen. NPR-22751: Hotfix für CQ-4237907
* Die Pfadvariable ist nicht korrekt kodiert und führt zu nicht beständiger Cross-Site-Skripterstellung (XSS). NPR-22851

### MSM {#msm-1}

* Wenn bei der Einführung einer LiveCopy mit mehreren Rollout-Konfigurationen unterhalb des Stammordners ein ResourceNameConflict auftritt, wird der Rollout-Fluss ohne Einbeziehung aller Verzweigungen beendet. NPR-22842: Hotfix für CQ-4236188

### Plattform {#platform-3}

* Implementieren Sie in einer Anfrage zur Rückwärtsanwendung eine Umfragebegrenzung. NPR-23351: Hotfix für Granite-21135****
* Die Änderung des Meldungsmusters wird bei benutzerdefinierten Protokollen nicht berücksichtigt. NPR-23486: Hotfix für CQ-4241974

### Sites {#sites-4}

* Das Erstellen einer Verknüpfung in einem Rich-Text-Editor mit einem Dokument mit Leerzeichen oder anderen Sonderzeichen funktioniert nicht. NPR-22289: Hotfix für CQ-4224321
* Wenn Sie das Segment mit einem riesigen Wert speichern (10000000000), wird der Impuls auf 0 gesetzt und es wird eine Fehlermeldung ausgegeben. NPR-22524: Hotfix für CQ-4237006
* In der Multifield-Komponente kann nicht auf Hinzufügen Element geklickt werden. NPR-22552: Hotfix für CQ-4237404
* Die horizontale Bildlaufleiste ist nicht sichtbar, wenn das Segment einen langen Titel hat. NPR-22615: Hotfix für CQ-4237001
* Beim Laden einer leeren Audience wird ein falscher JavaScript-Code generiert. NPR-22974: Hotfix für CQ-4238734
* Beim Planen einer Aktivierung oder Deaktivierung ist der Workflow-Titel obligatorisch. Daher wird der benutzerdefinierte Workflow-Titel nicht in die Zeitschiene übersetzt. NPR-23121: Hotfix für CQ-4237552
* Anforderung von Fehlerbehebungen bei Problemen im Zusammenhang mit Zielgruppen-Segmenten in Sites. NPR-23128
* (Firefox) Das Kontrollkästchen für ausgewählte Persona ist nicht korrekt. NPR-23345
* Bezeichnungen für die verschiedenen Modi werden zusammen mit Symbolen angezeigt. NPR-23275
* Fehler &quot;Ungültiger Rekursionsauswahlwert&quot;bei der Migration einer Komponente von AEM 6.0 auf AEM 6.2. NPR-23503: Hotfix für CQ-4241258

### Communities {#communities-1}

* Web- und E-Mail-Benachrichtigungen werden nicht ausgelöst, da die Gruppen nicht benachrichtigt werden. NPR-23447: Hotfix für CQ-4242880

### Übersetzung {#translation-1}

* Asset-Sprachkopien werden erstellt, wenn das Asset &quot;Nicht übersetzen&quot;in der Konvertierungskonfiguration eingestellt ist. NPR-22540: Hotfix für CQ-4237962

### Benutzeroberfläche {#user-interface-1}

* Wenn Sie Omniture Search mit einer Bindestrich-Abfrage verwenden, wird ein Serverfehler zurückgegeben. NPR-22999: Hotfix für Granite-19674
* DatePicker unterstützt nicht die manuelle Einstellung externer Typhinweise, die durch ein unsichtbares Feld festgelegt werden. Beim Ändern des Typhinweises wird ein Konvertierungsfehler ausgegeben. NPR-23333: Hotfix für Granite-21194

### WCM - Foundation-Komponenten {#wcm-foundation-components-2}

* Die CAPTCHA-Komponente wurde aus Sicherheitsgründen nicht mehr unterstützt. Wenn Sie die CAPTCHA-Komponente verwenden, wird die Meldung &quot;Captcha-Komponente ist veraltet und sollte nicht mehr verwendet werden&quot;angezeigt. wird nach der Installation von 6.2 SP2-CFP15 oder höher angezeigt. AEM Komponente kann angepasst werden, um reCAPTCHA für eine bessere Sicherheit NPR-22151 einzubeziehen: Hotfix für CQ-4220052
* Die WCM Foundation-Komponente &#39;Table&#39; ist anfällig für die Stored Cross Site Scripting. NPR-23206: Hotfix für CQ-4240760

### Schwachstelle {#vulnerability-2}

* Site-übergreifende Skripterstellung (XSS) in den Verknüpfungen zum Admin-UI-Projekt. NPR-23272: Hotfix für CQ-4241795

## Formulare {#forms-5}

### Forms-Add-on-Paket {#forms-add-on-package-5}

#### Korrespondenzverwaltung {#correspondence-management}

* Wenn eine Vorschau eines Briefs über eine Standardschaltfläche angezeigt wird, wird die Zuordnung von Layout-Fragmenten nicht angezeigt, während das entsprechende Symbol beim Klicken auf die Schaltfläche &quot;Vorschau&quot;korrekt angezeigt wird. NPR-23335: Hotfix für CQ-4237745
* Daten im Brief, die den in XDP definierten Bindungen entsprechen, werden bei der Verwendung der URL des Direktbriefs nicht ausgefüllt. NPR-24145: Hotfix für CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Correspondence Management) Fehlausrichtung der Daten beim Laden des Briefs mit Zielgruppe-XML. NPR-22993: Hotfix für CQ-4237663

#### Reader Extensions-Dienst {#reader-extensions-service}

* Reader Extension kann nicht auf Adobe PDF angewendet werden. NPR-23067

#### Forms Manager {#forms-manager}

* In Site eingebettete Forms werden beim erneuten Veröffentlichen der Site-Seite nicht veröffentlicht. NPR-23014: Hotfix für CQ-4236566

#### Schwachstelle {#vulnerability-3}

* Proaktive Hotfixes für Site-übergreifende Skripterstellung. NPR-20624: Hotfix für CQ-4206055
* Geschützte Cross-Site Scripting (XSS)-Schwachstelle auf der Registerkarte „Notizen“ des Forms Managers. NPR-27157: Hotfix für CQ-4255556

#### Encryption-Dienst {#encryption-service}

* (OSGI) [JEE] Falscher Signaturstatus für PDF mit Anlage bei der Überprüfung mit &quot;PDF-Prozess überprüfen&quot;. NPR-23269, NPR-23737

### Forms JEE-Installationsprogramm {#forms-jee-installer-5}

#### Core {#core-1}

* Die Probleme, die in der statischen Code-Analyse von Core-ext gemeldet werden, sollten behoben werden. NPR-13947

#### PDFG Service {#pdfg-service}

* &quot;HTML in PDF&quot;-Konvertierer funktioniert nicht. NPR-21545

### OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included-4}

Der folgende Text Dokumente die Liste von OSGI-Bundles und Inhaltspaketen, die in der CFP enthalten sind.

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP15 enthalten sind

[Datei laden](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Liste der in AEM 6.2SP1-CFP15 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Verbesserte Bearbeitbarkeit von Metadateneigenschaften von Assets.
* Der Auftrag zur Benachrichtigung zum Passwortablauf für Assets, die sich bereits im abgelaufenen Status befinden, wurde neu konfiguriert.
* Benutzerdefinierte Touch-UI-Konsole, um zusätzliche Gebietsschemata zu erweitern.
* Aktualisierung von cq-msm-core für eine effiziente Livecopyindex-Synchronisierung.
* Optimierte Replikationsfunktionen für verschiedene Rollouts.

### Assets {#assets-5}

* Benutzer können keine Assets mit Haftungsausschluss und langen Dateinamen herunterladen. NPR-22163: Hotfix für CQ-4235274
* Ein einfaches Anführungszeichen verhindert die Aktualisierung der Metadaten in der Ansicht &quot;bulkview&quot;und die Benutzeroberfläche ist vollständig beschädigt, wenn Sie die Eigenschaften eines Assets mit den Schnellaktionen in der Symbolleiste öffnen. NPR-22317, NPR-22353: Hotfix für CQ-4236990, CQ-4236469
* Asset-Ablaufbenachrichtigungsauftrag deaktiviert die abgelaufenen Assets nicht. NPR-22346: Hotfix für CQ-4237188
* Asset-Download schlägt fehl, wenn Digital Rights Management in Assets in Safari verwendet wird. NPR-22378: Hotfix für CQ-4236460
* Die Webdarstellung für kleine Bilder hat eine falsche Pixelgröße. NPR-22435: Hotfix für CQ-4236742

### Sites {#sites-5}

* (Touch-Benutzeroberfläche) Das &quot;Moved&quot;-Tag wird in den Seiteneigenschaften an der alten und neuen Position angezeigt. NPR-21921, Hotfix für CQ-4238598
* (Touch-Benutzeroberfläche) Der Rich-Text-Editor entfernt alle Attribute außer ID aus dem &lt;a>-Tag. NPR-22045: Hotfix für CQ-4234133
* Beim direkten Einfügen von Inhalten in den Rich Text Editor mit Strg+V werden die Zeilenumbrüche übersprungen. NPR-22117: Hotfix für CUI-5881
* (Touch-Benutzeroberfläche) Unter Namensraum können nicht mehr als 40 Tags angezeigt werden. NPR-22290: Hotfix für CQ-99114
* RSS-Feed-Probleme, Port -1 bis AEM 6.2 NPR-22158: Hotfix für CQ-4233339
* (IE) Beim ersten Authoring eines Zeichens im Feld &quot;Rich Text&quot;wird dem Zeichen ein Leerzeichen am Ende hinzugefügt. NPR-22443: Hotfix für CQ-4235343
* Bei dem Versuch, den Paketnamen zuzuordnen, friert das Java Use-Objekt den SightlyJavaCompilerService aufgrund eines Leerzeichen in der Paketdeklaration ein. NPR-22557: Hotfix für Granite-20836
* Die Touch-UI-Konsole erfasst keine neuen Sprachen für das Tagging. NPR-22250: Hotfix für CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Sowohl das Veröffentlichungsdatum als auch das Datum der Titelseite mussten für Folios festgelegt werden, bevor sie in DPS hochgeladen werden. NPR-22484

### Commerce {#commerce}

* Mehrere Site-übergreifende Skripting-Verwundbarkeiten (XSS) beim Handel erstellen Katalog-Assistenten. NPR-22344: Hotfix für CQ-4237017

### MSM {#msm-2}

* Die Synchronisierung von LiveCopyIndex führt bei langen Indexaktualisierungen zu einer Überlastung der Threads. NPR-22214: Hotfix für CQ-90667
* cq:cugEnabled-Eigenschaft ist deaktiviert, wenn ein anderes Feld in einer Livecopy bearbeitet wird, wodurch die Seite ungeschützt wird. NPR-22246: Hotfix für CQ-4236050
* Die Seitenausführungsaktion kann untergeordnete Elemente nicht aktualisieren, wenn eine Seite ausgesetzt wird. NPR-22483: Hotfix für CQ-4236956
* Das Rollout einer Struktur, die in einem Master verschoben wurde, führt zu einem falschen cq:moveTarget. NPR-22373: Hotfix für CQ-4232536

### Integrationen {#integration-6}

* Der Versuch, Angebot in der Angebot-Auswahlbibliothek zu sortieren, führt zu einem unregelmäßigen Verhalten. NPR-22208: Hotfix für CQ-4235439
* TargetContentImpl verlangsamt AEM bei langwierigen Abfragen. NPR-22361: Hotfix für CQ-4236907
* Die Target-Engine (mbox.js, at.js) verwendet keine verwalteten URLs, und sie verwendet URLs mit Doppelpunkten, die bei bestimmten Bereitstellungen fehlschlagen können. NPR-22366: Hotfix für CQ-4237854
* Die Personalisierung der Seite erfordert die Veröffentlichung direkt auf dem Markenknoten. NPR-22370: Hotfix für CQ-4236895

### Foundation {#foundation}

* Apache Sling Scripting Sightly Models verwenden Provider bundle **org.apache.sling.scripting.siwelly.models.provider/1.0.18**. NPR-22614: Hotfix für Sling-5944, Sling-6866

### Projekte {#projects}

* Workflow Starter kann den TypeHint-Wert von String nicht akzeptieren. NPR-22436: Hotfix für CQ-4237855

### Übersetzung {#translation-2}

* Untersuchen von Problemen mit der Vorschaufunktion. NPR-22201: Hotfix für CQ-4223753

### Benutzeroberfläche {#user-interface-2}

* (Klassische Benutzeroberfläche) Die Komponente zeigt die Standardwerte an, selbst wenn der zugehörige Formulardatenmodelldienst auf ein leeres Feld eingestellt ist. NPR-21903: Hotfix für GRANITE-19744

### WCM - Foundation-Komponenten  {#wcm-foundation-components-3}

* Fehler beim Veröffentlichen einer Live Copy-Seite, die auf eine Importer-Seite in Adobe Campaignen verweist. NPR-22470: Hotfix für CQ-4237164
* JavaScript-Fehler beim Öffnen des Experience Fragments Editor. NPR-22598: Hotfix für CQ-4238415

### Workflow {#workflow}

* Der Day CQ Workflow E-Mail-Benachrichtigungsdienst Trigger eine E-Mail pro Mongo-Knoten für WorkflowComplete- und WorkflowAborted-Benachrichtigungen. NPR-22486: Hotfix für CQ-4238172

## Formulare {#forms-6}

### Forms-Add-on-Paket {#forms-add-on-package-6}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

#### Adaptive Formulare {#adaptive-forms-4}

* Inkonsistenzen im Dropdown-Platzhalterwert im adaptiven Formular in IE11 und Chrome. NPR-22405: Hotfix für CQ-4227096

### Forms JEE-Installationsprogramm {#forms-jee-installer-6}

#### Installieren von LCM {#install-lcm}

* Aktualisieren von Jsafe Jars auf Cryptoj 6.1.3.1 im Installationsprogramm und LCM. NPR-22744

### Enthaltene Feature Packs {#feature-packs-included}

#### Prozessverwaltung {#process-management}

* (HTML Workspace) Wenn ein Benutzer eine Aufgabe beansprucht, wird die Anzahl der Warteschlangen für den betreffenden Benutzer aktualisiert, nicht jedoch für andere Benutzer, es sei denn, die Seite wird aktualisiert. NPR-19778: Hotfix für CQ-4233665

### OSGI-Pakete und Inhaltspakete, die in CFP14 enthalten sind {#osgi-bundles-and-content-packages-included-in-cfp}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP14 enthalten sind

[Datei laden](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Liste der in AEM 6.2SP1-CFP14 enthaltenen Inhaltspakete

[Get ](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
FileAEM Cumulative Fix Pack 6.2 SP1-CFP13 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Feldkonfiguration für statische Parameter in den Komponenteneinstellungen der Zielgruppe aktiviert, während AT.js als Client-Bibliothek verwendet wird.
* Korrekturen in der Ein-/Ausblenden-Funktion der Dropdown-Komponente.
* Fehlerbehebungen bei der Verwendung von Audiencen zum Synchronisieren von Zielgruppen.
* Die Vielseitigkeit von Correspondence Management zur Aufnahme von Sonderzeichen wurde verbessert.

### Assets {#assets-6}

* Bei der Versionsbereinigung werden alte Versionen von Assets nicht entfernt. NPR-21682: Hotfix für CQ-4212996
* Die Neuanordnung von Ordnern unter einem neu zu sortierbaren Ordner wird nicht beibehalten. NPR-21964: Hotfix für CQ-4231761

### Sites {#sites-6}

* (TouchUI)(ClassicUI) Mehrere Site-übergreifende Skripterstellungs-(XSS-)Schwachstellen in HTML- und Kernkomponenten. NPR-21532: Hotfix für CQ-4232305 und CQ-4232511
* Das Erstellen/Formatieren von Inhalten (z. B. Zuweisen/Entfernen neuer Liste-Stile) in einem ausgewählten Text funktioniert in Internet Explorer 11 nicht einwandfrei. NPR-21533: Hotfix für CQ-4230689
* (Safari) Benutzer können nicht alle Assets im Bedienfeld &quot;Asset-Suche&quot;Ansicht werden. NPR-21981: Hotfix für CQ-4213720
* Time Warp gibt den Fehler &quot;RecursionTooDeepException&quot;bei beschädigter Seite zurück. Es wird keine neue Version erstellt, auch wenn das Datum geändert wird. NPR-21707: Hotfix für CQ-4199536
* Beim Laden einer Seite im Editor wird der WorkflowStatusProvider (pageinfo.json) dreimal geladen, wodurch AEM Instanz langsam ausgeführt wird. NPR-21778: Hotfix für CQ-59232

### Integrationen {#integration-7}

* Die Erstellung von Audiencen von Mobiltyp und Browser im Authoring-Zielgruppe-Modus funktioniert AEM nicht. NPR-21676, NPR-21681: Hotfix für CQ-4232100
* Unter hoher Latenz während einer Aktualisierung einer Zielkomponente können Sie ein weiteres Angebot hinzufügen, bevor die Komponente vollständig aktualisiert wird. NPR-21744: Hotfix für CQ-4233158/CQ-4234293
* Benutzer können keine statischen Param-Werte im mbox-Aufruf sehen, die beim Testen mit AT.js als Client-Bibliothek in der Cloud-Konfiguration angezeigt werden. NPR-21930: Hotfix für CQ-4234520

### Plattform {#platform-4}

* Leistungsprobleme bei der Benutzersynchronisierung, wenn die Anzahl der Benutzer oder Gruppen groß ist. NPR-20431: Hotfix für CQ-4223282
* Benutzer, die mit der Benutzersynchronisierung nicht mit der Sling-Distribution synchronisiert wurden. NPR-21911: Hotfix für Granite-20404
* Verhindern, dass Stoppwörter in Suchauszügen (auf einer Geometrixx) hervorgehoben werden. NPR-21835: Hotfix für Granite-21067\
   Hinweis: Für diese Fehlerbehebung ist Oak CFP 1.4.20 oder höher erforderlich.

### Übersetzung {#translation-3}

* Die jcr-Eigenschaft fehlt für die Initiator-Benutzer-ID beim Erstellen des Übersetzungsprojekts. NPR-21715: Hotfix für CQ-4230713

### WCM - Foundation-Komponenten {#wcm-foundation-components-4}

* Die Funktion zum Anzeigen/Ausblenden der Formular-Dropdown-Komponente funktioniert nicht wie erwartet. NPR-22164: Hotfix für CQ-4235288

## Formulare {#forms-7}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-7}

#### Adaptive Formulare {#adaptive-forms-5}

* XML External Entity Injection (XXE)-Injektion in Adaptive Forms. NPR-21982: Hotfix für CQ-109878
* (iOS11) Wenn auf die Dateianlagenkomponente geklickt wird, wird beim Dateianhang die Kamera anstelle des Gerätedateibrowsers geöffnet. NPR-21926: Hotfix für CQ-4214348
* Fehlender Titel in der Benutzeroberfläche für die Designerstellung verursacht eine Ausnahme und das Rendering des Dialogfelds ist fehlgeschlagen. Hotfix für CQ-4236143

#### Korrespondenzverwaltung {#correspondence-management-1}

* Rendering-Probleme mit XML-Daten, die Sonderzeichen enthalten. NPR-21712: Hotfix für CQ-4229137

### Forms JEE-Installationsprogramm {#forms-jee-installer-7}

#### Assembler-Dienst {#assembler-service}

* Die mit 6.2.0-ASM-1017-003 generierte PDF-Datei ist beschädigt. NPR-21427: Hotfix für CQ-4228046

#### PDFG-Dienst {#pdfg-service-1}

* OCR-Fehler aufgrund unerwarteter Seitengröße (PDF) aus PNG-, JPEG- und TIFF-Dateien. NPR-19489: Hotfix für CQ-4209079

## OSGI-Pakete und Inhaltspakete, die in CFP13 enthalten sind{#osgi-bundles-and-content-packages-included-in-cfp-1}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP13 enthalten sind

[Datei laden](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Liste der in AEM 6.2SP1-CFP13 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Verbesserte Verarbeitung von Metadaten für Felder mit mehreren Werten.
* Unterstützung von mehrstelligen (mehr als zwei) Ländercodes in Workflows.
* Verbesserte Wiedergabe von Seiten mit mehreren verschachtelten Komponenten.
* Verbesserte Synchronisierung der Veröffentlichungsdaten für Assets zwischen AEM und Adobe Digital Publishing Suite.

### Assets {#assets-7}

* Zu viele Zeichen in OmniSearch führen zum Absturz des AEM-Servers. NPR-21083: Hotfix für CQ-4223602
* Werte, die in der zweiten Option in einem Feld mit mehreren Werten in Metadaten-Schemas angegeben sind, werden nicht an die zuvor angegebenen Werte in CRX-de angehängt. NPR-21220: Hotfix für CQ-4224526
* Asset-Download schlägt fehl, wenn Digital Rights Management in Assets in Safari verwendet wird. NPR-21387: Hotfix für CQ-4230287

### Sites {#sites-7}

* (DAM) (ClassicUI) Mehrere Site-übergreifende Skripterstellungs-(XSS-)Schwachstellen in einigen SWF-Dateien in AEM CQ Author/Publish quickstart. NPR-21073, NPR-21074: Hotfix für NPR-20612
* Die Tag-Auswahl übersetzt keine Tags, die in mehreren Sprachen verfügbar sind.NPR-21221: Hotfix für CQ-78855
* Durch das Rendern von Problemen mit AEM Artikelkonsole als Verwendung mehrerer verschachtelter Komponenten wird die Wiedergabe verlangsamt. NPR-21271: Hotfix für CQ-4224158

### Integrationen {#integration-8}

* Beim Hinzufügen eines Zielgruppe-Frameworks ist der Targeting-Modus in der Liste Select mode im Editor nicht verfügbar. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Die Veröffentlichungsdaten für Folios in AEM entsprechen nicht den Datumsangaben, die im Folio Producer angezeigt werden. NPR-21145

### MSM {#msm-3}

* Der Prozess zum Zurücksetzen der Live Copy-Funktion wird beendet, nachdem die erste lokale Seite im LC gelöscht wurde. NPR-21276: Hotfix für CQ-4229743

### Plattform {#platform-5}

* Benutzerdefinierte Taglib, die als Skript implementierte Referenz-Tags enthalten, werden nach der Aktualisierung auf AEM 6.3 nicht gefunden. NPR-20149: Hotfix für Granite-18433

### Übersetzung {#translation-4}

* Die Workflows schlagen mit lang_country-Codes fehl, die länger als 2 Zeichen sind. NPR-21088: Hotfix für CQ-4197439
* Die Asset-Seite darf erst nach Abschluss des Projekts erneut an ein Übersetzungsprojekt gesendet werden. NPR-21219: Hotfix für CQ-4209908

### Benutzeroberfläche {#user-interface-3}

* Die Eigenschaft &quot;Zielgruppe auswählen&quot;wird beim Senden des Formulars nicht gelöscht. NPR-21163: Hotfix für GRANITE-14125
* HTTP.encodePathOfURI expandieren Dublette kodiert das Pluszeichen &#39;+&#39;. NPR-21417: Hotfix für GRANITE-16340

### Schwachstelle {#vulnerability-4}

* Site-übergreifende Skripterstellung (XSS) im DAM-Metadaten-Editor. NPR-21434: Hotfix für CQ-83472
* Mehrere SWF-Dateien, die für Cross-Site Scripting (XSS) verwundbar sind. NPR-20612: Hotfix für CQ-4213297

## Formulare {#forms-8}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

### Forms-Add-on-Paket  {#forms-add-on-package-8}

#### Korrespondenzverwaltung {#correspondence-management-2}

* (IE11) Das anfängliche Rendering des HTML-Inhalts erfolgt nur auf der linken Seite, während die rechte Seite nach dem Laden der vollständigen Benutzeroberfläche gelegentlich geladen wird. NPR-21554
* Die Senden-Schaltfläche &quot;Brief-Vorschau&quot;wird nach der Installation von AEM 6.2 SP1-CFP9 deaktiviert. NPR-21547
* Bei Auswahl des Asset-Verknüpfungstyps wird das Fenster &quot;Asset-Auswahl&quot;im Assistenten zum Bearbeiten der Briefinbindung nicht geöffnet. NPR-21164: Hotfix für CQ-4194567
* Um ein Inline- oder bearbeitbares Textmodul zu bearbeiten, tippen Sie auf das entsprechende Symbol &quot;Bearbeiten&quot;oder klicken Sie in der Vorschau auf das entsprechende Textmodul. NPR-21402

#### Adaptive Formulare {#adaptive-forms-6}

* Die Komponente für die AEM Forms-Senden-Schaltfläche zeigt type=&quot;button&quot; anstelle von type=&quot;submit&quot; an. NPR-21007
* Beim Hinzufügen oder Löschen neuer Bereiche für wiederholbare Bereiche bleiben die Daten erhalten. NPR-21408

### Forms JEE-Installationsprogramm {#forms-jee-installer-8}

#### Core {#core-2}

* Beim Aktualisieren auf das neueste Java 8 Update 131 wird eine Ausnahme ausgelöst: &quot;Der JsafeJCE Provider ist deaktiviert, eine für FIPS 140 erforderliche Prüfung der Selbstintegrität ist fehlgeschlagen.&quot; NPR-21355

   **Hinweis:** Dieses NPR erfordert zusätzliche Einstellungen. Weitere Informationen finden Sie unter  [Neueste Java 8-Aktualisierung](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr).

* Aktualisieren Sie jsafe jars auf cryptoj 6.1.3.1 in Core, Encryption, Signature &amp; Dokument Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Installieren von LCM {#install-lcm-1}

* Aktualisieren Sie Jsafe Jars auf Cryptoj 6.1.3.1 im Installationsprogramm und LCM. NPR-21362

#### PDFG-Dienst {#pdfg-service-2}

* Aktualisieren Sie Jsafe Jars auf Cryptoj 6.1.3.1 in PDFG. NPR-21359

#### Prozessverwaltung {#process-management-1}

* (HTML Workspace) Aktivieren der Spaltengröße, sodass die Kategorie &quot;Name&quot;nicht abgeschnitten angezeigt wird. NPR-19770: Hotfix für CQ-4233668

#### Reader Extensions-Dienst {#reader-extensions-service-1}

* Aktualisieren Sie jsafe jars auf cryptoj 6.1.3.1 in RE. NPR-21357

## OSGI-Pakete und Inhaltspakete, die in CFP12.1 enthalten sind{#osgi-bundles-and-content-packages-included-in-cfp-2}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP12.1 enthalten sind

[Datei laden](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Liste der in AEM 6.2 SP1-CFP12.1 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Aktualisierung von cq-msm-core für eine effiziente Livecopyindex-Synchronisierung.
* Verbesserte Bearbeitungseffizienz für Inhaltsfragmente.
* Bietet eine Überprüfungsoption im Paketmanager zum Erkennen von ACL-Berechtigungen.
* Es wurde die Möglichkeit der Kampagne eingeführt, E-Mail-ID für Kundenkorrespondenz einzuschließen.
* Verbesserte Videokodierungsfunktionen für Dynamic Media-Dateien.
* Korrekturen in &quot;Sightly Component&quot;und &quot;LiveCopies&quot;.

### Assets {#assets-8}

* Die Dynamic Media-Videokodierung schlägt bei Dateien fehl, die Leerzeichen in ihren Namen enthalten. NPR-20818: Hotfix für CQ-102469
* Mehrere Site-übergreifende Skripting-(XSS-)Schwachstellen in einigen SWF-Dateien in AEM CQ Author/Publish quickstart. NPR-21071, NPR-21072
* Benutzer können keine Assets mit Haftungsausschluss und langen Dateinamen herunterladen. NPR-20255: Hotfix für CQ-4222139

### Sites {#sites-8}

* Integration von AEM und Kampagne: Spezielle Links werden in Adobe Campaign umgeschrieben, sodass die Kunden keine Mails senden können: Hyperlinks in ihren E-Mails. NPR-20787: Hotfix für CQ-4225760
* (Touch UI) AEM Probleme mit der Benutzerfreundlichkeit und der Leistung, wenn die Sprache auf Französisch eingestellt ist. NPR-20854: Hotfix für CQ-4227628
* Beim Verknüpfen einer kodierten Asset-Datei mit dem Link-Plugin in RTE wird ein leerer Link zurückgegeben. NPR-20626, NPR-21059: Hotfix für CQ-4223011
* Der Metadaten-Editor für Inhaltsfragmente verhindert, dass Inhaltsersteller Änderungen an Inhaltsfragmenten speichern. NPR-20641: Hotfix für CQ-4224755
* Der Alias für die Seiteneigenschaft führt zur Anforderung der Veröffentlichung/Aufhebung der Veröffentlichung. NPR-20731: Hotfix für CQ-4226227
* Textkomponente Probleme mit der Kodierung des Links im RTE-Element. NPR-20755: Hotfix für CQ-4224321

### Plattform {#platform-6}

* ResourceResolverImpl.map() ruft ResourceDecorator nicht auf. NPR-20788: Hotfix für GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver kann Anforderungen nicht über org.apache.sling.engine.SlingRequestProcessor verarbeiten. NPR-20706: Hotfix für CQ-94880
* Anforderung des Hinzufügens einer Überprüfungsoption in Package Manager, um festzustellen, ob ACL-Berechtigungen/-Berechtigungen für ein bestimmtes Paket geändert wurden. Hotfix für CQ-4229196

### Integrationen {#integration-9}

* (Search&amp;Promote) Eine unverbindliche Filterdefinition für das Inhaltspaket führt bei der Installation zu überschriebenen Pfaden. NPR-20808: Hotfix für CQ-4227615

### Workflow {#workflow-1}

* Stabilitätsprobleme bei der Bereitstellung des AEM-Produktions-Servers. NPR-20979: Hotfix für Granite-19104

### Projekte {#projects-1}

* (Touch-Benutzeroberfläche) Teammitglieder können keinem Projekt hinzugefügt werden. NPR-20990: Hotfix für CQ-4205375

### WCM – Foundation-Komponenten {#wcm-foundation-components-5}

* &quot;Link zu&quot;der Komponente &quot;Sightly Image&quot;erzeugt einen 403-Fehler aufgrund der fehlenden Erweiterung &quot;.html&quot;. NPR-20823: Hotfix für CQ-4195909
* Auf einer Blueprint-Site mit LiveCopy löscht der Versuch, eine Formularkomponente zu löschen, eine NullPointerException und fügt die Form-Komponente zurück, anstatt sie zu löschen. NPR-20855: Hotfix für CQ-4204628
* Die Synchronisierung von LiveCopyIndex führt bei langen Indexaktualisierungen zu einer Überlastung der Threads. NPR-20634: Hotfix für CQ-90667

### Sicherheit {#security}

* Proaktive XSS-Bibliotheksaktualisierung. NPR-21174
* Aktualisieren Sie auf Apache Commons Email 1.5, das eine vereinfachte API zum Senden von E-Mails enthält. NPR-20509: Hotfix für Granite-18240
* Sicherheits-Patch angewendet auf Apache Sling XSS Schutz API, um die Möglichkeit der XSS Umgehung zu beseitigen. NPR-21290: Hotfix für GRANITE-19924
* XSS-Umgehung in der Funktion XSSAPI#getValidHref. NPR-21174: Hotfix für Granite-19924

### Mobile Apps {#mobile-apps}

* Es wurden Probleme mit Curl Head-Anforderungen für OOTB-Assets in AEM behoben. NPR-20511: Hotfix für CQ-4221520 und CQ-103024

## Formulare {#forms-9}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

Die wichtigsten Highlights für AEM Forms sind:

* Zertifikatauthentifizierung für Workbench-Benutzer aktiviert.
* Korrekturen an der Benutzerfreundlichkeit für Correspondence Management, HTML5-Formulare und AEM Forms Workspace.

### Forms-Add-on-Paket {#forms-add-on-package-9}

#### HTML5-Formulare {#html-forms-1}

* Probleme mit der Benutzerfreundlichkeit bei der Scribble-Komponente auf iOS 10- und 11-Geräten. NPR-21092

#### Korrespondenzverwaltung {#correspondence-management-3}

* (Correspondence UI) Deaktivieren Sie die Senden-Schaltfläche nach einem Klick. NPR-21078

### Forms JEE-Installationsprogramm {#forms-jee-installer-9}

#### Assembler-Dienst {#assembler-service-1}

* docConvertor kann PDF/A nicht mit der Fehlermeldung &quot;Das Präfix &quot;stEvt&quot;für das Element &quot;stEvt:action&quot;ist nicht gebunden&quot;erzeugen. NPR-21032: Hotfix für CQ-4222540
* Eine Ausnahme wird mit dem Namen java.lang.IllegalArgumentException message:No enum-Konstante com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE beim Aufrufen des Dienstes OMPFSubmission/PDFA/PDFtoPDFA ausgelöst. Dadurch wird verhindert, dass der Prozess zur Überprüfung der Signatur mit kurzer Lebensdauer abgeschlossen wird, bis der Server neu gestartet wird. NPR-20792

#### Workbench {#workbench}

* Aktivieren Sie die Zertifikatauthentifizierung für Workbench-Benutzer. NPR-17548: Hotfix für CQ-4214486

#### Prozessverwaltung {#process-management-2}

* Vorbereiten von Datenverarbeitungsprozessen ruft mehrere Male auf, wenn ein mobiles Formular mit Datenformaten wiedergegeben wird. NPR-19801: Hotfix für CQ-4230427: CQ-4230400

## OSGI-Pakete und Inhaltspakete, die in CFP11 enthalten sind{#osgi-bundles-and-content-packages-included-in-cfp-3}

Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP11 enthalten sind

[Datei laden](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Liste der in AEM 6.2 SP1-CFP11 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Es wurde eine neue Dienstprogrammfunktion onDialogLoaded für Tests hinzugefügt.
* Tests und Konfigurationen der Frontend-Einheiten wurden zu ClientLibraryProxyServlet hinzugefügt.
* Leistungsverbesserungen in der Komponente &quot;Mehrere ersetzende Bilder&quot;.
* Konfigurationsaktualisierungen in Apache Sling JCR ResourceBundleProvider.

### Assets {#assets-9}

* Die Asset-Vorschau funktioniert nicht, wenn die Workflows für die Asset-Aktualisierung deaktiviert sind. NPR-20543: Hotfix für CQ-4204986
* Rendering-Probleme mit der im Granit hinzugefügten Klasse: class-Eigenschaft (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix für CQ-4219238
* Miniaturansichten mit Sonderzeichen im Titel zeigen Java-Objekt im Alt-Attribut von NPR-20347 an: Hotfix für CQ-4223620
* Ersetzen Sie Versionsvergleichscode durch Adobe-proprietären Code aufgrund von Lizenzproblemen. NPR-20273: Hotfix für CQ-4223758
* Verarbeitungsfehler beim Hochladen von CMYK-PSB-Dateien mit mehreren Alpha-Ebenen. NPR-20251: Hotfix für CQ-4220869
* Internationalisierungswörterbücher funktionieren nur, wenn der Server in org.apache.sling.i18n 2.5.6 neu gestartet wird. NPR-20525: Hotfix für Granit - 19490
* Es werden keine Thread-Dumps gemäß der Planung mit der standardmäßigen Thread Dump Collector-Konfiguration (Standard AEM Beginn-up) generiert. NPR-20288: Hotfix für GRANITE-19488/GRANITE-12741/CQ-90647.

### Sites {#sites-9}

* Wenn der Filter für das geänderte Datum nach dem Öffnen der gespeicherten Suche geändert wird, hat dies keine Auswirkungen auf die Ergebnisse und die angezeigten Ergebnisse sind mit dem vorherigen gespeicherten Wert des Filters für das geänderte Datum identisch. NPR-19739: Hotfix für CQ-4219425
* Seiten mit verschachtelten Komponenten konnten nicht geladen werden. NPR-20312
* Der Arbeitsablauf für die Löschanforderung wird beim Löschen von Workflow-Paketen ausgelöst. NPR-20266: Hotfix für CQ-4221686
* (Touch-Benutzeroberfläche) Problem beim Kopieren/Einfügen mit der Zwischenablage des Betriebssystems und der internen AEM. NPR-20228: Hotfix für CQ-4220383
* AEM Instanz wird bei der Ansicht der Liste schleppend, wenn mehrere Assets (über 100) geladen werden. NPR-20034: Hotfix für CQ-4222695
* (Touch-optimierte Benutzeroberläche) Das Löschen von Launches über die Konsole der klassischen Benutzeroberfläche macht alle Seiten unbearbeitbar. NPR-20520: Hotfix für CQ-4225074
* Das Dropdown-Menü &quot;Zielgruppe&quot;funktioniert nicht mit mehreren RTE-Komponenten in einem Dialogfeld. NPR-20345: Hotfix für CQ-4220981

### Plattform {#platform-7}

* Beim Zugriff über eine anonyme Sitzung proxyliert ClientLibraryProxyServlet nicht die Anforderungen an Client-Bibliotheken in der Veröffentlichungsinstanz und gibt den Fehler HTTP 404 nicht gefunden zurück. NPR-20195: Hotfix für Granite-14409

### Integrationen {#integration-10}

* Wenn Sie die Zielgruppe-Engine als Adobe Target auswählen, wird verhindert, dass die Komponente geladen wird, und es wird ein Fehler im Serverprotokoll ausgegeben. NPR-20058: Hotfix für CQ-88071, CQ-109698, CQ-4201600

### Commerce {#commerce-1}

* Beim Erstellen von Produkten derselben Seite wird keine Bestätigungs- oder Umleitungs-Popup-Meldung angezeigt. NPR-20257: Hotfix für CQ-4223414

### Benutzeroberfläche {#user-interface-4}

* Wenn der Datumsbereich ein Feld in einem Multifeld ist, werden die in Datumsfeldern gespeicherten Werte beim Bearbeiten der Komponente nicht beibehalten. NPR-20077: Hotfix für GRANITE-19147
* Vorherige Abfragen werden nicht abgebrochen, wenn aufeinander folgende Abfragen ausgelöst werden und zu falschen Ergebnissen führen. NPR-20397: Hotfix für GRANITE-19306

### WCM - Foundation-Komponenten {#wcm-foundation-components-6}

* Die ImageMap-Eigenschaft existiert auch nach dem Entfernen der Bilder aus der Komponente &quot;Mehrere Bilder an Ort und Stelle&quot;. NPR-20142: Hotfix für CQ-4222982

## Formulare {#forms-10}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

### Forms-Add-on-Paket  {#forms-add-on-package-10}

#### Adaptive Formulare {#adaptive-forms-7}

* valueCommit-Skript wird für DropDownList zweimal ausgeführt, wenn es über die Benutzeroberfläche geändert wird. NPR-19989: Hotfix für CQ-110212

### Forms JEE-Installationsprogramm {#forms-jee-installer-10}

**Prozessverwaltung**

* Das CFP-Paket enthält die AEM Forms HTML Workspace-Version 2.2.26. NPR-20099
* Das vorausgefüllte Formular funktioniert nicht, wenn das mobile Formular für die Ansicht als PDF konfiguriert ist. NPR-20566

**Rights Management**

* CAC/Dialogfeld zur Auswahl des Zertifikats für gegenseitige Authentifizierung sollte Zertifikate mit erweiterter Schlüsselverwendung (EKU) als Client-Authentifizierungs- oder Chipkartenanmeldung anzeigen. NPR-20708
* Forms JEE unterstützt die gegenseitige Authentifizierung mit PKCS#11. NPR-15001

## OSGI-Pakete und Inhaltspakete, die in CFP10 enthalten sind {#osgi-bundles-and-content-packages-included-in-cfp-4}

Liste von OSGi-Bundles, die in AEM CFP 6.2 SP1-CFP10 enthalten sind

[Datei laden](assets/do-not-localize/bundle-list-cfp10.txt)

Liste der in AEM CFP 6.2 SP1-CFP10 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Die Analytics Classic-UI-Konfiguration wurde für die geheime Eingabe angepasst.
* Fehlerbehebungen für unabhängigen Persistenzcache für Contexthub.
* Genaue Berechnung der Asset-Dimensionen.
* Die AEM Leistung wurde beim Veröffentlichen von Assets im Markenportal optimiert.
* Fehlerbehebungen im Ressourcentyp-Wert im Arbeitsflächenknoten.
* Die Suchfunktion für Dokument-Fragmentinhalte wurde mit der Unterscheidung zwischen Groß- und Kleinschreibung und Sonderzeichen aktiviert.
* Adaptives Forms wurde verbessert, um PDF als Anhänge in Safari anzuhängen.\
   Bietet ein neues Dynamic Media, das eine Verbindung zur neuen Dynamic Media Publishing Infrastruktur herstellt, um die Replikation zu beschleunigen und zu verbessern.

### Assets {#assets-10}

* AEM Assets kann für InDesign-Assets keine Unterasset-Verweise extrahieren, einschließlich Duplikat-Links zum Asset. NPR-19006: Hotfix für CQ-4204186
* Die Option &quot;Sortieren&quot;funktioniert nicht für Assets in der Sammlung unter &quot;Commerce&quot;. NPR-19508: Hotfix für CQ-4213622
* Wenn ein Asset mit demselben Namen wie ein bereits vorhandenes Asset an denselben Speicherort verschoben wird, wird der Wert cq: lastReplicationAction für die Assets wird untereinander ausgetauscht, wodurch falsche Metadaten erstellt werden. NPR-19531
* Beim Veröffentlichen einer großen Anzahl von Assets wird eine Fehlermeldung angezeigt, obwohl alle Assets korrekt veröffentlicht wurden. NPR-19629: Hotfix für CQ-4219611
* Statische Darstellungen werden mit festen Abmessungen aufgeführt und spiegeln nicht die Größe der tatsächlichen Darstellung wider. NPR-20004
* Wenn mehrere Assets (mehr als 4) in Brand Portal veröffentlicht werden sollen, reagiert die AEM-Instanz nur langsam. NPR-20009

### Sites {#sites-10}

* AEM zeigt unerwartetes Verhalten an, wenn ein Benutzer versucht, eine durch einen anderen Benutzer gesperrte Seite zu veröffentlichen/die Veröffentlichung rückgängig zu machen/zu erstellen. NPR-19249; Hotfix für CQ-4215298 und CQ-4203856
* Beim manuellen Werben für den verschachtelten Start wird die untergeordnete Seite gelöscht. NPR-19704
* Persistenzprobleme, wenn ContextHub während der Initialisierung die standardmäßige Persistenzschicht überschreibt. NPR-19979: Hotfix für CQ-4218399
* Inhaltsfragmente überschneiden sich mit anderen Schaltflächen. NPR-19980: Hotfix für CQ-4221519
* Die Site-Seite wird nicht angezeigt, wenn sie mit einem Alias in SiteAdmin angezeigt wird. NPR-20053: Hotfix für CQ-4221478
* Fehler beim Veröffentlichen einer Live Copy-Seite, die auf eine Importer-Seite in Adobe Campaignen verweist. NPR-20066: Hotfix für CQ-4220846

### Plattform {#platform-8}

* Apache POI wurde auf Version 3.16 aktualisiert, um die Einbeziehung des Hintergrundbilds von PPT-Folien in Darstellungen zu unterstützen. NPR-18286
* Rendering-Probleme mit Internet Browser 11 und Edge beim Hochladen mehrerer Assets in denselben Ordner. NPR-20062

### Integrationen {#integration-11}

* Die benutzerdefinierte at.js-Datei wird nicht veröffentlicht, wenn der Zugriff via anonymer Benutzer erfolgt. NPR-19542: Hotfix für CQ-4219592
* Migration vorhandener Analytics-Anmeldeinformationen zur WSSE-Authentifizierung. NPR-19962

### Brand Portal {#brand-portal}

* Ermöglicht die Veröffentlichung von Tags von AEM im Brand Portal über die Tagadmin/Tagging-Konsole. NPR-20271

## Formulare {#forms-11}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

### Forms-Add-on-Paket  {#forms-add-on-package-11}

#### Korrespondenzverwaltung {#correspondence-management-4}

* Aktivierte Funktion zum Suchen nach tatsächlichem Dokument in Fragmenten, wenn ein Brief in der Vorschau angezeigt wird. NPR-19712

#### Adaptive Formulare {#adaptive-forms-8}

* Adaptives Forms wurde verbessert, um PDF als Anhänge in Safari anzuhängen. Um die gleiche Funktionalität in vorhandenen Formularen zu unterstützen, müssen wir die Konfigurationsänderung im Anhang-Widget vornehmen und unter &quot;Unterstützte Dateitypen&quot;den Wert application/pdf anstelle von .pdf aktualisieren. NPR-19623

#### Forms Manager {#forms-manager-1}

* Wenn validationState für ein Feld des adaptiven Formulars nicht definiert ist und das Ereignis elementFocusChanged auftritt, wird ein Fehler-Ereignis (errorState) an den Adobe Analytics-Server zurückgegeben. NPR-19513

### Forms JEE-Installationsprogramm {#forms-jee-installer-11}

#### Core {#core-3}

* Der Verbindungsmanager ist beim Herunterfahren nicht verfügbar. Jboss schließt die JDBC-Abhängigkeit ab, bevor die EAR-Datei des Autors nicht mehr bereitgestellt wird, was zu Korruptionsproblemen führt. NPR-19703

## Enthaltene Feature Packs {#feature-packs-included-1}

* Verbesserte Miniaturkorrektur und Transparenz in Dynamic Media. NPR-15207

## OSGI-Pakete und Inhaltspakete, die in CFP9 enthalten sind {#osgi-bundles-and-content-packages-included-in-cfp-5}

Liste der in AEM 6.2SP1-CFP9 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Liste von OSGi-Bundles aktualisiert in AEM 6.2SP1-CFP9

[Datei laden](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Einführung von Tags zu benutzerdefinierten Benutzervorlagen beim Adobe-E-Mail-Vorlagendienst.
* Verbesserungen an TouchUI-Schaltflächen in der Desktop-App.
* Schaltfläche zum Senden beim Klicken deaktiviert, um zu verhindern, dass mehrere Formulare auf einer Übersetzungsseite gesendet werden.
* Mehrere RTE-Komponenten in einem Dialogfeld konfiguriert.
* Verbesserte ReferenzUpdates in Live Copy.
* Die Suchfunktion für Dokument-Fragmentinhalte wurde mit der Groß- und Kleinschreibung aktiviert.
* Liste von Linux-Bibliotheken zur AEM Forms-Installationsdokumentation hinzugefügt.

### Assets {#assets-11}

* Probleme bei der Anwendung des Omniture-Suchfilters auf intelligente Sammlungen im Safari-Browser. NPR-19511
* PDF-Stichwortmetadaten werden nicht korrekt extrahiert und geändert, wenn mehrere Stichwörter mit einem PDF-Asset verknüpft sind. Um das Problem zu beheben, wurde die Metadateneigenschaft für das Feld „Betreff“ für PDF-Assets entfernt. Sie können das Metadatenschema jedoch bearbeiten, um ein Textfeld mit mehreren Werten für das Feld „Betreff“ hinzuzufügen. NPR-19126
* Der Workflow-Benachrichtigungsdienst kodiert die Links nicht in E-Mails, wodurch verhindert wird, dass sie geladen werden, wenn der Benutzer darauf klickt. NPR-19490: Hotfix für CQ-4218055
* Die vollständige Liste der Seiten/Assets kann nicht in der Spaltenansicht mit Chrome geladen werden. NPR-19458: Hotfix für CQ-4214248
* Beim Aktivieren des Arbeitsablaufs &quot;Anforderung zur Aktivierung&quot;wird AEM Posteingang mit dem falschen Symbol für die Zeitüberschreitung angezeigt. NPR-19365: CQ-4216174
* Probleme mit der Sortierung in der Ansicht Liste. NPR-19217: CQ-95602
* Wenn Sie den Titel oder das Miniaturbild in den Einstellungen für den Asset-Ordner ändern, werden die ursprüngliche Gruppe und die Berechtigungen des Ordners überschrieben. NPR-19283: Hotfix für CQ-4216080
* Windows 10-Workstations wechseln automatisch in den Touch-Modus, wodurch einige Schaltflächen nicht mehr funktionieren. NPR-19183

### Sites {#sites-11}

* Probleme mit mehreren RTE-Komponenten in einem Dialogfeld. NPR-19311: NPR-19587
* Die automatische Versionsbereinigung in Vanille AEM 6.2 funktioniert nur einmal, nachdem VersionManagerImpl initialisiert wurde. NPR-19315: Hotfix für CQ-4217175
* Die Workflow-Instanz wird beim Workflow-Schritt &quot;Salesforce.com Export&quot;angehalten. NPR-19222: Hotfix für CQ-4212976
* Seiten mit Sprachkopien, die aus Live-Kopien erstellt wurden, können nicht bearbeitet werden. NPR-18967
* ReferencesUpdateAction kann Links nicht mit Hierarchieänderungen in eine verschachtelte LiveCopy aktualisieren. NPR-18715: Hotfix für CQ-4214105

### Plattform {#platform-9}

* Der Adobe-E-Mail-Vorlagendienst fügt benutzerdefinierten Benutzervorlagen Tags hinzu. NPR-19190: Hotfix für CQ-4217113

### Projekte {#projects-2}

* Projekteditoren können keine Assets in den Asset-Ordner des Projekts kopieren/einfügen. NPR-19619
* Nach der Installation von 6.2 SP1-CFP1 kann keine Vorschau für Übersetzungsprojekte generiert werden. NPR-16481: CQ-4204655

### Integrationen {#integration-12}

* Zugriffseigenschaften für Artikel werden in Adobe Digital Publishing Solution in der klassischen Benutzeroberfläche falsch eingestellt. NPR-19366
* Reduzieren Sie die Wiedergabe von Miniaturbildern aufgrund von Artikeln in voller Größe in AEM Artikelkonsole. NPR-19086: CQ-4217148
* Falsches Verhalten der automatischen Faltung bei der Personalisierung von Angeboten über Campaign, wenn Benutzer Zugriff auf mehrere Bereiche haben. NPR-19290: Hotfix für CQ-4218029
* Dialogfeld „Targeting“ wird nicht im Targeting-Modus angezeigt, wenn ein Zielmodul bearbeitet und mehr als einmal gespeichert wird. NPR-19144: Hotfix für CQ-4216708

### Workflow {#workflow-2}

* Benutzer, die in der Benutzeroberfläche von Inbox Classic keine Benachrichtigungen im Posteingang nach Benutzer/Gruppe filtern können. NPR-19122: Hotfix für CQ-4215374
* Die ausgewählten Koordinaten in der HTML-Bildkomponente werden in der Imagemap nicht beibehalten. NPR-18911: CQ-4211584

## Formulare {#forms-12}

* AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-12}

* Wenn Inhalte aus Microsoft Word oder einem Webbrowser in den Texteditor von Correspondence Manager kopiert werden, geht der Stil verloren. NPR-19530
* Inhalt ohne Zeilenumbruch im Texteditor wird nicht umgebrochen. NPR-19481
* Aktivierte Funktion zum Suchen nach tatsächlichem Dokument in Fragmenten, wenn ein Brief in der Vorschau angezeigt wird. NPR-17792: Hotfix für CQ-4214501

#### Korrespondenzverwaltung {#correspondence-management-5}

>[!NOTE]
>
>Diese Suchfunktion für Textfragmente hat einige Einschränkungen:-
>
>* Bei Dokument-Fragmentinhalten wird die Groß-/Kleinschreibung beachtet, bei Titeln wird nicht zwischen Groß- und Kleinschreibung unterschieden.
>* Die Suchergebnisse werden nicht hervorgehoben, wenn ein Teil des gesuchten Wortes in einem anderen Stil oder mit Sonderzeichen wie &quot; oder &quot; oder &quot; oder \ steht.
>* Die Suche funktioniert nicht bei dynamischen Inhalten (wie Datenwörterbuchelementwerten oder Variablenwerten) im Dokument-Fragment.


#### Forms Manager {#forms-manager-2}

* XML-Schema-Eigenschaften von Adaptive Forms können nach Anwendung von CFP6 auf AEM 6.2 nicht bearbeitet werden. Hotfix für CQ-4219684
* Alle Dienste des AEM Forms Manager-Kernpakets werden beim Neustart des Servers nicht gestartet. Hotfix für CQ-4217014

### Forms JEE-Installationsprogramm {#forms-jee-installer-12}

#### Installieren von LCM {#install-lcm-2}

* Auf dem Bildschirm &quot;Administrator&quot;unter Microsoft Windows wird die Versionsnummer 6.0 nach der Installation von CFP6 angezeigt. Hotfix für CQ-4217573

## Enthaltene Feature Packs {#feature-packs-included-2}

* Verbesserungen an TouchUI-Schaltflächen in der Desktop-App. NPR-18676

## OSGi-Pakete im CFP8 {#osgi-bundles-included-in-cfp}

Liste von OSGi-Bundles aktualisiert in AEM 6.2SP1-CFP8

[Datei laden](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Liste der in AEM 6.2SP1-CFP8 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Verhaltensänderung bei der Anzeige von Titeln auf der Grafikkarte für das Bild mit dc: title-Eigenschaft auf String [] (multifield) eingestellt.
* Fehlerbehebungen in Leistungsproblem mit Dynamic Media-Cloud Services, Touch-Benutzeroberfläche und Benutzeroberfläche für Sicherheit.
* Fehlerbehebungen in Apache Felix HTTP Bridge 3.0.8
* Binärlose Replikation (BLR) zwischen Autor- und Veröffentlichungs-Umgebung wurde behoben.
* Unterstützung für die Bibliotheksdatei der Zielgruppe, AT.JS, eine Implementierungsbibliothek zur clientseitigen Integration mit Adobe Target, die sowohl für typische Webimplementierungen als auch für Einzelseitenanwendungen entwickelt wurde.
* Verbesserte AEM durch Einführung benutzerdefinierbarer Zeitlimits für die Verbindung mit Marketing Cloud-Lösungen (Analytics, DTM, Zielgruppe und S&amp;P).

### Assets {#assets-12}

* Beim Testen der Videoaufnahme mit AEM 6.3, die mit Dynamic Media-Cloud Services konfiguriert wurden, wird die Ausnahme &quot;Zu viele geöffnete Dateien&quot;ausgelöst. NPR-18734; Hotfix für CQ-4211407
* Die Einstellung für die Vanity-URL für Assets auf einer Seite funktioniert nicht, nachdem die AEM Instanz neu gestartet wurde. NPR-18634; Hotfix für Granite-18085
* In TouchUI wird die Schaltfläche &quot;Veröffentlichen&quot;für Benutzer ohne Berechtigung zum Veröffentlichen von Assets angezeigt. NPR-18620; Hotfix für CQ-4214042
* Die Option &quot;Dynamische Darstellung&quot;ist nicht im Dialogfeld &quot;Herunterladen&quot;für ein Asset vorhanden, nachdem die Lizenzvereinbarung für dieses Element festgelegt wurde. NPR-18607; Hotfix für CQ-4212342
* Dynamische Ausgaben können nicht für Assets heruntergeladen werden, die Leerzeichen in ihren Namen enthalten. NPR-18571; Hotfix für CQ-4211738
* Es können nicht mehr als ein Benutzer gespeichert werden, wenn der Asset-Ordner für Creative Cloud freigegeben wird. NPR-18489; Hotfix für CQ-103297
* dc: title &amp; dc: Beschreibung ändert sich nicht in einen Wert für mehrere Felder in crx/de. NPR-18474; Hotfix für CQ-4209086
* Der Vorgang zum Verschieben von Assets führt zu einer Leistungsbeeinträchtigung. NPR-18346
* In der Zeitleiste werden keine Elemente angezeigt, wenn die Standardoption &quot;Alle anzeigen&quot;aktiviert ist. NPR-18302; Hotfix für CQ-4211957
* Ein Fehler tritt auf, wenn eine ASCII/UTF-8-kodierte Textdatei in AEM Assets hochgeladen wird und die Erstellung von Miniaturbildern fehlschlägt. NPR-18006: CFP für CQ-4209345
* Schaltflächen für Veröffentlichungsaktionen sind auch dann sichtbar, wenn der Benutzer nicht über den Replikationszugriff verfügt. NPR-17353; Hotfix für CQ-4209269
* Sowohl SiteAdmin als auch Miscadmin funktionieren nicht, wenn die Minimierung mit min:gcc;obfuscate=true aktiviert ist. NPR-18593; Hotfix für CQ-4209220
* Benutzerdefinierte Menüelemente werden erst angezeigt, wenn der Bildschirm jedes Mal aktualisiert wird. NPR-18500; Hotfix für CQ-4213581
* Aktualisieren Sie moment.js auf 2.10.6. NPR-18596; Hotfix für Granite-11881
* Das Anwenden von Berechtigungen für DM-Makros bricht die Ansicht für Admin-Benutzer. NPR-18544; Hotfix für CQ-4211729
* Später veröffentlichen für Assets wird eine ungültige ArgumentException ausgelöst. CQ-4214532

### Sites {#sites-12}

* Auf einem Active-Active-Authoring-Cluster mit MongoDB versuchen beide Autoren, die Replikation für denselben Trigger auszuführen, wenn die Zeitdauer für den Inhalt auf die für ihn festgelegte Zeitdauer eingestellt ist. NPR-18708; Hotfix für CQ-4210982
* NPE beim Verschieben einer Ressource mit einem Verweis ohne jcr: content-Knoten. NPR-18664
* Platzhalter sind nicht auf einer Seite sichtbar, die mehrere parsys-Komponenten enthält. NPR-18645; Hotfix für CQ-110253
* Probleme mit der Gleichzeitigkeit in AbstractCopyMoveCommand. NPR-18591
* Wenn Text aus einer anderen AEM in eine parsys-Komponente kopiert wird, werden die Parameter ohne einen resourceType-Satz erstellt. NPR-18511; Hotfix für CQ-4212306

### Plattform {#platform-10}

* JCR Installer aktualisiert keine Bundle-Version nach der Paketinstallation. NPR-18728; Hotfix für NPR-15135
* Die Binaryless-Replikation (BLR) schlägt mit Binärdateien b/w Autor- und Veröffentlichungs-Umgebung fehl. NPR-18704
* Apache Felix Http Bridge-Auflösungsanforderung in AEM Umgebung. NPR-18297
* Die Replikation schlägt fehl, wenn mehrere Seiten mit ähnlicher Struktur gleichzeitig mit der Sling Content Distribution repliziert werden. NPR-18665; Hotfix für Granite-13712
* Sling Distribution Pakete aufbauen und nicht selbst gereinigt. NPR-18601; Hotfix für Granite-16183

### Integrationen {#integration-13}

* Die Anzeige von Angeboten, die aus Bibliotheksordnern veröffentlicht wurden, führt zu NPE. NPR-18732; Hotfix für CQ-4214593
* Das Beginns-/Enddatum einer Aktivität wird in JCR und Zielgruppe nicht aktualisiert, wenn von einem bestimmten Datum zu &quot;Bei Aktivierung/Deaktivierung&quot;geändert wird. NPR-18612; Hotfix für CQ-104831
* Für die Analytics-Integration mit AEM wurden keine Verbindungs- oder Socket-Timeouts für die HTTPClient-Verbindungen festgelegt. NPR-18497
* Für die DTM-Integration mit AEM sind keine Verbindungs- oder Socket-Timeouts für die HTTPClient-Verbindungen festgelegt. NPR-18495
* Für die Zielgruppe-Integration mit AEM wurden keine Verbindungs- oder Socket-Timeouts für die HTTPClient-Verbindungen festgelegt. NPR-18494
* Für die Search &amp; Promote-Integration mit AEM wurden keine Verbindungs- oder Socket-Timeouts für die HTTPClient-Verbindungen festgelegt. NPR-18493
* Target-Aktivität wird deaktiviert, nachdem ein zusätzliches Erlebnis hinzugefügt wurde. NPR-18227; Hotfix für CQ-4201895

### WCM – Foundation-Komponenten {#wcm-foundation-components-7}

* Bei Imagemaps werden ausgewählte Koordinaten in der HTML-Bildkomponente nicht beibehalten. NPR-18530; Hotfix für CQ-4211584

### Übersetzung {#translation-5}

* In Ergebnissen einer Übersetzungssuche sind keine Namen von Übersetzungsprojekten enthalten. NPR-18224; Hotfix für CQ-4210658

### Markenportal {#brand-portal-1}

* Ermöglicht die Veröffentlichung von Tags von AEM im Brand Portal über die Tagadmin/Tagging-Konsole. CQ-4212165

## Formulare {#forms-13}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-13}

#### Korrespondenzverwaltung {#correspondence-management-6}

* Die korrekten Daten werden erst dann im Bearbeitungsbereich angezeigt, wenn das Fragment gespeichert wurde. NPR-19092
* Das Hinzufügen von Dokument-Fragmenten zu einem Brief nimmt viel Zeit in Anspruch. NPR-18958
* Wenn in einer XML-Datendatei eine XML-Deklaration vorhanden ist und per POST-Anforderung eine Briefausgabe veranlasst wird, werden die Daten im zugehörigen Brief nicht angezeigt. NPR-18870
* Für Aktionen, die an CM-Assets vorgenommen werden, werden keine Prüfprotokolle generiert. NPR-16618

>[!NOTE]
>
>Installieren Sie dieses CFP-Hinzufügen-On-Paket nicht, wenn die folgenden zwei Probleme auftreten:
>
>* &quot;Einfügen aus Word/Web in CM Text Editor kopieren&quot;zeigt Zeilenumbruchinhalte an. NPR-19530
>* Inhalt ohne Zeilenumbruch im CM-Texteditor wird nicht umgebrochen. NPR-19449

>
>
Diese werden in der künftigen GFP behandelt.

#### Adaptive Formulare {#adaptive-forms-9}

* Beim Hinzufügen eines neuen Bereichs für wiederholbare Bereiche wird der Wert des Dropdown-Felds im vorherigen Bedienfeld gelöscht. NPR-18772
* Adaptive Formularfelder, die als Ganzzahlen markiert sind, akzeptieren auch einige Sonderzeichen aus dem numerischen Pad. NPR-18680
* Skript zum Ändern des Schaltflächentitels beim initialize-Ereignis des guideroot-Bedienfelds funktioniert nicht. NPR-18476
* Die Bildlaufleiste wird für Regeln, die im Regeleditor erstellt wurden, im rechten Bereich nicht angezeigt. NPR-18716

#### AEM Forms-App {#aem-forms-app}

* Forms wird in der AEM Forms-App nicht korrekt dargestellt, wenn es sich im Offlinemodus befindet oder nicht mit dem Netzwerk verbunden ist. CQ-4218368

### Forms JEE-Installationsprogramm  {#forms-jee-installer-13}

#### PDFG-Dienst {#pdfg-service-3}

* PDF Generator kann keine PDF-Dokumente mit bestimmten Lesezeichenebenen erstellen. Hotfix für CQ-4211102

## OSGi-Pakete, die in CFP7 {#osgi-bundles-included-in-cfp-1} enthalten sind

Liste von OSGi-Paketen, die in AEM 6.2SP1-CFP7 aktualisiert wurden

[Datei laden](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Liste der in AEM 6.2SP1-CFP7 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Effiziente Verwaltung ausgeblendeter Komponenten im Layoutmodus auf dem Tablet.
* Einführung von Schnellaktionen auf Hybridgeräten.
* Beheben von Synchronisierungsproblemen auf Komponentenebene mit Live-Kopien.

### Assets {#assets-13}

* Der Kunde wird blockiert, wenn ein Benutzer, der nicht über die erforderliche Berechtigung verfügt, versucht, den Vorgang für ein Asset zu verschieben. NPR-18330; Hotfix für CQ-4212560
* Das Zusammenführen mehrerer Konfigurationen für intelligente Inhaltsdienste führt zu einem Benutzerfreundlichkeits-Problem. NPR-18273; Hotfix für CQ-4201557
* Kassengang-Aktion/Workflows sind in der Timeline-Konsole nicht einmal ca. Im Ordner &quot;Assets&quot;werden 80 Fragmente hinzugefügt. NPR-18257; Hotfix für CQ-4211214 und NPR-18251; Hotfix für CQ-4211216.
* Das System stürzt bei Ausfall des Speichers ab und es fehlt an Paginierung während der Assets-Berichte. NPR-17865; Hotfix für CQ-4209759
* Das veröffentlichte Video kann nicht auf kodierten Video-Assets wiedergegeben werden. NPR-17849; Hotfix für CQ-4210739
* Miniaturansicht für PDF wird nicht generiert. NPR-17831, NPR-17750; Hotfix für CQ-4210547
* Abgelaufene Assets werden vom Adobe CQ DAM-Ablaufbenachrichtigungsauftrag nicht deaktiviert. NPR-17666; Hotfix für CQ-107766
* Die Aktivitäten zum Ablauf von Assets werden beendet, wenn einem Asset kein Eigentümer zugewiesen ist. NPR-17665; Hotfix für CQ-4197946
* Wenn ein Asset-Ordner mit mehr als 150 eingehenden Referenzen verschoben wird, wird eine Null Pointer-Ausnahme ausgelöst. CQ-4200981

### Sites {#sites-13}

* Die Personalisierung funktioniert nur für die erste IP, wenn die Segmentierungsregel für einen IP-Bereich festgelegt ist. NPR-18121; Hotfix für CQ-83767
* Die Anmeldung schlägt aufgrund von NumberFormatException fehl, wenn die historyShow-Eigenschaft aktiviert ist. NPR-18073; Hotfix für CQ-101965
* Gelöschte Seiten, die als markiert sind, sind in der Touch-Benutzeroberfläche sichtbar. NPR-18025; Hotfix für CQ-86694
* Leistungsprobleme beim Laden einer Seite mit großen (über 2000) Zielgruppen. NPR-17884; Hotfix für CQ-4209567
* Ein Bild kann nicht ausgewählt werden, nachdem ein anderes Bild auf der Seite entfernt wurde. NPR-17711; Hotfix für CQ-4201323

### Plattform {#platform-11}

* Touch-Steuerelemente der Benutzeroberfläche werden nicht für Benutzer ausgeblendet, die nicht über die erforderlichen Berechtigungen verfügen. NPR-17945; Hotfix für CQ-4211231
* Japanische Tags fehlen im Tag-Picker-Feld. NPR-17768; Hotfix für CQ-4210456
* Die getsize()-Abfrage gibt bei Aktivierung von FastQuerySize falsche Ergebnisse zurück. NPR-18018
* Auf die Webkonsole auf der Standby-Instanz kann nicht zugegriffen werden. NPR-17861; Hotfix für Granite-14582

### Commerce {#commerce-2}

* Abfrage-Traversal tritt auf, wenn für den Katalogentwurf keine Bedingung für einen Abschnitt definiert wurde. NPR-18229; Hotfix für CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. verzögert AEM Herunterfahren. NPR-18298; Hotfix für CQ-96133

### Integrationen {#integrations}

* Behebung von Fehlern in der AEM-Suchkomponente, die auftreten können, wenn AEM Day HTTP Client 3.1 OSGI mit einem Proxy konfiguriert ist, für den die Digest-Authentifizierung erforderlich ist. NPR 18128
* Kontrollkästchen fehlen, um Vererbung wiederherzustellen. NPR-17753; Hotfix-Anfrage für CQ-4210139
* Benutzer können die Priorität nicht einrichten, wenn sie eine Komponente mit mehreren Aktivitäten als Ziel auswählen. NPR-18658; Hotfix für CQ-4210727
* Benutzer können nicht im Ordner &quot;/etc/segmentation&quot;nach einer Audience suchen, die im Ordner &quot;/etc/segmentation/group1&quot;erstellt wurde. NPR-18522

### Sicherheit {#security-1}

* Der Assistent zum Verschieben von Assets hängt ab, wenn der Benutzer keine Schreibberechtigung für den Ordner &quot;Zielgruppe&quot;hat. NPR-18300
* Anforderung der Verwendung einer aktualisierten Version von org.apache.sling.servlets.post Servelet (2.3.22) in der Apache Sling API, um eine XSS-Verwundbarkeit zu verhindern. NPR-18963

### Übersetzung {#translation-6}

* Die Asset-Seite darf erst nach Abschluss des Projekts erneut an ein Übersetzungsprojekt gesendet werden. NPR-18249; Hotfix für CQ-4209908

### WCM – Foundation-Komponenten {#wcm-foundation-components-8}

* Die iparsys-Komponente der WCM Foundation kann nicht in editierbaren Vorlagen verwendet werden. NPR-18223; Hotfix für CQ-4210384
* Die ausgewählten Koordinaten in der HTML-Bildkomponente werden in der Imagemap nicht beibehalten. NPR-18032; Hotfix für CQ-4211584
* Wenn eine HTML-Bildkomponente gerendert wird, wird der Dateiname in der URL umbenannt, wodurch die URL beschädigt wird. NPR-17908; Hotfix für CQ-4211587
* Die Seiteneigenschaften können nicht mehr verlassen werden, nachdem Änderungen vorgenommen wurden. NPR-17832; Hotfix für CQ-96110

## Formulare {#forms-14}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms Releases](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-14}

**Korrespondenzverwaltung**

* Das Datenwörterbuch wird beim Rendern von Briefen wiederholt gelesen. NPR-18482, Hotfix für CQ-4210805
* JavaDocs für die Klasse com.adobe.livecycle.content hinzugefügt. NPR-18467
* Beim Erstellen eines Briefs wird die Beschreibung des Briefs nicht gespeichert. NPR-18039
* Wenn ein Textmodul gespeichert wird und ein Ausdruck im Textmodul keine öffnenden oder schließenden Ausdrucks-Tags enthält, wird keine Fehlermeldung angezeigt. Das Textmodul zeigt eine Fehlermeldung an und Rendering im Brief funktioniert nicht. NPR-17798
* Unerwartete Fehler in Protokollen zur Installation des Add-On-Pakets. NPR-18295

**Forms Manager**

* In der Benutzeroberfläche von AEM Forms werden die Assets beginnend mit dem ältesten aufgelistet. Benutzer können die Sortierreihenfolge nicht so ändern, dass mit dem neuesten Asset begonnen wird. NPR-18451

### Forms JEE-Installationsprogramm  {#forms-jee-installer-14}

**Output-Dienst**

* Verbesserte Leistungsprobleme des Output-Dienstes für AEM Forms 6.2. NPR-18033

**Dienst für Unterschriften**

* PDF-Dokumente können nicht mit dem Remote-Hardware-Sicherheitsmodul signiert werden. NPR-18017

## OSGi-Pakete im CFP6 {#osgi-bundles-included-in-cfp-2}

Liste von OSGi-Paketen, die in AEM 6.2SP1-CFP6 aktualisiert wurden

[Datei laden](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Liste der in AEM 6.2SP1-CFP6 aktualisierten Inhaltspakete

[Datei laden](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Es wurden mehrere Probleme mit der Benutzeroberfläche beim Freigeben, Verschieben, Veröffentlichen und Herunterladen von Assets behoben.
* Verbesserte Kapazität des Dialogfelds &quot;Verschieben&quot;bei der Anzeige referenzierter Assets.
* Es wurden mehrere Probleme mit WCM-Komponenten und Workflows behoben, z. B. &quot;Rückgängig&quot;und &quot;Bereinigen der Version&quot;.
* Verbesserte Reaktionsfähigkeit der Aktionsleiste in Bezug auf die Anzeige von Symbolleistenaktionen und Korallenkomponenten.

### Assets {#assets-14}

* Leistungsverbesserungen bei der Funktion &quot;Im Markenportal veröffentlichen&quot;. NPR-17189; Hotfix für CQ-4204150
* Wenn Sie ein Asset mit der Option &quot;Link freigeben&quot;freigeben, wird keine ZIP-Datei mit einer flachen Ordnerstruktur zum Herunterladen erstellt. NPR-17513; Hotfix für CQ-4209381
* Wenn Sie ein Asset in DAM auswählen und auf &quot;Veröffentlichen&quot;klicken, wird die Option &quot;Im Markenportal veröffentlichen&quot;auf der Seite &quot;Asset-Details&quot;nicht angezeigt. NPR-17351; Hotfix für CQ-94905
* In DAM-Workflow-Schritten müssen Binärstreams, die von Session oder ResourceResolver erfasst werden, in einem endgültigen Block geschlossen werden, um sicherzustellen, dass keine Ressourcenlecks auftreten. NPR-17385; Hotfix für CQ-4209452
* Das Hochladen eines Word-Dokuments in DAM führt zu einer Null-Zeiger-Ausnahme und die Workflow-Instanz bleibt im Status &quot;Wird ausgeführt&quot;hängen. NPR-17160; Hotfix für CQ-4207358
* Die Schaltflächen &quot;Freigeben&quot;, &quot;Verschieben&quot;, &quot;Veröffentlichen&quot;und &quot;Herunterladen&quot;sind für abgelaufene Assets auf der Seite &quot;Metadaten-Editor&quot;für Benutzer ohne Administratorrechte sichtbar. NPR-16903; Hotfix für CQ-101440/CQ-104535
* Aktionen wie &quot;Freigeben&quot;, &quot;Verschieben&quot;, &quot;Veröffentlichen&quot;und &quot;Kopieren&quot;sollten für Administratoren in der Assets-Konsole sichtbar sein. NPR-16902; Hotfix für CQ-4207111

### Sites {#sites-14}

* Beim Verschieben einer Seite mithilfe der Benutzeroberfläche &quot;Klassisch&quot;und &quot;Touch&quot;werden im Dialogfeld &quot;Verschieben&quot;keine Verweise über 150 angezeigt, sodass Benutzer diese Verweise nicht aktualisieren und die Seite erneut veröffentlichen können. Dieses Problem wurde behoben, indem eine Eigenschaft für die klassische Benutzeroberfläche eingeführt wurde: &#39;maxRefNo&#39;, das auf dem Siteadmin-Knoten konfiguriert werden kann: &#39;/libs/wcm/core/content/siteadmin&#39;. Diese Eigenschaft gibt die maximale Anzahl von Verweisen (Standardwert 150) an, die vor einem Vorgang mit starkem Verschieben angezeigt werden. Wenn eine Seite mehr Verweise enthält, werden diese nicht im Dialogfeld movePage angezeigt. Diese Konfiguration funktioniert auch für &quot;damadmin&quot;und &quot;miscadmin&quot;durch Anwendung der Konfiguration auf den Knoten: `'/libs/wcm/core/content/damadmin'` und `'/libs/wcm/core/content/miscadmin'`. NPR-17222; Hotfix für CQ-85878

* Beim Arbeiten mit WCM-Komponenten werden Hyperlinks mit Leerzeichen im Touch UI Rich Text Editor entfernt. NPR-17698, NPR-17570; Hotfix für CQ-4206768
* Beim Auslösen des Arbeitsablaufs zum Rückgängigmachen der Veröffentlichung aus den Seiteneigenschaften werden für Benutzer ohne Replizierungsrechte JavaScript-Fehler angezeigt. NPR-17294; Hotfix für CQ-102064
* Beim Rendern oder Exportieren einer HTML-Bildkomponente wird die URL in eine Zahl geändert, wobei der Dateiname umbenannt wird, wodurch fehlerhafte Links entstehen. NPR-17245; Hotfix für CQ-59616
* Wenn Sie einen Launch in einem verschachtelten Launch löschen, sind die Sub-Launches verwaist. NPR-17228; Hotfix für CQ-4202639
* Die Ausführung von Version Purge in AEM 6.2 mit Oak 1.4.13 führt zu einer ständig wiederholten Warnung in den Protokollen. NPR-17391; Hotfix für CQ-4206870
* Nach der Installation eines Hotfixes oder einer Aktualisierung für die ContextHub-Komponente überschreibt das Inhaltspaket alle Segmente in /etc/segmentation/contexthub, wodurch alle benutzerdefinierten ContextHub-Segmente verloren gehen. NPR-17250; Hotfix für CQ-79958
* Beim Ausführen eines Workflows mit verschachtelten Gruppen als Workflow-Benutzer führt der WorkflowStatusProvider (pageinfo.json) zu einer Sperrung der Workflow-Instanz. NPR-17555; Hotfix für CQ-4202056
* Bei Verwendung der WCM-Seiten-Editor-Komponenten ist am Ende der Seite im Touch-UI-Bearbeitungsmodus der Autoreninstanz ein riesiger Leerraum vorhanden. NPR-17510; Hotfix für CQ-4205441
* Beim Rendern oder Exportieren einer HTML-Bildkomponente wird die URL in eine Zahl geändert, wodurch fehlerhafte Links entstehen. NPR-17245; Hotfix für CQ-59616

### Benutzeroberfläche {#ui}

* Wenn Sie ein Asset auswählen und auf &quot;Developer Tools&quot;klicken, werden die Symbolleistenaktionen in der Aktionsleiste nicht immer in langsamen Verbindungen angezeigt und die Seite muss neu geladen werden. NPR-17568; Hotfix für CQ-108365
* Die Aktionsleiste sollte aktualisiert werden, um zwei Container zu verwenden: coral-actionbar-primary und coral-actionbar-secondary, anstelle des coral-actionbar-Containers. NPR-17591; Hotfix für GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Benutzer mit der Berechtigung &quot;Schreibgeschützt&quot;für die AEM Mobile-App können keine Inhalte von der AEM Mobile-Content-Management-Seite aus Vorschau werden. NPR-17390; Hotfix für CQ-4209690

### Sicherheit {#security-2}

* XSS-Verwundbarkeit in der Ausgabe, die von HTMLRendererServlet generiert wurde. NPR-17136
* Anforderung, die Offenlegung AEM Version in AEM Web Syndication Feeds-Seite zu verhindern. NPR-16219

### Formulare {#forms-15}

#### Forms-Add-on-Paket {#forms-add-on-package-15}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter AEM Forms-Versionen.

**Adaptive Formulare**

* Bei adaptiven Formularen mit Anlagen werden Duplikat-Einträge für die afSubmissionInfo-Tags in der gesendeten XML erstellt, wenn das Formular zum zweiten Mal gesendet wird. NPR-17364
* Bei Verwendung des Google Chrome-Browsers wird nach dem Entfernen einer Anlage aus einem Formular ein Fehler ausgegeben, wenn versucht wird, dieselbe Anlage erneut anzuhängen. NPR-17297
* Bei verschachtelten, wiederholbaren verzögert geladenen Bereichen im adaptiven Forms, das auf XSD-basierten oder auf dem Nicht-Formularmodell basiert, werden die im Formular eingegebenen Werte im Dokument des Datensatzes (DOR) nicht beibehalten. NPR-17176
* Fehler, die im Fehlerprotokoll für den Regeleditor angezeigt werden, sollten im catch-Block eines try/catch-Blocks JavaScript-Code hinzugefügt werden. NPR-16757
* Wenn Sie auf eine Dateianlage in einem Formular klicken, wird ein Browser-Konsolenfehler ausgegeben und die Vorschau des Anhangs wird nicht angezeigt. NPR-17174

**Korrespondenzverwaltung**

* Die Funktion &quot;Korrespondenz erstellen&quot;bricht bei Inline-Text oder einer leeren Zeile in der Benutzeroberfläche um. NPR-17748
* Der Browser flimmert, wenn ein Brief zur Bearbeitung geöffnet wird. NPR-17576
* Wenn Remote-Funktionen in berechneten Datenwörterbuchelementen hinzugefügt werden, wird die Bildlaufleiste nicht auf der Registerkarte angezeigt, wenn die Anzahl der Funktionen größer ist als die Länge der Registerkarte mit Remote-Funktionen. NPR-17359
* Die API-Methode import com.adobe.icc.services.api.LetterInstanceService funktioniert nicht. NPR-17922, NPR-16008
* Eine in einem Textmodul hinzugefügte Variable ist beim Bearbeiten eines Briefs im Bedienfeld &quot;Datenbindung&quot;nicht sichtbar. NPR-17940
* Die Correspondence Management-Benutzeroberfläche wird nicht gestartet, wenn die HTML-Übermittlungsaktion die POST verwendet. NPR-17595

**Forms Manager**

* Bei einem für AB-Tests konfigurierten adaptiven Formular wird der Test durch Klicken auf Beginn AB-Test nicht Beginn und es wird ein Fehler in der Browserkonsole ausgegeben. NPR-17838

**Formularservice**

* Die in der Analyse für statischen Code von OSGI-Formularen gemeldeten Probleme sollten behoben werden. NPR-13951

#### Forms JEE-Installationsprogramm {#forms-jee-installer-15}

**Output-Dienst**

* Die Verwendung von AEM Forms 6.2 Output Service zum Zusammenführen eines bestimmten Formulars mit einer Daten-XML dauert 20 Mal länger als die Zeit, die LiveCycle ES4 SP1 für denselben Vorgang benötigt. Es wurde auf Windows- und Linux-Umgebung behoben. NPR-17501

**Installieren von LCM**

* Nach der Installation von AEM Forms 6.2 GM Build und der Anwendung der AEM 6.2 CFP zeigt LiveCycle Configuration Manager ein unerwünschtes Semikolon in den Versionsinformationen an und das Installationsdatum des Patches wird nicht aktualisiert. NPR-14322

**Prozessverwaltung**

* Die TaskContext-Variable wird für AEM Forms-Prozesse nicht gefüllt. CQ-4211857

#### AEM Forms JEE Bundles Package {#aem-forms-jee-bundles-package}

* Die Funktionen von Formularbenutzern sollten identisch sein, unabhängig davon, ob die JEE Admin UI Console oder die OSGi-Konsole verwendet werden. NPR-17670

### Feature Packs in CFP5 {#feature-packs-included-in-cfp}

**Forms JEE-Paket**

Process Management - HTML Workspace

* Beim Zuweisen eines Arbeitsbereichsschritts sollte auf der Registerkarte &quot;Arbeitsbereichsanlagen&quot;ein Zähler für die Anlagen oder Hinweise angezeigt werden, falls mehrere Anlagen oder Notizen vorhanden sind. NPR-17771
* Anfrage zur Unterstützung von Office 365 in AEM JEE Forms für E-Mail-Funktionen im Formular-Workflow. NPR-13866

**Forms Hinzufügen-On-Paket**

Korrespondenzverwaltung

* Beim Bearbeiten von Fragmenten im Texteditor während einer Vorschau des Briefs sollte der verarbeitete Text anstelle der Inline-Bedingungen in Fragmenten zur Bearbeitung angezeigt werden. NPR-15748, NPR-17504

### OSGi-Pakete im CFP5 {#osgi-bundles-included-in-cfp-3}

Liste von OSGi-Paketen, die zwischen AEM6.2 SP1 und CFP5 aktualisiert wurden

[Datei laden](assets/do-not-localize/cfp5_osgi_bundles.txt)

Liste von Inhaltspaketen, die zwischen AEM6.2 SP1 und CFP5 aktualisiert wurden

[Datei laden](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 ist ein wichtiges Update, das wichtige Fehlerbehebungen enthält, die seit der allgemeinen Verfügbarkeit von AEM 6.2 SP1 veröffentlicht wurden.

Die wichtigsten Highlights dieses Kumulative Fix Pack sind:

* Fehlerbehebungen in Assets für die Camera Raw-Dateiwiedergabe, die Ansicht der Zeitleiste und die Bildausrichtung
* Verbesserung der

   * WCM startet für Sites
   * Projektarbeitsablauf
   * ContextHub-Komponenten

* Fehlerbehebungen für Kampagne, Mobile On-Demand und Übersetzung
* Verbesserungen der Benutzerfreundlichkeit im Regeleditor für adaptive Formulare
* Erweiterter Inline-Bedingungseditor für Correspondence Management in Formularen
* Fehlerbehebungen für Process Management und Output Service für AEM Forms on JEE
* Fehlerbehebung für Forms Designer im Skript-Editor

### Plattform {#platform-12}

* Das Suchformular ignoriert die Einstellung `environment`, wenn der Cloud-Dienst konfiguriert ist, sodass sie auf der Autoreninstanz nicht mehr verwendet werden kann. NPR-16594: Hotfix für CQ-4206076
* Das Hinzufügen oder Anpassen von Spalten zu den Ergebnissen von OmniSearch **durch Überlagerung in /apps funktioniert nicht.** NPR-16737: Hotfix für CQ-4206785
* Die **Diagnosewerkzeug **Seite funktioniert nach einem ersetzenden Upgrade von AEM 6.1 SP2 auf AEM 6.2 SP1 nicht. NPR-17121; Hotfix für CQ-4196786
* HTL: Wenn Sie ein Forum auswählen und ein Thema und einen Beitrag erstellen, fügt die `Sightly SightlyCompiledScript`-Eigenschaft `addSelectors` der `RequestDispatcherOption`-Eigenschaft falsche hinzu. NPR-17008: Hotfix für GRANITE-16384

* Unterstützung für `CRON expressions` in `ManagedPollConfigs` hinzugefügt, die von `ReportImporter` verwendet wird. NPR-16608: Hotfix-Anfrage für GRANITE-4206066

* Das Hochladen eines Avatarbilds für einen LDAP-Benutzer schlägt fehl. NPR-16561; Hotfix für Granite-17013
* Die Anzahl der im Bildschirm &quot;Benutzerverwaltung&quot;angezeigten Ergebnisse unterscheidet sich in der Ansicht &quot;Karte&quot;und &quot;Liste&quot;. NPR-16241; Hotfix für GRANITE-16914
* Arbeitsablaufbenachrichtigungen werden beim Anzeigen im Google Chrome-Browser im Vollbildmodus nicht verzögert geladen. NPR-17013: Hotfix für CQ-4207567

### Assets {#assets-15}

* Die Bildausrichtung wird beim Importieren eines Bildes mit einer definierten Ausrichtung nicht korrekt angewendet. NPR-16750: Hotfix für CQ-4204356
* In der Ansicht &quot;Asset-Zeitschiene&quot;werden keine Assets angezeigt, obwohl &quot;Alle anzeigen&quot;standardmäßig eingestellt ist. NPR-16957: Hotfix für CQ-98780
* Dateien mit Rohdaten (einschließlich ARW, CR2, NEF, DNG und EPS) können nicht ausgewählt oder gelöscht werden, wenn sie als Darstellung in Assets hinzugefügt werden. Solche Dateien werden automatisch heruntergeladen, wenn der Benutzer darauf klickt. NPR-16949: Hotfix für CQ-4206846
* Beim Erstellen einer PDF-Datei in einer anderen PDF-Datei in der Benutzeroberfläche &quot;Assets&quot;werden die erstellten PDF-Dateien in der DAM-Benutzeroberfläche nicht angezeigt, obwohl sie im CRX-Repository sichtbar sind. NPR-16833: Hotfix für CQ-4206501
* Das Hochladen eines Assets als direkt untergeordneter Knoten mit der Touch-optimierten Benutzeroberfläche verursacht ein Problem. Das Asset wird als direkt untergeordnetes Element des zuvor ausgewählten Assets hochgeladen. NPR-16534: Hotfix für CQ-4204287
* In der DAM-Benutzeroberfläche wird beim Kommentieren eines Assets und beim Taggen eines Benutzers im Kommentar keine E-Mail-Benachrichtigung generiert. NPR-16589: Hotfix für CQ-102318

### Projekte {#projects-3}

Die Projekt-Workflow-Konsole zeigt eine NullPointerException auf der Seite an, wenn Workflows bereinigt werden. NPR-17017: Hotfix für CQ-4194269

### Sites {#sites-15}

* Dateien im Ordner `ContextHub` werden auf der Autoreninstanz nicht minimiert. NPR-17022: Hotfix für CQ-79456
* Die Startwerbung von WCM-Starts benötigt lange Zeit, um einen Start zu bewerben, der aus einem großen Baum einer Seite besteht. NPR-16480: Hotfix für CQ-82731
* `ClientContext` Segmentbedingungs-Renderer stürzt ab, wenn ein Segment (oder eine Audience) mit einer nicht funktionierenden oder unfertigen Regel erstellt wird. NPR-16759: Hotfix für CQ-4205104
* Bei WCM-Launches wird die Veröffentlichung von Seiten, die mit einem Launch verknüpft sind, nicht rückgängig gemacht, wenn die Aktion von den Seiteneigenschaften in der Touch-Benutzeroberfläche aus initiiert wird. NPR-16560: Hotfix für CQ-4204681
* Link Rewriter schreibt fälschlicherweise href-Werte, die einen Doppelpunkt enthalten, um anzunehmen, dass der Doppelpunkt &quot;:&quot;einen JCR-Namensraum definiert. NPR-16753: Hotfix für CQ-4203762
* In WCM-Design Importer führt das Öffnen einer Testimportseite und das Hochladen einer ZIP-Datei zu Problemen, wenn diese zuvor hochgeladen und gelöscht wurde. NPR-16486: Hotfix für CQ-90962
* Die Navigation zum Bereich **[!UICONTROL Globale Navigation]** mit den Browsern Firefox Safari und Google Chrome bietet eine andere Benutzererfahrung. Der Firefox-Browser zeigt das Menü **[!UICONTROL Tools]** an, während der Google Chrome-Browser das Menü **[!UICONTROL Navigation]** anzeigt. NPR-16770; Hotfix für CQ-4200456

### Campaign {#campaign}

* Während Sie AEM Kampagnenvorlagen testen und Testadressen ändern, um &quot;Zusätzliche Daten&quot;einzuschließen, wird die Dropdown-Liste &quot;Adobe Campaign&quot;im Touch UI Context Hub ausgeblendet. NPR-16771: Hotfix für CQ-105748

### Mobile On-Demand {#mobile-on-demand-3}

* Beim Preflight einer Veröffentlichung aus der Umgebung des AEM Autors verursacht eine Preflight-Aktion, die länger als 5 Sekunden dauert, eine ungewöhnliche Spitze des AEMM - AEM PECS Integration-Splunk-Dashboards mit einer hohen Anzahl von Statusanforderungen pro Sekunde. NPR-16908: Hotfix für CQ-4207055
* Das AEM Mobile-Konfigurationsmanagement schlägt nach der Installation des Updates AEM-6.2-SP1-CFP1-1.0 fehl. NPR-16909: Hotfix für CQ-4204892

### Übersetzung {#translation-7}

* Die Vorschau von Übersetzungsaufträgen funktioniert nach der Installation von 6.2 SP1 - CFP1 nicht. NPR-16481; Hotfix für CQ-4204655
* Die Sprachkopie, die mithilfe von Übersetzungspunkten erstellt wurde, wird auf &quot;Stammordner&quot;statt auf &quot;Lebenszyklus&quot;des jeweiligen Landes Übergeordnet. NPR-17257; Hotfix für CQ-4208287

### Sicherheit {#security-3}

* Wenn Binärdateien von Dateien in AEM hochgeladen werden, wird keine MIME-Typüberprüfung durchgeführt. NPR-16617
* Probleme beim Hochladen von Avatar-Bildern für LDAP-Benutzer. NPR-16561

### Formulare {#forms-16}

#### Forms-Add-on-Paket {#forms-add-on-package-16}

**Adaptive Formulare**

* Im adaptiven Forms Editor sollte der Kommentar &quot;Zielgruppe-Einstellung&quot;in head.jsp durch die neue Context Hub-Anweisung ersetzt werden. NPR-17173
* Im Regeleditor für adaptive Forms-Regeln zeigt **[!UICONTROL Element auswählen]** das Ereignis als &#39;null&#39; an. NPR-17139
* Das gesendete Formular wird erneut gesendet, wenn Sie mit dem Pfeil nach vorn navigieren (>). NPR-17080
* Beim Senden eines adaptiven Formulars über AJAX wird die Rückruffunktion &quot;error&quot;im Falle eines Fehlers nie aufgerufen. NPR-17034
* Wenn Sie im Regeleditor zur Laufzeit auf die Schaltfläche **[!UICONTROL Formular speichern]** klicken, wird das Formular nicht gespeichert. NPR-16905
* Statischer Text sollte von der Tab-Reihenfolge im adaptiven Formular ausgeschlossen werden. NPR-16749
* Der berechnete Wert eines Dezimalfeldes wird nicht korrekt angezeigt. NPR-16596
* Das Symbol zum Anzeigen des Hilfeinhalts sollte in der Tab-Reihenfolge in adaptiven Formularen enthalten sein. NPR-16484
* Unterstützung für die Verwendung von regulärem Ausdruck des Typs `dataRef=C:/Users/`in der &#39; **[!UICONTROL Standardkonfiguration für Vorausfüllung]**&#39; zum Vorausfüllen von Daten für das adaptive Forms. NPR-16425

* Überprüfungen werden nicht korrekt für alle Bereiche ausgelöst, wenn ein verschachteltes verzögertes Laden-Szenario vorliegt. NPR-15821

**Korrespondenzverwaltung**

* Die Darstellung von Briefen schlägt fehl, wenn ein Brief ein leeres Textmodul enthält (eines ohne Text). NPR-17054
* Zeilenumbrüche und Tabulatorräume werden nach dem Einfügen in den Texteditor aus dem Inhalt entfernt. NPR-17039
* Die Anzeige von Referenzen eines Textmoduls nimmt viel Zeit in Anspruch, wenn auf das Textmodul in vielen Briefen verwiesen wird. NPR-17035
* Das Bearbeiten, Speichern, Löschen und Festlegen von Verweisen für Dokument-Fragmente nimmt viel Zeit in Anspruch. NPR-17033
* Bei der Vorschau des Briefs wird Blocksatz in einer anderen Schrift dargestellt. NPR-16976
* Die Suchfunktion funktioniert nicht ordnungsgemäß, wenn der gesuchte Text mehrmals vorkommt. NPR-16920
* Die Symbolleiste Texteditor wird gelegentlich im Browser angezeigt. NPR-16919
* Das Konstrukt **[!UICONTROL Formular speichern]** im Regeleditor funktioniert nicht. NPR-16905
* Die Dropdown-Liste &quot;Schrift&quot;füllt die Schriftfamilie beim Erstellen eines Textmoduls, das auf einem Datenwörterbuch mit Internet Explorer basiert, nicht. NPR-16944
* Nachdem Sie ein Textfragment erstellt haben, ändert sich die Schriftart des Briefs bei der Vorschau des Briefs. NPR-16830
* Briefe mit Tabulatorzeichen am Anfang oder zwischen Ausdrücken im Dokument-Fragment können nicht gerendert oder in der Vorschau angezeigt werden. NPR-16769

**Mobile Forms**

* Die Vorschau für Mobile Forms zeigt überlappenden Inhalt an, obwohl das Formular für die PDF-Wiedergabe korrekt angezeigt wird. NPR-17105

**Formularportal**

* Durch Klicken auf den Link **[!UICONTROL Download]** für ein gesendetes Formular wird eine HTML-Seite anstelle eines PDF-Formulars geöffnet. NPR-17082

* `Upload Comments` für Dateianlagen nicht in der Benutzeroberfläche für gesendete Instanzen angezeigt werden, obwohl sie in der im CRX-Repository gespeicherten XML vorhanden sind. NPR-17075

**Reader Extensions-Dienst**

* Eine bestimmte Datei ist nicht Reader Extended bei AEM OSGI-Installation von Forms. NPR-16625

#### Forms JEE-Installationsprogramm  {#forms-jee-installer-16}

**Core**

* Während des Aktualisierungsprozesses schlägt Configuration Manager mit einem Timeout fehl. NPR-16774 (Siehe [Konfigurieren des Timeouts für Vorgänge auf Komponentenebene](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Process Management - HTML Workspace**

* Der Startpunkt einer Beginn-Aufgabe beginnt nicht mit den Daten, die zum Zeitpunkt der Übermittlung des Startpunkts gesendet werden. NPR-16917
* Durch Klicken auf die Schaltfläche **[!UICONTROL return]** für ein Formular in HTML Workspace wird das Formular nicht geschlossen, sondern in seine Gruppenwarteschlange zurückgegeben.\
   NPR-16352

**Prozessverwaltung**

* Erlauben Sie Benutzern, den Anzeigenamen früherer Aufgaben auf eine der nächsten Aufgaben in einer Prozessinstanz festzulegen. NPR-15382

**Output-Dienst**

* Der Output-Dienst kann eine PDF-Datei nicht verarbeiten, die geändert wurde, um ein zusätzliches Feld &#39;milli-sec&#39; in die `date-time format`-Metadaten einzuschließen. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer-Skript-Editor entspricht nicht den Standardeinstellungen der Formulareigenschaften für `Calculate Event`und `Validate Event`. NPR-15921

### Feature Packs in CFP4 {#feature-packs-included-in-cfp-1}

**Forms Hinzufügen-On-Paket**

* Verbesserung im Inline-Bedingungseditor für Correspondence Management. NPR-10981

### OSGi-Pakete, die in CFP4 {#osgi-bundles-included-in-cfp-4} enthalten sind

Liste der OSGi-Pakete, die zwischen AEM 6.2 SP1 und CFP4 aktualisiert wurden

Die wichtigsten Highlights der GFP3 sind:

* Effizientere Suchfunktion für die klassische Benutzeroberfläche und für die AEM Suchkomponente mit Proxy mit Digest-Authentifizierung
* Fehlerbehebungen beim Hochladen von Assets und beim Anzeigen von Asset-Metadaten
* Behebt Probleme beim Erstellen von Ordnern und Verschieben von Seiten, wenn der Titel Sonderzeichen enthält.
* Fehlerbehebungen bei der Verwendung von Targeting - Synchronisieren von Audiencen, Veröffentlichen von Kampagnen und Auswählen der Zielmetrik in der Touch-Benutzeroberfläche
* Behebt Synchronisationsprobleme bei Übersetzungsaufträgen
* Bietet erweiterte Sicherheit für den Forms Prefill-Dienst
* Verbesserungen in der Komponente &quot;Formularportalentwürfe und Übermittlungen&quot;und im Barcoded Forms-Dienst
* Verbesserungen der Benutzerfreundlichkeit für adaptive Formulare, die Dateianhangswidgets oder verzögert geladene Fragmente enthalten.
* Verbesserungen der Benutzerfreundlichkeit in Correspondence Management, einschließlich verbesserter Suchfunktion, Protokollierung gelöschter Assets und Import von Datenwörterbüchern.

### Plattform {#platform-13}

* Eine Race-Bedingung in der **ModelAdapterFactory**, die möglich ist, wenn zwei Threads versuchen, dasselbe Feld zu injizieren, führt zu einem Fehler beim Erstellen des Modells. NPR-16443: Hotfix für SLING-6584
* Überprüfungsoption im Paketmanager, um Konflikte zwischen überlagerter Datei (JSP- oder JavaScript-Datei) unter /apps und der Datei, die in einem Hotfix unter /libs enthalten ist, zu erkennen. Betroffene Überlagerungen können dann neu aufgebaut werden, um Änderungen aus der Datei unter /libs einzuschließen. NPR-16216: Hotfix für CQ-81729
* Die Anmeldung bei error.log wird manchmal einige Sekunden nach dem Starten des Herausgebers beendet und muss gelöscht werden, um erneut ausgeführt werden zu können. Anforderung der Aktualisierung des Logging-Frameworks und Bereitstellung der Sling-Protokollierung. NPR-15913: Hotfix für Granite-15452
* Anforderung der Aktualisierung der JavaScript &quot; `use"`-API, um Fehler bei der Implementierung der HTML-JavaScript-Use-API zu vermeiden. NPR-16461: Hotfix für SLING-6780

### Sites {#sites-16}

* Nach dem Upgrade von AEM 6.0 auf AEM 6.2 zeigt die klassische Benutzeroberfläche aufgrund zahlreicher Abfragen eine langsame Performance bei der Suche nach Tags. Um das Problem zu beheben, können die unter [Replizierungsstatus in der Tagging-Konsole (klassische Benutzeroberfläche)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr) beschriebenen Schritte ausgeführt werden. NPR-15842: Hotfix für CQ-4201748.

* Beim Erstellen einer Seite in der Touch-Benutzeroberfläche wird bei der Eingabeprüfung für das Feld &quot;Name&quot;das Sonderzeichen &quot;Apostroph&quot;nicht geprüft (wie in der klassischen Benutzeroberfläche). Daher kann die Seite nicht verschoben werden. NPR-16404: Hotfix für CQ-4205321.
* Wenn Sie zwei Zeilen im Rich-Text-Editor unterschiedliche Stile anwenden und diese dann zusammenführen, wird der Stil entfernt, der auf die zweite Zeile angewendet wird. NPR-16389: Hotfix für CQ-4203835.
* Im Bildschirm &quot;Touch UI Sites&quot;funktioniert der Versuch, eine Seite in eine Seite ohne Unterseiten einzufügen, nicht, da die Schaltfläche Einfügen nicht angezeigt wird. NPR-15894: Hotfix für CQ-4201696.
* Beim Blättern durch die Registerkarte &quot;Seiten&quot;im Inhaltssuchenbedienfeld werden einige Seitensätze in der klassischen Benutzeroberfläche auf unbestimmte Zeit angezeigt, während in der Touch-Benutzeroberfläche nur wenige nicht wiederholende Seiten angezeigt werden. NPR-16271: Hotfix für CQ-4202371
* Wenn Sie die Seiteneigenschaften einer LiveCopy in der Touch-Benutzeroberfläche öffnen und ohne Änderungen auf &quot;Speichern&quot;klicken, werden alle LiveCopy-Registerkarten heruntergeladen und ein LiveSync-Konfigurationsknoten erstellt. NPR-16327: Hotfix für CQ-108562
* Die Formularbeschränkung kann die `ConstraintMessage`-Eigenschaft nicht lesen. NPR-16388: Hotfix für CQ-101330
* Die Komponente `wcm/foundation/components/parsys` zeigt den Platzhalter **[!UICONTROL &quot;Komponenten hierher ziehen]**&quot;nicht an. NPR: 16748: Hotfix für CQ-4205187

### Assets {#assets-16}

* Der PDF-Rasterassistent funktioniert nicht mehr und verursacht Probleme mit dem Arbeitsspeicher nach der Installation von 6.2 SP1 oder Hotfix 12430. NPR-15991
* Die Metadaten für eine Zeichenfolgeneigenschaft `documentNumber` werden als Datum angezeigt, während es sich um eine Zahl handeln sollte. NPR-16134: Hotfix für GRANITE-16916
* Textkürzungen im Timeline-Ereignis-Ballon. NPR-16226: Hotfix für CQ-85226
* Beim Erstellen eines Ordners unter der Inhaltshierarchie mit einem Titel mit Sonderzeichen wird die kodierte Form des Sonderzeichens angezeigt. NPR-15935: Hotfix für CQ-4202987
* Benutzer können keine Assets hochladen oder Ordner erstellen, während sie durch Assets navigieren. Dies ist auf ein inkonsistentes Verhalten zurückzuführen, das bei Verwendung der Schaltfläche &quot;Erstellen&quot;angezeigt wird. NPR-16410: Hotfix für CQ-4204793
* Unerwartete Fehler treten beim Hochladen freigegebener HTML-Ressourcen aus der Ansicht &quot;Artikel&quot;in AEM Authoring auf. NPR-16133: Hotfix für AEMM-4155970

### Integrationen {#integration-14}

* Wenn Sie die Proxyauthentifizierung mit der Digest-Authentifizierung aktivieren, löst die AEM Search-Komponente eine ConcurrentModificationException aus. NPR-15309: Hotfix für CQ-4199191
* Beim Erstellen einer Zielgruppe-A/B-Test-Aktivität in AEM synchronisiert die Audience nicht mit der Zielgruppe und zeigt &quot;Keine Audiencen&quot;an. NPR-16229: Hotfix für CQ-4204210
* Nach der Installation von SP1+NPR-11577 v1.2 wird die Dropdown-Liste der Metriken nie geladen, wenn Sie beim Targeting in der TouchUI die Option &quot;Analytics-Metrik verwenden&quot;für die Zielmetrik auswählen. NPR-16129: Hotfix für CQ-4204316
* Beim Targeting wird bei der Veröffentlichung der Kampagne nicht automatisch der gesamte Baum veröffentlicht, einschließlich Marke und Übergeordnet. NPR-15855: Hotfix für CQ-94630

### Übersetzung {#translation-8}

* Der Synchronisierungsübersetzungsauftrag wird nicht automatisch ausgelöst, und AEM Abfrage erfolgt nicht ohne die Konvertierung der Übersetzungsprojekte. NPR-15163: Hotfix für CQ-90856

### Formulare {#forms-17}

#### Forms-Add-on-Paket {#forms-add-on-package-17}

**Adaptive Formulare**

* Beim Speichern eines adaptiven Formulars mit einer Anlage wird der vollständige Pfad der Anlage im `fileAttachment`-Tag der generierten XML statt dem Namen der Anlage hinzugefügt. NPR-16529
* In XDP-basierten adaptiven Formularen ist der `afData/afBoundData`-Wrapper in der gesendeten XML vorhanden, auch wenn die XML zum Vorausfüllen keine `afData/afBoundData`-Wrapper aufweist. NPR-16118

* Exponentielle Notation im Zahlenfeld: Wenn bei der Verwendung adaptiver Formulare eine Zahl mit einer Dezimalzahl eingegeben wird, die insgesamt mehr als zehn Zeichen umfasst, wird die Zahl in der gesendeten XML in eine exponentielle Notation umgewandelt. NPR-16106
* Bei Formularen, die sowohl eine Dateianlagenkomponente als auch ein verzögert geladenes Fragment enthalten, enthält die XML-Datei für die gesendeten Daten keine Informationen für die Dateianlagenkomponente. NPR-16022
* Bei einem verzögert geladenen wiederholbaren Bedienfeld ohne wiederholbaren Vorgänger können wiederholbare untergeordnete Elemente innerhalb einer zweiten Instanz des Bedienfelds nicht wiederholt werden. NPR-15944
* Wenn Sie versuchen, ein Fragment in einem Fragment im Formulareditor zu speichern, füllt der Fragmentmodellstamm den Wert des untergeordneten Fragments nicht. NPR-15943
* Beim Erstellen eines Kontrollkästchens mit nur einem Element und beim Anzeigen des Kontrollkästchentitels wird bei der Aktion zum Erstellen eines Wörterbuchs ein `ArrayIndexOutOfBoundException` zurückgegeben, wenn der Elementtext leer ist. Das Wörterbuch wird nicht erstellt und es wird keine Fehlerantwort auf dem Bildschirm generiert. NPR-15816
* Bei adaptiven Formularen mit Dateianhang-Widgets werden einige Teile des Formulars deaktiviert, nachdem die angehängte Datei in der Vorschau angezeigt wurde.\
   NPR: 16611

* Bei Dateianhangswidgets, bei denen mehrere Anlagen zulässig sind, wird beim Öffnen der hinzugefügten Anlage anstelle des eigentlichen Inhalts ein Fehlercode angezeigt, wenn eine neue Formularinstanz mit einer Anlage in einem Widget mit einer vorherigen Anlage gesendet wird. NPR-16258
* Sichern des Forms-Vorfülldienstes vor unbefugtem Zugriff durch Protokolle wie `file://`, `http://` und `ftp://`. Siehe &quot; [Konfigurieren des Vorfülldienstes mit Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)&quot;. NPR-15414

* Anforderung der Wiedergabe des adaptiven Formulars im PDF-Format anstelle von HTML im Schritt &quot;Überprüfen&quot;und Anfügen aller Anlagen an die PDF-Datei, damit der Ausdruck das vollständige Formular anzeigt. NPR-9011

**Korrespondenzverwaltung**

* Beim Arbeiten mit Textfragmenten in einem Brief im Vorschau-/Bearbeitungsmodus wird bei der Textkonvertierung in Liste die gesamte Funktionalität des Briefs unterbrochen und ein JavaScript-Fehler erzeugt. NPR-16460
* Das Importieren einer XSD-Datei zum Erstellen eines Datenwörterbuchs im Correspondence Management-Knoten schlägt fehl, wenn der Browser bei jedem Hochladen der XSD-Datei und bei Auswahl des Stammknotens nicht mehr reagiert. Dieses Problem ist Browser-unabhängig und wird nicht in Serverprotokollen angezeigt. NPR-16452
* Während Sie einen Brief mit dem Internet Explorer in der Vorschau anzeigen und versuchen, die Schriftgröße des Inhalts zu bearbeiten, werden die Duplikat-Werte im Dropdown-Menü Schriftgröße zwischen 8 und 72 angezeigt. NPR-16387
* Wenn ein schwebendes Feld als Eingabefeld aus einem XDP-Fragment angezeigt wird, wird das Feld in der Vorschau des Briefs bei Verwendung des Internet Explorer-Browsers nicht erweitert. NPR-16367
* Beim Versuch, einen Brief direkt von der Vorschau zu senden, wird das Popup für den Briefnamen nicht korrekt angezeigt, da er ausgeblendet wird. NPR-16353
* Zeilenräume, die beim Bearbeiten eines Briefs hinzugefügt werden, werden nicht im Fenster &quot;Vorschau&quot;angezeigt. Bei Listen in Textfragmenten zeigt die PDF-Ausgabe nicht den richtigen Abstand an. NPR-16267
* Beim Bearbeiten eines Textfragments mit dem Internet Explorer-Browser schlägt der Einzug des Dokuments fehl, da der Cursor keinen Texteinzug zulässt. NPR-16128
* Das Hinzufügen oder Ändern eines Datenwörterbuchs zu einem vorhandenen Textfeldfragment nimmt viel Zeit in Anspruch und der Dokument wird nicht immer benachrichtigt. NPR-16102
* Bei der Vorschau eines Briefs mit durchlaufbaren Inhalten im Internet Explorer-Browser überschneidet sich die Browser-Bildlaufleiste mit der Bildlaufleiste des Briefs, und der gesamte Inhalt kann nicht für Fragmente auf der rechten Seite angezeigt werden. NPR-16068
* Beim Erstellen oder Bearbeiten von Text-Dokument-Fragmenten mit Google Chrome wird das Dropdown-Menü &quot;Farbauswahl&quot;automatisch angezeigt und kann nicht entfernt werden. Der Benutzer muss Liste als Typ der Dateneingabe auswählen, damit das Fragment bearbeitet werden kann. NPR-16067
* Bei Verwendung der Briefinstanz-API funktioniert die Methode `import com.adobe.icc.services.api.LetterInstanceService` nicht. NPR-16008
* Das Ändern der Datumsanzeigeformate in der Asset Composer-Konfiguration in `locale=en_US; dateFormat=MMM dd,yyyy;` funktioniert nicht wie erwartet und das Datumsformat wird als Junk-Zeichen angezeigt. NPR-16007
* Datenverknüpfungstyp in Briefen beim erneuten Authoring wird als &quot;Benutzer&quot;angezeigt, auch wenn er zuvor anders eingestellt wurde. NPR-16619

**Formularportal**

* Aktualisierungsszenarien für Entwurfs- und Übermittlungskomponenten funktionieren nicht bei der Implementierung von Datenbankbeispielen. NPR: 16752

**Barcoded Forms Service (BCF)**

* Die Analyse für statischen Code des Barcoded Forms Service (BCF) meldet Probleme. NPR-13855

#### Forms JEE-Installationsprogramm  {#forms-jee-installer-17}

**Process Management - HTML Workspace**

* Sichern des Forms-Vorfülldienstes vor unbefugtem Zugriff durch Protokolle wie &quot;file://&quot;, &quot;http://&quot;und &quot;ftp://&quot;. Weitere Informationen finden Sie unter [Konfigurieren des Vorfülldienstes mit Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**Benutzerverwaltung **

* Der SAML-Anmeldebildschirm zeigt eine falsche Version (6.1.0) des AEM 6.2-Servers an. NPR-13825
* Wenn AEM Forms für die Single-Sign-On (Kerberos)-Authentifizierung konfiguriert ist und die Benutzerauthentifizierung bei der Anmeldung fehlschlägt, wird der Fehlercode &quot;404&quot;zurückgegeben. Der Benutzer wird erst nach dem Aktualisieren der Seite zur Anmelde-Site weitergeleitet. NPR-15015

#### Forms Designer {#forms-designer-1}

* Das Ändern der Sprache des Formulars in Französisch (Kanada) in der Rechtschreibprüfung für Wörterbücher funktioniert in AEM Forms Designer nicht.\
   NPR-15896

### Feature Packs in CFP3 {#feature-packs-included-in-cfp-2}

**Forms Hinzufügen-On-Paket**

* Beim Löschen eines Assets im Correspondence Management sollte eine Warnmeldung in der Datei &quot;error.log&quot;protokolliert werden. NPR-13225
* Verbessern Sie die Suchfunktion bei der Vorschau eines Briefs im Korrespondenzmanagement, um die Suche im Textfragmentinhalt zu aktivieren, anstatt nur den Brieftitel oder die Beschriftung zu durchsuchen. NPR-16103

### OSGi-Pakete im CFP3 {#osgi-bundles-included-in-cfp-5}

Liste der OSGi-Pakete, die zwischen AEM 6.2 SP1 und CFP3 aktualisiert wurden

[Get ](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
FileDie wichtigsten Highlights von Cumulative Fix Pack 2 sind:

* Stabilitäts- und Leistungsverbesserungen in AEM Plattform, einschließlich Sling-Framework und Betrieb
* Verbesserte Asset-Verwaltung mit mehreren Korrekturen für Zugriff, Verschieben, Suchen, Hochladen und Veröffentlichen von Assets
* Verbessertes Authoring und Management von Sites mit Fehlerbehebungen in Inhaltsfragmenten, Anker-Plugin, Diashow und Context Hub-Komponenten
* Mehrere Fehlerbehebungen in der Touch-Benutzeroberfläche, einschließlich Texteditor, Omniture-Suche und Variantenerstellungsprozess
* Verbesserte Workflows; Erweiterter Microsoft Connector für die Verwendung neuer Übersetzungs-APIs für das Azurblase-Portal
* Fehlerbehebungen in Projekten und Kampagne
* Verbessertes Authoring und Management mit Fehlerbehebungen in den Funktionen für adaptive Formulare, Korrespondenzverwaltung und Formularportal
* Fehlerbehebungen in Forms JEE core, XTG und HTML Workspace

### Plattform {#platform-14}

* Das `SlingPostProcessor` wird ausgelöst, wenn die Seite, die direkt auf das Sling-Framework verweist, bearbeitet wird. NPR-15754: Hotfix für CQ-104153

* Der Wert für Tags mit der Eigenschaft `tagBasePath` wird beim Navigieren zu einer Seitenkomponente nicht im klassischen UI-Dialogfeld abgerufen. NPR-15543: Hotfix für CQ-4199950

* Bei der Ausführung von Sling-Operationen läuft ein Abschnitt mit dem Namen &#39;chunk_n_n-1&#39; `SlingFileUpload handler.getLastChunk` in eine Endlosschleife mit leeren Abschnitten. NPR-15455: Hotfix für SLING-5701

* Wenn eine Schnittstelle eine andere Schnittstelle erweitert, werden die injizierbaren Methoden auf der Super-Schnittstelle nicht korrekt injiziert. NPR-15202: Hotfix für SLING-5710
* Bei Verwendung des Funktionsaufrufs `com.adobe.granite.infocollector.impl.FilesTraversal`wird eine potenzielle Null-Zeiger-Ausnahme nicht verhindert. NPR-15169 Hotfix für CQ-4197640
* Der Workflow-Status ist für einige sekundäre Knoten inkonsistent und es wird ein Fehler angezeigt, während Beobachtungsdaten für diesen Knoten gesendet werden. NPR-15701: Hotfix für GRANITE-13786
* Wenn der Benutzer einen Knoten in CRXDE auswählt (z. B. /content/dam/) und dann auf der Registerkarte &quot;Zugriffskontrolle&quot;auf die Liste &quot;Zugriffskontrolle&quot;zugreift, werden beim Ziehen und Ablegen einiger Elemente die anderen Elemente als das ausgewählte verschoben. NPR-15696 Hotfix für GRANITE-16300
* Wenn Sie beim Identitätswechsel einen Benutzer aus der Dropdown-Liste auswählen, wird das gesamte Popup-Fenster ausgeblendet. NPR-15774: Hotfix für CQ-4201738/GRANITE-11895
* In Omniture funktioniert die Suche nach Tags mit automatisch ausgefüllten Empfehlungen nicht. NPR-15088: Hotfix für GRANITE-14426.\
   Hinweis: Für diese Fehlerbehebung ist Oak CFP 1.4.11 oder höher erforderlich.

### Mobile AEM-Autor {#mobile-aem-author}

* Bei der Verwendung von AEM Mobile- und ContentSync-Paketen mit einer Hybridanwendung reagiert AEM auf eine Abrufanforderung (mit Zeitstempeln), die von der Anwendung mit dem ältesten Paket und nicht mit dem von der Anwendung angeforderten Paket erstellt wurde. NPR-15749: Hotfix für CQ-104153

### Sites {#sites-17}

* Der Änderungsstatus für Workflow-Posteingang im WCM-Core ändert sich nicht, wenn der Benutzer eine Seite nach der Aktivierung eines Workflows ändert. NPR-15684: Hotfix für CQ-4196974
* Das Anker-Zusatzmodul in der Benutzeroberfläche &quot;Rich Text Editor for Touch&quot;generiert nicht konformes HTML5, wenn der Benutzer auf das Ankersymbol klickt und einen Namen hinzufügt. Es sollte ein Attribut &#39;id&#39; anstelle des Attributs &#39;name&#39; im HTML5-Tag für das Ankerelement hinzugefügt werden. NPR-15650: Hotfix für CQ-89782
* Wenn ein Metadaten-Schema mit zahlreichen Feldern erstellt und auf die Metadaten des Inhaltsfragments angewendet wird, wird im Anzeigebereich &quot;Inhaltsfragment-Metadaten&quot;keine Bildlaufleiste erstellt, sodass die Felder nicht bearbeitet werden können. NPR-15478: Hotfix für CQ-4202622
* Beim Bearbeiten der Feldkomponente `TagInput` werden die zuvor konfigurierten Werte nicht mit den Dialogfeldern verglichen. NPR-15464: Hotfix für CQ-4200360

* Wenn in der Benutzeroberfläche des Inhaltsfragment-Editors viele Varianten eines Inhaltsfragments erstellt werden, zeigt das Seitenbedienfeld nicht die Bildlaufleiste an, um durch alle Varianten zu navigieren. NPR-15445: Hotfix für CQ-4199444
* Wenn Benutzer aus direkten Gruppen entfernt werden, werden sie zu geerbten Gruppen hinzugefügt. NPR-15400: Hotfix für CQ-98758
* WCM-Authoring: Touch-UI-Autor lässt die Bearbeitung von Seiten, die Kommas im Namen enthalten, nicht zu. NPR-15396: Hotfix für CQ-4199723
* Bei Verwendung der Touch-Benutzeroberfläche zum Authoring übergibt die Funktion `Granite.author.editableHelper.doSelectParent` Argumente in der falschen Reihenfolge, die zu einem JavaScript-Fehler führen. NPR-15349: Hotfix für CQ-4198594
* Das ContextHub-Segment zeigt das Erlebnis auch dann an, wenn das Ausschluss-Cookie vorhanden ist. NPR-15293: Hotfix für CQ-4198024
* Die Diashow-Komponente in der klassischen Benutzeroberfläche kann keine Folien erstellen oder Bilder per Drag &amp; Drop verschieben, um neue Folien zu erstellen. NPR-15281: Hotfix für CQ-4194164
* Benutzern werden unabhängig von der Berechtigung die Menüoptionen &quot;Erstellen&quot;angezeigt, z. B. &quot;Seite erstellen&quot;, &quot;Site erstellen&quot;, &quot;Live-Kopie erstellen&quot;, &quot;Launch erstellen&quot;und &quot;Katalog erstellen&quot;in der Site-Admin-Konsole. NPR-15278: Hotfix für CQ-94436
* Nach der Installation von AEM 6.2 Service Pack 1 funktioniert der Schieberegler &quot;Unterseiten einschließen&quot;nicht mehr bei Seitenaufrufen. NPR-15230: Hotfix für CQ-4198449
* Anforderung zur Verbesserung der Versionsbereinigung, um Versionen in Blöcken abzurufen und zu verarbeiten und auch in der Lage zu sein, einen angegebenen Pfad in eine XPath-Abfrage zu verwenden. NPR-15186: Hotfix für CQ-109205
* Die Schaltfläche &quot;Löschen&quot;fehlt auf der Registerkarte &quot;Miniaturansicht der Seiteneigenschaften&quot;der Komponente &quot;Sites&quot;. NPR-15143 Hotfix für CQ-4196997
* Bei einer Site, die Live Copies verwendet, zeigt die Auswahl des Kontrollkästchens &quot;Live Copy&quot;im Bereich &quot;Spalten&quot;in der SiteAdmin-Konsole den Status &quot;Live Copy&quot;nicht korrekt an und es wird nur HTML-Markup angezeigt. NPR-15108: Hotfix für CQ-97086
* Wenn der Benutzer beim Bearbeiten von Inhaltsfragmenten zur Bearbeitung auf Fertig klickt (&#39;**), bevor er die Antwort des Beitrags erhält, wird der bearbeitete Inhalt nicht korrekt gespeichert. NPR-15014: Hotfix für CQ-4194095
* Wenn Sie die Seite &quot;Bearbeiten&quot;während des Timewarp-Modus schließen und versuchen, sie erneut von SiteAdmin zu öffnen, wird ein Fehler mit dem Status &quot;500&quot;angezeigt, anstatt die Seite erneut zu öffnen. NPR-14965: Hotfix für CQ-109647:
* In der Benutzeroberfläche von Digital Asset Manager (DAM) führt die Suche nach Autorisierungen durch den Benutzer-wähler zu einer Ausnahme vom Typ &quot;Nicht genügend Arbeitsspeicher&quot;. NPR: 15307: Hotfix für CQ-98542

### Assets {#assets-17}

* Nachdem Sie ein Asset in Omniture Search durchsucht haben, ein Asset ausgewählt und versucht haben, Eigenschaften zu bearbeiten, indem Sie auf &quot;Ansichten-Eigenschaften&quot;klicken und dann mit der Schaltfläche &quot;Speichern&quot;Benutzer zu einer leeren Seite weitergeleitet werden. NPR-15900: Hotfix für CQ-4202372
* Die Benutzeroberfläche &quot;Assets&quot;reagiert nicht auf Ereignis. Wenn Sie ein Asset auswählen und auf &quot;Veröffentlichen&quot;oder &quot;Darstellungen&quot;klicken, wird keine Aktivität angezeigt. NPR-15828: Hotfix für CQ-4202247
* Beim Veröffentlichen eines Assets aus der Ansicht &quot;Karte&quot;wird die Karte nicht aktualisiert, um einen veröffentlichten Status wiederzugeben, es sei denn, die Seite wird aktualisiert. NPR-15826: Hotfix für CQ-102732
* Kumulativer Hotfix mit Hotfixes für Assets. NPR-15225
* Wenn das kaufmännische Und-Zeichen (&#39;&amp;&#39;) im Namen eines Asset-Ordners enthalten ist, wird der Ordnername beim Navigieren zum Asset nicht korrekt angezeigt. NPR-15775: Hotfix für CQ-4201735
* Die Verwendung von kaufmännischem und (&#39;&amp;&#39;) Zeichen im Namen einer Asset-Datei verursacht Probleme beim Zugriff auf die Eigenschaften. NPR-15770: Hotfix für CQ-4201737
* Wenn der Benutzer beim Navigieren in Assets und beim Verwenden des Anzeigemodus &quot;Spaltenansicht&quot;die Ansicht aktualisiert, nachdem er ein Asset ausgewählt und angeklickt hat, werden die Asset-Details anstelle des aktualisierten Inhalts angezeigt. NPR-15768: Hotfix für CQ-4201727
* Die PDS-Erfassung nimmt 100% CPU-Auslastung mit einer Heap an Bibliotheken für PDF-Dienste in Anspruch. NPR-15606 HotFix for GRANITE-12929
* Beim Zugriff auf die Benutzeroberfläche &quot;Meine Linkfreigabe&quot;mit dem Firefox-Browser werden die freigegebenen Elemente oder Benutzer nicht angezeigt, und der Bildschirm ist unbrauchbar. NPR-15539: Hotfix für CQ-4200992
* Wenn eine Seite mit einem Bildsatz verknüpft ist und Sie den Digital Asset Manager verwenden, werden beim Verschieben der Bilder in einen neuen Ordner die Seitenverknüpfung unterbrochen und einige Bilder fehlen auf der verknüpften Seite. NPR-15538: Hotfix für CQ-111479
* In der Dam-Viewer-Komponente führt die Verwendung des Ausführungsmodus &quot;nosampleContent&quot;zu Fehlern bei dynamischen Medien. NPR-15449: Hotfix für CQ-4195425
* Wenn beim Erstellen von Video-Profilen sowohl eine Videokodierungsvorgabe hoher Qualität als auch eine Videokodierungsvorgabe mittlerer Qualität ausgewählt wird, werden die vorgenommenen Änderungen nicht gespeichert. NPR-15447: Hotfix für CQ-4195482
* Obwohl das Hochladen eines Assets in das Markenportal aufgrund einer Serverfehlermeldung fehlschlägt, wird der Status auf &quot;Veröffentlicht&quot;in der Benutzeroberfläche des Markenportals aktualisiert, sodass es schwierig ist, die verpasste Datei zu verfolgen. NPR-15442: Hotfix für CQ-4197968
* Beim Veröffentlichen eines Asset-Ordners im Markenportal, dessen Veröffentlichung mehr als eine Stunde dauert, können einige Dateien nicht veröffentlicht werden. NPR-15441: Hotfix für CQ-4199493
* Bei der Verwendung der Asset Finder-Konsole in der Ansicht der Spalten schlägt der Versuch, einen Ordner zu erstellen, fehl, obwohl es beim erneuten Versuch erfolgreich war. NPR-15370: Hotfix für CQ-4199448
* Wenn ein in der DAM-Benutzeroberfläche ausgewähltes Asset oder Ordner ein Komma im Namen enthält, ist die Registerkarte &quot;Referenzen&quot;nicht verfügbar und zeigt die Meldung &quot;Liste von Referenzen ist nicht für mehrere Auswahlen verfügbar&quot;an. NPR-15362: Hotfix für CQ-4199721
* Beim Veröffentlichen eines Ordners im Markenportal wird der Status &quot;Veröffentlicht&quot;des Ordners nicht geändert, auch wenn die Assets im Ordner erfolgreich veröffentlicht wurden. NPR-15292: Hotfix für CQ-4197667
* Beim Navigieren zur Assets-Konsole in der Touch-Benutzeroberfläche wird beim Aktivieren bestimmter Assets eine Ausnahme angezeigt. NPR-15217: Hotfix für CQ-108779
* Veröffentlichen eines Videos auf YouTube, wenn die Verbindung über einen Proxyserver erfolgt. NPR-15109: Hotfix für CQ-110332
* Verwenden eines Assets mit einem Namen, der einen Punkt oder Punkt (.) enthält in der datenbasierten Ressource wird nicht auf dasselbe Asset aufgelöst, und der Ausgabepfad wird an dem Punkt beendet. NPR-15069: Hotfix für CQ-4195914
* Nach der Aktualisierung von AEM 6.2 auf Service Pack 1 schlägt die Synchronisierung von Assets in Scene7 fehl. Die Eigenschaft dam:Scene7FileStatus zeigt den Status `UploadFailed` auch für veröffentlichte Assets an. NPR-15269: Hotfix für CQ-4197708

### Benutzeroberfläche {#user-interface-5}

* In **[!UICONTROL Touch UI]** wird das gespeicherte Datum nicht für Datumsfelder angezeigt, die bei Verwendung von Internet Chrome Browser Version 56.0.2924.87 nicht type=&#39;datetime&#39; haben. NPR-15383: Hotfix für GRANITE-16481
* In **[!UICONTROL Touch UI]** entfernt der Rich-Text-Editor den Thread und die Beschriftungselemente während der Wiedergabe aus den HTML-Tabellen. NPR-15267: Hotfix für CRTE-41
* `FileUpload Validator` behandelt keine Fälle, in denen autostart true ist oder manuell aufgerufen  `uploadFile()` wird, und generiert in diesen Fällen einen ungültigen Überprüfungsbericht. NPR-15295: Hotfix für GRANITE-13499

* Omniture erlaubt Kunden, die /apps verwenden, keine Spaltendatenquelle hinzuzufügen, da davon ausgegangen wird, dass die Standortkonfiguration unter */libs/granite/omnisearch/content/metadata/* aufgeführt ist. NPR-13188 Hotfix für GRANITE-16479
* Bei Verwendung der **[!UICONTROL Touch-Benutzeroberfläche]** werden keine Produktvarianten auf derselben Ebene wie das Produkt erstellt. Der Benutzer wird nicht über den Status der Variantenerstellung informiert. NPR-15345: Hotfix für CQ-4198948

**Scene7**

* Die Ausführung des Scene7-Workflows führt zu geöffneten Dateien, die nicht geschlossen werden. Anforderung zur Verbesserung des AEM-S7-Dienstes, damit eine einzelne HttpClient-Instanz mit einer freigegebenen Pooling-Konfiguration beibehalten und wiederverwendet wird. NPR-15357: Hotfix für CQ-109958

### Übersetzung {#translation-9}

* Wenn Sie Übersetzungsprojekte verwenden und Sprachkopien vom englischen Übergeordnete aktualisieren, werden 11 separate Starts mit demselben Namen und demselben Quellstamm, jedoch mit etwas unterschiedlichen Startwurzeln erzeugt, falls der Seitenname einem bestimmten Muster folgt. NPR-15605: Hotfix für CQ-4200699
* Übersetzungsprojekte werden nicht für Seiten erstellt, deren sprachliche Wurzeln Bindestriche und Bindestriche im Namen haben. NPR-15171: Hotfix für CQ-96286
* Anforderung, den Microsoft Connector zu aktualisieren, um die Microsoft Translator APIs verwenden zu können, die Microsoft im Azurblauen Portal zur Verfügung stellt. NPR-15320: Hotfix für CQ-101010

### Projekte {#projects-4}

* Im Projektbildschirm sind nur 20 inaktive Projekte sichtbar, obwohl mehr als 20 inaktive Projekte im Repository vorhanden sind. NPR-15656: Hotfix für CQ-4200903

### Kampagne {#campaign-1}

* Bei Verwendung der Komponenten Kampagne - Targeting und MAC - Test- und Zielgruppe-Integration wird der Status der Aktivität in der Übergeordnet-Benutzeroberfläche nicht durch die Deveröffentlichung von Aktivitäten aktualisiert. NPR-15401: Hotfix für CQ-4199839
* Beim Verschieben eines Produkts in AEM Commerce vermisst der Produktverschieben-Assistent die vorausgefüllten Werte für Produktname, Titel, referenzierte Seiten, Autor und Erstellungsdatum. NPR-15228: Hotfix für CQ-98617

### Sicherheit {#security-4}

* CSRF-Token-Parameter, der Formularen mit einer GET hinzugefügt wird. NPR-15229

### Formulare {#forms-18}

#### Forms-Add-on-Paket {#forms-add-on-package-18}

`**Adaptive Forms**`

* Standardwerte werden beim Vorausfüllen des adaptiven Formulars mit Eingabe-XML durch leere Werte in xml überschrieben. NPR-15721
* Der `afData/afBoundData`-Wrapper ist in der gesendeten XML vorhanden, auch wenn die XML zum Vorausfüllen keinen `afData/afBoundData`-Wrapper in XML-Schema-basierten adaptiven Formularen aufweist. NPR-15541

* Die Titel in der Akkordeon-Leiste sollten bearbeitbare HTML-Überschriften des Typs &quot;h2&quot;anstelle des Tags &quot;a&quot;sein. NPR-15475
* Das Akkordeon-Layout eines Formularfelds ist für Benutzer von Bildschirmlesehilfen nicht verfügbar. Benutzer können nicht allein mit Bildschirmlesehilfen wie JAWS oder NVDA zur Akkordeon-Registerkarte navigieren. NPR-15474

`**Correspondence Management**`

* Das Speichern, Löschen und Festlegen des Verweises für ein Dokument-Fragment nimmt erhebliche Zeit in Anspruch. NPR-15939
* Die Registerkartenausrichtung wird in &quot;Elemente verwalten&quot;für Text mit mehreren Kopfzeilen-Umbrüchen in der CCR-Benutzeroberfläche festgelegt. NPR-15818
* Miniaturansichten von Textmodulen zeigen keine ausgerichteten Inhalte an, obwohl der Text ausgerichtete Inhalte enthält, die mit Tabs in Google Chrome erstellt wurden. NPR-15819

`**Forms Portal**`

* Der Vorfülldienst funktioniert nicht für XDP Forms. NPR-15466
* Beim Speichern von Entwürfen und Übermittlungen adaptiver Formulare in die Datenbank wird der Status des adaptiven Formulars beschädigt, wenn die Datenbankverbindung aus irgendeinem Grund (z. B. nach einer langen Inaktivität) fehlschlägt. NPR-15297

#### Forms JEE-Installationsprogramm  {#forms-jee-installer-18}

`**Core**`

* Nach dem Upgrade auf die neueste Version von Java 1.8.0_121-b13 ist die Admin-Benutzeroberfläche in AEM Forms nicht verfügbar. NPR-15330

`**XTG**`

* Beim Zusammenführen eines bestimmten Formulars mit einem Dataxml mit dem Output-Dienst beträgt die Antwortzeit 20-mal im Vergleich zur Zeit, die der ES4 SP1-Server für denselben Vorgang benötigt. NPR-15283

#### AEM Forms-App {#aem-forms-app-1}

* Beim Wiederherstellen nicht gespeicherter Aufgaben muss die Meldung bei der Wiederherstellung nicht gespeicherter Aufgaben deutlicher gemacht werden, um Benutzerfehler zu reduzieren. NPR-15377
* Die AEM Forms-App gibt keine Formulare wieder, die aus benutzerdefinierten Vorlagen erstellt wurden. NPR-15892
* Benutzer können sich nicht bei der AEM Forms-App anmelden. NPR-15891

Die wichtigsten Highlights von AEM 6.2 SP2-CFP1 sind:

* Optimiert die Replikationsfunktion in Sites:

   * Fehlerbehebungen bei verschiedenen Rollout-, LiveCopy- und Schreibfehlern

* Verbessert die Reaktionsgeschwindigkeit der Touch-Benutzeroberfläche während:

   * Asset-Suchen
   * Größenbasierte Sortierung

* Verbessert das Tag-Management in intelligenten Sammlungen
* Strengere Zugriffskontrollen bei CRUD-Vorgängen in Ordnern

### Plattform {#previous}

* Anforderung zum Entfernen von `ReplicationQueue#forceRetry`-API-Aufrufen beim Starten von Replizierungsagenten, da solche Aufrufe die Instanz erheblich verlangsamen, insbesondere, wenn es viele Replizierungsagenten gibt. NPR-14032: Hotfix für GRANITE-13095
* Anforderung der OSGi-Konfiguration, um Felder zu unterstützen, die ein Array von Werten speichern können. `DurboImportConfigurationProviderService` NPR-14570: Hotfix für CQ-108684
* Die Verwendung der Komponente &quot;Sightly&quot;auf einer Seite nach der Migration auf AEM 6.2 führt dazu, dass das Dialogfeld Eigenschaften der Seite nicht mehr funktioniert. NPR-14328: Hotfix für CQ-108355
* Durch die Aufhebung der Zeitplanung für einen zuvor geplanten Auftrag wird der entsprechende Knoten unter */var/event/schedule-jobs* nicht entfernt. NPR-14253: Hotfix für SLING-5666
* Wenn ein Administrator versucht, die Identität eines gelöschten Benutzers zu imitieren, kann die Benutzeroberfläche nicht aktualisiert werden. NPR-14247: Hotfix für CQ-107446
* XSS-Schutzprüfung, die eine falsche Kodierung in Sightly-Komponente verursacht. NPR-14004: Hotfix für CQ-93821
* Anfrage zur Aktualisierung von Jackrabbit Filevault auf 3.1.30, um mehrere Probleme zu lösen. NPR-13454
* Der Cache-Fehler tritt auf, wenn die Sling-Distribution die Distributionspakete vom Autor zur Veröffentlichung synchronisiert. NPR-13034: Hotfix für GRANITE-13970

### Sites {#sites-18}

* Probleme mit VersionManagerImpl, wenn falsche Versionen aus dem Versionsverlauf entfernt wurden. NPR-14372
* Die Komponente &quot;WCM Sightly Foundation parsys&quot;ignoriert die Tag-Namen der Komponentendeklaration `cq:htmlTag / cq:tagName`. NPR-14225
* Wenn Sightly Parsys zum Rendern von Komponenten verwendet wird, die über JavaScript in der Touch-Benutzeroberfläche eingefügt wurden, wird die benutzerdefinierte Dekoration ignoriert, nachdem die Seite aktualisiert wurde. NPR-14122
* Dropdown-Listen für Zielgruppen funktionieren nicht im Dialogfeld der Touch-Benutzeroberfläche, wenn mehrere RichText-Felder, z. B. Links, erstellt werden. NPR-13911
* Beim Bearbeiten eines Textfelds mit mehreren Rich Text Editor-Eigenschaften (RTE) in einem Dialogfeld (Touch UI) wechselt der Fokus zufällig zu einer bestimmten RTE-Eigenschaft. NPR-13703
* Die standardmäßige Out-of-the-Box-Videokomponente gibt die Videominiatur nicht wieder. NPR-14976
* Informationen werden im Vorlageneditor langsam auf der Registerkarte &quot;Live-Verwendung&quot;geladen. NPR-14880: Hotfix für CQ-83417
* Wenn Sie Hotfix-10936 auf einer AEM 6.2-Instanz installieren, wird die iparsys-Komponente deaktiviert. NPR-14330: Hotfix für CQ-106982
* Probleme mit mehreren Rollout-Komponenten und ein Live Copy-Problem nach der Migration auf AEM 6.1 SP1. NPR-15256
* Bei der Seitenausführungsaktion können auch bei mehreren Roll-out-Konfigurationen keine untergeordneten Elemente über die erste Ebene hinaus erstellt werden. NPR-15055
* Beim Senden des Dialogfelds &quot;PageProperties&quot;aus dem Editor werden unveränderte Daten auf den LiveCopy-Registerkarten neu geschrieben. NPR-14693
* Wenn das Dialogfeld &quot;PageProperties&quot;vom Editor gesendet wird, schreibt MSM Post Processor einige Parameter aus der Anforderung anstelle des Parameters `msm:writeLiveCopyConfig`. NPR-14434
* Mehrere Probleme im Zusammenhang mit der Rollout-Komponente, Live Copies und anderen Aspekten von MSM. NPR-12235

### Assets {#assets-18}

* UnPack Workflow kann Bilder mit Sonderzeichen im Bilddateinamen nicht verarbeiten. NPR-15227: Hotfix für CQ-103887
* Assets, die mit Bedingungs-Ausdruck wiederholt werden, werden nicht richtig angezeigt. Wenn der Benutzer die Briefvorlage `*CDN3835RLCEN*` Vorschau, werden keine Elemente angezeigt, die sich im Bereich &quot;Zielgruppe des Textkörpers&quot;befinden. Wenn das Asset `*VIPReassement*`, ein optionales Asset, das vorab ausgewählt ist, nicht ausgewählt ist, werden die anderen vorab ausgewählten Assets im Brief angezeigt. NPR-14844

* Beim Erstellen einer intelligenten Sammlung wird das style-Tag beim Speichern der intelligenten Sammlung nicht beibehalten. NPR-15081: Hotfix für CQ-4195494
* Abfragen zur Asset-Suche, die bei gleichzeitigen Suchvorgängen durch mehrere Benutzer langsam in der Touch-Benutzeroberfläche ausgeführt werden. NPR-15019: Hotifx für CQ-4195405
* Metadaten, die für eine Eigenschaft des Typs `Long[]` extrahiert wurden, werden in den Typ `String[]` konvertiert, wenn das ursprüngliche Asset an einen anderen Speicherort hochgeladen wird. NPR-15016: Hotfix von CQ-4195005

* Benutzer, die eine gespeicherte Suche oder eine intelligente Sammlung nicht löschen können. NPR-14924: Hotfix für CQ-108494
* Beim Bearbeiten von Metadaten für Assets als Massendatei (im Anhangsmodus) und beim Verwenden eines booleschen Werts für TypeHint in einem Dropdown-Feld im zugrunde liegenden Metadaten-Schema wird ein Fehler ausgegeben. NPR-14529: Hotfix für CQ-106876
* Benutzer ohne Replikationsrechte können Asset-Ordner nicht löschen. NPR-14321: Hotfix für CQ-88271
* Beim Versuch, die Video-Profile für ein Video im Kanal Editor zu bearbeiten, wird das Dialogfeld &quot;Entwurf&quot;nicht geöffnet und löst eine Null-Zeiger-Ausnahme im Fehlerprotokoll aus. NPR-14144: Hotfix für CQ-81101
* Die systemgenerierte Zeitstempeleigenschaft &quot;Erstellt&quot;, die auf der Eigenschaftenseite für ein Asset angezeigt wird, ist nicht korrekt. NPR-13992: Hotfix für CQ-95029
* Anfrage zur Aktivierung der Erkennung von Duplikat-Assets für Benutzer ohne Lesezugriff in AEM Assets NPR-13851: Hotfix für CQ-102281
* Benutzer können auf der Eigenschaftenseite keine Metadaten für Assets stapelweise bearbeiten. NPR-13721: Hotfix für CQ-100703
* Falsche Fehlermeldung in der klassischen Benutzeroberfläche beim Hochladen eines Duplikat-Assets. Die Fehlermeldung gibt nicht an, warum der Upload fehlgeschlagen ist. NPR-13691: Hotfix für CQ-99272
* AEM Assets kann in der Ansicht der Liste nicht mehr als 50 Assets nach Größe sortieren, wenn der Ordner mehrere Assets enthält. CQ-100588
* Wenn Sie mehrere Assets auswählen, wird ein Fehler mit dem Antwortcode 414 (Request-URI zu lang) angezeigt, wenn der URI für den Asset/Ordner zu lang ist. NPR-13516: Hotfix für CQ-76076
* Die Seite &quot;Bericht zu Assets&quot;reagiert nicht mehr, wenn der Benutzer im Dialogfeld &quot;Spalten konfigurieren&quot;alle Optionen auswählt. NPR-13187: Hotfix für CQ-95589
* Unerwartetes Verhalten von Tag Picker in Safari und Internet Explorer. NPR-13134
* Durch Bearbeiten der gespeicherten Suche in der Leiste &quot;Asset-Admin-Suche&quot;können Sie diese als verschachtelte intelligente Auswahlen speichern, was Probleme mit der Umgebung verursacht. NPR-13119: Hotfix für CQ-99460
* Nach dem Verschieben einer Datei (oder eines Ordners) und dem anschließenden Umbenennen der Datei spiegeln die Metadaten &quot;cq:name&quot;nicht den neuen Dateinamen (Ordnernamen) wider. NPR-13036: Hotfix für CQ-99141
* Asset mit Namen, die Sonderzeichen enthalten, können nicht aus dem per E-Mail freigegebenen Download-Link heruntergeladen werden. NPR-12872: Hotfix für CQ-95795
* Standardmäßig verfügbare Asset-Berichte, die generiert werden, wenn eine erhebliche Anzahl von Assets zu hohen Durchgängen führt, bei denen die Suche keinen Index- und CPU-Auslastungsspitzen erreicht. NPR-12811: Hotfix für CQ-84409
* Benutzer mit AMS AEM Assets Autoreninstanz haben Zugriff von verschiedenen Netzwerken, die Assets nicht über das Hochladen von Paketen ohne Löschberechtigungen in Ordnern hochladen können. NPR-12768: Hotfix für CQ-82715
* Bei tagbasierten Suchen nach Assets mit der Leiste &quot;Asset-Suche&quot;beschränkt sich die Funktion &quot;Type Ahead&quot;nicht auf den Stammpfad und zeigt Tags aus allen Namensräumen an. NPR-12666
* Die Komponente StaticRenditions löst eine Null-Zeiger-Ausnahme aus. NPR-12665
* Anforderung zur Deaktivierung von MissingMetadataNotificationJob, da dadurch die Benutzeroberfläche für die Badge-Benachrichtigung die Seite mit der Ausnahme &quot;Eingabe kann nicht überprüft werden&quot;umbricht. NPR-12500: Hotfix für CQ-93573
* Die Option &quot;Bearbeiten deaktivieren&quot;für ein Tag-Feld funktioniert nicht in den Seiten mit den Asset-Eigenschaften auf der TouchUI. NPR-12429: Hotfix für CQ-88835
* API-Korrekturen in AEM Assets 6.2 für die Implementierung von Companion App SMB. NPR-11099
* Seit der Aktualisierung von Jquery können Benutzer keine Asset-Sammlung auswählen und die Auswahl eines Inhaltsfragments im Bedienfeld &quot;Inhalt zuordnen&quot;bestätigen. NPR-14847: Support für CQ-4194209
* Obwohl auf der Clientseite unendliche Sortierung aufgerufen wird, werden nur Artikel/Banner/Sammlungen sortiert, die derzeit in der Benutzeroberfläche angezeigt werden. NPR-14493: Hotfix für CQ-109926
* Anforderung der Implementierung der Suchfunktion für AEM On-Demand-Dienste für Mobilgeräte. Die Suchbegriffsuche nach Artikeln, Sammlungen oder Bannern gibt keine Übereinstimmungen zurück. NPR-14093: Hotfix für CQ-101394
* Bei Verwendung der Komponente &quot;Korallenauswahl&quot;(*granite/ui/components/coral/foundation/form/select*) in einem Dialogfeld funktioniert die Wertinitialisierung in Internet Explorer (IE11- oder Edge-Browser) nicht ordnungsgemäß, wenn der ausgewählte Wert ein einzelnes Element enthält. NPR-13395: Hotfix für CQ-101013

### Projekte {#projects-5}

* Beim Exportieren eines Übersetzungsprojekts, das mit der Übersetzungsmethode als &quot;human&quot;und dem Übersetzungsanbieter als &quot;none&quot;erstellt wurde, wird keine Datei &quot;translation_export_summary.xml&quot;generiert, da die GUID-Zuordnungsdatei fehlt. NPR-13137: Hotfix für CQ-91976
* Bei AEM Projekten wird bei der Erstellung eines Projekts mit der Eigenschaft &quot;due date&quot;die Uhrzeit bei der Datumskonvertierung aufgrund der Zeitzone zwischen Server und Client falsch eingestellt. NPR-13003: Hotfix für CQ-98288
* Die Option &quot;In Sites anzeigen&quot;wird beim Übersetzungsauftrag nicht angezeigt, wenn ein Übersetzungsprojekt aktualisiert wird. NPR-12966: Hotfix für CQ-93740
* Wenn ein Übersetzungsprojekt für eine exportierte Siteseite erstellt wird, wird es in der Vorschau nicht korrekt dargestellt. NPR-12964: Hotfix für CQ-84627

### Workflow {#workflow-3}

* Der Link Nutzlast auf der Registerkarte Archiv der Workflow-Konsole gibt einen Fehler mit dem Antwortcode &#39;404&#39; zurück, wenn darauf geklickt wird. NPR-14993: Hotfix für CQ-4194977
* Bei Verwendung AEM standardmäßigen Workflows versäumt es der CQ-Mailer, eine E-Mail-Benachrichtigung an die Gruppe zu senden, die die E-Mail-Adresse eines einzelnen Mitglieds nicht erreicht hat. NPR-14804: Hotfix-Anfrage für GRANITE-91499
* Leistungsverbesserungen für Posteingang und Benachrichtigungsabzeichen in der Touch-Benutzeroberfläche. NPR-14145: Hotfix für CQ-101125
* Benutzer, die die Nutzlast nicht aus der Workflow-Inbox-Konsole beim Starten der Workflows Vorschau haben. NPR-13226: Hotfix für CQ-100275
* Das mit dem SAML-Authentifizierungs-Handler konfigurierte Cookie &quot;saml_request_path&quot;zeigt Cookies, die mit einem zusätzlichen &#39;?&#39; gesetzt wurden. Zeichen. Wenn eine SAML-Antwort an AEM zurückgesendet wird, gibt das AEM-Cookie &quot;saml_request_path&quot;aufgrund bereits kodierter Zeichen einen ungültigen Wert zurück. NPR-13517: Proaktiver Hotfix für GRANITE-11722 und GRANITE-14414

### Lösungsintegration {#solution-integration}

* Wenn ein Benutzer nach der Integration von AEM 6.2 mit Search&amp;Promote einen Begriff durchsucht, der ein Banner zurückgibt, reagiert die Suchfunktion nicht mehr. NPR-14549: CFP für CQ-109631

### Dynamic Media {#dynamic-media}

* Zahlreiche AEM-Scene7 Sling-Aufträge, die während der AEM Aktivierung erstellt und abgebrochen wurden, werden während der Replikation als Archivaufträge protokolliert. NPR-12835: Hotfix für CQ-86115

### Sicherheit {#security-5}

* Anforderung zur Behebung eines Problems bei der Eingabevalidierung im WCMDebug-Filter. NPR-12444: Hotfix-Anfrage für GRANITE-94890
* Proaktive Anforderung zum Korrigieren des XSS-Verhaltens bei Verwendung des Assistenten zum Erstellen des Starts.\
   NPR-13062: Hotfix-Anfrage für GRANITE-99577

#### Forms-Add-on-Paket {#forms-add-on-package-19}

`Adaptive Forms`

* Beim Erstellen eines wiederholbaren Bereichs mit adaptiven Formularen kann der Bereichstitel zur Laufzeit nicht aktualisiert werden. NPR-15325
* Wenn beim Speichern oder Senden der Standardwert für ein Optionsfeld festgelegt und ein anderer Wert als der Standardwert ausgewählt wird, wird der Wert nicht in der Vorausfüllung angezeigt. NPR-15304
* Google Chrome zeigt ein falsches Verhalten bei der Verwendung des Options-Ereignisses zum dynamischen Ausfüllen der Dropdown-Liste und zum Senden des ausgewählten Elementwerts an. NPR-15198
* Beim Erstellen eines wiederholbaren Bereichs mit adaptiven Formularen kann der Bereichstitel zur Laufzeit nicht aktualisiert werden. NPR-15181
* Bei der Verwendung des Bearbeitungsmodus für adaptive Formulare treten JavaScript-Fehler auf, z. B. &quot;Handler der Komponente ist ungültig&quot;und &quot;guidelib ist nicht definiert&quot;. NPR-15112
* Das Laden von Fragmenten in einem sich wiederholenden Bedienfeld funktioniert nicht wie erwartet. NPR-13916, NPR-14785

`Correspondence Management`

* Correspondence Management-Assets mit `'Repeat with condition'`Ausdruck-Set werden nicht richtig angezeigt. NPR-14844
* Wenn Sie nach einem Correspondence Management-Asset (z. B. einem Brief, einem Dokument-Fragment oder einem anderen Typ) suchen, fehlt das Symbol &quot;Download-Warteschlange&quot;in der Symbolleiste. NPR-14745
* Beim Erstellen eines Listen-Moduls funktioniert das Umschalten zwischen den Asset-spezifischen Eigenschaften (z. B. editierbar, obligatorisch) nicht. NPR-14689
* Das Datenelement-Bedienfeld im Dienstprogramm Ausdruck Builder lädt weiter, wenn ein Bedingungsmodul ohne Auswahl eines Datenwörterbuchs erstellt wird. NPR-14688
* Beim Anzeigen einer Briefvorschau können Benutzer keine Tabulatorzeichen verwenden, um Inhalte im Tabellenformat auszurichten. NPR-14481
* Wenn Correspondence Management-Assets stapelweise aus der Benutzeroberfläche exportiert werden, generiert der AEM Forms-Server unnötige Protokolle. NPR-15226
* Wenn eine Vorschau eines Briefs angezeigt wird, wird Text mit Blocksatz in einer anderen Schrift angezeigt. NPR-15468

`**Forms Portal**`

* Anlagen von gesendeten Formularen im Forms-Portal sind nicht sichtbar, wenn ein neuer Entwurf aus der Portalübermittlung gesendet wird. NPR-13515

`**Forms Manager**`

* Beim Navigieren im Ordner &quot;*Forms andDocuments*&quot;wird die Schaltfläche &quot;Einfügen&quot;nicht angezeigt, wenn der Benutzer ein Asset kopiert und dann zu einem anderen Ordner navigiert. CQ-111327

#### Forms JEE-Installationsprogramm {#forms-jee-installer-19}

`Rights Management`

* Das Ereignis zur Benutzeranmeldung bei der Prüfung wird mit ungültiger Uhrzeit protokolliert. Die richtige Uhrzeit für das Audit-Ereignis ist nicht rückverfolgbar. NPR-13107
* Adobe Acrobat Reader und Microsoft Office können keine mit erweiterter Authentifizierung geschützten Dokumente öffnen. NPR-14482

`Process Management`

* Wenn eine weitergeleitete Entwurfsversion in HTML Workspace an den Ausgangsbenutzer zurückgegeben wird, wird die Aufgabe nicht in der Warteschlange des Ausgangsbenutzers angezeigt. NPR-15178

`Assembler Service`

* AEM Forms kann PDF/A-2b mit mehr als zwei Signaturen nicht validieren. NPR-14101

`XTG`

* Beim Drucken eines Dokuments mit einem Umgehungsfach des Druckers aktiviert die Funktion `GeneratePrintedOutput` nicht das Abrufen von Papier aus dem rechten Bypass-Fach. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer stürzt ab, wenn der Benutzer das Dienstprogramm &quot;Rechtschreibprüfung&quot;mit der ausgewählten Sprache als Französisch (Kanada) ausführt. NPR-13740
* Forms Designer stürzt ab, wenn der Benutzer &quot;Ereignis berechnen&quot;oder &quot;Ereignis überprüfen&quot;für ein Formularfeld auswählt und die Sprache in &quot;JavaScript&quot;ändert und `this.` in das Fenster **[!UICONTROL Skript-Editor]** eingibt. NPR-12974

### Feature Packs in CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Hinzufügen-On-Paket):

* Wenn ein adaptives Formular aus einer XDP-Datei erstellt wird, folgen die Tab-Taste für Barrierefreiheit nicht dem festgelegten Muster. NPR-12562

`Adaptive forms` (Forms Hinzufügen-On-Paket):

* Rule Builder für adaptive Formulare bietet keinen rollenbasierten Zugriff. Änderungen, die von einem Autor vorgenommen wurden, können nicht verfolgt werden. NPR-12840

`Core` (Forms JEE-Installationsprogramm):

* Die CORS-Funktion (CoreCross Herkunft Resource Sharing) als Servlet-Filter ist für Jboss+ nicht aktiviert. NPR-13050

## Download-Anweisungen für CFP über Softwareverteilung {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Für AEM Forms-Kunden ist es unerlässlich, AEM Forms Add-On-Paket nach der Installation von AEM Service Pack, Cumulative Service Pack oder Feature Pack zu installieren.

Sie können das CFP-Paket direkt von der Softwareverteilung herunterladen oder die folgenden Schritte ausführen:

1. Öffnen Sie [Software-Distribution](https://experience.adobe.com/downloads). Zum Anmelden bei Software Distribution benötigen Sie eine Adobe ID.
1. Tippen Sie im Kopfzeilenmenü auf **[!UICONTROL Adobe Experience Manager]**.
1. Tippen Sie auf den Paketnamen, wählen Sie **[!UICONTROL EULA-Begriffe akzeptieren]** und tippen Sie auf **[!UICONTROL Herunterladen]**.

## Installationsanweisungen für CFP {#installation-instructions-for-cfp}

Dieser Abschnitt erläutert die Anforderungen und Schritte zur Installation von CFP.

### Vor der Installation  {#before-you-install}

>[!NOTE]
>
>Die von Adobe bereitgestellten optionalen Funktionspakete hängen von der Release-Version und dem Cumulative Fix Pack ab. Wenn Sie ein Feature Pack installiert haben, wenden Sie sich bitte an den [AEM Kundendienst](https://helpx.adobe.com/de/marketing-cloud/contact-support.html), um die Kompatibilität mit diesem Cumulative Fix Pack für AEM 6.2 zu überprüfen.

>[!NOTE]
>
>Es wird empfohlen, die Überprüfung für jedes neue Installationspaket auszuführen, bevor Sie versuchen, das Paket zu installieren. Vor der Überprüfung werden alle Fehler analysiert und berichtet, die vor der Installation gefunden wurden, und die Benutzer werden proaktiv vor solchen Fehlern, Überlagerungen und Berechtigungen gewarnt.
>
>Sie können unter [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator) auf die Dokumentation für die Option &quot;Validate&quot;zugreifen.

* AEM 6.2 Service Pack 1 ist eine Voraussetzung für die GFP. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).

* Der kumulative Fix Pack-Download ist unter [Software-Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) verfügbar, auf den Sie direkt von der AEM zugreifen können.
* Bei einer Clusterbereitstellung mit ( RDBMK oder MongoDB) kann das CFP-Paket auf einer der Autoreninstanzen installiert werden, die Package Manager verwenden.

* Bevor Sie das Cumulative Fix Pack installieren, stellen Sie sicher, dass Sie einen Schnappschuss oder eine Sicherungskopie Ihrer AEM-Instanz erstellen.
* Die Deinstallation von CFP wird nicht unterstützt.

### Installieren Sie die CFP über die Softwareverteilung {#install-the-cfp-via-package-share}

Führen Sie die folgenden Schritte aus, um das Cumulative Fix Pack auf einer vorhandenen AEM 6.2 SP1-Instanz zu installieren:

1. Klicken Sie auf den Link [Software-Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip), um das Paket herunterzuladen.

1. Öffnen Sie [Package Manager](http://localhost:4502/crx/packmgr/index.jsp) und klicken Sie auf **[!UICONTROL Paket hochladen]**, um das Paket hochzuladen.

1. Wählen Sie den Paketnamen und klicken Sie auf **[!UICONTROL Install]**.

### Automatische Installation {#automatic-installation}

CFP kann wie folgt automatisch in einer laufenden Instanz installiert werden:

* Platzieren Sie das Paket in ../crx-quickstart/install, während der Server ausgeführt wird. Das Paket wird automatisch installiert.
* Verwenden Sie die [HTTP-API von Package Manager](https://helpx.adobe.com/de/experience-manager/6-2/sites/administering/using/package-manager.html) - stellen Sie sicher, dass Sie `cmd=install&recursive=true` verwenden - damit das verschachtelte Paket installiert ist.

### Bestätigen der Installation {#validate-installation}

1. Auf der Seite &quot;Produktinformationen&quot;(/system/console/productinfo ) sollte nun die aktualisierte Versionszeichenfolge &quot;Adobe Experience Manager, Version 6.2.0.SP1-CFP20&quot;unter &quot;Installierte Produkte&quot;angezeigt werden.
1. Alle OSGI-Bundles sind in der OSGI-Konsole entweder AKTIV oder FRAGMENT. (Verwenden Sie die Webkonsole: /system/console/bundles.)

>[!NOTE]
>
>Bei erfolgreicher Installation des Pakets wird eine Informationsmeldung angezeigt, die angibt, dass das Inhaltspaket erfolgreich installiert wurde, z. B. &quot;Inhaltspaket AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 erfolgreich installiert&quot;.

>[!NOTE]
>
>Seit AEM 6.2 SP1-CFP1 hat sich die Protokollierungsstufe in Jackrabbit FileVault für die meisten Meldungen von INFO in DEBUG geändert. Um Installationsprotokolle für ein auf AEM 6.2 SP1-CFP1 oder höher installiertes Inhaltspaket abzurufen, aktivieren Sie die DEBUG-Protokollierungsstufe für `org.apache.jackrabbit.vault.packaging.impl`.

### Installieren von AEM Forms {#install-forms}

>[!NOTE]
>
>Überspringen Sie diesen Abschnitt, wenn Sie AEM Forms nicht verwenden.

#### AEM Forms-Add-on installieren  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**Nur AEM Forms auf JEE**) Das Verfahren zum Installieren einer CFP auf AEM Forms on JEE wird unter [Installieren von CFP auf AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee) beschrieben.

1. Vergewissern Sie sich, dass Sie das AEM 6.2 SP1 CFP-Paket installiert haben.
1. Laden Sie das entsprechende Forms Add-On-Paket herunter, das unter [AEM Forms-Versionen](aem-forms-releases.md) für Ihr Betriebssystem aufgeführt ist.
1. Installieren Sie das Forms Add-On-Paket, wie unter [Installieren AEM Forms Add-On-Pakete](https://helpx.adobe.com/de/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html) beschrieben.

#### Installieren des AEM Forms JEE-Bundles-Pakets {#install-aem-forms-jee-bundles-package}

Fehlerbehebungen in AEM Forms JEE werden über ein separates Installationsprogramm bereitgestellt. Informationen zum Installieren einer CFP auf AEM Forms on JEE finden Sie unter [Installieren von CFP auf AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Forms Designer-Installationsprogramm  {#designer-installer}

1. Um das Update zu installieren, führen Sie die Datei Designer6.2.0__Cumulative_QF.msp aus.
1. Klicken Sie auf dem Begrüßungsbildschirm auf **Aktualisieren**. Die Installation wird gestartet.
1. Klicken Sie nach Abschluss der Installation auf **Beenden**.

## Benutzerkonfigurierte Zeitüberschreitungsparameter für DTM, Analytics, Zielgruppe, Search &amp; Promote-Verbindungen {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Mit AEM Cumulative Fix Pack 6.2 SP1-CFP7 und späteren Versionen wurden Zeiträume für die Zeitüberschreitung von Verbindungen für alle oben genannten Verbindungen gemäß den unten stehenden Details konfiguriert:

| **Verbindungen** | **Verbindungs-Zeitüberschreitung*** | **Socket-Timeout**** |
|---|---|---|
| DTM | 30000ms | 30000 ms |
| Analyse | 30000 ms | 30000 ms |
| Target | 60000ms | 30000 ms |
| Search&amp;Promote | 30000 ms | 30000 ms |

* **Zeitüberschreitung der Verbindung***- Zeitüberschreitung in Millisekunden, bis eine Verbindung hergestellt ist. Ein Timeout-Wert von null wird als unendlicher Timeout interpretiert.
* **Socket-Timeout****- Timeout in Millisekunden, um auf Daten zu warten, oder eine maximale Inaktivität zwischen zwei aufeinander folgenden Datenpaketen.

>[!NOTE]
>
>Bei AEM Cumulative Fix Pack 6.2 SP1-CFP6 und späteren Versionen ist die OSGi-Konfiguration, die für die Search &amp; Promote-Integration verwendet wird, die Apache HTTP-Komponenten-Proxy-Konfiguration. Die Proxy-Konfiguration von Day Commons HTTP Client 3.1 wird nicht mehr verwendet.

## Deaktivieren des Replikationsstatus in der Tagging-Konsole (Classic UI) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Falls Sie CFP3 oder höher verwenden, führen Sie die folgenden Anweisungen aus, um den Replizierungsstatus in der Tagging-Konsole der klassischen Benutzeroberfläche zu deaktivieren:

* Überlagerung *&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;* in */apps*

* hinzufügen `replicationStateRequired`: &quot;false&quot;nach Zeile 416.

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## Das neueste Java 8 Update 131 gibt eine Ausnahme aus (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Diese Konfigurationseinstellungen gelten für AEM Forms-Kunden, die Dokument Security verwenden.

NPR-21355 ist in GFP 12.1 enthalten. Wenn Sie CFP12.1 oder höher installieren, führen Sie das folgende Verfahren aus, um NPR-21355 auf dem JBoss-Anwendungsserver zu konfigurieren. Wenn Sie CFP12.1 auf einem AEM Forms-Server installieren, der auf Oracle WebLogic- oder IBM WebSphere-Anwendungsservern ausgeführt wird, ist keine zusätzliche Konfiguration erforderlich:

1. Sichern, löschen und erstellen Sie die neue Datei &quot;module.xml&quot;. Der Standardspeicherort der Datei ist [AEM_Forms_Installationsordner]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. Öffnen Sie die neu erstellte Datei &quot;module.xml&quot;zur Bearbeitung. Fügen Sie der Datei „“ den folgenden Code hinzu:

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. Erstellen Sie eine Sicherung der Dateien &quot;jsafeFIPS.jar&quot;, &quot;jsafeJCEFIPS.jar&quot;und &quot;certjFIPS.jar&quot;unter [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ und löschen Sie die Dateien aus dem oben genannten Ordner.

   Wenden Sie sich an [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html), um neue JAR-Dateien zu erhalten. Platzieren Sie die JAR-Dateien, die Sie von [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) erhalten haben, unter [AEM_Forms_Installationsordner]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Nur Windows) Ändern Sie die Konfigurationsdateien `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` oder `domain.conf.bat`:

   * Für JBoss-Server in eigenständiger Konfiguration öffnen Sie die Datei &quot;standalone.conf.bat&quot;zur Bearbeitung.
   * Für JBoss-Server in der Clusterkonfiguration öffnen Sie domain.conf.bat zur Bearbeitung.

   hinzufügen Sie die folgenden Zeilen am Ende und speichern Sie die Datei:

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. (Nur Linux-Betriebssystem) Ändern Sie die Konfigurationsdateien [AEM_Forms_Installation_directory]/jboss/standalone.conf oder domain.conf:

   * Für JBoss-Server in eigenständiger Konfiguration öffnen Sie die Datei &quot;standalone.conf&quot;zur Bearbeitung.
   * Für JBoss-Server in der Clusterkonfiguration öffnen Sie domain.conf zur Bearbeitung.

   hinzufügen Sie die folgenden Zeilen am Ende und speichern Sie die Datei:

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## Für NPR-19778 erforderliche Konfigurationseinstellungen {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Der NPR-19778 ist Teil der GFP14.

Die Anzahl freigegebener Warteschlangen wird für andere Benutzer nicht standardmäßig aktualisiert, wenn ein Benutzer eine Aufgabe beantragt. Dafür haben wir eine neue Eigenschaft eingeführt. Gehen Sie wie folgt vor, um diese Eigenschaft in Ihrer AEM zu konfigurieren:

1. Gehen Sie zu Admin-Benutzeroberfläche -> Dienste -> Arbeitsbereich -> Globale Verwaltung.
1. Globale Einstellungen exportieren.
1. Fügen Sie in der heruntergeladenen XML-Datei das Tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>` Hier ist 10 der Beispielwert in Sekunden. Sie können sie entsprechend ändern.
1. Speichern Sie die Datei .
1. Gehen Sie zurück zur Admin-Benutzeroberfläche -> Dienste -> Arbeitsbereich -> Globale Verwaltung.
1. Importieren Sie die XML-Datei im Abschnitt &quot;Globale Einstellungen importieren&quot;.
1. Sie können sich jetzt vom System abmelden und sich erneut anmelden.
1. Die Anzahl der Beginn für freigegebene Warteschlangen, die für andere Benutzer im Arbeitsbereich aktualisiert werden.
1. Um die Abfrage zu deaktivieren, ändern Sie den Wert in 0 und importieren Sie die XML-Datei erneut.

## UI-Änderungen {#ui-changes}

* Verhaltensänderung bei der Anzeige von Titeln auf der Grafikkarte für das Bild mit dc: title-Eigenschaft auf String [] ( multifield ) eingestellt: Nur der zuletzt geänderte Titel wird auf der Grafikkarte in der Benutzeroberfläche angezeigt, obwohl alle Titel in CRX gespeichert werden. Hotfix für CQ-4217165

## Bekannte Probleme {#known-issues}

* Durch die Aktualisierung von AEM 6.2SP1-CFP19 und AEM 6.2SP1-CFP20 von CFP18 wird die Root-Umleitung zur Startseite der klassischen Benutzeroberfläche statt zu /sites.html/content geändert. Eventuell müssen Sie das Sling korrigieren: zielgruppe-Eigenschaft von /welcome.html bis /index.html mit CRX Explorer. Dieses Problem wird beim Aktualisieren von CFP17 oder älteren Versionen nicht behoben.

Die folgenden vorübergehenden Fehler können auftreten, wenn Sie AEM 6.2 SP1-CFPx installieren. Für diese Fehler ist jedoch keine Auflösung erforderlich, da sie sich nicht auf Ihre AEM Instanz auswirken und nach der Installation von CFP verschwinden:

* Bei der Aktualisierung AEM 6.2SP1-CFP20-Instanz auf AEM 6.5 funktionieren einige Vanity-URLs möglicherweise nicht wie:

   * */projects.html*
   * */sites.html*

Die Lösung besteht jedoch darin, die AEM Instanz nach einer Aktualisierung neu zu starten.

* HTTP 500 Interner Serverfehler wird empfangen, wenn die Detailseite der Webconsole-Komponente geöffnet wird.
* Fehler, da **Komponenteninstanz erstellen** und **Dienstfactory null** zurückgegeben hat, weil das Repository neu gestartet wird:

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Komponenteninstanz kann nicht erstellt werden, weil die Bindung des Referenz-profileManager fehlgeschlagen ist
   * org.apache.sling.commons.Planung FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service Factory gab null zurück. (Komponente: com.day.cq.tagging.impl.TagGarbageCollector (1687))

* Fehler bei der CFP-Installation in Mongo und DB2: **org.apache.sling.discover.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Ausnahme: java.lang.NullPointerException**. Dieser Fehler tritt nach der Installation einer CFP über CFP8 nicht auf.
* (Adobe Granite Maintenance Planung Update Aufgabe) com.adobe.granite.maintenance.impl.TaskScheduler: Keine Maintenance-Aufgabe mit dem Namen WorkflowPurgeTask für Fenstergranite:wöchentlich
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Wenn Sie CFPx auf AEM 6.2 SP1 installieren, das das Feature Pack für intelligente Tags enthält, wird der zuvor hinzugefügte Workflow-Schritt für intelligente Tag-Assets aus dem DAM Update Asset-Arbeitsablauf gelöscht.

Siehe Liste der bekannten Probleme in AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Probleme).[

## Uber Jar {#uber-jar}

Die Uber-Jar für 6.2 SP1-CFP20 ist unter [Adobe Public Maven Repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/) verfügbar.

Um das Uber Jar in einem Maven-Projekt zu verwenden, beziehen Sie folgende Abhängigkeit in Ihr Projekt-POM ein:

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## OSGI-Bundles und Inhaltspakete sind enthalten{#osgi-bundles-and-content-packages-included-5}

Der folgende Text Dokumente die Liste von OSGI-Bundles und Inhaltspaketen, die in der CFP enthalten sind.

* [Liste der OSGi-Pakete, die in AEM 6.2 SP1-CFP20 enthalten sind](assets/do-not-localize/updated.txt)
* [Liste der in AEM 6.2SP1-CFP20 enthaltenen Inhaltspakete](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 Hotfixes-Seite](https://helpx.adobe.com/de/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1 Versionshinweise](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2 – Versionshinweise](https://docs.adobe.com/docs/de/aem/6-2/release-notes.html)
>* [AEM-Produktseite](http://www.adobe.com/de/solutions/web-experience-management.html)
>* [Dokumentation zu AEM 6.2](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [Produktaktualisierungen mit Priorität ](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) für  [Adoben abonnieren](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

