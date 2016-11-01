## Buttons (als Auslöser für ein funktionales Element, z.B. ein Off-Canvas-Menü)

* sind zu vermeiden, wenn sie zu vermeiden sind (abgesehen von Formularen)
	* Möglichst keine erweiterte Funktionalität hinter Buttons verbergen
* sollten auch wie Buttons aussehen (Rahmen)
* dies betrifft auch den Hamburger-Menü-Button (am besten eingerahmt mit Beschriftung "Menü")
* Mögliche Differenzierung (bei gleicher Farbgebung, z.B. "blau" für "Interaktives Element")
	* Link (unterstrichen)
	* Aktion (Ghost Button)
	* Button (Formular)

### Icons

#### Methoden

* als Hintergrundbild: wird im "High Contrast Mode" ausgeblendet → ohne Beschriftung wertlos
* als Vordergrundbilder: können im "High Contrast Mode" eine andere Bedeutung erhalten (durch Invertierung des Hintergrunds)
* Icon-Font
	* Benutzerdefinierte Icon-Fonts können nicht getauscht werden, ohne dass potenziell Glyphen fehlen
	* Icon-Fonts können blockiert werden (z.B. Opera Mini)
* Unicode-Symbole: werden möglicherweise von Screenreadern interpretiert und namentlich verlesen
* SVG-Sprites: Inline embedding + `<use>` + `currentColor` zum Umfärben
	* Inline-SVG: Screenreader können `<text>` lesen (kann verwendet werden, um visuell versteckte Texte zu ergänzen)

#### Label (wenn der Inhalt nicht per se lesbar ist, z.B. Icon)

* per `visually-hidden` Text, z.B. in einem `<span>`
* per `aria-label` (wie `alt`-Attribut, aber für alle Elemente)

### Status

* WAI-ARIA, um Status an den Accessibility Tree zu melden
* `aria-expanded` lässt den Screenreader ausdrücklich `"expanded"` oder `"collapsed"` vorlesen

### Größe

* Nicht zu klein, denn sonst ist der Button auf Touchscreen-Geräten nicht nutzbar, insbesondere wenn es zu dicht an anderen Touch Targets liegt (Apple empfiehlt 44 x 44 Pixel, Google 48 x 48 Pixel)
* Im Bestfall Abstand zwischen allen Touch Targets
* Google PageSpeed Insights moniert zu kleine und zu dicht liegende Links