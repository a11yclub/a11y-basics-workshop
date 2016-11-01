## Fonts

* **F**lash **O**f **U**nstyled **T**ext (FOUT) besser als **F**lash **O**f **I**nvisible **T**ext (FOIT)
* So wenig wie möglich Schriftschnitte laden
* Fonts verkleinern: Subsetting
* Vermeidung zusätzlicher Requests: Einbetten von Fonts ins CSS per Data-URI
* Vermeidung starker Irritationen: Wahl eine Ersatz-Systemfonts im Font-Stack, dessen Metriken dem endgültigen Font nahe kommen
* Divere Lösungen *TODO: Beispiel*

**Links**

* [https://www.filamentgroup.com/lab/font-events.html](https://www.filamentgroup.com/lab/font-events.html) (Filament Group)

## Schriftgröße

* Standardgröße 16px (= 100%)
* Schriftgrößen stets nur relativ angeben, da sonst die benutzerdefinierten Voreinstellungen ausgehebelt werden:
  ```
	html {
		font-size: 100%;
	}
  ```
* Auch möglich: Angabe in Viewport-Einheiten `font-size: calc(1em + 1vw)`
* `margin` und `padding` von Texten sollten sich proportional zum Text verändern → Angabe in den schriftartbezogenen Maßeinheiten `em` und `rem`
* `line-height` sollte als Fließkommazahl angegeben werden und bezieht sich dann ebenfalls auf die aktuelle Schriftgröße