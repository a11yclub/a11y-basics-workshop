# Allgemein

* `<fieldset>` nur einsetzen, wo sinnvoll
    * `<fieldset>` ohne `<legend>` ergibt keinen sinn
    * `<legend>` wird **vor jedem Formularfeld** als Präfix verlesen
    * nur bei mehr als einem Formularfeld
* `<label>` verwenden (bei allen Elementen außer `<button>`)

# Progressive Enhancement
* solide HTML-Lösung als Basis
* optische Aufwertung per CSS
    * z.B. `<input type="radio">` verbergen, stattdessen `<label>`s zeigen und stylen
* Funktionale Aufwertung per JavaScript, z.B. dynamisches Laden per AJAX
* Weitere Ergänzung durch WAI-ARIA
    * [Live Regions](http://w3c.github.io/aria/practices/aria-practices.html#LiveRegions): Werden von Screenreadern verlesen, sobald sich der Inhalt ändert
        * Z.B. während und bei Abschluss von AJAX-Ladevorgängen oder zur Formularvalidierung

```html
<div aria-live="assertive" role="alert">Daten werden geladen ...</div>
```