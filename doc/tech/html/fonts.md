# Schriftarten

* so wenig wie möglich Schriftschnitte laden
* Fonts verkleinern: Subsetting
* **F**lash **O**f **U**nstyled **T**ext (_FOUT_) besser als **F**lash **O**f **I**nvisible **T**ext (_FOIT_)
* Vermeidung zusätzlicher Requests: Einbetten von Fonts ins CSS per [Data-URI](https://de.wikipedia.org/wiki/Data-URL)
* Vermeidung starker Irritationen: Wahl eine Ersatz-Systemfonts im Font-Stack, dessen Metriken dem endgültigen Font nahe kommen

**Beispiel**

```html
<!-- Nicht-blockierendes Laden von Schriftarten (im CSS als Data-URI) -->
<link rel="stylesheet" href="fonts.css" media="none" onload="if(media!='all')media='all'">
<noscript><link rel="stylesheet" href="fonts.css"></noscript>
```

**Links**

* [https://www.filamentgroup.com/lab/font-events.html](https://www.filamentgroup.com/lab/font-events.html) (Filament Group)
* [Umsetzung mit FontFaceObserver](https://github.com/filamentgroup/font-loading/blob/master/font-events.html) (Filament Group)

# Schriftgrößen

* Standardgröße 16px (= 100%)
* Schriftgrößen stets nur relativ angeben, da sonst die benutzerdefinierten Voreinstellungen ausgehebelt werden:

```css
html {
    font-size: 100%;
}
```

* Auch möglich: Angabe in Viewport-Einheiten `font-size: calc(1em + 1vw)`
* `margin` und `padding` von Texten sollten sich proportional zum Text verändern → Angabe in den schriftartbezogenen Maßeinheiten `em` und `rem`
* `line-height` sollte als Fließkommazahl angegeben werden und bezieht sich dann ebenfalls auf die aktuelle Schriftgröße