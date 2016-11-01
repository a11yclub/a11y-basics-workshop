Die Grundstruktur eines HTML-Dokuments sollte stets bestimmte Merkmale aufweisen.

# `<!DOCTYPE html>`-Deklaration

* signalisiert den verwendeten Standard (HTML5)
* verhindert den Quirks-Mode (möglicherweise Anzeigeprobleme)

# `lang`-Attribut

* definiert die Sprache des Dokuments (`<html lang="de">`)
* nützlich für Übersetzungstools (z.B. [Google Übersetzer](https://translate.google.de/))
* entscheidet über das Sprachprofil von Screenreadern
* definiert Wörterbücher / Rechtschreibregeln beim Schreiben im Dokument (in Formularen)
* lässt den Browser die korrekten Schriftarten zur Darstellung der Texte wählen
* auch inline nutzbar (z.B. für Fremdworte `<span lang="en">...</span>`)
    * Achtung: Häufiger Sprachwechsel kann für Screenreader-Nutzer anstrengend werden (wechselnde Sprachprofile)

# Viewport

* Pinch-to-zoom zulassen!

```html
<!-- NICHT VERWENDEN! --->
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no"/>
```

# `<title>`-Element

* liefert den *Accessible Name* eines Dokuments (auch SVG-Dokumente)
* wird vom Screenreader als erstes verlesen
* ideal: Inhaltsbeschreibung + Autorenangabe
    * z.b. auch „Suche auf test.de: Ergebnisse für Suche nach xyz“

# `<main>`-Element

* erlaubt die Markierung des zentralen Inhalts (websitespezifisch)
* ideal: Nach Kopfbereich und Navigation
* eindeutig je Dokument → kann von Screenreadern direkt angesprungen werden (JAWS: `Q`-Taste)

# Externe Resourcen

* CSS- und JavaScript-Resourcen sollten soweit möglich asynchron / nicht-blockierend geladen werden, um die sichtbaren Inhalte so schnell wie möglich zur Anzeige zu bringen („Critical Render Path“, „Time to First Meaningful Render“)
* ggf. „Inlining“ geringer Mengen CSS im `<head>` in Betracht ziehen (Optimierung per Cookies-Lösung möglich)
* unkritische Resourcen am Ende des `<body>` einbinden

**Links**

* [loadCSS](https://github.com/filamentgroup/loadCSS) (Filament Group)
* [loadJS](https://github.com/filamentgroup/loadJS) (Filament Group)

# Beispiel

```html
<!DOCTYPE html>

<!-- Hauptsprache des Dokuments -->
<html lang="en">
    <head>
        <!-- Korrekte Zeichenkodierung -->
        <meta charset="utf-8">

        <!-- Viewport-Definition mit zulässigem Pinch-To-Zoom -->
        <meta name="viewport" content="width=device-width, initialscale=1.0">

        <!-- Nicht blockierendes Stylesheet -->
        <link rel="stylesheet" href="main.css" media="none" onload="if(media!='all')media='all'">
        <noscript><link rel="stylesheet" href="main.css"></noscript>

        <!-- Beschreibender Dokumenttitel -->
        <title>Grundlagen barrierefreie Web-Programmierung | Accessibility Club</title>
    </head>
    <body>
        <!-- Kopfbereich und Navigation ... -->

        <!-- Hauptinhalt des Dokuments -->
        <main id="main" role="main">

            <!-- Inhalt -->

        </main>

        <!-- Nicht-blockierendes, nachgelagertes Skript -->
        <script src="scripts.js"></script>
    </body>
</html>
```

[Beispielhafte Dokumentstruktur](https://cdn.rawgit.com/a11yclub/a11y-basics-workshop/master/examples/document.html)