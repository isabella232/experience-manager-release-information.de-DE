---
title: AEM 6.3 Cumulative Fix Pack
description: AEM 6.3 Versionshinweise zum Cumulative Fix Pack
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: 894a2a98b9d1a135a2f488f2167ec3302c122339
workflow-type: tm+mt
source-wordcount: '15916'
ht-degree: 99%

---

# AEM 6.3 Versionshinweise zum Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Versionsinformationen {#release-information}

| **Produkt** | Adobe Experience Manager |
|---|---|
| **Version** | 6.3 |
| **Release** | Cumulative Fix Pack 6.3.3.8 auf [PackageShare](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8), [Software Distribution (Beta)](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Voraussetzung** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/de/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **Allgemeine Verfügbarkeit** | 5. März 2020 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe hat ein Modell für die einmalige Bereitstellung für die Veröffentlichung von Fehlerbehebungen eingeführt. Anstatt Hotfixes für einzelne Probleme freizugeben, veröffentlicht Adobe jetzt jeden Monat ein Cumulative Fix Pack (CFP) (vorbehaltlich erfolgreicher Qualitätsprüfungen). Ein CFP ist ein aggregiertes Inhaltspaket für mehrere Fehlerbehebungen. CFPs enthalten in erster Linie Fehlerbehebungen, können aber auch Feature Packs enthalten. Sie haben folgende Vorteile gegenüber einzelnen Hotfix-Versionen:

* Kumulierter Charakter (ein CFP enthält beispielsweise Korrekturen, die über frühere CFPs geliefert wurden)
* Erhöhte Qualitätssicherung
* Vereinfachte Installation (Benutzer installieren CFPs als einzelnes Paket ohne Abhängigkeiten, abgesehen vom neuesten Service-Pack)

Weitere Informationen zu CFPs und anderen Versionstypen finden Sie unter [Definitionen von Wartungsversionen](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html).

## Informationen zur Version {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.8 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.20 aktualisiert.

>[!CAUTION]
>
>Die Anwendung von CFPs ohne Überprüfung der Kompatibilität zwischen installierten Feature Packs kann zu einem Systemausfall oder zum Verlust benutzerdefinierter Konfigurationen führen, bei denen die Wiederherstellung von der Sicherung bis zur Behebung erforderlich sein könnte.

>[!NOTE]
>
>Für AEM-Instanzen mit einer Version unter 6.3.3.0 empfiehlt Adobe für Kunden, die eine große Anzahl von Benutzern auf einer AEM-Instanz haben, die Bereitstellung von SPs/CFPs über den Installationsordner.

>[!NOTE]
>
>MongoDB Enterprise 3.6 wird ab AEM-Version 6.3.3.1 unterstützt.

## Liste der Probleme {#changes}

In diesem Abschnitt werden alle im aktuellen CFP enthaltenen Probleme und Hotfixes aufgeführt.

Darüber hinaus enthält dieses CFP Hotfixes, die in [früheren Cumulative Fix Packs](#previous) bereitgestellt wurden.

### Assets {#assets}

* Auf der Seite „Zu Sammlung hinzufügen“ werden nicht alle verfügbaren Sammlungen in der Kartenansicht angezeigt, während Assets zur Sammlung hinzugefügt werden (NPR-32537).

### Sites {#sites}

* Wenn Sie einen Parameter und eine darin enthaltene Komponente auswählen und den Tastaturbefehl zum Löschen ausgewählter Elemente verwenden, werden sowohl die Komponente als auch das übergeordnete parsys-Element gelöscht (NPR-32071).
* Wenn die Eigenschaften einer Seite gespeichert werden, wird ein falscher Knoten erstellt (NPR-31774).

### Integrationen {#integrations}

* ReportSuitesServlet ist anfällig für SSRF (NPR-32162).

### Kampagnen-Targeting {#campaign-targeting}

* Der Inhalt einer Komponente, die in der Autoreninstanz geändert und dann aktiviert wurde, ist in der Veröffentlichungsinstanz erst sichtbar, wenn die Komponente neu gestartet wird **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 und NPR-32232).
* Contexthub-Performances stürzen beim Veröffentlichen ab (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O ist nicht in Adobe Experience Manager 6.3 for Brand Portal (NPR-32056) integriert.

### Formulare {#forms}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

#### Forms-Add-on-Paket {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms-Add-on-Pakete helfen, die Formularfunktionalität mit AEM Service Packs und Cumulative Fix Packs abzustimmen. Daher ist es unerlässlich, das AEM Forms Add-on-Paket nach der Installation eines AEM Service Packs, Cumulative Fix Packs oder Feature Packs zu installieren.

* Designer: Wenn die Tagging-Option aktiviert ist, ist der Rand des Teilformulars in der generierten PDF-Ausgabe nicht sichtbar (NPR-32324 und NPR-32545).
* Designer: Wenn eine Tabelle zusammengeführte Zellen enthält, schlägt der Barrierefreiheitstest für die Ausgabe-PDF-Datei fehl, die mithilfe des Ausgabe-Service aus einem XDP-Formular konvertiert wurde (NPR-32068).
* Document Security: Eine geschützte PDF-Datei kann nicht offline geöffnet werden, wenn die `DisableGlobalOfflineSynchronizationData`-Option auf `True` eingestellt ist (NPR-32080).

## Hotfixes und Feature Packs, die in früheren Cumulative Fix Packs enthalten waren {#previous}

### Cumulative Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.7 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Assets {#assets-1}

* Assets, die ausgewählt wurden (in der Spaltenansicht in der Touch-optimierten Benutzeroberfläche), bevor Sie die Filteroption aus der Dropdown-Liste „Nur Inhalt“ und dann die Option „Verschieben“ auswählen, werden ebenfalls verschoben (NPR-30693).
* Die `${extension}`-Variable wird bei der Workflow-Verarbeitung nicht in der Autoreninstanz gerendert (NPR-31694).
* Der für den Modus „Dynamic Media Hybrid“ konfigurierte Wert zum Ablauf (Client-Cache-Zeit bis zum Livestream) wird nicht in die Umgebung für die Bereitstellung von Dynamic Media repliziert (NPR-31114).
* Assets werden von der Autoreninstanz, die mit der Bereitstellung „Dynamic Media – Scene7“ ausgeführt wird, auch nach Verwendung von Standardfiltern in die Veröffentlichungsinstanz repliziert (NPR-30856).

### Sites {#sites-1}

* Die Seiteneigenschaften einer primären Seite können nicht geladen werden und es wird eine NullPointerException ausgegeben. Das Problem wird durch Hinzufügen der Eigenschaft cq:blueprint behoben (NPR-30901).
* Rollout-Konfigurationen werden nicht ordnungsgemäß aus der blueprintConfig des Root-Knotens abgerufen. Die Deaktivierung wird sowohl für Blueprints als auch für Live Copies ausgelöst. Die Deaktivierung sollte nur für die Blueprint ausgelöst werden (NPR-30866).
* Wenn ein Benutzer einen Seiten-Rollout durchführt, zeigt der Rollout-Konfigurationsdialog doppelte Live Copy-Pfade an (NPR-30438).
* Vorkonfiguriert wendet der Rich-Text-Editor (RTE) die Inline-Schriftgröße unerwartet auf Elemente an (NPR-31283, NPR-30922).
* Die Kampagne in Adobe Campaign mit der vordefinierten Design Importer-Komponente kann nicht synchronisiert werden (NPR-30890).
* Rich-Text-Editor (RTE) erlaubt es nicht, eine eingebettete Tabelle als Listenelement einzufügen (NPR-30878).
* Wenn ein Benutzer den Fokus auf Felder in der linken Schiene legt und zum Einfügen von Inhalten einen Tastaturbefehl verwendet, wird der Inhalt der Zwischenablage des Seiteneditors anstelle des Inhalts eingefügt, der aus den Feldern der linken Schiene kopiert wurde (NPR-31173).
* Wenn ein Benutzer ein Inhaltsfragment bearbeitet, wird die bereits gelöschte Variante des Inhaltsfragments wiederhergestellt (NPR-31272).
* AEM-Site verfügt nicht über die Möglichkeit, eine Sprachkopie zu erstellen (NPR-30690).
* Die Aktionen des Seiteneditors verfügen nicht über die Steuerelemente für den Rollout von Live Copies (NPR-30613).

### Communities {#communities}

* Die Titel der Aktivitäten und Benachrichtigungen sind inkonsistent (NPR-30940).
* Analytics-Berichte werden nicht in der AEM-Autorenumgebung ausgefüllt, eine leere Seite wird angezeigt (NPR-30905).
* Die Paginierung in Communities Blogs funktioniert nicht richtig (NPR-30827).

### Foundation {#foundation}

* Aktualisierungen der Puffergrößenkonfiguration für den Jetty-basierten HTTP-Service werden nicht gespeichert (NPR-30925).

### Forms {#forms-1}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms-Add-on-Pakete helfen, die Formularfunktionalität mit AEM Service Packs und Cumulative Fix Packs abzustimmen. Daher ist es unerlässlich, das AEM Forms Add-on-Paket nach der Installation eines AEM Service Packs, Cumulative Fix Packs oder Feature Packs zu installieren.

#### Adaptive Formulare {#adaptive-forms}

* Gleitkommawerte, die mit einem Skript berechnet werden, werden in einem Formular, das Teil eines Formularsatzes ist, nicht korrekt angezeigt (NPR-30802).

#### HTML5-Formulare {#html-forms}

* Beim Generieren einer HTML5-Vorschau eines XDP-Formulars tritt Flackern auf, während Instanzen eines Teilformulars hinzugefügt werden (NPR-30908).

### Forms JEE-Installationsprogramm {#forms-jee-installer}

#### Document Services {#document-services}

* OutputService zeigt eine falsche Antwort an, nachdem ein Patch zur Behebung von HTML-zu-PDF-Problemen angewendet wurde (NPR-31504).

#### PDFG Service {#pdfg-service}

* Max. Wiederverwendungs-Anzahl mit JMX-Konsole wird für den HTML2PDF-Service nicht angezeigt (NPR-30305).

#### Foundation JEE  {#foundation-jee}

* Max. Wiederverwendungs-Anzahl mit JMX-Konsole wird für den HTML2PDF-Service nicht angezeigt (NPR-30136).

### Cumulative Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.6 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Assets {#assets-2}

* Bei der Videoaggregation nach dynamischem Video werden nur die 100 wichtigsten Elemente in der Ergebnismenge zurückgegeben. NPR-30441; Hotfix für CQ-4213561
* Problem bei der Verbindung mit Adobe Smart-Tag über DataPower. NPR-30026: Hotfix für CQ-4269457
* Enthält ein Archiv einen Ordner mit einem Prozentzeichen (%) im Namen, kann es über die Assets-Oberfläche nicht entpackt werden. NPR-29989: Hotfix für CQ-4270467
* Die Verarbeitung von Sub-Assets großer PDF-Dateien führt zu einer OutOfMemoryError-Ausnahme (OOME). NPR-29851: Hotfix für CQ-4269574

### Sites {#sites-2}

* ContextHub-Fehler während der AEM- und Campaign-Integration. NPR-30624: Hotfix für CQ-4250790
* Für Assets gespeicherte „onTime“- oder „offTime“-Metadateneigenschaften werden nicht abgerufen, wenn der AEM-Server neu gestartet wird. NPR-30412: Hotfix für CQ-4272784
* Beim Generieren eines CSV-Exports wird der Bericht durch Hinzufügen benutzerdefinierter Spalten für die Listenansicht beschädigt. NPR-30208: Hotfix für CQ-4273344
* OOTB-Berichte in „/etc/reports/“ funktionieren nicht ordnungsgemäß und historische Datendiagramme werden nicht angezeigt. NPR-30016: Hotfix für CQ-4220180
* Der Wert des Abfrageparameters „resourceType“ wird in den Wert eines HTML-Tag-Attributs kopiert, das in doppelte Anführungszeichen eingeschlossen ist. NPR-29832: Hotfix für CQ-4255365

### Communities {#communities-1}

* Problem mit doppelten Inhalten in der AEM Communities-Moderationskonsole. NPR-30667: Hotfix für CQ-4276829

### Übersetzung {#translation}

* Übersetzungsfehler - Nur einige wenige Komponenten werden mit maschineller Übersetzung übersetzt. NPR-30079: Hotfix für CQ-4273764
* Wenn Sie das Übersetzungs-Framework verwenden, löst das Hinzufügen von Seiten zu mehreren Übersetzungsaufträgen einen Fehler aus. NPR-29746: Hotfix für CQ-4270953

### Forms {#forms-2}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms-Add-on-Pakete helfen, die Formularfunktionalität mit AEM Service Packs und Cumulative Fix Packs abzustimmen. Daher ist es unerlässlich, das AEM Forms Add-on-Paket nach der Installation eines AEM Service Packs, Cumulative Fix Packs oder Feature Packs zu installieren.

#### HTML5-Formulare {#html-forms-1}

* Wird im Durchsuchen-Modus „NonVisual Desktop Access“ zum Lesen eines HTML5-Formulars verwendet, liest der Chrome-Browser vor jeder skalierbaren Vektorgrafik (SVG) im Formularentwurf das Wort „Grafik“. NPR-30451: Hotfix für CQ-4274732

#### Forms - Backend-Integration {#forms-backend-integration}

* Service/Datenquelle für die Datenbankverbindung konnte beim Erstellen des Formulardatenmodells (FDM) nicht angezeigt werden. NPR-30108: Hotfix für CQ-4273359

### Forms JEE-Installationsprogramm {#forms-jee-installer-1}

#### Forms - Document Services {#forms-document-services}

* Wenn ein Ladetest für den HTML-zu-PDF-Service ausgeführt wird, schlägt er mit einem Fehler fehl und die Dateitypeinstellungen werden vom AEM Forms-Server entfernt. NPR-30111, NPR-30086: Hotfix für CQ-4271495

### Cumulative Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.5 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.17 aktualisiert.

### Assets {#assets-3}

* Die DAM DMGateway-Schnittstelle bietet jetzt Unterstützung für S3 Multipart. NPR-29740: Hotfix für Q-4226303
* Eine Bildwiedergabe für ein Video-Asset kann nicht von der Seite mit den Asset-Details gelöscht werden. NPR-29417: Hotfix für CQ-4268675
* Der Inhaber kann keinen privaten Ordner in einem privaten Ordner erstellen. NPR-29397: Hotfix für CQ-4229830
* Beim Hochladen einer Adobe Illustrator-Grafikdatei mit mehr als 2 GB tritt ein Java-Heap-Space-Fehler auf. NPR-29265: Hotfix für CQ-4226217
* Assets können nicht mehr verwendet werden, nachdem der DAM CQ Mime Type Service Text für m3u8 angewendet hat. NPR-29259: Hotfix für CQ-4264052
* Option „Erstellen“ funktioniert nicht, wenn versucht wird, Sammlungen in Edge zu erstellen. NPR-29248: Hotfix für CQ-4265699 und CQ-4265438
* Asset Link Share zeigt leere graue Karten für einige Assets im Ordner an. NPR-29831: Hotfix für CQ-4270187
* Die neuen Tags, die zu Assets hinzugefügt wurden, können nicht gespeichert und aus den Eigenschaften entfernt werden. Hotfix für CQ-4271931, CQ-4270476

### Sites {#sites-3}

* Bei Verwendung von CoralUI für Multifield wird fileReferenceParameter auf Komponentenebene statt auf Multifield-Ebene abgelegt. NPR-29535: Hotfix für CQ-4266129
* Problem beim Vergleich der neuesten und aktuellen Seitenversion in AEM 6.3.3.3. NPR-29532: Hotfix für CQ-4269639
* Das Pfadfeld wird unabhängig vom Pfad, der für die Suche angegeben ist, am Stammpfad geöffnet. NPR-29398: Hotfix für CQ-4268897
* (Experience Fragments) FacebookApplication#setUpApp verwendet eine veraltete API, die nicht mehr funktioniert. NPR-29213: Hotfix für CQ-4266630
* Beim Hinzufügen von Komponenten zur WCM-Seite wird eine Fehlerwarnung erzeugt, wenn die Minimierung in der Instanz aktiviert ist. NPR-29476: Hotfix für CQ-4266197
* Leere Eigenschaften und mehrere Eigenschaften werden beim Rollout nicht von Blueprint übertragen. Live Copy mit Blueprint zurücksetzen funktioniert nicht bei Komponenten. NPR-29252: Hotfix für CQ-4264928, CQ-4264926, CQ-4267722
* Die Minimierung des Rich-Text-Editors im Vollbildmodus im Quellbearbeitungsmodus führt zum Verlust von Inhalten. NPR-28838: Hotfix für CQ-4260584

### Communities {#communities-2}

* Besucher und Mitglieder, die keine Moderatorenrechte haben, können nicht genehmigte und ausstehende Beiträge durch Einfügen der URL sehen. NPR-29726: Hotfix für CQ-4271124
* Bei der Community-Benutzeranmeldung kommt es zu langsamen Reaktionszeiten von mitunter 40–50 Sekunden. NPR-29679: Hotfix für CQ-4269444
* Das Kennwort kann nicht zurückgesetzt werden, wenn der Benutzer mit einem anderen Benutzernamen und einer anderen E-Mail-Adresse angemeldet ist, da der Schlüssel mit einem ausgetauschten Benutzernamen und einer getauschten E-Mail generiert zu werden scheint. NPR-29281: Hotfix für CQ-4268694

### Experience Fragments {#experience-fragments}

* Experience Fragments können nicht als Ziel exportiert werden, wenn die intelligente Bildkomponente verwendet wird. Hotfix für CQ-4269606

### Replikation {#replication}

* Die Komponente „Replikationsagent“ ist anfällig für eine Sicherheitslücke, die nicht autorisierten Benutzern vertrauliche Informationen offenlegt. NPR-29613: Hotfix für Granite-25070
* Vom Benutzer bereitgestellte Daten werden bei der Ausgabe in der Komponente `cq/replication/components/agent` nicht ausgegeben, was zu einer gespeicherten Cross-Site-Scripting- (XSS)-Schwachstelle führt. NPR-29452: Hotfix für CQ-4266263

### Forms {#forms-3}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

### Forms-Add-on-Paket {#forms-add-on-package-3}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms-Add-on-Paket.

### Forms JEE-Installationsprogramm {#forms-jee-installer-2}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

### In Version 6.3.3.5 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in}

Liste der in AEM 6.3.3.5 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_5-bundle-list.txt)

Liste der in AEM 6.3.3.5 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_packages6335.txt)

### Cumulative Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.4 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.16 aktualisiert.
* Socket-Timeout- und Verbindungs-Timeout-Funktion in den Replikationsagenten von Brand Portal hinzugefügt.

### Assets {#assets-4}

* Wenn ein Archiv mit demselben Namen erneut hochgeladen wird, werden für die neuen verarbeiteten Assets keine Darstellungen generiert. NPR-28643: Hotfix für CQ-4262286
* Workflow CommandLineProcess schlägt fehl, wenn der Dateiname ein einfaches Anführungszeichen enthält. NPR-28805: Hotfix für CQ-4262287
* Die Werte unterscheiden sich zwischen der Sammlungsseite und der Sammlungsseite mit Filter. NPR-28642: Hotfix für CQ-4261405
* CommitFailedException löst das Hochladen großer ZIP-Archivelemente aus. NPR-28528: Hotfix für CQ-4260903
* Ordner-Metadaten können nicht gespeichert werden, wenn ein Ordner mit Sonderzeichen bearbeitet wird. NPR-28211: Hotfix für CQ-4260401
* Es ist nicht möglich, Bildwiedergaben eines Video-Assets von der Asset-Details-Seite zu löschen. NPR-29149: Hotfix für CQ-4266073
* Bei der Bereitstellung von DMS7-Desktop-Videos mit DMComponent wird progressives Herunterladen zur Wiedergabe von Videos im Veröffentlichungsmodus verwendet und kein Streaming durchgeführt. NPR-28754: Hotfix für CQ-4263732
* Bildvorgaben können nicht erstellt/bearbeitet werden, da die eingeschränkten Zugriffsrechte auf Funktionen von /etc/dam/video/dynamicmedia für Image Manager deaktivieren. NPR-28662: Hotfix für CQ-4263022
* Die Linkfreigabe mit DMS7-kodierten Videodateien führt zu leeren Ordnern. NPR-28851: Hotfix für CQ-4206743
* Die Replizierung von AEM zu Brand Portal wird über lange Zeit blockiert. NPR-28913: Hotfix für CQ-4254932

