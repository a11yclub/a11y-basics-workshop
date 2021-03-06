# Allgemein

* CSS als „visuelles Enhancement“ der HTML-Basis begreifen
* visuelle Gestaltung darf keine Grundvoraussetzung für die Benutzbarkeit sein
* Lackmustest: CSS deaktivieren und prüfen, ob die Website noch benutzbar ist

# Responsive Design

* Layout sollte möglichst viele Ausgabeplattformen untertützen
* Content Breakpoints („Tweakpoints“)
* Breakpoints In relativen Maßeinheiten (`em`) definieren, damit sie sich an Schriftgrößen orientieren

# Verbergen von Inhalten

* `display="none"` und `visibility="hidden"` verbergen Inhalte visuell und auch vor Screenreadern
* `hidden`-Attribut (HTML5)
    * verbirgt untergeordnete Inhalte visuell und auch vor Screenreadern
    * macht alle untergeordneten Element „unfocusable“, sie sind also auch per Keyboard nicht mehr anzuspringen
    * lange nicht konsistent implementiert (immer noch problematisch?)
* `aria-hidden="true"` verbirgt Inhalte nur vor Screenreadern

**Beispiel 1: Visuelles Verbergen eines Elements** (aber sichtbar für Screenreader)

```css
.visually-hidden {
	position: absolute;
	width: 1px;
	height: 1px;
	overflow: hidden;
	clip: rect(1px, 1px, 1px, 1px);
}
```

**Beispiel 2: Visuelles Verbergen von Textinhalten bei sichtbarem Element** (z.B. Ersatz durch Hintergrundbild)

```css
.visually-hidden-content {
    text-indent: 100%;
    overflow: hidden;
    white-space: nowrap;
}
```