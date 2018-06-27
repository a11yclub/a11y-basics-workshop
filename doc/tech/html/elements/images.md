## Bilder

* Bilder müssen stets über ein `alt`-Attribut verfügen
* das `alt`-Attribut sollte eine sinnvolle Beschreibung enthalten oder leer sein (siehe [WAI `alt` decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/))
* ein leeres `alt`-Attribut teilt Screenreadern mit, dass es sich um ein rein dekoratives Bild handelt, das nicht signifikant zur Aussage beiträgt
* Bilder sollten so gut wie möglich komprimiert werden (verlustbehaftet oder verlustfrei)
* „Lazy Loading“: Laden eines Bildes, sobald es den Viewport erreicht
* `<picture>`-Element mit mehreren Varianten für unterschiedliche Viewports

**Beispiele**

`<picture>` für verschiedene Viewportgrößen (`media`-Attribut):

```html
<picture>
    <source srcset="/pfad/zum/bild_gross.jpg" media="(min-width: 800px)">
    <img src="/pfad/zum/bild_klein.jpg" alt="Sinnvolle Beschreibung zum Bild">
</picture>
```

`<picture>` für verschiedene Auflösungen (`srcset`-Attribut):

```html
<picture>
    <source srcset="bild.jpg 1x, bild-2x.jpg 2x, bild-3x.jpg 3x">
    <img src="bild.jpg" alt="Sinnvolle Beschreibung zum Bild">
</picture>
```

`<picture>` für verschiedene Bildformate (`type`-Attribut):

```html
<picture>
    <source srcset="/pfad/zum/bild.svg" type="image/svg+xml"">
    <img src="/pfad/zum/bild.jpg" alt="Sinnvolle Beschreibung zum Bild">
</picture>
```

*Ein Beispiel mit `sizes`-Attribut wird aus Vereinfachungsgründen hier nicht wiedergegeben.*

**Links**

* [WAI `alt` decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/)
* [ImageOptim](https://imageoptim.com) für Mac OS
* [TinyPNG](https://tinypng.com/) zur Optimierung von PNG-Grafiken
* [SVGOMG](https://jakearchibald.github.io/svgomg/) zur Optimierung von SVG-Grafiken
