# Relevante Komponenten

* [→ Technik](tech.md) (HTML, CSS, JavaScript, WAI-ARIA)
* [→ Inhalte](content.md) (Texte, Bilder, Video / Audio)
* [→ Verfahren](patterns.md) (Patterns)

# Progressive Enhancement

* „Start small, grow big“
* Orientierung am schwächsten Glied (= leistungsärmster Client,
  schlechteste Bedingungen, etc.)
* Zurüsten von Leistungsmerkmalen, wenn sie zur Verfügung stehen
* HTML als solide, „unverwüstliche“ Grundlage
* CSS als fehlertolerante „Schmuckschicht“
* JavaScript als interaktive Aufwertung, nicht als
  Voraussetzung

**Links**

* https://de.wikipedia.org/wiki/Progressive_Verbesserung
* http://alistapart.com/article/understandingprogressiveenhancement
  (Aaaron Gustafson)
* https://adactio.com/journal/7706 (Jeremy Keith)

# Accessibility Tree

* kein spezifizierter Standard
* Parallelstruktur zum DOM Tree, die sich aus UI-Objekten des Clients und aus DOM-Objekten ableitet
* für jedes DOM-Element, das assistiven Technologien gegenüber exponiert werden soll, existiert ein „Accessible Object“ im Accessibility Tree
* direkte Schnittstelle zum Betriebssystem
* aus Web-Perspektive: Beeinflussung des Accessibility Tree ausschließlich passiv über das DOM (durch HTML, ARIA und JavaScript), jedoch keine direkte Schnittstelle
* Darstellung im Chrome: [chrome://accessibility](chrome://accessibility)

**Links**

* https://www.paciellogroup.com/blog/2015/01/the-browser-accessibility-tree/
* http://whatsock.com/training/
* http://www.barrierefreies-webdesign.de/knowhow/msaa/tools.html
* https://egghead.io/lessons/html-5-what-is-the-accessibility-tree