### Communities {#communities-3}

* Nachrichten mit Anlagen in den Outlook-Ordnern „sent“ und „inbox“ können nicht geöffnet werden. NPR-28559: Hotfix für CQ-4217072

### Sites {#sites-4}

* Cross-Site-Scripting (XSS) in SuggestionHandler für 6.3. NPR-28692: Hotfix für CQ-4253821
* Deep-Rollout endet, ohne dass alle Verzweigungen in der jeweiligen LiveCopy enthalten sind. NPR-29175: Hotfix für CQ-4239472
* (MSM) Implementieren von LiveCopyIndex mithilfe von oak-index. NPR-29198: Hotfix für CQ-4222472
* Die Datei „coral.js“ enthält eine anfällige Version der Bibliothek „handlebars.js“. NPR-26973: Hotfix für CQ-4255377
* Bei Verwendung einer Target-Komponente mit einem verschachtelten Layout-Container und einer Textkomponente wird der JavaScript-Fehler „Eigenschaft currentPos von Null kann nicht gelesen werden“ ausgegeben, wenn Sie Text bearbeiten oder auf den Container klicken. NPR-29077: Hotfix für CQ-4246594
* (Touch-optimierte Benutzeroberfläche) Die Aktualisierung von Tags auf Seiten, die bereits mit anderen Tags versehen sind, kann nicht als Massenaktualisierung durchgeführt werden. NPR-28729: Hotfix für CQ-4262922
* Das Öffnen der Variante in der Kartenansicht führt zu einem 500-Fehler. NPR-28611: Hotfix für CQ-4263571
* Das Rollout einer Struktur, die in einer primären Version verschoben wurde, führt zu einem falschen cq:moveTarget. NPR-28968: Hotfix für CQ-4265280

### Integration {#integration}

* (Cloud Service Config) Das Kontrollkästchen „geerbt von“ auf der Stammebene sollte entfernt werden. NPR-28771: Hotfix für CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler wird in eine unendliche Schleife verschoben und führt bei Veröffentlichungsinstanzen zu Aktualisierungen der Knoten. NPR-28561: Hotfix für CQ-4263096
* Die Verwendung der Brightedge-Berechtigung schlägt mit einem Verbindungsfehler fehl. NPR-29167: Hotfix für CQ-4265872
* Kompilierungsproblem in OfferproxyTandtProvider.java aufgrund fehlender Importanweisung für die „Resource“-Klasse: Fehlende Importanweisung: import org.apache.sling.api.resource.Resource. NPR-28772

### Commerce {#commerce}

* Die Option „Sortieren“ funktioniert nicht für Assets in der Commerce-Sammlung. NPR-28755: Hotfix für CQ-4213622

### Jetty {#jetty}

* Jetty-Ausnahmen in error.log für alle 302 Weiterleitungen nach der Installation von CFP2 über 6.3.3. NPR-28606: Backport für CQ-4262844

### Benutzeroberfläche – Foundation {#ui-foundation}

* Durch Klicken auf das Tag wird das globale „Mouseup“-Ereignis entfernt und das Dialogfeld wird im „Drag-Modus“ eingefroren. NPR-28641: Hotfix für CUI-7294

### WCM - MSM {#wcm-msm}

* PushOnModify-Rollout für PageManager-Verschiebung überträgt für zwei Sitzungen wiederholt Daten, wodurch eine Race-Bedingung entsteht. NPR-28880: Hotfix für CQ-4266191

### Schwachstelle {#vulnerability}

* CSRF-Schutz-Framework funktioniert nicht mit AEM Foundation-Formularen. NPR-28612: Hotfix für GRANITE-22231

### Forms {#forms-4}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

Die wichtigsten Highlights für AEM Forms sind:

* Option zur Auswahl der Elemente pro Seite auf der Seite „Ansicht des Richtliniensatzes“ aktiviert.
* Funktion „Warteschlange freigeben“ für alle Browser hinzugefügt.

### Forms-Add-on-Paket {#forms-add-on-package-4}

#### Forms – Workflow {#forms-workflow}

* Die Antwortaufgabe für freigegebene Warteschlangen öffnet ein Flash-Element im HTML5-Arbeitsbereich. NPR-29161: Hotfix für CQ-4266498
* Kann nicht vom Arbeitsbereich gesendet werden, wenn die Schaltfläche Umlaute enthält. NPR-29014: Hotfix für CQ-4263172

#### Forms - Document Security {#forms-document-security}

* Option zur Auswahl der Elemente pro Seite auf der Seite „Ansicht des Richtliniensatzes“ aktivieren. NPR-29243: Hotfix für CQ-4268567 und CQ-4265132

#### Forms - Document Services {#forms-document-services-1}

* OSGi Forms Assembler funktioniert nicht mit Acrobat-Dateien. NPR-29049: Hotfix für CQ-4254426

#### HTML5-Formulare {#html-forms-2}

* Bei der Vorschau einer XDP als PDF und derselben XDP als HTML in Designer tritt unterschiedliches Verhalten auf. NPR-28602: Hotfix für CQ-4260239

### Forms JEE-Installationsprogramm {#forms-jee-installer-3}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

### In Version 6.3.3.4 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-1}

Liste der in AEM 6.3.3.4 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Liste der in AEM 6.3.3.4 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulative Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.3 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.16 aktualisiert.
* Die Paginierung der Richtliniensatzliste ändert sich, um Seiten auf 50 Datensätze zu begrenzen.
* Rep hinzugefügt: Cache in Ignorable-Knoten bei AEM Communities User Sync Listener auf Veröffentlichungsinstanzen.
* Es wurde eine aria-Beschriftung für die Listen- und Kartenansichtsschaltfläche hinzugefügt.
* Es wurde ein Escape-Zeichen für das Komma eingefügt, wenn eine Suche durchgeführt wird.
* Unterstützung synthetischer Ressourcen für die Inhaltsrichtlinie aktiviert.

#### Assets {#assets-5}

* Es können nicht mehrere Dateien des Typs .jp2, .max, .oft, .msg heruntergeladen werden. NPR-28002: Hotfix für CQ-4210856
* Die ImageServer-Veröffentlichungseinstellungen werden nicht für die Hybridauslieferung repliziert. NPR-28329: Hotfix für CQ-4253030

#### Communities {#communities-4}

* Aktivierung der Tastaturnavigation für AEM Communities-Komponenten bei der Veröffentlichung. NPR-27739: Hotfix für CQ-4253856
* Die Tastaturnavigation wurde aktiviert, um die Inhaltswiedergabe auszulösen. NPR-27738: Hotfix für CQ-4254026
* Es wurde eine aria-Beschriftung für die Listen- und Kartenansichtsschaltfläche hinzugefügt. NPR-27736: Hotfix für CQ-4254027
* (Backport) Rep hinzugefügt: Cache in Ignorable-Knoten bei AEM Communities User Sync Listener auf Veröffentlichungsinstanzen. NPR-27841: Hotfix für CQ-4247234
* Sonderzeichen wird auf Benutzeroberflächen-Ebene im Suchfeld ein Escape-Zeichen (\) vorangestellt. NPR-27839: Hotfix für CQ-4259757
* Fehler bei der Suche nach Zeichen wie (, + und ? bei der Schnellsuche. NPR-28212: Hotfix für CQ-4260969
* Kommentare können nicht mit der API im benutzerdefinierten Inhalt gelöscht werden. NPR-28075: Hotfix für CQ-4260534
* Auf der nächsten Seite veröffentlichte Kommentare werden gelb hervorgehoben, wenn ein neuer Kommentar veröffentlicht wird. NPR-28148: Hotfix für CQ-4259681
* Nachrichten mit Anlagen in den Outlook-Ordnern „sent“ und „inbox“ können nicht geöffnet werden. NPR-28559: Hotfix für CQ-4217072

#### Sites {#sites-5}

* Die Ausführung der Versionsbereinigung in AEM 6.3 führt zu einer ständig wiederholten Warnung in den Protokollen. NPR-27750; Hotfix für CQ-4206870
* Das Stil-Plug-in wird im Vollbildmodus des Rich-Text-Editors nicht unterstützt. NPR-27622: Hotfix für CQ-4258674
* Die Liste „loaderPromises“ wird nicht geleert, nachdem der Inhaltsrahmen in editor.js geladen wurde. NPR-27768: Hotfix für CQ-4205337
* Die Vorlagenrichtlinie kann nicht für verschachtelte Parsys-Elemente festgelegt werden, ohne auch für die übergeordnete Komponente festgelegt zu werden. NPR-27987: Hotfix für CQ-4246095
* Der Komponenten-Browser bereinigt Benutzereingaben nicht und kann daher JavaScript-Fehler auslösen. NPR-27986: Hotfix für CQ-4247590
* Die Seite wird leer angezeigt, wenn der Benutzer versucht, das Inhaltsfragment zu bearbeiten. NPR-27669
* Die Hervorhebung der Anmerkung wird ausgeblendet, sobald der Benutzer auf die Anmerkung klickt. BPR-27196: Hotfix für CQ-4254423

#### Integration {#integration-1}

* ResourceResolver löst nicht mehrere Domains für die Target-Komponente auf. NPR-28265: Hotfix für CQ-107847
* Die Aufhebung der LiveCopy-Vererbung funktioniert bei zielgerichteten Behältern nicht ordnungsgemäß, da keine Aktionen angezeigt werden. NPR-28129: Hotfix für CQ-4259813

#### Replikation {#replication-1}

* DispatcherFlushRules lösen die Replikation in 6.3.3.1 aus. NPR-28150: Hotfix für CQ-4261401

#### Campaign - Targeting  {#campaign-targeting-1}

* NullPointerException in TargetedContentManager. Hotfix für CQ-4263485

#### Social - SCORM  {#social-scorm}

* Entfernen des Verweises auf die SCORM-Cloud (Shareable Content Object Reference Model) im Player. Hotfix für CQ-4260779

#### DAM - Allgemeines {#dam-general}

* Download über Link-Share-E-Mail gibt leere/beschädigte ZIP-Datei zurück. Hotfix für CQ-4259686

#### MAC - Test&amp;Target-Integration  {#mac-test-target-integration}

* Die Option „Target-Komponente konfigurieren“ steht für die Zielgruppen außer der Standardzielgruppe nicht zur Verfügung. Hotfix für CQ-4261370

#### Übersetzung {#translation-1}

* Aktivieren der Unterstützung für den MS Translator-Service in AEM 6.3 nach der Aktualisierung von MS Translator auf API-Version 3.0. NPR-28365: Hotfix für CQ-4259096

### Forms {#forms-5}

### Forms-Add-on-Paket {#forms-add-on-package-5}

#### Forms – Workflow {#forms-workflow-1}

* PDF-Formulare können nicht im HTML5-Arbeitsbereich wiedergegeben werden. NPR-28059: Hotfix für CQ-4260373

#### Forms - Document Services {#forms-document-services-2}

* Es können keine Richtliniensätze angezeigt werden, die über die ersten 1000 hinausgehen und in der Ansicht „Policy Sets“ (Richtliniensätze) in der Admin-Konsole aufgeführt sind. NPR-28060, NPR-26047: Hotfix für CQ-4249865
* Eine Ausnahme mit dem Namen „java.lang.IllegalArgumentException message:Keine Enum-Konstante com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE“ wird ausgelöst, die den Abschluss des Prozesses mit kurzer Lebensdauer verhindert. NPR-28652

#### Forms - Adaptive Formulare  {#forms-adaptive-forms}

* In der Dropdown-Liste hinzugefügte/entfernte Elemente werden beim Aktivieren der Kontrollkästchen nicht aktualisiert. NPR-28224: Hotfix für CQ-4252834

### Forms – JEE-Installationsprogramm {#forms-jee-installer-4}

* Keine neuen AEM Forms-Fehlerbehebungen im Forms JEE-Installationsprogramm.

### In Version 6.3.3.3 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-2}

Liste der in AEM 6.3.3.3 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6333_bundle_list.txt)

Liste der in AEM 6.3.3.3 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_list_6333.txt)

### Cumulative Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.2 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter Versionshinweise zu AEM 6.3 Service Pack 3.

Die wichtigsten Highlights des AEM Cumulative Fix Pack sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.15 aktualisiert.
* Unterstützung für die Registerkarte „Regeln“ und deren Durchsetzung im Asset-Ordner im Ordner-Metadatenschema hinzugefügt.
* Unterstützung für Paginierung bei der Gruppenauflistungsseite in der  publish.
* Die unreadCount-Benachrichtigung kann nun mit jeder beliebigen Zahl konfiguriert werden. Standardwert ist 20.
* Fehlerbehebungen in der Prüfung externer Links.

#### Assets {#assets-6}

* Die Dropdown-Liste „Kaskadieren“ wird in dynamischen Dropdown-Listen nicht unterstützt. NPR-27044; Hotfix für CQ-4252564
* Verbessern Sie die Abfrage, um die Funktion „ExpiryNotification“ zu verwenden. NPR-26999: Hotfix für CQ-4251188
* Migration von Regeln vom Metadatenschema zum Metadatenschema des Ordners. NPR-27771: Backport für CQ-4257737, CQ-4257735, CQ-4259822
* Bei der Asset-Referenzanpassung werden Verweise für Assets, die Teil von Sling ResourceCollections sind, nicht aktualisiert. NPR-26759: Hotfix für CQ-4252605
* Download über Link-Share-E-Mail gibt leere/beschädigte ZIP-Datei aus. NPR-27997: Hotfix für CQ-4259686
* Die Hybrid-Videokodierung ist nicht abgeschlossen und es wird keine Miniaturansicht erstellt. NPR-27122: Hotfix für CQ-4255080

#### Sites {#sites-6}

* Aussetzen der übergeordneten Seite entfernt „cq : LiveRelationship mixin type“ von der fehlenden Seite. NPR-26996: Hotfix für CQ-4254113
* (External Link Checker) Interne Links werden auf einzelnen Seiten als beschädigt angezeigt, bei externen Links funktioniert dies jedoch nicht. NPR-27481: Hotfix für CQ-4257780
* Die Cloud Service Config-Vererbung schlägt beim Bearbeiten anderer Seiteneigenschaften fehl. NPR-27311: Hotfix für CQ-4256785
* „Null Pointer“-Ausnahme bei Verwendung eines Kernkomponenten-  Formulars zusammen mit einem Foundation-Formular. NPR-27333: Hotfix für CQ-4249176
* Rich-Text-Editor entfernt das leere Alt-Tag. NPR-26938: Hotfix für CQ-4253267
* (Klassische Benutzeroberfläche) Leistungsprobleme mit selectionchanged-Listener bei mehreren Dropdown-Listen. NPR-27115: Hotfix für CQ-4237215
* Wenn der Rich-Text-Editor mit mehreren Feldern kombiniert wird, lautet der Fehler „Uncaught TypeError: fieldAPI.getName ist keine Funktion beim Fehler foundation.js“. NPR-27146: Hotfix für CQ-4253155, CQ-4259967
* Der Fokus/Cursor bleibt auch dann auf dem Rich-Text-Editor, wenn Sie im Safari-Browser auf ein Optionsfeld klicken. NPR-27144: Hotfix für CQ-4249635
* Die Seite wird leer angezeigt, wenn der Benutzer versucht, das Inhaltsfragment zu bearbeiten. NPR-27669
* Version für Experience Fragments kann nicht erstellt werden. NPR-27689: Hotfix für CQ-4259009

#### Integration {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever durchsucht den gesamten Baum, um die verfügbaren Marken zu sammeln. NPR-27060: Hotfix für CQ-4255790
* Die   cq : -Aktionen werden für eine Targeting-Komponente nicht berücksichtigt. NPR-27616: Hotfix für CQ-4257497

#### Sling {#sling}

* Wird die datengesteuerte Verwendung mit Klassen mit einem identischen Namen verwendet, wird der nicht-obligatorische Code erzeugt. NPR-27282: Hotfix für Sling-7581

#### Commerce {#commerce-1}

* Update auf Apache Felix Http Jetty 4.0.6. NPR-26472: Hotfix für Granite-22916

#### DAM – DM Client {#dam-dm-client}

* Ein Bild wird nach Angabe von Haltepunkten in der Dynamic Media-Komponente nicht angezeigt. Hotfix für CQ-4256168

#### DAM - DMServices  {#dam-dmservices}

* MixedMediaSet mit zugehörigen Videos wird nicht richtig synchronisiert. Hotfix für CQ-4251650
* Wiedergabe im Viewer-Vorgabeneditor für gemischte Mediensets nicht möglich. Hotfix für CQ-4251442

#### DAM - Allgemeines {#dam-general-1}

* Die Verknüpfung zum Inhaltsfragmentmodell fehlt nach der Anwendung des SP3-Patches. Hotfix für CQ-4259029

#### DAM - Benutzeroberfläche  {#dam-ui}

* Die Benutzeroberfläche (UI) des Metadatenschemas für Ordner ist nach der Installation von SP3 beschädigt. Hotfix für CQ-4257737

#### Communities {#communities-5}

* Fügen Sie Paginierungsunterstützung für Gruppenauflistungen bei der Veröffentlichung hinzu. NPR-26953: Hotfix für CQ-4246525
* Bei Ungelesen-Benachrichtigungen kann die Anzahl nicht über 21 sein. NPR-27496: Hotfix für CQ-4252829
* Die Beschränkung für das Benutzerabonnement liegt bei 1000. NPR-27615: Hotfix für CQ-4254689
* Fehler beim Hochladen eines anderen Anhangs als Bild (z. B. .pdf) im Forum. NPR-27375: Hotfix für CQ-4257753
* Link für Antworten funktioniert beim Klicken auf eine Zeile nicht. NPR-24556: Hotfix für CQ-4256138
* Die Beziehungen zu UGC werden nach der Löschung der UGC nicht gelöscht. NPR-27631: Hotfix für CQ-4258706
* Die Suche nach dem Adresswert in der Suchbegriffsuche ist nicht möglich, wenn die Community mit dem Datenbankspeicherressource-Provider (DSRP) eingestellt wurde. NPR-27652: Hotfix für CQ-4253261
* Durch Klicken auf das Papierkorbsymbol im Bild nach der Löschbestätigung wird die Anlage endgültig entfernt. NPR-27340: Hotfix für CQ-4255150
* Forumsbeiträge und -antworten werden über der zweiten Seite hinzugefügt. Bei Aktualisierung wird der Beitrag an die richtige Position auf der ersten Seite verschoben. NPR-27341: Hotfix für CQ-4247338
* Die Statusbeschriftung zum Abschluss der Aktivierungs-Scorm-Ressource wird in der Benutzeroberfläche leer angezeigt. NPR-27152: Hotfix für CQ-4249994
* Wenn Sie „Privilegierte Mitglieder zulassen“ aktivieren, sollten die privilegierten Mitglieder nur Inhalte für Benutzer erstellen können, die Mitglieder der Community sind. NPR-27901: Hotfix für CQ-4251235

#### Unterstützung {#sustenance}

* Die Aktivitätsprotokolle von Package Manager sollten in einer separaten Protokolldatei extrahiert werden. NPR-27323: Hotfix für Granite-14866

#### Übersetzung {#translation-2}

* Übersetzungsvorschau funktioniert nicht mit den „We.Retail“-Beispielinhalten. NPR-27170: Hotfix für CQ-4241179

