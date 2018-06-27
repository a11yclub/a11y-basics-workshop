# Inhalt

* Verknüpfungen („Links“) referenzieren andere / ferne Ressourcen; die grundlegende Erwartungshaltung ist also, dass Links „irgendwohin führen“
* eindeutiger, beschreibender Link-Inhalt, so dass er auch ohne Kontext bedeutungsvoll ist (Link-Listen zur Navigation per Screenreader)
* ggf. visuell unsichtbare Ergänzung, um den Kontext herzustellen

```html
<a href="...">Jetzt <span class="visually-hidden">Modisches T-Shirt</span> kaufen</a>
```

* positiver SEO-Effekt, wenn der Link-Inhalt dem `<title>` der verlinkten Seite entspricht (hohe Relevanz)
* gern praktiziert, aber **Anti-Pattern**: Links ohne sinnvollen Inhalt

```html
Ich mache <a href="...">viele</a> <a href="...">tolle</a> <a href="...">Sachen</a>!
```

# Gestaltung

* Inline-Links sollten sich in ihrer Gestaltung deutlich vom umgebenden Text abheben
    * unterschiedliche Stile im Normal- und Hover-Zustand
    * nicht nur rein farbliche Unterscheidung (Farbfehlsichtigkeit)
    * keine Simulation eines `<buttons>`
* sinnvolle gestalterische Differenzierung, z.B. Link ↔ Aktion ↔ Button
* auch sinnvoll: Einheitliche Ästhetik für alle interaktiven Elemente (z.B. Blau als gelernte Konvention für Interaktion)

# Typ

Seit HTML5 sind Block-Level-Links legitim (per CSS umzusetzen)

**Vorteile**

* Vergrößern die klickbare Fläche
* können komplexe Strukturen & Inhalte einschließen

**Nachteile**

* verhindern untergeordnete Links
* wird nicht als Link wahrgenommen, bis damit interagiert wird (Hover, Klick / Tap, Tastaturfokus)
* mögliche Störungen
    * Screenreader: innenliegende Überschriften können nicht ohne Weiteres fokusiert werden
    * Screenreader: Fokussieren liest den kompletten Inhalt vor
    * Touchscreens: Versehentliches Aktivieren des Links beim Scrollen