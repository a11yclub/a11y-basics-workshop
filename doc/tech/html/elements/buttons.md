# Allgemein

* Buttons sind in erster Linie Formularelemente(!)
* sind als Auslöser außerhalb von Formularen wo immer möglich zu vermeiden (z.B. Off-Canvas-Menü)

# Gestaltung

* sollten wie übliche Buttons aussehen (UX-Problematik)
* ideal: Einheitliche Ästhetik für alle interaktiven Elemente
    * z.B. Blau als gelernte Konvention für Interaktion
    * mögliche gestalterische Differenzierung
    	* Link (unterstrichen)
    	* Aktion (Ghost Button)
    	* Button (Formular)
* nicht zu klein, damit auf Touchscreen-Geräten nutzbar
    * insbesondere bei dicht aneinander liegenden _Touch Targets_
    * Apple empfiehlt 44 x 44 Pixel, Google 48 x 48 Pixel Mindestgröße
* idesl: Abstand zwischen allen _Touch Targets_
* [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights) moniert zu kleine und zu dicht liegende Links

# Icon-Buttons

* als Hintergrundbild: wird im „High Contrast Mode“ ausgeblendet → ohne Beschriftung wertlos
* als Vordergrundbilder: können im „High Contrast Mode“ eine andere Bedeutung erhalten (z.B. Invertierung der Hintergrundfarbe)
* Icon-Font
	* benutzerdefinierte Icon-Fonts können nicht getauscht werden, ohne dass potenziell Glyphen fehlen
	* Icon-Fonts können blockiert werden (z.B. Opera Mini)
* Unicode-Symbole: werden möglicherweise von Screenreadern interpretiert und namentlich verlesen
* ideal: [Scalable Vector Graphics](https://de.wikipedia.org/wiki/Scalable_Vector_Graphics) (SVG)
    * optimale Darstellung, da Vektorformat (verlustfreie Skalierung, Retina-Displays)
    * geringe Dateigröße / gute Kompression
    * unterstützt eingebetteten `<title>` als Beschriftung
    * als externe Resource und „inline“ ins HTML-Dokument eingebettet
	* Inline-SVG: Screenreader können `<text>` lesen (z.B. visuell versteck)
	* SVG-Sprites: „Inline embedding“ + `<use>` + `currentColor` zum Umfärben

# Beschriftung

* sollten stets einen Beschriftung haben (auch Hamburger-Menü)
* ergänzende Beschriftung, wenn der Button-Inhalt nicht direkt lesbar ist, z.B. bei Icon-Button
    * per `visually-hidden`-Text, z.B. in einem `<span>`
    * per `aria-label` (wie `alt`-Attribut, aber für alle Elemente)

# Status

* `aria-pressed`, um Status an den Accessibility Tree zu melden
* `aria-expanded` bei kollabierbaren Strukturen (lässt den Screenreader ausdrücklich `"expanded"` oder `"collapsed"` vorlesen)