* Proaktive Fehlerbehebungen für platform.login. NPR-26961
* Speichern und Schließen auf den Seiteneigenschaften kehrt nicht zur  richtigen Seite in AEM WAR mit Tomcat zurück. NPR-27567: Hotfix für Granite-23671

* Der eingegebene Text geht nach dem Speichern durch die Funktion sourceEdit verloren. Hotfix für CQ-4259273

### Forms {#forms-6}

### Forms-Add-on-Paket {#forms-add-on-package-6}

#### Forms - Document Security {#forms-document-security-1}

* Gleichzeitigkeitsproblem mit dem JEE Client SDK. NPR-27572: Hotfix für CQ-4247156

#### Forms - Document Services {#forms-document-services-3}

* Das Erstellen eines auf SOAP basierenden Formulardatenmodells schlägt auf WebSphere fehl. NPR-27692: Hotfix für CQ-4253702

#### Forms - Adaptive Formulare  {#forms-adaptive-forms-1}

* XML-Injection-Schwachstelle mit AEM Forms. NPR-27863: Hotfix für CQ-4257315
* Die AEM Forms Container-Komponente wird unsichtbar, sobald das falsche Formular auf der Website-Seite konfiguriert wurde und das Kontrollkästchen „Formulare decken die gesamte Breite der Seite“ aktiviert ist. NPR-25972: Hotfix für CQ-4239287, CQ-4249133

### Forms JEE-Installationsprogramm {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* Das Erstellen eines auf SOAP basierenden Formulardatenmodells schlägt auf WebSphere fehl. NPR-27692: Hotfix für CQ-4253702

#### Enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included}

Liste der in AEM 6.3.3.2 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/63332bundle_list.txt)

Liste der in AEM 6.3.3.2 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6332content_package.txt)

### Cumulative Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 3 (6.3.3.0) im September 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.3.1 ist von AEM 6.3 Service Pack 3 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.3.x-Paket nach der Installation von AEM 6.3 Service Pack 3 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 3](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.14 aktualisiert.
* Leistungsverbesserungen bei Eigenschaften und Suchen.
* Korrektur des Problems in der FormData-Verarbeitung für den Standardwert.
* FormBuilder wurde auf die neueste Version von Handlebars aktualisiert.
* Das config-Servlet für die Bearbeitungskonfiguration für die RTE im Dialogmodus wurde hinzugefügt.
* Zusätzliche Unterstützung für zusammengesetzte Felder.
* Aktiviert/deaktiviert Symbolleistenelemente des Rich-Text-Editors mit einer Inhaltsrichtlinie für das Bearbeitungsdialogfeld.

#### Assets {#assets-7}

* Bei aktivierter IDS-Entkopplung werden im DAM Update Asset-Arbeitsablauf keine Verknüpfungsreferenzen mehr angezeigt. NPR-26135: Hotfix für CQ-4250933
* Das entpackte Archiv, das vom Entarchivierungsschritt erstellt wurde, mit einem Ordner, der ein % in seinem Namen hat, wird nicht geöffnet. NPR-26275: Hotfix für CQ-4251482
* Ein einfaches Anführungszeichen verhindert die Aktualisierung der Metadaten. NPR-26808: Hotfix für CQ-4254305
* (Omnisearch) Leistungsproblem beim Suchen innerhalb einer Sammlung. NPR-26714: Hotfix für CQ-4253408
* Die Verwendung von GQLConverter mit einer Volltextsuche, die die „OR“-Buchstaben im Text enthält, wird falsch verarbeitet. NPR-26564: Hotfix für CQ-4247362
* Durch das Freigeben des Asset-Links von einem Multi-Mandanten wird die Mandanten-ID als ungültige URL vorgezogen. NPR-26482: Hotfix für CQ-4253540
* Deaktivieren von „Pfad zum Stammordner des Unternehmens“ in der Benutzeroberfläche zur Konfiguration von Dynamic Media Cloud. NPR-26361: Hotfix für CQ-4249505
* Die Aufnahme von .mos RAW-Dateien wird verlängert. NPR-26296: Hotfix für CQ-4250661
* Bei der Freigabe von Asset-Links ist es nicht möglich, mehr als einen internen Benutzer mit numerischer Benutzer-ID hinzuzufügen. NPR-26206: Hotfix für CQ-4251466
* Korruptionsfall in ZIP-Dateien, die mit dem deflate64-Algorithmus komprimiert wurden. NPR-26793: Hotfix für CQ-4253995
* Die Erstellung von Miniaturbildern funktioniert bei komplexen PDF-Dateien nicht ordnungsgemäß, was zu Miniaturbildern führt, bei denen ein Teil des Bildes fehlt. NPR-26057: Hotfix für CQ-4250944
* Problem mit der Speichernutzung im Heap-Speicher bei der Erstellung von Miniaturansichten. NPR-25545: Hotfix für CQ-4246960
* Das Erstellen einer großen Anzahl von Beziehungen zu einem Asset verursacht einen Fehler. NPR-26309: Hotfix für CQ-4250708
* Die Option „Ausgabe löschen“ funktioniert nicht und gibt den Fehler „Nichts zu löschen“ aus. NPR-26007: Hotfix für CQ-4213414
* Standardwerte für Felder mit mehreren Werten können nicht gelöscht werden. NPR-25116: Hotfix für CQ-4247856
* (DM Hybrid) Katalogreplikation schlägt für AEM 6.3.2 mit Dynamic Media fehl. NPR-26406: Hotfix für CQ-4251306

#### Sites {#sites-7}

* Korrekturen an der proaktiven Unterstützung von Sites. NPR-26963
* Tags werden zweimal erstellt, wenn die Groß-/Kleinschreibung von Titel und Name unterschiedlich ist. NPR-26877: Hotfix für CQ-4254134
* Rich-Text-Editor-Funktionen im Bearbeitungsdialogfeld werden nicht von Richtlinien gesteuert. NPR-27059, NPR-26750: Hotfix für CQ-4241130
* Fragen zum Zwischenspeichern in segment.js in Client Context bzw. Nicht-Zwischenspeichern. NPR-26622: Hotfix für CQ-4253486
* Die Aktivierung der Segmentregel (/etc/segmentation) für untergeordnete Regeln in der klassischen Benutzeroberfläche führt dazu, dass die Veröffentlichungsinstanz inaktiv wird. NPR-26601: Hotfix für CQ-4253588
* Durch Hinzufügen eines Sonderzeichens wird das Dialogfeld „Rich-Text-Editor“ nach oben verschoben. NPR-26435: Hotfix für CQ-4249869
* (Touch-optimierte Benutzeroberfläche) Die Symbolleiste kann mit mehreren Rich-Text-Editor-Versionen beim Umschalten von Vollbild auf schwebendes Dialogfeld nicht verwendet werden. NPR-25652: Hotfix für CQ-4206008
* Beim Bewerben eines mehrseitigen Launches werden für jede Seite mehrere Versionen erstellt. NPR-26810: Hotfix für CQ-4254663
* Vorgänge zum Verschieben von Tags werden von  Tag-Feldern für das Inhaltsfragmentmodell nicht widergespiegelt. NPR-26801: Hotfix für CQ-4251805
* (Touch-optimierte Benutzeroberfläche) Das Rückgängigmachen der Veröffentlichung der untergeordneten Seite im Seiteneditor funktioniert nach dem Umbenennen der Seite im Entwurf nicht. NPR-26774: Hotfix für CQ-4254175
* Veröffentlichung rückgängig gemacht Seite funktioniert nicht mit Verweisen. NPR-26749: Hotfix für CQ-4254372
* Wenn Sie eine Variante als Live Copy erstellen, muss der Benutzer die Seite aktualisieren, damit sie angezeigt wird. NPR-26663: Hotfix für CQ-4254328
* (Klassische Benutzeroberfläche) Wenn Sie zu den Seiteneigenschaften zurückkehren, verwendet das Miniaturbild keine Vererbung mehr und verschwindet aus der Site-Administration und dem Sidekick. Das Bild wird als leer angezeigt. NPR-26562: Hotfix für CQ-4252346
* Wenn eine Version einer Seite erstellt und ein Vergleich ausgelöst wird, werden die Knoten von „/content/ versionshistory“ in der Liste der Live Copies für den Entwurf aufgeführt. NPR-26506: Hotfix für CQ-4243957
* URLs im Experience Fragment Admin Editor lassen keine Überlagerungen zu. NPR-26318: Hotfix für CQ-4252156

#### Plattform {#platform}

* Sitzungs-Schwachstelle in ReplicationEventListener mit Testereignissen. NPR-25937: Hotfix für CQ-4251090
* Die Replikation verwendet das abgelaufene Token für OAuth, das mehrere Fehler verursacht. NPR-25894: Hotfix für GRANITE-22388

#### Integration {#integration-3}

* In AEM eingebettetes TSDK stürzt bei einer Aktualisierung auf Handlebars 4 aufgrund der Verwendung inkompatibler Vorlagen ab. NPR-26699: Hotfix für CQ-4248974
* Wenn Sie eine Seite mit einem neuen Asset veröffentlichen, wird die untergeordnete Seite ohne Benachrichtigung in der Veröffentlichungsinstanz deaktiviert. NPR-24869: Hotfix für CQ-4247832
* Die Replikation verwendet ein abgelaufenes Token für  oauth . NPR-25984: Hotfix für Granite-22388

#### Replikation {#replication-2}

* Der Http-Transport kann offene Sitzungen durchlassen. Hotfix für Granite-17434
* Ausnahmen in Protokollen, während auf den Zugriffstoken-Knoten von mehr als einem Replikationsagenten gleichzeitig zugegriffen wird. NPR-26964: Hotfix für GRANITE-23276, Granite-23155

#### ContextHub {#contexthub}

* Die Datei „coral.js“ enthält eine anfällige Version der Bibliothek „handlebars.js“. Hotfix für CQ-4255377

#### DAM – DM Client {#dam-dm-client-1}

* Wenn Sie eine Kopie eines Bild-Assets löschen, kann das ursprüngliche Bild-Asset nicht mehr verwendet werden. Hotfix für CQ-4251648
* Redundanter Download zusätzlicher Bildinhalte von S7-Servern. Hotfix für CQ-4248770

#### Granite {#granite}

* AEM OAuth Provider führt keine Suche ohne Unterscheidung zwischen Groß- und Kleinschreibung durch. NPR-26133: Hotfix für GRANITE-22650
* Package Validator überprüft keine Pakete, die in CFP/SP enthalten sind. NPR-26775: Hotfix für Granite-22825

#### Communities {#communities-6}

* Problem mit Trennzeichen bei Suchergebnissen. NPR-27051: Hotfix für CQ-4248939
* Ändern des Dropdown-Werts von Dallas in Virginia in Adobe Storage Resource Provider. NPR-26936: Hotfix für CQ-4254434
* Aktivieren der Unterstützung für die lokalisierte Titelsuche in SocialTagManager. NPR-26932: Hotfix für CQ-4250276
* Bilder im Anhang zeigen beim Erstellen eines Forumsbeitrags keine Miniaturansicht. NPR-26380: Hotfix für CQ-4253105
* Beim Einfügen aus Word-Plug-in kann nicht mehr als ein Bild geladen werden. NPR-26728: Hotfix für CQ-4253638
* Der Inhalt auf der Moderationsseite kann nicht gefiltert werden. NPR-26697: Hotfix für CQ-4213766
* (Sicherheitslücke) Kontoübernahme aufgrund von JWT-Fehlkonfiguration. NPR-26440: Hotfix für CQ-4253314
* Das Abrufen von Daten von Adobe Storage Resource Provider ist langsam. NPR-26237: Hotfix für NPR-24152
* Die Seite zum Erstellen privater Nachrichten arbeitet fehlerhaft und langsam. NPR-26120: Hotfix für CQ-4250923
* Die Benachrichtigung „Alle als gelesen markieren“ markiert ohne Seitenaktualisierung nur die ersten 10 als ungelesen. NPR-27036: Hotfix für CQ-4254058
* Verhalten bei Klicks zur Abschnittspagnierung in Communities-Kommentaren und beim Laden von Seiten. NPR-27030: Hotfix für CQ-4251228
* (Forensuche) Die Schaltfläche „Zurück“ überspringt die Seite und wechselt zurück zu forum.html. NPR-26949: Hotfix für CQ-4254804
* Die Ungelesen-Benachrichtigung ermöglicht keine höhere Anzahl als 21. NPR-26947: Hotfix für CQ-4251251
* (Auftrag „SearchScheduledPosts“) Hinzufügen des Schalters „enable/disable“ in ConfigMgr. NPR-26924: Hotfix für CQ-4250463
* Tomcat Context(/aempublish) Path verschwindet beim Blättern auf der Seite „Assignments“. NPR-26919: Hotfix für CQ-4254345
* NullPointerException beim Erstellen einer Gruppe und eines Mitglieds. NPR-26778: Hotfix für CQ-4248095
* Aufhebung der Fixierung durch Moderator und nicht spezielle Inhalte funktionieren nicht mit dem SRP (Single Responsibility Principle) von MySQL. NPR-26767: Hotfix für CQ-4251520
* Probleme mit der Suchfunktion bei bestimmten Zeichen. NPR-26726: Hotfix für CQ-4247744
* Aktivieren von Deep-Links für die Moderations-Benutzeroberfläche und die Aktivierungsressourcen. NPR-26705: Hotfix für CQ-4251381
* Suchproblem in der Forenkomponente. NPR-26577: Hotfix für CQ-4251303
* Die Suche mit dem Vor- und Nachnamen zusammen in Communities-Nachrichten liefert nicht die erwarteten Ergebnisse. NPR-26377: Hotfix für CQ-4253150
* Die Paginierung wird beim Entfernen von Antworten nicht aktualisiert. NPR-26327
* Die Löschung von Beiträgen funktioniert, gibt jedoch einen Fehler in der Konsole aus und Beiträge bleiben in der Benutzeroberfläche sichtbar. NPR-26292: Hotfix für CQ-4252803
* Die Paginierung wird nicht dynamisch aktualisiert und die Liste der Antworten wird immer länger. NPR-26145: Hotfix für CQ-4251586
* Gruppeneinstellungen werden für eine Gruppe mit 50.000-100.000 Benutzern nicht geladen. NPR-25642: Hotfix für CQ-4238426
* Catalog Resource Player für Kontextpfade versagt. NPR-25640: Hotfix für CQ-4238426
* (Forensuche) Paginierte Links zu Threads mit vielen Beiträgen funktionieren nicht bei Benachrichtigungen. Hotfix für CQ-4254202
* Moderationskonsole zeigt mit Firefox nur 5 Einträge an. Hotfix für CQ-4254128
* Gruppen sind beim Erstellen einer Site nicht sichtbar. NPR-27148: Hotfix für CQ-4251788
* „Null Pointer“-Ausnahme beim Hinzufügen von Gruppen und Mitgliedern zu Rolleneinstellungen und beim Zulassen des privilegierten Mitglieds in der Blog-Funktion. NPR-21732, NPR-27176: Hotfix für CQ-4255909
* Wenn Sie die Site bearbeiten und Mitglieder in den Rolleneinstellungen hinzufügen, wird eine „Null Pointer“-Ausnahme ausgelöst. NPR-27132: Hotfix für CQ-4255909

#### Benutzeroberfläche {#user-interface}

* Proaktive Fehlerbehebungen für platform.login. NPR-26961
* (Mehrfeld) Zulassen von benutzerdefinierten Namen für Composite-Elemente. NPR-26493: Hotfix für Granite-20568
* Update der Spaltenansicht funktioniert nach dem Einfügen einer Seite erst, nachdem sie aktualisiert wurde. NPR-26030: Hotfix für CQ-4236346
* Proaktive Fehlerbehebungen für granite.ui.commons. NPR-26960
* Proaktive Fehlerbehebungen für granite.ui.content. NPR-26959
* Proaktive Fehlerbehebungen für CQ/Experience-Protokoll. NPR-26943
* Proaktive Unterstützung von Foundation UI Backports. NPR-26942
* (IE11) Im Zahlenfeld wird „NaN“ angezeigt, wenn ein negativer Wert eingegeben wird. NPR-26701: Hotfix für CQ-100826
* (Coral- Mehrfeld) Verschachtelte Mehrfelder verwenden die falsche Vorlage, um die Elemente zu erstellen. NPR-25649: Hotfix für CUI-6743
* Aktualisieren Sie die Granite-ClientBibliotheken „coralui2“ und „coralui3“, um Handlebars aus dem Build zu entfernen. NPR-25606: Hotfix für Granite-22116

### Forms {#forms-7}

### Forms-Add-on-Paket {#forms-add-on-package-7}

#### Forms - Document Security {#forms-document-security-2}

* Ausnahmen von der Schlüsselaktualisierung in Server-Protokollen für inaktive Schlüssel. NPR-26748: Hotfix für CQ-4253705
* Wasserzeicheneinstellungen von Document Security können nicht erstellt oder geändert werden. NPR-26267, NPR-26129: Hotfix für CQ-4250234

#### Forms - Document Services {#forms-document-services-4}

* PDF/A-Überprüfung mit „validate PDF/A“ wird als nicht gültig angezeigt. NPR-25934: Hotfix für CQ-4248558

#### Forms – Interaktive Kommunikation {#forms-interactive-communication}

* Die PDF- und HTML-Vorschau des Briefs sind im selben Fenster sichtbar und funktionsfähig, wenn ein bearbeitbares Modul bearbeitet, gespeichert und dann die PDF-Vorschau geöffnet/geschlossen wird. NPR-26770: Hotfix für CQ-4253217

#### Forms – Workflow {#forms-workflow-2}

* Arbeitsbereich hängt gelegentlich und zeigt die Startpunkte wiederholt an. NPR-26461: Hotfix für CQ-4253439
* ESAPI-Ausnahme wird in den Protokollen ausgegeben, wenn im Aufgabennamen Klammern verwendet werden. Hotfix für CQ-4256627
* „Null Pointer“-Ausnahme beim Öffnen eines nicht mit einem vorausgefüllten adaptiven Formular/Formularsatz verknüpften Startpunktes. Hotfix für CQ-4256124
* E-Mail kann nicht mit der globalen Einstellung gesendet werden. NPR-26163: Hotfix für CQ-111110
* Arbeitsbereich kann nach dem Anwenden der Datei „axis.jar“ nicht geöffnet werden. NPR-26131: Hotfix für CQ-4251126
* Die Schaltfläche „Aktualisieren“ kann die neuesten Daten vom Server nicht mit adaptiven Formularen synchronisieren. Hotfix für CQ-4255670
* Beim Festlegen der Suchvorlage über die Admin-Benutzeroberfläche und Verwenden derselben Suchvorlage für das Suchen im AEM Forms-Arbeitsbereich wird eine Ausnahme ausgelöst. Hotfix für CQ-4255649
* Die Verfolgungsdetails der Prozesse unter den Programmen mit Klammern-Symbol im Namen werden im HTML-Arbeitsbereich nicht angezeigt. Hotfix für CQ-4242101
* Beim Speichern von Änderungen im Anzeigebereich „Voreinstellungen“ des HTML-Arbeitsbereichs wird eine Ausnahme ausgelöst. Hotfix für CQ-4241485
* Die Massengenehmigung ist beim neuesten JEE-Setup ungültig. Hotfix für CQ-4241486
* Der Entwurf der Aufgabe/des Startpunkts schlägt auf dem neuesten 6.4 JEE-Server fehl. Hotfix für CQ-4241484
* Setzen Sie den Parameter „Date().getTime().toString“, um die Sitzung damit anstelle von „Date.toString()“ zu initialisieren. Hotfix für CQ-4241483
* Beim Öffnen von /lc/ws tritt eine anfällige Zeichenausnahme im HTML-Parameter auf. Hotfix für CQ-4241481

#### Schwachstelle {#vulnerability-1}

