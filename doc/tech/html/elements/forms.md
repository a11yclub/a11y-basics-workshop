## Formulare

* `<label>`s verwenden! (gilt für alle interaktiven Element, außer `<button>`, deren Inhalt als Label fungieren)
* Progressive Enhancement
	* Solide HTML-Lösung als Basis
	* Optische Aufwertung per CSS (z.B. `<input type="radio">` verbergen und stattdessen `<label>`s zeigen und stylen)
	* Funktionale Aufwertung per JavaScript, z.B. dynamisches Laden per XHR
	* Weitere Ergänzung durch WAI-ARIA
		* [Live Regions](http://w3c.github.io/aria/practices/aria-practices.html#LiveRegions): Werden von Screenreadern verlesen, sobald sich ihr Inhalt ändert

			```html
			<div aria-live="assertive" role="alert">Daten werden geladen ...</div>
			```