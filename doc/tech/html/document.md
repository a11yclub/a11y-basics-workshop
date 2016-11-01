## `<DOCTYPE>`-Deklaration

* Signalisiert den verwendeten Standard (HTML5)
* Verhindert den Quirks-Mode

## `lang`-Attribut

* Definiert die Sprache des Dokuments
* Nützlich für Übersetzungstools
* Entscheidet über das Sprachprofil von Screenreadern
* Definiert Wörterbücher / Rechtschreibregeln für Formularen
* Lässt den Browser die korrekten Schriftarten zur Darstellung der Texte wählen
* Auch inline nutzbar (z.B. für Fremdworte)

## Viewport

* Pinch-to-zoom zulassen! *TODO: Beispiel*

## `<title>`-Element

* Liefert den *accessible name* eines Dokuments (auch SVG)
* Wird vom Screenreader als erstes vorgelesen
* Best practice: Inhaltsbeschreibung + Autorenangabe (z.b. auch "Suche example.com: Ergebnisse für Suche nach xyz")

## `<main>`-Element

* Erlaubt die Markierung des zentralen Inhalts (websitespezifisch)
* Eindeutig je Dokument → kann von Screenreadern direkt angesprungen werden

[Grundsätzliche Dokumentstruktur](https://cdn.rawgit.com/a11yclub/a11y-basics-workshop/master/examples/document.html)
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>
    </head>

    <body>

        <!-- Hauptinhalt des Dokuments -->
        <main id="main" role="main">

        </main>
    </body>
</html>
```