* Geschützte Cross-Site Scripting (XSS)-Schwachstelle auf der Registerkarte „Notizen“ des Forms Managers. NPR-27157: Hotfix für CQ-4255556

### Forms JEE-Installationsprogramm {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Code-Überprüfung für Enterprise Security API. Hotfix für CQ-4255638
* esapi.properties konnte nicht als Classification-Ressource in WAS9 geladen werden. Hotfix für CQ-4255631
* Fehler beim Klicken auf „Authentifizierung hinzufügen“ während der Konfiguration der Domain. Hotfix für CQ-4255634
* Forms JEE unterstützt die gegenseitige Authentifizierung mit PKCS#11. NPR-21372
* Korrektur der Probleme, die in der Analyse von statischem Code von Core gemeldet wurden. Hotfix für CQ-104446
* Die Bereitstellung von adobe.livecycle.weblogic.ear und adobe.livecycle.websphere.ear schlägt während der Ausführung von LCM fehl. Hotfix für CQ-4255629, CQ-4255630
* Ungültige Fehlermeldungen in der Programmverwaltung. NPR-23289: Hotfix für CQ-4233163, CQ-4255636
* Fehler beim Klicken auf „Authentifizierung hinzufügen“ während der Konfiguration der Domain. Hotfix für CQ-4255634

#### Forms - JEE Connector {#forms-jee-connector}

* Korrektur der Probleme, die in der Analyse von statischem Code von Connector gemeldet wurden. NPR-22260

#### PDFG Service {#pdfg-service-1}

* org.jgroups.Message-Fehler in den Protokollen nach der Aktualisierung von LiveCycle auf AEM 6.2 Forms. NPR-26795: Hotfix für CQ-4220415
* AEM Forms - Fehler beim Migrieren von Stilen. Hotfix für CQ-4251969
* Die im statischen Code-Analysebericht von PDFG gemeldeten Probleme wurden behoben. NPR-23251: Hotfix für CQ-4213930

#### In Version 6.3.3.1 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-3}

Liste der in AEM 6.3.3.1 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Liste der in AEM 6.3.3.1 enthaltenen Inhaltspakete

### Cumulative Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 2 (6.3.2.0) im April 2018 mehrere interne und kundenspezifische Korrekturen enthält.

AEM Cumulative Fix Pack 6.3.2.2 ist von AEM 6.3 Service Pack 2 abhängig. Daher müssen Sie das AEM Cumulative Fix Pack 6.3.2.x-Paket nach der Installation von AEM 6.3 Service Pack 2 installieren. Installationsanweisungen finden Sie unter [Versionshinweise zu AEM 6.3 Service Pack 2](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html).

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.11 aktualisiert.
* Sub-Assets und mehrseitige Asset-Viewer in Brand Portal aktiviert.
* Die Länge des Feldtyps wurde auf 255 geändert, um alle möglichen MIME-Typen für die verschiedenen Anlagenarten zu unterstützen.
* Vom Server konfigurierte Fehlermeldung, wenn ein Bild gegen die Upload-Kriterien verstößt.
* STARTTLS-Unterstützung im Day CQ Mail Service hinzugefügt.
* Aktualisieren auf die neuesten Versionen von cq-wcm-content und com.adobe.cq.launches.it.serverside.
* Aktualisieren von com.adobe.granite.ui.coralui3-rte auf die neueste Version.
* Gesicherte Render-Bedingung gibt korrektes Ergebnis zurück, wenn expressionResolver NULL ist.
* Coral.ColumnView: Unterstützung für Shift+Click hinzugefügt.

### Assets {#assets-8}

* Feld „Asset Folder Closed User Group (CUG)“ gibt nicht die Gruppe „everyone“ aus. NPR-23163: Hotfix für CQ-4239377
* Die Suche nach gespeicherten Suchvorgängen mit Smart-Sammlung gibt nicht alle Ergebnisse zurück. NPR-23243: Hotfix für CQ-4240355
* (ExpiryNotificationJobImpl) Optimierung der vorhandenen Abfrage. NPR-23330: Hotfix für CQ-4205249
* (Metadatenprofil) Standard-Tag-Werte, die zum Zeitpunkt der Erstellung festgelegt wurden, stehen nach dem Speichern nicht zur Verfügung. NPR-23370: Hotfix für CQ-4235458
* (Touch-optimierte Benutzeroberfläche) Aufgrund eines JS-Fehlers können mehrere Assets nicht verschoben werden. NPR-23395: Hotfix für CQ-4241279
* Falsche Angaben zur Downloadgröße und zu den angezeigten Informationen führen zu Verwirrung. NPR-23418: Hotfix für CQ-4242774
* Extrahierter mimetype für die Dateierweiterung LSR und SKETCH ist nicht korrekt und führt zu einem ungültigen Datei-Download. NPR-23644: Hotfix für CQ-4243260
* (Firefox/Chrome) Auf der Seite „Asset-Freigabe“ können keine Assets heruntergeladen werden. NPR-23963: Hotfix für CQ-4244391
* Die Suchfacetten der Asset-Admin werden nach der Vorschau in den Suchfeldern ausgeblendet. NPR-23964: Hotfix für CQ-4244410
* Rückgängigmachen der Veröffentlichung des Suchformulars entfernt das Standardsuchformular vollständig. NPR-23291: Hotfix für CQ-4241382
* (Brand Portal) Die Suche in der Verzeichniseigenschaft sollte bei der Replikation herausgefiltert werden. NPR-23292: Hotfix für CQ-4241385
* Die Benutzeroberflächenaktion „In Brand Portal veröffentlichen“ ist nicht verfügbar. NPR-23293: Hotfix für CQ-4241161
* Die Schaltfläche „In Brand Portal veröffentlichen/entfernen“ sollte für Inhaltsfragmente nicht verfügbar sein. NPR-23318: Hotfix für CQ-4245086
* (Brand Portal) Aktivieren Sie die Erstellung von Sub-Assets, wenn ein Asset veröffentlicht wird. NPR-23331: Hotfix für CQ-4242018
* Anfragen für Dynamic Media verwenden keinen allgemeinen Proxy/HTTP-Client; NPR-10727: Hotfix für CQ-45695, CQ-88800
* MP4-Video-Asset für einzelne Darstellungen kann in Dynamic Media S7 (DMS7) nicht kommentiert werden. NPR-22046: Hotfix für CQ-4215912
* EmbedXMP-Daten werden für den Ptiff-Generierungsprozess immer auf „aktiv“ gesetzt. NPR-22903: Hotfix für CQ-4234498
* Probleme bei der Anzeige/Auswahl dynamischer Ausgaben bei hoher Bildvorgabenzahl. NPR-23151: Hotfix für CQ-4217511
* Problem mit Dynamic Media Encode Video - Modification/Reupload Launcher. NPR-23237: Hotfix für CQ-4240260
* Korrektur zur Proxy-Verarbeitung für HTTP-Forwarder in Dynamic Media S7. NPR-24001: Hotfix für CQ-244140

### Sites {#sites-8}

* Abfrageaufbau-Diskrepanzen führten zu unterschiedlichen xPath-Konvertierungen zwischen 6.2 und 6.3. NPR-23245: Hotfix für CQ-4240396
* Die Registerkarte „Thumbnail“ in der Seiteneigenschaft funktioniert beim Erweitern des Dialogfelds nicht. NPR-22844: Hotfix für CQ-4241474
* Parsys unterbricht die Rahmenbreite des Emulators und schneidet alle hinzugefügten Komponenten ab. NPR-22926: Hotfix für CQ-4238224
* Beim Ausführen mehrerer Starts erfolgt der Start im Autorenmodus, die Änderungen werden jedoch aufgrund fehlender Replizierungsberechtigungen nicht auf dem Publish-Server repliziert. NPR-22934: Hotfix für CQ-4234746
* Eine von einem Benutzer in der ersten Sitzung gesperrte Seite kann von einem anderen Benutzer in einer anderen Sitzung geändert werden. NPR-23057; Hotfix für CQ-4199017
* Korrigierte Option „Neu sortierbar“ in der Listenansicht. NPR-23065: Hotfix für CQ-4239321
* (Seiteneditor) Bild in einer Bildkomponente ist beim erneuten Öffnen des Dialogfelds nicht sichtbar. NPR-23156: Hotfix für CQ-4239978
* Der Vorlagen-Editor zeigt nur 20 Vorlagen/Ordner an und lädt die anderen nicht, wenn ein Bildlauf zum Seitenende durchgeführt wird. NPR-23185: Hotfix für CQ-4238483
* (Klassische Benutzeroberfläche) Beim Verschieben oder Umbenennen der Seiten wird ein Fehler erzeugt. NPR-23213: Hotfix für CQ-4240971
* ContextHub-Segmente können nicht bearbeitet/erstellt werden. NPR-23218: Hotfix für CQ-4226948
* (Rich-Text-Editor) Durch den Vorgang „Ersetzen“ wird das Format eines Wortes geändert. NPR-23271: Hotfix für CQ-4239677
* Schaltfläche „Rollout“ fehlt auf der Registerkarte „Blueprint“ für XF-Varianten. NPR-23320: Hotfix für CQ-4240404
* Die klassische Benutzeroberfläche funktioniert aufgrund der veralteten Version nicht, um CUG zu bearbeiten. NPR-24122: Hotfix für 4241823
* Proaktive Fehlerbehebung zum Schutz vor unerwünschten Inhaltspromotions. NPR-24387: Hotfix für 4244993
* Ungefähr 80 Fragmente werden in einem Ordner in Assets hinzugefügt. Es treten Fehler auf, wenn der Workflow über die Timeline-Konsole ausgelöst wurde. NPR-23393; Hotfix für CQ-4211216
* Bilder können nicht aus der Inhaltssuche in das Dialogfeld „Rich Text Editor“ gezogen und dort abgelegt werden. NPR-23403: Hotfix für CQ-4242094
* Fehler „Invalid Recursion Selector Value“ bei der Migration einer Komponente von AEM 6.0 auf AEM 6.2. NPR-23532: Hotfix für CQ-4241258
* (Rich-Text-Editor) QuickInfos zeigen den Variablennamen des Plug-ins anstelle des lesbaren Plug-in-Namens an. NPR-23550: Hotfix für CQ-4243269
* Dialogfeld mit erforderlichem Dropdown-Menü in der Mobilgeräteversion kann nicht gespeichert werden. NPR-23904: Hotfix für CQ-4243096
* Stilsystemoptionen werden auf allen Seiten nach der Installation von 6.3.2.1 angezeigt. NPR-23972: Hotfix für CQ-4244394
* Die klassische Benutzeroberfläche funktioniert aufgrund der veralteten Version nicht, um CUG zu bearbeiten. NPR-24122: Hotfix für 4241823
* Proaktive Fehlerbehebung zum Schutz vor unerwünschten Inhaltspromotions. NPR-24387: Hotfix für 4244993
* Asset-Verweise werden beim Verschieben von Assets nicht aktualisiert. NPR-23208: Hotfix für CQ-4239879

### Plattform {#platform-1}

* Die Smart-Sammlung zeigt bei der Verwendung der Tag-Eigenschaft in der Suchfacette nach dem Speichern keine Ergebnisse an. NPR-23401: Hotfix für Granite-21278
* Patch jQuery 1.12.4 von clientlib enthält Sicherheitskorrektur. NPR-24128: Hotfix für Granite-20058
* Internationalisierungs-Übersetzungen werden nur dann aktualisiert, wenn das Paket neu gestartet wird. NPR-23193: Hotfix für Sling-7190
* Ungeschlossener Ressourcenauflöser in ReplicationEventListener. NPR-23240: Hotfix für CQ-4241350
* Unterstützt STARTTLS in „Day CQ Mail Service“. NPR-23941: Hotfix für CQ-4240397
* Der JCR-Complaint-Tag-Name sollte basierend auf dem Tag-Titel automatisch gefüllt werden. NPR-24173: Hotfix für CQ-4199411

### Integration {#integration-4}

* (Target) Kampagnen werden nicht aktiviert, wenn als API-Typ XML verwendet wird. NPR-23199: Hotfix für CQ-4240936****
* Die Replikation der Konfigurationsreferenzen mit der Zwischenordnerstruktur schlägt fehl. NPR-23485: Hotfix für CQ-4242751

### Schwachstelle {#vulnerability-2}

* Die Salesforce-Integration ist anfällig für Server-seitige Anforderungsfälschung (SSRF, Server Side Request Forgery). NPR-24289: Hotfix für CQ-424527
* Cross-Site-Scripting (XSS) in Verknüpfungen zum Admin-UI-Projekt. NPR-23272: Hotfix für CQ-4241795

### WCM – Foundation-Komponenten {#wcm-foundation-components}

* Foundation-Tabelle ist anfällig für Stored Cross Site Scripting. NPR-23214: Hotfix für CQ-4240760

### Übersetzung {#translation-3}

* Eigenschaften von Live Copies werden beim Erstellen von Sprachkopien nicht gelöscht. NPR-23123: Hotfix für CQ-4230641

### Benutzeroberfläche {#user-interface-1}

* DatePicker unterstützt nicht die manuelle Einstellung externer Typhinweise, die durch ein unsichtbares Feld festgelegt werden. Beim Ändern des Typhinweises wird ein Konvertierungsfehler ausgegeben. NPR-23371: Hotfix für Granite-21194
* Coral.ColumnView: Unterstützung für Shift+Click hinzugefügt. NPR-23404: Hotfix für Granite-13338
* Select RT nimmt keine Überprüfung vor, wenn ein Element mit leerem Wert ausgewählt ist. NPR-23405: Hotfix für Granite-21283
* (OMEGA) Bericht „Feature“ nur auf Englisch. NPR-23990: Hotfix für Granite-21231
* Korrekturen der Coral.Autocomplete-API. NPR-23516

### Granite  {#granite-1}

* Apache HTTP-Client-Tracking-Verbindungen und eine hohe Heap-Nutzung führen zum Absturz des AEM-Servers. NPR-23906: Hotfix für Granite-21056

### Commerce {#commerce-2}

* Campaign-json-Ausgabe enthält keinen Servlet-Kontextstamm. NPR-23733: Hotfix für CQ-4243827

### Communities {#communities-7}

* Die Suche in Communities schlägt bei einigen Wörtern fehl. NPR-23256: Hotfix für CQ-4240717
* Es können keine Gruppen für das Problem mit der Rolle von Community-Managern zugewiesen werden. NPR-23317: Hotfix für CQ-4241233: CQ-4221399
* Probleme bei der Ressourcenerstellung mit einem ähnlichen Asset-Namen. NPR-23319: Hotfix für CQ-4240700
* (ContextPath) Die „Breaking Message“-Funktionalität schlägt bei Jetty-Konfigurationen und bei der Suche nach Gruppenmitgliedern in der Community-Gruppenmitgliedsliste fehl. NPR-23336: Hotfix für CQ-4241519, CQ-4242080
* Das Hochladen eines Bildes in ein Communities-Forum wird nicht im Adobe Storage Resource Provider (ASRP) angezeigt. NPR-23397: Hotfix für CQ-4242497
* Gelöschte Ideen werden als aktive Links in Aktivitäten angezeigt. NPR-23406
* Imsmanifest.xml, das mit Context Root läuft, kann nicht mit AEM geladen werden. NPR-23483: Hotfix für CQ-4242193
* Sicherheitslücken in einer älteren Version von Handlebars. NPR-23518: Hotfix für CQ-4243055
* Tunnel Service funktioniert nicht. NPR-23543: Hotfix für CQ-4242217
* Probleme mit Communities-Komponenten, werden ebenfalls aktiviert, wenn der Zugriff über Dispatcher und Sling-Dynamik erfolgt. NPR-23586: Hotfix für CQ-4242360, CQ-4241522
* Wenn Sie nach einem Suchbegriff schauen, der viele Ergebnisse durch Suchen generiert, und dann einen neuen Suchbegriff eingeben, wird die Seite nicht zurückgesetzt. NPR-23739: Hotfix für CQ-4222593
* Probleme beim Ausführen von  Suche in der Forenkomponente. NPR-23838: Hotfix für CQ-4243770
* (Kennzeichnung für Community-Moderation) Massengenehmigung von gekennzeichneten Nachrichten funktioniert nicht. NPR-23845: Hotfix für CQ-4243962
* Sortieren-Schaltflächentext zeigt nicht den standardmäßig ausgewählten  Wert trotz Auswahl der Standardsortierreihenfolge. NPR-23881: Hotfix für CQ-4243375
* Web- und E-Mail-Benachrichtigungen werden nicht ausgelöst, da die Gruppen nicht benachrichtigt werden. NPR-23934: Hotfix für CQ-4242880
* Mit der DSRP-Konfiguration werden keine Details zu den Kennzeichenbenutzern und den Gründen angezeigt. NPR-23973: Hotfix für CQ-4243205
* Flag-Gründe von nicht gekennzeichneten Benutzern bleiben sichtbar. NPR-23974: Hotfix für CQ-4243822
* Wenn zwei Dateien mit demselben Namen zweimal an einen Formularbeitrag angehängt werden, tritt ein Server-Fehler auf. NPR-24166: Hotfix für CQ-4244367
* Anlagen mit MIME-Typen von mehr als 15 Zeichen können nicht mit Database Storage Resource Developer (DSRP) gespeichert werden. NPR-24174
* Wenn ein Bild, das gegen die Upload-Kriterien verstößt, gezogen und in den Beitragstext eingefügt wird, wird ein Server-Fehler ausgegeben und dem Benutzer wird eine allgemeine Fehlermeldung angezeigt. NPR-24243
* Fehlerbehebungen bei mehreren Server-seitigen AEM Communities-Problemen. NPR-23971: Hotfix für CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Fehlerbehebungen bei mehreren Adobe Social-Problemen. NPR-24242: Hotfix für CQ-4245054, CQ-4245120, CQ-4245296

### Campaign {#campaign}

* Campaign-json-Ausgabe enthält keinen Servlet-Kontextstamm. NPR-23733: Hotfix für CQ-4243827

### MSM {#msm}

* Beim Rollout der Seite zeigt die LiveCopy nicht die von der primären Version geerbten Ein-/Auslaufzeiteigenschaften an. NPR-23873: Hotfix für CQ-4243431
* Der LiveCopy-Vorgang ignoriert keine untergeordneten Knoten gelöschter Komponenten. NPR-23058: Hotfix für CQ-4211662

### Entladen {#offloading}

* Anforderung eines Mechanismus zum Bereinigen von Assets aus den Arbeitsinstanzen nach der Verarbeitung oder regelmäßig. NPR-23638: Hotfix für Granite-21337

## Forms {#forms-8}

### Forms-Add-on-Paket {#forms-add-on-package-8}

#### Adaptive Formulare {#adaptive-forms-1}

* Verschieben von ReCaptchaConfigService in das interne Paket. Hotfix für CQ-4217459
* Numerisches Feld entspricht nicht dem Mindestwert. NPR-23967: Hotfix für CQ-4244830
* Unterstützung von Multi-Sharing in der Integration adaptiver Formulare mit AdobeSign. NPR-23383

#### Backend-Integration  {#backend-integration}

* (FDM) (WebService) Unterstützung des Erweiterungs-Konstrukts von WSDL in WSDL Parser. NPR-23640, NPR:23236: Hotfix für 4205821
* Hinzufügen von SDLInvokerParams in Forms Add-on Client SDK. NPR-23157

### Forms JEE-Installationsprogramm {#forms-jee-installer-7}

#### Prozessverwaltung {#process-management}

* Arbeitsbereich kann nach dem Anwenden der neuen axis.jar-Datei nicht geöffnet werden. NPR-23316
* LiveCycle ist anfällig für XSS auf PMAdmin. NPR-23267
* Nach der Aktualisierung auf AEM 6.1 Forms friert der HTML-Arbeitsbereich beim Zugriff auf die Aufgabenliste für bestimmte Benutzer ein. NPR-23943

