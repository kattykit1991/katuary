# 🗺️ PROJECT BUILD GUIDE

<!-- KAT · DEV TOOLS | Vorlagen-Release: v1.0.0 | 2026-11-03 -->

> Meine Bauanleitung vom aktuellen Ziel zum funktionierenden DING™.
> Nicht in Stein gemeißelt: Wenn sich beim Bauen ein besserer Weg zeigt, darf der Bauplan mitwachsen.

**Projekt:** KATUARY — Your Cozy Personal Workspace 👻💜

**Aktueller Fokus:** Das erste eigene Hauptfenster mit CUTE_COZY, Sidebar und Dashboard entwickeln.

**Ausgangspunkt:** Das Tauri-2-Projekt mit React, TypeScript und Vite wurde erstellt und das Standard-Desktop-Fenster erfolgreich gestartet. Der CUTE_COZY-Ordner liegt bereits unter `public/styles/CUTE_COZY/`.

---

## 🧭 BUILD ROUTE

- [STAGE 01 · CUTE_COZY integrieren](#stage-01--cute_cozy-integrieren)
- [STAGE 02 · Hauptfenster und Sidebar](#stage-02--hauptfenster-und-sidebar)
- [STAGE 03 · Dashboard-Grundstruktur](#stage-03--dashboard-grundstruktur)

---

# STAGE 01 · CUTE_COZY integrieren

## 🎯 ZIEL

Das bestehende CUTE_COZY Style System in die React-Anwendung einbinden und seine grundlegenden Gestaltungsmöglichkeiten ausprobieren.

Am Ende zeigt KATUARY eigene, mit CUTE_COZY gestaltete Elemente statt ausschließlich das Tauri-Standarddesign.

## 🔨 BAUEN

### 1 · Style System anbinden

- [x] Vollständigen `CUTE_COZY`-Ordner nach `public/styles/CUTE_COZY/` kopieren.
- [ ] In `index.html` das Stylesheet nach den Anweisungen der CUTE_COZY-README einbinden.
- [ ] Prüfen, welche vorhandenen Styles aus dem Tauri-Startertemplate mit CUTE_COZY kollidieren könnten.
- [ ] Die benötigte CUTE_COZY-Grundstruktur in der React-Oberfläche verwenden.

#### 🧱 DAFÜR BRAUCHST DU

**CSS-Dateien in HTML einbinden**

```html
<link rel="stylesheet" href="pfad/zur/datei.css" />
```

Der Browser lädt dadurch das angegebene Stylesheet. Für Vite-Projekte kann bei Dateien im `public/`-Ordner die konfigurierte Basis-URL relevant sein.

**CSS-Klassen in React**

```tsx
<div className="beispiel-klasse">Beispielinhalt</div>
```

In React wird `className` statt des HTML-Attributs `class` verwendet.

### 2 · Erste eigene Oberfläche ausprobieren

- [ ] Den Aufbau der vorhandenen `App.tsx` verstehen.
- [ ] Nicht mehr benötigte Demo-Inhalte schrittweise ersetzen.
- [ ] Eine einfache KATUARY-Begrüßung anzeigen.
- [ ] Eine vorhandene CUTE_COZY-Komponentenklasse ausprobieren.
- [ ] Prüfen, ob Styles und Schriftarten korrekt dargestellt werden.

#### 🧱 DAFÜR BRAUCHST DU

**Eine einfache React-Komponente**

```tsx
function Example() {
  return <h1>Hallo!</h1>;
}

export default Example;
```

Eine React-Komponente ist eine Funktion, die JSX zurückgibt. Damit können wir unsere Oberfläche in kleinere, verständliche Bestandteile aufteilen.

## ✅ FERTIG, WENN

- [ ] KATUARY startet weiterhin erfolgreich als Desktop-App.
- [ ] Die eigene Begrüßung wird angezeigt.
- [ ] CUTE_COZY-Styling ist sichtbar.
- [ ] Keine erkennbaren Stylingkonflikte verhindern die Nutzung.

---

# STAGE 02 · Hauptfenster und Sidebar

## 🎯 ZIEL

Das erste richtige KATUARY-Hauptfenster entwickeln.

Es besteht aus einem Header, einer schmalen ein- und ausklappbaren Sidebar sowie einem zentralen Arbeitsbereich.

## 🔨 BAUEN

### 1 · Grundlayout erstellen

- [ ] Eine verständliche Komponentenstruktur für das Hauptfenster überlegen.
- [ ] Header mit KATUARY-Identität erstellen.
- [ ] Schmale linke Sidebar gestalten.
- [ ] Zentralen Arbeitsbereich einrichten.
- [ ] Das Layout mit vorhandenen CUTE_COZY-Styles gestalten.

#### 🧱 DAFÜR BRAUCHST DU

**Komponenten zusammensetzen**

```tsx
function Container() {
  return (
    <div>
      <Header />
      <Content />
    </div>
  );
}
```

Komponenten können andere Komponenten enthalten. Dadurch müssen Header, Navigation und Arbeitsbereich nicht in einer einzigen riesigen Datei stehen.

### 2 · Sidebar einklappbar machen

- [ ] Einen React-State für den Sidebar-Zustand erstellen.
- [ ] Einen Button zum Ein- und Ausklappen ergänzen.
- [ ] Im eingeklappten Zustand eine schmale Icon-Navigation anzeigen.
- [ ] Prüfen, ob der Arbeitsbereich die verfügbare Breite sinnvoll nutzt.

#### 🧱 DAFÜR BRAUCHST DU

**React-State mit einem Boolean**

```tsx
const [isOpen, setIsOpen] = useState(true);

function toggle() {
  setIsOpen((previous) => !previous);
}
```

`useState` speichert einen veränderlichen Zustand innerhalb einer React-Komponente.

Mit der Setter-Funktion können wir den Zustand ändern. React rendert danach die betroffenen Elemente neu.

### 3 · Erste Navigation vorbereiten

- [ ] Dashboard als Startansicht festlegen.
- [ ] Erste Navigationspunkte als UI-Elemente erstellen.
- [ ] Eine einfache Navigation zwischen Beispielansichten ermöglichen.
- [ ] Aktuell ausgewählten Bereich sichtbar hervorheben.

Die endgültige Navigation und sämtliche späteren Workspace-Bereiche müssen dafür noch nicht feststehen.

## ✅ FERTIG, WENN

- [ ] Header, Sidebar und Arbeitsbereich sichtbar sind.
- [ ] Die Sidebar ein- und ausgeklappt werden kann.
- [ ] Die Hauptansicht über die Navigation gewechselt werden kann.
- [ ] Das Layout bei unterschiedlichen Fenstergrößen benutzbar bleibt.

---

# STAGE 03 · Dashboard-Grundstruktur

## 🎯 ZIEL

Eine erste gemütliche Dashboard-Startseite mit eigenständigen Widget-Bereichen entwickeln.

Das Dashboard soll bereits wie KATUARY aussehen, auch wenn die Widgets zunächst nur Beispieldaten anzeigen.

## 🔨 BAUEN

### 1 · Dashboard-Layout

- [ ] Begrüßungsbereich erstellen.
- [ ] Ein responsives Raster für Widgets aufbauen.
- [ ] Eine erste Widget-Komponente entwickeln.
- [ ] Wiederverwendbare Widget-Eigenschaften überlegen.
- [ ] Beispielwidgets für Schnellzugriff, aktuellen Fokus und Dingsies anzeigen.

#### 🧱 DAFÜR BRAUCHST DU

**Komponenten mit Props**

```tsx
type CardProps = {
  title: string;
};

function Card({ title }: CardProps) {
  return <section>{title}</section>;
}
```

Props ermöglichen es, Informationen an Komponenten zu übergeben.

So kann eine gemeinsame Komponente später unterschiedliche Widget-Inhalte darstellen.

### 2 · Dashboard vorbereiten

- [ ] Widget-Inhalte zunächst mit lokalen Beispieldaten darstellen.
- [ ] Den Aufbau so gestalten, dass spätere Erweiterungen möglich bleiben.
- [ ] Dashboard bei verschiedenen Fenstergrößen testen.

Der geplante Widget-Bearbeitungsmodus mit Drag-and-drop, Größenänderungen, Hinzufügen und Entfernen bleibt ein bestätigtes Entwicklungsziel, wird aber erst in einer späteren Stage konkret ausgearbeitet.

## ✅ FERTIG, WENN

- [ ] Das Dashboard als Startseite geöffnet werden kann.
- [ ] Mehrere Widgets sichtbar sind.
- [ ] Widgets auf einer wiederverwendbaren Komponentenstruktur aufbauen.
- [ ] Das Raster bei verschiedenen Fenstergrößen sinnvoll reagiert.

---

> 👻 Part of **KAT · DEV TOOLS** · katcoded.de
>
> See `DEV_TOOLS_README.md` for information about this toolkit.
