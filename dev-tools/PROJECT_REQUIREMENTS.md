# 📋 PROJECT REQUIREMENTS

<!-- KAT · DEV TOOLS | Vorlagen-Release: v1.0.0 | 2026-11-03 -->

> Was muss KATUARY erfüllen – und was wurde tatsächlich überprüft?
> Anforderungen, Implementierung und Review bleiben getrennt.

---

## 🎯 PURPOSE

KATUARY wird eine private, gemütliche und modular erweiterbare Desktop-Anwendung für macOS.

Langfristig soll die Anwendung als persönliche Organisations- und Kommandozentrale dienen und bestehende Werkzeuge sowie ausgewählte Inhalte von `katcoded.de` verwalten können.

Diese Datei dokumentiert zunächst die Anforderungen an das **technische Grundgerüst und die erste Benutzeroberfläche**.

Der endgültige MVP-Umfang ist noch offen. Weitere Anforderungen werden bei der gemeinsamen Entwicklungsplanung ergänzt.

Die Tabelle unterscheidet zwischen implementierten und tatsächlich überprüften Funktionen.

---

## 📌 REQUIREMENTS

### Technisches Grundgerüst

| ID    | Requirement                                                                                               | Implementation | Review       |
| ----- | --------------------------------------------------------------------------------------------------------- | -------------- | ------------ |
| FR001 | KATUARY lässt sich unter macOS als eigenständiges Desktop-Fenster starten.                                | Done           | Passed       |
| FR002 | Die Benutzeroberfläche verwendet React und TypeScript innerhalb der Tauri-Anwendung.                      | Done           | Not Reviewed |
| FR003 | Das vorhandene KATCODED-Designsystem CUTE_COZY wird für die KATUARY-Oberfläche eingebunden und verwendet. | Open           | Not Reviewed |

### Hauptfenster & Navigation

| ID    | Requirement                                                                                              | Implementation | Review       |
| ----- | -------------------------------------------------------------------------------------------------------- | -------------- | ------------ |
| FR004 | KATUARY besitzt ein Hauptfenster mit Header, schmaler linker Sidebar und einem zentralen Arbeitsbereich. | Open           | Not Reviewed |
| FR005 | Die Sidebar lässt sich ein- und ausklappen.                                                              | Open           | Not Reviewed |
| FR006 | Über die Sidebar können die vorgesehenen Workspace-Bereiche aufgerufen werden.                           | Open           | Not Reviewed |

### Dashboard

| ID    | Requirement                                                                       | Implementation | Review       |
| ----- | --------------------------------------------------------------------------------- | -------------- | ------------ |
| FR007 | KATUARY besitzt eine persönliche Dashboard-Startseite.                            | Open           | Not Reviewed |
| FR008 | Das Dashboard kann verschiedene Informationen in eigenständigen Widgets anzeigen. | Open           | Not Reviewed |

### Bestätigtes späteres UI-Ziel

Die folgenden Anforderungen gehören zur bestätigten Designrichtung. Ihre Zuordnung zu einer konkreten Version ist noch offen.

| ID    | Requirement                                                                                           | Implementation | Review       |
| ----- | ----------------------------------------------------------------------------------------------------- | -------------- | ------------ |
| FR009 | Das Dashboard besitzt einen Bearbeitungsmodus, in dem Widgets hinzugefügt und entfernt werden können. | Open           | Not Reviewed |
| FR010 | Widgets können im Bearbeitungsmodus per Drag-and-drop verschoben werden.                              | Open           | Not Reviewed |
| FR011 | Widgets können im Bearbeitungsmodus vergrößert und verkleinert werden.                                | Open           | Not Reviewed |

---

## 🔎 REVIEW NOTES

### FR001 · Desktop-Start

- **Geprüft:** 09.11.2026
- **Prüfart:** Manueller Start über `npm run tauri dev`.
- **Ergebnis:** Die Tauri-Anwendung startete erfolgreich und zeigte das React-Standardfenster als eigenständige macOS-Anwendung.
- **Nachweis:** Screenshot des geöffneten KATUARY-Fensters.
- **Grenze:** Noch kein produktiver Release-Build geprüft.

Für FR002 ist das generierte Projektgrundgerüst vorhanden. Eine gesonderte Code- oder Buildprüfung wurde hier nicht dokumentiert.

Für die übrigen Anforderungen liegen noch keine abgeschlossenen Reviews vor.

---

## 🧭 KAT-REGELN FÜR REQUIREMENTS

- **Implementation ≠ Review.** Fertig programmiert ist nicht automatisch erfolgreich geprüft.
- **Nur belegte Ergebnisse eintragen.** Keine bestandenen Tests oder Reviews behaupten, die nicht durchgeführt wurden.
- **Requirements originalgetreu halten.** Die Datei beschreibt _was_, nicht die ausführliche Schrittfolge zur Umsetzung.
- **Keine doppelte Projektpflege.** Entwicklungsschritte gehören in `PROJECT_BUILD_GUIDE.md`; der aktuelle Wiedereinstiegsstand in `PROJECT_STATE.md`.
- **Kompakt bleiben.** Akzeptanzkriterien, Testdetails oder weitere Abschnitte nur ergänzen, wenn das Projekt sie wirklich braucht.
- **Keine zusätzlichen Agentenregeln.** Zuständigkeiten und Schreibrechte regelt `AGENTS.md`.

---

> 👻 Part of **KAT · DEV TOOLS** · katcoded.de
>
> See `DEV_TOOLS_README.md` for information about this toolkit.