#### Core {#core}

* Forms JEE unterstützt die gegenseitige Authentifizierung mit PKCS#11. NPR-21372

#### PDFG-Dienst {#pdfg-service-2}

* Der Paper Capture-Service stürzt bei gleichzeitiger Verarbeitung von TIFF-Dateien ab (Größe ca. 50 KB). NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output - Alternative Beschreibung für Anmerkungen fehlt. NPR-22207
* Fügt XML-Formularen, die über Designer und den Output Service generiert wurden, PDF/UA-Unterstützung hinzu. NPR-23132

### In Version 6.3.2.2 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-4}

Liste der in AEM 6.3.2.2 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Liste der in AEM 6.3.2.2 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulative Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 2 (6.3.2.0) im April 2018 mehrere interne und kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des **AEM Cumulative Fix Pack** sind:

* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.10 aktualisiert.
* Verbessertes Rendering von Parsys-Komponenten in der klassischen Benutzeroberfläche.
* Die Pakete für Sling-Modelle wurden aktualisiert und enthalten jetzt eine Korrektur des Zeichensatzes.
* Veröffentlichung in Brand Portal wurde für alle Asset-Typen asynchron gemacht.
* Aktualisierung von coralui-component-richtexteditor.git von 0.1.15 auf 0.1.16
* Korrekturen in der Funktion zum Einblenden/Ausblenden der Dropdown-Komponente.
* Das Spiegeln von Bildern für die Core-Image-Komponente wurde aktiviert.
* Aktualisierung von  Felix-HTTP-Bundles, um Sitzungsattribute zu aktivieren.

* Cache=true wurde bei Sling-Modellen aufgrund von Problemen mit dem Speicherverbrauch entfernt.

### Assets {#assets-9}

* Wenn Sie den Titel oder das Miniaturbild in den Einstellungen für den Asset-Ordner ändern, werden die ursprüngliche Gruppe und die Berechtigungen des Ordners überschrieben. NPR-22171: Hotfix für CQ-4216080
* Die Benutzeroberfläche gibt fälschlicherweise den Fehler „Veröffentlichung in Brand Portal fehlgeschlagen“ aus, obwohl der Auftrag zur Replikationswarteschlange hinzugefügt und Assets in Brand Portal veröffentlicht werden. NPR-22179: Hotfix für CQ-4205273
* (Touch-optimierte Benutzeroberfläche) Standardmäßiger Upload-Speicherort für Assets in der Spaltenansicht. NPR-22465: Hotfix für CQ-4237057
* AEM gibt beim Versuch, ein Asset-Schema von /conf/global nach /conf/mytenant zu kopieren, den Fehler StackOverflow aus . NPR-22489: Hotfix für CQ-4235875
* Der Versuch, ein ZIP-Archiv zu entpacken, schlägt fehl, da am Ende des Ordnernamens Leerzeichen stehen. NPR-22522: Hotfix für CQ-4238036
* Die Sortierung mit der Spalte „Asset-Titel“ funktioniert nicht bei Suchergebnissen. NPR-22908: Hotfix für CQ-4239076
* YouTube-Videos werden mit dem vollständigen Pfad anstatt mit dem Tag-Namen selbst getaggt. NPR-22976: Hotfix für CQ-4238669
* Die Neuanordnung von Ordnern mit einem neu zu sortierenden Ordner wird nicht beibehalten. NPR-23125: Hotfix für CQ-4231761
* HTTP 504: Gateway-Timeout-Fehler beim Versuch, Sammlungen über den Freigabe-Link freizugeben. NPR-21928: Hotfix für CQ-4234507
* PDF-Stichwortmetadaten werden nicht korrekt extrahiert und geändert, wenn mehrere Stichwörter mit einem PDF-Asset verknüpft sind. Um das Problem zu beheben, wurde die Metadateneigenschaft für das Feld „Betreff“ für PDF-Assets entfernt. Sie können das Metadatenschema jedoch bearbeiten, um ein Textfeld mit mehreren Werten für das Feld „Betreff“ hinzuzufügen. NPR-21972: Hotfix für 4215741****
* Falsche Assets werden gelöscht, wenn der ausgewählte Ordner zwischen der Anzeige der beiden Popups geändert wird. NPR-21980: Hotfix für CQ-4233675
* (DAM) Mehrere Schwachstellen bei Cross-Site-Scripting (XSS) beim Hinzufügen zum Sammlungs-Assistenten. NPR-22432: Hotfix für CQ-4327086
* Asset-Download schlägt fehl, wenn Digital Rights Management in Assets in Safari verwendet wird. Benutzer können keine Assets mit Haftungsausschluss und langen Dateinamen herunterladen. NPR-22747: Hotfix für CQ-4236460 und CQ-4235274
* Legen Sie beim Veröffentlichen von Assets in Brand Portal die Standardoption „Öffentlich freigeben“ fest. NPR-21931: Hotfix für CQ-4218816

### Sites {#sites-9}

* Neues Element im Workflow-Posteingang zeigt Seitenpfad anstelle des Titels der Seite an. NPR-21634: Hotfix für CQ-4230672
* Bei der Bearbeitung von Komponenten der bearbeitbaren Struktur gehen die für das interaktive Raster benötigten CSS-Klassennamen verloren. NPR-21741: Hotfix für CQ-4232374
* (Touch-optimierte Benutzeroberfläche) Mehrere Schwachstellen bei Cross-Site-Scripting (XSS) für HTL-Komponenten. NPR-21899: Hotfix für CQ-4232511
* Der Ressourcentyp für Inhaltsfragmente mit gemischten Medien kann nicht geändert werden. NPR-21907: Hotfix für CQ-4233401
* Das RTE-Vollbild verdeckt bei der Touch-optimierten Benutzeroberfläche die RTE-Plug-ins. NPR-22034: Hotfix für CQ-4235457
* (Touch-optimierte Benutzeroberfläche) Rich-Text-Editor entfernt alle Attribute außer ID aus dem &lt;a>-Tag. NPR-22044: Hotfix für CQ-4234133
* Mehrere gestapelte Parsys aufgrund langwieriger Abfragen (über 6) verlangsamen AEM. NPR-22134: Hotfix für CQ-4233904
* Die Berechtigungen für Knoten mit Doppelpunkten im Namen können nicht geändert werden. NPR-22136: Hotfix für CQ-4236221
* (Klassische Benutzeroberfläche) Die HTML-Ausgabe des Rich-Text-Editors fügt „list-position-style: inside;“ als Inline-Stil zum &lt;ul>-Tag hinzu. NPR-22145: Hotfix für CRTE-114
* TreeNode auf das Attribut Name zurückfallen lassen, wenn der Text leer ist. NPR-22146: Hotfix für CQ-4234724/CQ-4236300
* RSS-Feed-Probleme, Port -1 bis AEM 6.3. NPR-22176: Hotfix für CQ-4233339
* (Klassische Benutzeroberfläche) Der Tastaturbefehl zum Einfügen von Text (Strg+V) funktioniert nicht für die Komponente OOTB Text (Rich Text). NPR-22224: Hotfix für CQ-4236224
* Die Filterung von Tagfield funktioniert bei der Eingabe des Texts nicht erwartungsgemäß. NPR-22236: Hotfix für CQ-4236655
* (Seiteneditor) Beim Einfügen von Textdaten in die Imagemap-Komponente wird die Textkomponente ebenfalls mit eingefügt. NPR-22264: Hotfix für CQ-4236230
* Das erforderliche Dialogfeld „FileUpload“ verursacht Probleme beim Bestätigen. NPR-22464: Hotfix für CQ-4222192
* Das Verschieben ohne Replikationsberechtigungen startet einen Workflow für die Aktivierung, wenn die verschobene Seite oder ihre Referrer nicht aktiviert werden können. NPR-22467: Hotfix für CQ-4211765
* Leistungsprobleme beim Laden einer Seite mit großen (über 2000) Zielgruppen. NPR-22478; Hotfix für CQ-4209567
* Persistenzprobleme, wenn ContextHub während der Initialisierung die standardmäßige Persistenzschicht überschreibt. NPR-22479: Hotfix für CQ-4218399
* „Mit mehreren Seiten starten“ veröffentlicht keine Unterseiten auf den Veröffentlichungs-Servern, wenn „Unterseiten einschließen“ nicht  Erster Inhaltsstamm. NPR-22482: Hotfix für CQ-4237818
* (Touch-optimierte Benutzeroberfläche) Das Löschen von Launches über die Konsole der klassischen Benutzeroberfläche macht alle Seiten unbearbeitbar. NPR-22491: Hotfix für CQ-4225074
* Probleme mit der Bildkomponente aufgrund von zusätzlichem Leerzeichen im  Dialog gewechselt wird. NPR-22528: Hotfix für CQ-4238183
* Beim Öffnen der Komponente im  Inline-Modus sind zuvor geladene Plug-ins beim zweiten Mal nicht sichtbar. NPR-22591: Hotfix für CQ-4236850
* Wenn Sie einen Launch in einem verschachtelten Launch löschen, sind die Sub-Launches verwaist. NPR-22621; Hotfix für CQ-4202639
* (Sidekick der klassischen Benutzeroberfläche) Registerkarte „Workflow“ ist deaktiviert, wenn sich die Seite im Workflow-Sperrstadium befindet. NPR-22722: Hotfix für CQ-4237557
* Nach dem Spiegeln eines Bildes, das der Bildkomponente auf einer Seite hinzugefügt wurde, werden die Änderungen nicht gespeichert und das  Bild wird auf der Seite angezeigt. Rendering-Unterstützung wurde der Image-Core-Komponente über [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141) hinzugefügt. NPR-22801: Hotfix für CQ-4221539
* Wenn der Benutzer versucht, den vorhandenen Anker aus dem Ankermenü zu löschen, wird das Fenster der Rich-Text-Editor-Komponente geschlossen und die Änderungen werden nicht gespeichert. NPR-22802: Hotfix für CQ-4238167
* Der Omnisearch-Filter zeigt nicht alle Aktionen in der Site-Konsole an. NPR-22804: Hotfix für CQ-4239007
* Problem mit Kopieren/Einfügen in der Touch-Benutzeroberfläche mit der OS-Zwischenablage und der internen AEM-Zwischenablage. NPR-22807: Hotfix für CQ-4220383
* Inkonsistenzen bei der Hervorhebung des Auszugs wie von Lucene Search zurückgegeben. NPR-22879: Hotfix für CQ-4238513
* Aktivieren einer Seite mit  deaktivierter Instanzveröffentlichung führt zu einem grünen statt einem gelben Status. NPR-22927: Hotfix für CQ-4236310
* (StyleSystem) Die Bildschirmposition springt, während im Popup ein Stil ausgewählt wird. NPR-23183: Hotfix für CQ-4238867
* (Veröffentlichung verwalten) Für den Wechsel zum nächsten Monat des Kalenders sind mehrere Klicks erforderlich. NPR-23508: Hotfix für CQ-4242732

### Plattform {#platform-2}

* Das Sling Exporter-Servlet exportiert japanische Zeichen nicht korrekt. NPR-22153: Hotfix für CQ-4228920
* Deaktivierung des Schedulers beim Start. NPR-22440: Hotfix für Sling-7004
* Gruppen können nicht zwischen zwei Instanzen im Veröffentlichungsmodus synchronisiert werden. NPR-21943: Hotfix für Granite-19564
* Leistungsprobleme mit org.apache.sling.i18n Shared Session/Resource Resolver. NPR-23390: Hotfix für Sling-7543

### Integration {#integration-5}

* Ungeschlossener ResourceResolver in com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix für CQ-4236515
* TargetContentImpl verlangsamt AEM bei langwierigen Abfragen. NPR-22361: Hotfix für CQ-4236907
* Die Target-Engine (mbox.js, at.js) verwendet keine verwalteten URLs, und sie verwendet URLs mit Doppelpunkten, die bei bestimmten Bereitstellungen fehlschlagen können. NPR-22366: Hotfix für CQ-4237854
* Bei der Bereitstellung einer benutzerdefinierten at.js- oder mbox.js-Datei wird das „include“-Skript als Text und nicht als HTML-Tags in eine Seite geschrieben. NPR-22441: Hotfix für CQ-4203691
* Im Target-Modus können Autoren eine aus der Blueprint geerbte Komponente ändern, ohne die Vererbung abzubrechen. NPR-22751: Hotfix für CQ-4237907
* PersonalizationDataSource löst eine „Null Pointer“-Ausnahme aufgrund eines fehlenden  „jcr : content“-Knotens aus. NPR-22850: Hotfix für CQ-4222122
* AEM Targeting schlägt bei der Verwendung von  nicht englischer Sprache fehl. NPR-22917: Hotfix für CQ-4218213
* Beim Veröffentlichen einer Seite mit zielgerichteten Inhalten fehlen zugehörige Ressourcen. NPR-23064: Hotfix für CQ-4227119
* Benutzer können im mbox-Aufruf keine statischen Testparameterwerte sehen, die beim Testen mit AT.js als Client-Bibliothek in der Cloud-Konfiguration angezeigt werden. NPR-21930: Hotfix für CQ-4234520

### WCM – Foundation-Komponenten {#wcm-foundation-components-1}

* iParsys erstellt die Positionsänderung, nachdem das Kontrollkästchen „Vererbung abbrechen/deaktivieren“ deaktiviert wurde. NPR-21905: Hotfix für CQ-4230951
* Die Funktion zum Anzeigen/Ausblenden der Formular-Dropdown-Komponente funktioniert nicht wie erwartet. NPR-22327: Hotfix für CQ-4222853
* Die CAPTCHA-Komponente wird aus Sicherheitsgründen nicht mehr unterstützt. Wenn Sie die CAPTCHA-Komponente verwenden, wird nach der Installation von 6.3.2.1 oder höher die Meldung „Captcha-Komponente ist veraltet und sollte nicht mehr verwendet werden.“ angezeigt. Die AEM-Komponente kann angepasst werden, um reCAPTCHA für mehr Sicherheit einzubeziehen. NPR-22151 Hotfix für CQ-4220052

### WCM – Seiteneditor {#wcm-page-editor}

* Reflektiertes Cross-Site-Scripting (XSS) bei Verwendung einer ungültigen Auswahl. Hotfix für CQ-4270397

### Übersetzung {#translation-4}

* Untersuchen von Problemen mit der Vorschaufunktion. NPR-22114: Hotfix für CQ-4223753

### Benutzeroberfläche {#user-interface-2}

* Probleme bei der Monatsauswahl für Coral-Kalender, wenn der Datumsbereich mit „min“ und „max“ festgelegt ist. NPR-22716: Hotfix für CUI-7187
* (Klassische Benutzeroberfläche) Die Komponente zeigt die Standardwerte an, selbst wenn der zugehörige Formulardatenmodell-Service auf ein leeres Feld eingestellt ist. NPR-22272: Hotfix für GRANITE-19744

### Granite {#granite-2}

* Stabilitätsprobleme mit der Asset Share AEM-Publisher-Instanz, verursacht durch ein Speicherleck. NPR-22205, NPR-23178: Hotfix für Sling-5668, Sling-7292 und Sling-7470.
* Die instabile Service-ID sollte nicht für Sitzungs-Attributnamen verwendet werden. NPR-22821: Hotfix für Granite-21059
* Wenn ein HTTP   die von Whiteboard verwaltete Sitzung ungültig gemacht wird, wird die Container-Sitzung ebenfalls invalidiert, wenn die Sitzung keine anderen Sitzungsattribute aufweist. NPR-23059: Hotfix für FELIX-5819
* LogbackManager kann einige OSGi-Konfigurationen beim Start auslassen. NPR-23060: Hotfix für Granite-19791

### Commerce {#commerce-3}

* Aktivieren Sie die Erstellung des Workflows im Experience Fragments-Menü. NPR-22347: Hotfix für CQ-4221661
* Experience Fragments-Fehler, die in WeRetail reproduzierbar sind. NPR-21958: Hotfix für CQ-4220061
* „Null Pointer“-Ausnahme beim Aktivieren einer Seite, die ein gelöschtes Experience Fragment enthält. NPR-23179: Hotfix für CQ-4239939

### Projekte {#projects}

* (Mehrsprachiges Projekt) Das Projekt listet für mehr als 19 Sprachen keine Übersetzungsaufträge auf. NPR-22498: Hotfix für CQ-4229978

### Workflow {#workflow}

* (Klassische Benutzeroberfläche) Die Aktivierung oder Deaktivierung eines Workflow-Starters führt zu fehlerhaftem Verhalten. NPR-22907: Hotfix für CQ-4239153

## Forms {#forms-9}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

Die wichtigsten Highlights für AEM Forms sind:

* Unterstützung für HTML5-Eingabetyp hinzugefügt.
* Grundlegende SOAP-Header-Authentifizierung behoben.
* Unterstützung für das Titelattribut für Hyperlink hinzugefügt.
* PDF/UA-ID in der Barrierefreiheits-Struktur von Forms Designer aktiviert.
* Zertifikatsauthentifizierung für Workbench-Benutzer aktiviert.
* Unterstützung für die Erstellung von PDF-Dateien hinzugefügt, die PDF/A-2a- oder PDF/A-3a-kompatibel sind.

### Forms-Add-on-Paket {#forms-add-on-package-9}

#### Forms-Admin-Benutzeroberfläche {#forms-admin-ui}

* Das Kennwort ist auf den Konfigurationsseiten von ECM Connectors im Klartext sichtbar. NPR-22508: Hotfix für CQ-4236065

#### Formularservice {#forms-service}

* Wenn SSL aktiviert ist, funktionieren die Ereignisse „Senden“ und „Abbrechen“ nicht mit Form Analytics. NPR-22637; Hotfix für CQ-4237973

#### Benutzerverwaltung {#user-management}

* LDAP kann aufgrund einer falschen Version von cglib-nodep nicht synchronisiert werden. NPR-22493: Hotfix für CQ-4234099

#### Adaptive Formulare {#adaptive-forms-2}

* Benutzerdefinierte Funktionen für den Regel-Editor fügen einen zusätzlichen Aufruf nach einer Funktion hinzu, sodass die Validierung fehlschlägt, obwohl die benutzerdefinierte Funktion true zurückgibt. NPR-22481: Hotfix für CQ-4235499
* Unabhängig vom ausgewählten Datumsmuster folgt die Komponente „Datumsauswahl“ beim Anzeigen von Mindest- und Höchstwerten nicht dem Muster. NPR-22444: Hotfix für CQ-4236269
* Das Datumsformat, das in einer Übermittlungsanforderung gesendet wird, sollte an dem Muster in der Komponente für die Datumsauswahl ausgerichtet sein. NPR-22384
* Die angegebene maximale Zeichenanzahl für ein adaptives Formulartextfeld wird auf Samsung-Geräten mit Android 6.0 nicht berücksichtigt. NPR-22363, NPR-22364: Hotfix für CQ-4235205
* (Microsoft Edge) (IE11) Textfeldkomponente für adaptive Formulare mit mehrzeiligen Feldern zeigt als Standardwert „Null“ anstelle von „Leer“ an. NPR-22284: Hotfix für CQ-69107
* SOAP UTF-8-Eingabekodierung in adaptiven Formularen gibt Fehler mit beschädigter Seite zurück. NPR-20105: Hotfix für CQ-4222669
* Die AEM Forms-Container-Komponente kann nicht bearbeitet werden, wenn auf der Website-Seite ein falsches Formular konfiguriert wurde. Hotfix für CQ-4237456
* Entwicklungstests schlagen fehl, wenn sie auf JEE-Servern ausgeführt werden. Hotfix für CQ-4222082
* AF-Tests schlagen auf JEE-Servern aufgrund von Minimierungsproblemen im Calvin-Framework fehl. Hotfix für CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) Die XML-Schemaeigenschaften von adaptiven Formularen können nicht aktualisiert werden, da die Optionen im Datensatzdokument (DOR, Document of Record) auf der Eigenschaftsseite nicht vorausgewählt sind. NPR-22298: Hotfix für CQ-4237402
* Formulare, die nach dem Veröffentlichen der Seite geändert werden, werden beim Veröffentlichen der Site nicht erneut veröffentlicht. NPR-23013: Hotfix für CQ-4236566

