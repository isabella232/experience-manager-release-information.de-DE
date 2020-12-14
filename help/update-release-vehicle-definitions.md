---
title: Definitionen des Releasebilds aktualisieren
description: In diesem Artikel werden die verschiedenen Arten von [!DNL Experience Manager] Versionen beschrieben, einschließlich Vollversionen, Feature Packs und Services Packs.
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 34%

---


# [!DNL Experience Manager] Definitionen von Releasebildern aktualisieren  {#update-release-vehicle-definitions}

Dieses Dokument enthält Informationen zu den verschiedenen Versionen von [!DNL Adobe Experience Manager], einschließlich Vollversionen, Feature Packs und Services Packs, die [!DNL Adobe] an Kunden liefert.

>[!NOTE]
>
>Versionsplan für [!DNL Experience Manager] Update-Versionen finden Sie unter [[!DNL Experience Manager] Roadmap für Updateversionen](update-releases-roadmap.md)

## Vollversion {#full-release}

| Elemente | Beschreibung |
|-------|------|
| Definition | <ul> <li> Geplante Veröffentlichung </li> <li> Unterstützt Aktualisierungspfade für bestimmte Versionen, die in den Versionshinweisen definiert sind </li> </ul> |
| Benennung  | <ul> <li> Die Versionsnummern für größere Releases erhöhen sich nach der Formel X+1.Y.Z. </li> <li> Versionsnummern für kleinere Releases erhöhen sich je nach Formel X.Y+1.Z </li> </ul> Dabei ist X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer. |
| Lieferumfang  | <ul> <li> Neue Funktionen </li> <li>  Verbesserungen </li> <li>  Fehlerbehebungen </li> </ul> |
| Dokumentation | <ul> <li> Versionshinweise finden Sie im Dokumentationsportal. </li> <li> Dokumentation zu Funktionen, Verbesserungen und Fehlerkorrekturen finden Sie im Dokumentationsportal </li> </ul> |
| Veröffentlichungsintervall  | Jährlich |
| Verfügbarkeit und Installation  | <ul> <li> Lieferbar als eigenständiges Produktinstallationsprogramm </li> <li>  Verfügbar auf der Lizenzierungs-Website und Managed Services </li> <li> Lizenzierungs-Website erfordert möglicherweise eine Migration zum Content Repository </li> </ul> |
| Teststufe  | Vollständige Validierung durch Qualitätssicherung |

## Service Pack {#service-pack}

| Item | Beschreibung |
|-----|-----|
| Definition | <ul> <li> Geplante Veröffentlichung </li> <li> Derzeit kann kein Rollback durchgeführt werden </li> </ul> |
| Benennung  | <ul> <li> Patch-Versionsnummer ist eine einstellige Zahl </li> <li> Erhöhen Sie nach der Installation die Zahl des installierten Patch für die Versionsnummer, basierend auf der Formel X.Y.Z.SPx. </li> </ul> Dabei ist X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer. x ist die Service-Pack-Nummer. |
| Lieferumfang  | <ul> <li> Neue Funktionen</li> <li>  Verbesserungen </li> <li> Fehlerbehebungen </li> <li> Häufig verwendete Funktionspakete (falls vorhanden) </li> </ul> |
| Dokumentation | <ul> <li> Versionshinweise im Dokumentationsportal </li> <li> Dokumentation zu Funktionen, Verbesserungen, Fehlerbehebungen im Dokumentationsportal </li> </ul> |
| Veröffentlichungsintervall  | Vierteljährlich |
| Verfügbarkeit und Installation  | <ul> <li> Wird als Paket bereitgestellt </li> <li> Verfügbar über Softwareverteilung</li> <li>  Vorhandene funktionale Installation erforderlich </li> </ul> |
| Teststufe  | <ul> <li> Alle für die Qualitätssicherung validierten Fehlerbehebungen </li> <li>  Gesamte Paketsicherheit mit Automatisierungsläufen </li> </ul> |

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

