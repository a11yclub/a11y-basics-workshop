## Bilder

* Bilder (und andere Elemente) sollten stets über Textalternativen verfügen; Mögliche Quellen:
    * `alt`-, `title`-, `placeholder`-Attribute
    * ARIA-Attribute (`aria-label`, `aria-describedby`)
    * Generated Content (CSS-Pseudoelemente)
* Bilder müssen stets ein `alt`-Attribut haben
* das `alt`-Attribut sollte eine sinnvolle Beschreibung enthalten oder leer sein (siehe [WAI `alt` decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/))
    * Präzise und gleichwertige Beschreibung des Inhalts und der Funktion des Bildes
    * Kurz und bündig; meist sind wenige Worte ausreichend, manchmal ein kurzer Satz
    * Nicht redundant und deckungssgleich mit dem Kontext um das Bild herum
    * Vermeidung von Platzhaltern wie "Foto von ..." oder "Bild mit ..."; den Nutzern ist bereits klar, dass es sich um ein Bild handelt
* ein leeres `alt`-Attribut teilt Screenreadern mit, dass es sich um ein rein dekoratives Bild handelt, das nicht signifikant zur Aussage beiträgt
* Konzept des **zugänglichen Namens** („Accessible Name“): Logik zur Ermittlung für alle Elemente zur Weitergabe an assistive Technologie

**Links**

* [WebAIM: Alternative Text](https://webaim.org/techniques/alttext/)
* [What is an accessible name?](https://developer.paciellogroup.com/blog/2017/04/what-is-an-accessible-name/) (Léonie Watson)
* [Accessible Name and Description Computation 1.1](https://www.w3.org/TR/accname-1.1/)
* [How the W3C Text Alternative Computation Works - Level Access](https://www.levelaccess.com/how-the-w3c-text-alternative-computation-works/)