#### Backend-Integration  {#backend-integration-1}

* OOTB-Basisauthentifizierung für SOAP-Services funktioniert nicht für einfache Authentifizierung in der FDM-Integration. NPR-23238: Hotfix für CQ-4241308

#### Korrespondenzverwaltung {#correspondence-management}

* Die OOTB-XDPs zeigen, wenn sie innerhalb des Briefs verwendet und in der Vorschau angezeigt werden, den Inhalt mit der Fußzeile überlagert an. Hotfix für CQ-4212414

#### Assembler-Service {#assembler-service}

* Diskrepanz zwischen Acrobat DC- und AEM-Berichten zum Fehler bei der PDF/A-1b-Konformitätsprüfung. NPR-22051, NPR-22050: Hotfix für CQ-4226128, CQ-4227671

### Forms JEE-Installationsprogramm {#forms-jee-installer-8}

#### Workbench {#workbench}

* Zertifikatauthentifizierung für Workbench-Benutzer aktiviert. NPR-20644: Hotfix für CQ-4214486
* Das Herunterladen des Server-Protokolls mit Workbench funktioniert nur auf einem Server und auf dem anderen Server nicht. NPR-21079: Hotfix für CQ-4229842

#### Prozessverwaltung {#process-management-1}

* (HTML-Arbeitsbereich) Probleme mit der Bildschirmgröße bei Bildlaufleisten. NPR-23288
* (HTML-Arbeitsbereich) Prozess-Startpunkte sind nicht in alphanumerischer Reihenfolge sortiert. NPR-22841 Hotfix für CQ-4238944
* (HTML-Arbeitsbereich) Datenvorbereitung wird beim Schließen des Formulars im Arbeitsbereich ausgelöst. NPR-21127: Hotfix für CQ-4224574
* (HTML-Arbeitsbereich) Beim Aufrufen eines Prozesses, der Notizen mit langen Beschreibungen erfordert, funktioniert die Schaltfläche zum Erweitern der Notizen nicht. Hotfix für CQ-4241488

#### Core {#core-1}

* Fehler beim Starten des Schedulers. NPR-22990
* Verhindert, dass Browser in HTML-Formularen eingegebene Anmeldedaten speichern. NPR-21762: Hotfix für CQ-4206543
* Die in der statischen Code-Analyse von Core gemeldeten Probleme sollten behoben sein. Hotfix für CQ-104446

#### PDFG-Dienst {#pdfg-service-3}

* PDF Generator kann keine PDF-Dokumente mit bestimmten Lesezeichenebenen erstellen. NPR-22921, NPR-22285: Hotfix für CQ-4230562
* Unterstützung für die Erstellung von PDF-Dateien hinzugefügt, die PDF/A-2a- oder PDF/A-3a-kompatibel sind. NPR-23021: Hotfix für CQ-4214172

#### Forms Designer {#forms-designer-1}

* PDF/UA-ID fehlt beim Speichern als PDF in Designer. NPR-23137
* Path-Objekte, z. B. Rahmen, Unterstriche und Hyperlinks, werden beim Speichern als PDF in Designer nicht mit Tags versehen. NPR-23136
* Beim Speichern im PDF-Format in Designer steht für das Bildobjekt kein Begrenzungsrahmen zur Verfügung. NPR-23134
* Inline-Hyperlinks, die in Designer definiert sind, werden weder mit Tags versehen, noch haben sie alternativen Text, wenn sie als PDF in Designer gespeichert werden. NPR-23133
* Beim Öffnen des XML-Datenpakets mit AEM 6.3 Forms Designer wird die XHTML-Formatierung aus der XML-Quelle entfernt. NPR-21178: Hotfix für LC-3917046

#### Installieren von LCM {#install-lcm}

* Aktualisieren von Jsafe Jars auf Cryptoj 6.1.3.1 im Installationsprogramm und LCM. NPR-21370

#### Signatur-Service  {#signatures-service}

* Beim Versuch, ein PDF-Dokument digital über HSM zu signieren/zertifizieren, ist eine Ausnahme aufgetreten. NPR-21154: Hotfix für CQ-4226978

### In Version 6.3.2.1 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-5}

Liste der in AEM 6.3.2.1 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/bundle-list_002_.txt)

Liste der in AEM 6.3.2.1 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 1 (6.3.1.0) im Oktober 2017 mehrere interne und kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Pack sind:

* Die Benutzeroberfläche wurde geändert, um die Implementierung der CUG-Funktionalität in AEM Assets zu unterstützen.
* Es wurden Benutzeroberflächen-Probleme auf der Seite zur Lizenzprüfung behoben, um eine bessere Benutzerfreundlichkeit zu erzielen.
* Unterstützung von OSGi-Workflow-Aufgaben in der AEM Forms-App aktiviert.

### Assets {#assets-10}

* Die Benutzeroberfläche wurde geändert, um die Implementierung der CUG-Funktionalität in AEM Assets zu unterstützen. NPR-19485
* Das Hochladen eines Assets als direkt untergeordneter Knoten mit der Touch-optimierten Benutzeroberfläche verursacht ein Problem. Das Asset wird als direkt untergeordnetes Element des zuvor ausgewählten Assets hochgeladen. NPR-19736
* Datumsbereichseigenschaft und Bereichseigenschaft funktionieren nicht, wenn eine gespeicherte Suche/Smart-Sammlung geladen wird. NPR-19844: Hotfix für CQ-4220808
* Wenn mehrere Assets (mehr als 4) in Brand Portal veröffentlicht werden sollen, reagiert die AEM-Instanz nur langsam. NPR-20009: Hotfix für CQ-4213426
* Es können keine Assets mit Leerzeichen von der Lizenzprüfungsseite heruntergeladen werden. NPR-20067: Hotfix für CQ-4216557
* Verarbeitungsfehler beim Hochladen von PSB-Dateien mit mehreren Alpha-Ebenen. NPR-20250: Hotfix für CQ-4220869
* Benutzer können keine Assets mit langen Dateinamen und definiertem Haftungsausschluss herunterladen. NPR-20254
* ProductAssetsUploader belässt die temporären Dateien des JAVA-Caches im Java-TEMP-Ordner. NPR-20256: Hotfix für CQ-4221801
* Ersetzen Sie Versionsvergleichs-Code durch Adobe-proprietären Code aufgrund von Lizenzproblemen. NPR-20272: Hotfix für CQ-4223758
* In den Metadaten für eine Zeichenfolgeneigenschaft wird documentNumber als Datum angezeigt, es sollte sich jedoch um eine Zahl handeln. NPR-20291: Hotfix für CQ-4223991
* Die Textextraktion bleibt bei einer beschädigten PDF hängen. NPR-20416: Hotfix für CTG-4150375
* Komprimierte Dateien, die Assets mit nicht UTF-8-kompatiblen Namen enthalten, werden nicht korrekt heruntergeladen. NPR-20420: Hotfix für CQ-4219961
* Zu viele Zeichen in OmniSearch führen zum Absturz des AEM-Servers. NPR-20434: Hotfix für CQ-4223602
* Der Metadaten-Fehler der DAM-Asset-API unterbricht die xmp-write-back-APIs. NPR-20607: Hotfix für CQ-4220455
* Leistungsprobleme beim Hinzufügen von Benutzern zu Sammlungen. NPR-20699: Hotfix für CQ-4225733
* Die Veröffentlichung über AEM in Brand Portal ist für Dynamic Media-Sets nicht zulässig. NPR-20320: Hotfix für CQ-4221147
* Videos mit Leerzeichen und Akzent geben kein Video für die Renditions-Seite aus. NPR-19961: Hotfix für CQ-4221014
* Es wurden mehrere Probleme mit der Ordnerverarbeitung mit Assets-APIs behoben. NPR-20569
* AEM Dynamic Media Classic (früher Scene7) kann Assets nicht vom AEM-Server synchronisieren, wenn der Zielpfad in der Cloud Service-Konfiguration auf einen Unterordner im Stammpfad verweist. CQ-4228265
* Es wurde ein E-Mail-Bundle mit Apache Commons `{org.apache.commons/commons-email/1.5}` hinzugefügt, das `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}` ersetzt.

### Sites {#sites-10}

* Probleme mit Administratorberechtigungen: Die Mitglieder der geschlossenen Benutzergruppe können nicht aus den Seiteneigenschaften entfernt werden. NPR-20631
* Der eingegebene Workflow-Name sollte im Feld „Benachrichtigung“ verfügbar sein, wenn die Seite über „Veröffentlichung verwalten“ veröffentlicht wird. NPR-20046: Hotfix für CQ-4221586
* Durch die Anwendung von formatiertem Text auf zwei Zeilen im Rich-Text-Editor und die anschließende Zusammenführung in einem Absatz werden die formatierten Bereiche entfernt. NPR-20110: Hotfix für CQ-4223051
* Änderungen, die an den Feldeigenschaften in mehreren Registerkarten des Dialogfelds zum Bearbeiten von Eigenschaften vorgenommen wurden, werden manchmal nicht gespeichert. NPR-20286
* Unerwartetes Tag am Ende des eingefügten Inhalts im Inhaltsfragment. NPR-20413: Hotfix für CQ-4224014
* Es wurde ein Mechanismus in Adobe Campaign implementiert, um die Richtlinie einer Inhaltsressource aus einer externen Targeting-Ressource abzurufen. NPR-20667
* Richtext-Plug-in funktioniert nicht – sowohl für die Inline- als auch für die Vollbildleiste in der Touch-optimierten Mehrfeld-Benutzeroberfläche. NPR-20973

### Campaign {#campaign-1}

* Platzhalter sind nicht auf einer Seite sichtbar, die mehrere parsys-Komponenten enthält. NPR-20436; Hotfix für CQ-4215000

### Commerce {#commerce-4}

* Experience Fragments werden in Internet Explorer 11 nicht korrekt angezeigt. NPR-20161: Hotfix für CQ-4223319
* In Commerce-Workflows wird automatisch ein leeres Bild eingefügt, wenn eine Variante basierend auf einem primären Produkt mit mehreren Bildern erstellt wird. NPR-20068: Hotfix für CQ-4222048
* Die Filterung nach Tags auf Sammelseiten in der Produktkonsole funktioniert nicht. NPR-20292: Hotfix für CQ-4224023

### Communities {#communities-8}

* Inkonsistente Suchergebnisse mit Suchergebniskomponente. NPR-20070: Hotfix für CQ-4220913
* E-Mail-Benachrichtigungen werden für keine der Moderatoraktivitäten für veröffentlichte Komponenten ausgelöst. NPR-20122
* Für anonyme Community-Benutzer wird eine leere Paginierung ohne Ergebnisse angezeigt. NPR-20136: Hotfix für CQ-4220738
* Konfigurieren Sie einen Warnungsauslöser, wenn ein UGC als Spam erkannt wird oder wenn ein Benutzer auf einer vor-moderierten Site postet. NPR-20274: Hotfix für CQ-96850
* Es wurden mehrere Probleme mit AEM Communities-Website-Seiten behoben, einschließlich inkorrekter Umleitungen und Problemen mit der Seitenaktualisierung. NPR-20344
* CommunityUserOperationExtension stößt auf eine Klassenausnahme. NPR-20532: Hotfix für CQ-4224385
* Nach dem Erstellen einer Communities-Site können Benutzer die Site nicht aus der Sitemap öffnen, da der Kontextpfad nicht der URL vorangestellt wird. NPR-20730

### Integration {#integration-6}

* Migration vorhandener Analytics-Anmeldeinformationen zur WSSE-Authentifizierung. NPR-19962: Hotfix für CQ-4218071
* Ein Segment kann nach einer Änderung nicht erneut aktiviert werden und es wird ein Fehler ausgegeben. NPR-20054: Hotfix für CQ-4218401
* Bei der Konfiguration von Search&amp;Promote Cloud Service wird die Methode zum Abrufen von Formularen ignoriert, sodass sie auf der Autoreninstanz nicht mehr verwendet werden kann. NPR-20447: Hotfix für CQ-4206076
* Eine unübersichtliche Filterdefinition im Inhaltspaket führt dazu, dass Pfade überschrieben werden, wenn die Search&amp;Promote-Funktion installiert ist. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* Metadateneigenschaften für Assets des Typs TXT, die bei jeder Anzeige ihrer Eigenschaften in verschiedenen Metadaten-Editoren angezeigt werden. NPR-20239

### Plattform {#platform-3}

* Es wurde eine Ausnahme für den nicht geschlossenen Ressourcenauflöser behoben. NPR-19749: Hotfix für Granite-19143
* Anforderung der Anzeige benutzerdefinierter Karten zusammen mit standardmäßigen Statusprüfungen im Operations-Dashboard. NPR-20145
* Die Anmerkungsebene des Seiten-Editors funktioniert im Internet Explorer 11 nicht ordnungsgemäß. NPR-20222: Hotfix für CQ-4222818
* Sitzungsfehler beim Festlegen des Benutzeragenten als Administrator im Replikationsagenten. NPR-20578
* Die Funktion „requestAttributes“ ist für die anderen datenbasierten Ressourcenanweisungen nicht deaktiviert. NPR-20639: Hotfix für 4226206
* Es wurden Probleme mit Curl Head-Anforderungen für OOTB-Assets in AEM behoben. NPR-20781: Hotfix für CQ-4221520

### Projekte {#projects-1}

* Der Zugriff auf verschiedene Projekte über die Projektkonsole dauert länger. NPR-20314
* Bei der Installation von AEM 6.3.0.1 wird der Keystore des Benutzers für dam-update-service entfernt. NPR-20018
* Bei einigen benutzerdefinierten Bereitstellungen dauert es länger, bis Benutzer, die im addTask-Modul einen Verantwortlichen auswählen möchten, die Liste im UserPicker füllen. NPR-20283: Hotfix für CQ-4224193

### Benutzeroberfläche {#user-interface-3}

* Colorfield ist trotz der Attribute im Dialog auf „immer erforderlich“ eingestellt. NPR-19702
* Die Bildlaufleiste wird im Internet Explorer 11 für eine Komponente mit mehreren Feldern nicht im Vollbildmodus angezeigt. NPR-20261: Hotfix für CQ-4219782
* Vorherige Abfragen werden nicht abgebrochen, wenn aufeinander folgende Abfragen ausgelöst werden und zu falschen Ergebnissen führen. NPR-20398: Hotfix für GRANITE-19306

### Workflow {#workflow-1}

* Benutzer werden nicht über die Workflow-Aufgaben in ihrem Posteingang informiert. NPR-20213: Hotfix für CQ-4221639
* Die OOTB-Granite-Benutzerauswahl lädt keine Benutzer, wenn im Dialogfeld „Teilnehmer – Schritt“ des Workflow-Modells auf die Dropdown-Liste geklickt wird. NPR-20236

## Forms {#forms-10}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-10}

#### Adaptive Formulare {#adaptive-forms-3}

* Die Unterstützung für den Aggregationsausdruck für wiederholte Felder fehlt. NPR-20861
* Dropdown zeigt den zuletzt gespeicherten Wert an, auch wenn der zugehörige Formular-Datenmodell-Service keinen Wert ausgibt. NPR-20710
* Die vorhandenen Regeln können im Regel-Editor nicht mit booleschen Einschränkungen bearbeitet werden. NPR-21128

#### Form Portal  {#form-portal}

* HTML-Profil wird für ein adaptives Formular angezeigt, auch wenn der Asset-Typ nicht XDP ist. NPR-20079

#### Backend-Integration  {#backend-integration-2}

* Der Wert der Switch-Komponente kann nicht auf true/false festgelegt werden. NPR-21111

#### OSGi-Workflow  {#osgi-workflow}

* Workflow verwalten: Beim Übermitteln werden nur zehn Programme aufgelistet. CQ-4230193

#### HTML5-Formulare {#html-forms-3}

* Der Name eines XDP-Formularobjekts wie eines Teilformulars wird als QuickInfo angezeigt, wenn es nicht in den Barrierefreiheits-Konfigurationen definiert ist. NPR-20523

### Forms JEE-Installationsprogramm {#forms-jee-installer-9}

#### Prozessverwaltung {#process-management-2}

* Der FormSetPrefillApp-Startpunkt füllt keine Formularsatzfelder in der AEM Forms-App im Voraus aus. NPR-20950

#### Forms - AEM (LiveCycle)  {#forms-aem-livecycle}

* Installieren der neuesten CTJPEG2K-Bibliothek wegen einer kritischen Sicherheitslücke. Dies wirkt sich auf die Module XMLFM (AEM und IfBA), RM und PDFG aus. NPR-20625: NPR-21337.

### Enthaltene Feature Packs {#feature-packs-included}

#### AEM Forms-App {#aem-forms-app}

* Unterstützung von OSGi-Workflow-Aufgaben in der AEM Forms-App aktiviert. CQ-4222638

### In Version 6.3.1.2 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-6}

Liste der in AEM 6.3.1.2 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Liste der in AEM 6.3.1.2 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM Cumulative Fix Pack 6.3.1.1 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 Service Pack 1 (6.3.1.0) im Oktober 2017 mehrere interne und kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Pack sind:

* Aktivierung der Aktion „In Brand Portal veröffentlichen“ für das standardmäßige Metadaten-Schemaformular.
* Verhaltensänderung bei der Anzeige von Titeln auf der Bildkarte für das Bild, für das die dc:title-Eigenschaft auf String [] (Mehrfeld) eingestellt ist.
* Server-seitige Wiedergabe der Zeit durch eine Foundation-Time-Komponente ersetzt.
* Veröffentlichung von Tags von AEM in Brand Portal über die Tagadmin/Tagging-Konsole ermöglicht.
* JSON-API für die Entgegennahme von Inhaltsfragmenten veröffentlicht.
* Das integrierte Repository (Apache Jackrabbit Oak) wird auf Version 1.6.5 aktualisiert.

### Assets {#assets-11}

* Wenn zwei Felder mit derselben Eigenschaft unterschiedlichen Typen von Eigenschaftenfeldern zugeordnet werden, wird ein interner Fehler ausgegeben. NPR-19462: HF für CQ-4216828
* dc:title und dc:description ändert sich nicht in einen Mehrfeld-Wert in  crx/de. NPR-19570: HF für CQ-4209086
* Der Dynamic Viewer lädt eine Videowiedergabe mit der niedrigsten Qualität, um die Videowiedergabe im Autorenmodus zu testen. NPR-19004
* Dynamische Ausgaben können nicht für Assets heruntergeladen werden, die Leerzeichen in ihren Namen enthalten. NPR-19433: Hotfix für CQ-4211738
* Die vollständige Liste der Seiten/Assets kann nicht in der Spaltenansicht mit Chrome geladen werden. NPR-19566: Hotfix für CQ-4214248
* Die Option „In Brand Portal veröffentlichen“ ist bei Auswahl eines Schemas, einer Suchfacette oder einer Vorgabe nicht verfügbar. NPR-19550
* Wenn Sie ein Asset in der Spaltenansicht auswählen und auf „Bearbeiten“ klicken, gibt die Seite einen Fehler aus. NPR-20301: Hotfix für CQ-4224052
* Beim Überschreiten positiver und negativer Zeitzonen ist die Anzeige zum Asset-Ablauf deaktiviert. NPR-20329: Hotfix für CQ-4219333

### Kampagne {#campaign-2}

* Die Komponenten des Campaign-Schiebers werden nicht angezeigt, wenn das Standarderlebnis für eine Campaign ausgewählt wurde. NPR-19213

### Integration {#integration-7}

