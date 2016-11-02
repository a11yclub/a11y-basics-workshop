# Skip-Link

* Am Anfang des `<body>`, visuell zunächst unsichtbar, als direkter Weg zum `<main>`
* Es profitieren Screenreader und v.a. Tastaturbediener

**Beispiel**

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Grundlagen barrierefreie Web-Programmierung | Accessibility Club</title>
    </head>
    <body>

        <!-- Skip link -->
        <a href="#main">skip to main content</a>

        <!-- Kopfbereich und Navigation ... -->

        <!-- Hauptinhalt des Dokuments -->
        <main id="main" role="main">

            <!-- Inhalt -->

        </main>
    </body>
</html>
```

[Skip-Link](https://cdn.rawgit.com/a11yclub/a11y-basics-workshop/master/examples/navigation.html)

# Naviation per Screenreader

* Navigation per Überschriftenstruktur
* Navigation per Landmarks

**Links**

* [NVDA Tastaturkürzel](http://webaim.org/resources/shortcuts/nvda)