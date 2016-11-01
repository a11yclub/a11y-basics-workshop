# `<main>`-Element

* Jedes HTML-Dokument sollte eines haben
* In Kombination mit einem Skip-Link: `id`-Attribut
* `role="main"`, wenn ältere Browser / Screenreader unterstützt werden sollen

```html
<main id="main" role="main">
	...
</main>
```

# "Sectioning elements"

http://blog.teamtreehouse.com/use-html5-sectioning-elements
https://www.w3.org/TR/html5/dom.html#sectioning-content-0
http://vanseodesign.com/web-design/html5-sectioning-elements/

* `<article>` entspricht `role="article"`
* `<section>` entspricht `role="region"`
* `<aside>` entspricht `role="complementary"`
* `<nav>` entspricht `role="navigation"`

Unklar, ob ebenfalls "sectioning"
* `<main>`
* `<footer>`
* `<header>`


* "Sectioning elements" haben streng genommen stets eine Überschrift
* Ist keine Überschrift explizit angegeben, werden sie intern als "unbenannt" betrachtet