* Die benutzerdefinierte at.js-Datei wird nicht veröffentlicht, wenn der Zugriff via anonymer Benutzer erfolgt. NPR-19542: Hotfix für CQ-4219592
* Das Targeting-Engine-Feld im Konfigurationsassistenten ist auf ContextHub (AEM) anstelle von Adobe Target eingestellt. NPR-19320: HF für CQ-4218465
* Zielgruppenabschnitt wird beim Erstellen von Experience beschädigt. NPR-19110
* Dialogfeld „Targeting“ wird nicht im Targeting-Modus angezeigt, wenn ein Zielmodul bearbeitet und mehr als einmal gespeichert wird. NPR-19144: Hotfix für CQ-4216708
* Zugriffseigenschaften für Artikel werden in Adobe Digital Publishing Solution in der klassischen Benutzeroberfläche falsch eingestellt. NPR-19367
* Falsches Verhalten der automatischen Faltung bei der Personalisierung von Angeboten über Campaign, wenn Benutzer Zugriff auf mehrere Bereiche haben. NPR-19290: Hotfix für CQ-4218029

### Sites {#sites-11}

* Dropdown-Werte für Felder mit mehreren Kombinationen werden nicht erneut ausgefüllt, da der Code in Sidekick.js nach der Aktualisierung der Instanz auf AEM 6.1SP2-CFP3 geändert wird. NPR-19450: HF für CQ-4194771
* WCMMode.EDIT funktioniert nicht für zielgerichtete Komponenten im Bearbeitungsmodus. NPR-19387
* JSON-API für die Entgegennahme von Inhaltsfragmenten veröffentlicht. NPR-19500
* Fett/kursiv/unterstrichen in Rich-Text-Editor-Feldern im Autorendialogfeld nicht möglich. NPR-19670: NPR-19718: Hotfix für CQ-4219088

### Mobile On-Demand {#mobile-on-demand-1}

* Probleme beim Rendern mit AEM-Artikelkonsole: Verlangsamung bei Verwendung von Bildern in voller Größe. NPR-19088

### Übersetzung {#translation-5}

* Vorschau für Übersetzungsprojekte kann nicht erstellt werden. NPR-19289

### Sicherheit {#security}

* SSL-Verbindungsfehler. Es kann keine sichere Verbindung zum Server hergestellt werden. NPR-19628

### Communities {#communities-9}

* Beim Posten von Inhalten mit vormoderierten Sites wird Mail ausgelöst. NPR-20008
* E-Mail-Benachrichtigungen funktionieren bei keiner der Moderator-bezogenen Aktivitäten zu veröffentlichten Komponenten. NPR-19767: HF für CQ-4218060

### Plattform {#platform-4}

* Stabilitätsprobleme bei der Bereitstellung des AEM-Produktions-Servers. NPR-19707
* Benutzerdefinierte Taglibs, die als Skript implementierte Referenz-Tags enthalten, werden nach der Aktualisierung auf AEM 6.3 nicht gefunden. NPR-19087
* Fehlerbehebungen bei HTL für AEM 6.3.1. NPR-19161
* Das Richtext-Feld kann in den Komponenten mit mehreren Feldern nicht bearbeitet werden. NPR-19604: Hotfix für Granite-16755
* Der Adobe-E-Mail-Vorlagen-Service fügt benutzerdefinierten Benutzervorlagen Tags hinzu. NPR-19190
* Hotfix für Oak 1.6.5. NPR-19148

### Commerce {#commerce-5}

* Schaltfläche „Workflow starten“ nach Auswahl eines XF-Varianteneditors hat keine Auswirkungen. NPR-19642: Hotfix für CQ-4207796

### Projekte {#projects-2}

* Projekteditoren können keine Assets in den Asset-Ordner des Projekts kopieren/einfügen. NPR-19619: Hotfix für CQ-4215321

### Verwaltung von Web-Inhalten  {#web-content-management}

* Im Anzeigebereich „Rollout“ können Kontrollkästchen für LiveCycle-Seiten nicht aktiviert oder deaktiviert werden. NPR-19518
* Die Massenbearbeitung von Seiteneigenschaften ist nicht korrekt nutzbar, da derzeit alle Registerkarten und Felder für die Massenausgabe verfügbar sind. NPR-19451
* OOTB-Eigenschaften und Bildausrichtungseigenschaften werden nicht angezeigt, wenn ein Bild in der klassischen Benutzeroberfläche bearbeitet wird. NPR-19488: HF für CQ-4217914

### Benutzeroberfläche {#user-interface-4}

* Bei Verwendung des Google Chrome-Browsers können Benutzer die vollständige Liste der Seiten/Assets nicht mithilfe der Spaltenansicht in der Touch-optimierten Benutzeroberfläche laden. NPR-19566: Hotfix für CQ-4214248

### Brand Portal {#brand-portal-1}

* Assets können nicht mit Kommentaren und Anmerkungen aus AEM veröffentlicht werden. NPR-19590: Hotfix für CQ-4218386
* Ermöglicht die Veröffentlichung von Tags von AEM im Brand Portal über die Tagadmin/Tagging-Konsole. NPR-20271: Hotfix für CQ-4223948
* Das Feld „Aktiviert“ in der Benutzeroberfläche der Brand Portal-Cloudservice-Konfiguration korrigiert. Hotfix für CQ-4211101
* Suchformular-Replikation schlägt fehl. Hotfix für CQ-4220080

## Forms {#forms-11}

AEM Forms-Fehlerbehebungen werden über Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter den AEM Forms-Versionen.

### Forms-Add-on-Paket {#forms-add-on-package-11}

#### Adaptive Formulare {#adaptive-forms-4}

