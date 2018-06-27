# Allgemein

* Überschriften prägen in Kombination mit [Abschnitten](sections.md) maßgeblich die Struktur eines Dokuments
* werden zur Erstellung eines „Inhaltsverzeichnisses“ (_Outline_) verwendet („Document Outlining Algorithm“, der die Struktur aus den Abschnitten ableitet, ist nirgends implementiert) → wäre insbesondere bei komponentengetriebenen Entwurfs- und Entwicklungsansätzen sehr nützlich
* sollten selbsterklärend sein und sich nicht auf den Kontext stützen (Screenreader bieten eine Überschriftenliste zur Navigation an, die ohne Kontext auskommen muss)
* Lackmustest: CSS abschalten und prüfen, ob das Dokument noch sinnvoll lesbar ist und funktioniert

# `<h1>`

* repräsentiert den Titel / das Thema des gesamten Dokuments, daher sind mehrere `<h1>` nicht sinnvoll (wenn auch nicht verboten)
* Shortcut in vielen Screenreadern (`1` in JAWS / NVDA)

# `<h2>` - `<h6>`

* wichtig, dass kein Level ausgelassen wird (ansonsten keine Strukturelle Integrität)

**Links**

* [There Is No Document Outline Algorithm](http://adrianroselli.com/2016/08/there-is-no-document-outline-algorithm.html) (Adrian Roselli)
* [The Document Outline Dilemma](https://css-tricks.com/document-outline-dilemma) (Amelia Bellamy-Royds)
* [Managing Heading Levels In Design Systems](https://css-tricks.com/managing-heading-levels-in-design-systems/) (Heydon Pickering)
* [HeadingsMap Chrome Plugin](https://chrome.google.com/webstore/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi)
* [HeadingsMap Firefox Add-On](https://addons.mozilla.org/de/firefox/addon/headingsmap/)