| Posten | Beschreibung |
|-----|-----|
| Definition | <ul> <li> Ein Versand-Modell für die Freigabe von Korrekturen </li> <li> Aggregator-Inhaltspaket mit Inhaltspaket einzelner Komponenten </li> <li>  CFPs sind ein Rollover von Hotfixes, und es gibt keine Verbesserungen.  </li> </ul> |
| Benennung  | X.Y.Z.CFPx <br> wobei X die primäre Versionsnummer, Y die sekundäre Versionsnummer und Z die Patch-Nummer ist. x ist die Nummer des Cumulative Service Packs. |
| Lieferumfang  | CFP ist ein kumulatives Fixpack, das Korrekturen aller Komponenten bis zu einem bestimmten Datum enthält. Wenn ein Kunde z. B. CFP3 anwendet, gilt CFP3 = CFP1 + CFP2. |
| Dokumentation | Versionshinweise im Dokumentationsportal |
| Veröffentlichungsintervall  | Vierteljährlich |
| Verfügbarkeit und Installation  | <ul> <li> Wird als Paket bereitgestellt </li> <li>  Verfügbar über Softwareverteilung </li> <li>  Abhängig vom neuesten Service Pack veröffentlicht </li> <li>  Die CFP ist selbstständig. Kunden müssen sich nicht über die Suche nach/das Auflösen von Abhängigkeiten den Kopf zerbrechen. CFPs sollten nach dem zuletzt veröffentlichten Service Pack installiert werden. </li> <li>  CFPs können als ein Paket installiert werden und verbessern so das Kundenerlebnis.  </li> </ul> |
| Teststufe  | Auf Integration validierte Qualitätssicherung und Regressionstests |

## Überlagerung {#overlay}

| Posten | Details |
|-------|--------|
| Benennung  | overlay-&lt;Ticket-ID> |
| Lieferumfang  | Fehlerbehebung für eine JS- oder JSP-Datei |
| Dokumentation | Kein |
| Veröffentlichungsintervall  | Erforderlich |
| Verfügbarkeit und Installation  | <ul> <li> Lieferbar als Paket von [!DNL Experience Manager] Kundendienst  </li> <li> Nicht unbedingt in Service Packs oder Vollversionen enthalten </li> </ul> |
| Teststufe  | Validiert durch die Kundenunterstützung |

## Feature Pack {#feature-pack}

| Elemente | Details |
|--------|-----|
| Definition | <ul> <li>Feature Packs sind Zusatzfunktionalitäten und werden über Service Packs bereitgestellt. Wenn eine [!DNL Experience Manager]-Version ihr letztes Service Pack veröffentlicht hat, stellt die Adobe in Zukunft kein Feature Pack dafür bereit. </li> <li> RPs enthalten Produktverbesserungen, die für eine spätere Produktversion geplant sind, aber frühzeitig auf der Grundlage der Entscheidung von [!DNL Adobe's] Produktverwaltung bereitgestellt werden.</li> <li>  Funktionen werden immer mit der nächsten Hauptversion zusammengeführt und dann in die [!DNL Experience Manager] Version portiert, die vom Kunden benötigt wird </li> <li>  Feature Packs mit Funktionen von allgemeinem Interesse und GA Feature Packs werden mit dem nächsten Service Pack zusammengeführt  </li> </ul> |
| Benennung  | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Lieferumfang  | <ul> <li> Neue Funktionen </li> <li> Verbesserungen </li> <li> Fehlerkorrekturen (inkrementelle Produktaktualisierungen) </li> </ul> |
| Dokumentation | Die Dokumentation ist auf adobe.com verfügbar. |
| Veröffentlichungsintervall  | Abhängig vom Produktbereich |
| Verfügbarkeit und Installation  | <ul> <li>Wird über Service Packs bereitgestellt </li> <li> Verfügbar über Softwareverteilung. Kunden akzeptieren die Geschäftsbedingungen für [!DNL Adobe's] über die Softwareverteilung. </li> </ul> |
| Teststufe  | Die Pakete mit den allgemeinen Verfügbarkeitsfunktionen werden validiert. |

* 1: OAK-Korrekturen werden nicht als einzelne Hotfixes bereitgestellt. Sie sind jedoch im Lieferumfang des nachfolgenden Cumulative Oak Hot Fix enthalten. Bei Bedarf kann ein Diagnose-Build zusätzlich zum aktuellen COFP bereitgestellt werden. Eine Vorbedingung hierfür ist, dass der Kunde das aktuelle COFP ausgeführt hat. Diagnose-Builds bieten nur die Qualitätssicherungsstufe eines Hotfixes. Sie bieten nicht dieselbe Qualitätssicherungsstufe wie ein Cumulative Fix Pack, ein Service Pack oder eine Produktversion. Die endgültige Fehlerbehebung wird mit der nächsten GFP geliefert.
