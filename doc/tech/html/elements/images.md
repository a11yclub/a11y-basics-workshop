## Bilder

* Bilder müssen stets über ein `alt`-Attribut verfügen
* das `alt`-Attribut sollte eine sinnvolle Beschreibung enthalten oder leer sein (siehe [WAI `alt` decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/))
* ein leeres `alt`-Attribut teilt Screenreadern mit, dass es sich um ein rein dekoratives Bild handelt, das nicht signifikant zur Aussage beiträgt
* Bilder sollten so gut wie möglich komprimiert werden (verlustbehaftet oder verlustfrei)
* „Lazy Loading“: Laden eines Bildes, sobald es den Viewport erreicht
* `<picture>`-Element mit mehreren Varianten für unterschiedliche Viewports (TODO: Codebeispiel)

**Beispiel**

```html
<picture>
    <source media="(min-width: 800px;)" srcset="/pfad/zum/bild_gross.jpg">
    <img src="/pfad/zum/bild_klein.jpg" alt="Sinnvolle Beschreibung zum Bild">
</picture>
```

**Links**

* [WAI `alt` decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/)
* [ImageOptim für Mac OS](https://imageoptim.com)