# Listen

* `<ol>`, `<ul>` und `<dl>` drücken eine hierarchische Struktur aus
    * `<ol>`, wenn die Reihenfolge signifikant ist (z.B. in einer Navigation)
    * `<ul>`, wenn die Reihenfolge theoretisch keine Rolle spielt
    * `<dl>`, wenn es Paare aus Bezeichnern und Wert gibt (und eine `<table>` semantisch falsch wäre)
* Listenpunkte dürfen durchaus komplexe Strukturen enthalten (z.B. Produktliste)
* Vorteil für Screenreader: Anzahl der Listenpunkte wird vorab angesagt (sehr hilfreich z.B. auch in Menüs)

```html
<li>
    <a href="/product/t-shirt">
        <h3>Modisches T-Shirt</h3>
        <img src="/pfad/zum/bild.jpg" alt="Bequemes T-Shirt aus pflegeleichter Baumwolle" />
        <dl>
            <dt>Größe:</dt>
            <dd>M</dd>
            <dt>Preis:</dt>
            <dd>€ 35.95</dd>
            <dt>Bewertung:</dt>
            <dd><img src="/images/rating_4_5.svg" alt="">4 von 5 Sternen</dd>
        </dl>
    </a>
</li>
```