* Beim Senden an den JEE-Arbeitsablauf wird der Ausgabeparameter nicht von JEE-Seite an AEM zurückgegeben und der Fehler „Ignorieren, weil dies kein primitiver Wert ist“ wird angezeigt. NPR-20265
* Adaptive Formulare lassen PDFs nicht als Anhang in Safari zu. NPR-19625
* RestoreGuideState überschreibt customcontextproperty map. CQ-4222877
* Bei der Konfiguration von Google reCaptcha mithilfe von Cloud Service erfolgen POST-Aufrufe in Umgebungen, die eine Konfiguration von org.apache.http.proxyconfiguration für externe Verbindungen erfordern, offenbar nicht über PROXY. NPR-20454
* Adaptive Formulare, die auf XSD-Schemas basieren, senden fehlerhafte XML-Werte für numerische Felder bei Installationen mit Gebietsschemas, die über ein anderes Dezimaltrennzeichen als „.“ verfügen, was zu Fehlern führt. NPR-20444
* Proxy-Einstellungen, die für „Apache HTTP Components Proxy Configuration“ festgelegt wurden, werden bei HTTP-Anforderungen an Drittanbieter-Server nicht berücksichtigt. Verbindungs-Timeout-Probleme mit HTTP GET- oder POST-Aufrufen. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Forms-Datenintegration {#forms-data-integration}

* UTF-8-Zeichen als Ausgabe des SOAP-Service werden für nicht englischsprachige Gebietsschemas nicht korrekt in adaptive Formularfelder kopiert. NPR-20238: NPR-20103

#### Korrespondenzverwaltung {#correspondence-management-1}

* „Inhalt kopieren“ aus der Textdatei entfernt die Inhaltsfarbe und -schrift im Texteditor. NPR-19521

#### Assembler-Services  {#assembler-services}

* Diskrepanz zwischen den Ergebnissen von Acrobat und AEM bei der Überprüfung der Konformität eines Dokuments mit dem PDF/A-1b-Format. NPR-19280

#### Workflow {#workflow-2}

* Workflow-Signaturschritt, damit HTTP-Aufrufe über den Proxy eine Verbindung herstellen können. NPR-20529

#### HTML5-Formulare {#html-forms-4}

* Unterstützung für preSubmit-Ereignis hinzugefügt. NPR-20604

### Forms JEE-Installationsprogramm {#forms-jee-installer-10}

#### Prozessverwaltung {#process-management-3}

* Registerkarten mit Anlagen, Notizen und Details zum Arbeitsablauf funktionieren nicht im Arbeitsbereich, wenn das Formular maximiert/minimiert und als Entwurf gespeichert oder weitergeleitet wird. NPR-20243
* Mehrzeiliges Textfeld (TextArea) behält kein Zeilenzeichen oder Umbruch im Text bei, nachdem Daten im HTML-Arbeitsbereich übermittelt wurden. NPR-20085

#### Prozessberichterstellung  {#process-reporting}

* Prozessberichte werden aufgrund der „Null Pointer“-Ausnahme nicht korrekt abgerufen. NPR-19759

>[!NOTE]
>
>Installieren Sie das im Artikel [AEM Forms-Versionen](aem-forms-releases.md) aufgelistete LiveCycle-Einbettungspaket, um das Problem zu beheben.

#### Standard-Services {#standard-services}

* docConvertor unterstützt keine Reduzierung von Transparenzen in PDF und erzeugt keine PDF/A-Datei. NPR-16228: Hotfix für CQ-4214488

#### Core  {#core-2}

* Wenn der AEM Forms-Server, der in einer Cluster-Konfiguration auf der JBoss-Anwendung ausgeführt wird, beendet wird, wird der Programm-Server von der Datenbank getrennt. Dies kann zu Datenbeschädigung führen. NPR-19724

### Enthaltene Feature Packs {#feature-packs-included-1}

* „Obligatorisch“ für Dropdown-Metadatenschema-Feld nicht möglich, da die obligatorische Feldüberprüfung für Assets fehlt. NPR-17882: FP für CQ-4208373

### In Version 6.3.1.1 enthaltene OSGi-Bundles und Inhaltspakete  {#osgi-bundles-and-content-packages-included-in-7}

Liste der in AEM CFP 6.3.1.1 enthaltenen OSGi-Bundles

[Datei laden](assets/do-not-localize/bundle-list.txt)

Liste der in AEM CFP 6.3.1.1 enthaltenen Inhaltspakete

[Datei laden](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2 ist ein wichtiges Update, das seit der allgemeinen Verfügbarkeit von AEM 6.3 im April 2017 mehrere interne und kundenspezifische Korrekturen enthält.

Die wichtigsten Highlights des AEM Cumulative Fix Pack sind:

* Berechenbarkeit der Benutzerzugriffssteuerung
* Enthält Version 1.6.2 des eingebauten Repositorys (Apache Jackrabbit Oak)
* Gelöste, nicht abgeschlossene Ressourcen-Resolutionsprobleme
* Vereinfachte Konfiguration für intelligente Inhalts-Services
* Validierungsprobleme von Inhaltsfragmenten behoben
* Verbesserte Bearbeitbarkeit von Metadatenschemas auf Hybridgeräten
* Behobene Synchronisierungsprobleme auf Komponentenebene in Live Copies
* Verbesserte Benutzerfreundlichkeit von Seiten mit viel Inhalt in der Spaltenansicht
* Verbesserte Einhaltung der Seitenbenennungsregel für Seiten mit langen Titeln
* Verbesserte Kampagnenpersonalisierung in der Touch-optimierten Benutzeroberfläche
* Fehlerbehebungen bei verschiedenen Problemen mit der Projektüberlagerung

### Plattform {#platform-5}

* Hotfix für Oak 1.6.2. NPR-16993
* Beim Öffnen von Omnisearch mit einem Filter wird der Pfad nicht mehr festgelegt. NPR-17398: Hotfix für CQ-4204870
* Voraussetzung für die Prüfbarkeit von Änderungen an Benutzerberechtigungen in AEM. NPR-17061
* „Hängende“ Verbindungen zu DM Cloud Services, wodurch Ausnahmen vom Typ „Zu viele geöffnete Dateien“ entstehen. CQ-4211407

### Assets {#assets-12}

* Probleme mit der Benutzerfreundlichkeit bei der Konfiguration intelligenter Inhalts-Services mit verschiedenen Optionen. NPR-18200: Hotfix für CQ-4201557
* Ressourcen-Verluste in binären Streams zum S3-Datenspeicher. NPR-18041: Hotfix für CQ-4209506
* Ein Fehler tritt auf, wenn eine ASCII/UTF-8-kodierte Textdatei in AEM Assets hochgeladen wird und die Erstellung von Miniaturbildern fehlschlägt. NPR-18006: CFP für CQ-4209345
* Das Standard-Metadatenschema verursacht einen Fehler bei der Überprüfung des Inhaltsfragments. NPR-17769: Hotfix für CQ-4211111
* Nicht geschlossener Ressourcen-Resolver in com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP für CQ-4209018
* Anforderung zum Erstellen mehrerer Replikationsagenten für das Veröffentlichen von Assets in Brand Portal. NPR-17189
* Überprüfungsaufgabe für Assets im japanischen Sprachordner funktioniert nicht. CQ-4204782
* „Null Pointer“-Ausnahme beim Verschieben eines Assets von seiner Eigenschaftsseite. CQ-4204251
* AEM kann nachfolgende Verweise auf ein Asset auf der Eigenschaftsseite nicht verfolgen, wenn es mehrmals mit einem InDesign-Dokument verknüpft ist. CQ-4204186
* Probleme mit dem Hinzufügen neuer Registerkarten im Metadatenschema-Formular, wenn es in Chrome auf Hybrid-Geräten bearbeitet wird. CQ-4201810
* Beim Hochladen doppelter Assets wird die (löschen/beibehalten)-Option auf alle Assets angewendet, auch wenn sie nicht im Dialogfeld „Duplikate erkannt“ ausgewählt ist. CQ-4201673
* „Null Pointer“-Ausnahme beim Verschieben eines Asset-Ordners mit mehr als 150 eingehenden Referenzen. CQ-4200981
* Wenn bei einem heruntergeladenen Asset-Ordner beim Extrahieren des Inhalts der ZIP-Datei ein Konflikt auftritt, wird die Standardoption als „Version erstellen“ anstelle von „Beide behalten“ angezeigt. CQ-97800
* Benutzer mit Nur-Lese-Berechtigungen für die App können keine Vorschau von Inhalten aus dem AEM Mobile-Inhalts-Management anzeigen. NPR-17486: CFP für CQ-4209690
* Die Schaltfläche „Katalog erstellen“ funktioniert in der Spaltenansicht der Katalogkonsole nicht. CQ-4209952

### Sites {#sites-12}

* Probleme mit dem Einbetten von Bild-/Videokomponenten über das data-sly-resource-Attribut. NPR-18182: CFP für CQ-4212100
* Geänderte lokalisierte Komponenten werden nicht in ihrem ursprünglichen Formular wiederhergestellt, wenn die Vererbung in einer LiveCopy erneut angewendet wird. NPR-18172: Hotfix für CQ-4211379
* Probleme beim Navigieren in einer inhaltsreichen Seite in der Spaltenansicht der Touch-optimierten Benutzeroberfläche. NPR-17799: Hotfix für CQ-4199611
* Ungeschlossener Ressourcenauflöser in `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP für CQ-4211152
* Seitenname wird nicht gemäß der Regel für lange Seitentitel generiert. NPR-17633: Hotfix für CQ-4209056
* Probleme mit der Seitenerstellung in der Touch-optimierten Benutzeroberfläche in AEM 6.3, die auf Jboss EAP 6.4 bereitgestellt wurde. NPR-17589: Hotfix von CQ-4210137
* Der Workflow-Status-Provider veranlasst die Sperrung der Instanz, wenn verschachtelte Gruppen vorhanden sind. NPR-17556: CFP-Anfrage für CQ-4202056
* Nicht geschlossener Ressourcen-Resolver in den folgenden Objekten:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP für CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP für CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP für CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP für GRANITE-17404

### Integrationen {#integrations-1}

* Behebung von Fehlern in der AEM-Suchkomponente, die auftreten können, wenn AEM Day HTTP Client 3.1 OSGi mit einem Proxy konfiguriert ist, für den die Digest-Authentifizierung erforderlich ist. NPR 18128: Hotfix für NPR-18029
* Probleme mit der Personalisierung von Kampagnen und zugehörigen Erlebnissen über die klassische Benutzeroberfläche. NPR-18127: Hotfix für CQ-4211559
* Wenn Sie eine Marke/Zone auf eine Stammseite einer Site setzen, kann die Vererbung nach dem Abbrechen für Bereiche in Unterseiten nicht wiederhergestellt werden. NPR-17753: Hotfix für CQ-4210139

### Workflow {#workflow-3}

* In einem nicht-transienten Workflow werden die vor einem externen Prozessschritt vorgenommenen Änderungen am Prozessverlauf und an den Metadaten nicht beibehalten. NPR-17848: Hotfix für GRANITE-17757
* Werte aus Workflow-Dialogfeldfeldern bleiben nicht im Arbeitselementknoten erhalten. NPR-17734: Hotfix für CQ-4210369
* Fehler „Datum kann nicht geparst werden“ tritt auf, wenn eine Aufgabe aus dem Posteingang bearbeitet wird. CQ-4208749

### Projekte {#projects-3}

* Fehlerbehebungen bei verschiedenen Problemen mit der Projektüberlagerung. NPR-17733
* Die Umstrukturierung der Pods im Projektmodul macht es weniger konfigurierbar. CQ-4209859
* Asset-Pfad ändert sich zu den jeweiligen lokalisierten Sites, wenn dem Übersetzungsauftrag Seiten hinzugefügt werden. CQ-4206007

### Sicherheit {#security-1}

* Probleme beim Hochladen von Avatar-Bildern für LDAP-Benutzer. NPR-16561
* Anforderung der Verwendung einer aktualisierten Version von org.apache.sling.servlets.post servlet (2.3.22) in der Apache Sling API, um eine XSS-Schwachstelle zu verhindern. NPR-18963

## Forms {#forms-12}

AEM Forms-Fehlerbehebungen werden über Forms-Add-on-Pakete und andere mit der Version gelieferte Patch-Installationsprogramme bereitgestellt. Weitere Informationen finden Sie unter [AEM Forms-Versionen](aem-forms-releases.md).

Die wichtigsten Highlights für AEM Forms sind:

* Korrekturen in Textmodulen der Korrespondenzverwaltung, Briefvorschauen und programmgesteuertem Starten der Benutzeroberfläche zum Erstellen in der Korrespondenzverwaltung.
* Korrekturen für die PDF/A-1b-Validierung, Konvertierung großer Bilddateien in PDF und PDF-Dokumente in japanischer Sprache in PDF Generator.
* Korrekturen an der Benutzerfreundlichkeit für Korrespondenzverwaltung, Dokumentsicherheit und Formular-Workflow.
* Unterstützung zum Erfassen von Prüfereignissen für das Freihand-Signaturfeld hinzugefügt.

### Forms-Add-on-Paket {#forms-add-on-package-12}

**Korrespondenzverwaltung**

* Beim Bearbeiten eines Korrespondenzverwaltungs-Fragments zeigt der Texteditor Inline-Bedingungen zusammen mit dem verarbeiteten Text an. CQ-4211930
* Beim Erstellen eines Korrespondenzverwaltungs-Briefs wird die Beschreibung des Briefs nicht gespeichert. NPR-18089
* Zusätzliche Ränder über und unter einer Liste mit Aufzählungszeichen sind im Texteditor sichtbar, nicht jedoch in der HTML- und PDF-Wiedergabe. NPR-18126
* Wenn beim HTML-Senden die POST-Methode verwendet wurde, kann die Benutzeroberfläche „Korrespondenz erstellen“ nicht gestartet werden. NPR-18202
* Wenn ein Textmodul gespeichert wird und ein Ausdruck im Textmodul keine öffnenden oder schließenden Ausdrucks-Tags enthält, wird keine Fehlermeldung angezeigt. Das Textmodul zeigt eine Fehlermeldung an und Rendering im Brief funktioniert nicht. NPR-18535
* Wenn neue Inhalte hinzugefügt werden oder die Eingabetaste gedrückt wird, wird dem Textmodul ein div-Tag hinzugefügt. NPR-18240

**Assembler**

* Beim Überprüfen eines PDF-Dokuments auf PDF/A-1b-Kompatibilität gibt AEM Forms einen Validierungsfehler zurück: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. Das PDF-Dokument gibt den Fehler nicht zurück, wenn es mit Adobe Preflight und Software von Drittanbietern validiert wurde. NPR-18011
* Bei der Validierung von PDF-Dokumenten auf PDF/A-1b-Konformität gibt AEM Forms einen Validierungsfehler zurück: Das Formularfeld wird mehrfach angezeigt. Die PDF-Dokumente sind PDF/A-1b-kompatibel. NPR-18013

**Überwachungsordner**

* Bei der Auswahl, ob Dateien mit einem Workflow verarbeitet werden sollen, während Sie einen Überwachungsordner erstellen, wird die Dropdown-Liste für die Auswahl des Workflow-Modells abgeschnitten angezeigt. NPR-17566

**HTML5-Formulare**

* AEM Forms erfasst keine Audit-Ereignisse für das Freihand-Signaturfeld. NPR-15286

**Forms Manager**

* In der Benutzeroberfläche von AEM Forms werden die Assets beginnend mit dem ältesten aufgelistet. Benutzer können die Sortierreihenfolge nicht so ändern, dass mit dem neuesten Asset begonnen wird. NPR-18450

**Java API-Referenz**

JavaDocs für die Klasse com.adobe.livecycle.content hinzugefügt. NPR-18468

### Forms JEE-Installationsprogramm {#forms-jee-installer-11}

**PDF Generator**

* Der PDF Generator-Service kann Bilder, die größer als 100 MB sind, nicht in PDF-Dokumente konvertieren. Referenznummer CQ-4208628
* Bei Verwendung des PDF Generator-Servoce mit Japanisch-OCR (Zeichenerkennung) wird eine invertierte PDF generiert. NPR-17602

**Prozessverwaltung**

* Die TaskContext-Variable wird für AEM Forms-Prozesse nicht gefüllt. NPR-18199

**Dokumentensicherheit**

* Microsoft Excel und Microsoft PowerPoint brauchen viel länger, um die mit AEM Document Security Extension for Microsoft Office geschützten Dokumente zu öffnen. CQ-4212358
* Wenn eine neue Richtlinie mit demselben Namen wie eine vorhandene erstellt wird, tritt ein interner Server-Fehler auf. NPR-18247

## Enthaltene Feature Packs {#feature-packs-included-2}

* Voraussetzung für die Prüfbarkeit von Änderungen an Benutzerberechtigungen in AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 ist ein wichtiges Update, das mehrere interne und kundenspezifische Fehlerbehebungen seit der allgemeinen Verfügbarkeit von AEM 6.3 im April 2017 enthält. Die wichtigsten Highlights des AEM Cumulative Fix Pack sind:

* Verbesserungen in folgenden Bereichen:

   * Inhaltsfragmente, Sites- und Rich-Text-Editor-, Regel-Editor- und Vorlagen-Editor-Komponenten
   * Social Review und Facebook Social-Anmeldung
   * Konfigurieren und Starten von Übersetzungsaufträgen
   * Reaktionszeit für den Zugriff auf Benachrichtigungen in Social Communities
   * Anzeigen von Review-Aufgaben im DAM-Repository

* Überprüfungsoption im Package Manager zum Erkennen von Konflikten zwischen Überlagerung und CFP

## Download-Anweisungen für CFP über Software Distribution {#download-instructions-for-cfp-via-package-share}

Sie können das CFP-Paket direkt von der Seite [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/AEM-CFP-6.3.3.8) herunterladen oder die folgenden Schritte ausführen:

1. Öffnen Sie [Software Distribution](https://experience.adobe.com/downloads). Zum Anmelden bei Software Distribution benötigen Sie eine Adobe ID.
1. Tippen Sie im Kopfzeilenmenü auf **[!UICONTROL Adobe Experience Manager]**.
1. Tippen Sie auf den Paketnamen, wählen Sie **[!UICONTROL EULA-Bedingungen akzeptieren]** und tippen Sie auf **[!UICONTROL Herunterladen]**.

## Installationsanweisungen {#installation-instructions}

Dieser Abschnitt erläutert die Anforderungen und Schritte zur Installation von CFP.

### Vor der Installation {#before-you-install}

>[!NOTE]
>
>Die von Adobe bereitgestellten optionalen Funktionspakete hängen von der Release-Version und dem Cumulative Fix Pack ab. Wenn Sie ein Feature Pack installiert haben, wenden Sie sich bitte an die [AEM-Kundenunterstützung](https://helpx.adobe.com/de/marketing-cloud/contact-support.html), um die Kompatibilität mit diesem Cumulative Fix Pack für AEM 6.3 zu überprüfen.

>[!NOTE]
>
>Es wird empfohlen, die Überprüfung für jedes neue Installationspaket auszuführen, bevor Sie versuchen, das Paket zu installieren. Vor der Überprüfung werden alle Fehler analysiert und protokolliert, die vor der Installation gefunden wurden, und die Benutzer werden proaktiv vor solchen Fehlern gewarnt.
>
>Sie finden die Dokumentation zur Überprüfungsoption unter [https://docs.adobe.com/content/docs/de-DE/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/de-DE/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 ist eine Voraussetzung für CFP. Detaillierte Anweisungen zum Aktualisieren einer AEM-Installation auf AEM 6.3 finden Sie in der [Upgrade-Dokumentation.](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html)
* Bei einer Cluster-Bereitstellung mit RDBMK oder MongoDB kann das CFP-Paket auf einer der Autorinstanzen installiert werden, die Package Manager verwendet.
* Bevor Sie das Cumulative Fix Pack installieren, stellen Sie sicher, dass Sie einen Schnappschuss oder eine Sicherungskopie Ihrer AEM-Instanz erstellen.
* Die Deinstallation von CFP wird nicht unterstützt.

### Hinzufügen neuer Logger  {#adding-new-loggers}

Gehen Sie wie folgt vor, um die Protokollierung auf Debugging-Ebene zu konfigurieren und während der Installation von SPs/CFPs ein Aktivitätsprotokoll abzurufen:

* Sie können mit den folgenden Eigenschaften eine neue Protokollfunktion am Standardspeicherort [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) hinzufügen:

   * Protokollebene: Debug
   * Additive: false
   * Log File: logs/activity.log
   * Protokollfunktion: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

activity.log wird erstellt im Ordner crx-quickstart/logs.

### Installieren Sie das Cumulative Fix Pack über Software Distribution {#install-the-cumulative-fix-pack-via-package-share}

Führen Sie die folgenden Schritte aus, um das Cumulative Fix Pack auf einer vorhandenen AEM 6.3-Instanz zu installieren:

1. Klicken Sie auf den Link [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip), um das Paket herunterzuladen.

1. Öffnen Sie [Package Manager](http://localhost:4502/crx/packmgr/index.jsp) und klicken Sie auf **[!UICONTROL Paket hochladen]**, um das Paket hochzuladen.

1. Wählen Sie das Paket aus und klicken Sie auf **[!UICONTROL Installieren]**.

### Automatische Installation {#automatic-installation}

CFP kann wie folgt automatisch in einer laufenden Instanz installiert werden:

* Platzieren Sie das Paket in `../crx-quickstart/install`, während der Server läuft. Das Paket wird automatisch installiert.
* Verwenden Sie die [HTTP-API aus Package Manager](https://helpx.adobe.com/de/experience-manager/6-3/sites/administering/using/package-manager.html) – es muss `cmd=install&recursive=true` sein –, damit das verschachtelte Paket installiert wird.

### Bestätigen der Installation {#validate-installation}

1. Auf der Seite „Produktinformationen“ (`/system/console/  productinfo`) sollte nun unter „Installierte Produkte“ die aktualisierte Version „Adobe Experience Manager, Version 6.3.3.8“ angezeigt werden.
1. Alle OSGi-Bundles sind entweder ACTIVE oder FRAGMENT in der OSGi-Konsole (Web-Konsole verwenden: `/system/console/bundles`).

>[!NOTE]
>
>Bei erfolgreicher Installation des Pakets wird in den Fehlerprotokollen eine Informationsmeldung angezeigt, die darauf hinweist, dass das Inhaltspaket erfolgreich installiert wurde, z. B. „**AEM-6.3.3-Cumulative-Fix-Pack-7** wurde erfolgreich installiert.“

>[!NOTE]
>
>Seit AEM 6.3.3.1 hat sich die Protokollierungsstufe in Jackrabbit FileVault für die meisten Meldungen von INFO in DEBUG geändert. Um Installationsprotokolle für ein auf AEM 6.3.3.1 oder höher installiertes Inhaltspaket zu erhalten, aktivieren Sie die DEBUG-Protokollierungsstufe für org.apache.jackrabbit.vault.processing.impl.

### Installieren von AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Überspringen Sie diesen Abschnitt, wenn Sie AEM Forms nicht verwenden.

#### AEM Forms-Add-on installieren  {#install-forms}

1. Vergewissern Sie sich, dass Sie das AEM 6.3.3.x CFP-Paket installiert haben.
1. Wählen Sie unter den aufgeführten [AEM Forms-Versionen](aem-forms-releases.md) das für Ihr Betriebssystem passende Forms-Add-on-Paket aus und laden Sie es herunter.
1. Installieren Sie das Forms-Add-on-Paket wie unter [Installieren des AEM Forms-Add-on-Pakets](https://helpx.adobe.com/de/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html) beschrieben.

#### Installieren des AEM Forms JEE-Bundles-Pakets {#install-aem-forms-jee-bundles-package}

Fehlerbehebungen in AEM Forms JEE werden über ein separates Installationsprogramm bereitgestellt. Informationen zum Installieren einer CFP auf AEM Forms on JEE finden Sie unter [Installieren von CFP auf AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Forms Designer-Installationsprogramm  {#designer-installer}

1. Führen Sie zur Installation des Updates die Datei „Designer 6.2.0_&lt;Sprache>_Cumulative_QF.msp“ aus.
1. Klicken Sie auf dem Begrüßungsbildschirm auf **Aktualisieren**. Die Installation wird gestartet.
1. Klicken Sie nach Abschluss der Installation auf **Beenden**.

## Konfigurationseinstellungen für AEM Forms JEE (JBoss EAP)  {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Wenn Sie Version 6.3.3.0 oder höher installieren, führen Sie das folgende Verfahren aus, um die Einstellungen für JBoss Application Server zu konfigurieren. Wenn Sie 6.3.3.0 auf dem AEM Forms Server installieren, der auf Oracle WebLogic- oder IBM WebSphere-Programm-Servern ausgeführt wird, ist keine zusätzliche Konfiguration erforderlich. Weitere Informationen finden Sie unter [AEM 6.3.3.0 - Versionshinweise](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

## Konfigurationsaktualisierungen für die Search&amp;Promote-Integration {#configuration-updates-for-search-promote-integration}

Bei AEM Cumulative Fix Pack 6.3.0.2 und höher ist die OSGi-Konfiguration, die für die Search&amp;Promote-Integration verwendet wird, die **Apache HTTP Components Proxy Configuration**. Die Proxy-Konfiguration von Day Commons HTTP Client 3.1 wird nicht mehr verwendet.

## Bekannte Probleme {#known-issues}

* Die folgenden Fehler und Warnungen können während der Installation von AEM CFP 6.3.3.x auftreten und können ignoriert werden:

   * *WARN* [OsgiInstallerImpl] org.apache.jackrabbit.package.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallaken-0.0.2-jar-with-dependencies.jar gab eine Laufzeitausnahme aus.
   * *ERROR* [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Zeitüberschreitung beim Warten darauf, dass die Registrierung geändert wird, um das Aufheben der Registrierung abzuschließen. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver-Service fehlt, kann keine Service-Anforderungen senden, Sendestatus 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: Ressource [/bin/receive] kann nicht überprüft werden, Seitenmanager nicht verfügbar
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Der Aufruf des Fehlerhandlers führte zu einem Fehler
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Ursprünglicher Fehler null
   * org.apache.sling.engine.impl.DefaultErrorHandler Fehlerhandler failed:java.io.IOException
   * *ERROR* [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service Factory gibt Null aus. (Component: com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* Ab 6.3.1.2 wurde die Schaltfläche „In Brand Portal veröffentlichen“ für Smart-Sammlungen entfernt.

**Benutzeroberfläche**

>[!NOTE]
>
>Falls Sie von einem dieser beiden Probleme betroffen sind, wenden Sie sich an die [AEM-Kundenunterstützung](https://helpx.adobe.com/marketing-cloud/contact-support.html).

* Eine hohe CPU-Auslastung wird durch viele Anforderungen in der Funktionalität der Admin-Suche festgestellt. NPR-24229
* PathField wird beim erneuten Öffnen der Komponente nicht in pathBrowser ausgewählt. NPR-24177

## Für NPR-27692 erforderliche Konfigurationseinstellungen  {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Diese Konfigurationseinstellung gilt für CFP 6.3.3.2 und höher. Sie weist Sie an, die Eigenschaften der Bootdelegation in der`sling` .properties-Datei zu aktualisieren.

Gehen Sie wie folgt vor, um Änderungen in adobe-livecycle-cq-author.ear/cq.war manuell zu aktualisieren:

* Beenden Sie den AEM-Server.
* Wechseln Sie zu adobe-livecycle-cq-author.ear/cq.war
* Öffnen Sie adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml zur Bearbeitung:

   * Aktualisieren Sie den Wert **sling.bootdelegation.ibm** param-name mit:

      * com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * Nach der obigen Änderung sollte init-param wie folgt aussehen:

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.*,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* Deinstallieren Sie die vorherige EAR-Datei (Enterprise Archive) vom Websphere-Programm-Server und installieren Sie die aktualisierte EAR-Datei, wie in Abschnitt 10.2 in [https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-websphere.pdf) beschrieben.
* Speichern Sie die Datei und starten Sie den Server neu. [https://helpx.adobe.com/de/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Für NPR-23208 erforderliche Konfigurationseinstellungen {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Diese Konfigurationseinstellung gilt für 6.3.2.2 und höher. Sie weist Sie an, die Richtlinien für Zugriffskontrolllisten (ACLs) manuell über CRX-DE zu aktualisieren, da ACLs aufgrund von „merge_preserve“ nicht über die CFP-Installation aktualisiert werden.

**Dokumentation zum manuellen Hinzufügen von ACL-Richtlinien**

Um ACL-Richtlinien zu aktualisieren, fügen Sie die folgenden Zugriffssteuerelemente über CRX-DE hinzu:

`1)` Pfad „/content“\
`a)` Prinzipal : reference-Adjustment-Service\
Typ : Allow\
Berechtigungen : jcr:read, jcr:modifyProperties\
Einschränkungen : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Prinzipal : reference-Adjustment-Service\
Typ : Allow\
Berechtigungen : jcr:read, jcr:modifyProperties\
Einschränkungen : rep:glob=&quot;/*/jcr:content/*&quot;

`2)` Pfad „/content/usergenerated“\
`a)` Prinzipal : reference-Adjustment-Service\
Typ : Allow\
Einschränkungen : jcr:write

`3)` Pfad „/etc“\
`a)` Prinzipal : reference-Adjustment-Service\
Typ : Allow\
Berechtigungen : jcr:read, jcr:modifyProperties\
Einschränkungen : rep:glob=&quot;/*/jcr:content&quot;\
`b)` Prinzipal : reference-Adjustment-Service\
Typ : Allow\
Berechtigungen : jcr:read, jcr:modifyProperties\
Einschränkungen : rep:glob=&quot;/*/jcr:content/*&quot;

## Für NPR-19450 erforderliche Konfigurationseinstellungen {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Diese Konfigurationseinstellung gilt für CFP 6.3.1.1 und höher.

**Konfigurieren Sie die Eigenschaft CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

Die Eigenschaft steuert die maximale Tiefe des Knotenunterbaums unter dem Seitenknoten ` /  jcr   :content`, bis zu dem die im Repository vorhandenen Knoten zum Abrufen der Seiteneigenschaften verwendet werden. Jeder Knoten, der unter der angegebenen Tiefe in dieser Eigenschaft vorhanden ist, wird ignoriert.

Der Standardwert ist 1. Der Wert kann  überschrieben werden, indem die Datei „constants.js“ (`/libs/cq/ui/widgets/source/constants.js`) durch Auskommentieren der Eigenschaft „CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL“ aufgehoben und ihr der erforderliche Wert zugewiesen wird (die maximale Tiefe unter dem / jcr  :content-Knoten der Seite, bis zu dem die Daten der Seiteneigenschaften gespeichert werden).

**Wenn der Benutzer mehrere Seitenvarianten erstellen muss, sodass die Anzahl der Knoten unter dem /  jcr   :content-Knoten größer als 1000 ist, führen Sie die folgenden Schritte aus, um Konfigurationsänderungen vorzunehmen:**

* Konfigurieren Sie die Eigenschaft „JSON Max results“ von Apache Sling
* Get-Servlet mit `/system/console/  configMgr`/
* Setzen Sie den Wert auf eine Zahl > 1.000 (der aktuelle Standard), sodass diese Zahl größer ist als die Gesamtanzahl der Knoten im Unterknoten / jcr  :content bis zur oben konfigurierten Tiefe.

Dadurch kann das Sling GET-Servlet alle erforderlichen Knoten ausgeben.

## Uber Jar {#uber-jar}

Uber Jar für 6.3.3.8 ist im [Adobe Public Maven Repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/) verfügbar.

Informationen zur Verwendung von Uber Jar in einem Maven-Projekt finden Sie in [diesem Artikel](https://helpx.adobe.com/de/experience-manager/6-3/sites/developing/using/ht-projects-maven.html). Beziehen Sie die folgenden Abhängigkeiten in Ihr Projekt-POM ein:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Entfernte/veraltete Funktionen {#deprecated}

Dieser Abschnitt listet Funktionen und Fähigkeiten auf, die aus AEM 6.3 entfernt oder veraltet sind.

| Bereich | Funktion | Ersatz | Version |
|----|-----|-----|-----|
| Assets und Adobe Creative Cloud-Integration | [Die gemeinsame Nutzung von AEM-Ordnern in Creative Cloud](https://helpx.adobe.com/de/experience-manager/6-3/sites/administering/using/creative-cloud.html) wurde in AEM 6.2 eingeführt, um Benutzern von Creative Cloud den Zugang zu den Assets von AEM zu ermöglichen. Eine neue Funktion des Creative Cloud-Programms, Adobe Asset Link, bietet ein wesentlich besseres Benutzererlebnis und einen leistungsfähigeren Zugriff auf Assets aus AEM direkt aus Photoshop, InDesign und Illustrator heraus.<br /> Adobe wird die Ordnerfreigabe nicht weiter verbessern. Obwohl die Funktion in AEM enthalten ist, wird den Kunden dringend empfohlen, den Ersatz zu verwenden. | Adobe Asset Link oder Desktop-Programm. Weitere Informationen finden Sie im Artikel zur [AEM Creative Cloud-Integration](https://helpx.adobe.com/de/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html). | AEM 6.3.3.x |

## Enthaltene OSGi-Bundles und Inhaltspakete {#osgi-bundles-and-content-packages-included-1}

In den folgenden Textdokumenten sind die OSGi-Bundles und Content-Pakete der CFP aufgeführt.

* [Liste der in AEM 6.3.3.8 enthaltenen OSGi-Bundles](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Liste der in AEM 6.3.3.8 enthaltenen Inhaltspakete](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [Versionen und Aktualisierungen von AEM](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates.html?lang=de)
>* [Seite mit den AEM 6.3 Hotfixes](https://helpx.adobe.com/de/experience-manager/kb/aem63-available-hotfixes.html)
>* [AEM 6.3 – Versionshinweise](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM-Produktseite](http://www.adobe.com/de/solutions/web-experience-management.html)
>* [Dokumentation zu AEM 6.3](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* Abonnieren von [Adobe-Prioritäts-Produkt-Updates](https://www.adobe.com/subscription/priority-product-update.html)

