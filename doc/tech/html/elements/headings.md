# Allgemein

* Überschriften prägen in Kombination mit [Abschnitten](sections.md) maßgeblich die Struktur eines Dokuments
* werden zur Erstellung eines „Inhaltsverzeichnisses“ (_Outline_) verwendet („Document Outlining Algorithm“, der die Struktur aus den Abschnitten ableitet, ist nirgends implementiert)
* sollten selbsterklärend sein und sich nicht auf den Kontext stützen (Screenreader bieten eine Überschriftenliste zur Navigation an, die ohne Kontext auskommen muss)
* Lackmustest: CSS abschalten und prüfen, ob das Dokument noch sinnvoll lesbar ist und funktioniert

# `<h1>`

* repräsentiert den Titel / das Thema des gesamten Dokuments, daher sind mehrere `<h1>` nicht sinnvoll (wenn auch nicht verboten)
* Shortcut in vielen Screenreadern (`1` in JAWS / NVDA)

# `<h2>` - `<h6>`

* wichtig, dass kein Level ausgelassen wird (ansonsten keine Strukturelle Integrität)

**Links**

* [HeadingsMap Chrome Plugin](https://chrome.google.com/webstore/detail/headingsmap/flbjommegcjonpdmenkdiocclhjacmbi)
* [HeadingsMap Firefox Add-On](https://addons.mozilla.org/de/firefox/addon/headingsmap/)